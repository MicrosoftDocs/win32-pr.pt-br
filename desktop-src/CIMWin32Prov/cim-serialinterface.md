---
description: A \_ classe CIM SerialInterface representa um \_ relacionamento CIM ControlledBy que indica quais dispositivos são acessados por meio do controlador serial e as características do acesso.
ms.assetid: bebc304a-c2b7-41c7-b24a-8f450ee3c4bb
ms.tgt_platform: multiple
title: Classe CIM_SerialInterface
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SerialInterface
- CIM_SerialInterface.NegotiatedDataWidth
- CIM_SerialInterface.NegotiatedSpeed
- CIM_SerialInterface.AccessState
- CIM_SerialInterface.NumberOfHardResets
- CIM_SerialInterface.NumberOfSoftResets
- CIM_SerialInterface.Dependent
- CIM_SerialInterface.Antecedent
- CIM_SerialInterface.FlowControlInfo
- CIM_SerialInterface.NumberOfStopBits
- CIM_SerialInterface.ParityInfo
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1df787ff64798f412035a72e6db6d7b01b4b9b0a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826342"
---
# <a name="cim_serialinterface-class"></a><span data-ttu-id="eb989-103">\_Classe CIM SerialInterface</span><span class="sxs-lookup"><span data-stu-id="eb989-103">CIM\_SerialInterface class</span></span>

<span data-ttu-id="eb989-104">A classe **CIM \_ SerialInterface** representa um relacionamento [**CIM \_ ControlledBy**](cim-controlledby.md) que indica quais dispositivos são acessados por meio do controlador serial e as características do acesso.</span><span class="sxs-lookup"><span data-stu-id="eb989-104">The **CIM\_SerialInterface** class represents a [**CIM\_ControlledBy**](cim-controlledby.md) relationship that indicates which devices are accessed through the serial controller and the characteristics of the access.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="eb989-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="eb989-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="eb989-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="eb989-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="eb989-107">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="eb989-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="eb989-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="eb989-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb989-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eb989-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8B309BDA-E3D4-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_SerialInterface : CIM_ControlledBy
{
  uint32                   NegotiatedDataWidth;
  uint64                   NegotiatedSpeed;
  uint16                   AccessState;
  uint32                   NumberOfHardResets;
  uint32                   NumberOfSoftResets;
  CIM_LogicalDevice    REF Dependent;
  CIM_SerialController REF Antecedent;
  uint16                   FlowControlInfo;
  uint16                   NumberOfStopBits;
  uint16                   ParityInfo;
};
```

## <a name="members"></a><span data-ttu-id="eb989-110">Membros</span><span class="sxs-lookup"><span data-stu-id="eb989-110">Members</span></span>

<span data-ttu-id="eb989-111">A classe **CIM \_ SerialInterface** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="eb989-111">The **CIM\_SerialInterface** class has these types of members:</span></span>

-   [<span data-ttu-id="eb989-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="eb989-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="eb989-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="eb989-113">Properties</span></span>

<span data-ttu-id="eb989-114">A classe **CIM \_ SerialInterface** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="eb989-114">The **CIM\_SerialInterface** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="eb989-115">**Accessstate**</span><span class="sxs-lookup"><span data-stu-id="eb989-115">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb989-116">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="eb989-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="eb989-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="eb989-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb989-118">Indica se o controlador está ativando ou acessando ativamente o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="eb989-118">Indicates whether the controller is actively commanding or accessing the device.</span></span> <span data-ttu-id="eb989-119">Essas informações são necessárias quando um dispositivo lógico pode ser acessado ou acessado por meio de vários controladores.</span><span class="sxs-lookup"><span data-stu-id="eb989-119">This information is necessary when a logical device can be commanded by, or accessed through, multiple controllers.</span></span>

<span data-ttu-id="eb989-120">Essa propriedade é herdada do [**CIM \_ ControlledBy**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="eb989-120">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="eb989-121">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="eb989-121">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>

<span data-ttu-id="eb989-122">**Ativo** (1)</span><span class="sxs-lookup"><span data-stu-id="eb989-122">**Active** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Inactive"></span><span id="inactive"></span><span id="INACTIVE"></span>

<span data-ttu-id="eb989-123">**Inativo** (2)</span><span class="sxs-lookup"><span data-stu-id="eb989-123">**Inactive** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="eb989-124">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="eb989-124">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb989-125">Tipo de dados: **CIM \_ SerialController**</span><span class="sxs-lookup"><span data-stu-id="eb989-125">Data type: **CIM\_SerialController**</span></span>
</dt> <dt>

<span data-ttu-id="eb989-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="eb989-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb989-127">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="eb989-127">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="eb989-128">Um [**\_ SerialController CIM**](cim-serialcontroller.md) que descreve o controlador serial.</span><span class="sxs-lookup"><span data-stu-id="eb989-128">A [**CIM\_SerialController**](cim-serialcontroller.md) that describes the serial controller.</span></span>

</dd> <dt>

<span data-ttu-id="eb989-129">**Depende**</span><span class="sxs-lookup"><span data-stu-id="eb989-129">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb989-130">Tipo de dados **: \_ LogicalDevice CIM**</span><span class="sxs-lookup"><span data-stu-id="eb989-130">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="eb989-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="eb989-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb989-132">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="eb989-132">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="eb989-133">Um [**\_ LogicalDevice CIM**](cim-logicaldevice.md) que descreve o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="eb989-133">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="eb989-134">**FlowControlInfo**</span><span class="sxs-lookup"><span data-stu-id="eb989-134">**FlowControlInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb989-135">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="eb989-135">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="eb989-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="eb989-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb989-137">Indica o controle de fluxo para dados transmitidos.</span><span class="sxs-lookup"><span data-stu-id="eb989-137">Indicates the flow control for transmitted data.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="eb989-138"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="eb989-138"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="eb989-139"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="eb989-139"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="eb989-140"><span id="None"></span><span id="none"></span><span id="NONE"></span>**Nenhum** (2)</span><span class="sxs-lookup"><span data-stu-id="eb989-140"><span id="None"></span><span id="none"></span><span id="NONE"></span>**None** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="XonXoff"></span><span id="xonxoff"></span><span id="XONXOFF"></span>

<span data-ttu-id="eb989-141"><span id="XonXoff"></span><span id="xonxoff"></span><span id="XONXOFF"></span>**XOnXOff** (3)</span><span class="sxs-lookup"><span data-stu-id="eb989-141"><span id="XonXoff"></span><span id="xonxoff"></span><span id="XONXOFF"></span>**XonXoff** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="RTS_CTS"></span><span id="rts_cts"></span>

<span data-ttu-id="eb989-142"><span id="RTS_CTS"></span><span id="rts_cts"></span>**RTS/CTS** (4)</span><span class="sxs-lookup"><span data-stu-id="eb989-142"><span id="RTS_CTS"></span><span id="rts_cts"></span>**RTS/CTS** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Both_XonXoff_and_RTS_CTS"></span><span id="both_xonxoff_and_rts_cts"></span><span id="BOTH_XONXOFF_AND_RTS_CTS"></span>

<span data-ttu-id="eb989-143"><span id="Both_XonXoff_and_RTS_CTS"></span><span id="both_xonxoff_and_rts_cts"></span><span id="BOTH_XONXOFF_AND_RTS_CTS"></span>**XOnXOff e RTS/CTS** (5)</span><span class="sxs-lookup"><span data-stu-id="eb989-143"><span id="Both_XonXoff_and_RTS_CTS"></span><span id="both_xonxoff_and_rts_cts"></span><span id="BOTH_XONXOFF_AND_RTS_CTS"></span>**Both XonXoff and RTS/CTS** (5)</span></span>


</dt> <dd>

<span data-ttu-id="eb989-144">XonXoff e RTS/CTS</span><span class="sxs-lookup"><span data-stu-id="eb989-144">XonXoff and RTS/CTS</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="eb989-145">**NegotiatedDataWidth**</span><span class="sxs-lookup"><span data-stu-id="eb989-145">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb989-146">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="eb989-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="eb989-147">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="eb989-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb989-148">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span><span class="sxs-lookup"><span data-stu-id="eb989-148">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="eb989-149">Quando várias larguras de dados de barramento ou conexão são possíveis, essa propriedade define a que está em uso entre os dispositivos.</span><span class="sxs-lookup"><span data-stu-id="eb989-149">When several bus or connection-data widths are possible, this property defines the one in use between the devices.</span></span> <span data-ttu-id="eb989-150">A largura dos dados é especificada em bits.</span><span class="sxs-lookup"><span data-stu-id="eb989-150">Data width is specified in bits.</span></span> <span data-ttu-id="eb989-151">Se a largura dos dados não for negociada ou se essas informações não estiverem disponíveis ou importantes para o gerenciamento de dispositivos, a propriedade deverá ser definida como 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="eb989-151">If data width is not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="eb989-152">Essa propriedade é herdada do [**CIM \_ DeviceConnection**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="eb989-152">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb989-153">**NegotiatedSpeed**</span><span class="sxs-lookup"><span data-stu-id="eb989-153">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb989-154">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="eb989-154">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="eb989-155">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="eb989-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb989-156">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits por segundo")</span><span class="sxs-lookup"><span data-stu-id="eb989-156">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="eb989-157">Quando várias velocidades de barramento ou conexão são possíveis, essa propriedade define a que está sendo usada entre os dispositivos.</span><span class="sxs-lookup"><span data-stu-id="eb989-157">When several bus or connection speeds are possible, this property defines the one being used between the devices.</span></span> <span data-ttu-id="eb989-158">A velocidade é especificada em bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="eb989-158">Speed is specified in bits-per-second.</span></span> <span data-ttu-id="eb989-159">Se as velocidades de conexão ou de barramento não forem negociadas ou se essas informações não estiverem disponíveis ou importantes para o gerenciamento de dispositivos, a propriedade deverá ser definida como 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="eb989-159">If connection or bus speeds are not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="eb989-160">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="eb989-160">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="eb989-161">Essa propriedade é herdada do [**CIM \_ DeviceConnection**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="eb989-161">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb989-162">**NumberOfHardResets**</span><span class="sxs-lookup"><span data-stu-id="eb989-162">**NumberOfHardResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb989-163">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="eb989-163">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="eb989-164">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="eb989-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb989-165">Número de redefinições de hardware emitidas pelo controlador.</span><span class="sxs-lookup"><span data-stu-id="eb989-165">Number of hard resets issued by the controller.</span></span> <span data-ttu-id="eb989-166">Uma reinicialização forçada retorna o dispositivo para seu estado de inicialização ou inicialização.</span><span class="sxs-lookup"><span data-stu-id="eb989-166">A hard reset returns the device to its initialization or boot-up state.</span></span> <span data-ttu-id="eb989-167">Todos os dados e informações de estado do dispositivo interno são perdidos.</span><span class="sxs-lookup"><span data-stu-id="eb989-167">All internal device state information and data are lost.</span></span>

<span data-ttu-id="eb989-168">Essa propriedade é herdada do [**CIM \_ ControlledBy**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="eb989-168">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb989-169">**NumberOfSoftResets**</span><span class="sxs-lookup"><span data-stu-id="eb989-169">**NumberOfSoftResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb989-170">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="eb989-170">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="eb989-171">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="eb989-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb989-172">Número de redefinições reversível emitidas pelo controlador.</span><span class="sxs-lookup"><span data-stu-id="eb989-172">Number of soft resets issued by the controller.</span></span> <span data-ttu-id="eb989-173">Uma redefinição reversível não limpa completamente o estado e os dados atuais do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="eb989-173">A soft reset does not completely clear current device state and data.</span></span> <span data-ttu-id="eb989-174">A semântica exata depende do dispositivo e dos protocolos e mecanismos usados para se comunicar com ele.</span><span class="sxs-lookup"><span data-stu-id="eb989-174">Exact semantics are dependent on the device and on the protocols and mechanisms used to communicate to it.</span></span>

<span data-ttu-id="eb989-175">Essa propriedade é herdada do [**CIM \_ ControlledBy**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="eb989-175">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb989-176">**NumberOfStopBits**</span><span class="sxs-lookup"><span data-stu-id="eb989-176">**NumberOfStopBits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb989-177">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="eb989-177">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="eb989-178">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="eb989-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb989-179">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span><span class="sxs-lookup"><span data-stu-id="eb989-179">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="eb989-180">Número de bits de parada a serem transmitidos.</span><span class="sxs-lookup"><span data-stu-id="eb989-180">Number of stop bits to transmit.</span></span>

</dd> <dt>

<span data-ttu-id="eb989-181">**ParityInfo**</span><span class="sxs-lookup"><span data-stu-id="eb989-181">**ParityInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb989-182">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="eb989-182">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="eb989-183">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="eb989-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb989-184">Informações sobre a configuração de paridade para dados transmitidos.</span><span class="sxs-lookup"><span data-stu-id="eb989-184">Information about the parity setting for transmitted data.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="eb989-185">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="eb989-185">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="eb989-186">**Nenhum** (1)</span><span class="sxs-lookup"><span data-stu-id="eb989-186">**None** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Even"></span><span id="even"></span><span id="EVEN"></span>

<span data-ttu-id="eb989-187">**Par** (2)</span><span class="sxs-lookup"><span data-stu-id="eb989-187">**Even** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Odd"></span><span id="odd"></span><span id="ODD"></span>

<span data-ttu-id="eb989-188">**Odd** (3)</span><span class="sxs-lookup"><span data-stu-id="eb989-188">**Odd** (3)</span></span>


<span data-ttu-id="eb989-189"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="eb989-189"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="eb989-190">Comentários</span><span class="sxs-lookup"><span data-stu-id="eb989-190">Remarks</span></span>

<span data-ttu-id="eb989-191">A classe **CIM \_ SerialInterface** é derivada de [**\_ ControlledBy CIM**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="eb989-191">The **CIM\_SerialInterface** class is derived from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<span data-ttu-id="eb989-192">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="eb989-192">WMI does not implement this class.</span></span>

<span data-ttu-id="eb989-193">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="eb989-193">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="eb989-194">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="eb989-194">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb989-195">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eb989-195">Requirements</span></span>



| <span data-ttu-id="eb989-196">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb989-196">Requirement</span></span> | <span data-ttu-id="eb989-197">Valor</span><span class="sxs-lookup"><span data-stu-id="eb989-197">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eb989-198">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eb989-198">Minimum supported client</span></span><br/> | <span data-ttu-id="eb989-199">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="eb989-199">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="eb989-200">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eb989-200">Minimum supported server</span></span><br/> | <span data-ttu-id="eb989-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eb989-201">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="eb989-202">Namespace</span><span class="sxs-lookup"><span data-stu-id="eb989-202">Namespace</span></span><br/>                | <span data-ttu-id="eb989-203">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="eb989-203">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="eb989-204">MOF</span><span class="sxs-lookup"><span data-stu-id="eb989-204">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eb989-205"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="eb989-205"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="eb989-206">DLL</span><span class="sxs-lookup"><span data-stu-id="eb989-206">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eb989-207"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb989-207"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb989-208">Confira também</span><span class="sxs-lookup"><span data-stu-id="eb989-208">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb989-209">**\_CONTROLLEDBY CIM**</span><span class="sxs-lookup"><span data-stu-id="eb989-209">**CIM\_ControlledBy**</span></span>](cim-controlledby.md)
</dt> </dl>

 

