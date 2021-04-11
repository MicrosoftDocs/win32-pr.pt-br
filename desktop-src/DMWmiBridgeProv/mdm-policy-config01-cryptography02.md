---
title: Classe MDM_Policy_Config01_Cryptography02
description: A \_ classe MDM Policy \_ Config01 \_ Cryptography02 representa políticas relacionadas à criptografia.
ms.assetid: e1e06dbd-507e-4da5-bcd5-4d551bd99302
keywords:
- Classe MDM_Policy_Config01_Cryptography02
- Classe MDM_Policy_Config01_Cryptography02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Cryptography02
- MDM_Policy_Config01_Cryptography02.InstanceID
- MDM_Policy_Config01_Cryptography02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92f13a5a04e3d312d8ba262359847719652ecc4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454914"
---
# <a name="mdm_policy_config01_cryptography02-class"></a><span data-ttu-id="17dea-105">\_Classe MDM \_ Config01 \_ Cryptography02</span><span class="sxs-lookup"><span data-stu-id="17dea-105">MDM\_Policy\_Config01\_Cryptography02 class</span></span>

<span data-ttu-id="17dea-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="17dea-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="17dea-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="17dea-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="17dea-108">A classe **MDM \_ Policy \_ Config01 \_ Cryptography02** representa políticas relacionadas à criptografia.</span><span class="sxs-lookup"><span data-stu-id="17dea-108">The **MDM\_Policy\_Config01\_Cryptography02** class represents policies related to cryptography.</span></span>

<span data-ttu-id="17dea-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="17dea-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="17dea-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="17dea-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Cryptography02
{
  string InstanceID;
  string ParentID;
  sint32 AllowFipsAlgorithmPolicy;
  string TLSCipherSuites;
};
```

## <a name="members"></a><span data-ttu-id="17dea-111">Membros</span><span class="sxs-lookup"><span data-stu-id="17dea-111">Members</span></span>

<span data-ttu-id="17dea-112">A **classe \_ \_ Config01 \_ Cryptography02 da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="17dea-112">The **MDM\_Policy\_Config01\_Cryptography02** class has these types of members:</span></span>

-   [<span data-ttu-id="17dea-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="17dea-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="17dea-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="17dea-114">Properties</span></span>

<span data-ttu-id="17dea-115">A **classe \_ \_ Config01 \_ Cryptography02 da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="17dea-115">The **MDM\_Policy\_Config01\_Cryptography02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="17dea-116">AllowFipsAlgorithmPolicy</span><span class="sxs-lookup"><span data-stu-id="17dea-116">AllowFipsAlgorithmPolicy</span></span>](/windows/client-management/mdm/policy-csp-cryptography#cryptography-allowfipsalgorithmpolicy)
</dt> <dd> <dl> <dt>

<span data-ttu-id="17dea-117">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="17dea-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="17dea-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="17dea-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="17dea-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="17dea-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17dea-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="17dea-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="17dea-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="17dea-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="17dea-122">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="17dea-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="17dea-123">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="17dea-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="17dea-124">Para essa classe, a cadeia de caracteres é "Cryptography"</span><span class="sxs-lookup"><span data-stu-id="17dea-124">For this class, the string is "Cryptography"</span></span>

</dd> <dt>

<span data-ttu-id="17dea-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="17dea-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17dea-126">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="17dea-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="17dea-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="17dea-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="17dea-128">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="17dea-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="17dea-129">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="17dea-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="17dea-130">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/Policy/Config"</span><span class="sxs-lookup"><span data-stu-id="17dea-130">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> <dt>

[<span data-ttu-id="17dea-131">TLSCipherSuites</span><span class="sxs-lookup"><span data-stu-id="17dea-131">TLSCipherSuites</span></span>](/windows/client-management/mdm/policy-csp-cryptography#cryptography-tlsciphersuites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="17dea-132">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="17dea-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="17dea-133">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="17dea-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="17dea-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="17dea-134">Requirements</span></span>



| <span data-ttu-id="17dea-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="17dea-135">Requirement</span></span> | <span data-ttu-id="17dea-136">Valor</span><span class="sxs-lookup"><span data-stu-id="17dea-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17dea-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="17dea-137">Minimum supported client</span></span><br/> | <span data-ttu-id="17dea-138">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="17dea-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="17dea-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="17dea-139">Minimum supported server</span></span><br/> | <span data-ttu-id="17dea-140">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="17dea-140">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="17dea-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="17dea-141">Namespace</span></span><br/>                | <span data-ttu-id="17dea-142">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="17dea-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="17dea-143">MOF</span><span class="sxs-lookup"><span data-stu-id="17dea-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="17dea-144"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="17dea-144"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="17dea-145">DLL</span><span class="sxs-lookup"><span data-stu-id="17dea-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17dea-146"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17dea-146"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17dea-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="17dea-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17dea-148">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="17dea-148">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

