---
description: Uma relação que indica que dois ou mais dispositivos estão conectados juntos.
ms.assetid: 84282740-f60f-46fa-95b7-b52a7e6efcc4
title: Classe CIM_DeviceConnection (gerenciamento do Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceConnection
- CIM_DeviceConnection.Antecedent
- CIM_DeviceConnection.Dependent
- CIM_DeviceConnection.NegotiatedSpeed
- CIM_DeviceConnection.NegotiatedDataWidth
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f58c66199abeb5b3586f52e91828b8b194bdbbd1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770229"
---
# <a name="cim_deviceconnection-class-hyper-v-management"></a><span data-ttu-id="f39b2-103">Classe CIM_DeviceConnection (gerenciamento do Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="f39b2-103">CIM_DeviceConnection class (Hyper-V management)</span></span>

<span data-ttu-id="f39b2-104">Uma relação que indica que dois ou mais dispositivos estão conectados juntos.</span><span class="sxs-lookup"><span data-stu-id="f39b2-104">A relationship that indicates that two or more devices are connected together.</span></span>

## <a name="syntax"></a><span data-ttu-id="f39b2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f39b2-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::DeviceElements"), AMENDMENT]
class CIM_DeviceConnection : CIM_Dependency
{
  CIM_LogicalDevice REF Antecedent;
  CIM_LogicalDevice REF Dependent;
  uint64                NegotiatedSpeed;
  uint32                NegotiatedDataWidth;
};
```

## <a name="members"></a><span data-ttu-id="f39b2-106">Membros</span><span class="sxs-lookup"><span data-stu-id="f39b2-106">Members</span></span>

<span data-ttu-id="f39b2-107">A classe **CIM \_ DeviceConnection** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="f39b2-107">The **CIM\_DeviceConnection** class has these types of members:</span></span>

-   [<span data-ttu-id="f39b2-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f39b2-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f39b2-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f39b2-109">Properties</span></span>

<span data-ttu-id="f39b2-110">A classe **CIM \_ DeviceConnection** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="f39b2-110">The **CIM\_DeviceConnection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f39b2-111">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="f39b2-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f39b2-112">Tipo de dados **: \_ LogicalDevice CIM**</span><span class="sxs-lookup"><span data-stu-id="f39b2-112">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="f39b2-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f39b2-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f39b2-114">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="f39b2-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="f39b2-115">Um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f39b2-115">A device.</span></span>

</dd> <dt>

<span data-ttu-id="f39b2-116">**Depende**</span><span class="sxs-lookup"><span data-stu-id="f39b2-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f39b2-117">Tipo de dados **: \_ LogicalDevice CIM**</span><span class="sxs-lookup"><span data-stu-id="f39b2-117">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="f39b2-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f39b2-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f39b2-119">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="f39b2-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="f39b2-120">Um segundo dispositivo que está conectado a outro dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f39b2-120">A second device that is connected to the other device.</span></span>

</dd> <dt>

<span data-ttu-id="f39b2-121">**NegotiatedDataWidth**</span><span class="sxs-lookup"><span data-stu-id="f39b2-121">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f39b2-122">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f39b2-122">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f39b2-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f39b2-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f39b2-124">Qualificadores: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Associação de porta do barramento DMTF \| 1,3 "), **PUnit** (" bit ")</span><span class="sxs-lookup"><span data-stu-id="f39b2-124">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port Association\|001.3"), **PUnit** ("bit")</span></span>
</dt> </dl>

<span data-ttu-id="f39b2-125">Quando várias larguras de dados de conexão e barramento são possíveis, a propriedade NegotiatedDataWidth define aquela que está em uso entre os dispositivos.</span><span class="sxs-lookup"><span data-stu-id="f39b2-125">When several bus and connection data widths are possible, the NegotiatedDataWidth property defines the one that is in use between the Devices.</span></span> <span data-ttu-id="f39b2-126">A largura dos dados é especificada em bits.</span><span class="sxs-lookup"><span data-stu-id="f39b2-126">Data width is specified in bits.</span></span> <span data-ttu-id="f39b2-127">Se a largura dos dados não for negociada ou se essas informações não estiverem disponíveis ou não forem importantes para o gerenciamento de dispositivos, a propriedade deverá ser definida como 0.</span><span class="sxs-lookup"><span data-stu-id="f39b2-127">If data width is not negotiated, or if this information is not available or not important to Device management, the property should be set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="f39b2-128">**NegotiatedSpeed**</span><span class="sxs-lookup"><span data-stu-id="f39b2-128">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f39b2-129">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f39b2-129">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f39b2-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f39b2-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f39b2-131">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits por segundo"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Associação de porta do barramento DMTF \| 1,2 "), **PUnit** (" bit/segundo ")</span><span class="sxs-lookup"><span data-stu-id="f39b2-131">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits per Second"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port Association\|001.2"), **PUnit** ("bit / second")</span></span>
</dt> </dl>

<span data-ttu-id="f39b2-132">Quando várias velocidades de barramento e conexão são possíveis, essa propriedade define a velocidade em uso entre os dispositivos, em bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="f39b2-132">When several bus and connection speeds are possible, this property defines the speed that is in use between the devices, in bits per second.</span></span> <span data-ttu-id="f39b2-133">Se as velocidades de conexão ou de barramento não forem negociadas, ou se essas informações não estiverem disponíveis ou não forem importantes para o gerenciamento de dispositivos, a propriedade deverá ser definida como "0".</span><span class="sxs-lookup"><span data-stu-id="f39b2-133">If connection or bus speeds are not negotiated, or if this information is not available, or not important to device management, the property should be set to "0".</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f39b2-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f39b2-134">Requirements</span></span>



| <span data-ttu-id="f39b2-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="f39b2-135">Requirement</span></span> | <span data-ttu-id="f39b2-136">Valor</span><span class="sxs-lookup"><span data-stu-id="f39b2-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f39b2-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f39b2-137">Minimum supported client</span></span><br/> | <span data-ttu-id="f39b2-138">Windows 8</span><span class="sxs-lookup"><span data-stu-id="f39b2-138">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="f39b2-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f39b2-139">Minimum supported server</span></span><br/> | <span data-ttu-id="f39b2-140">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f39b2-140">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="f39b2-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="f39b2-141">Namespace</span></span><br/>                | <span data-ttu-id="f39b2-142">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="f39b2-142">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f39b2-143">MOF</span><span class="sxs-lookup"><span data-stu-id="f39b2-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f39b2-144"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f39b2-144"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f39b2-145">DLL</span><span class="sxs-lookup"><span data-stu-id="f39b2-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f39b2-146"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f39b2-146"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f39b2-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="f39b2-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f39b2-148">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="f39b2-148">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

