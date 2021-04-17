---
description: A \_ classe CIM LogicalFile representa uma coleção nomeada de dados, que pode ser código executável, que está localizada em um sistema de arquivos em uma extensão de armazenamento.
ms.assetid: 96bf95a1-c8d7-4035-8d5a-38cdb9c75cce
ms.tgt_platform: multiple
title: Classe CIM_LogicalFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile
- CIM_LogicalFile.Caption
- CIM_LogicalFile.Description
- CIM_LogicalFile.InstallDate
- CIM_LogicalFile.Status
- CIM_LogicalFile.AccessMask
- CIM_LogicalFile.Archive
- CIM_LogicalFile.Compressed
- CIM_LogicalFile.CompressionMethod
- CIM_LogicalFile.CreationClassName
- CIM_LogicalFile.CreationDate
- CIM_LogicalFile.CSCreationClassName
- CIM_LogicalFile.CSName
- CIM_LogicalFile.Drive
- CIM_LogicalFile.EightDotThreeFileName
- CIM_LogicalFile.Encrypted
- CIM_LogicalFile.EncryptionMethod
- CIM_LogicalFile.Name
- CIM_LogicalFile.Extension
- CIM_LogicalFile.FileName
- CIM_LogicalFile.FileSize
- CIM_LogicalFile.FileType
- CIM_LogicalFile.FSCreationClassName
- CIM_LogicalFile.FSName
- CIM_LogicalFile.Hidden
- CIM_LogicalFile.InUseCount
- CIM_LogicalFile.LastAccessed
- CIM_LogicalFile.LastModified
- CIM_LogicalFile.Path
- CIM_LogicalFile.Readable
- CIM_LogicalFile.System
- CIM_LogicalFile.Writeable
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a06d2abd1c4ad92d751afa6c8aa47c0cfaa8b1f9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105755212"
---
# <a name="cim_logicalfile-class"></a><span data-ttu-id="e2edb-103">\_Classe de LogicalFile CIM</span><span class="sxs-lookup"><span data-stu-id="e2edb-103">CIM\_LogicalFile class</span></span>

<span data-ttu-id="e2edb-104">A classe **CIM \_ LogicalFile** representa uma coleção nomeada de dados, que pode ser código executável, que está localizada em um sistema de arquivos em uma extensão de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="e2edb-104">The **CIM\_LogicalFile** class represents a named collection of data, which can be executable code, that is located in a file system on a storage extent.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e2edb-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="e2edb-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e2edb-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="e2edb-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="e2edb-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="e2edb-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="e2edb-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="e2edb-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2edb-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e2edb-109">Syntax</span></span>

``` syntax
[SupportsDelete, DeleteBy("DeleteInstance"), Abstract, Provider("CIMWin32"), UUID("{8502C559-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("Files (CIM)"), AMENDMENT]
class CIM_LogicalFile : CIM_LogicalElement
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
};
```

## <a name="members"></a><span data-ttu-id="e2edb-110">Membros</span><span class="sxs-lookup"><span data-stu-id="e2edb-110">Members</span></span>

<span data-ttu-id="e2edb-111">A classe **CIM \_ LogicalFile** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="e2edb-111">The **CIM\_LogicalFile** class has these types of members:</span></span>

-   [<span data-ttu-id="e2edb-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="e2edb-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="e2edb-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e2edb-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e2edb-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="e2edb-114">Methods</span></span>

<span data-ttu-id="e2edb-115">A classe **CIM \_ LogicalFile** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="e2edb-115">The **CIM\_LogicalFile** class has these methods.</span></span>



| <span data-ttu-id="e2edb-116">Método</span><span class="sxs-lookup"><span data-stu-id="e2edb-116">Method</span></span>                                                                                             | <span data-ttu-id="e2edb-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="e2edb-117">Description</span></span>                                                                                                                                              |
|:---------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e2edb-118">**ChangeSecurityPermissions**</span><span class="sxs-lookup"><span data-stu-id="e2edb-118">**ChangeSecurityPermissions**</span></span>](changesecuritypermissions-method-in-class-cim-logicalfile.md)     | <span data-ttu-id="e2edb-119">Altera as permissões de segurança para o arquivo lógico especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="e2edb-119">Changes the security permissions for the logical file specified in the object path.</span></span> <span data-ttu-id="e2edb-120">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="e2edb-120">Not implemented by WMI.</span></span><br/>                                   |
| [<span data-ttu-id="e2edb-121">**ChangeSecurityPermissionsEx**</span><span class="sxs-lookup"><span data-stu-id="e2edb-121">**ChangeSecurityPermissionsEx**</span></span>](changesecuritypermissionsex-method-in-class-cim-logicalfile.md) | <span data-ttu-id="e2edb-122">Altera as permissões de segurança para o arquivo lógico especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="e2edb-122">Changes the security permissions for the logical file specified in the object path.</span></span> <span data-ttu-id="e2edb-123">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="e2edb-123">Not implemented by WMI.</span></span><br/>                                   |
| [<span data-ttu-id="e2edb-124">**Compactar**</span><span class="sxs-lookup"><span data-stu-id="e2edb-124">**Compress**</span></span>](compress-method-in-class-cim-logicalfile.md)                                       | <span data-ttu-id="e2edb-125">Compacta o arquivo lógico (ou diretório) especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="e2edb-125">Compresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="e2edb-126">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="e2edb-126">Not implemented by WMI.</span></span><br/>                                              |
| [<span data-ttu-id="e2edb-127">**CompressEx**</span><span class="sxs-lookup"><span data-stu-id="e2edb-127">**CompressEx**</span></span>](compressex-method-in-class-cim-logicalfile.md)                                   | <span data-ttu-id="e2edb-128">Compacta o arquivo lógico (ou diretório) especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="e2edb-128">Compresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="e2edb-129">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="e2edb-129">Not implemented by WMI.</span></span><br/>                                              |
| [<span data-ttu-id="e2edb-130">**Copiar**</span><span class="sxs-lookup"><span data-stu-id="e2edb-130">**Copy**</span></span>](copy-method-in-class-cim-logicalfile.md)                                               | <span data-ttu-id="e2edb-131">Copia o arquivo lógico (ou diretório) especificado no caminho do objeto para o local especificado pelo parâmetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="e2edb-131">Copies the logical file (or directory) specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="e2edb-132">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="e2edb-132">Not implemented by WMI.</span></span><br/> |
| [<span data-ttu-id="e2edb-133">**CopyEx**</span><span class="sxs-lookup"><span data-stu-id="e2edb-133">**CopyEx**</span></span>](copyex-method-in-class-cim-logicalfile.md)                                           | <span data-ttu-id="e2edb-134">Copia o arquivo lógico (ou diretório) especificado no caminho do objeto para o local especificado pelo parâmetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="e2edb-134">Copies the logical file (or directory) specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="e2edb-135">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="e2edb-135">Not implemented by WMI.</span></span><br/> |
| [<span data-ttu-id="e2edb-136">**Excluir**</span><span class="sxs-lookup"><span data-stu-id="e2edb-136">**Delete**</span></span>](delete-method-in-class-cim-logicalfile.md)                                           | <span data-ttu-id="e2edb-137">Exclui o arquivo lógico (ou diretório) especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="e2edb-137">Deletes the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="e2edb-138">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="e2edb-138">Not implemented by WMI.</span></span><br/>                                                 |
| [<span data-ttu-id="e2edb-139">**DeleteEx**</span><span class="sxs-lookup"><span data-stu-id="e2edb-139">**DeleteEx**</span></span>](deleteex-method-in-class-cim-logicalfile.md)                                       | <span data-ttu-id="e2edb-140">Exclui o arquivo lógico (ou diretório) especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="e2edb-140">Deletes the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="e2edb-141">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="e2edb-141">Not implemented by WMI.</span></span><br/>                                                 |
| [<span data-ttu-id="e2edb-142">**GetEffectivePermission**</span><span class="sxs-lookup"><span data-stu-id="e2edb-142">**GetEffectivePermission**</span></span>](geteffectivepermission-method-in-class-cim-logicalfile.md)           | <span data-ttu-id="e2edb-143">Determina se o chamador tem as permissões agregadas especificadas pelo argumento de **permissão** .</span><span class="sxs-lookup"><span data-stu-id="e2edb-143">Determines whether the caller has the aggregated permissions specified by the **Permission** argument.</span></span> <span data-ttu-id="e2edb-144">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="e2edb-144">Not implemented by WMI.</span></span><br/>                |
| [<span data-ttu-id="e2edb-145">**Renomear**</span><span class="sxs-lookup"><span data-stu-id="e2edb-145">**Rename**</span></span>](rename-method-in-class-cim-logicalfile.md)                                           | <span data-ttu-id="e2edb-146">Renomeia o arquivo lógico (ou diretório) especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="e2edb-146">Renames the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="e2edb-147">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="e2edb-147">Not implemented by WMI.</span></span><br/>                                                 |
| [<span data-ttu-id="e2edb-148">**TakeOwnerShip**</span><span class="sxs-lookup"><span data-stu-id="e2edb-148">**TakeOwnerShip**</span></span>](takeownership-method-in-class-cim-logicalfile.md)                             | <span data-ttu-id="e2edb-149">Obtém a propriedade do arquivo lógico (ou diretório) especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="e2edb-149">Obtains ownership of the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="e2edb-150">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="e2edb-150">Not implemented by WMI.</span></span><br/>                                    |
| [<span data-ttu-id="e2edb-151">**TakeOwnerShipEx**</span><span class="sxs-lookup"><span data-stu-id="e2edb-151">**TakeOwnerShipEx**</span></span>](takeownershipex-method-in-class-cim-logicalfile.md)                         | <span data-ttu-id="e2edb-152">Obtém a propriedade do arquivo lógico (ou diretório) especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="e2edb-152">Obtains ownership of the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="e2edb-153">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="e2edb-153">Not implemented by WMI.</span></span><br/>                                    |
| [<span data-ttu-id="e2edb-154">**Descompactar**</span><span class="sxs-lookup"><span data-stu-id="e2edb-154">**Uncompress**</span></span>](uncompress-method-in-class-cim-logicalfile.md)                                   | <span data-ttu-id="e2edb-155">Descompacta o arquivo lógico (ou diretório) especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="e2edb-155">Uncompresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="e2edb-156">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="e2edb-156">Not implemented by WMI.</span></span><br/>                                            |
| [<span data-ttu-id="e2edb-157">**UncompressEx**</span><span class="sxs-lookup"><span data-stu-id="e2edb-157">**UncompressEx**</span></span>](uncompressex-method-in-class-cim-logicalfile.md)                               | <span data-ttu-id="e2edb-158">Descompacta o arquivo lógico (ou diretório) especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="e2edb-158">Uncompresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="e2edb-159">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="e2edb-159">Not implemented by WMI.</span></span><br/>                                            |



 

### <a name="properties"></a><span data-ttu-id="e2edb-160">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e2edb-160">Properties</span></span>

<span data-ttu-id="e2edb-161">A classe **CIM \_ LogicalFile** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="e2edb-161">The **CIM\_LogicalFile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e2edb-162">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="e2edb-162">**AccessMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2edb-163">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e2edb-163">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e2edb-164">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e2edb-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2edb-165">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("direitos de acesso")</span><span class="sxs-lookup"><span data-stu-id="e2edb-165">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Access Rights")</span></span>
</dt> </dl>

<span data-ttu-id="e2edb-166">Bitmask que representa os direitos de acesso necessários para acessar ou executar operações específicas no arquivo.</span><span class="sxs-lookup"><span data-stu-id="e2edb-166">Bitmask that represents the access rights required to access or perform specific operations on the file.</span></span> <span data-ttu-id="e2edb-167">Para valores de bit, consulte [**constantes de direitos de acesso de arquivo e diretório**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants).</span><span class="sxs-lookup"><span data-stu-id="e2edb-167">For bit values, see [**File and Directory Access Rights Constants**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants).</span></span>

> [!Note]  
> <span data-ttu-id="e2edb-168">Em volumes FAT, o valor de **\_ acesso completo** é retornado, o que indica que nenhuma segurança foi definida no objeto.</span><span class="sxs-lookup"><span data-stu-id="e2edb-168">On FAT volumes, the **FULL\_ACCESS** value is returned instead, which indicates no security has been set on the object.</span></span>

 

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="e2edb-169">Do **arquivo \_ LER \_ os dados (arquivo) ou \_ \_ diretório de lista de arquivos (diretório)** (1)</span><span class="sxs-lookup"><span data-stu-id="e2edb-169">**FILE\_READ\_DATA (file) or FILE\_LIST\_DIRECTORY (directory)** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="e2edb-170">Do **arquivo \_ GRAVAR \_ dados (arquivo) ou arquivo \_ Adicionar \_ arquivo (diretório)** (2)</span><span class="sxs-lookup"><span data-stu-id="e2edb-170">**FILE\_WRITE\_DATA (file) or FILE\_ADD\_FILE (directory)** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="e2edb-171">Do **arquivo \_ ACRESCENTAR \_ dados (arquivo) ou arquivo \_ Adicionar \_ subdiretório (diretório)** (4)</span><span class="sxs-lookup"><span data-stu-id="e2edb-171">**FILE\_APPEND\_DATA (file) or FILE\_ADD\_SUBDIRECTORY (directory)** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="e2edb-172">Do **arquivo \_ LER \_ ea** (8)</span><span class="sxs-lookup"><span data-stu-id="e2edb-172">**FILE\_READ\_EA** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="e2edb-173">Do **arquivo \_ GRAVAR \_ ea** (16)</span><span class="sxs-lookup"><span data-stu-id="e2edb-173">**FILE\_WRITE\_EA** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

<span data-ttu-id="e2edb-174">Do **arquivo \_ EXECUTAR (arquivo) ou \_ atravessamento de arquivo (diretório)** (32)</span><span class="sxs-lookup"><span data-stu-id="e2edb-174">**FILE\_EXECUTE (file) or FILE\_TRAVERSE (directory)** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="e2edb-175">Do **arquivo \_ EXCLUIR \_ filho (diretório)** (64)</span><span class="sxs-lookup"><span data-stu-id="e2edb-175">**FILE\_DELETE\_CHILD (directory)** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="e2edb-176">Do **arquivo \_ \_Atributos de leitura** (128)</span><span class="sxs-lookup"><span data-stu-id="e2edb-176">**FILE\_READ\_ATTRIBUTES** (128)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="e2edb-177">Do **arquivo \_ \_Atributos de gravação** (256)</span><span class="sxs-lookup"><span data-stu-id="e2edb-177">**FILE\_WRITE\_ATTRIBUTES** (256)</span></span>


</dt> <dd></dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="e2edb-178">**Excluir** (65536)</span><span class="sxs-lookup"><span data-stu-id="e2edb-178">**DELETE** (65536)</span></span>


</dt> <dd></dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="e2edb-179">**Ler \_ CONTROLE** (131072)</span><span class="sxs-lookup"><span data-stu-id="e2edb-179">**READ\_CONTROL** (131072)</span></span>


</dt> <dd></dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="e2edb-180">**Gravar \_ DAC** (262144)</span><span class="sxs-lookup"><span data-stu-id="e2edb-180">**WRITE\_DAC** (262144)</span></span>


</dt> <dd></dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="e2edb-181">**Gravar \_ PROPRIETÁRIO** (524288)</span><span class="sxs-lookup"><span data-stu-id="e2edb-181">**WRITE\_OWNER** (524288)</span></span>


</dt> <dd></dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="e2edb-182">**Sincronizar** (1048576)</span><span class="sxs-lookup"><span data-stu-id="e2edb-182">**SYNCHRONIZE** (1048576)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e2edb-183">**Arquivar**</span><span class="sxs-lookup"><span data-stu-id="e2edb-183">**Archive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2edb-184">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="e2edb-184">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e2edb-185">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e2edb-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2edb-186">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("deve ser arquivado")</span><span class="sxs-lookup"><span data-stu-id="e2edb-186">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Should Be Archived")</span></span>
</dt> </dl>

<span data-ttu-id="e2edb-187">Se **for true**, o arquivo deverá ser arquivado.</span><span class="sxs-lookup"><span data-stu-id="e2edb-187">If **True**, the file should be archived.</span></span>

</dd> <dt>

<span data-ttu-id="e2edb-188">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="e2edb-188">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2edb-189">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e2edb-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2edb-190">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e2edb-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2edb-191">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="e2edb-191">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="e2edb-192">Uma breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="e2edb-192">A short textual description of the object.</span></span>

<span data-ttu-id="e2edb-193">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e2edb-193">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2edb-194">**Compactado**</span><span class="sxs-lookup"><span data-stu-id="e2edb-194">**Compressed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2edb-195">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="e2edb-195">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e2edb-196">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e2edb-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2edb-197">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("compactado")</span><span class="sxs-lookup"><span data-stu-id="e2edb-197">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compressed")</span></span>
</dt> </dl>

<span data-ttu-id="e2edb-198">Se **for true**, o arquivo será compactado.</span><span class="sxs-lookup"><span data-stu-id="e2edb-198">If **True**, the file is compressed.</span></span>

</dd> <dt>

<span data-ttu-id="e2edb-199">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="e2edb-199">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2edb-200">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e2edb-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2edb-201">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e2edb-201">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2edb-202">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("método de compactação")</span><span class="sxs-lookup"><span data-stu-id="e2edb-202">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compression Method")</span></span>
</dt> </dl>

<span data-ttu-id="e2edb-203">Cadeia de caracteres de forma livre que indica o algoritmo ou a ferramenta usada para compactar o arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="e2edb-203">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="e2edb-204">Se o esquema de compactação for desconhecido ou não estiver descrito, use "desconhecido".</span><span class="sxs-lookup"><span data-stu-id="e2edb-204">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="e2edb-205">Se o arquivo lógico estiver compactado, mas o esquema de compactação for desconhecido ou não estiver descrito, use "compactado".</span><span class="sxs-lookup"><span data-stu-id="e2edb-205">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="e2edb-206">Se o arquivo lógico não estiver compactado, use "não compactado".</span><span class="sxs-lookup"><span data-stu-id="e2edb-206">If the logical file is not compressed, use "Not Compressed".</span></span>

</dd> <dt>

<span data-ttu-id="e2edb-207">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="e2edb-207">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2edb-208">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e2edb-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2edb-209">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e2edb-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2edb-210">Qualificadores: [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nome da classe")</span><span class="sxs-lookup"><span data-stu-id="e2edb-210">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="e2edb-211">Nome da classe.</span><span class="sxs-lookup"><span data-stu-id="e2edb-211">Name of the class.</span></span>

</dd> <dt>

<span data-ttu-id="e2edb-212">**CreationDate**</span><span class="sxs-lookup"><span data-stu-id="e2edb-212">**CreationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2edb-213">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e2edb-213">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e2edb-214">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e2edb-214">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2edb-215">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("data de criação")</span><span class="sxs-lookup"><span data-stu-id="e2edb-215">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Creation Date")</span></span>
</dt> </dl>

<span data-ttu-id="e2edb-216">Data e hora da criação do arquivo.</span><span class="sxs-lookup"><span data-stu-id="e2edb-216">Date and time of the file's creation.</span></span>

</dd> <dt>

<span data-ttu-id="e2edb-217">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="e2edb-217">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2edb-218">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e2edb-218">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2edb-219">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e2edb-219">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2edb-220">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema de arquivos CIM**](cim-filesystem.md).**CSCreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome da classe do sistema de computador ")</span><span class="sxs-lookup"><span data-stu-id="e2edb-220">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSCreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="e2edb-221">Classe do sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="e2edb-221">Class of the computer system.</span></span>

</dd> <dt>

<span data-ttu-id="e2edb-222">**CSName**</span><span class="sxs-lookup"><span data-stu-id="e2edb-222">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2edb-223">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e2edb-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2edb-224">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e2edb-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2edb-225">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema de arquivos CIM**](cim-filesystem.md).**CSName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome do sistema de computador ")</span><span class="sxs-lookup"><span data-stu-id="e2edb-225">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Name")</span></span>
</dt> </dl>

<span data-ttu-id="e2edb-226">Nome do sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="e2edb-226">Name of the computer system.</span></span>

</dd> <dt>

<span data-ttu-id="e2edb-227">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="e2edb-227">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2edb-228">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e2edb-228">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2edb-229">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e2edb-229">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2edb-230">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="e2edb-230">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="e2edb-231">Uma descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="e2edb-231">A textual description of the object.</span></span>

<span data-ttu-id="e2edb-232">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e2edb-232">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2edb-233">**Unidade**</span><span class="sxs-lookup"><span data-stu-id="e2edb-233">**Drive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2edb-234">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e2edb-234">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2edb-235">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e2edb-235">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2edb-236">Qualificadores: [**fixo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("drive")</span><span class="sxs-lookup"><span data-stu-id="e2edb-236">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Drive")</span></span>
</dt> </dl>

<span data-ttu-id="e2edb-237">Letra da unidade (incluindo os dois-pontos que segue a letra da unidade) do arquivo.</span><span class="sxs-lookup"><span data-stu-id="e2edb-237">Drive letter (including the colon that follows the drive letter) of the file.</span></span> <span data-ttu-id="e2edb-238">Essa propriedade é herdada **do \_ LogicalFile CIM**. Exemplo: "c:"</span><span class="sxs-lookup"><span data-stu-id="e2edb-238">This property is inherited from **CIM\_LogicalFile**.Example: "c:"</span></span>

</dd> <dt>

<span data-ttu-id="e2edb-239">**EightDotThreeFileName**</span><span class="sxs-lookup"><span data-stu-id="e2edb-239">**EightDotThreeFileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2edb-240">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e2edb-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2edb-241">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e2edb-241">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2edb-242">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("oito pontos três nome de arquivo")</span><span class="sxs-lookup"><span data-stu-id="e2edb-242">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Eight Dot Three File Name")</span></span>
</dt> </dl>

<span data-ttu-id="e2edb-243">Nome de arquivo compatível com o DOS.</span><span class="sxs-lookup"><span data-stu-id="e2edb-243">DOS-compatible file name.</span></span> <span data-ttu-id="e2edb-244">Exemplo: "c: \\ progra ~ 1"</span><span class="sxs-lookup"><span data-stu-id="e2edb-244">Example: "c:\\progra~1"</span></span>

</dd> <dt>

<span data-ttu-id="e2edb-245">**Criptografado**</span><span class="sxs-lookup"><span data-stu-id="e2edb-245">**Encrypted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2edb-246">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="e2edb-246">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e2edb-247">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e2edb-247">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2edb-248">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encrypted")</span><span class="sxs-lookup"><span data-stu-id="e2edb-248">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encrypted")</span></span>
</dt> </dl>

<span data-ttu-id="e2edb-249">Se **for true**, o arquivo será criptografado.</span><span class="sxs-lookup"><span data-stu-id="e2edb-249">If **True**, the file is encrypted.</span></span>

</dd> <dt>

<span data-ttu-id="e2edb-250">**EncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="e2edb-250">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2edb-251">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e2edb-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2edb-252">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e2edb-252">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2edb-253">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("método de criptografia")</span><span class="sxs-lookup"><span data-stu-id="e2edb-253">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encryption Method")</span></span>
</dt> </dl>

<span data-ttu-id="e2edb-254">Cadeia de caracteres de forma livre que identifica o algoritmo ou a ferramenta usada para criptografar um arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="e2edb-254">Free-form string that identifies the algorithm or tool used to encrypt a logical file.</span></span> <span data-ttu-id="e2edb-255">Se o esquema de criptografia não for indulged (por motivos de segurança, por exemplo), use "desconhecido".</span><span class="sxs-lookup"><span data-stu-id="e2edb-255">If the encryption scheme is not indulged (for security reasons, for example), use "Unknown".</span></span> <span data-ttu-id="e2edb-256">Se o arquivo estiver criptografado, mas seu esquema de criptografia for desconhecido ou não for divulgado, use "Encrypted".</span><span class="sxs-lookup"><span data-stu-id="e2edb-256">If the file is encrypted, but either its encryption scheme is unknown or not disclosed, use "Encrypted".</span></span> <span data-ttu-id="e2edb-257">Se o arquivo lógico não estiver criptografado, use "não criptografado".</span><span class="sxs-lookup"><span data-stu-id="e2edb-257">If the logical file is not encrypted, use "Not Encrypted".</span></span>

</dd> <dt>

<span data-ttu-id="e2edb-258">**Extensão**</span><span class="sxs-lookup"><span data-stu-id="e2edb-258">**Extension**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2edb-259">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e2edb-259">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2edb-260">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e2edb-260">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2edb-261">Qualificadores: [**fixo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("extensão de arquivo")</span><span class="sxs-lookup"><span data-stu-id="e2edb-261">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Extension")</span></span>
</dt> </dl>

<span data-ttu-id="e2edb-262">Extensão de nome de arquivo sem o ponto anterior (ponto).</span><span class="sxs-lookup"><span data-stu-id="e2edb-262">File name extension without the preceding period (dot).</span></span> <span data-ttu-id="e2edb-263">Exemplo: "txt", "MOF", "mdb"</span><span class="sxs-lookup"><span data-stu-id="e2edb-263">Example: "txt", "mof", "mdb"</span></span>

</dd> <dt>

<span data-ttu-id="e2edb-264">**FileName**</span><span class="sxs-lookup"><span data-stu-id="e2edb-264">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2edb-265">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e2edb-265">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2edb-266">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e2edb-266">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2edb-267">Qualificadores: [**fixo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nome do arquivo")</span><span class="sxs-lookup"><span data-stu-id="e2edb-267">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Name")</span></span>
</dt> </dl>

<span data-ttu-id="e2edb-268">Nome do arquivo sem a extensão de nome de arquivo.</span><span class="sxs-lookup"><span data-stu-id="e2edb-268">File name without the file name extension.</span></span> <span data-ttu-id="e2edb-269">Exemplo: "mydatafile"</span><span class="sxs-lookup"><span data-stu-id="e2edb-269">Example: "MyDataFile"</span></span>

</dd> <dt>

<span data-ttu-id="e2edb-270">**Tamanho**</span><span class="sxs-lookup"><span data-stu-id="e2edb-270">**FileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2edb-271">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e2edb-271">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e2edb-272">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e2edb-272">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2edb-273">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("tamanho"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="e2edb-273">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Size"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="e2edb-274">Tamanho do arquivo, em bytes.</span><span class="sxs-lookup"><span data-stu-id="e2edb-274">Size of the file, in bytes.</span></span>

<span data-ttu-id="e2edb-275">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="e2edb-275">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="e2edb-276">**Talvez**</span><span class="sxs-lookup"><span data-stu-id="e2edb-276">**FileType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2edb-277">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e2edb-277">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2edb-278">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e2edb-278">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2edb-279">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("tipo de arquivo")</span><span class="sxs-lookup"><span data-stu-id="e2edb-279">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Type")</span></span>
</dt> </dl>

<span data-ttu-id="e2edb-280">Descritor que representa o tipo de arquivo indicado pela propriedade de **extensão** .</span><span class="sxs-lookup"><span data-stu-id="e2edb-280">Descriptor that represents the file type indicated by the **Extension** property.</span></span>

</dd> <dt>

<span data-ttu-id="e2edb-281">**FSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="e2edb-281">**FSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2edb-282">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e2edb-282">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2edb-283">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e2edb-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2edb-284">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema de arquivos CIM**](cim-filesystem.md).**CreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome da classe do sistema de arquivos ")</span><span class="sxs-lookup"><span data-stu-id="e2edb-284">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="e2edb-285">Classe do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="e2edb-285">Class of the file system.</span></span>

</dd> <dt>

<span data-ttu-id="e2edb-286">**FSName**</span><span class="sxs-lookup"><span data-stu-id="e2edb-286">**FSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2edb-287">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e2edb-287">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2edb-288">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e2edb-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2edb-289">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema de arquivos CIM**](cim-filesystem.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome do sistema de arquivos ")</span><span class="sxs-lookup"><span data-stu-id="e2edb-289">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Name")</span></span>
</dt> </dl>

<span data-ttu-id="e2edb-290">Nome do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="e2edb-290">Name of the file system.</span></span>

</dd> <dt>

<span data-ttu-id="e2edb-291">**Oculto**</span><span class="sxs-lookup"><span data-stu-id="e2edb-291">**Hidden**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2edb-292">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="e2edb-292">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e2edb-293">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e2edb-293">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2edb-294">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hidden")</span><span class="sxs-lookup"><span data-stu-id="e2edb-294">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hidden")</span></span>
</dt> </dl>

<span data-ttu-id="e2edb-295">Se for **true**, o arquivo ficará oculto.</span><span class="sxs-lookup"><span data-stu-id="e2edb-295">If **True**, the file is hidden.</span></span>

</dd> <dt>

<span data-ttu-id="e2edb-296">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="e2edb-296">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2edb-297">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e2edb-297">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e2edb-298">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e2edb-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2edb-299">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="e2edb-299">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="e2edb-300">Indica quando o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="e2edb-300">Indicates when the object was installed.</span></span> <span data-ttu-id="e2edb-301">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="e2edb-301">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="e2edb-302">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e2edb-302">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2edb-303">**InUseCount**</span><span class="sxs-lookup"><span data-stu-id="e2edb-303">**InUseCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2edb-304">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e2edb-304">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e2edb-305">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e2edb-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2edb-306">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("contagem de abertura de arquivo atual")</span><span class="sxs-lookup"><span data-stu-id="e2edb-306">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Current File Open Count")</span></span>
</dt> </dl>

<span data-ttu-id="e2edb-307">Número de "aberturas de arquivo" que estão atualmente ativos no arquivo.</span><span class="sxs-lookup"><span data-stu-id="e2edb-307">Number of "file opens" that are currently active against the file.</span></span>

<span data-ttu-id="e2edb-308">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="e2edb-308">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="e2edb-309">**LastAccessed**</span><span class="sxs-lookup"><span data-stu-id="e2edb-309">**LastAccessed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2edb-310">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e2edb-310">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e2edb-311">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e2edb-311">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2edb-312">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("último acesso")</span><span class="sxs-lookup"><span data-stu-id="e2edb-312">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Accessed")</span></span>
</dt> </dl>

<span data-ttu-id="e2edb-313">Data e hora do último acesso ao arquivo.</span><span class="sxs-lookup"><span data-stu-id="e2edb-313">Date and time the file was last accessed.</span></span>

</dd> <dt>

<span data-ttu-id="e2edb-314">**LastModified**</span><span class="sxs-lookup"><span data-stu-id="e2edb-314">**LastModified**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2edb-315">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e2edb-315">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e2edb-316">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e2edb-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2edb-317">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("última modificação")</span><span class="sxs-lookup"><span data-stu-id="e2edb-317">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Modified")</span></span>
</dt> </dl>

<span data-ttu-id="e2edb-318">Data e hora da última modificação do arquivo.</span><span class="sxs-lookup"><span data-stu-id="e2edb-318">Date and time the file was last modified.</span></span>

</dd> <dt>

<span data-ttu-id="e2edb-319">**Nome**</span><span class="sxs-lookup"><span data-stu-id="e2edb-319">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2edb-320">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e2edb-320">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2edb-321">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e2edb-321">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2edb-322">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e2edb-322">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e2edb-323">A propriedade Name é uma cadeia de caracteres que representa o nome herdado que serve como uma chave de uma instância de arquivo lógico em um sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="e2edb-323">The Name property is a string representing the inherited name that serves as a key of a logical file instance within a file system.</span></span> <span data-ttu-id="e2edb-324">Devem ser fornecidos nomes de caminho completos.</span><span class="sxs-lookup"><span data-stu-id="e2edb-324">Full path names should be provided.</span></span> <span data-ttu-id="e2edb-325">Exemplo: C: \\ \\ sistema Windows \\win.ini</span><span class="sxs-lookup"><span data-stu-id="e2edb-325">Example: C:\\Windows\\system\\win.ini</span></span>

</dd> <dt>

<span data-ttu-id="e2edb-326">**Caminho**</span><span class="sxs-lookup"><span data-stu-id="e2edb-326">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2edb-327">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e2edb-327">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2edb-328">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e2edb-328">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2edb-329">Qualificadores: [**fixo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Path")</span><span class="sxs-lookup"><span data-stu-id="e2edb-329">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Path")</span></span>
</dt> </dl>

<span data-ttu-id="e2edb-330">Caminho do arquivo, incluindo as barras invertidas à esquerda e à direita.</span><span class="sxs-lookup"><span data-stu-id="e2edb-330">Path of the file including the leading and trailing backslashes.</span></span> <span data-ttu-id="e2edb-331">Exemplo: " \\ sistema do Windows \\ \\ "</span><span class="sxs-lookup"><span data-stu-id="e2edb-331">Example: "\\windows\\system\\"</span></span>

</dd> <dt>

<span data-ttu-id="e2edb-332">**Seres**</span><span class="sxs-lookup"><span data-stu-id="e2edb-332">**Readable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2edb-333">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="e2edb-333">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e2edb-334">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e2edb-334">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2edb-335">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("legível")</span><span class="sxs-lookup"><span data-stu-id="e2edb-335">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Readable")</span></span>
</dt> </dl>

<span data-ttu-id="e2edb-336">Se **for true**, o arquivo poderá ser lido.</span><span class="sxs-lookup"><span data-stu-id="e2edb-336">If **True**, the file can be read.</span></span>

</dd> <dt>

<span data-ttu-id="e2edb-337">**Status**</span><span class="sxs-lookup"><span data-stu-id="e2edb-337">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2edb-338">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e2edb-338">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2edb-339">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e2edb-339">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2edb-340">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="e2edb-340">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="e2edb-341">Cadeia de caracteres que indica o status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="e2edb-341">String that indicates the current status of the object.</span></span> <span data-ttu-id="e2edb-342">O status operacional e não operacional pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="e2edb-342">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="e2edb-343">O status operacional pode incluir "OK", "degradado" e "Pred falha".</span><span class="sxs-lookup"><span data-stu-id="e2edb-343">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="e2edb-344">"Pred Fail" indica que um elemento está funcionando corretamente, mas está prevendo uma falha (por exemplo, uma unidade de disco rígido habilitada para inteligente).</span><span class="sxs-lookup"><span data-stu-id="e2edb-344">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="e2edb-345">O status não operacional pode incluir "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="e2edb-345">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="e2edb-346">O "serviço" pode ser aplicado durante o espelhamento de disco – reprateando, recarregando uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="e2edb-346">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="e2edb-347">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="e2edb-347">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="e2edb-348">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e2edb-348">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="e2edb-349">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="e2edb-349">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="e2edb-350">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="e2edb-350">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="e2edb-351">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="e2edb-351">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="e2edb-352">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="e2edb-352">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e2edb-353">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="e2edb-353">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="e2edb-354">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="e2edb-354">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="e2edb-355">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="e2edb-355">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="e2edb-356">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="e2edb-356">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="e2edb-357">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="e2edb-357">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="e2edb-358">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="e2edb-358">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="e2edb-359">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="e2edb-359">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="e2edb-360">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="e2edb-360">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="e2edb-361">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="e2edb-361">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e2edb-362">**System**</span><span class="sxs-lookup"><span data-stu-id="e2edb-362">**System**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2edb-363">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="e2edb-363">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e2edb-364">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e2edb-364">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2edb-365">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("arquivo do sistema")</span><span class="sxs-lookup"><span data-stu-id="e2edb-365">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System File")</span></span>
</dt> </dl>

<span data-ttu-id="e2edb-366">Se for **true**, o arquivo será um arquivo do sistema.</span><span class="sxs-lookup"><span data-stu-id="e2edb-366">If **True**, the file is a system file.</span></span>

</dd> <dt>

<span data-ttu-id="e2edb-367">**Gravável**</span><span class="sxs-lookup"><span data-stu-id="e2edb-367">**Writeable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2edb-368">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="e2edb-368">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e2edb-369">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e2edb-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2edb-370">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("gravável")</span><span class="sxs-lookup"><span data-stu-id="e2edb-370">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Writeable")</span></span>
</dt> </dl>

<span data-ttu-id="e2edb-371">Se **for true**, o arquivo poderá ser gravado.</span><span class="sxs-lookup"><span data-stu-id="e2edb-371">If **True**, the file can be written.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e2edb-372">Comentários</span><span class="sxs-lookup"><span data-stu-id="e2edb-372">Remarks</span></span>

<span data-ttu-id="e2edb-373">A classe de **\_ LogicalFile CIM** é derivada de [**CIM \_ LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="e2edb-373">The **CIM\_LogicalFile** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="e2edb-374">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="e2edb-374">WMI does not implement this class.</span></span> <span data-ttu-id="e2edb-375">Para classes derivadas de **CIM \_ LogicalFile**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="e2edb-375">For classes derived from **CIM\_LogicalFile**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="e2edb-376">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="e2edb-376">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e2edb-377">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="e2edb-377">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2edb-378">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e2edb-378">Requirements</span></span>



| <span data-ttu-id="e2edb-379">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2edb-379">Requirement</span></span> | <span data-ttu-id="e2edb-380">Valor</span><span class="sxs-lookup"><span data-stu-id="e2edb-380">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e2edb-381">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e2edb-381">Minimum supported client</span></span><br/> | <span data-ttu-id="e2edb-382">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e2edb-382">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e2edb-383">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e2edb-383">Minimum supported server</span></span><br/> | <span data-ttu-id="e2edb-384">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e2edb-384">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e2edb-385">Namespace</span><span class="sxs-lookup"><span data-stu-id="e2edb-385">Namespace</span></span><br/>                | <span data-ttu-id="e2edb-386">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="e2edb-386">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e2edb-387">MOF</span><span class="sxs-lookup"><span data-stu-id="e2edb-387">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e2edb-388"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e2edb-388"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e2edb-389">DLL</span><span class="sxs-lookup"><span data-stu-id="e2edb-389">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e2edb-390"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e2edb-390"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2edb-391">Confira também</span><span class="sxs-lookup"><span data-stu-id="e2edb-391">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2edb-392">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="e2edb-392">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

