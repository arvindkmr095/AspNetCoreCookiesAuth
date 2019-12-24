<?xml version="1.0" encoding="utf-8"?>
<!-- For more information on how to configure your ASP.NET application, please visit http://go.microsoft.com/fwlink/?LinkId=169433 -->
<configuration>
  <configSections>
    <!-- For more information on Entity Framework configuration, visit http://go.microsoft.com/fwlink/?LinkID=237468 -->
    <section name="entityFramework" type="System.Data.Entity.Internal.ConfigFile.EntityFrameworkSection, EntityFramework, Version=6.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089" requirePermission="false" />
    <section name="dataCacheClient" type="Microsoft.ApplicationServer.Caching.DataCacheClientSection, Microsoft.ApplicationServer.Caching.Core, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35" allowLocation="true" allowDefinition="Everywhere" />
    <section name="submissionConfiguration" type="Accenture.eFaxInterface.EFaxConfigurationSectionHandler, Accenture.eFaxInterface, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null" allowLocation="true" allowDefinition="Everywhere" />
    <sectionGroup name="dotNetOpenAuth" type="DotNetOpenAuth.Configuration.DotNetOpenAuthSection, DotNetOpenAuth.Core">
      <section name="messaging" type="DotNetOpenAuth.Configuration.MessagingElement, DotNetOpenAuth.Core" requirePermission="false" allowLocation="true" />
      <section name="reporting" type="DotNetOpenAuth.Configuration.ReportingElement, DotNetOpenAuth.Core" requirePermission="false" allowLocation="true" />
      <section name="oauth" type="DotNetOpenAuth.Configuration.OAuthElement, DotNetOpenAuth.OAuth" requirePermission="false" allowLocation="true" />
      <section name="openid" type="DotNetOpenAuth.Configuration.OpenIdElement, DotNetOpenAuth.OpenId" requirePermission="false" allowLocation="true" />
    </sectionGroup>
  </configSections>
  <connectionStrings>
    <add name="CrmServiceConfig" connectionString="Url=http://10.171.3.15/ProviewSIT3; Domain=CAQH; Username=svc_crmportalqa; Password=hhlk$%78GVK" />
    <add name="CAQHUPDCRMConn" connectionString="Server=10.171.3.15;Database=CAQHUPDCRM_SIT3;User Id=dev;Password=P@ssw0rd1;MultipleActiveResultSets=True" providerName="System.Data.SqlClient" />
    <add name="ADLDSConn" connectionString="LDAP://INFCAQAD0007:50004/CN=Roles,CN=TestPartition1,DC=CAQH-LDS,DC=LOCAL" />
    <add name="DMSConnection" connectionString="Server=10.171.3.15; Database=UPDDocumentManagement_SIT3; user Id=filestream;Password=FIle@Stream13;MultipleActiveResultSets=True" providerName="System.Data.SqlClient" />
    <add name="HistoryViewerContext" connectionString="Data Source=INFCAQAT0004;Initial Catalog=CAQHCentral_UAT;User Id=History_Viewer;Password=P@ssw0rd1;" providerName="System.Data.SqlClient" />
    <add name="HistoryViewer" connectionString="Data Source=INFCAQAT0004;Initial Catalog=CAQHCentral_UAT;User Id=History_Viewer;Password=P@ssw0rd1;" providerName="System.Data.SqlClient" />
    <!-- CAQH Portal SQL Server DB Context -->
    <add name="CAQHPortalContext" connectionString="Server=10.171.3.15;Database=CAQHUPDPortal_SIT3;User Id=dev;Password=P@ssw0rd1;" providerName="System.Data.SqlClient" />
    <add name="ProviderChangeIntegrationContext" connectionString="Server=10.171.3.15;Database=CAQH_Integration_SIT3;User Id=dev;Password=P@ssw0rd1;MultipleActiveResultSets=True" providerName="System.Data.SqlClient" />
    <add name="FileUploadInfoContext" connectionString="Server=10.171.3.15;Database=CAQH_Integration_SIT3;User Id=dev;Password=P@ssw0rd1;MultipleActiveResultSets=True" providerName="System.Data.SqlClient" />
    <add name="DirectoryAssureContext" connectionString="Server=10.171.3.15;Database=CAQH_DirectoryAssure_SIT3;User Id=dev;Password=P@ssw0rd1;MultipleActiveResultSets=True" providerName="System.Data.SqlClient" />
  </connectionStrings>
  <appSettings>
    <add key="SQLCommandTimeOut" value="300" />
    <add key="CAQHOutPutFile" value="C:\Test\PDF\" />
    <add key="webpages:Version" value="3.0.0.0" />
    <add key="webpages:Enabled" value="false" />
    <add key="PreserveLoginUrl" value="true" />
    <add key="ClientValidationEnabled" value="true" />
    <add key="UnobtrusiveJavaScriptEnabled" value="true" />
    <add key="EmailsEnabled" value="true" />
    <add key="CacheManagerEnabled" value="false" />
    <add key="BuildVersion" value="Feb2020 Release B15 (.23)" />
    <add key="EnableProfileMigration" value="true" />
    <add key="InitiateCacheOnStartup" value="true" />
    <add key="EnableGoogleAnalytics" value="false" />
    <add key="DisablePageCache" value="true" />
    <add key="PORegistrationURL" value="http://INFCAQWD0017/HistoryViewer/PO/Registration/Index?contactId={0}" />
    <!-- Replica Service Url -->
    <add key="ReplicaServiceURL" value="http://INFCAQAT0022:802/PDFGenerator/" />
    <add key="DAAPIURL" value="http://INFCAQAT0022:802/DAPracticeLocationsAzureAPI/" />
    <add key="IsAPICall" value="false" />
    <!--ADLDS keys-->
    <add key="ADLDSUsername" value="CN=admin,CN=Roles,CN=TestPartition1,DC=CAQH-LDS,DC=LOCAL" />
    <add key="ADLDSServer" value="INFCAQAD0007" />
    <add key="ADLDSPassword" value="P@ssw0rd" />
    <add key="ADLDSPort" value="50004" />
    <add key="ADLDSPartitionName" value="TestPartition1,DC=CAQH-LDS,DC=LOCAL" />
    <add key="ADLDSEnableSSL" value="false" />
    <add key="ADALoginURL" value="https://test.ebusiness.ada.org/login/loginCAQH.aspx?PO3ORGAPICODE=CAQHPRW89798928" />
    <!-- History Viewer-->
    <add key="HVDataProvider" value="System.Data.SqlClient" />
    <add key="PhysicalPath" value="\\infcaqad0006\XeroxData\caqhroot\ProviderDocs\" />
    <add key="CAQHKeyPrefix" value="00" />
    <add key="CAQHKeySuffix" value="000" />
    <add key="CAQHID" value="0010371000" />
    <add key="AttachamentPath" value="Attachments" />
    <add key="GoLiveDate" value="09/10/2014" />
    <add key="TestProviderID" value="11505426" />
    <add key="EnableTestProviderID" value="false" />
    <!-- B2B File Uploads-->
    <add key="Rosterftppath" value="\\INFCAQWD0003\B2BServices_FTP_Test\SIT3_FTP\RosterImport\" />
    <add key="SimpleRosterftppath" value="\\INFCAQWD0003\B2BServices_FTP_Test\SIT3_FTP\PSVSimpleRosterImport\" />
    <add key="EnhancedRosterftppath" value="\\INFCAQWD0003\B2BServices_FTP_Test\SIT3_FTP\PSVEnhancedRosterImport\" />
    <add key="Sanctionftppath" value="\\INFCAQWD0003\B2BServices_FTP_Test\SIT3_FTP\SanctionImport\" />
    <add key="BulkUploadFtpPath" value="\\INFCAQWD0003\B2BServices_FTP_Test\SIT3_FTP\BulkUploadImport\" />
    <add key="BulkUploadTempPath" value="C:\Miscellaneous\BulkUpload\BulkUploadTemp\" />
    <!-- AL Ignore PropertyList-->
    <add key="ALIgnorePropertyList" value="Question,ProviderID" />
    <!--DOO PDF Keys-->
    <add key="PDFInputPath" value="C:\SIT3\Replica\Input\" />
    <add key="PDFOutputPath" value="C:\SIT3\Replica\Output\" />
    <add key="ProviderReplicaOutputPath" value="C:\SIT3\Replica\Portal_Generated\" />
    <!--Encryption Key-->
    <add key="EncryptionKey" value="Rolling Stones" />
    <!-- Enforce Provider Validations for Attestation -->
    <add key="EnforceProviderValidations" value="true" />
    <!-- External Validations -->
    <!--<add key="EnableExternalValidation" value="false" />-->
    <!--As part of WO0102-->
    <add key="EnableTINValidation" value="false" />
    <add key="EnableNPIValidation" value="true" />
    <add key="EnableDEAValidation" value="false" />
    <add key="EnableAddressValidation" value="true" />
    <!-- USPS -->
    <add key="USPSBaseUrl" value="http://production.shippingapis.com/ShippingAPI.dll" />
    <add key="USPSUserID" value="263CAQH04218" />
    <!-- NPI -->
    <add key="NPISecurityToken" value="84620F8877CA4EA8B809C8E606174A72F623951A62C541AAA9BB193A329122F4" />
    <!-- DEA -->
    <add key="DEAUsername" value="1619352" />
    <add key="DEAPassword" value="changeme" />
    <!-- TIN -->
    <add key="TINUsername" value="tincheck7@mailinator.com" />
    <add key="TINPassword" value="tincheck7@mailinator.com" />
    <add key="TINCAQHMailID" value="tincheck2@mailinator.com" />
    <add key="APICode" value="CAQH007T3T1T371" />
    <add key="LearnMoreLink" value="https://www.caqh.org/sites/default/files/solutions/proview/ada/dentist-quick-reference-guide.pdf" />
    <add key="ADAorg" value="http://www.ada.org/attestationlogin" />
    <!--TINCaching TimeSpan-->
    <add key="TINCachingTimeSpan" value="3" />
    <!-- BPO DMS Configurations -->
    <!--<add key="ClientID" value="CAQHDoc"/>
		<add key="DecryptionKey" value="O1zM$-wG#5mL3F~q"/>
		<add key="RetrievalServiceURL" value="https://dvstaging-edmservices.accenture.com/DocViewer/DocServ.svc/?get="/>
		<add key="ID" value="bsstest\v.bojja"/>
		<add key="PASSWORD" value="Start5544!"/>-->
    <add key="ClientID" value="CAQHDoc" />
    <add key="DecryptionKey" value="O1zM$-wG#5mL3F~q" />
    <add key="RetrievalServiceURL" value="https://ddservices-uat.accenture.com/DocViewer/DocServ.svc/?get=" />
    <add key="ID" value="bsstest\v.bojja" />
    <add key="PASSWORD" value="Start5544!" />
    <add key="BESuccessResponse" value="Request Received Successfully !!" />
    <add key="UploadClientID" value="CAQHDoc" />
    <add key="UploadDecryptionKey" value="O1zM$-wG#5mL3F~q" />
    <add key="UploadServiceURL" value="https://dduploadservices-uat.accenture.com/FileStoreDocStorage/StorageService.svc?wsdl" />
    <add key="UploadUserID" value="svc-ia-test" />
    <add key="UploadPASSWORD" value="X8m#qEtbv68sVYc" />
    <!-- Sanction download -->
    <add key="SanctionHistoryPath" value="\\infcaqad0006\XeroxData\" />
    <!-- Fileshare -->
    <add key="FileShareDomain" value="CAQH" />
    <add key="FileShareUserName" value="svc_b2b" />
    <add key="FileSharePassword" value="Pr0d@BtoB3!" />
    <!-- Beta Portal -->
    <add key="EnableBetaPortal" value="false" />
    <add key="IsBetaPortal" value="false" />
    <add key="BetaPortalUrl" value="http://INFCAQAT0022:802/beta/" />
    <add key="PortalUrl" value="http://INFCAQAT0022:802/" />
    <!-- Groups Portal -->
    <add key="EnableGroups" value="true" />
    <add key="GroupsPOPortal" value="https://pogroupssit.caqh.org/" />
    <!-- Directory Portal -->
    <add key="EnableDirectory" value="true" />
<add key="DirectoryPOPortal" value="https://da-sit3.nonprod.caqh.org" />
    <!-- Auth Token Secret Key -->
    <add key="AuthTokenSecretKey" value="671D1F71B3C25529A739919054DECBF92CC2337654680D87A4B2D04777F950AA" />
    <!-- Auth Token Expiry (In min) -->
    <add key="AuthTokenExpiry" value="5" />
    <!--SAI Authorization-->
    <add key="SAIPOList" value="571,487" />
    <!--POID-->
    <add key="POIDList" value="110,127,172,142,1041" />
    <!--ADAPOID-->
    <add key="ADAPOID" value="1051" />
    <!--Feature toggles-->
    <add key="ADAFeatureToggle" value="true" />
    <!--Google Captcha-->
    <add key="GoogleSiteKey" value="6LetnzYUAAAAANciDHqaaj-nyth8I4d_eqrGF8_N" />
    <add key="GoogleSecretKey" value="6LetnzYUAAAAAClR_GNKc9RN5s1FDNZiIkv5SYSy" />
    <!--DAExtractVersion-->
    <add key="DAJsonVersion" value="10" />
    <!--Resource-->
    <add key="Resourcefiles" value="C:\SIT3\Portal\Content\Resources\" />
    <add key="EnableCOQuestionSwap" value="True" />
    <add key="COReplicaReleaseDate" value="02/22/2018" />
    <add key="DirectAssureRoles" value="PO Standard User (ProView and Sanctions),PO View-Only User (ProView and Sanctions),PO Standard User (ProView Only),PO Back-Up Administrator (ProView Only),PO Billing Administrator (ProView Only),PO Temporary Administrator (ProView Only)" />
    <add key="DefaultDirectAssureRoles" value="PO DirectAssure Standard User" />
    <add key="ChangePasswordFlag" value="false" />
    <add key="ChangePasswordRestriction" value="false" />
    <!--Verifide-->
    <add key="VeriFideURL" value="https://verifideportalsit.nonprod.caqh.org/home/index " />
    <add key="VeriFideAuthTokenSecretKey" value="671D1F71B3C25529A739919054DECBF92CC2337654680D87A4B2D04777F950AA" />
    <!-- VeriFide Auth Token Expiry (In min) -->
    <add key="VeriFideAuthTokenExpiry" value="5" />
    <add key="issuerToken" value="proview-sit3.nonprod.caqh.org" />
    <add key="audToken" value="proview-sit3.nonprod.caqh.org" />
    <!--SMTP Enabler for Reset password-->
    <add key="IsSMTPEnabled" value="false" />
    <!--Google Analytics UAID-->
    <add key="GoogleAnalyticsUAId" value="UA-60154506-3" />
    <add key="APPLICATION_INSIGHTS_INSTRUMENTATION_KEY" value="07e1d3ed-c91f-48f5-afb2-33fc5f5f7c47" />
    <add key="InviteNewGroupsFeature" value="true" />
    <add key="ADALogoutURL" value="https://test.ebusiness.ada.org/login/logoutpo3.aspx?PO3ReturnURL=https://test.ebusiness.ada.org" />
    <add key="PSVEnhancedFileSharePath" value="\\INFCAQAP00015\sit2_b2b\PSVEnhanced_SIT\Import\" />
    <add key="PSVSimpleFileSharePath" value="\\INFCAQAP00015\sit2_b2b\PSVSimpleRoster_SIT\Import\" />
	<add key="AHANotification" value="true"/>
    <!--Correction workflow config keys-->
    <add key="CorrectionWorkFlowEnabled" value="false" />
    <add key="CorrectionWorkFlowAllowedStates" value="" />
    <add key="GraphQLServerURL" value="https://apiproxypperf.caqh.org/dussit3/graphql" />
    <add key="AadApplicationId" value="2712b69b-fa61-40c6-b1b5-f086c22d2817" />
    <add key="AadClientSecret" value="OjhKEfPPSWhihSpMcdnsDj+yMVhzn3NxuLPMx5uJByY=" />
    <add key="SubscriptionKey" value="a19f41462860423a85fc6ea59cf9c7da" />
    <add key="SuppressRetryTimeInMonths" value="6" />
	<add key="httpClientTimeout" value="30"/>
	<add key="IsPasswordComplexityEnable" value="true" />
	<add key="POBOXDerivatives" value="Post Office Box,POB,P O B,PO BOX,pobox,po. box.,po. box,po.box,p.o.b.,p.o. box,p.o. box.,p.o.box,P O BOX" />
	<add key="CorrectionWorkFlowEnabled" value="false"/>
		<!--3Pillar-->
	<add key="AttestationPublisherURL" value="http://10.171.3.6/api/AttestationMessage/publish"/>
	<add key="AttestationPublisherAuthToken" value="QWRtaW4=" /> 
	<add key="IsAttestationNotificationEnabled" value="true" />

    </appSettings>
  <system.web>
    <compilation targetFramework="4.7.2" />
    <httpRuntime targetFramework="4.7.2" maxRequestLength="10240" executionTimeout="600" />
    <authentication mode="Forms">
      <forms loginUrl="~/Login/Index" timeout="45" />
    </authentication>
    <sessionState mode="InProc" timeout="45" />
    <membership defaultProvider="MyDSProvider">
      <providers>
        <add name="MyDSProvider" type="System.Web.Security.ActiveDirectoryMembershipProvider,System.Web, Version=2.0.0.0, Culture=neutral, PublicKeyToken=b03f5f7f11d50a3a" applicationName="CAQHUPD" connectionStringName="ADLDSConn" connectionUsername="CN=admin,CN=Roles,CN=TestPartition1,DC=CAQH-LDS,DC=LOCAL" connectionPassword="P@ssw0rd" connectionProtection="None" />
      </providers>
    </membership>
    <pages>
      <namespaces>
        <add namespace="System.Web.Helpers" />
        <add namespace="System.Web.Mvc" />
        <add namespace="System.Web.Mvc.Ajax" />
        <add namespace="System.Web.Mvc.Html" />
        <add namespace="System.Web.Optimization" />
        <add namespace="System.Web.Routing" />
        <add namespace="System.Web.WebPages" />
        <add namespace="CAQH.UPD.Portal.Web.Helpers" />
        <add namespace="CAQH.UPD.DomainModels" />
        <add namespace="CAQH.UPD.CommonComponents" />
        <add namespace="CAQH.UPD.CommonComponents.WebHelpers" />
        <add namespace="CAQH.UPD.CRM.DAL" />
        <add namespace="CAQH.UPD.CRM.XrmClient" />
        <add namespace="Syncfusion.JavaScript" />
        <add namespace="Syncfusion.JavaScript.DataVisualization" />
        <add namespace="Syncfusion.MVC.EJ" />
      </namespaces>
    </pages>
    <httpHandlers></httpHandlers>
    <customErrors mode="Off" defaultRedirect="~/Error/Index">
      <error statusCode="404" redirect="~/Error/NotFound" />
    </customErrors>
    <httpModules>
      <add name="ApplicationInsightsWebTracking" type="Microsoft.ApplicationInsights.Web.ApplicationInsightsHttpModule, Microsoft.AI.Web" />
      <add name="TelemetryCorrelationHttpModule" type="Microsoft.AspNet.TelemetryCorrelation.TelemetryCorrelationHttpModule, Microsoft.AspNet.TelemetryCorrelation" />
    </httpModules>
  </system.web>
  <system.webServer>
    <!--adding this code as a part of PV-13368-->
    <httpCompression>
      <scheme name="gzip" dll="%Windir%\system32\inetsrv\gzip.dll" />
      <dynamicTypes>
        <add mimeType="text/*" enabled="true" />
        <add mimeType="message/*" enabled="true" />
        <add mimeType="application/javascript" enabled="true" />
        <add mimeType="*/*" enabled="false" />
      </dynamicTypes>
      <staticTypes>
        <add mimeType="text/*" enabled="true" />
        <add mimeType="message/*" enabled="true" />
        <add mimeType="application/javascript" enabled="true" />
        <add mimeType="*/*" enabled="false" />
      </staticTypes>
    </httpCompression>
    <validation validateIntegratedModeConfiguration="false" />
    <httpProtocol>
      <customHeaders>
        <add name="X-Frame-Options" value="SAMEORIGIN" />
      </customHeaders>
    </httpProtocol>
    <staticContent>
      <clientCache cacheControlMode="UseMaxAge" cacheControlMaxAge="15.00:00:00" />
    </staticContent>
    <security>
      <requestFiltering>
        <requestLimits maxAllowedContentLength="20971520" />
      </requestFiltering>
    </security>
    <handlers>
      <remove name="ExtensionlessUrlHandler-Integrated-4.0" />
      <remove name="OPTIONSVerbHandler" />
      <remove name="TRACEVerbHandler" />
      <remove name="ViewReplicaPDFFileHandler" />
      <add name="ViewReplicaPDFFileHandler" path="*.pdf" verb="*" type="System.Web.Handlers.TransferRequestHandler" preCondition="integratedMode,runtimeVersionv4.0" responseBufferLimit="0" />
      <add name="ExtensionlessUrlHandler-Integrated-4.0" path="*." verb="*" type="System.Web.Handlers.TransferRequestHandler" preCondition="integratedMode,runtimeVersionv4.0" />
    </handlers>
    <modules>
      <remove name="ApplicationInsightsWebTracking" />
      <add name="ApplicationInsightsWebTracking" type="Microsoft.ApplicationInsights.Web.ApplicationInsightsHttpModule, Microsoft.AI.Web" preCondition="managedHandler" />
      <remove name="TelemetryCorrelationHttpModule" />
      <add name="TelemetryCorrelationHttpModule" type="Microsoft.AspNet.TelemetryCorrelation.TelemetryCorrelationHttpModule, Microsoft.AspNet.TelemetryCorrelation" preCondition="managedHandler" />
    </modules>
  </system.webServer>
  <system.net>
    <mailSettings>
      <smtp deliveryMethod="Network" from="admin@caqh.com">
        <network host="AMREXT1.SMTP.ACCENTURE.COM" port="25" defaultCredentials="true" enableSsl="true" />
      </smtp>
    </mailSettings>
    <defaultProxy enabled="true" />
    <settings>
      <!-- This setting causes .NET to check certificate revocation lists (CRL) 
			     before trusting HTTPS certificates.  But this setting tends to not 
			     be allowed in shared hosting environments. -->
      <!--<servicePointManager checkCertificateRevocationList="true"/>-->
    </settings>
  </system.net>
  <!--userName="" password="" enableSsl="true"-->
  <runtime>
    <assemblyBinding xmlns="urn:schemas-microsoft-com:asm.v1">
      <dependentAssembly>
        <assemblyIdentity name="System.Web.Helpers" publicKeyToken="31bf3856ad364e35" />
        <bindingRedirect oldVersion="0.0.0.0-3.0.0.0" newVersion="3.0.0.0" />
      </dependentAssembly>
      <dependentAssembly>
        <assemblyIdentity name="System.Web.Mvc" publicKeyToken="31bf3856ad364e35" />
        <bindingRedirect oldVersion="0.0.0.0-5.0.0.0" newVersion="5.0.0.0" />
      </dependentAssembly>
      <dependentAssembly>
        <assemblyIdentity name="System.Web.WebPages" publicKeyToken="31bf3856ad364e35" />
        <bindingRedirect oldVersion="0.0.0.0-3.0.0.0" newVersion="3.0.0.0" />
      </dependentAssembly>
      <dependentAssembly>
        <assemblyIdentity name="System.Web.Abstractions" publicKeyToken="31bf3856ad364e35" culture="neutral" />
        <bindingRedirect oldVersion="0.0.0.0-4.0.0.0" newVersion="4.0.0.0" />
      </dependentAssembly>
      <dependentAssembly>
        <assemblyIdentity name="EntityFramework" publicKeyToken="b77a5c561934e089" culture="neutral" />
        <bindingRedirect oldVersion="0.0.0.0-5.0.0.0" newVersion="6.0.0.0" />
      </dependentAssembly>
      <dependentAssembly>
        <assemblyIdentity name="System.Web.Razor" publicKeyToken="31bf3856ad364e35" culture="neutral" />
        <bindingRedirect oldVersion="0.0.0.0-3.0.0.0" newVersion="3.0.0.0" />
      </dependentAssembly>
      <dependentAssembly>
        <assemblyIdentity name="System.Web.WebPages.Razor" publicKeyToken="31bf3856ad364e35" culture="neutral" />
        <bindingRedirect oldVersion="0.0.0.0-3.0.0.0" newVersion="3.0.0.0" />
      </dependentAssembly>
      <dependentAssembly>
        <assemblyIdentity name="WebMatrix.WebData" publicKeyToken="31bf3856ad364e35" culture="neutral" />
        <bindingRedirect oldVersion="0.0.0.0-3.0.0.0" newVersion="3.0.0.0" />
      </dependentAssembly>
      <dependentAssembly>
        <assemblyIdentity name="log4net" publicKeyToken="669e0ddf0bb1aa2a" culture="neutral" />
        <bindingRedirect oldVersion="0.0.0.0-1.2.13.0" newVersion="1.2.13.0" />
      </dependentAssembly>
      <dependentAssembly>
        <assemblyIdentity name="DotNetOpenAuth.AspNet" publicKeyToken="2780ccd10d57b246" culture="neutral" />
        <bindingRedirect oldVersion="0.0.0.0-4.1.0.0" newVersion="4.1.0.0" />
      </dependentAssembly>
      <dependentAssembly>
        <assemblyIdentity name="DotNetOpenAuth.Core" publicKeyToken="2780ccd10d57b246" culture="neutral" />
        <bindingRedirect oldVersion="0.0.0.0-4.1.0.0" newVersion="4.1.0.0" />
      </dependentAssembly>
      <dependentAssembly>
        <assemblyIdentity name="System.Web.Http" publicKeyToken="31bf3856ad364e35" culture="neutral" />
        <bindingRedirect oldVersion="0.0.0.0-5.0.0.0" newVersion="5.0.0.0" />
      </dependentAssembly>
      <dependentAssembly>
        <assemblyIdentity name="System.Net.Http.Formatting" publicKeyToken="31bf3856ad364e35" culture="neutral" />
        <bindingRedirect oldVersion="0.0.0.0-5.0.0.0" newVersion="5.0.0.0" />
      </dependentAssembly>
      <dependentAssembly>
        <assemblyIdentity name="Newtonsoft.Json" publicKeyToken="30ad4fe6b2a6aeed" culture="neutral" />
        <bindingRedirect oldVersion="0.0.0.0-12.0.0.0" newVersion="12.0.0.0" />
      </dependentAssembly>  
	<dependentAssembly>
        <assemblyIdentity name="Microsoft.Xrm.Sdk" publicKeyToken="31bf3856ad364e35" culture="neutral" />
        <bindingRedirect oldVersion="0.0.0.0-6.0.0.0" newVersion="6.0.0.0" />
	</dependentAssembly>
	<dependentAssembly>
        <assemblyIdentity name="System.Diagnostics.DiagnosticSource" publicKeyToken="cc7b13ffcd2ddd51" culture="neutral"/>
        <bindingRedirect oldVersion="0.0.0.0-4.0.3.1" newVersion="4.0.3.1"/>
	</dependentAssembly>
	<dependentAssembly>
        <assemblyIdentity name="Microsoft.ApplicationInsights" publicKeyToken="31bf3856ad364e35" culture="neutral" />
        <bindingRedirect oldVersion="0.0.0.0-2.9.1.0" newVersion="2.9.1.0" />
	</dependentAssembly>

    </assemblyBinding>
    <!-- This prevents the Windows Event Log from frequently logging that HMAC1 is being used (when the other party needs it). -->
    <legacyHMACWarning enabled="0" />
    <!-- When targeting ASP.NET MVC 3, this assemblyBinding makes MVC 1 and 2 references relink
		     to MVC 3 so libraries such as DotNetOpenAuth that compile against MVC 1 will work with it.
		<assemblyBinding xmlns="urn:schemas-microsoft-com:asm.v1">
			<dependentAssembly>
				<assemblyIdentity name="System.Web.Mvc" publicKeyToken="31bf3856ad364e35" />
				<bindingRedirect oldVersion="1.0.0.0-3.0.0.0" newVersion="3.0.0.0" />
			</dependentAssembly>
		</assemblyBinding>
		 -->
  </runtime>
  <entityFramework>
    <defaultConnectionFactory type="System.Data.Entity.Infrastructure.LocalDbConnectionFactory, EntityFramework">
      <parameters>
        <parameter value="v11.0" />
      </parameters>
    </defaultConnectionFactory>
  </entityFramework>
  <!--<dataCacheClient>
    -->
  <!-- cache host(s) -->
  <!--R
    <hosts>
      <host
         name="INFCAQWD0007"
         cachePort="22233"/>
    </hosts>
  </dataCacheClient>-->
  <dataCacheClient requestTimeout="60000" channelOpenTimeout="19999" maxConnectionsToServer="1">
    <!--<localCache isEnabled="false" sync="TimeoutBased" ttlValue="300" objectCount="10000"/>
    <clientNotification pollInterval="300" maxQueueLength="10000"/>-->
    <hosts>
      <host name="INFCAQWD0007" cachePort="22233" />
      <!--<host name="CacheServer2" cachePort="22233"/>-->
    </hosts>
    <!--<securityProperties mode="Transport" protectionLevel="EncryptAndSign" />-->
    <securityProperties mode="None" protectionLevel="None" />
    <localCache isEnabled="false" />
    <transportProperties maxOutputDelay="2" channelInitializationTimeout="60000" maxBufferPoolSize="2147483647" maxBufferSize="2147483647" />
  </dataCacheClient>
  <system.serviceModel>
    <bindings>
      <basicHttpBinding>
        <binding name="PVSServiceSoap" closeTimeout="00:01:00" openTimeout="00:01:00" receiveTimeout="00:10:00" sendTimeout="00:01:00" allowCookies="false" bypassProxyOnLocal="false" hostNameComparisonMode="StrongWildcard" maxBufferPoolSize="524288" maxBufferSize="65536" maxReceivedMessageSize="65536" textEncoding="utf-8" transferMode="Buffered" useDefaultWebProxy="true" messageEncoding="Text">
          <readerQuotas maxDepth="32" maxStringContentLength="8192" maxArrayLength="16384" maxBytesPerRead="4096" maxNameTableCharCount="16384" />
          <security mode="Transport">
            <transport clientCredentialType="None" proxyCredentialType="None" realm="" />
            <message clientCredentialType="UserName" algorithmSuite="Default" />
          </security>
        </binding>
        <binding name="PVSServiceSoap1" closeTimeout="00:01:00" openTimeout="00:01:00" receiveTimeout="00:10:00" sendTimeout="00:01:00" allowCookies="false" bypassProxyOnLocal="false" hostNameComparisonMode="StrongWildcard" maxBufferPoolSize="524288" maxBufferSize="65536" maxReceivedMessageSize="65536" textEncoding="utf-8" transferMode="Buffered" useDefaultWebProxy="true" messageEncoding="Text">
          <readerQuotas maxDepth="32" maxStringContentLength="8192" maxArrayLength="16384" maxBytesPerRead="4096" maxNameTableCharCount="16384" />
          <security mode="None">
            <transport clientCredentialType="None" proxyCredentialType="None" realm="" />
            <message clientCredentialType="UserName" algorithmSuite="Default" />
          </security>
        </binding>
        <binding name="wspHVLookupSoap" closeTimeout="00:01:00" openTimeout="00:01:00" receiveTimeout="00:10:00" sendTimeout="00:01:00" allowCookies="false" bypassProxyOnLocal="false" hostNameComparisonMode="StrongWildcard" maxBufferPoolSize="2147483647" maxBufferSize="2147483647" maxReceivedMessageSize="2147483647" textEncoding="utf-8" transferMode="Buffered" useDefaultWebProxy="true" messageEncoding="Text">
          <readerQuotas maxDepth="2147483647" maxStringContentLength="2147483647" maxArrayLength="2147483647" maxBytesPerRead="2147483647" maxNameTableCharCount="2147483647" />
          <security mode="None">
            <transport clientCredentialType="None" proxyCredentialType="None" realm="" />
            <message clientCredentialType="UserName" algorithmSuite="Default" />
          </security>
        </binding>
        <binding name="deawebsvcSoap" maxReceivedMessageSize="2097152">
          <security mode="Transport" />
        </binding>
        <binding name="CAQHInfoSoap">
          <security mode="Transport" />
        </binding>
        <binding name="CAQHInfoSoap1" />
      </basicHttpBinding>
      <customBinding>
        <binding name="WebHttpBinding_IDocServ1">
          <textMessageEncoding messageVersion="Soap12" />
        </binding>
      </customBinding>
      <netTcpBinding>
        <binding name="BasicHttpBinding_IDocConvertorService" closeTimeout="00:20:00" openTimeout="00:20:00" receiveTimeout="00:20:00" sendTimeout="00:20:00" transferMode="Buffered" hostNameComparisonMode="StrongWildcard" maxBufferPoolSize="524288" maxBufferSize="65536" maxReceivedMessageSize="65536">
          <readerQuotas maxDepth="32" maxStringContentLength="8192" maxArrayLength="16384" maxBytesPerRead="4096" maxNameTableCharCount="16384" />
          <security mode="Message">
            <message clientCredentialType="UserName" algorithmSuite="Default" />
          </security>
        </binding>
      </netTcpBinding>
      <wsHttpBinding>
        <binding name="WSHttpBinding_IBulkExtractDocs" messageEncoding="Mtom">
          <security mode="Transport" />
        </binding>
        <binding name="WSHttpBinding_IStorageService">
          <security mode="Transport">
            <transport clientCredentialType="None" />
          </security>
        </binding>
      </wsHttpBinding>
      <webHttpBinding>
        <binding name="WebHttpBinding_IDocServ" maxBufferSize="2147483647" maxBufferPoolSize="2147483647" maxReceivedMessageSize="2147483647">
          <readerQuotas maxDepth="2147483647" maxStringContentLength="2147483647" maxArrayLength="2147483647" maxBytesPerRead="2147483647" maxNameTableCharCount="2147483647" />
          <security mode="Transport">
            <transport clientCredentialType="None" />
          </security>
        </binding>
      </webHttpBinding>
    </bindings>
    <client>
      <endpoint address="https://www.tincheck.com/pvsws/pvsservice.asmx" binding="basicHttpBinding" bindingConfiguration="PVSServiceSoap" contract="TINCheck.PVSServiceSoap" name="PVSServiceSoap" />
      <endpoint address="http://www.hipaaspace.com/wspHVLookup.asmx" binding="basicHttpBinding" bindingConfiguration="wspHVLookupSoap" contract="HIPAASpace.wspHVLookupSoap" name="wspHVLookupSoap" />
      <endpoint address="https://www.deanumber.com/Websvc/deaWebsvc.asmx" binding="basicHttpBinding" bindingConfiguration="deawebsvcSoap" contract="DEAService.deawebsvcSoap" name="deawebsvcSoap" />
      <endpoint address="net.tcp://66.77.1.145:1801/DocumentConvertorWS" binding="netTcpBinding" bindingConfiguration="BasicHttpBinding_IDocConvertorService" contract="DocConvertor.IDocConvertorService" name="eFaxServiceConfiguration">
        <identity>
          <dns value="Dicertlocalhost" />
        </identity>
      </endpoint>
      <endpoint address="https://ddservices-uat.accenture.com/BulkExtractDocs/BulkExtractDocs.svc" binding="wsHttpBinding" bindingConfiguration="WSHttpBinding_IBulkExtractDocs" contract="BulkExtractDocsService.IBulkExtractDocs" name="WSHttpBinding_IBulkExtractDocs">
        <identity>
          <servicePrincipalName value="host/QWEDCTMTSTWB1.BSSTEST.accenture.com" />
        </identity>
      </endpoint>
      <endpoint address="https://ddservices-uat.accenture.com/DocViewer/DocServ.svc/?get=" behaviorConfiguration="web" binding="webHttpBinding" bindingConfiguration="WebHttpBinding_IDocServ" contract="DocService.IDocServ" name="WebHttpBinding_IDocServ" />
      <endpoint address="https://dduploadservices-uat.accenture.com/FileStoreDocStorage/StorageService.svc?wsdl" binding="wsHttpBinding" bindingConfiguration="WSHttpBinding_IStorageService" contract="StorageService.IStorageService" name="WSHttpBinding_IStorageService" />
      <endpoint address="https://ebusiness.ada.org/webservices/CAQHinfo.asmx" binding="basicHttpBinding" bindingConfiguration="CAQHInfoSoap" contract="ADAService.CAQHInfoSoap" name="CAQHInfoSoap" />
    </client>
    <!-- BPO DMS Configurations -->
    <behaviors>
      <serviceBehaviors>
        <behavior name="DocumentRetrieval.DocServBehavior">
          <serviceMetadata httpsGetEnabled="true" httpsGetUrl="" />
        </behavior>
      </serviceBehaviors>
      <endpointBehaviors>
        <behavior name="web">
          <webHttp />
          <!--<enableWebScript/>-->
        </behavior>
      </endpointBehaviors>
    </behaviors>
  </system.serviceModel>
  <!-- BPO DMS Configurations -->
  <submissionConfiguration>
    <client clientId="1" isEnabled="false" traceToLog="false">
      <endpointconfigurationName>eFaxServiceConfiguration</endpointconfigurationName>
      <userName>Dicertlocalhost</userName>
      <password>Acc1234$$</password>
    </client>
  </submissionConfiguration>
  <dotNetOpenAuth>
    <messaging>
      <untrustedWebRequest>
        <whitelistHosts>
          <!-- Uncomment to enable communication with localhost (should generally not activate in production!) -->
          <!--<add name="localhost" />-->
        </whitelistHosts>
      </untrustedWebRequest>
    </messaging>
    <!-- Allow DotNetOpenAuth to publish usage statistics to library authors to improve the library. -->
    <reporting enabled="true" />
    <!-- This is an optional configuration section where aspects of dotnetopenauth can be customized. -->
    <!-- For a complete set of configuration options see http://www.dotnetopenauth.net/developers/code-snippets/configuration-options/ -->
    <openid>
      <relyingParty>
        <security requireSsl="false">
          <!-- Uncomment the trustedProviders tag if your relying party should only accept positive assertions from a closed set of OpenID Providers. -->
          <!--<trustedProviders rejectAssertionsFromUntrustedProviders="true">
						<add endpoint="https://www.google.com/accounts/o8/ud" />
					</trustedProviders>-->
        </security>
        <behaviors>
          <!-- The following OPTIONAL behavior allows RPs to use SREG only, but be compatible
					     with OPs that use Attribute Exchange (in various formats). -->
          <add type="DotNetOpenAuth.OpenId.RelyingParty.Behaviors.AXFetchAsSregTransform, DotNetOpenAuth.OpenId.RelyingParty" />
        </behaviors>
      </relyingParty>
    </openid>
  </dotNetOpenAuth>
  <uri>
    <!-- The uri section is necessary to turn on .NET 3.5 support for IDN (international domain names),
		     which is necessary for OpenID urls with unicode characters in the domain/host name.
		     It is also required to put the Uri class into RFC 3986 escaping mode, which OpenID and OAuth require. -->
    <idn enabled="All" />
    <iriParsing enabled="true" />
  </uri>
</configuration>
<!--ProjectGuid: {294E15AE-824C-4889-A562-3A433B2ED641}-->