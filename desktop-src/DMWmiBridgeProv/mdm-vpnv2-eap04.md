---
title: Classe MDM_VPNv2_Eap04
description: A \_ classe MDM VPNv2 \_ Eap04 contém as informações de configuração XML necessárias quando o perfil nativo especifica a autenticação EAP.
ms.assetid: 87a78743-1ee6-4b86-bfbf-62ba9059535a
keywords:
- Classe MDM_VPNv2_Eap04
- Classe MDM_VPNv2_Eap04, descrita
topic_type:
- apiref
api_name:
- MDM_VPNv2_Eap04
- MDM_VPNv2_Eap04.InstanceID
- MDM_VPNv2_Eap04.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9270bf1cae37c345fe81be674e9d9afc2c533bc9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645065"
---
# <a name="mdm_vpnv2_eap04-class"></a><span data-ttu-id="9df42-105">\_ \_ Classe EAP04 do MDM VPNv2</span><span class="sxs-lookup"><span data-stu-id="9df42-105">MDM\_VPNv2\_Eap04 class</span></span>

<span data-ttu-id="9df42-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="9df42-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="9df42-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="9df42-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="9df42-108">A classe **MDM \_ VPNv2 \_ Eap04** contém as informações de configuração XML necessárias quando o perfil nativo especifica a autenticação EAP.</span><span class="sxs-lookup"><span data-stu-id="9df42-108">The **MDM\_VPNv2\_Eap04** class contains the required configuration XML information when the native profile specifies EAP authentication.</span></span>

<span data-ttu-id="9df42-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="9df42-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9df42-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9df42-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_Eap04
{
  string InstanceID;
  string ParentID;
  string Configuration;
  sint32 Type;
};
```

## <a name="members"></a><span data-ttu-id="9df42-111">Membros</span><span class="sxs-lookup"><span data-stu-id="9df42-111">Members</span></span>

<span data-ttu-id="9df42-112">A **classe \_ \_ Eap04 de MDM VPNv2** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="9df42-112">The **MDM\_VPNv2\_Eap04** class has these types of members:</span></span>

-   [<span data-ttu-id="9df42-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9df42-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9df42-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9df42-114">Properties</span></span>

<span data-ttu-id="9df42-115">A **classe \_ \_ Eap04 do MDM VPNv2** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="9df42-115">The **MDM\_VPNv2\_Eap04** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="9df42-116">Configuration</span><span class="sxs-lookup"><span data-stu-id="9df42-116">Configuration</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-authentication-eap-configuration)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9df42-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9df42-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9df42-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9df42-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9df42-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="9df42-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9df42-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9df42-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9df42-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9df42-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9df42-122">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9df42-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9df42-123">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="9df42-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="9df42-124">Para essa classe, a cadeia de caracteres é "EAP"</span><span class="sxs-lookup"><span data-stu-id="9df42-124">For this class, the string is "Eap"</span></span>

</dd> <dt>

<span data-ttu-id="9df42-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="9df42-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9df42-126">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9df42-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9df42-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9df42-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9df42-128">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9df42-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9df42-129">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="9df42-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="9df42-130">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/VPNv2/*ProfileName*/NativeProfile/Authentication"</span><span class="sxs-lookup"><span data-stu-id="9df42-130">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*/NativeProfile/Authentication"</span></span>

</dd> <dt>

[<span data-ttu-id="9df42-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="9df42-131">Type</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-apptriggerlist-apptriggerrowid-app-type)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9df42-132">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9df42-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9df42-133">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9df42-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9df42-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9df42-134">Requirements</span></span>



| <span data-ttu-id="9df42-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="9df42-135">Requirement</span></span> | <span data-ttu-id="9df42-136">Valor</span><span class="sxs-lookup"><span data-stu-id="9df42-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9df42-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9df42-137">Minimum supported client</span></span><br/> | <span data-ttu-id="9df42-138">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="9df42-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9df42-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9df42-139">Minimum supported server</span></span><br/> | <span data-ttu-id="9df42-140">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="9df42-140">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="9df42-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="9df42-141">Namespace</span></span><br/>                | <span data-ttu-id="9df42-142">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="9df42-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="9df42-143">MOF</span><span class="sxs-lookup"><span data-stu-id="9df42-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9df42-144"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9df42-144"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="9df42-145">DLL</span><span class="sxs-lookup"><span data-stu-id="9df42-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9df42-146"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9df42-146"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9df42-147">Consulte também</span><span class="sxs-lookup"><span data-stu-id="9df42-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9df42-148">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="9df42-148">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

