---
title: Classe MDM_Policy_Result01_InternetExplorer02
description: A política de MDM \_ \_ Result01 \_ InternetExplorer02 representa as políticas do Internet Explorer.
ms.assetid: 4b14c9ea-2f4d-4e5a-8aab-3741f15b0b1e
keywords:
- Classe MDM_Policy_Result01_InternetExplorer02
- Classe MDM_Policy_Result01_InternetExplorer02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_InternetExplorer02
- MDM_Policy_Result01_InternetExplorer02.InstanceID
- MDM_Policy_Result01_InternetExplorer02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63308b6100d6bd4ec924307a9dcd3892096fc0fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918336"
---
# <a name="mdm_policy_result01_internetexplorer02-class"></a><span data-ttu-id="5e5c3-105">\_Classe MDM \_ Result01 \_ InternetExplorer02</span><span class="sxs-lookup"><span data-stu-id="5e5c3-105">MDM\_Policy\_Result01\_InternetExplorer02 class</span></span>

<span data-ttu-id="5e5c3-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="5e5c3-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="5e5c3-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="5e5c3-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="5e5c3-108">A política de MDM \_ \_ Result01 \_ InternetExplorer02 representa as políticas do Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="5e5c3-108">The MDM\_Policy\_Result01\_InternetExplorer02 represents the Internet Explorer policies.</span></span>

<span data-ttu-id="5e5c3-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="5e5c3-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e5c3-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5e5c3-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_InternetExplorer02
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

## <a name="members"></a><span data-ttu-id="5e5c3-111">Membros</span><span class="sxs-lookup"><span data-stu-id="5e5c3-111">Members</span></span>

<span data-ttu-id="5e5c3-112">A **classe \_ \_ Result01 \_ InternetExplorer02 da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="5e5c3-112">The **MDM\_Policy\_Result01\_InternetExplorer02** class has these types of members:</span></span>

-   [<span data-ttu-id="5e5c3-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5e5c3-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5e5c3-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5e5c3-114">Properties</span></span>

<span data-ttu-id="5e5c3-115">A **classe \_ \_ Result01 \_ InternetExplorer02 da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="5e5c3-115">The **MDM\_Policy\_Result01\_InternetExplorer02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="5e5c3-116">AddSearchProvider</span><span class="sxs-lookup"><span data-stu-id="5e5c3-116">AddSearchProvider</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-addsearchprovider)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-119">AllowActiveXFiltering</span><span class="sxs-lookup"><span data-stu-id="5e5c3-119">AllowActiveXFiltering</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowactivexfiltering)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-122">AllowAddOnList</span><span class="sxs-lookup"><span data-stu-id="5e5c3-122">AllowAddOnList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowaddonlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-124">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-125">AllowCertificateAddressMismatchWarning</span><span class="sxs-lookup"><span data-stu-id="5e5c3-125">AllowCertificateAddressMismatchWarning</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowcertificateaddressmismatchwarning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-126">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-127">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-128">AllowDeletingBrowsingHistoryOnExit</span><span class="sxs-lookup"><span data-stu-id="5e5c3-128">AllowDeletingBrowsingHistoryOnExit</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowdeletingbrowsinghistoryonexit)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-130">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-131">AllowEnhancedProtectedMode</span><span class="sxs-lookup"><span data-stu-id="5e5c3-131">AllowEnhancedProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenhancedprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-132">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-133">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-134">AllowEnterpriseModeFromToolsMenu</span><span class="sxs-lookup"><span data-stu-id="5e5c3-134">AllowEnterpriseModeFromToolsMenu</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenterprisemodefromtoolsmenu)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-135">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-136">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-137">AllowEnterpriseModeSiteList</span><span class="sxs-lookup"><span data-stu-id="5e5c3-137">AllowEnterpriseModeSiteList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenterprisemodesitelist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-138">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-139">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-140">AllowFallbackToSSL3</span><span class="sxs-lookup"><span data-stu-id="5e5c3-140">AllowFallbackToSSL3</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowfallbacktossl3)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-141">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-142">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-143">AllowInternetExplorer7PolicyList</span><span class="sxs-lookup"><span data-stu-id="5e5c3-143">AllowInternetExplorer7PolicyList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetexplorer7policylist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-144">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-145">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-146">AllowInternetExplorerStandardsMode</span><span class="sxs-lookup"><span data-stu-id="5e5c3-146">AllowInternetExplorerStandardsMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetexplorerstandardsmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-147">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-148">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-149">AllowInternetZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="5e5c3-149">AllowInternetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-150">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-151">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-152">AllowIntranetZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="5e5c3-152">AllowIntranetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowintranetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-153">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-154">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-155">AllowLocalMachineZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="5e5c3-155">AllowLocalMachineZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlocalmachinezonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-156">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-157">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-158">AllowLockedDownInternetZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="5e5c3-158">AllowLockedDownInternetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddowninternetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-159">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-160">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-161">AllowLockedDownIntranetZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="5e5c3-161">AllowLockedDownIntranetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownintranetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-162">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-163">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-164">AllowLockedDownLocalMachineZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="5e5c3-164">AllowLockedDownLocalMachineZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownlocalmachinezonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-165">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-166">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-167">AllowLockedDownRestrictedSitesZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="5e5c3-167">AllowLockedDownRestrictedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownrestrictedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-168">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-169">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-170">AllowOneWordEntry</span><span class="sxs-lookup"><span data-stu-id="5e5c3-170">AllowOneWordEntry</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowonewordentry)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-171">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-172">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-173">AllowSiteToZoneAssignmentList</span><span class="sxs-lookup"><span data-stu-id="5e5c3-173">AllowSiteToZoneAssignmentList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsitetozoneassignmentlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-174">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-175">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-175">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-176">AllowsLockedDownTrustedSitesZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="5e5c3-176">AllowsLockedDownTrustedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowslockeddowntrustedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-177">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-178">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-178">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-179">AllowSoftwareWhenSignatureIsInvalid</span><span class="sxs-lookup"><span data-stu-id="5e5c3-179">AllowSoftwareWhenSignatureIsInvalid</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsoftwarewhensignatureisinvalid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-180">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-181">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-182">AllowsRestrictedSitesZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="5e5c3-182">AllowsRestrictedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsrestrictedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-183">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-184">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-184">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-185">AllowSuggestedSites</span><span class="sxs-lookup"><span data-stu-id="5e5c3-185">AllowSuggestedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsuggestedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-186">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-187">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-187">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-188">AllowTrustedSitesZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="5e5c3-188">AllowTrustedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowtrustedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-189">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-190">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-190">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-191">CheckServerCertificateRevocation</span><span class="sxs-lookup"><span data-stu-id="5e5c3-191">CheckServerCertificateRevocation</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-checkservercertificaterevocation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-192">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-193">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-193">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-194">CheckSignaturesOnDownloadedPrograms</span><span class="sxs-lookup"><span data-stu-id="5e5c3-194">CheckSignaturesOnDownloadedPrograms</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-checksignaturesondownloadedprograms)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-195">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-196">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-196">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-197">ConsistentMimeHandlingInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="5e5c3-197">ConsistentMimeHandlingInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-consistentmimehandlinginternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-198">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-199">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-199">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-200">DisableAdobeFlash</span><span class="sxs-lookup"><span data-stu-id="5e5c3-200">DisableAdobeFlash</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableadobeflash)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-201">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-202">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-202">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5e5c3-203">DisableBlockingOfOutdatedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="5e5c3-203">DisableBlockingOfOutdatedActiveXControls</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-204">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-205">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-205">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-206">DisableBypassOfSmartScreenWarnings</span><span class="sxs-lookup"><span data-stu-id="5e5c3-206">DisableBypassOfSmartScreenWarnings</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablebypassofsmartscreenwarnings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-207">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-208">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-208">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-209">DisableBypassOfSmartScreenWarningsAboutUncommonFiles</span><span class="sxs-lookup"><span data-stu-id="5e5c3-209">DisableBypassOfSmartScreenWarningsAboutUncommonFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablebypassofsmartscreenwarningsaboutuncommonfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-210">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-211">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-211">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-212">DisableConfiguringHistory</span><span class="sxs-lookup"><span data-stu-id="5e5c3-212">DisableConfiguringHistory</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableconfiguringhistory)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-213">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-214">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-214">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-215">DisableCrashDetection</span><span class="sxs-lookup"><span data-stu-id="5e5c3-215">DisableCrashDetection</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablecrashdetection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-216">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-217">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-217">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-218">DisableCustomerExperienceImprovementProgramParticipation</span><span class="sxs-lookup"><span data-stu-id="5e5c3-218">DisableCustomerExperienceImprovementProgramParticipation</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablecustomerexperienceimprovementprogramparticipation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-219">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-220">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-220">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-221">DisableDeletingUserVisitedWebsites</span><span class="sxs-lookup"><span data-stu-id="5e5c3-221">DisableDeletingUserVisitedWebsites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disabledeletinguservisitedwebsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-222">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-223">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-223">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-224">DisableEnclosureDownloading</span><span class="sxs-lookup"><span data-stu-id="5e5c3-224">DisableEnclosureDownloading</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableenclosuredownloading)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-225">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-226">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-226">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-227">DisableEncryptionSupport</span><span class="sxs-lookup"><span data-stu-id="5e5c3-227">DisableEncryptionSupport</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableencryptionsupport)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-228">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-228">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-229">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-229">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-230">DisableFirstRunWizard</span><span class="sxs-lookup"><span data-stu-id="5e5c3-230">DisableFirstRunWizard</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablefirstrunwizard)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-231">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-232">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-232">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-233">DisableFlipAheadFeature</span><span class="sxs-lookup"><span data-stu-id="5e5c3-233">DisableFlipAheadFeature</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableflipaheadfeature)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-234">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-234">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-235">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-235">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-236">DisableIgnoringCertificateErrors</span><span class="sxs-lookup"><span data-stu-id="5e5c3-236">DisableIgnoringCertificateErrors</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableignoringcertificateerrors)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-237">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-238">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-238">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-239">DisableInPrivateBrowsing</span><span class="sxs-lookup"><span data-stu-id="5e5c3-239">DisableInPrivateBrowsing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableinprivatebrowsing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-240">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-241">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-241">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-242">DisableProcessesInEnhancedProtectedMode</span><span class="sxs-lookup"><span data-stu-id="5e5c3-242">DisableProcessesInEnhancedProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableprocessesinenhancedprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-243">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-244">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-244">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-245">DisableProxyChange</span><span class="sxs-lookup"><span data-stu-id="5e5c3-245">DisableProxyChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableproxychange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-246">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-247">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-247">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-248">DisableSearchProviderChange</span><span class="sxs-lookup"><span data-stu-id="5e5c3-248">DisableSearchProviderChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesearchproviderchange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-249">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-250">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-250">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-251">DisableSecondaryHomePageChange</span><span class="sxs-lookup"><span data-stu-id="5e5c3-251">DisableSecondaryHomePageChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesecondaryhomepagechange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-252">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-253">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-253">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-254">DisableSecuritySettingsCheck</span><span class="sxs-lookup"><span data-stu-id="5e5c3-254">DisableSecuritySettingsCheck</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesecuritysettingscheck)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-255">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-256">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-256">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-257">DisableUpdateCheck</span><span class="sxs-lookup"><span data-stu-id="5e5c3-257">DisableUpdateCheck</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableupdatecheck)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-258">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-259">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-259">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-260">DoNotAllowActiveXControlsInProtectedMode</span><span class="sxs-lookup"><span data-stu-id="5e5c3-260">DoNotAllowActiveXControlsInProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotallowactivexcontrolsinprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-261">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-262">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-262">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-263">DoNotAllowUsersToAddSites</span><span class="sxs-lookup"><span data-stu-id="5e5c3-263">DoNotAllowUsersToAddSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotallowuserstoaddsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-264">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-265">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-265">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-266">DoNotAllowUsersToChangePolicies</span><span class="sxs-lookup"><span data-stu-id="5e5c3-266">DoNotAllowUsersToChangePolicies</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotallowuserstochangepolicies)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-267">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-267">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-268">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-268">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-269">DoNotBlockOutdatedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="5e5c3-269">DoNotBlockOutdatedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotblockoutdatedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-270">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-270">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-271">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-271">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-272">DoNotBlockOutdatedActiveXControlsOnSpecificDomains</span><span class="sxs-lookup"><span data-stu-id="5e5c3-272">DoNotBlockOutdatedActiveXControlsOnSpecificDomains</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotblockoutdatedactivexcontrolsonspecificdomains)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-273">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-273">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-274">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-274">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-275">IncludeAllLocalSites</span><span class="sxs-lookup"><span data-stu-id="5e5c3-275">IncludeAllLocalSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-includealllocalsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-276">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-276">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-277">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-277">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-278">IncludeAllNetworkPaths</span><span class="sxs-lookup"><span data-stu-id="5e5c3-278">IncludeAllNetworkPaths</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-includeallnetworkpaths)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-279">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-280">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-280">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5e5c3-281">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-281">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-282">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-282">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-283">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5e5c3-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-284">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5e5c3-284">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-285">InternetZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="5e5c3-285">InternetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-286">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-287">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-287">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-288">InternetZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="5e5c3-288">InternetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-289">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-290">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-290">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-291">InternetZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="5e5c3-291">InternetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-292">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-293">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-293">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-294">InternetZoneAllowCopyPasteViaScript</span><span class="sxs-lookup"><span data-stu-id="5e5c3-294">InternetZoneAllowCopyPasteViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowcopypasteviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-295">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-295">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-296">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-296">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-297">InternetZoneAllowDragAndDropCopyAndPasteFiles</span><span class="sxs-lookup"><span data-stu-id="5e5c3-297">InternetZoneAllowDragAndDropCopyAndPasteFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowdraganddropcopyandpastefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-298">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-298">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-299">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-299">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-300">InternetZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="5e5c3-300">InternetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-301">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-302">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-302">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-303">InternetZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="5e5c3-303">InternetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-304">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-305">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-305">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-306">InternetZoneAllowLoadingOfXAMLFiles</span><span class="sxs-lookup"><span data-stu-id="5e5c3-306">InternetZoneAllowLoadingOfXAMLFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowloadingofxamlfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-307">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-308">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-308">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-309">InternetZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="5e5c3-309">InternetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-310">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-311">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-311">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-312">InternetZoneAllowOnlyApprovedDomainsToUseActiveXControls</span><span class="sxs-lookup"><span data-stu-id="5e5c3-312">InternetZoneAllowOnlyApprovedDomainsToUseActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowonlyapproveddomainstouseactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-313">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-314">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-314">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-315">InternetZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span><span class="sxs-lookup"><span data-stu-id="5e5c3-315">InternetZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowonlyapproveddomainstousetdcactivexcontrol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-316">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-316">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-317">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-317">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-318">InternetZoneAllowScriptingOfInternetExplorerWebBrowserControls</span><span class="sxs-lookup"><span data-stu-id="5e5c3-318">InternetZoneAllowScriptingOfInternetExplorerWebBrowserControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptingofinternetexplorerwebbrowsercontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-319">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-320">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-320">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-321">InternetZoneAllowScriptInitiatedWindows</span><span class="sxs-lookup"><span data-stu-id="5e5c3-321">InternetZoneAllowScriptInitiatedWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptinitiatedwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-322">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-323">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-323">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-324">InternetZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="5e5c3-324">InternetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-325">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-326">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-326">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-327">InternetZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="5e5c3-327">InternetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-328">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-328">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-329">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-329">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-330">InternetZoneAllowUpdatesToStatusBarViaScript</span><span class="sxs-lookup"><span data-stu-id="5e5c3-330">InternetZoneAllowUpdatesToStatusBarViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowupdatestostatusbarviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-331">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-331">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-332">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-332">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-333">InternetZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="5e5c3-333">InternetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-334">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-334">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-335">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-335">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-336">InternetZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="5e5c3-336">InternetZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-337">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-338">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-338">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-339">InternetZoneDownloadSignedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="5e5c3-339">InternetZoneDownloadSignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedownloadsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-340">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-341">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-341">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-342">InternetZoneDownloadUnsignedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="5e5c3-342">InternetZoneDownloadUnsignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedownloadunsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-343">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-343">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-344">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-344">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-345">InternetZoneEnableCrossSiteScriptingFilter</span><span class="sxs-lookup"><span data-stu-id="5e5c3-345">InternetZoneEnableCrossSiteScriptingFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenablecrosssitescriptingfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-346">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-347">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-347">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-348">InternetZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span><span class="sxs-lookup"><span data-stu-id="5e5c3-348">InternetZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenabledraggingofcontentfromdifferentdomainsacrosswindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-349">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-350">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-350">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-351">InternetZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span><span class="sxs-lookup"><span data-stu-id="5e5c3-351">InternetZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenabledraggingofcontentfromdifferentdomainswithinwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-352">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-353">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-353">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-354">InternetZoneEnableMIMESniffing</span><span class="sxs-lookup"><span data-stu-id="5e5c3-354">InternetZoneEnableMIMESniffing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenablemimesniffing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-355">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-356">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-356">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-357">InternetZoneEnableProtectedMode</span><span class="sxs-lookup"><span data-stu-id="5e5c3-357">InternetZoneEnableProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenableprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-358">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-358">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-359">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-359">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-360">InternetZoneIncludeLocalPathWhenUploadingFilesToServer</span><span class="sxs-lookup"><span data-stu-id="5e5c3-360">InternetZoneIncludeLocalPathWhenUploadingFilesToServer</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneincludelocalpathwhenuploadingfilestoserver)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-361">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-362">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-362">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-363">InternetZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="5e5c3-363">InternetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-364">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-364">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-365">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-365">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-366">InternetZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="5e5c3-366">InternetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-367">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-367">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-368">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-368">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-369">InternetZoneLaunchingApplicationsAndFilesInIFRAME</span><span class="sxs-lookup"><span data-stu-id="5e5c3-369">InternetZoneLaunchingApplicationsAndFilesInIFRAME</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonelaunchingapplicationsandfilesiniframe)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-370">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-370">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-371">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-371">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-372">InternetZoneLogonOptions</span><span class="sxs-lookup"><span data-stu-id="5e5c3-372">InternetZoneLogonOptions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonelogonoptions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-373">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-373">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-374">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-374">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-375">InternetZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="5e5c3-375">InternetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-376">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-376">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-377">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-377">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5e5c3-378">InternetZoneRunNETFrameworkReliantComponentsNotSignedWithAuthenticode</span><span class="sxs-lookup"><span data-stu-id="5e5c3-378">InternetZoneRunNETFrameworkReliantComponentsNotSignedWithAuthenticode</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-379">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-380">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-380">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-381">InternetZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span><span class="sxs-lookup"><span data-stu-id="5e5c3-381">InternetZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonerunnetframeworkreliantcomponentssignedwithauthenticode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-382">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-382">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-383">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-383">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-384">InternetZoneShowSecurityWarningForPotentiallyUnsafeFiles</span><span class="sxs-lookup"><span data-stu-id="5e5c3-384">InternetZoneShowSecurityWarningForPotentiallyUnsafeFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneshowsecuritywarningforpotentiallyunsafefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-385">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-385">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-386">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-386">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-387">InternetZoneUsePopupBlocker</span><span class="sxs-lookup"><span data-stu-id="5e5c3-387">InternetZoneUsePopupBlocker</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneusepopupblocker)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-388">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-388">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-389">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-389">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5e5c3-390">InternetZoneWebsitesInLessPrivilegedZonesCanNavigateIntoThisZone</span><span class="sxs-lookup"><span data-stu-id="5e5c3-390">InternetZoneWebsitesInLessPrivilegedZonesCanNavigateIntoThisZone</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-391">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-391">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-392">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-392">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-393">IntranetZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="5e5c3-393">IntranetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-394">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-394">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-395">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-395">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-396">IntranetZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="5e5c3-396">IntranetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-397">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-397">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-398">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-398">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-399">IntranetZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="5e5c3-399">IntranetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-400">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-400">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-401">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-401">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-402">IntranetZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="5e5c3-402">IntranetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-403">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-403">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-404">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-404">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-405">IntranetZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="5e5c3-405">IntranetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-406">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-406">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-407">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-407">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-408">IntranetZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="5e5c3-408">IntranetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-409">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-409">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-410">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-410">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-411">IntranetZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="5e5c3-411">IntranetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-412">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-412">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-413">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-413">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-414">IntranetZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="5e5c3-414">IntranetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-415">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-415">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-416">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-416">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-417">IntranetZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="5e5c3-417">IntranetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-418">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-418">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-419">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-419">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-420">IntranetZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="5e5c3-420">IntranetZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-421">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-421">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-422">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-422">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-423">IntranetZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="5e5c3-423">IntranetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-424">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-424">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-425">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-425">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5e5c3-426">IntranetZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span><span class="sxs-lookup"><span data-stu-id="5e5c3-426">IntranetZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-427">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-427">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-428">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-428">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-429">IntranetZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="5e5c3-429">IntranetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-430">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-430">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-431">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-431">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-432">IntranetZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="5e5c3-432">IntranetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-433">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-433">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-434">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-434">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-435">LocalMachineZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="5e5c3-435">LocalMachineZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-436">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-436">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-437">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-437">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-438">LocalMachineZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="5e5c3-438">LocalMachineZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-439">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-439">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-440">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-440">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-441">LocalMachineZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="5e5c3-441">LocalMachineZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-442">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-442">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-443">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-443">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-444">LocalMachineZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="5e5c3-444">LocalMachineZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-445">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-445">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-446">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-446">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-447">LocalMachineZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="5e5c3-447">LocalMachineZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-448">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-448">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-449">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-449">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-450">LocalMachineZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="5e5c3-450">LocalMachineZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-451">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-451">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-452">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-452">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-453">LocalMachineZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="5e5c3-453">LocalMachineZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-454">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-454">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-455">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-455">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-456">LocalMachineZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="5e5c3-456">LocalMachineZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-457">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-457">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-458">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-458">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-459">LocalMachineZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="5e5c3-459">LocalMachineZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-460">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-460">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-461">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-461">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-462">LocalMachineZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="5e5c3-462">LocalMachineZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-463">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-463">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-464">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-464">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-465">LocalMachineZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="5e5c3-465">LocalMachineZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-466">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-466">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-467">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-467">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-468">LocalMachineZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="5e5c3-468">LocalMachineZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-469">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-469">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-470">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-470">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-471">LocalMachineZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="5e5c3-471">LocalMachineZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-472">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-472">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-473">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-473">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-474">LockedDownInternetZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="5e5c3-474">LockedDownInternetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-475">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-475">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-476">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-476">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-477">LockedDownInternetZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="5e5c3-477">LockedDownInternetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-478">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-478">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-479">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-479">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-480">LockedDownInternetZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="5e5c3-480">LockedDownInternetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-481">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-481">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-482">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-482">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-483">LockedDownInternetZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="5e5c3-483">LockedDownInternetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-484">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-484">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-485">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-485">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-486">LockedDownInternetZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="5e5c3-486">LockedDownInternetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-487">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-487">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-488">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-488">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-489">LockedDownInternetZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="5e5c3-489">LockedDownInternetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-490">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-490">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-491">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-491">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-492">LockedDownInternetZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="5e5c3-492">LockedDownInternetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-493">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-493">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-494">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-494">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-495">LockedDownInternetZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="5e5c3-495">LockedDownInternetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-496">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-496">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-497">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-497">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-498">LockedDownInternetZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="5e5c3-498">LockedDownInternetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-499">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-499">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-500">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-500">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-501">LockedDownInternetZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="5e5c3-501">LockedDownInternetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-502">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-502">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-503">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-503">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-504">LockedDownInternetZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="5e5c3-504">LockedDownInternetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-505">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-505">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-506">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-506">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-507">LockedDownInternetZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="5e5c3-507">LockedDownInternetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-508">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-508">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-509">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-509">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-510">LockedDownIntranetZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="5e5c3-510">LockedDownIntranetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-511">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-511">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-512">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-512">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-513">LockedDownIntranetZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="5e5c3-513">LockedDownIntranetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-514">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-514">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-515">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-515">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-516">LockedDownIntranetZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="5e5c3-516">LockedDownIntranetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-517">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-517">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-518">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-518">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-519">LockedDownIntranetZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="5e5c3-519">LockedDownIntranetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-520">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-520">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-521">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-521">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-522">LockedDownIntranetZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="5e5c3-522">LockedDownIntranetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-523">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-523">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-524">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-524">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-525">LockedDownIntranetZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="5e5c3-525">LockedDownIntranetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-526">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-526">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-527">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-527">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-528">LockedDownIntranetZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="5e5c3-528">LockedDownIntranetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-529">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-529">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-530">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-530">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-531">LockedDownIntranetZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="5e5c3-531">LockedDownIntranetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-532">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-532">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-533">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-533">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-534">LockedDownIntranetZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="5e5c3-534">LockedDownIntranetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-535">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-535">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-536">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-536">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-537">LockedDownIntranetZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="5e5c3-537">LockedDownIntranetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-538">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-538">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-539">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-539">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-540">LockedDownIntranetZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="5e5c3-540">LockedDownIntranetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-541">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-541">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-542">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-542">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-543">LockedDownLocalMachineZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="5e5c3-543">LockedDownLocalMachineZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-544">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-544">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-545">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-545">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-546">LockedDownLocalMachineZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="5e5c3-546">LockedDownLocalMachineZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-547">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-547">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-548">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-548">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-549">LockedDownLocalMachineZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="5e5c3-549">LockedDownLocalMachineZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-550">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-550">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-551">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-551">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-552">LockedDownLocalMachineZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="5e5c3-552">LockedDownLocalMachineZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-553">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-553">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-554">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-554">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-555">LockedDownLocalMachineZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="5e5c3-555">LockedDownLocalMachineZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-556">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-556">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-557">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-557">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-558">LockedDownLocalMachineZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="5e5c3-558">LockedDownLocalMachineZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-559">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-559">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-560">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-560">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-561">LockedDownLocalMachineZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="5e5c3-561">LockedDownLocalMachineZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-562">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-562">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-563">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-563">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-564">LockedDownLocalMachineZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="5e5c3-564">LockedDownLocalMachineZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-565">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-565">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-566">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-566">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-567">LockedDownLocalMachineZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="5e5c3-567">LockedDownLocalMachineZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-568">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-568">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-569">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-569">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-570">LockedDownLocalMachineZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="5e5c3-570">LockedDownLocalMachineZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-571">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-571">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-572">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-572">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-573">LockedDownLocalMachineZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="5e5c3-573">LockedDownLocalMachineZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-574">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-574">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-575">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-575">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-576">LockedDownLocalMachineZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="5e5c3-576">LockedDownLocalMachineZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-577">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-577">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-578">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-578">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-579">LockedDownRestrictedSitesZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="5e5c3-579">LockedDownRestrictedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-580">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-580">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-581">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-581">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-582">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="5e5c3-582">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-583">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-583">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-584">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-584">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-585">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="5e5c3-585">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-586">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-586">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-587">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-587">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-588">LockedDownRestrictedSitesZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="5e5c3-588">LockedDownRestrictedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-589">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-589">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-590">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-590">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-591">LockedDownRestrictedSitesZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="5e5c3-591">LockedDownRestrictedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-592">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-592">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-593">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-593">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-594">LockedDownRestrictedSitesZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="5e5c3-594">LockedDownRestrictedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-595">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-595">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-596">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-596">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-597">LockedDownRestrictedSitesZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="5e5c3-597">LockedDownRestrictedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-598">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-598">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-599">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-599">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-600">LockedDownRestrictedSitesZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="5e5c3-600">LockedDownRestrictedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-601">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-601">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-602">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-602">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-603">LockedDownRestrictedSitesZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="5e5c3-603">LockedDownRestrictedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-604">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-604">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-605">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-605">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-606">LockedDownRestrictedSitesZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="5e5c3-606">LockedDownRestrictedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-607">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-607">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-608">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-608">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-609">LockedDownRestrictedSitesZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="5e5c3-609">LockedDownRestrictedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-610">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-610">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-611">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-611">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-612">LockedDownRestrictedSitesZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="5e5c3-612">LockedDownRestrictedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-613">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-613">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-614">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-614">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-615">LockedDownTrustedSitesZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="5e5c3-615">LockedDownTrustedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-616">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-616">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-617">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-617">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-618">LockedDownTrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="5e5c3-618">LockedDownTrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-619">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-619">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-620">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-620">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-621">LockedDownTrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="5e5c3-621">LockedDownTrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-622">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-622">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-623">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-623">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-624">LockedDownTrustedSitesZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="5e5c3-624">LockedDownTrustedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-625">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-625">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-626">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-626">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-627">LockedDownTrustedSitesZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="5e5c3-627">LockedDownTrustedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-628">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-628">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-629">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-629">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-630">LockedDownTrustedSitesZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="5e5c3-630">LockedDownTrustedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-631">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-631">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-632">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-632">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-633">LockedDownTrustedSitesZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="5e5c3-633">LockedDownTrustedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-634">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-634">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-635">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-635">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-636">LockedDownTrustedSitesZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="5e5c3-636">LockedDownTrustedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-637">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-637">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-638">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-638">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-639">LockedDownTrustedSitesZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="5e5c3-639">LockedDownTrustedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-640">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-640">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-641">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-641">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-642">LockedDownTrustedSitesZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="5e5c3-642">LockedDownTrustedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-643">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-643">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-644">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-644">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-645">LockedDownTrustedSitesZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="5e5c3-645">LockedDownTrustedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-646">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-646">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-647">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-647">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-648">LockedDownTrustedSitesZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="5e5c3-648">LockedDownTrustedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-649">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-649">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-650">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-650">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-651">MimeSniffingSafetyFeatureInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="5e5c3-651">MimeSniffingSafetyFeatureInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-mimesniffingsafetyfeatureinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-652">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-652">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-653">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-653">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-654">MKProtocolSecurityRestrictionInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="5e5c3-654">MKProtocolSecurityRestrictionInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-mkprotocolsecurityrestrictioninternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-655">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-655">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-656">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-656">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-657">NotificationBarInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="5e5c3-657">NotificationBarInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-notificationbarinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-658">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-658">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-659">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-659">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5e5c3-660">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-660">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-661">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-661">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-662">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5e5c3-662">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-663">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5e5c3-663">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-664">PreventManagingSmartScreenFilter</span><span class="sxs-lookup"><span data-stu-id="5e5c3-664">PreventManagingSmartScreenFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-preventmanagingsmartscreenfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-665">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-665">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-666">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-666">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-667">PreventPerUserInstallationOfActiveXControls</span><span class="sxs-lookup"><span data-stu-id="5e5c3-667">PreventPerUserInstallationOfActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-preventperuserinstallationofactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-668">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-668">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-669">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-669">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-670">ProtectionFromZoneElevationInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="5e5c3-670">ProtectionFromZoneElevationInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-protectionfromzoneelevationinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-671">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-671">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-672">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-672">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-673">RemoveRunThisTimeButtonForOutdatedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="5e5c3-673">RemoveRunThisTimeButtonForOutdatedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-removerunthistimebuttonforoutdatedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-674">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-674">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-675">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-675">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-676">RestrictActiveXInstallInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="5e5c3-676">RestrictActiveXInstallInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictactivexinstallinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-677">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-677">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-678">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-678">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-679">RestrictedSitesZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="5e5c3-679">RestrictedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-680">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-680">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-681">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-681">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-682">RestrictedSitesZoneAllowActiveScripting</span><span class="sxs-lookup"><span data-stu-id="5e5c3-682">RestrictedSitesZoneAllowActiveScripting</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowactivescripting)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-683">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-683">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-684">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-684">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-685">RestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="5e5c3-685">RestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-686">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-686">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-687">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-687">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-688">RestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="5e5c3-688">RestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-689">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-689">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-690">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-690">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-691">RestrictedSitesZoneAllowBinaryAndScriptBehaviors</span><span class="sxs-lookup"><span data-stu-id="5e5c3-691">RestrictedSitesZoneAllowBinaryAndScriptBehaviors</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowbinaryandscriptbehaviors)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-692">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-692">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-693">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-693">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-694">RestrictedSitesZoneAllowCopyPasteViaScript</span><span class="sxs-lookup"><span data-stu-id="5e5c3-694">RestrictedSitesZoneAllowCopyPasteViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowcopypasteviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-695">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-695">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-696">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-696">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-697">RestrictedSitesZoneAllowDragAndDropCopyAndPasteFiles</span><span class="sxs-lookup"><span data-stu-id="5e5c3-697">RestrictedSitesZoneAllowDragAndDropCopyAndPasteFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowdraganddropcopyandpastefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-698">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-698">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-699">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-699">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-700">RestrictedSitesZoneAllowFileDownloads</span><span class="sxs-lookup"><span data-stu-id="5e5c3-700">RestrictedSitesZoneAllowFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-701">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-701">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-702">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-702">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-703">RestrictedSitesZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="5e5c3-703">RestrictedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-704">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-704">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-705">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-705">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-706">RestrictedSitesZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="5e5c3-706">RestrictedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-707">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-707">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-708">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-708">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-709">RestrictedSitesZoneAllowLoadingOfXAMLFiles</span><span class="sxs-lookup"><span data-stu-id="5e5c3-709">RestrictedSitesZoneAllowLoadingOfXAMLFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowloadingofxamlfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-710">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-710">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-711">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-711">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-712">RestrictedSitesZoneAllowMETAREFRESH</span><span class="sxs-lookup"><span data-stu-id="5e5c3-712">RestrictedSitesZoneAllowMETAREFRESH</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowmetarefresh)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-713">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-713">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-714">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-714">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-715">RestrictedSitesZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="5e5c3-715">RestrictedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-716">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-716">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-717">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-717">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-718">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseActiveXControls</span><span class="sxs-lookup"><span data-stu-id="5e5c3-718">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowonlyapproveddomainstouseactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-719">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-719">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-720">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-720">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-721">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span><span class="sxs-lookup"><span data-stu-id="5e5c3-721">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowonlyapproveddomainstousetdcactivexcontrol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-722">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-722">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-723">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-723">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-724">RestrictedSitesZoneAllowScriptingOfInternetExplorerWebBrowserControls</span><span class="sxs-lookup"><span data-stu-id="5e5c3-724">RestrictedSitesZoneAllowScriptingOfInternetExplorerWebBrowserControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptingofinternetexplorerwebbrowsercontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-725">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-725">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-726">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-726">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-727">RestrictedSitesZoneAllowScriptInitiatedWindows</span><span class="sxs-lookup"><span data-stu-id="5e5c3-727">RestrictedSitesZoneAllowScriptInitiatedWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptinitiatedwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-728">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-728">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-729">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-729">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-730">RestrictedSitesZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="5e5c3-730">RestrictedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-731">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-731">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-732">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-732">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-733">RestrictedSitesZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="5e5c3-733">RestrictedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-734">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-734">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-735">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-735">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-736">RestrictedSitesZoneAllowUpdatesToStatusBarViaScript</span><span class="sxs-lookup"><span data-stu-id="5e5c3-736">RestrictedSitesZoneAllowUpdatesToStatusBarViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowupdatestostatusbarviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-737">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-737">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-738">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-738">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-739">RestrictedSitesZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="5e5c3-739">RestrictedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-740">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-740">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-741">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-741">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-742">RestrictedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="5e5c3-742">RestrictedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-743">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-743">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-744">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-744">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-745">RestrictedSitesZoneDownloadSignedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="5e5c3-745">RestrictedSitesZoneDownloadSignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedownloadsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-746">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-746">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-747">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-747">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-748">RestrictedSitesZoneDownloadUnsignedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="5e5c3-748">RestrictedSitesZoneDownloadUnsignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedownloadunsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-749">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-749">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-750">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-750">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-751">RestrictedSitesZoneEnableCrossSiteScriptingFilter</span><span class="sxs-lookup"><span data-stu-id="5e5c3-751">RestrictedSitesZoneEnableCrossSiteScriptingFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenablecrosssitescriptingfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-752">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-752">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-753">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-753">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-754">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span><span class="sxs-lookup"><span data-stu-id="5e5c3-754">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenabledraggingofcontentfromdifferentdomainsacrosswindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-755">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-755">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-756">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-756">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-757">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span><span class="sxs-lookup"><span data-stu-id="5e5c3-757">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenabledraggingofcontentfromdifferentdomainswithinwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-758">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-758">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-759">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-759">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-760">RestrictedSitesZoneEnableMIMESniffing</span><span class="sxs-lookup"><span data-stu-id="5e5c3-760">RestrictedSitesZoneEnableMIMESniffing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenablemimesniffing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-761">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-761">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-762">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-762">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-763">RestrictedSitesZoneIncludeLocalPathWhenUploadingFilesToServer</span><span class="sxs-lookup"><span data-stu-id="5e5c3-763">RestrictedSitesZoneIncludeLocalPathWhenUploadingFilesToServer</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneincludelocalpathwhenuploadingfilestoserver)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-764">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-764">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-765">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-765">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-766">RestrictedSitesZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="5e5c3-766">RestrictedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-767">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-767">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-768">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-768">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-769">RestrictedSitesZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="5e5c3-769">RestrictedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-770">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-770">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-771">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-771">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-772">RestrictedSitesZoneLaunchingApplicationsAndFilesInIFRAME</span><span class="sxs-lookup"><span data-stu-id="5e5c3-772">RestrictedSitesZoneLaunchingApplicationsAndFilesInIFRAME</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonelaunchingapplicationsandfilesiniframe)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-773">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-773">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-774">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-774">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-775">RestrictedSitesZoneLogonOptions</span><span class="sxs-lookup"><span data-stu-id="5e5c3-775">RestrictedSitesZoneLogonOptions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonelogonoptions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-776">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-776">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-777">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-777">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-778">RestrictedSitesZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="5e5c3-778">RestrictedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-779">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-779">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-780">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-780">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5e5c3-781">RestrictedSitesZoneNavigateWindowsAndFramesAcrossDomains</span><span class="sxs-lookup"><span data-stu-id="5e5c3-781">RestrictedSitesZoneNavigateWindowsAndFramesAcrossDomains</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-782">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-782">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-783">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-783">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-784">RestrictedSitesZoneRunActiveXControlsAndPlugins</span><span class="sxs-lookup"><span data-stu-id="5e5c3-784">RestrictedSitesZoneRunActiveXControlsAndPlugins</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonerunactivexcontrolsandplugins)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-785">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-785">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-786">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-786">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-787">RestrictedSitesZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span><span class="sxs-lookup"><span data-stu-id="5e5c3-787">RestrictedSitesZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonerunnetframeworkreliantcomponentssignedwithauthenticode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-788">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-788">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-789">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-789">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-790">RestrictedSitesZoneScriptActiveXControlsMarkedSafeForScripting</span><span class="sxs-lookup"><span data-stu-id="5e5c3-790">RestrictedSitesZoneScriptActiveXControlsMarkedSafeForScripting</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonescriptactivexcontrolsmarkedsafeforscripting)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-791">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-791">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-792">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-792">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-793">RestrictedSitesZoneScriptingOfJavaApplets</span><span class="sxs-lookup"><span data-stu-id="5e5c3-793">RestrictedSitesZoneScriptingOfJavaApplets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonescriptingofjavaapplets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-794">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-794">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-795">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-795">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-796">RestrictedSitesZoneShowSecurityWarningForPotentiallyUnsafeFiles</span><span class="sxs-lookup"><span data-stu-id="5e5c3-796">RestrictedSitesZoneShowSecurityWarningForPotentiallyUnsafeFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneshowsecuritywarningforpotentiallyunsafefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-797">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-797">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-798">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-798">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5e5c3-799">RestrictedSitesZoneTurnOnCrossSiteScriptingFilter</span><span class="sxs-lookup"><span data-stu-id="5e5c3-799">RestrictedSitesZoneTurnOnCrossSiteScriptingFilter</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-800">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-800">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-801">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-801">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-802">RestrictedSitesZoneTurnOnProtectedMode</span><span class="sxs-lookup"><span data-stu-id="5e5c3-802">RestrictedSitesZoneTurnOnProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneturnonprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-803">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-803">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-804">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-804">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-805">RestrictedSitesZoneUsePopupBlocker</span><span class="sxs-lookup"><span data-stu-id="5e5c3-805">RestrictedSitesZoneUsePopupBlocker</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneusepopupblocker)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-806">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-806">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-807">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-807">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-808">RestrictFileDownloadInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="5e5c3-808">RestrictFileDownloadInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictfiledownloadinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-809">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-809">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-810">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-810">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-811">ScriptedWindowSecurityRestrictionsInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="5e5c3-811">ScriptedWindowSecurityRestrictionsInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-scriptedwindowsecurityrestrictionsinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-812">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-812">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-813">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-813">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-814">SearchProviderList</span><span class="sxs-lookup"><span data-stu-id="5e5c3-814">SearchProviderList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-searchproviderlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-815">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-815">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-816">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-816">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-817">SecurityZonesUseOnlyMachineSettings</span><span class="sxs-lookup"><span data-stu-id="5e5c3-817">SecurityZonesUseOnlyMachineSettings</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-securityzonesuseonlymachinesettings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-818">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-818">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-819">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-819">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-820">SpecifyUseOfActiveXInstallerService</span><span class="sxs-lookup"><span data-stu-id="5e5c3-820">SpecifyUseOfActiveXInstallerService</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-specifyuseofactivexinstallerservice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-821">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-821">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-822">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-822">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-823">TrustedSitesZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="5e5c3-823">TrustedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-824">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-824">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-825">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-825">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-826">TrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="5e5c3-826">TrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-827">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-827">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-828">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-828">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-829">TrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="5e5c3-829">TrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-830">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-830">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-831">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-831">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-832">TrustedSitesZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="5e5c3-832">TrustedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-833">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-833">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-834">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-834">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-835">TrustedSitesZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="5e5c3-835">TrustedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-836">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-836">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-837">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-837">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-838">TrustedSitesZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="5e5c3-838">TrustedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-839">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-839">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-840">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-840">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-841">TrustedSitesZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="5e5c3-841">TrustedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-842">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-842">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-843">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-843">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-844">TrustedSitesZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="5e5c3-844">TrustedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-845">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-845">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-846">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-846">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-847">TrustedSitesZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="5e5c3-847">TrustedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-848">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-848">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-849">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-849">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-850">TrustedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="5e5c3-850">TrustedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-851">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-851">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-852">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-852">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5e5c3-853">TrustedSitesZoneDontRunAntimalwareProgramsAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="5e5c3-853">TrustedSitesZoneDontRunAntimalwareProgramsAgainstActiveXControls</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-854">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-854">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-855">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-855">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-856">TrustedSitesZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="5e5c3-856">TrustedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-857">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-857">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-858">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-858">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5e5c3-859">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedAsSafe</span><span class="sxs-lookup"><span data-stu-id="5e5c3-859">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedAsSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-860">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-860">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-861">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-861">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5e5c3-862">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span><span class="sxs-lookup"><span data-stu-id="5e5c3-862">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-863">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-863">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-864">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-864">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-865">TrustedSitesZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="5e5c3-865">TrustedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-866">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-866">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-867">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-867">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5e5c3-868">TrustedSitesZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="5e5c3-868">TrustedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e5c3-869">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e5c3-869">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e5c3-870">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5e5c3-870">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5e5c3-871">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e5c3-871">Requirements</span></span>



| <span data-ttu-id="5e5c3-872">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e5c3-872">Requirement</span></span> | <span data-ttu-id="5e5c3-873">Valor</span><span class="sxs-lookup"><span data-stu-id="5e5c3-873">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e5c3-874">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5e5c3-874">Minimum supported client</span></span><br/> | <span data-ttu-id="5e5c3-875">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="5e5c3-875">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5e5c3-876">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5e5c3-876">Minimum supported server</span></span><br/> | <span data-ttu-id="5e5c3-877">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="5e5c3-877">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="5e5c3-878">Namespace</span><span class="sxs-lookup"><span data-stu-id="5e5c3-878">Namespace</span></span><br/>                | <span data-ttu-id="5e5c3-879">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="5e5c3-879">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="5e5c3-880">MOF</span><span class="sxs-lookup"><span data-stu-id="5e5c3-880">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5e5c3-881"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5e5c3-881"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="5e5c3-882">DLL</span><span class="sxs-lookup"><span data-stu-id="5e5c3-882">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5e5c3-883"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5e5c3-883"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

