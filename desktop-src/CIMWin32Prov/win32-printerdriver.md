---
description: A \_ classe WMI PrinterDriver do Win32 representa os drivers para uma \_ instância de impressora Win32.
ms.assetid: baf48bbf-60a3-4d9b-93b7-c1b22518a9c1
ms.tgt_platform: multiple
title: Classe Win32_PrinterDriver
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterDriver
- Win32_PrinterDriver.Caption
- Win32_PrinterDriver.ConfigFile
- Win32_PrinterDriver.CreationClassName
- Win32_PrinterDriver.DataFile
- Win32_PrinterDriver.DefaultDataType
- Win32_PrinterDriver.DependentFiles
- Win32_PrinterDriver.Description
- Win32_PrinterDriver.DriverPath
- Win32_PrinterDriver.FilePath
- Win32_PrinterDriver.HelpFile
- Win32_PrinterDriver.InfName
- Win32_PrinterDriver.InstallDate
- Win32_PrinterDriver.MonitorName
- Win32_PrinterDriver.Name
- Win32_PrinterDriver.OEMUrl
- Win32_PrinterDriver.Started
- Win32_PrinterDriver.StartMode
- Win32_PrinterDriver.Status
- Win32_PrinterDriver.SupportedPlatform
- Win32_PrinterDriver.SystemCreationClassName
- Win32_PrinterDriver.SystemName
- Win32_PrinterDriver.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 615d6561e12f67edee34e0de84dade12f250e0f0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826416"
---
# <a name="win32_printerdriver-class"></a><span data-ttu-id="0b0f7-103">\_Classe Win32 PrinterDriver</span><span class="sxs-lookup"><span data-stu-id="0b0f7-103">Win32\_PrinterDriver class</span></span>

<span data-ttu-id="0b0f7-104">A [classe WMI](../wmisdk/retrieving-a-class.md) **\_ PrinterDriver do Win32** representa os drivers para uma instância de [**\_ impressora Win32**](win32-printer.md) .</span><span class="sxs-lookup"><span data-stu-id="0b0f7-104">The **Win32\_PrinterDriver** [WMI class](../wmisdk/retrieving-a-class.md) represents the drivers for a [**Win32\_Printer**](win32-printer.md) instance.</span></span>

<span data-ttu-id="0b0f7-105">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as propriedades herdadas, mas exclui métodos.</span><span class="sxs-lookup"><span data-stu-id="0b0f7-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties, but excludes methods.</span></span> <span data-ttu-id="0b0f7-106">Para obter informações de referência sobre métodos, consulte a tabela de métodos neste tópico.</span><span class="sxs-lookup"><span data-stu-id="0b0f7-106">For reference information about methods, see the table of methods in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b0f7-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0b0f7-107">Syntax</span></span>

``` syntax
class Win32_PrinterDriver : CIM_Service
{
  string   Caption;
  string   ConfigFile;
  string   CreationClassName;
  string   DataFile;
  string   DefaultDataType;
  string   DependentFiles[];
  string   Description;
  string   DriverPath;
  string   FilePath;
  string   HelpFile;
  string   InfName;
  datetime InstallDate;
  string   MonitorName;
  string   Name;
  string   OEMUrl;
  boolean  Started;
  string   StartMode;
  string   Status;
  string   SupportedPlatform;
  string   SystemCreationClassName;
  string   SystemName;
  uint16   Version;
};
```

## <a name="members"></a><span data-ttu-id="0b0f7-108">Membros</span><span class="sxs-lookup"><span data-stu-id="0b0f7-108">Members</span></span>

<span data-ttu-id="0b0f7-109">A classe **Win32 \_ PrinterDriver** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="0b0f7-109">The **Win32\_PrinterDriver** class has these types of members:</span></span>

-   [<span data-ttu-id="0b0f7-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="0b0f7-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="0b0f7-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0b0f7-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="0b0f7-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="0b0f7-112">Methods</span></span>

<span data-ttu-id="0b0f7-113">A classe **Win32 \_ PrinterDriver** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="0b0f7-113">The **Win32\_PrinterDriver** class has these methods.</span></span>



| <span data-ttu-id="0b0f7-114">Método</span><span class="sxs-lookup"><span data-stu-id="0b0f7-114">Method</span></span>                                                                           | <span data-ttu-id="0b0f7-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="0b0f7-115">Description</span></span>                              |
|:---------------------------------------------------------------------------------|:-----------------------------------------|
| [<span data-ttu-id="0b0f7-116">**AddPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="0b0f7-116">**AddPrinterDriver**</span></span>](addprinterdriver-method-in-class-win32-printerdriver.md) | <span data-ttu-id="0b0f7-117">Cria um novo driver de impressora.</span><span class="sxs-lookup"><span data-stu-id="0b0f7-117">Creates a new printer driver.</span></span><br/> |
| [<span data-ttu-id="0b0f7-118">**StartService**</span><span class="sxs-lookup"><span data-stu-id="0b0f7-118">**StartService**</span></span>](startservice-method-in-class-win32-printerdriver.md)         | <span data-ttu-id="0b0f7-119">Inicia o serviço de impressão.</span><span class="sxs-lookup"><span data-stu-id="0b0f7-119">Starts print service.</span></span><br/>         |
| [<span data-ttu-id="0b0f7-120">**StopService**</span><span class="sxs-lookup"><span data-stu-id="0b0f7-120">**StopService**</span></span>](stopservice-method-in-class-win32-printerdriver.md)           | <span data-ttu-id="0b0f7-121">Interrompe o serviço de impressão.</span><span class="sxs-lookup"><span data-stu-id="0b0f7-121">Stops print service.</span></span><br/>          |



 

### <a name="properties"></a><span data-ttu-id="0b0f7-122">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0b0f7-122">Properties</span></span>

<span data-ttu-id="0b0f7-123">A classe **Win32 \_ PrinterDriver** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="0b0f7-123">The **Win32\_PrinterDriver** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0b0f7-124">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="0b0f7-124">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b0f7-125">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0b0f7-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b0f7-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0b0f7-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b0f7-127">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="0b0f7-127">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="0b0f7-128">Breve descrição do objeto — uma cadeia de caracteres de uma linha.</span><span class="sxs-lookup"><span data-stu-id="0b0f7-128">Short description of the object—a one-line string.</span></span>

<span data-ttu-id="0b0f7-129">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0b0f7-129">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0b0f7-130">**ConfigFile**</span><span class="sxs-lookup"><span data-stu-id="0b0f7-130">**ConfigFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b0f7-131">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0b0f7-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b0f7-132">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0b0f7-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b0f7-133">Arquivo de configuração para este driver de impressora.</span><span class="sxs-lookup"><span data-stu-id="0b0f7-133">Configuration file for this printer driver.</span></span>

<span data-ttu-id="0b0f7-134">Exemplo: "pscrptui.dll"</span><span class="sxs-lookup"><span data-stu-id="0b0f7-134">Example: "pscrptui.dll"</span></span>

</dd> <dt>

<span data-ttu-id="0b0f7-135">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="0b0f7-135">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b0f7-136">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0b0f7-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b0f7-137">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0b0f7-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b0f7-138">Qualificadores: [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("nome da classe")</span><span class="sxs-lookup"><span data-stu-id="0b0f7-138">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="0b0f7-139">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="0b0f7-139">Name of the class or the subclass used in the creation of an instance.</span></span> <span data-ttu-id="0b0f7-140">Quando usado com as outras propriedades de chave dessa classe, essa propriedade permite que todas as instâncias dessa classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="0b0f7-140">When used with the other key properties of this class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="0b0f7-141">Essa propriedade é herdada [**do \_ serviço CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="0b0f7-141">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="0b0f7-142">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="0b0f7-142">**DataFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b0f7-143">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0b0f7-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b0f7-144">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0b0f7-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b0f7-145">Qualificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) (CIM \_ DataFile. FileName)</span><span class="sxs-lookup"><span data-stu-id="0b0f7-145">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) (CIM\_DataFile.FileName)</span></span>
</dt> </dl>

<span data-ttu-id="0b0f7-146">Arquivo de dados para este driver de impressora.</span><span class="sxs-lookup"><span data-stu-id="0b0f7-146">Data file for this printer driver.</span></span>

<span data-ttu-id="0b0f7-147">Exemplo: "qms810. PPD"</span><span class="sxs-lookup"><span data-stu-id="0b0f7-147">Example: "qms810.ppd"</span></span>

</dd> <dt>

<span data-ttu-id="0b0f7-148">**Defaultdatatype**</span><span class="sxs-lookup"><span data-stu-id="0b0f7-148">**DefaultDataType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b0f7-149">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0b0f7-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b0f7-150">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0b0f7-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b0f7-151">Tipo de dados padrão para este driver de impressora.</span><span class="sxs-lookup"><span data-stu-id="0b0f7-151">Default data type for this printer driver.</span></span>

<span data-ttu-id="0b0f7-152">Exemplo: "EMF"</span><span class="sxs-lookup"><span data-stu-id="0b0f7-152">Example: "EMF"</span></span>

</dd> <dt>

<span data-ttu-id="0b0f7-153">**DependentFiles**</span><span class="sxs-lookup"><span data-stu-id="0b0f7-153">**DependentFiles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b0f7-154">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0b0f7-154">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0b0f7-155">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0b0f7-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b0f7-156">Matriz de arquivos dependentes para este driver de impressora.</span><span class="sxs-lookup"><span data-stu-id="0b0f7-156">Array of dependent files for this printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="0b0f7-157">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="0b0f7-157">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b0f7-158">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0b0f7-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b0f7-159">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0b0f7-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b0f7-160">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="0b0f7-160">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="0b0f7-161">Comentário que descreve o link.</span><span class="sxs-lookup"><span data-stu-id="0b0f7-161">Comment that describes the link.</span></span>

<span data-ttu-id="0b0f7-162">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0b0f7-162">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0b0f7-163">**DriverPath**</span><span class="sxs-lookup"><span data-stu-id="0b0f7-163">**DriverPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b0f7-164">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0b0f7-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b0f7-165">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0b0f7-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b0f7-166">Qualificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) (CIM \_ DataFile. Path)</span><span class="sxs-lookup"><span data-stu-id="0b0f7-166">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) (CIM\_DataFile.Path)</span></span>
</dt> </dl>

<span data-ttu-id="0b0f7-167">Caminho para este driver de impressora.</span><span class="sxs-lookup"><span data-stu-id="0b0f7-167">Path for this printer driver.</span></span>

<span data-ttu-id="0b0f7-168">Exemplo: "C: \\ \\ drivers \\ \\pscript.dll"</span><span class="sxs-lookup"><span data-stu-id="0b0f7-168">Example: "C:\\\\drivers\\\\pscript.dll"</span></span>

</dd> <dt>

<span data-ttu-id="0b0f7-169">**FilePath**</span><span class="sxs-lookup"><span data-stu-id="0b0f7-169">**FilePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b0f7-170">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0b0f7-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b0f7-171">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0b0f7-171">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0b0f7-172">Caminho para o arquivo INF que está sendo usado.</span><span class="sxs-lookup"><span data-stu-id="0b0f7-172">Path to the INF file being used.</span></span>

<span data-ttu-id="0b0f7-173">Exemplo: "c: \\ \\ \\ \\ Driver temporário"</span><span class="sxs-lookup"><span data-stu-id="0b0f7-173">Example: "c:\\\\temp\\\\driver"</span></span>

</dd> <dt>

<span data-ttu-id="0b0f7-174">**HelpFile**</span><span class="sxs-lookup"><span data-stu-id="0b0f7-174">**HelpFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b0f7-175">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0b0f7-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b0f7-176">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0b0f7-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b0f7-177">Arquivo de ajuda para este driver de impressora.</span><span class="sxs-lookup"><span data-stu-id="0b0f7-177">Help file for this printer driver.</span></span>

<span data-ttu-id="0b0f7-178">Exemplo: "pscrptui. hlp"</span><span class="sxs-lookup"><span data-stu-id="0b0f7-178">Example: "pscrptui.hlp"</span></span>

</dd> <dt>

<span data-ttu-id="0b0f7-179">**InfName**</span><span class="sxs-lookup"><span data-stu-id="0b0f7-179">**InfName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b0f7-180">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0b0f7-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b0f7-181">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0b0f7-181">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0b0f7-182">Nome do arquivo INF que está sendo usado.</span><span class="sxs-lookup"><span data-stu-id="0b0f7-182">Name of the INF file being used.</span></span> <span data-ttu-id="0b0f7-183">O padrão é usar um arquivo INF de impressora fornecido pelo sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="0b0f7-183">The default is to use an operating system provided printer INF file.</span></span> <span data-ttu-id="0b0f7-184">Um nome de arquivo diferente será usado se o driver for fornecido diretamente pelo fabricante da impressora e não pelo sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="0b0f7-184">A different file name is used if the driver is provided directly by the manufacturer of the printer and not the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="0b0f7-185">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="0b0f7-185">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b0f7-186">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="0b0f7-186">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0b0f7-187">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0b0f7-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b0f7-188">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="0b0f7-188">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="0b0f7-189">Data e hora em que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="0b0f7-189">Date and time the object is installed.</span></span> <span data-ttu-id="0b0f7-190">Essa propriedade não requer um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="0b0f7-190">This property does not require a value to indicate that the object is installed.</span></span>

<span data-ttu-id="0b0f7-191">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0b0f7-191">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0b0f7-192">**MonitorName**</span><span class="sxs-lookup"><span data-stu-id="0b0f7-192">**MonitorName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b0f7-193">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0b0f7-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b0f7-194">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0b0f7-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b0f7-195">Nome do monitor para este driver de impressora.</span><span class="sxs-lookup"><span data-stu-id="0b0f7-195">Name of the monitor for this printer driver.</span></span>

<span data-ttu-id="0b0f7-196">Exemplo: "Monitor de PJL"</span><span class="sxs-lookup"><span data-stu-id="0b0f7-196">Example: "PJL monitor"</span></span>

</dd> <dt>

<span data-ttu-id="0b0f7-197">**Nome**</span><span class="sxs-lookup"><span data-stu-id="0b0f7-197">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b0f7-198">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0b0f7-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b0f7-199">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0b0f7-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b0f7-200">Qualificadores: [ **chave**](../wmisdk/key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="0b0f7-200">Qualifiers: [**Key**](../wmisdk/key-qualifier.md)</span></span>
</dt> </dl>

<span data-ttu-id="0b0f7-201">Nome do driver para esta impressora.</span><span class="sxs-lookup"><span data-stu-id="0b0f7-201">Driver name for this printer.</span></span> <span data-ttu-id="0b0f7-202">Essa é uma chave composta composta pelos valores de **nome**, **versão** e **SupportedPlatform** .</span><span class="sxs-lookup"><span data-stu-id="0b0f7-202">This is a compound key composed of the **Name**, **Version**, and **SupportedPlatform** values.</span></span>

<span data-ttu-id="0b0f7-203">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) e substitui a definição de **nome** nessa classe.</span><span class="sxs-lookup"><span data-stu-id="0b0f7-203">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) and overrides the **Name** definition in that class.</span></span>

</dd> <dt>

<span data-ttu-id="0b0f7-204">**OEMUrl**</span><span class="sxs-lookup"><span data-stu-id="0b0f7-204">**OEMUrl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b0f7-205">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0b0f7-205">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b0f7-206">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0b0f7-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b0f7-207">Link do World Wide Web (WWW) para o site do fabricante da impressora.</span><span class="sxs-lookup"><span data-stu-id="0b0f7-207">World Wide Web (WWW) link to the printer manufacturer's website.</span></span> <span data-ttu-id="0b0f7-208">Observe que essa propriedade não é populada quando o arquivo Win32. inf é usado e só é aplicável a drivers fornecidos diretamente do fabricante.</span><span class="sxs-lookup"><span data-stu-id="0b0f7-208">Note that this property is not populated when the Win32.inf file is used, and is only applicable for drivers provided directly from the manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="0b0f7-209">**Iniciado**</span><span class="sxs-lookup"><span data-stu-id="0b0f7-209">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b0f7-210">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="0b0f7-210">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0b0f7-211">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0b0f7-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b0f7-212">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("iniciado")</span><span class="sxs-lookup"><span data-stu-id="0b0f7-212">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Started")</span></span>
</dt> </dl>

<span data-ttu-id="0b0f7-213">Se for **true**, o serviço será iniciado.</span><span class="sxs-lookup"><span data-stu-id="0b0f7-213">If **TRUE**, the service is started.</span></span> <span data-ttu-id="0b0f7-214">Se for **false**, o serviço será interrompido.</span><span class="sxs-lookup"><span data-stu-id="0b0f7-214">If **FALSE**, the service is stopped.</span></span>

<span data-ttu-id="0b0f7-215">Essa propriedade é herdada [**do \_ serviço CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="0b0f7-215">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="0b0f7-216">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="0b0f7-216">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b0f7-217">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0b0f7-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b0f7-218">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0b0f7-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b0f7-219">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("modo de início")</span><span class="sxs-lookup"><span data-stu-id="0b0f7-219">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Start Mode")</span></span>
</dt> </dl>

<span data-ttu-id="0b0f7-220">O modo de início do serviço é iniciado automaticamente por um sistema operacional ou iniciado somente quando solicitado.</span><span class="sxs-lookup"><span data-stu-id="0b0f7-220">Start mode of the service is automatically started by an operating system, or only started when requested.</span></span>

<span data-ttu-id="0b0f7-221">Essa propriedade é herdada [**do \_ serviço CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="0b0f7-221">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

<span data-ttu-id="0b0f7-222">O valores possíveis são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="0b0f7-222">The following are possible values:</span></span>

<dl> <dd><span data-ttu-id="0b0f7-223">Automática</span><span class="sxs-lookup"><span data-stu-id="0b0f7-223">"Automatic"</span></span></dd> <dd><span data-ttu-id="0b0f7-224">Manual</span><span class="sxs-lookup"><span data-stu-id="0b0f7-224">"Manual"</span></span></dd> </dl>

<dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="0b0f7-225">**Automático** ("automático")</span><span class="sxs-lookup"><span data-stu-id="0b0f7-225">**Automatic** ("Automatic")</span></span>


</dt> <dd></dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="0b0f7-226">**Manual** ("manual")</span><span class="sxs-lookup"><span data-stu-id="0b0f7-226">**Manual** ("Manual")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0b0f7-227">**Status**</span><span class="sxs-lookup"><span data-stu-id="0b0f7-227">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b0f7-228">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0b0f7-228">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b0f7-229">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0b0f7-229">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b0f7-230">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="0b0f7-230">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="0b0f7-231">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="0b0f7-231">Current status of the object.</span></span> <span data-ttu-id="0b0f7-232">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="0b0f7-232">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="0b0f7-233">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="0b0f7-233">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="0b0f7-234">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="0b0f7-234">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="0b0f7-235">O último, "serviço", pode ser aplicado durante o espelhamento de espelho de um disco, recarregamento de uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="0b0f7-235">The latter, "Service", can apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="0b0f7-236">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="0b0f7-236">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="0b0f7-237">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0b0f7-237">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="0b0f7-238">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="0b0f7-238">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="0b0f7-239">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="0b0f7-239">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="0b0f7-240">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="0b0f7-240">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="0b0f7-241">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="0b0f7-241">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0b0f7-242">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="0b0f7-242">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="0b0f7-243">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="0b0f7-243">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="0b0f7-244">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="0b0f7-244">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="0b0f7-245">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="0b0f7-245">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="0b0f7-246">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="0b0f7-246">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="0b0f7-247">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="0b0f7-247">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="0b0f7-248">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="0b0f7-248">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="0b0f7-249">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="0b0f7-249">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="0b0f7-250">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="0b0f7-250">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0b0f7-251">**SupportedPlatform**</span><span class="sxs-lookup"><span data-stu-id="0b0f7-251">**SupportedPlatform**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b0f7-252">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0b0f7-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b0f7-253">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0b0f7-253">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0b0f7-254">Ambientes operacionais para os quais o driver se destina.</span><span class="sxs-lookup"><span data-stu-id="0b0f7-254">Operating environments that the driver is intended for.</span></span>

<span data-ttu-id="0b0f7-255">Exemplo: "Windows NT x86".</span><span class="sxs-lookup"><span data-stu-id="0b0f7-255">Example: "Windows NT x86".</span></span>

</dd> <dt>

<span data-ttu-id="0b0f7-256">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="0b0f7-256">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b0f7-257">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0b0f7-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b0f7-258">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0b0f7-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b0f7-259">Qualificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" nome da classe do sistema ")</span><span class="sxs-lookup"><span data-stu-id="0b0f7-259">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="0b0f7-260">Nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="0b0f7-260">Scoping system's creation class name.</span></span>

<span data-ttu-id="0b0f7-261">Essa propriedade é herdada [**do \_ serviço CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="0b0f7-261">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="0b0f7-262">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="0b0f7-262">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b0f7-263">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0b0f7-263">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b0f7-264">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0b0f7-264">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b0f7-265">Qualificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" nome do sistema ")</span><span class="sxs-lookup"><span data-stu-id="0b0f7-265">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("System Name")</span></span>
</dt> </dl>

<span data-ttu-id="0b0f7-266">Nome do sistema que hospeda este serviço.</span><span class="sxs-lookup"><span data-stu-id="0b0f7-266">Name of the system that hosts this service.</span></span>

<span data-ttu-id="0b0f7-267">Essa propriedade é herdada [**do \_ serviço CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="0b0f7-267">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="0b0f7-268">**Versão**</span><span class="sxs-lookup"><span data-stu-id="0b0f7-268">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b0f7-269">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0b0f7-269">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0b0f7-270">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0b0f7-270">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0b0f7-271">Versão do sistema operacional para o driver de impressora.</span><span class="sxs-lookup"><span data-stu-id="0b0f7-271">Operating system version for the printer driver.</span></span>

<dt>

<span id="3"></span>

<span data-ttu-id="0b0f7-272"><span id="3"></span>**Beta**</span><span class="sxs-lookup"><span data-stu-id="0b0f7-272"><span id="3"></span>**3**</span></span>


</dt> <dd>

<span data-ttu-id="0b0f7-273">Win2000</span><span class="sxs-lookup"><span data-stu-id="0b0f7-273">Win2k</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0b0f7-274">Comentários</span><span class="sxs-lookup"><span data-stu-id="0b0f7-274">Remarks</span></span>

<span data-ttu-id="0b0f7-275">A classe **Win32 \_ PrinterDriver** é derivada do [**\_ serviço CIM**](cim-service.md) que deriva de [**CIM \_ LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="0b0f7-275">The **Win32\_PrinterDriver** class is derived from [**CIM\_Service**](cim-service.md) which derives from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="0b0f7-276">Os usuários podem desinstalar um driver de impressora excluindo uma instância correspondente dessa classe.</span><span class="sxs-lookup"><span data-stu-id="0b0f7-276">Users can uninstall a printer driver by deleting a corresponding instance of this class.</span></span> <span data-ttu-id="0b0f7-277">Para fazer isso, o processo de chamada deve ter o privilégio **SeLoadDriverPrivilege** definido para excluir uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="0b0f7-277">To do so, the calling process must have the **SeLoadDriverPrivilege** privilege set to delete an instance of this class.</span></span>

## <a name="examples"></a><span data-ttu-id="0b0f7-278">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0b0f7-278">Examples</span></span>

<span data-ttu-id="0b0f7-279">O exemplo do VBScript [gerenciar drivers de impressora e](https://Gallery.TechNet.Microsoft.Com/710bb2ad-9a8d-42cb-b142-cda2c1452548) impressora gerencia drivers de impressora e portas de impressora.</span><span class="sxs-lookup"><span data-stu-id="0b0f7-279">The [Manage Printer and Printer Drivers](https://Gallery.TechNet.Microsoft.Com/710bb2ad-9a8d-42cb-b142-cda2c1452548) VBScript sample manages printer drivers and printer ports.</span></span>

<span data-ttu-id="0b0f7-280">A discussão a seguir [sobre os fóruns do TechNet](https://social.technet.microsoft.com/Forums/scriptcenter/6210fa0b-0c32-4bce-a79c-dfe835922613/create-printers-in-powershell-with-wmi-win32printer-createinstance?forum=ITCG) descreve como criar uma impressora e carregar drivers de um servidor do.</span><span class="sxs-lookup"><span data-stu-id="0b0f7-280">The following [discussion on the TechNet forums](https://social.technet.microsoft.com/Forums/scriptcenter/6210fa0b-0c32-4bce-a79c-dfe835922613/create-printers-in-powershell-with-wmi-win32printer-createinstance?forum=ITCG) describes how to create a printer and upload drivers from a server.</span></span>

<span data-ttu-id="0b0f7-281">O exemplo de VBScript a seguir lista todos os drivers de impressora que foram instalados em um computador.</span><span class="sxs-lookup"><span data-stu-id="0b0f7-281">The following VBScript sample lists all the printer drivers that have been installed on a computer.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
Set colInstalledPrinters =  objWMIService.ExecQuery _ 
    ("Select * from Win32_PrinterDriver") 
 
For each objPrinter in colInstalledPrinters 
    Wscript.Echo "Configuration File: " & objPrinter.ConfigFile 
    Wscript.Echo "Data File: " & objPrinter.DataFile 
    Wscript.Echo "Description: " & objPrinter.Description 
    Wscript.Echo "Driver Path: " & objPrinter.DriverPath 
    Wscript.Echo "File Path: " & objPrinter.FilePath 
    Wscript.Echo "Help File: " & objPrinter.HelpFile 
    Wscript.Echo "INF Name: " & objPrinter.InfName 
    Wscript.Echo "Monitor Name: " & objPrinter.MonitorName 
    Wscript.Echo "Name: " & objPrinter.Name 
    Wscript.Echo "OEM Url: " & objPrinter.OEMUrl 
    Wscript.Echo "Supported Platform: " & objPrinter.SupportedPlatform 
    Wscript.Echo "Version: " & objPrinter.Version 
Next 
```



## <a name="requirements"></a><span data-ttu-id="0b0f7-282">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b0f7-282">Requirements</span></span>



| <span data-ttu-id="0b0f7-283">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b0f7-283">Requirement</span></span> | <span data-ttu-id="0b0f7-284">Valor</span><span class="sxs-lookup"><span data-stu-id="0b0f7-284">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b0f7-285">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0b0f7-285">Minimum supported client</span></span><br/> | <span data-ttu-id="0b0f7-286">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0b0f7-286">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="0b0f7-287">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0b0f7-287">Minimum supported server</span></span><br/> | <span data-ttu-id="0b0f7-288">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0b0f7-288">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="0b0f7-289">Namespace</span><span class="sxs-lookup"><span data-stu-id="0b0f7-289">Namespace</span></span><br/>                | <span data-ttu-id="0b0f7-290">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="0b0f7-290">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="0b0f7-291">MOF</span><span class="sxs-lookup"><span data-stu-id="0b0f7-291">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0b0f7-292"><dt>\_Impressora. mof do Win32</dt></span><span class="sxs-lookup"><span data-stu-id="0b0f7-292"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="0b0f7-293">DLL</span><span class="sxs-lookup"><span data-stu-id="0b0f7-293">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b0f7-294"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b0f7-294"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="0b0f7-295">Confira também</span><span class="sxs-lookup"><span data-stu-id="0b0f7-295">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b0f7-296">**\_Serviço CIM**</span><span class="sxs-lookup"><span data-stu-id="0b0f7-296">**CIM\_Service**</span></span>](./cim-service.md)
</dt> <dt>

[<span data-ttu-id="0b0f7-297">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="0b0f7-297">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
