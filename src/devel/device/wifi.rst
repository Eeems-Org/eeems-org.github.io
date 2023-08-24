====
Wifi
====

.. raw:: html

    <div class="warning">
        ⚠️ FIXME. ⚠️

This page is just a stub that needs to be completed. You can `open a PR on the repo <https://github.com/toltec-dev/toltec>`_ to add more content to the page.

.. raw:: html

    </div>

https://web.archive.org/web/20230129155419/https://remarkablewiki.com/tips/wifi

Xochitl Network Settings
------------------------

.. code-block:: c++

  QSettings settings("/home/root/.config/remarkable/xochitl.conf");
  settings.sync();
  settings.beginGroup("wifinetworks");
  QMap<QString, QVariantMap> wifinetworks;
  for(const QString& key : allKeys()){
      QVariantMap network = settings.value(key).toMap();
      wifinetworks[key] = network;
  }
  settings.endGroup();

DBus communication with wpa_supplicant
--------------------------------------
