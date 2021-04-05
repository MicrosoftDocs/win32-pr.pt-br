---
description: A \_ classe FileSystem do CIM representa um arquivo ou conjunto de dados local para um sistema de computador ou montado remotamente de um servidor de arquivos.
ms.assetid: 5a54ab35-b9b6-49e6-96a8-cb2820b054eb
ms.tgt_platform: multiple
title: Classe CIM_FileSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_FileSystem
- CIM_FileSystem.Caption
- CIM_FileSystem.Description
- CIM_FileSystem.InstallDate
- CIM_FileSystem.Name
- CIM_FileSystem.Status
- CIM_FileSystem.AvailableSpace
- CIM_FileSystem.BlockSize
- CIM_FileSystem.CasePreserved
- CIM_FileSystem.CaseSensitive
- CIM_FileSystem.CodeSet
- CIM_FileSystem.CompressionMethod
- CIM_FileSystem.CreationClassName
- CIM_FileSystem.CSCreationClassName
- CIM_FileSystem.CSName
- CIM_FileSystem.EncryptionMethod
- CIM_FileSystem.FileSystemSize
- CIM_FileSystem.MaxFileNameLength
- CIM_FileSystem.ReadOnly
- CIM_FileSystem.Root
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2795e76c686e8f2bb4079aee376dae397b36f510
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826457"
---
# <a name="cim_filesystem-class"></a><span data-ttu-id="5af1b-103">\_Classe FileSystem do CIM</span><span class="sxs-lookup"><span data-stu-id="5af1b-103">CIM\_FileSystem class</span></span>

<span data-ttu-id="5af1b-104">A **classe \_ FileSystem do CIM** representa um arquivo ou conjunto de dados local para um sistema de computador ou montado remotamente de um servidor de arquivos.</span><span class="sxs-lookup"><span data-stu-id="5af1b-104">The **CIM\_FileSystem** class represents a file or data set local to a computer system or remotely mounted from a file server.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5af1b-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="5af1b-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="5af1b-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="5af1b-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="5af1b-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="5af1b-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="5af1b-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="5af1b-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5af1b-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5af1b-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{4DA18760-E3D0-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_FileSystem : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  uint64   AvailableSpace;
  uint64   BlockSize;
  boolean  CasePreserved;
  boolean  CaseSensitive;
  uint16   CodeSet[];
  string   CompressionMethod;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSName;
  string   EncryptionMethod;
  uint64   FileSystemSize;
  uint32   MaxFileNameLength;
  boolean  ReadOnly;
  string   Root;
};
```

## <a name="members"></a><span data-ttu-id="5af1b-110">Membros</span><span class="sxs-lookup"><span data-stu-id="5af1b-110">Members</span></span>

<span data-ttu-id="5af1b-111">A **classe \_ FileSystem do CIM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="5af1b-111">The **CIM\_FileSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="5af1b-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5af1b-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5af1b-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5af1b-113">Properties</span></span>

<span data-ttu-id="5af1b-114">A **classe \_ FileSystem do CIM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="5af1b-114">The **CIM\_FileSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5af1b-115">**AvailableSpace**</span><span class="sxs-lookup"><span data-stu-id="5af1b-115">**AvailableSpace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5af1b-116">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5af1b-116">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5af1b-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5af1b-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5af1b-118">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Partição DMTF \| 2,4 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="5af1b-118">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="5af1b-119">Quantidade de espaço livre, em bytes, para o sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="5af1b-119">Amount of free space, in bytes, for the file system.</span></span> <span data-ttu-id="5af1b-120">Se for desconhecido, insira 0.</span><span class="sxs-lookup"><span data-stu-id="5af1b-120">If unknown, enter 0.</span></span>

<span data-ttu-id="5af1b-121">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="5af1b-121">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="5af1b-122">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="5af1b-122">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5af1b-123">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5af1b-123">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5af1b-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5af1b-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5af1b-125">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="5af1b-125">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="5af1b-126">Tamanho do bloco do sistema de arquivos para armazenamento e recuperação de dados.</span><span class="sxs-lookup"><span data-stu-id="5af1b-126">Block size of the file system for data storage and retrieval.</span></span>

<span data-ttu-id="5af1b-127">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="5af1b-127">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="5af1b-128">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="5af1b-128">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5af1b-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5af1b-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5af1b-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5af1b-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5af1b-131">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="5af1b-131">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="5af1b-132">Uma breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="5af1b-132">A short textual description of the object.</span></span>

<span data-ttu-id="5af1b-133">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5af1b-133">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5af1b-134">**CasePreserved**</span><span class="sxs-lookup"><span data-stu-id="5af1b-134">**CasePreserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5af1b-135">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="5af1b-135">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5af1b-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5af1b-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5af1b-137">Se **for true**, o caso dos nomes de arquivo será preservado.</span><span class="sxs-lookup"><span data-stu-id="5af1b-137">If **TRUE**, the case of file names are preserved.</span></span>

</dd> <dt>

<span data-ttu-id="5af1b-138">**CaseSensitive**</span><span class="sxs-lookup"><span data-stu-id="5af1b-138">**CaseSensitive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5af1b-139">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="5af1b-139">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5af1b-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5af1b-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5af1b-141">Se **verdadeiro**, os nomes de arquivo com diferenciação de maiúsculas e minúsculas têm suporte.</span><span class="sxs-lookup"><span data-stu-id="5af1b-141">If **TRUE**, case-sensitive file names are supported.</span></span>

</dd> <dt>

<span data-ttu-id="5af1b-142">**Código de**</span><span class="sxs-lookup"><span data-stu-id="5af1b-142">**CodeSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5af1b-143">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5af1b-143">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="5af1b-144">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5af1b-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5af1b-145">Matriz que define os conjuntos de caracteres ou a codificação com suporte no sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="5af1b-145">Array that defines the character sets or encoding supported by the file system.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5af1b-146">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="5af1b-146">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5af1b-147">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="5af1b-147">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="ASCII"></span><span id="ascii"></span>

<span data-ttu-id="5af1b-148">**ASCII** (2)</span><span class="sxs-lookup"><span data-stu-id="5af1b-148">**ASCII** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Unicode"></span><span id="unicode"></span><span id="UNICODE"></span>

<span data-ttu-id="5af1b-149">**Unicode** (3)</span><span class="sxs-lookup"><span data-stu-id="5af1b-149">**Unicode** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO2022"></span><span id="iso2022"></span>

<span data-ttu-id="5af1b-150">**ISO2022** (4)</span><span class="sxs-lookup"><span data-stu-id="5af1b-150">**ISO2022** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO8859"></span><span id="iso8859"></span>

<span data-ttu-id="5af1b-151">**ISO8859** (5)</span><span class="sxs-lookup"><span data-stu-id="5af1b-151">**ISO8859** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Extended_UNIX_Code"></span><span id="extended_unix_code"></span><span id="EXTENDED_UNIX_CODE"></span>

<span data-ttu-id="5af1b-152">**Código UNIX estendido** (6)</span><span class="sxs-lookup"><span data-stu-id="5af1b-152">**Extended UNIX Code** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="UTF-8"></span><span id="utf-8"></span>

<span data-ttu-id="5af1b-153">**UTF-8** (7)</span><span class="sxs-lookup"><span data-stu-id="5af1b-153">**UTF-8** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="UCS-2"></span><span id="ucs-2"></span>

<span data-ttu-id="5af1b-154">**UCS-2** (8)</span><span class="sxs-lookup"><span data-stu-id="5af1b-154">**UCS-2** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5af1b-155">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="5af1b-155">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5af1b-156">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5af1b-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5af1b-157">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5af1b-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5af1b-158">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Partição DMTF \| 2,7 ")</span><span class="sxs-lookup"><span data-stu-id="5af1b-158">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.7")</span></span>
</dt> </dl>

<span data-ttu-id="5af1b-159">Cadeia de caracteres de forma livre que indica o algoritmo ou a ferramenta usada para compactar o arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="5af1b-159">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="5af1b-160">Se o esquema de compactação for desconhecido ou não estiver descrito, use "desconhecido".</span><span class="sxs-lookup"><span data-stu-id="5af1b-160">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="5af1b-161">Se o arquivo lógico estiver compactado, mas o esquema de compactação for desconhecido ou não estiver descrito, use "compactado".</span><span class="sxs-lookup"><span data-stu-id="5af1b-161">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="5af1b-162">Se o arquivo lógico não estiver compactado, use "não compactado".</span><span class="sxs-lookup"><span data-stu-id="5af1b-162">If the logical file is not compressed, use "Not Compressed".</span></span>

</dd> <dt>

<span data-ttu-id="5af1b-163">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="5af1b-163">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5af1b-164">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5af1b-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5af1b-165">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5af1b-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5af1b-166">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="5af1b-166">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="5af1b-167">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="5af1b-167">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="5af1b-168">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="5af1b-168">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="5af1b-169">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="5af1b-169">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5af1b-170">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5af1b-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5af1b-171">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5af1b-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5af1b-172">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-computersystem.md).**CreationClassName**")</span><span class="sxs-lookup"><span data-stu-id="5af1b-172">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="5af1b-173">Nome da classe de criação do sistema do computador de escopo.</span><span class="sxs-lookup"><span data-stu-id="5af1b-173">Scoping computer system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="5af1b-174">**CSName**</span><span class="sxs-lookup"><span data-stu-id="5af1b-174">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5af1b-175">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5af1b-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5af1b-176">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5af1b-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5af1b-177">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-computersystem.md).**Nome**")</span><span class="sxs-lookup"><span data-stu-id="5af1b-177">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="5af1b-178">Nome do sistema do computador de escopo.</span><span class="sxs-lookup"><span data-stu-id="5af1b-178">Scoping computer system's name.</span></span>

</dd> <dt>

<span data-ttu-id="5af1b-179">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="5af1b-179">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5af1b-180">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5af1b-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5af1b-181">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5af1b-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5af1b-182">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="5af1b-182">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="5af1b-183">Uma descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="5af1b-183">A textual description of the object.</span></span>

<span data-ttu-id="5af1b-184">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5af1b-184">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5af1b-185">**EncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="5af1b-185">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5af1b-186">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5af1b-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5af1b-187">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5af1b-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5af1b-188">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Partição DMTF \| 2,8 ")</span><span class="sxs-lookup"><span data-stu-id="5af1b-188">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.8")</span></span>
</dt> </dl>

<span data-ttu-id="5af1b-189">Cadeia de caracteres de forma livre que identifica o algoritmo ou a ferramenta usada para criptografar um arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="5af1b-189">Free-form string that identifies the algorithm or tool used to encrypt a logical file.</span></span> <span data-ttu-id="5af1b-190">Se o esquema de criptografia não for indulged (por motivos de segurança, por exemplo), use "desconhecido".</span><span class="sxs-lookup"><span data-stu-id="5af1b-190">If the encryption scheme is not indulged (for security reasons, for example), use "Unknown".</span></span> <span data-ttu-id="5af1b-191">Se o arquivo estiver criptografado, mas seu esquema de criptografia for desconhecido ou não for divulgado, use "Encrypted".</span><span class="sxs-lookup"><span data-stu-id="5af1b-191">If the file is encrypted, but either its encryption scheme is unknown or not disclosed, use "Encrypted".</span></span> <span data-ttu-id="5af1b-192">Se o arquivo lógico não estiver criptografado, use "não criptografado".</span><span class="sxs-lookup"><span data-stu-id="5af1b-192">If the logical file is not encrypted, use "Not Encrypted".</span></span>

</dd> <dt>

<span data-ttu-id="5af1b-193">**Filesystemize**</span><span class="sxs-lookup"><span data-stu-id="5af1b-193">**FileSystemSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5af1b-194">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5af1b-194">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5af1b-195">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5af1b-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5af1b-196">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="5af1b-196">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="5af1b-197">Tamanho do sistema de arquivos, em bytes.</span><span class="sxs-lookup"><span data-stu-id="5af1b-197">Size of the file system, in bytes.</span></span> <span data-ttu-id="5af1b-198">Se for desconhecido, insira 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="5af1b-198">If unknown, enter 0 (zero).</span></span>

<span data-ttu-id="5af1b-199">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="5af1b-199">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="5af1b-200">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="5af1b-200">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5af1b-201">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5af1b-201">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5af1b-202">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5af1b-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5af1b-203">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="5af1b-203">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="5af1b-204">Indica quando o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="5af1b-204">Indicates when the object was installed.</span></span> <span data-ttu-id="5af1b-205">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="5af1b-205">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="5af1b-206">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5af1b-206">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5af1b-207">**MaxFileNameLength**</span><span class="sxs-lookup"><span data-stu-id="5af1b-207">**MaxFileNameLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5af1b-208">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5af1b-208">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5af1b-209">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5af1b-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5af1b-210">Comprimento máximo de um nome de arquivo dentro do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="5af1b-210">Maximum length of a file name within the file system.</span></span> <span data-ttu-id="5af1b-211">Um valor de 0 (zero) indica que não há nenhum limite para o comprimento do nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="5af1b-211">A value of 0 (zero) indicates that there is no limit to the file name length.</span></span>

</dd> <dt>

<span data-ttu-id="5af1b-212">**Nome**</span><span class="sxs-lookup"><span data-stu-id="5af1b-212">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5af1b-213">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5af1b-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5af1b-214">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5af1b-214">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5af1b-215">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="5af1b-215">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="5af1b-216">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="5af1b-216">Label by which the object is known.</span></span> <span data-ttu-id="5af1b-217">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="5af1b-217">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="5af1b-218">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5af1b-218">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5af1b-219">**ReadOnly (somente-leitura)**</span><span class="sxs-lookup"><span data-stu-id="5af1b-219">**ReadOnly**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5af1b-220">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="5af1b-220">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5af1b-221">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5af1b-221">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5af1b-222">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrFSAccess ")</span><span class="sxs-lookup"><span data-stu-id="5af1b-222">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrFSAccess")</span></span>
</dt> </dl>

<span data-ttu-id="5af1b-223">Se **for true**, o sistema de arquivos será designado como somente leitura.</span><span class="sxs-lookup"><span data-stu-id="5af1b-223">If **TRUE**, the file system is designated as read only.</span></span>

</dd> <dt>

<span data-ttu-id="5af1b-224">**Básica**</span><span class="sxs-lookup"><span data-stu-id="5af1b-224">**Root**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5af1b-225">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5af1b-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5af1b-226">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5af1b-226">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5af1b-227">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrFSMountPoint ")</span><span class="sxs-lookup"><span data-stu-id="5af1b-227">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrFSMountPoint")</span></span>
</dt> </dl>

<span data-ttu-id="5af1b-228">Nome do caminho ou outras informações que definem a raiz do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="5af1b-228">Path name or other information that defines the root of the file system.</span></span>

</dd> <dt>

<span data-ttu-id="5af1b-229">**Status**</span><span class="sxs-lookup"><span data-stu-id="5af1b-229">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5af1b-230">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5af1b-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5af1b-231">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5af1b-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5af1b-232">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="5af1b-232">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="5af1b-233">Cadeia de caracteres que indica o status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="5af1b-233">String that indicates the current status of the object.</span></span> <span data-ttu-id="5af1b-234">O status operacional e não operacional pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="5af1b-234">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="5af1b-235">O status operacional pode incluir "OK", "degradado" e "Pred falha".</span><span class="sxs-lookup"><span data-stu-id="5af1b-235">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="5af1b-236">"Pred Fail" indica que um elemento está funcionando corretamente, mas está prevendo uma falha (por exemplo, uma unidade de disco rígido habilitada para inteligente).</span><span class="sxs-lookup"><span data-stu-id="5af1b-236">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="5af1b-237">O status não operacional pode incluir "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="5af1b-237">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="5af1b-238">O "serviço" pode ser aplicado durante o espelhamento de disco – reprateando, recarregando uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="5af1b-238">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="5af1b-239">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="5af1b-239">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="5af1b-240">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5af1b-240">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="5af1b-241">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="5af1b-241">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="5af1b-242">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="5af1b-242">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="5af1b-243">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="5af1b-243">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="5af1b-244">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="5af1b-244">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5af1b-245">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="5af1b-245">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="5af1b-246">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="5af1b-246">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="5af1b-247">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="5af1b-247">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="5af1b-248">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="5af1b-248">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="5af1b-249">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="5af1b-249">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="5af1b-250">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="5af1b-250">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="5af1b-251">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="5af1b-251">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="5af1b-252">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="5af1b-252">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="5af1b-253">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="5af1b-253">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="5af1b-254"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="5af1b-254"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="5af1b-255">Comentários</span><span class="sxs-lookup"><span data-stu-id="5af1b-255">Remarks</span></span>

<span data-ttu-id="5af1b-256">A **classe \_ FileSystem do CIM** é derivada de [**CIM \_ LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="5af1b-256">The **CIM\_FileSystem** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="5af1b-257">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="5af1b-257">WMI does not implement this class.</span></span>

<span data-ttu-id="5af1b-258">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="5af1b-258">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="5af1b-259">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="5af1b-259">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="5af1b-260">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5af1b-260">Requirements</span></span>



| <span data-ttu-id="5af1b-261">Requisito</span><span class="sxs-lookup"><span data-stu-id="5af1b-261">Requirement</span></span> | <span data-ttu-id="5af1b-262">Valor</span><span class="sxs-lookup"><span data-stu-id="5af1b-262">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5af1b-263">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5af1b-263">Minimum supported client</span></span><br/> | <span data-ttu-id="5af1b-264">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5af1b-264">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5af1b-265">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5af1b-265">Minimum supported server</span></span><br/> | <span data-ttu-id="5af1b-266">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5af1b-266">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5af1b-267">Namespace</span><span class="sxs-lookup"><span data-stu-id="5af1b-267">Namespace</span></span><br/>                | <span data-ttu-id="5af1b-268">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="5af1b-268">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5af1b-269">MOF</span><span class="sxs-lookup"><span data-stu-id="5af1b-269">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5af1b-270"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5af1b-270"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5af1b-271">DLL</span><span class="sxs-lookup"><span data-stu-id="5af1b-271">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5af1b-272"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5af1b-272"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5af1b-273">Confira também</span><span class="sxs-lookup"><span data-stu-id="5af1b-273">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5af1b-274">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="5af1b-274">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

