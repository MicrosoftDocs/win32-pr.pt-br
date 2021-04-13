---
title: Classe MDM_Policy_Result01_BitLocker02
description: A \_ classe Result01 Bitlocker02 de política de MDM \_ \_ representa as políticas de BitLocker disponíveis.
ms.assetid: 5b20a129-65a8-4ec1-b938-57ddaca46ac3
keywords:
- Classe MDM_Policy_Result01_BitLocker02
- Classe MDM_Policy_Result01_BitLocker02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_BitLocker02
- MDM_Policy_Result01_BitLocker02.InstanceID
- MDM_Policy_Result01_BitLocker02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b063ab67411d8be7fc4c819934b63c0af0096ec5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455931"
---
# <a name="mdm_policy_result01_bitlocker02-class"></a><span data-ttu-id="39aa0-105">\_Classe MDM \_ Result01 \_ BitLocker02</span><span class="sxs-lookup"><span data-stu-id="39aa0-105">MDM\_Policy\_Result01\_BitLocker02 class</span></span>

<span data-ttu-id="39aa0-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="39aa0-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="39aa0-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="39aa0-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="39aa0-108">A **classe \_ \_ Result01 \_ Bitlocker02 de política de MDM** representa as políticas de BitLocker disponíveis.</span><span class="sxs-lookup"><span data-stu-id="39aa0-108">The **MDM\_Policy\_Result01\_Bitlocker02** class represents the BitLocker policies available.</span></span>

<span data-ttu-id="39aa0-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="39aa0-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="39aa0-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="39aa0-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_BitLocker02
{
  string InstanceID;
  string ParentID;
  sint32 EncryptionMethod;
};
```

## <a name="members"></a><span data-ttu-id="39aa0-111">Membros</span><span class="sxs-lookup"><span data-stu-id="39aa0-111">Members</span></span>

<span data-ttu-id="39aa0-112">A **classe \_ \_ Result01 \_ BitLocker02 da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="39aa0-112">The **MDM\_Policy\_Result01\_BitLocker02** class has these types of members:</span></span>

-   [<span data-ttu-id="39aa0-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="39aa0-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="39aa0-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="39aa0-114">Properties</span></span>

<span data-ttu-id="39aa0-115">A **classe \_ \_ Result01 \_ BitLocker02 da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="39aa0-115">The **MDM\_Policy\_Result01\_BitLocker02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="39aa0-116">EncryptionMethod</span><span class="sxs-lookup"><span data-stu-id="39aa0-116">EncryptionMethod</span></span>](/windows/client-management/mdm/policy-csp-bitlocker#bitlocker-encryptionmethod)
</dt> <dd> <dl> <dt>

<span data-ttu-id="39aa0-117">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="39aa0-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="39aa0-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="39aa0-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="39aa0-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="39aa0-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39aa0-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="39aa0-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39aa0-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="39aa0-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39aa0-122">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="39aa0-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="39aa0-123">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="39aa0-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="39aa0-124">Para essa classe, a cadeia de caracteres é "BitLocker"</span><span class="sxs-lookup"><span data-stu-id="39aa0-124">For this class, the string is "BitLocker"</span></span>

</dd> <dt>

<span data-ttu-id="39aa0-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="39aa0-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39aa0-126">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="39aa0-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39aa0-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="39aa0-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39aa0-128">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="39aa0-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="39aa0-129">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="39aa0-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="39aa0-130">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/Policy/Result"</span><span class="sxs-lookup"><span data-stu-id="39aa0-130">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="39aa0-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39aa0-131">Requirements</span></span>



| <span data-ttu-id="39aa0-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="39aa0-132">Requirement</span></span> | <span data-ttu-id="39aa0-133">Valor</span><span class="sxs-lookup"><span data-stu-id="39aa0-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39aa0-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="39aa0-134">Minimum supported client</span></span><br/> | <span data-ttu-id="39aa0-135">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="39aa0-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="39aa0-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="39aa0-136">Minimum supported server</span></span><br/> | <span data-ttu-id="39aa0-137">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="39aa0-137">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="39aa0-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="39aa0-138">Namespace</span></span><br/>                | <span data-ttu-id="39aa0-139">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="39aa0-139">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="39aa0-140">MOF</span><span class="sxs-lookup"><span data-stu-id="39aa0-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="39aa0-141"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="39aa0-141"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="39aa0-142">DLL</span><span class="sxs-lookup"><span data-stu-id="39aa0-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="39aa0-143"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39aa0-143"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39aa0-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="39aa0-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39aa0-145">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="39aa0-145">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

