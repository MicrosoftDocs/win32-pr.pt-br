---
title: Classe MDM_Policy_Result01_Authentication02
description: A \_ classe MDM Policy \_ Result01 \_ Authentication02 representa as políticas de gerenciamento de autenticação disponíveis.
ms.assetid: a67275dc-5f4d-4672-9a6e-84fa65cde3ad
keywords:
- Classe MDM_Policy_Result01_Authentication02
- Classe MDM_Policy_Result01_Authentication02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Authentication02
- MDM_Policy_Result01_Authentication02.InstanceID
- MDM_Policy_Result01_Authentication02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80d80979fe7b025ea7b0677436036c8760d4b0ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086374"
---
# <a name="mdm_policy_result01_authentication02-class"></a><span data-ttu-id="89f85-105">\_Classe MDM \_ Result01 \_ Authentication02</span><span class="sxs-lookup"><span data-stu-id="89f85-105">MDM\_Policy\_Result01\_Authentication02 class</span></span>

<span data-ttu-id="89f85-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="89f85-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="89f85-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="89f85-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="89f85-108">A classe **MDM \_ Policy \_ Result01 \_ Authentication02** representa as políticas de gerenciamento de autenticação disponíveis.</span><span class="sxs-lookup"><span data-stu-id="89f85-108">The **MDM\_Policy\_Result01\_Authentication02** class represents the authentication management policies available.</span></span>

<span data-ttu-id="89f85-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="89f85-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="89f85-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="89f85-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Authentication02
{
  string InstanceID;
  string ParentID;
  sint32 AllowAadPasswordReset;
  sint32 AllowFastReconnect;
  sint32 AllowFidoDeviceSignon;
  sint32 AllowSecondaryAuthenticationDevice;
};
```

## <a name="members"></a><span data-ttu-id="89f85-111">Membros</span><span class="sxs-lookup"><span data-stu-id="89f85-111">Members</span></span>

<span data-ttu-id="89f85-112">A **classe \_ \_ Result01 \_ Authentication02 da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="89f85-112">The **MDM\_Policy\_Result01\_Authentication02** class has these types of members:</span></span>

-   [<span data-ttu-id="89f85-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="89f85-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="89f85-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="89f85-114">Properties</span></span>

<span data-ttu-id="89f85-115">A **classe \_ \_ Result01 \_ Authentication02 da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="89f85-115">The **MDM\_Policy\_Result01\_Authentication02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="89f85-116">AllowAadPasswordReset</span><span class="sxs-lookup"><span data-stu-id="89f85-116">AllowAadPasswordReset</span></span>](/windows/client-management/mdm/policy-csp-authentication#authentication-allowaadpasswordreset)
</dt> <dd> <dl> <dt>

<span data-ttu-id="89f85-117">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="89f85-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="89f85-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="89f85-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="89f85-119">AllowFastReconnect</span><span class="sxs-lookup"><span data-stu-id="89f85-119">AllowFastReconnect</span></span>](/windows/client-management/mdm/policy-csp-authentication#authentication-allowfastreconnect)
</dt> <dd> <dl> <dt>

<span data-ttu-id="89f85-120">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="89f85-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="89f85-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="89f85-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="89f85-122">AllowFidoDeviceSignon</span><span class="sxs-lookup"><span data-stu-id="89f85-122">AllowFidoDeviceSignon</span></span>](/windows/client-management/mdm/policy-csp-authentication#authentication-allowfidodevicesignon)
</dt> <dd> <dl> <dt>

<span data-ttu-id="89f85-123">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="89f85-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="89f85-124">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="89f85-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="89f85-125">AllowSecondaryAuthenticationDevice</span><span class="sxs-lookup"><span data-stu-id="89f85-125">AllowSecondaryAuthenticationDevice</span></span>](/windows/client-management/mdm/policy-csp-authentication#authentication-allowsecondaryauthenticationdevice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="89f85-126">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="89f85-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="89f85-127">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="89f85-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="89f85-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="89f85-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89f85-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="89f85-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89f85-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="89f85-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89f85-131">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="89f85-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="89f85-132">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="89f85-132">Identifies the name of the parent node.</span></span> <span data-ttu-id="89f85-133">Para essa classe, a cadeia de caracteres é "Authentication".</span><span class="sxs-lookup"><span data-stu-id="89f85-133">For this class, the string is "Authentication".</span></span>

</dd> <dt>

<span data-ttu-id="89f85-134">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="89f85-134">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89f85-135">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="89f85-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89f85-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="89f85-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89f85-137">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="89f85-137">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="89f85-138">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="89f85-138">Describes the full path to the parent node.</span></span> <span data-ttu-id="89f85-139">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/Policy/Result"</span><span class="sxs-lookup"><span data-stu-id="89f85-139">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="89f85-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="89f85-140">Requirements</span></span>



| <span data-ttu-id="89f85-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="89f85-141">Requirement</span></span> | <span data-ttu-id="89f85-142">Valor</span><span class="sxs-lookup"><span data-stu-id="89f85-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89f85-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="89f85-143">Minimum supported client</span></span><br/> | <span data-ttu-id="89f85-144">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="89f85-144">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="89f85-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="89f85-145">Minimum supported server</span></span><br/> | <span data-ttu-id="89f85-146">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="89f85-146">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="89f85-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="89f85-147">Namespace</span></span><br/>                | <span data-ttu-id="89f85-148">\\DMMap de \\ MDM \\ CIMv2 raiz</span><span class="sxs-lookup"><span data-stu-id="89f85-148">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="89f85-149">MOF</span><span class="sxs-lookup"><span data-stu-id="89f85-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="89f85-150"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="89f85-150"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="89f85-151">DLL</span><span class="sxs-lookup"><span data-stu-id="89f85-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="89f85-152"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89f85-152"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89f85-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="89f85-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89f85-154">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="89f85-154">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

