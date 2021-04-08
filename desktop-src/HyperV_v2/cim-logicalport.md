---
description: A abstração de um ponto de conexão ou porta de um dispositivo.
ms.assetid: ee725c64-587b-4e5f-9b1c-7a58902b0631
title: Classe CIM_LogicalPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalPort
- CIM_LogicalPort.Speed
- CIM_LogicalPort.MaxSpeed
- CIM_LogicalPort.RequestedSpeed
- CIM_LogicalPort.UsageRestriction
- CIM_LogicalPort.PortType
- CIM_LogicalPort.OtherPortType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: eeed69e9669048377340cb0ca21e7a2e89f4baff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920666"
---
# <a name="cim_logicalport-class"></a><span data-ttu-id="8f849-103">\_Classe CIM LogicalPort</span><span class="sxs-lookup"><span data-stu-id="8f849-103">CIM\_LogicalPort class</span></span>

<span data-ttu-id="8f849-104">A abstração de um ponto de conexão ou porta de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8f849-104">The abstraction of a port or connection point of a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f849-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8f849-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::Ports"), AMENDMENT]
class CIM_LogicalPort : CIM_LogicalDevice
{
  uint64 Speed;
  uint64 MaxSpeed;
  uint64 RequestedSpeed;
  uint16 UsageRestriction;
  uint16 PortType;
  string OtherPortType;
};
```

## <a name="members"></a><span data-ttu-id="8f849-106">Membros</span><span class="sxs-lookup"><span data-stu-id="8f849-106">Members</span></span>

<span data-ttu-id="8f849-107">A classe **CIM \_ LogicalPort** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="8f849-107">The **CIM\_LogicalPort** class has these types of members:</span></span>

-   [<span data-ttu-id="8f849-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8f849-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8f849-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8f849-109">Properties</span></span>

<span data-ttu-id="8f849-110">A classe **CIM \_ LogicalPort** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="8f849-110">The **CIM\_LogicalPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8f849-111">**MaxSpeed**</span><span class="sxs-lookup"><span data-stu-id="8f849-111">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f849-112">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8f849-112">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8f849-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8f849-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f849-114">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits por segundo"), **PUnit** ("bit/segundo")</span><span class="sxs-lookup"><span data-stu-id="8f849-114">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits per Second"), **PUnit** ("bit / second")</span></span>
</dt> </dl>

<span data-ttu-id="8f849-115">A largura de banda máxima da porta, em bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="8f849-115">The maximum bandwidth of the port, in bits per second.</span></span>

</dd> <dt>

<span data-ttu-id="8f849-116">**OtherPortType**</span><span class="sxs-lookup"><span data-stu-id="8f849-116">**OtherPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f849-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8f849-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f849-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8f849-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f849-119">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ LogicalPort**.**PortType**")</span><span class="sxs-lookup"><span data-stu-id="8f849-119">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_LogicalPort**.**PortType**")</span></span>
</dt> </dl>

<span data-ttu-id="8f849-120">Descreve o tipo de módulo, quando **PortType** é definido como **Other** ("1").</span><span class="sxs-lookup"><span data-stu-id="8f849-120">Describes the type of module, when **PortType** is set to **Other** ("1").</span></span>

</dd> <dt>

<span data-ttu-id="8f849-121">**PortType**</span><span class="sxs-lookup"><span data-stu-id="8f849-121">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f849-122">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8f849-122">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8f849-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8f849-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f849-124">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ NetworkPort**](cim-networkport.md).**OtherNetworkPortType**")</span><span class="sxs-lookup"><span data-stu-id="8f849-124">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_NetworkPort**](cim-networkport.md).**OtherNetworkPortType**")</span></span>
</dt> </dl>

<span data-ttu-id="8f849-125">O tipo de porta.</span><span class="sxs-lookup"><span data-stu-id="8f849-125">The port type.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8f849-126">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="8f849-126">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="8f849-127">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="8f849-127">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="8f849-128">**Não aplicável** (2)</span><span class="sxs-lookup"><span data-stu-id="8f849-128">**Not Applicable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="8f849-129">**DMTF reservado** (3.. 15999)</span><span class="sxs-lookup"><span data-stu-id="8f849-129">**DMTF Reserved** (3..15999)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="8f849-130">**Fornecedor reservado** (16000.. 65535)</span><span class="sxs-lookup"><span data-stu-id="8f849-130">**Vendor Reserved** (16000..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8f849-131">**RequestedSpeed**</span><span class="sxs-lookup"><span data-stu-id="8f849-131">**RequestedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f849-132">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8f849-132">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8f849-133">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8f849-133">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8f849-134">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits por segundo"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ LogicalPort**.**Speed**"), **PUnit** (" bit/segundo ")</span><span class="sxs-lookup"><span data-stu-id="8f849-134">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits per Second"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_LogicalPort**.**Speed**"), **PUnit** ("bit / second")</span></span>
</dt> </dl>

<span data-ttu-id="8f849-135">A largura de banda solicitada da porta, em bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="8f849-135">The requested bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="8f849-136">A largura de banda real é relatada na propriedade **Speed** .</span><span class="sxs-lookup"><span data-stu-id="8f849-136">The actual bandwidth is reported in the **Speed** property.</span></span>

</dd> <dt>

<span data-ttu-id="8f849-137">**Velocidade**</span><span class="sxs-lookup"><span data-stu-id="8f849-137">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f849-138">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8f849-138">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8f849-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8f849-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f849-140">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits por segundo"), **PUnit** ("bit/segundo")</span><span class="sxs-lookup"><span data-stu-id="8f849-140">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits per Second"), **PUnit** ("bit / second")</span></span>
</dt> </dl>

<span data-ttu-id="8f849-141">A largura de banda da porta, em bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="8f849-141">The bandwidth of the port, in bits per second.</span></span>

</dd> <dt>

<span data-ttu-id="8f849-142">**UsageRestriction**</span><span class="sxs-lookup"><span data-stu-id="8f849-142">**UsageRestriction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f849-143">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8f849-143">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8f849-144">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8f849-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f849-145">Indica se a porta está restrita a ser uma porta de front-end ou de back-end.</span><span class="sxs-lookup"><span data-stu-id="8f849-145">Indicates whether the port is restricted to being a front-end or back-end port.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8f849-146">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="8f849-146">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>

<span data-ttu-id="8f849-147">**Somente front-end** (2)</span><span class="sxs-lookup"><span data-stu-id="8f849-147">**Front-end only** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span>

<span data-ttu-id="8f849-148">**Somente back-end** (3)</span><span class="sxs-lookup"><span data-stu-id="8f849-148">**Back-end only** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_restricted"></span><span id="not_restricted"></span><span id="NOT_RESTRICTED"></span>

<span data-ttu-id="8f849-149">**Não restrito** (4)</span><span class="sxs-lookup"><span data-stu-id="8f849-149">**Not restricted** (4)</span></span>


<span data-ttu-id="8f849-150"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="8f849-150"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="8f849-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8f849-151">Requirements</span></span>



| <span data-ttu-id="8f849-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f849-152">Requirement</span></span> | <span data-ttu-id="8f849-153">Valor</span><span class="sxs-lookup"><span data-stu-id="8f849-153">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f849-154">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8f849-154">Minimum supported client</span></span><br/> | <span data-ttu-id="8f849-155">Windows 8</span><span class="sxs-lookup"><span data-stu-id="8f849-155">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="8f849-156">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8f849-156">Minimum supported server</span></span><br/> | <span data-ttu-id="8f849-157">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8f849-157">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="8f849-158">Namespace</span><span class="sxs-lookup"><span data-stu-id="8f849-158">Namespace</span></span><br/>                | <span data-ttu-id="8f849-159">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="8f849-159">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="8f849-160">MOF</span><span class="sxs-lookup"><span data-stu-id="8f849-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8f849-161"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8f849-161"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8f849-162">DLL</span><span class="sxs-lookup"><span data-stu-id="8f849-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8f849-163"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8f849-163"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8f849-164">Confira também</span><span class="sxs-lookup"><span data-stu-id="8f849-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f849-165">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="8f849-165">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

