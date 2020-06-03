---
default: 'contains'
acceptValues: 'contains' | 'startswith'
type: String
---
---
##### shortDescription
Specifies whether the widget finds entries that contain your search string or entries that only start with it.

---
When using the widget as an [ASP.NET MVC Control](/concepts/35%20ASP.NET%20MVC%20Controls/20%20Fundamentals '/Documentation/Guide/ASP.NET_MVC_Controls/Fundamentals/'), specify this option using the `CollectionSearchMode` enum. This enum accepts the following values: `Contains` and `StartsWith`.