# Changelog

All notable changes to `laravel-livewire-tables` will be documented in this file

## [Unreleased]

## [1.10.0] - 2021-06-20

**This release requires re-publishing of assets.**

### Added

- [Column selector for users to show/hide columns](https://github.com/rappasoft/laravel-livewire-tables/wiki/User-column-selection)
- [Drag & Drop reordering](https://github.com/rappasoft/laravel-livewire-tables/wiki/Drag-and-drop)

## [1.9.0] - 2021-06-15

**This release requires re-publishing of assets.**

### Added

- [Date filters](https://github.com/rappasoft/laravel-livewire-tables/pull/332)

### Changed

- Replaced bootstrap dropdowns with Alpine on bootstrap themes which fixes them closing prematurely when selecting filters.
- Added wrapping divs around needed `if` statements.
- Fixed Bootstrap pagination DOM-diffing issues.

## [1.8.0] - 2021-06-06

### Added

- [Actual default sorting](https://github.com/rappasoft/laravel-livewire-tables/pull/313)
- [Added place to put modals in the scope of the component](https://github.com/rappasoft/laravel-livewire-tables/wiki/Working-with-modals)
- Added `setTableRowClass`, `setTableRowId`, `setTableRowAttributes`, `setTableDataClass`, `setTableDataId`, `setTableDataAttributes` methods to modify cells and rows depending on data for non-custom rows.

### Changed

- [Fix tailwind style for div containing checkbox](https://github.com/rappasoft/laravel-livewire-tables/pull/314)

## [1.7.1] - 2021-05-30

### Added

- [Arabic translation file](https://github.com/rappasoft/laravel-livewire-tables/pull/299)

### Changed

- [Fix select tag className in Bootstrap 5](https://github.com/rappasoft/laravel-livewire-tables/pull/291)

## [1.7.0] - 2021-05-18

### Added

- [Ability to turn off filter dropdown](https://github.com/rappasoft/laravel-livewire-tables/pull/285)

### Changed

- [Fix ambiguous column id when using Relation instead of Builder](https://github.com/rappasoft/laravel-livewire-tables/pull/283)
- [Use column text for sorting and filter pills if no $filterNames or $sortNames exist](https://github.com/rappasoft/laravel-livewire-tables/pull/286)
- [Fix tailwind pagination view](https://github.com/rappasoft/laravel-livewire-tables/pull/284)

## [1.6.1] - 2021-05-13

### Changed

- [Allows to use Relation instead of Builder to generate data](https://github.com/rappasoft/laravel-livewire-tables/pull/279)

## [1.6.0] - 2021-05-04

### Added

- Added Unselect All button on bulk row when selecting page.
- Added disabled delay on select checkboxes.
- Added disabled on bulk row button clicks.
- Added missing showPagination conditional to views.
- Added getFilters and getFiltersWithoutSearch methods and refactor views.
- Added checkFilters method and refactor mountWithFilters
- Added hasIntegerKeys method

### Changed

- When selecting a page, if there are the same selected as total rows, just show the amount of selected instead of showing "Selecting 1 row. Do you want to select all 1 rows.".
- Move bulk select row to its own partial for all templates.
- Moved updatedFilters from WithSearch to WithFilters
- Refactor hasFilter to support numeric keys
- Refactor getFilter to support numeric keys
- Refactor getFilterOptions to support numeric keys

### Removed

- Removed updatingFilters from WithFilters

## [1.5.1] - 2021-05-02

### Added

- Added clear search method.

### Changed

- Changed resetAll method to include search and page and moved to parent component.
- Refactored search method to use new resetSearch.
- [Use custom per page on first load](https://github.com/rappasoft/laravel-livewire-tables/pull/270)

## [1.5.0] - 2021-05-02

### Added

- Added hideIf for columns to hide a column with a conditional, works out of the box for cells not using rowView, if using rowView you must wrap the cells you want to hide in the same conditional. [See documentation](https://github.com/rappasoft/laravel-livewire-tables/wiki/Conditionally-hiding-columns).
- Added selected row de-selector when not selecting full page or all.

## [1.4.0] - 2021-04-29

### Added

- Added option for single column sorting only.
- Ability to change empty message per table.
- Added en.json lang file.
- Ability to add 'All' option to per-page.

### Changed

- Modified views to support localization better where necessary (republish views).
- Alphabetize en.json
- Fixed bulk actions using wrong key to select instead of $primaryKey
- Make bulk select checkbox use primary key

## [1.3.1] - 2021-04-26

### Added

- Use the filter option name instead of the value on the filter pills. (https://github.com/rappasoft/laravel-livewire-tables/pull/238)

### Changed

- Added row count when pagination is disabled. (https://github.com/rappasoft/laravel-livewire-tables/pull/239**)
- Fixed whitespace-nowrap in tailwind cell. (https://github.com/rappasoft/laravel-livewire-tables/issues/240)

### Removed

- Removed old readme for the documentation link.

## [1.3.0] - 2021-04-25

### Added

- Added searchable() to columns (https://github.com/rappasoft/laravel-livewire-tables/pull/233)

### Changed

- Fixed offline indicators to display block.
- Tailwind cool-gray to just gray since it is included by default.

## [1.2.2] - 2021-04-23

### Changed

- Removed hard coded bulk text of **users** and changed to **rows**

## [1.2.1] - 2021-04-22

### Changed

- Remove padding from bootstrap container to keep it flush with sides like Tailwind

## [1.2.0] - 2021-04-22

### Added

- Ability to disable pagination (https://github.com/rappasoft/laravel-livewire-tables/pull/222)
- Ability to define the sorting direction names for each column. i.e. A-Z, Z-A, Yes, No, Enabled, Disabled, etc.
- Added ability to define primary key of rows for bulk select
- Added selectedKeys property that returns an array of the ids of the selected rows

### Changed

- Clarified where rowView looks in read me
- Null the search filter when it's empty
- Fill per page options from $perPageAccepted in views
- Make $perPageAccepted public

### Removed

- Removed `text-secondary` class from sorting title

## [1.1.0] - 2021-04-21

### Added

- Added callback to column's sortable() method to customize sorting functionality per column. (https://github.com/rappasoft/laravel-livewire-tables/pull/216)
- Support for polling `keep-alive` and `visible`.
- Start of a test suite (https://github.com/rappasoft/laravel-livewire-tables/pull/218)

### Changed

- Updated Tailwind search clear button (https://github.com/rappasoft/laravel-livewire-tables/pull/217).
- Updated readme

## [1.0.4] - 2021-04-18

### Added

- `$searchFilterDebounce`, `$searchFilterDefer`, `$searchFilterLazy`, for defining the search input data binding property. https://github.com/rappasoft/laravel-livewire-tables/pull/211
- Remove ability to need to define filters if not defining defaults. https://github.com/rappasoft/laravel-livewire-tables/pull/213

### Changed

- Rearrange wire:keys

## [1.0.3] - 2021-04-18

### Added

- Added Bootstrap 5 theme

### Changed

- Removed calls to custom primary color with indigo for tailwind
- Updated search and row click sections of read me to be more clear.
- Added resetPage to per page dropdown and filters.

## [1.0.2] - 2021-04-17

### Changed

- Fixed checkbox click with row click combination following URL and not checking checkbox.

## [1.0.1] - 2021-04-17

### Changed

- Fixed missing bootstrap components aliased to bs4.table.*
- Updated readme
- Added missing row click on bootstrap

## [1.0.0] - 2021-04-16

- Ground up rebuild, see documentation for usage.

## [0.4.0] - 2021-04-14

### Changed

- Fixed polling issue
- Fixed [MongoDB per page issue](https://github.com/rappasoft/laravel-livewire-tables/pull/107)
- [Fixed use of $clearSearchButtonClass variable](https://github.com/rappasoft/laravel-livewire-tables/pull/118)

## [0.3.3] - 2020-12-13

### Added

- PHP8 Support
- Spanish translations
- German translations
- French translations

### Changed

- Updated Arabic translations

## [0.3.2] - 2020-09-25

### Added

- Added thead class to option array
- Ability to export the list set to CSV/XLS/XLSX/PDF
- Ability to mark a visible column as not to be exported
- Ability to mark a column as export only, which hides it from UI
- Ability to format a single column differently for export as it is for its UI
- Added option to change the button class from the config

## [0.3.1] - 2020-09-18

### Changed

- Fixed non-sortable column headers not getting classes applied.
- Updated documentation

## [0.3] - 2020-09-16

- Ground up rebuild

### Added

- Config file to choose frontend framework - currently limited to bootstrap
- Render method to columns which returns whatever you put into it, you can return a view, html, an attribute, etc.
- Pulled in and modified the HTML component library from laravelcollective so you can return html components from the render method. i.e.: $this->image(...);
- Added new loading config on whether to keep displaying the current data while loading or collapse it
- Added ability to set frontend framework specific options via a property on a per component basis.

### Changed

- Extracted the sorting icons out to their actual HTML, so you can use whatever you want, not limited to the 'i' tag.

### Removed

- Checkbox functionality for now
- Component functionality pending debate
- All class and styling based properties. It's better to publish the views to change something.

## [0.2.1] - 2020-09-10

### Added

- Arabic translations
- Ability to add a link to make table rows clickable
- Added the ability to change the sort icons
- Ability to hide a column based on a condition or permanently

### Updated

- Livewire to 2.x

### Removed

- Removed 1 hard coded font awesome icon

### Changed

- Publish tags to service provider

## [0.2.0] - 2020-08-10

### Added

- Add pagination reset for perPage updates
- Add second parameter to view method for the name of the model variable available in the view.
- Allow publishing of views
- Make docblocks work with psalm
- Added searching method either debounce or lazy
- Allow dot notation for customer attributes
- Added loading message to table body if $loadingIndicator is true
- Add clear button option to search box

### Changed

- Updated Livewire to 1.3
- $disableSearchOnLoading default to false
- Trim the search term when processing
- Added language to publishable translation file

### Removed

- Existing loading subview for tbody message

## [0.1.6] - 2020-06-15

### Changed
- Add second parameter to view method for the name of the model variable available in the view.

## [0.1.5] - 2020-05-26

### Changed

- Use constructor instead of mount so that the child classes have access to a mount method that they can accept parameters in.

## [0.1.4] - 2020-05-24

### Changed

- Changed $models to $builder
- Changed callback parameters for sorting to $builder, $direction. (Removed sortField because we know what it is, until someone gives me an example of why it would be beneficial to keep it).

## [0.1.3] - 2020-05-12

### Changed

- Ability to turn off per page option while keeping pagination on
- Fix the search feature if pagination is on, and you're not searching from the first page using Livewire's native resetPage() method.

## [0.1.2] - 2020-04-28

### Changed

- Fixed pagination text when there are zero results

## [0.1.1] - 2020-04-04

### Changed

- Name of table blade view to avoid issues with other like named packages

## 0.1.0 - 2020-04-03

- Initial release

[Unreleased]: https://github.com/rappasoft/laravel-livewire-tables/compare/v1.10.0...development
[1.10.0]: https://github.com/rappasoft/laravel-livewire-tables/compare/v1.9.0...v1.10.0
[1.9.0]: https://github.com/rappasoft/laravel-livewire-tables/compare/v1.8.0...v1.9.0
[1.8.0]: https://github.com/rappasoft/laravel-livewire-tables/compare/v1.7.1...v1.8.0
[1.7.1]: https://github.com/rappasoft/laravel-livewire-tables/compare/v1.7.0...v1.7.1
[1.7.0]: https://github.com/rappasoft/laravel-livewire-tables/compare/v1.6.1...v1.7.0
[1.6.1]: https://github.com/rappasoft/laravel-livewire-tables/compare/v1.6.0...v1.6.1
[1.6.0]: https://github.com/rappasoft/laravel-livewire-tables/compare/v1.5.1...v1.6.0
[1.5.1]: https://github.com/rappasoft/laravel-livewire-tables/compare/v1.4.0...v1.5.1
[1.5.0]: https://github.com/rappasoft/laravel-livewire-tables/compare/v1.4.0...v1.5.0
[1.4.0]: https://github.com/rappasoft/laravel-livewire-tables/compare/v1.3.1...v1.4.0
[1.3.1]: https://github.com/rappasoft/laravel-livewire-tables/compare/v1.3.0...v1.3.1
[1.3.0]: https://github.com/rappasoft/laravel-livewire-tables/compare/v1.2.2...v1.3.0
[1.2.2]: https://github.com/rappasoft/laravel-livewire-tables/compare/v1.2.1...v1.2.2
[1.2.1]: https://github.com/rappasoft/laravel-livewire-tables/compare/v1.2.0...v1.2.1
[1.2.0]: https://github.com/rappasoft/laravel-livewire-tables/compare/v1.1.0...v1.2.0
[1.1.0]: https://github.com/rappasoft/laravel-livewire-tables/compare/v1.0.4...v1.1.0
[1.0.4]: https://github.com/rappasoft/laravel-livewire-tables/compare/v1.0.3...v1.0.4
[1.0.3]: https://github.com/rappasoft/laravel-livewire-tables/compare/v1.0.2...v1.0.3
[1.0.2]: https://github.com/rappasoft/laravel-livewire-tables/compare/v1.0.1...v1.0.2
[1.0.1]: https://github.com/rappasoft/laravel-livewire-tables/compare/v1.0.0...v1.0.1
[1.0.0]: https://github.com/rappasoft/laravel-livewire-tables/compare/v0.4.0...v1.0.0
[0.4.0]: https://github.com/rappasoft/laravel-livewire-tables/compare/v0.3.3...v0.4.0
[0.3.3]: https://github.com/rappasoft/laravel-livewire-tables/compare/v0.3.2...v0.3.3
[0.3.2]: https://github.com/rappasoft/laravel-livewire-tables/compare/v0.3.1...v0.3.2
[0.3.1]: https://github.com/rappasoft/laravel-livewire-tables/compare/v0.3.0...v0.3.1
[0.3.0]: https://github.com/rappasoft/laravel-livewire-tables/compare/v0.2.1...v0.3.0
[0.2.1]: https://github.com/rappasoft/laravel-livewire-tables/compare/v0.2.0...v0.2.1
[0.2.0]: https://github.com/rappasoft/laravel-livewire-tables/compare/v0.1.6...v0.2.0
[0.1.6]: https://github.com/rappasoft/laravel-livewire-tables/compare/v0.1.5...v0.1.6
[0.1.5]: https://github.com/rappasoft/laravel-livewire-tables/compare/v0.1.4...v0.1.5
[0.1.4]: https://github.com/rappasoft/laravel-livewire-tables/compare/v0.1.3...v0.1.4
[0.1.3]: https://github.com/rappasoft/laravel-livewire-tables/compare/v0.1.2...v0.1.3
[0.1.2]: https://github.com/rappasoft/laravel-livewire-tables/compare/v0.1.1...v0.1.2
[0.1.1]: https://github.com/rappasoft/laravel-livewire-tables/compare/v0.1.0...v0.1.1
