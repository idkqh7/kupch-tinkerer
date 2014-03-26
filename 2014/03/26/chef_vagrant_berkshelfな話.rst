Chef+Vagrant+Berkshelfな話
========================

題名の通り、Chef+Vagrant+BerkshelfのBest Practice的なものを考える。

.. code-block:: bash

    berks cookbook COOKBOOK-NAME
    cd COOKBOOK-NAME
    vim Berksfile（スクリプトの修正）
    berks vendor cookbooks
    vim Vagrantfile（スクリプトの修正）


この後 vagrant upを適用することになるが、
面倒臭い。

というわけでさっくりスクリプト書く。

https://github.com/idkqh7/BuildForge

.. code-block:: bash

    bforge init mycookbook
    cd mycookbook
    bforge install apt git nginx
    vagrant up
    
みたいな感じで使えます。
(※OSはdebian)


.. author:: default
.. categories:: none
.. tags:: none
.. comments::
