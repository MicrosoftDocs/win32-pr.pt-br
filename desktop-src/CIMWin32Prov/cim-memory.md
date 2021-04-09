---
description: A \_ classe de memória CIM representa os recursos e o gerenciamento de dispositivos lógicos relacionados à memória.
ms.assetid: ddc72aad-5687-4bc1-b402-e27b27eca9be
ms.tgt_platform: multiple
title: Classe CIM_Memory (provedores WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Memory
- CIM_Memory.Caption
- CIM_Memory.Description
- CIM_Memory.InstallDate
- CIM_Memory.Name
- CIM_Memory.Status
- CIM_Memory.Availability
- CIM_Memory.ConfigManagerErrorCode
- CIM_Memory.ConfigManagerUserConfig
- CIM_Memory.CreationClassName
- CIM_Memory.DeviceID
- CIM_Memory.PowerManagementCapabilities
- CIM_Memory.ErrorCleared
- CIM_Memory.ErrorDescription
- CIM_Memory.LastErrorCode
- CIM_Memory.PNPDeviceID
- CIM_Memory.PowerManagementSupported
- CIM_Memory.StatusInfo
- CIM_Memory.SystemCreationClassName
- CIM_Memory.SystemName
- CIM_Memory.Access
- CIM_Memory.BlockSize
- CIM_Memory.NumberOfBlocks
- CIM_Memory.Purpose
- CIM_Memory.ErrorMethodology
- CIM_Memory.AdditionalErrorData
- CIM_Memory.CorrectableError
- CIM_Memory.EndingAddress
- CIM_Memory.ErrorAccess
- CIM_Memory.ErrorAddress
- CIM_Memory.ErrorData
- CIM_Memory.ErrorDataOrder
- CIM_Memory.ErrorInfo
- CIM_Memory.ErrorResolution
- CIM_Memory.ErrorTime
- CIM_Memory.ErrorTransferSize
- CIM_Memory.OtherErrorDescription
- CIM_Memory.StartingAddress
- CIM_Memory.SystemLevelAddress
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 35fbb8467337da1ceab044a42533a6ca8628cf63
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089385"
---
# <a name="cim_memory-class-cimwin32-wmi-providers"></a><span data-ttu-id="756b9-103">Classe CIM_Memory (provedores WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="756b9-103">CIM_Memory class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="756b9-104">A classe de **\_ memória CIM** representa os recursos e o gerenciamento de dispositivos lógicos relacionados à memória.</span><span class="sxs-lookup"><span data-stu-id="756b9-104">The **CIM\_Memory** class represents the capabilities and management of memory-related logical devices.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="756b9-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="756b9-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="756b9-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="756b9-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="756b9-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="756b9-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="756b9-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="756b9-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="756b9-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="756b9-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B64-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Memory : CIM_StorageExtent
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  uint16   Availability;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   DeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  ErrorCleared;
  string   ErrorDescription;
  uint32   LastErrorCode;
  string   PNPDeviceID;
  boolean  PowerManagementSupported;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  uint16   Access;
  uint64   BlockSize;
  uint64   NumberOfBlocks;
  string   Purpose;
  string   ErrorMethodology;
  uint8    AdditionalErrorData[];
  boolean  CorrectableError;
  uint64   EndingAddress;
  uint16   ErrorAccess;
  uint64   ErrorAddress;
  uint8    ErrorData[];
  uint16   ErrorDataOrder;
  uint16   ErrorInfo;
  uint64   ErrorResolution;
  datetime ErrorTime;
  uint32   ErrorTransferSize;
  string   OtherErrorDescription;
  uint64   StartingAddress;
  boolean  SystemLevelAddress;
};
```

## <a name="members"></a><span data-ttu-id="756b9-110">Membros</span><span class="sxs-lookup"><span data-stu-id="756b9-110">Members</span></span>

<span data-ttu-id="756b9-111">A classe de **\_ memória CIM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="756b9-111">The **CIM\_Memory** class has these types of members:</span></span>

-   [<span data-ttu-id="756b9-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="756b9-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="756b9-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="756b9-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="756b9-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="756b9-114">Methods</span></span>

<span data-ttu-id="756b9-115">A classe de **\_ memória CIM** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="756b9-115">The **CIM\_Memory** class has these methods.</span></span>



| <span data-ttu-id="756b9-116">Método</span><span class="sxs-lookup"><span data-stu-id="756b9-116">Method</span></span>                                                            | <span data-ttu-id="756b9-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="756b9-117">Description</span></span>                                                                                                                              |
|:------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="756b9-118">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="756b9-118">**Reset**</span></span>](reset-method-in-class-cim-memory.md)                 | <span data-ttu-id="756b9-119">Solicita uma redefinição do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="756b9-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="756b9-120">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="756b9-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="756b9-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="756b9-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-memory.md) | <span data-ttu-id="756b9-122">Define o estado de energia desejado para um dispositivo lógico e quando um dispositivo deve ser colocado nesse estado.</span><span class="sxs-lookup"><span data-stu-id="756b9-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="756b9-123">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="756b9-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="756b9-124">Propriedades</span><span class="sxs-lookup"><span data-stu-id="756b9-124">Properties</span></span>

<span data-ttu-id="756b9-125">A classe de **\_ memória CIM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="756b9-125">The **CIM\_Memory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="756b9-126">**Acesso**</span><span class="sxs-lookup"><span data-stu-id="756b9-126">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="756b9-127">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="756b9-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="756b9-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="756b9-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="756b9-129">Descreve as propriedades de leitura/gravação da mídia.</span><span class="sxs-lookup"><span data-stu-id="756b9-129">Describes the read/write properties of the media.</span></span>

<span data-ttu-id="756b9-130">Essa propriedade é herdada do [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="756b9-130">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="756b9-131">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="756b9-131">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="756b9-132">**Legível** (1)</span><span class="sxs-lookup"><span data-stu-id="756b9-132">**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="756b9-133">**Gravável** (2)</span><span class="sxs-lookup"><span data-stu-id="756b9-133">**Writeable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="756b9-134">**Suporte de leitura/gravação** (3)</span><span class="sxs-lookup"><span data-stu-id="756b9-134">**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="756b9-135">**Gravar uma vez** (4)</span><span class="sxs-lookup"><span data-stu-id="756b9-135">**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="756b9-136">**AdditionalErrorData**</span><span class="sxs-lookup"><span data-stu-id="756b9-136">**AdditionalErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="756b9-137">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="756b9-137">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="756b9-138">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="756b9-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="756b9-139">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memória DMTF \| 2,18 "," MIF. \|Matriz de memória física da DMTF \| 1,13 "), [**máx**](/windows/desktop/WmiSdk/standard-qualifiers) . (64)</span><span class="sxs-lookup"><span data-stu-id="756b9-139">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.18", "MIF.DMTF\|Physical Memory Array\|001.13"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="756b9-140">Matriz de octetos que contém informações de erro adicionais.</span><span class="sxs-lookup"><span data-stu-id="756b9-140">Array of octets that hold additional error information.</span></span> <span data-ttu-id="756b9-141">Um exemplo é a verificação de erros e a síndrome de correção (ECC) ou o retorno dos bits de verificação se uma metodologia de erro baseada em CRC for usada.</span><span class="sxs-lookup"><span data-stu-id="756b9-141">An example is Error Checking and Correcting (ECC) Syndrome, or the return of the check bits if a CRC-based error methodology is used.</span></span> <span data-ttu-id="756b9-142">No último caso, se um erro de bit único for reconhecido e o algoritmo CRC for conhecido, o bit exato que falhou poderá ser determinado.</span><span class="sxs-lookup"><span data-stu-id="756b9-142">In the latter case, if a single-bit error is recognized and the CRC algorithm is known, the exact bit that failed can be determined.</span></span> <span data-ttu-id="756b9-143">Esse tipo de dados (síndrome de ECC, dados de verificação de bits ou de bits de paridade ou outras informações fornecidas pelo fornecedor) está incluído neste campo.</span><span class="sxs-lookup"><span data-stu-id="756b9-143">This type of data (ECC Syndrome, check-bit or parity-bit data, or other vendor supplied information) is included in this field.</span></span> <span data-ttu-id="756b9-144">Se a propriedade **errorInfo** for igual a 3 ("OK"), essa propriedade não terá significado.</span><span class="sxs-lookup"><span data-stu-id="756b9-144">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="756b9-145">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="756b9-145">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="756b9-146">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="756b9-146">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="756b9-147">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="756b9-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="756b9-148">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="756b9-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="756b9-149">Disponibilidade e status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="756b9-149">Availability and status of the device.</span></span>

<span data-ttu-id="756b9-150">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="756b9-150">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="756b9-151"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="756b9-151"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="756b9-152"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="756b9-152"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="756b9-153"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Execução/energia completa** (3)</span><span class="sxs-lookup"><span data-stu-id="756b9-153"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="756b9-154"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Aviso** (4)</span><span class="sxs-lookup"><span data-stu-id="756b9-154"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="756b9-155"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (5)</span><span class="sxs-lookup"><span data-stu-id="756b9-155"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="756b9-156"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (6)</span><span class="sxs-lookup"><span data-stu-id="756b9-156"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="756b9-157"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desligar (7** )</span><span class="sxs-lookup"><span data-stu-id="756b9-157"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="756b9-158"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off line** (8)</span><span class="sxs-lookup"><span data-stu-id="756b9-158"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="756b9-159"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fora do imposto** (9)</span><span class="sxs-lookup"><span data-stu-id="756b9-159"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="756b9-160"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="756b9-160"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="756b9-161"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Não instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="756b9-161"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="756b9-162"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erro de instalação** (12)</span><span class="sxs-lookup"><span data-stu-id="756b9-162"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="756b9-163"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Economia **de energia-desconhecido** (13)</span><span class="sxs-lookup"><span data-stu-id="756b9-163"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="756b9-164">O dispositivo é conhecido por estar em um modo de economia de energia, mas seu status exato é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="756b9-164">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="756b9-165"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Economia **de energia-modo de baixa energia** (14)</span><span class="sxs-lookup"><span data-stu-id="756b9-165"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="756b9-166">O dispositivo está em um estado de economia de energia, mas ainda está funcionando e pode exibir o desempenho degradado.</span><span class="sxs-lookup"><span data-stu-id="756b9-166">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="756b9-167"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save-em espera** (15)</span><span class="sxs-lookup"><span data-stu-id="756b9-167"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="756b9-168">O dispositivo não está funcionando, mas pode ser levado a uma potência completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="756b9-168">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="756b9-169"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energia** (16)</span><span class="sxs-lookup"><span data-stu-id="756b9-169"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="756b9-170"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Economia **de energia-aviso** (17)</span><span class="sxs-lookup"><span data-stu-id="756b9-170"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="756b9-171">O dispositivo está em um estado de aviso, embora também esteja em um modo de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="756b9-171">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="756b9-172"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>Em **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="756b9-172"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="756b9-173">O dispositivo está em pausa.</span><span class="sxs-lookup"><span data-stu-id="756b9-173">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="756b9-174"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Não pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="756b9-174"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="756b9-175">O dispositivo não está pronto.</span><span class="sxs-lookup"><span data-stu-id="756b9-175">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="756b9-176"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Não configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="756b9-176"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="756b9-177">O dispositivo não está configurado.</span><span class="sxs-lookup"><span data-stu-id="756b9-177">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="756b9-178"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Desativado** (21)</span><span class="sxs-lookup"><span data-stu-id="756b9-178"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="756b9-179">O dispositivo está silencioso.</span><span class="sxs-lookup"><span data-stu-id="756b9-179">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="756b9-180">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="756b9-180">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="756b9-181">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="756b9-181">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="756b9-182">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="756b9-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="756b9-183">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrStorageAllocationUnits "), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="756b9-183">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="756b9-184">Tamanho, em bytes, dos blocos que formam a extensão de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="756b9-184">Size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="756b9-185">Se o tamanho do bloco variável, o tamanho máximo do bloco, em bytes, deverá ser especificado.</span><span class="sxs-lookup"><span data-stu-id="756b9-185">If variable block size, then the maximum block size, in bytes, should be specified.</span></span> <span data-ttu-id="756b9-186">Se o tamanho do bloco for desconhecido ou se um conceito de bloco não for válido (por exemplo, para extensões de agregação, memória ou discos lógicos), insira um 1 (um).</span><span class="sxs-lookup"><span data-stu-id="756b9-186">If the block size is unknown, or if a block concept is not valid (for example, for aggregate extents, memory, or logical disks), enter a 1 (one).</span></span>

<span data-ttu-id="756b9-187">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="756b9-187">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="756b9-188">Essa propriedade é herdada do [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="756b9-188">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="756b9-189">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="756b9-189">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="756b9-190">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="756b9-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="756b9-191">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="756b9-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="756b9-192">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="756b9-192">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="756b9-193">Uma breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="756b9-193">A short textual description of the object.</span></span>

<span data-ttu-id="756b9-194">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="756b9-194">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="756b9-195">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="756b9-195">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="756b9-196">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="756b9-196">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="756b9-197">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="756b9-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="756b9-198">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="756b9-198">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="756b9-199">Código de erro do Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="756b9-199">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="756b9-200">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="756b9-200">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="756b9-201">**Este dispositivo está funcionando corretamente.**</span><span class="sxs-lookup"><span data-stu-id="756b9-201">**This device is working properly.**</span></span> <span data-ttu-id="756b9-202"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="756b9-202">(0)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="756b9-203">**Este dispositivo não está configurado corretamente.**</span><span class="sxs-lookup"><span data-stu-id="756b9-203">**This device is not configured correctly.**</span></span> <span data-ttu-id="756b9-204">(1)</span><span class="sxs-lookup"><span data-stu-id="756b9-204">(1)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="756b9-205">**O Windows não pode carregar o driver para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="756b9-205">**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="756b9-206">(2)</span><span class="sxs-lookup"><span data-stu-id="756b9-206">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="756b9-207">**O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.**</span><span class="sxs-lookup"><span data-stu-id="756b9-207">**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="756b9-208">(3)</span><span class="sxs-lookup"><span data-stu-id="756b9-208">(3)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="756b9-209">**Este dispositivo não está funcionando corretamente. Um de seus drivers ou seu registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="756b9-209">**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="756b9-210">(4)</span><span class="sxs-lookup"><span data-stu-id="756b9-210">(4)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="756b9-211">**O driver para este dispositivo precisa de um recurso que o Windows não possa gerenciar.**</span><span class="sxs-lookup"><span data-stu-id="756b9-211">**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="756b9-212">(5)</span><span class="sxs-lookup"><span data-stu-id="756b9-212">(5)</span></span>


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="756b9-213">**A configuração de inicialização para este dispositivo está em conflito com outros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="756b9-213">**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="756b9-214"> (6)</span><span class="sxs-lookup"><span data-stu-id="756b9-214">(6)</span></span>


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="756b9-215">**Não é possível filtrar.**</span><span class="sxs-lookup"><span data-stu-id="756b9-215">**Cannot filter.**</span></span> <span data-ttu-id="756b9-216">(7)</span><span class="sxs-lookup"><span data-stu-id="756b9-216">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="756b9-217">**O carregador de driver para o dispositivo está ausente.**</span><span class="sxs-lookup"><span data-stu-id="756b9-217">**The driver loader for the device is missing.**</span></span> <span data-ttu-id="756b9-218">(8)</span><span class="sxs-lookup"><span data-stu-id="756b9-218">(8)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="756b9-219">**Este dispositivo não está funcionando corretamente porque o firmware de controle está relatando os recursos para o dispositivo incorretamente.**</span><span class="sxs-lookup"><span data-stu-id="756b9-219">**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="756b9-220">(9)</span><span class="sxs-lookup"><span data-stu-id="756b9-220">(9)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="756b9-221">**Este dispositivo não pode ser iniciado.**</span><span class="sxs-lookup"><span data-stu-id="756b9-221">**This device cannot start.**</span></span> <span data-ttu-id="756b9-222">(10)</span><span class="sxs-lookup"><span data-stu-id="756b9-222">(10)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="756b9-223">**Este dispositivo falhou.**</span><span class="sxs-lookup"><span data-stu-id="756b9-223">**This device failed.**</span></span> <span data-ttu-id="756b9-224">(11)</span><span class="sxs-lookup"><span data-stu-id="756b9-224">(11)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="756b9-225">**Este dispositivo não pode encontrar recursos livres suficientes que podem ser usados.**</span><span class="sxs-lookup"><span data-stu-id="756b9-225">**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="756b9-226">12</span><span class="sxs-lookup"><span data-stu-id="756b9-226">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="756b9-227">**O Windows não pode verificar os recursos deste dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="756b9-227">**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="756b9-228">(13)</span><span class="sxs-lookup"><span data-stu-id="756b9-228">(13)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="756b9-229">**Este dispositivo não funcionará corretamente até que você reinicie o computador.**</span><span class="sxs-lookup"><span data-stu-id="756b9-229">**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="756b9-230">(14)</span><span class="sxs-lookup"><span data-stu-id="756b9-230">(14)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="756b9-231">**Este dispositivo não está funcionando corretamente porque provavelmente há um problema de nova enumeração.**</span><span class="sxs-lookup"><span data-stu-id="756b9-231">**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="756b9-232">(15)</span><span class="sxs-lookup"><span data-stu-id="756b9-232">(15)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="756b9-233">**O Windows não pode identificar todos os recursos que este dispositivo usa.**</span><span class="sxs-lookup"><span data-stu-id="756b9-233">**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="756b9-234">(16)</span><span class="sxs-lookup"><span data-stu-id="756b9-234">(16)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="756b9-235">**Este dispositivo está solicitando um tipo de recurso desconhecido.**</span><span class="sxs-lookup"><span data-stu-id="756b9-235">**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="756b9-236">(17)</span><span class="sxs-lookup"><span data-stu-id="756b9-236">(17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="756b9-237">**Reinstale os drivers para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="756b9-237">**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="756b9-238">(18)</span><span class="sxs-lookup"><span data-stu-id="756b9-238">(18)</span></span>


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="756b9-239">**Falha ao usar o carregador VxD.**</span><span class="sxs-lookup"><span data-stu-id="756b9-239">**Failure using the VxD loader.**</span></span> <span data-ttu-id="756b9-240">(19)</span><span class="sxs-lookup"><span data-stu-id="756b9-240">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="756b9-241">**O registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="756b9-241">**Your registry might be corrupted.**</span></span> <span data-ttu-id="756b9-242">(20)</span><span class="sxs-lookup"><span data-stu-id="756b9-242">(20)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="756b9-243">**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware. O Windows está removendo este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="756b9-243">**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="756b9-244">(21)</span><span class="sxs-lookup"><span data-stu-id="756b9-244">(21)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="756b9-245">**Este dispositivo está desabilitado.**</span><span class="sxs-lookup"><span data-stu-id="756b9-245">**This device is disabled.**</span></span> <span data-ttu-id="756b9-246">(22)</span><span class="sxs-lookup"><span data-stu-id="756b9-246">(22)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="756b9-247">**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware.**</span><span class="sxs-lookup"><span data-stu-id="756b9-247">**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="756b9-248">(23)</span><span class="sxs-lookup"><span data-stu-id="756b9-248">(23)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="756b9-249">**Este dispositivo não está presente, não está funcionando corretamente ou não tem todos os drivers instalados.**</span><span class="sxs-lookup"><span data-stu-id="756b9-249">**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="756b9-250">(24)</span><span class="sxs-lookup"><span data-stu-id="756b9-250">(24)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="756b9-251">**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="756b9-251">**Windows is still setting up this device.**</span></span> <span data-ttu-id="756b9-252">(25)</span><span class="sxs-lookup"><span data-stu-id="756b9-252">(25)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="756b9-253">**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="756b9-253">**Windows is still setting up this device.**</span></span> <span data-ttu-id="756b9-254">(26)</span><span class="sxs-lookup"><span data-stu-id="756b9-254">(26)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="756b9-255">**Este dispositivo não tem uma configuração de log válida.**</span><span class="sxs-lookup"><span data-stu-id="756b9-255">**This device does not have valid log configuration.**</span></span> <span data-ttu-id="756b9-256">(27)</span><span class="sxs-lookup"><span data-stu-id="756b9-256">(27)</span></span>


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="756b9-257">**Os drivers para este dispositivo não estão instalados.**</span><span class="sxs-lookup"><span data-stu-id="756b9-257">**The drivers for this device are not installed.**</span></span> <span data-ttu-id="756b9-258">(28)</span><span class="sxs-lookup"><span data-stu-id="756b9-258">(28)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="756b9-259">**Este dispositivo está desabilitado porque o firmware do dispositivo não forneceu os recursos necessários.**</span><span class="sxs-lookup"><span data-stu-id="756b9-259">**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="756b9-260">(29)</span><span class="sxs-lookup"><span data-stu-id="756b9-260">(29)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="756b9-261">**Este dispositivo está usando um recurso de IRQ (solicitação de interrupção) que outro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="756b9-261">**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="756b9-262">(30)</span><span class="sxs-lookup"><span data-stu-id="756b9-262">(30)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="756b9-263">**Este dispositivo não está funcionando corretamente porque o Windows não pode carregar os drivers necessários para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="756b9-263">**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="756b9-264">(31)</span><span class="sxs-lookup"><span data-stu-id="756b9-264">(31)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="756b9-265">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="756b9-265">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="756b9-266">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="756b9-266">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="756b9-267">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="756b9-267">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="756b9-268">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="756b9-268">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="756b9-269">Se for **true**, o dispositivo estará usando uma configuração definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="756b9-269">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="756b9-270">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="756b9-270">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="756b9-271">**CorrectableError**</span><span class="sxs-lookup"><span data-stu-id="756b9-271">**CorrectableError**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="756b9-272">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="756b9-272">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="756b9-273">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="756b9-273">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="756b9-274">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memória DMTF \| 2,12 "," MIF. \|Matriz de memória física da DMTF \| 1,8 ")</span><span class="sxs-lookup"><span data-stu-id="756b9-274">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.12", "MIF.DMTF\|Physical Memory Array\|001.8")</span></span>
</dt> </dl>

<span data-ttu-id="756b9-275">Se **for true**, o erro mais recente era corrigível.</span><span class="sxs-lookup"><span data-stu-id="756b9-275">If **TRUE**, the most recent error was correctable.</span></span> <span data-ttu-id="756b9-276">Se a propriedade **errorInfo** for igual a 3 ("OK"), essa propriedade não terá significado.</span><span class="sxs-lookup"><span data-stu-id="756b9-276">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="756b9-277">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="756b9-277">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="756b9-278">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="756b9-278">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="756b9-279">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="756b9-279">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="756b9-280">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="756b9-280">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="756b9-281">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="756b9-281">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="756b9-282">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="756b9-282">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="756b9-283">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="756b9-283">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="756b9-284">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="756b9-284">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="756b9-285">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="756b9-285">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="756b9-286">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="756b9-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="756b9-287">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="756b9-287">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="756b9-288">Uma descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="756b9-288">A textual description of the object.</span></span>

<span data-ttu-id="756b9-289">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="756b9-289">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="756b9-290">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="756b9-290">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="756b9-291">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="756b9-291">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="756b9-292">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="756b9-292">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="756b9-293">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="756b9-293">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="756b9-294">Endereço ou outras informações de identificação para nomear exclusivamente o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="756b9-294">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="756b9-295">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="756b9-295">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="756b9-296">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="756b9-296">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="756b9-297">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="756b9-297">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="756b9-298">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="756b9-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="756b9-299">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Os \| endereços mapeados da matriz de memória DMTF \| 1,4 "," MIF. \|Endereços mapeados do dispositivo \| de memória DMTF 1,5 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" kilobytes ")</span><span class="sxs-lookup"><span data-stu-id="756b9-299">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Array Mapped Addresses\|001.4", "MIF.DMTF\|Memory Device Mapped Addresses\|001.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="756b9-300">Endereço final referenciado por um aplicativo ou sistema operacional e mapeado por um controlador de memória para este objeto de memória.</span><span class="sxs-lookup"><span data-stu-id="756b9-300">Ending address referenced by an application or operating system and mapped by a memory controller for this memory object.</span></span> <span data-ttu-id="756b9-301">O endereço final é especificado em kilobytes.</span><span class="sxs-lookup"><span data-stu-id="756b9-301">The ending address is specified in kilobytes.</span></span>

<span data-ttu-id="756b9-302">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="756b9-302">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="756b9-303">**ErrorAccess**</span><span class="sxs-lookup"><span data-stu-id="756b9-303">**ErrorAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="756b9-304">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="756b9-304">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="756b9-305">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="756b9-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="756b9-306">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memória DMTF \| 2,15 "," MIF. \|Matriz de memória física da DMTF \| 1,10 ")</span><span class="sxs-lookup"><span data-stu-id="756b9-306">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.15", "MIF.DMTF\|Physical Memory Array\|001.10")</span></span>
</dt> </dl>

<span data-ttu-id="756b9-307">Operação de acesso à memória que causou o último erro.</span><span class="sxs-lookup"><span data-stu-id="756b9-307">Memory access operation that caused the last error.</span></span> <span data-ttu-id="756b9-308">O tipo de erro é descrito pela propriedade **errorInfo** .</span><span class="sxs-lookup"><span data-stu-id="756b9-308">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="756b9-309">Se a propriedade **errorInfo** for igual a 3 ("OK"), essa propriedade não terá significado.</span><span class="sxs-lookup"><span data-stu-id="756b9-309">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="756b9-310">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="756b9-310">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="756b9-311">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="756b9-311">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="756b9-312">**Leitura** (3)</span><span class="sxs-lookup"><span data-stu-id="756b9-312">**Read** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

<span data-ttu-id="756b9-313">**Gravação** (4)</span><span class="sxs-lookup"><span data-stu-id="756b9-313">**Write** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>

<span data-ttu-id="756b9-314">**Gravação parcial** (5)</span><span class="sxs-lookup"><span data-stu-id="756b9-314">**Partial Write** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="756b9-315">**ErrorAddress**</span><span class="sxs-lookup"><span data-stu-id="756b9-315">**ErrorAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="756b9-316">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="756b9-316">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="756b9-317">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="756b9-317">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="756b9-318">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memória DMTF \| 2,19 "," MIF. \|Dispositivo de memória DMTF \| 2,20 "," MIF. \|Matriz de memória física da DMTF \| 1,14 ")</span><span class="sxs-lookup"><span data-stu-id="756b9-318">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.19", "MIF.DMTF\|Memory Device\|002.20", "MIF.DMTF\|Physical Memory Array\|001.14")</span></span>
</dt> </dl>

<span data-ttu-id="756b9-319">Endereço do último erro de memória.</span><span class="sxs-lookup"><span data-stu-id="756b9-319">Address of the last memory error.</span></span> <span data-ttu-id="756b9-320">O tipo de erro é descrito pela propriedade **errorInfo** .</span><span class="sxs-lookup"><span data-stu-id="756b9-320">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="756b9-321">Se a propriedade **errorInfo** for igual a 3 ("OK"), essa propriedade não terá significado.</span><span class="sxs-lookup"><span data-stu-id="756b9-321">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="756b9-322">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="756b9-322">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="756b9-323">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="756b9-323">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="756b9-324">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="756b9-324">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="756b9-325">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="756b9-325">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="756b9-326">Se **for true**, o erro relatado na propriedade **LastErrorCode** será apagado agora.</span><span class="sxs-lookup"><span data-stu-id="756b9-326">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="756b9-327">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="756b9-327">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="756b9-328">**ErrorData**</span><span class="sxs-lookup"><span data-stu-id="756b9-328">**ErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="756b9-329">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="756b9-329">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="756b9-330">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="756b9-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="756b9-331">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memória DMTF \| 2,17 "," MIF. \|Matriz de memória física da DMTF \| 1,12 "), [**máx**](/windows/desktop/WmiSdk/standard-qualifiers) . (64)</span><span class="sxs-lookup"><span data-stu-id="756b9-331">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.17", "MIF.DMTF\|Physical Memory Array\|001.12"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="756b9-332">Dados capturados durante o último acesso de memória incorreto.</span><span class="sxs-lookup"><span data-stu-id="756b9-332">Data captured during the last erroneous memory access.</span></span> <span data-ttu-id="756b9-333">Os dados ocupam os primeiros *n* octetos da matriz que são necessários para manter o número de bits especificado pela propriedade **ErrorTransferSize** .</span><span class="sxs-lookup"><span data-stu-id="756b9-333">The data occupies the first *n* octets of the array that are necessary to hold the number of bits specified by the **ErrorTransferSize** property.</span></span> <span data-ttu-id="756b9-334">Se **ErrorTransferSize** for 0, essa propriedade não terá significado.</span><span class="sxs-lookup"><span data-stu-id="756b9-334">If **ErrorTransferSize** is 0, then this property has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="756b9-335">**ErrorDataOrder**</span><span class="sxs-lookup"><span data-stu-id="756b9-335">**ErrorDataOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="756b9-336">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="756b9-336">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="756b9-337">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="756b9-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="756b9-338">Ordem dos dados armazenados na propriedade **ErrorData** .</span><span class="sxs-lookup"><span data-stu-id="756b9-338">Order of data stored in the **ErrorData** property.</span></span> <span data-ttu-id="756b9-339">Se **ErrorTransferSize** for 0, essa propriedade não terá significado.</span><span class="sxs-lookup"><span data-stu-id="756b9-339">If **ErrorTransferSize** is 0, then this property has no meaning.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="756b9-340"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="756b9-340"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="756b9-341">Desconhecido.</span><span class="sxs-lookup"><span data-stu-id="756b9-341">Unknown.</span></span>

</dd> <dt>

<span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="756b9-342"><span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>**Byte menos significativo primeiro** (1)</span><span class="sxs-lookup"><span data-stu-id="756b9-342"><span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>**Least Significant Byte First** (1)</span></span>


</dt> <dd>

<span data-ttu-id="756b9-343">Byte menos significativo primeiro.</span><span class="sxs-lookup"><span data-stu-id="756b9-343">Least significant byte first.</span></span>

</dd> <dt>

<span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="756b9-344"><span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>**Byte mais significativo primeiro** (2)</span><span class="sxs-lookup"><span data-stu-id="756b9-344"><span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>**Most Significant Byte First** (2)</span></span>


</dt> <dd>

<span data-ttu-id="756b9-345">Byte mais significativo primeiro.</span><span class="sxs-lookup"><span data-stu-id="756b9-345">Most significant byte first.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="756b9-346">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="756b9-346">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="756b9-347">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="756b9-347">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="756b9-348">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="756b9-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="756b9-349">Cadeia de caracteres de forma livre que fornece informações sobre o erro registrado na propriedade **LastErrorCode** e as ações corretivas a serem executadas.</span><span class="sxs-lookup"><span data-stu-id="756b9-349">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="756b9-350">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="756b9-350">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="756b9-351">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="756b9-351">**ErrorInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="756b9-352">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="756b9-352">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="756b9-353">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="756b9-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="756b9-354">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memória DMTF \| 2,12 "," MIF. \|Matriz de memória física da DMTF \| 1,8 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ memória CIM**.**OtherErrorDescription**")</span><span class="sxs-lookup"><span data-stu-id="756b9-354">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.12", "MIF.DMTF\|Physical Memory Array\|001.8"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Memory**.**OtherErrorDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="756b9-355">Tipo de erro que ocorreu mais recentemente.</span><span class="sxs-lookup"><span data-stu-id="756b9-355">Type of error that occurred most recently.</span></span> <span data-ttu-id="756b9-356">Os valores de 12 a 14 são indefinidos no esquema CIM porque a DMI combina a semântica do tipo de erro e se ela foi corrigida.</span><span class="sxs-lookup"><span data-stu-id="756b9-356">The values 12 through 14 are undefined in the CIM schema because DMI mixes the semantics of the error type and whether it was correctable.</span></span> <span data-ttu-id="756b9-357">Se um erro é corrigível é indicado na propriedade **CorrectableError** .</span><span class="sxs-lookup"><span data-stu-id="756b9-357">Whether an error is correctable is indicated in the **CorrectableError** property.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="756b9-358"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="756b9-358"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="756b9-359">Outros.</span><span class="sxs-lookup"><span data-stu-id="756b9-359">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="756b9-360"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="756b9-360"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="756b9-361">Desconhecido.</span><span class="sxs-lookup"><span data-stu-id="756b9-361">Unknown.</span></span>

</dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="756b9-362"><span id="OK"></span><span id="ok"></span>**OK** (3)</span><span class="sxs-lookup"><span data-stu-id="756b9-362"><span id="OK"></span><span id="ok"></span>**OK** (3)</span></span>


</dt> <dd>

<span data-ttu-id="756b9-363">OK.</span><span class="sxs-lookup"><span data-stu-id="756b9-363">OK.</span></span>

</dd> <dt>

<span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>

<span data-ttu-id="756b9-364"><span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>**Leitura inadequada** (4)</span><span class="sxs-lookup"><span data-stu-id="756b9-364"><span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>**Bad Read** (4)</span></span>


</dt> <dd>

<span data-ttu-id="756b9-365">Leitura inadequada.</span><span class="sxs-lookup"><span data-stu-id="756b9-365">Bad read.</span></span>

</dd> <dt>

<span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>

<span data-ttu-id="756b9-366"><span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>**Erro de paridade** (5)</span><span class="sxs-lookup"><span data-stu-id="756b9-366"><span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>**Parity Error** (5)</span></span>


</dt> <dd>

<span data-ttu-id="756b9-367">Erro de paridade.</span><span class="sxs-lookup"><span data-stu-id="756b9-367">Parity error.</span></span>

</dd> <dt>

<span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>

<span data-ttu-id="756b9-368"><span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>**Erro de bit único** (6)</span><span class="sxs-lookup"><span data-stu-id="756b9-368"><span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>**Single-Bit Error** (6)</span></span>


</dt> <dd>

<span data-ttu-id="756b9-369">Erro de bit único.</span><span class="sxs-lookup"><span data-stu-id="756b9-369">Single-bit error.</span></span>

</dd> <dt>

<span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>

<span data-ttu-id="756b9-370"><span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>**Erro de bit duplo** (7)</span><span class="sxs-lookup"><span data-stu-id="756b9-370"><span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>**Double-Bit Error** (7)</span></span>


</dt> <dd>

<span data-ttu-id="756b9-371">Erro de bit duplo.</span><span class="sxs-lookup"><span data-stu-id="756b9-371">Double-bit error.</span></span>

</dd> <dt>

<span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>

<span data-ttu-id="756b9-372"><span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>**Erro de vários bits** (8)</span><span class="sxs-lookup"><span data-stu-id="756b9-372"><span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>**Multi-Bit Error** (8)</span></span>


</dt> <dd>

<span data-ttu-id="756b9-373">Erro de vários bits.</span><span class="sxs-lookup"><span data-stu-id="756b9-373">Multi-bit error.</span></span>

</dd> <dt>

<span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>

<span data-ttu-id="756b9-374"><span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>**Erro de Nibble** (9)</span><span class="sxs-lookup"><span data-stu-id="756b9-374"><span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>**Nibble Error** (9)</span></span>


</dt> <dd>

<span data-ttu-id="756b9-375">Erro de Nibble.</span><span class="sxs-lookup"><span data-stu-id="756b9-375">Nibble error.</span></span>

</dd> <dt>

<span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>

<span data-ttu-id="756b9-376"><span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>**Erro de soma de verificação** (10)</span><span class="sxs-lookup"><span data-stu-id="756b9-376"><span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>**Checksum Error** (10)</span></span>


</dt> <dd>

<span data-ttu-id="756b9-377">Erro de soma de verificação.</span><span class="sxs-lookup"><span data-stu-id="756b9-377">Checksum error.</span></span>

</dd> <dt>

<span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>

<span data-ttu-id="756b9-378"><span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>**Erro de CRC** (11)</span><span class="sxs-lookup"><span data-stu-id="756b9-378"><span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>**CRC Error** (11)</span></span>


</dt> <dd>

<span data-ttu-id="756b9-379">Erro de CRC.</span><span class="sxs-lookup"><span data-stu-id="756b9-379">CRC error.</span></span>

</dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="756b9-380"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Indefinido** (12)</span><span class="sxs-lookup"><span data-stu-id="756b9-380"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Undefined** (12)</span></span>


</dt> <dd>

<span data-ttu-id="756b9-381">Indefinido.</span><span class="sxs-lookup"><span data-stu-id="756b9-381">Undefined.</span></span>

</dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="756b9-382"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Indefinido** (13)</span><span class="sxs-lookup"><span data-stu-id="756b9-382"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Undefined** (13)</span></span>


</dt> <dd>

<span data-ttu-id="756b9-383">Indefinido.</span><span class="sxs-lookup"><span data-stu-id="756b9-383">Undefined.</span></span>

</dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="756b9-384"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Indefinido** (14)</span><span class="sxs-lookup"><span data-stu-id="756b9-384"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Undefined** (14)</span></span>


</dt> <dd>

<span data-ttu-id="756b9-385">Indefinido.</span><span class="sxs-lookup"><span data-stu-id="756b9-385">Undefined.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="756b9-386">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="756b9-386">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="756b9-387">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="756b9-387">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="756b9-388">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="756b9-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="756b9-389">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ErrorMethodology"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Matriz de memória física da DMTF \| 1,7 ")</span><span class="sxs-lookup"><span data-stu-id="756b9-389">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ErrorMethodology"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Memory Array\|001.7")</span></span>
</dt> </dl>

<span data-ttu-id="756b9-390">Indica se os algoritmos de paridade ou CRC, ECC ou outros mecanismos são usados.</span><span class="sxs-lookup"><span data-stu-id="756b9-390">Indicates whether parity or CRC algorithms, ECC or other mechanisms are used.</span></span> <span data-ttu-id="756b9-391">Também é possível fornecer detalhes sobre o algoritmo.</span><span class="sxs-lookup"><span data-stu-id="756b9-391">Details on the algorithm can also be supplied.</span></span>

</dd> <dt>

<span data-ttu-id="756b9-392">**ErrorResolution**</span><span class="sxs-lookup"><span data-stu-id="756b9-392">**ErrorResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="756b9-393">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="756b9-393">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="756b9-394">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="756b9-394">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="756b9-395">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memória DMTF \| 2,21 "," MIF. \|Matriz de memória física da DMTF \| 1,15 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="756b9-395">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.21", "MIF.DMTF\|Physical Memory Array\|001.15"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="756b9-396">Especifica o intervalo, em bytes, para o qual o último erro pode ser resolvido.</span><span class="sxs-lookup"><span data-stu-id="756b9-396">Specifies the range, in bytes, to which the last error can be resolved.</span></span> <span data-ttu-id="756b9-397">Por exemplo, se os endereços de erro forem resolvidos para o bit 11 (ou seja, em uma base de página típica), os erros poderão ser resolvidos para os limites de 4 KB e essa propriedade será definida como 4000.</span><span class="sxs-lookup"><span data-stu-id="756b9-397">For example, if error addresses are resolved to bit 11 (that is, on a typical page basis), then errors can be resolved to 4 KB boundaries and this property is set to 4000.</span></span> <span data-ttu-id="756b9-398">Se a propriedade **errorInfo** for igual a 3 ("OK"), essa propriedade não terá significado.</span><span class="sxs-lookup"><span data-stu-id="756b9-398">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="756b9-399">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="756b9-399">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="756b9-400">**ErrorTime**</span><span class="sxs-lookup"><span data-stu-id="756b9-400">**ErrorTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="756b9-401">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="756b9-401">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="756b9-402">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="756b9-402">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="756b9-403">Data e hora em que ocorreu o último erro de memória.</span><span class="sxs-lookup"><span data-stu-id="756b9-403">Date and time that the last memory error occurred.</span></span> <span data-ttu-id="756b9-404">O tipo de erro é descrito pela propriedade **errorInfo** .</span><span class="sxs-lookup"><span data-stu-id="756b9-404">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="756b9-405">Se a propriedade **errorInfo** for igual a 3 ("OK"), essa propriedade não terá significado.</span><span class="sxs-lookup"><span data-stu-id="756b9-405">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="756b9-406">**ErrorTransferSize**</span><span class="sxs-lookup"><span data-stu-id="756b9-406">**ErrorTransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="756b9-407">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="756b9-407">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="756b9-408">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="756b9-408">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="756b9-409">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memória DMTF \| 2,16 "," MIF. \|Matriz de memória física da DMTF \| 1,11 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bits ")</span><span class="sxs-lookup"><span data-stu-id="756b9-409">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.16", "MIF.DMTF\|Physical Memory Array\|001.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="756b9-410">Tamanho da transferência de dados, em bits, que causou o último erro.</span><span class="sxs-lookup"><span data-stu-id="756b9-410">Size of the data transfer, in bits, that caused the last error.</span></span> <span data-ttu-id="756b9-411">Um valor de 0 indica que não há erro.</span><span class="sxs-lookup"><span data-stu-id="756b9-411">A value of 0 indicates no error.</span></span> <span data-ttu-id="756b9-412">Se a propriedade **errorInfo** for igual a 3 ("OK"), essa propriedade deverá ser definida como 0.</span><span class="sxs-lookup"><span data-stu-id="756b9-412">If the **ErrorInfo** property is equal to 3 ("OK"), then this property should be set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="756b9-413">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="756b9-413">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="756b9-414">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="756b9-414">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="756b9-415">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="756b9-415">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="756b9-416">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="756b9-416">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="756b9-417">Indica quando o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="756b9-417">Indicates when the object was installed.</span></span> <span data-ttu-id="756b9-418">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="756b9-418">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="756b9-419">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="756b9-419">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="756b9-420">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="756b9-420">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="756b9-421">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="756b9-421">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="756b9-422">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="756b9-422">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="756b9-423">Código do último erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="756b9-423">Last error code reported by the logical device.</span></span>

<span data-ttu-id="756b9-424">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="756b9-424">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="756b9-425">**Nome**</span><span class="sxs-lookup"><span data-stu-id="756b9-425">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="756b9-426">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="756b9-426">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="756b9-427">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="756b9-427">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="756b9-428">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="756b9-428">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="756b9-429">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="756b9-429">Label by which the object is known.</span></span> <span data-ttu-id="756b9-430">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="756b9-430">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="756b9-431">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="756b9-431">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="756b9-432">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="756b9-432">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="756b9-433">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="756b9-433">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="756b9-434">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="756b9-434">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="756b9-435">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrStorageSize ")</span><span class="sxs-lookup"><span data-stu-id="756b9-435">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="756b9-436">Número de blocos consecutivos, cada um deles bloqueia o tamanho do valor contido na propriedade **BlockSize** , que formam a extensão de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="756b9-436">Number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, that form the storage extent.</span></span> <span data-ttu-id="756b9-437">O tamanho total da extensão de armazenamento pode ser calculado multiplicando o valor da propriedade **BlockSize** pelo valor dessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="756b9-437">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="756b9-438">Se o valor de **BlockSize** for 1 (um), essa propriedade será o tamanho total da extensão de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="756b9-438">If the value of **BlockSize** is 1 (one), this property is the total size of the storage extent.</span></span>

<span data-ttu-id="756b9-439">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="756b9-439">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="756b9-440">Essa propriedade é herdada do [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="756b9-440">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="756b9-441">**OtherErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="756b9-441">**OtherErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="756b9-442">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="756b9-442">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="756b9-443">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="756b9-443">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="756b9-444">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ memória CIM**.**ErrorInfo**")</span><span class="sxs-lookup"><span data-stu-id="756b9-444">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Memory**.**ErrorInfo**")</span></span>
</dt> </dl>

<span data-ttu-id="756b9-445">Cadeia de caracteres de forma livre que fornece informações se a propriedade **ErrorType** estiver definida como 1 ("other").</span><span class="sxs-lookup"><span data-stu-id="756b9-445">Free form string that provides information if the **ErrorType** property is set to 1 ("Other").</span></span> <span data-ttu-id="756b9-446">Se não estiver definido como 1, essa cadeia de caracteres não terá significado.</span><span class="sxs-lookup"><span data-stu-id="756b9-446">If it is not set to 1, then this string has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="756b9-447">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="756b9-447">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="756b9-448">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="756b9-448">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="756b9-449">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="756b9-449">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="756b9-450">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="756b9-450">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="756b9-451">Indica o identificador do dispositivo de Plug and Play do Win32 do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="756b9-451">Indicates the Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="756b9-452">Exemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="756b9-452">Example: "\*PNP030b"</span></span>

<span data-ttu-id="756b9-453">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="756b9-453">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="756b9-454">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="756b9-454">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="756b9-455">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="756b9-455">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="756b9-456">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="756b9-456">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="756b9-457">Indica os recursos específicos relacionados à energia do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="756b9-457">Indicates the specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="756b9-458">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="756b9-458">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="756b9-459"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="756b9-459"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="756b9-460">As capacidades relacionadas à energia são desconhecidas.</span><span class="sxs-lookup"><span data-stu-id="756b9-460">The power-related capacities are unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="756b9-461"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="756b9-461"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="756b9-462">Não há suporte para capacidades relacionadas a energia para este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="756b9-462">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="756b9-463"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="756b9-463"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="756b9-464">As capacidades relacionadas à energia foram desabilitadas.</span><span class="sxs-lookup"><span data-stu-id="756b9-464">Power-related capacities have been disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="756b9-465"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="756b9-465"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="756b9-466">Os recursos de gerenciamento de energia estão habilitados no momento, mas o conjunto de recursos exato é desconhecido ou as informações não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="756b9-466">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="756b9-467"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de economia de energia inseridos automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="756b9-467"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="756b9-468">O dispositivo pode alterar seu estado de energia com base no uso ou em outros critérios.</span><span class="sxs-lookup"><span data-stu-id="756b9-468">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="756b9-469"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energia configurável** (5)</span><span class="sxs-lookup"><span data-stu-id="756b9-469"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="756b9-470">Há suporte para o método **SetPowerState** .</span><span class="sxs-lookup"><span data-stu-id="756b9-470">The **SetPowerState** method is supported.</span></span> <span data-ttu-id="756b9-471">Esse método é encontrado na classe pai [**de \_ LogicalDevice CIM**](cim-logicaldevice.md) e pode ser implementado.</span><span class="sxs-lookup"><span data-stu-id="756b9-471">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="756b9-472">Para obter mais informações, consulte [Designing formato MOF (MOF) classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="756b9-472">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="756b9-473"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energia com suporte** (6)</span><span class="sxs-lookup"><span data-stu-id="756b9-473"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="756b9-474">O método **SetPowerState** pode ser invocado com o parâmetro *PowerState* definido como 5 ("ciclo de energia").</span><span class="sxs-lookup"><span data-stu-id="756b9-474">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="756b9-475"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Energia cronometrada com suporte** (7)</span><span class="sxs-lookup"><span data-stu-id="756b9-475"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="756b9-476">O método **SetPowerState** pode ser invocado com o parâmetro *PowerState* definido como 5 ("ciclo de energia") e o parâmetro de *hora* definido como uma data e hora e um intervalo específicos para o Power-on.</span><span class="sxs-lookup"><span data-stu-id="756b9-476">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="756b9-477">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="756b9-477">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="756b9-478">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="756b9-478">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="756b9-479">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="756b9-479">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="756b9-480">Se for **true**, o dispositivo poderá ser gerenciado por energia, ou seja, colocado em um estado de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="756b9-480">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="756b9-481">Se **for false**, o valor inteiro 1 ("sem suporte") deverá ser a única entrada na matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="756b9-481">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="756b9-482">Essa propriedade não indica se os recursos de gerenciamento de energia estão habilitados no momento ou se estão habilitados, quais recursos têm suporte.</span><span class="sxs-lookup"><span data-stu-id="756b9-482">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="756b9-483">Para obter mais informações, consulte a matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="756b9-483">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="756b9-484">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="756b9-484">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="756b9-485">**Finalidade**</span><span class="sxs-lookup"><span data-stu-id="756b9-485">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="756b9-486">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="756b9-486">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="756b9-487">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="756b9-487">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="756b9-488">Cadeia de caracteres de forma livre que descreve a mídia e seu uso.</span><span class="sxs-lookup"><span data-stu-id="756b9-488">Free form string that describes the media and its use.</span></span>

<span data-ttu-id="756b9-489">Essa propriedade é herdada do [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="756b9-489">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="756b9-490">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="756b9-490">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="756b9-491">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="756b9-491">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="756b9-492">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="756b9-492">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="756b9-493">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Os \| endereços mapeados da matriz de memória DMTF \| 1,3 "," MIF. \|Endereços mapeados do dispositivo \| de memória DMTF 1,4 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" kilobytes ")</span><span class="sxs-lookup"><span data-stu-id="756b9-493">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Array Mapped Addresses\|001.3", "MIF.DMTF\|Memory Device Mapped Addresses\|001.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="756b9-494">Endereço inicial, referenciado por um aplicativo ou sistema operacional e mapeado por um controlador de memória, para esse objeto de memória.</span><span class="sxs-lookup"><span data-stu-id="756b9-494">Beginning address, referenced by an application or operating system and mapped by a memory controller, for this memory object.</span></span> <span data-ttu-id="756b9-495">O endereço inicial é especificado em kilobytes.</span><span class="sxs-lookup"><span data-stu-id="756b9-495">The starting address is specified in kilobytes.</span></span>

<span data-ttu-id="756b9-496">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="756b9-496">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="756b9-497">**Status**</span><span class="sxs-lookup"><span data-stu-id="756b9-497">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="756b9-498">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="756b9-498">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="756b9-499">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="756b9-499">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="756b9-500">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="756b9-500">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="756b9-501">Cadeia de caracteres que indica o status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="756b9-501">String that indicates the current status of the object.</span></span> <span data-ttu-id="756b9-502">O status operacional e não operacional pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="756b9-502">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="756b9-503">O status operacional pode incluir "OK", "degradado" e "Pred falha".</span><span class="sxs-lookup"><span data-stu-id="756b9-503">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="756b9-504">"Pred Fail" indica que um elemento está funcionando corretamente, mas está prevendo uma falha (por exemplo, uma unidade de disco rígido habilitada para inteligente).</span><span class="sxs-lookup"><span data-stu-id="756b9-504">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="756b9-505">O status não operacional pode incluir "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="756b9-505">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="756b9-506">O "serviço" pode ser aplicado durante o espelhamento de disco – reprateando, recarregando uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="756b9-506">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="756b9-507">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="756b9-507">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="756b9-508">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="756b9-508">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="756b9-509">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="756b9-509">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="756b9-510">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="756b9-510">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="756b9-511">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="756b9-511">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="756b9-512">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="756b9-512">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="756b9-513">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="756b9-513">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="756b9-514">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="756b9-514">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="756b9-515">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="756b9-515">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="756b9-516">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="756b9-516">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="756b9-517">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="756b9-517">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="756b9-518">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="756b9-518">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="756b9-519">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="756b9-519">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="756b9-520">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="756b9-520">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="756b9-521">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="756b9-521">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="756b9-522">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="756b9-522">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="756b9-523">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="756b9-523">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="756b9-524">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="756b9-524">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="756b9-525">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="756b9-525">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="756b9-526">Estado do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="756b9-526">State of the logical device.</span></span> <span data-ttu-id="756b9-527">Se essa propriedade não se aplicar ao dispositivo lógico, o valor 5 ("não aplicável") deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="756b9-527">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<span data-ttu-id="756b9-528">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="756b9-528">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="756b9-529">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="756b9-529">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="756b9-530">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="756b9-530">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="756b9-531">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="756b9-531">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="756b9-532">**Desabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="756b9-532">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="756b9-533">**Não aplicável** (5)</span><span class="sxs-lookup"><span data-stu-id="756b9-533">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="756b9-534">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="756b9-534">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="756b9-535">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="756b9-535">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="756b9-536">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="756b9-536">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="756b9-537">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="756b9-537">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="756b9-538">O nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="756b9-538">The scoping system's creation class name.</span></span>

<span data-ttu-id="756b9-539">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="756b9-539">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="756b9-540">**SystemLevelAddress**</span><span class="sxs-lookup"><span data-stu-id="756b9-540">**SystemLevelAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="756b9-541">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="756b9-541">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="756b9-542">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="756b9-542">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="756b9-543">Indica se as informações de endereço na propriedade **ErrorAddress** são um endereço de nível de sistema (**true**) ou um endereço físico (**false**).</span><span class="sxs-lookup"><span data-stu-id="756b9-543">Indicates whether the address information in the **ErrorAddress** property is a system-level address (**TRUE**) or a physical address (**FALSE**).</span></span> <span data-ttu-id="756b9-544">Se a propriedade **errorInfo** for igual a 3 ("OK"), essa propriedade não terá significado.</span><span class="sxs-lookup"><span data-stu-id="756b9-544">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="756b9-545">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="756b9-545">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="756b9-546">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="756b9-546">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="756b9-547">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="756b9-547">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="756b9-548">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="756b9-548">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="756b9-549">O nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="756b9-549">The scoping system's name.</span></span>

<span data-ttu-id="756b9-550">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="756b9-550">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="756b9-551">Comentários</span><span class="sxs-lookup"><span data-stu-id="756b9-551">Remarks</span></span>

<span data-ttu-id="756b9-552">A classe de **\_ memória CIM** é derivada de [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="756b9-552">The **CIM\_Memory** class is derived from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="756b9-553">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="756b9-553">WMI does not implement this class.</span></span> <span data-ttu-id="756b9-554">Para classes derivadas da **\_ memória CIM**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="756b9-554">For classes that are derived from **CIM\_Memory**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="756b9-555">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="756b9-555">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="756b9-556">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="756b9-556">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="756b9-557">Requisitos</span><span class="sxs-lookup"><span data-stu-id="756b9-557">Requirements</span></span>



| <span data-ttu-id="756b9-558">Requisito</span><span class="sxs-lookup"><span data-stu-id="756b9-558">Requirement</span></span> | <span data-ttu-id="756b9-559">Valor</span><span class="sxs-lookup"><span data-stu-id="756b9-559">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="756b9-560">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="756b9-560">Minimum supported client</span></span><br/> | <span data-ttu-id="756b9-561">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="756b9-561">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="756b9-562">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="756b9-562">Minimum supported server</span></span><br/> | <span data-ttu-id="756b9-563">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="756b9-563">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="756b9-564">Namespace</span><span class="sxs-lookup"><span data-stu-id="756b9-564">Namespace</span></span><br/>                | <span data-ttu-id="756b9-565">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="756b9-565">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="756b9-566">MOF</span><span class="sxs-lookup"><span data-stu-id="756b9-566">MOF</span></span><br/>                      | <dl> <span data-ttu-id="756b9-567"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="756b9-567"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="756b9-568">DLL</span><span class="sxs-lookup"><span data-stu-id="756b9-568">DLL</span></span><br/>                      | <dl> <span data-ttu-id="756b9-569"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="756b9-569"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="756b9-570">Confira também</span><span class="sxs-lookup"><span data-stu-id="756b9-570">See also</span></span>

<dl> <dt>

[<span data-ttu-id="756b9-571">**\_STORAGEEXTENT CIM**</span><span class="sxs-lookup"><span data-stu-id="756b9-571">**CIM\_StorageExtent**</span></span>](cim-storageextent.md)
</dt> </dl>

 

