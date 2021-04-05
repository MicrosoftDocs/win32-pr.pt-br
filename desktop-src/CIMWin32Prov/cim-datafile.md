---
description: A classe de DataFile do CIM \_ representa uma coleção nomeada de dados ou código executável. Somente as instâncias de arquivos em discos fixos locais serão retornadas.
ms.assetid: e90e1216-e943-4f3a-9f6c-8a0b4568a11f
ms.tgt_platform: multiple
title: Classe CIM_DataFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile
- CIM_DataFile.Caption
- CIM_DataFile.Description
- CIM_DataFile.InstallDate
- CIM_DataFile.Status
- CIM_DataFile.AccessMask
- CIM_DataFile.Archive
- CIM_DataFile.Compressed
- CIM_DataFile.CompressionMethod
- CIM_DataFile.CreationClassName
- CIM_DataFile.CreationDate
- CIM_DataFile.CSCreationClassName
- CIM_DataFile.CSName
- CIM_DataFile.Drive
- CIM_DataFile.EightDotThreeFileName
- CIM_DataFile.Encrypted
- CIM_DataFile.EncryptionMethod
- CIM_DataFile.Name
- CIM_DataFile.Extension
- CIM_DataFile.FileName
- CIM_DataFile.FileSize
- CIM_DataFile.FileType
- CIM_DataFile.FSCreationClassName
- CIM_DataFile.FSName
- CIM_DataFile.Hidden
- CIM_DataFile.InUseCount
- CIM_DataFile.LastAccessed
- CIM_DataFile.LastModified
- CIM_DataFile.Path
- CIM_DataFile.Readable
- CIM_DataFile.System
- CIM_DataFile.Writeable
- CIM_DataFile.Manufacturer
- CIM_DataFile.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0badba05eafa5cba06e48b8494ca893936af360e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826466"
---
# <a name="cim_datafile-class"></a><span data-ttu-id="6163d-104">Classe de DataFile do CIM \_</span><span class="sxs-lookup"><span data-stu-id="6163d-104">CIM\_DataFile class</span></span>

<span data-ttu-id="6163d-105">A classe de **\_ DataFile do CIM** representa uma coleção nomeada de dados ou código executável.</span><span class="sxs-lookup"><span data-stu-id="6163d-105">The **CIM\_DataFile** class represents a named collection of data or executable code.</span></span> <span data-ttu-id="6163d-106">Somente as instâncias de arquivos em discos fixos locais serão retornadas.</span><span class="sxs-lookup"><span data-stu-id="6163d-106">Only instances of files on local fixed disks will be returned.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6163d-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="6163d-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="6163d-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="6163d-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="6163d-109">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="6163d-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="6163d-110">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="6163d-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6163d-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6163d-111">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C55A-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("All Files (CIM)"), AMENDMENT]
class CIM_DataFile : CIM_LogicalFile
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  uint32   AccessMask;
  boolean  Archive;
  boolean  Compressed;
  string   CompressionMethod;
  string   CreationClassName;
  datetime CreationDate;
  string   CSCreationClassName;
  string   CSName;
  string   Drive;
  string   EightDotThreeFileName;
  boolean  Encrypted;
  string   EncryptionMethod;
  string   Name;
  string   Extension;
  string   FileName;
  uint64   FileSize;
  string   FileType;
  string   FSCreationClassName;
  string   FSName;
  boolean  Hidden;
  uint64   InUseCount;
  datetime LastAccessed;
  datetime LastModified;
  string   Path;
  boolean  Readable;
  boolean  System;
  boolean  Writeable;
  string   Manufacturer;
  string   Version;
};
```

## <a name="members"></a><span data-ttu-id="6163d-112">Membros</span><span class="sxs-lookup"><span data-stu-id="6163d-112">Members</span></span>

<span data-ttu-id="6163d-113">A classe de **\_ DataFile do CIM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="6163d-113">The **CIM\_DataFile** class has these types of members:</span></span>

-   [<span data-ttu-id="6163d-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="6163d-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="6163d-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6163d-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="6163d-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="6163d-116">Methods</span></span>

<span data-ttu-id="6163d-117">A classe de **\_ DataFile de arquivo CIM** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="6163d-117">The **CIM\_DataFile** class has these methods.</span></span>



| <span data-ttu-id="6163d-118">Método</span><span class="sxs-lookup"><span data-stu-id="6163d-118">Method</span></span>                                                                                          | <span data-ttu-id="6163d-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="6163d-119">Description</span></span>                                                                                                                                          |
|:------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6163d-120">**ChangeSecurityPermissions**</span><span class="sxs-lookup"><span data-stu-id="6163d-120">**ChangeSecurityPermissions**</span></span>](changesecuritypermissions-method-in-class-cim-datafile.md)     | <span data-ttu-id="6163d-121">Altera as permissões de segurança para o arquivo lógico especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="6163d-121">Changes the security permissions for the logical file specified in the object path.</span></span> <span data-ttu-id="6163d-122">Implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="6163d-122">Implemented by WMI.</span></span><br/>                                   |
| [<span data-ttu-id="6163d-123">**ChangeSecurityPermissionsEx**</span><span class="sxs-lookup"><span data-stu-id="6163d-123">**ChangeSecurityPermissionsEx**</span></span>](changesecuritypermissionsex-method-in-class-cim-datafile.md) | <span data-ttu-id="6163d-124">Altera as permissões de segurança para o arquivo lógico especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="6163d-124">Changes the security permissions for the logical file specified in the object path.</span></span> <span data-ttu-id="6163d-125">Implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="6163d-125">Implemented by WMI.</span></span><br/>                                   |
| [<span data-ttu-id="6163d-126">**Compactar**</span><span class="sxs-lookup"><span data-stu-id="6163d-126">**Compress**</span></span>](compress-method-in-class-cim-datafile.md)                                       | <span data-ttu-id="6163d-127">Usa a compactação NTFS para compactar o arquivo lógico (ou diretório) especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="6163d-127">Uses NTFS compression to compress the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="6163d-128">Implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="6163d-128">Implemented by WMI.</span></span><br/>                       |
| [<span data-ttu-id="6163d-129">**CompressEx**</span><span class="sxs-lookup"><span data-stu-id="6163d-129">**CompressEx**</span></span>](compressex-method-in-class-cim-datafile.md)                                   | <span data-ttu-id="6163d-130">Compacta o arquivo lógico (ou diretório) especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="6163d-130">Compresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="6163d-131">Implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="6163d-131">Implemented by WMI.</span></span><br/>                                              |
| [<span data-ttu-id="6163d-132">**CopiarObjeto**</span><span class="sxs-lookup"><span data-stu-id="6163d-132">**Copy**</span></span>](copy-method-in-class-cim-datafile.md)                                               | <span data-ttu-id="6163d-133">Copia o arquivo lógico (ou diretório) especificado no caminho do objeto para o local especificado pelo parâmetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="6163d-133">Copies the logical file (or directory) specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="6163d-134">Implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="6163d-134">Implemented by WMI.</span></span><br/> |
| [<span data-ttu-id="6163d-135">**CopyEx**</span><span class="sxs-lookup"><span data-stu-id="6163d-135">**CopyEx**</span></span>](copyex-method-in-class-cim-datafile.md)                                           | <span data-ttu-id="6163d-136">Copia o arquivo lógico (ou diretório) especificado no caminho do objeto para o local especificado pelo parâmetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="6163d-136">Copies the logical file (or directory) specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="6163d-137">Implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="6163d-137">Implemented by WMI.</span></span><br/> |
| [<span data-ttu-id="6163d-138">**Apagar**</span><span class="sxs-lookup"><span data-stu-id="6163d-138">**Delete**</span></span>](delete-method-in-class-cim-datafile.md)                                           | <span data-ttu-id="6163d-139">Exclui o arquivo lógico (ou diretório) especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="6163d-139">Deletes the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="6163d-140">Implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="6163d-140">Implemented by WMI.</span></span><br/>                                                 |
| [<span data-ttu-id="6163d-141">**DeleteEx**</span><span class="sxs-lookup"><span data-stu-id="6163d-141">**DeleteEx**</span></span>](deleteex-method-in-class-cim-datafile.md)                                       | <span data-ttu-id="6163d-142">Exclui o arquivo lógico (ou diretório) especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="6163d-142">Deletes the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="6163d-143">Implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="6163d-143">Implemented by WMI.</span></span><br/>                                                 |
| [<span data-ttu-id="6163d-144">**GetEffectivePermission**</span><span class="sxs-lookup"><span data-stu-id="6163d-144">**GetEffectivePermission**</span></span>](geteffectivepermission-method-in-class-cim-datafile.md)           | <span data-ttu-id="6163d-145">Determina se o chamador tem as permissões agregadas especificadas pelo argumento de **permissão** .</span><span class="sxs-lookup"><span data-stu-id="6163d-145">Determines whether the caller has the aggregated permissions specified by the **Permission** argument.</span></span> <span data-ttu-id="6163d-146">Implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="6163d-146">Implemented by WMI.</span></span><br/>                |
| [<span data-ttu-id="6163d-147">**Renomear**</span><span class="sxs-lookup"><span data-stu-id="6163d-147">**Rename**</span></span>](rename-method-in-class-cim-datafile.md)                                           | <span data-ttu-id="6163d-148">Renomeia o arquivo lógico (ou diretório) especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="6163d-148">Renames the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="6163d-149">Implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="6163d-149">Implemented by WMI.</span></span><br/>                                                 |
| [<span data-ttu-id="6163d-150">**TakeOwnerShip**</span><span class="sxs-lookup"><span data-stu-id="6163d-150">**TakeOwnerShip**</span></span>](takeownership-method-in-class-cim-datafile.md)                             | <span data-ttu-id="6163d-151">Obtém a propriedade do arquivo lógico especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="6163d-151">Obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="6163d-152">Implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="6163d-152">Implemented by WMI.</span></span><br/>                                                   |
| [<span data-ttu-id="6163d-153">**TakeOwnerShipEx**</span><span class="sxs-lookup"><span data-stu-id="6163d-153">**TakeOwnerShipEx**</span></span>](takeownershipex-method-in-class-cim-datafile.md)                         | <span data-ttu-id="6163d-154">Obtém a propriedade do arquivo lógico especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="6163d-154">Obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="6163d-155">Implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="6163d-155">Implemented by WMI.</span></span><br/>                                                   |
| [<span data-ttu-id="6163d-156">**Descompactar**</span><span class="sxs-lookup"><span data-stu-id="6163d-156">**Uncompress**</span></span>](uncompress-method-in-class-cim-datafile.md)                                   | <span data-ttu-id="6163d-157">Descompacta o arquivo lógico (ou diretório) especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="6163d-157">Uncompresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="6163d-158">Implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="6163d-158">Implemented by WMI.</span></span><br/>                                            |
| [<span data-ttu-id="6163d-159">**UncompressEx**</span><span class="sxs-lookup"><span data-stu-id="6163d-159">**UncompressEx**</span></span>](uncompressex-method-in-class-cim-datafile.md)                               | <span data-ttu-id="6163d-160">Descompacta o arquivo lógico (ou diretório) especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="6163d-160">Uncompresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="6163d-161">Implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="6163d-161">Implemented by WMI.</span></span><br/>                                            |



 

### <a name="properties"></a><span data-ttu-id="6163d-162">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6163d-162">Properties</span></span>

<span data-ttu-id="6163d-163">A classe de **\_ DataFile de arquivo CIM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="6163d-163">The **CIM\_DataFile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6163d-164">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="6163d-164">**AccessMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6163d-165">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6163d-165">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6163d-166">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6163d-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6163d-167">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("direitos de acesso")</span><span class="sxs-lookup"><span data-stu-id="6163d-167">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Access Rights")</span></span>
</dt> </dl>

<span data-ttu-id="6163d-168">Bitmask que representa os direitos de acesso necessários para acessar ou executar operações específicas no arquivo.</span><span class="sxs-lookup"><span data-stu-id="6163d-168">Bitmask that represents the access rights required to access or perform specific operations on the file.</span></span> <span data-ttu-id="6163d-169">Para valores de bit, consulte [**constantes de direitos de acesso de arquivo e diretório**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants).</span><span class="sxs-lookup"><span data-stu-id="6163d-169">For bit values, see [**File and Directory Access Rights Constants**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants).</span></span>

> [!Note]  
> <span data-ttu-id="6163d-170">Em volumes FAT, o valor de **\_ acesso completo** é retornado, o que indica que nenhuma segurança foi definida no objeto.</span><span class="sxs-lookup"><span data-stu-id="6163d-170">On FAT volumes, the **FULL\_ACCESS** value is returned instead, which indicates no security has been set on the object.</span></span>

 

<span data-ttu-id="6163d-171">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6163d-171">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="6163d-172">Do **arquivo \_ LER \_ os dados (arquivo) ou \_ \_ diretório de lista de arquivos (diretório)** (1)</span><span class="sxs-lookup"><span data-stu-id="6163d-172">**FILE\_READ\_DATA (file) or FILE\_LIST\_DIRECTORY (directory)** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="6163d-173">Do **arquivo \_ GRAVAR \_ dados (arquivo) ou arquivo \_ Adicionar \_ arquivo (diretório)** (2)</span><span class="sxs-lookup"><span data-stu-id="6163d-173">**FILE\_WRITE\_DATA (file) or FILE\_ADD\_FILE (directory)** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="6163d-174">Do **arquivo \_ ACRESCENTAR \_ dados (arquivo) ou arquivo \_ Adicionar \_ subdiretório (diretório)** (4)</span><span class="sxs-lookup"><span data-stu-id="6163d-174">**FILE\_APPEND\_DATA (file) or FILE\_ADD\_SUBDIRECTORY (directory)** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="6163d-175">Do **arquivo \_ LER \_ ea** (8)</span><span class="sxs-lookup"><span data-stu-id="6163d-175">**FILE\_READ\_EA** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="6163d-176">Do **arquivo \_ GRAVAR \_ ea** (16)</span><span class="sxs-lookup"><span data-stu-id="6163d-176">**FILE\_WRITE\_EA** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

<span data-ttu-id="6163d-177">Do **arquivo \_ EXECUTAR (arquivo) ou \_ atravessamento de arquivo (diretório)** (32)</span><span class="sxs-lookup"><span data-stu-id="6163d-177">**FILE\_EXECUTE (file) or FILE\_TRAVERSE (directory)** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="6163d-178">Do **arquivo \_ EXCLUIR \_ filho (diretório)** (64)</span><span class="sxs-lookup"><span data-stu-id="6163d-178">**FILE\_DELETE\_CHILD (directory)** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="6163d-179">Do **arquivo \_ \_Atributos de leitura** (128)</span><span class="sxs-lookup"><span data-stu-id="6163d-179">**FILE\_READ\_ATTRIBUTES** (128)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="6163d-180">Do **arquivo \_ \_Atributos de gravação** (256)</span><span class="sxs-lookup"><span data-stu-id="6163d-180">**FILE\_WRITE\_ATTRIBUTES** (256)</span></span>


</dt> <dd></dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="6163d-181">**Excluir** (65536)</span><span class="sxs-lookup"><span data-stu-id="6163d-181">**DELETE** (65536)</span></span>


</dt> <dd></dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="6163d-182">**Ler \_ CONTROLE** (131072)</span><span class="sxs-lookup"><span data-stu-id="6163d-182">**READ\_CONTROL** (131072)</span></span>


</dt> <dd></dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="6163d-183">**Gravar \_ DAC** (262144)</span><span class="sxs-lookup"><span data-stu-id="6163d-183">**WRITE\_DAC** (262144)</span></span>


</dt> <dd></dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="6163d-184">**Gravar \_ PROPRIETÁRIO** (524288)</span><span class="sxs-lookup"><span data-stu-id="6163d-184">**WRITE\_OWNER** (524288)</span></span>


</dt> <dd></dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="6163d-185">**Sincronizar** (1048576)</span><span class="sxs-lookup"><span data-stu-id="6163d-185">**SYNCHRONIZE** (1048576)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6163d-186">**Arquivar**</span><span class="sxs-lookup"><span data-stu-id="6163d-186">**Archive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6163d-187">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="6163d-187">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6163d-188">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6163d-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6163d-189">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("deve ser arquivado")</span><span class="sxs-lookup"><span data-stu-id="6163d-189">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Should Be Archived")</span></span>
</dt> </dl>

<span data-ttu-id="6163d-190">Se **for true**, o arquivo deverá ser arquivado.</span><span class="sxs-lookup"><span data-stu-id="6163d-190">If **True**, the file should be archived.</span></span>

<span data-ttu-id="6163d-191">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6163d-191">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6163d-192">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="6163d-192">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6163d-193">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6163d-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6163d-194">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6163d-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6163d-195">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="6163d-195">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="6163d-196">Uma breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="6163d-196">A short textual description of the object.</span></span>

<span data-ttu-id="6163d-197">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6163d-197">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6163d-198">**Compactado**</span><span class="sxs-lookup"><span data-stu-id="6163d-198">**Compressed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6163d-199">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="6163d-199">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6163d-200">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6163d-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6163d-201">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("compactado")</span><span class="sxs-lookup"><span data-stu-id="6163d-201">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compressed")</span></span>
</dt> </dl>

<span data-ttu-id="6163d-202">Se **for true**, o arquivo será compactado.</span><span class="sxs-lookup"><span data-stu-id="6163d-202">If **True**, the file is compressed.</span></span>

<span data-ttu-id="6163d-203">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6163d-203">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6163d-204">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="6163d-204">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6163d-205">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6163d-205">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6163d-206">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6163d-206">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6163d-207">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("método de compactação")</span><span class="sxs-lookup"><span data-stu-id="6163d-207">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compression Method")</span></span>
</dt> </dl>

<span data-ttu-id="6163d-208">Cadeia de caracteres de forma livre que indica o algoritmo ou a ferramenta usada para compactar o arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="6163d-208">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="6163d-209">Se o esquema de compactação for desconhecido ou não estiver descrito, use "desconhecido".</span><span class="sxs-lookup"><span data-stu-id="6163d-209">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="6163d-210">Se o arquivo lógico estiver compactado, mas o esquema de compactação for desconhecido ou não estiver descrito, use "compactado".</span><span class="sxs-lookup"><span data-stu-id="6163d-210">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="6163d-211">Se o arquivo lógico não estiver compactado, use "não compactado".</span><span class="sxs-lookup"><span data-stu-id="6163d-211">If the logical file is not compressed, use "Not Compressed".</span></span>

<span data-ttu-id="6163d-212">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6163d-212">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6163d-213">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="6163d-213">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6163d-214">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6163d-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6163d-215">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6163d-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6163d-216">Qualificadores: [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nome da classe")</span><span class="sxs-lookup"><span data-stu-id="6163d-216">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="6163d-217">Nome da classe.</span><span class="sxs-lookup"><span data-stu-id="6163d-217">Name of the class.</span></span>

<span data-ttu-id="6163d-218">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6163d-218">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6163d-219">**CreationDate**</span><span class="sxs-lookup"><span data-stu-id="6163d-219">**CreationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6163d-220">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6163d-220">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6163d-221">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6163d-221">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6163d-222">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("data de criação")</span><span class="sxs-lookup"><span data-stu-id="6163d-222">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Creation Date")</span></span>
</dt> </dl>

<span data-ttu-id="6163d-223">Data e hora da criação do arquivo.</span><span class="sxs-lookup"><span data-stu-id="6163d-223">Date and time of the file's creation.</span></span>

<span data-ttu-id="6163d-224">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6163d-224">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6163d-225">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="6163d-225">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6163d-226">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6163d-226">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6163d-227">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6163d-227">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6163d-228">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema de arquivos CIM**](cim-filesystem.md).**CSCreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome da classe do sistema de computador ")</span><span class="sxs-lookup"><span data-stu-id="6163d-228">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSCreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="6163d-229">Classe do sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="6163d-229">Class of the computer system.</span></span>

<span data-ttu-id="6163d-230">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6163d-230">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6163d-231">**CSName**</span><span class="sxs-lookup"><span data-stu-id="6163d-231">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6163d-232">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6163d-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6163d-233">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6163d-233">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6163d-234">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema de arquivos CIM**](cim-filesystem.md).**CSName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome do sistema de computador ")</span><span class="sxs-lookup"><span data-stu-id="6163d-234">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Name")</span></span>
</dt> </dl>

<span data-ttu-id="6163d-235">Nome do sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="6163d-235">Name of the computer system.</span></span>

<span data-ttu-id="6163d-236">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6163d-236">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6163d-237">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="6163d-237">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6163d-238">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6163d-238">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6163d-239">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6163d-239">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6163d-240">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="6163d-240">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="6163d-241">Uma descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="6163d-241">A textual description of the object.</span></span>

<span data-ttu-id="6163d-242">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6163d-242">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6163d-243">**Unidade**</span><span class="sxs-lookup"><span data-stu-id="6163d-243">**Drive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6163d-244">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6163d-244">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6163d-245">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6163d-245">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6163d-246">Qualificadores: [**fixo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("drive")</span><span class="sxs-lookup"><span data-stu-id="6163d-246">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Drive")</span></span>
</dt> </dl>

<span data-ttu-id="6163d-247">Letra da unidade (incluindo os dois-pontos que segue a letra da unidade) do arquivo.</span><span class="sxs-lookup"><span data-stu-id="6163d-247">Drive letter (including the colon that follows the drive letter) of the file.</span></span>

<span data-ttu-id="6163d-248">Exemplo: "c:"</span><span class="sxs-lookup"><span data-stu-id="6163d-248">Example: "c:"</span></span>

<span data-ttu-id="6163d-249">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6163d-249">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6163d-250">**EightDotThreeFileName**</span><span class="sxs-lookup"><span data-stu-id="6163d-250">**EightDotThreeFileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6163d-251">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6163d-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6163d-252">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6163d-252">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6163d-253">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("oito pontos três nome de arquivo")</span><span class="sxs-lookup"><span data-stu-id="6163d-253">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Eight Dot Three File Name")</span></span>
</dt> </dl>

<span data-ttu-id="6163d-254">Nome de arquivo compatível com o DOS.</span><span class="sxs-lookup"><span data-stu-id="6163d-254">DOS-compatible file name.</span></span>

<span data-ttu-id="6163d-255">Exemplo: "c: \\ progra ~ 1"</span><span class="sxs-lookup"><span data-stu-id="6163d-255">Example: "c:\\progra~1"</span></span>

<span data-ttu-id="6163d-256">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6163d-256">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6163d-257">**Criptografado**</span><span class="sxs-lookup"><span data-stu-id="6163d-257">**Encrypted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6163d-258">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="6163d-258">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6163d-259">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6163d-259">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6163d-260">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encrypted")</span><span class="sxs-lookup"><span data-stu-id="6163d-260">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encrypted")</span></span>
</dt> </dl>

<span data-ttu-id="6163d-261">Se **for true**, o arquivo será criptografado.</span><span class="sxs-lookup"><span data-stu-id="6163d-261">If **True**, the file is encrypted.</span></span>

<span data-ttu-id="6163d-262">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6163d-262">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6163d-263">**EncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="6163d-263">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6163d-264">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6163d-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6163d-265">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6163d-265">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6163d-266">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("método de criptografia")</span><span class="sxs-lookup"><span data-stu-id="6163d-266">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encryption Method")</span></span>
</dt> </dl>

<span data-ttu-id="6163d-267">Cadeia de caracteres de forma livre que identifica o algoritmo ou a ferramenta usada para criptografar um arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="6163d-267">Free-form string that identifies the algorithm or tool used to encrypt a logical file.</span></span> <span data-ttu-id="6163d-268">Se o esquema de criptografia não for indulged (por motivos de segurança, por exemplo), use "desconhecido".</span><span class="sxs-lookup"><span data-stu-id="6163d-268">If the encryption scheme is not indulged (for security reasons, for example), use "Unknown".</span></span> <span data-ttu-id="6163d-269">Se o arquivo estiver criptografado, mas seu esquema de criptografia for desconhecido ou não for divulgado, use "Encrypted".</span><span class="sxs-lookup"><span data-stu-id="6163d-269">If the file is encrypted, but either its encryption scheme is unknown or not disclosed, use "Encrypted".</span></span> <span data-ttu-id="6163d-270">Se o arquivo lógico não estiver criptografado, use "não criptografado".</span><span class="sxs-lookup"><span data-stu-id="6163d-270">If the logical file is not encrypted, use "Not Encrypted".</span></span>

<span data-ttu-id="6163d-271">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6163d-271">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6163d-272">**Extensão**</span><span class="sxs-lookup"><span data-stu-id="6163d-272">**Extension**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6163d-273">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6163d-273">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6163d-274">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6163d-274">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6163d-275">Qualificadores: [**fixo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("extensão de arquivo")</span><span class="sxs-lookup"><span data-stu-id="6163d-275">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Extension")</span></span>
</dt> </dl>

<span data-ttu-id="6163d-276">Extensão de nome de arquivo sem o ponto anterior (ponto).</span><span class="sxs-lookup"><span data-stu-id="6163d-276">File name extension without the preceding period (dot).</span></span>

<span data-ttu-id="6163d-277">Exemplo: "txt", "MOF", "mdb"</span><span class="sxs-lookup"><span data-stu-id="6163d-277">Example: "txt", "mof", "mdb"</span></span>

<span data-ttu-id="6163d-278">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6163d-278">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6163d-279">**FileName**</span><span class="sxs-lookup"><span data-stu-id="6163d-279">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6163d-280">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6163d-280">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6163d-281">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6163d-281">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6163d-282">Qualificadores: [**fixo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nome do arquivo")</span><span class="sxs-lookup"><span data-stu-id="6163d-282">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Name")</span></span>
</dt> </dl>

<span data-ttu-id="6163d-283">Nome do arquivo sem a extensão de nome de arquivo.</span><span class="sxs-lookup"><span data-stu-id="6163d-283">File name without the file name extension.</span></span> <span data-ttu-id="6163d-284">Exemplo: "mydatafile"</span><span class="sxs-lookup"><span data-stu-id="6163d-284">Example: "MyDataFile"</span></span>

<span data-ttu-id="6163d-285">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6163d-285">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6163d-286">**Tamanho**</span><span class="sxs-lookup"><span data-stu-id="6163d-286">**FileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6163d-287">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6163d-287">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6163d-288">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6163d-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6163d-289">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("tamanho"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="6163d-289">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Size"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="6163d-290">Tamanho do arquivo, em bytes.</span><span class="sxs-lookup"><span data-stu-id="6163d-290">Size of the file, in bytes.</span></span>

<span data-ttu-id="6163d-291">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="6163d-291">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="6163d-292">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6163d-292">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6163d-293">**Talvez**</span><span class="sxs-lookup"><span data-stu-id="6163d-293">**FileType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6163d-294">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6163d-294">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6163d-295">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6163d-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6163d-296">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("tipo de arquivo")</span><span class="sxs-lookup"><span data-stu-id="6163d-296">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Type")</span></span>
</dt> </dl>

<span data-ttu-id="6163d-297">Descritor que representa o tipo de arquivo indicado pela propriedade de **extensão** .</span><span class="sxs-lookup"><span data-stu-id="6163d-297">Descriptor that represents the file type indicated by the **Extension** property.</span></span>

<span data-ttu-id="6163d-298">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6163d-298">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6163d-299">**FSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="6163d-299">**FSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6163d-300">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6163d-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6163d-301">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6163d-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6163d-302">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema de arquivos CIM**](cim-filesystem.md).**CreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome da classe do sistema de arquivos ")</span><span class="sxs-lookup"><span data-stu-id="6163d-302">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="6163d-303">Classe do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="6163d-303">Class of the file system.</span></span>

<span data-ttu-id="6163d-304">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6163d-304">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6163d-305">**FSName**</span><span class="sxs-lookup"><span data-stu-id="6163d-305">**FSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6163d-306">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6163d-306">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6163d-307">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6163d-307">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6163d-308">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema de arquivos CIM**](cim-filesystem.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome do sistema de arquivos ")</span><span class="sxs-lookup"><span data-stu-id="6163d-308">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Name")</span></span>
</dt> </dl>

<span data-ttu-id="6163d-309">Nome do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="6163d-309">Name of the file system.</span></span>

<span data-ttu-id="6163d-310">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6163d-310">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6163d-311">**Oculto**</span><span class="sxs-lookup"><span data-stu-id="6163d-311">**Hidden**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6163d-312">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="6163d-312">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6163d-313">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6163d-313">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6163d-314">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hidden")</span><span class="sxs-lookup"><span data-stu-id="6163d-314">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hidden")</span></span>
</dt> </dl>

<span data-ttu-id="6163d-315">Se for **true**, o arquivo ficará oculto.</span><span class="sxs-lookup"><span data-stu-id="6163d-315">If **True**, the file is hidden.</span></span>

<span data-ttu-id="6163d-316">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6163d-316">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6163d-317">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="6163d-317">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6163d-318">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6163d-318">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6163d-319">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6163d-319">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6163d-320">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="6163d-320">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="6163d-321">Indica quando o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="6163d-321">Indicates when the object was installed.</span></span> <span data-ttu-id="6163d-322">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="6163d-322">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="6163d-323">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6163d-323">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6163d-324">**InUseCount**</span><span class="sxs-lookup"><span data-stu-id="6163d-324">**InUseCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6163d-325">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6163d-325">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6163d-326">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6163d-326">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6163d-327">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("contagem de abertura de arquivo atual")</span><span class="sxs-lookup"><span data-stu-id="6163d-327">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Current File Open Count")</span></span>
</dt> </dl>

<span data-ttu-id="6163d-328">Número de "aberturas de arquivo" que estão atualmente ativos no arquivo.</span><span class="sxs-lookup"><span data-stu-id="6163d-328">Number of "file opens" that are currently active against the file.</span></span>

<span data-ttu-id="6163d-329">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="6163d-329">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="6163d-330">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6163d-330">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6163d-331">**LastAccessed**</span><span class="sxs-lookup"><span data-stu-id="6163d-331">**LastAccessed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6163d-332">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6163d-332">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6163d-333">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6163d-333">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6163d-334">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("último acesso")</span><span class="sxs-lookup"><span data-stu-id="6163d-334">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Accessed")</span></span>
</dt> </dl>

<span data-ttu-id="6163d-335">Data e hora do último acesso ao arquivo.</span><span class="sxs-lookup"><span data-stu-id="6163d-335">Date and time the file was last accessed.</span></span>

<span data-ttu-id="6163d-336">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6163d-336">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6163d-337">**LastModified**</span><span class="sxs-lookup"><span data-stu-id="6163d-337">**LastModified**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6163d-338">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6163d-338">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6163d-339">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6163d-339">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6163d-340">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("última modificação")</span><span class="sxs-lookup"><span data-stu-id="6163d-340">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Modified")</span></span>
</dt> </dl>

<span data-ttu-id="6163d-341">Data e hora da última modificação do arquivo.</span><span class="sxs-lookup"><span data-stu-id="6163d-341">Date and time the file was last modified.</span></span>

<span data-ttu-id="6163d-342">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6163d-342">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6163d-343">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="6163d-343">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6163d-344">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6163d-344">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6163d-345">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6163d-345">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6163d-346">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("fabricante")</span><span class="sxs-lookup"><span data-stu-id="6163d-346">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Manufacturer")</span></span>
</dt> </dl>

<span data-ttu-id="6163d-347">Cadeia de caracteres do fabricante do recurso de versão (se houver um).</span><span class="sxs-lookup"><span data-stu-id="6163d-347">Manufacturer string from the version resource (if one is present).</span></span>

</dd> <dt>

<span data-ttu-id="6163d-348">**Nome**</span><span class="sxs-lookup"><span data-stu-id="6163d-348">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6163d-349">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6163d-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6163d-350">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6163d-350">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6163d-351">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6163d-351">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="6163d-352">A propriedade Name é uma cadeia de caracteres que representa o nome herdado que serve como uma chave de uma instância de arquivo lógico em um sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="6163d-352">The Name property is a string representing the inherited name that serves as a key of a logical file instance within a file system.</span></span> <span data-ttu-id="6163d-353">Devem ser fornecidos nomes de caminho completos.</span><span class="sxs-lookup"><span data-stu-id="6163d-353">Full path names should be provided.</span></span>

<span data-ttu-id="6163d-354">Exemplo: C: \\ \\ sistema Windows \\win.ini</span><span class="sxs-lookup"><span data-stu-id="6163d-354">Example: C:\\Windows\\system\\win.ini</span></span>

<span data-ttu-id="6163d-355">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6163d-355">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6163d-356">**Caminho**</span><span class="sxs-lookup"><span data-stu-id="6163d-356">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6163d-357">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6163d-357">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6163d-358">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6163d-358">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6163d-359">Qualificadores: [**fixo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Path")</span><span class="sxs-lookup"><span data-stu-id="6163d-359">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Path")</span></span>
</dt> </dl>

<span data-ttu-id="6163d-360">Caminho do arquivo, incluindo as barras invertidas à esquerda e à direita.</span><span class="sxs-lookup"><span data-stu-id="6163d-360">Path of the file including the leading and trailing backslashes.</span></span> <span data-ttu-id="6163d-361">Exemplo: " \\ sistema do Windows \\ \\ "</span><span class="sxs-lookup"><span data-stu-id="6163d-361">Example: "\\windows\\system\\"</span></span>

<span data-ttu-id="6163d-362">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6163d-362">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6163d-363">**Seres**</span><span class="sxs-lookup"><span data-stu-id="6163d-363">**Readable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6163d-364">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="6163d-364">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6163d-365">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6163d-365">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6163d-366">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("legível")</span><span class="sxs-lookup"><span data-stu-id="6163d-366">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Readable")</span></span>
</dt> </dl>

<span data-ttu-id="6163d-367">Se **for true**, o arquivo poderá ser lido.</span><span class="sxs-lookup"><span data-stu-id="6163d-367">If **True**, the file can be read.</span></span>

<span data-ttu-id="6163d-368">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6163d-368">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6163d-369">**Status**</span><span class="sxs-lookup"><span data-stu-id="6163d-369">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6163d-370">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6163d-370">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6163d-371">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6163d-371">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6163d-372">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="6163d-372">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="6163d-373">Cadeia de caracteres que indica o status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="6163d-373">String that indicates the current status of the object.</span></span> <span data-ttu-id="6163d-374">O status operacional e não operacional pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="6163d-374">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="6163d-375">O status operacional pode incluir "OK", "degradado" e "Pred falha".</span><span class="sxs-lookup"><span data-stu-id="6163d-375">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="6163d-376">"Pred Fail" indica que um elemento está funcionando corretamente, mas está prevendo uma falha (por exemplo, uma unidade de disco rígido habilitada para inteligente).</span><span class="sxs-lookup"><span data-stu-id="6163d-376">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="6163d-377">O status não operacional pode incluir "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="6163d-377">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="6163d-378">O "serviço" pode ser aplicado durante o espelhamento de disco – reprateando, recarregando uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="6163d-378">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="6163d-379">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="6163d-379">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="6163d-380">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6163d-380">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="6163d-381">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="6163d-381">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="6163d-382">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="6163d-382">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="6163d-383">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="6163d-383">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="6163d-384">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="6163d-384">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6163d-385">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="6163d-385">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="6163d-386">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="6163d-386">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="6163d-387">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="6163d-387">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="6163d-388">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="6163d-388">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="6163d-389">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="6163d-389">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="6163d-390">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="6163d-390">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="6163d-391">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="6163d-391">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="6163d-392">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="6163d-392">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="6163d-393">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="6163d-393">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6163d-394">**System**</span><span class="sxs-lookup"><span data-stu-id="6163d-394">**System**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6163d-395">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="6163d-395">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6163d-396">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6163d-396">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6163d-397">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("arquivo do sistema")</span><span class="sxs-lookup"><span data-stu-id="6163d-397">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System File")</span></span>
</dt> </dl>

<span data-ttu-id="6163d-398">Se for **true**, o arquivo será um arquivo do sistema.</span><span class="sxs-lookup"><span data-stu-id="6163d-398">If **True**, the file is a system file.</span></span>

<span data-ttu-id="6163d-399">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6163d-399">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6163d-400">**Versão**</span><span class="sxs-lookup"><span data-stu-id="6163d-400">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6163d-401">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6163d-401">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6163d-402">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6163d-402">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6163d-403">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Version")</span><span class="sxs-lookup"><span data-stu-id="6163d-403">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Version")</span></span>
</dt> </dl>

<span data-ttu-id="6163d-404">Cadeia de caracteres da versão do recurso de versão (se houver uma).</span><span class="sxs-lookup"><span data-stu-id="6163d-404">Version string from the version resource (if one is present).</span></span>

</dd> <dt>

<span data-ttu-id="6163d-405">**Gravável**</span><span class="sxs-lookup"><span data-stu-id="6163d-405">**Writeable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6163d-406">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="6163d-406">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6163d-407">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6163d-407">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6163d-408">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("gravável")</span><span class="sxs-lookup"><span data-stu-id="6163d-408">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Writeable")</span></span>
</dt> </dl>

<span data-ttu-id="6163d-409">Se **for true**, o arquivo poderá ser gravado.</span><span class="sxs-lookup"><span data-stu-id="6163d-409">If **True**, the file can be written.</span></span>

<span data-ttu-id="6163d-410">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6163d-410">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6163d-411">Comentários</span><span class="sxs-lookup"><span data-stu-id="6163d-411">Remarks</span></span>

<span data-ttu-id="6163d-412">A classe de **\_ DataFile do CIM** é derivada de [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6163d-412">The **CIM\_DataFile** class is derived from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="6163d-413">O WMI implementa a classe de **\_ DataFile de arquivo CIM** e todos os seus métodos.</span><span class="sxs-lookup"><span data-stu-id="6163d-413">WMI implements the **CIM\_DataFile** class and all of its methods.</span></span> <span data-ttu-id="6163d-414">A classe de **\_ DataFile do CIM** é uma classe dinâmica.</span><span class="sxs-lookup"><span data-stu-id="6163d-414">The **CIM\_DataFile** class is a dynamic class.</span></span>

<span data-ttu-id="6163d-415">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="6163d-415">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="6163d-416">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="6163d-416">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

<span data-ttu-id="6163d-417">Devido a fins de segurança, o WMI não dá suporte diretamente à chamada de um computador remoto e ao instruí-lo a copiar arquivos para si mesmo.</span><span class="sxs-lookup"><span data-stu-id="6163d-417">Due to security purposes, WMI does not directly support calling a remote computer and instructing it to copy files to itself.</span></span> <span data-ttu-id="6163d-418">No entanto, você pode usar a linguagem de programação relevante para chamar FTP ou RoboCopy, por exemplo.</span><span class="sxs-lookup"><span data-stu-id="6163d-418">However, you can use the relevant programming language to call FTP or RoboCopy, for example.</span></span>

## <a name="examples"></a><span data-ttu-id="6163d-419">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6163d-419">Examples</span></span>

<span data-ttu-id="6163d-420">O [exemplo de código](https://Gallery.TechNet.Microsoft.Com/scriptcenter/Generate-Exchange-2388e7c9) do centro de scripts a seguir usa uma classe de **DataFile de \_ arquivo CIM** como parte de um aplicativo maior para gerar relatórios de ambiente do Exchange usando o PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6163d-420">The following Scripting Center [code example](https://Gallery.TechNet.Microsoft.Com/scriptcenter/Generate-Exchange-2388e7c9) uses a **CIM\_DataFile** class as part of a larger application to Generate exchange environment reports using Powershell.</span></span>

<span data-ttu-id="6163d-421">O exemplo de código [Localizar arquivos com o WMI PowerShell](https://Gallery.TechNet.Microsoft.Com/Find-files-with-WMI-8851e1ea) na galeria do TechNet usa um **\_ arquivo** de informações CIM para pesquisar um ou mais arquivos em vários computadores.</span><span class="sxs-lookup"><span data-stu-id="6163d-421">The [Find files with WMI PowerShell](https://Gallery.TechNet.Microsoft.Com/Find-files-with-WMI-8851e1ea) code sample in TechNet Gallery uses a **CIM\_DataFile** to search for one or more files across multiple computers.</span></span>

<span data-ttu-id="6163d-422">O exemplo de código VBS a seguir descreve como executar uma pesquisa de curingas padrão em um DataFile.</span><span class="sxs-lookup"><span data-stu-id="6163d-422">The following VBS code sample describes how to perform a standard wildcard search on a datafile.</span></span> <span data-ttu-id="6163d-423">Observe que os delimitadores de barra invertida devem ter um escape com outra barra invertida ( \\ \\ ).</span><span class="sxs-lookup"><span data-stu-id="6163d-423">Note that the backslash delimiters must be escaped with another backslash (\\\\).</span></span> <span data-ttu-id="6163d-424">Além disso, ao usar **" \_ arquivo de DataFile CIM**.**FileName**"na cláusula WHERE, o processo Wmiprvse verificará todos os diretórios em qualquer dispositivo de armazenamento disponível.</span><span class="sxs-lookup"><span data-stu-id="6163d-424">Also, when using "**CIM\_DataFile**.**FileName**" in the WHERE clause, the WMIPRVSE process will scan all directories on any available storage device.</span></span> <span data-ttu-id="6163d-425">Isso pode levar algum tempo, especialmente se você tiver mapeado compartilhamentos remotos e puder disparar avisos de antivírus.</span><span class="sxs-lookup"><span data-stu-id="6163d-425">This may take some time, especially if you have mapped remote shares, and can trigger antivirus warnings.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colFiles = objWMIService.ExecQuery("Select * from CIM_DataFile where FileName Like '%~%'")
For Each objFile in colFiles
   Wscript.Echo objFile.Name
Next
```



<span data-ttu-id="6163d-426">O trecho a seguir limita o intervalo de pesquisa a uma unidade, um caminho e uma extensão de arquivo específicos.</span><span class="sxs-lookup"><span data-stu-id="6163d-426">The following snippet limits the search range to a specific drive, path, and file extension.</span></span>


```VB
Set colFiles = objWMIService.ExecQuery("Select * from CIM_DataFile where Drive='"C:"' And Path='"\\"' and Name Like '%~%' and Extension='doc' ")
```



<span data-ttu-id="6163d-427">O exemplo de código do PowerShell a seguir recupera um único valor de atributo.</span><span class="sxs-lookup"><span data-stu-id="6163d-427">The following PowerShell code sample retrieves a single attribute value.</span></span>


```PowerShell
 $computer = "."

  $path = "C:\\Program Files\\Microsoft SQL Server\\MSSQL.1\\MSSQL\\LOG\\"

  $filename = "ERRORLOG"

  $fullname = $path + $filename

  $wql = 'SELECT Archive FROM CIM_DataFile WHERE Name = "' + $fullname + '"'


  Get-WmiObject -ComputerName $computer -Query $wql | foreach { $_.Archive }
```



## <a name="requirements"></a><span data-ttu-id="6163d-428">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6163d-428">Requirements</span></span>



| <span data-ttu-id="6163d-429">Requisito</span><span class="sxs-lookup"><span data-stu-id="6163d-429">Requirement</span></span> | <span data-ttu-id="6163d-430">Valor</span><span class="sxs-lookup"><span data-stu-id="6163d-430">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6163d-431">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6163d-431">Minimum supported client</span></span><br/> | <span data-ttu-id="6163d-432">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6163d-432">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6163d-433">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6163d-433">Minimum supported server</span></span><br/> | <span data-ttu-id="6163d-434">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6163d-434">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6163d-435">Namespace</span><span class="sxs-lookup"><span data-stu-id="6163d-435">Namespace</span></span><br/>                | <span data-ttu-id="6163d-436">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="6163d-436">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6163d-437">MOF</span><span class="sxs-lookup"><span data-stu-id="6163d-437">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6163d-438"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6163d-438"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6163d-439">DLL</span><span class="sxs-lookup"><span data-stu-id="6163d-439">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6163d-440"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6163d-440"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6163d-441">Confira também</span><span class="sxs-lookup"><span data-stu-id="6163d-441">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6163d-442">**CIM \_ LogicalFile**</span><span class="sxs-lookup"><span data-stu-id="6163d-442">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="6163d-443">Tarefas do WMI: arquivos e pastas</span><span class="sxs-lookup"><span data-stu-id="6163d-443">WMI Tasks: Files and Folders</span></span>](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[<span data-ttu-id="6163d-444">**Constantes de direitos de acesso de arquivo e diretório**</span><span class="sxs-lookup"><span data-stu-id="6163d-444">**File and Directory Access Rights Constants**</span></span>](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

