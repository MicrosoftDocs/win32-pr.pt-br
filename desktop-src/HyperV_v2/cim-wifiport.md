---
description: Representa um dispositivo de comunicações de rede local sem fio que está em conformidade com a série de especificações do IEEE 802,11.
ms.assetid: c4e3345f-5c7d-4d1d-9a94-64112d7334ff
title: Classe CIM_WiFiPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_WiFiPort
- CIM_WiFiPort.Speed
- CIM_WiFiPort.MaxSpeed
- CIM_WiFiPort.PortType
- CIM_WiFiPort.PermanentAddress
- CIM_WiFiPort.NetworkAddresses
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 098bd0a3795f3e8e0531be5286a65b79d9f6ee0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828719"
---
# <a name="cim_wifiport-class"></a><span data-ttu-id="a3dff-103">\_Classe CIM WiFiPort</span><span class="sxs-lookup"><span data-stu-id="a3dff-103">CIM\_WiFiPort class</span></span>

<span data-ttu-id="a3dff-104">Representa um dispositivo de comunicações de rede local sem fio que está em conformidade com a série de especificações do IEEE 802,11.</span><span class="sxs-lookup"><span data-stu-id="a3dff-104">Represents a wireless local area network communications device that conforms to the IEEE 802.11 series of specifications.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3dff-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a3dff-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Device::Ports"), AMENDMENT]
class CIM_WiFiPort : CIM_NetworkPort
{
  uint64 Speed;
  uint64 MaxSpeed;
  uint16 PortType;
  string PermanentAddress;
  string NetworkAddresses[];
};
```

## <a name="members"></a><span data-ttu-id="a3dff-106">Membros</span><span class="sxs-lookup"><span data-stu-id="a3dff-106">Members</span></span>

<span data-ttu-id="a3dff-107">A classe **CIM \_ WiFiPort** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="a3dff-107">The **CIM\_WiFiPort** class has these types of members:</span></span>

-   [<span data-ttu-id="a3dff-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a3dff-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a3dff-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a3dff-109">Properties</span></span>

<span data-ttu-id="a3dff-110">A classe **CIM \_ WiFiPort** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="a3dff-110">The **CIM\_WiFiPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a3dff-111">**MaxSpeed**</span><span class="sxs-lookup"><span data-stu-id="a3dff-111">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3dff-112">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a3dff-112">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a3dff-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a3dff-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a3dff-114">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("MaxSpeed")</span><span class="sxs-lookup"><span data-stu-id="a3dff-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("MaxSpeed")</span></span>
</dt> </dl>

<span data-ttu-id="a3dff-115">A largura de banda máxima com suporte, em bits por segundo, com base no modo de operação especificado na propriedade **PortType** .</span><span class="sxs-lookup"><span data-stu-id="a3dff-115">The maximum supported bandwidth, in bits per second, based on the operating mode specified in the **PortType** property.</span></span> <span data-ttu-id="a3dff-116">Por exemplo, **MaxSpeed** será "11 milhões" se **PortType** contiver "71" (802.11 b).</span><span class="sxs-lookup"><span data-stu-id="a3dff-116">For example, **MaxSpeed** is "11000000" if **PortType** contains "71" (802.11b).</span></span>

</dd> <dt>

<span data-ttu-id="a3dff-117">**NetworkAddresses**</span><span class="sxs-lookup"><span data-stu-id="a3dff-117">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3dff-118">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a3dff-118">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a3dff-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a3dff-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a3dff-120">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NetworkAddresses")</span><span class="sxs-lookup"><span data-stu-id="a3dff-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NetworkAddresses")</span></span>
</dt> </dl>

<span data-ttu-id="a3dff-121">Uma matriz que contém os endereços MAC IEEE 802 EUI-48.</span><span class="sxs-lookup"><span data-stu-id="a3dff-121">An array that contains the IEEE 802 EUI-48 MAC addresses.</span></span> <span data-ttu-id="a3dff-122">O endereço MAC é formatado como doze dígitos hexadecimais, sendo cada par que representa um dos seis octetos do endereço MAC na ordem de bits canônica.</span><span class="sxs-lookup"><span data-stu-id="a3dff-122">The MAC address is formatted as twelve hexadecimal digits, with each pair representing one of the six octets of the MAC address in canonical bit order.</span></span>

</dd> <dt>

<span data-ttu-id="a3dff-123">**PermanentAddress**</span><span class="sxs-lookup"><span data-stu-id="a3dff-123">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3dff-124">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a3dff-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a3dff-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a3dff-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a3dff-126">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PermanentAddress")</span><span class="sxs-lookup"><span data-stu-id="a3dff-126">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PermanentAddress")</span></span>
</dt> </dl>

<span data-ttu-id="a3dff-127">O endereço MAC IEEE 802 EUI-48 da porta.</span><span class="sxs-lookup"><span data-stu-id="a3dff-127">The IEEE 802 EUI-48 MAC address of the port.</span></span> <span data-ttu-id="a3dff-128">O endereço MAC é formatado como doze dígitos hexadecimais, sendo cada par que representa um dos seis octetos do endereço MAC na ordem de bits canônica.</span><span class="sxs-lookup"><span data-stu-id="a3dff-128">The MAC address is formatted as twelve hexadecimal digits, with each pair representing one of the six octets of the MAC address in canonical bit order.</span></span>

</dd> <dt>

<span data-ttu-id="a3dff-129">**PortType**</span><span class="sxs-lookup"><span data-stu-id="a3dff-129">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3dff-130">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a3dff-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a3dff-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a3dff-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a3dff-132">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PortType")</span><span class="sxs-lookup"><span data-stu-id="a3dff-132">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PortType")</span></span>
</dt> </dl>

<span data-ttu-id="a3dff-133">O modo de operação 802,11 que está habilitado na porta.</span><span class="sxs-lookup"><span data-stu-id="a3dff-133">The 802.11 operating mode that is enabled on the port.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a3dff-134">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="a3dff-134">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a3dff-135">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="a3dff-135">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="802.11a"></span><span id="802.11A"></span>

<span data-ttu-id="a3dff-136">**802.11 a** (70)</span><span class="sxs-lookup"><span data-stu-id="a3dff-136">**802.11a** (70)</span></span>


</dt> <dd></dd> <dt>

<span id="802.11b"></span><span id="802.11B"></span>

<span data-ttu-id="a3dff-137">**802.11 b** (71)</span><span class="sxs-lookup"><span data-stu-id="a3dff-137">**802.11b** (71)</span></span>


</dt> <dd></dd> <dt>

<span id="802.11g"></span><span id="802.11G"></span>

<span data-ttu-id="a3dff-138">**802.11 g** (72)</span><span class="sxs-lookup"><span data-stu-id="a3dff-138">**802.11g** (72)</span></span>


</dt> <dd></dd> <dt>

<span id="802.11n"></span><span id="802.11N"></span>

<span data-ttu-id="a3dff-139">**802.11 n** (73)</span><span class="sxs-lookup"><span data-stu-id="a3dff-139">**802.11n** (73)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="a3dff-140">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="a3dff-140">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="a3dff-141">**Fornecedor reservado** (16000..)</span><span class="sxs-lookup"><span data-stu-id="a3dff-141">**Vendor Reserved** (16000..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a3dff-142">**Velocidade**</span><span class="sxs-lookup"><span data-stu-id="a3dff-142">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3dff-143">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a3dff-143">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a3dff-144">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a3dff-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a3dff-145">Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("velocidade")</span><span class="sxs-lookup"><span data-stu-id="a3dff-145">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Speed")</span></span>
</dt> </dl>

<span data-ttu-id="a3dff-146">A taxa de dados na qual a unidade de dados do protocolo PPDU (PLCP (protocolo de convergência de camada física) atual foi recebida, em bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="a3dff-146">The data rate at which the current PPDU (PLCP (Physical Layer Convergence Protocol) Protocol Data Unit) was received, in bits per second.</span></span> <span data-ttu-id="a3dff-147">Esse valor é codificado nos primeiros 4 bits do cabeçalho PLCP em cada quadro PLCP.</span><span class="sxs-lookup"><span data-stu-id="a3dff-147">This value is encoded in the first 4 bits of the PLCP header in each PLCP frame.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a3dff-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a3dff-148">Requirements</span></span>



| <span data-ttu-id="a3dff-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3dff-149">Requirement</span></span> | <span data-ttu-id="a3dff-150">Valor</span><span class="sxs-lookup"><span data-stu-id="a3dff-150">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3dff-151">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a3dff-151">Minimum supported client</span></span><br/> | <span data-ttu-id="a3dff-152">Windows 8</span><span class="sxs-lookup"><span data-stu-id="a3dff-152">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="a3dff-153">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a3dff-153">Minimum supported server</span></span><br/> | <span data-ttu-id="a3dff-154">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a3dff-154">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="a3dff-155">Namespace</span><span class="sxs-lookup"><span data-stu-id="a3dff-155">Namespace</span></span><br/>                | <span data-ttu-id="a3dff-156">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="a3dff-156">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="a3dff-157">MOF</span><span class="sxs-lookup"><span data-stu-id="a3dff-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a3dff-158"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a3dff-158"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a3dff-159">DLL</span><span class="sxs-lookup"><span data-stu-id="a3dff-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a3dff-160"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a3dff-160"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a3dff-161">Confira também</span><span class="sxs-lookup"><span data-stu-id="a3dff-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3dff-162">**\_NETWORKPORT CIM**</span><span class="sxs-lookup"><span data-stu-id="a3dff-162">**CIM\_NetworkPort**</span></span>](cim-networkport.md)
</dt> </dl>

 

