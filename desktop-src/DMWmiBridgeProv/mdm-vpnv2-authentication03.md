---
title: Classe MDM_VPNv2_Authentication03
description: A \_ classe MDM VPNv2 \_ Authentication03 contém informações de autenticação para o perfil VPN nativo.
ms.assetid: 931752a9-6de5-46d4-b9d9-2c59c49e8ed9
keywords:
- Classe MDM_VPNv2_Authentication03
- Classe MDM_VPNv2_Authentication03, descrita
topic_type:
- apiref
api_name:
- MDM_VPNv2_Authentication03
- MDM_VPNv2_Authentication03.InstanceID
- MDM_VPNv2_Authentication03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ca50bcc83df01b4aa5e7ec900985cf15f7e67d1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009386"
---
# <a name="mdm_vpnv2_authentication03-class"></a><span data-ttu-id="11385-105">\_ \_ Classe AUTHENTICATION03 do MDM VPNv2</span><span class="sxs-lookup"><span data-stu-id="11385-105">MDM\_VPNv2\_Authentication03 class</span></span>

<span data-ttu-id="11385-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="11385-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="11385-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="11385-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="11385-108">A classe [**MDM \_ VPNv2 \_ Authentication03**](mdm-vpnv2-01.md) contém informações de autenticação para o perfil VPN nativo.</span><span class="sxs-lookup"><span data-stu-id="11385-108">The [**MDM\_VPNv2\_Authentication03**](mdm-vpnv2-01.md) class contains authentication information for the native VPN profile.</span></span>

<span data-ttu-id="11385-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="11385-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="11385-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="11385-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_Authentication03
{
  string InstanceID;
  string ParentID;
  string UserMethod;
  string MachineMethod;
};
```

## <a name="members"></a><span data-ttu-id="11385-111">Membros</span><span class="sxs-lookup"><span data-stu-id="11385-111">Members</span></span>

<span data-ttu-id="11385-112">A **classe \_ \_ Authentication03 de MDM VPNv2** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="11385-112">The **MDM\_VPNv2\_Authentication03** class has these types of members:</span></span>

-   [<span data-ttu-id="11385-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="11385-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="11385-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="11385-114">Properties</span></span>

<span data-ttu-id="11385-115">A **classe \_ \_ Authentication03 do MDM VPNv2** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="11385-115">The **MDM\_VPNv2\_Authentication03** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="11385-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="11385-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11385-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="11385-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11385-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="11385-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11385-119">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="11385-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="11385-120">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="11385-120">Identifies the name of the parent node.</span></span>

</dd> <dt>

[<span data-ttu-id="11385-121">MachineMethod</span><span class="sxs-lookup"><span data-stu-id="11385-121">MachineMethod</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-authentication-machinemethod)
</dt> <dd> <dl> <dt>

<span data-ttu-id="11385-122">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="11385-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11385-123">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="11385-123">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="11385-124">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="11385-124">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11385-125">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="11385-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11385-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="11385-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11385-127">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="11385-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="11385-128">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="11385-128">Describes the full path to the parent node.</span></span> <span data-ttu-id="11385-129">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/VPNv2/*ProfileName*/NativeProfile"</span><span class="sxs-lookup"><span data-stu-id="11385-129">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*/NativeProfile"</span></span>

</dd> <dt>

[<span data-ttu-id="11385-130">Usermethod</span><span class="sxs-lookup"><span data-stu-id="11385-130">UserMethod</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-authentication-usermethod)
</dt> <dd> <dl> <dt>

<span data-ttu-id="11385-131">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="11385-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11385-132">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="11385-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="11385-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="11385-133">Requirements</span></span>



| <span data-ttu-id="11385-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="11385-134">Requirement</span></span> | <span data-ttu-id="11385-135">Valor</span><span class="sxs-lookup"><span data-stu-id="11385-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11385-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="11385-136">Minimum supported client</span></span><br/> | <span data-ttu-id="11385-137">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="11385-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="11385-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="11385-138">Minimum supported server</span></span><br/> | <span data-ttu-id="11385-139">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="11385-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="11385-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="11385-140">Namespace</span></span><br/>                | <span data-ttu-id="11385-141">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="11385-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="11385-142">MOF</span><span class="sxs-lookup"><span data-stu-id="11385-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="11385-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="11385-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="11385-144">DLL</span><span class="sxs-lookup"><span data-stu-id="11385-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11385-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11385-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11385-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="11385-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11385-147">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="11385-147">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

