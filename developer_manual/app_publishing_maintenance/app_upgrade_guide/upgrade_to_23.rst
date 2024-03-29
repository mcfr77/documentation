=======================
Upgrade to Nextcloud 23
=======================

.. note:: Critical changes were collected `on GitHub <https://github.com/nextcloud/server/issues/27846>`__. See the original ticket for links to the pull requests and tickets.

Back-end changes
----------------

Changed APIs
^^^^^^^^^^^^

* ``\OCP\User\Events\UserLoggedInEvent::getPassword`` is now nullable because logins are possible without a password in SSO setups

Deprecated APIs
^^^^^^^^^^^^^^^

* ``\OCP\Calendar\IManager::search``: use :ref:`the new calendar search API<calendar-search>`
* ``\OCP\Calendar\IManager::isEnabled``: there is no replacement
* ``\OCP\Calendar\IManager::registerCalendar``: use :ref:`calendar providers<calendar-providers>`
* ``\OCP\Calendar\IManager::unregisterCalendar`` there is no replacement
* ``\OCP\Calendar\IManager::register``: use :ref:`calendar providers<calendar-providers>`
* ``\OCP\Calendar\IManager::getCalendars``: use :ref:`the new calendar API<calendar-access>`
* ``\OCP\Calendar\IManager::clear``: there is no replacement

