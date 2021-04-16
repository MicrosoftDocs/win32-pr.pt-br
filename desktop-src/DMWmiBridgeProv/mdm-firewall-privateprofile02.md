---
title: Classe MDM_Firewall_PrivateProfile02
description: A \_ classe PrivateProfile02 do MDM firewall \_ é usada para definir as configurações do Windows Defender firewall.
ms.assetid: 9d25c181-e9a8-4f63-b276-b22676842667
keywords:
- Classe MDM_Firewall_PrivateProfile02
- Classe MDM_Firewall_PrivateProfile02, descrita
topic_type:
- apiref
api_name:
- MDM_Firewall_PrivateProfile02
- MDM_Firewall_PrivateProfile02.InstanceID
- MDM_Firewall_PrivateProfile02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57812ef7c8550937b009e4ff4855321983391585
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105751298"
---
# <a name="mdm_firewall_privateprofile02-class"></a><span data-ttu-id="b1e18-105">\_ \_ Classe PRIVATEPROFILE02 do MDM firewall</span><span class="sxs-lookup"><span data-stu-id="b1e18-105">MDM\_Firewall\_PrivateProfile02 class</span></span>

<span data-ttu-id="b1e18-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="b1e18-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="b1e18-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="b1e18-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="b1e18-108">A \_ classe PrivateProfile02 do MDM firewall \_ é usada para definir as configurações do Windows Defender firewall.</span><span class="sxs-lookup"><span data-stu-id="b1e18-108">The MDM\_Firewall\_PrivateProfile02 class is used to configure the Windows Defender Firewall settings.</span></span>

<span data-ttu-id="b1e18-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="b1e18-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1e18-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b1e18-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Firewall_PrivateProfile02
{
  string InstanceID;
  string ParentID;
  sint32 EnableFirewall;
  sint32 DisableStealthMode;
  sint32 Shielded;
  sint32 DisableUnicastResponsesToMulticastBroadcast;
  sint32 DisableInboundNotifications;
  sint32 AuthAppsAllowUserPrefMerge;
  sint32 GlobalPortsAllowUserPrefMerge;
  sint32 AllowLocalPolicyMerge;
  sint32 AllowLocalIpsecPolicyMerge;
  sint32 DefaultOutboundAction;
  sint32 DefaultInboundAction;
  sint32 DisableStealthModeIpsecSecuredPacketExemption;
};
```

## <a name="members"></a><span data-ttu-id="b1e18-111">Membros</span><span class="sxs-lookup"><span data-stu-id="b1e18-111">Members</span></span>

<span data-ttu-id="b1e18-112">A **classe \_ \_ PrivateProfile02 do MDM firewall** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="b1e18-112">The **MDM\_Firewall\_PrivateProfile02** class has these types of members:</span></span>

-   [<span data-ttu-id="b1e18-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b1e18-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b1e18-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b1e18-114">Properties</span></span>

<span data-ttu-id="b1e18-115">A **classe \_ \_ PrivateProfile02 do MDM firewall** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="b1e18-115">The **MDM\_Firewall\_PrivateProfile02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="b1e18-116">AllowLocalIpsecPolicyMerge</span><span class="sxs-lookup"><span data-stu-id="b1e18-116">AllowLocalIpsecPolicyMerge</span></span>](/windows/client-management/mdm/firewall-csp#allowlocalipsecpolicymerge)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1e18-117">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b1e18-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b1e18-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="b1e18-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b1e18-119">AllowLocalPolicyMerge</span><span class="sxs-lookup"><span data-stu-id="b1e18-119">AllowLocalPolicyMerge</span></span>](/windows/client-management/mdm/firewall-csp#allowlocalpolicymerge)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1e18-120">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b1e18-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b1e18-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="b1e18-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b1e18-122">AuthAppsAllowUserPrefMerge</span><span class="sxs-lookup"><span data-stu-id="b1e18-122">AuthAppsAllowUserPrefMerge</span></span>](/windows/client-management/mdm/firewall-csp#authappsallowuserprefmerge)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1e18-123">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b1e18-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b1e18-124">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="b1e18-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b1e18-125">DefaultInboundAction</span><span class="sxs-lookup"><span data-stu-id="b1e18-125">DefaultInboundAction</span></span>](/windows/client-management/mdm/firewall-csp#defaultinboundaction)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1e18-126">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b1e18-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b1e18-127">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="b1e18-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b1e18-128">Outboundaction</span><span class="sxs-lookup"><span data-stu-id="b1e18-128">DefaultOutboundAction</span></span>](/windows/client-management/mdm/firewall-csp#defaultoutboundaction)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1e18-129">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b1e18-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b1e18-130">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="b1e18-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b1e18-131">DisableInboundNotifications</span><span class="sxs-lookup"><span data-stu-id="b1e18-131">DisableInboundNotifications</span></span>](/windows/client-management/mdm/firewall-csp#disableinboundnotifications)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1e18-132">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b1e18-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b1e18-133">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="b1e18-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b1e18-134">DisableStealthMode</span><span class="sxs-lookup"><span data-stu-id="b1e18-134">DisableStealthMode</span></span>](/windows/client-management/mdm/firewall-csp#disablestealthmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1e18-135">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b1e18-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b1e18-136">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="b1e18-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b1e18-137">DisableStealthModeIpsecSecuredPacketExemption</span><span class="sxs-lookup"><span data-stu-id="b1e18-137">DisableStealthModeIpsecSecuredPacketExemption</span></span>](/windows/client-management/mdm/firewall-csp#disablestealthmodeipsecsecuredpacketexemption)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1e18-138">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b1e18-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b1e18-139">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="b1e18-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b1e18-140">DisableUnicastResponsesToMulticastBroadcast</span><span class="sxs-lookup"><span data-stu-id="b1e18-140">DisableUnicastResponsesToMulticastBroadcast</span></span>](/windows/client-management/mdm/firewall-csp#disableunicastresponsestomulticastbroadcast)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1e18-141">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b1e18-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b1e18-142">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="b1e18-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b1e18-143">EnableFirewall</span><span class="sxs-lookup"><span data-stu-id="b1e18-143">EnableFirewall</span></span>](/windows/client-management/mdm/firewall-csp#enablefirewall)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1e18-144">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b1e18-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b1e18-145">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="b1e18-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b1e18-146">GlobalPortsAllowUserPrefMerge</span><span class="sxs-lookup"><span data-stu-id="b1e18-146">GlobalPortsAllowUserPrefMerge</span></span>](/windows/client-management/mdm/firewall-csp#globalportsallowuserprefmerge)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1e18-147">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b1e18-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b1e18-148">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="b1e18-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b1e18-149">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b1e18-149">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1e18-150">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b1e18-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1e18-151">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b1e18-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1e18-152">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b1e18-152">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b1e18-153">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="b1e18-153">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1e18-154">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b1e18-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1e18-155">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b1e18-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1e18-156">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b1e18-156">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b1e18-157">Blindado</span><span class="sxs-lookup"><span data-stu-id="b1e18-157">Shielded</span></span>](/windows/client-management/mdm/firewall-csp#shielded)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1e18-158">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b1e18-158">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b1e18-159">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="b1e18-159">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b1e18-160">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b1e18-160">Requirements</span></span>



| <span data-ttu-id="b1e18-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1e18-161">Requirement</span></span> | <span data-ttu-id="b1e18-162">Valor</span><span class="sxs-lookup"><span data-stu-id="b1e18-162">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1e18-163">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b1e18-163">Minimum supported client</span></span><br/> | <span data-ttu-id="b1e18-164">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="b1e18-164">Windows 10 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b1e18-165">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b1e18-165">Minimum supported server</span></span><br/> | <span data-ttu-id="b1e18-166">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="b1e18-166">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="b1e18-167">Namespace</span><span class="sxs-lookup"><span data-stu-id="b1e18-167">Namespace</span></span><br/>                | <span data-ttu-id="b1e18-168">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="b1e18-168">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                              |
| <span data-ttu-id="b1e18-169">MOF</span><span class="sxs-lookup"><span data-stu-id="b1e18-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b1e18-170"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b1e18-170"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl> |
| <span data-ttu-id="b1e18-171">DLL</span><span class="sxs-lookup"><span data-stu-id="b1e18-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b1e18-172"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b1e18-172"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl>  |



 

