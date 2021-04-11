---
title: Classe MDM_EnterpriseAPN_01
description: A \_ classe MDM EnterpriseAPN \_ 01 é usada pela empresa para provisionar um APN para a Internet.
ms.assetid: c5fc0a86-98b7-4d0c-aae5-be836e48eee7
keywords:
- Classe MDM_EnterpriseAPN_01
- Classe MDM_EnterpriseAPN_01, descrita
topic_type:
- apiref
api_name:
- MDM_EnterpriseAPN_01
- MDM_EnterpriseAPN_01.InstanceID
- MDM_EnterpriseAPN_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2bf8b9563b2f681e71e355f4c21aa097eedf64a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104163602"
---
# <a name="mdm_enterpriseapn_01-class"></a><span data-ttu-id="f7daa-105">\_Classe MDM EnterpriseAPN \_ 01</span><span class="sxs-lookup"><span data-stu-id="f7daa-105">MDM\_EnterpriseAPN\_01 class</span></span>

<span data-ttu-id="f7daa-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="f7daa-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="f7daa-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="f7daa-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="f7daa-108">A classe **MDM \_ EnterpriseAPN \_ 01** é usada pela empresa para provisionar um APN para a Internet.</span><span class="sxs-lookup"><span data-stu-id="f7daa-108">The **MDM\_EnterpriseAPN\_01** class is used by the enterprise to provision an APN for the Internet.</span></span>

<span data-ttu-id="f7daa-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="f7daa-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7daa-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f7daa-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_EnterpriseAPN_01
{
  string  InstanceID;
  string  ParentID;
  string  APNName;
  string  IPType;
  boolean IsAttachAPN;
  string  ClassId;
  string  AuthType;
  string  UserName;
  string  Password;
  string  IccId;
  boolean AlwaysOn;
  boolean Enabled;
  string  Roaming;
};
```

## <a name="members"></a><span data-ttu-id="f7daa-111">Membros</span><span class="sxs-lookup"><span data-stu-id="f7daa-111">Members</span></span>

<span data-ttu-id="f7daa-112">A classe **MDM \_ EnterpriseAPN \_ 01** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="f7daa-112">The **MDM\_EnterpriseAPN\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="f7daa-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f7daa-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f7daa-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f7daa-114">Properties</span></span>

<span data-ttu-id="f7daa-115">A classe **MDM \_ EnterpriseAPN \_ 01** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="f7daa-115">The **MDM\_EnterpriseAPN\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="f7daa-116">AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="f7daa-116">AlwaysOn</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-alwayson)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7daa-117">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="f7daa-117">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f7daa-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f7daa-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f7daa-119">APNName</span><span class="sxs-lookup"><span data-stu-id="f7daa-119">APNName</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-apnname)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7daa-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f7daa-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7daa-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f7daa-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f7daa-122">AuthType</span><span class="sxs-lookup"><span data-stu-id="f7daa-122">AuthType</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-authtype)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7daa-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f7daa-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7daa-124">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f7daa-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f7daa-125">ClassId</span><span class="sxs-lookup"><span data-stu-id="f7daa-125">ClassId</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-classid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7daa-126">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f7daa-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7daa-127">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f7daa-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f7daa-128">Enabled</span><span class="sxs-lookup"><span data-stu-id="f7daa-128">Enabled</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-enabled)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7daa-129">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="f7daa-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f7daa-130">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f7daa-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f7daa-131">IccId</span><span class="sxs-lookup"><span data-stu-id="f7daa-131">IccId</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-iccid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7daa-132">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f7daa-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7daa-133">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f7daa-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f7daa-134">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f7daa-134">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7daa-135">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f7daa-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7daa-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f7daa-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7daa-137">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f7daa-137">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f7daa-138">Nome da conexão como visto pelo Gerenciador de conexões do Windows.</span><span class="sxs-lookup"><span data-stu-id="f7daa-138">Name of the connection as seen by Windows Connection Manager.</span></span>

</dd> <dt>

[<span data-ttu-id="f7daa-139">IPType</span><span class="sxs-lookup"><span data-stu-id="f7daa-139">IPType</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-iptype)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7daa-140">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f7daa-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7daa-141">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f7daa-141">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f7daa-142">IsAttachAPN</span><span class="sxs-lookup"><span data-stu-id="f7daa-142">IsAttachAPN</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-isattachapn)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7daa-143">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="f7daa-143">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f7daa-144">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f7daa-144">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f7daa-145">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="f7daa-145">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7daa-146">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f7daa-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7daa-147">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f7daa-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7daa-148">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f7daa-148">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f7daa-149">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="f7daa-149">Describes the full path to the parent node.</span></span> <span data-ttu-id="f7daa-150">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/EnterpriseAPN"</span><span class="sxs-lookup"><span data-stu-id="f7daa-150">For this class, the string is "./Vendor/MSFT/EnterpriseAPN"</span></span>

</dd> <dt>

[<span data-ttu-id="f7daa-151">Senha</span><span class="sxs-lookup"><span data-stu-id="f7daa-151">Password</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-password)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7daa-152">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f7daa-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7daa-153">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f7daa-153">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f7daa-154">Roaming</span><span class="sxs-lookup"><span data-stu-id="f7daa-154">Roaming</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-roaming)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7daa-155">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f7daa-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7daa-156">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f7daa-156">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f7daa-157">UserName</span><span class="sxs-lookup"><span data-stu-id="f7daa-157">UserName</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-username)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7daa-158">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f7daa-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7daa-159">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f7daa-159">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f7daa-160">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f7daa-160">Requirements</span></span>



| <span data-ttu-id="f7daa-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7daa-161">Requirement</span></span> | <span data-ttu-id="f7daa-162">Valor</span><span class="sxs-lookup"><span data-stu-id="f7daa-162">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7daa-163">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f7daa-163">Minimum supported client</span></span><br/> | <span data-ttu-id="f7daa-164">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="f7daa-164">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f7daa-165">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f7daa-165">Minimum supported server</span></span><br/> | <span data-ttu-id="f7daa-166">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="f7daa-166">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="f7daa-167">Namespace</span><span class="sxs-lookup"><span data-stu-id="f7daa-167">Namespace</span></span><br/>                | <span data-ttu-id="f7daa-168">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="f7daa-168">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="f7daa-169">MOF</span><span class="sxs-lookup"><span data-stu-id="f7daa-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f7daa-170"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f7daa-170"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="f7daa-171">DLL</span><span class="sxs-lookup"><span data-stu-id="f7daa-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f7daa-172"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7daa-172"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7daa-173">Confira também</span><span class="sxs-lookup"><span data-stu-id="f7daa-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7daa-174">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="f7daa-174">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

