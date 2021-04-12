---
title: Classe MDM_Policy_Config01_InternetExplorer02
description: A \_ classe Config01 InternetExplorer02 de política de MDM \_ \_ configura as políticas do Internet Explorer.
ms.assetid: 32cc6a64-3008-4add-96e8-33b31beb207f
keywords:
- Classe MDM_Policy_Config01_InternetExplorer02
- Classe MDM_Policy_Config01_InternetExplorer02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_InternetExplorer02
- MDM_Policy_Config01_InternetExplorer02.InstanceID
- MDM_Policy_Config01_InternetExplorer02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48a448b0034e3f4658f1c13b238abf455bf413a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455113"
---
# <a name="mdm_policy_config01_internetexplorer02-class"></a><span data-ttu-id="0d676-105">\_Classe MDM \_ Config01 \_ InternetExplorer02</span><span class="sxs-lookup"><span data-stu-id="0d676-105">MDM\_Policy\_Config01\_InternetExplorer02 class</span></span>

<span data-ttu-id="0d676-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="0d676-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="0d676-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="0d676-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="0d676-108">A \_ classe Config01 InternetExplorer02 de política de MDM \_ \_ configura as políticas do Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="0d676-108">The MDM\_Policy\_Config01\_InternetExplorer02 class configures the Internet Explorer policies.</span></span>

<span data-ttu-id="0d676-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="0d676-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d676-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0d676-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_InternetExplorer02
{
  string InstanceID;
  string ParentID;
  string AddSearchProvider;
  string AllowActiveXFiltering;
  string AllowAddOnList;
  string AllowDeletingBrowsingHistoryOnExit;
  string AllowCertificateAddressMismatchWarning;
  string AllowEnhancedProtectedMode;
  string AllowEnterpriseModeFromToolsMenu;
  string AllowEnterpriseModeSiteList;
  string AllowFallbackToSSL3;
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
  string DisableProcessesInEnhancedProtectedMode;
  string DisableInPrivateBrowsing;
  string DisableIgnoringCertificateErrors;
  string DisableProxyChange;
  string DisableSearchProviderChange;
  string DisableSecondaryHomePageChange;
  string DisableSecuritySettingsCheck;
  string DisableUpdateCheck;
  string DoNotAllowActiveXControlsInProtectedMode;
  string DoNotAllowUsersToAddSites;
  string DoNotAllowUsersToChangePolicies;
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
  string SecurityZonesUseOnlyMachineSettings;
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

## <a name="members"></a><span data-ttu-id="0d676-111">Membros</span><span class="sxs-lookup"><span data-stu-id="0d676-111">Members</span></span>

<span data-ttu-id="0d676-112">A **classe \_ \_ Config01 \_ InternetExplorer02 da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="0d676-112">The **MDM\_Policy\_Config01\_InternetExplorer02** class has these types of members:</span></span>

-   [<span data-ttu-id="0d676-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0d676-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0d676-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0d676-114">Properties</span></span>

<span data-ttu-id="0d676-115">A **classe \_ \_ Config01 \_ InternetExplorer02 da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="0d676-115">The **MDM\_Policy\_Config01\_InternetExplorer02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="0d676-116">AddSearchProvider</span><span class="sxs-lookup"><span data-stu-id="0d676-116">AddSearchProvider</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-addsearchprovider)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-119">AllowActiveXFiltering</span><span class="sxs-lookup"><span data-stu-id="0d676-119">AllowActiveXFiltering</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowactivexfiltering)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-122">AllowAddOnList</span><span class="sxs-lookup"><span data-stu-id="0d676-122">AllowAddOnList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowaddonlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-124">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-125">AllowCertificateAddressMismatchWarning</span><span class="sxs-lookup"><span data-stu-id="0d676-125">AllowCertificateAddressMismatchWarning</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowcertificateaddressmismatchwarning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-126">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-127">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-128">AllowDeletingBrowsingHistoryOnExit</span><span class="sxs-lookup"><span data-stu-id="0d676-128">AllowDeletingBrowsingHistoryOnExit</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowdeletingbrowsinghistoryonexit)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-130">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-131">AllowEnhancedProtectedMode</span><span class="sxs-lookup"><span data-stu-id="0d676-131">AllowEnhancedProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenhancedprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-132">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-133">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-134">AllowEnterpriseModeFromToolsMenu</span><span class="sxs-lookup"><span data-stu-id="0d676-134">AllowEnterpriseModeFromToolsMenu</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenterprisemodefromtoolsmenu)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-135">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-136">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-137">AllowEnterpriseModeSiteList</span><span class="sxs-lookup"><span data-stu-id="0d676-137">AllowEnterpriseModeSiteList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenterprisemodesitelist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-138">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-139">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-140">AllowFallbackToSSL3</span><span class="sxs-lookup"><span data-stu-id="0d676-140">AllowFallbackToSSL3</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowfallbacktossl3)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-141">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-142">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-143">AllowInternetExplorer7PolicyList</span><span class="sxs-lookup"><span data-stu-id="0d676-143">AllowInternetExplorer7PolicyList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetexplorer7policylist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-144">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-145">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-146">AllowInternetExplorerStandardsMode</span><span class="sxs-lookup"><span data-stu-id="0d676-146">AllowInternetExplorerStandardsMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetexplorerstandardsmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-147">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-148">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-149">AllowInternetZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="0d676-149">AllowInternetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-150">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-151">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-152">AllowIntranetZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="0d676-152">AllowIntranetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowintranetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-153">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-154">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-155">AllowLocalMachineZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="0d676-155">AllowLocalMachineZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlocalmachinezonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-156">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-157">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-158">AllowLockedDownInternetZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="0d676-158">AllowLockedDownInternetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddowninternetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-159">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-160">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-161">AllowLockedDownIntranetZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="0d676-161">AllowLockedDownIntranetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownintranetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-162">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-163">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-164">AllowLockedDownLocalMachineZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="0d676-164">AllowLockedDownLocalMachineZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownlocalmachinezonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-165">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-166">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-167">AllowLockedDownRestrictedSitesZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="0d676-167">AllowLockedDownRestrictedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownrestrictedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-168">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-169">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-170">AllowOneWordEntry</span><span class="sxs-lookup"><span data-stu-id="0d676-170">AllowOneWordEntry</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowonewordentry)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-171">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-172">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-173">AllowSiteToZoneAssignmentList</span><span class="sxs-lookup"><span data-stu-id="0d676-173">AllowSiteToZoneAssignmentList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsitetozoneassignmentlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-174">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-175">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-175">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-176">AllowsLockedDownTrustedSitesZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="0d676-176">AllowsLockedDownTrustedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowslockeddowntrustedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-177">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-178">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-178">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-179">AllowSoftwareWhenSignatureIsInvalid</span><span class="sxs-lookup"><span data-stu-id="0d676-179">AllowSoftwareWhenSignatureIsInvalid</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsoftwarewhensignatureisinvalid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-180">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-181">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-182">AllowsRestrictedSitesZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="0d676-182">AllowsRestrictedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsrestrictedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-183">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-184">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-184">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-185">AllowSuggestedSites</span><span class="sxs-lookup"><span data-stu-id="0d676-185">AllowSuggestedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsuggestedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-186">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-187">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-187">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-188">AllowTrustedSitesZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="0d676-188">AllowTrustedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowtrustedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-189">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-190">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-190">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-191">CheckServerCertificateRevocation</span><span class="sxs-lookup"><span data-stu-id="0d676-191">CheckServerCertificateRevocation</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-checkservercertificaterevocation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-192">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-193">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-193">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-194">CheckSignaturesOnDownloadedPrograms</span><span class="sxs-lookup"><span data-stu-id="0d676-194">CheckSignaturesOnDownloadedPrograms</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-checksignaturesondownloadedprograms)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-195">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-196">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-196">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-197">ConsistentMimeHandlingInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="0d676-197">ConsistentMimeHandlingInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-consistentmimehandlinginternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-198">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-199">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-199">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-200">DisableAdobeFlash</span><span class="sxs-lookup"><span data-stu-id="0d676-200">DisableAdobeFlash</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableadobeflash)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-201">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-202">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-202">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0d676-203">DisableBlockingOfOutdatedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0d676-203">DisableBlockingOfOutdatedActiveXControls</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-204">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-205">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-205">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-206">DisableBypassOfSmartScreenWarnings</span><span class="sxs-lookup"><span data-stu-id="0d676-206">DisableBypassOfSmartScreenWarnings</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablebypassofsmartscreenwarnings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-207">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-208">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-208">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-209">DisableBypassOfSmartScreenWarningsAboutUncommonFiles</span><span class="sxs-lookup"><span data-stu-id="0d676-209">DisableBypassOfSmartScreenWarningsAboutUncommonFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablebypassofsmartscreenwarningsaboutuncommonfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-210">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-211">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-211">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-212">DisableConfiguringHistory</span><span class="sxs-lookup"><span data-stu-id="0d676-212">DisableConfiguringHistory</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableconfiguringhistory)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-213">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-214">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-214">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-215">DisableCrashDetection</span><span class="sxs-lookup"><span data-stu-id="0d676-215">DisableCrashDetection</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablecrashdetection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-216">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-217">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-217">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-218">DisableCustomerExperienceImprovementProgramParticipation</span><span class="sxs-lookup"><span data-stu-id="0d676-218">DisableCustomerExperienceImprovementProgramParticipation</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablecustomerexperienceimprovementprogramparticipation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-219">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-220">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-220">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-221">DisableDeletingUserVisitedWebsites</span><span class="sxs-lookup"><span data-stu-id="0d676-221">DisableDeletingUserVisitedWebsites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disabledeletinguservisitedwebsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-222">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-223">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-223">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-224">DisableEnclosureDownloading</span><span class="sxs-lookup"><span data-stu-id="0d676-224">DisableEnclosureDownloading</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableenclosuredownloading)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-225">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-226">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-226">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-227">DisableEncryptionSupport</span><span class="sxs-lookup"><span data-stu-id="0d676-227">DisableEncryptionSupport</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableencryptionsupport)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-228">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-228">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-229">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-229">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-230">DisableFirstRunWizard</span><span class="sxs-lookup"><span data-stu-id="0d676-230">DisableFirstRunWizard</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablefirstrunwizard)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-231">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-232">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-232">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-233">DisableFlipAheadFeature</span><span class="sxs-lookup"><span data-stu-id="0d676-233">DisableFlipAheadFeature</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableflipaheadfeature)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-234">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-234">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-235">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-235">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-236">DisableIgnoringCertificateErrors</span><span class="sxs-lookup"><span data-stu-id="0d676-236">DisableIgnoringCertificateErrors</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableignoringcertificateerrors)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-237">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-238">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-238">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-239">DisableInPrivateBrowsing</span><span class="sxs-lookup"><span data-stu-id="0d676-239">DisableInPrivateBrowsing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableinprivatebrowsing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-240">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-241">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-241">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-242">DisableProcessesInEnhancedProtectedMode</span><span class="sxs-lookup"><span data-stu-id="0d676-242">DisableProcessesInEnhancedProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableprocessesinenhancedprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-243">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-244">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-244">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-245">DisableProxyChange</span><span class="sxs-lookup"><span data-stu-id="0d676-245">DisableProxyChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableproxychange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-246">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-247">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-247">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-248">DisableSearchProviderChange</span><span class="sxs-lookup"><span data-stu-id="0d676-248">DisableSearchProviderChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesearchproviderchange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-249">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-250">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-250">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-251">DisableSecondaryHomePageChange</span><span class="sxs-lookup"><span data-stu-id="0d676-251">DisableSecondaryHomePageChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesecondaryhomepagechange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-252">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-253">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-253">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-254">DisableSecuritySettingsCheck</span><span class="sxs-lookup"><span data-stu-id="0d676-254">DisableSecuritySettingsCheck</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesecuritysettingscheck)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-255">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-256">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-256">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-257">DisableUpdateCheck</span><span class="sxs-lookup"><span data-stu-id="0d676-257">DisableUpdateCheck</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableupdatecheck)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-258">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-259">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-259">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-260">DoNotAllowActiveXControlsInProtectedMode</span><span class="sxs-lookup"><span data-stu-id="0d676-260">DoNotAllowActiveXControlsInProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotallowactivexcontrolsinprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-261">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-262">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-262">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-263">DoNotAllowUsersToAddSites</span><span class="sxs-lookup"><span data-stu-id="0d676-263">DoNotAllowUsersToAddSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotallowuserstoaddsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-264">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-265">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-265">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-266">DoNotAllowUsersToChangePolicies</span><span class="sxs-lookup"><span data-stu-id="0d676-266">DoNotAllowUsersToChangePolicies</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotallowuserstochangepolicies)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-267">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-267">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-268">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-268">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-269">DoNotBlockOutdatedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0d676-269">DoNotBlockOutdatedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotblockoutdatedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-270">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-270">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-271">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-271">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-272">DoNotBlockOutdatedActiveXControlsOnSpecificDomains</span><span class="sxs-lookup"><span data-stu-id="0d676-272">DoNotBlockOutdatedActiveXControlsOnSpecificDomains</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotblockoutdatedactivexcontrolsonspecificdomains)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-273">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-273">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-274">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-274">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-275">IncludeAllLocalSites</span><span class="sxs-lookup"><span data-stu-id="0d676-275">IncludeAllLocalSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-includealllocalsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-276">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-276">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-277">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-277">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-278">IncludeAllNetworkPaths</span><span class="sxs-lookup"><span data-stu-id="0d676-278">IncludeAllNetworkPaths</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-includeallnetworkpaths)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-279">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-280">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-280">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0d676-281">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="0d676-281">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-282">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-282">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-283">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d676-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d676-284">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0d676-284">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-285">InternetZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="0d676-285">InternetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-286">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-287">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-287">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-288">InternetZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0d676-288">InternetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-289">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-290">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-290">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-291">InternetZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="0d676-291">InternetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-292">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-293">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-293">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-294">InternetZoneAllowCopyPasteViaScript</span><span class="sxs-lookup"><span data-stu-id="0d676-294">InternetZoneAllowCopyPasteViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowcopypasteviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-295">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-295">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-296">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-296">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-297">InternetZoneAllowDragAndDropCopyAndPasteFiles</span><span class="sxs-lookup"><span data-stu-id="0d676-297">InternetZoneAllowDragAndDropCopyAndPasteFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowdraganddropcopyandpastefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-298">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-298">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-299">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-299">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-300">InternetZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="0d676-300">InternetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-301">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-302">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-302">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-303">InternetZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="0d676-303">InternetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-304">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-305">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-305">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-306">InternetZoneAllowLoadingOfXAMLFiles</span><span class="sxs-lookup"><span data-stu-id="0d676-306">InternetZoneAllowLoadingOfXAMLFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowloadingofxamlfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-307">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-308">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-308">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-309">InternetZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="0d676-309">InternetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-310">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-311">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-311">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-312">InternetZoneAllowOnlyApprovedDomainsToUseActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0d676-312">InternetZoneAllowOnlyApprovedDomainsToUseActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowonlyapproveddomainstouseactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-313">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-314">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-314">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-315">InternetZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span><span class="sxs-lookup"><span data-stu-id="0d676-315">InternetZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowonlyapproveddomainstousetdcactivexcontrol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-316">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-316">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-317">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-317">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-318">InternetZoneAllowScriptingOfInternetExplorerWebBrowserControls</span><span class="sxs-lookup"><span data-stu-id="0d676-318">InternetZoneAllowScriptingOfInternetExplorerWebBrowserControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptingofinternetexplorerwebbrowsercontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-319">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-320">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-320">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-321">InternetZoneAllowScriptInitiatedWindows</span><span class="sxs-lookup"><span data-stu-id="0d676-321">InternetZoneAllowScriptInitiatedWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptinitiatedwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-322">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-323">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-323">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-324">InternetZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="0d676-324">InternetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-325">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-326">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-326">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-327">InternetZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="0d676-327">InternetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-328">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-328">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-329">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-329">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-330">InternetZoneAllowUpdatesToStatusBarViaScript</span><span class="sxs-lookup"><span data-stu-id="0d676-330">InternetZoneAllowUpdatesToStatusBarViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowupdatestostatusbarviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-331">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-331">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-332">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-332">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-333">InternetZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="0d676-333">InternetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-334">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-334">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-335">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-335">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-336">InternetZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0d676-336">InternetZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-337">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-338">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-338">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-339">InternetZoneDownloadSignedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0d676-339">InternetZoneDownloadSignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedownloadsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-340">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-341">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-341">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-342">InternetZoneDownloadUnsignedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0d676-342">InternetZoneDownloadUnsignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedownloadunsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-343">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-343">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-344">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-344">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-345">InternetZoneEnableCrossSiteScriptingFilter</span><span class="sxs-lookup"><span data-stu-id="0d676-345">InternetZoneEnableCrossSiteScriptingFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenablecrosssitescriptingfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-346">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-347">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-347">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-348">InternetZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span><span class="sxs-lookup"><span data-stu-id="0d676-348">InternetZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenabledraggingofcontentfromdifferentdomainsacrosswindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-349">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-350">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-350">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-351">InternetZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span><span class="sxs-lookup"><span data-stu-id="0d676-351">InternetZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenabledraggingofcontentfromdifferentdomainswithinwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-352">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-353">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-353">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-354">InternetZoneEnableMIMESniffing</span><span class="sxs-lookup"><span data-stu-id="0d676-354">InternetZoneEnableMIMESniffing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenablemimesniffing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-355">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-356">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-356">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-357">InternetZoneEnableProtectedMode</span><span class="sxs-lookup"><span data-stu-id="0d676-357">InternetZoneEnableProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenableprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-358">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-358">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-359">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-359">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-360">InternetZoneIncludeLocalPathWhenUploadingFilesToServer</span><span class="sxs-lookup"><span data-stu-id="0d676-360">InternetZoneIncludeLocalPathWhenUploadingFilesToServer</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneincludelocalpathwhenuploadingfilestoserver)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-361">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-362">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-362">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-363">InternetZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0d676-363">InternetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-364">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-364">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-365">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-365">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-366">InternetZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="0d676-366">InternetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-367">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-367">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-368">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-368">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-369">InternetZoneLaunchingApplicationsAndFilesInIFRAME</span><span class="sxs-lookup"><span data-stu-id="0d676-369">InternetZoneLaunchingApplicationsAndFilesInIFRAME</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonelaunchingapplicationsandfilesiniframe)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-370">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-370">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-371">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-371">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-372">InternetZoneLogonOptions</span><span class="sxs-lookup"><span data-stu-id="0d676-372">InternetZoneLogonOptions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonelogonoptions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-373">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-373">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-374">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-374">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-375">InternetZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="0d676-375">InternetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-376">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-376">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-377">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-377">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0d676-378">InternetZoneRunNETFrameworkReliantComponentsNotSignedWithAuthenticode</span><span class="sxs-lookup"><span data-stu-id="0d676-378">InternetZoneRunNETFrameworkReliantComponentsNotSignedWithAuthenticode</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-379">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-380">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-380">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-381">InternetZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span><span class="sxs-lookup"><span data-stu-id="0d676-381">InternetZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonerunnetframeworkreliantcomponentssignedwithauthenticode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-382">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-382">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-383">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-383">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-384">InternetZoneShowSecurityWarningForPotentiallyUnsafeFiles</span><span class="sxs-lookup"><span data-stu-id="0d676-384">InternetZoneShowSecurityWarningForPotentiallyUnsafeFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneshowsecuritywarningforpotentiallyunsafefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-385">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-385">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-386">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-386">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-387">InternetZoneUsePopupBlocker</span><span class="sxs-lookup"><span data-stu-id="0d676-387">InternetZoneUsePopupBlocker</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneusepopupblocker)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-388">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-388">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-389">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-389">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0d676-390">InternetZoneWebsitesInLessPrivilegedZonesCanNavigateIntoThisZone</span><span class="sxs-lookup"><span data-stu-id="0d676-390">InternetZoneWebsitesInLessPrivilegedZonesCanNavigateIntoThisZone</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-391">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-391">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-392">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-392">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-393">IntranetZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="0d676-393">IntranetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-394">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-394">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-395">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-395">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-396">IntranetZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0d676-396">IntranetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-397">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-397">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-398">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-398">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-399">IntranetZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="0d676-399">IntranetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-400">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-400">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-401">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-401">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-402">IntranetZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="0d676-402">IntranetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-403">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-403">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-404">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-404">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-405">IntranetZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="0d676-405">IntranetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-406">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-406">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-407">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-407">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-408">IntranetZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="0d676-408">IntranetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-409">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-409">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-410">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-410">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-411">IntranetZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="0d676-411">IntranetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-412">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-412">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-413">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-413">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-414">IntranetZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="0d676-414">IntranetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-415">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-415">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-416">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-416">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-417">IntranetZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="0d676-417">IntranetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-418">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-418">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-419">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-419">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-420">IntranetZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0d676-420">IntranetZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-421">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-421">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-422">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-422">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-423">IntranetZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0d676-423">IntranetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-424">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-424">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-425">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-425">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0d676-426">IntranetZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span><span class="sxs-lookup"><span data-stu-id="0d676-426">IntranetZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-427">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-427">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-428">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-428">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-429">IntranetZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="0d676-429">IntranetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-430">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-430">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-431">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-431">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-432">IntranetZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="0d676-432">IntranetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-433">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-433">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-434">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-434">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-435">LocalMachineZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="0d676-435">LocalMachineZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-436">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-436">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-437">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-437">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-438">LocalMachineZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0d676-438">LocalMachineZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-439">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-439">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-440">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-440">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-441">LocalMachineZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="0d676-441">LocalMachineZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-442">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-442">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-443">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-443">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-444">LocalMachineZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="0d676-444">LocalMachineZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-445">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-445">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-446">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-446">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-447">LocalMachineZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="0d676-447">LocalMachineZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-448">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-448">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-449">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-449">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-450">LocalMachineZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="0d676-450">LocalMachineZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-451">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-451">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-452">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-452">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-453">LocalMachineZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="0d676-453">LocalMachineZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-454">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-454">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-455">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-455">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-456">LocalMachineZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="0d676-456">LocalMachineZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-457">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-457">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-458">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-458">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-459">LocalMachineZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="0d676-459">LocalMachineZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-460">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-460">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-461">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-461">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-462">LocalMachineZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0d676-462">LocalMachineZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-463">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-463">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-464">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-464">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-465">LocalMachineZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0d676-465">LocalMachineZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-466">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-466">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-467">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-467">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-468">LocalMachineZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="0d676-468">LocalMachineZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-469">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-469">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-470">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-470">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-471">LocalMachineZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="0d676-471">LocalMachineZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-472">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-472">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-473">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-473">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-474">LockedDownInternetZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="0d676-474">LockedDownInternetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-475">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-475">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-476">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-476">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-477">LockedDownInternetZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0d676-477">LockedDownInternetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-478">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-478">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-479">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-479">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-480">LockedDownInternetZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="0d676-480">LockedDownInternetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-481">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-481">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-482">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-482">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-483">LockedDownInternetZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="0d676-483">LockedDownInternetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-484">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-484">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-485">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-485">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-486">LockedDownInternetZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="0d676-486">LockedDownInternetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-487">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-487">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-488">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-488">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-489">LockedDownInternetZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="0d676-489">LockedDownInternetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-490">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-490">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-491">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-491">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-492">LockedDownInternetZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="0d676-492">LockedDownInternetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-493">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-493">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-494">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-494">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-495">LockedDownInternetZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="0d676-495">LockedDownInternetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-496">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-496">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-497">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-497">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-498">LockedDownInternetZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="0d676-498">LockedDownInternetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-499">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-499">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-500">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-500">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-501">LockedDownInternetZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0d676-501">LockedDownInternetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-502">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-502">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-503">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-503">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-504">LockedDownInternetZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="0d676-504">LockedDownInternetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-505">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-505">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-506">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-506">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-507">LockedDownInternetZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="0d676-507">LockedDownInternetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-508">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-508">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-509">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-509">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-510">LockedDownIntranetZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="0d676-510">LockedDownIntranetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-511">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-511">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-512">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-512">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-513">LockedDownIntranetZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0d676-513">LockedDownIntranetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-514">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-514">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-515">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-515">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-516">LockedDownIntranetZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="0d676-516">LockedDownIntranetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-517">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-517">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-518">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-518">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-519">LockedDownIntranetZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="0d676-519">LockedDownIntranetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-520">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-520">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-521">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-521">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-522">LockedDownIntranetZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="0d676-522">LockedDownIntranetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-523">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-523">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-524">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-524">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-525">LockedDownIntranetZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="0d676-525">LockedDownIntranetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-526">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-526">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-527">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-527">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-528">LockedDownIntranetZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="0d676-528">LockedDownIntranetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-529">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-529">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-530">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-530">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-531">LockedDownIntranetZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="0d676-531">LockedDownIntranetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-532">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-532">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-533">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-533">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-534">LockedDownIntranetZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="0d676-534">LockedDownIntranetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-535">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-535">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-536">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-536">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-537">LockedDownIntranetZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0d676-537">LockedDownIntranetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-538">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-538">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-539">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-539">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-540">LockedDownIntranetZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="0d676-540">LockedDownIntranetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-541">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-541">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-542">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-542">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-543">LockedDownLocalMachineZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="0d676-543">LockedDownLocalMachineZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-544">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-544">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-545">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-545">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-546">LockedDownLocalMachineZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0d676-546">LockedDownLocalMachineZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-547">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-547">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-548">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-548">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-549">LockedDownLocalMachineZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="0d676-549">LockedDownLocalMachineZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-550">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-550">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-551">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-551">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-552">LockedDownLocalMachineZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="0d676-552">LockedDownLocalMachineZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-553">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-553">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-554">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-554">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-555">LockedDownLocalMachineZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="0d676-555">LockedDownLocalMachineZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-556">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-556">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-557">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-557">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-558">LockedDownLocalMachineZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="0d676-558">LockedDownLocalMachineZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-559">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-559">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-560">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-560">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-561">LockedDownLocalMachineZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="0d676-561">LockedDownLocalMachineZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-562">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-562">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-563">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-563">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-564">LockedDownLocalMachineZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="0d676-564">LockedDownLocalMachineZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-565">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-565">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-566">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-566">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-567">LockedDownLocalMachineZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="0d676-567">LockedDownLocalMachineZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-568">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-568">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-569">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-569">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-570">LockedDownLocalMachineZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0d676-570">LockedDownLocalMachineZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-571">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-571">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-572">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-572">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-573">LockedDownLocalMachineZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="0d676-573">LockedDownLocalMachineZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-574">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-574">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-575">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-575">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-576">LockedDownLocalMachineZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="0d676-576">LockedDownLocalMachineZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-577">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-577">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-578">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-578">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-579">LockedDownRestrictedSitesZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="0d676-579">LockedDownRestrictedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-580">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-580">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-581">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-581">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-582">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0d676-582">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-583">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-583">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-584">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-584">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-585">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="0d676-585">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-586">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-586">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-587">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-587">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-588">LockedDownRestrictedSitesZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="0d676-588">LockedDownRestrictedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-589">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-589">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-590">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-590">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-591">LockedDownRestrictedSitesZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="0d676-591">LockedDownRestrictedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-592">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-592">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-593">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-593">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-594">LockedDownRestrictedSitesZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="0d676-594">LockedDownRestrictedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-595">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-595">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-596">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-596">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-597">LockedDownRestrictedSitesZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="0d676-597">LockedDownRestrictedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-598">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-598">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-599">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-599">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-600">LockedDownRestrictedSitesZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="0d676-600">LockedDownRestrictedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-601">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-601">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-602">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-602">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-603">LockedDownRestrictedSitesZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="0d676-603">LockedDownRestrictedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-604">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-604">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-605">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-605">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-606">LockedDownRestrictedSitesZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0d676-606">LockedDownRestrictedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-607">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-607">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-608">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-608">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-609">LockedDownRestrictedSitesZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="0d676-609">LockedDownRestrictedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-610">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-610">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-611">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-611">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-612">LockedDownRestrictedSitesZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="0d676-612">LockedDownRestrictedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-613">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-613">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-614">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-614">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-615">LockedDownTrustedSitesZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="0d676-615">LockedDownTrustedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-616">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-616">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-617">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-617">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-618">LockedDownTrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0d676-618">LockedDownTrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-619">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-619">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-620">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-620">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-621">LockedDownTrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="0d676-621">LockedDownTrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-622">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-622">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-623">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-623">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-624">LockedDownTrustedSitesZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="0d676-624">LockedDownTrustedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-625">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-625">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-626">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-626">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-627">LockedDownTrustedSitesZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="0d676-627">LockedDownTrustedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-628">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-628">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-629">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-629">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-630">LockedDownTrustedSitesZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="0d676-630">LockedDownTrustedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-631">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-631">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-632">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-632">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-633">LockedDownTrustedSitesZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="0d676-633">LockedDownTrustedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-634">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-634">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-635">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-635">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-636">LockedDownTrustedSitesZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="0d676-636">LockedDownTrustedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-637">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-637">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-638">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-638">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-639">LockedDownTrustedSitesZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="0d676-639">LockedDownTrustedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-640">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-640">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-641">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-641">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-642">LockedDownTrustedSitesZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0d676-642">LockedDownTrustedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-643">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-643">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-644">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-644">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-645">LockedDownTrustedSitesZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="0d676-645">LockedDownTrustedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-646">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-646">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-647">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-647">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-648">LockedDownTrustedSitesZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="0d676-648">LockedDownTrustedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-649">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-649">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-650">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-650">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-651">MimeSniffingSafetyFeatureInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="0d676-651">MimeSniffingSafetyFeatureInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-mimesniffingsafetyfeatureinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-652">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-652">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-653">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-653">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-654">MKProtocolSecurityRestrictionInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="0d676-654">MKProtocolSecurityRestrictionInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-mkprotocolsecurityrestrictioninternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-655">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-655">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-656">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-656">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-657">NotificationBarInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="0d676-657">NotificationBarInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-notificationbarinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-658">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-658">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-659">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-659">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0d676-660">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="0d676-660">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-661">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-661">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-662">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d676-662">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d676-663">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0d676-663">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-664">PreventManagingSmartScreenFilter</span><span class="sxs-lookup"><span data-stu-id="0d676-664">PreventManagingSmartScreenFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-preventmanagingsmartscreenfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-665">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-665">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-666">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-666">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-667">PreventPerUserInstallationOfActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0d676-667">PreventPerUserInstallationOfActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-preventperuserinstallationofactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-668">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-668">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-669">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-669">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-670">ProtectionFromZoneElevationInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="0d676-670">ProtectionFromZoneElevationInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-protectionfromzoneelevationinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-671">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-671">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-672">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-672">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-673">RemoveRunThisTimeButtonForOutdatedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0d676-673">RemoveRunThisTimeButtonForOutdatedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-removerunthistimebuttonforoutdatedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-674">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-674">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-675">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-675">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-676">RestrictActiveXInstallInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="0d676-676">RestrictActiveXInstallInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictactivexinstallinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-677">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-677">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-678">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-678">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-679">RestrictedSitesZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="0d676-679">RestrictedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-680">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-680">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-681">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-681">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-682">RestrictedSitesZoneAllowActiveScripting</span><span class="sxs-lookup"><span data-stu-id="0d676-682">RestrictedSitesZoneAllowActiveScripting</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowactivescripting)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-683">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-683">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-684">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-684">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-685">RestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0d676-685">RestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-686">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-686">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-687">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-687">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-688">RestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="0d676-688">RestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-689">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-689">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-690">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-690">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-691">RestrictedSitesZoneAllowBinaryAndScriptBehaviors</span><span class="sxs-lookup"><span data-stu-id="0d676-691">RestrictedSitesZoneAllowBinaryAndScriptBehaviors</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowbinaryandscriptbehaviors)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-692">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-692">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-693">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-693">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-694">RestrictedSitesZoneAllowCopyPasteViaScript</span><span class="sxs-lookup"><span data-stu-id="0d676-694">RestrictedSitesZoneAllowCopyPasteViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowcopypasteviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-695">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-695">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-696">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-696">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-697">RestrictedSitesZoneAllowDragAndDropCopyAndPasteFiles</span><span class="sxs-lookup"><span data-stu-id="0d676-697">RestrictedSitesZoneAllowDragAndDropCopyAndPasteFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowdraganddropcopyandpastefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-698">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-698">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-699">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-699">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-700">RestrictedSitesZoneAllowFileDownloads</span><span class="sxs-lookup"><span data-stu-id="0d676-700">RestrictedSitesZoneAllowFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-701">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-701">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-702">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-702">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-703">RestrictedSitesZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="0d676-703">RestrictedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-704">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-704">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-705">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-705">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-706">RestrictedSitesZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="0d676-706">RestrictedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-707">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-707">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-708">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-708">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-709">RestrictedSitesZoneAllowLoadingOfXAMLFiles</span><span class="sxs-lookup"><span data-stu-id="0d676-709">RestrictedSitesZoneAllowLoadingOfXAMLFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowloadingofxamlfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-710">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-710">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-711">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-711">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-712">RestrictedSitesZoneAllowMETAREFRESH</span><span class="sxs-lookup"><span data-stu-id="0d676-712">RestrictedSitesZoneAllowMETAREFRESH</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowmetarefresh)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-713">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-713">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-714">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-714">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-715">RestrictedSitesZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="0d676-715">RestrictedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-716">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-716">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-717">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-717">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-718">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0d676-718">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowonlyapproveddomainstouseactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-719">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-719">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-720">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-720">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-721">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span><span class="sxs-lookup"><span data-stu-id="0d676-721">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowonlyapproveddomainstousetdcactivexcontrol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-722">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-722">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-723">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-723">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-724">RestrictedSitesZoneAllowScriptingOfInternetExplorerWebBrowserControls</span><span class="sxs-lookup"><span data-stu-id="0d676-724">RestrictedSitesZoneAllowScriptingOfInternetExplorerWebBrowserControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptingofinternetexplorerwebbrowsercontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-725">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-725">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-726">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-726">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-727">RestrictedSitesZoneAllowScriptInitiatedWindows</span><span class="sxs-lookup"><span data-stu-id="0d676-727">RestrictedSitesZoneAllowScriptInitiatedWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptinitiatedwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-728">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-728">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-729">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-729">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-730">RestrictedSitesZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="0d676-730">RestrictedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-731">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-731">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-732">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-732">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-733">RestrictedSitesZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="0d676-733">RestrictedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-734">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-734">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-735">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-735">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-736">RestrictedSitesZoneAllowUpdatesToStatusBarViaScript</span><span class="sxs-lookup"><span data-stu-id="0d676-736">RestrictedSitesZoneAllowUpdatesToStatusBarViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowupdatestostatusbarviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-737">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-737">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-738">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-738">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-739">RestrictedSitesZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="0d676-739">RestrictedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-740">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-740">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-741">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-741">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-742">RestrictedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0d676-742">RestrictedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-743">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-743">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-744">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-744">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-745">RestrictedSitesZoneDownloadSignedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0d676-745">RestrictedSitesZoneDownloadSignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedownloadsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-746">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-746">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-747">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-747">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-748">RestrictedSitesZoneDownloadUnsignedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0d676-748">RestrictedSitesZoneDownloadUnsignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedownloadunsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-749">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-749">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-750">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-750">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-751">RestrictedSitesZoneEnableCrossSiteScriptingFilter</span><span class="sxs-lookup"><span data-stu-id="0d676-751">RestrictedSitesZoneEnableCrossSiteScriptingFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenablecrosssitescriptingfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-752">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-752">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-753">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-753">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-754">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span><span class="sxs-lookup"><span data-stu-id="0d676-754">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenabledraggingofcontentfromdifferentdomainsacrosswindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-755">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-755">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-756">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-756">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-757">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span><span class="sxs-lookup"><span data-stu-id="0d676-757">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenabledraggingofcontentfromdifferentdomainswithinwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-758">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-758">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-759">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-759">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-760">RestrictedSitesZoneEnableMIMESniffing</span><span class="sxs-lookup"><span data-stu-id="0d676-760">RestrictedSitesZoneEnableMIMESniffing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenablemimesniffing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-761">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-761">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-762">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-762">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-763">RestrictedSitesZoneIncludeLocalPathWhenUploadingFilesToServer</span><span class="sxs-lookup"><span data-stu-id="0d676-763">RestrictedSitesZoneIncludeLocalPathWhenUploadingFilesToServer</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneincludelocalpathwhenuploadingfilestoserver)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-764">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-764">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-765">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-765">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-766">RestrictedSitesZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0d676-766">RestrictedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-767">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-767">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-768">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-768">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-769">RestrictedSitesZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="0d676-769">RestrictedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-770">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-770">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-771">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-771">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-772">RestrictedSitesZoneLaunchingApplicationsAndFilesInIFRAME</span><span class="sxs-lookup"><span data-stu-id="0d676-772">RestrictedSitesZoneLaunchingApplicationsAndFilesInIFRAME</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonelaunchingapplicationsandfilesiniframe)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-773">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-773">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-774">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-774">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-775">RestrictedSitesZoneLogonOptions</span><span class="sxs-lookup"><span data-stu-id="0d676-775">RestrictedSitesZoneLogonOptions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonelogonoptions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-776">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-776">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-777">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-777">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-778">RestrictedSitesZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="0d676-778">RestrictedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-779">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-779">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-780">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-780">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0d676-781">RestrictedSitesZoneNavigateWindowsAndFramesAcrossDomains</span><span class="sxs-lookup"><span data-stu-id="0d676-781">RestrictedSitesZoneNavigateWindowsAndFramesAcrossDomains</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-782">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-782">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-783">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-783">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-784">RestrictedSitesZoneRunActiveXControlsAndPlugins</span><span class="sxs-lookup"><span data-stu-id="0d676-784">RestrictedSitesZoneRunActiveXControlsAndPlugins</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonerunactivexcontrolsandplugins)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-785">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-785">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-786">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-786">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-787">RestrictedSitesZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span><span class="sxs-lookup"><span data-stu-id="0d676-787">RestrictedSitesZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonerunnetframeworkreliantcomponentssignedwithauthenticode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-788">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-788">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-789">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-789">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-790">RestrictedSitesZoneScriptActiveXControlsMarkedSafeForScripting</span><span class="sxs-lookup"><span data-stu-id="0d676-790">RestrictedSitesZoneScriptActiveXControlsMarkedSafeForScripting</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonescriptactivexcontrolsmarkedsafeforscripting)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-791">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-791">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-792">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-792">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-793">RestrictedSitesZoneScriptingOfJavaApplets</span><span class="sxs-lookup"><span data-stu-id="0d676-793">RestrictedSitesZoneScriptingOfJavaApplets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonescriptingofjavaapplets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-794">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-794">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-795">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-795">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-796">RestrictedSitesZoneShowSecurityWarningForPotentiallyUnsafeFiles</span><span class="sxs-lookup"><span data-stu-id="0d676-796">RestrictedSitesZoneShowSecurityWarningForPotentiallyUnsafeFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneshowsecuritywarningforpotentiallyunsafefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-797">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-797">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-798">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-798">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0d676-799">RestrictedSitesZoneTurnOnCrossSiteScriptingFilter</span><span class="sxs-lookup"><span data-stu-id="0d676-799">RestrictedSitesZoneTurnOnCrossSiteScriptingFilter</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-800">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-800">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-801">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-801">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-802">RestrictedSitesZoneTurnOnProtectedMode</span><span class="sxs-lookup"><span data-stu-id="0d676-802">RestrictedSitesZoneTurnOnProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneturnonprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-803">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-803">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-804">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-804">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-805">RestrictedSitesZoneUsePopupBlocker</span><span class="sxs-lookup"><span data-stu-id="0d676-805">RestrictedSitesZoneUsePopupBlocker</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneusepopupblocker)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-806">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-806">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-807">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-807">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-808">RestrictFileDownloadInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="0d676-808">RestrictFileDownloadInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictfiledownloadinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-809">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-809">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-810">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-810">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-811">ScriptedWindowSecurityRestrictionsInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="0d676-811">ScriptedWindowSecurityRestrictionsInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-scriptedwindowsecurityrestrictionsinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-812">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-812">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-813">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-813">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-814">SearchProviderList</span><span class="sxs-lookup"><span data-stu-id="0d676-814">SearchProviderList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-searchproviderlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-815">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-815">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-816">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-816">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-817">SecurityZonesUseOnlyMachineSettings</span><span class="sxs-lookup"><span data-stu-id="0d676-817">SecurityZonesUseOnlyMachineSettings</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-securityzonesuseonlymachinesettings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-818">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-818">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-819">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-819">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-820">SpecifyUseOfActiveXInstallerService</span><span class="sxs-lookup"><span data-stu-id="0d676-820">SpecifyUseOfActiveXInstallerService</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-specifyuseofactivexinstallerservice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-821">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-821">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-822">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-822">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-823">TrustedSitesZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="0d676-823">TrustedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-824">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-824">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-825">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-825">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-826">TrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0d676-826">TrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-827">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-827">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-828">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-828">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-829">TrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="0d676-829">TrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-830">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-830">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-831">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-831">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-832">TrustedSitesZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="0d676-832">TrustedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-833">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-833">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-834">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-834">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-835">TrustedSitesZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="0d676-835">TrustedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-836">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-836">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-837">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-837">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-838">TrustedSitesZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="0d676-838">TrustedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-839">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-839">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-840">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-840">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-841">TrustedSitesZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="0d676-841">TrustedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-842">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-842">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-843">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-843">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-844">TrustedSitesZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="0d676-844">TrustedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-845">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-845">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-846">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-846">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-847">TrustedSitesZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="0d676-847">TrustedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-848">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-848">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-849">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-849">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-850">TrustedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0d676-850">TrustedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-851">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-851">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-852">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-852">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0d676-853">TrustedSitesZoneDontRunAntimalwareProgramsAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0d676-853">TrustedSitesZoneDontRunAntimalwareProgramsAgainstActiveXControls</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-854">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-854">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-855">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-855">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-856">TrustedSitesZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0d676-856">TrustedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-857">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-857">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-858">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-858">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0d676-859">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedAsSafe</span><span class="sxs-lookup"><span data-stu-id="0d676-859">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedAsSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-860">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-860">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-861">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-861">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0d676-862">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span><span class="sxs-lookup"><span data-stu-id="0d676-862">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-863">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-863">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-864">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-864">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-865">TrustedSitesZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="0d676-865">TrustedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-866">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-866">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-867">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-867">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d676-868">TrustedSitesZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="0d676-868">TrustedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d676-869">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d676-869">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d676-870">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d676-870">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0d676-871">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0d676-871">Requirements</span></span>



| <span data-ttu-id="0d676-872">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d676-872">Requirement</span></span> | <span data-ttu-id="0d676-873">Valor</span><span class="sxs-lookup"><span data-stu-id="0d676-873">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d676-874">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0d676-874">Minimum supported client</span></span><br/> | <span data-ttu-id="0d676-875">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="0d676-875">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0d676-876">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0d676-876">Minimum supported server</span></span><br/> | <span data-ttu-id="0d676-877">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="0d676-877">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="0d676-878">Namespace</span><span class="sxs-lookup"><span data-stu-id="0d676-878">Namespace</span></span><br/>                | <span data-ttu-id="0d676-879">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="0d676-879">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="0d676-880">MOF</span><span class="sxs-lookup"><span data-stu-id="0d676-880">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0d676-881"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0d676-881"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="0d676-882">DLL</span><span class="sxs-lookup"><span data-stu-id="0d676-882">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0d676-883"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d676-883"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

