---
title: Classe MDM_VPNv2_Certificate04
description: Reservado para uso futuro.
ms.assetid: 0fa831e0-918a-472f-88bf-7e40c4081417
keywords:
- Classe MDM_VPNv2_Certificate04
- Classe MDM_VPNv2_Certificate04, descrita
topic_type:
- apiref
api_name:
- MDM_VPNv2_Certificate04
- MDM_VPNv2_Certificate04.InstanceID
- MDM_VPNv2_Certificate04.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea88bd26e8dc9916e7e2db97b980065d7a8733ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918463"
---
# <a name="mdm_vpnv2_certificate04-class"></a><span data-ttu-id="61828-105">\_ \_ Classe CERTIFICATE04 do MDM VPNv2</span><span class="sxs-lookup"><span data-stu-id="61828-105">MDM\_VPNv2\_Certificate04 class</span></span>

<span data-ttu-id="61828-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="61828-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="61828-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="61828-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="61828-108">Reservado para uso futuro</span><span class="sxs-lookup"><span data-stu-id="61828-108">Reserved for future Use</span></span>

<span data-ttu-id="61828-109">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="61828-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="61828-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="61828-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_Certificate04
{
  string InstanceID;
  string ParentID;
  string Issuer;
  string Eku;
};
```

## <a name="members"></a><span data-ttu-id="61828-111">Membros</span><span class="sxs-lookup"><span data-stu-id="61828-111">Members</span></span>

<span data-ttu-id="61828-112">A **classe \_ \_ Certificate04 de MDM VPNv2** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="61828-112">The **MDM\_VPNv2\_Certificate04** class has these types of members:</span></span>

-   [<span data-ttu-id="61828-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="61828-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="61828-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="61828-114">Properties</span></span>

<span data-ttu-id="61828-115">A **classe \_ \_ Certificate04 do MDM VPNv2** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="61828-115">The **MDM\_VPNv2\_Certificate04** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="61828-116">EKU</span><span class="sxs-lookup"><span data-stu-id="61828-116">Eku</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-authentication-certificate-eku)
</dt> <dd> <dl> <dt>

<span data-ttu-id="61828-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="61828-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="61828-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="61828-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="61828-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="61828-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61828-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="61828-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="61828-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="61828-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="61828-122">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="61828-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="61828-123">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="61828-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="61828-124">Para essa classe, a cadeia de caracteres é "EAP"</span><span class="sxs-lookup"><span data-stu-id="61828-124">For this class, the string is "Eap"</span></span>

</dd> <dt>

[<span data-ttu-id="61828-125">Emissor</span><span class="sxs-lookup"><span data-stu-id="61828-125">Issuer</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-authentication-certificate-issuer)
</dt> <dd> <dl> <dt>

<span data-ttu-id="61828-126">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="61828-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="61828-127">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="61828-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="61828-128">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="61828-128">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61828-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="61828-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="61828-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="61828-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="61828-131">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="61828-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="61828-132">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="61828-132">Describes the full path to the parent node.</span></span> <span data-ttu-id="61828-133">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/VPNv2/*ProfileName*/NativeProfile/Authentication"</span><span class="sxs-lookup"><span data-stu-id="61828-133">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*/NativeProfile/Authentication"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="61828-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61828-134">Requirements</span></span>



| <span data-ttu-id="61828-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="61828-135">Requirement</span></span> | <span data-ttu-id="61828-136">Valor</span><span class="sxs-lookup"><span data-stu-id="61828-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61828-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="61828-137">Minimum supported client</span></span><br/> | <span data-ttu-id="61828-138">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="61828-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="61828-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="61828-139">Minimum supported server</span></span><br/> | <span data-ttu-id="61828-140">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="61828-140">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="61828-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="61828-141">Namespace</span></span><br/>                | <span data-ttu-id="61828-142">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="61828-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="61828-143">MOF</span><span class="sxs-lookup"><span data-stu-id="61828-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="61828-144"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="61828-144"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="61828-145">DLL</span><span class="sxs-lookup"><span data-stu-id="61828-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="61828-146"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="61828-146"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61828-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="61828-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61828-148">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="61828-148">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

