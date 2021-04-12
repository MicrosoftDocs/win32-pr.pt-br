---
title: Classe MDM_VPNv2_APNBinding02
description: Reservado para uso futuro. | Classe MDM_VPNv2_APNBinding02
ms.assetid: ef530e79-b9cc-4bee-8d7b-45227ed55dbe
keywords:
- Classe MDM_VPNv2_APNBinding02
- Classe MDM_VPNv2_APNBinding02, descrita
topic_type:
- apiref
api_name:
- MDM_VPNv2_APNBinding02
- MDM_VPNv2_APNBinding02.InstanceID
- MDM_VPNv2_APNBinding02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d4447d1403903c9633523466504817338db969f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104298129"
---
# <a name="mdm_vpnv2_apnbinding02-class"></a><span data-ttu-id="bc4ee-106">\_ \_ Classe APNBINDING02 do MDM VPNv2</span><span class="sxs-lookup"><span data-stu-id="bc4ee-106">MDM\_VPNv2\_APNBinding02 class</span></span>

<span data-ttu-id="bc4ee-107">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="bc4ee-107">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="bc4ee-108">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="bc4ee-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="bc4ee-109">Reservado para uso futuro</span><span class="sxs-lookup"><span data-stu-id="bc4ee-109">Reserved for Future Use</span></span>

<span data-ttu-id="bc4ee-110">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="bc4ee-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc4ee-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bc4ee-111">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_APNBinding02
{
  string  InstanceID;
  string  ParentID;
  string  ProviderId;
  string  AccessPointName;
  string  UserName;
  string  Password;
  boolean IsCompressionEnabled;
  string  AuthenticationType;
};
```

## <a name="members"></a><span data-ttu-id="bc4ee-112">Membros</span><span class="sxs-lookup"><span data-stu-id="bc4ee-112">Members</span></span>

<span data-ttu-id="bc4ee-113">A **classe \_ \_ APNBinding02 de MDM VPNv2** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="bc4ee-113">The **MDM\_VPNv2\_APNBinding02** class has these types of members:</span></span>

-   [<span data-ttu-id="bc4ee-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="bc4ee-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bc4ee-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="bc4ee-115">Properties</span></span>

<span data-ttu-id="bc4ee-116">A **classe \_ \_ APNBinding02 do MDM VPNv2** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="bc4ee-116">The **MDM\_VPNv2\_APNBinding02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="bc4ee-117">AccessPointName</span><span class="sxs-lookup"><span data-stu-id="bc4ee-117">AccessPointName</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-apnbinding-accesspointname)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc4ee-118">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="bc4ee-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc4ee-119">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="bc4ee-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bc4ee-120">AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="bc4ee-120">AuthenticationType</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-apnbinding-authenticationtype)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc4ee-121">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="bc4ee-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc4ee-122">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="bc4ee-122">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="bc4ee-123">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="bc4ee-123">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc4ee-124">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="bc4ee-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc4ee-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bc4ee-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc4ee-126">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="bc4ee-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="bc4ee-127">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="bc4ee-127">Reserved for future use.</span></span>

</dd> <dt>

[<span data-ttu-id="bc4ee-128">IsCompressionEnabled</span><span class="sxs-lookup"><span data-stu-id="bc4ee-128">IsCompressionEnabled</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-apnbinding-iscompressionenabled)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc4ee-129">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="bc4ee-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bc4ee-130">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="bc4ee-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="bc4ee-131">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="bc4ee-131">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc4ee-132">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="bc4ee-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc4ee-133">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bc4ee-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc4ee-134">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="bc4ee-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="bc4ee-135">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="bc4ee-135">Reserved for future use.</span></span>

</dd> <dt>

[<span data-ttu-id="bc4ee-136">Senha</span><span class="sxs-lookup"><span data-stu-id="bc4ee-136">Password</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-apnbinding-password)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc4ee-137">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="bc4ee-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc4ee-138">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="bc4ee-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bc4ee-139">ProviderId</span><span class="sxs-lookup"><span data-stu-id="bc4ee-139">ProviderId</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-apnbinding-providerid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc4ee-140">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="bc4ee-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc4ee-141">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="bc4ee-141">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bc4ee-142">UserName</span><span class="sxs-lookup"><span data-stu-id="bc4ee-142">UserName</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-apnbinding-username)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc4ee-143">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="bc4ee-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc4ee-144">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="bc4ee-144">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bc4ee-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bc4ee-145">Requirements</span></span>



| <span data-ttu-id="bc4ee-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc4ee-146">Requirement</span></span> | <span data-ttu-id="bc4ee-147">Valor</span><span class="sxs-lookup"><span data-stu-id="bc4ee-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc4ee-148">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bc4ee-148">Minimum supported client</span></span><br/> | <span data-ttu-id="bc4ee-149">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="bc4ee-149">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bc4ee-150">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bc4ee-150">Minimum supported server</span></span><br/> | <span data-ttu-id="bc4ee-151">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="bc4ee-151">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="bc4ee-152">Namespace</span><span class="sxs-lookup"><span data-stu-id="bc4ee-152">Namespace</span></span><br/>                | <span data-ttu-id="bc4ee-153">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="bc4ee-153">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="bc4ee-154">MOF</span><span class="sxs-lookup"><span data-stu-id="bc4ee-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bc4ee-155"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bc4ee-155"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="bc4ee-156">DLL</span><span class="sxs-lookup"><span data-stu-id="bc4ee-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc4ee-157"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc4ee-157"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc4ee-158">Confira também</span><span class="sxs-lookup"><span data-stu-id="bc4ee-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc4ee-159">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="bc4ee-159">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

