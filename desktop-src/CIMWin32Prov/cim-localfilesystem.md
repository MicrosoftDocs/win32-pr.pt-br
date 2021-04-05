---
description: A \_ classe CIM LocalFileSystem representa o repositório de arquivos controlado por um sistema de computador por meio de meios locais (por exemplo, acesso direto ao driver de dispositivo).
ms.assetid: eab52a25-ca24-4a69-b030-091603d3582c
ms.tgt_platform: multiple
title: Classe CIM_LocalFileSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LocalFileSystem
- CIM_LocalFileSystem.Caption
- CIM_LocalFileSystem.Description
- CIM_LocalFileSystem.InstallDate
- CIM_LocalFileSystem.Name
- CIM_LocalFileSystem.Status
- CIM_LocalFileSystem.AvailableSpace
- CIM_LocalFileSystem.BlockSize
- CIM_LocalFileSystem.CasePreserved
- CIM_LocalFileSystem.CaseSensitive
- CIM_LocalFileSystem.CodeSet
- CIM_LocalFileSystem.CompressionMethod
- CIM_LocalFileSystem.CreationClassName
- CIM_LocalFileSystem.CSCreationClassName
- CIM_LocalFileSystem.CSName
- CIM_LocalFileSystem.EncryptionMethod
- CIM_LocalFileSystem.FileSystemSize
- CIM_LocalFileSystem.MaxFileNameLength
- CIM_LocalFileSystem.ReadOnly
- CIM_LocalFileSystem.Root
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6a4a45541a651c92b45baba70828ba99c911d59a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826448"
---
# <a name="cim_localfilesystem-class"></a><span data-ttu-id="6db71-103">\_Classe CIM LocalFileSystem</span><span class="sxs-lookup"><span data-stu-id="6db71-103">CIM\_LocalFileSystem class</span></span>

<span data-ttu-id="6db71-104">A classe **CIM \_ LocalFileSystem** representa o repositório de arquivos controlado por um sistema de computador por meio de meios locais (por exemplo, acesso direto ao driver de dispositivo).</span><span class="sxs-lookup"><span data-stu-id="6db71-104">The **CIM\_LocalFileSystem** class represents the file store controlled by a computer system through local means (for example, direct device-driver access).</span></span> <span data-ttu-id="6db71-105">O armazenamento de arquivos pode ser gerenciado diretamente pelo sistema de computador, sem a necessidade de outro computador agir como um servidor de arquivos.</span><span class="sxs-lookup"><span data-stu-id="6db71-105">The file store can be managed directly by the computer system, without the need for another computer to act as a file server.</span></span> <span data-ttu-id="6db71-106">No entanto, para um sistema de arquivos clusterizado, o sistema de arquivos é local e, portanto, é adiado para o cluster.</span><span class="sxs-lookup"><span data-stu-id="6db71-106">For a clustered file system, however, the file system is local and, therefore, defers to the cluster.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6db71-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="6db71-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="6db71-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="6db71-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="6db71-109">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="6db71-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="6db71-110">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="6db71-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6db71-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6db71-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{5B6C820A-E3D0-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_LocalFileSystem : CIM_FileSystem
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

## <a name="members"></a><span data-ttu-id="6db71-112">Membros</span><span class="sxs-lookup"><span data-stu-id="6db71-112">Members</span></span>

<span data-ttu-id="6db71-113">A classe **CIM \_ LocalFileSystem** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="6db71-113">The **CIM\_LocalFileSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="6db71-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6db71-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6db71-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6db71-115">Properties</span></span>

<span data-ttu-id="6db71-116">A classe **CIM \_ LocalFileSystem** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="6db71-116">The **CIM\_LocalFileSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6db71-117">**AvailableSpace**</span><span class="sxs-lookup"><span data-stu-id="6db71-117">**AvailableSpace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6db71-118">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6db71-118">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6db71-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6db71-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6db71-120">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Partição DMTF \| 2,4 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="6db71-120">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="6db71-121">Quantidade de espaço livre, em bytes, para o sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="6db71-121">Amount of free space, in bytes, for the file system.</span></span> <span data-ttu-id="6db71-122">Se for desconhecido, insira 0.</span><span class="sxs-lookup"><span data-stu-id="6db71-122">If unknown, enter 0.</span></span>

<span data-ttu-id="6db71-123">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="6db71-123">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="6db71-124">Essa propriedade é herdada [**do \_ sistema de arquivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="6db71-124">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="6db71-125">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="6db71-125">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6db71-126">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6db71-126">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6db71-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6db71-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6db71-128">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="6db71-128">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="6db71-129">Tamanho do bloco do sistema de arquivos para armazenamento e recuperação de dados.</span><span class="sxs-lookup"><span data-stu-id="6db71-129">Block size of the file system for data storage and retrieval.</span></span>

<span data-ttu-id="6db71-130">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="6db71-130">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="6db71-131">Essa propriedade é herdada [**do \_ sistema de arquivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="6db71-131">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="6db71-132">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="6db71-132">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6db71-133">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6db71-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6db71-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6db71-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6db71-135">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="6db71-135">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="6db71-136">Uma breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="6db71-136">A short textual description of the object.</span></span>

<span data-ttu-id="6db71-137">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6db71-137">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6db71-138">**CasePreserved**</span><span class="sxs-lookup"><span data-stu-id="6db71-138">**CasePreserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6db71-139">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="6db71-139">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6db71-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6db71-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6db71-141">Se **for true**, o caso dos nomes de arquivo será preservado.</span><span class="sxs-lookup"><span data-stu-id="6db71-141">If **TRUE**, the case of file names are preserved.</span></span>

<span data-ttu-id="6db71-142">Essa propriedade é herdada [**do \_ sistema de arquivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="6db71-142">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="6db71-143">**CaseSensitive**</span><span class="sxs-lookup"><span data-stu-id="6db71-143">**CaseSensitive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6db71-144">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="6db71-144">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6db71-145">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6db71-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6db71-146">Se **verdadeiro**, os nomes de arquivo com diferenciação de maiúsculas e minúsculas têm suporte.</span><span class="sxs-lookup"><span data-stu-id="6db71-146">If **TRUE**, case-sensitive file names are supported.</span></span>

<span data-ttu-id="6db71-147">Essa propriedade é herdada [**do \_ sistema de arquivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="6db71-147">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="6db71-148">**Código de**</span><span class="sxs-lookup"><span data-stu-id="6db71-148">**CodeSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6db71-149">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6db71-149">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="6db71-150">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6db71-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6db71-151">Matriz que define os conjuntos de caracteres ou a codificação com suporte no sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="6db71-151">Array that defines the character sets or encoding supported by the file system.</span></span>

<span data-ttu-id="6db71-152">Essa propriedade é herdada [**do \_ sistema de arquivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="6db71-152">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6db71-153">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="6db71-153">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6db71-154">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="6db71-154">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="ASCII"></span><span id="ascii"></span>

<span data-ttu-id="6db71-155">**ASCII** (2)</span><span class="sxs-lookup"><span data-stu-id="6db71-155">**ASCII** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Unicode"></span><span id="unicode"></span><span id="UNICODE"></span>

<span data-ttu-id="6db71-156">**Unicode** (3)</span><span class="sxs-lookup"><span data-stu-id="6db71-156">**Unicode** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO2022"></span><span id="iso2022"></span>

<span data-ttu-id="6db71-157">**ISO2022** (4)</span><span class="sxs-lookup"><span data-stu-id="6db71-157">**ISO2022** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO8859"></span><span id="iso8859"></span>

<span data-ttu-id="6db71-158">**ISO8859** (5)</span><span class="sxs-lookup"><span data-stu-id="6db71-158">**ISO8859** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Extended_UNIX_Code"></span><span id="extended_unix_code"></span><span id="EXTENDED_UNIX_CODE"></span>

<span data-ttu-id="6db71-159">**Código UNIX estendido** (6)</span><span class="sxs-lookup"><span data-stu-id="6db71-159">**Extended UNIX Code** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="UTF-8"></span><span id="utf-8"></span>

<span data-ttu-id="6db71-160">**UTF-8** (7)</span><span class="sxs-lookup"><span data-stu-id="6db71-160">**UTF-8** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="UCS-2"></span><span id="ucs-2"></span>

<span data-ttu-id="6db71-161">**UCS-2** (8)</span><span class="sxs-lookup"><span data-stu-id="6db71-161">**UCS-2** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6db71-162">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="6db71-162">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6db71-163">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6db71-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6db71-164">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6db71-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6db71-165">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Partição DMTF \| 2,7 ")</span><span class="sxs-lookup"><span data-stu-id="6db71-165">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.7")</span></span>
</dt> </dl>

<span data-ttu-id="6db71-166">Cadeia de caracteres de forma livre que indica o algoritmo ou a ferramenta usada para compactar o arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="6db71-166">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="6db71-167">Se o esquema de compactação for desconhecido ou não estiver descrito, use "desconhecido".</span><span class="sxs-lookup"><span data-stu-id="6db71-167">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="6db71-168">Se o arquivo lógico estiver compactado, mas o esquema de compactação for desconhecido ou não estiver descrito, use "compactado".</span><span class="sxs-lookup"><span data-stu-id="6db71-168">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="6db71-169">Se o arquivo lógico não estiver compactado, use "não compactado".</span><span class="sxs-lookup"><span data-stu-id="6db71-169">If the logical file is not compressed, use "Not Compressed".</span></span>

<span data-ttu-id="6db71-170">Essa propriedade é herdada [**do \_ sistema de arquivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="6db71-170">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="6db71-171">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="6db71-171">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6db71-172">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6db71-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6db71-173">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6db71-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6db71-174">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="6db71-174">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="6db71-175">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="6db71-175">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="6db71-176">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="6db71-176">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="6db71-177">Essa propriedade é herdada [**do \_ sistema de arquivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="6db71-177">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="6db71-178">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="6db71-178">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6db71-179">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6db71-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6db71-180">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6db71-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6db71-181">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-computersystem.md).**CreationClassName**")</span><span class="sxs-lookup"><span data-stu-id="6db71-181">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="6db71-182">Nome da classe de criação do sistema do computador de escopo.</span><span class="sxs-lookup"><span data-stu-id="6db71-182">Scoping computer system's creation class name.</span></span>

<span data-ttu-id="6db71-183">Essa propriedade é herdada [**do \_ sistema de arquivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="6db71-183">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="6db71-184">**CSName**</span><span class="sxs-lookup"><span data-stu-id="6db71-184">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6db71-185">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6db71-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6db71-186">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6db71-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6db71-187">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-computersystem.md).**Nome**")</span><span class="sxs-lookup"><span data-stu-id="6db71-187">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="6db71-188">Nome do sistema do computador de escopo.</span><span class="sxs-lookup"><span data-stu-id="6db71-188">Scoping computer system's name.</span></span>

<span data-ttu-id="6db71-189">Essa propriedade é herdada [**do \_ sistema de arquivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="6db71-189">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="6db71-190">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="6db71-190">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6db71-191">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6db71-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6db71-192">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6db71-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6db71-193">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="6db71-193">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="6db71-194">Uma descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="6db71-194">A textual description of the object.</span></span>

<span data-ttu-id="6db71-195">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6db71-195">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6db71-196">**EncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="6db71-196">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6db71-197">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6db71-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6db71-198">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6db71-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6db71-199">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Partição DMTF \| 2,8 ")</span><span class="sxs-lookup"><span data-stu-id="6db71-199">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.8")</span></span>
</dt> </dl>

<span data-ttu-id="6db71-200">Cadeia de caracteres de forma livre que identifica o algoritmo ou a ferramenta usada para criptografar um arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="6db71-200">Free-form string that identifies the algorithm or tool used to encrypt a logical file.</span></span> <span data-ttu-id="6db71-201">Se o esquema de criptografia não for indulged (por motivos de segurança, por exemplo), use "desconhecido".</span><span class="sxs-lookup"><span data-stu-id="6db71-201">If the encryption scheme is not indulged (for security reasons, for example), use "Unknown".</span></span> <span data-ttu-id="6db71-202">Se o arquivo estiver criptografado, mas seu esquema de criptografia for desconhecido ou não for divulgado, use "Encrypted".</span><span class="sxs-lookup"><span data-stu-id="6db71-202">If the file is encrypted, but either its encryption scheme is unknown or not disclosed, use "Encrypted".</span></span> <span data-ttu-id="6db71-203">Se o arquivo lógico não estiver criptografado, use "não criptografado".</span><span class="sxs-lookup"><span data-stu-id="6db71-203">If the logical file is not encrypted, use "Not Encrypted".</span></span>

<span data-ttu-id="6db71-204">Essa propriedade é herdada [**do \_ sistema de arquivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="6db71-204">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="6db71-205">**Filesystemize**</span><span class="sxs-lookup"><span data-stu-id="6db71-205">**FileSystemSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6db71-206">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6db71-206">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6db71-207">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6db71-207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6db71-208">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="6db71-208">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="6db71-209">Tamanho do sistema de arquivos, em bytes.</span><span class="sxs-lookup"><span data-stu-id="6db71-209">Size of the file system, in bytes.</span></span> <span data-ttu-id="6db71-210">Se for desconhecido, insira 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="6db71-210">If unknown, enter 0 (zero).</span></span>

<span data-ttu-id="6db71-211">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="6db71-211">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="6db71-212">Essa propriedade é herdada [**do \_ sistema de arquivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="6db71-212">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="6db71-213">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="6db71-213">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6db71-214">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6db71-214">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6db71-215">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6db71-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6db71-216">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="6db71-216">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="6db71-217">Indica quando o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="6db71-217">Indicates when the object was installed.</span></span> <span data-ttu-id="6db71-218">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="6db71-218">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="6db71-219">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6db71-219">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6db71-220">**MaxFileNameLength**</span><span class="sxs-lookup"><span data-stu-id="6db71-220">**MaxFileNameLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6db71-221">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6db71-221">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6db71-222">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6db71-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6db71-223">Comprimento máximo de um nome de arquivo dentro do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="6db71-223">Maximum length of a file name within the file system.</span></span> <span data-ttu-id="6db71-224">Um valor de 0 (zero) indica que não há nenhum limite para o comprimento do nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="6db71-224">A value of 0 (zero) indicates that there is no limit to the file name length.</span></span>

<span data-ttu-id="6db71-225">Essa propriedade é herdada [**do \_ sistema de arquivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="6db71-225">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="6db71-226">**Nome**</span><span class="sxs-lookup"><span data-stu-id="6db71-226">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6db71-227">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6db71-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6db71-228">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6db71-228">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6db71-229">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="6db71-229">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="6db71-230">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="6db71-230">Label by which the object is known.</span></span> <span data-ttu-id="6db71-231">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="6db71-231">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="6db71-232">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6db71-232">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6db71-233">**ReadOnly (somente-leitura)**</span><span class="sxs-lookup"><span data-stu-id="6db71-233">**ReadOnly**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6db71-234">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="6db71-234">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6db71-235">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6db71-235">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6db71-236">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrFSAccess ")</span><span class="sxs-lookup"><span data-stu-id="6db71-236">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrFSAccess")</span></span>
</dt> </dl>

<span data-ttu-id="6db71-237">Se **for true**, o sistema de arquivos será designado como somente leitura.</span><span class="sxs-lookup"><span data-stu-id="6db71-237">If **TRUE**, the file system is designated as read only.</span></span>

<span data-ttu-id="6db71-238">Essa propriedade é herdada [**do \_ sistema de arquivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="6db71-238">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="6db71-239">**Básica**</span><span class="sxs-lookup"><span data-stu-id="6db71-239">**Root**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6db71-240">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6db71-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6db71-241">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6db71-241">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6db71-242">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrFSMountPoint ")</span><span class="sxs-lookup"><span data-stu-id="6db71-242">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrFSMountPoint")</span></span>
</dt> </dl>

<span data-ttu-id="6db71-243">Nome do caminho ou outras informações que definem a raiz do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="6db71-243">Path name or other information that defines the root of the file system.</span></span>

<span data-ttu-id="6db71-244">Essa propriedade é herdada [**do \_ sistema de arquivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="6db71-244">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="6db71-245">**Status**</span><span class="sxs-lookup"><span data-stu-id="6db71-245">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6db71-246">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6db71-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6db71-247">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6db71-247">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6db71-248">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="6db71-248">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="6db71-249">Cadeia de caracteres que indica o status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="6db71-249">String that indicates the current status of the object.</span></span> <span data-ttu-id="6db71-250">O status operacional e não operacional pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="6db71-250">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="6db71-251">O status operacional pode incluir "OK", "degradado" e "Pred falha".</span><span class="sxs-lookup"><span data-stu-id="6db71-251">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="6db71-252">"Pred Fail" indica que um elemento está funcionando corretamente, mas está prevendo uma falha (por exemplo, uma unidade de disco rígido habilitada para inteligente).</span><span class="sxs-lookup"><span data-stu-id="6db71-252">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="6db71-253">O status não operacional pode incluir "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="6db71-253">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="6db71-254">O "serviço" pode ser aplicado durante o espelhamento de disco – reprateando, recarregando uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="6db71-254">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="6db71-255">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="6db71-255">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="6db71-256">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6db71-256">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="6db71-257">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="6db71-257">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="6db71-258">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="6db71-258">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="6db71-259">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="6db71-259">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="6db71-260">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="6db71-260">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6db71-261">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="6db71-261">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="6db71-262">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="6db71-262">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="6db71-263">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="6db71-263">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="6db71-264">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="6db71-264">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="6db71-265">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="6db71-265">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="6db71-266">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="6db71-266">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="6db71-267">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="6db71-267">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="6db71-268">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="6db71-268">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="6db71-269">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="6db71-269">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="6db71-270"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="6db71-270"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="6db71-271">Comentários</span><span class="sxs-lookup"><span data-stu-id="6db71-271">Remarks</span></span>

<span data-ttu-id="6db71-272">A classe **CIM \_ LocalFileSystem** é derivada do [**sistema de \_ arquivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="6db71-272">The **CIM\_LocalFileSystem** class is derived from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

<span data-ttu-id="6db71-273">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="6db71-273">WMI does not implement this class.</span></span>

<span data-ttu-id="6db71-274">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="6db71-274">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="6db71-275">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="6db71-275">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="6db71-276">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6db71-276">Requirements</span></span>



| <span data-ttu-id="6db71-277">Requisito</span><span class="sxs-lookup"><span data-stu-id="6db71-277">Requirement</span></span> | <span data-ttu-id="6db71-278">Valor</span><span class="sxs-lookup"><span data-stu-id="6db71-278">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6db71-279">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6db71-279">Minimum supported client</span></span><br/> | <span data-ttu-id="6db71-280">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6db71-280">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6db71-281">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6db71-281">Minimum supported server</span></span><br/> | <span data-ttu-id="6db71-282">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6db71-282">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6db71-283">Namespace</span><span class="sxs-lookup"><span data-stu-id="6db71-283">Namespace</span></span><br/>                | <span data-ttu-id="6db71-284">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="6db71-284">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6db71-285">MOF</span><span class="sxs-lookup"><span data-stu-id="6db71-285">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6db71-286"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6db71-286"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6db71-287">DLL</span><span class="sxs-lookup"><span data-stu-id="6db71-287">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6db71-288"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6db71-288"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6db71-289">Confira também</span><span class="sxs-lookup"><span data-stu-id="6db71-289">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6db71-290">**\_Sistema de arquivos CIM**</span><span class="sxs-lookup"><span data-stu-id="6db71-290">**CIM\_FileSystem**</span></span>](cim-filesystem.md)
</dt> </dl>

 

