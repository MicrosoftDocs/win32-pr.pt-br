---
title: Classe MDM_Policy_User_Config01_InternetExplorer02
description: A \_ classe Config01 InternetExplorer02 do usuário da política de MDM \_ \_ \_ representa as políticas disponíveis do Internet Explorer.
ms.assetid: 2b155e65-5a81-4916-815f-23763759bb9a
keywords:
- Classe MDM_Policy_User_Config01_InternetExplorer02
- Classe MDM_Policy_User_Config01_InternetExplorer02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_User_Config01_InternetExplorer02
- MDM_Policy_User_Config01_InternetExplorer02.InstanceID
- MDM_Policy_User_Config01_InternetExplorer02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2f79c00505037508307e93120f9e2545b135678
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009416"
---
# <a name="mdm_policy_user_config01_internetexplorer02-class"></a><span data-ttu-id="f266b-105">Config01 de usuário de política de MDM- \_ \_ \_ \_ classe InternetExplorer02</span><span class="sxs-lookup"><span data-stu-id="f266b-105">MDM\_Policy\_User\_Config01\_InternetExplorer02 class</span></span>

<span data-ttu-id="f266b-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="f266b-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="f266b-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="f266b-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="f266b-108">A \_ classe Config01 InternetExplorer02 do usuário da política de MDM \_ \_ \_ representa as políticas disponíveis do Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="f266b-108">The MDM\_Policy\_User\_Config01\_InternetExplorer02 class represents the available Internet Explorer policies.</span></span>

<span data-ttu-id="f266b-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="f266b-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f266b-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f266b-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Config01_InternetExplorer02
{
  string InstanceID;
  string ParentID;
  string AddSearchProvider;
  string AllowActiveXFiltering;
  string AllowAddOnList;
  string AllowDeletingBrowsingHistoryOnExit;
  string AllowCertificateAddressMismatchWarning;
  string AllowAutoComplete;
  string AllowEnhancedProtectedMode;
  string AllowEnterpriseModeFromToolsMenu;
  string AllowEnterpriseModeSiteList;
  string AllowInternetExplorer7PolicyList;
  string AllowInternetExplorerStandardsMode;
  string AllowInternetZoneTemplate;
  string AllowIntranetZoneTemplate;
  string AllowLocalMachineZoneTemplate;
  string AllowLockedDownInternetZoneTemplate;
  string AllowLockedDownIntranetZoneTemplate;
  string AllowLockedDownLocalMachineZoneTemplate;
  string AllowLockedDownRestrictedSitesZoneTemplate;
  string AllowOneWordEntry;
  string AllowSiteToZoneAssignmentList;
  string AllowsLockedDownTrustedSitesZoneTemplate;
  string AllowSoftwareWhenSignatureIsInvalid;
  string AllowsRestrictedSitesZoneTemplate;
  string AllowSuggestedSites;
  string AllowTrustedSitesZoneTemplate;
  string ConsistentMimeHandlingInternetExplorerProcesses;
  string CheckSignaturesOnDownloadedPrograms;
  string CheckServerCertificateRevocation;
  string DisableAdobeFlash;
  string DisableBlockingOfOutdatedActiveXControls;
  string DisableBypassOfSmartScreenWarnings;
  string DisableBypassOfSmartScreenWarningsAboutUncommonFiles;
  string DisableCrashDetection;
  string DisableConfiguringHistory;
  string DisableCustomerExperienceImprovementProgramParticipation;
  string DisableDeletingUserVisitedWebsites;
  string DisableEnclosureDownloading;
  string DisableEncryptionSupport;
  string DisableFirstRunWizard;
  string DisableFlipAheadFeature;
  string DisableHomePageChange;
  string DisableProcessesInEnhancedProtectedMode;
  string DisableInPrivateBrowsing;
  string DisableIgnoringCertificateErrors;
  string DisableProxyChange;
  string DisableSearchProviderChange;
  string DisableSecondaryHomePageChange;
  string DoNotAllowActiveXControlsInProtectedMode;
  string DisableSecuritySettingsCheck;
  string DoNotBlockOutdatedActiveXControls;
  string DoNotBlockOutdatedActiveXControlsOnSpecificDomains;
  string IncludeAllLocalSites;
  string IncludeAllNetworkPaths;
  string InternetZoneAllowAccessToDataSources;
  string InternetZoneAllowAutomaticPromptingForActiveXControls;
  string InternetZoneAllowAutomaticPromptingForFileDownloads;
  string InternetZoneAllowDragAndDropCopyAndPasteFiles;
  string InternetZoneAllowCopyPasteViaScript;
  string InternetZoneAllowFontDownloads;
  string InternetZoneAllowLessPrivilegedSites;
  string InternetZoneAllowLoadingOfXAMLFiles;
  string InternetZoneAllowNETFrameworkReliantComponents;
  string InternetZoneAllowScriptInitiatedWindows;
  string InternetZoneAllowScriptingOfInternetExplorerWebBrowserControls;
  string InternetZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl;
  string InternetZoneAllowOnlyApprovedDomainsToUseActiveXControls;
  string InternetZoneAllowScriptlets;
  string InternetZoneAllowSmartScreenIE;
  string InternetZoneAllowUpdatesToStatusBarViaScript;
  string InternetZoneAllowUserDataPersistence;
  string InternetZoneDoNotRunAntimalwareAgainstActiveXControls;
  string InternetZoneIncludeLocalPathWhenUploadingFilesToServer;
  string InternetZoneEnableProtectedMode;
  string InternetZoneEnableMIMESniffing;
  string InternetZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows;
  string InternetZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows;
  string InternetZoneEnableCrossSiteScriptingFilter;
  string InternetZoneDownloadUnsignedActiveXControls;
  string InternetZoneDownloadSignedActiveXControls;
  string InternetZoneInitializeAndScriptActiveXControls;
  string InternetZoneJavaPermissions;
  string InternetZoneLogonOptions;
  string InternetZoneLaunchingApplicationsAndFilesInIFRAME;
  string InternetZoneNavigateWindowsAndFrames;
  string InternetZoneWebsitesInLessPrivilegedZonesCanNavigateIntoThisZone;
  string InternetZoneUsePopupBlocker;
  string InternetZoneShowSecurityWarningForPotentiallyUnsafeFiles;
  string InternetZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode;
  string InternetZoneRunNETFrameworkReliantComponentsNotSignedWithAuthenticode;
  string IntranetZoneAllowAccessToDataSources;
  string IntranetZoneAllowAutomaticPromptingForActiveXControls;
  string IntranetZoneAllowAutomaticPromptingForFileDownloads;
  string IntranetZoneAllowFontDownloads;
  string IntranetZoneAllowLessPrivilegedSites;
  string IntranetZoneAllowNETFrameworkReliantComponents;
  string IntranetZoneAllowScriptlets;
  string IntranetZoneAllowSmartScreenIE;
  string IntranetZoneAllowUserDataPersistence;
  string IntranetZoneDoNotRunAntimalwareAgainstActiveXControls;
  string IntranetZoneInitializeAndScriptActiveXControls;
  string IntranetZoneJavaPermissions;
  string IntranetZoneInitializeAndScriptActiveXControlsNotMarkedSafe;
  string IntranetZoneNavigateWindowsAndFrames;
  string LocalMachineZoneAllowAccessToDataSources;
  string LocalMachineZoneAllowAutomaticPromptingForActiveXControls;
  string LocalMachineZoneAllowAutomaticPromptingForFileDownloads;
  string LocalMachineZoneAllowFontDownloads;
  string LocalMachineZoneAllowLessPrivilegedSites;
  string LocalMachineZoneAllowNETFrameworkReliantComponents;
  string LocalMachineZoneAllowScriptlets;
  string LocalMachineZoneAllowSmartScreenIE;
  string LocalMachineZoneAllowUserDataPersistence;
  string LocalMachineZoneDoNotRunAntimalwareAgainstActiveXControls;
  string LocalMachineZoneInitializeAndScriptActiveXControls;
  string LocalMachineZoneJavaPermissions;
  string LocalMachineZoneNavigateWindowsAndFrames;
  string LockedDownInternetZoneAllowAccessToDataSources;
  string LockedDownInternetZoneAllowAutomaticPromptingForActiveXControls;
  string LockedDownInternetZoneAllowAutomaticPromptingForFileDownloads;
  string LockedDownInternetZoneAllowFontDownloads;
  string LockedDownInternetZoneAllowLessPrivilegedSites;
  string LockedDownInternetZoneAllowNETFrameworkReliantComponents;
  string LockedDownInternetZoneAllowScriptlets;
  string LockedDownInternetZoneAllowSmartScreenIE;
  string LockedDownInternetZoneAllowUserDataPersistence;
  string LockedDownInternetZoneInitializeAndScriptActiveXControls;
  string LockedDownInternetZoneJavaPermissions;
  string LockedDownInternetZoneNavigateWindowsAndFrames;
  string LockedDownIntranetZoneAllowAccessToDataSources;
  string LockedDownIntranetZoneAllowAutomaticPromptingForActiveXControls;
  string LockedDownIntranetZoneAllowAutomaticPromptingForFileDownloads;
  string LockedDownIntranetZoneAllowFontDownloads;
  string LockedDownIntranetZoneAllowLessPrivilegedSites;
  string LockedDownIntranetZoneAllowNETFrameworkReliantComponents;
  string LockedDownIntranetZoneAllowScriptlets;
  string LockedDownIntranetZoneAllowSmartScreenIE;
  string LockedDownIntranetZoneAllowUserDataPersistence;
  string LockedDownIntranetZoneInitializeAndScriptActiveXControls;
  string LockedDownIntranetZoneNavigateWindowsAndFrames;
  string LockedDownLocalMachineZoneAllowAccessToDataSources;
  string LockedDownLocalMachineZoneAllowAutomaticPromptingForActiveXControls;
  string LockedDownLocalMachineZoneAllowAutomaticPromptingForFileDownloads;
  string LockedDownLocalMachineZoneAllowFontDownloads;
  string LockedDownLocalMachineZoneAllowLessPrivilegedSites;
  string LockedDownLocalMachineZoneAllowNETFrameworkReliantComponents;
  string LockedDownLocalMachineZoneAllowScriptlets;
  string LockedDownLocalMachineZoneAllowSmartScreenIE;
  string LockedDownLocalMachineZoneAllowUserDataPersistence;
  string LockedDownLocalMachineZoneInitializeAndScriptActiveXControls;
  string LockedDownLocalMachineZoneJavaPermissions;
  string LockedDownLocalMachineZoneNavigateWindowsAndFrames;
  string LockedDownRestrictedSitesZoneAllowAccessToDataSources;
  string LockedDownRestrictedSitesZoneAllowAutomaticPromptingForActiveXControls;
  string LockedDownRestrictedSitesZoneAllowAutomaticPromptingForFileDownloads;
  string LockedDownRestrictedSitesZoneAllowFontDownloads;
  string LockedDownRestrictedSitesZoneAllowLessPrivilegedSites;
  string LockedDownRestrictedSitesZoneAllowNETFrameworkReliantComponents;
  string LockedDownRestrictedSitesZoneAllowScriptlets;
  string LockedDownRestrictedSitesZoneAllowSmartScreenIE;
  string LockedDownRestrictedSitesZoneAllowUserDataPersistence;
  string LockedDownRestrictedSitesZoneInitializeAndScriptActiveXControls;
  string LockedDownRestrictedSitesZoneJavaPermissions;
  string LockedDownRestrictedSitesZoneNavigateWindowsAndFrames;
  string LockedDownTrustedSitesZoneAllowAccessToDataSources;
  string LockedDownTrustedSitesZoneAllowAutomaticPromptingForActiveXControls;
  string LockedDownTrustedSitesZoneAllowAutomaticPromptingForFileDownloads;
  string LockedDownTrustedSitesZoneAllowFontDownloads;
  string LockedDownTrustedSitesZoneAllowLessPrivilegedSites;
  string LockedDownTrustedSitesZoneAllowNETFrameworkReliantComponents;
  string LockedDownTrustedSitesZoneAllowScriptlets;
  string LockedDownTrustedSitesZoneAllowSmartScreenIE;
  string LockedDownTrustedSitesZoneAllowUserDataPersistence;
  string LockedDownTrustedSitesZoneInitializeAndScriptActiveXControls;
  string LockedDownTrustedSitesZoneJavaPermissions;
  string LockedDownTrustedSitesZoneNavigateWindowsAndFrames;
  string RestrictActiveXInstallInternetExplorerProcesses;
  string RemoveRunThisTimeButtonForOutdatedActiveXControls;
  string ProtectionFromZoneElevationInternetExplorerProcesses;
  string PreventPerUserInstallationOfActiveXControls;
  string PreventManagingSmartScreenFilter;
  string NotificationBarInternetExplorerProcesses;
  string MKProtocolSecurityRestrictionInternetExplorerProcesses;
  string MimeSniffingSafetyFeatureInternetExplorerProcesses;
  string RestrictedSitesZoneAllowAccessToDataSources;
  string RestrictedSitesZoneAllowActiveScripting;
  string RestrictedSitesZoneAllowAutomaticPromptingForActiveXControls;
  string RestrictedSitesZoneAllowAutomaticPromptingForFileDownloads;
  string RestrictedSitesZoneAllowFileDownloads;
  string RestrictedSitesZoneAllowDragAndDropCopyAndPasteFiles;
  string RestrictedSitesZoneAllowCopyPasteViaScript;
  string RestrictedSitesZoneAllowBinaryAndScriptBehaviors;
  string RestrictedSitesZoneAllowFontDownloads;
  string RestrictedSitesZoneAllowLessPrivilegedSites;
  string RestrictedSitesZoneAllowMETAREFRESH;
  string RestrictedSitesZoneAllowLoadingOfXAMLFiles;
  string RestrictedSitesZoneAllowNETFrameworkReliantComponents;
  string RestrictedSitesZoneAllowScriptInitiatedWindows;
  string RestrictedSitesZoneAllowScriptingOfInternetExplorerWebBrowserControls;
  string RestrictedSitesZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl;
  string RestrictedSitesZoneAllowOnlyApprovedDomainsToUseActiveXControls;
  string RestrictedSitesZoneAllowScriptlets;
  string RestrictedSitesZoneAllowSmartScreenIE;
  string RestrictedSitesZoneAllowUpdatesToStatusBarViaScript;
  string RestrictedSitesZoneAllowUserDataPersistence;
  string RestrictedSitesZoneIncludeLocalPathWhenUploadingFilesToServer;
  string RestrictedSitesZoneEnableMIMESniffing;
  string RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows;
  string RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows;
  string RestrictedSitesZoneDownloadUnsignedActiveXControls;
  string RestrictedSitesZoneEnableCrossSiteScriptingFilter;
  string RestrictedSitesZoneDownloadSignedActiveXControls;
  string RestrictedSitesZoneDoNotRunAntimalwareAgainstActiveXControls;
  string RestrictedSitesZoneInitializeAndScriptActiveXControls;
  string RestrictedSitesZoneLogonOptions;
  string RestrictedSitesZoneLaunchingApplicationsAndFilesInIFRAME;
  string RestrictedSitesZoneJavaPermissions;
  string RestrictedSitesZoneNavigateWindowsAndFrames;
  string ScriptedWindowSecurityRestrictionsInternetExplorerProcesses;
  string RestrictFileDownloadInternetExplorerProcesses;
  string RestrictedSitesZoneScriptActiveXControlsMarkedSafeForScripting;
  string RestrictedSitesZoneUsePopupBlocker;
  string RestrictedSitesZoneTurnOnProtectedMode;
  string RestrictedSitesZoneTurnOnCrossSiteScriptingFilter;
  string RestrictedSitesZoneShowSecurityWarningForPotentiallyUnsafeFiles;
  string RestrictedSitesZoneScriptingOfJavaApplets;
  string RestrictedSitesZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode;
  string RestrictedSitesZoneRunActiveXControlsAndPlugins;
  string RestrictedSitesZoneNavigateWindowsAndFramesAcrossDomains;
  string SearchProviderList;
  string SpecifyUseOfActiveXInstallerService;
  string TrustedSitesZoneAllowAccessToDataSources;
  string TrustedSitesZoneAllowAutomaticPromptingForActiveXControls;
  string TrustedSitesZoneAllowAutomaticPromptingForFileDownloads;
  string TrustedSitesZoneAllowFontDownloads;
  string TrustedSitesZoneAllowLessPrivilegedSites;
  string TrustedSitesZoneAllowNETFrameworkReliantComponents;
  string TrustedSitesZoneAllowScriptlets;
  string TrustedSitesZoneAllowSmartScreenIE;
  string TrustedSitesZoneAllowUserDataPersistence;
  string TrustedSitesZoneDontRunAntimalwareProgramsAgainstActiveXControls;
  string TrustedSitesZoneDoNotRunAntimalwareAgainstActiveXControls;
  string TrustedSitesZoneInitializeAndScriptActiveXControls;
  string TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedSafe;
  string TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedAsSafe;
  string TrustedSitesZoneJavaPermissions;
  string TrustedSitesZoneNavigateWindowsAndFrames;
};
```

## <a name="members"></a><span data-ttu-id="f266b-111">Membros</span><span class="sxs-lookup"><span data-stu-id="f266b-111">Members</span></span>

<span data-ttu-id="f266b-112">A **classe \_ \_ \_ Config01 \_ InternetExplorer02 do usuário da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="f266b-112">The **MDM\_Policy\_User\_Config01\_InternetExplorer02** class has these types of members:</span></span>

-   [<span data-ttu-id="f266b-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f266b-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f266b-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f266b-114">Properties</span></span>

<span data-ttu-id="f266b-115">A **classe \_ \_ \_ Config01 \_ InternetExplorer02 do usuário da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="f266b-115">The **MDM\_Policy\_User\_Config01\_InternetExplorer02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="f266b-116">AddSearchProvider</span><span class="sxs-lookup"><span data-stu-id="f266b-116">AddSearchProvider</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-addsearchprovider)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-119">AllowActiveXFiltering</span><span class="sxs-lookup"><span data-stu-id="f266b-119">AllowActiveXFiltering</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowactivexfiltering)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-122">AllowAddOnList</span><span class="sxs-lookup"><span data-stu-id="f266b-122">AllowAddOnList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowaddonlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-124">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-125">AllowAutoComplete</span><span class="sxs-lookup"><span data-stu-id="f266b-125">AllowAutoComplete</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowautocomplete)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-126">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-127">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-128">AllowCertificateAddressMismatchWarning</span><span class="sxs-lookup"><span data-stu-id="f266b-128">AllowCertificateAddressMismatchWarning</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowcertificateaddressmismatchwarning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-130">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-131">AllowDeletingBrowsingHistoryOnExit</span><span class="sxs-lookup"><span data-stu-id="f266b-131">AllowDeletingBrowsingHistoryOnExit</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowdeletingbrowsinghistoryonexit)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-132">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-133">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-134">AllowEnhancedProtectedMode</span><span class="sxs-lookup"><span data-stu-id="f266b-134">AllowEnhancedProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenhancedprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-135">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-136">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-137">AllowEnterpriseModeFromToolsMenu</span><span class="sxs-lookup"><span data-stu-id="f266b-137">AllowEnterpriseModeFromToolsMenu</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenterprisemodefromtoolsmenu)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-138">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-139">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-140">AllowEnterpriseModeSiteList</span><span class="sxs-lookup"><span data-stu-id="f266b-140">AllowEnterpriseModeSiteList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenterprisemodesitelist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-141">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-142">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-143">AllowInternetExplorer7PolicyList</span><span class="sxs-lookup"><span data-stu-id="f266b-143">AllowInternetExplorer7PolicyList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetexplorer7policylist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-144">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-145">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-146">AllowInternetExplorerStandardsMode</span><span class="sxs-lookup"><span data-stu-id="f266b-146">AllowInternetExplorerStandardsMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetexplorerstandardsmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-147">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-148">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-149">AllowInternetZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="f266b-149">AllowInternetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-150">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-151">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-152">AllowIntranetZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="f266b-152">AllowIntranetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowintranetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-153">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-154">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-155">AllowLocalMachineZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="f266b-155">AllowLocalMachineZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlocalmachinezonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-156">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-157">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-158">AllowLockedDownInternetZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="f266b-158">AllowLockedDownInternetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddowninternetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-159">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-160">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-161">AllowLockedDownIntranetZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="f266b-161">AllowLockedDownIntranetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownintranetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-162">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-163">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-164">AllowLockedDownLocalMachineZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="f266b-164">AllowLockedDownLocalMachineZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownlocalmachinezonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-165">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-166">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-167">AllowLockedDownRestrictedSitesZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="f266b-167">AllowLockedDownRestrictedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownrestrictedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-168">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-169">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-170">AllowOneWordEntry</span><span class="sxs-lookup"><span data-stu-id="f266b-170">AllowOneWordEntry</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowonewordentry)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-171">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-172">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-173">AllowSiteToZoneAssignmentList</span><span class="sxs-lookup"><span data-stu-id="f266b-173">AllowSiteToZoneAssignmentList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsitetozoneassignmentlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-174">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-175">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-175">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-176">AllowsLockedDownTrustedSitesZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="f266b-176">AllowsLockedDownTrustedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowslockeddowntrustedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-177">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-178">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-178">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-179">AllowSoftwareWhenSignatureIsInvalid</span><span class="sxs-lookup"><span data-stu-id="f266b-179">AllowSoftwareWhenSignatureIsInvalid</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsoftwarewhensignatureisinvalid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-180">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-181">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-182">AllowsRestrictedSitesZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="f266b-182">AllowsRestrictedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsrestrictedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-183">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-184">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-184">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-185">AllowSuggestedSites</span><span class="sxs-lookup"><span data-stu-id="f266b-185">AllowSuggestedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsuggestedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-186">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-187">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-187">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-188">AllowTrustedSitesZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="f266b-188">AllowTrustedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowtrustedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-189">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-190">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-190">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-191">CheckServerCertificateRevocation</span><span class="sxs-lookup"><span data-stu-id="f266b-191">CheckServerCertificateRevocation</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-checkservercertificaterevocation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-192">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-193">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-193">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-194">CheckSignaturesOnDownloadedPrograms</span><span class="sxs-lookup"><span data-stu-id="f266b-194">CheckSignaturesOnDownloadedPrograms</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-checksignaturesondownloadedprograms)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-195">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-196">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-196">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-197">ConsistentMimeHandlingInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="f266b-197">ConsistentMimeHandlingInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-consistentmimehandlinginternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-198">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-199">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-199">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-200">DisableAdobeFlash</span><span class="sxs-lookup"><span data-stu-id="f266b-200">DisableAdobeFlash</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableadobeflash)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-201">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-202">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-202">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f266b-203">DisableBlockingOfOutdatedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="f266b-203">DisableBlockingOfOutdatedActiveXControls</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-204">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-205">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-205">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-206">DisableBypassOfSmartScreenWarnings</span><span class="sxs-lookup"><span data-stu-id="f266b-206">DisableBypassOfSmartScreenWarnings</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablebypassofsmartscreenwarnings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-207">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-208">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-208">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-209">DisableBypassOfSmartScreenWarningsAboutUncommonFiles</span><span class="sxs-lookup"><span data-stu-id="f266b-209">DisableBypassOfSmartScreenWarningsAboutUncommonFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablebypassofsmartscreenwarningsaboutuncommonfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-210">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-211">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-211">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-212">DisableConfiguringHistory</span><span class="sxs-lookup"><span data-stu-id="f266b-212">DisableConfiguringHistory</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableconfiguringhistory)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-213">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-214">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-214">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-215">DisableCrashDetection</span><span class="sxs-lookup"><span data-stu-id="f266b-215">DisableCrashDetection</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablecrashdetection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-216">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-217">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-217">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-218">DisableCustomerExperienceImprovementProgramParticipation</span><span class="sxs-lookup"><span data-stu-id="f266b-218">DisableCustomerExperienceImprovementProgramParticipation</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablecustomerexperienceimprovementprogramparticipation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-219">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-220">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-220">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-221">DisableDeletingUserVisitedWebsites</span><span class="sxs-lookup"><span data-stu-id="f266b-221">DisableDeletingUserVisitedWebsites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disabledeletinguservisitedwebsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-222">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-223">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-223">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-224">DisableEnclosureDownloading</span><span class="sxs-lookup"><span data-stu-id="f266b-224">DisableEnclosureDownloading</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableenclosuredownloading)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-225">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-226">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-226">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-227">DisableEncryptionSupport</span><span class="sxs-lookup"><span data-stu-id="f266b-227">DisableEncryptionSupport</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableencryptionsupport)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-228">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-228">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-229">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-229">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-230">DisableFirstRunWizard</span><span class="sxs-lookup"><span data-stu-id="f266b-230">DisableFirstRunWizard</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablefirstrunwizard)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-231">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-232">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-232">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-233">DisableFlipAheadFeature</span><span class="sxs-lookup"><span data-stu-id="f266b-233">DisableFlipAheadFeature</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableflipaheadfeature)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-234">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-234">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-235">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-235">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-236">DisableHomePageChange</span><span class="sxs-lookup"><span data-stu-id="f266b-236">DisableHomePageChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablehomepagechange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-237">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-238">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-238">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-239">DisableIgnoringCertificateErrors</span><span class="sxs-lookup"><span data-stu-id="f266b-239">DisableIgnoringCertificateErrors</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableignoringcertificateerrors)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-240">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-241">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-241">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-242">DisableInPrivateBrowsing</span><span class="sxs-lookup"><span data-stu-id="f266b-242">DisableInPrivateBrowsing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableinprivatebrowsing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-243">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-244">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-244">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-245">DisableProcessesInEnhancedProtectedMode</span><span class="sxs-lookup"><span data-stu-id="f266b-245">DisableProcessesInEnhancedProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableprocessesinenhancedprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-246">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-247">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-247">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-248">DisableProxyChange</span><span class="sxs-lookup"><span data-stu-id="f266b-248">DisableProxyChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableproxychange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-249">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-250">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-250">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-251">DisableSearchProviderChange</span><span class="sxs-lookup"><span data-stu-id="f266b-251">DisableSearchProviderChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesearchproviderchange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-252">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-253">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-253">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-254">DisableSecondaryHomePageChange</span><span class="sxs-lookup"><span data-stu-id="f266b-254">DisableSecondaryHomePageChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesecondaryhomepagechange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-255">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-256">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-256">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-257">DisableSecuritySettingsCheck</span><span class="sxs-lookup"><span data-stu-id="f266b-257">DisableSecuritySettingsCheck</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesecuritysettingscheck)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-258">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-259">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-259">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-260">DoNotAllowActiveXControlsInProtectedMode</span><span class="sxs-lookup"><span data-stu-id="f266b-260">DoNotAllowActiveXControlsInProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotallowactivexcontrolsinprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-261">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-262">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-262">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-263">DoNotBlockOutdatedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="f266b-263">DoNotBlockOutdatedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotblockoutdatedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-264">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-265">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-265">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-266">DoNotBlockOutdatedActiveXControlsOnSpecificDomains</span><span class="sxs-lookup"><span data-stu-id="f266b-266">DoNotBlockOutdatedActiveXControlsOnSpecificDomains</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotblockoutdatedactivexcontrolsonspecificdomains)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-267">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-267">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-268">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-268">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-269">IncludeAllLocalSites</span><span class="sxs-lookup"><span data-stu-id="f266b-269">IncludeAllLocalSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-includealllocalsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-270">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-270">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-271">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-271">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-272">IncludeAllNetworkPaths</span><span class="sxs-lookup"><span data-stu-id="f266b-272">IncludeAllNetworkPaths</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-includeallnetworkpaths)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-273">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-273">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-274">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-274">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f266b-275">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f266b-275">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-276">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-276">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-277">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f266b-277">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f266b-278">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f266b-278">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-279">InternetZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="f266b-279">InternetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-280">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-280">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-281">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-281">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-282">InternetZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="f266b-282">InternetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-283">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-283">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-284">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-284">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-285">InternetZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="f266b-285">InternetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-286">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-287">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-287">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-288">InternetZoneAllowCopyPasteViaScript</span><span class="sxs-lookup"><span data-stu-id="f266b-288">InternetZoneAllowCopyPasteViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowcopypasteviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-289">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-290">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-290">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-291">InternetZoneAllowDragAndDropCopyAndPasteFiles</span><span class="sxs-lookup"><span data-stu-id="f266b-291">InternetZoneAllowDragAndDropCopyAndPasteFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowdraganddropcopyandpastefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-292">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-293">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-293">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-294">InternetZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="f266b-294">InternetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-295">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-295">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-296">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-296">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-297">InternetZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="f266b-297">InternetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-298">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-298">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-299">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-299">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-300">InternetZoneAllowLoadingOfXAMLFiles</span><span class="sxs-lookup"><span data-stu-id="f266b-300">InternetZoneAllowLoadingOfXAMLFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowloadingofxamlfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-301">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-302">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-302">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-303">InternetZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="f266b-303">InternetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-304">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-305">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-305">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-306">InternetZoneAllowOnlyApprovedDomainsToUseActiveXControls</span><span class="sxs-lookup"><span data-stu-id="f266b-306">InternetZoneAllowOnlyApprovedDomainsToUseActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowonlyapproveddomainstouseactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-307">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-308">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-308">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-309">InternetZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span><span class="sxs-lookup"><span data-stu-id="f266b-309">InternetZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowonlyapproveddomainstousetdcactivexcontrol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-310">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-311">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-311">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-312">InternetZoneAllowScriptingOfInternetExplorerWebBrowserControls</span><span class="sxs-lookup"><span data-stu-id="f266b-312">InternetZoneAllowScriptingOfInternetExplorerWebBrowserControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptingofinternetexplorerwebbrowsercontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-313">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-314">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-314">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-315">InternetZoneAllowScriptInitiatedWindows</span><span class="sxs-lookup"><span data-stu-id="f266b-315">InternetZoneAllowScriptInitiatedWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptinitiatedwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-316">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-316">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-317">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-317">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-318">InternetZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="f266b-318">InternetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-319">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-320">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-320">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-321">InternetZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="f266b-321">InternetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-322">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-323">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-323">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-324">InternetZoneAllowUpdatesToStatusBarViaScript</span><span class="sxs-lookup"><span data-stu-id="f266b-324">InternetZoneAllowUpdatesToStatusBarViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowupdatestostatusbarviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-325">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-326">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-326">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-327">InternetZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="f266b-327">InternetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-328">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-328">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-329">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-329">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-330">InternetZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="f266b-330">InternetZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-331">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-331">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-332">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-332">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-333">InternetZoneDownloadSignedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="f266b-333">InternetZoneDownloadSignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedownloadsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-334">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-334">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-335">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-335">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-336">InternetZoneDownloadUnsignedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="f266b-336">InternetZoneDownloadUnsignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedownloadunsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-337">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-338">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-338">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-339">InternetZoneEnableCrossSiteScriptingFilter</span><span class="sxs-lookup"><span data-stu-id="f266b-339">InternetZoneEnableCrossSiteScriptingFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenablecrosssitescriptingfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-340">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-341">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-341">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-342">InternetZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span><span class="sxs-lookup"><span data-stu-id="f266b-342">InternetZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenabledraggingofcontentfromdifferentdomainsacrosswindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-343">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-343">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-344">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-344">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-345">InternetZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span><span class="sxs-lookup"><span data-stu-id="f266b-345">InternetZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenabledraggingofcontentfromdifferentdomainswithinwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-346">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-347">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-347">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-348">InternetZoneEnableMIMESniffing</span><span class="sxs-lookup"><span data-stu-id="f266b-348">InternetZoneEnableMIMESniffing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenablemimesniffing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-349">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-350">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-350">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-351">InternetZoneEnableProtectedMode</span><span class="sxs-lookup"><span data-stu-id="f266b-351">InternetZoneEnableProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenableprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-352">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-353">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-353">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-354">InternetZoneIncludeLocalPathWhenUploadingFilesToServer</span><span class="sxs-lookup"><span data-stu-id="f266b-354">InternetZoneIncludeLocalPathWhenUploadingFilesToServer</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneincludelocalpathwhenuploadingfilestoserver)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-355">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-356">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-356">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-357">InternetZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="f266b-357">InternetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-358">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-358">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-359">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-359">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-360">InternetZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="f266b-360">InternetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-361">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-362">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-362">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-363">InternetZoneLaunchingApplicationsAndFilesInIFRAME</span><span class="sxs-lookup"><span data-stu-id="f266b-363">InternetZoneLaunchingApplicationsAndFilesInIFRAME</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonelaunchingapplicationsandfilesiniframe)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-364">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-364">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-365">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-365">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-366">InternetZoneLogonOptions</span><span class="sxs-lookup"><span data-stu-id="f266b-366">InternetZoneLogonOptions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonelogonoptions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-367">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-367">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-368">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-368">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-369">InternetZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="f266b-369">InternetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-370">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-370">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-371">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-371">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f266b-372">InternetZoneRunNETFrameworkReliantComponentsNotSignedWithAuthenticode</span><span class="sxs-lookup"><span data-stu-id="f266b-372">InternetZoneRunNETFrameworkReliantComponentsNotSignedWithAuthenticode</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-373">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-373">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-374">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-374">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-375">InternetZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span><span class="sxs-lookup"><span data-stu-id="f266b-375">InternetZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonerunnetframeworkreliantcomponentssignedwithauthenticode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-376">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-376">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-377">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-377">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-378">InternetZoneShowSecurityWarningForPotentiallyUnsafeFiles</span><span class="sxs-lookup"><span data-stu-id="f266b-378">InternetZoneShowSecurityWarningForPotentiallyUnsafeFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneshowsecuritywarningforpotentiallyunsafefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-379">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-380">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-380">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-381">InternetZoneUsePopupBlocker</span><span class="sxs-lookup"><span data-stu-id="f266b-381">InternetZoneUsePopupBlocker</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneusepopupblocker)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-382">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-382">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-383">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-383">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f266b-384">InternetZoneWebsitesInLessPrivilegedZonesCanNavigateIntoThisZone</span><span class="sxs-lookup"><span data-stu-id="f266b-384">InternetZoneWebsitesInLessPrivilegedZonesCanNavigateIntoThisZone</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-385">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-385">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-386">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-386">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-387">IntranetZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="f266b-387">IntranetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-388">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-388">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-389">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-389">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-390">IntranetZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="f266b-390">IntranetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-391">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-391">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-392">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-392">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-393">IntranetZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="f266b-393">IntranetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-394">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-394">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-395">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-395">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-396">IntranetZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="f266b-396">IntranetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-397">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-397">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-398">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-398">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-399">IntranetZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="f266b-399">IntranetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-400">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-400">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-401">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-401">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-402">IntranetZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="f266b-402">IntranetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-403">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-403">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-404">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-404">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-405">IntranetZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="f266b-405">IntranetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-406">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-406">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-407">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-407">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-408">IntranetZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="f266b-408">IntranetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-409">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-409">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-410">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-410">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-411">IntranetZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="f266b-411">IntranetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-412">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-412">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-413">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-413">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-414">IntranetZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="f266b-414">IntranetZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-415">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-415">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-416">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-416">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-417">IntranetZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="f266b-417">IntranetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-418">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-418">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-419">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-419">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f266b-420">IntranetZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span><span class="sxs-lookup"><span data-stu-id="f266b-420">IntranetZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-421">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-421">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-422">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-422">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-423">IntranetZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="f266b-423">IntranetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-424">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-424">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-425">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-425">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-426">IntranetZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="f266b-426">IntranetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-427">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-427">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-428">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-428">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-429">LocalMachineZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="f266b-429">LocalMachineZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-430">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-430">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-431">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-431">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-432">LocalMachineZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="f266b-432">LocalMachineZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-433">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-433">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-434">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-434">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-435">LocalMachineZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="f266b-435">LocalMachineZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-436">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-436">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-437">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-437">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-438">LocalMachineZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="f266b-438">LocalMachineZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-439">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-439">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-440">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-440">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-441">LocalMachineZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="f266b-441">LocalMachineZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-442">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-442">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-443">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-443">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-444">LocalMachineZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="f266b-444">LocalMachineZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-445">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-445">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-446">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-446">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-447">LocalMachineZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="f266b-447">LocalMachineZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-448">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-448">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-449">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-449">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-450">LocalMachineZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="f266b-450">LocalMachineZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-451">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-451">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-452">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-452">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-453">LocalMachineZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="f266b-453">LocalMachineZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-454">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-454">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-455">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-455">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-456">LocalMachineZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="f266b-456">LocalMachineZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-457">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-457">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-458">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-458">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-459">LocalMachineZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="f266b-459">LocalMachineZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-460">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-460">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-461">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-461">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-462">LocalMachineZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="f266b-462">LocalMachineZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-463">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-463">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-464">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-464">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-465">LocalMachineZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="f266b-465">LocalMachineZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-466">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-466">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-467">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-467">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-468">LockedDownInternetZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="f266b-468">LockedDownInternetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-469">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-469">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-470">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-470">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-471">LockedDownInternetZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="f266b-471">LockedDownInternetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-472">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-472">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-473">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-473">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-474">LockedDownInternetZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="f266b-474">LockedDownInternetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-475">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-475">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-476">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-476">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-477">LockedDownInternetZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="f266b-477">LockedDownInternetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-478">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-478">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-479">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-479">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-480">LockedDownInternetZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="f266b-480">LockedDownInternetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-481">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-481">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-482">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-482">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-483">LockedDownInternetZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="f266b-483">LockedDownInternetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-484">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-484">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-485">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-485">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-486">LockedDownInternetZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="f266b-486">LockedDownInternetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-487">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-487">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-488">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-488">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-489">LockedDownInternetZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="f266b-489">LockedDownInternetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-490">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-490">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-491">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-491">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-492">LockedDownInternetZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="f266b-492">LockedDownInternetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-493">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-493">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-494">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-494">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-495">LockedDownInternetZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="f266b-495">LockedDownInternetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-496">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-496">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-497">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-497">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-498">LockedDownInternetZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="f266b-498">LockedDownInternetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-499">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-499">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-500">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-500">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-501">LockedDownInternetZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="f266b-501">LockedDownInternetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-502">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-502">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-503">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-503">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-504">LockedDownIntranetZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="f266b-504">LockedDownIntranetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-505">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-505">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-506">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-506">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-507">LockedDownIntranetZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="f266b-507">LockedDownIntranetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-508">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-508">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-509">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-509">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-510">LockedDownIntranetZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="f266b-510">LockedDownIntranetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-511">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-511">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-512">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-512">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-513">LockedDownIntranetZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="f266b-513">LockedDownIntranetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-514">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-514">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-515">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-515">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-516">LockedDownIntranetZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="f266b-516">LockedDownIntranetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-517">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-517">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-518">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-518">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-519">LockedDownIntranetZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="f266b-519">LockedDownIntranetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-520">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-520">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-521">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-521">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-522">LockedDownIntranetZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="f266b-522">LockedDownIntranetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-523">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-523">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-524">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-524">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-525">LockedDownIntranetZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="f266b-525">LockedDownIntranetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-526">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-526">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-527">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-527">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-528">LockedDownIntranetZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="f266b-528">LockedDownIntranetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-529">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-529">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-530">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-530">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-531">LockedDownIntranetZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="f266b-531">LockedDownIntranetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-532">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-532">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-533">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-533">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-534">LockedDownIntranetZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="f266b-534">LockedDownIntranetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-535">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-535">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-536">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-536">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-537">LockedDownLocalMachineZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="f266b-537">LockedDownLocalMachineZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-538">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-538">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-539">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-539">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-540">LockedDownLocalMachineZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="f266b-540">LockedDownLocalMachineZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-541">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-541">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-542">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-542">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-543">LockedDownLocalMachineZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="f266b-543">LockedDownLocalMachineZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-544">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-544">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-545">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-545">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-546">LockedDownLocalMachineZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="f266b-546">LockedDownLocalMachineZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-547">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-547">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-548">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-548">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-549">LockedDownLocalMachineZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="f266b-549">LockedDownLocalMachineZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-550">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-550">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-551">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-551">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-552">LockedDownLocalMachineZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="f266b-552">LockedDownLocalMachineZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-553">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-553">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-554">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-554">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-555">LockedDownLocalMachineZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="f266b-555">LockedDownLocalMachineZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-556">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-556">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-557">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-557">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-558">LockedDownLocalMachineZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="f266b-558">LockedDownLocalMachineZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-559">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-559">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-560">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-560">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-561">LockedDownLocalMachineZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="f266b-561">LockedDownLocalMachineZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-562">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-562">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-563">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-563">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-564">LockedDownLocalMachineZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="f266b-564">LockedDownLocalMachineZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-565">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-565">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-566">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-566">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-567">LockedDownLocalMachineZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="f266b-567">LockedDownLocalMachineZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-568">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-568">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-569">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-569">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-570">LockedDownLocalMachineZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="f266b-570">LockedDownLocalMachineZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-571">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-571">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-572">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-572">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-573">LockedDownRestrictedSitesZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="f266b-573">LockedDownRestrictedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-574">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-574">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-575">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-575">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-576">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="f266b-576">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-577">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-577">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-578">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-578">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-579">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="f266b-579">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-580">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-580">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-581">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-581">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-582">LockedDownRestrictedSitesZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="f266b-582">LockedDownRestrictedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-583">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-583">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-584">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-584">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-585">LockedDownRestrictedSitesZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="f266b-585">LockedDownRestrictedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-586">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-586">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-587">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-587">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-588">LockedDownRestrictedSitesZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="f266b-588">LockedDownRestrictedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-589">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-589">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-590">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-590">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-591">LockedDownRestrictedSitesZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="f266b-591">LockedDownRestrictedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-592">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-592">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-593">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-593">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-594">LockedDownRestrictedSitesZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="f266b-594">LockedDownRestrictedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-595">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-595">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-596">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-596">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-597">LockedDownRestrictedSitesZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="f266b-597">LockedDownRestrictedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-598">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-598">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-599">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-599">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-600">LockedDownRestrictedSitesZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="f266b-600">LockedDownRestrictedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-601">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-601">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-602">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-602">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-603">LockedDownRestrictedSitesZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="f266b-603">LockedDownRestrictedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-604">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-604">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-605">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-605">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-606">LockedDownRestrictedSitesZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="f266b-606">LockedDownRestrictedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-607">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-607">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-608">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-608">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-609">LockedDownTrustedSitesZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="f266b-609">LockedDownTrustedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-610">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-610">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-611">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-611">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-612">LockedDownTrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="f266b-612">LockedDownTrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-613">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-613">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-614">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-614">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-615">LockedDownTrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="f266b-615">LockedDownTrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-616">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-616">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-617">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-617">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-618">LockedDownTrustedSitesZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="f266b-618">LockedDownTrustedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-619">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-619">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-620">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-620">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-621">LockedDownTrustedSitesZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="f266b-621">LockedDownTrustedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-622">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-622">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-623">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-623">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-624">LockedDownTrustedSitesZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="f266b-624">LockedDownTrustedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-625">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-625">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-626">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-626">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-627">LockedDownTrustedSitesZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="f266b-627">LockedDownTrustedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-628">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-628">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-629">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-629">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-630">LockedDownTrustedSitesZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="f266b-630">LockedDownTrustedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-631">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-631">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-632">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-632">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-633">LockedDownTrustedSitesZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="f266b-633">LockedDownTrustedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-634">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-634">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-635">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-635">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-636">LockedDownTrustedSitesZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="f266b-636">LockedDownTrustedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-637">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-637">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-638">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-638">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-639">LockedDownTrustedSitesZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="f266b-639">LockedDownTrustedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-640">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-640">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-641">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-641">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-642">LockedDownTrustedSitesZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="f266b-642">LockedDownTrustedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-643">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-643">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-644">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-644">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-645">MimeSniffingSafetyFeatureInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="f266b-645">MimeSniffingSafetyFeatureInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-mimesniffingsafetyfeatureinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-646">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-646">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-647">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-647">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-648">MKProtocolSecurityRestrictionInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="f266b-648">MKProtocolSecurityRestrictionInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-mkprotocolsecurityrestrictioninternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-649">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-649">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-650">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-650">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-651">NotificationBarInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="f266b-651">NotificationBarInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-notificationbarinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-652">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-652">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-653">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-653">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f266b-654">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="f266b-654">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-655">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-655">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-656">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f266b-656">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f266b-657">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f266b-657">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-658">PreventManagingSmartScreenFilter</span><span class="sxs-lookup"><span data-stu-id="f266b-658">PreventManagingSmartScreenFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-preventmanagingsmartscreenfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-659">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-659">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-660">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-660">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-661">PreventPerUserInstallationOfActiveXControls</span><span class="sxs-lookup"><span data-stu-id="f266b-661">PreventPerUserInstallationOfActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-preventperuserinstallationofactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-662">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-662">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-663">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-663">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-664">ProtectionFromZoneElevationInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="f266b-664">ProtectionFromZoneElevationInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-protectionfromzoneelevationinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-665">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-665">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-666">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-666">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-667">RemoveRunThisTimeButtonForOutdatedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="f266b-667">RemoveRunThisTimeButtonForOutdatedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-removerunthistimebuttonforoutdatedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-668">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-668">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-669">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-669">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-670">RestrictActiveXInstallInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="f266b-670">RestrictActiveXInstallInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictactivexinstallinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-671">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-671">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-672">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-672">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-673">RestrictedSitesZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="f266b-673">RestrictedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-674">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-674">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-675">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-675">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-676">RestrictedSitesZoneAllowActiveScripting</span><span class="sxs-lookup"><span data-stu-id="f266b-676">RestrictedSitesZoneAllowActiveScripting</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowactivescripting)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-677">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-677">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-678">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-678">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-679">RestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="f266b-679">RestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-680">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-680">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-681">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-681">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-682">RestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="f266b-682">RestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-683">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-683">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-684">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-684">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-685">RestrictedSitesZoneAllowBinaryAndScriptBehaviors</span><span class="sxs-lookup"><span data-stu-id="f266b-685">RestrictedSitesZoneAllowBinaryAndScriptBehaviors</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowbinaryandscriptbehaviors)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-686">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-686">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-687">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-687">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-688">RestrictedSitesZoneAllowCopyPasteViaScript</span><span class="sxs-lookup"><span data-stu-id="f266b-688">RestrictedSitesZoneAllowCopyPasteViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowcopypasteviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-689">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-689">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-690">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-690">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-691">RestrictedSitesZoneAllowDragAndDropCopyAndPasteFiles</span><span class="sxs-lookup"><span data-stu-id="f266b-691">RestrictedSitesZoneAllowDragAndDropCopyAndPasteFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowdraganddropcopyandpastefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-692">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-692">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-693">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-693">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-694">RestrictedSitesZoneAllowFileDownloads</span><span class="sxs-lookup"><span data-stu-id="f266b-694">RestrictedSitesZoneAllowFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-695">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-695">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-696">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-696">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-697">RestrictedSitesZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="f266b-697">RestrictedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-698">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-698">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-699">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-699">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-700">RestrictedSitesZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="f266b-700">RestrictedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-701">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-701">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-702">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-702">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-703">RestrictedSitesZoneAllowLoadingOfXAMLFiles</span><span class="sxs-lookup"><span data-stu-id="f266b-703">RestrictedSitesZoneAllowLoadingOfXAMLFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowloadingofxamlfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-704">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-704">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-705">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-705">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-706">RestrictedSitesZoneAllowMETAREFRESH</span><span class="sxs-lookup"><span data-stu-id="f266b-706">RestrictedSitesZoneAllowMETAREFRESH</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowmetarefresh)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-707">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-707">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-708">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-708">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-709">RestrictedSitesZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="f266b-709">RestrictedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-710">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-710">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-711">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-711">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-712">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseActiveXControls</span><span class="sxs-lookup"><span data-stu-id="f266b-712">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowonlyapproveddomainstouseactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-713">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-713">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-714">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-714">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-715">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span><span class="sxs-lookup"><span data-stu-id="f266b-715">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowonlyapproveddomainstousetdcactivexcontrol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-716">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-716">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-717">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-717">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-718">RestrictedSitesZoneAllowScriptingOfInternetExplorerWebBrowserControls</span><span class="sxs-lookup"><span data-stu-id="f266b-718">RestrictedSitesZoneAllowScriptingOfInternetExplorerWebBrowserControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptingofinternetexplorerwebbrowsercontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-719">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-719">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-720">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-720">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-721">RestrictedSitesZoneAllowScriptInitiatedWindows</span><span class="sxs-lookup"><span data-stu-id="f266b-721">RestrictedSitesZoneAllowScriptInitiatedWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptinitiatedwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-722">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-722">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-723">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-723">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-724">RestrictedSitesZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="f266b-724">RestrictedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-725">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-725">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-726">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-726">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-727">RestrictedSitesZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="f266b-727">RestrictedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-728">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-728">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-729">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-729">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-730">RestrictedSitesZoneAllowUpdatesToStatusBarViaScript</span><span class="sxs-lookup"><span data-stu-id="f266b-730">RestrictedSitesZoneAllowUpdatesToStatusBarViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowupdatestostatusbarviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-731">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-731">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-732">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-732">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-733">RestrictedSitesZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="f266b-733">RestrictedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-734">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-734">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-735">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-735">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-736">RestrictedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="f266b-736">RestrictedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-737">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-737">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-738">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-738">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-739">RestrictedSitesZoneDownloadSignedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="f266b-739">RestrictedSitesZoneDownloadSignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedownloadsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-740">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-740">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-741">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-741">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-742">RestrictedSitesZoneDownloadUnsignedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="f266b-742">RestrictedSitesZoneDownloadUnsignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedownloadunsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-743">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-743">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-744">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-744">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-745">RestrictedSitesZoneEnableCrossSiteScriptingFilter</span><span class="sxs-lookup"><span data-stu-id="f266b-745">RestrictedSitesZoneEnableCrossSiteScriptingFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenablecrosssitescriptingfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-746">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-746">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-747">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-747">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-748">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span><span class="sxs-lookup"><span data-stu-id="f266b-748">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenabledraggingofcontentfromdifferentdomainsacrosswindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-749">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-749">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-750">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-750">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-751">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span><span class="sxs-lookup"><span data-stu-id="f266b-751">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenabledraggingofcontentfromdifferentdomainswithinwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-752">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-752">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-753">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-753">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-754">RestrictedSitesZoneEnableMIMESniffing</span><span class="sxs-lookup"><span data-stu-id="f266b-754">RestrictedSitesZoneEnableMIMESniffing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenablemimesniffing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-755">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-755">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-756">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-756">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-757">RestrictedSitesZoneIncludeLocalPathWhenUploadingFilesToServer</span><span class="sxs-lookup"><span data-stu-id="f266b-757">RestrictedSitesZoneIncludeLocalPathWhenUploadingFilesToServer</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneincludelocalpathwhenuploadingfilestoserver)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-758">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-758">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-759">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-759">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-760">RestrictedSitesZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="f266b-760">RestrictedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-761">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-761">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-762">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-762">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-763">RestrictedSitesZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="f266b-763">RestrictedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-764">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-764">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-765">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-765">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-766">RestrictedSitesZoneLaunchingApplicationsAndFilesInIFRAME</span><span class="sxs-lookup"><span data-stu-id="f266b-766">RestrictedSitesZoneLaunchingApplicationsAndFilesInIFRAME</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonelaunchingapplicationsandfilesiniframe)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-767">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-767">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-768">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-768">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-769">RestrictedSitesZoneLogonOptions</span><span class="sxs-lookup"><span data-stu-id="f266b-769">RestrictedSitesZoneLogonOptions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonelogonoptions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-770">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-770">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-771">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-771">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-772">RestrictedSitesZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="f266b-772">RestrictedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-773">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-773">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-774">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-774">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f266b-775">RestrictedSitesZoneNavigateWindowsAndFramesAcrossDomains</span><span class="sxs-lookup"><span data-stu-id="f266b-775">RestrictedSitesZoneNavigateWindowsAndFramesAcrossDomains</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-776">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-776">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-777">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-777">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-778">RestrictedSitesZoneRunActiveXControlsAndPlugins</span><span class="sxs-lookup"><span data-stu-id="f266b-778">RestrictedSitesZoneRunActiveXControlsAndPlugins</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonerunactivexcontrolsandplugins)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-779">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-779">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-780">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-780">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-781">RestrictedSitesZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span><span class="sxs-lookup"><span data-stu-id="f266b-781">RestrictedSitesZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonerunnetframeworkreliantcomponentssignedwithauthenticode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-782">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-782">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-783">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-783">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-784">RestrictedSitesZoneScriptActiveXControlsMarkedSafeForScripting</span><span class="sxs-lookup"><span data-stu-id="f266b-784">RestrictedSitesZoneScriptActiveXControlsMarkedSafeForScripting</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonescriptactivexcontrolsmarkedsafeforscripting)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-785">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-785">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-786">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-786">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-787">RestrictedSitesZoneScriptingOfJavaApplets</span><span class="sxs-lookup"><span data-stu-id="f266b-787">RestrictedSitesZoneScriptingOfJavaApplets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonescriptingofjavaapplets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-788">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-788">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-789">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-789">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-790">RestrictedSitesZoneShowSecurityWarningForPotentiallyUnsafeFiles</span><span class="sxs-lookup"><span data-stu-id="f266b-790">RestrictedSitesZoneShowSecurityWarningForPotentiallyUnsafeFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneshowsecuritywarningforpotentiallyunsafefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-791">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-791">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-792">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-792">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f266b-793">RestrictedSitesZoneTurnOnCrossSiteScriptingFilter</span><span class="sxs-lookup"><span data-stu-id="f266b-793">RestrictedSitesZoneTurnOnCrossSiteScriptingFilter</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-794">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-794">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-795">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-795">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-796">RestrictedSitesZoneTurnOnProtectedMode</span><span class="sxs-lookup"><span data-stu-id="f266b-796">RestrictedSitesZoneTurnOnProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneturnonprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-797">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-797">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-798">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-798">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-799">RestrictedSitesZoneUsePopupBlocker</span><span class="sxs-lookup"><span data-stu-id="f266b-799">RestrictedSitesZoneUsePopupBlocker</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneusepopupblocker)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-800">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-800">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-801">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-801">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-802">RestrictFileDownloadInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="f266b-802">RestrictFileDownloadInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictfiledownloadinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-803">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-803">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-804">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-804">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-805">ScriptedWindowSecurityRestrictionsInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="f266b-805">ScriptedWindowSecurityRestrictionsInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-scriptedwindowsecurityrestrictionsinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-806">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-806">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-807">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-807">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-808">SearchProviderList</span><span class="sxs-lookup"><span data-stu-id="f266b-808">SearchProviderList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-searchproviderlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-809">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-809">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-810">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-810">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-811">SpecifyUseOfActiveXInstallerService</span><span class="sxs-lookup"><span data-stu-id="f266b-811">SpecifyUseOfActiveXInstallerService</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-specifyuseofactivexinstallerservice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-812">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-812">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-813">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-813">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-814">TrustedSitesZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="f266b-814">TrustedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-815">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-815">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-816">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-816">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-817">TrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="f266b-817">TrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-818">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-818">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-819">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-819">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-820">TrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="f266b-820">TrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-821">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-821">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-822">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-822">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-823">TrustedSitesZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="f266b-823">TrustedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-824">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-824">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-825">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-825">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-826">TrustedSitesZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="f266b-826">TrustedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-827">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-827">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-828">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-828">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-829">TrustedSitesZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="f266b-829">TrustedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-830">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-830">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-831">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-831">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-832">TrustedSitesZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="f266b-832">TrustedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-833">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-833">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-834">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-834">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-835">TrustedSitesZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="f266b-835">TrustedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-836">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-836">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-837">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-837">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-838">TrustedSitesZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="f266b-838">TrustedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-839">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-839">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-840">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-840">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-841">TrustedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="f266b-841">TrustedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-842">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-842">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-843">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-843">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f266b-844">TrustedSitesZoneDontRunAntimalwareProgramsAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="f266b-844">TrustedSitesZoneDontRunAntimalwareProgramsAgainstActiveXControls</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-845">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-845">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-846">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-846">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-847">TrustedSitesZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="f266b-847">TrustedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-848">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-848">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-849">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-849">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f266b-850">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedAsSafe</span><span class="sxs-lookup"><span data-stu-id="f266b-850">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedAsSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-851">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-851">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-852">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-852">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f266b-853">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span><span class="sxs-lookup"><span data-stu-id="f266b-853">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-854">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-854">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-855">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-855">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-856">TrustedSitesZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="f266b-856">TrustedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-857">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-857">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-858">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-858">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f266b-859">TrustedSitesZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="f266b-859">TrustedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f266b-860">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f266b-860">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f266b-861">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f266b-861">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f266b-862">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f266b-862">Requirements</span></span>



| <span data-ttu-id="f266b-863">Requisito</span><span class="sxs-lookup"><span data-stu-id="f266b-863">Requirement</span></span> | <span data-ttu-id="f266b-864">Valor</span><span class="sxs-lookup"><span data-stu-id="f266b-864">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f266b-865">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f266b-865">Minimum supported client</span></span><br/> | <span data-ttu-id="f266b-866">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="f266b-866">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f266b-867">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f266b-867">Minimum supported server</span></span><br/> | <span data-ttu-id="f266b-868">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="f266b-868">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="f266b-869">Namespace</span><span class="sxs-lookup"><span data-stu-id="f266b-869">Namespace</span></span><br/>                | <span data-ttu-id="f266b-870">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="f266b-870">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="f266b-871">MOF</span><span class="sxs-lookup"><span data-stu-id="f266b-871">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f266b-872"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f266b-872"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="f266b-873">DLL</span><span class="sxs-lookup"><span data-stu-id="f266b-873">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f266b-874"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f266b-874"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

