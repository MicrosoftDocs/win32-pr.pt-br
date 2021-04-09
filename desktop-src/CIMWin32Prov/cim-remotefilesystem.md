---
description: A \_ classe CIM RemoteFileSystem representa um sistema de arquivos remoto que é acessado por meio de um serviço relacionado à rede. Nesse caso, o armazenamento de arquivos é hospedado por um computador, que atua como um servidor de arquivos.
ms.assetid: 932970a8-0ab3-45d8-912d-c4ba7cf433b5
ms.tgt_platform: multiple
title: Classe CIM_RemoteFileSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RemoteFileSystem
- CIM_RemoteFileSystem.AvailableSpace
- CIM_RemoteFileSystem.BlockSize
- CIM_RemoteFileSystem.Caption
- CIM_RemoteFileSystem.CasePreserved
- CIM_RemoteFileSystem.CaseSensitive
- CIM_RemoteFileSystem.CodeSet
- CIM_RemoteFileSystem.CompressionMethod
- CIM_RemoteFileSystem.CreationClassName
- CIM_RemoteFileSystem.CSCreationClassName
- CIM_RemoteFileSystem.CSName
- CIM_RemoteFileSystem.Description
- CIM_RemoteFileSystem.EncryptionMethod
- CIM_RemoteFileSystem.FileSystemSize
- CIM_RemoteFileSystem.InstallDate
- CIM_RemoteFileSystem.MaxFileNameLength
- CIM_RemoteFileSystem.Name
- CIM_RemoteFileSystem.ReadOnly
- CIM_RemoteFileSystem.Root
- CIM_RemoteFileSystem.Status
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7c29e0212ba55b37abd734fb149d118ccc693908
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104088983"
---
# <a name="cim_remotefilesystem-class"></a><span data-ttu-id="f7c9a-104">\_Classe CIM RemoteFileSystem</span><span class="sxs-lookup"><span data-stu-id="f7c9a-104">CIM\_RemoteFileSystem class</span></span>

<span data-ttu-id="f7c9a-105">A classe **CIM \_ RemoteFileSystem** representa um sistema de arquivos remoto que é acessado por meio de um serviço relacionado à rede.</span><span class="sxs-lookup"><span data-stu-id="f7c9a-105">The **CIM\_RemoteFileSystem** class represents a remote file system that is accessed by way of a network-related service.</span></span> <span data-ttu-id="f7c9a-106">Nesse caso, o armazenamento de arquivos é hospedado por um computador, que atua como um servidor de arquivos.</span><span class="sxs-lookup"><span data-stu-id="f7c9a-106">In this case, the file store is hosted by a computer, which acts as a file server.</span></span> <span data-ttu-id="f7c9a-107">Por exemplo, o armazenamento de arquivos para um sistema de arquivos NFS normalmente não está na mídia controlada localmente de um sistema de computador, nem é acessado diretamente por meio de um driver de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f7c9a-107">For example, the file store for an NFS file system is typically not on a computer system's locally controlled media, nor is it directly accessed through a device driver.</span></span> <span data-ttu-id="f7c9a-108">As subclasses do **CIM \_ RemoteFileSystem** contêm informações de configuração do lado do cliente relacionadas ao acesso do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="f7c9a-108">Subclasses of **CIM\_RemoteFileSystem** contain client-side configuration information related to the access of the file system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f7c9a-109">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="f7c9a-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="f7c9a-110">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="f7c9a-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="f7c9a-111">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="f7c9a-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="f7c9a-112">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="f7c9a-112">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7c9a-113">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f7c9a-113">Syntax</span></span>

``` syntax
[Abstract, UUID("{75BCF4F9-DB46-11D2-B4C8-80080C7B6371}"), AMENDMENT]
class CIM_RemoteFileSystem : CIM_FileSystem
{
  uint64   AvailableSpace;
  uint64   BlockSize;
  string   Caption;
  boolean  CasePreserved;
  boolean  CaseSensitive;
  uint16   CodeSet[];
  string   CompressionMethod;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSName;
  string   Description;
  string   EncryptionMethod;
  uint64   FileSystemSize;
  datetime InstallDate;
  uint32   MaxFileNameLength;
  string   Name;
  boolean  ReadOnly;
  string   Root;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="f7c9a-114">Membros</span><span class="sxs-lookup"><span data-stu-id="f7c9a-114">Members</span></span>

<span data-ttu-id="f7c9a-115">A classe **CIM \_ RemoteFileSystem** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="f7c9a-115">The **CIM\_RemoteFileSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="f7c9a-116">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f7c9a-116">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f7c9a-117">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f7c9a-117">Properties</span></span>

<span data-ttu-id="f7c9a-118">A classe **CIM \_ RemoteFileSystem** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="f7c9a-118">The **CIM\_RemoteFileSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f7c9a-119">**AvailableSpace**</span><span class="sxs-lookup"><span data-stu-id="f7c9a-119">**AvailableSpace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7c9a-120">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f7c9a-120">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f7c9a-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f7c9a-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7c9a-122">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Partição DMTF \| 2,4 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="f7c9a-122">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="f7c9a-123">Quantidade de espaço livre para o sistema de arquivos, em bytes.</span><span class="sxs-lookup"><span data-stu-id="f7c9a-123">Amount of free space for the file system, in bytes.</span></span> <span data-ttu-id="f7c9a-124">Se for desconhecido, insira 0.</span><span class="sxs-lookup"><span data-stu-id="f7c9a-124">If unknown, enter 0.</span></span>

<span data-ttu-id="f7c9a-125">Essa propriedade é herdada [**do \_ sistema de arquivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="f7c9a-125">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

<span data-ttu-id="f7c9a-126">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="f7c9a-126">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="f7c9a-127">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="f7c9a-127">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7c9a-128">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f7c9a-128">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f7c9a-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f7c9a-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7c9a-130">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="f7c9a-130">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="f7c9a-131">Tamanho, em bytes, dos blocos que formam a extensão de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="f7c9a-131">Size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="f7c9a-132">Se for desconhecido ou se um conceito de bloco não for válido, (por exemplo, para extensões de agregação, memória ou discos lógicos), insira um 1 (um).</span><span class="sxs-lookup"><span data-stu-id="f7c9a-132">If unknown, or if a block concept is not valid, (for example, for aggregate extents, memory, or logical disks), enter a 1 (one).</span></span>

<span data-ttu-id="f7c9a-133">Essa propriedade é herdada [**do \_ sistema de arquivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="f7c9a-133">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

<span data-ttu-id="f7c9a-134">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="f7c9a-134">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="f7c9a-135">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="f7c9a-135">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7c9a-136">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f7c9a-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7c9a-137">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f7c9a-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7c9a-138">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="f7c9a-138">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="f7c9a-139">Descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="f7c9a-139">Textual description of the object.</span></span>

<span data-ttu-id="f7c9a-140">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f7c9a-140">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f7c9a-141">**CasePreserved**</span><span class="sxs-lookup"><span data-stu-id="f7c9a-141">**CasePreserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7c9a-142">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="f7c9a-142">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f7c9a-143">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f7c9a-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f7c9a-144">Se **for true**, o caso dos nomes de arquivo será preservado.</span><span class="sxs-lookup"><span data-stu-id="f7c9a-144">If **TRUE**, the case of file names are preserved.</span></span>

<span data-ttu-id="f7c9a-145">Essa propriedade é herdada [**do \_ sistema de arquivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="f7c9a-145">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="f7c9a-146">**CaseSensitive**</span><span class="sxs-lookup"><span data-stu-id="f7c9a-146">**CaseSensitive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7c9a-147">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="f7c9a-147">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f7c9a-148">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f7c9a-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f7c9a-149">Se **verdadeiro**, os nomes de arquivo com diferenciação de maiúsculas e minúsculas têm suporte.</span><span class="sxs-lookup"><span data-stu-id="f7c9a-149">If **TRUE**, case-sensitive file names are supported.</span></span>

<span data-ttu-id="f7c9a-150">Essa propriedade é herdada [**do \_ sistema de arquivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="f7c9a-150">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="f7c9a-151">**Código de**</span><span class="sxs-lookup"><span data-stu-id="f7c9a-151">**CodeSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7c9a-152">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f7c9a-152">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f7c9a-153">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f7c9a-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f7c9a-154">Conjuntos de caracteres ou codificação com suporte no sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="f7c9a-154">Character sets or encoding supported by the file system.</span></span> <span data-ttu-id="f7c9a-155">Essa propriedade é herdada [**do \_ sistema de arquivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="f7c9a-155">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f7c9a-156">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="f7c9a-156">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f7c9a-157">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="f7c9a-157">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="ASCII"></span><span id="ascii"></span>

<span data-ttu-id="f7c9a-158">**ASCII** (2)</span><span class="sxs-lookup"><span data-stu-id="f7c9a-158">**ASCII** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Unicode"></span><span id="unicode"></span><span id="UNICODE"></span>

<span data-ttu-id="f7c9a-159">**Unicode** (3)</span><span class="sxs-lookup"><span data-stu-id="f7c9a-159">**Unicode** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO2022"></span><span id="iso2022"></span>

<span data-ttu-id="f7c9a-160">**ISO2022** (4)</span><span class="sxs-lookup"><span data-stu-id="f7c9a-160">**ISO2022** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO8859"></span><span id="iso8859"></span>

<span data-ttu-id="f7c9a-161">**ISO8859** (5)</span><span class="sxs-lookup"><span data-stu-id="f7c9a-161">**ISO8859** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Extended_UNIX_Code"></span><span id="extended_unix_code"></span><span id="EXTENDED_UNIX_CODE"></span>

<span data-ttu-id="f7c9a-162">**Código UNIX estendido** (6)</span><span class="sxs-lookup"><span data-stu-id="f7c9a-162">**Extended UNIX Code** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="UTF-8"></span><span id="utf-8"></span>

<span data-ttu-id="f7c9a-163">**UTF-8** (7)</span><span class="sxs-lookup"><span data-stu-id="f7c9a-163">**UTF-8** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="UCS-2"></span><span id="ucs-2"></span>

<span data-ttu-id="f7c9a-164">**UCS-2** (8)</span><span class="sxs-lookup"><span data-stu-id="f7c9a-164">**UCS-2** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f7c9a-165">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="f7c9a-165">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7c9a-166">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f7c9a-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7c9a-167">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f7c9a-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7c9a-168">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Partição DMTF \| 2,7 ")</span><span class="sxs-lookup"><span data-stu-id="f7c9a-168">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.7")</span></span>
</dt> </dl>

<span data-ttu-id="f7c9a-169">Cadeia de caracteres de forma livre que indica o algoritmo ou a ferramenta usada para compactar o arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="f7c9a-169">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="f7c9a-170">Se o esquema de compactação for desconhecido ou não estiver descrito, use "desconhecido".</span><span class="sxs-lookup"><span data-stu-id="f7c9a-170">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="f7c9a-171">Se o arquivo lógico estiver compactado, mas o esquema de compactação for desconhecido ou não estiver descrito, use "compactado".</span><span class="sxs-lookup"><span data-stu-id="f7c9a-171">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="f7c9a-172">Se o arquivo lógico não estiver compactado, use "não compactado".</span><span class="sxs-lookup"><span data-stu-id="f7c9a-172">If the logical file is not compressed, use "Not Compressed".</span></span>

<span data-ttu-id="f7c9a-173">Essa propriedade é herdada [**do \_ sistema de arquivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="f7c9a-173">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="f7c9a-174">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="f7c9a-174">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7c9a-175">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f7c9a-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7c9a-176">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f7c9a-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7c9a-177">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="f7c9a-177">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="f7c9a-178">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="f7c9a-178">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="f7c9a-179">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="f7c9a-179">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="f7c9a-180">Essa propriedade é herdada [**do \_ sistema de arquivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="f7c9a-180">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="f7c9a-181">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="f7c9a-181">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7c9a-182">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f7c9a-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7c9a-183">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f7c9a-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7c9a-184">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-computersystem.md).**CreationClassName**")</span><span class="sxs-lookup"><span data-stu-id="f7c9a-184">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="f7c9a-185">Nome da classe de criação do sistema do computador de escopo.</span><span class="sxs-lookup"><span data-stu-id="f7c9a-185">Scoping computer system's creation class name.</span></span>

<span data-ttu-id="f7c9a-186">Essa propriedade é herdada [**do \_ sistema de arquivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="f7c9a-186">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="f7c9a-187">**CSName**</span><span class="sxs-lookup"><span data-stu-id="f7c9a-187">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7c9a-188">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f7c9a-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7c9a-189">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f7c9a-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7c9a-190">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-computersystem.md).**Nome**")</span><span class="sxs-lookup"><span data-stu-id="f7c9a-190">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="f7c9a-191">Nome do sistema do computador de escopo.</span><span class="sxs-lookup"><span data-stu-id="f7c9a-191">Scoping computer system's name.</span></span>

<span data-ttu-id="f7c9a-192">Essa propriedade é herdada [**do \_ sistema de arquivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="f7c9a-192">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="f7c9a-193">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="f7c9a-193">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7c9a-194">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f7c9a-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7c9a-195">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f7c9a-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7c9a-196">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="f7c9a-196">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="f7c9a-197">Descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="f7c9a-197">Textual description of the object.</span></span>

<span data-ttu-id="f7c9a-198">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f7c9a-198">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f7c9a-199">**EncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="f7c9a-199">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7c9a-200">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f7c9a-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7c9a-201">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f7c9a-201">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7c9a-202">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Partição DMTF \| 2,8 ")</span><span class="sxs-lookup"><span data-stu-id="f7c9a-202">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.8")</span></span>
</dt> </dl>

<span data-ttu-id="f7c9a-203">Cadeia de caracteres de forma livre que identifica o algoritmo ou a ferramenta usada para criptografar um arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="f7c9a-203">Free-form string that identifies the algorithm or tool used to encrypt a logical file.</span></span> <span data-ttu-id="f7c9a-204">Se o esquema de criptografia não for indulged (por motivos de segurança, por exemplo), use "desconhecido".</span><span class="sxs-lookup"><span data-stu-id="f7c9a-204">If the encryption scheme is not indulged (for security reasons, for example), use "Unknown".</span></span> <span data-ttu-id="f7c9a-205">Se o arquivo estiver criptografado, mas seu esquema de criptografia for desconhecido ou não for divulgado, use "Encrypted".</span><span class="sxs-lookup"><span data-stu-id="f7c9a-205">If the file is encrypted, but either its encryption scheme is unknown or not disclosed, use "Encrypted".</span></span> <span data-ttu-id="f7c9a-206">Se o arquivo lógico não estiver criptografado, use "não criptografado".</span><span class="sxs-lookup"><span data-stu-id="f7c9a-206">If the logical file is not encrypted, use "Not Encrypted".</span></span> <span data-ttu-id="f7c9a-207">Essa propriedade é herdada [**do \_ sistema de arquivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="f7c9a-207">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="f7c9a-208">**Filesystemize**</span><span class="sxs-lookup"><span data-stu-id="f7c9a-208">**FileSystemSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7c9a-209">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f7c9a-209">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f7c9a-210">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f7c9a-210">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7c9a-211">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="f7c9a-211">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="f7c9a-212">Tamanho total do sistema de arquivos, em bytes.</span><span class="sxs-lookup"><span data-stu-id="f7c9a-212">Total size of the file system, in bytes.</span></span> <span data-ttu-id="f7c9a-213">Se for desconhecido, insira 0.</span><span class="sxs-lookup"><span data-stu-id="f7c9a-213">If unknown, enter 0.</span></span>

<span data-ttu-id="f7c9a-214">Essa propriedade é herdada [**do \_ sistema de arquivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="f7c9a-214">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

<span data-ttu-id="f7c9a-215">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="f7c9a-215">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="f7c9a-216">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="f7c9a-216">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7c9a-217">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f7c9a-217">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f7c9a-218">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f7c9a-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7c9a-219">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="f7c9a-219">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="f7c9a-220">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="f7c9a-220">Date and time the object was installed.</span></span> <span data-ttu-id="f7c9a-221">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="f7c9a-221">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="f7c9a-222">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f7c9a-222">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f7c9a-223">**MaxFileNameLength**</span><span class="sxs-lookup"><span data-stu-id="f7c9a-223">**MaxFileNameLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7c9a-224">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f7c9a-224">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f7c9a-225">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f7c9a-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f7c9a-226">Comprimento máximo de um nome de arquivo dentro do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="f7c9a-226">Maximum length of a file name within the file system.</span></span> <span data-ttu-id="f7c9a-227">Um valor de 0 indica que o comprimento do nome do arquivo é ilimitado.</span><span class="sxs-lookup"><span data-stu-id="f7c9a-227">A value of 0 indicates that file name length is unlimited.</span></span>

<span data-ttu-id="f7c9a-228">Essa propriedade é herdada [**do \_ sistema de arquivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="f7c9a-228">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="f7c9a-229">**Nome**</span><span class="sxs-lookup"><span data-stu-id="f7c9a-229">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7c9a-230">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f7c9a-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7c9a-231">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f7c9a-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7c9a-232">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="f7c9a-232">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="f7c9a-233">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="f7c9a-233">Label by which the object is known.</span></span> <span data-ttu-id="f7c9a-234">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="f7c9a-234">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="f7c9a-235">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f7c9a-235">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f7c9a-236">**ReadOnly (somente-leitura)**</span><span class="sxs-lookup"><span data-stu-id="f7c9a-236">**ReadOnly**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7c9a-237">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="f7c9a-237">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f7c9a-238">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f7c9a-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7c9a-239">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrFSAccess ")</span><span class="sxs-lookup"><span data-stu-id="f7c9a-239">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrFSAccess")</span></span>
</dt> </dl>

<span data-ttu-id="f7c9a-240">Se **for true**, o sistema de arquivos será designado como somente leitura.</span><span class="sxs-lookup"><span data-stu-id="f7c9a-240">If **TRUE**, the file system is designated as read-only.</span></span>

<span data-ttu-id="f7c9a-241">Essa propriedade é herdada [**do \_ sistema de arquivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="f7c9a-241">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="f7c9a-242">**Básica**</span><span class="sxs-lookup"><span data-stu-id="f7c9a-242">**Root**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7c9a-243">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f7c9a-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7c9a-244">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f7c9a-244">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7c9a-245">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrFSMountPoint ")</span><span class="sxs-lookup"><span data-stu-id="f7c9a-245">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrFSMountPoint")</span></span>
</dt> </dl>

<span data-ttu-id="f7c9a-246">Nome do caminho ou outras informações que definem a raiz do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="f7c9a-246">Path name or other information that defines the root of the file system.</span></span>

<span data-ttu-id="f7c9a-247">Essa propriedade é herdada [**do \_ sistema de arquivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="f7c9a-247">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="f7c9a-248">**Status**</span><span class="sxs-lookup"><span data-stu-id="f7c9a-248">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7c9a-249">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f7c9a-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7c9a-250">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f7c9a-250">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7c9a-251">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="f7c9a-251">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="f7c9a-252">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="f7c9a-252">Current status of the object.</span></span>

<span data-ttu-id="f7c9a-253">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f7c9a-253">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="f7c9a-254">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="f7c9a-254">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="f7c9a-255">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="f7c9a-255">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="f7c9a-256">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="f7c9a-256">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="f7c9a-257">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="f7c9a-257">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f7c9a-258">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="f7c9a-258">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="f7c9a-259">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="f7c9a-259">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="f7c9a-260">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="f7c9a-260">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="f7c9a-261">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="f7c9a-261">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="f7c9a-262">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="f7c9a-262">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="f7c9a-263">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="f7c9a-263">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="f7c9a-264">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="f7c9a-264">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="f7c9a-265">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="f7c9a-265">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="f7c9a-266">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="f7c9a-266">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="f7c9a-267"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="f7c9a-267"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="f7c9a-268">Comentários</span><span class="sxs-lookup"><span data-stu-id="f7c9a-268">Remarks</span></span>

<span data-ttu-id="f7c9a-269">A classe **CIM \_ RemoteFileSystem** é derivada do [**sistema de \_ arquivos CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="f7c9a-269">The **CIM\_RemoteFileSystem** class is derived from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

<span data-ttu-id="f7c9a-270">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="f7c9a-270">WMI does not implement this class.</span></span>

<span data-ttu-id="f7c9a-271">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="f7c9a-271">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="f7c9a-272">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="f7c9a-272">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7c9a-273">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f7c9a-273">Requirements</span></span>



| <span data-ttu-id="f7c9a-274">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7c9a-274">Requirement</span></span> | <span data-ttu-id="f7c9a-275">Valor</span><span class="sxs-lookup"><span data-stu-id="f7c9a-275">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f7c9a-276">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f7c9a-276">Minimum supported client</span></span><br/> | <span data-ttu-id="f7c9a-277">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f7c9a-277">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f7c9a-278">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f7c9a-278">Minimum supported server</span></span><br/> | <span data-ttu-id="f7c9a-279">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f7c9a-279">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f7c9a-280">Namespace</span><span class="sxs-lookup"><span data-stu-id="f7c9a-280">Namespace</span></span><br/>                | <span data-ttu-id="f7c9a-281">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="f7c9a-281">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f7c9a-282">MOF</span><span class="sxs-lookup"><span data-stu-id="f7c9a-282">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f7c9a-283"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f7c9a-283"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f7c9a-284">DLL</span><span class="sxs-lookup"><span data-stu-id="f7c9a-284">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f7c9a-285"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7c9a-285"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7c9a-286">Confira também</span><span class="sxs-lookup"><span data-stu-id="f7c9a-286">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7c9a-287">**\_Sistema de arquivos CIM**</span><span class="sxs-lookup"><span data-stu-id="f7c9a-287">**CIM\_FileSystem**</span></span>](cim-filesystem.md)
</dt> </dl>

 

