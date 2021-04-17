---
description: O atalho do Win32file \_&\# 32; A classe WMI representa os arquivos que são atalhos para outros arquivos, diretórios e comandos.
ms.assetid: 15973234-e418-4869-839e-a7c439512e4e
ms.tgt_platform: multiple
title: Classe Win32_ShortcutFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ShortcutFile
- Win32_ShortcutFile.Caption
- Win32_ShortcutFile.Description
- Win32_ShortcutFile.InstallDate
- Win32_ShortcutFile.Status
- Win32_ShortcutFile.AccessMask
- Win32_ShortcutFile.Archive
- Win32_ShortcutFile.Compressed
- Win32_ShortcutFile.CompressionMethod
- Win32_ShortcutFile.CreationClassName
- Win32_ShortcutFile.CreationDate
- Win32_ShortcutFile.CSCreationClassName
- Win32_ShortcutFile.CSName
- Win32_ShortcutFile.Drive
- Win32_ShortcutFile.EightDotThreeFileName
- Win32_ShortcutFile.Encrypted
- Win32_ShortcutFile.EncryptionMethod
- Win32_ShortcutFile.Name
- Win32_ShortcutFile.Extension
- Win32_ShortcutFile.FileName
- Win32_ShortcutFile.FileSize
- Win32_ShortcutFile.FileType
- Win32_ShortcutFile.FSCreationClassName
- Win32_ShortcutFile.FSName
- Win32_ShortcutFile.Hidden
- Win32_ShortcutFile.InUseCount
- Win32_ShortcutFile.LastAccessed
- Win32_ShortcutFile.LastModified
- Win32_ShortcutFile.Path
- Win32_ShortcutFile.Readable
- Win32_ShortcutFile.System
- Win32_ShortcutFile.Writeable
- Win32_ShortcutFile.Manufacturer
- Win32_ShortcutFile.Version
- Win32_ShortcutFile.Target
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b714b4c8119f92931235734664726123744064d8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105762757"
---
# <a name="win32_shortcutfile-class"></a><span data-ttu-id="85061-103">\_Classe de atalhofile Win32</span><span class="sxs-lookup"><span data-stu-id="85061-103">Win32\_ShortcutFile class</span></span>

<span data-ttu-id="85061-104">A [classe WMI](../wmisdk/retrieving-a-class.md) **\_ shortcutfile do Win32** representa arquivos que são atalhos para outros arquivos, diretórios e comandos.</span><span class="sxs-lookup"><span data-stu-id="85061-104">The **Win32\_ShortcutFile** [WMI class](../wmisdk/retrieving-a-class.md) represents files that are shortcuts to other files, directories, and commands.</span></span>

<span data-ttu-id="85061-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="85061-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="85061-106">As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.</span><span class="sxs-lookup"><span data-stu-id="85061-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="85061-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="85061-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{F25FE466-783E-11d2-90BF-0060081A46FD}"), AMENDMENT]
class Win32_ShortcutFile : CIM_DataFile
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
  string   Target;
};
```

## <a name="members"></a><span data-ttu-id="85061-108">Membros</span><span class="sxs-lookup"><span data-stu-id="85061-108">Members</span></span>

<span data-ttu-id="85061-109">A **classe \_ Shortcutfile do Win32** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="85061-109">The **Win32\_ShortcutFile** class has these types of members:</span></span>

-   [<span data-ttu-id="85061-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="85061-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="85061-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="85061-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="85061-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="85061-112">Methods</span></span>

<span data-ttu-id="85061-113">A **classe \_ Shortcutfile do Win32** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="85061-113">The **Win32\_ShortcutFile** class has these methods.</span></span>



| <span data-ttu-id="85061-114">Método</span><span class="sxs-lookup"><span data-stu-id="85061-114">Method</span></span>                                                                                                | <span data-ttu-id="85061-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="85061-115">Description</span></span>                                                                                                                                                                                                                          |
|:------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="85061-116">**ChangeSecurityPermissions**</span><span class="sxs-lookup"><span data-stu-id="85061-116">**ChangeSecurityPermissions**</span></span>](changesecuritypermissions-method-in-class-win32-shortcutfile.md)     | <span data-ttu-id="85061-117">Método de classe que altera as permissões de segurança para o arquivo lógico especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="85061-117">Class method that changes the security permissions for the logical file specified in the object path.</span></span><br/>                                                                                                                     |
| [<span data-ttu-id="85061-118">**ChangeSecurityPermissionsEx**</span><span class="sxs-lookup"><span data-stu-id="85061-118">**ChangeSecurityPermissionsEx**</span></span>](changesecuritypermissionsex-method-in-class-win32-shortcutfile.md) | <span data-ttu-id="85061-119">Método de classe que altera as permissões de segurança para o arquivo lógico especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="85061-119">Class method that changes the security permissions for the logical file specified in the object path.</span></span><br/>                                                                                                                     |
| [<span data-ttu-id="85061-120">**Compactar**</span><span class="sxs-lookup"><span data-stu-id="85061-120">**Compress**</span></span>](compress-method-in-class-win32-shortcutfile.md)                                       | <span data-ttu-id="85061-121">Método de classe que compacta o arquivo lógico (ou diretório) especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="85061-121">Class method that compresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="85061-122">**CompressEx**</span><span class="sxs-lookup"><span data-stu-id="85061-122">**CompressEx**</span></span>](compressex-method-in-class-win32-shortcutfile.md)                                   | <span data-ttu-id="85061-123">Método de classe que compacta o arquivo lógico (ou diretório) especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="85061-123">Class method that compresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="85061-124">**Copiar**</span><span class="sxs-lookup"><span data-stu-id="85061-124">**Copy**</span></span>](copy-method-in-class-win32-shortcutfile.md)                                               | <span data-ttu-id="85061-125">Método de classe que copia o arquivo ou diretório lógico especificado no caminho do objeto para o local especificado pelo parâmetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="85061-125">Class method that copies the logical file or directory specified in the object path to the location specified by the input parameter.</span></span><br/>                                                                                     |
| [<span data-ttu-id="85061-126">**CopyEx**</span><span class="sxs-lookup"><span data-stu-id="85061-126">**CopyEx**</span></span>](copyex-method-in-class-win32-shortcutfile.md)                                           | <span data-ttu-id="85061-127">Método de classe que copia o arquivo ou diretório lógico especificado no caminho do objeto para o local especificado pelo parâmetro *filename* .</span><span class="sxs-lookup"><span data-stu-id="85061-127">Class method that copies the logical file or directory specified in the object path to the location specified by the *FileName* parameter.</span></span><br/>                                                                                |
| [<span data-ttu-id="85061-128">**Excluir**</span><span class="sxs-lookup"><span data-stu-id="85061-128">**Delete**</span></span>](delete-method-in-class-win32-shortcutfile.md)                                           | <span data-ttu-id="85061-129">Método de classe que exclui o arquivo lógico (ou diretório) especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="85061-129">Class method that deletes the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="85061-130">**DeleteEx**</span><span class="sxs-lookup"><span data-stu-id="85061-130">**DeleteEx**</span></span>](deleteex-method-in-class-win32-shortcutfile.md)                                       | <span data-ttu-id="85061-131">Método de classe que exclui o arquivo lógico (ou diretório) especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="85061-131">Class method that deletes the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="85061-132">**GetEffectivePermission**</span><span class="sxs-lookup"><span data-stu-id="85061-132">**GetEffectivePermission**</span></span>](geteffectivepermission-method-in-class-win32-shortcutfile.md)           | <span data-ttu-id="85061-133">Método de classe que determina se o chamador tem as permissões agregadas especificadas pelo argumento de permissão não apenas no objeto File, mas no compartilhamento o arquivo ou diretório reside (se estiver em um compartilhamento).</span><span class="sxs-lookup"><span data-stu-id="85061-133">Class method that determines whether the caller has the aggregated permissions specified by the Permission argument not only on the file object, but on the share the file or directory resides on (if it is on a share).</span></span><br/> |
| [<span data-ttu-id="85061-134">**Renomear**</span><span class="sxs-lookup"><span data-stu-id="85061-134">**Rename**</span></span>](rename-method-in-class-win32-shortcutfile.md)                                           | <span data-ttu-id="85061-135">Método de classe que renomeia o arquivo lógico (ou diretório) especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="85061-135">Class method that renames the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="85061-136">**TakeOwnerShip**</span><span class="sxs-lookup"><span data-stu-id="85061-136">**TakeOwnerShip**</span></span>](takeownership-method-in-class-win32-shortcutfile.md)                             | <span data-ttu-id="85061-137">Método de classe que obtém a propriedade do arquivo lógico especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="85061-137">Class method that obtains ownership of the logical file specified in the object path.</span></span><br/>                                                                                                                                     |
| [<span data-ttu-id="85061-138">**TakeOwnerShipEx**</span><span class="sxs-lookup"><span data-stu-id="85061-138">**TakeOwnerShipEx**</span></span>](takeownershipex-method-in-class-win32-shortcutfile.md)                         | <span data-ttu-id="85061-139">Método de classe que obtém a propriedade do arquivo lógico especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="85061-139">Class method that obtains ownership of the logical file specified in the object path.</span></span><br/>                                                                                                                                     |
| [<span data-ttu-id="85061-140">**Descompactar**</span><span class="sxs-lookup"><span data-stu-id="85061-140">**Uncompress**</span></span>](uncompress-method-in-class-win32-shortcutfile.md)                                   | <span data-ttu-id="85061-141">Método de classe que descompacta o arquivo lógico (ou diretório) especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="85061-141">Class method that uncompresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="85061-142">**UncompressEx**</span><span class="sxs-lookup"><span data-stu-id="85061-142">**UncompressEx**</span></span>](uncompressex-method-in-class-win32-shortcutfile.md)                               | <span data-ttu-id="85061-143">Método de classe que descompacta o arquivo lógico (ou diretório) especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="85061-143">Class method that uncompresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                              |



 

### <a name="properties"></a><span data-ttu-id="85061-144">Propriedades</span><span class="sxs-lookup"><span data-stu-id="85061-144">Properties</span></span>

<span data-ttu-id="85061-145">A **classe \_ Shortcutfile do Win32** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="85061-145">The **Win32\_ShortcutFile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="85061-146">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="85061-146">**AccessMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85061-147">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="85061-147">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="85061-148">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="85061-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85061-149">Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("direitos de acesso")</span><span class="sxs-lookup"><span data-stu-id="85061-149">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Access Rights")</span></span>
</dt> </dl>

<span data-ttu-id="85061-150">Bitmask que representa os direitos de acesso necessários para acessar ou executar operações específicas no arquivo.</span><span class="sxs-lookup"><span data-stu-id="85061-150">Bitmask that represents the access rights required to access or perform specific operations on the file.</span></span> <span data-ttu-id="85061-151">Para valores de bit, consulte [**constantes de direitos de acesso de arquivo e diretório**](../wmisdk/file-and-directory-access-rights-constants.md).</span><span class="sxs-lookup"><span data-stu-id="85061-151">For bit values, see [**File and Directory Access Rights Constants**](../wmisdk/file-and-directory-access-rights-constants.md).</span></span>

> [!Note]  
> <span data-ttu-id="85061-152">Em volumes FAT, o valor de **\_ acesso completo** é retornado, o que indica que nenhuma segurança foi definida no objeto.</span><span class="sxs-lookup"><span data-stu-id="85061-152">On FAT volumes, the **FULL\_ACCESS** value is returned instead, which indicates no security has been set on the object.</span></span>

 

<span data-ttu-id="85061-153">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="85061-153">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="85061-154">Do **arquivo \_ LER \_ os dados (arquivo) ou \_ \_ diretório de lista de arquivos (diretório)** (1)</span><span class="sxs-lookup"><span data-stu-id="85061-154">**FILE\_READ\_DATA (file) or FILE\_LIST\_DIRECTORY (directory)** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="85061-155">Do **arquivo \_ GRAVAR \_ dados (arquivo) ou arquivo \_ Adicionar \_ arquivo (diretório)** (2)</span><span class="sxs-lookup"><span data-stu-id="85061-155">**FILE\_WRITE\_DATA (file) or FILE\_ADD\_FILE (directory)** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="85061-156">Do **arquivo \_ ACRESCENTAR \_ dados (arquivo) ou arquivo \_ Adicionar \_ subdiretório (diretório)** (4)</span><span class="sxs-lookup"><span data-stu-id="85061-156">**FILE\_APPEND\_DATA (file) or FILE\_ADD\_SUBDIRECTORY (directory)** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="85061-157">Do **arquivo \_ LER \_ ea** (8)</span><span class="sxs-lookup"><span data-stu-id="85061-157">**FILE\_READ\_EA** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="85061-158">Do **arquivo \_ GRAVAR \_ ea** (16)</span><span class="sxs-lookup"><span data-stu-id="85061-158">**FILE\_WRITE\_EA** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

<span data-ttu-id="85061-159">Do **arquivo \_ EXECUTAR (arquivo) ou \_ atravessamento de arquivo (diretório)** (32)</span><span class="sxs-lookup"><span data-stu-id="85061-159">**FILE\_EXECUTE (file) or FILE\_TRAVERSE (directory)** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="85061-160">Do **arquivo \_ EXCLUIR \_ filho (diretório)** (64)</span><span class="sxs-lookup"><span data-stu-id="85061-160">**FILE\_DELETE\_CHILD (directory)** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="85061-161">Do **arquivo \_ \_Atributos de leitura** (128)</span><span class="sxs-lookup"><span data-stu-id="85061-161">**FILE\_READ\_ATTRIBUTES** (128)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="85061-162">Do **arquivo \_ \_Atributos de gravação** (256)</span><span class="sxs-lookup"><span data-stu-id="85061-162">**FILE\_WRITE\_ATTRIBUTES** (256)</span></span>


</dt> <dd></dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="85061-163">**Excluir** (65536)</span><span class="sxs-lookup"><span data-stu-id="85061-163">**DELETE** (65536)</span></span>


</dt> <dd></dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="85061-164">**Ler \_ CONTROLE** (131072)</span><span class="sxs-lookup"><span data-stu-id="85061-164">**READ\_CONTROL** (131072)</span></span>


</dt> <dd></dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="85061-165">**Gravar \_ DAC** (262144)</span><span class="sxs-lookup"><span data-stu-id="85061-165">**WRITE\_DAC** (262144)</span></span>


</dt> <dd></dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="85061-166">**Gravar \_ PROPRIETÁRIO** (524288)</span><span class="sxs-lookup"><span data-stu-id="85061-166">**WRITE\_OWNER** (524288)</span></span>


</dt> <dd></dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="85061-167">**Sincronizar** (1048576)</span><span class="sxs-lookup"><span data-stu-id="85061-167">**SYNCHRONIZE** (1048576)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="85061-168">**Arquivar**</span><span class="sxs-lookup"><span data-stu-id="85061-168">**Archive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85061-169">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="85061-169">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="85061-170">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="85061-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85061-171">Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("deve ser arquivado")</span><span class="sxs-lookup"><span data-stu-id="85061-171">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Should Be Archived")</span></span>
</dt> </dl>

<span data-ttu-id="85061-172">Se **for true**, o arquivo deverá ser arquivado.</span><span class="sxs-lookup"><span data-stu-id="85061-172">If **True**, the file should be archived.</span></span>

<span data-ttu-id="85061-173">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="85061-173">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="85061-174">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="85061-174">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85061-175">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="85061-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85061-176">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="85061-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85061-177">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="85061-177">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="85061-178">Uma breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="85061-178">A short textual description of the object.</span></span>

<span data-ttu-id="85061-179">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="85061-179">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="85061-180">**Compactado**</span><span class="sxs-lookup"><span data-stu-id="85061-180">**Compressed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85061-181">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="85061-181">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="85061-182">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="85061-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85061-183">Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("compactado")</span><span class="sxs-lookup"><span data-stu-id="85061-183">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Compressed")</span></span>
</dt> </dl>

<span data-ttu-id="85061-184">Se **for true**, o arquivo será compactado.</span><span class="sxs-lookup"><span data-stu-id="85061-184">If **True**, the file is compressed.</span></span>

<span data-ttu-id="85061-185">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="85061-185">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="85061-186">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="85061-186">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85061-187">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="85061-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85061-188">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="85061-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85061-189">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("método de compactação")</span><span class="sxs-lookup"><span data-stu-id="85061-189">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Compression Method")</span></span>
</dt> </dl>

<span data-ttu-id="85061-190">Cadeia de caracteres de forma livre que indica o algoritmo ou a ferramenta usada para compactar o arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="85061-190">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="85061-191">Se o esquema de compactação for desconhecido ou não estiver descrito, use "desconhecido".</span><span class="sxs-lookup"><span data-stu-id="85061-191">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="85061-192">Se o arquivo lógico estiver compactado, mas o esquema de compactação for desconhecido ou não estiver descrito, use "compactado".</span><span class="sxs-lookup"><span data-stu-id="85061-192">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="85061-193">Se o arquivo lógico não estiver compactado, use "não compactado".</span><span class="sxs-lookup"><span data-stu-id="85061-193">If the logical file is not compressed, use "Not Compressed".</span></span>

<span data-ttu-id="85061-194">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="85061-194">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="85061-195">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="85061-195">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85061-196">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="85061-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85061-197">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="85061-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85061-198">Qualificadores: [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("nome da classe")</span><span class="sxs-lookup"><span data-stu-id="85061-198">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="85061-199">Nome da classe.</span><span class="sxs-lookup"><span data-stu-id="85061-199">Name of the class.</span></span>

<span data-ttu-id="85061-200">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="85061-200">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="85061-201">**CreationDate**</span><span class="sxs-lookup"><span data-stu-id="85061-201">**CreationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85061-202">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="85061-202">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="85061-203">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="85061-203">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85061-204">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("data de criação")</span><span class="sxs-lookup"><span data-stu-id="85061-204">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Creation Date")</span></span>
</dt> </dl>

<span data-ttu-id="85061-205">Data e hora da criação do arquivo.</span><span class="sxs-lookup"><span data-stu-id="85061-205">Date and time of the file's creation.</span></span>

<span data-ttu-id="85061-206">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="85061-206">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="85061-207">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="85061-207">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85061-208">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="85061-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85061-209">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="85061-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85061-210">Qualificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ sistema de arquivos CIM**](cim-filesystem.md).**CSCreationClassName**"), [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" nome da classe do sistema de computador ")</span><span class="sxs-lookup"><span data-stu-id="85061-210">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSCreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Computer System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="85061-211">Classe do sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="85061-211">Class of the computer system.</span></span>

<span data-ttu-id="85061-212">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="85061-212">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="85061-213">**CSName**</span><span class="sxs-lookup"><span data-stu-id="85061-213">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85061-214">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="85061-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85061-215">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="85061-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85061-216">Qualificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ sistema de arquivos CIM**](cim-filesystem.md).**CSName**"), [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" nome do sistema de computador ")</span><span class="sxs-lookup"><span data-stu-id="85061-216">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Computer System Name")</span></span>
</dt> </dl>

<span data-ttu-id="85061-217">Nome do sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="85061-217">Name of the computer system.</span></span>

<span data-ttu-id="85061-218">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="85061-218">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="85061-219">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="85061-219">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85061-220">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="85061-220">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85061-221">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="85061-221">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85061-222">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="85061-222">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="85061-223">Uma descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="85061-223">A textual description of the object.</span></span>

<span data-ttu-id="85061-224">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="85061-224">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="85061-225">**Unidade**</span><span class="sxs-lookup"><span data-stu-id="85061-225">**Drive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85061-226">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="85061-226">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85061-227">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="85061-227">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85061-228">Qualificadores: [**fixo**](../wmisdk/standard-wmi-qualifiers.md), [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("drive")</span><span class="sxs-lookup"><span data-stu-id="85061-228">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Drive")</span></span>
</dt> </dl>

<span data-ttu-id="85061-229">Letra da unidade (incluindo os dois-pontos que segue a letra da unidade) do arquivo.</span><span class="sxs-lookup"><span data-stu-id="85061-229">Drive letter (including the colon that follows the drive letter) of the file.</span></span>

<span data-ttu-id="85061-230">Exemplo: "c:"</span><span class="sxs-lookup"><span data-stu-id="85061-230">Example: "c:"</span></span>

<span data-ttu-id="85061-231">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="85061-231">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="85061-232">**EightDotThreeFileName**</span><span class="sxs-lookup"><span data-stu-id="85061-232">**EightDotThreeFileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85061-233">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="85061-233">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85061-234">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="85061-234">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85061-235">Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("oito pontos três nome de arquivo")</span><span class="sxs-lookup"><span data-stu-id="85061-235">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Eight Dot Three File Name")</span></span>
</dt> </dl>

<span data-ttu-id="85061-236">Nome do arquivo no formato 8,3.</span><span class="sxs-lookup"><span data-stu-id="85061-236">File name in 8.3 format.</span></span>

<span data-ttu-id="85061-237">Exemplo: "c: \\ progra ~ 1"</span><span class="sxs-lookup"><span data-stu-id="85061-237">Example: "c:\\progra~1"</span></span>

<span data-ttu-id="85061-238">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="85061-238">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="85061-239">**Criptografado**</span><span class="sxs-lookup"><span data-stu-id="85061-239">**Encrypted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85061-240">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="85061-240">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="85061-241">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="85061-241">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85061-242">Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Encrypted")</span><span class="sxs-lookup"><span data-stu-id="85061-242">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Encrypted")</span></span>
</dt> </dl>

<span data-ttu-id="85061-243">Se **for true**, o arquivo será criptografado.</span><span class="sxs-lookup"><span data-stu-id="85061-243">If **True**, the file is encrypted.</span></span>

<span data-ttu-id="85061-244">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="85061-244">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="85061-245">**EncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="85061-245">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85061-246">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="85061-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85061-247">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="85061-247">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85061-248">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("método de criptografia")</span><span class="sxs-lookup"><span data-stu-id="85061-248">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Encryption Method")</span></span>
</dt> </dl>

<span data-ttu-id="85061-249">Cadeia de caracteres de forma livre que identifica o algoritmo ou a ferramenta usada para criptografar um arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="85061-249">Free-form string that identifies the algorithm or tool used to encrypt a logical file.</span></span> <span data-ttu-id="85061-250">Se o esquema de criptografia não for indulged (por motivos de segurança, por exemplo), use "desconhecido".</span><span class="sxs-lookup"><span data-stu-id="85061-250">If the encryption scheme is not indulged (for security reasons, for example), use "Unknown".</span></span> <span data-ttu-id="85061-251">Se o arquivo estiver criptografado, mas seu esquema de criptografia for desconhecido ou não for divulgado, use "Encrypted".</span><span class="sxs-lookup"><span data-stu-id="85061-251">If the file is encrypted, but either its encryption scheme is unknown or not disclosed, use "Encrypted".</span></span> <span data-ttu-id="85061-252">Se o arquivo lógico não estiver criptografado, use "não criptografado".</span><span class="sxs-lookup"><span data-stu-id="85061-252">If the logical file is not encrypted, use "Not Encrypted".</span></span>

<span data-ttu-id="85061-253">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="85061-253">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="85061-254">**Extensão**</span><span class="sxs-lookup"><span data-stu-id="85061-254">**Extension**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85061-255">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="85061-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85061-256">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="85061-256">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85061-257">Qualificadores: [**fixo**](../wmisdk/standard-wmi-qualifiers.md), [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("extensão de arquivo")</span><span class="sxs-lookup"><span data-stu-id="85061-257">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File Extension")</span></span>
</dt> </dl>

<span data-ttu-id="85061-258">Extensão de nome de arquivo sem o ponto anterior (ponto).</span><span class="sxs-lookup"><span data-stu-id="85061-258">File name extension without the preceding period (dot).</span></span>

<span data-ttu-id="85061-259">Exemplo: "txt", "MOF", "mdb"</span><span class="sxs-lookup"><span data-stu-id="85061-259">Example: "txt", "mof", "mdb"</span></span>

<span data-ttu-id="85061-260">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="85061-260">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="85061-261">**FileName**</span><span class="sxs-lookup"><span data-stu-id="85061-261">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85061-262">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="85061-262">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85061-263">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="85061-263">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85061-264">Qualificadores: [**fixo**](../wmisdk/standard-wmi-qualifiers.md), [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("nome do arquivo")</span><span class="sxs-lookup"><span data-stu-id="85061-264">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File Name")</span></span>
</dt> </dl>

<span data-ttu-id="85061-265">Nome do arquivo sem a extensão de nome de arquivo.</span><span class="sxs-lookup"><span data-stu-id="85061-265">File name without the file name extension.</span></span>

<span data-ttu-id="85061-266">Exemplo: "mydatafile"</span><span class="sxs-lookup"><span data-stu-id="85061-266">Example: "MyDataFile"</span></span>

<span data-ttu-id="85061-267">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="85061-267">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="85061-268">**Tamanho**</span><span class="sxs-lookup"><span data-stu-id="85061-268">**FileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85061-269">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="85061-269">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="85061-270">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="85061-270">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85061-271">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("tamanho"), [**unidades**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="85061-271">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Size"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="85061-272">Tamanho do arquivo, em bytes.</span><span class="sxs-lookup"><span data-stu-id="85061-272">Size of the file, in bytes.</span></span>

<span data-ttu-id="85061-273">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="85061-273">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

<span data-ttu-id="85061-274">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="85061-274">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="85061-275">**Talvez**</span><span class="sxs-lookup"><span data-stu-id="85061-275">**FileType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85061-276">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="85061-276">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85061-277">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="85061-277">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85061-278">Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("tipo de arquivo")</span><span class="sxs-lookup"><span data-stu-id="85061-278">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File Type")</span></span>
</dt> </dl>

<span data-ttu-id="85061-279">Descritor que representa o tipo de arquivo indicado pela propriedade de **extensão** .</span><span class="sxs-lookup"><span data-stu-id="85061-279">Descriptor that represents the file type indicated by the **Extension** property.</span></span>

<span data-ttu-id="85061-280">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="85061-280">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="85061-281">**FSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="85061-281">**FSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85061-282">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="85061-282">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85061-283">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="85061-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85061-284">Qualificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ sistema de arquivos CIM**](cim-filesystem.md).**CreationClassName**"), [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" nome da classe do sistema de arquivos ")</span><span class="sxs-lookup"><span data-stu-id="85061-284">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_FileSystem**](cim-filesystem.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="85061-285">Classe do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="85061-285">Class of the file system.</span></span>

<span data-ttu-id="85061-286">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="85061-286">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="85061-287">**FSName**</span><span class="sxs-lookup"><span data-stu-id="85061-287">**FSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85061-288">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="85061-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85061-289">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="85061-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85061-290">Qualificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ sistema de arquivos CIM**](cim-filesystem.md).**Name**"), [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" nome do sistema de arquivos ")</span><span class="sxs-lookup"><span data-stu-id="85061-290">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_FileSystem**](cim-filesystem.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File System Name")</span></span>
</dt> </dl>

<span data-ttu-id="85061-291">Nome do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="85061-291">Name of the file system.</span></span>

<span data-ttu-id="85061-292">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="85061-292">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="85061-293">**Oculto**</span><span class="sxs-lookup"><span data-stu-id="85061-293">**Hidden**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85061-294">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="85061-294">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="85061-295">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="85061-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85061-296">Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Hidden")</span><span class="sxs-lookup"><span data-stu-id="85061-296">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Hidden")</span></span>
</dt> </dl>

<span data-ttu-id="85061-297">Se for **true**, o arquivo ficará oculto.</span><span class="sxs-lookup"><span data-stu-id="85061-297">If **True**, the file is hidden.</span></span>

<span data-ttu-id="85061-298">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="85061-298">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="85061-299">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="85061-299">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85061-300">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="85061-300">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="85061-301">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="85061-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85061-302">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="85061-302">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="85061-303">Indica quando o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="85061-303">Indicates when the object was installed.</span></span> <span data-ttu-id="85061-304">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="85061-304">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="85061-305">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="85061-305">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="85061-306">**InUseCount**</span><span class="sxs-lookup"><span data-stu-id="85061-306">**InUseCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85061-307">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="85061-307">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="85061-308">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="85061-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85061-309">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("contagem de abertura de arquivo atual")</span><span class="sxs-lookup"><span data-stu-id="85061-309">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Current File Open Count")</span></span>
</dt> </dl>

<span data-ttu-id="85061-310">Número de "aberturas de arquivo" que estão atualmente ativos no arquivo.</span><span class="sxs-lookup"><span data-stu-id="85061-310">Number of "file opens" that are currently active against the file.</span></span>

<span data-ttu-id="85061-311">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="85061-311">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

<span data-ttu-id="85061-312">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="85061-312">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="85061-313">**LastAccessed**</span><span class="sxs-lookup"><span data-stu-id="85061-313">**LastAccessed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85061-314">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="85061-314">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="85061-315">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="85061-315">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85061-316">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("último acesso")</span><span class="sxs-lookup"><span data-stu-id="85061-316">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Last Accessed")</span></span>
</dt> </dl>

<span data-ttu-id="85061-317">Data e hora do último acesso ao arquivo.</span><span class="sxs-lookup"><span data-stu-id="85061-317">Date and time the file was last accessed.</span></span>

<span data-ttu-id="85061-318">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="85061-318">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="85061-319">**LastModified**</span><span class="sxs-lookup"><span data-stu-id="85061-319">**LastModified**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85061-320">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="85061-320">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="85061-321">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="85061-321">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85061-322">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("última modificação")</span><span class="sxs-lookup"><span data-stu-id="85061-322">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Last Modified")</span></span>
</dt> </dl>

<span data-ttu-id="85061-323">Data e hora da última modificação do arquivo.</span><span class="sxs-lookup"><span data-stu-id="85061-323">Date and time the file was last modified.</span></span>

<span data-ttu-id="85061-324">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="85061-324">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="85061-325">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="85061-325">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85061-326">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="85061-326">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85061-327">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="85061-327">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85061-328">Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("fabricante")</span><span class="sxs-lookup"><span data-stu-id="85061-328">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Manufacturer")</span></span>
</dt> </dl>

<span data-ttu-id="85061-329">Cadeia de caracteres do fabricante do recurso de versão (se houver um).</span><span class="sxs-lookup"><span data-stu-id="85061-329">Manufacturer string from the version resource (if one is present).</span></span>

<span data-ttu-id="85061-330">Esta propriedade é herdada [**do \_ arquivo**](cim-datafile.md)de propriedades CIM.</span><span class="sxs-lookup"><span data-stu-id="85061-330">This property is inherited from [**CIM\_DataFile**](cim-datafile.md).</span></span>

</dd> <dt>

<span data-ttu-id="85061-331">**Nome**</span><span class="sxs-lookup"><span data-stu-id="85061-331">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85061-332">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="85061-332">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85061-333">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="85061-333">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85061-334">Qualificadores: [ **chave**](../wmisdk/key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="85061-334">Qualifiers: [**Key**](../wmisdk/key-qualifier.md)</span></span>
</dt> </dl>

<span data-ttu-id="85061-335">A propriedade Name é uma cadeia de caracteres que representa o nome herdado que serve como uma chave de uma instância de arquivo lógico em um sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="85061-335">The Name property is a string representing the inherited name that serves as a key of a logical file instance within a file system.</span></span> <span data-ttu-id="85061-336">Devem ser fornecidos nomes de caminho completos.</span><span class="sxs-lookup"><span data-stu-id="85061-336">Full path names should be provided.</span></span>

<span data-ttu-id="85061-337">Exemplo: C: \\ \\ sistema Windows \\win.ini</span><span class="sxs-lookup"><span data-stu-id="85061-337">Example: C:\\Windows\\system\\win.ini</span></span>

<span data-ttu-id="85061-338">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="85061-338">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="85061-339">**Caminho**</span><span class="sxs-lookup"><span data-stu-id="85061-339">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85061-340">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="85061-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85061-341">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="85061-341">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85061-342">Qualificadores: [**fixo**](../wmisdk/standard-wmi-qualifiers.md), [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Path")</span><span class="sxs-lookup"><span data-stu-id="85061-342">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Path")</span></span>
</dt> </dl>

<span data-ttu-id="85061-343">Caminho do arquivo, incluindo as barras invertidas à esquerda e à direita.</span><span class="sxs-lookup"><span data-stu-id="85061-343">Path of the file including the leading and trailing backslashes.</span></span>

<span data-ttu-id="85061-344">Exemplo: " \\ sistema do Windows \\ \\ "</span><span class="sxs-lookup"><span data-stu-id="85061-344">Example: "\\windows\\system\\"</span></span>

<span data-ttu-id="85061-345">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="85061-345">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="85061-346">**Seres**</span><span class="sxs-lookup"><span data-stu-id="85061-346">**Readable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85061-347">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="85061-347">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="85061-348">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="85061-348">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85061-349">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("legível")</span><span class="sxs-lookup"><span data-stu-id="85061-349">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Readable")</span></span>
</dt> </dl>

<span data-ttu-id="85061-350">Se **for true**, o arquivo poderá ser lido.</span><span class="sxs-lookup"><span data-stu-id="85061-350">If **True**, the file can be read.</span></span>

<span data-ttu-id="85061-351">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="85061-351">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="85061-352">**Status**</span><span class="sxs-lookup"><span data-stu-id="85061-352">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85061-353">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="85061-353">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85061-354">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="85061-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85061-355">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="85061-355">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="85061-356">Cadeia de caracteres que indica o status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="85061-356">String that indicates the current status of the object.</span></span> <span data-ttu-id="85061-357">O status operacional e não operacional pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="85061-357">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="85061-358">O status operacional pode incluir "OK", "degradado" e "Pred falha".</span><span class="sxs-lookup"><span data-stu-id="85061-358">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="85061-359">"Pred Fail" indica que um elemento está funcionando corretamente, mas está prevendo uma falha (por exemplo, uma unidade de disco rígido habilitada para inteligente).</span><span class="sxs-lookup"><span data-stu-id="85061-359">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="85061-360">O status não operacional pode incluir "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="85061-360">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="85061-361">O "serviço" pode ser aplicado durante o espelhamento de disco – reprateando, recarregando uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="85061-361">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="85061-362">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="85061-362">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="85061-363">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="85061-363">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="85061-364">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="85061-364">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="85061-365">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="85061-365">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="85061-366">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="85061-366">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="85061-367">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="85061-367">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="85061-368">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="85061-368">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="85061-369">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="85061-369">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="85061-370">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="85061-370">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="85061-371">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="85061-371">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="85061-372">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="85061-372">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="85061-373">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="85061-373">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="85061-374">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="85061-374">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="85061-375">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="85061-375">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="85061-376">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="85061-376">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="85061-377">**System**</span><span class="sxs-lookup"><span data-stu-id="85061-377">**System**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85061-378">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="85061-378">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="85061-379">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="85061-379">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85061-380">Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("arquivo do sistema")</span><span class="sxs-lookup"><span data-stu-id="85061-380">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("System File")</span></span>
</dt> </dl>

<span data-ttu-id="85061-381">Se for **true**, o arquivo será um arquivo do sistema.</span><span class="sxs-lookup"><span data-stu-id="85061-381">If **True**, the file is a system file.</span></span>

<span data-ttu-id="85061-382">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="85061-382">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="85061-383">**Target (destino)**</span><span class="sxs-lookup"><span data-stu-id="85061-383">**Target**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85061-384">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="85061-384">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85061-385">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="85061-385">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85061-386">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| \_ beginthreadex")</span><span class="sxs-lookup"><span data-stu-id="85061-386">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|\_beginthreadex")</span></span>
</dt> </dl>

<span data-ttu-id="85061-387">Nome do objeto para o qual este é um atalho.</span><span class="sxs-lookup"><span data-stu-id="85061-387">Name of the object that this is a shortcut to.</span></span>

</dd> <dt>

<span data-ttu-id="85061-388">**Versão**</span><span class="sxs-lookup"><span data-stu-id="85061-388">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85061-389">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="85061-389">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85061-390">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="85061-390">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85061-391">Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Version")</span><span class="sxs-lookup"><span data-stu-id="85061-391">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Version")</span></span>
</dt> </dl>

<span data-ttu-id="85061-392">Cadeia de caracteres da versão do recurso de versão (se houver uma).</span><span class="sxs-lookup"><span data-stu-id="85061-392">Version string from the version resource (if one is present).</span></span>

<span data-ttu-id="85061-393">Esta propriedade é herdada [**do \_ arquivo**](cim-datafile.md)de propriedades CIM.</span><span class="sxs-lookup"><span data-stu-id="85061-393">This property is inherited from [**CIM\_DataFile**](cim-datafile.md).</span></span>

</dd> <dt>

<span data-ttu-id="85061-394">**Gravável**</span><span class="sxs-lookup"><span data-stu-id="85061-394">**Writeable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85061-395">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="85061-395">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="85061-396">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="85061-396">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85061-397">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("gravável")</span><span class="sxs-lookup"><span data-stu-id="85061-397">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Writeable")</span></span>
</dt> </dl>

<span data-ttu-id="85061-398">Se **for true**, o arquivo poderá ser gravado.</span><span class="sxs-lookup"><span data-stu-id="85061-398">If **True**, the file can be written.</span></span>

<span data-ttu-id="85061-399">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="85061-399">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="85061-400">Comentários</span><span class="sxs-lookup"><span data-stu-id="85061-400">Remarks</span></span>

<span data-ttu-id="85061-401">A **classe \_ shortcutfile do Win32** é derivada de [**CIM \_ DataFile**](cim-datafile.md).</span><span class="sxs-lookup"><span data-stu-id="85061-401">The **Win32\_ShortcutFile** class is derived from [**CIM\_DataFile**](cim-datafile.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="85061-402">Requisitos</span><span class="sxs-lookup"><span data-stu-id="85061-402">Requirements</span></span>



| <span data-ttu-id="85061-403">Requisito</span><span class="sxs-lookup"><span data-stu-id="85061-403">Requirement</span></span> | <span data-ttu-id="85061-404">Valor</span><span class="sxs-lookup"><span data-stu-id="85061-404">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="85061-405">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="85061-405">Minimum supported client</span></span><br/> | <span data-ttu-id="85061-406">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="85061-406">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="85061-407">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="85061-407">Minimum supported server</span></span><br/> | <span data-ttu-id="85061-408">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="85061-408">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="85061-409">Namespace</span><span class="sxs-lookup"><span data-stu-id="85061-409">Namespace</span></span><br/>                | <span data-ttu-id="85061-410">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="85061-410">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="85061-411">MOF</span><span class="sxs-lookup"><span data-stu-id="85061-411">MOF</span></span><br/>                      | <dl> <span data-ttu-id="85061-412"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="85061-412"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="85061-413">DLL</span><span class="sxs-lookup"><span data-stu-id="85061-413">DLL</span></span><br/>                      | <dl> <span data-ttu-id="85061-414"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="85061-414"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85061-415">Confira também</span><span class="sxs-lookup"><span data-stu-id="85061-415">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85061-416">**DataFile de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="85061-416">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="85061-417">Classes do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="85061-417">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
