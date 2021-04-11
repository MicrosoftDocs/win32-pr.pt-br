---
description: O \_ diretório Win32&\# 32; A classe WMI representa uma entrada de diretório em um sistema de computador que executa o Windows.
ms.assetid: d61cb5ee-8e87-4604-95e6-325c9b543411
ms.tgt_platform: multiple
title: Classe Win32_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory
- Win32_Directory.Caption
- Win32_Directory.Description
- Win32_Directory.InstallDate
- Win32_Directory.Name
- Win32_Directory.Status
- Win32_Directory.AccessMask
- Win32_Directory.Archive
- Win32_Directory.Compressed
- Win32_Directory.CompressionMethod
- Win32_Directory.CreationClassName
- Win32_Directory.CreationDate
- Win32_Directory.CSCreationClassName
- Win32_Directory.CSName
- Win32_Directory.Drive
- Win32_Directory.EightDotThreeFileName
- Win32_Directory.Encrypted
- Win32_Directory.EncryptionMethod
- Win32_Directory.Extension
- Win32_Directory.FileName
- Win32_Directory.FileSize
- Win32_Directory.FileType
- Win32_Directory.FSCreationClassName
- Win32_Directory.FSName
- Win32_Directory.Hidden
- Win32_Directory.InUseCount
- Win32_Directory.LastAccessed
- Win32_Directory.LastModified
- Win32_Directory.Path
- Win32_Directory.Readable
- Win32_Directory.System
- Win32_Directory.Writeable
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6185b9c0d427b7410d36f3fddfaf70c0ed8d364b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164123"
---
# <a name="win32_directory-class"></a><span data-ttu-id="759a5-103">\_Classe de diretório Win32</span><span class="sxs-lookup"><span data-stu-id="759a5-103">Win32\_Directory class</span></span>

<span data-ttu-id="759a5-104">A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de **\_ diretório do Win32** representa uma entrada de diretório em um sistema de computador executando o Windows.</span><span class="sxs-lookup"><span data-stu-id="759a5-104">The **Win32\_Directory** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a directory entry on a computer system running Windows.</span></span> <span data-ttu-id="759a5-105">Um diretório é um tipo de arquivo que agrupa logicamente os arquivos de dados e fornece informações de caminho para os arquivos agrupados.</span><span class="sxs-lookup"><span data-stu-id="759a5-105">A directory is a type of file that logically groups data files and provides path information for the grouped files.</span></span> <span data-ttu-id="759a5-106">Exemplo: C: \\ Temp.</span><span class="sxs-lookup"><span data-stu-id="759a5-106">Example: C:\\TEMP.</span></span> <span data-ttu-id="759a5-107">**Win32 \_ O diretório** não inclui diretórios de unidades de rede.</span><span class="sxs-lookup"><span data-stu-id="759a5-107">**Win32\_Directory** does not include directories of network drives.</span></span>

<span data-ttu-id="759a5-108">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="759a5-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="759a5-109">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="759a5-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="759a5-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="759a5-110">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4C7-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_Directory : CIM_Directory
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
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

## <a name="members"></a><span data-ttu-id="759a5-111">Membros</span><span class="sxs-lookup"><span data-stu-id="759a5-111">Members</span></span>

<span data-ttu-id="759a5-112">A classe do **\_ diretório Win32** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="759a5-112">The **Win32\_Directory** class has these types of members:</span></span>

-   [<span data-ttu-id="759a5-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="759a5-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="759a5-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="759a5-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="759a5-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="759a5-115">Methods</span></span>

<span data-ttu-id="759a5-116">A classe de **\_ diretório Win32** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="759a5-116">The **Win32\_Directory** class has these methods.</span></span>



| <span data-ttu-id="759a5-117">Método</span><span class="sxs-lookup"><span data-stu-id="759a5-117">Method</span></span>                                                                                             | <span data-ttu-id="759a5-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="759a5-118">Description</span></span>                                                                                                                                                                                                                             |
|:---------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="759a5-119">**ChangeSecurityPermissions**</span><span class="sxs-lookup"><span data-stu-id="759a5-119">**ChangeSecurityPermissions**</span></span>](changesecuritypermissions-method-in-class-win32-directory.md)     | <span data-ttu-id="759a5-120">Método de classe que altera as permissões de segurança para o arquivo lógico especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="759a5-120">Class method that changes the security permissions for the logical file specified in the object path.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="759a5-121">**ChangeSecurityPermissionsEx**</span><span class="sxs-lookup"><span data-stu-id="759a5-121">**ChangeSecurityPermissionsEx**</span></span>](changesecuritypermissionsex-method-in-class-win32-directory.md) | <span data-ttu-id="759a5-122">Método de classe que altera as permissões de segurança para o arquivo lógico especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="759a5-122">Class method that changes the security permissions for the logical file specified in the object path.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="759a5-123">**Compactar**</span><span class="sxs-lookup"><span data-stu-id="759a5-123">**Compress**</span></span>](compress-method-in-class-win32-directory.md)                                       | <span data-ttu-id="759a5-124">Método de classe que compacta o arquivo lógico (ou diretório) especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="759a5-124">Class method that compresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="759a5-125">**CompressEx**</span><span class="sxs-lookup"><span data-stu-id="759a5-125">**CompressEx**</span></span>](compressex-method-in-class-win32-directory.md)                                   | <span data-ttu-id="759a5-126">Método de classe que compacta o arquivo lógico (ou diretório) especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="759a5-126">Class method that compresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="759a5-127">**Copiar**</span><span class="sxs-lookup"><span data-stu-id="759a5-127">**Copy**</span></span>](copy-method-in-class-win32-directory.md)                                               | <span data-ttu-id="759a5-128">Método de classe que copia o arquivo ou diretório lógico especificado no caminho do objeto para o local especificado pelo parâmetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="759a5-128">Class method that copies the logical file or directory specified in the object path to the location specified by the input parameter.</span></span><br/>                                                                                        |
| [<span data-ttu-id="759a5-129">**CopyEx**</span><span class="sxs-lookup"><span data-stu-id="759a5-129">**CopyEx**</span></span>](copyex-method-in-class-win32-directory.md)                                           | <span data-ttu-id="759a5-130">Método de classe que copia o arquivo ou diretório lógico especificado no caminho do objeto para o local especificado pelo parâmetro *filename* .</span><span class="sxs-lookup"><span data-stu-id="759a5-130">Class method that copies the logical file or directory specified in the object path to the location specified by the *FileName* parameter.</span></span><br/>                                                                                   |
| [<span data-ttu-id="759a5-131">**Excluir**</span><span class="sxs-lookup"><span data-stu-id="759a5-131">**Delete**</span></span>](delete-method-in-class-win32-directory.md)                                           | <span data-ttu-id="759a5-132">Método de classe que exclui o arquivo lógico (ou diretório) especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="759a5-132">Class method that deletes the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                      |
| [<span data-ttu-id="759a5-133">**DeleteEx**</span><span class="sxs-lookup"><span data-stu-id="759a5-133">**DeleteEx**</span></span>](deleteex-method-in-class-win32-directory.md)                                       | <span data-ttu-id="759a5-134">Método de classe que exclui o arquivo lógico (ou diretório) especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="759a5-134">Class method that deletes the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                      |
| [<span data-ttu-id="759a5-135">**GetEffectivePermission**</span><span class="sxs-lookup"><span data-stu-id="759a5-135">**GetEffectivePermission**</span></span>](geteffectivepermission-method-in-class-win32-directory.md)           | <span data-ttu-id="759a5-136">Método de classe que determina se o chamador tem as permissões agregadas especificadas pelo argumento *Permissions* não apenas no objeto File, mas no compartilhamento o arquivo ou diretório reside (se estiver em um compartilhamento).</span><span class="sxs-lookup"><span data-stu-id="759a5-136">Class method that determines whether the caller has the aggregated permissions specified by the *Permissions* argument not only on the file object, but on the share the file or directory resides on (if it is on a share).</span></span><br/> |
| [<span data-ttu-id="759a5-137">**Renomear**</span><span class="sxs-lookup"><span data-stu-id="759a5-137">**Rename**</span></span>](rename-method-in-class-win32-directory.md)                                           | <span data-ttu-id="759a5-138">Método de classe que renomeia o arquivo lógico (ou diretório) especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="759a5-138">Class method that renames the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                      |
| [<span data-ttu-id="759a5-139">**TakeOwnerShip**</span><span class="sxs-lookup"><span data-stu-id="759a5-139">**TakeOwnerShip**</span></span>](takeownership-method-in-class-win32-directory.md)                             | <span data-ttu-id="759a5-140">Método de classe que obtém a propriedade do arquivo lógico especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="759a5-140">Class method that obtains ownership of the logical file specified in the object path.</span></span><br/>                                                                                                                                        |
| [<span data-ttu-id="759a5-141">**TakeOwnerShipEx**</span><span class="sxs-lookup"><span data-stu-id="759a5-141">**TakeOwnerShipEx**</span></span>](takeownershipex-method-in-class-win32-directory.md)                         | <span data-ttu-id="759a5-142">Método de classe que obtém a propriedade do arquivo lógico especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="759a5-142">Class method that obtains ownership of the logical file specified in the object path.</span></span><br/>                                                                                                                                        |
| [<span data-ttu-id="759a5-143">**Descompactar**</span><span class="sxs-lookup"><span data-stu-id="759a5-143">**Uncompress**</span></span>](uncompress-method-in-class-win32-directory.md)                                   | <span data-ttu-id="759a5-144">Método de classe que descompacta o arquivo lógico (ou diretório) especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="759a5-144">Class method that uncompresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                 |
| [<span data-ttu-id="759a5-145">**UncompressEx**</span><span class="sxs-lookup"><span data-stu-id="759a5-145">**UncompressEx**</span></span>](uncompressex-method-in-class-win32-directory.md)                               | <span data-ttu-id="759a5-146">Método de classe que descompacta o arquivo lógico (ou diretório) especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="759a5-146">Class method that uncompresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                 |



 

### <a name="properties"></a><span data-ttu-id="759a5-147">Propriedades</span><span class="sxs-lookup"><span data-stu-id="759a5-147">Properties</span></span>

<span data-ttu-id="759a5-148">A classe de **\_ diretório Win32** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="759a5-148">The **Win32\_Directory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="759a5-149">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="759a5-149">**AccessMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="759a5-150">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="759a5-150">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="759a5-151">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="759a5-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="759a5-152">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("direitos de acesso")</span><span class="sxs-lookup"><span data-stu-id="759a5-152">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Access Rights")</span></span>
</dt> </dl>

<span data-ttu-id="759a5-153">Bitmask que representa os direitos de acesso necessários para acessar ou executar operações específicas no diretório.</span><span class="sxs-lookup"><span data-stu-id="759a5-153">Bitmask that represents the access rights required to access or perform specific operations on the directory.</span></span> <span data-ttu-id="759a5-154">Para valores de bit, consulte [**constantes de direitos de acesso de arquivo e diretório**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants).</span><span class="sxs-lookup"><span data-stu-id="759a5-154">For bit values, see [**File and Directory Access Rights Constants**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants).</span></span>

> [!Note]  
> <span data-ttu-id="759a5-155">Em volumes FAT, o valor de **\_ acesso completo** é retornado, o que indica que nenhuma segurança foi definida no objeto.</span><span class="sxs-lookup"><span data-stu-id="759a5-155">On FAT volumes, the **FULL\_ACCESS** value is returned instead, which indicates no security has been set on the object.</span></span>

 

<span data-ttu-id="759a5-156">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="759a5-156">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="759a5-157"><span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>Do **arquivo \_ LER \_ os dados (arquivo) ou \_ \_ diretório de lista de arquivos (diretório)** (1)</span><span class="sxs-lookup"><span data-stu-id="759a5-157"><span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>**FILE\_READ\_DATA (file) or FILE\_LIST\_DIRECTORY (directory)** (1)</span></span>


</dt> <dd>

<span data-ttu-id="759a5-158">Concede o direito de ler dados do arquivo.</span><span class="sxs-lookup"><span data-stu-id="759a5-158">Grants the right to read data from the file.</span></span> <span data-ttu-id="759a5-159">Para um diretório, esse valor concede o direito de listar o conteúdo do diretório.</span><span class="sxs-lookup"><span data-stu-id="759a5-159">For a directory, this value grants the right to list the contents of the directory.</span></span>

</dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="759a5-160"><span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>Do **arquivo \_ GRAVAR \_ dados (arquivo) ou arquivo \_ Adicionar \_ arquivo (diretório)** (2)</span><span class="sxs-lookup"><span data-stu-id="759a5-160"><span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>**FILE\_WRITE\_DATA (file) or FILE\_ADD\_FILE (directory)** (2)</span></span>


</dt> <dd>

<span data-ttu-id="759a5-161">Concede o direito de gravar dados no arquivo.</span><span class="sxs-lookup"><span data-stu-id="759a5-161">Grants the right to write data to the file.</span></span> <span data-ttu-id="759a5-162">Para um diretório, esse valor concede o direito de criar um arquivo no diretório.</span><span class="sxs-lookup"><span data-stu-id="759a5-162">For a directory, this value grants the right to create a file in the directory.</span></span>

</dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY"></span><span id="file_append_data__file__or_file_add_subdirectory"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY"></span>

<span data-ttu-id="759a5-163"><span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY"></span><span id="file_append_data__file__or_file_add_subdirectory"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY"></span>Do **arquivo \_ ACRESCENTAR \_ dados (arquivo) ou arquivo \_ Adicionar \_ subdiretório** (4)</span><span class="sxs-lookup"><span data-stu-id="759a5-163"><span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY"></span><span id="file_append_data__file__or_file_add_subdirectory"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY"></span>**FILE\_APPEND\_DATA (file) or FILE\_ADD\_SUBDIRECTORY** (4)</span></span>


</dt> <dd>

<span data-ttu-id="759a5-164">Concede o direito de acrescentar dados ao arquivo.</span><span class="sxs-lookup"><span data-stu-id="759a5-164">Grants the right to append data to the file.</span></span> <span data-ttu-id="759a5-165">Para um diretório, esse valor concede o direito de criar um subdiretório.</span><span class="sxs-lookup"><span data-stu-id="759a5-165">For a directory, this value grants the right to create a subdirectory.</span></span>

</dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="759a5-166"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>Do **arquivo \_ LER \_ ea** (8)</span><span class="sxs-lookup"><span data-stu-id="759a5-166"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**FILE\_READ\_EA** (8)</span></span>


</dt> <dd>

<span data-ttu-id="759a5-167">Concede o direito de ler atributos estendidos.</span><span class="sxs-lookup"><span data-stu-id="759a5-167">Grants the right to read extended attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="759a5-168"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>Do **arquivo \_ GRAVAR \_ ea** (16)</span><span class="sxs-lookup"><span data-stu-id="759a5-168"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**FILE\_WRITE\_EA** (16)</span></span>


</dt> <dd>

<span data-ttu-id="759a5-169">Concede o direito de gravar atributos estendidos.</span><span class="sxs-lookup"><span data-stu-id="759a5-169">Grants the right to write extended attributes.</span></span>

</dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

<span data-ttu-id="759a5-170"><span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>Do **arquivo \_ EXECUTAR (arquivo) ou \_ atravessamento de arquivo (diretório)** (32)</span><span class="sxs-lookup"><span data-stu-id="759a5-170"><span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>**FILE\_EXECUTE (file) or FILE\_TRAVERSE (directory)** (32)</span></span>


</dt> <dd>

<span data-ttu-id="759a5-171">Concede o direito de executar um arquivo.</span><span class="sxs-lookup"><span data-stu-id="759a5-171">Grants the right to execute a file.</span></span> <span data-ttu-id="759a5-172">Para um diretório, o diretório pode ser atravessado.</span><span class="sxs-lookup"><span data-stu-id="759a5-172">For a directory, the directory can be traversed.</span></span>

</dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="759a5-173"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>Do **arquivo \_ EXCLUIR \_ filho (diretório)** (64)</span><span class="sxs-lookup"><span data-stu-id="759a5-173"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**FILE\_DELETE\_CHILD (directory)** (64)</span></span>


</dt> <dd>

<span data-ttu-id="759a5-174">Concede o direito de excluir um diretório e todos os arquivos que ele contém (seus filhos), mesmo que os arquivos sejam somente leitura.</span><span class="sxs-lookup"><span data-stu-id="759a5-174">Grants the right to delete a directory and all of the files it contains (its children), even if the files are read-only.</span></span>

</dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="759a5-175"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>Do **arquivo \_ \_Atributos de leitura** (128)</span><span class="sxs-lookup"><span data-stu-id="759a5-175"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**FILE\_READ\_ATTRIBUTES** (128)</span></span>


</dt> <dd>

<span data-ttu-id="759a5-176">Concede o direito de ler atributos de arquivo.</span><span class="sxs-lookup"><span data-stu-id="759a5-176">Grants the right to read file attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="759a5-177"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>Do **arquivo \_ \_Atributos de gravação** (256)</span><span class="sxs-lookup"><span data-stu-id="759a5-177"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**FILE\_WRITE\_ATTRIBUTES** (256)</span></span>


</dt> <dd>

<span data-ttu-id="759a5-178">Concede o direito de alterar atributos de arquivo.</span><span class="sxs-lookup"><span data-stu-id="759a5-178">Grants the right to change file attributes.</span></span>

</dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="759a5-179"><span id="DELETE"></span><span id="delete"></span>**Excluir** (65536)</span><span class="sxs-lookup"><span data-stu-id="759a5-179"><span id="DELETE"></span><span id="delete"></span>**DELETE** (65536)</span></span>


</dt> <dd>

<span data-ttu-id="759a5-180">Concede acesso de exclusão.</span><span class="sxs-lookup"><span data-stu-id="759a5-180">Grants delete access.</span></span>

</dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="759a5-181"><span id="READ_CONTROL"></span><span id="read_control"></span>**Ler \_ CONTROLE** (131072)</span><span class="sxs-lookup"><span data-stu-id="759a5-181"><span id="READ_CONTROL"></span><span id="read_control"></span>**READ\_CONTROL** (131072)</span></span>


</dt> <dd>

<span data-ttu-id="759a5-182">Concede acesso de leitura ao descritor de segurança e ao proprietário.</span><span class="sxs-lookup"><span data-stu-id="759a5-182">Grants read access to the security descriptor and owner.</span></span>

</dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="759a5-183"><span id="WRITE_DAC"></span><span id="write_dac"></span>**Gravar \_ DAC** (262144)</span><span class="sxs-lookup"><span data-stu-id="759a5-183"><span id="WRITE_DAC"></span><span id="write_dac"></span>**WRITE\_DAC** (262144)</span></span>


</dt> <dd>

<span data-ttu-id="759a5-184">Concede acesso de gravação à ACL discricionária.</span><span class="sxs-lookup"><span data-stu-id="759a5-184">Grants write access to the discretionary ACL.</span></span>

</dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="759a5-185"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**Gravar \_ PROPRIETÁRIO** (524288)</span><span class="sxs-lookup"><span data-stu-id="759a5-185"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**WRITE\_OWNER** (524288)</span></span>


</dt> <dd>

<span data-ttu-id="759a5-186">Atribui o proprietário da gravação.</span><span class="sxs-lookup"><span data-stu-id="759a5-186">Assigns the write owner.</span></span>

</dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="759a5-187"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**Sincronizar** (1048576)</span><span class="sxs-lookup"><span data-stu-id="759a5-187"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**SYNCHRONIZE** (1048576)</span></span>


</dt> <dd>

<span data-ttu-id="759a5-188">Sincroniza o acesso e permite que um processo Aguarde um objeto para entrar no estado sinalizado.</span><span class="sxs-lookup"><span data-stu-id="759a5-188">Synchronizes access and allows a process to wait for an object to enter the signaled state.</span></span>

</dd> <dt>

<span id="ACCESS_SYSTEM_SECURITY"></span><span id="access_system_security"></span>

<span data-ttu-id="759a5-189"><span id="ACCESS_SYSTEM_SECURITY"></span><span id="access_system_security"></span>**Acesso \_ ao \_Segurança do sistema** (18809343)</span><span class="sxs-lookup"><span data-stu-id="759a5-189"><span id="ACCESS_SYSTEM_SECURITY"></span><span id="access_system_security"></span>**ACCESS\_SYSTEM\_SECURITY** (18809343)</span></span>


</dt> <dd>

<span data-ttu-id="759a5-190">Controla a capacidade de obter ou definir a SACL no descritor de segurança de um objeto.</span><span class="sxs-lookup"><span data-stu-id="759a5-190">Controls the ability to get or set the SACL in an object's security descriptor.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="759a5-191">**Arquivar**</span><span class="sxs-lookup"><span data-stu-id="759a5-191">**Archive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="759a5-192">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="759a5-192">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="759a5-193">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="759a5-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="759a5-194">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("deve ser arquivado")</span><span class="sxs-lookup"><span data-stu-id="759a5-194">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Should Be Archived")</span></span>
</dt> </dl>

<span data-ttu-id="759a5-195">Indica se o bit de arquivo na pasta foi definido.</span><span class="sxs-lookup"><span data-stu-id="759a5-195">Indicates whether the archive bit on the folder has been set.</span></span> <span data-ttu-id="759a5-196">O bit de arquivo é usado pelos programas de backup para identificar os arquivos cujo backup deve ser feito.</span><span class="sxs-lookup"><span data-stu-id="759a5-196">The archive bit is used by backup programs to identify files that should be backed up.</span></span> <span data-ttu-id="759a5-197">Se **for true**, o arquivo deverá ser arquivado.</span><span class="sxs-lookup"><span data-stu-id="759a5-197">If **True**, the file should be archived.</span></span>

<span data-ttu-id="759a5-198">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="759a5-198">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="759a5-199">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="759a5-199">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="759a5-200">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="759a5-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="759a5-201">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="759a5-201">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="759a5-202">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="759a5-202">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="759a5-203">Uma breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="759a5-203">A short textual description of the object.</span></span>

<span data-ttu-id="759a5-204">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="759a5-204">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="759a5-205">**Compactado**</span><span class="sxs-lookup"><span data-stu-id="759a5-205">**Compressed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="759a5-206">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="759a5-206">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="759a5-207">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="759a5-207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="759a5-208">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("compactado")</span><span class="sxs-lookup"><span data-stu-id="759a5-208">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compressed")</span></span>
</dt> </dl>

<span data-ttu-id="759a5-209">Indica se a pasta foi compactada ou não.</span><span class="sxs-lookup"><span data-stu-id="759a5-209">Indicates whether or not the folder has been compressed.</span></span> <span data-ttu-id="759a5-210">O WMI reconhece pastas compactadas usando o próprio WMI ou usando a interface gráfica do usuário; no entanto, ele não reconhece. Arquivos ZIP como compactados.</span><span class="sxs-lookup"><span data-stu-id="759a5-210">WMI recognizes folders compressed using WMI itself or using the graphical user interface; it does not, however, recognize .ZIP files as being compressed.</span></span> <span data-ttu-id="759a5-211">Se **for true**, o arquivo será compactado.</span><span class="sxs-lookup"><span data-stu-id="759a5-211">If **True**, the file is compressed.</span></span>

<span data-ttu-id="759a5-212">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="759a5-212">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="759a5-213">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="759a5-213">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="759a5-214">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="759a5-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="759a5-215">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="759a5-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="759a5-216">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("método de compactação")</span><span class="sxs-lookup"><span data-stu-id="759a5-216">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compression Method")</span></span>
</dt> </dl>

<span data-ttu-id="759a5-217">Algoritmo ou ferramenta (geralmente um método) usado para compactar o arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="759a5-217">Algorithm or tool (usually a method) used to compress the logical file.</span></span> <span data-ttu-id="759a5-218">Se não for possível (ou não desejar) descrever o esquema de compactação (talvez porque não seja conhecido), use as seguintes palavras: "desconhecido" para representar que não é conhecido se o arquivo lógico está compactado; "Compactado" para representar que o arquivo está compactado, mas o esquema de compactação não é conhecido ou não é divulgado; e "não compactado" para representar que o arquivo lógico não está compactado.</span><span class="sxs-lookup"><span data-stu-id="759a5-218">If it is not possible (or not desired) to describe the compression scheme (perhaps because it is not known), use the following words: "Unknown" to represent that it is not known whether the logical file is compressed; "Compressed" to represent that the file is compressed, but either its compression scheme is not known or not disclosed; and "Not Compressed" to represent that the logical file is not compressed.</span></span>

<span data-ttu-id="759a5-219">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="759a5-219">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="759a5-220">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="759a5-220">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="759a5-221">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="759a5-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="759a5-222">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="759a5-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="759a5-223">Qualificadores: [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nome da classe")</span><span class="sxs-lookup"><span data-stu-id="759a5-223">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="759a5-224">Nome da primeira classe concreta a ser exibida na cadeia de herança usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="759a5-224">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="759a5-225">Quando usado com as outras propriedades de chave da classe, essa propriedade permite que todas as instâncias dessa classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="759a5-225">When used with the other key properties of the class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="759a5-226">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="759a5-226">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="759a5-227">**CreationDate**</span><span class="sxs-lookup"><span data-stu-id="759a5-227">**CreationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="759a5-228">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="759a5-228">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="759a5-229">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="759a5-229">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="759a5-230">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("data de criação")</span><span class="sxs-lookup"><span data-stu-id="759a5-230">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Creation Date")</span></span>
</dt> </dl>

<span data-ttu-id="759a5-231">Data em que o objeto do sistema de arquivos foi criado.</span><span class="sxs-lookup"><span data-stu-id="759a5-231">Date that the file system object was created.</span></span> <span data-ttu-id="759a5-232">Para obter mais informações sobre como trabalhar com formatos de data e hora do WMI, consulte [tarefas do WMI: datas e horas](/windows/desktop/WmiSdk/wmi-tasks--dates-and-times).</span><span class="sxs-lookup"><span data-stu-id="759a5-232">For more information on working with WMI date and time formats, see [WMI Tasks: Dates and Times](/windows/desktop/WmiSdk/wmi-tasks--dates-and-times).</span></span>

<span data-ttu-id="759a5-233">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="759a5-233">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="759a5-234">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="759a5-234">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="759a5-235">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="759a5-235">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="759a5-236">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="759a5-236">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="759a5-237">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema de arquivos CIM**](cim-filesystem.md).**CSCreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome da classe do sistema de computador ")</span><span class="sxs-lookup"><span data-stu-id="759a5-237">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSCreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="759a5-238">Nome da classe de criação do sistema de computador de escopo.</span><span class="sxs-lookup"><span data-stu-id="759a5-238">Creation class name of the scoping computer system.</span></span>

<span data-ttu-id="759a5-239">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="759a5-239">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="759a5-240">**CSName**</span><span class="sxs-lookup"><span data-stu-id="759a5-240">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="759a5-241">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="759a5-241">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="759a5-242">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="759a5-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="759a5-243">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema de arquivos CIM**](cim-filesystem.md).**CSName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome do sistema de computador ")</span><span class="sxs-lookup"><span data-stu-id="759a5-243">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Name")</span></span>
</dt> </dl>

<span data-ttu-id="759a5-244">Nome do computador em que o objeto do sistema de arquivos está armazenado.</span><span class="sxs-lookup"><span data-stu-id="759a5-244">Name of the computer where the file system object is stored.</span></span>

<span data-ttu-id="759a5-245">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="759a5-245">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="759a5-246">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="759a5-246">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="759a5-247">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="759a5-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="759a5-248">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="759a5-248">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="759a5-249">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="759a5-249">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="759a5-250">Uma descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="759a5-250">A textual description of the object.</span></span>

<span data-ttu-id="759a5-251">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="759a5-251">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="759a5-252">**Unidade**</span><span class="sxs-lookup"><span data-stu-id="759a5-252">**Drive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="759a5-253">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="759a5-253">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="759a5-254">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="759a5-254">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="759a5-255">Qualificadores: [**fixo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("drive")</span><span class="sxs-lookup"><span data-stu-id="759a5-255">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Drive")</span></span>
</dt> </dl>

<span data-ttu-id="759a5-256">Letra da unidade da unidade (incluindo dois-pontos) em que o objeto do sistema de arquivos está armazenado.</span><span class="sxs-lookup"><span data-stu-id="759a5-256">Drive letter of the drive (including colon) where the file system object is stored.</span></span>

<span data-ttu-id="759a5-257">Exemplo: "c:"</span><span class="sxs-lookup"><span data-stu-id="759a5-257">Example: "c:"</span></span>

<span data-ttu-id="759a5-258">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="759a5-258">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="759a5-259">**EightDotThreeFileName**</span><span class="sxs-lookup"><span data-stu-id="759a5-259">**EightDotThreeFileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="759a5-260">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="759a5-260">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="759a5-261">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="759a5-261">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="759a5-262">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("oito pontos três nome de arquivo")</span><span class="sxs-lookup"><span data-stu-id="759a5-262">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Eight Dot Three File Name")</span></span>
</dt> </dl>

<span data-ttu-id="759a5-263">Nome compatível com MS-DOS para a pasta.</span><span class="sxs-lookup"><span data-stu-id="759a5-263">MS-DOS -compatible name for the folder.</span></span>

<span data-ttu-id="759a5-264">Exemplo: "c: \\ progra ~ 1"</span><span class="sxs-lookup"><span data-stu-id="759a5-264">Example: "c:\\progra~1"</span></span>

<span data-ttu-id="759a5-265">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="759a5-265">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="759a5-266">**Criptografado**</span><span class="sxs-lookup"><span data-stu-id="759a5-266">**Encrypted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="759a5-267">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="759a5-267">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="759a5-268">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="759a5-268">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="759a5-269">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encrypted")</span><span class="sxs-lookup"><span data-stu-id="759a5-269">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encrypted")</span></span>
</dt> </dl>

<span data-ttu-id="759a5-270">Indica se a pasta foi criptografada ou não.</span><span class="sxs-lookup"><span data-stu-id="759a5-270">Indicates whether or not the folder has been encrypted.</span></span> <span data-ttu-id="759a5-271">Se for **true**, a pasta será criptografada.</span><span class="sxs-lookup"><span data-stu-id="759a5-271">If **True**, the folder is encrypted.</span></span>

<span data-ttu-id="759a5-272">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="759a5-272">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="759a5-273">**EncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="759a5-273">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="759a5-274">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="759a5-274">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="759a5-275">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="759a5-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="759a5-276">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("método de criptografia")</span><span class="sxs-lookup"><span data-stu-id="759a5-276">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encryption Method")</span></span>
</dt> </dl>

<span data-ttu-id="759a5-277">Algoritmo ou ferramenta usada para criptografar o arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="759a5-277">Algorithm or tool used to encrypt the logical file.</span></span> <span data-ttu-id="759a5-278">Se não for possível (ou não desejar) descrever o esquema de criptografia (talvez por motivos de segurança), use as seguintes palavras: "desconhecido" para representar que não é conhecido se o arquivo lógico está criptografado; "Encrypted" para representar que o arquivo está criptografado, mas seu esquema de criptografia não é conhecido ou não é divulgado; e "não criptografado" para representar que o arquivo lógico não está criptografado.</span><span class="sxs-lookup"><span data-stu-id="759a5-278">If it is not possible (or not desired) to describe the encryption scheme (perhaps for security reasons), use the following words: "Unknown" to represent that it is not known whether the logical file is encrypted; "Encrypted" to represent that the file is encrypted, but either its encryption scheme is not known or not disclosed; and "Not Encrypted" to represent that the logical file is not encrypted.</span></span>

<span data-ttu-id="759a5-279">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="759a5-279">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="759a5-280">**Extensão**</span><span class="sxs-lookup"><span data-stu-id="759a5-280">**Extension**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="759a5-281">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="759a5-281">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="759a5-282">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="759a5-282">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="759a5-283">Qualificadores: [**fixo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("extensão de arquivo")</span><span class="sxs-lookup"><span data-stu-id="759a5-283">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Extension")</span></span>
</dt> </dl>

<span data-ttu-id="759a5-284">Extensão de nome de arquivo para o objeto do sistema de arquivos, sem incluir o ponto (.) que separa a extensão do nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="759a5-284">File name extension for the file system object, not including the dot (.) that separates the extension from the file name.</span></span>

<span data-ttu-id="759a5-285">Exemplos: "txt", "MOF", "mdb"</span><span class="sxs-lookup"><span data-stu-id="759a5-285">Examples: "txt", "mof", "mdb"</span></span>

<span data-ttu-id="759a5-286">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="759a5-286">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="759a5-287">**FileName**</span><span class="sxs-lookup"><span data-stu-id="759a5-287">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="759a5-288">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="759a5-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="759a5-289">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="759a5-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="759a5-290">Qualificadores: [**fixo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nome do arquivo")</span><span class="sxs-lookup"><span data-stu-id="759a5-290">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Name")</span></span>
</dt> </dl>

<span data-ttu-id="759a5-291">Nome do arquivo (sem o ponto ou a extensão) do arquivo.</span><span class="sxs-lookup"><span data-stu-id="759a5-291">File name (without the dot or extension) of the file.</span></span>

<span data-ttu-id="759a5-292">Exemplo: "autoexec"</span><span class="sxs-lookup"><span data-stu-id="759a5-292">Example: "autoexec"</span></span>

<span data-ttu-id="759a5-293">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="759a5-293">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="759a5-294">**Tamanho**</span><span class="sxs-lookup"><span data-stu-id="759a5-294">**FileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="759a5-295">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="759a5-295">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="759a5-296">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="759a5-296">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="759a5-297">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("tamanho"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="759a5-297">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Size"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="759a5-298">Tamanho do objeto do sistema de arquivos, em bytes.</span><span class="sxs-lookup"><span data-stu-id="759a5-298">Size of the file system object, in bytes.</span></span> <span data-ttu-id="759a5-299">Embora as pastas possuam uma propriedade **filesize** , o valor 0 sempre é retornado.</span><span class="sxs-lookup"><span data-stu-id="759a5-299">Although folders possess a **FileSize** property, the value 0 is always returned.</span></span> <span data-ttu-id="759a5-300">Para determinar o tamanho de uma pasta, use FileSystemObject ou adicione o tamanho de todos os arquivos armazenados na pasta.</span><span class="sxs-lookup"><span data-stu-id="759a5-300">To determine the size of a folder, use the FileSystemObject or add up the size of all the files stored in the folder.</span></span>

<span data-ttu-id="759a5-301">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="759a5-301">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="759a5-302">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="759a5-302">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="759a5-303">**Talvez**</span><span class="sxs-lookup"><span data-stu-id="759a5-303">**FileType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="759a5-304">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="759a5-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="759a5-305">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="759a5-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="759a5-306">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("tipo de arquivo")</span><span class="sxs-lookup"><span data-stu-id="759a5-306">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Type")</span></span>
</dt> </dl>

<span data-ttu-id="759a5-307">Tipo de arquivo (indicado pela propriedade de **extensão** ).</span><span class="sxs-lookup"><span data-stu-id="759a5-307">File type (indicated by the **Extension** property).</span></span>

<span data-ttu-id="759a5-308">Por exemplo, um arquivo. mdb provavelmente terá o tipo de arquivo aplicativo Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="759a5-308">For example, an .mdb file is likely to have the file type Microsoft Access Application.</span></span> <span data-ttu-id="759a5-309">Um arquivo. asp provavelmente tem o tipo de arquivo documento HTML.</span><span class="sxs-lookup"><span data-stu-id="759a5-309">An .asp file likely has the file type HTML Document.</span></span> <span data-ttu-id="759a5-310">Normalmente, as pastas são relatadas simplesmente como pasta.</span><span class="sxs-lookup"><span data-stu-id="759a5-310">Folders are typically reported simply as Folder.</span></span>

<span data-ttu-id="759a5-311">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="759a5-311">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="759a5-312">**FSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="759a5-312">**FSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="759a5-313">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="759a5-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="759a5-314">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="759a5-314">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="759a5-315">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema de arquivos CIM**](cim-filesystem.md).**CreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome da classe do sistema de arquivos ")</span><span class="sxs-lookup"><span data-stu-id="759a5-315">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="759a5-316">Classe do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="759a5-316">Class of the file system.</span></span>

<span data-ttu-id="759a5-317">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="759a5-317">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="759a5-318">**FSName**</span><span class="sxs-lookup"><span data-stu-id="759a5-318">**FSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="759a5-319">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="759a5-319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="759a5-320">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="759a5-320">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="759a5-321">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema de arquivos CIM**](cim-filesystem.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome do sistema de arquivos ")</span><span class="sxs-lookup"><span data-stu-id="759a5-321">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Name")</span></span>
</dt> </dl>

<span data-ttu-id="759a5-322">Tipo de sistema de arquivos (NTFS, FAT, FAT32) instalado na unidade em que o arquivo ou pasta está localizado.</span><span class="sxs-lookup"><span data-stu-id="759a5-322">Type of file system (NTFS, FAT, FAT32) installed on the drive where the file or folder is located.</span></span>

<span data-ttu-id="759a5-323">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="759a5-323">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="759a5-324">**Oculto**</span><span class="sxs-lookup"><span data-stu-id="759a5-324">**Hidden**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="759a5-325">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="759a5-325">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="759a5-326">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="759a5-326">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="759a5-327">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hidden")</span><span class="sxs-lookup"><span data-stu-id="759a5-327">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hidden")</span></span>
</dt> </dl>

<span data-ttu-id="759a5-328">Indica se o objeto do sistema de arquivos está oculto.</span><span class="sxs-lookup"><span data-stu-id="759a5-328">Indicates whether the file system object is hidden.</span></span> <span data-ttu-id="759a5-329">Se for **true**, o arquivo ficará oculto.</span><span class="sxs-lookup"><span data-stu-id="759a5-329">If **True**, the file is hidden.</span></span>

<span data-ttu-id="759a5-330">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="759a5-330">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="759a5-331">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="759a5-331">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="759a5-332">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="759a5-332">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="759a5-333">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="759a5-333">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="759a5-334">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="759a5-334">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="759a5-335">Indica quando o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="759a5-335">Indicates when the object was installed.</span></span> <span data-ttu-id="759a5-336">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="759a5-336">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="759a5-337">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="759a5-337">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="759a5-338">**InUseCount**</span><span class="sxs-lookup"><span data-stu-id="759a5-338">**InUseCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="759a5-339">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="759a5-339">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="759a5-340">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="759a5-340">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="759a5-341">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("contagem de abertura de arquivo atual")</span><span class="sxs-lookup"><span data-stu-id="759a5-341">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Current File Open Count")</span></span>
</dt> </dl>

<span data-ttu-id="759a5-342">Número de "aberturas de arquivo" que estão atualmente ativos no arquivo.</span><span class="sxs-lookup"><span data-stu-id="759a5-342">Number of "file opens" that are currently active against the file.</span></span>

<span data-ttu-id="759a5-343">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="759a5-343">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="759a5-344">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="759a5-344">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="759a5-345">**LastAccessed**</span><span class="sxs-lookup"><span data-stu-id="759a5-345">**LastAccessed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="759a5-346">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="759a5-346">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="759a5-347">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="759a5-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="759a5-348">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("último acesso")</span><span class="sxs-lookup"><span data-stu-id="759a5-348">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Accessed")</span></span>
</dt> </dl>

<span data-ttu-id="759a5-349">Data em que o arquivo foi acessado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="759a5-349">Date the file was last accessed.</span></span> <span data-ttu-id="759a5-350">Para obter mais informações sobre como trabalhar com formatos de data e hora do WMI, consulte [tarefas do WMI: datas e horas](/windows/desktop/WmiSdk/wmi-tasks--dates-and-times).</span><span class="sxs-lookup"><span data-stu-id="759a5-350">For more information on working with WMI date and time formats, see [WMI Tasks: Dates and Times](/windows/desktop/WmiSdk/wmi-tasks--dates-and-times).</span></span>

<span data-ttu-id="759a5-351">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="759a5-351">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="759a5-352">**LastModified**</span><span class="sxs-lookup"><span data-stu-id="759a5-352">**LastModified**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="759a5-353">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="759a5-353">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="759a5-354">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="759a5-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="759a5-355">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("última modificação")</span><span class="sxs-lookup"><span data-stu-id="759a5-355">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Modified")</span></span>
</dt> </dl>

<span data-ttu-id="759a5-356">Data em que o arquivo foi modificado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="759a5-356">Date the file was last modified.</span></span> <span data-ttu-id="759a5-357">Para obter mais informações sobre como trabalhar com formatos de data e hora do WMI, consulte [tarefas do WMI: datas e horas](/windows/desktop/WmiSdk/wmi-tasks--dates-and-times).</span><span class="sxs-lookup"><span data-stu-id="759a5-357">For more information on working with WMI date and time formats, see [WMI Tasks: Dates and Times](/windows/desktop/WmiSdk/wmi-tasks--dates-and-times).</span></span>

<span data-ttu-id="759a5-358">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="759a5-358">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="759a5-359">**Nome**</span><span class="sxs-lookup"><span data-stu-id="759a5-359">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="759a5-360">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="759a5-360">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="759a5-361">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="759a5-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="759a5-362">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="759a5-362">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="759a5-363">A propriedade Name é uma cadeia de caracteres que representa o nome herdado que serve como uma chave de uma instância de arquivo lógico em um sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="759a5-363">The Name property is a string representing the inherited name that serves as a key of a logical file instance within a file system.</span></span> <span data-ttu-id="759a5-364">Devem ser fornecidos nomes de caminho completos.</span><span class="sxs-lookup"><span data-stu-id="759a5-364">Full path names should be provided.</span></span> <span data-ttu-id="759a5-365">Exemplo: C: \\ \\ sistema Windows \\win.ini</span><span class="sxs-lookup"><span data-stu-id="759a5-365">Example: C:\\Windows\\system\\win.ini</span></span>

<span data-ttu-id="759a5-366">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="759a5-366">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="759a5-367">**Caminho**</span><span class="sxs-lookup"><span data-stu-id="759a5-367">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="759a5-368">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="759a5-368">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="759a5-369">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="759a5-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="759a5-370">Qualificadores: [**fixo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Path")</span><span class="sxs-lookup"><span data-stu-id="759a5-370">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Path")</span></span>
</dt> </dl>

<span data-ttu-id="759a5-371">Caminho para o arquivo.</span><span class="sxs-lookup"><span data-stu-id="759a5-371">Path for the file.</span></span> <span data-ttu-id="759a5-372">O caminho inclui as barras invertidas à esquerda e à direita, mas não a letra da unidade ou o nome da pasta.</span><span class="sxs-lookup"><span data-stu-id="759a5-372">The path includes the leading and trailing backslashes, but not the drive letter or the folder name.</span></span>

<span data-ttu-id="759a5-373">Para a pasta c: \\ Windows \\ System32 \\ WBEM, o caminho é \\ Windows \\ System32 \\ .</span><span class="sxs-lookup"><span data-stu-id="759a5-373">For the folder c:\\windows\\system32\\wbem, the path is \\windows\\system32\\.</span></span> <span data-ttu-id="759a5-374">Para a pasta c: \\ scripts, o caminho é \\ .</span><span class="sxs-lookup"><span data-stu-id="759a5-374">For the folder c:\\scripts, the path is \\.</span></span>

<span data-ttu-id="759a5-375">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="759a5-375">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="759a5-376">**Seres**</span><span class="sxs-lookup"><span data-stu-id="759a5-376">**Readable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="759a5-377">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="759a5-377">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="759a5-378">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="759a5-378">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="759a5-379">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("legível")</span><span class="sxs-lookup"><span data-stu-id="759a5-379">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Readable")</span></span>
</dt> </dl>

<span data-ttu-id="759a5-380">Indica se você pode ler itens na pasta.</span><span class="sxs-lookup"><span data-stu-id="759a5-380">Indicates whether you can read items in the folder.</span></span> <span data-ttu-id="759a5-381">Se **for true**, o arquivo poderá ser lido.</span><span class="sxs-lookup"><span data-stu-id="759a5-381">If **True**, the file can be read.</span></span>

<span data-ttu-id="759a5-382">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="759a5-382">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="759a5-383">**Status**</span><span class="sxs-lookup"><span data-stu-id="759a5-383">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="759a5-384">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="759a5-384">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="759a5-385">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="759a5-385">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="759a5-386">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="759a5-386">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="759a5-387">Cadeia de caracteres que indica o status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="759a5-387">String that indicates the current status of the object.</span></span>

<span data-ttu-id="759a5-388">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="759a5-388">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="759a5-389">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="759a5-389">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="759a5-390">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="759a5-390">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="759a5-391">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="759a5-391">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="759a5-392">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="759a5-392">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="759a5-393">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="759a5-393">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="759a5-394">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="759a5-394">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="759a5-395">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="759a5-395">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="759a5-396">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="759a5-396">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="759a5-397">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="759a5-397">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="759a5-398">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="759a5-398">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="759a5-399">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="759a5-399">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="759a5-400">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="759a5-400">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="759a5-401">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="759a5-401">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="759a5-402">**System**</span><span class="sxs-lookup"><span data-stu-id="759a5-402">**System**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="759a5-403">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="759a5-403">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="759a5-404">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="759a5-404">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="759a5-405">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("arquivo do sistema")</span><span class="sxs-lookup"><span data-stu-id="759a5-405">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System File")</span></span>
</dt> </dl>

<span data-ttu-id="759a5-406">Indica se o objeto é um arquivo do sistema.</span><span class="sxs-lookup"><span data-stu-id="759a5-406">Indicates whether the object is a system file.</span></span> <span data-ttu-id="759a5-407">Se for **true**, o arquivo será um arquivo do sistema</span><span class="sxs-lookup"><span data-stu-id="759a5-407">If **True**, the file is a system file</span></span>

<span data-ttu-id="759a5-408">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="759a5-408">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="759a5-409">**Gravável**</span><span class="sxs-lookup"><span data-stu-id="759a5-409">**Writeable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="759a5-410">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="759a5-410">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="759a5-411">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="759a5-411">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="759a5-412">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("gravável")</span><span class="sxs-lookup"><span data-stu-id="759a5-412">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Writeable")</span></span>
</dt> </dl>

<span data-ttu-id="759a5-413">Se **for true**, o arquivo poderá ser gravado.</span><span class="sxs-lookup"><span data-stu-id="759a5-413">If **True**, the file can be written.</span></span>

<span data-ttu-id="759a5-414">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="759a5-414">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="759a5-415">Comentários</span><span class="sxs-lookup"><span data-stu-id="759a5-415">Remarks</span></span>

<span data-ttu-id="759a5-416">A classe do **\_ diretório Win32** é derivada [**do \_ diretório CIM**](cim-directory.md).</span><span class="sxs-lookup"><span data-stu-id="759a5-416">The **Win32\_Directory** class is derived from [**CIM\_Directory**](cim-directory.md).</span></span>

<span data-ttu-id="759a5-417">**Visão geral**</span><span class="sxs-lookup"><span data-stu-id="759a5-417">**Overview**</span></span>

<span data-ttu-id="759a5-418">As pastas são objetos do sistema de arquivos criados para conter outros objetos do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="759a5-418">Folders are file system objects designed to contain other file system objects.</span></span> <span data-ttu-id="759a5-419">No entanto, isso não significa que todas as pastas são semelhantes.</span><span class="sxs-lookup"><span data-stu-id="759a5-419">This does not mean that all folders are alike, however.</span></span> <span data-ttu-id="759a5-420">Em vez disso, as pastas podem variar consideravelmente.</span><span class="sxs-lookup"><span data-stu-id="759a5-420">Instead, folders can vary considerably.</span></span> <span data-ttu-id="759a5-421">Algumas pastas são pastas do sistema operacional, que geralmente não devem ser modificadas por um script.</span><span class="sxs-lookup"><span data-stu-id="759a5-421">Some folders are operating system folders, which generally should not be modified by a script.</span></span> <span data-ttu-id="759a5-422">Algumas pastas são somente leitura, o que significa que os usuários podem acessar o conteúdo dessa pasta, mas não podem adicionar, excluir ou modificar esses conteúdos.</span><span class="sxs-lookup"><span data-stu-id="759a5-422">Some folders are read-only, which means that users can access the contents of that folder but cannot add to, delete from, or modify those contents.</span></span> <span data-ttu-id="759a5-423">Algumas pastas são compactadas para armazenamento ideal, enquanto outras ficam ocultas e não são visíveis para os usuários.</span><span class="sxs-lookup"><span data-stu-id="759a5-423">Some folders are compressed for optimal storage, while others are hidden and not visible to users.</span></span>

<span data-ttu-id="759a5-424">O WMI usa a classe de **\_ diretório do Win32** para gerenciar pastas.</span><span class="sxs-lookup"><span data-stu-id="759a5-424">WMI uses the **Win32\_Directory** class to manage folders.</span></span> <span data-ttu-id="759a5-425">Significativamente, as propriedades e os métodos disponíveis nessa classe são idênticos às propriedades e aos métodos disponíveis na classe de [**\_ arquivo**](cim-datafile.md) de arquivos CIM, a classe usada para gerenciar arquivos.</span><span class="sxs-lookup"><span data-stu-id="759a5-425">Significantly, the properties and methods available in this class are identical to the properties and methods available in the [**CIM\_DataFile**](cim-datafile.md) class, the class used to manage files.</span></span> <span data-ttu-id="759a5-426">Isso significa que, depois de aprender a gerenciar pastas usando o WMI, você terá, sem qualquer trabalho extra, também saberá como gerenciar arquivos.</span><span class="sxs-lookup"><span data-stu-id="759a5-426">This means that after you have learned how to manage folders using WMI, you will, without any extra work, also know how to manage files.</span></span>

<span data-ttu-id="759a5-427">A classe de associação de [**\_ subdiretório Win32**](win32-subdirectory.md) também é usada para gerenciar arquivos e pastas.</span><span class="sxs-lookup"><span data-stu-id="759a5-427">The [**Win32\_Subdirectory**](win32-subdirectory.md) association class is also used to manage files and folders.</span></span> <span data-ttu-id="759a5-428">A classe de **\_ subdiretório Win32** relaciona uma pasta e suas subpastas imediatas.</span><span class="sxs-lookup"><span data-stu-id="759a5-428">The **Win32\_Subdirectory** class relates a folder and its immediate subfolders.</span></span> <span data-ttu-id="759a5-429">Por exemplo, na estrutura de pastas C: \\ scripts \\ logs, logs é uma subpasta de scripts e scripts é uma subpasta da pasta raiz C: \\ .</span><span class="sxs-lookup"><span data-stu-id="759a5-429">For example, in the folder structure C:\\Scripts\\Logs, Logs is a subfolder of Scripts, and Scripts is a subfolder of the root folder C:\\.</span></span> <span data-ttu-id="759a5-430">No entanto, os logs não são considerados uma subpasta de C: \\ .</span><span class="sxs-lookup"><span data-stu-id="759a5-430">However, Logs is not considered a subfolder of C:\\.</span></span>

<span data-ttu-id="759a5-431">Você pode recuperar as propriedades de qualquer pasta no sistema de arquivos usando a classe de **\_ diretório Win32** .</span><span class="sxs-lookup"><span data-stu-id="759a5-431">You can retrieve the properties of any folder in the file system using the **Win32\_Directory** class.</span></span> <span data-ttu-id="759a5-432">As propriedades disponíveis usando essa classe são mostradas na tabela 11,1.</span><span class="sxs-lookup"><span data-stu-id="759a5-432">The properties available using this class are shown in Table 11.1.</span></span> <span data-ttu-id="759a5-433">Para recuperar as propriedades de uma única pasta, construa uma consulta WQL (linguagem de consulta do Windows) para a classe do **\_ diretório Win32** , certificando-se de incluir o nome da pasta.</span><span class="sxs-lookup"><span data-stu-id="759a5-433">To retrieve the properties for a single folder, construct a Windows Query Language (WQL) query for the **Win32\_Directory** class, making sure that you include the name of the folder.</span></span> <span data-ttu-id="759a5-434">Por exemplo, essa consulta é vinculada à pasta D: \\ arquivo morto:</span><span class="sxs-lookup"><span data-stu-id="759a5-434">For example, this query binds to the folder D:\\Archive:</span></span>

`        Copy     "SELECT * FROM Win32_Directory WHERE Name = 'D:\\Archive'"`

<span data-ttu-id="759a5-435">Ao especificar um nome de arquivo ou pasta em uma consulta WQL, certifique-se de usar duas barras invertidas ( \\ \\ ) para separar componentes de caminho.</span><span class="sxs-lookup"><span data-stu-id="759a5-435">When specifying a file or folder name in a WQL query, be sure you use two backslashes (\\\\) to separate path components.</span></span>

<span data-ttu-id="759a5-436">Se você quiser limitar a recuperação de dados a uma única unidade de disco, inclua uma cláusula WHERE especificando a letra da unidade.</span><span class="sxs-lookup"><span data-stu-id="759a5-436">If you want to limit data retrieval to a single disk drive, include a Where clause specifying the drive letter.</span></span> <span data-ttu-id="759a5-437">Por exemplo, essa consulta retorna uma lista de todas as pastas na unidade C:</span><span class="sxs-lookup"><span data-stu-id="759a5-437">For example, this query returns a list of all the folders on drive C:</span></span>

`"SELECT * FROM Win32_Directory WHERE Drive = 'C:'"`

<span data-ttu-id="759a5-438">Se você precisar enumerar todas as pastas em um computador, lembre-se de que essa consulta pode levar um tempo estendido para ser concluída.</span><span class="sxs-lookup"><span data-stu-id="759a5-438">If you need to enumerate all the folders on a computer, be aware that this query can take an extended time to complete.</span></span>

## <a name="examples"></a><span data-ttu-id="759a5-439">Exemplos</span><span class="sxs-lookup"><span data-stu-id="759a5-439">Examples</span></span>

<span data-ttu-id="759a5-440">O exemplo de VBScript a seguir recupera as propriedades da pasta C: \\ scripts.</span><span class="sxs-lookup"><span data-stu-id="759a5-440">The following VBScript sample retrieves properties for the folder C:\\Scripts.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colFolders = objWMIService.ExecQuery("SELECT * FROM Win32_Directory WHERE Name = 'c:\\Scripts'")
For Each objFolder in colFolders
 Wscript.Echo "Archive: " & objFolder.Archive
 Wscript.Echo "Caption: " & objFolder.Caption
 Wscript.Echo "Compressed: " & objFolder.Compressed
 Wscript.Echo "Compression method: " & objFolder.CompressionMethod
 Wscript.Echo "Creation date: " & objFolder.CreationDate
 Wscript.Echo "Encrypted: " & objFolder.Encrypted
 Wscript.Echo "Encryption method: " & objFolder.EncryptionMethod
 Wscript.Echo "Hidden: " & objFolder.Hidden
 Wscript.Echo "In use count: " & objFolder.InUseCount
 Wscript.Echo "Last accessed: " & objFolder.LastAccessed
 Wscript.Echo "Last modified: " & objFolder.LastModified
 Wscript.Echo "Name: " & objFolder.Name
 Wscript.Echo "Path: " & objFolder.Path
 Wscript.Echo "Readable: " & objFolder.Readable
 Wscript.Echo "System: " & objFolder.System
 Wscript.Echo "Writeable: " & objFolder.Writeable
Next
```



<span data-ttu-id="759a5-441">O exemplo de VBScript a seguir retorna uma lista de todas as pastas ocultas em um computador.</span><span class="sxs-lookup"><span data-stu-id="759a5-441">The following VBScript sample returns a list of all the hidden folders on a computer.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colFiles = objWMIService.ExecQuery("SELECT * FROM Win32_Directory WHERE Hidden = True")
For Each objFile in colFiles
 Wscript.Echo objFile.Name
Next
```



## <a name="requirements"></a><span data-ttu-id="759a5-442">Requisitos</span><span class="sxs-lookup"><span data-stu-id="759a5-442">Requirements</span></span>



| <span data-ttu-id="759a5-443">Requisito</span><span class="sxs-lookup"><span data-stu-id="759a5-443">Requirement</span></span> | <span data-ttu-id="759a5-444">Valor</span><span class="sxs-lookup"><span data-stu-id="759a5-444">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="759a5-445">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="759a5-445">Minimum supported client</span></span><br/> | <span data-ttu-id="759a5-446">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="759a5-446">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="759a5-447">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="759a5-447">Minimum supported server</span></span><br/> | <span data-ttu-id="759a5-448">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="759a5-448">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="759a5-449">Namespace</span><span class="sxs-lookup"><span data-stu-id="759a5-449">Namespace</span></span><br/>                | <span data-ttu-id="759a5-450">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="759a5-450">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="759a5-451">MOF</span><span class="sxs-lookup"><span data-stu-id="759a5-451">MOF</span></span><br/>                      | <dl> <span data-ttu-id="759a5-452"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="759a5-452"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="759a5-453">DLL</span><span class="sxs-lookup"><span data-stu-id="759a5-453">DLL</span></span><br/>                      | <dl> <span data-ttu-id="759a5-454"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="759a5-454"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="759a5-455">Confira também</span><span class="sxs-lookup"><span data-stu-id="759a5-455">See also</span></span>

<dl> <dt>

[<span data-ttu-id="759a5-456">**\_Diretório CIM**</span><span class="sxs-lookup"><span data-stu-id="759a5-456">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> <dt>

<span data-ttu-id="759a5-457">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="759a5-457">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

