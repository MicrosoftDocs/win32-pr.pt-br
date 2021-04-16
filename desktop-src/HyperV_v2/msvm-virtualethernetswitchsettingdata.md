---
description: Representa a configuração atual de um comutador Ethernet virtual.
ms.assetid: a7c03517-332d-47ce-8e04-c2187bcb2977
title: Classe Msvm_VirtualEthernetSwitchSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchSettingData
- Msvm_VirtualEthernetSwitchSettingData.InstanceID
- Msvm_VirtualEthernetSwitchSettingData.Caption
- Msvm_VirtualEthernetSwitchSettingData.Description
- Msvm_VirtualEthernetSwitchSettingData.ElementName
- Msvm_VirtualEthernetSwitchSettingData.VirtualSystemIdentifier
- Msvm_VirtualEthernetSwitchSettingData.VirtualSystemType
- Msvm_VirtualEthernetSwitchSettingData.Notes
- Msvm_VirtualEthernetSwitchSettingData.CreationTime
- Msvm_VirtualEthernetSwitchSettingData.ConfigurationID
- Msvm_VirtualEthernetSwitchSettingData.ConfigurationDataRoot
- Msvm_VirtualEthernetSwitchSettingData.ConfigurationFile
- Msvm_VirtualEthernetSwitchSettingData.SnapshotDataRoot
- Msvm_VirtualEthernetSwitchSettingData.SuspendDataRoot
- Msvm_VirtualEthernetSwitchSettingData.SwapFileDataRoot
- Msvm_VirtualEthernetSwitchSettingData.LogDataRoot
- Msvm_VirtualEthernetSwitchSettingData.AutomaticStartupAction
- Msvm_VirtualEthernetSwitchSettingData.AutomaticStartupActionDelay
- Msvm_VirtualEthernetSwitchSettingData.AutomaticStartupActionSequenceNumber
- Msvm_VirtualEthernetSwitchSettingData.AutomaticShutdownAction
- Msvm_VirtualEthernetSwitchSettingData.AutomaticRecoveryAction
- Msvm_VirtualEthernetSwitchSettingData.RecoveryFile
- Msvm_VirtualEthernetSwitchSettingData.VLANConnection
- Msvm_VirtualEthernetSwitchSettingData.AssociatedResourcePool
- Msvm_VirtualEthernetSwitchSettingData.MaxNumMACAddress
- Msvm_VirtualEthernetSwitchSettingData.IOVPreferred
- Msvm_VirtualEthernetSwitchSettingData.ExtensionOrder
- Msvm_VirtualEthernetSwitchSettingData.BandwidthReservationMode
- Msvm_VirtualEthernetSwitchSettingData.TeamingEnabled
- Msvm_VirtualEthernetSwitchSettingData.PacketDirectEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3eccbd9dabe853f01c54c78ca651d590afc49f17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758633"
---
# <a name="msvm_virtualethernetswitchsettingdata-class"></a><span data-ttu-id="03d73-103">\_Classe Msvm VirtualEthernetSwitchSettingData</span><span class="sxs-lookup"><span data-stu-id="03d73-103">Msvm\_VirtualEthernetSwitchSettingData class</span></span>

<span data-ttu-id="03d73-104">Representa a configuração atual de um comutador Ethernet virtual.</span><span class="sxs-lookup"><span data-stu-id="03d73-104">Represents the current configuration of a virtual Ethernet switch.</span></span>

<span data-ttu-id="03d73-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="03d73-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="03d73-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="03d73-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualEthernetSwitchSettingData : CIM_VirtualEthernetSwitchSettingData
{
  string   InstanceID = "Microsoft:GUID\DeviceSpecificData";
  string   Caption = "Virtual Ethernet Switch Settings";
  string   Description = "Active settings for the virtual Ethernet switch";
  string   ElementName;
  string   VirtualSystemIdentifier;
  string   VirtualSystemType;
  string   Notes[];
  datetime CreationTime;
  string   ConfigurationID;
  string   ConfigurationDataRoot;
  string   ConfigurationFile;
  string   SnapshotDataRoot;
  string   SuspendDataRoot;
  string   SwapFileDataRoot;
  string   LogDataRoot;
  uint16   AutomaticStartupAction;
  datetime AutomaticStartupActionDelay;
  uint16   AutomaticStartupActionSequenceNumber;
  uint16   AutomaticShutdownAction;
  uint16   AutomaticRecoveryAction;
  string   RecoveryFile;
  string   VLANConnection[];
  string   AssociatedResourcePool[];
  uint32   MaxNumMACAddress;
  boolean  IOVPreferred = FALSE;
  string   ExtensionOrder[];
  uint32   BandwidthReservationMode = 0;
  boolean  TeamingEnabled = FALSE;
  boolean  PacketDirectEnabled = FALSE;
};
```

## <a name="members"></a><span data-ttu-id="03d73-107">Membros</span><span class="sxs-lookup"><span data-stu-id="03d73-107">Members</span></span>

<span data-ttu-id="03d73-108">A classe **Msvm \_ VirtualEthernetSwitchSettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="03d73-108">The **Msvm\_VirtualEthernetSwitchSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="03d73-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="03d73-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="03d73-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="03d73-110">Properties</span></span>

<span data-ttu-id="03d73-111">A classe **Msvm \_ VirtualEthernetSwitchSettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="03d73-111">The **Msvm\_VirtualEthernetSwitchSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="03d73-112">**AssociatedResourcePool**</span><span class="sxs-lookup"><span data-stu-id="03d73-112">**AssociatedResourcePool**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d73-113">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="03d73-113">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="03d73-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="03d73-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03d73-115">Uma lista de pools de recursos de host a serem associados ou que estão atualmente associados ao comutador Ethernet para fins de alocação de conexões Ethernet entre uma máquina virtual e um comutador Ethernet.</span><span class="sxs-lookup"><span data-stu-id="03d73-115">A list of host resource pools to be associated or that are currently associated with the Ethernet switch for the purpose of the allocation of Ethernet connections between a virtual machine and an Ethernet switch.</span></span> <span data-ttu-id="03d73-116">Cada valor deve estar em conformidade com o URI WBEM de produção \_ \_ UntypedInstancePath, conforme definido em DSP0207.</span><span class="sxs-lookup"><span data-stu-id="03d73-116">Each value must conform to the production WBEM\_URI\_UntypedInstancePath as defined in DSP0207.</span></span> <span data-ttu-id="03d73-117">Essa propriedade é herdada do **CIM \_ VirtualEthernetSwitchSettingData**.</span><span class="sxs-lookup"><span data-stu-id="03d73-117">This property is inherited from **CIM\_VirtualEthernetSwitchSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="03d73-118">**AutomaticRecoveryAction**</span><span class="sxs-lookup"><span data-stu-id="03d73-118">**AutomaticRecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d73-119">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="03d73-119">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="03d73-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="03d73-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03d73-121">Ação a ser tomada para a máquina virtual quando o software executado pela máquina virtual falha.</span><span class="sxs-lookup"><span data-stu-id="03d73-121">Action to take for the virtual machine when the software executed by the virtual machine fails.</span></span> <span data-ttu-id="03d73-122">As falhas nesse caso significam uma falha que é detectável pela plataforma do host, como uma condição de estado de espera não passível de interrupção.</span><span class="sxs-lookup"><span data-stu-id="03d73-122">Failures in this case means a failure that is detectable by the host platform, such as a non-interruptible wait state condition.</span></span> <span data-ttu-id="03d73-123">Essa propriedade é herdada de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))e não é usada.</span><span class="sxs-lookup"><span data-stu-id="03d73-123">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="03d73-124">**AutomaticShutdownAction**</span><span class="sxs-lookup"><span data-stu-id="03d73-124">**AutomaticShutdownAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d73-125">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="03d73-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="03d73-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="03d73-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03d73-127">Ação a ser tomada para a máquina virtual quando o host for desligado.</span><span class="sxs-lookup"><span data-stu-id="03d73-127">Action to take for the virtual machine when the host is shut down.</span></span> <span data-ttu-id="03d73-128">Essa propriedade é herdada de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))e não é usada.</span><span class="sxs-lookup"><span data-stu-id="03d73-128">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="03d73-129">**AutomaticStartupAction**</span><span class="sxs-lookup"><span data-stu-id="03d73-129">**AutomaticStartupAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d73-130">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="03d73-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="03d73-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="03d73-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03d73-132">Ação a ser tomada para a máquina virtual quando o host for iniciado.</span><span class="sxs-lookup"><span data-stu-id="03d73-132">Action to take for the virtual machine when the host is started.</span></span> <span data-ttu-id="03d73-133">Essa propriedade é herdada de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))e não é usada.</span><span class="sxs-lookup"><span data-stu-id="03d73-133">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="03d73-134">**AutomaticStartupActionDelay**</span><span class="sxs-lookup"><span data-stu-id="03d73-134">**AutomaticStartupActionDelay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d73-135">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="03d73-135">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="03d73-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="03d73-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03d73-137">O tempo de atraso antes que a máquina virtual seja iniciada automaticamente.</span><span class="sxs-lookup"><span data-stu-id="03d73-137">The delay time before the virtual machine is automatically started up.</span></span> <span data-ttu-id="03d73-138">Essa propriedade é herdada de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))e não é usada.</span><span class="sxs-lookup"><span data-stu-id="03d73-138">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="03d73-139">**AutomaticStartupActionSequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="03d73-139">**AutomaticStartupActionSequenceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d73-140">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="03d73-140">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="03d73-141">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="03d73-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03d73-142">Um número que indica a sequência relativa de ativação da máquina virtual quando o sistema host é iniciado.</span><span class="sxs-lookup"><span data-stu-id="03d73-142">A number that indicates the relative sequence of virtual machine activation when the host system is started.</span></span> <span data-ttu-id="03d73-143">Um número mais baixo indica ativação anterior.</span><span class="sxs-lookup"><span data-stu-id="03d73-143">A lower number indicates earlier activation.</span></span> <span data-ttu-id="03d73-144">Essa propriedade é herdada de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))e não é usada.</span><span class="sxs-lookup"><span data-stu-id="03d73-144">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="03d73-145">**BandwidthReservationMode**</span><span class="sxs-lookup"><span data-stu-id="03d73-145">**BandwidthReservationMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d73-146">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="03d73-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="03d73-147">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="03d73-147">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="03d73-148">O modo de reserva de largura de banda.</span><span class="sxs-lookup"><span data-stu-id="03d73-148">The bandwidth reservation mode.</span></span>

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

<span data-ttu-id="03d73-149">**Padrão** (0)</span><span class="sxs-lookup"><span data-stu-id="03d73-149">**Default** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Weight"></span><span id="weight"></span><span id="WEIGHT"></span>

<span data-ttu-id="03d73-150">**Peso** (1)</span><span class="sxs-lookup"><span data-stu-id="03d73-150">**Weight** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Absolute"></span><span id="absolute"></span><span id="ABSOLUTE"></span>

<span data-ttu-id="03d73-151">**Absoluto** (2)</span><span class="sxs-lookup"><span data-stu-id="03d73-151">**Absolute** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="03d73-152">**Nenhum** (3)</span><span class="sxs-lookup"><span data-stu-id="03d73-152">**None** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="03d73-153">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="03d73-153">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d73-154">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="03d73-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03d73-155">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="03d73-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03d73-156">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="03d73-156">A short description of the object.</span></span> <span data-ttu-id="03d73-157">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "configurações do comutador Ethernet virtual".</span><span class="sxs-lookup"><span data-stu-id="03d73-157">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Virtual Ethernet Switch Settings".</span></span>

</dd> <dt>

<span data-ttu-id="03d73-158">**ConfigurationDataRoot**</span><span class="sxs-lookup"><span data-stu-id="03d73-158">**ConfigurationDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d73-159">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="03d73-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03d73-160">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="03d73-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03d73-161">O caminho de um diretório em que as informações sobre a configuração da máquina virtual são armazenadas.</span><span class="sxs-lookup"><span data-stu-id="03d73-161">The path of a directory where information about the virtual machine configuration is stored.</span></span> <span data-ttu-id="03d73-162">Essa propriedade é herdada de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))e não é usada.</span><span class="sxs-lookup"><span data-stu-id="03d73-162">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="03d73-163">**ConfigurationFile**</span><span class="sxs-lookup"><span data-stu-id="03d73-163">**ConfigurationFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d73-164">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="03d73-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03d73-165">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="03d73-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03d73-166">O caminho relativo e o nome de arquivo de um arquivo em que as informações sobre a configuração da máquina virtual são armazenadas.</span><span class="sxs-lookup"><span data-stu-id="03d73-166">The relative path and file name of a file where information about the virtual machine configuration is stored.</span></span> <span data-ttu-id="03d73-167">Esse caminho é relativo à propriedade **ConfigurationDataRoot** .</span><span class="sxs-lookup"><span data-stu-id="03d73-167">This path is relative to the **ConfigurationDataRoot** property.</span></span> <span data-ttu-id="03d73-168">Essa propriedade é herdada de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))e não é usada.</span><span class="sxs-lookup"><span data-stu-id="03d73-168">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="03d73-169">**ConfigurationID**</span><span class="sxs-lookup"><span data-stu-id="03d73-169">**ConfigurationID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d73-170">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="03d73-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03d73-171">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="03d73-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03d73-172">O identificador exclusivo da configuração da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="03d73-172">The unique identifier of the virtual machine configuration.</span></span> <span data-ttu-id="03d73-173">Essa propriedade é herdada de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))e não é usada.</span><span class="sxs-lookup"><span data-stu-id="03d73-173">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="03d73-174">**CreationTime**</span><span class="sxs-lookup"><span data-stu-id="03d73-174">**CreationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d73-175">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="03d73-175">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="03d73-176">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="03d73-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03d73-177">A data e a hora em que as configurações foram criadas.</span><span class="sxs-lookup"><span data-stu-id="03d73-177">The date and time at which the settings were created.</span></span> <span data-ttu-id="03d73-178">Essa propriedade é herdada do [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="03d73-178">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="03d73-179">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="03d73-179">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d73-180">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="03d73-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03d73-181">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="03d73-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03d73-182">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="03d73-182">A description of the object.</span></span> <span data-ttu-id="03d73-183">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "configurações ativas para o comutador Ethernet virtual".</span><span class="sxs-lookup"><span data-stu-id="03d73-183">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Active settings for the virtual Ethernet switch".</span></span>

</dd> <dt>

<span data-ttu-id="03d73-184">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="03d73-184">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d73-185">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="03d73-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03d73-186">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="03d73-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03d73-187">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="03d73-187">A display name for the object.</span></span> <span data-ttu-id="03d73-188">Essa propriedade é herdada do [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="03d73-188">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="03d73-189">**ExtensionOrder**</span><span class="sxs-lookup"><span data-stu-id="03d73-189">**ExtensionOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d73-190">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="03d73-190">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="03d73-191">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="03d73-191">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="03d73-192">Uma matriz de instâncias inseridas da classe [**Msvm \_ EthernetSwitchExtension**](msvm-ethernetswitchextension.md) que representam as extensões de comutador associadas a essa opção, na ordem em que elas são aplicadas.</span><span class="sxs-lookup"><span data-stu-id="03d73-192">An array of embedded instances of the [**Msvm\_EthernetSwitchExtension**](msvm-ethernetswitchextension.md) class that represent the switch extensions bound to this switch, in the order in which they are applied.</span></span>

</dd> <dt>

<span data-ttu-id="03d73-193">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="03d73-193">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d73-194">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="03d73-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03d73-195">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="03d73-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03d73-196">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="03d73-196">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="03d73-197">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="03d73-197">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="03d73-198">Essa propriedade é herdada do [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)) e é sempre definida como "Microsoft:*GUID* \\ *DeviceSpecificData*".</span><span class="sxs-lookup"><span data-stu-id="03d73-198">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)) and is always set to "Microsoft:*GUID*\\*DeviceSpecificData*".</span></span>

</dd> <dt>

<span data-ttu-id="03d73-199">**IOVPreferred**</span><span class="sxs-lookup"><span data-stu-id="03d73-199">**IOVPreferred**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d73-200">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="03d73-200">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="03d73-201">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="03d73-201">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="03d73-202">Especifica se SR-IOV (virtualização de e/s de raiz única) é preferencial ou não, se disponível, no adaptador subjacente.</span><span class="sxs-lookup"><span data-stu-id="03d73-202">Specifies whether single root IO virtualization (SR-IOV) is preferred or not, if available, on the underlying adapter.</span></span>

</dd> <dt>

<span data-ttu-id="03d73-203">**LogDataRoot**</span><span class="sxs-lookup"><span data-stu-id="03d73-203">**LogDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d73-204">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="03d73-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03d73-205">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="03d73-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03d73-206">O caminho de um diretório em que as informações de log para a máquina virtual são armazenadas.</span><span class="sxs-lookup"><span data-stu-id="03d73-206">The path of a directory where log information for the virtual machine is stored.</span></span> <span data-ttu-id="03d73-207">Essa propriedade é herdada de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))e não é usada.</span><span class="sxs-lookup"><span data-stu-id="03d73-207">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="03d73-208">**MaxNumMACAddress**</span><span class="sxs-lookup"><span data-stu-id="03d73-208">**MaxNumMACAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d73-209">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="03d73-209">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="03d73-210">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="03d73-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03d73-211">Especifica o número máximo de endereços MAC exclusivos que podem ser aprendidos pelo comutador para dar suporte ao aprendizado de endereço MAC, conforme definido no padrão IEEE 802,1.</span><span class="sxs-lookup"><span data-stu-id="03d73-211">Specifies the maximum number of unique MAC addresses that can be learned by the switch to support MAC Address Learning, as defined in the IEEE 802.1 standard.</span></span> <span data-ttu-id="03d73-212">Essa propriedade é herdada do **CIM \_ VirtualEthernetSwitchSettingData**.</span><span class="sxs-lookup"><span data-stu-id="03d73-212">This property is inherited from **CIM\_VirtualEthernetSwitchSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="03d73-213">**Observações**</span><span class="sxs-lookup"><span data-stu-id="03d73-213">**Notes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d73-214">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="03d73-214">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="03d73-215">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="03d73-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03d73-216">Notas fornecidas pelo usuário que estão relacionadas à máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="03d73-216">User supplied notes that are related to the virtual machine.</span></span> <span data-ttu-id="03d73-217">Essa propriedade é herdada do [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="03d73-217">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="03d73-218">**PacketDirectEnabled**</span><span class="sxs-lookup"><span data-stu-id="03d73-218">**PacketDirectEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d73-219">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="03d73-219">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="03d73-220">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="03d73-220">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="03d73-221">Especifica se o PacketDirect deve ser usado, se disponível.</span><span class="sxs-lookup"><span data-stu-id="03d73-221">Specifies whether PacketDirect should be used, if available.</span></span> <span data-ttu-id="03d73-222">O valor padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="03d73-222">The default value is **false**.</span></span>

> [!Note]  
> <span data-ttu-id="03d73-223">Essa propriedade foi adicionada no Windows 10 e no Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="03d73-223">This property was added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="03d73-224">**Recuperação de**</span><span class="sxs-lookup"><span data-stu-id="03d73-224">**RecoveryFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d73-225">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="03d73-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03d73-226">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="03d73-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03d73-227">O caminho completo de um arquivo em que as informações relacionadas à recuperação para a máquina virtual são armazenadas.</span><span class="sxs-lookup"><span data-stu-id="03d73-227">The full path of a file where recovery related information for the virtual machine is stored.</span></span> <span data-ttu-id="03d73-228">Essa propriedade é herdada de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))e não é usada.</span><span class="sxs-lookup"><span data-stu-id="03d73-228">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="03d73-229">**SnapshotDataRoot**</span><span class="sxs-lookup"><span data-stu-id="03d73-229">**SnapshotDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d73-230">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="03d73-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03d73-231">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="03d73-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03d73-232">O caminho de um diretório em que as informações sobre os instantâneos de máquina virtual são armazenadas.</span><span class="sxs-lookup"><span data-stu-id="03d73-232">The path of a directory where information about the virtual machine snapshots is stored.</span></span> <span data-ttu-id="03d73-233">Essa propriedade é herdada de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))e não é usada.</span><span class="sxs-lookup"><span data-stu-id="03d73-233">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="03d73-234">**SuspendDataRoot**</span><span class="sxs-lookup"><span data-stu-id="03d73-234">**SuspendDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d73-235">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="03d73-235">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03d73-236">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="03d73-236">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03d73-237">O caminho de um diretório em que informações sobre as informações relacionadas à suspensão da máquina virtual são armazenadas.</span><span class="sxs-lookup"><span data-stu-id="03d73-237">The path of a directory where information about the virtual machine suspend-related information is stored.</span></span> <span data-ttu-id="03d73-238">Essa propriedade é herdada de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))e não é usada.</span><span class="sxs-lookup"><span data-stu-id="03d73-238">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="03d73-239">**SwapFileDataRoot**</span><span class="sxs-lookup"><span data-stu-id="03d73-239">**SwapFileDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d73-240">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="03d73-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03d73-241">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="03d73-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03d73-242">O caminho de um diretório em que os arquivos de permuta para a máquina virtual são armazenados.</span><span class="sxs-lookup"><span data-stu-id="03d73-242">The path of a directory where swap files for the virtual machine are stored.</span></span> <span data-ttu-id="03d73-243">Essa propriedade é herdada de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))e não é usada.</span><span class="sxs-lookup"><span data-stu-id="03d73-243">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="03d73-244">**TeamingEnabled**</span><span class="sxs-lookup"><span data-stu-id="03d73-244">**TeamingEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d73-245">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="03d73-245">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="03d73-246">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="03d73-246">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="03d73-247">Especifica se o agrupamento NIC deve ser usado.</span><span class="sxs-lookup"><span data-stu-id="03d73-247">Specifies whether NIC Teaming should be used.</span></span> <span data-ttu-id="03d73-248">O valor padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="03d73-248">The default value is **false**.</span></span>

> [!Note]  
> <span data-ttu-id="03d73-249">Essa propriedade foi adicionada ao Windows 10 e ao Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="03d73-249">This property was added inWindows 10 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="03d73-250">**VirtualSystemIdentifier**</span><span class="sxs-lookup"><span data-stu-id="03d73-250">**VirtualSystemIdentifier**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d73-251">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="03d73-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03d73-252">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="03d73-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03d73-253">O nome do objeto [**de \_ sistema**](/windows/desktop/CIMWin32Prov/cim-computersystem) de dados CIM ao qual esses dados de configuração pertencem.</span><span class="sxs-lookup"><span data-stu-id="03d73-253">The name of the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) object to which this setting data belongs.</span></span> <span data-ttu-id="03d73-254">Essa propriedade é uma substituição do [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="03d73-254">This property is an override from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="03d73-255">**VirtualSystemType**</span><span class="sxs-lookup"><span data-stu-id="03d73-255">**VirtualSystemType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d73-256">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="03d73-256">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03d73-257">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="03d73-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03d73-258">Especifica o tipo de máquina virtual que os dados de configuração representam.</span><span class="sxs-lookup"><span data-stu-id="03d73-258">Specifies the type of virtual machine the setting data represents.</span></span> <span data-ttu-id="03d73-259">Essa propriedade é herdada do [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="03d73-259">This property is inherited from the [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="03d73-260">**VLANConnection**</span><span class="sxs-lookup"><span data-stu-id="03d73-260">**VLANConnection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d73-261">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="03d73-261">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="03d73-262">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="03d73-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03d73-263">Uma lista de identificadores de VLAN que esse comutador pode acessar.</span><span class="sxs-lookup"><span data-stu-id="03d73-263">A list of VLAN identifiers that this switch can access.</span></span> <span data-ttu-id="03d73-264">Essa propriedade é herdada do **CIM \_ VirtualEthernetSwitchSettingData**.</span><span class="sxs-lookup"><span data-stu-id="03d73-264">This property is inherited from **CIM\_VirtualEthernetSwitchSettingData**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="03d73-265">Requisitos</span><span class="sxs-lookup"><span data-stu-id="03d73-265">Requirements</span></span>



| <span data-ttu-id="03d73-266">Requisito</span><span class="sxs-lookup"><span data-stu-id="03d73-266">Requirement</span></span> | <span data-ttu-id="03d73-267">Valor</span><span class="sxs-lookup"><span data-stu-id="03d73-267">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03d73-268">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="03d73-268">Minimum supported client</span></span><br/> | <span data-ttu-id="03d73-269">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="03d73-269">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="03d73-270">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="03d73-270">Minimum supported server</span></span><br/> | <span data-ttu-id="03d73-271">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="03d73-271">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="03d73-272">Namespace</span><span class="sxs-lookup"><span data-stu-id="03d73-272">Namespace</span></span><br/>                | <span data-ttu-id="03d73-273">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="03d73-273">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="03d73-274">MOF</span><span class="sxs-lookup"><span data-stu-id="03d73-274">MOF</span></span><br/>                      | <dl> <span data-ttu-id="03d73-275"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="03d73-275"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="03d73-276">DLL</span><span class="sxs-lookup"><span data-stu-id="03d73-276">DLL</span></span><br/>                      | <dl> <span data-ttu-id="03d73-277"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="03d73-277"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

