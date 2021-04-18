---
description: Descreve os recursos e o gerenciamento de um controlador serial.
ms.assetid: ce3e0424-4ab8-435d-a155-1164535b3b0d
title: Classe CIM_SerialController (gerenciamento do Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SerialController
- CIM_SerialController.Capabilities
- CIM_SerialController.CapabilityDescriptions
- CIM_SerialController.MaxBaudRate
- CIM_SerialController.Security
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4a2e69bab38bb8b68c15ed93b2bee721c35a7600
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105787112"
---
# <a name="cim_serialcontroller-class-hyper-v-management"></a><span data-ttu-id="ab348-103">Classe CIM_SerialController (gerenciamento do Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="ab348-103">CIM_SerialController class (Hyper-V management)</span></span>

<span data-ttu-id="ab348-104">Descreve os recursos e o gerenciamento de um controlador serial.</span><span class="sxs-lookup"><span data-stu-id="ab348-104">Describes the capabilities and management of a serial controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab348-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ab348-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::Controller"), AMENDMENT]
class CIM_SerialController : CIM_Controller
{
  uint16 Capabilities[];
  string CapabilityDescriptions[];
  uint32 MaxBaudRate;
  uint16 Security;
};
```

## <a name="members"></a><span data-ttu-id="ab348-106">Membros</span><span class="sxs-lookup"><span data-stu-id="ab348-106">Members</span></span>

<span data-ttu-id="ab348-107">A classe **CIM \_ SerialController** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="ab348-107">The **CIM\_SerialController** class has these types of members:</span></span>

-   [<span data-ttu-id="ab348-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ab348-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ab348-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ab348-109">Properties</span></span>

<span data-ttu-id="ab348-110">A classe **CIM \_ SerialController** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="ab348-110">The **CIM\_SerialController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ab348-111">**Funcionalidades**</span><span class="sxs-lookup"><span data-stu-id="ab348-111">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab348-112">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ab348-112">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ab348-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ab348-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab348-114">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Portas seriais DMTF \| 4,7 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ SerialController**.**CapabilityDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="ab348-114">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Serial Ports\|004.7"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_SerialController**.**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="ab348-115">A compatibilidade no nível do chip para o controlador serial.</span><span class="sxs-lookup"><span data-stu-id="ab348-115">The chip level compatibility for the serial controller.</span></span> <span data-ttu-id="ab348-116">Esta propriedade descreve o buffer e outros recursos do controlador serial que podem ser inerentes ao hardware do chip.</span><span class="sxs-lookup"><span data-stu-id="ab348-116">This property describes the buffering and other capabilities of the serial controller that might be inherent in the chip hardware.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ab348-117">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="ab348-117">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ab348-118">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="ab348-118">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="XT_AT_Compatible"></span><span id="xt_at_compatible"></span><span id="XT_AT_COMPATIBLE"></span>

<span data-ttu-id="ab348-119">**XT/at compatível** (3)</span><span class="sxs-lookup"><span data-stu-id="ab348-119">**XT/AT Compatible** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="16450_Compatible"></span><span id="16450_compatible"></span><span id="16450_COMPATIBLE"></span>

<span data-ttu-id="ab348-120">**compatível com 16450** (4)</span><span class="sxs-lookup"><span data-stu-id="ab348-120">**16450 Compatible** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="16550_Compatible"></span><span id="16550_compatible"></span><span id="16550_COMPATIBLE"></span>

<span data-ttu-id="ab348-121">**compatível com 16550** (5)</span><span class="sxs-lookup"><span data-stu-id="ab348-121">**16550 Compatible** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="16550A_Compatible"></span><span id="16550a_compatible"></span><span id="16550A_COMPATIBLE"></span>

<span data-ttu-id="ab348-122">**compatível com 16550A** (6)</span><span class="sxs-lookup"><span data-stu-id="ab348-122">**16550A Compatible** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="8251_Compatible"></span><span id="8251_compatible"></span><span id="8251_COMPATIBLE"></span>

<span data-ttu-id="ab348-123">**compatível com 8251** (160)</span><span class="sxs-lookup"><span data-stu-id="ab348-123">**8251 Compatible** (160)</span></span>


</dt> <dd></dd> <dt>

<span id="8251FIFO_Compatible"></span><span id="8251fifo_compatible"></span><span id="8251FIFO_COMPATIBLE"></span>

<span data-ttu-id="ab348-124">**compatível com 8251FIFO** (161)</span><span class="sxs-lookup"><span data-stu-id="ab348-124">**8251FIFO Compatible** (161)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ab348-125">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="ab348-125">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab348-126">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ab348-126">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ab348-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ab348-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab348-128">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (**" \_ CIM SerialController**.**Recursos**")</span><span class="sxs-lookup"><span data-stu-id="ab348-128">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_SerialController**.**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="ab348-129">Uma matriz que contém explicações mais detalhadas para recursos do controlador serial na matriz **Capabilities** .</span><span class="sxs-lookup"><span data-stu-id="ab348-129">An array that contains more detailed explanations for serial controller features in the **Capabilities** array.</span></span> <span data-ttu-id="ab348-130">Os itens na matriz **CapabilityDescriptions** correlacionam-se com aqueles na matriz de **recursos** .</span><span class="sxs-lookup"><span data-stu-id="ab348-130">The items in the **CapabilityDescriptions** array correlate to those in the **Capabilities** array.</span></span>

</dd> <dt>

<span data-ttu-id="ab348-131">**MaxBaudRate**</span><span class="sxs-lookup"><span data-stu-id="ab348-131">**MaxBaudRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab348-132">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ab348-132">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab348-133">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ab348-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab348-134">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits por segundo"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Portas seriais DMTF \| 4,6 "), **PUnit** (" bit/segundo ")</span><span class="sxs-lookup"><span data-stu-id="ab348-134">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits per Second"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Serial Ports\|004.6"), **PUnit** ("bit / second")</span></span>
</dt> </dl>

<span data-ttu-id="ab348-135">A taxa de baud máxima em, bits por segundo, com suporte do controlador serial.</span><span class="sxs-lookup"><span data-stu-id="ab348-135">The maximum baud rate in, bits per second, that is supported by the serial controller.</span></span>

</dd> <dt>

<span data-ttu-id="ab348-136">**Segurança**</span><span class="sxs-lookup"><span data-stu-id="ab348-136">**Security**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab348-137">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ab348-137">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ab348-138">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ab348-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab348-139">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Portas seriais DMTF \| 4,9 ")</span><span class="sxs-lookup"><span data-stu-id="ab348-139">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Serial Ports\|004.9")</span></span>
</dt> </dl>

<span data-ttu-id="ab348-140">A segurança operacional para o controlador.</span><span class="sxs-lookup"><span data-stu-id="ab348-140">The operational security for the controller.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ab348-141">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="ab348-141">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ab348-142">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="ab348-142">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="ab348-143">**Nenhum** (3)</span><span class="sxs-lookup"><span data-stu-id="ab348-143">**None** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="External_Interface_Locked_Out"></span><span id="external_interface_locked_out"></span><span id="EXTERNAL_INTERFACE_LOCKED_OUT"></span>

<span data-ttu-id="ab348-144">**Interface externa bloqueada** (4)</span><span class="sxs-lookup"><span data-stu-id="ab348-144">**External Interface Locked Out** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="External_Interface_Enabled"></span><span id="external_interface_enabled"></span><span id="EXTERNAL_INTERFACE_ENABLED"></span>

<span data-ttu-id="ab348-145">**Interface externa habilitada** (5)</span><span class="sxs-lookup"><span data-stu-id="ab348-145">**External Interface Enabled** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Boot_Bypass"></span><span id="boot_bypass"></span><span id="BOOT_BYPASS"></span>

<span data-ttu-id="ab348-146">**Bypass de inicialização** (6)</span><span class="sxs-lookup"><span data-stu-id="ab348-146">**Boot Bypass** (6)</span></span>


<span data-ttu-id="ab348-147"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="ab348-147"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="ab348-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ab348-148">Requirements</span></span>



| <span data-ttu-id="ab348-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab348-149">Requirement</span></span> | <span data-ttu-id="ab348-150">Valor</span><span class="sxs-lookup"><span data-stu-id="ab348-150">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab348-151">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ab348-151">Minimum supported client</span></span><br/> | <span data-ttu-id="ab348-152">Windows 8</span><span class="sxs-lookup"><span data-stu-id="ab348-152">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="ab348-153">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ab348-153">Minimum supported server</span></span><br/> | <span data-ttu-id="ab348-154">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ab348-154">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="ab348-155">Namespace</span><span class="sxs-lookup"><span data-stu-id="ab348-155">Namespace</span></span><br/>                | <span data-ttu-id="ab348-156">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="ab348-156">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ab348-157">MOF</span><span class="sxs-lookup"><span data-stu-id="ab348-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ab348-158"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ab348-158"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ab348-159">DLL</span><span class="sxs-lookup"><span data-stu-id="ab348-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ab348-160"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ab348-160"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ab348-161">Confira também</span><span class="sxs-lookup"><span data-stu-id="ab348-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab348-162">**\_Controlador CIM**</span><span class="sxs-lookup"><span data-stu-id="ab348-162">**CIM\_Controller**</span></span>](cim-controller.md)
</dt> </dl>

 

