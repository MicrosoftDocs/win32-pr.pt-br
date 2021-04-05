---
description: Representa um dispositivo de memória física localizado em um sistema de computador e disponível para o sistema operacional.
ms.assetid: 34baca53-ab85-4e06-9853-71b904ede4ab
ms.tgt_platform: multiple
title: Classe Win32_PhysicalMemory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PhysicalMemory
- Win32_PhysicalMemory.Attributes
- Win32_PhysicalMemory.BankLabel
- Win32_PhysicalMemory.Capacity
- Win32_PhysicalMemory.Caption
- Win32_PhysicalMemory.ConfiguredClockSpeed
- Win32_PhysicalMemory.ConfiguredVoltage
- Win32_PhysicalMemory.CreationClassName
- Win32_PhysicalMemory.DataWidth
- Win32_PhysicalMemory.Description
- Win32_PhysicalMemory.DeviceLocator
- Win32_PhysicalMemory.FormFactor
- Win32_PhysicalMemory.HotSwappable
- Win32_PhysicalMemory.InstallDate
- Win32_PhysicalMemory.InterleaveDataDepth
- Win32_PhysicalMemory.InterleavePosition
- Win32_PhysicalMemory.Manufacturer
- Win32_PhysicalMemory.MaxVoltage
- Win32_PhysicalMemory.MemoryType
- Win32_PhysicalMemory.MinVoltage
- Win32_PhysicalMemory.Model
- Win32_PhysicalMemory.Name
- Win32_PhysicalMemory.OtherIdentifyingInfo
- Win32_PhysicalMemory.PartNumber
- Win32_PhysicalMemory.PositionInRow
- Win32_PhysicalMemory.PoweredOn
- Win32_PhysicalMemory.Removable
- Win32_PhysicalMemory.Replaceable
- Win32_PhysicalMemory.SerialNumber
- Win32_PhysicalMemory.SKU
- Win32_PhysicalMemory.SMBIOSMemoryType
- Win32_PhysicalMemory.Speed
- Win32_PhysicalMemory.Status
- Win32_PhysicalMemory.Tag
- Win32_PhysicalMemory.TotalWidth
- Win32_PhysicalMemory.TypeDetail
- Win32_PhysicalMemory.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e026c3c3d0a29bbbd10ed2b5565708f0bcb0900c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457184"
---
# <a name="win32_physicalmemory-class"></a><span data-ttu-id="1a496-103">\_Classe Win32 PhysicalMemory</span><span class="sxs-lookup"><span data-stu-id="1a496-103">Win32\_PhysicalMemory class</span></span>

<span data-ttu-id="1a496-104">A [classe WMI](../wmisdk/retrieving-a-class.md) **\_ PhysicalMemory do Win32** representa um dispositivo de memória física localizado em um sistema de computador e disponível para o sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="1a496-104">The **Win32\_PhysicalMemory** [WMI class](../wmisdk/retrieving-a-class.md) represents a physical memory device located on a computer system and available to the operating system.</span></span>

<span data-ttu-id="1a496-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="1a496-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="1a496-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="1a496-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a496-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1a496-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B93-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_PhysicalMemory : CIM_PhysicalMemory
{
  uint32   Attributes;
  string   BankLabel;
  uint64   Capacity;
  string   Caption;
  uint32   ConfiguredClockSpeed;
  uint32   ConfiguredVoltage;
  string   CreationClassName;
  uint16   DataWidth;
  string   Description;
  string   DeviceLocator;
  uint16   FormFactor;
  boolean  HotSwappable;
  datetime InstallDate;
  uint16   InterleaveDataDepth;
  uint32   InterleavePosition;
  string   Manufacturer;
  uint32   MaxVoltage;
  uint16   MemoryType;
  uint32   MinVoltage;
  string   Model;
  string   Name;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  uint32   PositionInRow;
  boolean  PoweredOn;
  boolean  Removable;
  boolean  Replaceable;
  string   SerialNumber;
  string   SKU;
  uint32   SMBIOSMemoryType;
  uint32   Speed;
  string   Status;
  string   Tag;
  uint16   TotalWidth;
  uint16   TypeDetail;
  string   Version;
};
```

## <a name="members"></a><span data-ttu-id="1a496-108">Membros</span><span class="sxs-lookup"><span data-stu-id="1a496-108">Members</span></span>

<span data-ttu-id="1a496-109">A classe **Win32 \_ PhysicalMemory** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="1a496-109">The **Win32\_PhysicalMemory** class has these types of members:</span></span>

-   [<span data-ttu-id="1a496-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1a496-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1a496-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1a496-111">Properties</span></span>

<span data-ttu-id="1a496-112">A classe **Win32 \_ PhysicalMemory** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="1a496-112">The **Win32\_PhysicalMemory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1a496-113">**Atributos**</span><span class="sxs-lookup"><span data-stu-id="1a496-113">**Attributes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a496-114">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1a496-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1a496-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1a496-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a496-116">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| atributos do tipo SMBIOS 17 \| ")</span><span class="sxs-lookup"><span data-stu-id="1a496-116">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 17\|Attributes")</span></span>
</dt> </dl>

<span data-ttu-id="1a496-117">SMBIOS-Type 17-Attributes.</span><span class="sxs-lookup"><span data-stu-id="1a496-117">SMBIOS - Type 17 - Attributes.</span></span> <span data-ttu-id="1a496-118">Representa a classificação.</span><span class="sxs-lookup"><span data-stu-id="1a496-118">Represents the RANK.</span></span>

<span data-ttu-id="1a496-119">Esse valor é proveniente do membro **Attributes** da estrutura de **dispositivo de memória** nas informações de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="1a496-119">This value comes from the **Attributes** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="1a496-120">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows server 2008 e Windows Vista:** Não há suporte para essa propriedade antes do Windows Server 2016 e do Windows 10.</span><span class="sxs-lookup"><span data-stu-id="1a496-120">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows Server 2016 and Windows 10.</span></span>

</dd> <dt>

<span data-ttu-id="1a496-121">**BankLabel**</span><span class="sxs-lookup"><span data-stu-id="1a496-121">**BankLabel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a496-122">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1a496-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1a496-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1a496-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a496-124">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Dispositivo de memória DMTF \| 2,4 ")</span><span class="sxs-lookup"><span data-stu-id="1a496-124">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Memory Device\|002.4")</span></span>
</dt> </dl>

<span data-ttu-id="1a496-125">Rotulado fisicamente o banco em que a memória está localizada.</span><span class="sxs-lookup"><span data-stu-id="1a496-125">Physically labeled bank where the memory is located.</span></span>

<span data-ttu-id="1a496-126">Exemplos: "Bank 0", "Bank A"</span><span class="sxs-lookup"><span data-stu-id="1a496-126">Examples: "Bank 0", "Bank A"</span></span>

<span data-ttu-id="1a496-127">Esse valor é proveniente do membro do **localizador de banco** da estrutura do **dispositivo de memória** nas informações do SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="1a496-127">This value comes from the **Bank Locator** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="1a496-128">Essa propriedade é herdada do [**CIM \_ PhysicalMemory**](cim-physicalmemory.md).</span><span class="sxs-lookup"><span data-stu-id="1a496-128">This property is inherited from [**CIM\_PhysicalMemory**](cim-physicalmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="1a496-129">**Capacidade**</span><span class="sxs-lookup"><span data-stu-id="1a496-129">**Capacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a496-130">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1a496-130">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1a496-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1a496-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a496-132">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Dispositivo de memória DMTF \| 2,5 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="1a496-132">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Memory Device\|002.5"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="1a496-133">Capacidade total da memória física — em bytes.</span><span class="sxs-lookup"><span data-stu-id="1a496-133">Total capacity of the physical memory—in bytes.</span></span>

<span data-ttu-id="1a496-134">Esse valor é proveniente da estrutura de **dispositivo de memória** nas informações de versão do SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="1a496-134">This value comes from the **Memory Device** structure in the SMBIOS version information.</span></span> <span data-ttu-id="1a496-135">Para versões de SMBIOS 2,1 a 2,6, o valor é proveniente do membro de **tamanho** .</span><span class="sxs-lookup"><span data-stu-id="1a496-135">For SMBIOS versions 2.1 thru 2.6 the value comes from the **Size** member.</span></span> <span data-ttu-id="1a496-136">Para o SMBIOS versão 2.7 +, o valor é proveniente do membro de **tamanho estendido** .</span><span class="sxs-lookup"><span data-stu-id="1a496-136">For SMBIOS version 2.7+ the value comes from the **Extended Size** member.</span></span>

<span data-ttu-id="1a496-137">Essa propriedade é herdada do [**CIM \_ PhysicalMemory**](cim-physicalmemory.md).</span><span class="sxs-lookup"><span data-stu-id="1a496-137">This property is inherited from [**CIM\_PhysicalMemory**](cim-physicalmemory.md).</span></span>

<span data-ttu-id="1a496-138">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="1a496-138">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="1a496-139">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="1a496-139">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a496-140">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1a496-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1a496-141">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1a496-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a496-142">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="1a496-142">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="1a496-143">Breve descrição do objeto — uma cadeia de caracteres de uma linha.</span><span class="sxs-lookup"><span data-stu-id="1a496-143">Short description of the object—a one-line string.</span></span>

<span data-ttu-id="1a496-144">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1a496-144">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1a496-145">**ConfiguredClockSpeed**</span><span class="sxs-lookup"><span data-stu-id="1a496-145">**ConfiguredClockSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a496-146">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1a496-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1a496-147">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1a496-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a496-148">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| tipo SMBIOS 17 de velocidade de clock de \| memória configurada")</span><span class="sxs-lookup"><span data-stu-id="1a496-148">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 17\|Configured Memory Clock Speed")</span></span>
</dt> </dl>

<span data-ttu-id="1a496-149">A velocidade de clock configurada do dispositivo de memória, em megahertz (MHz) ou 0, se a velocidade for desconhecida.</span><span class="sxs-lookup"><span data-stu-id="1a496-149">The configured clock speed of the memory device, in megahertz (MHz), or 0, if the speed is unknown.</span></span>

<span data-ttu-id="1a496-150">Esse valor é proveniente do membro da **velocidade do relógio da memória configurada** da estrutura do **dispositivo de memória** nas informações do SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="1a496-150">This value comes from the **Configured Memory Clock Speed** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="1a496-151">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows server 2008 e Windows Vista:** Não há suporte para essa propriedade antes do Windows Server 2016 e do Windows 10.</span><span class="sxs-lookup"><span data-stu-id="1a496-151">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows Server 2016 and Windows 10.</span></span>

</dd> <dt>

<span data-ttu-id="1a496-152">**ConfiguredVoltage**</span><span class="sxs-lookup"><span data-stu-id="1a496-152">**ConfiguredVoltage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a496-153">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1a496-153">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1a496-154">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1a496-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a496-155">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| Type 17 \| configurative Voltage")</span><span class="sxs-lookup"><span data-stu-id="1a496-155">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 17\|Configured voltage")</span></span>
</dt> </dl>

<span data-ttu-id="1a496-156">A tensão configurada para este dispositivo, em milivolts ou 0, se a tensão for desconhecida.</span><span class="sxs-lookup"><span data-stu-id="1a496-156">Configured voltage for this device, in millivolts, or 0, if the voltage is unknown.</span></span>

<span data-ttu-id="1a496-157">Esse valor é proveniente do membro de **tensão configurado** da estrutura do **dispositivo de memória** nas informações do SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="1a496-157">This value comes from the **Configured voltage** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="1a496-158">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows server 2008 e Windows Vista:** Não há suporte para essa propriedade antes do Windows Server 2016 e do Windows 10.</span><span class="sxs-lookup"><span data-stu-id="1a496-158">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows Server 2016 and Windows 10.</span></span>

</dd> <dt>

<span data-ttu-id="1a496-159">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="1a496-159">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a496-160">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1a496-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1a496-161">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1a496-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a496-162">Qualificadores: [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="1a496-162">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="1a496-163">Nome da primeira classe concreta que aparece na cadeia de herança usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="1a496-163">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="1a496-164">Quando usado com as outras propriedades de chave da classe, a propriedade permite que todas as instâncias dessa classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="1a496-164">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="1a496-165">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="1a496-165">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1a496-166">**DataWidth**</span><span class="sxs-lookup"><span data-stu-id="1a496-166">**DataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a496-167">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1a496-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1a496-168">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1a496-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a496-169">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Dispositivo de memória DMTF \| 2,8 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" bits ")</span><span class="sxs-lookup"><span data-stu-id="1a496-169">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Memory Device\|002.8"), [**Units**](../wmisdk/standard-qualifiers.md) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="1a496-170">Largura de dados da memória física — em bits.</span><span class="sxs-lookup"><span data-stu-id="1a496-170">Data width of the physical memory—in bits.</span></span> <span data-ttu-id="1a496-171">Uma largura de dados de 0 (zero) e uma largura total de 8 (oito) indica que a memória é usada unicamente para fornecer bits de correção de erro.</span><span class="sxs-lookup"><span data-stu-id="1a496-171">A data width of 0 (zero) and a total width of 8 (eight) indicates that the memory is used solely to provide error correction bits.</span></span>

<span data-ttu-id="1a496-172">Esse valor é proveniente do membro de **largura de dados** da estrutura de **dispositivo de memória** nas informações de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="1a496-172">This value comes from the **Data Width** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="1a496-173">Essa propriedade é herdada do [**CIM \_ PhysicalMemory**](cim-physicalmemory.md).</span><span class="sxs-lookup"><span data-stu-id="1a496-173">This property is inherited from [**CIM\_PhysicalMemory**](cim-physicalmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="1a496-174">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="1a496-174">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a496-175">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1a496-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1a496-176">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1a496-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a496-177">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="1a496-177">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="1a496-178">Descrição de um objeto.</span><span class="sxs-lookup"><span data-stu-id="1a496-178">Description of an object.</span></span>

<span data-ttu-id="1a496-179">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1a496-179">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1a496-180">**DeviceLocator**</span><span class="sxs-lookup"><span data-stu-id="1a496-180">**DeviceLocator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a496-181">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1a496-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1a496-182">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1a496-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a496-183">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| localizador de dispositivo do tipo SMBIOS 17 \| ")</span><span class="sxs-lookup"><span data-stu-id="1a496-183">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 17\|Device Locator")</span></span>
</dt> </dl>

<span data-ttu-id="1a496-184">Rótulo do soquete ou placa de circuito que contém a memória.</span><span class="sxs-lookup"><span data-stu-id="1a496-184">Label of the socket or circuit board that holds the memory.</span></span>

<span data-ttu-id="1a496-185">Exemplo: "SIMM 3"</span><span class="sxs-lookup"><span data-stu-id="1a496-185">Example: "SIMM 3"</span></span>

<span data-ttu-id="1a496-186">Esse valor é proveniente do membro do **localizador de dispositivo** da estrutura de **dispositivo de memória** nas informações do SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="1a496-186">This value comes from the **Device Locator** member of the **Memory Device** structure in the SMBIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="1a496-187">**FormFactor**</span><span class="sxs-lookup"><span data-stu-id="1a496-187">**FormFactor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a496-188">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1a496-188">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1a496-189">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1a496-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a496-190">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Dispositivo de memória DMTF \| 2,6 ")</span><span class="sxs-lookup"><span data-stu-id="1a496-190">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Memory Device\|002.6")</span></span>
</dt> </dl>

<span data-ttu-id="1a496-191">Fator forma de implementação para o chip.</span><span class="sxs-lookup"><span data-stu-id="1a496-191">Implementation form factor for the chip.</span></span>

<span data-ttu-id="1a496-192">Esse valor vem do membro de **fator forma** da estrutura do **dispositivo de memória** nas informações do SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="1a496-192">This value comes from the **Form Factor** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="1a496-193">Essa propriedade é herdada [**do \_ chip CIM**](cim-chip.md).</span><span class="sxs-lookup"><span data-stu-id="1a496-193">This property is inherited from [**CIM\_Chip**](cim-chip.md).</span></span>

<dt>



 <span data-ttu-id="1a496-194"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="1a496-194">(0)</span></span>


</dt> <dd>

<span data-ttu-id="1a496-195">Unknown</span><span class="sxs-lookup"><span data-stu-id="1a496-195">Unknown</span></span>

</dd> <dt>



 <span data-ttu-id="1a496-196">(1)</span><span class="sxs-lookup"><span data-stu-id="1a496-196">(1)</span></span>


</dt> <dd>

<span data-ttu-id="1a496-197">Outro</span><span class="sxs-lookup"><span data-stu-id="1a496-197">Other</span></span>

</dd> <dt>



 <span data-ttu-id="1a496-198">(2)</span><span class="sxs-lookup"><span data-stu-id="1a496-198">(2)</span></span>


</dt> <dd>

<span data-ttu-id="1a496-199">SIP</span><span class="sxs-lookup"><span data-stu-id="1a496-199">SIP</span></span>

</dd> <dt>



 <span data-ttu-id="1a496-200">(3)</span><span class="sxs-lookup"><span data-stu-id="1a496-200">(3)</span></span>


</dt> <dd>

<span data-ttu-id="1a496-201">DIP</span><span class="sxs-lookup"><span data-stu-id="1a496-201">DIP</span></span>

</dd> <dt>



 <span data-ttu-id="1a496-202">(4)</span><span class="sxs-lookup"><span data-stu-id="1a496-202">(4)</span></span>


</dt> <dd>

<span data-ttu-id="1a496-203">ZIP</span><span class="sxs-lookup"><span data-stu-id="1a496-203">ZIP</span></span>

</dd> <dt>



 <span data-ttu-id="1a496-204">(5)</span><span class="sxs-lookup"><span data-stu-id="1a496-204">(5)</span></span>


</dt> <dd>

<span data-ttu-id="1a496-205">SOJ</span><span class="sxs-lookup"><span data-stu-id="1a496-205">SOJ</span></span>

</dd> <dt>



 <span data-ttu-id="1a496-206"> (6)</span><span class="sxs-lookup"><span data-stu-id="1a496-206">(6)</span></span>


</dt> <dd>

<span data-ttu-id="1a496-207">Proprietário</span><span class="sxs-lookup"><span data-stu-id="1a496-207">Proprietary</span></span>

</dd> <dt>



 <span data-ttu-id="1a496-208">(7)</span><span class="sxs-lookup"><span data-stu-id="1a496-208">(7)</span></span>


</dt> <dd>

<span data-ttu-id="1a496-209">SIMM</span><span class="sxs-lookup"><span data-stu-id="1a496-209">SIMM</span></span>

</dd> <dt>



 <span data-ttu-id="1a496-210">(8)</span><span class="sxs-lookup"><span data-stu-id="1a496-210">(8)</span></span>


</dt> <dd>

<span data-ttu-id="1a496-211">ACTIVA</span><span class="sxs-lookup"><span data-stu-id="1a496-211">DIMM</span></span>

</dd> <dt>



 <span data-ttu-id="1a496-212">(9)</span><span class="sxs-lookup"><span data-stu-id="1a496-212">(9)</span></span>


</dt> <dd>

<span data-ttu-id="1a496-213">TSOP</span><span class="sxs-lookup"><span data-stu-id="1a496-213">TSOP</span></span>

</dd> <dt>



 <span data-ttu-id="1a496-214">(10)</span><span class="sxs-lookup"><span data-stu-id="1a496-214">(10)</span></span>


</dt> <dd>

<span data-ttu-id="1a496-215">PGA</span><span class="sxs-lookup"><span data-stu-id="1a496-215">PGA</span></span>

</dd> <dt>



 <span data-ttu-id="1a496-216">(11)</span><span class="sxs-lookup"><span data-stu-id="1a496-216">(11)</span></span>


</dt> <dd>

<span data-ttu-id="1a496-217">DIMM</span><span class="sxs-lookup"><span data-stu-id="1a496-217">RIMM</span></span>

</dd> <dt>



 <span data-ttu-id="1a496-218">12</span><span class="sxs-lookup"><span data-stu-id="1a496-218">(12)</span></span>


</dt> <dd>

<span data-ttu-id="1a496-219">SODIMM</span><span class="sxs-lookup"><span data-stu-id="1a496-219">SODIMM</span></span>

</dd> <dt>



 <span data-ttu-id="1a496-220">(13)</span><span class="sxs-lookup"><span data-stu-id="1a496-220">(13)</span></span>


</dt> <dd>

<span data-ttu-id="1a496-221">SRIMM</span><span class="sxs-lookup"><span data-stu-id="1a496-221">SRIMM</span></span>

</dd> <dt>



 <span data-ttu-id="1a496-222">(14)</span><span class="sxs-lookup"><span data-stu-id="1a496-222">(14)</span></span>


</dt> <dd>

<span data-ttu-id="1a496-223">SMD</span><span class="sxs-lookup"><span data-stu-id="1a496-223">SMD</span></span>

</dd> <dt>



 <span data-ttu-id="1a496-224">(15)</span><span class="sxs-lookup"><span data-stu-id="1a496-224">(15)</span></span>


</dt> <dd>

<span data-ttu-id="1a496-225">SSMP</span><span class="sxs-lookup"><span data-stu-id="1a496-225">SSMP</span></span>

</dd> <dt>



 <span data-ttu-id="1a496-226">(16)</span><span class="sxs-lookup"><span data-stu-id="1a496-226">(16)</span></span>


</dt> <dd>

<span data-ttu-id="1a496-227">QFP</span><span class="sxs-lookup"><span data-stu-id="1a496-227">QFP</span></span>

</dd> <dt>



 <span data-ttu-id="1a496-228">(17)</span><span class="sxs-lookup"><span data-stu-id="1a496-228">(17)</span></span>


</dt> <dd>

<span data-ttu-id="1a496-229">TQFP</span><span class="sxs-lookup"><span data-stu-id="1a496-229">TQFP</span></span>

</dd> <dt>



 <span data-ttu-id="1a496-230">(18)</span><span class="sxs-lookup"><span data-stu-id="1a496-230">(18)</span></span>


</dt> <dd>

<span data-ttu-id="1a496-231">SOIC</span><span class="sxs-lookup"><span data-stu-id="1a496-231">SOIC</span></span>

</dd> <dt>



 <span data-ttu-id="1a496-232">(19)</span><span class="sxs-lookup"><span data-stu-id="1a496-232">(19)</span></span>


</dt> <dd>

<span data-ttu-id="1a496-233">LCCS</span><span class="sxs-lookup"><span data-stu-id="1a496-233">LCC</span></span>

</dd> <dt>



 <span data-ttu-id="1a496-234">(20)</span><span class="sxs-lookup"><span data-stu-id="1a496-234">(20)</span></span>


</dt> <dd>

<span data-ttu-id="1a496-235">PLCC</span><span class="sxs-lookup"><span data-stu-id="1a496-235">PLCC</span></span>

</dd> <dt>



 <span data-ttu-id="1a496-236">(21)</span><span class="sxs-lookup"><span data-stu-id="1a496-236">(21)</span></span>


</dt> <dd>

<span data-ttu-id="1a496-237">BGA</span><span class="sxs-lookup"><span data-stu-id="1a496-237">BGA</span></span>

</dd> <dt>



 <span data-ttu-id="1a496-238">(22)</span><span class="sxs-lookup"><span data-stu-id="1a496-238">(22)</span></span>


</dt> <dd>

<span data-ttu-id="1a496-239">FPBGA</span><span class="sxs-lookup"><span data-stu-id="1a496-239">FPBGA</span></span>

</dd> <dt>



 <span data-ttu-id="1a496-240">(23)</span><span class="sxs-lookup"><span data-stu-id="1a496-240">(23)</span></span>


</dt> <dd>

<span data-ttu-id="1a496-241">LGA</span><span class="sxs-lookup"><span data-stu-id="1a496-241">LGA</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1a496-242">**HotSwappable**</span><span class="sxs-lookup"><span data-stu-id="1a496-242">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a496-243">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="1a496-243">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1a496-244">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1a496-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a496-245">Se **for true**, esse componente de mídia física poderá ser substituído por um fisicamente diferente, mas equivalente a um, enquanto o pacote de contenção tiver a potência aplicada.</span><span class="sxs-lookup"><span data-stu-id="1a496-245">If **TRUE**, this physical media component can be replaced with a physically different but equivalent one while the containing package has the power applied.</span></span> <span data-ttu-id="1a496-246">Por exemplo, um componente de ventilador pode ser projetado para ser intercambiável.</span><span class="sxs-lookup"><span data-stu-id="1a496-246">For example, a fan component may be designed to be hot-swapped.</span></span> <span data-ttu-id="1a496-247">Todos os componentes que podem ser intercambiáveis são inerentemente removíveis e substituíveis.</span><span class="sxs-lookup"><span data-stu-id="1a496-247">All components that can be hot-swapped are inherently removable and replaceable.</span></span>

<span data-ttu-id="1a496-248">Essa propriedade é herdada do [**CIM \_ PhysicalComponent**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="1a496-248">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="1a496-249">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="1a496-249">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a496-250">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="1a496-250">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1a496-251">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1a496-251">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a496-252">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="1a496-252">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="1a496-253">Data e hora em que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="1a496-253">Date and time the object is installed.</span></span> <span data-ttu-id="1a496-254">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="1a496-254">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="1a496-255">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1a496-255">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1a496-256">**InterleaveDataDepth**</span><span class="sxs-lookup"><span data-stu-id="1a496-256">**InterleaveDataDepth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a496-257">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1a496-257">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1a496-258">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1a496-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a496-259">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| intensidade de \| dados intercalados do SMBIOS tipo 20")</span><span class="sxs-lookup"><span data-stu-id="1a496-259">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 20\|Interleaved Data Depth")</span></span>
</dt> </dl>

<span data-ttu-id="1a496-260">Número máximo de linhas consecutivas de dados de 16 bits não assinados que são acessados em uma única transferência intercalada do dispositivo de memória.</span><span class="sxs-lookup"><span data-stu-id="1a496-260">Unsigned 16-bit integer maximum number of consecutive rows of data that are accessed in a single interleaved transfer from the memory device.</span></span> <span data-ttu-id="1a496-261">Se o valor for 0 (zero), a memória não será intercalada.</span><span class="sxs-lookup"><span data-stu-id="1a496-261">If the value is 0 (zero), the memory is not interleaved.</span></span>

</dd> <dt>

<span data-ttu-id="1a496-262">**InterleavePosition**</span><span class="sxs-lookup"><span data-stu-id="1a496-262">**InterleavePosition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a496-263">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1a496-263">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1a496-264">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1a496-264">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a496-265">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Endereços mapeados do dispositivo de memória DMTF \| 1,7 ")</span><span class="sxs-lookup"><span data-stu-id="1a496-265">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Memory Device Mapped Addresses\|001.7")</span></span>
</dt> </dl>

<span data-ttu-id="1a496-266">Posição da memória física em uma intercalação.</span><span class="sxs-lookup"><span data-stu-id="1a496-266">Position of the physical memory in an interleave.</span></span> <span data-ttu-id="1a496-267">Por exemplo, em uma intercalação 2:1, um valor de "1" indica que a memória está na posição "uniforme".</span><span class="sxs-lookup"><span data-stu-id="1a496-267">For example, in a 2:1 interleave, a value of "1" indicates that the memory is in the "even" position.</span></span>

<span data-ttu-id="1a496-268">Essa propriedade é herdada do [**CIM \_ PhysicalMemory**](cim-physicalmemory.md).</span><span class="sxs-lookup"><span data-stu-id="1a496-268">This property is inherited from [**CIM\_PhysicalMemory**](cim-physicalmemory.md).</span></span>

<dt>

<span data-ttu-id="1a496-269">0</span><span class="sxs-lookup"><span data-stu-id="1a496-269">0</span></span>
</dt> <dd>

<span data-ttu-id="1a496-270">Não intercalado</span><span class="sxs-lookup"><span data-stu-id="1a496-270">Noninterleaved</span></span>

</dd> <dt>

<span data-ttu-id="1a496-271">1</span><span class="sxs-lookup"><span data-stu-id="1a496-271">1</span></span>
</dt> <dd>

<span data-ttu-id="1a496-272">Primeira posição</span><span class="sxs-lookup"><span data-stu-id="1a496-272">First position</span></span>

</dd> <dt>

<span data-ttu-id="1a496-273">2</span><span class="sxs-lookup"><span data-stu-id="1a496-273">2</span></span>
</dt> <dd>

<span data-ttu-id="1a496-274">Segunda posição</span><span class="sxs-lookup"><span data-stu-id="1a496-274">Second position</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1a496-275">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="1a496-275">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a496-276">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1a496-276">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1a496-277">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1a496-277">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a496-278">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="1a496-278">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="1a496-279">Nome da organização responsável por produzir o elemento físico.</span><span class="sxs-lookup"><span data-stu-id="1a496-279">Name of the organization responsible for producing the physical element.</span></span>

<span data-ttu-id="1a496-280">Esse valor é proveniente do membro do **fabricante** da estrutura do **dispositivo de memória** nas informações do SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="1a496-280">This value comes from the **Manufacturer** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="1a496-281">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="1a496-281">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1a496-282">**MaxVoltage**</span><span class="sxs-lookup"><span data-stu-id="1a496-282">**MaxVoltage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a496-283">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1a496-283">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1a496-284">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1a496-284">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a496-285">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| tipo SMBIOS 17 \| tensão máxima")</span><span class="sxs-lookup"><span data-stu-id="1a496-285">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 17\|Maximum voltage")</span></span>
</dt> </dl>

<span data-ttu-id="1a496-286">A tensão de operação máxima para este dispositivo, em milivolts ou 0, se a tensão for desconhecida.</span><span class="sxs-lookup"><span data-stu-id="1a496-286">The maximum operating voltage for this device, in millivolts, or 0, if the voltage is unknown.</span></span>

<span data-ttu-id="1a496-287">Esse valor é proveniente do membro de **tensão máxima** da estrutura do **dispositivo de memória** nas informações do SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="1a496-287">This value comes from the **Maximum voltage** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="1a496-288">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows server 2008 e Windows Vista:** Não há suporte para essa propriedade antes do Windows Server 2016 e do Windows 10.</span><span class="sxs-lookup"><span data-stu-id="1a496-288">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows Server 2016 and Windows 10.</span></span>

</dd> <dt>

<span data-ttu-id="1a496-289">**Memorytype**</span><span class="sxs-lookup"><span data-stu-id="1a496-289">**MemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a496-290">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1a496-290">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1a496-291">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1a496-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a496-292">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Dispositivo de memória DMTF \| 2,9 ")</span><span class="sxs-lookup"><span data-stu-id="1a496-292">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Memory Device\|002.9")</span></span>
</dt> </dl>

<span data-ttu-id="1a496-293">Tipo de memória física.</span><span class="sxs-lookup"><span data-stu-id="1a496-293">Type of physical memory.</span></span> <span data-ttu-id="1a496-294">Esse é um valor CIM que é mapeado para o valor SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="1a496-294">This is a CIM value that is mapped to the SMBIOS value.</span></span> <span data-ttu-id="1a496-295">A propriedade **SMBIOSMemoryType** contém o tipo de memória de SMBIOS bruto.</span><span class="sxs-lookup"><span data-stu-id="1a496-295">The **SMBIOSMemoryType** property contains the raw SMBIOS memory type.</span></span>

<span data-ttu-id="1a496-296">Esse valor é proveniente do membro do **tipo de memória** da estrutura do **dispositivo de memória** nas informações do SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="1a496-296">This value comes from the **Memory Type** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="1a496-297">Essa propriedade é herdada do [**CIM \_ PhysicalMemory**](cim-physicalmemory.md).</span><span class="sxs-lookup"><span data-stu-id="1a496-297">This property is inherited from [**CIM\_PhysicalMemory**](cim-physicalmemory.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1a496-298"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="1a496-298"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1a496-299"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="1a496-299"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="DRAM"></span><span id="dram"></span>

<span data-ttu-id="1a496-300"><span id="DRAM"></span><span id="dram"></span>**DRAM** (2)</span><span class="sxs-lookup"><span data-stu-id="1a496-300"><span id="DRAM"></span><span id="dram"></span>**DRAM** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Synchronous_DRAM"></span><span id="synchronous_dram"></span><span id="SYNCHRONOUS_DRAM"></span>

<span data-ttu-id="1a496-301"><span id="Synchronous_DRAM"></span><span id="synchronous_dram"></span><span id="SYNCHRONOUS_DRAM"></span>**DRAM síncrona** (3)</span><span class="sxs-lookup"><span data-stu-id="1a496-301"><span id="Synchronous_DRAM"></span><span id="synchronous_dram"></span><span id="SYNCHRONOUS_DRAM"></span>**Synchronous DRAM** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Cache_DRAM"></span><span id="cache_dram"></span><span id="CACHE_DRAM"></span>

<span data-ttu-id="1a496-302"><span id="Cache_DRAM"></span><span id="cache_dram"></span><span id="CACHE_DRAM"></span>**DRAM de cache** (4)</span><span class="sxs-lookup"><span data-stu-id="1a496-302"><span id="Cache_DRAM"></span><span id="cache_dram"></span><span id="CACHE_DRAM"></span>**Cache DRAM** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="EDO"></span><span id="edo"></span>

<span data-ttu-id="1a496-303"><span id="EDO"></span><span id="edo"></span>**Edo** (5)</span><span class="sxs-lookup"><span data-stu-id="1a496-303"><span id="EDO"></span><span id="edo"></span>**EDO** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="EDRAM"></span><span id="edram"></span>

<span data-ttu-id="1a496-304"><span id="EDRAM"></span><span id="edram"></span>**EDRAM** (6)</span><span class="sxs-lookup"><span data-stu-id="1a496-304"><span id="EDRAM"></span><span id="edram"></span>**EDRAM** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="VRAM"></span><span id="vram"></span>

<span data-ttu-id="1a496-305"><span id="VRAM"></span><span id="vram"></span>**VRAM** (7)</span><span class="sxs-lookup"><span data-stu-id="1a496-305"><span id="VRAM"></span><span id="vram"></span>**VRAM** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SRAM"></span><span id="sram"></span>

<span data-ttu-id="1a496-306"><span id="SRAM"></span><span id="sram"></span>**SRAM** (8)</span><span class="sxs-lookup"><span data-stu-id="1a496-306"><span id="SRAM"></span><span id="sram"></span>**SRAM** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="RAM"></span><span id="ram"></span>

<span data-ttu-id="1a496-307"><span id="RAM"></span><span id="ram"></span>**RAM** (9)</span><span class="sxs-lookup"><span data-stu-id="1a496-307"><span id="RAM"></span><span id="ram"></span>**RAM** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="ROM"></span><span id="rom"></span>

<span data-ttu-id="1a496-308"><span id="ROM"></span><span id="rom"></span>**ROM** (10)</span><span class="sxs-lookup"><span data-stu-id="1a496-308"><span id="ROM"></span><span id="rom"></span>**ROM** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Flash"></span><span id="flash"></span><span id="FLASH"></span>

<span data-ttu-id="1a496-309"><span id="Flash"></span><span id="flash"></span><span id="FLASH"></span>**Flash** (11)</span><span class="sxs-lookup"><span data-stu-id="1a496-309"><span id="Flash"></span><span id="flash"></span><span id="FLASH"></span>**Flash** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="EEPROM"></span><span id="eeprom"></span>

<span data-ttu-id="1a496-310"><span id="EEPROM"></span><span id="eeprom"></span>**EEPROM** (12)</span><span class="sxs-lookup"><span data-stu-id="1a496-310"><span id="EEPROM"></span><span id="eeprom"></span>**EEPROM** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="FEPROM"></span><span id="feprom"></span>

<span data-ttu-id="1a496-311"><span id="FEPROM"></span><span id="feprom"></span>**FEPROM** (13)</span><span class="sxs-lookup"><span data-stu-id="1a496-311"><span id="FEPROM"></span><span id="feprom"></span>**FEPROM** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="EPROM"></span><span id="eprom"></span>

<span data-ttu-id="1a496-312"><span id="EPROM"></span><span id="eprom"></span>**(14** )</span><span class="sxs-lookup"><span data-stu-id="1a496-312"><span id="EPROM"></span><span id="eprom"></span>**EPROM** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="CDRAM"></span><span id="cdram"></span>

<span data-ttu-id="1a496-313"><span id="CDRAM"></span><span id="cdram"></span>**CDRAM** (15)</span><span class="sxs-lookup"><span data-stu-id="1a496-313"><span id="CDRAM"></span><span id="cdram"></span>**CDRAM** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="3DRAM"></span><span id="3dram"></span>

<span data-ttu-id="1a496-314"><span id="3DRAM"></span><span id="3dram"></span>**3DRAM** (16)</span><span class="sxs-lookup"><span data-stu-id="1a496-314"><span id="3DRAM"></span><span id="3dram"></span>**3DRAM** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="SDRAM"></span><span id="sdram"></span>

<span data-ttu-id="1a496-315"><span id="SDRAM"></span><span id="sdram"></span>**SDRAM** (17)</span><span class="sxs-lookup"><span data-stu-id="1a496-315"><span id="SDRAM"></span><span id="sdram"></span>**SDRAM** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="SGRAM"></span><span id="sgram"></span>

<span data-ttu-id="1a496-316"><span id="SGRAM"></span><span id="sgram"></span>**SGRAM** (18)</span><span class="sxs-lookup"><span data-stu-id="1a496-316"><span id="SGRAM"></span><span id="sgram"></span>**SGRAM** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="RDRAM"></span><span id="rdram"></span>

<span data-ttu-id="1a496-317"><span id="RDRAM"></span><span id="rdram"></span>**RDRAM** (19)</span><span class="sxs-lookup"><span data-stu-id="1a496-317"><span id="RDRAM"></span><span id="rdram"></span>**RDRAM** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="DDR"></span><span id="ddr"></span>

<span data-ttu-id="1a496-318"><span id="DDR"></span><span id="ddr"></span>**DDR** (20)</span><span class="sxs-lookup"><span data-stu-id="1a496-318"><span id="DDR"></span><span id="ddr"></span>**DDR** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="DDR2"></span><span id="ddr2"></span>

<span data-ttu-id="1a496-319"><span id="DDR2"></span><span id="ddr2"></span>**DDR2** (21)</span><span class="sxs-lookup"><span data-stu-id="1a496-319"><span id="DDR2"></span><span id="ddr2"></span>**DDR2** (21)</span></span>


</dt> <dd>

<span data-ttu-id="1a496-320">DDR2 — pode não estar disponível.</span><span class="sxs-lookup"><span data-stu-id="1a496-320">DDR2—May not be available.</span></span>

</dd> <dt>

<span id="DDR2_FB-DIMM"></span><span id="ddr2_fb-dimm"></span>

<span data-ttu-id="1a496-321"><span id="DDR2_FB-DIMM"></span><span id="ddr2_fb-dimm"></span>**DDR2 FB-DIMM** (22)</span><span class="sxs-lookup"><span data-stu-id="1a496-321"><span id="DDR2_FB-DIMM"></span><span id="ddr2_fb-dimm"></span>**DDR2 FB-DIMM** (22)</span></span>


</dt> <dd>

<span data-ttu-id="1a496-322">O DDR2 – FB-DIMM, pode não estar disponível.</span><span class="sxs-lookup"><span data-stu-id="1a496-322">DDR2—FB-DIMM,May not be available.</span></span>

</dd> <dt>

<span data-ttu-id="1a496-323">24</span><span class="sxs-lookup"><span data-stu-id="1a496-323">24</span></span>
</dt> <dd>

<span data-ttu-id="1a496-324">DDR3 — pode não estar disponível.</span><span class="sxs-lookup"><span data-stu-id="1a496-324">DDR3—May not be available.</span></span>

</dd> <dt>

<span data-ttu-id="1a496-325">25</span><span class="sxs-lookup"><span data-stu-id="1a496-325">25</span></span>
</dt> <dd>

<span data-ttu-id="1a496-326">FBD2</span><span class="sxs-lookup"><span data-stu-id="1a496-326">FBD2</span></span>

</dt> <dd></dd> <dt>

<span data-ttu-id="1a496-327"><span id="DDR4"></span><span id="DDR4"></span>**DDR4** (26)</span><span class="sxs-lookup"><span data-stu-id="1a496-327"><span id="DDR4"></span><span id="DDR4"></span>**DDR4** (26)</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1a496-328">**MinVoltage**</span><span class="sxs-lookup"><span data-stu-id="1a496-328">**MinVoltage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a496-329">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1a496-329">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1a496-330">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1a496-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a496-331">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("tipo de SMBIOS \| 20 de \| Voltagem mínima")</span><span class="sxs-lookup"><span data-stu-id="1a496-331">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 20\|Minimum voltage")</span></span>
</dt> </dl>

<span data-ttu-id="1a496-332">A tensão operacional mínima para este dispositivo, em milivolts ou 0, se a tensão for desconhecida.</span><span class="sxs-lookup"><span data-stu-id="1a496-332">The minimum operating voltage for this device, in millivolts, or 0, if the voltage is unknown.</span></span>

<span data-ttu-id="1a496-333">Esse valor é proveniente do membro de **tensão mínima** da estrutura do **dispositivo de memória** nas informações do SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="1a496-333">This value comes from the **Minimum voltage** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="1a496-334">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows server 2008 e Windows Vista:** Não há suporte para essa propriedade antes do Windows Server 2016 e do Windows 10.</span><span class="sxs-lookup"><span data-stu-id="1a496-334">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows Server 2016 and Windows 10.</span></span>

</dd> <dt>

<span data-ttu-id="1a496-335">**Modelo**</span><span class="sxs-lookup"><span data-stu-id="1a496-335">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a496-336">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1a496-336">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1a496-337">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1a496-337">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a496-338">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="1a496-338">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="1a496-339">Nome do elemento físico.</span><span class="sxs-lookup"><span data-stu-id="1a496-339">Name for the physical element.</span></span>

<span data-ttu-id="1a496-340">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="1a496-340">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1a496-341">**Nome**</span><span class="sxs-lookup"><span data-stu-id="1a496-341">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a496-342">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1a496-342">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1a496-343">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1a496-343">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a496-344">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="1a496-344">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="1a496-345">Rótulo do objeto.</span><span class="sxs-lookup"><span data-stu-id="1a496-345">Label for the object.</span></span> <span data-ttu-id="1a496-346">Quando em uma subclasse, a propriedade pode ser substituída para ser uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="1a496-346">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="1a496-347">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1a496-347">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1a496-348">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="1a496-348">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a496-349">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1a496-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1a496-350">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1a496-350">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a496-351">Dados adicionais, além das informações de marca do ativo, que podem ser usados para identificar um elemento físico.</span><span class="sxs-lookup"><span data-stu-id="1a496-351">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="1a496-352">Um exemplo são os dados de código de barras associados a um elemento que também tem uma marca de ativo.</span><span class="sxs-lookup"><span data-stu-id="1a496-352">One example is bar code data associated with an element that also has an asset tag.</span></span> <span data-ttu-id="1a496-353">Se apenas os dados de código de barras estiverem disponíveis e exclusivos ou puderem ser usados como uma chave de elemento, essa propriedade será **NULL** e os dados de código de barras serão usados como a chave de classe na propriedade de marca.</span><span class="sxs-lookup"><span data-stu-id="1a496-353">If only bar code data is available and unique or able to be used as an element key, this property is be **NULL** and the bar code data is used as the class key in the tag property.</span></span>

<span data-ttu-id="1a496-354">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="1a496-354">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1a496-355">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="1a496-355">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a496-356">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1a496-356">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1a496-357">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1a496-357">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a496-358">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="1a496-358">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="1a496-359">Número de peça atribuído pela organização responsável por produzir ou fabricar o elemento físico.</span><span class="sxs-lookup"><span data-stu-id="1a496-359">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="1a496-360">Esse valor é proveniente do membro de **número de peça** da estrutura de **dispositivo de memória** nas informações de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="1a496-360">This value comes from the **Part Number** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="1a496-361">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="1a496-361">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1a496-362">**PositionInRow**</span><span class="sxs-lookup"><span data-stu-id="1a496-362">**PositionInRow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a496-363">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1a496-363">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1a496-364">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1a496-364">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a496-365">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Endereços mapeados do dispositivo de memória DMTF \| 1,6 ")</span><span class="sxs-lookup"><span data-stu-id="1a496-365">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Memory Device Mapped Addresses\|001.6")</span></span>
</dt> </dl>

<span data-ttu-id="1a496-366">Posição da memória física em uma linha.</span><span class="sxs-lookup"><span data-stu-id="1a496-366">Position of the physical memory in a row.</span></span> <span data-ttu-id="1a496-367">Por exemplo, se usar dispositivos de memória de 2 8 bits para formar uma linha de 16 bits, um valor de 2 (dois) significa que essa memória é o segundo dispositivo — 0 (zero) é um valor inválido para essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="1a496-367">For example, if it takes two 8-bit memory devices to form a 16-bit row, then a value of 2 (two) means that this memory is the second device—0 (zero) is an invalid value for this property.</span></span>

<span data-ttu-id="1a496-368">Essa propriedade é herdada do [**CIM \_ PhysicalMemory**](cim-physicalmemory.md).</span><span class="sxs-lookup"><span data-stu-id="1a496-368">This property is inherited from [**CIM\_PhysicalMemory**](cim-physicalmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="1a496-369">**Ligado**</span><span class="sxs-lookup"><span data-stu-id="1a496-369">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a496-370">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="1a496-370">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1a496-371">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1a496-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a496-372">Se **for true**, o elemento físico será ligado.</span><span class="sxs-lookup"><span data-stu-id="1a496-372">If **TRUE**, the physical element is powered on.</span></span>

<span data-ttu-id="1a496-373">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="1a496-373">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1a496-374">**Removível**</span><span class="sxs-lookup"><span data-stu-id="1a496-374">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a496-375">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="1a496-375">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1a496-376">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1a496-376">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a496-377">Se for **true**, um componente físico será removível (se for projetado para ser colocado dentro e fora do contêiner físico no qual ele é normalmente encontrado, sem encontrar a função do empacotamento geral).</span><span class="sxs-lookup"><span data-stu-id="1a496-377">If **TRUE**, a physical component is removable (if it is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging).</span></span> <span data-ttu-id="1a496-378">Um componente ainda poderá ser removível se a energia precisar ser "desativada" para executar a remoção.</span><span class="sxs-lookup"><span data-stu-id="1a496-378">A component can still be removable if power must be "off" to perform the removal.</span></span> <span data-ttu-id="1a496-379">Se a energia puder ser "ativada" e o componente for removido, o elemento será removível e poderá ser intercambiável.</span><span class="sxs-lookup"><span data-stu-id="1a496-379">If power can be "on" and the component removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="1a496-380">Por exemplo, um chip de processador atualizável é removível.</span><span class="sxs-lookup"><span data-stu-id="1a496-380">For example, an upgradable processor chip is removable.</span></span>

<span data-ttu-id="1a496-381">Essa propriedade é herdada do [**CIM \_ PhysicalComponent**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="1a496-381">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="1a496-382">**Peças**</span><span class="sxs-lookup"><span data-stu-id="1a496-382">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a496-383">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="1a496-383">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1a496-384">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1a496-384">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a496-385">Se **for true**, esse componente de mídia física poderá ser substituído por um fisicamente diferente.</span><span class="sxs-lookup"><span data-stu-id="1a496-385">If **TRUE**, this physical media component can be replaced with a physically different one.</span></span> <span data-ttu-id="1a496-386">Por exemplo, alguns sistemas de computador permitem que o chip do processador principal seja atualizado para uma classificação de clock mais alta.</span><span class="sxs-lookup"><span data-stu-id="1a496-386">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="1a496-387">Nesse caso, diz-se que o processador é substituível.</span><span class="sxs-lookup"><span data-stu-id="1a496-387">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="1a496-388">Todos os componentes removíveis são inerentemente substituíveis.</span><span class="sxs-lookup"><span data-stu-id="1a496-388">All removable components are inherently replaceable.</span></span>

<span data-ttu-id="1a496-389">Essa propriedade é herdada do [**CIM \_ PhysicalComponent**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="1a496-389">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="1a496-390">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="1a496-390">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a496-391">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1a496-391">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1a496-392">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1a496-392">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a496-393">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="1a496-393">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="1a496-394">O número alocado pelo fabricante para identificar o elemento físico.</span><span class="sxs-lookup"><span data-stu-id="1a496-394">Manufacturer-allocated number to identify the physical element.</span></span>

<span data-ttu-id="1a496-395">Esse valor é proveniente do membro de **número de série** da estrutura de **dispositivo de memória** nas informações de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="1a496-395">This value comes from the **Serial Number** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="1a496-396">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="1a496-396">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1a496-397">**SKU**</span><span class="sxs-lookup"><span data-stu-id="1a496-397">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a496-398">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1a496-398">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1a496-399">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1a496-399">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a496-400">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="1a496-400">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="1a496-401">Número de unidade de manutenção de estoque do elemento físico.</span><span class="sxs-lookup"><span data-stu-id="1a496-401">Stock keeping unit number for the physical element.</span></span>

<span data-ttu-id="1a496-402">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="1a496-402">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1a496-403">**SMBIOSMemoryType**</span><span class="sxs-lookup"><span data-stu-id="1a496-403">**SMBIOSMemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a496-404">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1a496-404">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1a496-405">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1a496-405">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a496-406">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("tipo de memória do SMBIOS \| tipo 17 \| \_ ")</span><span class="sxs-lookup"><span data-stu-id="1a496-406">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 17\|Memory\_Type")</span></span>
</dt> </dl>

<span data-ttu-id="1a496-407">O tipo de memória do SMBIOS bruto.</span><span class="sxs-lookup"><span data-stu-id="1a496-407">The raw SMBIOS memory type.</span></span> <span data-ttu-id="1a496-408">O valor da propriedade **memorytype** é um valor CIM que é mapeado para o valor SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="1a496-408">The value of the **MemoryType** property is a CIM value that is mapped to the SMBIOS value.</span></span>

<span data-ttu-id="1a496-409">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows server 2008 e Windows Vista:** Não há suporte para essa propriedade antes do Windows Server 2016 e do Windows 10.</span><span class="sxs-lookup"><span data-stu-id="1a496-409">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows Server 2016 and Windows 10.</span></span>

</dd> <dt>

<span data-ttu-id="1a496-410">**Velocidade**</span><span class="sxs-lookup"><span data-stu-id="1a496-410">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a496-411">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1a496-411">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1a496-412">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1a496-412">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a496-413">Qualificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("nanossegundos")</span><span class="sxs-lookup"><span data-stu-id="1a496-413">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("nanoseconds")</span></span>
</dt> </dl>

<span data-ttu-id="1a496-414">Velocidade da memória física — em nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="1a496-414">Speed of the physical memory—in nanoseconds.</span></span>

<span data-ttu-id="1a496-415">Esse valor é proveniente do membro **Speed** da estrutura do **dispositivo de memória** nas informações do SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="1a496-415">This value comes from the **Speed** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="1a496-416">Essa propriedade é herdada do [**CIM \_ PhysicalMemory**](cim-physicalmemory.md).</span><span class="sxs-lookup"><span data-stu-id="1a496-416">This property is inherited from [**CIM\_PhysicalMemory**](cim-physicalmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="1a496-417">**Status**</span><span class="sxs-lookup"><span data-stu-id="1a496-417">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a496-418">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1a496-418">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1a496-419">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1a496-419">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a496-420">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="1a496-420">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="1a496-421">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="1a496-421">Current status of the object.</span></span> <span data-ttu-id="1a496-422">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="1a496-422">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="1a496-423">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="1a496-423">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="1a496-424">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="1a496-424">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="1a496-425">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="1a496-425">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="1a496-426">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="1a496-426">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="1a496-427">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1a496-427">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="1a496-428">Os valores possíveis são.</span><span class="sxs-lookup"><span data-stu-id="1a496-428">The possible values are.</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="1a496-429">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="1a496-429">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="1a496-430">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="1a496-430">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="1a496-431">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="1a496-431">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1a496-432">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="1a496-432">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="1a496-433">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="1a496-433">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="1a496-434">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="1a496-434">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="1a496-435">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="1a496-435">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="1a496-436">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="1a496-436">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="1a496-437">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="1a496-437">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="1a496-438">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="1a496-438">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="1a496-439">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="1a496-439">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="1a496-440">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="1a496-440">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1a496-441">**Tag**</span><span class="sxs-lookup"><span data-stu-id="1a496-441">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a496-442">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1a496-442">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1a496-443">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1a496-443">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a496-444">Qualificadores: [**Key**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**override**](../wmisdk/standard-qualifiers.md) ("tag"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="1a496-444">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**Override**](../wmisdk/standard-qualifiers.md) ("Tag"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="1a496-445">Identificador exclusivo para o dispositivo de memória física que é representado por uma instância do **Win32 \_ PhysicalMemory**.</span><span class="sxs-lookup"><span data-stu-id="1a496-445">Unique identifier for the physical memory device that is represented by an instance of **Win32\_PhysicalMemory**.</span></span> <span data-ttu-id="1a496-446">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="1a496-446">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

<span data-ttu-id="1a496-447">Exemplo: "memória física 1"</span><span class="sxs-lookup"><span data-stu-id="1a496-447">Example: "Physical Memory 1"</span></span>

</dd> <dt>

<span data-ttu-id="1a496-448">**TotalWidth**</span><span class="sxs-lookup"><span data-stu-id="1a496-448">**TotalWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a496-449">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1a496-449">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1a496-450">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1a496-450">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a496-451">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Dispositivo de memória DMTF \| 2,7 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" bits ")</span><span class="sxs-lookup"><span data-stu-id="1a496-451">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Memory Device\|002.7"), [**Units**](../wmisdk/standard-qualifiers.md) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="1a496-452">Largura total, em bits, da memória física, incluindo bits de verificação ou correção de erro.</span><span class="sxs-lookup"><span data-stu-id="1a496-452">Total width, in bits, of the physical memory, including check or error correction bits.</span></span> <span data-ttu-id="1a496-453">Se não houver nenhum bit de correção de erro, o valor nessa propriedade deverá corresponder ao que é especificado para a propriedade **datalargura** .</span><span class="sxs-lookup"><span data-stu-id="1a496-453">If there are no error correction bits, the value in this property should match what is specified for the **DataWidth** property.</span></span>

<span data-ttu-id="1a496-454">Esse valor é proveniente do membro de **largura total** da estrutura de **dispositivo de memória** nas informações de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="1a496-454">This value comes from the **Total Width** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="1a496-455">Essa propriedade é herdada do [**CIM \_ PhysicalMemory**](cim-physicalmemory.md).</span><span class="sxs-lookup"><span data-stu-id="1a496-455">This property is inherited from [**CIM\_PhysicalMemory**](cim-physicalmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="1a496-456">**TypeDetail**</span><span class="sxs-lookup"><span data-stu-id="1a496-456">**TypeDetail**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a496-457">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1a496-457">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1a496-458">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1a496-458">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a496-459">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("tipo de SMBIOS- \| \| detalhe de tipo 17")</span><span class="sxs-lookup"><span data-stu-id="1a496-459">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 17\|Type Detail")</span></span>
</dt> </dl>

<span data-ttu-id="1a496-460">Tipo de memória física representada.</span><span class="sxs-lookup"><span data-stu-id="1a496-460">Type of physical memory represented.</span></span>

<span data-ttu-id="1a496-461">Esse valor é proveniente do membro de **detalhes de tipo** da estrutura do **dispositivo de memória** nas informações do SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="1a496-461">This value comes from the **Type Detail** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="1a496-462"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Reservado** (1)</span><span class="sxs-lookup"><span data-stu-id="1a496-462"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Reserved** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1a496-463"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (2)</span><span class="sxs-lookup"><span data-stu-id="1a496-463"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1a496-464"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (4)</span><span class="sxs-lookup"><span data-stu-id="1a496-464"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Fast-paged"></span><span id="fast-paged"></span><span id="FAST-PAGED"></span>

<span data-ttu-id="1a496-465"><span id="Fast-paged"></span><span id="fast-paged"></span><span id="FAST-PAGED"></span>**Com página rápida** (8)</span><span class="sxs-lookup"><span data-stu-id="1a496-465"><span id="Fast-paged"></span><span id="fast-paged"></span><span id="FAST-PAGED"></span>**Fast-paged** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Static_column"></span><span id="static_column"></span><span id="STATIC_COLUMN"></span>

<span data-ttu-id="1a496-466"><span id="Static_column"></span><span id="static_column"></span><span id="STATIC_COLUMN"></span>**Coluna estática** (16)</span><span class="sxs-lookup"><span data-stu-id="1a496-466"><span id="Static_column"></span><span id="static_column"></span><span id="STATIC_COLUMN"></span>**Static column** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Pseudo-static"></span><span id="pseudo-static"></span><span id="PSEUDO-STATIC"></span>

<span data-ttu-id="1a496-467"><span id="Pseudo-static"></span><span id="pseudo-static"></span><span id="PSEUDO-STATIC"></span>**Pseudo-estático** (32)</span><span class="sxs-lookup"><span data-stu-id="1a496-467"><span id="Pseudo-static"></span><span id="pseudo-static"></span><span id="PSEUDO-STATIC"></span>**Pseudo-static** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="RAMBUS"></span><span id="rambus"></span>

<span data-ttu-id="1a496-468"><span id="RAMBUS"></span><span id="rambus"></span>**Rambus** (64)</span><span class="sxs-lookup"><span data-stu-id="1a496-468"><span id="RAMBUS"></span><span id="rambus"></span>**RAMBUS** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="Synchronous"></span><span id="synchronous"></span><span id="SYNCHRONOUS"></span>

<span data-ttu-id="1a496-469"><span id="Synchronous"></span><span id="synchronous"></span><span id="SYNCHRONOUS"></span>**Síncrono** (128)</span><span class="sxs-lookup"><span data-stu-id="1a496-469"><span id="Synchronous"></span><span id="synchronous"></span><span id="SYNCHRONOUS"></span>**Synchronous** (128)</span></span>


</dt> <dd></dd> <dt>

<span id="CMOS"></span><span id="cmos"></span>

<span data-ttu-id="1a496-470"><span id="CMOS"></span><span id="cmos"></span>**CMOS** (256)</span><span class="sxs-lookup"><span data-stu-id="1a496-470"><span id="CMOS"></span><span id="cmos"></span>**CMOS** (256)</span></span>


</dt> <dd></dd> <dt>

<span id="EDO"></span><span id="edo"></span>

<span data-ttu-id="1a496-471"><span id="EDO"></span><span id="edo"></span>**Edo** (512)</span><span class="sxs-lookup"><span data-stu-id="1a496-471"><span id="EDO"></span><span id="edo"></span>**EDO** (512)</span></span>


</dt> <dd></dd> <dt>

<span id="Window_DRAM"></span><span id="window_dram"></span><span id="WINDOW_DRAM"></span>

<span data-ttu-id="1a496-472"><span id="Window_DRAM"></span><span id="window_dram"></span><span id="WINDOW_DRAM"></span>**DRAM de janela** (1024)</span><span class="sxs-lookup"><span data-stu-id="1a496-472"><span id="Window_DRAM"></span><span id="window_dram"></span><span id="WINDOW_DRAM"></span>**Window DRAM** (1024)</span></span>


</dt> <dd></dd> <dt>

<span id="Cache_DRAM"></span><span id="cache_dram"></span><span id="CACHE_DRAM"></span>

<span data-ttu-id="1a496-473"><span id="Cache_DRAM"></span><span id="cache_dram"></span><span id="CACHE_DRAM"></span>**DRAM de cache** (2048)</span><span class="sxs-lookup"><span data-stu-id="1a496-473"><span id="Cache_DRAM"></span><span id="cache_dram"></span><span id="CACHE_DRAM"></span>**Cache DRAM** (2048)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-volatile"></span><span id="non-volatile"></span><span id="NON-VOLATILE"></span>

<span data-ttu-id="1a496-474"><span id="Non-volatile"></span><span id="non-volatile"></span><span id="NON-VOLATILE"></span>**Não volátil** (4096)</span><span class="sxs-lookup"><span data-stu-id="1a496-474"><span id="Non-volatile"></span><span id="non-volatile"></span><span id="NON-VOLATILE"></span>**Non-volatile** (4096)</span></span>


</dt> <dd>

<span data-ttu-id="1a496-475">Não volátil</span><span class="sxs-lookup"><span data-stu-id="1a496-475">Nonvolatile</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1a496-476">**Versão**</span><span class="sxs-lookup"><span data-stu-id="1a496-476">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a496-477">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1a496-477">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1a496-478">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1a496-478">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a496-479">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="1a496-479">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="1a496-480">Versão do elemento físico.</span><span class="sxs-lookup"><span data-stu-id="1a496-480">Version of the physical element.</span></span>

<span data-ttu-id="1a496-481">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="1a496-481">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1a496-482">Comentários</span><span class="sxs-lookup"><span data-stu-id="1a496-482">Remarks</span></span>

<span data-ttu-id="1a496-483">A classe **Win32 \_ PhysicalMemory** é derivada de [**CIM \_ PhysicalMemory**](cim-physicalmemory.md).</span><span class="sxs-lookup"><span data-stu-id="1a496-483">The **Win32\_PhysicalMemory** class is derived from [**CIM\_PhysicalMemory**](cim-physicalmemory.md).</span></span>

## <a name="examples"></a><span data-ttu-id="1a496-484">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1a496-484">Examples</span></span>

<span data-ttu-id="1a496-485">As [informações do computador get-ComputerInfo-Query de computadores locais/remotos-(WMI) exemplo do](https://Gallery.TechNet.Microsoft.Com/Get-ComputerInfo-Query-23dd6042) PowerShell na galeria do TechNet usam várias chamadas para hardware e software, incluindo **Win32 \_ PhysicalMemory**, para exibir informações sobre um sistema local ou remoto.</span><span class="sxs-lookup"><span data-stu-id="1a496-485">The [Get-ComputerInfo - Query Computer Info From Local/Remote Computers - (WMI)](https://Gallery.TechNet.Microsoft.Com/Get-ComputerInfo-Query-23dd6042) PowerShell sample on TechNet Gallery uses a number of calls to hardware and software, including **Win32\_PhysicalMemory**, to display information about a local or remote system.</span></span>

<span data-ttu-id="1a496-486">A amostra do PowerShell de [relatório do servidor](https://Gallery.TechNet.Microsoft.Com/Server-Report-7b4ac2fb) na galeria do TechNet usa várias chamadas para hardware e software, incluindo **Win32 \_ PhysicalMemory**, para coletar informações do servidor e publicar no documento do Word.</span><span class="sxs-lookup"><span data-stu-id="1a496-486">The [Server Report](https://Gallery.TechNet.Microsoft.Com/Server-Report-7b4ac2fb) PowerShell sample on TechNet gallery uses a number of calls to hardware and software, including **Win32\_PhysicalMemory**, to gather server information and publish in Word document.</span></span>

<span data-ttu-id="1a496-487">O exemplo de código do PowerShell a seguir recupera informações sobre a memória física do computador local.</span><span class="sxs-lookup"><span data-stu-id="1a496-487">The following PowerShell code sample retrieves information regarding the physical memory of the local computer.</span></span>


```PowerShell
function get-WmiMemoryFormFactor {
param ([uint16] $char)

If ($char -ge 0 -and  $char  -le 22) {

switch ($char) {
0     {"00-Unknown"}
1     {"01-Other"}
2     {"02-SiP"}
3     {"03-DIP"}
4     {"04-ZIP"}
5     {"05-SOJ"}
6     {"06-Proprietary"}
7     {"07-SIMM"}
8     {"08-DIMM"}
9     {"09-TSOPO"}
10     {"10-PGA"}
11     {"11-RIM"}
12     {"12-SODIMM"}
13     {"13-SRIMM"}
14     {"14-SMD"}
15     {"15-SSMP"}
16     {"16-QFP"}
17     {"17-TQFP"}
18     {"18-SOIC"}
19     {"19-LCC"}
20     {"20-PLCC"}
21     {"21-FPGA"}
22     {"22-LGA"}
}
}

else {"{0} - undefined value" -f $char
}

Return
}

# Helper function to return memory Interleave  Position

function get-WmiInterleavePosition {
param ([uint32] $char)

If ($char -ge 0 -and  $char -le 2) {

switch ($char) {
0     {"00-Non-Interleaved"}
1     {"01-First Position"}
2     {"02-Second Position"}
}
}

else {"{0} - undefined value" -f $char
}

Return
}


# Helper function to return Memory Tupe
function get-WmiMemoryType {
param ([uint16] $char)

If ($char -ge 0 -and  $char  -le 20) {

switch ($char) {
0     {"00-Unknown"}
1     {"01-Other"}
2     {"02-DRAM"}
3     {"03-Synchronous DRAM"}
4     {"04-Cache DRAM"}
5     {"05-EDO"}
6     {"06-EDRAM"}
7     {"07-VRAM"}
8     {"08-SRAM"}
9     {"09-ROM"}
10     {"10-ROM"}
11     {"11-FLASH"}
12     {"12-EEPROM"}
13     {"13-FEPROM"}
14     {"14-EPROM"}
15     {"15-CDRAM"}
16     {"16-3DRAM"}
17     {"17-SDRAM"}
18     {"18-SGRAM"}
19     {"19-RDRAM"}
20     {"20-DDR"}
}

}

else {"{0} - undefined value" -f $char
}

Return
}


# Get the object
$memory = Get-WMIObject Win32_PhysicalMemory

#  Format and Print
"System has {0} memory sticks:" -f $memory.count

Foreach ($stick in $memory) {

# Do some conversions
$cap=$stick.capacity/1mb
$ff=get-WmiMemoryFormFactor($stick.FormFactor)
$ilp=get-WmiInterleavePosition($stick.InterleavePosition)
$mt=get-WMIMemoryType($stick.MemoryType)

# print details of each stick
"BankLabel            {0}"  -f $stick.banklabel
"Capacity (MB)        {0}"  -f $cap
"Caption              {0}"  -f $stick.Caption
"CreationClassName    {0}"  -f $stick.creationclassname
"DataWidth            {0}"  -f $stick.DataWidth
"Description          {0}"  -f $stick.Description
"DeviceLocator        {0}"  -f $stick.DeviceLocator
"FormFactor           {0}"  -f $ff
"HotSwappable         {0}"  -f $stick.HotSwappable
"InstallDate          {0}"  -f $stick.InstallDate
"InterleaveDataDepth  {0}"  -f $stick.InterleaveDataDepth
"InterleavePosition   {0}"  -f $ilp
"Manufacturer         {0}"  -f $stick.Manufacturer
"MemoryType           {0}"  -f $mt
"Model                {0}"  -f $stick.Model
"Name                 {0}"  -f $stick.Name
"OtherIdentifyingInfo {0}"  -f $stick.OtherIdentifyingInfo
"PartNumber           {0}"  -f $stick.PartNumber
"PositionInRow        {0}"  -f $stick.PositionInRow
"PoweredOn            {0}"  -f $stick.PoweredOn
"Removable            {0}"  -f $stick.Removable
"Replaceable          {0}"  -f $stick.Replaceable
"SerialNumber         {0}"  -f $stick.SerialNumber
"SKU                  {0}"  -f $stick.SKU 
"Speed                {0}"  -f $stick.Speed 
"Status               {0}"  -f $stick.Status
"Tag                  {0}"  -f $stick.Tag
"TotalWidth           {0}"  -f $stick.TotalWidth 
"TypeDetail           {0}"  -f $stick.TypeDetail
"Version              {0}"  -f $stick.Version
""
}
"-----"
```



## <a name="requirements"></a><span data-ttu-id="1a496-488">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1a496-488">Requirements</span></span>



| <span data-ttu-id="1a496-489">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a496-489">Requirement</span></span> | <span data-ttu-id="1a496-490">Valor</span><span class="sxs-lookup"><span data-stu-id="1a496-490">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1a496-491">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1a496-491">Minimum supported client</span></span><br/> | <span data-ttu-id="1a496-492">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1a496-492">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1a496-493">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1a496-493">Minimum supported server</span></span><br/> | <span data-ttu-id="1a496-494">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1a496-494">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1a496-495">Namespace</span><span class="sxs-lookup"><span data-stu-id="1a496-495">Namespace</span></span><br/>                | <span data-ttu-id="1a496-496">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="1a496-496">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1a496-497">MOF</span><span class="sxs-lookup"><span data-stu-id="1a496-497">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1a496-498"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1a496-498"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1a496-499">DLL</span><span class="sxs-lookup"><span data-stu-id="1a496-499">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1a496-500"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1a496-500"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a496-501">Confira também</span><span class="sxs-lookup"><span data-stu-id="1a496-501">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a496-502">**\_PHYSICALMEMORY CIM**</span><span class="sxs-lookup"><span data-stu-id="1a496-502">**CIM\_PhysicalMemory**</span></span>](cim-physicalmemory.md)
</dt> <dt>

[<span data-ttu-id="1a496-503">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="1a496-503">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
