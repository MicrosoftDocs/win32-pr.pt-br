---
title: Classe MDM_Policy_User_Result01_Experience02
description: A \_ classe Result01 Experience02 do usuário da política de MDM \_ \_ \_ representa as políticas de experiência disponíveis.
ms.assetid: 729dfc75-7458-426f-8173-9ba75b4ee306
keywords:
- Classe MDM_Policy_User_Result01_Experience02
- Classe MDM_Policy_User_Result01_Experience02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_User_Result01_Experience02
- MDM_Policy_User_Result01_Experience02.InstanceID
- MDM_Policy_User_Result01_Experience02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 320941108309264a2cce3be6e63edca305c1cd40
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824435"
---
# <a name="mdm_policy_user_result01_experience02-class"></a><span data-ttu-id="839da-105">Result01 de usuário de política de MDM- \_ \_ \_ \_ classe Experience02</span><span class="sxs-lookup"><span data-stu-id="839da-105">MDM\_Policy\_User\_Result01\_Experience02 class</span></span>

<span data-ttu-id="839da-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="839da-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="839da-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="839da-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="839da-108">A **classe \_ \_ \_ Result01 \_ Experience02 do usuário da política de MDM** representa as políticas de experiência disponíveis.</span><span class="sxs-lookup"><span data-stu-id="839da-108">The **MDM\_Policy\_User\_Result01\_Experience02** class represents the experience policies available.</span></span>

<span data-ttu-id="839da-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="839da-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="839da-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="839da-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Result01_Experience02
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

## <a name="members"></a><span data-ttu-id="839da-111">Membros</span><span class="sxs-lookup"><span data-stu-id="839da-111">Members</span></span>

<span data-ttu-id="839da-112">A **classe \_ \_ \_ Result01 \_ Experience02 do usuário da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="839da-112">The **MDM\_Policy\_User\_Result01\_Experience02** class has these types of members:</span></span>

-   [<span data-ttu-id="839da-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="839da-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="839da-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="839da-114">Properties</span></span>

<span data-ttu-id="839da-115">A **classe \_ \_ \_ Result01 \_ Experience02 do usuário da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="839da-115">The **MDM\_Policy\_User\_Result01\_Experience02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="839da-116">AllowTailoredExperiencesWithDiagnosticData</span><span class="sxs-lookup"><span data-stu-id="839da-116">AllowTailoredExperiencesWithDiagnosticData</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowtailoredexperienceswithdiagnosticdata)
</dt> <dd> <dl> <dt>

<span data-ttu-id="839da-117">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="839da-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="839da-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="839da-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="839da-119">AllowThirdPartySuggestionsInWindowsSpotlight</span><span class="sxs-lookup"><span data-stu-id="839da-119">AllowThirdPartySuggestionsInWindowsSpotlight</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowthirdpartysuggestionsinwindowsspotlight)
</dt> <dd> <dl> <dt>

<span data-ttu-id="839da-120">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="839da-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="839da-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="839da-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="839da-122">AllowWindowsConsumerFeatures</span><span class="sxs-lookup"><span data-stu-id="839da-122">AllowWindowsConsumerFeatures</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowwindowsconsumerfeatures)
</dt> <dd> <dl> <dt>

<span data-ttu-id="839da-123">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="839da-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="839da-124">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="839da-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="839da-125">AllowWindowsSpotlight</span><span class="sxs-lookup"><span data-stu-id="839da-125">AllowWindowsSpotlight</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowwindowsspotlight)
</dt> <dd> <dl> <dt>

<span data-ttu-id="839da-126">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="839da-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="839da-127">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="839da-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="839da-128">AllowWindowsSpotlightOnActionCenter</span><span class="sxs-lookup"><span data-stu-id="839da-128">AllowWindowsSpotlightOnActionCenter</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowwindowsspotlightonactioncenter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="839da-129">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="839da-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="839da-130">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="839da-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="839da-131">AllowWindowsSpotlightWindowsWelcomeExperience</span><span class="sxs-lookup"><span data-stu-id="839da-131">AllowWindowsSpotlightWindowsWelcomeExperience</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowwindowsspotlightwindowswelcomeexperience)
</dt> <dd> <dl> <dt>

<span data-ttu-id="839da-132">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="839da-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="839da-133">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="839da-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="839da-134">ConfigureWindowsSpotlightOnLockScreen</span><span class="sxs-lookup"><span data-stu-id="839da-134">ConfigureWindowsSpotlightOnLockScreen</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-configurewindowsspotlightonlockscreen)
</dt> <dd> <dl> <dt>

<span data-ttu-id="839da-135">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="839da-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="839da-136">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="839da-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="839da-137">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="839da-137">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="839da-138">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="839da-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="839da-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="839da-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="839da-140">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="839da-140">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="839da-141">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="839da-141">Identifies the name of the parent node.</span></span> <span data-ttu-id="839da-142">Para essa classe, a cadeia de caracteres é "Experience".</span><span class="sxs-lookup"><span data-stu-id="839da-142">For this class, the string is "Experience".</span></span>

</dd> <dt>

<span data-ttu-id="839da-143">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="839da-143">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="839da-144">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="839da-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="839da-145">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="839da-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="839da-146">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="839da-146">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="839da-147">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="839da-147">Describes the full path to the parent node.</span></span> <span data-ttu-id="839da-148">Para essa classe, a cadeia de caracteres é "./User/Vendor/MSFT/Policy/Result"</span><span class="sxs-lookup"><span data-stu-id="839da-148">For this class, the string is "./User/Vendor/MSFT/Policy/Result"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="839da-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="839da-149">Requirements</span></span>



| <span data-ttu-id="839da-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="839da-150">Requirement</span></span> | <span data-ttu-id="839da-151">Valor</span><span class="sxs-lookup"><span data-stu-id="839da-151">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="839da-152">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="839da-152">Minimum supported client</span></span><br/> | <span data-ttu-id="839da-153">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="839da-153">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="839da-154">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="839da-154">Minimum supported server</span></span><br/> | <span data-ttu-id="839da-155">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="839da-155">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="839da-156">Namespace</span><span class="sxs-lookup"><span data-stu-id="839da-156">Namespace</span></span><br/>                | <span data-ttu-id="839da-157">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="839da-157">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="839da-158">MOF</span><span class="sxs-lookup"><span data-stu-id="839da-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="839da-159"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="839da-159"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl>       |
| <span data-ttu-id="839da-160">DLL</span><span class="sxs-lookup"><span data-stu-id="839da-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="839da-161"><dt>\\DMWmiBridgeProv.dllMOFs</dt></span><span class="sxs-lookup"><span data-stu-id="839da-161"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

