---
description: A \_ classe WMI de associação PrinterController do Win32 relaciona uma impressora e o dispositivo local ao qual a impressora está conectada. Observe que essa classe só retorna instâncias para impressoras locais.
ms.assetid: fb483b28-11f1-4153-893e-492f71763712
ms.tgt_platform: multiple
title: Classe Win32_PrinterController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterController
- Win32_PrinterController.AccessState
- Win32_PrinterController.Antecedent
- Win32_PrinterController.Dependent
- Win32_PrinterController.NegotiatedDataWidth
- Win32_PrinterController.NegotiatedSpeed
- Win32_PrinterController.NumberOfHardResets
- Win32_PrinterController.NumberOfSoftResets
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1ee38b827aed2dfffe1e7ef4f5049b16eee50791
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826419"
---
# <a name="win32_printercontroller-class"></a><span data-ttu-id="1a3d0-104">\_Classe Win32 PrinterController</span><span class="sxs-lookup"><span data-stu-id="1a3d0-104">Win32\_PrinterController class</span></span>

<span data-ttu-id="1a3d0-105">A [classe WMI](../wmisdk/retrieving-a-class.md) de associação **\_ PrinterController do Win32** relaciona uma impressora e o dispositivo local ao qual a impressora está conectada.</span><span class="sxs-lookup"><span data-stu-id="1a3d0-105">The **Win32\_PrinterController** association [WMI class](../wmisdk/retrieving-a-class.md) relates a printer and the local device to which the printer is connected.</span></span> <span data-ttu-id="1a3d0-106">Observe que essa classe só retorna instâncias para impressoras locais.</span><span class="sxs-lookup"><span data-stu-id="1a3d0-106">Note that this class only returns instances for local printers.</span></span>

<span data-ttu-id="1a3d0-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="1a3d0-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="1a3d0-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="1a3d0-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a3d0-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1a3d0-109">Syntax</span></span>

``` syntax
class Win32_PrinterController : CIM_ControlledBy
{
  uint16             AccessState;
  CIM_Controller REF Antecedent;
  Win32_Printer  REF Dependent;
  uint32             NegotiatedDataWidth;
  uint64             NegotiatedSpeed;
  uint32             NumberOfHardResets;
  uint32             NumberOfSoftResets;
};
```

## <a name="members"></a><span data-ttu-id="1a3d0-110">Membros</span><span class="sxs-lookup"><span data-stu-id="1a3d0-110">Members</span></span>

<span data-ttu-id="1a3d0-111">A classe **Win32 \_ PrinterController** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="1a3d0-111">The **Win32\_PrinterController** class has these types of members:</span></span>

-   [<span data-ttu-id="1a3d0-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1a3d0-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1a3d0-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1a3d0-113">Properties</span></span>

<span data-ttu-id="1a3d0-114">A classe **Win32 \_ PrinterController** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="1a3d0-114">The **Win32\_PrinterController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1a3d0-115">**Accessstate**</span><span class="sxs-lookup"><span data-stu-id="1a3d0-115">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a3d0-116">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1a3d0-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1a3d0-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1a3d0-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a3d0-118">Estado do acesso do controlador ao dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1a3d0-118">State of the controller access to the device.</span></span> <span data-ttu-id="1a3d0-119">Essas informações são necessárias quando um dispositivo lógico pode ser acessado ou acessado por meio de vários controladores.</span><span class="sxs-lookup"><span data-stu-id="1a3d0-119">This information is necessary when a logical device can be commanded by, or accessed through, multiple controllers.</span></span>

<span data-ttu-id="1a3d0-120">Essa propriedade é herdada do [**CIM \_ ControlledBy**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="1a3d0-120">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="1a3d0-121"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="1a3d0-121"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="1a3d0-122">Unknown</span><span class="sxs-lookup"><span data-stu-id="1a3d0-122">Unknown</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="1a3d0-123"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="1a3d0-123"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="1a3d0-124">Ativo</span><span class="sxs-lookup"><span data-stu-id="1a3d0-124">Active</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="1a3d0-125"><span id="2"></span>**2**</span><span class="sxs-lookup"><span data-stu-id="1a3d0-125"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="1a3d0-126">Inativo</span><span class="sxs-lookup"><span data-stu-id="1a3d0-126">Inactive</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1a3d0-127">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="1a3d0-127">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a3d0-128">Tipo de dados **: \_ controlador CIM**</span><span class="sxs-lookup"><span data-stu-id="1a3d0-128">Data type: **CIM\_Controller**</span></span>
</dt> <dt>

<span data-ttu-id="1a3d0-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1a3d0-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a3d0-130">Qualificadores: [ **chave**](../wmisdk/standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="1a3d0-130">Qualifiers: [**Key**](../wmisdk/standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="1a3d0-131">Referência à instância [**do \_ controlador CIM**](cim-controller.md) que representa o dispositivo local associado a esta impressora.</span><span class="sxs-lookup"><span data-stu-id="1a3d0-131">Reference to the [**CIM\_Controller**](cim-controller.md) instance representing the local device associated with this printer.</span></span>

<span data-ttu-id="1a3d0-132">Essa propriedade é herdada [**da \_ dependência CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="1a3d0-132">This property is inherited from [**CIM\_Dependency**](cim-dependency.md).</span></span>

</dd> <dt>

<span data-ttu-id="1a3d0-133">**Depende**</span><span class="sxs-lookup"><span data-stu-id="1a3d0-133">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a3d0-134">Tipo de dados **: \_ impressora Win32**</span><span class="sxs-lookup"><span data-stu-id="1a3d0-134">Data type: **Win32\_Printer**</span></span>
</dt> <dt>

<span data-ttu-id="1a3d0-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1a3d0-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a3d0-136">Qualificadores: [ **chave**](../wmisdk/standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="1a3d0-136">Qualifiers: [**Key**](../wmisdk/standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="1a3d0-137">Referência à instância [**de \_ impressora do Win32**](win32-printer.md) que representa a impressora associada ao dispositivo local.</span><span class="sxs-lookup"><span data-stu-id="1a3d0-137">Reference to the [**Win32\_Printer**](win32-printer.md) instance representing the printer associated with the local device.</span></span>

<span data-ttu-id="1a3d0-138">Essa propriedade é herdada [**da \_ dependência CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="1a3d0-138">This property is inherited from [**CIM\_Dependency**](cim-dependency.md).</span></span>

</dd> <dt>

<span data-ttu-id="1a3d0-139">**NegotiatedDataWidth**</span><span class="sxs-lookup"><span data-stu-id="1a3d0-139">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a3d0-140">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1a3d0-140">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1a3d0-141">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1a3d0-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a3d0-142">Largura de dados em uso entre os dispositivos (quando várias larguras de dados de conexão ou barramento são possíveis).</span><span class="sxs-lookup"><span data-stu-id="1a3d0-142">Data width in use between devices (when several bus or connection data widths are possible).</span></span> <span data-ttu-id="1a3d0-143">A largura dos dados é especificada em bits.</span><span class="sxs-lookup"><span data-stu-id="1a3d0-143">Data width is specified in bits.</span></span> <span data-ttu-id="1a3d0-144">Se a largura dos dados não for negociada ou se essas informações não estiverem disponíveis ou importantes para o gerenciamento de dispositivos, a propriedade deverá ser definida como 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="1a3d0-144">If data width is not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="1a3d0-145">Essa propriedade é herdada do [**CIM \_ DeviceConnection**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="1a3d0-145">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="1a3d0-146">**NegotiatedSpeed**</span><span class="sxs-lookup"><span data-stu-id="1a3d0-146">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a3d0-147">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1a3d0-147">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1a3d0-148">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1a3d0-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a3d0-149">Velocidade em uso entre os dispositivos (quando várias velocidades de barramento ou conexão são possíveis).</span><span class="sxs-lookup"><span data-stu-id="1a3d0-149">Speed in use between devices (when several bus or connection speeds are possible).</span></span> <span data-ttu-id="1a3d0-150">A velocidade é especificada em bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="1a3d0-150">Speed is specified in bits per second.</span></span> <span data-ttu-id="1a3d0-151">Se as velocidades de conexão ou de barramento não forem negociadas ou se essas informações não estiverem disponíveis ou importantes para o gerenciamento de dispositivos, a propriedade deverá ser definida como 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="1a3d0-151">If connection or bus speeds are not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="1a3d0-152">Essa propriedade é herdada do [**CIM \_ DeviceConnection**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="1a3d0-152">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

<span data-ttu-id="1a3d0-153">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="1a3d0-153">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="1a3d0-154">**NumberOfHardResets**</span><span class="sxs-lookup"><span data-stu-id="1a3d0-154">**NumberOfHardResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a3d0-155">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1a3d0-155">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1a3d0-156">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1a3d0-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a3d0-157">Número de redefinições de hardware emitidas pelo controlador.</span><span class="sxs-lookup"><span data-stu-id="1a3d0-157">Number of hard resets issued by the controller.</span></span>

<span data-ttu-id="1a3d0-158">Essa propriedade é herdada do [**CIM \_ ControlledBy**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="1a3d0-158">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> <dt>

<span data-ttu-id="1a3d0-159">**NumberOfSoftResets**</span><span class="sxs-lookup"><span data-stu-id="1a3d0-159">**NumberOfSoftResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a3d0-160">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1a3d0-160">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1a3d0-161">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1a3d0-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a3d0-162">Número de redefinições reversível emitidas pelo controlador.</span><span class="sxs-lookup"><span data-stu-id="1a3d0-162">Number of soft resets issued by the controller.</span></span>

<span data-ttu-id="1a3d0-163">Essa propriedade é herdada do [**CIM \_ ControlledBy**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="1a3d0-163">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1a3d0-164">Comentários</span><span class="sxs-lookup"><span data-stu-id="1a3d0-164">Remarks</span></span>

<span data-ttu-id="1a3d0-165">A classe **Win32 \_ PrinterController** é derivada de [**CIM \_ ControlledBy**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="1a3d0-165">The **Win32\_PrinterController** class is derived from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1a3d0-166">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1a3d0-166">Requirements</span></span>



| <span data-ttu-id="1a3d0-167">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a3d0-167">Requirement</span></span> | <span data-ttu-id="1a3d0-168">Valor</span><span class="sxs-lookup"><span data-stu-id="1a3d0-168">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a3d0-169">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1a3d0-169">Minimum supported client</span></span><br/> | <span data-ttu-id="1a3d0-170">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1a3d0-170">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="1a3d0-171">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1a3d0-171">Minimum supported server</span></span><br/> | <span data-ttu-id="1a3d0-172">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1a3d0-172">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="1a3d0-173">Namespace</span><span class="sxs-lookup"><span data-stu-id="1a3d0-173">Namespace</span></span><br/>                | <span data-ttu-id="1a3d0-174">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="1a3d0-174">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="1a3d0-175">MOF</span><span class="sxs-lookup"><span data-stu-id="1a3d0-175">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1a3d0-176"><dt>\_Impressora. mof do Win32</dt></span><span class="sxs-lookup"><span data-stu-id="1a3d0-176"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="1a3d0-177">DLL</span><span class="sxs-lookup"><span data-stu-id="1a3d0-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1a3d0-178"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1a3d0-178"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="1a3d0-179">Confira também</span><span class="sxs-lookup"><span data-stu-id="1a3d0-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a3d0-180">**\_CONTROLLEDBY CIM**</span><span class="sxs-lookup"><span data-stu-id="1a3d0-180">**CIM\_ControlledBy**</span></span>](cim-controlledby.md)
</dt> <dt>

[<span data-ttu-id="1a3d0-181">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="1a3d0-181">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
