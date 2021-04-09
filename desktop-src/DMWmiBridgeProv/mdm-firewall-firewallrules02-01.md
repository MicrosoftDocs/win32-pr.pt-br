---
title: Classe MDM_Firewall_FirewallRules02_01
description: A \_ classe FirewallRules02 01 do firewall do MDM \_ \_ é usada para definir as configurações do Windows Defender firewall.
ms.assetid: b09cbd98-152e-486c-acb5-4e1d83e5f8e2
keywords:
- Classe MDM_Firewall_FirewallRules02_01
- Classe MDM_Firewall_FirewallRules02_01, descrita
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MDM_Firewall_FirewallRules02_01
- MDM_Firewall_FirewallRules02_01.InstanceID
- MDM_Firewall_FirewallRules02_01.ParentID
- MDM_Firewall_FirewallRules02_01.IcmpTypesAndCodes
- MDM_Firewall_FirewallRules02_01.FriendlyName
api_type:
- DllExport
api_location:
- DMWmiBridgeProv.dll
ms.openlocfilehash: 494be18ece91e7a1776780542f988b80cb822e42
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085390"
---
# <a name="mdm_firewall_firewallrules02_01-class"></a><span data-ttu-id="42b09-105">\_ \_ Classe FirewallRules02 01 do firewall \_ do MDM</span><span class="sxs-lookup"><span data-stu-id="42b09-105">MDM\_Firewall\_FirewallRules02\_01 class</span></span>

<span data-ttu-id="42b09-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="42b09-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="42b09-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="42b09-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="42b09-108">A \_ classe FirewallRules02 01 do firewall do MDM \_ \_ é usada para definir as configurações do Windows Defender firewall.</span><span class="sxs-lookup"><span data-stu-id="42b09-108">The MDM\_Firewall\_FirewallRules02\_01 class is used to configure the Windows Defender Firewall settings.</span></span>

<span data-ttu-id="42b09-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="42b09-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="42b09-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="42b09-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Firewall_FirewallRules02_01
{
  string  InstanceID;
  string  ParentID;
  sint32  Protocol;
  string  LocalPortRanges;
  string  RemotePortRanges;
  string  LocalAddressRanges;
  string  RemoteAddressRanges;
  string  Description;
  boolean Enabled;
  sint32  Profiles;
  string  Direction;
  string  InterfaceTypes;
  string  IcmpTypesAndCodes;
  boolean EdgeTraversal;
  string  LocalUserAuthorizedList;
  string  Status;
  string  FriendlyName;
  string  Name;
};
```

## <a name="members"></a><span data-ttu-id="42b09-111">Membros</span><span class="sxs-lookup"><span data-stu-id="42b09-111">Members</span></span>

<span data-ttu-id="42b09-112">A classe do **MDM \_ Firewall \_ FirewallRules02 \_ 01** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="42b09-112">The **MDM\_Firewall\_FirewallRules02\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="42b09-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="42b09-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="42b09-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="42b09-114">Properties</span></span>

<span data-ttu-id="42b09-115">A **classe \_ \_ FirewallRules02 \_ 01 do MDM firewall** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="42b09-115">The **MDM\_Firewall\_FirewallRules02\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="42b09-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="42b09-116">Description</span></span>](/windows/client-management/mdm/firewall-csp#description)
</dt> <dd> <dl> <dt>

<span data-ttu-id="42b09-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="42b09-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42b09-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="42b09-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="42b09-119">Direção</span><span class="sxs-lookup"><span data-stu-id="42b09-119">Direction</span></span>](/windows/client-management/mdm/firewall-csp#direction)
</dt> <dd> <dl> <dt>

<span data-ttu-id="42b09-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="42b09-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42b09-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="42b09-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="42b09-122">EdgeTraversal</span><span class="sxs-lookup"><span data-stu-id="42b09-122">EdgeTraversal</span></span>](/windows/client-management/mdm/firewall-csp#edgetraversal)
</dt> <dd> <dl> <dt>

<span data-ttu-id="42b09-123">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="42b09-123">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="42b09-124">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="42b09-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="42b09-125">Enabled</span><span class="sxs-lookup"><span data-stu-id="42b09-125">Enabled</span></span>](/windows/client-management/mdm/firewall-csp#enabled)
</dt> <dd> <dl> <dt>

<span data-ttu-id="42b09-126">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="42b09-126">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="42b09-127">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="42b09-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="42b09-128">**FriendlyName**</span><span class="sxs-lookup"><span data-stu-id="42b09-128">**FriendlyName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42b09-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="42b09-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42b09-130">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="42b09-130">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="42b09-131">TBD</span><span class="sxs-lookup"><span data-stu-id="42b09-131">TBD</span></span>

</dd> <dt>

<span data-ttu-id="42b09-132">**IcmpTypesAndCodes**</span><span class="sxs-lookup"><span data-stu-id="42b09-132">**IcmpTypesAndCodes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42b09-133">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="42b09-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42b09-134">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="42b09-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="42b09-135">TBD</span><span class="sxs-lookup"><span data-stu-id="42b09-135">TBD</span></span>

</dd> <dt>

<span data-ttu-id="42b09-136">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="42b09-136">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42b09-137">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="42b09-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42b09-138">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="42b09-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42b09-139">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="42b09-139">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="42b09-140">InterfaceType</span><span class="sxs-lookup"><span data-stu-id="42b09-140">InterfaceTypes</span></span>](/windows/client-management/mdm/firewall-csp#interfacetypes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="42b09-141">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="42b09-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42b09-142">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="42b09-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="42b09-143">LocalAddressRanges</span><span class="sxs-lookup"><span data-stu-id="42b09-143">LocalAddressRanges</span></span>](/windows/client-management/mdm/firewall-csp#localaddressranges)
</dt> <dd> <dl> <dt>

<span data-ttu-id="42b09-144">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="42b09-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42b09-145">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="42b09-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="42b09-146">LocalPortRanges</span><span class="sxs-lookup"><span data-stu-id="42b09-146">LocalPortRanges</span></span>](/windows/client-management/mdm/firewall-csp#localportranges)
</dt> <dd> <dl> <dt>

<span data-ttu-id="42b09-147">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="42b09-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42b09-148">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="42b09-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="42b09-149">LocalUserAuthorizedList</span><span class="sxs-lookup"><span data-stu-id="42b09-149">LocalUserAuthorizedList</span></span>](/windows/client-management/mdm/firewall-csp#localuserauthorizedlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="42b09-150">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="42b09-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42b09-151">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="42b09-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="42b09-152">Nome</span><span class="sxs-lookup"><span data-stu-id="42b09-152">Name</span></span>](/windows/client-management/mdm/firewall-csp#name)
</dt> <dd> <dl> <dt>

<span data-ttu-id="42b09-153">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="42b09-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42b09-154">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="42b09-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="42b09-155">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="42b09-155">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42b09-156">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="42b09-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42b09-157">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="42b09-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42b09-158">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="42b09-158">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="42b09-159">Perfis</span><span class="sxs-lookup"><span data-stu-id="42b09-159">Profiles</span></span>](/windows/client-management/mdm/firewall-csp#profiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="42b09-160">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="42b09-160">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="42b09-161">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="42b09-161">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="42b09-162">Protocolo</span><span class="sxs-lookup"><span data-stu-id="42b09-162">Protocol</span></span>](/windows/client-management/mdm/firewall-csp#protocol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="42b09-163">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="42b09-163">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="42b09-164">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="42b09-164">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="42b09-165">RemoteAddressRanges</span><span class="sxs-lookup"><span data-stu-id="42b09-165">RemoteAddressRanges</span></span>](/windows/client-management/mdm/firewall-csp#remoteaddressranges)
</dt> <dd> <dl> <dt>

<span data-ttu-id="42b09-166">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="42b09-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42b09-167">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="42b09-167">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="42b09-168">RemotePortRanges</span><span class="sxs-lookup"><span data-stu-id="42b09-168">RemotePortRanges</span></span>](/windows/client-management/mdm/firewall-csp#remoteportranges)
</dt> <dd> <dl> <dt>

<span data-ttu-id="42b09-169">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="42b09-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42b09-170">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="42b09-170">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="42b09-171">Status</span><span class="sxs-lookup"><span data-stu-id="42b09-171">Status</span></span>](/windows/client-management/mdm/firewall-csp#status)
</dt> <dd> <dl> <dt>

<span data-ttu-id="42b09-172">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="42b09-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42b09-173">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="42b09-173">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="42b09-174">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42b09-174">Requirements</span></span>



| <span data-ttu-id="42b09-175">Requisito</span><span class="sxs-lookup"><span data-stu-id="42b09-175">Requirement</span></span> | <span data-ttu-id="42b09-176">Valor</span><span class="sxs-lookup"><span data-stu-id="42b09-176">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42b09-177">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="42b09-177">Minimum supported client</span></span><br/> | <span data-ttu-id="42b09-178">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="42b09-178">Windows 10 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="42b09-179">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="42b09-179">Minimum supported server</span></span><br/> | <span data-ttu-id="42b09-180">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="42b09-180">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="42b09-181">Namespace</span><span class="sxs-lookup"><span data-stu-id="42b09-181">Namespace</span></span><br/>                | <span data-ttu-id="42b09-182">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="42b09-182">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                              |
| <span data-ttu-id="42b09-183">MOF</span><span class="sxs-lookup"><span data-stu-id="42b09-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="42b09-184"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="42b09-184"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl> |
| <span data-ttu-id="42b09-185">DLL</span><span class="sxs-lookup"><span data-stu-id="42b09-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="42b09-186"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="42b09-186"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl>  |



 

