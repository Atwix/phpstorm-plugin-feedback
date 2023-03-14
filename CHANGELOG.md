<!-- Keep a Changelog guide -> https://keepachangelog.com -->
# Magento and Adobe Commerce PhpStorm by Atwix Changelog

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

- [Freemium] Added action to search controller by its path
- [Freemium] Added inspection for detecting circular dependencies
- Added controller path/info above its class via code vision for project files
- Added controller path/info for class via line marker for vendor files 
- Added action to generate new controller

## [2022.2.1] - 2022-12-28

### Changed

- Updated plugin name
- Improved plugin description

## [2022.2.0] - 2022-12-26

### Added

- [Freemium] Possibility to execute Magento CLI commands via Run Configuration
- [Freemium] Validation for GIT commit that requires modules to be registered in `etc/config.php` file
- [Freemium] Local composer paths support (custom source code roots)
- Action for a new Magento 2 module/theme generation
- Auto-detection for installation path and local composer paths
- Navigation support for PHP classes in XML files
- Navigation support for Factory and Proxy classes in XML files
- Navigation support for module name in config.php file
- Navigation support for module name in module.xml (module dependencies under sequence tag)
- Typed properties support for the `dependency on implementation details` quick fix

### Changed

- [Freemium] Added possibility to compare overridden `*.phtml` template with the parent theme override
- [Freemium] It is possible to inject the original class if needed for the `dependency on implementation detail` quick fix
- [Freemium] Removed the `dependency on implementation details` inspection highlighting for classes required by parent constructor
- [Freemium] Added possibility to detect unspecified module dependencies in the XML files
- Copyright injection support for PHP and XML files (copyright module must be configured)
- Updated plugin logo

### Fixed

- [Freemium] Fixed slow usages search for the `dependency on implementation details` quick fix
- Fixed "Read access is allowed from inside read-action (or EDT) only" - while running on-demand inspections with the disabled `Include test sources` flag 

## [2022.1.1] - 2022-12-05

### Added

- [Freemium] Action for comparing overridden block template (in the theme or module) with the source template
- [Freemium] Action for showing/navigation to template overrides
- [Freemium] Inspection for detecting possible dependencies on implementation details and quick fix
- [Freemium] Inspection for detecting a used code inconsistency with the specified module dependencies and quick fix
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
