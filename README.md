# MacPEnumHelpers
A simple Library where I'll keep all enum helper methods I use throughout my apps.
<hr/>
The <i>GetEnumDisplayName</i> takes an enum value and returns the declared display name.

<b>Usage:</b>
<ul>
  <li>Decorate the enum value using the [Display()] attribute DataAnnotations method from System.ComponentModel.DataAnnotations</li>
  <li>Call the method passing the specific enum => EnumHelper.GetEnumDisplayName(someEnum)</li>
</ul>
<b>Sample code:</b>

    //Declare the enum
    public enum myColours : int //or any other type that makes sense for the app
    {
        [Display(Name = "Bright Red")]
        brightRed = 0,
        [Display(Name = "Sky Blue")]
        skyBlue
    }

    //Get an enum value display name
    string valueName = EnumHelper.GetEnumDisplayName(brightRed);
    //The string valueName will be assigned "Bright Red"
