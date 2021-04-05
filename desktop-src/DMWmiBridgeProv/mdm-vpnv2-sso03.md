---
title: Classe MDM_VPNv2_Sso03
description: A \_ classe MDM VPNv2 \_ Sso03 pode ser usada para selecionar um certificado diferente do certificado de autenticação de VPN para a autenticação Kerberos no caso de conformidade do dispositivo.
ms.assetid: 179b6b69-1319-4310-aebc-f61550af6c77
keywords:
- Classe MDM_VPNv2_Sso03
- Classe MDM_VPNv2_Sso03, descrita
topic_type:
- apiref
api_name:
- MDM_VPNv2_Sso03
- MDM_VPNv2_Sso03.InstanceID
- MDM_VPNv2_Sso03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc5f3f10d365e1405981e206963cd98f0b7f803c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918841"
---
# <a name="mdm_vpnv2_sso03-class"></a><span data-ttu-id="3bdb1-105">\_ \_ Classe SSO03 do MDM VPNv2</span><span class="sxs-lookup"><span data-stu-id="3bdb1-105">MDM\_VPNv2\_Sso03 class</span></span>

<span data-ttu-id="3bdb1-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="3bdb1-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="3bdb1-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="3bdb1-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="3bdb1-108">A classe **MDM \_ VPNv2 \_ Sso03** pode ser usada para selecionar um certificado diferente do certificado de autenticação de VPN para a autenticação Kerberos no caso de conformidade do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3bdb1-108">The **MDM\_VPNv2\_Sso03** class can be used to select a certificate different from the VPN Authentication certificate for the Kerberos Authentication in the case of Device Compliance.</span></span>

<span data-ttu-id="3bdb1-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="3bdb1-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3bdb1-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3bdb1-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_Sso03
{
  string  InstanceID;
  string  ParentID;
  boolean Enabled;
  string  IssuerHash;
  string  Eku;
};
```

## <a name="members"></a><span data-ttu-id="3bdb1-111">Membros</span><span class="sxs-lookup"><span data-stu-id="3bdb1-111">Members</span></span>

<span data-ttu-id="3bdb1-112">A **classe \_ \_ Sso03 de MDM VPNv2** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="3bdb1-112">The **MDM\_VPNv2\_Sso03** class has these types of members:</span></span>

-   [<span data-ttu-id="3bdb1-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3bdb1-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3bdb1-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3bdb1-114">Properties</span></span>

<span data-ttu-id="3bdb1-115">A **classe \_ \_ Sso03 do MDM VPNv2** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="3bdb1-115">The **MDM\_VPNv2\_Sso03** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="3bdb1-116">EKU</span><span class="sxs-lookup"><span data-stu-id="3bdb1-116">Eku</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-authentication-certificate-eku)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3bdb1-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3bdb1-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3bdb1-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="3bdb1-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3bdb1-119">Enabled</span><span class="sxs-lookup"><span data-stu-id="3bdb1-119">Enabled</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-devicecompliance-sso-enabled)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3bdb1-120">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="3bdb1-120">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3bdb1-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="3bdb1-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3bdb1-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="3bdb1-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3bdb1-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3bdb1-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3bdb1-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3bdb1-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3bdb1-125">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3bdb1-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="3bdb1-126">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="3bdb1-126">Identifies the name of the parent node.</span></span>

</dd> <dt>

[<span data-ttu-id="3bdb1-127">IssuerHash</span><span class="sxs-lookup"><span data-stu-id="3bdb1-127">IssuerHash</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-devicecompliance-sso-issuerhash)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3bdb1-128">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3bdb1-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3bdb1-129">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="3bdb1-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3bdb1-130">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="3bdb1-130">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3bdb1-131">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3bdb1-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3bdb1-132">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3bdb1-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3bdb1-133">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3bdb1-133">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="3bdb1-134">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="3bdb1-134">Describes the full path to the parent node.</span></span> <span data-ttu-id="3bdb1-135">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/VPNv2/*ProfileName*/DeviceCompliance"</span><span class="sxs-lookup"><span data-stu-id="3bdb1-135">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*/DeviceCompliance"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3bdb1-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3bdb1-136">Requirements</span></span>



| <span data-ttu-id="3bdb1-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="3bdb1-137">Requirement</span></span> | <span data-ttu-id="3bdb1-138">Valor</span><span class="sxs-lookup"><span data-stu-id="3bdb1-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3bdb1-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3bdb1-139">Minimum supported client</span></span><br/> | <span data-ttu-id="3bdb1-140">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="3bdb1-140">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3bdb1-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3bdb1-141">Minimum supported server</span></span><br/> | <span data-ttu-id="3bdb1-142">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="3bdb1-142">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="3bdb1-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="3bdb1-143">Namespace</span></span><br/>                | <span data-ttu-id="3bdb1-144">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="3bdb1-144">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="3bdb1-145">MOF</span><span class="sxs-lookup"><span data-stu-id="3bdb1-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3bdb1-146"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3bdb1-146"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="3bdb1-147">DLL</span><span class="sxs-lookup"><span data-stu-id="3bdb1-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3bdb1-148"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3bdb1-148"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3bdb1-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="3bdb1-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3bdb1-150">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="3bdb1-150">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

