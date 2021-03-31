---
title: Classe MDM_Policy_Result01_Accounts02
description: A \_ classe Result01 Accounts02 de política de MDM \_ \_ representa políticas relacionadas a contas.
ms.assetid: 581d63de-6ea8-4c4a-8b94-06228ed07371
keywords:
- Classe MDM_Policy_Result01_Accounts02
- Classe MDM_Policy_Result01_Accounts02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Accounts02
- MDM_Policy_Result01_Accounts02.InstanceID
- MDM_Policy_Result01_Accounts02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e5c240f9cd4d3703122c0ea051f35ec8326e2df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644691"
---
# <a name="mdm_policy_result01_accounts02-class"></a><span data-ttu-id="47c95-105">\_Classe MDM \_ Result01 \_ Accounts02</span><span class="sxs-lookup"><span data-stu-id="47c95-105">MDM\_Policy\_Result01\_Accounts02 class</span></span>

<span data-ttu-id="47c95-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="47c95-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="47c95-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="47c95-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="47c95-108">A **classe \_ \_ Result01 \_ Accounts02 de política de MDM** representa políticas relacionadas a contas.</span><span class="sxs-lookup"><span data-stu-id="47c95-108">The **MDM\_Policy\_Result01\_Accounts02** class represents policies related to accounts.</span></span>

<span data-ttu-id="47c95-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="47c95-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="47c95-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="47c95-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Accounts02
{
  string InstanceID;
  string ParentID;
  sint32 AllowMicrosoftAccountConnection;
  sint32 AllowMicrosoftAccountSignInAssistant;
  sint32 AllowAddingNonMicrosoftAccountsManually;
  string DomainNamesForEmailSync;
};
```

## <a name="members"></a><span data-ttu-id="47c95-111">Membros</span><span class="sxs-lookup"><span data-stu-id="47c95-111">Members</span></span>

<span data-ttu-id="47c95-112">A **classe \_ \_ Result01 \_ Accounts02 da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="47c95-112">The **MDM\_Policy\_Result01\_Accounts02** class has these types of members:</span></span>

-   [<span data-ttu-id="47c95-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="47c95-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="47c95-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="47c95-114">Properties</span></span>

<span data-ttu-id="47c95-115">A **classe \_ \_ Result01 \_ Accounts02 da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="47c95-115">The **MDM\_Policy\_Result01\_Accounts02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="47c95-116">AllowAddingNonMicrosoftAccountsManually</span><span class="sxs-lookup"><span data-stu-id="47c95-116">AllowAddingNonMicrosoftAccountsManually</span></span>](/windows/client-management/mdm/policy-csp-accounts#accounts-allowaddingnonmicrosoftaccountsmanually)
</dt> <dd> <dl> <dt>

<span data-ttu-id="47c95-117">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="47c95-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="47c95-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="47c95-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="47c95-119">AllowMicrosoftAccountConnection</span><span class="sxs-lookup"><span data-stu-id="47c95-119">AllowMicrosoftAccountConnection</span></span>](/windows/client-management/mdm/policy-csp-accounts#accounts-allowmicrosoftaccountconnection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="47c95-120">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="47c95-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="47c95-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="47c95-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="47c95-122">AllowMicrosoftAccountSignInAssistant</span><span class="sxs-lookup"><span data-stu-id="47c95-122">AllowMicrosoftAccountSignInAssistant</span></span>](/windows/client-management/mdm/policy-csp-accounts#accounts-allowmicrosoftaccountsigninassistant)
</dt> <dd> <dl> <dt>

<span data-ttu-id="47c95-123">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="47c95-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="47c95-124">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="47c95-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="47c95-125">DomainNamesForEmailSync</span><span class="sxs-lookup"><span data-stu-id="47c95-125">DomainNamesForEmailSync</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47c95-126">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="47c95-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="47c95-127">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="47c95-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="47c95-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="47c95-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47c95-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="47c95-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="47c95-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="47c95-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="47c95-131">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="47c95-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="47c95-132">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="47c95-132">Identifies the name of the parent node.</span></span> <span data-ttu-id="47c95-133">Para essa classe, a cadeia de caracteres é "contas".</span><span class="sxs-lookup"><span data-stu-id="47c95-133">For this class, the string is "Accounts".</span></span>

</dd> <dt>

<span data-ttu-id="47c95-134">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="47c95-134">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47c95-135">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="47c95-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="47c95-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="47c95-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="47c95-137">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="47c95-137">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="47c95-138">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="47c95-138">Describes the full path to the parent node.</span></span> <span data-ttu-id="47c95-139">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/Policy/Result"</span><span class="sxs-lookup"><span data-stu-id="47c95-139">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="47c95-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="47c95-140">Requirements</span></span>



| <span data-ttu-id="47c95-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="47c95-141">Requirement</span></span> | <span data-ttu-id="47c95-142">Valor</span><span class="sxs-lookup"><span data-stu-id="47c95-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47c95-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="47c95-143">Minimum supported client</span></span><br/> | <span data-ttu-id="47c95-144">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="47c95-144">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="47c95-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="47c95-145">Minimum supported server</span></span><br/> | <span data-ttu-id="47c95-146">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="47c95-146">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="47c95-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="47c95-147">Namespace</span></span><br/>                | <span data-ttu-id="47c95-148">\\DMMap de \\ MDM \\ CIMv2 raiz</span><span class="sxs-lookup"><span data-stu-id="47c95-148">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="47c95-149">MOF</span><span class="sxs-lookup"><span data-stu-id="47c95-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="47c95-150"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="47c95-150"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="47c95-151">DLL</span><span class="sxs-lookup"><span data-stu-id="47c95-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="47c95-152"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="47c95-152"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47c95-153">Consulte também</span><span class="sxs-lookup"><span data-stu-id="47c95-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47c95-154">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="47c95-154">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

