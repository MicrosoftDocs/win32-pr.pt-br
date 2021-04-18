---
title: Classe MDM_Policy_User_Result01_InternetExplorer02
description: A \_ classe Result01 InternetExplorer02 do usuário da política de MDM \_ \_ \_ representa as políticas disponíveis do Internet Explorer.
ms.assetid: efd999aa-4aa8-486d-82d4-20af7e2005fe
keywords:
- Classe MDM_Policy_User_Result01_InternetExplorer02
- Classe MDM_Policy_User_Result01_InternetExplorer02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_User_Result01_InternetExplorer02
- MDM_Policy_User_Result01_InternetExplorer02.InstanceID
- MDM_Policy_User_Result01_InternetExplorer02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8693720c7a973cc6bc689abbf76a4674f185e23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454677"
---
# <a name="mdm_policy_user_result01_internetexplorer02-class"></a><span data-ttu-id="70c05-105">Result01 de usuário de política de MDM- \_ \_ \_ \_ classe InternetExplorer02</span><span class="sxs-lookup"><span data-stu-id="70c05-105">MDM\_Policy\_User\_Result01\_InternetExplorer02 class</span></span>

<span data-ttu-id="70c05-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="70c05-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="70c05-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="70c05-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="70c05-108">A \_ classe Result01 InternetExplorer02 do usuário da política de MDM \_ \_ \_ representa as políticas disponíveis do Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="70c05-108">The MDM\_Policy\_User\_Result01\_InternetExplorer02 class represents the available Internet Explorer policies.</span></span>

<span data-ttu-id="70c05-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="70c05-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="70c05-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="70c05-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Result01_InternetExplorer02
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

## <a name="members"></a><span data-ttu-id="70c05-111">Membros</span><span class="sxs-lookup"><span data-stu-id="70c05-111">Members</span></span>

<span data-ttu-id="70c05-112">A **classe \_ \_ \_ Result01 \_ InternetExplorer02 do usuário da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="70c05-112">The **MDM\_Policy\_User\_Result01\_InternetExplorer02** class has these types of members:</span></span>

-   [<span data-ttu-id="70c05-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="70c05-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="70c05-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="70c05-114">Properties</span></span>

<span data-ttu-id="70c05-115">A **classe \_ \_ \_ Result01 \_ InternetExplorer02 do usuário da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="70c05-115">The **MDM\_Policy\_User\_Result01\_InternetExplorer02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="70c05-116">AddSearchProvider</span><span class="sxs-lookup"><span data-stu-id="70c05-116">AddSearchProvider</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-addsearchprovider)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-119">AllowActiveXFiltering</span><span class="sxs-lookup"><span data-stu-id="70c05-119">AllowActiveXFiltering</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowactivexfiltering)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-122">AllowAddOnList</span><span class="sxs-lookup"><span data-stu-id="70c05-122">AllowAddOnList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowaddonlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-124">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-125">AllowAutoComplete</span><span class="sxs-lookup"><span data-stu-id="70c05-125">AllowAutoComplete</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowautocomplete)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-126">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-127">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-128">AllowCertificateAddressMismatchWarning</span><span class="sxs-lookup"><span data-stu-id="70c05-128">AllowCertificateAddressMismatchWarning</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowcertificateaddressmismatchwarning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-130">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-131">AllowDeletingBrowsingHistoryOnExit</span><span class="sxs-lookup"><span data-stu-id="70c05-131">AllowDeletingBrowsingHistoryOnExit</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowdeletingbrowsinghistoryonexit)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-132">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-133">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-134">AllowEnhancedProtectedMode</span><span class="sxs-lookup"><span data-stu-id="70c05-134">AllowEnhancedProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenhancedprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-135">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-136">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-137">AllowEnterpriseModeFromToolsMenu</span><span class="sxs-lookup"><span data-stu-id="70c05-137">AllowEnterpriseModeFromToolsMenu</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenterprisemodefromtoolsmenu)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-138">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-139">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-140">AllowEnterpriseModeSiteList</span><span class="sxs-lookup"><span data-stu-id="70c05-140">AllowEnterpriseModeSiteList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenterprisemodesitelist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-141">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-142">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-143">AllowInternetExplorer7PolicyList</span><span class="sxs-lookup"><span data-stu-id="70c05-143">AllowInternetExplorer7PolicyList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetexplorer7policylist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-144">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-145">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-146">AllowInternetExplorerStandardsMode</span><span class="sxs-lookup"><span data-stu-id="70c05-146">AllowInternetExplorerStandardsMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetexplorerstandardsmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-147">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-148">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-149">AllowInternetZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="70c05-149">AllowInternetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-150">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-151">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-152">AllowIntranetZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="70c05-152">AllowIntranetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowintranetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-153">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-154">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-155">AllowLocalMachineZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="70c05-155">AllowLocalMachineZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlocalmachinezonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-156">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-157">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-158">AllowLockedDownInternetZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="70c05-158">AllowLockedDownInternetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddowninternetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-159">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-160">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-161">AllowLockedDownIntranetZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="70c05-161">AllowLockedDownIntranetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownintranetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-162">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-163">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-164">AllowLockedDownLocalMachineZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="70c05-164">AllowLockedDownLocalMachineZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownlocalmachinezonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-165">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-166">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-167">AllowLockedDownRestrictedSitesZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="70c05-167">AllowLockedDownRestrictedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownrestrictedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-168">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-169">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-170">AllowOneWordEntry</span><span class="sxs-lookup"><span data-stu-id="70c05-170">AllowOneWordEntry</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowonewordentry)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-171">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-172">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-173">AllowSiteToZoneAssignmentList</span><span class="sxs-lookup"><span data-stu-id="70c05-173">AllowSiteToZoneAssignmentList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsitetozoneassignmentlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-174">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-175">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-175">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-176">AllowsLockedDownTrustedSitesZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="70c05-176">AllowsLockedDownTrustedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowslockeddowntrustedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-177">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-178">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-178">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-179">AllowSoftwareWhenSignatureIsInvalid</span><span class="sxs-lookup"><span data-stu-id="70c05-179">AllowSoftwareWhenSignatureIsInvalid</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsoftwarewhensignatureisinvalid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-180">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-181">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-182">AllowsRestrictedSitesZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="70c05-182">AllowsRestrictedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsrestrictedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-183">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-184">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-184">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-185">AllowSuggestedSites</span><span class="sxs-lookup"><span data-stu-id="70c05-185">AllowSuggestedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsuggestedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-186">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-187">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-187">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-188">AllowTrustedSitesZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="70c05-188">AllowTrustedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowtrustedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-189">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-190">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-190">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-191">CheckServerCertificateRevocation</span><span class="sxs-lookup"><span data-stu-id="70c05-191">CheckServerCertificateRevocation</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-checkservercertificaterevocation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-192">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-193">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-193">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-194">CheckSignaturesOnDownloadedPrograms</span><span class="sxs-lookup"><span data-stu-id="70c05-194">CheckSignaturesOnDownloadedPrograms</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-checksignaturesondownloadedprograms)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-195">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-196">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-196">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-197">ConsistentMimeHandlingInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="70c05-197">ConsistentMimeHandlingInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-consistentmimehandlinginternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-198">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-199">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-199">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-200">DisableAdobeFlash</span><span class="sxs-lookup"><span data-stu-id="70c05-200">DisableAdobeFlash</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableadobeflash)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-201">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-202">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-202">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="70c05-203">DisableBlockingOfOutdatedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="70c05-203">DisableBlockingOfOutdatedActiveXControls</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-204">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-205">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-205">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-206">DisableBypassOfSmartScreenWarnings</span><span class="sxs-lookup"><span data-stu-id="70c05-206">DisableBypassOfSmartScreenWarnings</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablebypassofsmartscreenwarnings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-207">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-208">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-208">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-209">DisableBypassOfSmartScreenWarningsAboutUncommonFiles</span><span class="sxs-lookup"><span data-stu-id="70c05-209">DisableBypassOfSmartScreenWarningsAboutUncommonFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablebypassofsmartscreenwarningsaboutuncommonfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-210">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-211">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-211">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-212">DisableConfiguringHistory</span><span class="sxs-lookup"><span data-stu-id="70c05-212">DisableConfiguringHistory</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableconfiguringhistory)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-213">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-214">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-214">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-215">DisableCrashDetection</span><span class="sxs-lookup"><span data-stu-id="70c05-215">DisableCrashDetection</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablecrashdetection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-216">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-217">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-217">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-218">DisableCustomerExperienceImprovementProgramParticipation</span><span class="sxs-lookup"><span data-stu-id="70c05-218">DisableCustomerExperienceImprovementProgramParticipation</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablecustomerexperienceimprovementprogramparticipation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-219">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-220">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-220">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-221">DisableDeletingUserVisitedWebsites</span><span class="sxs-lookup"><span data-stu-id="70c05-221">DisableDeletingUserVisitedWebsites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disabledeletinguservisitedwebsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-222">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-223">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-223">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-224">DisableEnclosureDownloading</span><span class="sxs-lookup"><span data-stu-id="70c05-224">DisableEnclosureDownloading</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableenclosuredownloading)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-225">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-226">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-226">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-227">DisableEncryptionSupport</span><span class="sxs-lookup"><span data-stu-id="70c05-227">DisableEncryptionSupport</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableencryptionsupport)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-228">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-228">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-229">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-229">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-230">DisableFirstRunWizard</span><span class="sxs-lookup"><span data-stu-id="70c05-230">DisableFirstRunWizard</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablefirstrunwizard)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-231">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-232">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-232">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-233">DisableFlipAheadFeature</span><span class="sxs-lookup"><span data-stu-id="70c05-233">DisableFlipAheadFeature</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableflipaheadfeature)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-234">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-234">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-235">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-235">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-236">DisableHomePageChange</span><span class="sxs-lookup"><span data-stu-id="70c05-236">DisableHomePageChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablehomepagechange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-237">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-238">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-238">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-239">DisableIgnoringCertificateErrors</span><span class="sxs-lookup"><span data-stu-id="70c05-239">DisableIgnoringCertificateErrors</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableignoringcertificateerrors)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-240">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-241">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-241">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-242">DisableInPrivateBrowsing</span><span class="sxs-lookup"><span data-stu-id="70c05-242">DisableInPrivateBrowsing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableinprivatebrowsing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-243">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-244">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-244">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-245">DisableProcessesInEnhancedProtectedMode</span><span class="sxs-lookup"><span data-stu-id="70c05-245">DisableProcessesInEnhancedProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableprocessesinenhancedprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-246">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-247">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-247">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-248">DisableProxyChange</span><span class="sxs-lookup"><span data-stu-id="70c05-248">DisableProxyChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableproxychange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-249">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-250">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-250">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-251">DisableSearchProviderChange</span><span class="sxs-lookup"><span data-stu-id="70c05-251">DisableSearchProviderChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesearchproviderchange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-252">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-253">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-253">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-254">DisableSecondaryHomePageChange</span><span class="sxs-lookup"><span data-stu-id="70c05-254">DisableSecondaryHomePageChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesecondaryhomepagechange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-255">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-256">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-256">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-257">DisableSecuritySettingsCheck</span><span class="sxs-lookup"><span data-stu-id="70c05-257">DisableSecuritySettingsCheck</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesecuritysettingscheck)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-258">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-259">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-259">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-260">DoNotAllowActiveXControlsInProtectedMode</span><span class="sxs-lookup"><span data-stu-id="70c05-260">DoNotAllowActiveXControlsInProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotallowactivexcontrolsinprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-261">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-262">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-262">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-263">DoNotBlockOutdatedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="70c05-263">DoNotBlockOutdatedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotblockoutdatedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-264">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-265">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-265">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-266">DoNotBlockOutdatedActiveXControlsOnSpecificDomains</span><span class="sxs-lookup"><span data-stu-id="70c05-266">DoNotBlockOutdatedActiveXControlsOnSpecificDomains</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotblockoutdatedactivexcontrolsonspecificdomains)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-267">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-267">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-268">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-268">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-269">IncludeAllLocalSites</span><span class="sxs-lookup"><span data-stu-id="70c05-269">IncludeAllLocalSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-includealllocalsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-270">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-270">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-271">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-271">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-272">IncludeAllNetworkPaths</span><span class="sxs-lookup"><span data-stu-id="70c05-272">IncludeAllNetworkPaths</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-includeallnetworkpaths)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-273">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-273">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-274">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-274">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="70c05-275">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="70c05-275">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-276">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-276">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-277">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="70c05-277">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70c05-278">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="70c05-278">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-279">InternetZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="70c05-279">InternetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-280">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-280">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-281">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-281">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-282">InternetZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="70c05-282">InternetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-283">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-283">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-284">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-284">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-285">InternetZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="70c05-285">InternetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-286">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-287">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-287">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-288">InternetZoneAllowCopyPasteViaScript</span><span class="sxs-lookup"><span data-stu-id="70c05-288">InternetZoneAllowCopyPasteViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowcopypasteviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-289">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-290">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-290">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-291">InternetZoneAllowDragAndDropCopyAndPasteFiles</span><span class="sxs-lookup"><span data-stu-id="70c05-291">InternetZoneAllowDragAndDropCopyAndPasteFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowdraganddropcopyandpastefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-292">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-293">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-293">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-294">InternetZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="70c05-294">InternetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-295">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-295">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-296">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-296">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-297">InternetZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="70c05-297">InternetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-298">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-298">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-299">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-299">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-300">InternetZoneAllowLoadingOfXAMLFiles</span><span class="sxs-lookup"><span data-stu-id="70c05-300">InternetZoneAllowLoadingOfXAMLFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowloadingofxamlfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-301">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-302">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-302">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-303">InternetZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="70c05-303">InternetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-304">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-305">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-305">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-306">InternetZoneAllowOnlyApprovedDomainsToUseActiveXControls</span><span class="sxs-lookup"><span data-stu-id="70c05-306">InternetZoneAllowOnlyApprovedDomainsToUseActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowonlyapproveddomainstouseactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-307">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-308">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-308">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-309">InternetZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span><span class="sxs-lookup"><span data-stu-id="70c05-309">InternetZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowonlyapproveddomainstousetdcactivexcontrol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-310">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-311">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-311">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-312">InternetZoneAllowScriptingOfInternetExplorerWebBrowserControls</span><span class="sxs-lookup"><span data-stu-id="70c05-312">InternetZoneAllowScriptingOfInternetExplorerWebBrowserControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptingofinternetexplorerwebbrowsercontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-313">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-314">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-314">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-315">InternetZoneAllowScriptInitiatedWindows</span><span class="sxs-lookup"><span data-stu-id="70c05-315">InternetZoneAllowScriptInitiatedWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptinitiatedwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-316">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-316">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-317">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-317">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-318">InternetZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="70c05-318">InternetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-319">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-320">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-320">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-321">InternetZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="70c05-321">InternetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-322">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-323">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-323">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-324">InternetZoneAllowUpdatesToStatusBarViaScript</span><span class="sxs-lookup"><span data-stu-id="70c05-324">InternetZoneAllowUpdatesToStatusBarViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowupdatestostatusbarviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-325">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-326">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-326">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-327">InternetZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="70c05-327">InternetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-328">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-328">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-329">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-329">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-330">InternetZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="70c05-330">InternetZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-331">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-331">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-332">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-332">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-333">InternetZoneDownloadSignedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="70c05-333">InternetZoneDownloadSignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedownloadsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-334">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-334">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-335">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-335">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-336">InternetZoneDownloadUnsignedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="70c05-336">InternetZoneDownloadUnsignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedownloadunsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-337">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-338">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-338">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-339">InternetZoneEnableCrossSiteScriptingFilter</span><span class="sxs-lookup"><span data-stu-id="70c05-339">InternetZoneEnableCrossSiteScriptingFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenablecrosssitescriptingfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-340">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-341">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-341">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-342">InternetZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span><span class="sxs-lookup"><span data-stu-id="70c05-342">InternetZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenabledraggingofcontentfromdifferentdomainsacrosswindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-343">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-343">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-344">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-344">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-345">InternetZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span><span class="sxs-lookup"><span data-stu-id="70c05-345">InternetZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenabledraggingofcontentfromdifferentdomainswithinwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-346">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-347">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-347">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-348">InternetZoneEnableMIMESniffing</span><span class="sxs-lookup"><span data-stu-id="70c05-348">InternetZoneEnableMIMESniffing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenablemimesniffing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-349">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-350">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-350">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-351">InternetZoneEnableProtectedMode</span><span class="sxs-lookup"><span data-stu-id="70c05-351">InternetZoneEnableProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenableprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-352">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-353">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-353">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-354">InternetZoneIncludeLocalPathWhenUploadingFilesToServer</span><span class="sxs-lookup"><span data-stu-id="70c05-354">InternetZoneIncludeLocalPathWhenUploadingFilesToServer</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneincludelocalpathwhenuploadingfilestoserver)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-355">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-356">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-356">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-357">InternetZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="70c05-357">InternetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-358">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-358">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-359">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-359">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-360">InternetZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="70c05-360">InternetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-361">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-362">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-362">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-363">InternetZoneLaunchingApplicationsAndFilesInIFRAME</span><span class="sxs-lookup"><span data-stu-id="70c05-363">InternetZoneLaunchingApplicationsAndFilesInIFRAME</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonelaunchingapplicationsandfilesiniframe)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-364">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-364">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-365">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-365">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-366">InternetZoneLogonOptions</span><span class="sxs-lookup"><span data-stu-id="70c05-366">InternetZoneLogonOptions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonelogonoptions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-367">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-367">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-368">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-368">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-369">InternetZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="70c05-369">InternetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-370">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-370">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-371">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-371">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="70c05-372">InternetZoneRunNETFrameworkReliantComponentsNotSignedWithAuthenticode</span><span class="sxs-lookup"><span data-stu-id="70c05-372">InternetZoneRunNETFrameworkReliantComponentsNotSignedWithAuthenticode</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-373">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-373">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-374">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-374">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-375">InternetZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span><span class="sxs-lookup"><span data-stu-id="70c05-375">InternetZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonerunnetframeworkreliantcomponentssignedwithauthenticode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-376">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-376">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-377">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-377">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-378">InternetZoneShowSecurityWarningForPotentiallyUnsafeFiles</span><span class="sxs-lookup"><span data-stu-id="70c05-378">InternetZoneShowSecurityWarningForPotentiallyUnsafeFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneshowsecuritywarningforpotentiallyunsafefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-379">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-380">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-380">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-381">InternetZoneUsePopupBlocker</span><span class="sxs-lookup"><span data-stu-id="70c05-381">InternetZoneUsePopupBlocker</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneusepopupblocker)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-382">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-382">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-383">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-383">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="70c05-384">InternetZoneWebsitesInLessPrivilegedZonesCanNavigateIntoThisZone</span><span class="sxs-lookup"><span data-stu-id="70c05-384">InternetZoneWebsitesInLessPrivilegedZonesCanNavigateIntoThisZone</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-385">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-385">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-386">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-386">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-387">IntranetZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="70c05-387">IntranetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-388">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-388">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-389">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-389">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-390">IntranetZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="70c05-390">IntranetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-391">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-391">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-392">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-392">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-393">IntranetZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="70c05-393">IntranetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-394">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-394">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-395">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-395">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-396">IntranetZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="70c05-396">IntranetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-397">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-397">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-398">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-398">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-399">IntranetZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="70c05-399">IntranetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-400">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-400">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-401">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-401">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-402">IntranetZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="70c05-402">IntranetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-403">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-403">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-404">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-404">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-405">IntranetZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="70c05-405">IntranetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-406">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-406">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-407">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-407">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-408">IntranetZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="70c05-408">IntranetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-409">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-409">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-410">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-410">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-411">IntranetZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="70c05-411">IntranetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-412">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-412">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-413">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-413">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-414">IntranetZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="70c05-414">IntranetZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-415">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-415">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-416">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-416">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-417">IntranetZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="70c05-417">IntranetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-418">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-418">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-419">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-419">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="70c05-420">IntranetZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span><span class="sxs-lookup"><span data-stu-id="70c05-420">IntranetZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-421">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-421">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-422">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-422">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-423">IntranetZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="70c05-423">IntranetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-424">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-424">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-425">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-425">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-426">IntranetZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="70c05-426">IntranetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-427">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-427">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-428">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-428">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-429">LocalMachineZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="70c05-429">LocalMachineZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-430">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-430">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-431">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-431">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-432">LocalMachineZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="70c05-432">LocalMachineZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-433">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-433">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-434">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-434">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-435">LocalMachineZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="70c05-435">LocalMachineZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-436">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-436">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-437">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-437">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-438">LocalMachineZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="70c05-438">LocalMachineZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-439">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-439">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-440">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-440">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-441">LocalMachineZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="70c05-441">LocalMachineZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-442">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-442">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-443">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-443">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-444">LocalMachineZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="70c05-444">LocalMachineZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-445">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-445">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-446">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-446">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-447">LocalMachineZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="70c05-447">LocalMachineZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-448">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-448">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-449">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-449">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-450">LocalMachineZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="70c05-450">LocalMachineZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-451">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-451">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-452">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-452">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-453">LocalMachineZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="70c05-453">LocalMachineZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-454">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-454">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-455">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-455">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-456">LocalMachineZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="70c05-456">LocalMachineZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-457">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-457">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-458">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-458">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-459">LocalMachineZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="70c05-459">LocalMachineZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-460">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-460">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-461">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-461">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-462">LocalMachineZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="70c05-462">LocalMachineZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-463">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-463">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-464">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-464">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-465">LocalMachineZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="70c05-465">LocalMachineZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-466">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-466">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-467">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-467">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-468">LockedDownInternetZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="70c05-468">LockedDownInternetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-469">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-469">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-470">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-470">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-471">LockedDownInternetZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="70c05-471">LockedDownInternetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-472">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-472">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-473">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-473">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-474">LockedDownInternetZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="70c05-474">LockedDownInternetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-475">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-475">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-476">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-476">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-477">LockedDownInternetZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="70c05-477">LockedDownInternetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-478">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-478">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-479">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-479">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-480">LockedDownInternetZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="70c05-480">LockedDownInternetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-481">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-481">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-482">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-482">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-483">LockedDownInternetZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="70c05-483">LockedDownInternetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-484">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-484">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-485">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-485">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-486">LockedDownInternetZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="70c05-486">LockedDownInternetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-487">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-487">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-488">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-488">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-489">LockedDownInternetZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="70c05-489">LockedDownInternetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-490">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-490">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-491">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-491">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-492">LockedDownInternetZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="70c05-492">LockedDownInternetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-493">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-493">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-494">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-494">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-495">LockedDownInternetZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="70c05-495">LockedDownInternetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-496">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-496">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-497">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-497">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-498">LockedDownInternetZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="70c05-498">LockedDownInternetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-499">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-499">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-500">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-500">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-501">LockedDownInternetZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="70c05-501">LockedDownInternetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-502">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-502">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-503">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-503">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-504">LockedDownIntranetZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="70c05-504">LockedDownIntranetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-505">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-505">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-506">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-506">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-507">LockedDownIntranetZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="70c05-507">LockedDownIntranetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-508">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-508">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-509">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-509">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-510">LockedDownIntranetZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="70c05-510">LockedDownIntranetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-511">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-511">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-512">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-512">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-513">LockedDownIntranetZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="70c05-513">LockedDownIntranetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-514">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-514">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-515">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-515">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-516">LockedDownIntranetZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="70c05-516">LockedDownIntranetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-517">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-517">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-518">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-518">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-519">LockedDownIntranetZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="70c05-519">LockedDownIntranetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-520">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-520">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-521">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-521">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-522">LockedDownIntranetZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="70c05-522">LockedDownIntranetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-523">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-523">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-524">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-524">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-525">LockedDownIntranetZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="70c05-525">LockedDownIntranetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-526">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-526">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-527">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-527">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-528">LockedDownIntranetZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="70c05-528">LockedDownIntranetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-529">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-529">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-530">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-530">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-531">LockedDownIntranetZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="70c05-531">LockedDownIntranetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-532">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-532">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-533">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-533">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-534">LockedDownIntranetZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="70c05-534">LockedDownIntranetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-535">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-535">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-536">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-536">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-537">LockedDownLocalMachineZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="70c05-537">LockedDownLocalMachineZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-538">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-538">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-539">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-539">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-540">LockedDownLocalMachineZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="70c05-540">LockedDownLocalMachineZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-541">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-541">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-542">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-542">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-543">LockedDownLocalMachineZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="70c05-543">LockedDownLocalMachineZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-544">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-544">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-545">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-545">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-546">LockedDownLocalMachineZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="70c05-546">LockedDownLocalMachineZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-547">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-547">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-548">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-548">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-549">LockedDownLocalMachineZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="70c05-549">LockedDownLocalMachineZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-550">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-550">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-551">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-551">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-552">LockedDownLocalMachineZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="70c05-552">LockedDownLocalMachineZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-553">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-553">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-554">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-554">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-555">LockedDownLocalMachineZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="70c05-555">LockedDownLocalMachineZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-556">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-556">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-557">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-557">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-558">LockedDownLocalMachineZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="70c05-558">LockedDownLocalMachineZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-559">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-559">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-560">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-560">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-561">LockedDownLocalMachineZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="70c05-561">LockedDownLocalMachineZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-562">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-562">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-563">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-563">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-564">LockedDownLocalMachineZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="70c05-564">LockedDownLocalMachineZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-565">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-565">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-566">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-566">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-567">LockedDownLocalMachineZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="70c05-567">LockedDownLocalMachineZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-568">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-568">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-569">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-569">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-570">LockedDownLocalMachineZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="70c05-570">LockedDownLocalMachineZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-571">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-571">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-572">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-572">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-573">LockedDownRestrictedSitesZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="70c05-573">LockedDownRestrictedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-574">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-574">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-575">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-575">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-576">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="70c05-576">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-577">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-577">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-578">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-578">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-579">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="70c05-579">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-580">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-580">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-581">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-581">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-582">LockedDownRestrictedSitesZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="70c05-582">LockedDownRestrictedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-583">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-583">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-584">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-584">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-585">LockedDownRestrictedSitesZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="70c05-585">LockedDownRestrictedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-586">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-586">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-587">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-587">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-588">LockedDownRestrictedSitesZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="70c05-588">LockedDownRestrictedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-589">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-589">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-590">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-590">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-591">LockedDownRestrictedSitesZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="70c05-591">LockedDownRestrictedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-592">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-592">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-593">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-593">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-594">LockedDownRestrictedSitesZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="70c05-594">LockedDownRestrictedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-595">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-595">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-596">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-596">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-597">LockedDownRestrictedSitesZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="70c05-597">LockedDownRestrictedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-598">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-598">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-599">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-599">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-600">LockedDownRestrictedSitesZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="70c05-600">LockedDownRestrictedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-601">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-601">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-602">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-602">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-603">LockedDownRestrictedSitesZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="70c05-603">LockedDownRestrictedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-604">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-604">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-605">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-605">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-606">LockedDownRestrictedSitesZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="70c05-606">LockedDownRestrictedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-607">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-607">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-608">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-608">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-609">LockedDownTrustedSitesZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="70c05-609">LockedDownTrustedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-610">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-610">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-611">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-611">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-612">LockedDownTrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="70c05-612">LockedDownTrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-613">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-613">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-614">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-614">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-615">LockedDownTrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="70c05-615">LockedDownTrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-616">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-616">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-617">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-617">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-618">LockedDownTrustedSitesZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="70c05-618">LockedDownTrustedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-619">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-619">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-620">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-620">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-621">LockedDownTrustedSitesZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="70c05-621">LockedDownTrustedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-622">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-622">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-623">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-623">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-624">LockedDownTrustedSitesZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="70c05-624">LockedDownTrustedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-625">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-625">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-626">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-626">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-627">LockedDownTrustedSitesZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="70c05-627">LockedDownTrustedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-628">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-628">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-629">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-629">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-630">LockedDownTrustedSitesZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="70c05-630">LockedDownTrustedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-631">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-631">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-632">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-632">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-633">LockedDownTrustedSitesZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="70c05-633">LockedDownTrustedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-634">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-634">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-635">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-635">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-636">LockedDownTrustedSitesZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="70c05-636">LockedDownTrustedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-637">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-637">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-638">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-638">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-639">LockedDownTrustedSitesZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="70c05-639">LockedDownTrustedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-640">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-640">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-641">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-641">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-642">LockedDownTrustedSitesZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="70c05-642">LockedDownTrustedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-643">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-643">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-644">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-644">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-645">MimeSniffingSafetyFeatureInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="70c05-645">MimeSniffingSafetyFeatureInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-mimesniffingsafetyfeatureinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-646">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-646">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-647">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-647">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-648">MKProtocolSecurityRestrictionInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="70c05-648">MKProtocolSecurityRestrictionInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-mkprotocolsecurityrestrictioninternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-649">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-649">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-650">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-650">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-651">NotificationBarInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="70c05-651">NotificationBarInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-notificationbarinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-652">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-652">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-653">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-653">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="70c05-654">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="70c05-654">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-655">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-655">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-656">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="70c05-656">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70c05-657">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="70c05-657">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-658">PreventManagingSmartScreenFilter</span><span class="sxs-lookup"><span data-stu-id="70c05-658">PreventManagingSmartScreenFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-preventmanagingsmartscreenfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-659">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-659">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-660">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-660">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-661">PreventPerUserInstallationOfActiveXControls</span><span class="sxs-lookup"><span data-stu-id="70c05-661">PreventPerUserInstallationOfActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-preventperuserinstallationofactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-662">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-662">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-663">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-663">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-664">ProtectionFromZoneElevationInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="70c05-664">ProtectionFromZoneElevationInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-protectionfromzoneelevationinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-665">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-665">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-666">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-666">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-667">RemoveRunThisTimeButtonForOutdatedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="70c05-667">RemoveRunThisTimeButtonForOutdatedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-removerunthistimebuttonforoutdatedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-668">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-668">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-669">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-669">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-670">RestrictActiveXInstallInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="70c05-670">RestrictActiveXInstallInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictactivexinstallinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-671">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-671">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-672">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-672">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-673">RestrictedSitesZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="70c05-673">RestrictedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-674">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-674">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-675">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-675">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-676">RestrictedSitesZoneAllowActiveScripting</span><span class="sxs-lookup"><span data-stu-id="70c05-676">RestrictedSitesZoneAllowActiveScripting</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowactivescripting)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-677">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-677">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-678">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-678">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-679">RestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="70c05-679">RestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-680">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-680">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-681">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-681">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-682">RestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="70c05-682">RestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-683">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-683">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-684">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-684">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-685">RestrictedSitesZoneAllowBinaryAndScriptBehaviors</span><span class="sxs-lookup"><span data-stu-id="70c05-685">RestrictedSitesZoneAllowBinaryAndScriptBehaviors</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowbinaryandscriptbehaviors)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-686">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-686">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-687">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-687">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-688">RestrictedSitesZoneAllowCopyPasteViaScript</span><span class="sxs-lookup"><span data-stu-id="70c05-688">RestrictedSitesZoneAllowCopyPasteViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowcopypasteviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-689">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-689">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-690">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-690">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-691">RestrictedSitesZoneAllowDragAndDropCopyAndPasteFiles</span><span class="sxs-lookup"><span data-stu-id="70c05-691">RestrictedSitesZoneAllowDragAndDropCopyAndPasteFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowdraganddropcopyandpastefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-692">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-692">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-693">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-693">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-694">RestrictedSitesZoneAllowFileDownloads</span><span class="sxs-lookup"><span data-stu-id="70c05-694">RestrictedSitesZoneAllowFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-695">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-695">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-696">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-696">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-697">RestrictedSitesZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="70c05-697">RestrictedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-698">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-698">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-699">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-699">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-700">RestrictedSitesZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="70c05-700">RestrictedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-701">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-701">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-702">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-702">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-703">RestrictedSitesZoneAllowLoadingOfXAMLFiles</span><span class="sxs-lookup"><span data-stu-id="70c05-703">RestrictedSitesZoneAllowLoadingOfXAMLFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowloadingofxamlfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-704">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-704">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-705">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-705">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-706">RestrictedSitesZoneAllowMETAREFRESH</span><span class="sxs-lookup"><span data-stu-id="70c05-706">RestrictedSitesZoneAllowMETAREFRESH</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowmetarefresh)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-707">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-707">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-708">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-708">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-709">RestrictedSitesZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="70c05-709">RestrictedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-710">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-710">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-711">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-711">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-712">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseActiveXControls</span><span class="sxs-lookup"><span data-stu-id="70c05-712">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowonlyapproveddomainstouseactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-713">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-713">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-714">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-714">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-715">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span><span class="sxs-lookup"><span data-stu-id="70c05-715">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowonlyapproveddomainstousetdcactivexcontrol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-716">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-716">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-717">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-717">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-718">RestrictedSitesZoneAllowScriptingOfInternetExplorerWebBrowserControls</span><span class="sxs-lookup"><span data-stu-id="70c05-718">RestrictedSitesZoneAllowScriptingOfInternetExplorerWebBrowserControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptingofinternetexplorerwebbrowsercontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-719">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-719">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-720">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-720">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-721">RestrictedSitesZoneAllowScriptInitiatedWindows</span><span class="sxs-lookup"><span data-stu-id="70c05-721">RestrictedSitesZoneAllowScriptInitiatedWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptinitiatedwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-722">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-722">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-723">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-723">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-724">RestrictedSitesZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="70c05-724">RestrictedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-725">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-725">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-726">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-726">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-727">RestrictedSitesZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="70c05-727">RestrictedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-728">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-728">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-729">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-729">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-730">RestrictedSitesZoneAllowUpdatesToStatusBarViaScript</span><span class="sxs-lookup"><span data-stu-id="70c05-730">RestrictedSitesZoneAllowUpdatesToStatusBarViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowupdatestostatusbarviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-731">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-731">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-732">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-732">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-733">RestrictedSitesZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="70c05-733">RestrictedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-734">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-734">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-735">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-735">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-736">RestrictedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="70c05-736">RestrictedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-737">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-737">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-738">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-738">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-739">RestrictedSitesZoneDownloadSignedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="70c05-739">RestrictedSitesZoneDownloadSignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedownloadsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-740">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-740">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-741">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-741">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-742">RestrictedSitesZoneDownloadUnsignedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="70c05-742">RestrictedSitesZoneDownloadUnsignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedownloadunsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-743">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-743">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-744">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-744">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-745">RestrictedSitesZoneEnableCrossSiteScriptingFilter</span><span class="sxs-lookup"><span data-stu-id="70c05-745">RestrictedSitesZoneEnableCrossSiteScriptingFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenablecrosssitescriptingfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-746">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-746">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-747">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-747">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-748">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span><span class="sxs-lookup"><span data-stu-id="70c05-748">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenabledraggingofcontentfromdifferentdomainsacrosswindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-749">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-749">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-750">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-750">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-751">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span><span class="sxs-lookup"><span data-stu-id="70c05-751">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenabledraggingofcontentfromdifferentdomainswithinwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-752">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-752">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-753">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-753">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-754">RestrictedSitesZoneEnableMIMESniffing</span><span class="sxs-lookup"><span data-stu-id="70c05-754">RestrictedSitesZoneEnableMIMESniffing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenablemimesniffing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-755">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-755">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-756">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-756">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-757">RestrictedSitesZoneIncludeLocalPathWhenUploadingFilesToServer</span><span class="sxs-lookup"><span data-stu-id="70c05-757">RestrictedSitesZoneIncludeLocalPathWhenUploadingFilesToServer</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneincludelocalpathwhenuploadingfilestoserver)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-758">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-758">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-759">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-759">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-760">RestrictedSitesZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="70c05-760">RestrictedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-761">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-761">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-762">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-762">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-763">RestrictedSitesZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="70c05-763">RestrictedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-764">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-764">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-765">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-765">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-766">RestrictedSitesZoneLaunchingApplicationsAndFilesInIFRAME</span><span class="sxs-lookup"><span data-stu-id="70c05-766">RestrictedSitesZoneLaunchingApplicationsAndFilesInIFRAME</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonelaunchingapplicationsandfilesiniframe)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-767">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-767">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-768">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-768">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-769">RestrictedSitesZoneLogonOptions</span><span class="sxs-lookup"><span data-stu-id="70c05-769">RestrictedSitesZoneLogonOptions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonelogonoptions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-770">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-770">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-771">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-771">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-772">RestrictedSitesZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="70c05-772">RestrictedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-773">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-773">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-774">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-774">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="70c05-775">RestrictedSitesZoneNavigateWindowsAndFramesAcrossDomains</span><span class="sxs-lookup"><span data-stu-id="70c05-775">RestrictedSitesZoneNavigateWindowsAndFramesAcrossDomains</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-776">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-776">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-777">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-777">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-778">RestrictedSitesZoneRunActiveXControlsAndPlugins</span><span class="sxs-lookup"><span data-stu-id="70c05-778">RestrictedSitesZoneRunActiveXControlsAndPlugins</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonerunactivexcontrolsandplugins)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-779">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-779">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-780">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-780">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-781">RestrictedSitesZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span><span class="sxs-lookup"><span data-stu-id="70c05-781">RestrictedSitesZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonerunnetframeworkreliantcomponentssignedwithauthenticode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-782">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-782">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-783">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-783">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-784">RestrictedSitesZoneScriptActiveXControlsMarkedSafeForScripting</span><span class="sxs-lookup"><span data-stu-id="70c05-784">RestrictedSitesZoneScriptActiveXControlsMarkedSafeForScripting</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonescriptactivexcontrolsmarkedsafeforscripting)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-785">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-785">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-786">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-786">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-787">RestrictedSitesZoneScriptingOfJavaApplets</span><span class="sxs-lookup"><span data-stu-id="70c05-787">RestrictedSitesZoneScriptingOfJavaApplets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonescriptingofjavaapplets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-788">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-788">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-789">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-789">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-790">RestrictedSitesZoneShowSecurityWarningForPotentiallyUnsafeFiles</span><span class="sxs-lookup"><span data-stu-id="70c05-790">RestrictedSitesZoneShowSecurityWarningForPotentiallyUnsafeFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneshowsecuritywarningforpotentiallyunsafefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-791">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-791">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-792">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-792">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="70c05-793">RestrictedSitesZoneTurnOnCrossSiteScriptingFilter</span><span class="sxs-lookup"><span data-stu-id="70c05-793">RestrictedSitesZoneTurnOnCrossSiteScriptingFilter</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-794">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-794">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-795">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-795">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-796">RestrictedSitesZoneTurnOnProtectedMode</span><span class="sxs-lookup"><span data-stu-id="70c05-796">RestrictedSitesZoneTurnOnProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneturnonprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-797">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-797">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-798">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-798">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-799">RestrictedSitesZoneUsePopupBlocker</span><span class="sxs-lookup"><span data-stu-id="70c05-799">RestrictedSitesZoneUsePopupBlocker</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneusepopupblocker)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-800">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-800">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-801">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-801">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-802">RestrictFileDownloadInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="70c05-802">RestrictFileDownloadInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictfiledownloadinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-803">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-803">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-804">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-804">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-805">ScriptedWindowSecurityRestrictionsInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="70c05-805">ScriptedWindowSecurityRestrictionsInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-scriptedwindowsecurityrestrictionsinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-806">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-806">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-807">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-807">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-808">SearchProviderList</span><span class="sxs-lookup"><span data-stu-id="70c05-808">SearchProviderList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-searchproviderlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-809">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-809">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-810">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-810">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-811">SpecifyUseOfActiveXInstallerService</span><span class="sxs-lookup"><span data-stu-id="70c05-811">SpecifyUseOfActiveXInstallerService</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-specifyuseofactivexinstallerservice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-812">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-812">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-813">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-813">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-814">TrustedSitesZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="70c05-814">TrustedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-815">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-815">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-816">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-816">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-817">TrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="70c05-817">TrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-818">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-818">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-819">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-819">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-820">TrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="70c05-820">TrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-821">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-821">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-822">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-822">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-823">TrustedSitesZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="70c05-823">TrustedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-824">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-824">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-825">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-825">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-826">TrustedSitesZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="70c05-826">TrustedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-827">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-827">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-828">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-828">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-829">TrustedSitesZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="70c05-829">TrustedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-830">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-830">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-831">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-831">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-832">TrustedSitesZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="70c05-832">TrustedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-833">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-833">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-834">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-834">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-835">TrustedSitesZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="70c05-835">TrustedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-836">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-836">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-837">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-837">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-838">TrustedSitesZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="70c05-838">TrustedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-839">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-839">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-840">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-840">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-841">TrustedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="70c05-841">TrustedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-842">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-842">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-843">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-843">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="70c05-844">TrustedSitesZoneDontRunAntimalwareProgramsAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="70c05-844">TrustedSitesZoneDontRunAntimalwareProgramsAgainstActiveXControls</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-845">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-845">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-846">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-846">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-847">TrustedSitesZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="70c05-847">TrustedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-848">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-848">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-849">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-849">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="70c05-850">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedAsSafe</span><span class="sxs-lookup"><span data-stu-id="70c05-850">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedAsSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-851">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-851">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-852">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-852">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="70c05-853">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span><span class="sxs-lookup"><span data-stu-id="70c05-853">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-854">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-854">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-855">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-855">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-856">TrustedSitesZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="70c05-856">TrustedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-857">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-857">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-858">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-858">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70c05-859">TrustedSitesZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="70c05-859">TrustedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70c05-860">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="70c05-860">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70c05-861">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="70c05-861">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="70c05-862">Requisitos</span><span class="sxs-lookup"><span data-stu-id="70c05-862">Requirements</span></span>



| <span data-ttu-id="70c05-863">Requisito</span><span class="sxs-lookup"><span data-stu-id="70c05-863">Requirement</span></span> | <span data-ttu-id="70c05-864">Valor</span><span class="sxs-lookup"><span data-stu-id="70c05-864">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70c05-865">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="70c05-865">Minimum supported client</span></span><br/> | <span data-ttu-id="70c05-866">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="70c05-866">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="70c05-867">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="70c05-867">Minimum supported server</span></span><br/> | <span data-ttu-id="70c05-868">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="70c05-868">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="70c05-869">Namespace</span><span class="sxs-lookup"><span data-stu-id="70c05-869">Namespace</span></span><br/>                | <span data-ttu-id="70c05-870">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="70c05-870">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="70c05-871">MOF</span><span class="sxs-lookup"><span data-stu-id="70c05-871">MOF</span></span><br/>                      | <dl> <span data-ttu-id="70c05-872"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="70c05-872"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="70c05-873">DLL</span><span class="sxs-lookup"><span data-stu-id="70c05-873">DLL</span></span><br/>                      | <dl> <span data-ttu-id="70c05-874"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="70c05-874"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

