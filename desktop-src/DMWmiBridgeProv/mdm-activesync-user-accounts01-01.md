---
title: Classe MDM_ActiveSync_User_Accounts01_01
description: A \_ \_ classe Accounts01 01 do usuário do MDM ActiveSync \_ \_ define todas as contas do ActiveSync disponíveis.
ms.assetid: bcd1fdcb-675a-4833-9d3c-0509e68f7b00
keywords:
- Classe MDM_ActiveSync_User_Accounts01_01
- Classe MDM_ActiveSync_User_Accounts01_01, descrita
topic_type:
- apiref
api_name:
- MDM_ActiveSync_User_Accounts01_01
- MDM_ActiveSync_User_Accounts01_01.InstanceID
- MDM_ActiveSync_User_Accounts01_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a065fb3f33e69b636a35fc848e5d717898f1fa3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455003"
---
# <a name="mdm_activesync_user_accounts01_01-class"></a><span data-ttu-id="e17b2-105">\_ \_ \_ Classe Accounts01 01 do \_ usuário do MDM ActiveSync</span><span class="sxs-lookup"><span data-stu-id="e17b2-105">MDM\_ActiveSync\_User\_Accounts01\_01 class</span></span>

<span data-ttu-id="e17b2-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="e17b2-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="e17b2-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="e17b2-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="e17b2-108">A **classe \_ \_ \_ Accounts01 \_ 01 do usuário do MDM ActiveSync** define todas as contas do ActiveSync disponíveis.</span><span class="sxs-lookup"><span data-stu-id="e17b2-108">The **MDM\_ActiveSync\_User\_Accounts01\_01** class defines all available ActiveSync accounts.</span></span>

<span data-ttu-id="e17b2-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="e17b2-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e17b2-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e17b2-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_ActiveSync_User_Accounts01_01
{
  string InstanceID;
  string ParentID;
  string EmailAddress;
  string Domain;
  string AccountIcon;
  string AccountType;
  string AccountName;
  string Password;
  string ServerName;
  string UserName;
};
```

## <a name="members"></a><span data-ttu-id="e17b2-111">Membros</span><span class="sxs-lookup"><span data-stu-id="e17b2-111">Members</span></span>

<span data-ttu-id="e17b2-112">A **classe \_ \_ \_ Accounts01 \_ 01 do usuário do MDM ActiveSync** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="e17b2-112">The **MDM\_ActiveSync\_User\_Accounts01\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="e17b2-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e17b2-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e17b2-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e17b2-114">Properties</span></span>

<span data-ttu-id="e17b2-115">A classe **MDM \_ ActiveSync \_ user \_ Accounts01 \_ 01** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="e17b2-115">The **MDM\_ActiveSync\_User\_Accounts01\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="e17b2-116">AccountIcon</span><span class="sxs-lookup"><span data-stu-id="e17b2-116">AccountIcon</span></span>](/windows/client-management/mdm/activesync-csp#account-guid-accounticon)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e17b2-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e17b2-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e17b2-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="e17b2-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e17b2-119">AccountName</span><span class="sxs-lookup"><span data-stu-id="e17b2-119">AccountName</span></span>](/windows/client-management/mdm/activesync-csp#account-guid-accountname)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e17b2-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e17b2-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e17b2-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="e17b2-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e17b2-122">AccountType</span><span class="sxs-lookup"><span data-stu-id="e17b2-122">AccountType</span></span>](/windows/client-management/mdm/activesync-csp#account-guid-accounttype)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e17b2-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e17b2-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e17b2-124">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="e17b2-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e17b2-125">Domínio</span><span class="sxs-lookup"><span data-stu-id="e17b2-125">Domain</span></span>](/windows/client-management/mdm/activesync-csp#account-guid-domain)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e17b2-126">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e17b2-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e17b2-127">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="e17b2-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e17b2-128">EmailAddress</span><span class="sxs-lookup"><span data-stu-id="e17b2-128">EmailAddress</span></span>](/windows/client-management/mdm/activesync-csp#account-guid-emailaddress)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e17b2-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e17b2-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e17b2-130">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="e17b2-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e17b2-131">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e17b2-131">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e17b2-132">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e17b2-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e17b2-133">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e17b2-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e17b2-134">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e17b2-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e17b2-135">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="e17b2-135">Identifies the name of the parent node.</span></span>

</dd> <dt>

<span data-ttu-id="e17b2-136">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="e17b2-136">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e17b2-137">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e17b2-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e17b2-138">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e17b2-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e17b2-139">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e17b2-139">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e17b2-140">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="e17b2-140">Describes the full path to the parent node.</span></span> <span data-ttu-id="e17b2-141">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/ActiveSync/"</span><span class="sxs-lookup"><span data-stu-id="e17b2-141">For this class, the string is "./Vendor/MSFT/ActiveSync/"</span></span>

</dd> <dt>

[<span data-ttu-id="e17b2-142">Senha</span><span class="sxs-lookup"><span data-stu-id="e17b2-142">Password</span></span>](/windows/client-management/mdm/activesync-csp#account-guid-password)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e17b2-143">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e17b2-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e17b2-144">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="e17b2-144">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e17b2-145">ServerName</span><span class="sxs-lookup"><span data-stu-id="e17b2-145">ServerName</span></span>](/windows/client-management/mdm/activesync-csp#account-guid-servername)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e17b2-146">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e17b2-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e17b2-147">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="e17b2-147">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e17b2-148">UserName</span><span class="sxs-lookup"><span data-stu-id="e17b2-148">UserName</span></span>](/windows/client-management/mdm/activesync-csp#account-guid-username)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e17b2-149">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e17b2-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e17b2-150">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="e17b2-150">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e17b2-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e17b2-151">Requirements</span></span>



| <span data-ttu-id="e17b2-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="e17b2-152">Requirement</span></span> | <span data-ttu-id="e17b2-153">Valor</span><span class="sxs-lookup"><span data-stu-id="e17b2-153">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e17b2-154">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e17b2-154">Minimum supported client</span></span><br/> | <span data-ttu-id="e17b2-155">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="e17b2-155">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e17b2-156">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e17b2-156">Minimum supported server</span></span><br/> | <span data-ttu-id="e17b2-157">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="e17b2-157">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="e17b2-158">Namespace</span><span class="sxs-lookup"><span data-stu-id="e17b2-158">Namespace</span></span><br/>                | <span data-ttu-id="e17b2-159">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="e17b2-159">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="e17b2-160">MOF</span><span class="sxs-lookup"><span data-stu-id="e17b2-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e17b2-161"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e17b2-161"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="e17b2-162">DLL</span><span class="sxs-lookup"><span data-stu-id="e17b2-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e17b2-163"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e17b2-163"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e17b2-164">Confira também</span><span class="sxs-lookup"><span data-stu-id="e17b2-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e17b2-165">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="e17b2-165">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

