---
title: Classe MDM_Policy_Result01_Cryptography02
description: A \_ classe MDM Policy \_ Result01 \_ Cryptography02 representa políticas relacionadas à criptografia.
ms.assetid: 3ab41bb4-920d-4647-8f05-f6938f51c409
keywords:
- Classe MDM_Policy_Result01_Cryptography02
- Classe MDM_Policy_Result01_Cryptography02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Cryptography02
- MDM_Policy_Result01_Cryptography02.InstanceID
- MDM_Policy_Result01_Cryptography02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6beb62d7d9fdba320220c9bb4de5074fce416ac2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085986"
---
# <a name="mdm_policy_result01_cryptography02-class"></a><span data-ttu-id="bc8c5-105">\_Classe MDM \_ Result01 \_ Cryptography02</span><span class="sxs-lookup"><span data-stu-id="bc8c5-105">MDM\_Policy\_Result01\_Cryptography02 class</span></span>

<span data-ttu-id="bc8c5-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="bc8c5-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="bc8c5-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="bc8c5-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="bc8c5-108">A classe **MDM \_ Policy \_ Result01 \_ Cryptography02** representa políticas relacionadas à criptografia.</span><span class="sxs-lookup"><span data-stu-id="bc8c5-108">The **MDM\_Policy\_Result01\_Cryptography02** class represents policies related to cryptography.</span></span>

<span data-ttu-id="bc8c5-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="bc8c5-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc8c5-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bc8c5-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Cryptography02
{
  string InstanceID;
  string ParentID;
  sint32 AllowFipsAlgorithmPolicy;
  string TLSCipherSuites;
};
```

## <a name="members"></a><span data-ttu-id="bc8c5-111">Membros</span><span class="sxs-lookup"><span data-stu-id="bc8c5-111">Members</span></span>

<span data-ttu-id="bc8c5-112">A **classe \_ \_ Result01 \_ Cryptography02 da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="bc8c5-112">The **MDM\_Policy\_Result01\_Cryptography02** class has these types of members:</span></span>

-   [<span data-ttu-id="bc8c5-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="bc8c5-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bc8c5-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="bc8c5-114">Properties</span></span>

<span data-ttu-id="bc8c5-115">A **classe \_ \_ Result01 \_ Cryptography02 da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="bc8c5-115">The **MDM\_Policy\_Result01\_Cryptography02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="bc8c5-116">AllowFipsAlgorithmPolicy</span><span class="sxs-lookup"><span data-stu-id="bc8c5-116">AllowFipsAlgorithmPolicy</span></span>](/windows/client-management/mdm/policy-csp-cryptography#cryptography-allowfipsalgorithmpolicy)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc8c5-117">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="bc8c5-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc8c5-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="bc8c5-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="bc8c5-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="bc8c5-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc8c5-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="bc8c5-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc8c5-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bc8c5-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc8c5-122">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="bc8c5-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="bc8c5-123">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="bc8c5-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="bc8c5-124">Para essa classe, a cadeia de caracteres é "Cryptography"</span><span class="sxs-lookup"><span data-stu-id="bc8c5-124">For this class, the string is "Cryptography"</span></span>

</dd> <dt>

<span data-ttu-id="bc8c5-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="bc8c5-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc8c5-126">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="bc8c5-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc8c5-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bc8c5-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc8c5-128">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="bc8c5-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="bc8c5-129">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="bc8c5-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="bc8c5-130">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/Policy/Result"</span><span class="sxs-lookup"><span data-stu-id="bc8c5-130">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> <dt>

[<span data-ttu-id="bc8c5-131">TLSCipherSuites</span><span class="sxs-lookup"><span data-stu-id="bc8c5-131">TLSCipherSuites</span></span>](/windows/client-management/mdm/policy-csp-cryptography#cryptography-tlsciphersuites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc8c5-132">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="bc8c5-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc8c5-133">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="bc8c5-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bc8c5-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bc8c5-134">Requirements</span></span>



| <span data-ttu-id="bc8c5-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc8c5-135">Requirement</span></span> | <span data-ttu-id="bc8c5-136">Valor</span><span class="sxs-lookup"><span data-stu-id="bc8c5-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc8c5-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bc8c5-137">Minimum supported client</span></span><br/> | <span data-ttu-id="bc8c5-138">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="bc8c5-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bc8c5-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bc8c5-139">Minimum supported server</span></span><br/> | <span data-ttu-id="bc8c5-140">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="bc8c5-140">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="bc8c5-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="bc8c5-141">Namespace</span></span><br/>                | <span data-ttu-id="bc8c5-142">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="bc8c5-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="bc8c5-143">MOF</span><span class="sxs-lookup"><span data-stu-id="bc8c5-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bc8c5-144"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bc8c5-144"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="bc8c5-145">DLL</span><span class="sxs-lookup"><span data-stu-id="bc8c5-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc8c5-146"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc8c5-146"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc8c5-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="bc8c5-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc8c5-148">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="bc8c5-148">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

