---
description: A \_ classe WMI MemoryDevice do Win32 representa as propriedades de um dispositivo de memória do sistema de computador e seus endereços mapeados associados.
ms.assetid: d609dca5-2f5f-4f23-8fcc-bcc197d6c24b
ms.tgt_platform: multiple
title: Classe Win32_MemoryDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_MemoryDevice
- Win32_MemoryDevice.Reset
- Win32_MemoryDevice.SetPowerState
- Win32_MemoryDevice.Access
- Win32_MemoryDevice.AdditionalErrorData
- Win32_MemoryDevice.Availability
- Win32_MemoryDevice.BlockSize
- Win32_MemoryDevice.Caption
- Win32_MemoryDevice.ConfigManagerErrorCode
- Win32_MemoryDevice.ConfigManagerUserConfig
- Win32_MemoryDevice.CorrectableError
- Win32_MemoryDevice.CreationClassName
- Win32_MemoryDevice.Description
- Win32_MemoryDevice.DeviceID
- Win32_MemoryDevice.EndingAddress
- Win32_MemoryDevice.ErrorAccess
- Win32_MemoryDevice.ErrorAddress
- Win32_MemoryDevice.ErrorCleared
- Win32_MemoryDevice.ErrorData
- Win32_MemoryDevice.ErrorDataOrder
- Win32_MemoryDevice.ErrorDescription
- Win32_MemoryDevice.ErrorGranularity
- Win32_MemoryDevice.ErrorInfo
- Win32_MemoryDevice.ErrorMethodology
- Win32_MemoryDevice.ErrorResolution
- Win32_MemoryDevice.ErrorTime
- Win32_MemoryDevice.ErrorTransferSize
- Win32_MemoryDevice.InstallDate
- Win32_MemoryDevice.LastErrorCode
- Win32_MemoryDevice.Name
- Win32_MemoryDevice.NumberOfBlocks
- Win32_MemoryDevice.OtherErrorDescription
- Win32_MemoryDevice.PNPDeviceID
- Win32_MemoryDevice.PowerManagementCapabilities
- Win32_MemoryDevice.PowerManagementSupported
- Win32_MemoryDevice.Purpose
- Win32_MemoryDevice.StartingAddress
- Win32_MemoryDevice.Status
- Win32_MemoryDevice.StatusInfo
- Win32_MemoryDevice.SystemCreationClassName
- Win32_MemoryDevice.SystemLevelAddress
- Win32_MemoryDevice.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 277b868f1b92b9f7c6a0c520c77ab76fac6b544d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920213"
---
# <a name="win32_memorydevice-class"></a><span data-ttu-id="1c627-103">\_Classe Win32 MemoryDevice</span><span class="sxs-lookup"><span data-stu-id="1c627-103">Win32\_MemoryDevice class</span></span>

<span data-ttu-id="1c627-104">A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ MemoryDevice do Win32** representa as propriedades de um dispositivo de memória do sistema de computador e seus endereços mapeados associados.</span><span class="sxs-lookup"><span data-stu-id="1c627-104">The **Win32\_MemoryDevice** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the properties of a computer system memory device and its associated mapped addresses.</span></span>

<span data-ttu-id="1c627-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="1c627-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="1c627-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="1c627-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c627-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1c627-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B9B-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_MemoryDevice : Win32_SMBIOSMemory
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
  uint16   ErrorGranularity;
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
  uint16   StatusInfo;
  string   SystemCreationClassName;
  boolean  SystemLevelAddress;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="1c627-108">Membros</span><span class="sxs-lookup"><span data-stu-id="1c627-108">Members</span></span>

<span data-ttu-id="1c627-109">A classe **Win32 \_ MemoryDevice** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="1c627-109">The **Win32\_MemoryDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="1c627-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="1c627-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="1c627-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1c627-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="1c627-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="1c627-112">Methods</span></span>

<span data-ttu-id="1c627-113">A classe **Win32 \_ MemoryDevice** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="1c627-113">The **Win32\_MemoryDevice** class has these methods.</span></span>



| <span data-ttu-id="1c627-114">Método</span><span class="sxs-lookup"><span data-stu-id="1c627-114">Method</span></span>            | <span data-ttu-id="1c627-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="1c627-115">Description</span></span>                                                                                                                                                                                      |
|:------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c627-116">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="1c627-116">**Reset**</span></span>         | <span data-ttu-id="1c627-117">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="1c627-117">Not implemented.</span></span> <span data-ttu-id="1c627-118">Para implementar esse método, consulte o método [**Reset**](reset-method-in-class-cim-controller.md) no [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="1c627-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span><br/>                 |
| <span data-ttu-id="1c627-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="1c627-119">**SetPowerState**</span></span> | <span data-ttu-id="1c627-120">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="1c627-120">Not implemented.</span></span> <span data-ttu-id="1c627-121">Para implementar esse método, consulte o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) no [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="1c627-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="1c627-122">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1c627-122">Properties</span></span>

<span data-ttu-id="1c627-123">A classe **Win32 \_ MemoryDevice** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="1c627-123">The **Win32\_MemoryDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1c627-124">**Acesso**</span><span class="sxs-lookup"><span data-stu-id="1c627-124">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c627-125">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1c627-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1c627-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1c627-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c627-127">Acesso à mídia disponível.</span><span class="sxs-lookup"><span data-stu-id="1c627-127">Media access available.</span></span>

<span data-ttu-id="1c627-128">Essa propriedade é herdada do [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="1c627-128">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1c627-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="1c627-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="1c627-130"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Legível** (1)</span><span class="sxs-lookup"><span data-stu-id="1c627-130"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="1c627-131"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Gravável** (2)</span><span class="sxs-lookup"><span data-stu-id="1c627-131"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Writeable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="1c627-132">Gravável</span><span class="sxs-lookup"><span data-stu-id="1c627-132">Writable</span></span>

</dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="1c627-133"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Suporte de leitura/gravação** (3)</span><span class="sxs-lookup"><span data-stu-id="1c627-133"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="1c627-134"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Gravar uma vez** (4)</span><span class="sxs-lookup"><span data-stu-id="1c627-134"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1c627-135">**AdditionalErrorData**</span><span class="sxs-lookup"><span data-stu-id="1c627-135">**AdditionalErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c627-136">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="1c627-136">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="1c627-137">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1c627-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c627-138">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("tipo de SMBIOS \| 18 \| 32-bit de informação de erro de memória- \| síndrome do fornecedor"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="1c627-138">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Vendor Syndrome"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="1c627-139">Matriz de informações de erro adicionais.</span><span class="sxs-lookup"><span data-stu-id="1c627-139">Array of additional error information.</span></span> <span data-ttu-id="1c627-140">Um exemplo é a verificação de erros e a síndrome de correção (ECC) ou o retorno dos bits de verificação se uma metodologia de erro baseada em CRC (verificação de redundância cíclica) for usada.</span><span class="sxs-lookup"><span data-stu-id="1c627-140">An example is Error Checking and Correcting (ECC) Syndrome, or the return of the check bits if a cyclical redundancy check (CRC) based error methodology is used.</span></span> <span data-ttu-id="1c627-141">No último caso, se um erro de bit único for reconhecido e o algoritmo CRC for conhecido, será possível determinar o bit exato que falhou.</span><span class="sxs-lookup"><span data-stu-id="1c627-141">In the latter case, if a single-bit error is recognized and the CRC algorithm is known, it is possible to determine the exact bit that failed.</span></span> <span data-ttu-id="1c627-142">Esse tipo de dados (síndrome de ECC, bit de verificação, dados de bits de paridade ou outras informações fornecidas pelo fornecedor) está incluído neste campo.</span><span class="sxs-lookup"><span data-stu-id="1c627-142">This type of data (ECC Syndrome, Check Bit, Parity Bit data, or other vendor-supplied information) is included in this field.</span></span> <span data-ttu-id="1c627-143">Essa propriedade é usada somente quando a propriedade **errorInfo** não é igual a 3.</span><span class="sxs-lookup"><span data-stu-id="1c627-143">This property is used only when the **ErrorInfo** property is not equal to 3.</span></span>

<span data-ttu-id="1c627-144">Esta propriedade é herdada do [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="1c627-144">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c627-145">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="1c627-145">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c627-146">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1c627-146">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1c627-147">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1c627-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c627-148">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="1c627-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="1c627-149">Disponibilidade e status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1c627-149">Availability and status of the device.</span></span>

<span data-ttu-id="1c627-150">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="1c627-150">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1c627-151"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="1c627-151"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1c627-152"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="1c627-152"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="1c627-153"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Execução/energia completa** (3)</span><span class="sxs-lookup"><span data-stu-id="1c627-153"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="1c627-154">Energia completa ou em execução</span><span class="sxs-lookup"><span data-stu-id="1c627-154">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="1c627-155"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Aviso** (4)</span><span class="sxs-lookup"><span data-stu-id="1c627-155"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="1c627-156"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (5)</span><span class="sxs-lookup"><span data-stu-id="1c627-156"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="1c627-157"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (6)</span><span class="sxs-lookup"><span data-stu-id="1c627-157"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="1c627-158"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desligar (7** )</span><span class="sxs-lookup"><span data-stu-id="1c627-158"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="1c627-159"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off line** (8)</span><span class="sxs-lookup"><span data-stu-id="1c627-159"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="1c627-160"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fora do imposto** (9)</span><span class="sxs-lookup"><span data-stu-id="1c627-160"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="1c627-161"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="1c627-161"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="1c627-162"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Não instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="1c627-162"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="1c627-163"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erro de instalação** (12)</span><span class="sxs-lookup"><span data-stu-id="1c627-163"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="1c627-164"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Economia **de energia-desconhecido** (13)</span><span class="sxs-lookup"><span data-stu-id="1c627-164"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="1c627-165">O dispositivo é conhecido por estar em um modo de economia de energia, mas seu status exato é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="1c627-165">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="1c627-166"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Economia **de energia-modo de baixa energia** (14)</span><span class="sxs-lookup"><span data-stu-id="1c627-166"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="1c627-167">O dispositivo está em um estado de economia de energia, mas ainda está funcionando e pode exibir o desempenho degradado.</span><span class="sxs-lookup"><span data-stu-id="1c627-167">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="1c627-168"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save-em espera** (15)</span><span class="sxs-lookup"><span data-stu-id="1c627-168"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="1c627-169">O dispositivo não está funcionando, mas pode ser levado a uma potência completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="1c627-169">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="1c627-170"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energia** (16)</span><span class="sxs-lookup"><span data-stu-id="1c627-170"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="1c627-171"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Economia **de energia-aviso** (17)</span><span class="sxs-lookup"><span data-stu-id="1c627-171"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="1c627-172">O dispositivo está em um estado de aviso, embora também esteja em um modo de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="1c627-172">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="1c627-173"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>Em **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="1c627-173"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="1c627-174">O dispositivo está em pausa.</span><span class="sxs-lookup"><span data-stu-id="1c627-174">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="1c627-175"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Não pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="1c627-175"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="1c627-176">O dispositivo não está pronto.</span><span class="sxs-lookup"><span data-stu-id="1c627-176">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="1c627-177"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Não configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="1c627-177"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="1c627-178">O dispositivo não está configurado.</span><span class="sxs-lookup"><span data-stu-id="1c627-178">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="1c627-179"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Desativado** (21)</span><span class="sxs-lookup"><span data-stu-id="1c627-179"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="1c627-180">O dispositivo está silencioso.</span><span class="sxs-lookup"><span data-stu-id="1c627-180">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1c627-181">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="1c627-181">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c627-182">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1c627-182">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1c627-183">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1c627-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c627-184">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrStorageAllocationUnits "), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="1c627-184">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="1c627-185">Tamanho em bytes dos blocos que formam esta extensão de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="1c627-185">Size in bytes of the blocks that form this storage extent.</span></span> <span data-ttu-id="1c627-186">Se for desconhecido ou se um conceito de bloco não for válido (por exemplo, para extensões de agregação, memória ou discos lógicos), insira um 1.</span><span class="sxs-lookup"><span data-stu-id="1c627-186">If unknown or if a block concept is not valid (for example, for aggregate extents, memory or logical disks), enter a 1.</span></span>

<span data-ttu-id="1c627-187">Essa propriedade é herdada do [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="1c627-187">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="1c627-188">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="1c627-188">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="1c627-189">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="1c627-189">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c627-190">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1c627-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c627-191">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1c627-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c627-192">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="1c627-192">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="1c627-193">Breve descrição do objeto de uma cadeia de caracteres de uma linha.</span><span class="sxs-lookup"><span data-stu-id="1c627-193">Short description of the object a one-line string.</span></span>

<span data-ttu-id="1c627-194">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1c627-194">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c627-195">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="1c627-195">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c627-196">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1c627-196">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1c627-197">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1c627-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c627-198">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="1c627-198">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="1c627-199">Código de erro do Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="1c627-199">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="1c627-200">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="1c627-200">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="1c627-201"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo está funcionando corretamente.**</span><span class="sxs-lookup"><span data-stu-id="1c627-201"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="1c627-202"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="1c627-202">(0)</span></span>


</dt> <dd>

<span data-ttu-id="1c627-203">O dispositivo está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="1c627-203">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="1c627-204"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo não está configurado corretamente.**</span><span class="sxs-lookup"><span data-stu-id="1c627-204"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="1c627-205">(1)</span><span class="sxs-lookup"><span data-stu-id="1c627-205">(1)</span></span>


</dt> <dd>

<span data-ttu-id="1c627-206">O dispositivo não está configurado corretamente.</span><span class="sxs-lookup"><span data-stu-id="1c627-206">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="1c627-207"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**O Windows não pode carregar o driver para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="1c627-207"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="1c627-208">(2)</span><span class="sxs-lookup"><span data-stu-id="1c627-208">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="1c627-209"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.**</span><span class="sxs-lookup"><span data-stu-id="1c627-209"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="1c627-210">(3)</span><span class="sxs-lookup"><span data-stu-id="1c627-210">(3)</span></span>


</dt> <dd>

<span data-ttu-id="1c627-211">O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.</span><span class="sxs-lookup"><span data-stu-id="1c627-211">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="1c627-212"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo não está funcionando corretamente. Um de seus drivers ou seu registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="1c627-212"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="1c627-213">(4)</span><span class="sxs-lookup"><span data-stu-id="1c627-213">(4)</span></span>


</dt> <dd>

<span data-ttu-id="1c627-214">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="1c627-214">Device is not working properly.</span></span> <span data-ttu-id="1c627-215">Um de seus drivers ou o registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="1c627-215">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="1c627-216"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**O driver para este dispositivo precisa de um recurso que o Windows não possa gerenciar.**</span><span class="sxs-lookup"><span data-stu-id="1c627-216"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="1c627-217">(5)</span><span class="sxs-lookup"><span data-stu-id="1c627-217">(5)</span></span>


</dt> <dd>

<span data-ttu-id="1c627-218">O driver para o dispositivo requer um recurso que o Windows não pode gerenciar.</span><span class="sxs-lookup"><span data-stu-id="1c627-218">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="1c627-219"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**A configuração de inicialização para este dispositivo está em conflito com outros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="1c627-219"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="1c627-220"> (6)</span><span class="sxs-lookup"><span data-stu-id="1c627-220">(6)</span></span>


</dt> <dd>

<span data-ttu-id="1c627-221">A configuração de inicialização para o dispositivo está em conflito com outros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="1c627-221">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="1c627-222"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Não é possível filtrar.**</span><span class="sxs-lookup"><span data-stu-id="1c627-222"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="1c627-223">(7)</span><span class="sxs-lookup"><span data-stu-id="1c627-223">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="1c627-224"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**O carregador de driver para o dispositivo está ausente.**</span><span class="sxs-lookup"><span data-stu-id="1c627-224"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="1c627-225">(8)</span><span class="sxs-lookup"><span data-stu-id="1c627-225">(8)</span></span>


</dt> <dd>

<span data-ttu-id="1c627-226">O carregador de driver para o dispositivo está ausente.</span><span class="sxs-lookup"><span data-stu-id="1c627-226">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="1c627-227"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo não está funcionando corretamente porque o firmware de controle está relatando os recursos para o dispositivo incorretamente.**</span><span class="sxs-lookup"><span data-stu-id="1c627-227"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="1c627-228">(9)</span><span class="sxs-lookup"><span data-stu-id="1c627-228">(9)</span></span>


</dt> <dd>

<span data-ttu-id="1c627-229">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="1c627-229">Device is not working properly.</span></span> <span data-ttu-id="1c627-230">O firmware de controle está relatando incorretamente os recursos para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1c627-230">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="1c627-231"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo não pode ser iniciado.**</span><span class="sxs-lookup"><span data-stu-id="1c627-231"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="1c627-232">(10)</span><span class="sxs-lookup"><span data-stu-id="1c627-232">(10)</span></span>


</dt> <dd>

<span data-ttu-id="1c627-233">Não é possível iniciar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1c627-233">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="1c627-234"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Este dispositivo falhou.**</span><span class="sxs-lookup"><span data-stu-id="1c627-234"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="1c627-235">(11)</span><span class="sxs-lookup"><span data-stu-id="1c627-235">(11)</span></span>


</dt> <dd>

<span data-ttu-id="1c627-236">Falha no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1c627-236">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="1c627-237"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo não pode encontrar recursos livres suficientes que podem ser usados.**</span><span class="sxs-lookup"><span data-stu-id="1c627-237"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="1c627-238">12</span><span class="sxs-lookup"><span data-stu-id="1c627-238">(12)</span></span>


</dt> <dd>

<span data-ttu-id="1c627-239">O dispositivo não pode encontrar recursos livres suficientes para usar.</span><span class="sxs-lookup"><span data-stu-id="1c627-239">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="1c627-240"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**O Windows não pode verificar os recursos deste dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="1c627-240"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="1c627-241">(13)</span><span class="sxs-lookup"><span data-stu-id="1c627-241">(13)</span></span>


</dt> <dd>

<span data-ttu-id="1c627-242">O Windows não pode verificar os recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1c627-242">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="1c627-243"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo não funcionará corretamente até que você reinicie o computador.**</span><span class="sxs-lookup"><span data-stu-id="1c627-243"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="1c627-244">(14)</span><span class="sxs-lookup"><span data-stu-id="1c627-244">(14)</span></span>


</dt> <dd>

<span data-ttu-id="1c627-245">O dispositivo não funcionará corretamente até que o computador seja reiniciado.</span><span class="sxs-lookup"><span data-stu-id="1c627-245">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="1c627-246"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo não está funcionando corretamente porque provavelmente há um problema de nova enumeração.**</span><span class="sxs-lookup"><span data-stu-id="1c627-246"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="1c627-247">(15)</span><span class="sxs-lookup"><span data-stu-id="1c627-247">(15)</span></span>


</dt> <dd>

<span data-ttu-id="1c627-248">O dispositivo não está funcionando corretamente devido a um possível problema de reenumeração.</span><span class="sxs-lookup"><span data-stu-id="1c627-248">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="1c627-249"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**O Windows não pode identificar todos os recursos que este dispositivo usa.**</span><span class="sxs-lookup"><span data-stu-id="1c627-249"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="1c627-250">(16)</span><span class="sxs-lookup"><span data-stu-id="1c627-250">(16)</span></span>


</dt> <dd>

<span data-ttu-id="1c627-251">O Windows não pode identificar todos os recursos que o dispositivo usa.</span><span class="sxs-lookup"><span data-stu-id="1c627-251">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="1c627-252"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo está solicitando um tipo de recurso desconhecido.**</span><span class="sxs-lookup"><span data-stu-id="1c627-252"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="1c627-253">(17)</span><span class="sxs-lookup"><span data-stu-id="1c627-253">(17)</span></span>


</dt> <dd>

<span data-ttu-id="1c627-254">O dispositivo está solicitando um tipo de recurso desconhecido.</span><span class="sxs-lookup"><span data-stu-id="1c627-254">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="1c627-255"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstale os drivers para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="1c627-255"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="1c627-256">(18)</span><span class="sxs-lookup"><span data-stu-id="1c627-256">(18)</span></span>


</dt> <dd>

<span data-ttu-id="1c627-257">Os drivers de dispositivo devem ser reinstalados.</span><span class="sxs-lookup"><span data-stu-id="1c627-257">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="1c627-258"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Falha ao usar o carregador VxD.**</span><span class="sxs-lookup"><span data-stu-id="1c627-258"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="1c627-259">(19)</span><span class="sxs-lookup"><span data-stu-id="1c627-259">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="1c627-260"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**O registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="1c627-260"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="1c627-261">(20)</span><span class="sxs-lookup"><span data-stu-id="1c627-261">(20)</span></span>


</dt> <dd>

<span data-ttu-id="1c627-262">O registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="1c627-262">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="1c627-263"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware. O Windows está removendo este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="1c627-263"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="1c627-264">(21)</span><span class="sxs-lookup"><span data-stu-id="1c627-264">(21)</span></span>


</dt> <dd>

<span data-ttu-id="1c627-265">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="1c627-265">System failure.</span></span> <span data-ttu-id="1c627-266">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="1c627-266">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="1c627-267">O Windows está removendo o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1c627-267">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="1c627-268"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está desabilitado.**</span><span class="sxs-lookup"><span data-stu-id="1c627-268"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="1c627-269">(22)</span><span class="sxs-lookup"><span data-stu-id="1c627-269">(22)</span></span>


</dt> <dd>

<span data-ttu-id="1c627-270">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="1c627-270">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="1c627-271"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware.**</span><span class="sxs-lookup"><span data-stu-id="1c627-271"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="1c627-272">(23)</span><span class="sxs-lookup"><span data-stu-id="1c627-272">(23)</span></span>


</dt> <dd>

<span data-ttu-id="1c627-273">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="1c627-273">System failure.</span></span> <span data-ttu-id="1c627-274">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="1c627-274">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="1c627-275"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo não está presente, não está funcionando corretamente ou não tem todos os drivers instalados.**</span><span class="sxs-lookup"><span data-stu-id="1c627-275"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="1c627-276">(24)</span><span class="sxs-lookup"><span data-stu-id="1c627-276">(24)</span></span>


</dt> <dd>

<span data-ttu-id="1c627-277">O dispositivo não está presente, não está funcionando corretamente ou não tem todos os seus drivers instalados.</span><span class="sxs-lookup"><span data-stu-id="1c627-277">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="1c627-278"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="1c627-278"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="1c627-279">(25)</span><span class="sxs-lookup"><span data-stu-id="1c627-279">(25)</span></span>


</dt> <dd>

<span data-ttu-id="1c627-280">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1c627-280">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="1c627-281"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="1c627-281"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="1c627-282">(26)</span><span class="sxs-lookup"><span data-stu-id="1c627-282">(26)</span></span>


</dt> <dd>

<span data-ttu-id="1c627-283">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1c627-283">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="1c627-284"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo não tem uma configuração de log válida.**</span><span class="sxs-lookup"><span data-stu-id="1c627-284"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="1c627-285">(27)</span><span class="sxs-lookup"><span data-stu-id="1c627-285">(27)</span></span>


</dt> <dd>

<span data-ttu-id="1c627-286">O dispositivo não tem uma configuração de log válida.</span><span class="sxs-lookup"><span data-stu-id="1c627-286">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="1c627-287"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Os drivers para este dispositivo não estão instalados.**</span><span class="sxs-lookup"><span data-stu-id="1c627-287"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="1c627-288">(28)</span><span class="sxs-lookup"><span data-stu-id="1c627-288">(28)</span></span>


</dt> <dd>

<span data-ttu-id="1c627-289">Os drivers de dispositivo não estão instalados.</span><span class="sxs-lookup"><span data-stu-id="1c627-289">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="1c627-290"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está desabilitado porque o firmware do dispositivo não forneceu os recursos necessários.**</span><span class="sxs-lookup"><span data-stu-id="1c627-290"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="1c627-291">(29)</span><span class="sxs-lookup"><span data-stu-id="1c627-291">(29)</span></span>


</dt> <dd>

<span data-ttu-id="1c627-292">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="1c627-292">Device is disabled.</span></span> <span data-ttu-id="1c627-293">O firmware do dispositivo não forneceu os recursos necessários.</span><span class="sxs-lookup"><span data-stu-id="1c627-293">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="1c627-294"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo está usando um recurso de IRQ (solicitação de interrupção) que outro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="1c627-294"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="1c627-295">(30)</span><span class="sxs-lookup"><span data-stu-id="1c627-295">(30)</span></span>


</dt> <dd>

<span data-ttu-id="1c627-296">O dispositivo está usando um recurso de IRQ que outro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="1c627-296">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="1c627-297"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo não está funcionando corretamente porque o Windows não pode carregar os drivers necessários para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="1c627-297"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="1c627-298">(31)</span><span class="sxs-lookup"><span data-stu-id="1c627-298">(31)</span></span>


</dt> <dd>

<span data-ttu-id="1c627-299">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="1c627-299">Device is not working properly.</span></span> <span data-ttu-id="1c627-300">O Windows não pode carregar os drivers de dispositivo necessários.</span><span class="sxs-lookup"><span data-stu-id="1c627-300">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1c627-301">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="1c627-301">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c627-302">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="1c627-302">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1c627-303">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1c627-303">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c627-304">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="1c627-304">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="1c627-305">Se for **true**, o dispositivo estará usando uma configuração definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="1c627-305">If **True**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="1c627-306">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="1c627-306">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c627-307">**CorrectableError**</span><span class="sxs-lookup"><span data-stu-id="1c627-307">**CorrectableError**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c627-308">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="1c627-308">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1c627-309">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1c627-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c627-310">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("tipo de SMBIOS \| 18 \| 32-bit de erro informações de erro de memória \| ")</span><span class="sxs-lookup"><span data-stu-id="1c627-310">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Type")</span></span>
</dt> </dl>

<span data-ttu-id="1c627-311">Se **for true**, o erro mais recente era corrigível.</span><span class="sxs-lookup"><span data-stu-id="1c627-311">If **True**, the most recent error was correctable.</span></span> <span data-ttu-id="1c627-312">Essa propriedade não será usada se **errorInfo** estiver definida como 3.</span><span class="sxs-lookup"><span data-stu-id="1c627-312">This property is not used if **ErrorInfo** is set to 3.</span></span>

<span data-ttu-id="1c627-313">Esta propriedade é herdada do [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="1c627-313">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c627-314">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="1c627-314">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c627-315">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1c627-315">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c627-316">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1c627-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c627-317">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1c627-317">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1c627-318">Nome da primeira classe concreta a ser exibida na cadeia de herança usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="1c627-318">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="1c627-319">Quando usado com as outras propriedades de chave da classe, a propriedade permite que todas as instâncias dessa classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="1c627-319">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="1c627-320">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="1c627-320">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c627-321">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="1c627-321">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c627-322">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1c627-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c627-323">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1c627-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c627-324">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="1c627-324">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="1c627-325">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="1c627-325">Description of the object.</span></span>

<span data-ttu-id="1c627-326">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1c627-326">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c627-327">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="1c627-327">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c627-328">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1c627-328">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c627-329">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1c627-329">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c627-330">Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceID"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="1c627-330">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="1c627-331">Identificador exclusivo do dispositivo de memória.</span><span class="sxs-lookup"><span data-stu-id="1c627-331">Unique identifier of the memory device.</span></span>

<span data-ttu-id="1c627-332">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="1c627-332">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="1c627-333">Exemplo: "dispositivo de memória 1"</span><span class="sxs-lookup"><span data-stu-id="1c627-333">Example: "Memory Device 1"</span></span>

</dd> <dt>

<span data-ttu-id="1c627-334">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="1c627-334">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c627-335">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1c627-335">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1c627-336">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1c627-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c627-337">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("tipo de SMBIOS \| 19 \| endereços mapeados de dispositivo de memória \| endereço final")</span><span class="sxs-lookup"><span data-stu-id="1c627-337">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 19\|Memory Device Mapped Addresses\|Ending Address")</span></span>
</dt> </dl>

<span data-ttu-id="1c627-338">Endereço final referenciado por um aplicativo ou sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="1c627-338">Ending address referenced by an application or operating system.</span></span> <span data-ttu-id="1c627-339">Esse endereço de memória é mapeado por um controlador de memória para este objeto de memória.</span><span class="sxs-lookup"><span data-stu-id="1c627-339">This memory address is mapped by a memory controller for this memory object.</span></span>

<span data-ttu-id="1c627-340">Esta propriedade é herdada do [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="1c627-340">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<span data-ttu-id="1c627-341">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="1c627-341">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="1c627-342">**ErrorAccess**</span><span class="sxs-lookup"><span data-stu-id="1c627-342">**ErrorAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c627-343">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1c627-343">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1c627-344">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1c627-344">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c627-345">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("tipo de SMBIOS \| 18 \| 32-operação de erro de informações de erro de memória \| ")</span><span class="sxs-lookup"><span data-stu-id="1c627-345">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Operation")</span></span>
</dt> </dl>

<span data-ttu-id="1c627-346">Tipo de operação de acesso à memória que causou o último erro.</span><span class="sxs-lookup"><span data-stu-id="1c627-346">Type of memory access operation that caused the last error.</span></span> <span data-ttu-id="1c627-347">Essa propriedade é válida somente quando **errorInfo** não está definida como 3.</span><span class="sxs-lookup"><span data-stu-id="1c627-347">This property is valid only when **ErrorInfo** is not set to 3.</span></span>

<span data-ttu-id="1c627-348">Esta propriedade é herdada do [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="1c627-348">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1c627-349">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="1c627-349">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1c627-350">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="1c627-350">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="1c627-351">**Leitura** (3)</span><span class="sxs-lookup"><span data-stu-id="1c627-351">**Read** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

<span data-ttu-id="1c627-352">**Gravação** (4)</span><span class="sxs-lookup"><span data-stu-id="1c627-352">**Write** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>

<span data-ttu-id="1c627-353">**Gravação parcial** (5)</span><span class="sxs-lookup"><span data-stu-id="1c627-353">**Partial Write** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1c627-354">**ErrorAddress**</span><span class="sxs-lookup"><span data-stu-id="1c627-354">**ErrorAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c627-355">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1c627-355">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1c627-356">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1c627-356">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c627-357">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("tipo de SMBIOS \| 18 \| 32-bit erro de memória informações de erro \| endereço")</span><span class="sxs-lookup"><span data-stu-id="1c627-357">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Address")</span></span>
</dt> </dl>

<span data-ttu-id="1c627-358">Endereço do último erro de memória.</span><span class="sxs-lookup"><span data-stu-id="1c627-358">Address of the last memory error.</span></span> <span data-ttu-id="1c627-359">Essa propriedade é usada somente quando **errorInfo** não está definida como 3.</span><span class="sxs-lookup"><span data-stu-id="1c627-359">This property is used only when **ErrorInfo** is not set to 3.</span></span>

<span data-ttu-id="1c627-360">Esta propriedade é herdada do [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="1c627-360">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<span data-ttu-id="1c627-361">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="1c627-361">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="1c627-362">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="1c627-362">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c627-363">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="1c627-363">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1c627-364">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1c627-364">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c627-365">Se **for true**, o erro relatado em **LastErrorCode** agora será limpo.</span><span class="sxs-lookup"><span data-stu-id="1c627-365">If **True**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="1c627-366">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="1c627-366">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c627-367">**ErrorData**</span><span class="sxs-lookup"><span data-stu-id="1c627-367">**ErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c627-368">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="1c627-368">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="1c627-369">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1c627-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c627-370">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="1c627-370">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="1c627-371">Matriz de dados capturada do último acesso à memória com um erro.</span><span class="sxs-lookup"><span data-stu-id="1c627-371">Array of data captured from the last memory access with an error.</span></span> <span data-ttu-id="1c627-372">Os dados ocupam os primeiros *n* octetos da matriz necessários para manter o número de bits especificado pela propriedade **ErrorTransferSize** .</span><span class="sxs-lookup"><span data-stu-id="1c627-372">The data occupies the first *n* octets of the array necessary to hold the number of bits specified by the **ErrorTransferSize** property.</span></span> <span data-ttu-id="1c627-373">Se **ErrorTransferSize** for 0 (zero), essa propriedade não será usada.</span><span class="sxs-lookup"><span data-stu-id="1c627-373">If **ErrorTransferSize** is 0 (zero), then this property is not used.</span></span>

<span data-ttu-id="1c627-374">Esta propriedade é herdada do [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="1c627-374">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c627-375">**ErrorDataOrder**</span><span class="sxs-lookup"><span data-stu-id="1c627-375">**ErrorDataOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c627-376">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1c627-376">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1c627-377">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1c627-377">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c627-378">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="1c627-378">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="1c627-379">Ordenação de dados armazenados na propriedade **ErrorData** .</span><span class="sxs-lookup"><span data-stu-id="1c627-379">Ordering for data stored in the **ErrorData** property.</span></span> <span data-ttu-id="1c627-380">Essa propriedade é usada somente quando **ErrorTransferSize** é 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="1c627-380">This property is used only when **ErrorTransferSize** is 0 (zero).</span></span>

<span data-ttu-id="1c627-381">Esta propriedade é herdada do [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="1c627-381">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1c627-382">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="1c627-382">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="1c627-383">**Byte menos significativo primeiro** (1)</span><span class="sxs-lookup"><span data-stu-id="1c627-383">**Least Significant Byte First** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="1c627-384">**Byte mais significativo primeiro** (2)</span><span class="sxs-lookup"><span data-stu-id="1c627-384">**Most Significant Byte First** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1c627-385">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="1c627-385">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c627-386">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1c627-386">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c627-387">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1c627-387">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c627-388">Mais informações sobre o erro registrado em **LastErrorCode** e informações sobre as ações corretivas que podem ser executadas.</span><span class="sxs-lookup"><span data-stu-id="1c627-388">More information about the error recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="1c627-389">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="1c627-389">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c627-390">**ErrorGranularity**</span><span class="sxs-lookup"><span data-stu-id="1c627-390">**ErrorGranularity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c627-391">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1c627-391">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1c627-392">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1c627-392">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c627-393">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| tipo SMBIOS 18 \| granularidade de erro")</span><span class="sxs-lookup"><span data-stu-id="1c627-393">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|Error Granularity")</span></span>
</dt> </dl>

<span data-ttu-id="1c627-394">Nível em que o erro pode ser resolvido.</span><span class="sxs-lookup"><span data-stu-id="1c627-394">Level where the error can be resolved.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1c627-395">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="1c627-395">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1c627-396">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="1c627-396">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Device_level"></span><span id="device_level"></span><span id="DEVICE_LEVEL"></span>

<span data-ttu-id="1c627-397">**Nível do dispositivo** (3)</span><span class="sxs-lookup"><span data-stu-id="1c627-397">**Device level** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Memory_partition_level"></span><span id="memory_partition_level"></span><span id="MEMORY_PARTITION_LEVEL"></span>

<span data-ttu-id="1c627-398">**Nível de partição de memória** (4)</span><span class="sxs-lookup"><span data-stu-id="1c627-398">**Memory partition level** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1c627-399">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="1c627-399">**ErrorInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c627-400">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1c627-400">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1c627-401">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1c627-401">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c627-402">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ memória CIM**](cim-memory.md).**OtherErrorDescription**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" tipo de SMBIOS \| 18 \| 32-bit memória erro Information \| Type ")</span><span class="sxs-lookup"><span data-stu-id="1c627-402">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Memory**](cim-memory.md).**OtherErrorDescription**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Type")</span></span>
</dt> </dl>

<span data-ttu-id="1c627-403">Tipo de erro que ocorreu mais recentemente.</span><span class="sxs-lookup"><span data-stu-id="1c627-403">Type of error that occurred most recently.</span></span> <span data-ttu-id="1c627-404">Os valores 12-14, indicando se um erro é corrigível, não são usados com essa propriedade, mas essas informações são encontradas na propriedade **CorrectableError** .</span><span class="sxs-lookup"><span data-stu-id="1c627-404">The values 12-14, indicating whether an error is correctable, are not used with this property, but this information is found in the **CorrectableError** property.</span></span>

<span data-ttu-id="1c627-405">Esta propriedade é herdada do [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="1c627-405">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1c627-406">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="1c627-406">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1c627-407">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="1c627-407">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="1c627-408">**OK** (3)</span><span class="sxs-lookup"><span data-stu-id="1c627-408">**OK** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>

<span data-ttu-id="1c627-409">**Leitura inadequada** (4)</span><span class="sxs-lookup"><span data-stu-id="1c627-409">**Bad Read** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>

<span data-ttu-id="1c627-410">**Erro de paridade** (5)</span><span class="sxs-lookup"><span data-stu-id="1c627-410">**Parity Error** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>

<span data-ttu-id="1c627-411">**Erro de bit único** (6)</span><span class="sxs-lookup"><span data-stu-id="1c627-411">**Single-Bit Error** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>

<span data-ttu-id="1c627-412">**Erro de bit duplo** (7)</span><span class="sxs-lookup"><span data-stu-id="1c627-412">**Double-Bit Error** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>

<span data-ttu-id="1c627-413">**Erro de vários bits** (8)</span><span class="sxs-lookup"><span data-stu-id="1c627-413">**Multi-Bit Error** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>

<span data-ttu-id="1c627-414">**Erro de Nibble** (9)</span><span class="sxs-lookup"><span data-stu-id="1c627-414">**Nibble Error** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>

<span data-ttu-id="1c627-415">**Erro de soma de verificação** (10)</span><span class="sxs-lookup"><span data-stu-id="1c627-415">**Checksum Error** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>

<span data-ttu-id="1c627-416">**Erro de CRC** (11)</span><span class="sxs-lookup"><span data-stu-id="1c627-416">**CRC Error** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Corrected_single-bit_error"></span><span id="corrected_single-bit_error"></span><span id="CORRECTED_SINGLE-BIT_ERROR"></span>

<span data-ttu-id="1c627-417">**Erro de bit único corrigido** (12)</span><span class="sxs-lookup"><span data-stu-id="1c627-417">**Corrected single-bit error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Corrected_error"></span><span id="corrected_error"></span><span id="CORRECTED_ERROR"></span>

<span data-ttu-id="1c627-418">**Erro corrigido** (13)</span><span class="sxs-lookup"><span data-stu-id="1c627-418">**Corrected error** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Uncorrectable_error"></span><span id="uncorrectable_error"></span><span id="UNCORRECTABLE_ERROR"></span>

<span data-ttu-id="1c627-419">**Erro não corrigível** (14)</span><span class="sxs-lookup"><span data-stu-id="1c627-419">**Uncorrectable error** (14)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1c627-420">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="1c627-420">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c627-421">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1c627-421">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c627-422">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1c627-422">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c627-423">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("tipo do SMBIOS \| 16 \| correção de erro de memória da matriz de memória física \| ")</span><span class="sxs-lookup"><span data-stu-id="1c627-423">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 16\|Physical Memory Array\|Memory Error Correction")</span></span>
</dt> </dl>

<span data-ttu-id="1c627-424">Tipos de verificação de erros usados pelo hardware de memória.</span><span class="sxs-lookup"><span data-stu-id="1c627-424">Types of error checking used by the memory hardware.</span></span>

<span data-ttu-id="1c627-425">Essa propriedade é herdada do [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="1c627-425">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="1c627-426">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="1c627-426">The values are:</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1c627-427">**Outro** ("outro")</span><span class="sxs-lookup"><span data-stu-id="1c627-427">**Other** ("Other")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1c627-428">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="1c627-428">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>




</dt> <dd></dd> <dt>

<span id="Parity"></span><span id="parity"></span><span id="PARITY"></span>

<span data-ttu-id="1c627-429">**Paridade** ("paridade")</span><span class="sxs-lookup"><span data-stu-id="1c627-429">**Parity** ("Parity")</span></span>


</dt> <dd></dd> <dt>

<span id="Single-bit_ECC"></span><span id="single-bit_ecc"></span><span id="SINGLE-BIT_ECC"></span>

<span data-ttu-id="1c627-430">**ECC de bit único** ("ECC de bit único")</span><span class="sxs-lookup"><span data-stu-id="1c627-430">**Single-bit ECC** ("Single-bit ECC")</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-bit_ECC"></span><span id="multi-bit_ecc"></span><span id="MULTI-BIT_ECC"></span>

<span data-ttu-id="1c627-431">**ECC de vários bits** ("ECC de múltiplos bits")</span><span class="sxs-lookup"><span data-stu-id="1c627-431">**Multi-bit ECC** ("Multi-bit ECC")</span></span>


</dt> <dd></dd> <dt>




</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="1c627-432">**Nenhum** ("nenhum")</span><span class="sxs-lookup"><span data-stu-id="1c627-432">**None** ("None")</span></span>


</dt> <dd></dd> <dt>

<span id="CRC"></span><span id="crc"></span>

<span data-ttu-id="1c627-433">**CRC** ("CRC")</span><span class="sxs-lookup"><span data-stu-id="1c627-433">**CRC** ("CRC")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1c627-434">**ErrorResolution**</span><span class="sxs-lookup"><span data-stu-id="1c627-434">**ErrorResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c627-435">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1c627-435">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1c627-436">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1c627-436">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c627-437">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| tipo SMBIOS 18 \| 32-bit de erro de memória informações de \| resolução de erro"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="1c627-437">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Resolution"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="1c627-438">Quantidade de dados realmente determinados para causar o erro.</span><span class="sxs-lookup"><span data-stu-id="1c627-438">Amount of data actually determined to cause the error.</span></span> <span data-ttu-id="1c627-439">Essa propriedade não é usada quando a propriedade **errorInfo** está definida como 3.</span><span class="sxs-lookup"><span data-stu-id="1c627-439">This property is unused when the **ErrorInfo** property is set to 3.</span></span>

<span data-ttu-id="1c627-440">Esta propriedade é herdada do [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="1c627-440">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<span data-ttu-id="1c627-441">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="1c627-441">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="1c627-442">**ErrorTime**</span><span class="sxs-lookup"><span data-stu-id="1c627-442">**ErrorTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c627-443">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="1c627-443">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1c627-444">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1c627-444">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c627-445">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="1c627-445">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="1c627-446">Hora em que ocorreu o último erro de memória.</span><span class="sxs-lookup"><span data-stu-id="1c627-446">Time that the last memory error occurred.</span></span> <span data-ttu-id="1c627-447">Essa propriedade é válida somente quando **errorInfo** não está definida como 3.</span><span class="sxs-lookup"><span data-stu-id="1c627-447">This property is valid only when **ErrorInfo** is not set to 3.</span></span>

<span data-ttu-id="1c627-448">Esta propriedade é herdada do [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="1c627-448">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c627-449">**ErrorTransferSize**</span><span class="sxs-lookup"><span data-stu-id="1c627-449">**ErrorTransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c627-450">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1c627-450">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1c627-451">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1c627-451">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c627-452">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span><span class="sxs-lookup"><span data-stu-id="1c627-452">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="1c627-453">Tamanho dos dados (que contém o último erro) que estão sendo transferidos.</span><span class="sxs-lookup"><span data-stu-id="1c627-453">Size of the data (containing the last error) being transferred.</span></span> <span data-ttu-id="1c627-454">Essa propriedade será definida como 0 (zero) se não houver erro.</span><span class="sxs-lookup"><span data-stu-id="1c627-454">This property is set to 0 (zero) if there is no error.</span></span>

<span data-ttu-id="1c627-455">Esta propriedade é herdada do [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="1c627-455">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c627-456">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="1c627-456">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c627-457">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="1c627-457">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1c627-458">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1c627-458">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c627-459">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="1c627-459">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="1c627-460">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="1c627-460">Date and time the object was installed.</span></span> <span data-ttu-id="1c627-461">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="1c627-461">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="1c627-462">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1c627-462">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c627-463">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="1c627-463">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c627-464">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1c627-464">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1c627-465">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1c627-465">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c627-466">Código do último erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="1c627-466">Last error code reported by the logical device.</span></span>

<span data-ttu-id="1c627-467">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="1c627-467">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c627-468">**Nome**</span><span class="sxs-lookup"><span data-stu-id="1c627-468">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c627-469">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1c627-469">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c627-470">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1c627-470">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c627-471">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="1c627-471">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="1c627-472">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="1c627-472">Label by which the object is known.</span></span> <span data-ttu-id="1c627-473">Quando em uma subclasse, a propriedade pode ser substituída para ser uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="1c627-473">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="1c627-474">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1c627-474">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c627-475">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="1c627-475">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c627-476">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1c627-476">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1c627-477">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1c627-477">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c627-478">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrStorageSize ")</span><span class="sxs-lookup"><span data-stu-id="1c627-478">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="1c627-479">Número total de blocos consecutivos, cada um deles bloqueando o tamanho do valor contido na propriedade **BlockSize** , que formam essa extensão de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="1c627-479">Total number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, which form this storage extent.</span></span> <span data-ttu-id="1c627-480">O tamanho total da extensão de armazenamento pode ser calculado multiplicando o valor da propriedade **BlockSize** pelo valor dessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="1c627-480">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="1c627-481">Se o valor de **BlockSize** for 1, essa propriedade será o tamanho total da extensão de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="1c627-481">If the value of **BlockSize** is 1, this property is the total size of the storage extent.</span></span>

<span data-ttu-id="1c627-482">Essa propriedade é herdada do [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="1c627-482">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="1c627-483">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="1c627-483">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="1c627-484">**OtherErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="1c627-484">**OtherErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c627-485">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1c627-485">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c627-486">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1c627-486">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c627-487">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ memória CIM**](cim-memory.md).**ErrorInfo**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" SMBIOS ")</span><span class="sxs-lookup"><span data-stu-id="1c627-487">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Memory**](cim-memory.md).**ErrorInfo**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS")</span></span>
</dt> </dl>

<span data-ttu-id="1c627-488">Mais informações quando a propriedade **errorInfo** é definida como 1.</span><span class="sxs-lookup"><span data-stu-id="1c627-488">More information when the **ErrorInfo** property is set to 1.</span></span>

<span data-ttu-id="1c627-489">Esta propriedade é herdada do [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="1c627-489">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c627-490">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="1c627-490">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c627-491">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1c627-491">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c627-492">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1c627-492">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c627-493">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="1c627-493">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="1c627-494">Identificador de dispositivo do Windows Plug and Play do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="1c627-494">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="1c627-495">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="1c627-495">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="1c627-496">Exemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="1c627-496">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="1c627-497">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="1c627-497">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c627-498">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1c627-498">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1c627-499">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1c627-499">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c627-500">Matriz de recursos específicos relacionados à energia de um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="1c627-500">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="1c627-501">Essa propriedade é herdada **de \_ LogicalDevice CIM**.</span><span class="sxs-lookup"><span data-stu-id="1c627-501">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1c627-502"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="1c627-502"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="1c627-503"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="1c627-503"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="1c627-504"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="1c627-504"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="1c627-505"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="1c627-505"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="1c627-506">Os recursos de gerenciamento de energia estão habilitados no momento, mas o conjunto de recursos exato é desconhecido ou as informações não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="1c627-506">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="1c627-507"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de economia de energia inseridos automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="1c627-507"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="1c627-508">O dispositivo pode alterar seu estado de energia com base no uso ou em outros critérios.</span><span class="sxs-lookup"><span data-stu-id="1c627-508">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="1c627-509"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energia configurável** (5)</span><span class="sxs-lookup"><span data-stu-id="1c627-509"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="1c627-510">Há suporte para o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="1c627-510">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="1c627-511">Esse método é encontrado na classe pai **de \_ LogicalDevice CIM** e pode ser implementado.</span><span class="sxs-lookup"><span data-stu-id="1c627-511">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="1c627-512">Para obter mais informações, consulte [Designing formato MOF (MOF) classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="1c627-512">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="1c627-513"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energia com suporte** (6)</span><span class="sxs-lookup"><span data-stu-id="1c627-513"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="1c627-514">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia).</span><span class="sxs-lookup"><span data-stu-id="1c627-514">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="1c627-515"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Energia cronometrada com suporte** (7)</span><span class="sxs-lookup"><span data-stu-id="1c627-515"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="1c627-516">Tempo Power-On com suporte</span><span class="sxs-lookup"><span data-stu-id="1c627-516">Timed Power-On Supported</span></span>

<span data-ttu-id="1c627-517">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia) e o *tempo* definido como uma data e hora e um intervalo específicos para o Power-on.</span><span class="sxs-lookup"><span data-stu-id="1c627-517">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1c627-518">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="1c627-518">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c627-519">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="1c627-519">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1c627-520">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1c627-520">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c627-521">Se **for true**, o dispositivo poderá ser gerenciado por energia (pode ser colocado no modo de suspensão e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="1c627-521">If **True**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="1c627-522">A propriedade não indica que os recursos de gerenciamento de energia estão habilitados no momento, apenas que o dispositivo lógico é capaz de gerenciamento de energia.</span><span class="sxs-lookup"><span data-stu-id="1c627-522">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="1c627-523">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="1c627-523">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c627-524">**Finalidade**</span><span class="sxs-lookup"><span data-stu-id="1c627-524">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c627-525">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1c627-525">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c627-526">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1c627-526">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c627-527">Cadeia de caracteres de forma livre que descreve a mídia e seu uso.</span><span class="sxs-lookup"><span data-stu-id="1c627-527">Free-form string describing the media and its use.</span></span>

<span data-ttu-id="1c627-528">Essa propriedade é herdada do [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="1c627-528">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c627-529">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="1c627-529">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c627-530">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1c627-530">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1c627-531">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1c627-531">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c627-532">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("tipo de SMBIOS \| 19 \| endereços mapeados de dispositivo de memória \| iniciando endereço")</span><span class="sxs-lookup"><span data-stu-id="1c627-532">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 19\|Memory Device Mapped Addresses\|Starting Address")</span></span>
</dt> </dl>

<span data-ttu-id="1c627-533">Endereço inicial referenciado por um aplicativo ou pelo sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="1c627-533">Beginning address referenced by an application or the operating system.</span></span> <span data-ttu-id="1c627-534">Esse endereço de memória é mapeado por um controlador de memória para este objeto de memória.</span><span class="sxs-lookup"><span data-stu-id="1c627-534">This memory address is mapped by a memory controller for this memory object.</span></span>

<span data-ttu-id="1c627-535">Esta propriedade é herdada do [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="1c627-535">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<span data-ttu-id="1c627-536">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="1c627-536">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="1c627-537">**Status**</span><span class="sxs-lookup"><span data-stu-id="1c627-537">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c627-538">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1c627-538">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c627-539">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1c627-539">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c627-540">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="1c627-540">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="1c627-541">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="1c627-541">Current status of the object.</span></span> <span data-ttu-id="1c627-542">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="1c627-542">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="1c627-543">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="1c627-543">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="1c627-544">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="1c627-544">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="1c627-545">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="1c627-545">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="1c627-546">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="1c627-546">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="1c627-547">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1c627-547">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="1c627-548">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="1c627-548">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="1c627-549">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="1c627-549">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="1c627-550">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="1c627-550">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="1c627-551">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="1c627-551">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1c627-552">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="1c627-552">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="1c627-553">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="1c627-553">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="1c627-554">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="1c627-554">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="1c627-555">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="1c627-555">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="1c627-556">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="1c627-556">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="1c627-557">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="1c627-557">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="1c627-558">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="1c627-558">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="1c627-559">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="1c627-559">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="1c627-560">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="1c627-560">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1c627-561">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="1c627-561">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c627-562">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1c627-562">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1c627-563">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1c627-563">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c627-564">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="1c627-564">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="1c627-565">Estado do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="1c627-565">State of the logical device.</span></span> <span data-ttu-id="1c627-566">Se essa propriedade não se aplicar ao dispositivo lógico, o valor 5 (não aplicável) deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="1c627-566">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="1c627-567">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="1c627-567">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1c627-568">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="1c627-568">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1c627-569">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="1c627-569">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="1c627-570">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="1c627-570">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="1c627-571">**Desabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="1c627-571">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="1c627-572">**Não aplicável** (5)</span><span class="sxs-lookup"><span data-stu-id="1c627-572">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1c627-573">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="1c627-573">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c627-574">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1c627-574">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c627-575">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1c627-575">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c627-576">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1c627-576">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1c627-577">Valor da propriedade **CreationClassName** do computador de escopo.</span><span class="sxs-lookup"><span data-stu-id="1c627-577">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="1c627-578">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="1c627-578">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c627-579">**SystemLevelAddress**</span><span class="sxs-lookup"><span data-stu-id="1c627-579">**SystemLevelAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c627-580">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="1c627-580">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1c627-581">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1c627-581">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c627-582">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("tipo de SMBIOS \| 18 \| 32-bit erro de memória informações de erro \| endereço")</span><span class="sxs-lookup"><span data-stu-id="1c627-582">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Address")</span></span>
</dt> </dl>

<span data-ttu-id="1c627-583">Se **for true**, as informações de endereço na propriedade **ErrorAddress** serão um endereço de nível de sistema.</span><span class="sxs-lookup"><span data-stu-id="1c627-583">If **True**, the address information in the **ErrorAddress** property is a system-level address.</span></span> <span data-ttu-id="1c627-584">Se for **false**, será um endereço físico.</span><span class="sxs-lookup"><span data-stu-id="1c627-584">If **FALSE**, it is a physical address.</span></span> <span data-ttu-id="1c627-585">Essa propriedade é usada somente quando **errorInfo** não está definida como 3.</span><span class="sxs-lookup"><span data-stu-id="1c627-585">This property is used only when **ErrorInfo** is not set to 3.</span></span>

<span data-ttu-id="1c627-586">Esta propriedade é herdada do [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="1c627-586">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c627-587">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="1c627-587">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c627-588">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1c627-588">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c627-589">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1c627-589">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c627-590">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1c627-590">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1c627-591">Nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="1c627-591">Name of the scoping system.</span></span>

<span data-ttu-id="1c627-592">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="1c627-592">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1c627-593">Comentários</span><span class="sxs-lookup"><span data-stu-id="1c627-593">Remarks</span></span>

<span data-ttu-id="1c627-594">A classe **Win32 \_ MemoryDevice** é derivada de [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="1c627-594">The **Win32\_MemoryDevice** class is derived from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

## <a name="examples"></a><span data-ttu-id="1c627-595">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1c627-595">Examples</span></span>

<span data-ttu-id="1c627-596">A [lista de dispositivos de memória](https://Gallery.TechNet.Microsoft.Com/ddc9c2ab-3f88-44fb-935f-98da3bcf5858) de exemplo Perl retorna endereços inicial e final para todos os dispositivos de memória instalados em um computador.</span><span class="sxs-lookup"><span data-stu-id="1c627-596">The [List Memory Devices](https://Gallery.TechNet.Microsoft.Com/ddc9c2ab-3f88-44fb-935f-98da3bcf5858) Perl sample returns starting and ending addresses for all memory devices installed on a computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c627-597">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1c627-597">Requirements</span></span>



| <span data-ttu-id="1c627-598">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c627-598">Requirement</span></span> | <span data-ttu-id="1c627-599">Valor</span><span class="sxs-lookup"><span data-stu-id="1c627-599">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1c627-600">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1c627-600">Minimum supported client</span></span><br/> | <span data-ttu-id="1c627-601">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1c627-601">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1c627-602">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1c627-602">Minimum supported server</span></span><br/> | <span data-ttu-id="1c627-603">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1c627-603">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1c627-604">Namespace</span><span class="sxs-lookup"><span data-stu-id="1c627-604">Namespace</span></span><br/>                | <span data-ttu-id="1c627-605">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="1c627-605">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1c627-606">MOF</span><span class="sxs-lookup"><span data-stu-id="1c627-606">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1c627-607"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1c627-607"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1c627-608">DLL</span><span class="sxs-lookup"><span data-stu-id="1c627-608">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1c627-609"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c627-609"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c627-610">Confira também</span><span class="sxs-lookup"><span data-stu-id="1c627-610">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c627-611">**\_SMBIOSMemory Win32**</span><span class="sxs-lookup"><span data-stu-id="1c627-611">**Win32\_SMBIOSMemory**</span></span>](win32-smbiosmemory.md)
</dt> <dt>

[<span data-ttu-id="1c627-612">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="1c627-612">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

