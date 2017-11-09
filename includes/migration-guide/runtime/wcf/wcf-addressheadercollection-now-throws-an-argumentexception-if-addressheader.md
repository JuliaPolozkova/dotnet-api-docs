### WCF AddressHeaderCollection now throws an ArgumentException if an addressHeader element is null

|   |   |
|---|---|
|Details|Starting with the .NET Framework 4.7.1, the <code>M:System.ServiceModel.Channels.AddressHeaderCollection.#ctor(System.Collections.Generic.IEnumerable{System.ServiceModel.Channels.AddressHeader})</code> constructor throws an <code>T:System.ArgumentException</code> if one of the elements is <code>null</code>. In the .NET Framework 4.7 and earlier versions, no exception is thrown.|
|Suggestion|If you encounter compatibility issues with this change on the .NET Framework 4.7.1 or a later version, you can opt-out of it by adding the following line to the <code>&lt;runtime&gt;</code> section of the app.config file::<pre><code>&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceModel.DisableAddressHeaderCollectionValidation=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>|
|Scope|Minor|
|Version|4.7.1|
|Type|Runtime|
|Affected APIs|<ul><li><xref:System.ServiceModel.Channels.AddressHeaderCollection.%23ctor(System.Collections.Generic.IEnumerable%7BSystem.ServiceModel.Channels.AddressHeader%7D)?displayProperty=nameWithType></li></ul>|
