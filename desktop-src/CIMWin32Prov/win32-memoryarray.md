---
description: A \_ classe WMI MemoryArray do Win32 representa as propriedades da matriz de memória do sistema de computador e os endereços mapeados.
ms.assetid: 56ff6960-cde3-4e34-b4df-d2993bafaa62
ms.tgt_platform: multiple
title: Classe Win32_MemoryArray
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_MemoryArray
- Win32_MemoryArray.Reset
- Win32_MemoryArray.SetPowerState
- Win32_MemoryArray.Access
- Win32_MemoryArray.AdditionalErrorData
- Win32_MemoryArray.Availability
- Win32_MemoryArray.BlockSize
- Win32_MemoryArray.Caption
- Win32_MemoryArray.ConfigManagerErrorCode
- Win32_MemoryArray.ConfigManagerUserConfig
- Win32_MemoryArray.CorrectableError
- Win32_MemoryArray.CreationClassName
- Win32_MemoryArray.Description
- Win32_MemoryArray.DeviceID
- Win32_MemoryArray.EndingAddress
- Win32_MemoryArray.ErrorAccess
- Win32_MemoryArray.ErrorAddress
- Win32_MemoryArray.ErrorCleared
- Win32_MemoryArray.ErrorData
- Win32_MemoryArray.ErrorDataOrder
- Win32_MemoryArray.ErrorDescription
- Win32_MemoryArray.ErrorGranularity
- Win32_MemoryArray.ErrorInfo
- Win32_MemoryArray.ErrorMethodology
- Win32_MemoryArray.ErrorResolution
- Win32_MemoryArray.ErrorTime
- Win32_MemoryArray.ErrorTransferSize
- Win32_MemoryArray.InstallDate
- Win32_MemoryArray.LastErrorCode
- Win32_MemoryArray.Name
- Win32_MemoryArray.NumberOfBlocks
- Win32_MemoryArray.OtherErrorDescription
- Win32_MemoryArray.PNPDeviceID
- Win32_MemoryArray.PowerManagementCapabilities
- Win32_MemoryArray.PowerManagementSupported
- Win32_MemoryArray.Purpose
- Win32_MemoryArray.StartingAddress
- Win32_MemoryArray.Status
- Win32_MemoryArray.StatusInfo
- Win32_MemoryArray.SystemCreationClassName
- Win32_MemoryArray.SystemLevelAddress
- Win32_MemoryArray.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c102d383502bec4808b26a87eb2f6d8445b6c2a8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164151"
---
# <a name="win32_memoryarray-class"></a><span data-ttu-id="c7c08-103">\_Classe Win32 MemoryArray</span><span class="sxs-lookup"><span data-stu-id="c7c08-103">Win32\_MemoryArray class</span></span>

<span data-ttu-id="c7c08-104">A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ MemoryArray do Win32** representa as propriedades da matriz de memória do sistema de computador e os endereços mapeados.</span><span class="sxs-lookup"><span data-stu-id="c7c08-104">The **Win32\_MemoryArray** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the properties of the computer system memory array and mapped addresses.</span></span>

<span data-ttu-id="c7c08-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="c7c08-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="c7c08-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="c7c08-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7c08-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c7c08-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B9A-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_MemoryArray : Win32_SMBIOSMemory
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

## <a name="members"></a><span data-ttu-id="c7c08-108">Membros</span><span class="sxs-lookup"><span data-stu-id="c7c08-108">Members</span></span>

<span data-ttu-id="c7c08-109">A classe **Win32 \_ MemoryArray** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="c7c08-109">The **Win32\_MemoryArray** class has these types of members:</span></span>

-   [<span data-ttu-id="c7c08-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="c7c08-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="c7c08-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c7c08-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c7c08-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="c7c08-112">Methods</span></span>

<span data-ttu-id="c7c08-113">A classe **Win32 \_ MemoryArray** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="c7c08-113">The **Win32\_MemoryArray** class has these methods.</span></span>



| <span data-ttu-id="c7c08-114">Método</span><span class="sxs-lookup"><span data-stu-id="c7c08-114">Method</span></span>            | <span data-ttu-id="c7c08-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="c7c08-115">Description</span></span>                                                                                                                                                                                                        |
|:------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7c08-116">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="c7c08-116">**Reset**</span></span>         | <span data-ttu-id="c7c08-117">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="c7c08-117">Not implemented.</span></span> <span data-ttu-id="c7c08-118">Para implementar esse método, consulte o método [**Reset**](reset-method-in-class-cim-controller.md) no [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md) para obter a documentação.</span><span class="sxs-lookup"><span data-stu-id="c7c08-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md) for documentation.</span></span><br/>                 |
| <span data-ttu-id="c7c08-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="c7c08-119">**SetPowerState**</span></span> | <span data-ttu-id="c7c08-120">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="c7c08-120">Not implemented.</span></span> <span data-ttu-id="c7c08-121">Para implementar esse método, consulte o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) no [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md) para obter a documentação.</span><span class="sxs-lookup"><span data-stu-id="c7c08-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md) for documentation.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="c7c08-122">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c7c08-122">Properties</span></span>

<span data-ttu-id="c7c08-123">A classe **Win32 \_ MemoryArray** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="c7c08-123">The **Win32\_MemoryArray** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c7c08-124">**Acesso**</span><span class="sxs-lookup"><span data-stu-id="c7c08-124">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7c08-125">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c7c08-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c7c08-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7c08-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c7c08-127">Tipo de acesso à mídia disponível.</span><span class="sxs-lookup"><span data-stu-id="c7c08-127">Type of media access available.</span></span>

<span data-ttu-id="c7c08-128">Essa propriedade é herdada do [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="c7c08-128">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c7c08-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="c7c08-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="c7c08-130"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Legível** (1)</span><span class="sxs-lookup"><span data-stu-id="c7c08-130"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="c7c08-131"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Gravável** (2)</span><span class="sxs-lookup"><span data-stu-id="c7c08-131"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Writeable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="c7c08-132">Gravável</span><span class="sxs-lookup"><span data-stu-id="c7c08-132">Writable</span></span>

</dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="c7c08-133"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Suporte de leitura/gravação** (3)</span><span class="sxs-lookup"><span data-stu-id="c7c08-133"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="c7c08-134"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Gravar uma vez** (4)</span><span class="sxs-lookup"><span data-stu-id="c7c08-134"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c7c08-135">**AdditionalErrorData**</span><span class="sxs-lookup"><span data-stu-id="c7c08-135">**AdditionalErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7c08-136">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="c7c08-136">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="c7c08-137">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7c08-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7c08-138">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("tipo de SMBIOS \| 18 \| 32-bit de informação de erro de memória- \| síndrome do fornecedor"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="c7c08-138">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Vendor Syndrome"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="c7c08-139">Matriz de informações de erro adicionais.</span><span class="sxs-lookup"><span data-stu-id="c7c08-139">Array of additional error information.</span></span> <span data-ttu-id="c7c08-140">Um exemplo é a verificação de erros e a síndrome de correção (ECC), ou o retorno dos bits de verificação se um valor de **ErrorMethodology** baseado em CRC (verificação de redundância cíclica) for usado.</span><span class="sxs-lookup"><span data-stu-id="c7c08-140">An example is Error Checking and Correcting (ECC) Syndrome, or the return of the check bits if a cyclical redundancy check (CRC) based **ErrorMethodology** value is used.</span></span> <span data-ttu-id="c7c08-141">No último caso, se um erro de bit único for reconhecido e o algoritmo CRC for conhecido, será possível determinar o bit exato que falhou.</span><span class="sxs-lookup"><span data-stu-id="c7c08-141">In the latter case, if a single-bit error is recognized and the CRC algorithm is known, it is possible to determine the exact bit that failed.</span></span> <span data-ttu-id="c7c08-142">Esse tipo de dados (síndrome de ECC, bit de verificação, dados de bits de paridade ou outras informações fornecidas pelo fornecedor) está incluído neste campo.</span><span class="sxs-lookup"><span data-stu-id="c7c08-142">This type of data (ECC Syndrome, Check Bit, Parity Bit data, or other vendor-supplied information) is included in this field.</span></span> <span data-ttu-id="c7c08-143">Essa propriedade é usada somente quando a propriedade **errorInfo** não é igual a 3.</span><span class="sxs-lookup"><span data-stu-id="c7c08-143">This property is used only when the **ErrorInfo** property is not equal to 3.</span></span>

<span data-ttu-id="c7c08-144">Esta propriedade é herdada do [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="c7c08-144">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="c7c08-145">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="c7c08-145">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7c08-146">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c7c08-146">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c7c08-147">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7c08-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7c08-148">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="c7c08-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="c7c08-149">Disponibilidade e status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c7c08-149">Availability and status of the device.</span></span>

<span data-ttu-id="c7c08-150">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c7c08-150">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c7c08-151"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="c7c08-151"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c7c08-152"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="c7c08-152"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="c7c08-153"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Execução/energia completa** (3)</span><span class="sxs-lookup"><span data-stu-id="c7c08-153"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="c7c08-154">Energia completa ou em execução</span><span class="sxs-lookup"><span data-stu-id="c7c08-154">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="c7c08-155"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Aviso** (4)</span><span class="sxs-lookup"><span data-stu-id="c7c08-155"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="c7c08-156"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (5)</span><span class="sxs-lookup"><span data-stu-id="c7c08-156"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="c7c08-157"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (6)</span><span class="sxs-lookup"><span data-stu-id="c7c08-157"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="c7c08-158"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desligar (7** )</span><span class="sxs-lookup"><span data-stu-id="c7c08-158"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="c7c08-159"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off line** (8)</span><span class="sxs-lookup"><span data-stu-id="c7c08-159"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="c7c08-160"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fora do imposto** (9)</span><span class="sxs-lookup"><span data-stu-id="c7c08-160"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="c7c08-161"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="c7c08-161"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="c7c08-162"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Não instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="c7c08-162"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="c7c08-163"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erro de instalação** (12)</span><span class="sxs-lookup"><span data-stu-id="c7c08-163"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="c7c08-164"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Economia **de energia-desconhecido** (13)</span><span class="sxs-lookup"><span data-stu-id="c7c08-164"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="c7c08-165">O dispositivo é conhecido por estar em um modo de economia de energia, mas seu status exato é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="c7c08-165">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="c7c08-166"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Economia **de energia-modo de baixa energia** (14)</span><span class="sxs-lookup"><span data-stu-id="c7c08-166"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="c7c08-167">O dispositivo está em um estado de economia de energia, mas ainda está funcionando e pode exibir o desempenho degradado.</span><span class="sxs-lookup"><span data-stu-id="c7c08-167">The device is in a power save state but is still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="c7c08-168"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save-em espera** (15)</span><span class="sxs-lookup"><span data-stu-id="c7c08-168"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="c7c08-169">O dispositivo não está funcionando, mas pode ser levado a uma potência completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="c7c08-169">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="c7c08-170"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energia** (16)</span><span class="sxs-lookup"><span data-stu-id="c7c08-170"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="c7c08-171"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Economia **de energia-aviso** (17)</span><span class="sxs-lookup"><span data-stu-id="c7c08-171"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="c7c08-172">O dispositivo está em um estado de aviso, embora também esteja em um modo de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="c7c08-172">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="c7c08-173"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>Em **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="c7c08-173"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="c7c08-174">O dispositivo está em pausa.</span><span class="sxs-lookup"><span data-stu-id="c7c08-174">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="c7c08-175"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Não pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="c7c08-175"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="c7c08-176">O dispositivo não está pronto.</span><span class="sxs-lookup"><span data-stu-id="c7c08-176">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="c7c08-177"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Não configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="c7c08-177"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="c7c08-178">O dispositivo não está configurado.</span><span class="sxs-lookup"><span data-stu-id="c7c08-178">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="c7c08-179"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Desativado** (21)</span><span class="sxs-lookup"><span data-stu-id="c7c08-179"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="c7c08-180">O dispositivo está silencioso.</span><span class="sxs-lookup"><span data-stu-id="c7c08-180">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c7c08-181">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="c7c08-181">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7c08-182">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c7c08-182">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c7c08-183">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7c08-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7c08-184">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrStorageAllocationUnits "), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="c7c08-184">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="c7c08-185">Tamanho em bytes dos blocos que formam esta extensão de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="c7c08-185">Size in bytes of the blocks that form this storage extent.</span></span> <span data-ttu-id="c7c08-186">Se for desconhecido ou se um conceito de bloco não for válido (por exemplo, para extensões de agregação, memória ou discos lógicos), insira um 1.</span><span class="sxs-lookup"><span data-stu-id="c7c08-186">If unknown or if a block concept is not valid (for example, for aggregate extents, memory or logical disks), enter a 1.</span></span>

<span data-ttu-id="c7c08-187">Essa propriedade é herdada do [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="c7c08-187">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="c7c08-188">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="c7c08-188">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="c7c08-189">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="c7c08-189">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7c08-190">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c7c08-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7c08-191">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7c08-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7c08-192">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="c7c08-192">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="c7c08-193">Breve descrição do objeto de uma cadeia de caracteres de uma linha.</span><span class="sxs-lookup"><span data-stu-id="c7c08-193">Short description of the object a one-line string.</span></span>

<span data-ttu-id="c7c08-194">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c7c08-194">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c7c08-195">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="c7c08-195">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7c08-196">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c7c08-196">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c7c08-197">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7c08-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7c08-198">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="c7c08-198">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="c7c08-199">Código de erro do Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="c7c08-199">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="c7c08-200">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c7c08-200">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="c7c08-201"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo está funcionando corretamente.**</span><span class="sxs-lookup"><span data-stu-id="c7c08-201"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="c7c08-202"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="c7c08-202">(0)</span></span>


</dt> <dd>

<span data-ttu-id="c7c08-203">O dispositivo está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="c7c08-203">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="c7c08-204"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo não está configurado corretamente.**</span><span class="sxs-lookup"><span data-stu-id="c7c08-204"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="c7c08-205">(1)</span><span class="sxs-lookup"><span data-stu-id="c7c08-205">(1)</span></span>


</dt> <dd>

<span data-ttu-id="c7c08-206">O dispositivo não está configurado corretamente.</span><span class="sxs-lookup"><span data-stu-id="c7c08-206">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="c7c08-207"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**O Windows não pode carregar o driver para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="c7c08-207"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="c7c08-208">(2)</span><span class="sxs-lookup"><span data-stu-id="c7c08-208">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="c7c08-209"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.**</span><span class="sxs-lookup"><span data-stu-id="c7c08-209"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="c7c08-210">(3)</span><span class="sxs-lookup"><span data-stu-id="c7c08-210">(3)</span></span>


</dt> <dd>

<span data-ttu-id="c7c08-211">O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.</span><span class="sxs-lookup"><span data-stu-id="c7c08-211">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="c7c08-212"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo não está funcionando corretamente. Um de seus drivers ou seu registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="c7c08-212"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="c7c08-213">(4)</span><span class="sxs-lookup"><span data-stu-id="c7c08-213">(4)</span></span>


</dt> <dd>

<span data-ttu-id="c7c08-214">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="c7c08-214">Device is not working properly.</span></span> <span data-ttu-id="c7c08-215">Um de seus drivers ou o registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="c7c08-215">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="c7c08-216"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**O driver para este dispositivo precisa de um recurso que o Windows não possa gerenciar.**</span><span class="sxs-lookup"><span data-stu-id="c7c08-216"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="c7c08-217">(5)</span><span class="sxs-lookup"><span data-stu-id="c7c08-217">(5)</span></span>


</dt> <dd>

<span data-ttu-id="c7c08-218">O driver para o dispositivo requer um recurso que o Windows não pode gerenciar.</span><span class="sxs-lookup"><span data-stu-id="c7c08-218">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="c7c08-219"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**A configuração de inicialização para este dispositivo está em conflito com outros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="c7c08-219"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="c7c08-220"> (6)</span><span class="sxs-lookup"><span data-stu-id="c7c08-220">(6)</span></span>


</dt> <dd>

<span data-ttu-id="c7c08-221">A configuração de inicialização para o dispositivo está em conflito com outros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="c7c08-221">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="c7c08-222"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Não é possível filtrar.**</span><span class="sxs-lookup"><span data-stu-id="c7c08-222"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="c7c08-223">(7)</span><span class="sxs-lookup"><span data-stu-id="c7c08-223">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="c7c08-224"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**O carregador de driver para o dispositivo está ausente.**</span><span class="sxs-lookup"><span data-stu-id="c7c08-224"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="c7c08-225">(8)</span><span class="sxs-lookup"><span data-stu-id="c7c08-225">(8)</span></span>


</dt> <dd>

<span data-ttu-id="c7c08-226">O carregador de driver para o dispositivo está ausente.</span><span class="sxs-lookup"><span data-stu-id="c7c08-226">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="c7c08-227"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo não está funcionando corretamente porque o firmware de controle está relatando os recursos para o dispositivo incorretamente.**</span><span class="sxs-lookup"><span data-stu-id="c7c08-227"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="c7c08-228">(9)</span><span class="sxs-lookup"><span data-stu-id="c7c08-228">(9)</span></span>


</dt> <dd>

<span data-ttu-id="c7c08-229">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="c7c08-229">Device is not working properly.</span></span> <span data-ttu-id="c7c08-230">O firmware de controle está relatando incorretamente os recursos para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c7c08-230">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="c7c08-231"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo não pode ser iniciado.**</span><span class="sxs-lookup"><span data-stu-id="c7c08-231"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="c7c08-232">(10)</span><span class="sxs-lookup"><span data-stu-id="c7c08-232">(10)</span></span>


</dt> <dd>

<span data-ttu-id="c7c08-233">Não é possível iniciar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c7c08-233">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="c7c08-234"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Este dispositivo falhou.**</span><span class="sxs-lookup"><span data-stu-id="c7c08-234"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="c7c08-235">(11)</span><span class="sxs-lookup"><span data-stu-id="c7c08-235">(11)</span></span>


</dt> <dd>

<span data-ttu-id="c7c08-236">Falha no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c7c08-236">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="c7c08-237"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo não pode encontrar recursos livres suficientes que podem ser usados.**</span><span class="sxs-lookup"><span data-stu-id="c7c08-237"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="c7c08-238">12</span><span class="sxs-lookup"><span data-stu-id="c7c08-238">(12)</span></span>


</dt> <dd>

<span data-ttu-id="c7c08-239">O dispositivo não pode encontrar recursos livres suficientes para usar.</span><span class="sxs-lookup"><span data-stu-id="c7c08-239">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="c7c08-240"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**O Windows não pode verificar os recursos deste dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="c7c08-240"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="c7c08-241">(13)</span><span class="sxs-lookup"><span data-stu-id="c7c08-241">(13)</span></span>


</dt> <dd>

<span data-ttu-id="c7c08-242">O Windows não pode verificar os recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c7c08-242">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="c7c08-243"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo não funcionará corretamente até que você reinicie o computador.**</span><span class="sxs-lookup"><span data-stu-id="c7c08-243"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="c7c08-244">(14)</span><span class="sxs-lookup"><span data-stu-id="c7c08-244">(14)</span></span>


</dt> <dd>

<span data-ttu-id="c7c08-245">O dispositivo não funcionará corretamente até que o computador seja reiniciado.</span><span class="sxs-lookup"><span data-stu-id="c7c08-245">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="c7c08-246"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo não está funcionando corretamente porque provavelmente há um problema de nova enumeração.**</span><span class="sxs-lookup"><span data-stu-id="c7c08-246"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="c7c08-247">(15)</span><span class="sxs-lookup"><span data-stu-id="c7c08-247">(15)</span></span>


</dt> <dd>

<span data-ttu-id="c7c08-248">O dispositivo não está funcionando corretamente devido a um possível problema de reenumeração.</span><span class="sxs-lookup"><span data-stu-id="c7c08-248">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="c7c08-249"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**O Windows não pode identificar todos os recursos que este dispositivo usa.**</span><span class="sxs-lookup"><span data-stu-id="c7c08-249"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="c7c08-250">(16)</span><span class="sxs-lookup"><span data-stu-id="c7c08-250">(16)</span></span>


</dt> <dd>

<span data-ttu-id="c7c08-251">O Windows não pode identificar todos os recursos que o dispositivo usa.</span><span class="sxs-lookup"><span data-stu-id="c7c08-251">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="c7c08-252"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo está solicitando um tipo de recurso desconhecido.**</span><span class="sxs-lookup"><span data-stu-id="c7c08-252"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="c7c08-253">(17)</span><span class="sxs-lookup"><span data-stu-id="c7c08-253">(17)</span></span>


</dt> <dd>

<span data-ttu-id="c7c08-254">O dispositivo está solicitando um tipo de recurso desconhecido.</span><span class="sxs-lookup"><span data-stu-id="c7c08-254">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="c7c08-255"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstale os drivers para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="c7c08-255"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="c7c08-256">(18)</span><span class="sxs-lookup"><span data-stu-id="c7c08-256">(18)</span></span>


</dt> <dd>

<span data-ttu-id="c7c08-257">Os drivers de dispositivo devem ser reinstalados.</span><span class="sxs-lookup"><span data-stu-id="c7c08-257">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="c7c08-258"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Falha ao usar o carregador VxD.**</span><span class="sxs-lookup"><span data-stu-id="c7c08-258"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="c7c08-259">(19)</span><span class="sxs-lookup"><span data-stu-id="c7c08-259">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="c7c08-260"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**O registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="c7c08-260"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="c7c08-261">(20)</span><span class="sxs-lookup"><span data-stu-id="c7c08-261">(20)</span></span>


</dt> <dd>

<span data-ttu-id="c7c08-262">O registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="c7c08-262">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="c7c08-263"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware. O Windows está removendo este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="c7c08-263"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="c7c08-264">(21)</span><span class="sxs-lookup"><span data-stu-id="c7c08-264">(21)</span></span>


</dt> <dd>

<span data-ttu-id="c7c08-265">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="c7c08-265">System failure.</span></span> <span data-ttu-id="c7c08-266">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="c7c08-266">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="c7c08-267">O Windows está removendo o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c7c08-267">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="c7c08-268"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está desabilitado.**</span><span class="sxs-lookup"><span data-stu-id="c7c08-268"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="c7c08-269">(22)</span><span class="sxs-lookup"><span data-stu-id="c7c08-269">(22)</span></span>


</dt> <dd>

<span data-ttu-id="c7c08-270">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="c7c08-270">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="c7c08-271"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware.**</span><span class="sxs-lookup"><span data-stu-id="c7c08-271"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="c7c08-272">(23)</span><span class="sxs-lookup"><span data-stu-id="c7c08-272">(23)</span></span>


</dt> <dd>

<span data-ttu-id="c7c08-273">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="c7c08-273">System failure.</span></span> <span data-ttu-id="c7c08-274">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="c7c08-274">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="c7c08-275"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo não está presente, não está funcionando corretamente ou não tem todos os drivers instalados.**</span><span class="sxs-lookup"><span data-stu-id="c7c08-275"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="c7c08-276">(24)</span><span class="sxs-lookup"><span data-stu-id="c7c08-276">(24)</span></span>


</dt> <dd>

<span data-ttu-id="c7c08-277">O dispositivo não está presente, não está funcionando corretamente ou não tem todos os seus drivers instalados.</span><span class="sxs-lookup"><span data-stu-id="c7c08-277">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="c7c08-278"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="c7c08-278"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="c7c08-279">(25)</span><span class="sxs-lookup"><span data-stu-id="c7c08-279">(25)</span></span>


</dt> <dd>

<span data-ttu-id="c7c08-280">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c7c08-280">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="c7c08-281"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="c7c08-281"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="c7c08-282">(26)</span><span class="sxs-lookup"><span data-stu-id="c7c08-282">(26)</span></span>


</dt> <dd>

<span data-ttu-id="c7c08-283">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c7c08-283">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="c7c08-284"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo não tem uma configuração de log válida.**</span><span class="sxs-lookup"><span data-stu-id="c7c08-284"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="c7c08-285">(27)</span><span class="sxs-lookup"><span data-stu-id="c7c08-285">(27)</span></span>


</dt> <dd>

<span data-ttu-id="c7c08-286">O dispositivo não tem uma configuração de log válida.</span><span class="sxs-lookup"><span data-stu-id="c7c08-286">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="c7c08-287"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Os drivers para este dispositivo não estão instalados.**</span><span class="sxs-lookup"><span data-stu-id="c7c08-287"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="c7c08-288">(28)</span><span class="sxs-lookup"><span data-stu-id="c7c08-288">(28)</span></span>


</dt> <dd>

<span data-ttu-id="c7c08-289">Os drivers de dispositivo não estão instalados.</span><span class="sxs-lookup"><span data-stu-id="c7c08-289">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="c7c08-290"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está desabilitado porque o firmware do dispositivo não forneceu os recursos necessários.**</span><span class="sxs-lookup"><span data-stu-id="c7c08-290"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="c7c08-291">(29)</span><span class="sxs-lookup"><span data-stu-id="c7c08-291">(29)</span></span>


</dt> <dd>

<span data-ttu-id="c7c08-292">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="c7c08-292">Device is disabled.</span></span> <span data-ttu-id="c7c08-293">O firmware do dispositivo não forneceu os recursos necessários.</span><span class="sxs-lookup"><span data-stu-id="c7c08-293">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="c7c08-294"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo está usando um recurso de IRQ (solicitação de interrupção) que outro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="c7c08-294"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="c7c08-295">(30)</span><span class="sxs-lookup"><span data-stu-id="c7c08-295">(30)</span></span>


</dt> <dd>

<span data-ttu-id="c7c08-296">O dispositivo está usando um recurso de IRQ que outro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="c7c08-296">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="c7c08-297"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo não está funcionando corretamente porque o Windows não pode carregar os drivers necessários para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="c7c08-297"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="c7c08-298">(31)</span><span class="sxs-lookup"><span data-stu-id="c7c08-298">(31)</span></span>


</dt> <dd>

<span data-ttu-id="c7c08-299">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="c7c08-299">Device is not working properly.</span></span> <span data-ttu-id="c7c08-300">O Windows não pode carregar os drivers de dispositivo necessários.</span><span class="sxs-lookup"><span data-stu-id="c7c08-300">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c7c08-301">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="c7c08-301">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7c08-302">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="c7c08-302">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c7c08-303">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7c08-303">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7c08-304">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="c7c08-304">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="c7c08-305">Se for **true**, o dispositivo estará usando uma configuração definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="c7c08-305">If **True**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="c7c08-306">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c7c08-306">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c7c08-307">**CorrectableError**</span><span class="sxs-lookup"><span data-stu-id="c7c08-307">**CorrectableError**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7c08-308">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="c7c08-308">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c7c08-309">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7c08-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7c08-310">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("tipo de SMBIOS \| 18 \| 32-bit de erro informações de erro de memória \| ")</span><span class="sxs-lookup"><span data-stu-id="c7c08-310">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Type")</span></span>
</dt> </dl>

<span data-ttu-id="c7c08-311">Se **for true**, o erro mais recente era corrigível.</span><span class="sxs-lookup"><span data-stu-id="c7c08-311">If **True**, the most recent error was correctable.</span></span> <span data-ttu-id="c7c08-312">Essa propriedade não será usada se **errorInfo** estiver definida como 3.</span><span class="sxs-lookup"><span data-stu-id="c7c08-312">This property is not used if **ErrorInfo** is set to 3.</span></span>

<span data-ttu-id="c7c08-313">Esta propriedade é herdada do [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="c7c08-313">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="c7c08-314">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c7c08-314">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7c08-315">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c7c08-315">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7c08-316">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7c08-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7c08-317">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c7c08-317">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c7c08-318">Nome da primeira classe concreta que aparece na cadeia de herança usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="c7c08-318">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="c7c08-319">Quando usado com as outras propriedades de chave da classe, a propriedade permite que todas as instâncias dessa classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="c7c08-319">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="c7c08-320">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c7c08-320">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c7c08-321">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="c7c08-321">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7c08-322">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c7c08-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7c08-323">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7c08-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7c08-324">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="c7c08-324">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="c7c08-325">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="c7c08-325">Description of the object.</span></span>

<span data-ttu-id="c7c08-326">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c7c08-326">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c7c08-327">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="c7c08-327">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7c08-328">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c7c08-328">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7c08-329">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7c08-329">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7c08-330">Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceID"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="c7c08-330">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="c7c08-331">Identificador exclusivo da matriz de memória.</span><span class="sxs-lookup"><span data-stu-id="c7c08-331">Unique identifier of the memory array.</span></span>

<span data-ttu-id="c7c08-332">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c7c08-332">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="c7c08-333">Exemplo: "matriz de memória 1"</span><span class="sxs-lookup"><span data-stu-id="c7c08-333">Example: "Memory Array 1"</span></span>

</dd> <dt>

<span data-ttu-id="c7c08-334">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="c7c08-334">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7c08-335">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c7c08-335">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c7c08-336">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7c08-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7c08-337">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("tipo de SMBIOS \| 19 \| endereços mapeados de dispositivo de memória \| endereço final")</span><span class="sxs-lookup"><span data-stu-id="c7c08-337">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 19\|Memory Device Mapped Addresses\|Ending Address")</span></span>
</dt> </dl>

<span data-ttu-id="c7c08-338">Endereço final referenciado por um aplicativo ou sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="c7c08-338">Ending address referenced by an application or operating system.</span></span> <span data-ttu-id="c7c08-339">Esse endereço de memória é mapeado por um controlador de memória para este objeto de memória.</span><span class="sxs-lookup"><span data-stu-id="c7c08-339">This memory address is mapped by a memory controller for this memory object.</span></span>

<span data-ttu-id="c7c08-340">Esse valor é proveniente da estrutura de **endereço mapeada da matriz de memória** nas informações de versão do SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="c7c08-340">This value comes from the **Memory Array Mapped Address** structure in the SMBIOS version information.</span></span> <span data-ttu-id="c7c08-341">Para versões de SMBIOS 2,1 a 2,6, o valor é proveniente do membro de **endereço final** .</span><span class="sxs-lookup"><span data-stu-id="c7c08-341">For SMBIOS versions 2.1 thru 2.6 the value comes from the **Ending Address** member.</span></span> <span data-ttu-id="c7c08-342">Para o SMBIOS versão 2.7 +, o valor é proveniente do membro de **endereço final estendido** .</span><span class="sxs-lookup"><span data-stu-id="c7c08-342">For SMBIOS version 2.7+ the value comes from the **Extended Ending Address** member.</span></span>

<span data-ttu-id="c7c08-343">Esta propriedade é herdada do [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="c7c08-343">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<span data-ttu-id="c7c08-344">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="c7c08-344">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="c7c08-345">**ErrorAccess**</span><span class="sxs-lookup"><span data-stu-id="c7c08-345">**ErrorAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7c08-346">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c7c08-346">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c7c08-347">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7c08-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7c08-348">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("tipo de SMBIOS \| 18 \| 32-operação de erro de informações de erro de memória \| ")</span><span class="sxs-lookup"><span data-stu-id="c7c08-348">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Operation")</span></span>
</dt> </dl>

<span data-ttu-id="c7c08-349">Tipo de operação de acesso à memória que causou o último erro.</span><span class="sxs-lookup"><span data-stu-id="c7c08-349">Type of memory access operation that caused the last error.</span></span> <span data-ttu-id="c7c08-350">Essa propriedade é válida somente quando **errorInfo** não está definida como 3.</span><span class="sxs-lookup"><span data-stu-id="c7c08-350">This property is valid only when **ErrorInfo** is not set to 3.</span></span>

<span data-ttu-id="c7c08-351">Esta propriedade é herdada do [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="c7c08-351">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c7c08-352">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="c7c08-352">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c7c08-353">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="c7c08-353">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="c7c08-354">**Leitura** (3)</span><span class="sxs-lookup"><span data-stu-id="c7c08-354">**Read** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

<span data-ttu-id="c7c08-355">**Gravação** (4)</span><span class="sxs-lookup"><span data-stu-id="c7c08-355">**Write** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>

<span data-ttu-id="c7c08-356">**Gravação parcial** (5)</span><span class="sxs-lookup"><span data-stu-id="c7c08-356">**Partial Write** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c7c08-357">**ErrorAddress**</span><span class="sxs-lookup"><span data-stu-id="c7c08-357">**ErrorAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7c08-358">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c7c08-358">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c7c08-359">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7c08-359">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7c08-360">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("tipo de SMBIOS \| 18 \| 32-bit erro de memória informações de erro \| endereço")</span><span class="sxs-lookup"><span data-stu-id="c7c08-360">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Address")</span></span>
</dt> </dl>

<span data-ttu-id="c7c08-361">Endereço do último erro de memória.</span><span class="sxs-lookup"><span data-stu-id="c7c08-361">Address of the last memory error.</span></span> <span data-ttu-id="c7c08-362">Essa propriedade é usada somente quando **errorInfo** não está definida como 3.</span><span class="sxs-lookup"><span data-stu-id="c7c08-362">This property is used only when **ErrorInfo** is not set to 3.</span></span>

<span data-ttu-id="c7c08-363">Esta propriedade é herdada do [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="c7c08-363">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<span data-ttu-id="c7c08-364">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="c7c08-364">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="c7c08-365">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="c7c08-365">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7c08-366">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="c7c08-366">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c7c08-367">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7c08-367">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c7c08-368">Se **for true**, o erro relatado em **LastErrorCode** agora será limpo.</span><span class="sxs-lookup"><span data-stu-id="c7c08-368">If **True**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="c7c08-369">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c7c08-369">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c7c08-370">**ErrorData**</span><span class="sxs-lookup"><span data-stu-id="c7c08-370">**ErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7c08-371">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="c7c08-371">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="c7c08-372">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7c08-372">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7c08-373">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="c7c08-373">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="c7c08-374">Matriz de dados capturada do último acesso à memória com um erro.</span><span class="sxs-lookup"><span data-stu-id="c7c08-374">Array of data captured from the last memory access with an error.</span></span> <span data-ttu-id="c7c08-375">Os dados ocupam os primeiros *n* octetos da matriz necessários para manter o número de bits especificado pela propriedade **ErrorTransferSize** .</span><span class="sxs-lookup"><span data-stu-id="c7c08-375">The data occupies the first *n* octets of the array necessary to hold the number of bits specified by the **ErrorTransferSize** property.</span></span> <span data-ttu-id="c7c08-376">Se **ErrorTransferSize** for 0 (zero), essa propriedade não será usada.</span><span class="sxs-lookup"><span data-stu-id="c7c08-376">If **ErrorTransferSize** is 0 (zero), then this property is not used.</span></span>

<span data-ttu-id="c7c08-377">Esta propriedade é herdada do [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="c7c08-377">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="c7c08-378">**ErrorDataOrder**</span><span class="sxs-lookup"><span data-stu-id="c7c08-378">**ErrorDataOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7c08-379">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c7c08-379">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c7c08-380">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7c08-380">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7c08-381">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="c7c08-381">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="c7c08-382">Ordenação de dados armazenados na propriedade **ErrorData** .</span><span class="sxs-lookup"><span data-stu-id="c7c08-382">Ordering for data stored in the **ErrorData** property.</span></span> <span data-ttu-id="c7c08-383">Essa propriedade é usada somente quando **ErrorTransferSize** é 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="c7c08-383">This property is used only when **ErrorTransferSize** is 0 (zero).</span></span>

<span data-ttu-id="c7c08-384">Esta propriedade é herdada do [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="c7c08-384">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c7c08-385">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="c7c08-385">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="c7c08-386">**Byte menos significativo primeiro** (1)</span><span class="sxs-lookup"><span data-stu-id="c7c08-386">**Least Significant Byte First** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="c7c08-387">**Byte mais significativo primeiro** (2)</span><span class="sxs-lookup"><span data-stu-id="c7c08-387">**Most Significant Byte First** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c7c08-388">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="c7c08-388">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7c08-389">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c7c08-389">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7c08-390">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7c08-390">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c7c08-391">Mais informações sobre o erro registrado em **LastErrorCode** e informações sobre as ações corretivas que podem ser executadas.</span><span class="sxs-lookup"><span data-stu-id="c7c08-391">More information about the error recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="c7c08-392">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c7c08-392">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c7c08-393">**ErrorGranularity**</span><span class="sxs-lookup"><span data-stu-id="c7c08-393">**ErrorGranularity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7c08-394">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c7c08-394">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c7c08-395">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7c08-395">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7c08-396">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| tipo SMBIOS 18 \| granularidade de erro")</span><span class="sxs-lookup"><span data-stu-id="c7c08-396">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|Error Granularity")</span></span>
</dt> </dl>

<span data-ttu-id="c7c08-397">Nível em que o erro pode ser resolvido.</span><span class="sxs-lookup"><span data-stu-id="c7c08-397">Level where the error can be resolved.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="c7c08-398">**1** (outro)</span><span class="sxs-lookup"><span data-stu-id="c7c08-398">**1** (Other)</span></span>


</dt> <dd></dd> <dt>

<span id="2"></span>

<span data-ttu-id="c7c08-399">**2** (desconhecido)</span><span class="sxs-lookup"><span data-stu-id="c7c08-399">**2** (Unknown)</span></span>


</dt> <dd></dd> <dt>

<span id="3"></span>

<span data-ttu-id="c7c08-400">**3** (nível do dispositivo)</span><span class="sxs-lookup"><span data-stu-id="c7c08-400">**3** (Device level)</span></span>


</dt> <dd></dd> <dt>

<span id="4"></span>

<span data-ttu-id="c7c08-401">**4** (nível de partição de memória)</span><span class="sxs-lookup"><span data-stu-id="c7c08-401">**4** (Memory partition level)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c7c08-402">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="c7c08-402">**ErrorInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7c08-403">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c7c08-403">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c7c08-404">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7c08-404">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7c08-405">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ memória CIM**](cim-memory.md).**OtherErrorDescription**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" tipo de SMBIOS \| 18 \| 32-bit memória erro Information \| Type ")</span><span class="sxs-lookup"><span data-stu-id="c7c08-405">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Memory**](cim-memory.md).**OtherErrorDescription**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Type")</span></span>
</dt> </dl>

<span data-ttu-id="c7c08-406">Tipo de erro que ocorreu mais recentemente.</span><span class="sxs-lookup"><span data-stu-id="c7c08-406">Type of error that occurred most recently.</span></span> <span data-ttu-id="c7c08-407">Os valores 12-14, que indicam se um erro é corrigível, não são usados com essa propriedade, mas essas informações são encontradas na propriedade **CorrectableError** .</span><span class="sxs-lookup"><span data-stu-id="c7c08-407">The values 12-14, which indicate whether an error is correctable, are not used with this property, but this information is found in the **CorrectableError** property.</span></span>

<span data-ttu-id="c7c08-408">Esta propriedade é herdada do [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="c7c08-408">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c7c08-409">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="c7c08-409">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c7c08-410">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="c7c08-410">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="c7c08-411">**OK** (3)</span><span class="sxs-lookup"><span data-stu-id="c7c08-411">**OK** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>

<span data-ttu-id="c7c08-412">**Leitura inadequada** (4)</span><span class="sxs-lookup"><span data-stu-id="c7c08-412">**Bad Read** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>

<span data-ttu-id="c7c08-413">**Erro de paridade** (5)</span><span class="sxs-lookup"><span data-stu-id="c7c08-413">**Parity Error** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>

<span data-ttu-id="c7c08-414">**Erro de bit único** (6)</span><span class="sxs-lookup"><span data-stu-id="c7c08-414">**Single-Bit Error** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>

<span data-ttu-id="c7c08-415">**Erro de bit duplo** (7)</span><span class="sxs-lookup"><span data-stu-id="c7c08-415">**Double-Bit Error** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>

<span data-ttu-id="c7c08-416">**Erro de vários bits** (8)</span><span class="sxs-lookup"><span data-stu-id="c7c08-416">**Multi-Bit Error** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>

<span data-ttu-id="c7c08-417">**Erro de Nibble** (9)</span><span class="sxs-lookup"><span data-stu-id="c7c08-417">**Nibble Error** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>

<span data-ttu-id="c7c08-418">**Erro de soma de verificação** (10)</span><span class="sxs-lookup"><span data-stu-id="c7c08-418">**Checksum Error** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>

<span data-ttu-id="c7c08-419">**Erro de CRC** (11)</span><span class="sxs-lookup"><span data-stu-id="c7c08-419">**CRC Error** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Corrected_single-bit_error"></span><span id="corrected_single-bit_error"></span><span id="CORRECTED_SINGLE-BIT_ERROR"></span>

<span data-ttu-id="c7c08-420">**Erro de bit único corrigido** (12)</span><span class="sxs-lookup"><span data-stu-id="c7c08-420">**Corrected single-bit error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Corrected_error"></span><span id="corrected_error"></span><span id="CORRECTED_ERROR"></span>

<span data-ttu-id="c7c08-421">**Erro corrigido** (13)</span><span class="sxs-lookup"><span data-stu-id="c7c08-421">**Corrected error** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Uncorrectable_error"></span><span id="uncorrectable_error"></span><span id="UNCORRECTABLE_ERROR"></span>

<span data-ttu-id="c7c08-422">**Erro não corrigível** (14)</span><span class="sxs-lookup"><span data-stu-id="c7c08-422">**Uncorrectable error** (14)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c7c08-423">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="c7c08-423">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7c08-424">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c7c08-424">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7c08-425">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7c08-425">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7c08-426">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("tipo do SMBIOS \| 16 \| correção de erro de memória da matriz de memória física \| ")</span><span class="sxs-lookup"><span data-stu-id="c7c08-426">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 16\|Physical Memory Array\|Memory Error Correction")</span></span>
</dt> </dl>

<span data-ttu-id="c7c08-427">Tipos de verificação de erros usados pelo hardware de memória.</span><span class="sxs-lookup"><span data-stu-id="c7c08-427">Types of error checking used by the memory hardware.</span></span>

<span data-ttu-id="c7c08-428">Essa propriedade é herdada do [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="c7c08-428">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span> <span data-ttu-id="c7c08-429">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="c7c08-429">The values are:</span></span>

<dl> <dd><span data-ttu-id="c7c08-430">Outros</span><span class="sxs-lookup"><span data-stu-id="c7c08-430">"Other"</span></span></dd> <dd><span data-ttu-id="c7c08-431">Conhecidos</span><span class="sxs-lookup"><span data-stu-id="c7c08-431">"Unknown"</span></span></dd> <dd><span data-ttu-id="c7c08-432">"None"</span><span class="sxs-lookup"><span data-stu-id="c7c08-432">"None"</span></span></dd> <dd><span data-ttu-id="c7c08-433">Paridade</span><span class="sxs-lookup"><span data-stu-id="c7c08-433">"Parity"</span></span></dd> <dd><span data-ttu-id="c7c08-434">"ECC de bit único"</span><span class="sxs-lookup"><span data-stu-id="c7c08-434">"Single-bit ECC"</span></span></dd> <dd><span data-ttu-id="c7c08-435">"ECC de múltiplos bits"</span><span class="sxs-lookup"><span data-stu-id="c7c08-435">"Multi-bit ECC"</span></span></dd> <dd><span data-ttu-id="c7c08-436">CRC</span><span class="sxs-lookup"><span data-stu-id="c7c08-436">"CRC"</span></span></dd> </dl>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c7c08-437">**Outro** ("outro")</span><span class="sxs-lookup"><span data-stu-id="c7c08-437">**Other** ("Other")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c7c08-438">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="c7c08-438">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="c7c08-439">**Nenhum** ("nenhum")</span><span class="sxs-lookup"><span data-stu-id="c7c08-439">**None** ("None")</span></span>


</dt> <dd></dd> <dt>

<span id="Parity"></span><span id="parity"></span><span id="PARITY"></span>

<span data-ttu-id="c7c08-440">**Paridade** ("paridade")</span><span class="sxs-lookup"><span data-stu-id="c7c08-440">**Parity** ("Parity")</span></span>


</dt> <dd></dd> <dt>

<span id="Single-bit_ECC"></span><span id="single-bit_ecc"></span><span id="SINGLE-BIT_ECC"></span>

<span data-ttu-id="c7c08-441">**ECC de bit único** ("ECC de bit único")</span><span class="sxs-lookup"><span data-stu-id="c7c08-441">**Single-bit ECC** ("Single-bit ECC")</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-bit_ECC"></span><span id="multi-bit_ecc"></span><span id="MULTI-BIT_ECC"></span>

<span data-ttu-id="c7c08-442">**ECC de vários bits** ("ECC de múltiplos bits")</span><span class="sxs-lookup"><span data-stu-id="c7c08-442">**Multi-bit ECC** ("Multi-bit ECC")</span></span>


</dt> <dd></dd> <dt>

<span id="CRC"></span><span id="crc"></span>

<span data-ttu-id="c7c08-443">**CRC** ("CRC")</span><span class="sxs-lookup"><span data-stu-id="c7c08-443">**CRC** ("CRC")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c7c08-444">**ErrorResolution**</span><span class="sxs-lookup"><span data-stu-id="c7c08-444">**ErrorResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7c08-445">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c7c08-445">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c7c08-446">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7c08-446">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7c08-447">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| tipo SMBIOS 18 \| 32-bit de erro de memória informações de \| resolução de erro"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="c7c08-447">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Resolution"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="c7c08-448">Quantidade de dados realmente determinados para causar o erro.</span><span class="sxs-lookup"><span data-stu-id="c7c08-448">Amount of data actually determined to cause the error.</span></span> <span data-ttu-id="c7c08-449">Essa propriedade não é usada quando a propriedade **errorInfo** está definida como 3.</span><span class="sxs-lookup"><span data-stu-id="c7c08-449">This property is unused when the **ErrorInfo** property is set to 3.</span></span>

<span data-ttu-id="c7c08-450">Esta propriedade é herdada do [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="c7c08-450">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<span data-ttu-id="c7c08-451">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="c7c08-451">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="c7c08-452">**ErrorTime**</span><span class="sxs-lookup"><span data-stu-id="c7c08-452">**ErrorTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7c08-453">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c7c08-453">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c7c08-454">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7c08-454">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7c08-455">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="c7c08-455">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="c7c08-456">Hora em que ocorreu o último erro de memória.</span><span class="sxs-lookup"><span data-stu-id="c7c08-456">Time that the last memory error occurred.</span></span> <span data-ttu-id="c7c08-457">Essa propriedade é válida somente quando **errorInfo** não está definida como 3.</span><span class="sxs-lookup"><span data-stu-id="c7c08-457">This property is valid only when **ErrorInfo** is not set to 3.</span></span>

<span data-ttu-id="c7c08-458">Esta propriedade é herdada do [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="c7c08-458">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="c7c08-459">**ErrorTransferSize**</span><span class="sxs-lookup"><span data-stu-id="c7c08-459">**ErrorTransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7c08-460">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c7c08-460">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c7c08-461">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7c08-461">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7c08-462">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span><span class="sxs-lookup"><span data-stu-id="c7c08-462">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="c7c08-463">Tamanho dos dados (que contém o último erro) que estão sendo transferidos.</span><span class="sxs-lookup"><span data-stu-id="c7c08-463">Size of the data (containing the last error) being transferred.</span></span> <span data-ttu-id="c7c08-464">Essa propriedade será definida como 0 (zero) se não houver erro.</span><span class="sxs-lookup"><span data-stu-id="c7c08-464">This property is set to 0 (zero) if there is no error.</span></span>

<span data-ttu-id="c7c08-465">Esta propriedade é herdada do [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="c7c08-465">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="c7c08-466">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c7c08-466">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7c08-467">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c7c08-467">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c7c08-468">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7c08-468">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7c08-469">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="c7c08-469">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="c7c08-470">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="c7c08-470">Date and time the object was installed.</span></span> <span data-ttu-id="c7c08-471">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="c7c08-471">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="c7c08-472">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c7c08-472">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c7c08-473">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="c7c08-473">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7c08-474">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c7c08-474">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c7c08-475">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7c08-475">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c7c08-476">Código do último erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="c7c08-476">Last error code reported by the logical device.</span></span>

<span data-ttu-id="c7c08-477">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c7c08-477">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c7c08-478">**Nome**</span><span class="sxs-lookup"><span data-stu-id="c7c08-478">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7c08-479">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c7c08-479">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7c08-480">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7c08-480">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7c08-481">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="c7c08-481">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="c7c08-482">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="c7c08-482">Label by which the object is known.</span></span> <span data-ttu-id="c7c08-483">Quando em uma subclasse, a propriedade pode ser substituída para ser uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="c7c08-483">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="c7c08-484">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c7c08-484">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c7c08-485">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="c7c08-485">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7c08-486">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c7c08-486">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c7c08-487">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7c08-487">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7c08-488">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrStorageSize ")</span><span class="sxs-lookup"><span data-stu-id="c7c08-488">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="c7c08-489">Número total de blocos consecutivos, cada um deles bloqueando o tamanho do valor contido na propriedade **BlockSize** , que formam essa extensão de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="c7c08-489">Total number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, which form this storage extent.</span></span> <span data-ttu-id="c7c08-490">O tamanho total da extensão de armazenamento pode ser calculado multiplicando o valor da propriedade **BlockSize** pelo valor dessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="c7c08-490">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="c7c08-491">Se o valor de **BlockSize** for 1, essa propriedade será o tamanho total da extensão de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="c7c08-491">If the value of **BlockSize** is 1, this property is the total size of the storage extent.</span></span>

<span data-ttu-id="c7c08-492">Essa propriedade é herdada do [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="c7c08-492">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="c7c08-493">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="c7c08-493">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="c7c08-494">**OtherErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="c7c08-494">**OtherErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7c08-495">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c7c08-495">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7c08-496">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7c08-496">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7c08-497">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ memória CIM**](cim-memory.md).**ErrorInfo**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" SMBIOS ")</span><span class="sxs-lookup"><span data-stu-id="c7c08-497">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Memory**](cim-memory.md).**ErrorInfo**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS")</span></span>
</dt> </dl>

<span data-ttu-id="c7c08-498">Mais informações quando a propriedade **errorInfo** é definida como 1.</span><span class="sxs-lookup"><span data-stu-id="c7c08-498">More information when the **ErrorInfo** property is set to 1.</span></span>

<span data-ttu-id="c7c08-499">Esta propriedade é herdada do [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="c7c08-499">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="c7c08-500">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="c7c08-500">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7c08-501">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c7c08-501">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7c08-502">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7c08-502">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7c08-503">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="c7c08-503">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="c7c08-504">Identificador de dispositivo do Windows Plug and Play do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="c7c08-504">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="c7c08-505">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c7c08-505">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="c7c08-506">Exemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="c7c08-506">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="c7c08-507">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="c7c08-507">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7c08-508">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c7c08-508">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c7c08-509">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7c08-509">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c7c08-510">Matriz de recursos específicos relacionados à energia de um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="c7c08-510">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="c7c08-511">Essa propriedade é herdada **de \_ LogicalDevice CIM**.</span><span class="sxs-lookup"><span data-stu-id="c7c08-511">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c7c08-512"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="c7c08-512"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="c7c08-513"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="c7c08-513"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="c7c08-514"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="c7c08-514"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="c7c08-515"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="c7c08-515"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="c7c08-516">Os recursos de gerenciamento de energia estão habilitados no momento, mas o conjunto de recursos exato é desconhecido ou as informações não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="c7c08-516">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="c7c08-517"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de economia de energia inseridos automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="c7c08-517"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="c7c08-518">O dispositivo pode alterar seu estado de energia com base no uso ou em outros critérios.</span><span class="sxs-lookup"><span data-stu-id="c7c08-518">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="c7c08-519"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energia configurável** (5)</span><span class="sxs-lookup"><span data-stu-id="c7c08-519"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="c7c08-520">Há suporte para o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="c7c08-520">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="c7c08-521">Esse método é encontrado na classe pai **de \_ LogicalDevice CIM** e pode ser implementado.</span><span class="sxs-lookup"><span data-stu-id="c7c08-521">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="c7c08-522">Para obter mais informações, consulte [Designing formato MOF (MOF) classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="c7c08-522">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="c7c08-523"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energia com suporte** (6)</span><span class="sxs-lookup"><span data-stu-id="c7c08-523"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="c7c08-524">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia).</span><span class="sxs-lookup"><span data-stu-id="c7c08-524">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="c7c08-525"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Energia cronometrada com suporte** (7)</span><span class="sxs-lookup"><span data-stu-id="c7c08-525"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="c7c08-526">Tempo Power-On com suporte</span><span class="sxs-lookup"><span data-stu-id="c7c08-526">Timed Power-On Supported</span></span>

<span data-ttu-id="c7c08-527">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia) e o *tempo* definido como uma data e hora e um intervalo específicos para o Power-on.</span><span class="sxs-lookup"><span data-stu-id="c7c08-527">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c7c08-528">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="c7c08-528">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7c08-529">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="c7c08-529">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c7c08-530">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7c08-530">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c7c08-531">Se **for true**, o dispositivo poderá ser gerenciado por energia (pode ser colocado no modo de suspensão e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="c7c08-531">If **True**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="c7c08-532">A propriedade não indica que os recursos de gerenciamento de energia estão habilitados no momento, apenas que o dispositivo lógico é capaz de gerenciamento de energia.</span><span class="sxs-lookup"><span data-stu-id="c7c08-532">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="c7c08-533">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c7c08-533">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c7c08-534">**Finalidade**</span><span class="sxs-lookup"><span data-stu-id="c7c08-534">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7c08-535">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c7c08-535">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7c08-536">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7c08-536">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c7c08-537">Cadeia de caracteres de forma livre que descreve a mídia e seu uso.</span><span class="sxs-lookup"><span data-stu-id="c7c08-537">Free-form string describing the media and its use.</span></span>

<span data-ttu-id="c7c08-538">Essa propriedade é herdada do [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="c7c08-538">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="c7c08-539">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="c7c08-539">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7c08-540">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c7c08-540">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c7c08-541">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7c08-541">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7c08-542">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("tipo de SMBIOS \| 19 \| endereços mapeados de dispositivo de memória \| iniciando endereço")</span><span class="sxs-lookup"><span data-stu-id="c7c08-542">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 19\|Memory Device Mapped Addresses\|Starting Address")</span></span>
</dt> </dl>

<span data-ttu-id="c7c08-543">Endereço inicial referenciado por um aplicativo ou pelo sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="c7c08-543">Beginning address referenced by an application or the operating system.</span></span> <span data-ttu-id="c7c08-544">Esse endereço de memória é mapeado por um controlador de memória para este objeto de memória.</span><span class="sxs-lookup"><span data-stu-id="c7c08-544">This memory address is mapped by a memory controller for this memory object.</span></span>

<span data-ttu-id="c7c08-545">Esse valor é proveniente da estrutura de **endereço mapeada da matriz de memória** nas informações de versão do SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="c7c08-545">This value comes from the **Memory Array Mapped Address** structure in the SMBIOS version information.</span></span> <span data-ttu-id="c7c08-546">Para versões de SMBIOS 2,1 a 2,6, o valor é proveniente do membro de **endereço inicial** .</span><span class="sxs-lookup"><span data-stu-id="c7c08-546">For SMBIOS versions 2.1 thru 2.6 the value comes from the **Starting Address** member.</span></span> <span data-ttu-id="c7c08-547">Para o SMBIOS versão 2.7 +, o valor é proveniente do membro de **endereço de início estendido** .</span><span class="sxs-lookup"><span data-stu-id="c7c08-547">For SMBIOS version 2.7+ the value comes from the **Extended Starting Address** member.</span></span>

<span data-ttu-id="c7c08-548">Esta propriedade é herdada do [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="c7c08-548">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<span data-ttu-id="c7c08-549">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="c7c08-549">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="c7c08-550">**Status**</span><span class="sxs-lookup"><span data-stu-id="c7c08-550">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7c08-551">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c7c08-551">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7c08-552">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7c08-552">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7c08-553">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="c7c08-553">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="c7c08-554">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="c7c08-554">Current status of the object.</span></span> <span data-ttu-id="c7c08-555">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="c7c08-555">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="c7c08-556">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="c7c08-556">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="c7c08-557">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="c7c08-557">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="c7c08-558">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="c7c08-558">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="c7c08-559">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="c7c08-559">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="c7c08-560">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c7c08-560">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="c7c08-561">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="c7c08-561">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="c7c08-562">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="c7c08-562">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="c7c08-563">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="c7c08-563">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="c7c08-564">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="c7c08-564">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c7c08-565">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="c7c08-565">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="c7c08-566">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="c7c08-566">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="c7c08-567">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="c7c08-567">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="c7c08-568">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="c7c08-568">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="c7c08-569">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="c7c08-569">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="c7c08-570">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="c7c08-570">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="c7c08-571">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="c7c08-571">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="c7c08-572">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="c7c08-572">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="c7c08-573">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="c7c08-573">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c7c08-574">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="c7c08-574">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7c08-575">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c7c08-575">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c7c08-576">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7c08-576">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7c08-577">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="c7c08-577">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="c7c08-578">Estado do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="c7c08-578">State of the logical device.</span></span> <span data-ttu-id="c7c08-579">Se essa propriedade não se aplicar ao dispositivo lógico, o valor 5 (não aplicável) deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="c7c08-579">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="c7c08-580">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c7c08-580">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c7c08-581">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="c7c08-581">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c7c08-582">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="c7c08-582">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="c7c08-583">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="c7c08-583">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="c7c08-584">**Desabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="c7c08-584">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="c7c08-585">**Não aplicável** (5)</span><span class="sxs-lookup"><span data-stu-id="c7c08-585">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c7c08-586">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c7c08-586">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7c08-587">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c7c08-587">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7c08-588">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7c08-588">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7c08-589">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c7c08-589">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c7c08-590">Valor da propriedade **CreationClassName** do computador de escopo.</span><span class="sxs-lookup"><span data-stu-id="c7c08-590">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="c7c08-591">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c7c08-591">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c7c08-592">**SystemLevelAddress**</span><span class="sxs-lookup"><span data-stu-id="c7c08-592">**SystemLevelAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7c08-593">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="c7c08-593">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c7c08-594">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7c08-594">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7c08-595">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("tipo de SMBIOS \| 18 \| 32-bit erro de memória informações de erro \| endereço")</span><span class="sxs-lookup"><span data-stu-id="c7c08-595">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Address")</span></span>
</dt> </dl>

<span data-ttu-id="c7c08-596">Se **for true**, as informações de endereço na propriedade **ErrorAddress** serão um endereço de nível de sistema.</span><span class="sxs-lookup"><span data-stu-id="c7c08-596">If **True**, the address information in the **ErrorAddress** property is a system-level address.</span></span> <span data-ttu-id="c7c08-597">Se for **false**, será um endereço físico.</span><span class="sxs-lookup"><span data-stu-id="c7c08-597">If **False**, it is a physical address.</span></span> <span data-ttu-id="c7c08-598">Essa propriedade é usada somente quando **errorInfo** não está definida como 3.</span><span class="sxs-lookup"><span data-stu-id="c7c08-598">This property is used only when **ErrorInfo** is not set to 3.</span></span>

<span data-ttu-id="c7c08-599">Esta propriedade é herdada do [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="c7c08-599">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="c7c08-600">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="c7c08-600">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7c08-601">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c7c08-601">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7c08-602">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7c08-602">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7c08-603">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c7c08-603">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c7c08-604">Nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="c7c08-604">Name of the scoping system.</span></span>

<span data-ttu-id="c7c08-605">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c7c08-605">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c7c08-606">Comentários</span><span class="sxs-lookup"><span data-stu-id="c7c08-606">Remarks</span></span>

<span data-ttu-id="c7c08-607">A classe **Win32 \_ MemoryArray** é derivada de [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="c7c08-607">The **Win32\_MemoryArray** class is derived from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c7c08-608">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c7c08-608">Requirements</span></span>



| <span data-ttu-id="c7c08-609">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7c08-609">Requirement</span></span> | <span data-ttu-id="c7c08-610">Valor</span><span class="sxs-lookup"><span data-stu-id="c7c08-610">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c7c08-611">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c7c08-611">Minimum supported client</span></span><br/> | <span data-ttu-id="c7c08-612">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c7c08-612">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c7c08-613">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c7c08-613">Minimum supported server</span></span><br/> | <span data-ttu-id="c7c08-614">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c7c08-614">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c7c08-615">Namespace</span><span class="sxs-lookup"><span data-stu-id="c7c08-615">Namespace</span></span><br/>                | <span data-ttu-id="c7c08-616">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="c7c08-616">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c7c08-617">MOF</span><span class="sxs-lookup"><span data-stu-id="c7c08-617">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c7c08-618"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c7c08-618"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c7c08-619">DLL</span><span class="sxs-lookup"><span data-stu-id="c7c08-619">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7c08-620"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7c08-620"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7c08-621">Confira também</span><span class="sxs-lookup"><span data-stu-id="c7c08-621">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7c08-622">**\_SMBIOSMemory Win32**</span><span class="sxs-lookup"><span data-stu-id="c7c08-622">**Win32\_SMBIOSMemory**</span></span>](win32-smbiosmemory.md)
</dt> <dt>

[<span data-ttu-id="c7c08-623">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="c7c08-623">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

