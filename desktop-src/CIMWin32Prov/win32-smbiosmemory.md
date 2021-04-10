---
description: A \_ classe WMI abstrata do Win32 SMBIOSMemory representa as propriedades de uma memória do sistema de computador, como visto por meio da interface do SMBIOS (BIOS de gerenciamento do sistema).
ms.assetid: 2f609fc6-f0f5-45a5-9f9a-3873da034d49
ms.tgt_platform: multiple
title: Classe Win32_SMBIOSMemory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SMBIOSMemory
- Win32_SMBIOSMemory.Reset
- Win32_SMBIOSMemory.SetPowerState
- Win32_SMBIOSMemory.Access
- Win32_SMBIOSMemory.AdditionalErrorData
- Win32_SMBIOSMemory.Availability
- Win32_SMBIOSMemory.BlockSize
- Win32_SMBIOSMemory.Caption
- Win32_SMBIOSMemory.ConfigManagerErrorCode
- Win32_SMBIOSMemory.ConfigManagerUserConfig
- Win32_SMBIOSMemory.CorrectableError
- Win32_SMBIOSMemory.CreationClassName
- Win32_SMBIOSMemory.Description
- Win32_SMBIOSMemory.DeviceID
- Win32_SMBIOSMemory.EndingAddress
- Win32_SMBIOSMemory.ErrorAccess
- Win32_SMBIOSMemory.ErrorAddress
- Win32_SMBIOSMemory.ErrorCleared
- Win32_SMBIOSMemory.ErrorData
- Win32_SMBIOSMemory.ErrorDataOrder
- Win32_SMBIOSMemory.ErrorDescription
- Win32_SMBIOSMemory.ErrorInfo
- Win32_SMBIOSMemory.ErrorMethodology
- Win32_SMBIOSMemory.ErrorResolution
- Win32_SMBIOSMemory.ErrorTime
- Win32_SMBIOSMemory.ErrorTransferSize
- Win32_SMBIOSMemory.InstallDate
- Win32_SMBIOSMemory.LastErrorCode
- Win32_SMBIOSMemory.Name
- Win32_SMBIOSMemory.NumberOfBlocks
- Win32_SMBIOSMemory.OtherErrorDescription
- Win32_SMBIOSMemory.PNPDeviceID
- Win32_SMBIOSMemory.PowerManagementCapabilities
- Win32_SMBIOSMemory.PowerManagementSupported
- Win32_SMBIOSMemory.Purpose
- Win32_SMBIOSMemory.StartingAddress
- Win32_SMBIOSMemory.Status
- Win32_SMBIOSMemory.StatusInfo
- Win32_SMBIOSMemory.SystemCreationClassName
- Win32_SMBIOSMemory.SystemLevelAddress
- Win32_SMBIOSMemory.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4dc7a42732dfb00d965f79045254878f690309fc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089523"
---
# <a name="win32_smbiosmemory-class"></a><span data-ttu-id="604ef-103">\_Classe Win32 SMBIOSMemory</span><span class="sxs-lookup"><span data-stu-id="604ef-103">Win32\_SMBIOSMemory class</span></span>

<span data-ttu-id="604ef-104">A [classe WMI](../wmisdk/retrieving-a-class.md) abstrata do **Win32 \_ SMBIOSMemory** representa as propriedades de uma memória do sistema de computador, como visto por meio da interface do SMBIOS (BIOS de gerenciamento do sistema).</span><span class="sxs-lookup"><span data-stu-id="604ef-104">The **Win32\_SMBIOSMemory** abstract [WMI class](../wmisdk/retrieving-a-class.md) represents the properties of a computer system memory as seen through the system management BIOS (SMBIOS) interface.</span></span> <span data-ttu-id="604ef-105">A interface SMBIOS não faz distinção entre lembranças não voláteis, voláteis e flash.</span><span class="sxs-lookup"><span data-stu-id="604ef-105">The SMBIOS interface does not distinguish between nonvolatile, volatile, and flash memories.</span></span> <span data-ttu-id="604ef-106">A classe de [**\_ memória CIM**](cim-memory.md) é a classe pai de todos os tipos de memória.</span><span class="sxs-lookup"><span data-stu-id="604ef-106">The [**CIM\_Memory**](cim-memory.md) class is the parent class of all types of memory.</span></span>

<span data-ttu-id="604ef-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="604ef-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="604ef-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="604ef-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="604ef-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="604ef-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FECB095B-F0FA-11d2-8617-0000F8102E5F}"), AMENDMENT]
class Win32_SMBIOSMemory : CIM_StorageExtent
{
  uint16   Access;
  uint8    AdditionalErrorData[];
  uint16   Availability;
  uint64   BlockSize;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  boolean  CorrectableError;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  uint64   EndingAddress;
  uint16   ErrorAccess;
  uint64   ErrorAddress;
  boolean  ErrorCleared;
  uint8    ErrorData[];
  uint16   ErrorDataOrder;
  string   ErrorDescription;
  uint16   ErrorInfo;
  string   ErrorMethodology;
  uint64   ErrorResolution;
  datetime ErrorTime;
  uint32   ErrorTransferSize;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Name;
  uint64   NumberOfBlocks;
  string   OtherErrorDescription;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Purpose;
  uint64   StartingAddress;
  string   Status;
  uint16e  StatusInfo;
  string   SystemCreationClassName;
  boolean  SystemLevelAddress;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="604ef-110">Membros</span><span class="sxs-lookup"><span data-stu-id="604ef-110">Members</span></span>

<span data-ttu-id="604ef-111">A classe **Win32 \_ SMBIOSMemory** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="604ef-111">The **Win32\_SMBIOSMemory** class has these types of members:</span></span>

-   [<span data-ttu-id="604ef-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="604ef-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="604ef-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="604ef-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="604ef-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="604ef-114">Methods</span></span>

<span data-ttu-id="604ef-115">A classe **Win32 \_ SMBIOSMemory** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="604ef-115">The **Win32\_SMBIOSMemory** class has these methods.</span></span>



| <span data-ttu-id="604ef-116">Método</span><span class="sxs-lookup"><span data-stu-id="604ef-116">Method</span></span>            | <span data-ttu-id="604ef-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="604ef-117">Description</span></span>                                                                                                                                                                                    |
|:------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="604ef-118">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="604ef-118">**Reset**</span></span>         | <span data-ttu-id="604ef-119">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="604ef-119">Not implemented.</span></span> <span data-ttu-id="604ef-120">Para implementar esse método, consulte o método [**Reset**](reset-method-in-class-cim-controller.md) no [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="604ef-120">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_StorageExtent**](cim-storageextent.md).</span></span><br/>                 |
| <span data-ttu-id="604ef-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="604ef-121">**SetPowerState**</span></span> | <span data-ttu-id="604ef-122">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="604ef-122">Not implemented.</span></span> <span data-ttu-id="604ef-123">Para implementar esse método, consulte o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) no [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="604ef-123">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_StorageExtent**](cim-storageextent.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="604ef-124">Propriedades</span><span class="sxs-lookup"><span data-stu-id="604ef-124">Properties</span></span>

<span data-ttu-id="604ef-125">A classe **Win32 \_ SMBIOSMemory** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="604ef-125">The **Win32\_SMBIOSMemory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="604ef-126">**Acesso**</span><span class="sxs-lookup"><span data-stu-id="604ef-126">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="604ef-127">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="604ef-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="604ef-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="604ef-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="604ef-129">Tipo de acesso.</span><span class="sxs-lookup"><span data-stu-id="604ef-129">Type of access.</span></span>

<span data-ttu-id="604ef-130">Essa propriedade é herdada do [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="604ef-130">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="604ef-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="604ef-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="604ef-132"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Legível** (1)</span><span class="sxs-lookup"><span data-stu-id="604ef-132"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="604ef-133"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Gravável** (2)</span><span class="sxs-lookup"><span data-stu-id="604ef-133"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Writeable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="604ef-134">Gravável</span><span class="sxs-lookup"><span data-stu-id="604ef-134">Writable</span></span>

</dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="604ef-135"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Suporte de leitura/gravação** (3)</span><span class="sxs-lookup"><span data-stu-id="604ef-135"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="604ef-136"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Gravar uma vez** (4)</span><span class="sxs-lookup"><span data-stu-id="604ef-136"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="604ef-137">**AdditionalErrorData**</span><span class="sxs-lookup"><span data-stu-id="604ef-137">**AdditionalErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="604ef-138">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="604ef-138">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="604ef-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="604ef-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="604ef-140">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("tipo de SMBIOS \| 18 \| 32-bit de informação de erro de memória- \| síndrome do fornecedor"), [**Max**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="604ef-140">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Vendor Syndrome"), [**MAX**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="604ef-141">Matriz de octetos que contém informações de erro adicionais.</span><span class="sxs-lookup"><span data-stu-id="604ef-141">Array of octets that hold additional error information.</span></span> <span data-ttu-id="604ef-142">Um exemplo é a verificação de erros e a síndrome de correção (ECC) ou o retorno dos bits de verificação se uma metodologia de erro baseada em CRC for usada.</span><span class="sxs-lookup"><span data-stu-id="604ef-142">An example is Error Checking and Correcting (ECC) Syndrome, or the return of the check bits if a CRC-based error methodology is used.</span></span> <span data-ttu-id="604ef-143">No último caso, se um único erro de bit for reconhecido e o algoritmo CRC (verificação de redundância cíclica) for conhecido, será possível determinar o bit exato que falhou.</span><span class="sxs-lookup"><span data-stu-id="604ef-143">In the latter case, if a single bit error is recognized and the cyclical redundancy check (CRC) algorithm is known, it is possible to determine the exact bit that failed.</span></span> <span data-ttu-id="604ef-144">Esse tipo de dados (síndrome de ECC, dados de verificação de bits ou de bits de paridade ou outras informações fornecidas pelo fornecedor) está incluído neste campo.</span><span class="sxs-lookup"><span data-stu-id="604ef-144">This type of data (ECC Syndrome, Check Bit or Parity Bit data, or other vendor supplied information) is included in this field.</span></span> <span data-ttu-id="604ef-145">Se a propriedade **errorInfo** for igual a 3 (OK), essa propriedade não terá significado.</span><span class="sxs-lookup"><span data-stu-id="604ef-145">If the **ErrorInfo** property is equal to 3 (OK), then this property has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="604ef-146">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="604ef-146">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="604ef-147">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="604ef-147">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="604ef-148">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="604ef-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="604ef-149">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Estado operacional da DMTF \| 3,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="604ef-149">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="604ef-150">Disponibilidade e status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="604ef-150">Availability and status of the device.</span></span>

<span data-ttu-id="604ef-151">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="604ef-151">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="604ef-152"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="604ef-152"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="604ef-153"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="604ef-153"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="604ef-154"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Execução/energia completa** (3)</span><span class="sxs-lookup"><span data-stu-id="604ef-154"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="604ef-155">Energia completa ou em execução</span><span class="sxs-lookup"><span data-stu-id="604ef-155">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="604ef-156"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Aviso** (4)</span><span class="sxs-lookup"><span data-stu-id="604ef-156"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="604ef-157"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (5)</span><span class="sxs-lookup"><span data-stu-id="604ef-157"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="604ef-158"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (6)</span><span class="sxs-lookup"><span data-stu-id="604ef-158"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="604ef-159"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desligar (7** )</span><span class="sxs-lookup"><span data-stu-id="604ef-159"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="604ef-160"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off line** (8)</span><span class="sxs-lookup"><span data-stu-id="604ef-160"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="604ef-161"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fora do imposto** (9)</span><span class="sxs-lookup"><span data-stu-id="604ef-161"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="604ef-162"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="604ef-162"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="604ef-163"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Não instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="604ef-163"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="604ef-164"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erro de instalação** (12)</span><span class="sxs-lookup"><span data-stu-id="604ef-164"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="604ef-165"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Economia **de energia-desconhecido** (13)</span><span class="sxs-lookup"><span data-stu-id="604ef-165"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="604ef-166">O dispositivo é conhecido por estar em um modo de economia de energia, mas seu status exato é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="604ef-166">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="604ef-167"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Economia **de energia-modo de baixa energia** (14)</span><span class="sxs-lookup"><span data-stu-id="604ef-167"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="604ef-168">O dispositivo está em um estado de economia de energia, mas ainda está funcionando e pode exibir o desempenho degradado.</span><span class="sxs-lookup"><span data-stu-id="604ef-168">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="604ef-169"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save-em espera** (15)</span><span class="sxs-lookup"><span data-stu-id="604ef-169"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="604ef-170">O dispositivo não está funcionando, mas pode ser levado a uma potência completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="604ef-170">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="604ef-171"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energia** (16)</span><span class="sxs-lookup"><span data-stu-id="604ef-171"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="604ef-172"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Economia **de energia-aviso** (17)</span><span class="sxs-lookup"><span data-stu-id="604ef-172"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="604ef-173">O dispositivo está em um estado de aviso, embora também esteja em um modo de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="604ef-173">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="604ef-174"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>Em **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="604ef-174"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="604ef-175">O dispositivo está em pausa.</span><span class="sxs-lookup"><span data-stu-id="604ef-175">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="604ef-176"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Não pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="604ef-176"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="604ef-177">O dispositivo não está pronto.</span><span class="sxs-lookup"><span data-stu-id="604ef-177">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="604ef-178"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Não configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="604ef-178"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="604ef-179">O dispositivo não está configurado.</span><span class="sxs-lookup"><span data-stu-id="604ef-179">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="604ef-180"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Desativado** (21)</span><span class="sxs-lookup"><span data-stu-id="604ef-180"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="604ef-181">O dispositivo está silencioso.</span><span class="sxs-lookup"><span data-stu-id="604ef-181">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="604ef-182">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="604ef-182">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="604ef-183">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="604ef-183">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="604ef-184">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="604ef-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="604ef-185">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| host-REsources-MIB. hrStorageAllocationUnits "), [**Units**](../wmisdk/standard-qualifiers.md) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="604ef-185">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="604ef-186">Tamanho em bytes dos blocos que formam esta extensão de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="604ef-186">Size in bytes of the blocks that form this storage extent.</span></span> <span data-ttu-id="604ef-187">Se for desconhecido ou se um conceito de bloco não for válido (por exemplo, para extensões de agregação, memória ou discos lógicos), insira um 1.</span><span class="sxs-lookup"><span data-stu-id="604ef-187">If unknown or if a block concept is not valid (for example, for aggregate extents, memory or logical disks), enter a 1.</span></span>

<span data-ttu-id="604ef-188">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="604ef-188">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

<span data-ttu-id="604ef-189">Essa propriedade é herdada do [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="604ef-189">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="604ef-190">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="604ef-190">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="604ef-191">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="604ef-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="604ef-192">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="604ef-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="604ef-193">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="604ef-193">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="604ef-194">Breve descrição do objeto — uma cadeia de caracteres de uma linha.</span><span class="sxs-lookup"><span data-stu-id="604ef-194">Short description of the object—a one-line string.</span></span>

<span data-ttu-id="604ef-195">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="604ef-195">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="604ef-196">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="604ef-196">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="604ef-197">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="604ef-197">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="604ef-198">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="604ef-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="604ef-199">Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="604ef-199">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="604ef-200">Código de erro do Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="604ef-200">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="604ef-201">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="604ef-201">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="604ef-202"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo está funcionando corretamente.**</span><span class="sxs-lookup"><span data-stu-id="604ef-202"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="604ef-203"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="604ef-203">(0)</span></span>


</dt> <dd>

<span data-ttu-id="604ef-204">O dispositivo está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="604ef-204">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="604ef-205"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo não está configurado corretamente.**</span><span class="sxs-lookup"><span data-stu-id="604ef-205"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="604ef-206">(1)</span><span class="sxs-lookup"><span data-stu-id="604ef-206">(1)</span></span>


</dt> <dd>

<span data-ttu-id="604ef-207">O dispositivo não está configurado corretamente.</span><span class="sxs-lookup"><span data-stu-id="604ef-207">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="604ef-208"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**O Windows não pode carregar o driver para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="604ef-208"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="604ef-209">(2)</span><span class="sxs-lookup"><span data-stu-id="604ef-209">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="604ef-210"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.**</span><span class="sxs-lookup"><span data-stu-id="604ef-210"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="604ef-211">(3)</span><span class="sxs-lookup"><span data-stu-id="604ef-211">(3)</span></span>


</dt> <dd>

<span data-ttu-id="604ef-212">O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.</span><span class="sxs-lookup"><span data-stu-id="604ef-212">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="604ef-213"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo não está funcionando corretamente. Um de seus drivers ou seu registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="604ef-213"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="604ef-214">(4)</span><span class="sxs-lookup"><span data-stu-id="604ef-214">(4)</span></span>


</dt> <dd>

<span data-ttu-id="604ef-215">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="604ef-215">Device is not working properly.</span></span> <span data-ttu-id="604ef-216">Um de seus drivers ou o registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="604ef-216">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="604ef-217"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**O driver para este dispositivo precisa de um recurso que o Windows não possa gerenciar.**</span><span class="sxs-lookup"><span data-stu-id="604ef-217"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="604ef-218">(5)</span><span class="sxs-lookup"><span data-stu-id="604ef-218">(5)</span></span>


</dt> <dd>

<span data-ttu-id="604ef-219">O driver para o dispositivo requer um recurso que o Windows não pode gerenciar.</span><span class="sxs-lookup"><span data-stu-id="604ef-219">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="604ef-220"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**A configuração de inicialização para este dispositivo está em conflito com outros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="604ef-220"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="604ef-221"> (6)</span><span class="sxs-lookup"><span data-stu-id="604ef-221">(6)</span></span>


</dt> <dd>

<span data-ttu-id="604ef-222">A configuração de inicialização para o dispositivo está em conflito com outros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="604ef-222">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="604ef-223"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Não é possível filtrar.**</span><span class="sxs-lookup"><span data-stu-id="604ef-223"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="604ef-224">(7)</span><span class="sxs-lookup"><span data-stu-id="604ef-224">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="604ef-225"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**O carregador de driver para o dispositivo está ausente.**</span><span class="sxs-lookup"><span data-stu-id="604ef-225"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="604ef-226">(8)</span><span class="sxs-lookup"><span data-stu-id="604ef-226">(8)</span></span>


</dt> <dd>

<span data-ttu-id="604ef-227">O carregador de driver para o dispositivo está ausente.</span><span class="sxs-lookup"><span data-stu-id="604ef-227">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="604ef-228"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo não está funcionando corretamente porque o firmware de controle está relatando os recursos para o dispositivo incorretamente.**</span><span class="sxs-lookup"><span data-stu-id="604ef-228"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="604ef-229">(9)</span><span class="sxs-lookup"><span data-stu-id="604ef-229">(9)</span></span>


</dt> <dd>

<span data-ttu-id="604ef-230">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="604ef-230">Device is not working properly.</span></span> <span data-ttu-id="604ef-231">O firmware de controle está relatando incorretamente os recursos para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="604ef-231">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="604ef-232"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo não pode ser iniciado.**</span><span class="sxs-lookup"><span data-stu-id="604ef-232"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="604ef-233">(10)</span><span class="sxs-lookup"><span data-stu-id="604ef-233">(10)</span></span>


</dt> <dd>

<span data-ttu-id="604ef-234">Não é possível iniciar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="604ef-234">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="604ef-235"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Este dispositivo falhou.**</span><span class="sxs-lookup"><span data-stu-id="604ef-235"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="604ef-236">(11)</span><span class="sxs-lookup"><span data-stu-id="604ef-236">(11)</span></span>


</dt> <dd>

<span data-ttu-id="604ef-237">Falha no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="604ef-237">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="604ef-238"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo não pode encontrar recursos livres suficientes que podem ser usados.**</span><span class="sxs-lookup"><span data-stu-id="604ef-238"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="604ef-239">12</span><span class="sxs-lookup"><span data-stu-id="604ef-239">(12)</span></span>


</dt> <dd>

<span data-ttu-id="604ef-240">O dispositivo não pode encontrar recursos livres suficientes para usar.</span><span class="sxs-lookup"><span data-stu-id="604ef-240">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="604ef-241"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**O Windows não pode verificar os recursos deste dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="604ef-241"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="604ef-242">(13)</span><span class="sxs-lookup"><span data-stu-id="604ef-242">(13)</span></span>


</dt> <dd>

<span data-ttu-id="604ef-243">O Windows não pode verificar os recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="604ef-243">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="604ef-244"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo não funcionará corretamente até que você reinicie o computador.**</span><span class="sxs-lookup"><span data-stu-id="604ef-244"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="604ef-245">(14)</span><span class="sxs-lookup"><span data-stu-id="604ef-245">(14)</span></span>


</dt> <dd>

<span data-ttu-id="604ef-246">O dispositivo não funcionará corretamente até que o computador seja reiniciado.</span><span class="sxs-lookup"><span data-stu-id="604ef-246">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="604ef-247"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo não está funcionando corretamente porque provavelmente há um problema de nova enumeração.**</span><span class="sxs-lookup"><span data-stu-id="604ef-247"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="604ef-248">(15)</span><span class="sxs-lookup"><span data-stu-id="604ef-248">(15)</span></span>


</dt> <dd>

<span data-ttu-id="604ef-249">O dispositivo não está funcionando corretamente devido a um possível problema de reenumeração.</span><span class="sxs-lookup"><span data-stu-id="604ef-249">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="604ef-250"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**O Windows não pode identificar todos os recursos que este dispositivo usa.**</span><span class="sxs-lookup"><span data-stu-id="604ef-250"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="604ef-251">(16)</span><span class="sxs-lookup"><span data-stu-id="604ef-251">(16)</span></span>


</dt> <dd>

<span data-ttu-id="604ef-252">O Windows não pode identificar todos os recursos que o dispositivo usa.</span><span class="sxs-lookup"><span data-stu-id="604ef-252">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="604ef-253"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo está solicitando um tipo de recurso desconhecido.**</span><span class="sxs-lookup"><span data-stu-id="604ef-253"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="604ef-254">(17)</span><span class="sxs-lookup"><span data-stu-id="604ef-254">(17)</span></span>


</dt> <dd>

<span data-ttu-id="604ef-255">O dispositivo está solicitando um tipo de recurso desconhecido.</span><span class="sxs-lookup"><span data-stu-id="604ef-255">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="604ef-256"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstale os drivers para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="604ef-256"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="604ef-257">(18)</span><span class="sxs-lookup"><span data-stu-id="604ef-257">(18)</span></span>


</dt> <dd>

<span data-ttu-id="604ef-258">Os drivers de dispositivo devem ser reinstalados.</span><span class="sxs-lookup"><span data-stu-id="604ef-258">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="604ef-259"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Falha ao usar o carregador VxD.**</span><span class="sxs-lookup"><span data-stu-id="604ef-259"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="604ef-260">(19)</span><span class="sxs-lookup"><span data-stu-id="604ef-260">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="604ef-261"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**O registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="604ef-261"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="604ef-262">(20)</span><span class="sxs-lookup"><span data-stu-id="604ef-262">(20)</span></span>


</dt> <dd>

<span data-ttu-id="604ef-263">O registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="604ef-263">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="604ef-264"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware. O Windows está removendo este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="604ef-264"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="604ef-265">(21)</span><span class="sxs-lookup"><span data-stu-id="604ef-265">(21)</span></span>


</dt> <dd>

<span data-ttu-id="604ef-266">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="604ef-266">System failure.</span></span> <span data-ttu-id="604ef-267">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="604ef-267">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="604ef-268">O Windows está removendo o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="604ef-268">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="604ef-269"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está desabilitado.**</span><span class="sxs-lookup"><span data-stu-id="604ef-269"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="604ef-270">(22)</span><span class="sxs-lookup"><span data-stu-id="604ef-270">(22)</span></span>


</dt> <dd>

<span data-ttu-id="604ef-271">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="604ef-271">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="604ef-272"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware.**</span><span class="sxs-lookup"><span data-stu-id="604ef-272"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="604ef-273">(23)</span><span class="sxs-lookup"><span data-stu-id="604ef-273">(23)</span></span>


</dt> <dd>

<span data-ttu-id="604ef-274">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="604ef-274">System failure.</span></span> <span data-ttu-id="604ef-275">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="604ef-275">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="604ef-276"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo não está presente, não está funcionando corretamente ou não tem todos os drivers instalados.**</span><span class="sxs-lookup"><span data-stu-id="604ef-276"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="604ef-277">(24)</span><span class="sxs-lookup"><span data-stu-id="604ef-277">(24)</span></span>


</dt> <dd>

<span data-ttu-id="604ef-278">O dispositivo não está presente, não está funcionando corretamente ou não tem todos os seus drivers instalados.</span><span class="sxs-lookup"><span data-stu-id="604ef-278">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="604ef-279"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="604ef-279"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="604ef-280">(25)</span><span class="sxs-lookup"><span data-stu-id="604ef-280">(25)</span></span>


</dt> <dd>

<span data-ttu-id="604ef-281">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="604ef-281">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="604ef-282"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="604ef-282"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="604ef-283">(26)</span><span class="sxs-lookup"><span data-stu-id="604ef-283">(26)</span></span>


</dt> <dd>

<span data-ttu-id="604ef-284">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="604ef-284">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="604ef-285"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo não tem uma configuração de log válida.**</span><span class="sxs-lookup"><span data-stu-id="604ef-285"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="604ef-286">(27)</span><span class="sxs-lookup"><span data-stu-id="604ef-286">(27)</span></span>


</dt> <dd>

<span data-ttu-id="604ef-287">O dispositivo não tem uma configuração de log válida.</span><span class="sxs-lookup"><span data-stu-id="604ef-287">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="604ef-288"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Os drivers para este dispositivo não estão instalados.**</span><span class="sxs-lookup"><span data-stu-id="604ef-288"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="604ef-289">(28)</span><span class="sxs-lookup"><span data-stu-id="604ef-289">(28)</span></span>


</dt> <dd>

<span data-ttu-id="604ef-290">Os drivers de dispositivo não estão instalados.</span><span class="sxs-lookup"><span data-stu-id="604ef-290">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="604ef-291"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está desabilitado porque o firmware do dispositivo não forneceu os recursos necessários.**</span><span class="sxs-lookup"><span data-stu-id="604ef-291"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="604ef-292">(29)</span><span class="sxs-lookup"><span data-stu-id="604ef-292">(29)</span></span>


</dt> <dd>

<span data-ttu-id="604ef-293">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="604ef-293">Device is disabled.</span></span> <span data-ttu-id="604ef-294">O firmware do dispositivo não forneceu os recursos necessários.</span><span class="sxs-lookup"><span data-stu-id="604ef-294">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="604ef-295"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo está usando um recurso de IRQ (solicitação de interrupção) que outro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="604ef-295"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="604ef-296">(30)</span><span class="sxs-lookup"><span data-stu-id="604ef-296">(30)</span></span>


</dt> <dd>

<span data-ttu-id="604ef-297">O dispositivo está usando um recurso de IRQ que outro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="604ef-297">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="604ef-298"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo não está funcionando corretamente porque o Windows não pode carregar os drivers necessários para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="604ef-298"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="604ef-299">(31)</span><span class="sxs-lookup"><span data-stu-id="604ef-299">(31)</span></span>


</dt> <dd>

<span data-ttu-id="604ef-300">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="604ef-300">Device is not working properly.</span></span> <span data-ttu-id="604ef-301">O Windows não pode carregar os drivers de dispositivo necessários.</span><span class="sxs-lookup"><span data-stu-id="604ef-301">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="604ef-302">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="604ef-302">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="604ef-303">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="604ef-303">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="604ef-304">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="604ef-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="604ef-305">Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="604ef-305">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="604ef-306">Se for **true**, o dispositivo estará usando uma configuração definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="604ef-306">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="604ef-307">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="604ef-307">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="604ef-308">**CorrectableError**</span><span class="sxs-lookup"><span data-stu-id="604ef-308">**CorrectableError**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="604ef-309">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="604ef-309">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="604ef-310">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="604ef-310">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="604ef-311">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("tipo de SMBIOS \| 18 \| 32-bit de erro informações de erro de memória \| ")</span><span class="sxs-lookup"><span data-stu-id="604ef-311">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Type")</span></span>
</dt> </dl>

<span data-ttu-id="604ef-312">Se **for true**, o erro mais recente era corrigível.</span><span class="sxs-lookup"><span data-stu-id="604ef-312">If **TRUE**, the most recent error was correctable.</span></span> <span data-ttu-id="604ef-313">Se a propriedade **errorInfo** for igual a 3 (OK), essa propriedade não terá significado.</span><span class="sxs-lookup"><span data-stu-id="604ef-313">If the **ErrorInfo** property is equal to 3 (OK), then this property has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="604ef-314">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="604ef-314">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="604ef-315">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="604ef-315">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="604ef-316">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="604ef-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="604ef-317">Qualificadores: [ **\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="604ef-317">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="604ef-318">Nome da primeira classe concreta que aparece na cadeia de herança usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="604ef-318">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="604ef-319">Quando usado com as outras propriedades de chave da classe, a propriedade permite que todas as instâncias dessa classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="604ef-319">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="604ef-320">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="604ef-320">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="604ef-321">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="604ef-321">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="604ef-322">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="604ef-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="604ef-323">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="604ef-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="604ef-324">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="604ef-324">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="604ef-325">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="604ef-325">Description of the object.</span></span>

<span data-ttu-id="604ef-326">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="604ef-326">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="604ef-327">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="604ef-327">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="604ef-328">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="604ef-328">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="604ef-329">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="604ef-329">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="604ef-330">Qualificadores: [ **\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="604ef-330">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="604ef-331">Identificador exclusivo do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="604ef-331">Unique identifier of the logical device.</span></span>

<span data-ttu-id="604ef-332">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="604ef-332">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="604ef-333">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="604ef-333">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="604ef-334">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="604ef-334">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="604ef-335">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="604ef-335">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="604ef-336">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("tipo de SMBIOS \| 19 \| endereços mapeados de dispositivo de memória \| endereço final")</span><span class="sxs-lookup"><span data-stu-id="604ef-336">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 19\|Memory Device Mapped Addresses\|Ending Address")</span></span>
</dt> </dl>

<span data-ttu-id="604ef-337">Endereço final, referenciado por um aplicativo ou sistema operacional e mapeado por um controlador de memória para esse objeto de memória.</span><span class="sxs-lookup"><span data-stu-id="604ef-337">Ending address, referenced by an application or operating system and mapped by a memory controller for this memory object.</span></span> <span data-ttu-id="604ef-338">O endereço final é especificado em kilobytes.</span><span class="sxs-lookup"><span data-stu-id="604ef-338">The ending address is specified in kilobytes.</span></span>

<span data-ttu-id="604ef-339">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="604ef-339">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="604ef-340">**ErrorAccess**</span><span class="sxs-lookup"><span data-stu-id="604ef-340">**ErrorAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="604ef-341">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="604ef-341">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="604ef-342">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="604ef-342">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="604ef-343">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("tipo de SMBIOS \| 18 \| 32-operação de erro de informações de erro de memória \| ")</span><span class="sxs-lookup"><span data-stu-id="604ef-343">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Operation")</span></span>
</dt> </dl>

<span data-ttu-id="604ef-344">Operação de acesso à memória que causou o último erro.</span><span class="sxs-lookup"><span data-stu-id="604ef-344">Memory access operation that caused the last error.</span></span> <span data-ttu-id="604ef-345">O tipo de erro é descrito pela propriedade **errorInfo** .</span><span class="sxs-lookup"><span data-stu-id="604ef-345">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="604ef-346">Se **errorInfo** for igual a 3 (OK), essa propriedade não terá significado.</span><span class="sxs-lookup"><span data-stu-id="604ef-346">If **ErrorInfo** is equal to 3 (OK), then this property has no meaning.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="604ef-347">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="604ef-347">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="604ef-348">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="604ef-348">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="604ef-349">**Leitura** (3)</span><span class="sxs-lookup"><span data-stu-id="604ef-349">**Read** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

<span data-ttu-id="604ef-350">**Gravação** (4)</span><span class="sxs-lookup"><span data-stu-id="604ef-350">**Write** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>

<span data-ttu-id="604ef-351">**Gravação parcial** (5)</span><span class="sxs-lookup"><span data-stu-id="604ef-351">**Partial Write** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="604ef-352">**ErrorAddress**</span><span class="sxs-lookup"><span data-stu-id="604ef-352">**ErrorAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="604ef-353">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="604ef-353">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="604ef-354">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="604ef-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="604ef-355">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("tipo de SMBIOS \| 18 \| 32-bit erro de memória informações de erro \| endereço")</span><span class="sxs-lookup"><span data-stu-id="604ef-355">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Address")</span></span>
</dt> </dl>

<span data-ttu-id="604ef-356">Endereço do último erro de memória.</span><span class="sxs-lookup"><span data-stu-id="604ef-356">Address of the last memory error.</span></span> <span data-ttu-id="604ef-357">O tipo de erro é descrito pela propriedade **errorInfo** .</span><span class="sxs-lookup"><span data-stu-id="604ef-357">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="604ef-358">Se **errorInfo** for igual a 3 (OK), essa propriedade não terá significado.</span><span class="sxs-lookup"><span data-stu-id="604ef-358">If **ErrorInfo** is equal to 3 (OK), then this property has no meaning.</span></span>

<span data-ttu-id="604ef-359">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="604ef-359">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="604ef-360">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="604ef-360">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="604ef-361">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="604ef-361">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="604ef-362">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="604ef-362">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="604ef-363">Se **for true**, o erro relatado em **LastErrorCode** agora será limpo.</span><span class="sxs-lookup"><span data-stu-id="604ef-363">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="604ef-364">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="604ef-364">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="604ef-365">**ErrorData**</span><span class="sxs-lookup"><span data-stu-id="604ef-365">**ErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="604ef-366">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="604ef-366">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="604ef-367">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="604ef-367">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="604ef-368">Qualificadores: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("indexado"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS"), [**Max**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="604ef-368">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS"), [**MAX**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="604ef-369">Matriz de dados capturados durante o último acesso de memória incorreto.</span><span class="sxs-lookup"><span data-stu-id="604ef-369">Array of data captured during the last erroneous memory access.</span></span> <span data-ttu-id="604ef-370">Os dados ocupam os primeiros *n* octetos da matriz necessários para manter o número de bits especificado pela propriedade **ErrorTransferSize** .</span><span class="sxs-lookup"><span data-stu-id="604ef-370">The data occupies the first *n* octets of the array necessary to hold the number of bits specified by the **ErrorTransferSize** property.</span></span> <span data-ttu-id="604ef-371">Se **ErrorTransferSize** for 0 (zero), essa propriedade não terá significado.</span><span class="sxs-lookup"><span data-stu-id="604ef-371">If **ErrorTransferSize** is 0 (zero), then this property has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="604ef-372">**ErrorDataOrder**</span><span class="sxs-lookup"><span data-stu-id="604ef-372">**ErrorDataOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="604ef-373">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="604ef-373">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="604ef-374">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="604ef-374">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="604ef-375">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="604ef-375">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="604ef-376">Ordenação de dados armazenados na propriedade **ErrorData** .</span><span class="sxs-lookup"><span data-stu-id="604ef-376">Ordering for data stored in the **ErrorData** property.</span></span> <span data-ttu-id="604ef-377">Se **ErrorTransferSize** for 0 (zero), essa propriedade não terá significado.</span><span class="sxs-lookup"><span data-stu-id="604ef-377">If **ErrorTransferSize** is 0 (zero), then this property has no meaning.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="604ef-378">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="604ef-378">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="604ef-379">**Byte menos significativo primeiro** (1)</span><span class="sxs-lookup"><span data-stu-id="604ef-379">**Least Significant Byte First** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="604ef-380">**Byte mais significativo primeiro** (2)</span><span class="sxs-lookup"><span data-stu-id="604ef-380">**Most Significant Byte First** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="604ef-381">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="604ef-381">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="604ef-382">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="604ef-382">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="604ef-383">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="604ef-383">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="604ef-384">Mais informações sobre o erro registrado em **LastErrorCode** e informações sobre as ações corretivas que podem ser executadas.</span><span class="sxs-lookup"><span data-stu-id="604ef-384">More information about the error recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="604ef-385">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="604ef-385">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="604ef-386">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="604ef-386">**ErrorInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="604ef-387">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="604ef-387">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="604ef-388">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="604ef-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="604ef-389">Qualificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ memória CIM**](cim-memory.md).**OtherErrorDescription**"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" tipo de SMBIOS \| 18 \| 32-bit memória erro Information \| Type ")</span><span class="sxs-lookup"><span data-stu-id="604ef-389">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Memory**](cim-memory.md).**OtherErrorDescription**"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Type")</span></span>
</dt> </dl>

<span data-ttu-id="604ef-390">Tipo de erro que ocorreu mais recentemente.</span><span class="sxs-lookup"><span data-stu-id="604ef-390">Type of error that occurred most recently.</span></span> <span data-ttu-id="604ef-391">Os valores de 12 a 14 não são usados.</span><span class="sxs-lookup"><span data-stu-id="604ef-391">The values 12 through 14 are unused.</span></span> <span data-ttu-id="604ef-392">A capacidade de ser corrigida é indicada na propriedade **CorrectableError**.</span><span class="sxs-lookup"><span data-stu-id="604ef-392">The ability to be corrected is indicated in the property **CorrectableError**.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="604ef-393">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="604ef-393">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="604ef-394">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="604ef-394">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="604ef-395">**OK** (3)</span><span class="sxs-lookup"><span data-stu-id="604ef-395">**OK** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>

<span data-ttu-id="604ef-396">**Leitura inadequada** (4)</span><span class="sxs-lookup"><span data-stu-id="604ef-396">**Bad Read** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>

<span data-ttu-id="604ef-397">**Erro de paridade** (5)</span><span class="sxs-lookup"><span data-stu-id="604ef-397">**Parity Error** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>

<span data-ttu-id="604ef-398">**Erro de bit único** (6)</span><span class="sxs-lookup"><span data-stu-id="604ef-398">**Single-Bit Error** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>

<span data-ttu-id="604ef-399">**Erro de bit duplo** (7)</span><span class="sxs-lookup"><span data-stu-id="604ef-399">**Double-Bit Error** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>

<span data-ttu-id="604ef-400">**Erro de vários bits** (8)</span><span class="sxs-lookup"><span data-stu-id="604ef-400">**Multi-Bit Error** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>

<span data-ttu-id="604ef-401">**Erro de Nibble** (9)</span><span class="sxs-lookup"><span data-stu-id="604ef-401">**Nibble Error** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>

<span data-ttu-id="604ef-402">**Erro de soma de verificação** (10)</span><span class="sxs-lookup"><span data-stu-id="604ef-402">**Checksum Error** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>

<span data-ttu-id="604ef-403">**Erro de CRC** (11)</span><span class="sxs-lookup"><span data-stu-id="604ef-403">**CRC Error** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Corrected_single-bit_error"></span><span id="corrected_single-bit_error"></span><span id="CORRECTED_SINGLE-BIT_ERROR"></span>

<span data-ttu-id="604ef-404">**Erro de bit único corrigido** (12)</span><span class="sxs-lookup"><span data-stu-id="604ef-404">**Corrected single-bit error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Corrected_error"></span><span id="corrected_error"></span><span id="CORRECTED_ERROR"></span>

<span data-ttu-id="604ef-405">**Erro corrigido** (13)</span><span class="sxs-lookup"><span data-stu-id="604ef-405">**Corrected error** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Uncorrectable_error"></span><span id="uncorrectable_error"></span><span id="UNCORRECTABLE_ERROR"></span>

<span data-ttu-id="604ef-406">**Erro não corrigível** (14)</span><span class="sxs-lookup"><span data-stu-id="604ef-406">**Uncorrectable error** (14)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="604ef-407">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="604ef-407">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="604ef-408">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="604ef-408">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="604ef-409">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="604ef-409">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="604ef-410">Qualificadores: [**override**](../wmisdk/standard-qualifiers.md) ("ErrorMethodology"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| correção de erro de memória da matriz de memória física do SMBIOS tipo 16 \| \| ")</span><span class="sxs-lookup"><span data-stu-id="604ef-410">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("ErrorMethodology"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 16\|Physical Memory Array\|Memory Error Correction")</span></span>
</dt> </dl>

<span data-ttu-id="604ef-411">Detalhes sobre os algoritmos de paridade ou CRC, ECC ou outros mecanismos usados.</span><span class="sxs-lookup"><span data-stu-id="604ef-411">Details on the parity or CRC algorithms, ECC or other mechanisms used.</span></span>

<span data-ttu-id="604ef-412">Essa propriedade é herdada do [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="604ef-412">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="604ef-413">**Outro** ("outro")</span><span class="sxs-lookup"><span data-stu-id="604ef-413">**Other** ("Other")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="604ef-414">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="604ef-414">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="604ef-415">**Nenhum** ("nenhum")</span><span class="sxs-lookup"><span data-stu-id="604ef-415">**None** ("None")</span></span>


</dt> <dd></dd> <dt>

<span id="Parity"></span><span id="parity"></span><span id="PARITY"></span>

<span data-ttu-id="604ef-416">**Paridade** ("paridade")</span><span class="sxs-lookup"><span data-stu-id="604ef-416">**Parity** ("Parity")</span></span>


</dt> <dd></dd> <dt>

<span id="Single-bit_ECC"></span><span id="single-bit_ecc"></span><span id="SINGLE-BIT_ECC"></span>

<span data-ttu-id="604ef-417">**ECC de bit único** ("ECC de bit único")</span><span class="sxs-lookup"><span data-stu-id="604ef-417">**Single-bit ECC** ("Single-bit ECC")</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-bit_ECC"></span><span id="multi-bit_ecc"></span><span id="MULTI-BIT_ECC"></span>

<span data-ttu-id="604ef-418">**ECC de vários bits** ("ECC de múltiplos bits")</span><span class="sxs-lookup"><span data-stu-id="604ef-418">**Multi-bit ECC** ("Multi-bit ECC")</span></span>


</dt> <dd></dd> <dt>

<span id="CRC"></span><span id="crc"></span>

<span data-ttu-id="604ef-419">**CRC** ("CRC")</span><span class="sxs-lookup"><span data-stu-id="604ef-419">**CRC** ("CRC")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="604ef-420">**ErrorResolution**</span><span class="sxs-lookup"><span data-stu-id="604ef-420">**ErrorResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="604ef-421">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="604ef-421">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="604ef-422">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="604ef-422">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="604ef-423">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| tipo SMBIOS 18 \| 32-bit de erro de memória informações de \| resolução de erro"), [**unidades**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="604ef-423">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Resolution"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="604ef-424">Intervalo, em bytes, para o qual o último erro pode ser resolvido.</span><span class="sxs-lookup"><span data-stu-id="604ef-424">Range, in bytes, to which the last error can be resolved.</span></span> <span data-ttu-id="604ef-425">Por exemplo, se os endereços de erro forem resolvidos para o bit 11 (ou seja, em uma base de página típica), os erros poderão ser resolvidos para os limites de 4 KB e essa propriedade será definida como 4000.</span><span class="sxs-lookup"><span data-stu-id="604ef-425">For example, if error addresses are resolved to bit 11 (that is, on a typical page basis), then errors can be resolved to 4 KB boundaries and this property is set to 4000.</span></span> <span data-ttu-id="604ef-426">Se a propriedade **errorInfo** for igual a 3 (OK), essa propriedade não terá significado.</span><span class="sxs-lookup"><span data-stu-id="604ef-426">If the **ErrorInfo** property is equal to 3 (OK), then this property has no meaning.</span></span>

<span data-ttu-id="604ef-427">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="604ef-427">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="604ef-428">**ErrorTime**</span><span class="sxs-lookup"><span data-stu-id="604ef-428">**ErrorTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="604ef-429">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="604ef-429">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="604ef-430">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="604ef-430">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="604ef-431">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="604ef-431">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="604ef-432">Hora em que ocorreu o último erro de memória.</span><span class="sxs-lookup"><span data-stu-id="604ef-432">Time that the last memory error occurred.</span></span> <span data-ttu-id="604ef-433">O tipo de erro é descrito pela propriedade **errorInfo** .</span><span class="sxs-lookup"><span data-stu-id="604ef-433">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="604ef-434">Se a propriedade **errorInfo** for igual a 3 (OK), essa propriedade não terá significado.</span><span class="sxs-lookup"><span data-stu-id="604ef-434">If the **ErrorInfo** property is equal to 3 (OK), then this property has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="604ef-435">**ErrorTransferSize**</span><span class="sxs-lookup"><span data-stu-id="604ef-435">**ErrorTransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="604ef-436">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="604ef-436">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="604ef-437">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="604ef-437">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="604ef-438">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS"), [**Units**](../wmisdk/standard-qualifiers.md) ("bits")</span><span class="sxs-lookup"><span data-stu-id="604ef-438">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS"), [**Units**](../wmisdk/standard-qualifiers.md) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="604ef-439">Tamanho da transferência de dados em bits que causou o último erro – 0 (zero) indica que não há erro.</span><span class="sxs-lookup"><span data-stu-id="604ef-439">Size of the data transfer in bits that caused the last error—0 (zero) indicates no error.</span></span> <span data-ttu-id="604ef-440">Se a propriedade **errorInfo** for igual a 3 (OK), essa propriedade deverá ser definida como 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="604ef-440">If the **ErrorInfo** property is equal to 3 (OK), then this property should be set to 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="604ef-441">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="604ef-441">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="604ef-442">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="604ef-442">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="604ef-443">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="604ef-443">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="604ef-444">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="604ef-444">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="604ef-445">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="604ef-445">Date and time the object was installed.</span></span> <span data-ttu-id="604ef-446">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="604ef-446">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="604ef-447">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="604ef-447">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="604ef-448">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="604ef-448">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="604ef-449">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="604ef-449">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="604ef-450">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="604ef-450">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="604ef-451">Código do último erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="604ef-451">Last error code reported by the logical device.</span></span>

<span data-ttu-id="604ef-452">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="604ef-452">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="604ef-453">**Nome**</span><span class="sxs-lookup"><span data-stu-id="604ef-453">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="604ef-454">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="604ef-454">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="604ef-455">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="604ef-455">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="604ef-456">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="604ef-456">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="604ef-457">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="604ef-457">Label by which the object is known.</span></span> <span data-ttu-id="604ef-458">Quando em uma subclasse, a propriedade pode ser substituída para ser uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="604ef-458">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="604ef-459">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="604ef-459">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="604ef-460">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="604ef-460">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="604ef-461">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="604ef-461">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="604ef-462">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="604ef-462">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="604ef-463">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| host-REsources-MIB. hrStorageSize ")</span><span class="sxs-lookup"><span data-stu-id="604ef-463">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="604ef-464">Número total de blocos consecutivos, cada um deles bloqueando o tamanho do valor contido na propriedade **BlockSize** , que formam essa extensão de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="604ef-464">Total number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, which form this storage extent.</span></span> <span data-ttu-id="604ef-465">O tamanho total da extensão de armazenamento pode ser calculado multiplicando o valor da propriedade **BlockSize** pelo valor dessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="604ef-465">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="604ef-466">Se o valor de **BlockSize** for 1, essa propriedade será o tamanho total da extensão de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="604ef-466">If the value of **BlockSize** is 1, this property is the total size of the storage extent.</span></span>

<span data-ttu-id="604ef-467">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="604ef-467">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

<span data-ttu-id="604ef-468">Essa propriedade é herdada do [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="604ef-468">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="604ef-469">**OtherErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="604ef-469">**OtherErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="604ef-470">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="604ef-470">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="604ef-471">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="604ef-471">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="604ef-472">Qualificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ memória CIM**](cim-memory.md).**ErrorInfo**"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" SMBIOS ")</span><span class="sxs-lookup"><span data-stu-id="604ef-472">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Memory**](cim-memory.md).**ErrorInfo**"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS")</span></span>
</dt> </dl>

<span data-ttu-id="604ef-473">Cadeia de caracteres de forma livre que fornece mais informações se a propriedade **ErrorType** estiver definida como 1; caso contrário, essa cadeia de caracteres não tem significado.</span><span class="sxs-lookup"><span data-stu-id="604ef-473">Free-form string that provides more information if the **ErrorType** property is set to 1; otherwise, this string has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="604ef-474">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="604ef-474">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="604ef-475">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="604ef-475">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="604ef-476">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="604ef-476">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="604ef-477">Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="604ef-477">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="604ef-478">Identificador de dispositivo do Windows Plug and Play do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="604ef-478">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="604ef-479">Exemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="604ef-479">Example: "\*PNP030b"</span></span>

<span data-ttu-id="604ef-480">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="604ef-480">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="604ef-481">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="604ef-481">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="604ef-482">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="604ef-482">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="604ef-483">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="604ef-483">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="604ef-484">Matriz de recursos específicos relacionados à energia de um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="604ef-484">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="604ef-485">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="604ef-485">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="604ef-486"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="604ef-486"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="604ef-487"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="604ef-487"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="604ef-488"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="604ef-488"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="604ef-489"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="604ef-489"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="604ef-490">Os recursos de gerenciamento de energia estão habilitados no momento, mas o conjunto de recursos exato é desconhecido ou as informações não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="604ef-490">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="604ef-491"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de economia de energia inseridos automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="604ef-491"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="604ef-492">O dispositivo pode alterar seu estado de energia com base no uso ou em outros critérios.</span><span class="sxs-lookup"><span data-stu-id="604ef-492">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="604ef-493"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energia configurável** (5)</span><span class="sxs-lookup"><span data-stu-id="604ef-493"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="604ef-494">Há suporte para o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="604ef-494">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="604ef-495">Esse método é encontrado na classe pai **de \_ LogicalDevice CIM** e pode ser implementado.</span><span class="sxs-lookup"><span data-stu-id="604ef-495">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="604ef-496">Para obter mais informações, consulte [Designing formato MOF (MOF) classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="604ef-496">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="604ef-497"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energia com suporte** (6)</span><span class="sxs-lookup"><span data-stu-id="604ef-497"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="604ef-498">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia).</span><span class="sxs-lookup"><span data-stu-id="604ef-498">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="604ef-499"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Energia cronometrada com suporte** (7)</span><span class="sxs-lookup"><span data-stu-id="604ef-499"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="604ef-500">Tempo Power-On com suporte</span><span class="sxs-lookup"><span data-stu-id="604ef-500">Timed Power-On Supported</span></span>

<span data-ttu-id="604ef-501">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia) e o *tempo* definido como uma data e hora e um intervalo específicos para o Power-on.</span><span class="sxs-lookup"><span data-stu-id="604ef-501">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="604ef-502">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="604ef-502">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="604ef-503">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="604ef-503">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="604ef-504">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="604ef-504">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="604ef-505">Se **for true**, o dispositivo poderá ser gerenciado por energia (pode ser colocado no modo de suspensão e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="604ef-505">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="604ef-506">A propriedade não indica que os recursos de gerenciamento de energia estão habilitados no momento, apenas que o dispositivo lógico é capaz de gerenciamento de energia.</span><span class="sxs-lookup"><span data-stu-id="604ef-506">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="604ef-507">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="604ef-507">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="604ef-508">**Finalidade**</span><span class="sxs-lookup"><span data-stu-id="604ef-508">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="604ef-509">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="604ef-509">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="604ef-510">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="604ef-510">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="604ef-511">Cadeia de caracteres de forma livre que descreve a mídia e seu uso.</span><span class="sxs-lookup"><span data-stu-id="604ef-511">Free-form string describing the media and its use.</span></span>

<span data-ttu-id="604ef-512">Essa propriedade é herdada do [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="604ef-512">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="604ef-513">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="604ef-513">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="604ef-514">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="604ef-514">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="604ef-515">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="604ef-515">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="604ef-516">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("tipo de SMBIOS \| 19 \| endereços mapeados de dispositivo de memória \| iniciando endereço")</span><span class="sxs-lookup"><span data-stu-id="604ef-516">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 19\|Memory Device Mapped Addresses\|Starting Address")</span></span>
</dt> </dl>

<span data-ttu-id="604ef-517">Endereço inicial referenciado por um aplicativo ou sistema operacional e mapeado por um controlador de memória para esse objeto de memória.</span><span class="sxs-lookup"><span data-stu-id="604ef-517">Beginning address that is referenced by an application or operating system, and mapped by a memory controller for this memory object.</span></span> <span data-ttu-id="604ef-518">O endereço inicial é especificado em kilobytes.</span><span class="sxs-lookup"><span data-stu-id="604ef-518">The starting address is specified in kilobytes.</span></span>

<span data-ttu-id="604ef-519">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="604ef-519">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="604ef-520">**Status**</span><span class="sxs-lookup"><span data-stu-id="604ef-520">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="604ef-521">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="604ef-521">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="604ef-522">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="604ef-522">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="604ef-523">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="604ef-523">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="604ef-524">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="604ef-524">Current status of the object.</span></span> <span data-ttu-id="604ef-525">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="604ef-525">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="604ef-526">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="604ef-526">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="604ef-527">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="604ef-527">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="604ef-528">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="604ef-528">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="604ef-529">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="604ef-529">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="604ef-530">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="604ef-530">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="604ef-531">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="604ef-531">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="604ef-532">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="604ef-532">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="604ef-533">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="604ef-533">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="604ef-534">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="604ef-534">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="604ef-535">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="604ef-535">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="604ef-536">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="604ef-536">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="604ef-537">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="604ef-537">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="604ef-538">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="604ef-538">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="604ef-539">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="604ef-539">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="604ef-540">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="604ef-540">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="604ef-541">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="604ef-541">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="604ef-542">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="604ef-542">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="604ef-543">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="604ef-543">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="604ef-544">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="604ef-544">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="604ef-545">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="604ef-545">Data type: **uint16e**</span></span>
</dt> <dt>

<span data-ttu-id="604ef-546">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="604ef-546">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="604ef-547">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Estado operacional da DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="604ef-547">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="604ef-548">Estado do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="604ef-548">State of the logical device.</span></span> <span data-ttu-id="604ef-549">Se essa propriedade não se aplicar ao dispositivo lógico, o valor 5 (não aplicável) deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="604ef-549">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="604ef-550">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="604ef-550">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="604ef-551">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="604ef-551">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="604ef-552">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="604ef-552">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="604ef-553">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="604ef-553">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="604ef-554">**Desabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="604ef-554">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="604ef-555">**Não aplicável** (5)</span><span class="sxs-lookup"><span data-stu-id="604ef-555">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="604ef-556">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="604ef-556">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="604ef-557">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="604ef-557">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="604ef-558">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="604ef-558">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="604ef-559">Qualificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="604ef-559">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="604ef-560">Valor da propriedade **CreationClassName** do computador de escopo.</span><span class="sxs-lookup"><span data-stu-id="604ef-560">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="604ef-561">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="604ef-561">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="604ef-562">**SystemLevelAddress**</span><span class="sxs-lookup"><span data-stu-id="604ef-562">**SystemLevelAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="604ef-563">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="604ef-563">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="604ef-564">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="604ef-564">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="604ef-565">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("tipo de SMBIOS \| 18 \| 32-bit erro de memória informações de erro \| endereço")</span><span class="sxs-lookup"><span data-stu-id="604ef-565">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Address")</span></span>
</dt> </dl>

<span data-ttu-id="604ef-566">Se **for true**, as informações de endereço na propriedade **ErrorAddress** serão um endereço de nível de sistema.</span><span class="sxs-lookup"><span data-stu-id="604ef-566">If **TRUE**, the address information in the **ErrorAddress** property is a system-level address.</span></span> <span data-ttu-id="604ef-567">Se for **false**, será um endereço físico.</span><span class="sxs-lookup"><span data-stu-id="604ef-567">If **FALSE**, it is a physical address.</span></span> <span data-ttu-id="604ef-568">Se a propriedade **errorInfo** for igual a 3 (OK), essa propriedade não terá significado.</span><span class="sxs-lookup"><span data-stu-id="604ef-568">If the **ErrorInfo** property is equal to 3 (OK), then this property has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="604ef-569">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="604ef-569">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="604ef-570">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="604ef-570">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="604ef-571">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="604ef-571">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="604ef-572">Qualificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="604ef-572">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="604ef-573">Nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="604ef-573">Name of the scoping system.</span></span>

<span data-ttu-id="604ef-574">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="604ef-574">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="604ef-575">Comentários</span><span class="sxs-lookup"><span data-stu-id="604ef-575">Remarks</span></span>

<span data-ttu-id="604ef-576">A classe **Win32 \_ SMBIOSMemory** é derivada de [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="604ef-576">The **Win32\_SMBIOSMemory** class is derived from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="604ef-577">Requisitos</span><span class="sxs-lookup"><span data-stu-id="604ef-577">Requirements</span></span>



| <span data-ttu-id="604ef-578">Requisito</span><span class="sxs-lookup"><span data-stu-id="604ef-578">Requirement</span></span> | <span data-ttu-id="604ef-579">Valor</span><span class="sxs-lookup"><span data-stu-id="604ef-579">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="604ef-580">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="604ef-580">Minimum supported client</span></span><br/> | <span data-ttu-id="604ef-581">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="604ef-581">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="604ef-582">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="604ef-582">Minimum supported server</span></span><br/> | <span data-ttu-id="604ef-583">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="604ef-583">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="604ef-584">Namespace</span><span class="sxs-lookup"><span data-stu-id="604ef-584">Namespace</span></span><br/>                | <span data-ttu-id="604ef-585">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="604ef-585">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="604ef-586">MOF</span><span class="sxs-lookup"><span data-stu-id="604ef-586">MOF</span></span><br/>                      | <dl> <span data-ttu-id="604ef-587"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="604ef-587"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="604ef-588">DLL</span><span class="sxs-lookup"><span data-stu-id="604ef-588">DLL</span></span><br/>                      | <dl> <span data-ttu-id="604ef-589"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="604ef-589"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="604ef-590">Confira também</span><span class="sxs-lookup"><span data-stu-id="604ef-590">See also</span></span>

<dl> <dt>

[<span data-ttu-id="604ef-591">**\_STORAGEEXTENT CIM**</span><span class="sxs-lookup"><span data-stu-id="604ef-591">**CIM\_StorageExtent**</span></span>](cim-storageextent.md)
</dt> <dt>

[<span data-ttu-id="604ef-592">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="604ef-592">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
