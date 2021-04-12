---
title: Classe MDM_Policy_User_Config01_Experience02
description: A \_ classe Config01 Experience02 do usuário da política de MDM \_ \_ \_ representa as políticas de experiência disponíveis.
ms.assetid: 61a5f093-812a-4fcb-940d-d5f0de7f8c5f
keywords:
- Classe MDM_Policy_User_Config01_Experience02
- Classe MDM_Policy_User_Config01_Experience02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_User_Config01_Experience02
- MDM_Policy_User_Config01_Experience02.InstanceID
- MDM_Policy_User_Config01_Experience02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a982728a3b2f2a899cdbdbd6239a29c5310a258e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455522"
---
# <a name="mdm_policy_user_config01_experience02-class"></a><span data-ttu-id="a7818-105">Config01 de usuário de política de MDM- \_ \_ \_ \_ classe Experience02</span><span class="sxs-lookup"><span data-stu-id="a7818-105">MDM\_Policy\_User\_Config01\_Experience02 class</span></span>

<span data-ttu-id="a7818-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="a7818-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="a7818-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="a7818-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="a7818-108">A **classe \_ \_ \_ Config01 \_ Experience02 do usuário da política de MDM** representa as políticas de experiência disponíveis.</span><span class="sxs-lookup"><span data-stu-id="a7818-108">The **MDM\_Policy\_User\_Config01\_Experience02** class represents the experience policies available.</span></span>

<span data-ttu-id="a7818-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="a7818-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7818-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a7818-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Config01_Experience02
{
  string InstanceID;
  string ParentID;
  sint32 AllowTailoredExperiencesWithDiagnosticData;
  sint32 AllowWindowsConsumerFeatures;
  sint32 AllowWindowsSpotlight;
  sint32 AllowWindowsSpotlightWindowsWelcomeExperience;
  sint32 AllowWindowsSpotlightOnActionCenter;
  sint32 ConfigureWindowsSpotlightOnLockScreen;
  sint32 AllowThirdPartySuggestionsInWindowsSpotlight;
};
```

## <a name="members"></a><span data-ttu-id="a7818-111">Membros</span><span class="sxs-lookup"><span data-stu-id="a7818-111">Members</span></span>

<span data-ttu-id="a7818-112">A **classe \_ \_ \_ Config01 \_ Experience02 do usuário da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="a7818-112">The **MDM\_Policy\_User\_Config01\_Experience02** class has these types of members:</span></span>

-   [<span data-ttu-id="a7818-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a7818-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a7818-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a7818-114">Properties</span></span>

<span data-ttu-id="a7818-115">A **classe \_ \_ \_ Config01 \_ Experience02 do usuário da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="a7818-115">The **MDM\_Policy\_User\_Config01\_Experience02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="a7818-116">AllowTailoredExperiencesWithDiagnosticData</span><span class="sxs-lookup"><span data-stu-id="a7818-116">AllowTailoredExperiencesWithDiagnosticData</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowtailoredexperienceswithdiagnosticdata)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7818-117">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a7818-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a7818-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="a7818-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a7818-119">AllowThirdPartySuggestionsInWindowsSpotlight</span><span class="sxs-lookup"><span data-stu-id="a7818-119">AllowThirdPartySuggestionsInWindowsSpotlight</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowthirdpartysuggestionsinwindowsspotlight)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7818-120">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a7818-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a7818-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="a7818-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a7818-122">AllowWindowsConsumerFeatures</span><span class="sxs-lookup"><span data-stu-id="a7818-122">AllowWindowsConsumerFeatures</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowwindowsconsumerfeatures)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7818-123">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a7818-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a7818-124">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="a7818-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a7818-125">AllowWindowsSpotlight</span><span class="sxs-lookup"><span data-stu-id="a7818-125">AllowWindowsSpotlight</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowwindowsspotlight)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7818-126">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a7818-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a7818-127">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="a7818-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a7818-128">AllowWindowsSpotlightOnActionCenter</span><span class="sxs-lookup"><span data-stu-id="a7818-128">AllowWindowsSpotlightOnActionCenter</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowwindowsspotlightonactioncenter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7818-129">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a7818-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a7818-130">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="a7818-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a7818-131">AllowWindowsSpotlightWindowsWelcomeExperience</span><span class="sxs-lookup"><span data-stu-id="a7818-131">AllowWindowsSpotlightWindowsWelcomeExperience</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowwindowsspotlightwindowswelcomeexperience)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7818-132">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a7818-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a7818-133">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="a7818-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a7818-134">ConfigureWindowsSpotlightOnLockScreen</span><span class="sxs-lookup"><span data-stu-id="a7818-134">ConfigureWindowsSpotlightOnLockScreen</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-configurewindowsspotlightonlockscreen)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7818-135">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a7818-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a7818-136">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="a7818-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a7818-137">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="a7818-137">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7818-138">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a7818-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7818-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a7818-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7818-140">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a7818-140">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a7818-141">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="a7818-141">Identifies the name of the parent node.</span></span> <span data-ttu-id="a7818-142">Para essa classe, a cadeia de caracteres é "Experience".</span><span class="sxs-lookup"><span data-stu-id="a7818-142">For this class, the string is "Experience".</span></span>

</dd> <dt>

<span data-ttu-id="a7818-143">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="a7818-143">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7818-144">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a7818-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7818-145">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a7818-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7818-146">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a7818-146">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a7818-147">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="a7818-147">Describes the full path to the parent node.</span></span> <span data-ttu-id="a7818-148">Para essa classe, a cadeia de caracteres é "./User/Vendor/MSFT/Policy/Config"</span><span class="sxs-lookup"><span data-stu-id="a7818-148">For this class, the string is "./User/Vendor/MSFT/Policy/Config"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a7818-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a7818-149">Requirements</span></span>



| <span data-ttu-id="a7818-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7818-150">Requirement</span></span> | <span data-ttu-id="a7818-151">Valor</span><span class="sxs-lookup"><span data-stu-id="a7818-151">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7818-152">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a7818-152">Minimum supported client</span></span><br/> | <span data-ttu-id="a7818-153">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="a7818-153">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="a7818-154">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a7818-154">Minimum supported server</span></span><br/> | <span data-ttu-id="a7818-155">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="a7818-155">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="a7818-156">Namespace</span><span class="sxs-lookup"><span data-stu-id="a7818-156">Namespace</span></span><br/>                | <span data-ttu-id="a7818-157">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="a7818-157">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="a7818-158">MOF</span><span class="sxs-lookup"><span data-stu-id="a7818-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a7818-159"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a7818-159"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl>       |
| <span data-ttu-id="a7818-160">DLL</span><span class="sxs-lookup"><span data-stu-id="a7818-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a7818-161"><dt>\\DMWmiBridgeProv.dllMOFs</dt></span><span class="sxs-lookup"><span data-stu-id="a7818-161"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

