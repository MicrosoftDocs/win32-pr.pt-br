---
description: Representa as configurações de QOS VFP.
ms.assetid: e58a7a8d-0301-43ea-9338-18bc8c458e2d
title: Classe Msvm_EthernetSwitchPortMigrationQosSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortMigrationQosSettingData
- Msvm_EthernetSwitchPortMigrationQosSettingData.QueueId
- Msvm_EthernetSwitchPortMigrationQosSettingData.Switch_ReservationMode
- Msvm_EthernetSwitchPortMigrationQosSettingData.Switch_LinkSpeedPercentage
- Msvm_EthernetSwitchPortMigrationQosSettingData.Switch_DefaultReservation
- Msvm_EthernetSwitchPortMigrationQosSettingData.Switch_EnableHardwareLimits
- Msvm_EthernetSwitchPortMigrationQosSettingData.Switch_EnableHardwareReservations
- Msvm_EthernetSwitchPortMigrationQosSettingData.Switch_EnableSoftwareReservations
- Msvm_EthernetSwitchPortMigrationQosSettingData.OutboundReservedValue
- Msvm_EthernetSwitchPortMigrationQosSettingData.OutboundMaximumMbps
- Msvm_EthernetSwitchPortMigrationQosSettingData.InboundMaximumMbps
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e279b24178c33c760477995ff744a0699cea1aaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105778590"
---
# <a name="msvm_ethernetswitchportmigrationqossettingdata-class"></a><span data-ttu-id="f36c4-103">\_Classe Msvm EthernetSwitchPortMigrationQosSettingData</span><span class="sxs-lookup"><span data-stu-id="f36c4-103">Msvm\_EthernetSwitchPortMigrationQosSettingData class</span></span>

<span data-ttu-id="f36c4-104">Representa as configurações de QOS VFP.</span><span class="sxs-lookup"><span data-stu-id="f36c4-104">Represents the VFP QOS settings.</span></span>

<span data-ttu-id="f36c4-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="f36c4-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f36c4-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f36c4-106">Syntax</span></span>

``` syntax
[Dynamic, UUID("FD2A5DE3-DC6C-4320-82A5-234D3AF55297"), Provider("VmmsWmiInstanceAndMethodProvider"), ExtensionId("E9B59CFA-2BE1-4B21-828F-B6FBDBDDC017"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port VFP QOS Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortMigrationQosSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string  QueueId = "";
  uint8   Switch_ReservationMode = 0;
  uint8   Switch_LinkSpeedPercentage = 0;
  uint64  Switch_DefaultReservation = 0;
  boolean Switch_EnableHardwareLimits = FALSE;
  boolean Switch_EnableHardwareReservations = FALSE;
  boolean Switch_EnableSoftwareReservations = TRUE;
  uint64  OutboundReservedValue = 0;
  uint64  OutboundMaximumMbps = 0;
  uint64  InboundMaximumMbps = 0;
};
```

## <a name="members"></a><span data-ttu-id="f36c4-107">Membros</span><span class="sxs-lookup"><span data-stu-id="f36c4-107">Members</span></span>

<span data-ttu-id="f36c4-108">A classe **Msvm \_ EthernetSwitchPortMigrationQosSettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="f36c4-108">The **Msvm\_EthernetSwitchPortMigrationQosSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="f36c4-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f36c4-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f36c4-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f36c4-110">Properties</span></span>

<span data-ttu-id="f36c4-111">A classe **Msvm \_ EthernetSwitchPortMigrationQosSettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="f36c4-111">The **Msvm\_EthernetSwitchPortMigrationQosSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f36c4-112">**InboundMaximumMbps**</span><span class="sxs-lookup"><span data-stu-id="f36c4-112">**InboundMaximumMbps**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f36c4-113">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f36c4-113">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f36c4-114">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f36c4-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f36c4-115">Qualificadores: **WmiDataId** (10), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="f36c4-115">Qualifiers: **WmiDataId** (10), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="f36c4-116">O valor de limite de largura de banda para o tráfego de entrada.</span><span class="sxs-lookup"><span data-stu-id="f36c4-116">The bandwidth cap value for inbound traffic.</span></span>

</dd> <dt>

<span data-ttu-id="f36c4-117">**OutboundMaximumMbps**</span><span class="sxs-lookup"><span data-stu-id="f36c4-117">**OutboundMaximumMbps**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f36c4-118">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f36c4-118">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f36c4-119">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f36c4-119">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f36c4-120">Qualificadores: **WmiDataId** (9), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="f36c4-120">Qualifiers: **WmiDataId** (9), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="f36c4-121">O valor de limite de largura de banda para o tráfego de saída.</span><span class="sxs-lookup"><span data-stu-id="f36c4-121">The bandwidth cap value for outbound traffic.</span></span>

</dd> <dt>

<span data-ttu-id="f36c4-122">**OutboundReservedValue**</span><span class="sxs-lookup"><span data-stu-id="f36c4-122">**OutboundReservedValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f36c4-123">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f36c4-123">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f36c4-124">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f36c4-124">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f36c4-125">Qualificadores: **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="f36c4-125">Qualifiers: **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="f36c4-126">O valor de reserva de largura de banda.</span><span class="sxs-lookup"><span data-stu-id="f36c4-126">The bandwidth reservation value.</span></span>

</dd> <dt>

<span data-ttu-id="f36c4-127">**Queueid**</span><span class="sxs-lookup"><span data-stu-id="f36c4-127">**QueueId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f36c4-128">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f36c4-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f36c4-129">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f36c4-129">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f36c4-130">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="f36c4-130">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="f36c4-131">A ID da fila de QOS.</span><span class="sxs-lookup"><span data-stu-id="f36c4-131">The ID of the QOS queue.</span></span>

</dd> <dt>

<span data-ttu-id="f36c4-132">**Alternar \_ Defaultreservation**</span><span class="sxs-lookup"><span data-stu-id="f36c4-132">**Switch\_DefaultReservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f36c4-133">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f36c4-133">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f36c4-134">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f36c4-134">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f36c4-135">Qualificadores: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="f36c4-135">Qualifiers: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="f36c4-136">O valor de reserva padrão.</span><span class="sxs-lookup"><span data-stu-id="f36c4-136">The default reservation value.</span></span>

</dd> <dt>

<span data-ttu-id="f36c4-137">**Alternar \_ EnableHardwareLimits**</span><span class="sxs-lookup"><span data-stu-id="f36c4-137">**Switch\_EnableHardwareLimits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f36c4-138">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="f36c4-138">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f36c4-139">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f36c4-139">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f36c4-140">Qualificadores: **WmiDataId** (5), [**versão**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**revisão**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="f36c4-140">Qualifiers: **WmiDataId** (5), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="f36c4-141">Indica se há uma tentativa de descarregamentos de hardware para limites, se disponível.</span><span class="sxs-lookup"><span data-stu-id="f36c4-141">Indicates whether hardware offloads for limits are attempted if available.</span></span>

</dd> <dt>

<span data-ttu-id="f36c4-142">**Alternar \_ EnableHardwareReservations**</span><span class="sxs-lookup"><span data-stu-id="f36c4-142">**Switch\_EnableHardwareReservations**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f36c4-143">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="f36c4-143">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f36c4-144">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f36c4-144">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f36c4-145">Qualificadores: **WmiDataId** (6), [**versão**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**revisão**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="f36c4-145">Qualifiers: **WmiDataId** (6), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="f36c4-146">Indica se há tentativas de descarregamentos de hardware para reservas, se disponíveis.</span><span class="sxs-lookup"><span data-stu-id="f36c4-146">Indicates whether hardware offloads for reservations are attempted if available.</span></span>

</dd> <dt>

<span data-ttu-id="f36c4-147">**Alternar \_ EnableSoftwareReservations**</span><span class="sxs-lookup"><span data-stu-id="f36c4-147">**Switch\_EnableSoftwareReservations**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f36c4-148">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="f36c4-148">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f36c4-149">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f36c4-149">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f36c4-150">Qualificadores: **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="f36c4-150">Qualifiers: **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="f36c4-151">Indica se a reserva baseada em software está disponível.</span><span class="sxs-lookup"><span data-stu-id="f36c4-151">Indicates whether software based reservation is available.</span></span>

</dd> <dt>

<span data-ttu-id="f36c4-152">**Alternar \_ LinkSpeedPercentage**</span><span class="sxs-lookup"><span data-stu-id="f36c4-152">**Switch\_LinkSpeedPercentage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f36c4-153">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="f36c4-153">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="f36c4-154">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f36c4-154">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f36c4-155">Qualificadores: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="f36c4-155">Qualifiers: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="f36c4-156">A porcentagem de velocidade do link a ser usada para reserva.</span><span class="sxs-lookup"><span data-stu-id="f36c4-156">The link speed percentage to be used for reservation.</span></span>

</dd> <dt>

<span data-ttu-id="f36c4-157">**Alternar \_ reservamode**</span><span class="sxs-lookup"><span data-stu-id="f36c4-157">**Switch\_ReservationMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f36c4-158">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="f36c4-158">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="f36c4-159">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f36c4-159">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f36c4-160">Qualificadores: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="f36c4-160">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="f36c4-161">O modo de reserva de QOS no comutador.</span><span class="sxs-lookup"><span data-stu-id="f36c4-161">The QOS reservation mode on the switch.</span></span>

<dt>

<span id="Absolute"></span><span id="absolute"></span><span id="ABSOLUTE"></span>

<span data-ttu-id="f36c4-162">**Absoluto** (0)</span><span class="sxs-lookup"><span data-stu-id="f36c4-162">**Absolute** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Weight"></span><span id="weight"></span><span id="WEIGHT"></span>

<span data-ttu-id="f36c4-163">**Peso** (1)</span><span class="sxs-lookup"><span data-stu-id="f36c4-163">**Weight** (1)</span></span>


<span data-ttu-id="f36c4-164"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="f36c4-164"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="f36c4-165">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f36c4-165">Requirements</span></span>



| <span data-ttu-id="f36c4-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="f36c4-166">Requirement</span></span> | <span data-ttu-id="f36c4-167">Valor</span><span class="sxs-lookup"><span data-stu-id="f36c4-167">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f36c4-168">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f36c4-168">Minimum supported client</span></span><br/> | <span data-ttu-id="f36c4-169">\[Somente aplicativos da área de trabalho do Windows 10, versão 1703\]</span><span class="sxs-lookup"><span data-stu-id="f36c4-169">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="f36c4-170">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f36c4-170">Minimum supported server</span></span><br/> | <span data-ttu-id="f36c4-171">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="f36c4-171">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="f36c4-172">Namespace</span><span class="sxs-lookup"><span data-stu-id="f36c4-172">Namespace</span></span><br/>                | <span data-ttu-id="f36c4-173">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="f36c4-173">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f36c4-174">MOF</span><span class="sxs-lookup"><span data-stu-id="f36c4-174">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f36c4-175"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f36c4-175"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f36c4-176">DLL</span><span class="sxs-lookup"><span data-stu-id="f36c4-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f36c4-177"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f36c4-177"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f36c4-178">Confira também</span><span class="sxs-lookup"><span data-stu-id="f36c4-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f36c4-179">**Msvm \_ EthernetSwitchPortFeatureSettingData**</span><span class="sxs-lookup"><span data-stu-id="f36c4-179">**Msvm\_EthernetSwitchPortFeatureSettingData**</span></span>](msvm-ethernetswitchportfeaturesettingdata.md)
</dt> </dl>

 

