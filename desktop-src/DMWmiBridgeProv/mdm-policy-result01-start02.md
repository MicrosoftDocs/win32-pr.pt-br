---
title: Classe MDM_Policy_Result01_Start02
description: A \_ classe MDM Policy \_ Result01 \_ Start02 representa as políticas de tela inicial disponíveis.
ms.assetid: 997d64f9-b2be-47b8-8a84-97438e7fa842
keywords:
- Classe MDM_Policy_Result01_Start02
- Classe MDM_Policy_Result01_Start02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Start02
- MDM_Policy_Result01_Start02.InstanceID
- MDM_Policy_Result01_Start02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 412e9ccecdc9f691b03a94ba5528eb6b7e3d7315
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009248"
---
# <a name="mdm_policy_result01_start02-class"></a><span data-ttu-id="669ee-105">\_Classe MDM \_ Result01 \_ Start02</span><span class="sxs-lookup"><span data-stu-id="669ee-105">MDM\_Policy\_Result01\_Start02 class</span></span>

<span data-ttu-id="669ee-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="669ee-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="669ee-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="669ee-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="669ee-108">A classe **MDM \_ Policy \_ Result01 \_ Start02** representa as políticas de tela inicial disponíveis.</span><span class="sxs-lookup"><span data-stu-id="669ee-108">The **MDM\_Policy\_Result01\_Start02** class represents the start screen policies available.</span></span>

<span data-ttu-id="669ee-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="669ee-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="669ee-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="669ee-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Start02
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

## <a name="members"></a><span data-ttu-id="669ee-111">Membros</span><span class="sxs-lookup"><span data-stu-id="669ee-111">Members</span></span>

<span data-ttu-id="669ee-112">A **classe \_ \_ Result01 \_ Start02 da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="669ee-112">The **MDM\_Policy\_Result01\_Start02** class has these types of members:</span></span>

-   [<span data-ttu-id="669ee-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="669ee-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="669ee-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="669ee-114">Properties</span></span>

<span data-ttu-id="669ee-115">A **classe \_ \_ Result01 \_ Start02 da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="669ee-115">The **MDM\_Policy\_Result01\_Start02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="669ee-116">AllowPinnedFolderDocuments</span><span class="sxs-lookup"><span data-stu-id="669ee-116">AllowPinnedFolderDocuments</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfolderdocuments)
</dt> <dd> <dl> <dt>

<span data-ttu-id="669ee-117">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="669ee-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="669ee-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="669ee-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="669ee-119">AllowPinnedFolderDownloads</span><span class="sxs-lookup"><span data-stu-id="669ee-119">AllowPinnedFolderDownloads</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfolderdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="669ee-120">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="669ee-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="669ee-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="669ee-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="669ee-122">AllowPinnedFolderFileExplorer</span><span class="sxs-lookup"><span data-stu-id="669ee-122">AllowPinnedFolderFileExplorer</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfolderfileexplorer)
</dt> <dd> <dl> <dt>

<span data-ttu-id="669ee-123">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="669ee-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="669ee-124">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="669ee-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="669ee-125">AllowPinnedFolderHomeGroup</span><span class="sxs-lookup"><span data-stu-id="669ee-125">AllowPinnedFolderHomeGroup</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfolderhomegroup)
</dt> <dd> <dl> <dt>

<span data-ttu-id="669ee-126">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="669ee-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="669ee-127">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="669ee-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="669ee-128">AllowPinnedFolderMusic</span><span class="sxs-lookup"><span data-stu-id="669ee-128">AllowPinnedFolderMusic</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfoldermusic)
</dt> <dd> <dl> <dt>

<span data-ttu-id="669ee-129">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="669ee-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="669ee-130">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="669ee-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="669ee-131">AllowPinnedFolderNetwork</span><span class="sxs-lookup"><span data-stu-id="669ee-131">AllowPinnedFolderNetwork</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfoldernetwork)
</dt> <dd> <dl> <dt>

<span data-ttu-id="669ee-132">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="669ee-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="669ee-133">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="669ee-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="669ee-134">AllowPinnedFolderPersonalFolder</span><span class="sxs-lookup"><span data-stu-id="669ee-134">AllowPinnedFolderPersonalFolder</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfolderpersonalfolder)
</dt> <dd> <dl> <dt>

<span data-ttu-id="669ee-135">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="669ee-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="669ee-136">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="669ee-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="669ee-137">AllowPinnedFolderPictures</span><span class="sxs-lookup"><span data-stu-id="669ee-137">AllowPinnedFolderPictures</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfolderpictures)
</dt> <dd> <dl> <dt>

<span data-ttu-id="669ee-138">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="669ee-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="669ee-139">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="669ee-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="669ee-140">AllowPinnedFolderSettings</span><span class="sxs-lookup"><span data-stu-id="669ee-140">AllowPinnedFolderSettings</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfoldersettings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="669ee-141">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="669ee-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="669ee-142">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="669ee-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="669ee-143">AllowPinnedFolderVideos</span><span class="sxs-lookup"><span data-stu-id="669ee-143">AllowPinnedFolderVideos</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfoldervideos)
</dt> <dd> <dl> <dt>

<span data-ttu-id="669ee-144">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="669ee-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="669ee-145">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="669ee-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="669ee-146">ForceStartSize</span><span class="sxs-lookup"><span data-stu-id="669ee-146">ForceStartSize</span></span>](/windows/client-management/mdm/policy-csp-start#start-forcestartsize)
</dt> <dd> <dl> <dt>

<span data-ttu-id="669ee-147">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="669ee-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="669ee-148">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="669ee-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="669ee-149">HideAppList</span><span class="sxs-lookup"><span data-stu-id="669ee-149">HideAppList</span></span>](/windows/client-management/mdm/policy-csp-start#start-hideapplist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="669ee-150">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="669ee-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="669ee-151">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="669ee-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="669ee-152">HideChangeAccountSettings</span><span class="sxs-lookup"><span data-stu-id="669ee-152">HideChangeAccountSettings</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidechangeaccountsettings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="669ee-153">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="669ee-153">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="669ee-154">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="669ee-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="669ee-155">HideFrequentlyUsedApps</span><span class="sxs-lookup"><span data-stu-id="669ee-155">HideFrequentlyUsedApps</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidefrequentlyusedapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="669ee-156">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="669ee-156">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="669ee-157">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="669ee-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="669ee-158">HideHibernate</span><span class="sxs-lookup"><span data-stu-id="669ee-158">HideHibernate</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidehibernate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="669ee-159">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="669ee-159">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="669ee-160">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="669ee-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="669ee-161">HideLock</span><span class="sxs-lookup"><span data-stu-id="669ee-161">HideLock</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidelock)
</dt> <dd> <dl> <dt>

<span data-ttu-id="669ee-162">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="669ee-162">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="669ee-163">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="669ee-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="669ee-164">HidePowerButton</span><span class="sxs-lookup"><span data-stu-id="669ee-164">HidePowerButton</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidepowerbutton)
</dt> <dd> <dl> <dt>

<span data-ttu-id="669ee-165">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="669ee-165">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="669ee-166">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="669ee-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="669ee-167">HideRecentJumplists</span><span class="sxs-lookup"><span data-stu-id="669ee-167">HideRecentJumplists</span></span>](/windows/client-management/mdm/policy-csp-start#start-hiderecentjumplists)
</dt> <dd> <dl> <dt>

<span data-ttu-id="669ee-168">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="669ee-168">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="669ee-169">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="669ee-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="669ee-170">HideRecentlyAddedApps</span><span class="sxs-lookup"><span data-stu-id="669ee-170">HideRecentlyAddedApps</span></span>](/windows/client-management/mdm/policy-csp-start#start-hiderecentlyaddedapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="669ee-171">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="669ee-171">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="669ee-172">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="669ee-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="669ee-173">HideRestart</span><span class="sxs-lookup"><span data-stu-id="669ee-173">HideRestart</span></span>](/windows/client-management/mdm/policy-csp-start#start-hiderestart)
</dt> <dd> <dl> <dt>

<span data-ttu-id="669ee-174">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="669ee-174">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="669ee-175">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="669ee-175">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="669ee-176">HideShutDown</span><span class="sxs-lookup"><span data-stu-id="669ee-176">HideShutDown</span></span>](/windows/client-management/mdm/policy-csp-start#start-hideshutdown)
</dt> <dd> <dl> <dt>

<span data-ttu-id="669ee-177">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="669ee-177">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="669ee-178">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="669ee-178">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="669ee-179">HideSignOut</span><span class="sxs-lookup"><span data-stu-id="669ee-179">HideSignOut</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidesignout)
</dt> <dd> <dl> <dt>

<span data-ttu-id="669ee-180">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="669ee-180">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="669ee-181">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="669ee-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="669ee-182">HideSleep</span><span class="sxs-lookup"><span data-stu-id="669ee-182">HideSleep</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidesleep)
</dt> <dd> <dl> <dt>

<span data-ttu-id="669ee-183">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="669ee-183">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="669ee-184">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="669ee-184">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="669ee-185">HideSwitchAccount</span><span class="sxs-lookup"><span data-stu-id="669ee-185">HideSwitchAccount</span></span>](/windows/client-management/mdm/policy-csp-start#start-hideswitchaccount)
</dt> <dd> <dl> <dt>

<span data-ttu-id="669ee-186">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="669ee-186">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="669ee-187">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="669ee-187">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="669ee-188">HideUserTile</span><span class="sxs-lookup"><span data-stu-id="669ee-188">HideUserTile</span></span>](/windows/client-management/mdm/policy-csp-start#start-hideusertile)
</dt> <dd> <dl> <dt>

<span data-ttu-id="669ee-189">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="669ee-189">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="669ee-190">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="669ee-190">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="669ee-191">ImportEdgeAssets</span><span class="sxs-lookup"><span data-stu-id="669ee-191">ImportEdgeAssets</span></span>](/windows/client-management/mdm/policy-csp-start#start-importedgeassets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="669ee-192">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="669ee-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="669ee-193">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="669ee-193">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="669ee-194">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="669ee-194">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="669ee-195">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="669ee-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="669ee-196">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="669ee-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="669ee-197">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="669ee-197">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="669ee-198">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="669ee-198">Identifies the name of the parent node.</span></span> <span data-ttu-id="669ee-199">Para essa classe, a cadeia de caracteres é "Start"</span><span class="sxs-lookup"><span data-stu-id="669ee-199">For this class, the string is "Start"</span></span>

</dd> <dt>

[<span data-ttu-id="669ee-200">NoPinningToTaskbar</span><span class="sxs-lookup"><span data-stu-id="669ee-200">NoPinningToTaskbar</span></span>](/windows/client-management/mdm/policy-csp-start#start-nopinningtotaskbar)
</dt> <dd> <dl> <dt>

<span data-ttu-id="669ee-201">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="669ee-201">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="669ee-202">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="669ee-202">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="669ee-203">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="669ee-203">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="669ee-204">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="669ee-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="669ee-205">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="669ee-205">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="669ee-206">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="669ee-206">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="669ee-207">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="669ee-207">Describes the full path to the parent node.</span></span> <span data-ttu-id="669ee-208">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/Policy/Result"</span><span class="sxs-lookup"><span data-stu-id="669ee-208">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> <dt>

[<span data-ttu-id="669ee-209">StartLayout</span><span class="sxs-lookup"><span data-stu-id="669ee-209">StartLayout</span></span>](/windows/client-management/mdm/policy-csp-start#start-startlayout)
</dt> <dd> <dl> <dt>

<span data-ttu-id="669ee-210">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="669ee-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="669ee-211">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="669ee-211">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="669ee-212">Requisitos</span><span class="sxs-lookup"><span data-stu-id="669ee-212">Requirements</span></span>



| <span data-ttu-id="669ee-213">Requisito</span><span class="sxs-lookup"><span data-stu-id="669ee-213">Requirement</span></span> | <span data-ttu-id="669ee-214">Valor</span><span class="sxs-lookup"><span data-stu-id="669ee-214">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="669ee-215">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="669ee-215">Minimum supported client</span></span><br/> | <span data-ttu-id="669ee-216">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="669ee-216">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="669ee-217">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="669ee-217">Minimum supported server</span></span><br/> | <span data-ttu-id="669ee-218">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="669ee-218">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="669ee-219">Namespace</span><span class="sxs-lookup"><span data-stu-id="669ee-219">Namespace</span></span><br/>                | <span data-ttu-id="669ee-220">\\DMMap de \\ MDM \\ CIMv2 raiz</span><span class="sxs-lookup"><span data-stu-id="669ee-220">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="669ee-221">MOF</span><span class="sxs-lookup"><span data-stu-id="669ee-221">MOF</span></span><br/>                      | <dl> <span data-ttu-id="669ee-222"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="669ee-222"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="669ee-223">DLL</span><span class="sxs-lookup"><span data-stu-id="669ee-223">DLL</span></span><br/>                      | <dl> <span data-ttu-id="669ee-224"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="669ee-224"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="669ee-225">Confira também</span><span class="sxs-lookup"><span data-stu-id="669ee-225">See also</span></span>

<dl> <dt>

[<span data-ttu-id="669ee-226">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="669ee-226">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

