---
description: Representa as configurações de ACL de porta estendida.
ms.assetid: 357dd891-6692-4ffc-b8a8-4ece40d4af28
title: Classe Msvm_EthernetSwitchPortExtendedAclSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortExtendedAclSettingData
- Msvm_EthernetSwitchPortExtendedAclSettingData.Name
- Msvm_EthernetSwitchPortExtendedAclSettingData.Direction
- Msvm_EthernetSwitchPortExtendedAclSettingData.Action
- Msvm_EthernetSwitchPortExtendedAclSettingData.LocalIPAddress
- Msvm_EthernetSwitchPortExtendedAclSettingData.RemoteIPAddress
- Msvm_EthernetSwitchPortExtendedAclSettingData.LocalPort
- Msvm_EthernetSwitchPortExtendedAclSettingData.RemotePort
- Msvm_EthernetSwitchPortExtendedAclSettingData.Protocol
- Msvm_EthernetSwitchPortExtendedAclSettingData.Weight
- Msvm_EthernetSwitchPortExtendedAclSettingData.Stateful
- Msvm_EthernetSwitchPortExtendedAclSettingData.IdleSessionTimeout
- Msvm_EthernetSwitchPortExtendedAclSettingData.IsolationID
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 25ae81e4f00e87e41170ac5713ced0d9b523c844
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756928"
---
# <a name="msvm_ethernetswitchportextendedaclsettingdata-class"></a><span data-ttu-id="5bcfe-103">\_Classe Msvm EthernetSwitchPortExtendedAclSettingData</span><span class="sxs-lookup"><span data-stu-id="5bcfe-103">Msvm\_EthernetSwitchPortExtendedAclSettingData class</span></span>

<span data-ttu-id="5bcfe-104">Representa as configurações de ACL de porta estendida.</span><span class="sxs-lookup"><span data-stu-id="5bcfe-104">Represents the extended port ACL settings.</span></span>

<span data-ttu-id="5bcfe-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="5bcfe-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5bcfe-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5bcfe-106">Syntax</span></span>

``` syntax
[Dynamic, UUID("CD168FF0-A16D-4514-B7B5-8BBBA791A928"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), Provider("VmmsWmiInstanceAndMethodProvider"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Extended ACL Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortExtendedAclSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string  Name = "";
  uint8   Direction = 0;
  uint8   Action = 0;
  string  LocalIPAddress = "ANY";
  string  RemoteIPAddress = "ANY";
  string  LocalPort = "ANY";
  string  RemotePort = "ANY";
  string  Protocol = "ANY";
  Uint16  Weight = 0;
  Boolean Stateful = FALSE;
  Uint16  IdleSessionTimeout = 255;
  Uint32  IsolationID = 0;
};
```

## <a name="members"></a><span data-ttu-id="5bcfe-107">Membros</span><span class="sxs-lookup"><span data-stu-id="5bcfe-107">Members</span></span>

<span data-ttu-id="5bcfe-108">A classe **Msvm \_ EthernetSwitchPortExtendedAclSettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="5bcfe-108">The **Msvm\_EthernetSwitchPortExtendedAclSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="5bcfe-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5bcfe-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5bcfe-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5bcfe-110">Properties</span></span>

<span data-ttu-id="5bcfe-111">A classe **Msvm \_ EthernetSwitchPortExtendedAclSettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="5bcfe-111">The **Msvm\_EthernetSwitchPortExtendedAclSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5bcfe-112">**Ação**</span><span class="sxs-lookup"><span data-stu-id="5bcfe-112">**Action**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5bcfe-113">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="5bcfe-113">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="5bcfe-114">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5bcfe-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5bcfe-115">Qualificadores: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="5bcfe-115">Qualifiers: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="5bcfe-116">A ação da ACL estendida.</span><span class="sxs-lookup"><span data-stu-id="5bcfe-116">The action of the extended ACL.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5bcfe-117">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="5bcfe-117">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>

<span data-ttu-id="5bcfe-118">**Permitir** (1)</span><span class="sxs-lookup"><span data-stu-id="5bcfe-118">**Allow** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Deny"></span><span id="deny"></span><span id="DENY"></span>

<span data-ttu-id="5bcfe-119">**Negar** (2)</span><span class="sxs-lookup"><span data-stu-id="5bcfe-119">**Deny** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5bcfe-120">**Direção**</span><span class="sxs-lookup"><span data-stu-id="5bcfe-120">**Direction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5bcfe-121">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="5bcfe-121">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="5bcfe-122">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5bcfe-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5bcfe-123">Qualificadores: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="5bcfe-123">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="5bcfe-124">Indica se a ACL estendida se aplica à direção de entrada ou saída.</span><span class="sxs-lookup"><span data-stu-id="5bcfe-124">Indicates if the extended ACL applies to incoming or outgoing direction.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5bcfe-125">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="5bcfe-125">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Incoming"></span><span id="incoming"></span><span id="INCOMING"></span>

<span data-ttu-id="5bcfe-126">**Entrada** (1)</span><span class="sxs-lookup"><span data-stu-id="5bcfe-126">**Incoming** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Outgoing"></span><span id="outgoing"></span><span id="OUTGOING"></span>

<span data-ttu-id="5bcfe-127">**Saída** (2)</span><span class="sxs-lookup"><span data-stu-id="5bcfe-127">**Outgoing** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5bcfe-128">**IdleSessionTimeout**</span><span class="sxs-lookup"><span data-stu-id="5bcfe-128">**IdleSessionTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5bcfe-129">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5bcfe-129">Data type: **Uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5bcfe-130">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5bcfe-130">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5bcfe-131">Qualificadores: **WmiDataId** (11), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="5bcfe-131">Qualifiers: **WmiDataId** (11), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="5bcfe-132">Valor de tempo limite de sessão ociosa (em segundos) para ACL com estado.</span><span class="sxs-lookup"><span data-stu-id="5bcfe-132">Idle session timeout value (in seconds) for stateful ACL.</span></span>

</dd> <dt>

<span data-ttu-id="5bcfe-133">**Isolamentoid**</span><span class="sxs-lookup"><span data-stu-id="5bcfe-133">**IsolationID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5bcfe-134">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5bcfe-134">Data type: **Uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5bcfe-135">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5bcfe-135">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5bcfe-136">Qualificadores: **InterfaceVersion** (1), **InterfaceRevision** (0), **WmiDataId** (12)</span><span class="sxs-lookup"><span data-stu-id="5bcfe-136">Qualifiers: **InterfaceVersion** (1), **InterfaceRevision** (0), **WmiDataId** (12)</span></span>
</dt> </dl>

<span data-ttu-id="5bcfe-137">ID de isolamento para a qual a ACL estendida deve ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="5bcfe-137">Isolation ID for which the extended ACL should be applied.</span></span>

</dd> <dt>

<span data-ttu-id="5bcfe-138">**LocalIPAddress**</span><span class="sxs-lookup"><span data-stu-id="5bcfe-138">**LocalIPAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5bcfe-139">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5bcfe-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5bcfe-140">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5bcfe-140">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5bcfe-141">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (40), **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="5bcfe-141">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (40), **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="5bcfe-142">O endereço IP local.</span><span class="sxs-lookup"><span data-stu-id="5bcfe-142">The local IP address.</span></span>

</dd> <dt>

<span data-ttu-id="5bcfe-143">**LocalPort**</span><span class="sxs-lookup"><span data-stu-id="5bcfe-143">**LocalPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5bcfe-144">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5bcfe-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5bcfe-145">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5bcfe-145">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5bcfe-146">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (21), **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="5bcfe-146">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (21), **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="5bcfe-147">O intervalo de portas local.</span><span class="sxs-lookup"><span data-stu-id="5bcfe-147">The local port range.</span></span>

</dd> <dt>

<span data-ttu-id="5bcfe-148">**Nome**</span><span class="sxs-lookup"><span data-stu-id="5bcfe-148">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5bcfe-149">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5bcfe-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5bcfe-150">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5bcfe-150">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5bcfe-151">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="5bcfe-151">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="5bcfe-152">O nome amigável da ACL estendida.</span><span class="sxs-lookup"><span data-stu-id="5bcfe-152">The friendly name of the Extended ACL.</span></span>

</dd> <dt>

<span data-ttu-id="5bcfe-153">**Protocolo**</span><span class="sxs-lookup"><span data-stu-id="5bcfe-153">**Protocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5bcfe-154">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5bcfe-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5bcfe-155">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5bcfe-155">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5bcfe-156">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (15), **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="5bcfe-156">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (15), **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="5bcfe-157">A cadeia de caracteres do protocolo.</span><span class="sxs-lookup"><span data-stu-id="5bcfe-157">The protocol string.</span></span>

</dd> <dt>

<span data-ttu-id="5bcfe-158">**RemoteIPAddress**</span><span class="sxs-lookup"><span data-stu-id="5bcfe-158">**RemoteIPAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5bcfe-159">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5bcfe-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5bcfe-160">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5bcfe-160">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5bcfe-161">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (40), **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="5bcfe-161">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (40), **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="5bcfe-162">O endereço IP remoto.</span><span class="sxs-lookup"><span data-stu-id="5bcfe-162">The remote IP address.</span></span>

</dd> <dt>

<span data-ttu-id="5bcfe-163">**RemotePort**</span><span class="sxs-lookup"><span data-stu-id="5bcfe-163">**RemotePort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5bcfe-164">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5bcfe-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5bcfe-165">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5bcfe-165">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5bcfe-166">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (21), **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="5bcfe-166">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (21), **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="5bcfe-167">O intervalo de portas remotas.</span><span class="sxs-lookup"><span data-stu-id="5bcfe-167">The remote port range.</span></span>

</dd> <dt>

<span data-ttu-id="5bcfe-168">**Dinâmico**</span><span class="sxs-lookup"><span data-stu-id="5bcfe-168">**Stateful**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5bcfe-169">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="5bcfe-169">Data type: **Boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5bcfe-170">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5bcfe-170">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5bcfe-171">Qualificadores: **WmiDataId** (10), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="5bcfe-171">Qualifiers: **WmiDataId** (10), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="5bcfe-172">Indica se a ACL estendida tem estado ou sem estado.</span><span class="sxs-lookup"><span data-stu-id="5bcfe-172">Indicates if the extended ACL is stateful or stateless.</span></span>

</dd> <dt>

<span data-ttu-id="5bcfe-173">**Weight**</span><span class="sxs-lookup"><span data-stu-id="5bcfe-173">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5bcfe-174">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5bcfe-174">Data type: **Uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5bcfe-175">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5bcfe-175">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5bcfe-176">Qualificadores: **WmiDataId** (9), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="5bcfe-176">Qualifiers: **WmiDataId** (9), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="5bcfe-177">O peso aplicado à ACL estendida.</span><span class="sxs-lookup"><span data-stu-id="5bcfe-177">The weight applied to the extended ACL.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5bcfe-178">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5bcfe-178">Requirements</span></span>



| <span data-ttu-id="5bcfe-179">Requisito</span><span class="sxs-lookup"><span data-stu-id="5bcfe-179">Requirement</span></span> | <span data-ttu-id="5bcfe-180">Valor</span><span class="sxs-lookup"><span data-stu-id="5bcfe-180">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5bcfe-181">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5bcfe-181">Minimum supported client</span></span><br/> | <span data-ttu-id="5bcfe-182">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="5bcfe-182">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="5bcfe-183">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5bcfe-183">Minimum supported server</span></span><br/> | <span data-ttu-id="5bcfe-184">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="5bcfe-184">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="5bcfe-185">Namespace</span><span class="sxs-lookup"><span data-stu-id="5bcfe-185">Namespace</span></span><br/>                | <span data-ttu-id="5bcfe-186">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="5bcfe-186">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="5bcfe-187">MOF</span><span class="sxs-lookup"><span data-stu-id="5bcfe-187">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5bcfe-188"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5bcfe-188"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5bcfe-189">DLL</span><span class="sxs-lookup"><span data-stu-id="5bcfe-189">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5bcfe-190"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5bcfe-190"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5bcfe-191">Confira também</span><span class="sxs-lookup"><span data-stu-id="5bcfe-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bcfe-192">**Msvm \_ EthernetSwitchPortFeatureSettingData**</span><span class="sxs-lookup"><span data-stu-id="5bcfe-192">**Msvm\_EthernetSwitchPortFeatureSettingData**</span></span>](msvm-ethernetswitchportfeaturesettingdata.md)
</dt> </dl>

 

