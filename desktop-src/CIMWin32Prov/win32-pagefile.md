---
description: O \_ arquivo de paginação Win32&\# 32; A classe WMI representa o arquivo usado para lidar com a troca de arquivos de memória virtual em um sistema Win32. Essa classe foi substituída.
ms.assetid: 5599d09d-a2fd-4217-8560-5fd56f09d47b
ms.tgt_platform: multiple
title: Classe Win32_PageFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFile
- Win32_PageFile.Caption
- Win32_PageFile.Description
- Win32_PageFile.InstallDate
- Win32_PageFile.Archive
- Win32_PageFile.Compressed
- Win32_PageFile.CompressionMethod
- Win32_PageFile.CreationClassName
- Win32_PageFile.CreationDate
- Win32_PageFile.CSCreationClassName
- Win32_PageFile.CSName
- Win32_PageFile.Drive
- Win32_PageFile.EightDotThreeFileName
- Win32_PageFile.Encrypted
- Win32_PageFile.EncryptionMethod
- Win32_PageFile.Extension
- Win32_PageFile.FileName
- Win32_PageFile.FileSize
- Win32_PageFile.FileType
- Win32_PageFile.FSCreationClassName
- Win32_PageFile.FSName
- Win32_PageFile.Hidden
- Win32_PageFile.InUseCount
- Win32_PageFile.LastAccessed
- Win32_PageFile.LastModified
- Win32_PageFile.Path
- Win32_PageFile.Readable
- Win32_PageFile.System
- Win32_PageFile.Writeable
- Win32_PageFile.AccessMask
- Win32_PageFile.Manufacturer
- Win32_PageFile.Status
- Win32_PageFile.Version
- Win32_PageFile.FreeSpace
- Win32_PageFile.InitialSize
- Win32_PageFile.MaximumSize
- Win32_PageFile.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fb63c4242ae8fa3cca5133a25d2742d07210ca1c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756430"
---
# <a name="win32_pagefile-class"></a><span data-ttu-id="3dd31-104">\_Classe de arquivo de paginação Win32</span><span class="sxs-lookup"><span data-stu-id="3dd31-104">Win32\_PageFile class</span></span>

<span data-ttu-id="3dd31-105">A [classe WMI](../wmisdk/retrieving-a-class.md) de arquivo de **\_ paginação Win32** representa o arquivo usado para lidar com a troca de arquivos de memória virtual em um sistema Win32.</span><span class="sxs-lookup"><span data-stu-id="3dd31-105">The **Win32\_PageFile** [WMI class](../wmisdk/retrieving-a-class.md) represents the file used for handling virtual memory file swapping on a Win32 system.</span></span> <span data-ttu-id="3dd31-106">Essa classe foi substituída.</span><span class="sxs-lookup"><span data-stu-id="3dd31-106">This class has been deprecated.</span></span>

<span data-ttu-id="3dd31-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="3dd31-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="3dd31-108">As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.</span><span class="sxs-lookup"><span data-stu-id="3dd31-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3dd31-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3dd31-109">Syntax</span></span>

``` syntax
[DEPRECATED, Dynamic, Provider("CIMWin32"), Privileges("SeCreatePagefilePrivilege"), UUID("{8502C4C6-5FBB-11D2-AAC1-006008C78BC7}"), SupportsCreate, CreateBy("PutInstance"), SupportsDelete, DeleteBy("DeleteInstance"), SupportsUpdate, AMENDMENT]
class Win32_PageFile : CIM_DataFile
{
  string   Caption;
  string   Description;
  datetime InstallDate;
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
  uint32   AccessMask;
  string   Manufacturer;
  string   Status;
  string   Version;
  uint32   FreeSpace;
  uint32   InitialSize;
  uint32   MaximumSize;
  string   Name;
};
```

## <a name="members"></a><span data-ttu-id="3dd31-110">Membros</span><span class="sxs-lookup"><span data-stu-id="3dd31-110">Members</span></span>

<span data-ttu-id="3dd31-111">A classe de **\_ arquivo de paginação Win32** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="3dd31-111">The **Win32\_PageFile** class has these types of members:</span></span>

-   [<span data-ttu-id="3dd31-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="3dd31-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="3dd31-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3dd31-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="3dd31-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="3dd31-114">Methods</span></span>

<span data-ttu-id="3dd31-115">A classe de **\_ arquivo de paginação Win32** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="3dd31-115">The **Win32\_PageFile** class has these methods.</span></span>



| <span data-ttu-id="3dd31-116">Método</span><span class="sxs-lookup"><span data-stu-id="3dd31-116">Method</span></span>                                                                                            | <span data-ttu-id="3dd31-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="3dd31-117">Description</span></span>                                                                                                                                                                                                                            |
|:--------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3dd31-118">**ChangeSecurityPermissions**</span><span class="sxs-lookup"><span data-stu-id="3dd31-118">**ChangeSecurityPermissions**</span></span>](changesecuritypermissions-method-in-class-win32-pagefile.md)     | <span data-ttu-id="3dd31-119">Método de classe que altera as permissões de segurança para o arquivo lógico especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="3dd31-119">Class method that changes the security permissions for the logical file specified in the object path.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="3dd31-120">**ChangeSecurityPermissionsEx**</span><span class="sxs-lookup"><span data-stu-id="3dd31-120">**ChangeSecurityPermissionsEx**</span></span>](changesecuritypermissionsex-method-in-class-win32-pagefile.md) | <span data-ttu-id="3dd31-121">Método de classe que altera as permissões de segurança para o arquivo lógico especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="3dd31-121">Class method that changes the security permissions for the logical file specified in the object path.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="3dd31-122">**Compactar**</span><span class="sxs-lookup"><span data-stu-id="3dd31-122">**Compress**</span></span>](compress-method-in-class-win32-pagefile.md)                                       | <span data-ttu-id="3dd31-123">Método de classe que compacta o arquivo lógico (ou diretório) especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="3dd31-123">Class method that compresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="3dd31-124">**CompressEx**</span><span class="sxs-lookup"><span data-stu-id="3dd31-124">**CompressEx**</span></span>](compressex-method-in-class-win32-pagefile.md)                                   | <span data-ttu-id="3dd31-125">Método de classe que compacta o arquivo lógico (ou diretório) especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="3dd31-125">Class method that compresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="3dd31-126">**Copiar**</span><span class="sxs-lookup"><span data-stu-id="3dd31-126">**Copy**</span></span>](copy-method-in-class-win32-pagefile.md)                                               | <span data-ttu-id="3dd31-127">Método de classe que copia o arquivo ou diretório lógico especificado no caminho do objeto para o local especificado pelo parâmetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="3dd31-127">Class method that copies the logical file or directory specified in the object path to the location specified by the input parameter.</span></span><br/>                                                                                       |
| [<span data-ttu-id="3dd31-128">**CopyEx**</span><span class="sxs-lookup"><span data-stu-id="3dd31-128">**CopyEx**</span></span>](copyex-method-in-class-win32-pagefile.md)                                           | <span data-ttu-id="3dd31-129">Método de classe que copia o arquivo ou diretório lógico especificado no caminho do objeto para o local especificado pelo parâmetro FileName.</span><span class="sxs-lookup"><span data-stu-id="3dd31-129">Class method that copies the logical file or directory specified in the object path to the location specified by the FileName parameter.</span></span><br/>                                                                                    |
| [<span data-ttu-id="3dd31-130">**Excluir**</span><span class="sxs-lookup"><span data-stu-id="3dd31-130">**Delete**</span></span>](delete-method-in-class-win32-pagefile.md)                                           | <span data-ttu-id="3dd31-131">Método de classe que exclui o arquivo lógico (ou diretório) especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="3dd31-131">Class method that deletes the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                     |
| [<span data-ttu-id="3dd31-132">**DeleteEx**</span><span class="sxs-lookup"><span data-stu-id="3dd31-132">**DeleteEx**</span></span>](deleteex-method-in-class-win32-pagefile.md)                                       | <span data-ttu-id="3dd31-133">Método de classe que exclui o arquivo lógico (ou diretório) especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="3dd31-133">Class method that deletes the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                     |
| [<span data-ttu-id="3dd31-134">**GetEffectivePermission**</span><span class="sxs-lookup"><span data-stu-id="3dd31-134">**GetEffectivePermission**</span></span>](geteffectivepermission-method-in-class-win32-pagefile.md)           | <span data-ttu-id="3dd31-135">Método de classe que determina se o chamador tem as permissões agregadas especificadas pelo argumento de *permissão* não apenas no objeto File, mas no compartilhamento o arquivo ou diretório reside (se estiver em um compartilhamento).</span><span class="sxs-lookup"><span data-stu-id="3dd31-135">Class method that determines whether the caller has the aggregated permissions specified by the *Permission* argument not only on the file object, but on the share the file or directory resides on (if it is on a share).</span></span><br/> |
| [<span data-ttu-id="3dd31-136">**Renomear**</span><span class="sxs-lookup"><span data-stu-id="3dd31-136">**Rename**</span></span>](rename-method-in-class-win32-pagefile.md)                                           | <span data-ttu-id="3dd31-137">Método de classe que renomeia o arquivo lógico (ou diretório) especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="3dd31-137">Class method that renames the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                     |
| [<span data-ttu-id="3dd31-138">**TakeOwnerShip**</span><span class="sxs-lookup"><span data-stu-id="3dd31-138">**TakeOwnerShip**</span></span>](takeownership-method-in-class-win32-pagefile.md)                             | <span data-ttu-id="3dd31-139">Método de classe que obtém a propriedade do arquivo lógico especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="3dd31-139">Class method that obtains ownership of the logical file specified in the object path.</span></span><br/>                                                                                                                                       |
| [<span data-ttu-id="3dd31-140">**TakeOwnerShipEx**</span><span class="sxs-lookup"><span data-stu-id="3dd31-140">**TakeOwnerShipEx**</span></span>](takeownershipex-method-in-class-win32-pagefile.md)                         | <span data-ttu-id="3dd31-141">Método de classe que obtém a propriedade do arquivo lógico especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="3dd31-141">Class method that obtains ownership of the logical file specified in the object path.</span></span><br/>                                                                                                                                       |
| [<span data-ttu-id="3dd31-142">**Descompactar**</span><span class="sxs-lookup"><span data-stu-id="3dd31-142">**Uncompress**</span></span>](uncompress-method-in-class-win32-pagefile.md)                                   | <span data-ttu-id="3dd31-143">Método de classe que descompacta o arquivo lógico (ou diretório) especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="3dd31-143">Class method that uncompresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="3dd31-144">**UncompressEx**</span><span class="sxs-lookup"><span data-stu-id="3dd31-144">**UncompressEx**</span></span>](uncompressex-method-in-class-win32-pagefile.md)                               | <span data-ttu-id="3dd31-145">Método de classe que descompacta o arquivo lógico (ou diretório) especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="3dd31-145">Class method that uncompresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                |



 

### <a name="properties"></a><span data-ttu-id="3dd31-146">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3dd31-146">Properties</span></span>

<span data-ttu-id="3dd31-147">A classe de **\_ arquivo de paginação Win32** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="3dd31-147">The **Win32\_PageFile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3dd31-148">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="3dd31-148">**AccessMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dd31-149">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3dd31-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3dd31-150">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3dd31-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3dd31-151">Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("direitos de acesso")</span><span class="sxs-lookup"><span data-stu-id="3dd31-151">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Access Rights")</span></span>
</dt> </dl>

<span data-ttu-id="3dd31-152">Bitmask que representa os direitos de acesso necessários para acessar ou executar operações específicas no arquivo.</span><span class="sxs-lookup"><span data-stu-id="3dd31-152">Bitmask that represents the access rights required to access or perform specific operations on the file.</span></span> <span data-ttu-id="3dd31-153">Para obter valores, consulte [**constantes de direitos de acesso de arquivo e diretório**](../wmisdk/file-and-directory-access-rights-constants.md).</span><span class="sxs-lookup"><span data-stu-id="3dd31-153">For values, see [**File and Directory Access Rights Constants**](../wmisdk/file-and-directory-access-rights-constants.md).</span></span>

<span data-ttu-id="3dd31-154">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="3dd31-154">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="3dd31-155">Do **arquivo \_ LER \_ os dados (arquivo) ou \_ \_ diretório de lista de arquivos (diretório)** (1)</span><span class="sxs-lookup"><span data-stu-id="3dd31-155">**FILE\_READ\_DATA (file) or FILE\_LIST\_DIRECTORY (directory)** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="3dd31-156">Do **arquivo \_ GRAVAR \_ dados (arquivo) ou arquivo \_ Adicionar \_ arquivo (diretório)** (2)</span><span class="sxs-lookup"><span data-stu-id="3dd31-156">**FILE\_WRITE\_DATA (file) or FILE\_ADD\_FILE (directory)** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="3dd31-157">Do **arquivo \_ ACRESCENTAR \_ dados (arquivo) ou arquivo \_ Adicionar \_ subdiretório (diretório)** (4)</span><span class="sxs-lookup"><span data-stu-id="3dd31-157">**FILE\_APPEND\_DATA (file) or FILE\_ADD\_SUBDIRECTORY (directory)** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="3dd31-158">Do **arquivo \_ LER \_ ea** (8)</span><span class="sxs-lookup"><span data-stu-id="3dd31-158">**FILE\_READ\_EA** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="3dd31-159">Do **arquivo \_ GRAVAR \_ ea** (16)</span><span class="sxs-lookup"><span data-stu-id="3dd31-159">**FILE\_WRITE\_EA** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

<span data-ttu-id="3dd31-160">Do **arquivo \_ EXECUTAR (arquivo) ou \_ atravessamento de arquivo (diretório)** (32)</span><span class="sxs-lookup"><span data-stu-id="3dd31-160">**FILE\_EXECUTE (file) or FILE\_TRAVERSE (directory)** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="3dd31-161">Do **arquivo \_ EXCLUIR \_ filho (diretório)** (64)</span><span class="sxs-lookup"><span data-stu-id="3dd31-161">**FILE\_DELETE\_CHILD (directory)** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="3dd31-162">Do **arquivo \_ \_Atributos de leitura** (128)</span><span class="sxs-lookup"><span data-stu-id="3dd31-162">**FILE\_READ\_ATTRIBUTES** (128)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="3dd31-163">Do **arquivo \_ \_Atributos de gravação** (256)</span><span class="sxs-lookup"><span data-stu-id="3dd31-163">**FILE\_WRITE\_ATTRIBUTES** (256)</span></span>


</dt> <dd></dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="3dd31-164">**Excluir** (65536)</span><span class="sxs-lookup"><span data-stu-id="3dd31-164">**DELETE** (65536)</span></span>


</dt> <dd></dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="3dd31-165">**Ler \_ CONTROLE** (131072)</span><span class="sxs-lookup"><span data-stu-id="3dd31-165">**READ\_CONTROL** (131072)</span></span>


</dt> <dd></dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="3dd31-166">**Gravar \_ DAC** (262144)</span><span class="sxs-lookup"><span data-stu-id="3dd31-166">**WRITE\_DAC** (262144)</span></span>


</dt> <dd></dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="3dd31-167">**Gravar \_ PROPRIETÁRIO** (524288)</span><span class="sxs-lookup"><span data-stu-id="3dd31-167">**WRITE\_OWNER** (524288)</span></span>


</dt> <dd></dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="3dd31-168">**Sincronizar** (1048576)</span><span class="sxs-lookup"><span data-stu-id="3dd31-168">**SYNCHRONIZE** (1048576)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3dd31-169">**Arquivar**</span><span class="sxs-lookup"><span data-stu-id="3dd31-169">**Archive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dd31-170">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="3dd31-170">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3dd31-171">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3dd31-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3dd31-172">Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("deve ser arquivado")</span><span class="sxs-lookup"><span data-stu-id="3dd31-172">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Should Be Archived")</span></span>
</dt> </dl>

<span data-ttu-id="3dd31-173">Se **for true**, o arquivo deverá ser arquivado.</span><span class="sxs-lookup"><span data-stu-id="3dd31-173">If **True**, the file should be archived.</span></span>

<span data-ttu-id="3dd31-174">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="3dd31-174">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="3dd31-175">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="3dd31-175">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dd31-176">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3dd31-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3dd31-177">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3dd31-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3dd31-178">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="3dd31-178">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="3dd31-179">Uma breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="3dd31-179">A short textual description of the object.</span></span>

<span data-ttu-id="3dd31-180">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3dd31-180">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3dd31-181">**Compactado**</span><span class="sxs-lookup"><span data-stu-id="3dd31-181">**Compressed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dd31-182">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="3dd31-182">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3dd31-183">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3dd31-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3dd31-184">Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("compactado")</span><span class="sxs-lookup"><span data-stu-id="3dd31-184">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Compressed")</span></span>
</dt> </dl>

<span data-ttu-id="3dd31-185">Se **for true**, o arquivo será compactado.</span><span class="sxs-lookup"><span data-stu-id="3dd31-185">If **True**, the file is compressed.</span></span>

<span data-ttu-id="3dd31-186">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="3dd31-186">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="3dd31-187">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="3dd31-187">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dd31-188">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3dd31-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3dd31-189">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3dd31-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3dd31-190">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("método de compactação")</span><span class="sxs-lookup"><span data-stu-id="3dd31-190">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Compression Method")</span></span>
</dt> </dl>

<span data-ttu-id="3dd31-191">Cadeia de caracteres de forma livre que indica o algoritmo ou a ferramenta usada para compactar o arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="3dd31-191">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="3dd31-192">Se o esquema de compactação for desconhecido ou não estiver descrito, use "desconhecido".</span><span class="sxs-lookup"><span data-stu-id="3dd31-192">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="3dd31-193">Se o arquivo lógico estiver compactado, mas o esquema de compactação for desconhecido ou não estiver descrito, use "compactado".</span><span class="sxs-lookup"><span data-stu-id="3dd31-193">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="3dd31-194">Se o arquivo lógico não estiver compactado, use "não compactado".</span><span class="sxs-lookup"><span data-stu-id="3dd31-194">If the logical file is not compressed, use "Not Compressed".</span></span>

<span data-ttu-id="3dd31-195">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="3dd31-195">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="3dd31-196">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="3dd31-196">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dd31-197">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3dd31-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3dd31-198">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3dd31-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3dd31-199">Qualificadores: [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("nome da classe")</span><span class="sxs-lookup"><span data-stu-id="3dd31-199">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="3dd31-200">Nome da classe.</span><span class="sxs-lookup"><span data-stu-id="3dd31-200">Name of the class.</span></span>

<span data-ttu-id="3dd31-201">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="3dd31-201">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="3dd31-202">**CreationDate**</span><span class="sxs-lookup"><span data-stu-id="3dd31-202">**CreationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dd31-203">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="3dd31-203">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3dd31-204">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3dd31-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3dd31-205">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("data de criação")</span><span class="sxs-lookup"><span data-stu-id="3dd31-205">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Creation Date")</span></span>
</dt> </dl>

<span data-ttu-id="3dd31-206">Data e hora da criação do arquivo.</span><span class="sxs-lookup"><span data-stu-id="3dd31-206">Date and time of the file's creation.</span></span>

<span data-ttu-id="3dd31-207">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="3dd31-207">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="3dd31-208">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="3dd31-208">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dd31-209">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3dd31-209">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3dd31-210">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3dd31-210">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3dd31-211">Qualificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ sistema de arquivos CIM**](cim-filesystem.md).**CSCreationClassName**"), [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" nome da classe do sistema de computador ")</span><span class="sxs-lookup"><span data-stu-id="3dd31-211">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSCreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Computer System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="3dd31-212">Classe do sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="3dd31-212">Class of the computer system.</span></span>

<span data-ttu-id="3dd31-213">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="3dd31-213">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="3dd31-214">**CSName**</span><span class="sxs-lookup"><span data-stu-id="3dd31-214">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dd31-215">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3dd31-215">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3dd31-216">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3dd31-216">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3dd31-217">Qualificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ sistema de arquivos CIM**](cim-filesystem.md).**CSName**"), [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" nome do sistema de computador ")</span><span class="sxs-lookup"><span data-stu-id="3dd31-217">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Computer System Name")</span></span>
</dt> </dl>

<span data-ttu-id="3dd31-218">Nome do sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="3dd31-218">Name of the computer system.</span></span>

<span data-ttu-id="3dd31-219">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="3dd31-219">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="3dd31-220">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="3dd31-220">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dd31-221">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3dd31-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3dd31-222">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3dd31-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3dd31-223">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="3dd31-223">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="3dd31-224">Uma descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="3dd31-224">A textual description of the object.</span></span>

<span data-ttu-id="3dd31-225">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3dd31-225">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3dd31-226">**Unidade**</span><span class="sxs-lookup"><span data-stu-id="3dd31-226">**Drive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dd31-227">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3dd31-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3dd31-228">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3dd31-228">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3dd31-229">Qualificadores: [**fixo**](../wmisdk/standard-wmi-qualifiers.md), [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("drive")</span><span class="sxs-lookup"><span data-stu-id="3dd31-229">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Drive")</span></span>
</dt> </dl>

<span data-ttu-id="3dd31-230">Letra da unidade (incluindo os dois-pontos que segue a letra da unidade) do arquivo.</span><span class="sxs-lookup"><span data-stu-id="3dd31-230">Drive letter (including the colon that follows the drive letter) of the file.</span></span> <span data-ttu-id="3dd31-231">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="3dd31-231">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="3dd31-232">Exemplo: "c:"</span><span class="sxs-lookup"><span data-stu-id="3dd31-232">Example: "c:"</span></span>

<span data-ttu-id="3dd31-233">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="3dd31-233">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="3dd31-234">**EightDotThreeFileName**</span><span class="sxs-lookup"><span data-stu-id="3dd31-234">**EightDotThreeFileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dd31-235">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3dd31-235">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3dd31-236">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3dd31-236">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3dd31-237">Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("oito pontos três nome de arquivo")</span><span class="sxs-lookup"><span data-stu-id="3dd31-237">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Eight Dot Three File Name")</span></span>
</dt> </dl>

<span data-ttu-id="3dd31-238">Nome de arquivo compatível com o DOS.</span><span class="sxs-lookup"><span data-stu-id="3dd31-238">DOS-compatible file name.</span></span>

<span data-ttu-id="3dd31-239">Exemplo: "c: \\ progra ~ 1"</span><span class="sxs-lookup"><span data-stu-id="3dd31-239">Example: "c:\\progra~1"</span></span>

<span data-ttu-id="3dd31-240">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="3dd31-240">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="3dd31-241">**Criptografado**</span><span class="sxs-lookup"><span data-stu-id="3dd31-241">**Encrypted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dd31-242">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="3dd31-242">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3dd31-243">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3dd31-243">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3dd31-244">Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Encrypted")</span><span class="sxs-lookup"><span data-stu-id="3dd31-244">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Encrypted")</span></span>
</dt> </dl>

<span data-ttu-id="3dd31-245">Se **for true**, o arquivo será criptografado.</span><span class="sxs-lookup"><span data-stu-id="3dd31-245">If **True**, the file is encrypted.</span></span>

<span data-ttu-id="3dd31-246">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="3dd31-246">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="3dd31-247">**EncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="3dd31-247">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dd31-248">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3dd31-248">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3dd31-249">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3dd31-249">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3dd31-250">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("método de criptografia")</span><span class="sxs-lookup"><span data-stu-id="3dd31-250">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Encryption Method")</span></span>
</dt> </dl>

<span data-ttu-id="3dd31-251">Cadeia de caracteres de forma livre que identifica o algoritmo ou a ferramenta usada para criptografar um arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="3dd31-251">Free-form string that identifies the algorithm or tool used to encrypt a logical file.</span></span> <span data-ttu-id="3dd31-252">Se o esquema de criptografia não for indulged (por motivos de segurança, por exemplo), use "desconhecido".</span><span class="sxs-lookup"><span data-stu-id="3dd31-252">If the encryption scheme is not indulged (for security reasons, for example), use "Unknown".</span></span> <span data-ttu-id="3dd31-253">Se o arquivo estiver criptografado, mas seu esquema de criptografia for desconhecido ou não for divulgado, use "Encrypted".</span><span class="sxs-lookup"><span data-stu-id="3dd31-253">If the file is encrypted, but either its encryption scheme is unknown or not disclosed, use "Encrypted".</span></span> <span data-ttu-id="3dd31-254">Se o arquivo lógico não estiver criptografado, use "não criptografado".</span><span class="sxs-lookup"><span data-stu-id="3dd31-254">If the logical file is not encrypted, use "Not Encrypted".</span></span>

<span data-ttu-id="3dd31-255">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="3dd31-255">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="3dd31-256">**Extensão**</span><span class="sxs-lookup"><span data-stu-id="3dd31-256">**Extension**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dd31-257">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3dd31-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3dd31-258">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3dd31-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3dd31-259">Qualificadores: [**fixo**](../wmisdk/standard-wmi-qualifiers.md), [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("extensão de arquivo")</span><span class="sxs-lookup"><span data-stu-id="3dd31-259">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File Extension")</span></span>
</dt> </dl>

<span data-ttu-id="3dd31-260">Extensão de nome de arquivo sem o ponto anterior (ponto).</span><span class="sxs-lookup"><span data-stu-id="3dd31-260">File name extension without the preceding period (dot).</span></span>

<span data-ttu-id="3dd31-261">Exemplo: "txt", "MOF", "mdb"</span><span class="sxs-lookup"><span data-stu-id="3dd31-261">Example: "txt", "mof", "mdb"</span></span>

<span data-ttu-id="3dd31-262">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="3dd31-262">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="3dd31-263">**FileName**</span><span class="sxs-lookup"><span data-stu-id="3dd31-263">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dd31-264">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3dd31-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3dd31-265">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3dd31-265">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3dd31-266">Qualificadores: [**fixo**](../wmisdk/standard-wmi-qualifiers.md), [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("nome do arquivo")</span><span class="sxs-lookup"><span data-stu-id="3dd31-266">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File Name")</span></span>
</dt> </dl>

<span data-ttu-id="3dd31-267">Nome do arquivo sem a extensão de nome de arquivo.</span><span class="sxs-lookup"><span data-stu-id="3dd31-267">File name without the file name extension.</span></span> <span data-ttu-id="3dd31-268">Exemplo: "mydatafile"</span><span class="sxs-lookup"><span data-stu-id="3dd31-268">Example: "MyDataFile"</span></span>

<span data-ttu-id="3dd31-269">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="3dd31-269">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="3dd31-270">**Tamanho**</span><span class="sxs-lookup"><span data-stu-id="3dd31-270">**FileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dd31-271">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3dd31-271">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3dd31-272">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3dd31-272">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3dd31-273">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("tamanho"), [**unidades**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="3dd31-273">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Size"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="3dd31-274">Tamanho do arquivo, em bytes.</span><span class="sxs-lookup"><span data-stu-id="3dd31-274">Size of the file, in bytes.</span></span>

<span data-ttu-id="3dd31-275">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3dd31-275">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="3dd31-276">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="3dd31-276">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="3dd31-277">**Talvez**</span><span class="sxs-lookup"><span data-stu-id="3dd31-277">**FileType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dd31-278">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3dd31-278">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3dd31-279">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3dd31-279">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3dd31-280">Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("tipo de arquivo")</span><span class="sxs-lookup"><span data-stu-id="3dd31-280">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File Type")</span></span>
</dt> </dl>

<span data-ttu-id="3dd31-281">Descritor que representa o tipo de arquivo indicado pela propriedade de **extensão** .</span><span class="sxs-lookup"><span data-stu-id="3dd31-281">Descriptor that represents the file type indicated by the **Extension** property.</span></span>

<span data-ttu-id="3dd31-282">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="3dd31-282">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="3dd31-283">**FreeSpace**</span><span class="sxs-lookup"><span data-stu-id="3dd31-283">**FreeSpace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dd31-284">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3dd31-284">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3dd31-285">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3dd31-285">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3dd31-286">Qualificadores: [**preteridos**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de gerenciamento de memória win32api \| [**MEMORYSTATUS**](/windows/win32/api/winbase/ns-winbase-memorystatus) \| dwAvailPageFile"), [**unidades**](../wmisdk/standard-qualifiers.md) ("megabytes")</span><span class="sxs-lookup"><span data-stu-id="3dd31-286">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Memory Management Structures\|[**MEMORYSTATUS**](/windows/win32/api/winbase/ns-winbase-memorystatus)\|dwAvailPageFile"), [**Units**](../wmisdk/standard-qualifiers.md) ("megabytes")</span></span>
</dt> </dl>

<span data-ttu-id="3dd31-287">Espaço disponível no arquivo de paginação.</span><span class="sxs-lookup"><span data-stu-id="3dd31-287">Space available in the paging file.</span></span> <span data-ttu-id="3dd31-288">O sistema operacional pode aumentar o arquivo de paginação conforme necessário, até o limite imposto pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="3dd31-288">The operating system can enlarge the paging file as necessary, up to the limit imposed by the user.</span></span> <span data-ttu-id="3dd31-289">Essa propriedade mostra a diferença entre o tamanho da memória confirmada atual e o tamanho atual do arquivo de paginação; Ele não mostra o maior tamanho possível do arquivo de paginação.</span><span class="sxs-lookup"><span data-stu-id="3dd31-289">This property shows the difference between the size of current committed memory and the current size of the paging file; it does not show the largest possible size of the paging file.</span></span>

</dd> <dt>

<span data-ttu-id="3dd31-290">**FSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="3dd31-290">**FSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dd31-291">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3dd31-291">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3dd31-292">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3dd31-292">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3dd31-293">Qualificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ sistema de arquivos CIM**](cim-filesystem.md).**CreationClassName**"), [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" nome da classe do sistema de arquivos ")</span><span class="sxs-lookup"><span data-stu-id="3dd31-293">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_FileSystem**](cim-filesystem.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="3dd31-294">Classe do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="3dd31-294">Class of the file system.</span></span>

<span data-ttu-id="3dd31-295">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="3dd31-295">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="3dd31-296">**FSName**</span><span class="sxs-lookup"><span data-stu-id="3dd31-296">**FSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dd31-297">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3dd31-297">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3dd31-298">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3dd31-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3dd31-299">Qualificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ sistema de arquivos CIM**](cim-filesystem.md).**Name**"), [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" nome do sistema de arquivos ")</span><span class="sxs-lookup"><span data-stu-id="3dd31-299">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_FileSystem**](cim-filesystem.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File System Name")</span></span>
</dt> </dl>

<span data-ttu-id="3dd31-300">Nome do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="3dd31-300">Name of the file system.</span></span>

<span data-ttu-id="3dd31-301">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="3dd31-301">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="3dd31-302">**Oculto**</span><span class="sxs-lookup"><span data-stu-id="3dd31-302">**Hidden**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dd31-303">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="3dd31-303">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3dd31-304">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3dd31-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3dd31-305">Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Hidden")</span><span class="sxs-lookup"><span data-stu-id="3dd31-305">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Hidden")</span></span>
</dt> </dl>

<span data-ttu-id="3dd31-306">Se for **true**, o arquivo ficará oculto.</span><span class="sxs-lookup"><span data-stu-id="3dd31-306">If **True**, the file is hidden.</span></span>

<span data-ttu-id="3dd31-307">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="3dd31-307">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="3dd31-308">**InitialSize**</span><span class="sxs-lookup"><span data-stu-id="3dd31-308">**InitialSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dd31-309">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3dd31-309">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3dd31-310">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3dd31-310">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3dd31-311">Qualificadores: [**preterido**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Regstry \| sistema \\ \\ CurrentControlSet \\ \\ Control \\ \\ Session Manager \\ \\ Memory Management \| PagingFiles"), [**unidades**](../wmisdk/standard-qualifiers.md) ("megabytes")</span><span class="sxs-lookup"><span data-stu-id="3dd31-311">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Regstry\|System\\\\CurrentControlSet\\\\Control\\\\Session Manager\\\\Memory Management\|PagingFiles"), [**Units**](../wmisdk/standard-qualifiers.md) ("megabytes")</span></span>
</dt> </dl>

<span data-ttu-id="3dd31-312">Tamanho inicial do arquivo de paginação.</span><span class="sxs-lookup"><span data-stu-id="3dd31-312">Initial size of the page file.</span></span>

</dd> <dt>

<span data-ttu-id="3dd31-313">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="3dd31-313">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dd31-314">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="3dd31-314">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3dd31-315">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3dd31-315">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3dd31-316">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="3dd31-316">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="3dd31-317">Indica quando o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="3dd31-317">Indicates when the object was installed.</span></span> <span data-ttu-id="3dd31-318">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="3dd31-318">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="3dd31-319">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3dd31-319">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3dd31-320">**InUseCount**</span><span class="sxs-lookup"><span data-stu-id="3dd31-320">**InUseCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dd31-321">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3dd31-321">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3dd31-322">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3dd31-322">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3dd31-323">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("contagem de abertura de arquivo atual")</span><span class="sxs-lookup"><span data-stu-id="3dd31-323">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Current File Open Count")</span></span>
</dt> </dl>

<span data-ttu-id="3dd31-324">Número de "aberturas de arquivo" que estão atualmente ativos no arquivo.</span><span class="sxs-lookup"><span data-stu-id="3dd31-324">Number of "file opens" that are currently active against the file.</span></span>

<span data-ttu-id="3dd31-325">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3dd31-325">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="3dd31-326">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="3dd31-326">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="3dd31-327">**LastAccessed**</span><span class="sxs-lookup"><span data-stu-id="3dd31-327">**LastAccessed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dd31-328">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="3dd31-328">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3dd31-329">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3dd31-329">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3dd31-330">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("último acesso")</span><span class="sxs-lookup"><span data-stu-id="3dd31-330">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Last Accessed")</span></span>
</dt> </dl>

<span data-ttu-id="3dd31-331">Data e hora do último acesso ao arquivo.</span><span class="sxs-lookup"><span data-stu-id="3dd31-331">Date and time the file was last accessed.</span></span>

<span data-ttu-id="3dd31-332">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="3dd31-332">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="3dd31-333">**LastModified**</span><span class="sxs-lookup"><span data-stu-id="3dd31-333">**LastModified**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dd31-334">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="3dd31-334">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3dd31-335">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3dd31-335">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3dd31-336">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("última modificação")</span><span class="sxs-lookup"><span data-stu-id="3dd31-336">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Last Modified")</span></span>
</dt> </dl>

<span data-ttu-id="3dd31-337">Data e hora da última modificação do arquivo.</span><span class="sxs-lookup"><span data-stu-id="3dd31-337">Date and time the file was last modified.</span></span>

<span data-ttu-id="3dd31-338">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="3dd31-338">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="3dd31-339">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="3dd31-339">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dd31-340">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3dd31-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3dd31-341">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3dd31-341">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3dd31-342">Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("fabricante")</span><span class="sxs-lookup"><span data-stu-id="3dd31-342">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Manufacturer")</span></span>
</dt> </dl>

<span data-ttu-id="3dd31-343">Cadeia de caracteres do fabricante do recurso de versão (se houver um).</span><span class="sxs-lookup"><span data-stu-id="3dd31-343">Manufacturer string from the version resource (if one is present).</span></span>

<span data-ttu-id="3dd31-344">Esta propriedade é herdada [**do \_ arquivo**](cim-datafile.md)de propriedades CIM.</span><span class="sxs-lookup"><span data-stu-id="3dd31-344">This property is inherited from [**CIM\_DataFile**](cim-datafile.md).</span></span>

</dd> <dt>

<span data-ttu-id="3dd31-345">**MaximumSize**</span><span class="sxs-lookup"><span data-stu-id="3dd31-345">**MaximumSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dd31-346">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3dd31-346">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3dd31-347">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3dd31-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3dd31-348">Qualificadores: [**preteridos**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de gerenciamento de memória win32api \| [**MEMORYSTATUS**](/windows/win32/api/winbase/ns-winbase-memorystatus) \| dwTotalPageFile"), [**unidades**](../wmisdk/standard-qualifiers.md) ("megabytes")</span><span class="sxs-lookup"><span data-stu-id="3dd31-348">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Memory Management Structures\|[**MEMORYSTATUS**](/windows/win32/api/winbase/ns-winbase-memorystatus)\|dwTotalPageFile"), [**units**](../wmisdk/standard-qualifiers.md) ("megabytes")</span></span>
</dt> </dl>

<span data-ttu-id="3dd31-349">Tamanho máximo do arquivo de paginação definido pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="3dd31-349">Maximum size of the page file as set by the user.</span></span> <span data-ttu-id="3dd31-350">O sistema operacional não permitirá que o arquivo de paginação exceda esse limite.</span><span class="sxs-lookup"><span data-stu-id="3dd31-350">The operating system will not allow the page file to exceed this limit.</span></span>

</dd> <dt>

<span data-ttu-id="3dd31-351">**Nome**</span><span class="sxs-lookup"><span data-stu-id="3dd31-351">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dd31-352">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3dd31-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3dd31-353">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3dd31-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3dd31-354">Qualificadores: [**preterido**](../wmisdk/standard-wmi-qualifiers.md), [**substituir**](../wmisdk/standard-qualifiers.md) ("nome"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32DLL \|NTDLL.DLL\| [**NtQuerySystemInformation**](/windows/win32/api/winternl/nf-winternl-ntquerysysteminformation) \| SystemPageFileInformation \| arquivo de paginaname")</span><span class="sxs-lookup"><span data-stu-id="3dd31-354">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32DLL\|NTDLL.DLL\|[**NtQuerySystemInformation**](/windows/win32/api/winternl/nf-winternl-ntquerysysteminformation)\|SystemPageFileInformation\|PageFileName")</span></span>
</dt> </dl>

<span data-ttu-id="3dd31-355">Nome do arquivo de paginação.</span><span class="sxs-lookup"><span data-stu-id="3dd31-355">Name of the page file.</span></span>

<span data-ttu-id="3dd31-356">Exemplo: "C: \\PAGEFILE.SYS"</span><span class="sxs-lookup"><span data-stu-id="3dd31-356">Example: "C:\\PAGEFILE.SYS"</span></span>

</dd> <dt>

<span data-ttu-id="3dd31-357">**Caminho**</span><span class="sxs-lookup"><span data-stu-id="3dd31-357">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dd31-358">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3dd31-358">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3dd31-359">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3dd31-359">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3dd31-360">Qualificadores: [**fixo**](../wmisdk/standard-wmi-qualifiers.md), [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Path")</span><span class="sxs-lookup"><span data-stu-id="3dd31-360">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Path")</span></span>
</dt> </dl>

<span data-ttu-id="3dd31-361">Caminho do arquivo, incluindo as barras invertidas à esquerda e à direita.</span><span class="sxs-lookup"><span data-stu-id="3dd31-361">Path of the file including the leading and trailing backslashes.</span></span>

<span data-ttu-id="3dd31-362">Exemplo: " \\ sistema do Windows \\ \\ "</span><span class="sxs-lookup"><span data-stu-id="3dd31-362">Example: "\\windows\\system\\"</span></span>

<span data-ttu-id="3dd31-363">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="3dd31-363">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="3dd31-364">**Seres**</span><span class="sxs-lookup"><span data-stu-id="3dd31-364">**Readable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dd31-365">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="3dd31-365">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3dd31-366">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3dd31-366">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3dd31-367">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("legível")</span><span class="sxs-lookup"><span data-stu-id="3dd31-367">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Readable")</span></span>
</dt> </dl>

<span data-ttu-id="3dd31-368">Se **for true**, o arquivo poderá ser lido.</span><span class="sxs-lookup"><span data-stu-id="3dd31-368">If **True**, the file can be read.</span></span>

<span data-ttu-id="3dd31-369">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="3dd31-369">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="3dd31-370">**Status**</span><span class="sxs-lookup"><span data-stu-id="3dd31-370">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dd31-371">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3dd31-371">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3dd31-372">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3dd31-372">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3dd31-373">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="3dd31-373">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="3dd31-374">Cadeia de caracteres que indica o status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="3dd31-374">String that indicates the current status of the object.</span></span>

<span data-ttu-id="3dd31-375">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3dd31-375">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="3dd31-376">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="3dd31-376">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="3dd31-377">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="3dd31-377">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="3dd31-378">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="3dd31-378">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="3dd31-379">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="3dd31-379">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3dd31-380">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="3dd31-380">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="3dd31-381">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="3dd31-381">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="3dd31-382">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="3dd31-382">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="3dd31-383">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="3dd31-383">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="3dd31-384">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="3dd31-384">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="3dd31-385">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="3dd31-385">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="3dd31-386">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="3dd31-386">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="3dd31-387">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="3dd31-387">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="3dd31-388">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="3dd31-388">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3dd31-389">**System**</span><span class="sxs-lookup"><span data-stu-id="3dd31-389">**System**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dd31-390">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="3dd31-390">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3dd31-391">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3dd31-391">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3dd31-392">Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("arquivo do sistema")</span><span class="sxs-lookup"><span data-stu-id="3dd31-392">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("System File")</span></span>
</dt> </dl>

<span data-ttu-id="3dd31-393">Se for **true**, o arquivo será um arquivo do sistema.</span><span class="sxs-lookup"><span data-stu-id="3dd31-393">If **True**, the file is a system file.</span></span>

<span data-ttu-id="3dd31-394">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="3dd31-394">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="3dd31-395">**Versão**</span><span class="sxs-lookup"><span data-stu-id="3dd31-395">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dd31-396">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3dd31-396">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3dd31-397">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3dd31-397">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3dd31-398">Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Version")</span><span class="sxs-lookup"><span data-stu-id="3dd31-398">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Version")</span></span>
</dt> </dl>

<span data-ttu-id="3dd31-399">Cadeia de caracteres da versão do recurso de versão (se houver uma).</span><span class="sxs-lookup"><span data-stu-id="3dd31-399">Version string from the version resource (if one is present).</span></span>

<span data-ttu-id="3dd31-400">Esta propriedade é herdada [**do \_ arquivo**](cim-datafile.md)de propriedades CIM.</span><span class="sxs-lookup"><span data-stu-id="3dd31-400">This property is inherited from [**CIM\_DataFile**](cim-datafile.md).</span></span>

</dd> <dt>

<span data-ttu-id="3dd31-401">**Gravável**</span><span class="sxs-lookup"><span data-stu-id="3dd31-401">**Writeable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dd31-402">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="3dd31-402">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3dd31-403">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3dd31-403">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3dd31-404">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("gravável")</span><span class="sxs-lookup"><span data-stu-id="3dd31-404">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Writeable")</span></span>
</dt> </dl>

<span data-ttu-id="3dd31-405">Se **for true**, o arquivo poderá ser gravado.</span><span class="sxs-lookup"><span data-stu-id="3dd31-405">If **True**, the file can be written.</span></span>

<span data-ttu-id="3dd31-406">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="3dd31-406">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3dd31-407">Comentários</span><span class="sxs-lookup"><span data-stu-id="3dd31-407">Remarks</span></span>

<span data-ttu-id="3dd31-408">A classe de **\_ arquivo de paginação Win32** é derivada do [**\_ diretório CIM**](cim-directory.md).</span><span class="sxs-lookup"><span data-stu-id="3dd31-408">The **Win32\_PageFile** class is derived from [**CIM\_Directory**](cim-directory.md).</span></span>

## <a name="examples"></a><span data-ttu-id="3dd31-409">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3dd31-409">Examples</span></span>

<span data-ttu-id="3dd31-410">O exemplo de código VBScript a seguir demonstra como recuperar estatísticas de arquivos de paginação de instâncias do arquivo de **\_ paginação Win32**.</span><span class="sxs-lookup"><span data-stu-id="3dd31-410">The following VBScript code sample demonstrates how to retrieve page file stats from instances of **Win32\_PageFile**.</span></span>


```VB
Set PageFileSet = GetObject("winmgmts:").InstancesOf ("Win32_PageFile")

for each PageFile in PageFileSet
 WScript.Echo PageFile.Name & Chr(13) 
 WScript.Echo " Initial: " & PageFile.InitialSize & " MB"
 WScript.Echo " Max: " & PageFile.MaximumSize & " MB" 

next
```



<span data-ttu-id="3dd31-411">O exemplo de código Perl a seguir demonstra como recuperar estatísticas de arquivos de paginação de instâncias do arquivo de **\_ paginação Win32**.</span><span class="sxs-lookup"><span data-stu-id="3dd31-411">The following Perl code sample demonstrates how to retrieve page file stats from instances of **Win32\_PageFile**.</span></span>


```
use strict;
use Win32::OLE;

my $PageFileSet;

eval { $PageFileSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
 InstancesOf ("Win32_PageFile"); };
if (!$@ && defined $PageFileSet)
{
 foreach my $PageFileInst (in $PageFileSet)
 {
  print "\n$PageFileInst->{Name}\n";
  print " Initial: $PageFileInst->{InitialSize} MB\n";
  print " Maximum: $PageFileInst->{MaximumSize} MB\n";
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="3dd31-412">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3dd31-412">Requirements</span></span>



| <span data-ttu-id="3dd31-413">Requisito</span><span class="sxs-lookup"><span data-stu-id="3dd31-413">Requirement</span></span> | <span data-ttu-id="3dd31-414">Valor</span><span class="sxs-lookup"><span data-stu-id="3dd31-414">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3dd31-415">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3dd31-415">Minimum supported client</span></span><br/> | <span data-ttu-id="3dd31-416">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3dd31-416">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3dd31-417">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3dd31-417">Minimum supported server</span></span><br/> | <span data-ttu-id="3dd31-418">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3dd31-418">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3dd31-419">Namespace</span><span class="sxs-lookup"><span data-stu-id="3dd31-419">Namespace</span></span><br/>                | <span data-ttu-id="3dd31-420">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="3dd31-420">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3dd31-421">MOF</span><span class="sxs-lookup"><span data-stu-id="3dd31-421">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3dd31-422"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3dd31-422"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3dd31-423">DLL</span><span class="sxs-lookup"><span data-stu-id="3dd31-423">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3dd31-424"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3dd31-424"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3dd31-425">Confira também</span><span class="sxs-lookup"><span data-stu-id="3dd31-425">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3dd31-426">**DataFile de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="3dd31-426">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="3dd31-427">Classes do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="3dd31-427">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
