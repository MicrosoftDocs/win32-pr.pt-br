---
title: Classe MDM_Policy_Config01_Start02
description: A \_ classe MDM Policy \_ Config01 \_ Start02 representa as políticas de tela inicial disponíveis.
ms.assetid: 2aef29c8-164a-4111-9c1a-e63eeec2531e
keywords:
- Classe MDM_Policy_Config01_Start02
- Classe MDM_Policy_Config01_Start02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Start02
- MDM_Policy_Config01_Start02.InstanceID
- MDM_Policy_Config01_Start02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9095fcf1611ef106fed5ad93f059e165ebcac15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455217"
---
# <a name="mdm_policy_config01_start02-class"></a><span data-ttu-id="ad73c-105">\_Classe MDM \_ Config01 \_ Start02</span><span class="sxs-lookup"><span data-stu-id="ad73c-105">MDM\_Policy\_Config01\_Start02 class</span></span>

<span data-ttu-id="ad73c-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="ad73c-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="ad73c-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="ad73c-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="ad73c-108">A classe **MDM \_ Policy \_ Config01 \_ Start02** representa as políticas de tela inicial disponíveis.</span><span class="sxs-lookup"><span data-stu-id="ad73c-108">The **MDM\_Policy\_Config01\_Start02** class represents the start screen policies available.</span></span>

<span data-ttu-id="ad73c-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="ad73c-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad73c-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ad73c-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Start02
{
  string InstanceID;
  string ParentID;
  sint32 AllowPinnedFolderVideos;
  sint32 AllowPinnedFolderSettings;
  sint32 AllowPinnedFolderPictures;
  sint32 AllowPinnedFolderPersonalFolder;
  sint32 AllowPinnedFolderNetwork;
  sint32 AllowPinnedFolderMusic;
  sint32 AllowPinnedFolderHomeGroup;
  sint32 AllowPinnedFolderFileExplorer;
  sint32 AllowPinnedFolderDownloads;
  sint32 AllowPinnedFolderDocuments;
  sint32 ForceStartSize;
  string StartLayout;
  sint32 NoPinningToTaskbar;
  string ImportEdgeAssets;
  sint32 HideUserTile;
  sint32 HideSwitchAccount;
  sint32 HideSleep;
  sint32 HideSignOut;
  sint32 HideShutDown;
  sint32 HideRestart;
  sint32 HideRecentlyAddedApps;
  sint32 HideRecentJumplists;
  sint32 HidePowerButton;
  sint32 HideLock;
  sint32 HideHibernate;
  sint32 HideFrequentlyUsedApps;
  sint32 HideChangeAccountSettings;
  sint32 HideAppList;
};
```

## <a name="members"></a><span data-ttu-id="ad73c-111">Membros</span><span class="sxs-lookup"><span data-stu-id="ad73c-111">Members</span></span>

<span data-ttu-id="ad73c-112">A **classe \_ \_ Config01 \_ Start02 da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="ad73c-112">The **MDM\_Policy\_Config01\_Start02** class has these types of members:</span></span>

-   [<span data-ttu-id="ad73c-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ad73c-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ad73c-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ad73c-114">Properties</span></span>

<span data-ttu-id="ad73c-115">A **classe \_ \_ Config01 \_ Start02 da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="ad73c-115">The **MDM\_Policy\_Config01\_Start02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="ad73c-116">AllowPinnedFolderDocuments</span><span class="sxs-lookup"><span data-stu-id="ad73c-116">AllowPinnedFolderDocuments</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfolderdocuments)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad73c-117">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ad73c-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad73c-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ad73c-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ad73c-119">AllowPinnedFolderDownloads</span><span class="sxs-lookup"><span data-stu-id="ad73c-119">AllowPinnedFolderDownloads</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfolderdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad73c-120">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ad73c-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad73c-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ad73c-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ad73c-122">AllowPinnedFolderFileExplorer</span><span class="sxs-lookup"><span data-stu-id="ad73c-122">AllowPinnedFolderFileExplorer</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfolderfileexplorer)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad73c-123">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ad73c-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad73c-124">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ad73c-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ad73c-125">AllowPinnedFolderHomeGroup</span><span class="sxs-lookup"><span data-stu-id="ad73c-125">AllowPinnedFolderHomeGroup</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfolderhomegroup)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad73c-126">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ad73c-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad73c-127">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ad73c-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ad73c-128">AllowPinnedFolderMusic</span><span class="sxs-lookup"><span data-stu-id="ad73c-128">AllowPinnedFolderMusic</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfoldermusic)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad73c-129">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ad73c-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad73c-130">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ad73c-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ad73c-131">AllowPinnedFolderNetwork</span><span class="sxs-lookup"><span data-stu-id="ad73c-131">AllowPinnedFolderNetwork</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfoldernetwork)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad73c-132">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ad73c-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad73c-133">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ad73c-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ad73c-134">AllowPinnedFolderPersonalFolder</span><span class="sxs-lookup"><span data-stu-id="ad73c-134">AllowPinnedFolderPersonalFolder</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfolderpersonalfolder)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad73c-135">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ad73c-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad73c-136">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ad73c-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ad73c-137">AllowPinnedFolderPictures</span><span class="sxs-lookup"><span data-stu-id="ad73c-137">AllowPinnedFolderPictures</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfolderpictures)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad73c-138">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ad73c-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad73c-139">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ad73c-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ad73c-140">AllowPinnedFolderSettings</span><span class="sxs-lookup"><span data-stu-id="ad73c-140">AllowPinnedFolderSettings</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfoldersettings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad73c-141">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ad73c-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad73c-142">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ad73c-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ad73c-143">AllowPinnedFolderVideos</span><span class="sxs-lookup"><span data-stu-id="ad73c-143">AllowPinnedFolderVideos</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfoldervideos)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad73c-144">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ad73c-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad73c-145">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ad73c-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ad73c-146">ForceStartSize</span><span class="sxs-lookup"><span data-stu-id="ad73c-146">ForceStartSize</span></span>](/windows/client-management/mdm/policy-csp-start#start-forcestartsize)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad73c-147">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ad73c-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad73c-148">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ad73c-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ad73c-149">HideAppList</span><span class="sxs-lookup"><span data-stu-id="ad73c-149">HideAppList</span></span>](/windows/client-management/mdm/policy-csp-start#start-hideapplist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad73c-150">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ad73c-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad73c-151">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ad73c-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ad73c-152">HideChangeAccountSettings</span><span class="sxs-lookup"><span data-stu-id="ad73c-152">HideChangeAccountSettings</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidechangeaccountsettings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad73c-153">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ad73c-153">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad73c-154">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ad73c-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ad73c-155">HideFrequentlyUsedApps</span><span class="sxs-lookup"><span data-stu-id="ad73c-155">HideFrequentlyUsedApps</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidefrequentlyusedapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad73c-156">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ad73c-156">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad73c-157">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ad73c-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ad73c-158">HideHibernate</span><span class="sxs-lookup"><span data-stu-id="ad73c-158">HideHibernate</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidehibernate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad73c-159">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ad73c-159">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad73c-160">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ad73c-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ad73c-161">HideLock</span><span class="sxs-lookup"><span data-stu-id="ad73c-161">HideLock</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidelock)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad73c-162">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ad73c-162">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad73c-163">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ad73c-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ad73c-164">HidePowerButton</span><span class="sxs-lookup"><span data-stu-id="ad73c-164">HidePowerButton</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidepowerbutton)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad73c-165">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ad73c-165">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad73c-166">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ad73c-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ad73c-167">HideRecentJumplists</span><span class="sxs-lookup"><span data-stu-id="ad73c-167">HideRecentJumplists</span></span>](/windows/client-management/mdm/policy-csp-start#start-hiderecentjumplists)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad73c-168">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ad73c-168">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad73c-169">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ad73c-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ad73c-170">HideRecentlyAddedApps</span><span class="sxs-lookup"><span data-stu-id="ad73c-170">HideRecentlyAddedApps</span></span>](/windows/client-management/mdm/policy-csp-start#start-hiderecentlyaddedapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad73c-171">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ad73c-171">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad73c-172">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ad73c-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ad73c-173">HideRestart</span><span class="sxs-lookup"><span data-stu-id="ad73c-173">HideRestart</span></span>](/windows/client-management/mdm/policy-csp-start#start-hiderestart)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad73c-174">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ad73c-174">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad73c-175">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ad73c-175">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ad73c-176">HideShutDown</span><span class="sxs-lookup"><span data-stu-id="ad73c-176">HideShutDown</span></span>](/windows/client-management/mdm/policy-csp-start#start-hideshutdown)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad73c-177">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ad73c-177">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad73c-178">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ad73c-178">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ad73c-179">HideSignOut</span><span class="sxs-lookup"><span data-stu-id="ad73c-179">HideSignOut</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidesignout)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad73c-180">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ad73c-180">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad73c-181">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ad73c-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ad73c-182">HideSleep</span><span class="sxs-lookup"><span data-stu-id="ad73c-182">HideSleep</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidesleep)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad73c-183">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ad73c-183">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad73c-184">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ad73c-184">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ad73c-185">HideSwitchAccount</span><span class="sxs-lookup"><span data-stu-id="ad73c-185">HideSwitchAccount</span></span>](/windows/client-management/mdm/policy-csp-start#start-hideswitchaccount)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad73c-186">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ad73c-186">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad73c-187">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ad73c-187">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ad73c-188">HideUserTile</span><span class="sxs-lookup"><span data-stu-id="ad73c-188">HideUserTile</span></span>](/windows/client-management/mdm/policy-csp-start#start-hideusertile)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad73c-189">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ad73c-189">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad73c-190">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ad73c-190">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ad73c-191">ImportEdgeAssets</span><span class="sxs-lookup"><span data-stu-id="ad73c-191">ImportEdgeAssets</span></span>](/windows/client-management/mdm/policy-csp-start#start-importedgeassets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad73c-192">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ad73c-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ad73c-193">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ad73c-193">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ad73c-194">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ad73c-194">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad73c-195">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ad73c-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ad73c-196">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ad73c-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad73c-197">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ad73c-197">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ad73c-198">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="ad73c-198">Identifies the name of the parent node.</span></span> <span data-ttu-id="ad73c-199">Para essa classe, a cadeia de caracteres é "Start"</span><span class="sxs-lookup"><span data-stu-id="ad73c-199">For this class, the string is "Start"</span></span>

</dd> <dt>

[<span data-ttu-id="ad73c-200">NoPinningToTaskbar</span><span class="sxs-lookup"><span data-stu-id="ad73c-200">NoPinningToTaskbar</span></span>](/windows/client-management/mdm/policy-csp-start#start-nopinningtotaskbar)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad73c-201">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ad73c-201">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad73c-202">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ad73c-202">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ad73c-203">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="ad73c-203">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad73c-204">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ad73c-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ad73c-205">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ad73c-205">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad73c-206">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ad73c-206">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ad73c-207">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="ad73c-207">Describes the full path to the parent node.</span></span> <span data-ttu-id="ad73c-208">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/Policy/Config"</span><span class="sxs-lookup"><span data-stu-id="ad73c-208">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> <dt>

[<span data-ttu-id="ad73c-209">StartLayout</span><span class="sxs-lookup"><span data-stu-id="ad73c-209">StartLayout</span></span>](/windows/client-management/mdm/policy-csp-start#start-startlayout)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad73c-210">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ad73c-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ad73c-211">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ad73c-211">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ad73c-212">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ad73c-212">Requirements</span></span>



| <span data-ttu-id="ad73c-213">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad73c-213">Requirement</span></span> | <span data-ttu-id="ad73c-214">Valor</span><span class="sxs-lookup"><span data-stu-id="ad73c-214">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad73c-215">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ad73c-215">Minimum supported client</span></span><br/> | <span data-ttu-id="ad73c-216">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="ad73c-216">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ad73c-217">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ad73c-217">Minimum supported server</span></span><br/> | <span data-ttu-id="ad73c-218">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="ad73c-218">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="ad73c-219">Namespace</span><span class="sxs-lookup"><span data-stu-id="ad73c-219">Namespace</span></span><br/>                | <span data-ttu-id="ad73c-220">\\DMMap de \\ MDM \\ CIMv2 raiz</span><span class="sxs-lookup"><span data-stu-id="ad73c-220">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="ad73c-221">MOF</span><span class="sxs-lookup"><span data-stu-id="ad73c-221">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ad73c-222"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ad73c-222"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="ad73c-223">DLL</span><span class="sxs-lookup"><span data-stu-id="ad73c-223">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ad73c-224"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ad73c-224"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad73c-225">Confira também</span><span class="sxs-lookup"><span data-stu-id="ad73c-225">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad73c-226">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="ad73c-226">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

