<!-- Keep a Changelog guide -> https://keepachangelog.com -->
# Magento 2 Support by Atwix Changelog

## [Unreleased]

### Added

- [Paid] Navigation support from event usage to its dispatching
- Navigation support from event dispatching to its usages in events.xml files

### Changed

- Added the last fetched date and time for URNs mapping status
- Added support for the catalog_attributes.xml file in the Magento 2 Configuration File action.

### Fixed

- Fixed NoClassDefFoundError: LocalHistoryImpl in OldestHistorySnapshotManager:33
- Fixed PSI can be created only for a file with LanguageFileType but actual is class DetectedByContentFileType in TranslationIndex:32

## [2024.2.0] - 2024-08-16

### Added

- [Paid] Action to generate a `_module.less` file for the module
- [Paid] Action for extending 3rd party module styles within custom themes using the `_extend.less` file
- Navigation support from PHP classes to its usages in XML files
- Inspection for detecting missing Magento 2 URN mapping for XSD schema within XML files and quick fix

### Changed

- Added support for Mage-OS
- Updated the minimum supported version to PHPStorm 2024.2
- Removed the action for running code refactoring with ChatGPT (recommended to use the official AI Assistant from JetBrains)
- Removed the ChatGPT widget in favor of the official AI Assistant from JetBrains

### Fixed

- Added support for PHPStorm 2024.2

## [2024.1.4] - 2024-06-11

### Added

- [Paid] Navigation support for referencing JavaScript files using relative paths defined in `requirejs-config.js` [RequireJS]
- [Paid] Navigation support for referencing JavaScript files through relative paths specified in the `define` function arguments [RequireJS]
- [Paid] Navigation support for referencing JavaScript files via relative paths outlined in the `require` function arguments in PHTML files [RequireJS]
- [Paid] Navigation support for referencing HTML templates using relative paths defined in requirejs-config.js [RequireJS, typically used for template overrides]
- [Paid] Navigation support for referencing HTML templates through relative paths specified in the define function arguments [RequireJS, commonly used with the !text plugin]
- Navigation support from observer class to its declaration
- Completion support for Magento component names within the `require` section of the composer.json file

### Changed

- Added disabled plugins to navigation from plugin implementation to its declaration
- Implemented auto-detection for the default directory of git patches in the git patch generation dialog
- Enhanced navigation from UI components JavaScript files to their associated template files and vice versa
- Enhanced completion support for ACL resource IDs in the `aclResource` attribute of `<block>` tags (layouts), the `aclResource` tag in UI components declaration files, and the `resource` attribute in `menu.xml` files
- Enhanced navigation support from ACL resource ID usages to their declarations, including `menu.xml`, `webapi.xml`, `extension_attributes.xml`, `system.xml`, layouts, and UI component layout files

### Fixed

- Prevented the completion popup from closing when the `:` character is entered while completing ACL resource IDs

## [2024.1.3] - 2024-05-16

### Added

- [Paid] Action to generate a page configuration layout update from a module
- [Paid] Action to generate a page configuration layout update from a target layout XML file
- Action to override a PHTML template in a theme
- Action to override a PHTML template in a module
- Action to override a page layout in a theme
- Action to override an email template in a theme
- Action to override a JS template in a theme
- Action to override a JS template in a module
- Navigation support from ACL resource id usages to its declaration

### Changed

- Included module name in the navigatable presentation section of the "Navigate to Usages" (phtml usages) popup
- [CLI Commands] Implemented parsing of a command name when provided as a default value for the `$name` constructor parameter
- [CLI Commands] Implemented parsing of command name and description when provided as default values for the `$defaultName` and `$defaultDescription` properties

## [2024.1.2] - 2024-04-15

### Added

- [Paid] Navigation support from UI component template usages in UI component JavaScript files to their corresponding template files
- [Paid] Navigation support from UI component templates to their usages in JavaScript UI component files
- Action for generating a Magento observer for an event
- Inspection to identify violations of the PHPMD.UnusedFormalParameter rule in Magento 2 plugins, quick fix to suppress it
- Navigation support for navigating from di.xml argument configurations to corresponding PHP class constructor parameters in types and virtual types

### Changed

- Navigation support from pluginized JavaScript files to JavaScript Mixins now includes searching for mixins declared in themes

### Fixed

- The generated plugin file now includes the `Plugin` suffix in its name automatically (plugin generation)
- Plugin class names can no longer be generated from lowercase letters (plugin generation)

## [2024.1.1] - 2024-03-18

### Added

- [Paid] Added functionality for running/debugging Magento CLI commands directly next to the command class name
- [Paid] Automatic/manual generation of URNs schema with status tracking
- [Paid] Navigation support from pluginized JavaScript files to JavaScript Mixins
- Navigation support from JavaScript Mixin implementation to its declaration
- Navigation support from JavaScript Mixin to pluginized JavaScript files
- Intention support for adding CDATA to the empty comment tag in the system.xml file
- Implemented an implicit usage provider for the controller class (and execute method) to prevent highlighting as unused elements
- Implemented an implicit usage provider for the plugin class (and its methods) to prevent highlighting as unused elements
- Implemented an implicit usage provider for the observer class (and execute method) to prevent highlighting as unused elements

### Changed

- Improved user experience for selecting module dependencies during the creation of a new Magento 2 module

### Fixed

- Fixed cannot generate plugin for another plugin method
- Fixed Do not perform a synchronous refresh under read lock (MagentoProjectUtil:78)
- Fixed patch generator compatibility issue with OS Windows

## [2024.1.0] - 2024-02-26

### Added

- [Paid] Action to generate a git patch for an individual vendor file based on its changes before executing the action
- [Paid] Completion support for various elements in the di.xml file
- [Paid] Completion support for various elements in the communication.xml, queue_consumer.xml, queue_publisher.xml, and queue_topology.xml files
- [Paid] Completion support for various elements in the webapi.xml file
- Completion support for various elements in the extension_attributes.xml file
- Completion support for various elements in the indexer.xml and mview.xml files
- Completion support for various elements in the events.xml file
- Completion support for various elements in the db_schema.xml file
- Completion support for various elements in the routes.xml file
- Completion support for various elements in the acl.xml file
- Completion support for various elements in the system.xml file
- Completion support for various elements in the module.xml file

### Changed

- Enhanced performance for the Magento CLI Run Configuration settings panel when opening
- Added a context menu action in the Git Patches Viewer tree to open files in the editor

### Fixed

- Resolved issues related to read access being allowed from inside read-action for various actions
- Fixed slow operations are prohibited on EDT for MyIsam engine usage inspection
- Fixed PSI element is provided on EDT by ListPopupImpl for dependency on implementation details quick fix

## [2023.5.3] - 2023-12-13

### Added

- [Paid] Action to view codebase changes for a given patch file (individual patch viewer)
- [Paid] Action to break at first line of Magento plugins (configurable)
- [Paid] Action to break at first line of Magento observers (configurable)
- Added core contribution project support (source code is a Magento itself)
- Navigation support from plugin implementation to its declaration
- Navigation support from plugin to intercepted method
- Navigation support from intercepted method to plugins
- Inspection for detecting non-existent class declaration in 'for' attribute of the 'extension_attributes' tag inside the extension_attributes.xml file

### Changed

- [Paid] Added debugging support for Magento CLI Run Configuration
- Added multiple results for navigation from WEB API service method to its declarations
- Added quick navigation to the plugin configurable from the Magento Support main menu
- Updated the minimum supported version to PHPStorm 2023.3

### Fixed

- Fixed IllegalArgumentException: Argument for @NotNull parameter must not be null at TemplateReferenceProvider:87
- Fixed Assertion failed: Do not use PsiElement for popup model. See PsiTargetNavigator (navigation to layouts from controller)
- Fixed Slow operations are prohibited on EDT for UpdatePlatformVersionService:23

## [2023.5.2] - 2023-10-30

### Added

- [Paid] Action to search WEB API service by its URL
- [Paid] Intentions support for most commonly used XML configuration files (di.xml, events.xml, routes.xml, and more)
- Navigation support from WEB API declaration to WEB API service and vice versa
- Action to copy path for Magento assets (supported asset types include: phtml templates, html templates, JavaScript files, CSS files, and images)
- Inspection for detecting non-existent class/method declaration in webapi.xml file

### Changed

- Updated the minimum supported version to PHPStorm 2023.2
- Copyright injection support for JS files (copyright module must be configured)
- Added menu.xml file generation to the module configuration files generation action

### Fixed

- Fixed UnsupportedOperationException at Method getParent is not yet implemented in I18nReference$wrapPhraseInElement
- Fixed Assertion failed starting at PluginCyclicCallLoopInspection.findWrappedMethodCalls:97

## [2023.5.1] - 2023-09-30

### Added

- [Paid] Action for generating a Magento JavaScript mixin (for modules)
- Action for generating Magento before/after/around plugins under [Code | Generate](https://www.jetbrains.com/help/phpstorm/generating-code.html)
- Action to manually refreshing the Magento version in settings
- Reference navigation for custom (not overridden) templates in the custom themes

### Changed

- Updated the minimum supported version to PHPStorm 2023.1

### Fixed

- Fixed an issue where the Magento version in settings was not updated after a Magento upgrade; now, the update happens automatically during project startup

## [2023.5.0] - 2023-07-04

### Added

- [Paid] Action for viewing quality patches (QPT) for Magento installation
- [Paid] Inspection for detecting missed variables in @vars comment block for email templates and quick fix
- [Paid] Action for comparing overridden template with the source in Hyva compatibility module
- [Paid] Action for showing/navigation to template overrides in Hyva compatibility module
- Multiple module configuration files generation action
- Collapsing for phrases that translated in dictionaries for PHP files
- Collapsing for phrases that translated in dictionaries for JavaScript files
- Collapsing for phrases that translated in dictionaries for <!-- ko i18n: 'XXX'--><!-- /ko --> syntax in HTML files

### Changed

- Reference to the translation line when using corresponding i18n reference navigation

### Fixed

- Fixed ChatGPT widget infinite login page

## [2023.4.0] - 2023-05-19

### Added

- [Paid] Inspection for detecting usage of non InnoDB storage engines
- [Paid] Inspection for detecting legacy objects injecting within email templates
- Navigation support from used i18n string literals to declaration file(s) in PHP files
- Navigation support from used i18n string literals to declaration file(s) in email templates (HTML files)
- Navigation support from used i18n string literals to declaration file(s) in ui components templates (HTML files)
- Navigation support from used i18n string literals to declaration file(s) in JavaScript files
- Highlighting as JSON for text/x-magento-init script syntax

### Changed

- Made ChatGPT widget integration into IDE Tool Window feature free

### Fixed

- Fixed reentrant indexing at MagentoTestSourceVerifier:143 [#23](https://github.com/Atwix/phpstorm-plugin-feedback/issues/23)
- Fixed ConcurrentModificationException at ControllerListService.kt:24 [#28](https://github.com/Atwix/phpstorm-plugin-feedback/issues/28)
- Fixed ConcurrentModificationException in UiComponentLibService.kt:46 [#25](https://github.com/Atwix/phpstorm-plugin-feedback/issues/25)
- Fixed failed to build index `ModuleIndex` for file `file:lib/internal/.../registration.php` [#24](https://github.com/Atwix/phpstorm-plugin-feedback/issues/24)
- Fixed InvalidPathException while resolving JavaScript file by path [#26](https://github.com/Atwix/phpstorm-plugin-feedback/issues/26)
- Fixed ArrayIndexOutOfBoundsException in UiComponentLibService:134 [#22](https://github.com/Atwix/phpstorm-plugin-feedback/issues/22)

## [2023.3.0] - 2023-04-10

### Added

- [Paid] Action for running code refactoring with ChatGPT
- [Paid] Core JavaScript UiComponents library (list) view and navigation
- [Paid] Completion support for JavaScript widgets names
- [Paid] Completion support for JavaScript UiComponents names
- [Paid] Navigation support for JS Widget (from usage to implementation)
- [Paid] Navigation support for UiComponent (from usage to implementation)
- [Paid] Navigation support for JS Files (from usage in js module dependencies to implementation)
- Action for showing/navigation to layouts where corresponding template is used
- Action for comparing overridden by preference PHP file with original
- Navigation support from layout to controller and vice versa

### Fixed

- Fixed failed to build index: [#20](https://github.com/Atwix/phpstorm-plugin-feedback/issues/20)

## [2023.2.1] - 2023-03-22

### Fixed

- Fixed a compatibility issue with OS Windows

## [2023.2.0] - 2023-03-06

### Added

- [Paid] Integrated ChatGPT widget into IDE Tool Window
- [Paid] Action for comparing overridden JavaScript file with original
- [Paid] Action for comparing overridden HTML template file with original
- [Paid] Action for comparing overridden email template file with original
- [Paid] Action for comparing overridden layout file with original
- Navigation support for phtml templates inside layout files and blocks
- Completion support for phtml template names inside layout files and blocks

### Changed

- [Paid] It is possible to access templates comparison action from the context menu in the Project tool window
- [Paid] It is possible to access navigate to the template overrides action from the context menu in the Project tool window

### Fixed

- Fixed PsiInvalidElementAccessException: Element class CompositeElement of type CLASS (class PhpClassElementType) in PhpClassEditUtil.kt:62

## [2023.1.0] - 2023-02-10

### Added

- [Paid] Added action to search controller by its path
- [Paid] Added inspection for detecting circular dependencies
- Added controller path/info above its class via code vision for project files
- Added controller path/info for class via line marker for vendor files
- Added action to generate new controller

## [2022.2.1] - 2022-12-28

### Changed

- Updated plugin name
- Improved plugin description

## [2022.2.0] - 2022-12-26

### Added

- [Paid] Possibility to execute Magento CLI commands via Run Configuration
- [Paid] Validation for GIT commit that requires modules to be registered in `etc/config.php` file
- [Paid] Local composer paths support (custom source code roots)
- Action for a new Magento 2 module/theme generation
- Auto-detection for installation path and local composer paths
- Navigation support for PHP classes in XML files
- Navigation support for Factory and Proxy classes in XML files
- Navigation support for module name in config.php file
- Navigation support for module name in module.xml (module dependencies under sequence tag)
- Typed properties support for the `dependency on implementation details` quick fix

### Changed

- [Paid] Added possibility to compare overridden `*.phtml` template with the parent theme override
- [Paid] It is possible to inject the original class if needed for the `dependency on implementation detail` quick fix
- [Paid] Removed the `dependency on implementation details` inspection highlighting for classes required by parent constructor
- [Paid] Added possibility to detect unspecified module dependencies in the XML files
- Copyright injection support for PHP and XML files (copyright module must be configured)
- Updated plugin logo

### Fixed

- [Paid] Fixed slow usages search for the `dependency on implementation details` quick fix
- Fixed "Read access is allowed from inside read-action (or EDT) only" - while running on-demand inspections with the disabled `Include test sources` flag

## [2022.1.1] - 2022-12-05

### Added

- [Paid] Action for comparing overridden block template (in the theme or module) with the source template
- [Paid] Action for showing/navigation to template overrides
- [Paid] Inspection for detecting possible dependencies on implementation details and quick fix
- [Paid] Inspection for detecting a used code inconsistency with the specified module dependencies and quick fix
- Inspection for detecting objects instantiation via ObjectManger instance and quick fix
- Inspection for detecting a session usage without a Proxy declaration (lazy loading) and quick fix
- Inspection for detecting wrong Proxy (lazy loading) declaration and quick fix
- Inspection for detecting cyclical event loops in observers
- Inspection for detecting cyclical call loops in plugins
- Inspection for detecting business logic in observer classes
- Inspection for detecting preferences declared in the non-global areas and quick fix
- Inspection for detecting observers registration in the global area and quick fix
- Inspection for detecting helper classes creation
- Test source filter for recognising test classes in the project tree and other IDE areas
- Error reporter to allow users report critical issues from IDE
