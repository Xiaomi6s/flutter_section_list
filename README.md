# flutter_section_list

a list and grid support section like iOS，header pinned，item staggered.



## Getting Started

### List

```
class SectionListDemo extends StatelessWidget with SectionAdapterMixin{

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(title: Text('SectionListDemo'),),
      body: SectionListView.builder(adapter: this),
    );
  }

  @override
  int numberOfSections() {
    return 10;
  }

  @override
  int numberOfItems(int section) {
    return 15;
  }

  @override
  Widget getItem(BuildContext context, IndexPath indexPath) {
    ...
  }

  @override
  bool shouldExistSectionHeader(int section) {
    return true;
  }

  @override
  bool shouldSectionHeaderStick(int section) {
    return true;
  }

  @override
  bool shouldExistSectionFooter(int section) {
    return false;
  }

  @override
  Widget getSectionHeader(BuildContext context, int section) {
    ...
  }

  @override
  Widget getSectionFooter(BuildContext context, int section) {
    ...
  }
}
```

### Grid

```
class _SectionGridViewWidget extends StatelessWidget with SectionAdapterMixin, SectionGridAdapterMixin {

  @override
  Widget build(BuildContext context) {

    return Scaffold(
      appBar: AppBar(
        title: Text("SectionGridView"),
      ),
      body: SectionGridView.builder(adapter: this),
    );
  }

  @override
  Widget getItem(BuildContext context, IndexPath indexPath) {
    ...
  }

  @override
  int numberOfItems(int section) {
    return 10;
  }

  @override
  int numberOfSections() {
    return 10;
  }

  @override
  double getMainAxisSpacing(int section) {
    return 5;
  }

  @override
  double getCrossAxisSpacing(int section) {
    return 5;
  }

  @override
  EdgeInsets getSectionInsets(int section) {
    return EdgeInsets.fromLTRB(10, 8, 10, 8);
  }

  @override
  bool shouldExistSectionHeader(int section) {
    return true;
  }

  @override
  bool shouldSectionHeaderStick(int section) {
    return true;
  }

  @override
  bool shouldExistSectionFooter(int section) {
    return false;
  }

  @override
  double getFooterItemSpacing(int section) {
    return 5;
  }

  @override
  double getHeaderItemSpacing(int section) {
    return 5;
  }

  @override
  Widget getSectionHeader(BuildContext context, int section) {
    ...
  }

  @override
  Widget getSectionFooter(BuildContext context, int section) {
    ...
  }
}
```
