---
title: Classe MDM_Policy_Config01_Authentication02
description: A \_ classe MDM Policy \_ Config01 \_ Authentication02 representa as políticas de gerenciamento de autenticação disponíveis.
ms.assetid: 928e0b60-5533-45dc-90e6-be7d70210138
keywords:
- Classe MDM_Policy_Config01_Authentication02
- Classe MDM_Policy_Config01_Authentication02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Authentication02
- MDM_Policy_Config01_Authentication02.InstanceID
- MDM_Policy_Config01_Authentication02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfab66a548f4a92c445f748aca1bb15758ac48c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105811134"
---
# <a name="mdm_policy_config01_authentication02-class"></a><span data-ttu-id="d899e-105">\_Classe MDM \_ Config01 \_ Authentication02</span><span class="sxs-lookup"><span data-stu-id="d899e-105">MDM\_Policy\_Config01\_Authentication02 class</span></span>

<span data-ttu-id="d899e-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="d899e-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="d899e-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="d899e-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="d899e-108">A classe **MDM \_ Policy \_ Config01 \_ Authentication02** representa as políticas de gerenciamento de autenticação disponíveis.</span><span class="sxs-lookup"><span data-stu-id="d899e-108">The **MDM\_Policy\_Config01\_Authentication02** class represents the authentication management policies available.</span></span>

<span data-ttu-id="d899e-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="d899e-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d899e-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d899e-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Authentication02
{
  string InstanceID;
  string ParentID;
  sint32 AllowAadPasswordReset;
  sint32 AllowFastReconnect;
  sint32 AllowFidoDeviceSignon;
  sint32 AllowSecondaryAuthenticationDevice;
};
```

## <a name="members"></a><span data-ttu-id="d899e-111">Membros</span><span class="sxs-lookup"><span data-stu-id="d899e-111">Members</span></span>

<span data-ttu-id="d899e-112">A **classe \_ \_ Config01 \_ Authentication02 da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="d899e-112">The **MDM\_Policy\_Config01\_Authentication02** class has these types of members:</span></span>

-   [<span data-ttu-id="d899e-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d899e-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d899e-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d899e-114">Properties</span></span>

<span data-ttu-id="d899e-115">A **classe \_ \_ Config01 \_ Authentication02 da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="d899e-115">The **MDM\_Policy\_Config01\_Authentication02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="d899e-116">AllowAadPasswordReset</span><span class="sxs-lookup"><span data-stu-id="d899e-116">AllowAadPasswordReset</span></span>](/windows/client-management/mdm/policy-csp-authentication#authentication-allowaadpasswordreset)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d899e-117">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d899e-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d899e-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d899e-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d899e-119">AllowFastReconnect</span><span class="sxs-lookup"><span data-stu-id="d899e-119">AllowFastReconnect</span></span>](/windows/client-management/mdm/policy-csp-authentication#authentication-allowfastreconnect)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d899e-120">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d899e-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d899e-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d899e-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d899e-122">AllowFidoDeviceSignon</span><span class="sxs-lookup"><span data-stu-id="d899e-122">AllowFidoDeviceSignon</span></span>](/windows/client-management/mdm/policy-csp-authentication#authentication-allowfidodevicesignon)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d899e-123">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d899e-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d899e-124">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d899e-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d899e-125">AllowSecondaryAuthenticationDevice</span><span class="sxs-lookup"><span data-stu-id="d899e-125">AllowSecondaryAuthenticationDevice</span></span>](/windows/client-management/mdm/policy-csp-authentication#authentication-allowsecondaryauthenticationdevice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d899e-126">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d899e-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d899e-127">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d899e-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d899e-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d899e-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d899e-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d899e-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d899e-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d899e-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d899e-131">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d899e-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d899e-132">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="d899e-132">Identifies the name of the parent node.</span></span> <span data-ttu-id="d899e-133">Para essa classe, a cadeia de caracteres é "Authentication".</span><span class="sxs-lookup"><span data-stu-id="d899e-133">For this class, the string is "Authentication".</span></span>

</dd> <dt>

<span data-ttu-id="d899e-134">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="d899e-134">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d899e-135">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d899e-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d899e-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d899e-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d899e-137">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d899e-137">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d899e-138">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="d899e-138">Describes the full path to the parent node.</span></span> <span data-ttu-id="d899e-139">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/Policy/Config"</span><span class="sxs-lookup"><span data-stu-id="d899e-139">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d899e-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d899e-140">Requirements</span></span>



| <span data-ttu-id="d899e-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="d899e-141">Requirement</span></span> | <span data-ttu-id="d899e-142">Valor</span><span class="sxs-lookup"><span data-stu-id="d899e-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d899e-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d899e-143">Minimum supported client</span></span><br/> | <span data-ttu-id="d899e-144">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="d899e-144">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d899e-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d899e-145">Minimum supported server</span></span><br/> | <span data-ttu-id="d899e-146">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="d899e-146">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="d899e-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="d899e-147">Namespace</span></span><br/>                | <span data-ttu-id="d899e-148">\\DMMap de \\ MDM \\ CIMv2 raiz</span><span class="sxs-lookup"><span data-stu-id="d899e-148">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="d899e-149">MOF</span><span class="sxs-lookup"><span data-stu-id="d899e-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d899e-150"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d899e-150"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="d899e-151">DLL</span><span class="sxs-lookup"><span data-stu-id="d899e-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d899e-152"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d899e-152"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d899e-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="d899e-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d899e-154">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="d899e-154">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

