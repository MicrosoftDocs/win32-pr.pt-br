---
description: O codec do Win32 \_&\# 32; A classe WMI representa o codec de áudio ou vídeo instalado no sistema de computador.
ms.assetid: 48ea3b92-0ea1-4aba-b067-bce0ec356cd2
ms.tgt_platform: multiple
title: Classe Win32_CodecFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile
- Win32_CodecFile.AccessMask
- Win32_CodecFile.Archive
- Win32_CodecFile.Caption
- Win32_CodecFile.Compressed
- Win32_CodecFile.CompressionMethod
- Win32_CodecFile.CreationClassName
- Win32_CodecFile.CreationDate
- Win32_CodecFile.CSCreationClassName
- Win32_CodecFile.CSName
- Win32_CodecFile.Description
- Win32_CodecFile.Drive
- Win32_CodecFile.EightDotThreeFileName
- Win32_CodecFile.Encrypted
- Win32_CodecFile.EncryptionMethod
- Win32_CodecFile.Extension
- Win32_CodecFile.FileName
- Win32_CodecFile.FileSize
- Win32_CodecFile.FileType
- Win32_CodecFile.FSCreationClassName
- Win32_CodecFile.FSName
- Win32_CodecFile.Group
- Win32_CodecFile.Hidden
- Win32_CodecFile.InstallDate
- Win32_CodecFile.InUseCount
- Win32_CodecFile.LastAccessed
- Win32_CodecFile.LastModified
- Win32_CodecFile.Manufacturer
- Win32_CodecFile.Name
- Win32_CodecFile.Path
- Win32_CodecFile.Readable
- Win32_CodecFile.Status
- Win32_CodecFile.System
- Win32_CodecFile.Version
- Win32_CodecFile.Writeable
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fc7a6073ab2841fde4492cd59ae1696aeca9f6a7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089471"
---
# <a name="win32_codecfile-class"></a><span data-ttu-id="5b994-103">Classe de codec do Win32 \_</span><span class="sxs-lookup"><span data-stu-id="5b994-103">Win32\_CodecFile class</span></span>

<span data-ttu-id="5b994-104">A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de **\_ codec do win32file** representa o codec de áudio ou vídeo instalado no sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="5b994-104">The **Win32\_CodecFile** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the audio or video codec installed on the computer system.</span></span> <span data-ttu-id="5b994-105">Os codecs convertem um tipo de formato de mídia para outro, normalmente um formato compactado para um formato descompactado.</span><span class="sxs-lookup"><span data-stu-id="5b994-105">Codecs convert one media format type to another, typically a compressed format to an uncompressed format.</span></span> <span data-ttu-id="5b994-106">O nome "codec" é derivado de uma combinação de compactar e descompactar.</span><span class="sxs-lookup"><span data-stu-id="5b994-106">The name "codec" is derived from a combination of compress and decompress.</span></span> <span data-ttu-id="5b994-107">Por exemplo, um codec pode converter um formato compactado, como o MS-ADPCM, em um formato descompactado, como o PCM, que a maioria dos hardwares de áudio pode reproduzir diretamente.</span><span class="sxs-lookup"><span data-stu-id="5b994-107">For example, a codec can convert a compressed format, such as MS-ADPCM, to an uncompressed format such as PCM, which most audio hardware can play directly.</span></span>

<span data-ttu-id="5b994-108">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="5b994-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="5b994-109">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="5b994-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b994-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5b994-110">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4C3-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_CodecFile : CIM_DataFile
{
  uint32   AccessMask;
  boolean  Archive;
  string   Caption;
  boolean  Compressed;
  string   CompressionMethod;
  string   CreationClassName;
  datetime CreationDate;
  string   CSCreationClassName;
  string   CSName;
  string   Description;
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
  string   Group;
  boolean  Hidden;
  datetime InstallDate;
  uint64   InUseCount;
  datetime LastAccessed;
  datetime LastModified;
  string   Manufacturer;
  string   Name;
  string   Path;
  boolean  Readable;
  string   Status;
  boolean  System;
  string   Version;
  boolean  Writeable;
};
```

## <a name="members"></a><span data-ttu-id="5b994-111">Membros</span><span class="sxs-lookup"><span data-stu-id="5b994-111">Members</span></span>

<span data-ttu-id="5b994-112">A classe de um **\_ codec do Win32** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="5b994-112">The **Win32\_CodecFile** class has these types of members:</span></span>

-   [<span data-ttu-id="5b994-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="5b994-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="5b994-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5b994-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="5b994-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="5b994-115">Methods</span></span>

<span data-ttu-id="5b994-116">A classe de um **\_ codec do Win32** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="5b994-116">The **Win32\_CodecFile** class has these methods.</span></span>



| <span data-ttu-id="5b994-117">Método</span><span class="sxs-lookup"><span data-stu-id="5b994-117">Method</span></span>                                                                                             | <span data-ttu-id="5b994-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="5b994-118">Description</span></span>                                                                                                                                                                                                            |
|:---------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5b994-119">**ChangeSecurityPermissions**</span><span class="sxs-lookup"><span data-stu-id="5b994-119">**ChangeSecurityPermissions**</span></span>](changesecuritypermissions-method-in-class-win32-codecfile.md)     | <span data-ttu-id="5b994-120">Altera as permissões de segurança para o arquivo lógico especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="5b994-120">Changes the security permissions for the logical file specified in the object path.</span></span><br/>                                                                                                                         |
| [<span data-ttu-id="5b994-121">**ChangeSecurityPermissionsEx**</span><span class="sxs-lookup"><span data-stu-id="5b994-121">**ChangeSecurityPermissionsEx**</span></span>](changesecuritypermissionsex-method-in-class-win32-codecfile.md) | <span data-ttu-id="5b994-122">Altera as permissões de segurança para o arquivo lógico especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="5b994-122">Changes the security permissions for the logical file specified in the object path.</span></span><br/>                                                                                                                         |
| [<span data-ttu-id="5b994-123">**Compactar**</span><span class="sxs-lookup"><span data-stu-id="5b994-123">**Compress**</span></span>](compress-method-in-class-win32-codecfile.md)                                       | <span data-ttu-id="5b994-124">Compacta o arquivo lógico (ou diretório) especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="5b994-124">Compresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                    |
| [<span data-ttu-id="5b994-125">**CompressEx**</span><span class="sxs-lookup"><span data-stu-id="5b994-125">**CompressEx**</span></span>](compressex-method-in-class-win32-codecfile.md)                                   | <span data-ttu-id="5b994-126">Compacta o arquivo lógico (ou diretório) especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="5b994-126">Compresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                    |
| [<span data-ttu-id="5b994-127">**Copiar**</span><span class="sxs-lookup"><span data-stu-id="5b994-127">**Copy**</span></span>](copy-method-in-class-win32-codecfile.md)                                               | <span data-ttu-id="5b994-128">Copia o arquivo ou diretório lógico especificado no caminho do objeto para o local especificado pelo parâmetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="5b994-128">Copies the logical file or directory specified in the object path to the location specified by the input parameter.</span></span><br/>                                                                                         |
| [<span data-ttu-id="5b994-129">**CopyEx**</span><span class="sxs-lookup"><span data-stu-id="5b994-129">**CopyEx**</span></span>](copyex-method-in-class-win32-codecfile.md)                                           | <span data-ttu-id="5b994-130">Método de classe que copia o arquivo ou diretório lógico especificado no caminho do objeto para o local especificado pelo parâmetro FileName.</span><span class="sxs-lookup"><span data-stu-id="5b994-130">Class method that copies the logical file or directory specified in the object path to the location specified by the FileName parameter.</span></span><br/>                                                                    |
| [<span data-ttu-id="5b994-131">**Excluir**</span><span class="sxs-lookup"><span data-stu-id="5b994-131">**Delete**</span></span>](delete-method-in-class-win32-codecfile.md)                                           | <span data-ttu-id="5b994-132">Exclui o arquivo lógico (ou diretório) especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="5b994-132">Deletes the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                       |
| [<span data-ttu-id="5b994-133">**DeleteEx**</span><span class="sxs-lookup"><span data-stu-id="5b994-133">**DeleteEx**</span></span>](deleteex-method-in-class-win32-codecfile.md)                                       | <span data-ttu-id="5b994-134">Exclui o arquivo lógico (ou diretório) especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="5b994-134">Deletes the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                       |
| [<span data-ttu-id="5b994-135">**GetEffectivePermission**</span><span class="sxs-lookup"><span data-stu-id="5b994-135">**GetEffectivePermission**</span></span>](geteffectivepermission-method-in-class-win32-codecfile.md)           | <span data-ttu-id="5b994-136">Determina se o chamador tem as permissões agregadas especificadas pelo argumento de **permissão** não apenas no objeto de arquivo, mas no compartilhamento o arquivo ou diretório reside (se estiver em um compartilhamento).</span><span class="sxs-lookup"><span data-stu-id="5b994-136">Determines whether the caller has the aggregated permissions specified by the **permission** argument not only on the file object, but on the share the file or directory resides on (if it is on a share).</span></span><br/> |
| [<span data-ttu-id="5b994-137">**Renomear**</span><span class="sxs-lookup"><span data-stu-id="5b994-137">**Rename**</span></span>](rename-method-in-class-win32-codecfile.md)                                           | <span data-ttu-id="5b994-138">Método de classe que renomeia o arquivo lógico (ou diretório) especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="5b994-138">Class method that renames the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                     |
| [<span data-ttu-id="5b994-139">**TakeOwnerShip**</span><span class="sxs-lookup"><span data-stu-id="5b994-139">**TakeOwnerShip**</span></span>](takeownership-method-in-class-win32-codecfile.md)                             | <span data-ttu-id="5b994-140">Obtém a propriedade do arquivo lógico especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="5b994-140">Obtains ownership of the logical file specified in the object path.</span></span><br/>                                                                                                                                         |
| [<span data-ttu-id="5b994-141">**TakeOwnerShipEx**</span><span class="sxs-lookup"><span data-stu-id="5b994-141">**TakeOwnerShipEx**</span></span>](takeownershipex-method-in-class-win32-codecfile.md)                         | <span data-ttu-id="5b994-142">Método de classe que obtém a propriedade do arquivo lógico especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="5b994-142">Class method that obtains ownership of the logical file specified in the object path.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="5b994-143">**Descompactar**</span><span class="sxs-lookup"><span data-stu-id="5b994-143">**Uncompress**</span></span>](uncompress-method-in-class-win32-codecfile.md)                                   | <span data-ttu-id="5b994-144">Descompacta o arquivo lógico (ou diretório) especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="5b994-144">Uncompresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="5b994-145">**UncompressEx**</span><span class="sxs-lookup"><span data-stu-id="5b994-145">**UncompressEx**</span></span>](uncompressex-method-in-class-win32-codecfile.md)                               | <span data-ttu-id="5b994-146">Descompacta o arquivo lógico (ou diretório) especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="5b994-146">Uncompresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                  |



 

### <a name="properties"></a><span data-ttu-id="5b994-147">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5b994-147">Properties</span></span>

<span data-ttu-id="5b994-148">A classe de um **\_ codec do Win32** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="5b994-148">The **Win32\_CodecFile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5b994-149">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="5b994-149">**AccessMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b994-150">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5b994-150">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5b994-151">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5b994-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b994-152">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("direitos de acesso")</span><span class="sxs-lookup"><span data-stu-id="5b994-152">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Access Rights")</span></span>
</dt> </dl>

<span data-ttu-id="5b994-153">Bitmask que representa os direitos de acesso necessários para acessar ou executar operações específicas no arquivo de codec.</span><span class="sxs-lookup"><span data-stu-id="5b994-153">Bitmask that represents the access rights required to access or perform specific operations on the codec file.</span></span> <span data-ttu-id="5b994-154">Para valores de bit, consulte [**constantes de direitos de acesso de arquivo e diretório**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants).</span><span class="sxs-lookup"><span data-stu-id="5b994-154">For bit values, see [**File and Directory Access Rights Constants**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants).</span></span>

> [!Note]  
> <span data-ttu-id="5b994-155">Em volumes FAT, o valor de **\_ acesso completo** é retornado, o que indica que nenhuma segurança foi definida no objeto.</span><span class="sxs-lookup"><span data-stu-id="5b994-155">On FAT volumes, the **FULL\_ACCESS** value is returned instead, which indicates no security has been set on the object.</span></span>

 

<span data-ttu-id="5b994-156">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="5b994-156">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="5b994-157">Do **arquivo \_ LER \_ os dados (arquivo) ou \_ \_ diretório de lista de arquivos (diretório)** (1)</span><span class="sxs-lookup"><span data-stu-id="5b994-157">**FILE\_READ\_DATA (file) or FILE\_LIST\_DIRECTORY (directory)** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="5b994-158">Do **arquivo \_ GRAVAR \_ dados (arquivo) ou arquivo \_ Adicionar \_ arquivo (diretório)** (2)</span><span class="sxs-lookup"><span data-stu-id="5b994-158">**FILE\_WRITE\_DATA (file) or FILE\_ADD\_FILE (directory)** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="5b994-159">Do **arquivo \_ ACRESCENTAR \_ dados (arquivo) ou arquivo \_ Adicionar \_ subdiretório (diretório)** (4)</span><span class="sxs-lookup"><span data-stu-id="5b994-159">**FILE\_APPEND\_DATA (file) or FILE\_ADD\_SUBDIRECTORY (directory)** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="5b994-160">Do **arquivo \_ LER \_ ea** (8)</span><span class="sxs-lookup"><span data-stu-id="5b994-160">**FILE\_READ\_EA** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="5b994-161">Do **arquivo \_ GRAVAR \_ ea** (16)</span><span class="sxs-lookup"><span data-stu-id="5b994-161">**FILE\_WRITE\_EA** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

<span data-ttu-id="5b994-162">Do **arquivo \_ EXECUTAR (arquivo) ou \_ atravessamento de arquivo (diretório)** (32)</span><span class="sxs-lookup"><span data-stu-id="5b994-162">**FILE\_EXECUTE (file) or FILE\_TRAVERSE (directory)** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="5b994-163">Do **arquivo \_ EXCLUIR \_ filho (diretório)** (64)</span><span class="sxs-lookup"><span data-stu-id="5b994-163">**FILE\_DELETE\_CHILD (directory)** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="5b994-164">Do **arquivo \_ \_Atributos de leitura** (128)</span><span class="sxs-lookup"><span data-stu-id="5b994-164">**FILE\_READ\_ATTRIBUTES** (128)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="5b994-165">Do **arquivo \_ \_Atributos de gravação** (256)</span><span class="sxs-lookup"><span data-stu-id="5b994-165">**FILE\_WRITE\_ATTRIBUTES** (256)</span></span>


</dt> <dd></dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="5b994-166">**Excluir** (65536)</span><span class="sxs-lookup"><span data-stu-id="5b994-166">**DELETE** (65536)</span></span>


</dt> <dd></dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="5b994-167">**Ler \_ CONTROLE** (131072)</span><span class="sxs-lookup"><span data-stu-id="5b994-167">**READ\_CONTROL** (131072)</span></span>


</dt> <dd></dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="5b994-168">**Gravar \_ DAC** (262144)</span><span class="sxs-lookup"><span data-stu-id="5b994-168">**WRITE\_DAC** (262144)</span></span>


</dt> <dd></dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="5b994-169">**Gravar \_ PROPRIETÁRIO** (524288)</span><span class="sxs-lookup"><span data-stu-id="5b994-169">**WRITE\_OWNER** (524288)</span></span>


</dt> <dd></dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="5b994-170">**Sincronizar** (1048576)</span><span class="sxs-lookup"><span data-stu-id="5b994-170">**SYNCHRONIZE** (1048576)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5b994-171">**Arquivar**</span><span class="sxs-lookup"><span data-stu-id="5b994-171">**Archive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b994-172">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="5b994-172">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5b994-173">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5b994-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b994-174">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("deve ser arquivado")</span><span class="sxs-lookup"><span data-stu-id="5b994-174">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Should Be Archived")</span></span>
</dt> </dl>

<span data-ttu-id="5b994-175">Se **for true**, o arquivo deverá ser arquivado.</span><span class="sxs-lookup"><span data-stu-id="5b994-175">If **True**, the file should be archived.</span></span>

<span data-ttu-id="5b994-176">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="5b994-176">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="5b994-177">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="5b994-177">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b994-178">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5b994-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b994-179">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5b994-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b994-180">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="5b994-180">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="5b994-181">Breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="5b994-181">Short description of the object.</span></span>

<span data-ttu-id="5b994-182">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5b994-182">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5b994-183">**Compactado**</span><span class="sxs-lookup"><span data-stu-id="5b994-183">**Compressed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b994-184">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="5b994-184">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5b994-185">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5b994-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b994-186">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("compactado")</span><span class="sxs-lookup"><span data-stu-id="5b994-186">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compressed")</span></span>
</dt> </dl>

<span data-ttu-id="5b994-187">Se **for true**, o arquivo será compactado.</span><span class="sxs-lookup"><span data-stu-id="5b994-187">If **True**, the file is compressed.</span></span>

<span data-ttu-id="5b994-188">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="5b994-188">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="5b994-189">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="5b994-189">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b994-190">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5b994-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b994-191">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5b994-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b994-192">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("método de compactação")</span><span class="sxs-lookup"><span data-stu-id="5b994-192">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compression Method")</span></span>
</dt> </dl>

<span data-ttu-id="5b994-193">Algoritmo ou ferramenta usada para compactar o arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="5b994-193">Algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="5b994-194">Se não for possível (ou não desejar) descrever o esquema de compactação (talvez porque não seja conhecido), use as seguintes palavras: "desconhecido" para representar que não é conhecido se o arquivo lógico está compactado ou não; "Compactado" para representar que o arquivo está compactado, mas o seu esquema de compactação não é conhecido ou não foi divulgado; e "não compactado" para representar que o arquivo lógico não está compactado.</span><span class="sxs-lookup"><span data-stu-id="5b994-194">If it is not possible (or not desired) to describe the compression scheme (perhaps because it is not known), use the following words: "Unknown" to represent that it is not known whether the logical file is compressed or not; "Compressed" to represent that the file is compressed but either its compression scheme is not known or not disclosed; and "Not Compressed" to represent that the logical file is not compressed.</span></span>

<span data-ttu-id="5b994-195">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="5b994-195">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="5b994-196">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="5b994-196">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b994-197">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5b994-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b994-198">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5b994-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b994-199">Qualificadores: [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nome da classe")</span><span class="sxs-lookup"><span data-stu-id="5b994-199">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="5b994-200">Nome da primeira classe concreta a ser exibida na cadeia de herança usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="5b994-200">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="5b994-201">Quando usado com as outras propriedades de chave da classe, a propriedade permite que todas as instâncias dessa classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="5b994-201">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="5b994-202">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="5b994-202">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="5b994-203">**CreationDate**</span><span class="sxs-lookup"><span data-stu-id="5b994-203">**CreationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b994-204">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5b994-204">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5b994-205">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5b994-205">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b994-206">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("data de criação")</span><span class="sxs-lookup"><span data-stu-id="5b994-206">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Creation Date")</span></span>
</dt> </dl>

<span data-ttu-id="5b994-207">Data de criação do arquivo.</span><span class="sxs-lookup"><span data-stu-id="5b994-207">File creation date.</span></span>

<span data-ttu-id="5b994-208">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="5b994-208">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="5b994-209">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="5b994-209">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b994-210">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5b994-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b994-211">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5b994-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b994-212">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema de arquivos CIM**](cim-filesystem.md).**CSCreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome da classe do sistema de computador ")</span><span class="sxs-lookup"><span data-stu-id="5b994-212">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSCreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="5b994-213">Classe do sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="5b994-213">Class of the computer system.</span></span>

<span data-ttu-id="5b994-214">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="5b994-214">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="5b994-215">**CSName**</span><span class="sxs-lookup"><span data-stu-id="5b994-215">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b994-216">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5b994-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b994-217">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5b994-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b994-218">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema de arquivos CIM**](cim-filesystem.md).**CSName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome do sistema de computador ")</span><span class="sxs-lookup"><span data-stu-id="5b994-218">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Name")</span></span>
</dt> </dl>

<span data-ttu-id="5b994-219">Cadeia de caracteres que representa o nome do sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="5b994-219">String representing the name of the computer system.</span></span>

<span data-ttu-id="5b994-220">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="5b994-220">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="5b994-221">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="5b994-221">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b994-222">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5b994-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b994-223">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5b994-223">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b994-224">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (descrição), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry do \| sistema \\ \\ CurrentControlSet \\ \\ Control \\ \\ MediaResources \\ \\ ICM \| Descrição")</span><span class="sxs-lookup"><span data-stu-id="5b994-224">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) (Description), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|System\\\\CurrentControlSet\\\\control\\\\MediaResources\\\\icm\|Description")</span></span>
</dt> </dl>

<span data-ttu-id="5b994-225">Nome completo do driver do codec.</span><span class="sxs-lookup"><span data-stu-id="5b994-225">Full name of the codec driver.</span></span> <span data-ttu-id="5b994-226">Esta cadeia de caracteres deve ser exibida em espaços grandes (descritivos).</span><span class="sxs-lookup"><span data-stu-id="5b994-226">This string is intended to be displayed in large (descriptive) spaces.</span></span>

<span data-ttu-id="5b994-227">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5b994-227">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="5b994-228">Exemplo: "conversor de PCM da Microsoft"</span><span class="sxs-lookup"><span data-stu-id="5b994-228">Example: "Microsoft PCM Converter"</span></span>

</dd> <dt>

<span data-ttu-id="5b994-229">**Unidade**</span><span class="sxs-lookup"><span data-stu-id="5b994-229">**Drive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b994-230">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5b994-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b994-231">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5b994-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b994-232">Qualificadores: [**fixo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("drive")</span><span class="sxs-lookup"><span data-stu-id="5b994-232">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Drive")</span></span>
</dt> </dl>

<span data-ttu-id="5b994-233">Letra da unidade (incluindo dois-pontos) do arquivo.</span><span class="sxs-lookup"><span data-stu-id="5b994-233">Drive letter (including colon) of the file.</span></span>

<span data-ttu-id="5b994-234">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="5b994-234">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="5b994-235">Exemplo: "c:"</span><span class="sxs-lookup"><span data-stu-id="5b994-235">Example: "c:"</span></span>

</dd> <dt>

<span data-ttu-id="5b994-236">**EightDotThreeFileName**</span><span class="sxs-lookup"><span data-stu-id="5b994-236">**EightDotThreeFileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b994-237">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5b994-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b994-238">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5b994-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b994-239">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("oito pontos três nome de arquivo")</span><span class="sxs-lookup"><span data-stu-id="5b994-239">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Eight Dot Three File Name")</span></span>
</dt> </dl>

<span data-ttu-id="5b994-240">Nome de arquivo compatível com o DOS para este arquivo.</span><span class="sxs-lookup"><span data-stu-id="5b994-240">DOS-compatible file name for this file.</span></span>

<span data-ttu-id="5b994-241">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="5b994-241">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="5b994-242">Exemplo: "c: \\ progra ~ 1"</span><span class="sxs-lookup"><span data-stu-id="5b994-242">Example: "c:\\progra~1"</span></span>

</dd> <dt>

<span data-ttu-id="5b994-243">**Criptografado**</span><span class="sxs-lookup"><span data-stu-id="5b994-243">**Encrypted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b994-244">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="5b994-244">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5b994-245">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5b994-245">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b994-246">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encrypted")</span><span class="sxs-lookup"><span data-stu-id="5b994-246">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encrypted")</span></span>
</dt> </dl>

<span data-ttu-id="5b994-247">Se **for true**, o arquivo será criptografado.</span><span class="sxs-lookup"><span data-stu-id="5b994-247">If **True**, the file is encrypted.</span></span>

<span data-ttu-id="5b994-248">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="5b994-248">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="5b994-249">**EncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="5b994-249">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b994-250">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5b994-250">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b994-251">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5b994-251">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b994-252">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("método de criptografia")</span><span class="sxs-lookup"><span data-stu-id="5b994-252">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encryption Method")</span></span>
</dt> </dl>

<span data-ttu-id="5b994-253">Algoritmo ou ferramenta usada para criptografar o arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="5b994-253">Algorithm or tool used to encrypt the logical file.</span></span> <span data-ttu-id="5b994-254">Se não for possível (ou não desejar) descrever o esquema de criptografia (talvez por motivos de segurança), use as seguintes palavras: "desconhecido" para representar que não é conhecido se o arquivo lógico está criptografado ou não; "Encrypted" para representar que o arquivo está criptografado, mas seu esquema de criptografia não é conhecido ou não é divulgado; e "não criptografado" para representar que o arquivo lógico não está criptografado.</span><span class="sxs-lookup"><span data-stu-id="5b994-254">If it is not possible (or not desired) to describe the encryption scheme (perhaps for security reasons), use the following words: "Unknown" to represent that it is not known whether the logical file is encrypted or not; "Encrypted" to represent that the file is encrypted but either its encryption scheme is not known or not disclosed; and "Not Encrypted" to represent that the logical file is not encrypted.</span></span>

<span data-ttu-id="5b994-255">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="5b994-255">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="5b994-256">**Extensão**</span><span class="sxs-lookup"><span data-stu-id="5b994-256">**Extension**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b994-257">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5b994-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b994-258">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5b994-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b994-259">Qualificadores: [**fixo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("extensão de arquivo")</span><span class="sxs-lookup"><span data-stu-id="5b994-259">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Extension")</span></span>
</dt> </dl>

<span data-ttu-id="5b994-260">Extensão de nome de arquivo (sem o ponto).</span><span class="sxs-lookup"><span data-stu-id="5b994-260">File name extension (without the dot).</span></span>

<span data-ttu-id="5b994-261">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="5b994-261">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="5b994-262">Exemplos: "txt", "MOF", "mdb"</span><span class="sxs-lookup"><span data-stu-id="5b994-262">Examples: "txt", "mof", "mdb"</span></span>

</dd> <dt>

<span data-ttu-id="5b994-263">**FileName**</span><span class="sxs-lookup"><span data-stu-id="5b994-263">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b994-264">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5b994-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b994-265">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5b994-265">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b994-266">Qualificadores: [**fixo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nome do arquivo")</span><span class="sxs-lookup"><span data-stu-id="5b994-266">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Name")</span></span>
</dt> </dl>

<span data-ttu-id="5b994-267">Nome (sem a extensão) do arquivo.</span><span class="sxs-lookup"><span data-stu-id="5b994-267">Name (without the extension) of the file.</span></span>

<span data-ttu-id="5b994-268">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="5b994-268">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="5b994-269">Exemplo: "autoexec"</span><span class="sxs-lookup"><span data-stu-id="5b994-269">Example: "autoexec"</span></span>

</dd> <dt>

<span data-ttu-id="5b994-270">**Tamanho**</span><span class="sxs-lookup"><span data-stu-id="5b994-270">**FileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b994-271">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5b994-271">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5b994-272">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5b994-272">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b994-273">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("tamanho"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="5b994-273">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Size"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="5b994-274">Tamanho do arquivo (em bytes).</span><span class="sxs-lookup"><span data-stu-id="5b994-274">Size of the file (in bytes).</span></span>

<span data-ttu-id="5b994-275">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="5b994-275">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="5b994-276">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="5b994-276">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="5b994-277">**Talvez**</span><span class="sxs-lookup"><span data-stu-id="5b994-277">**FileType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b994-278">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5b994-278">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b994-279">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5b994-279">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b994-280">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("tipo de arquivo")</span><span class="sxs-lookup"><span data-stu-id="5b994-280">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Type")</span></span>
</dt> </dl>

<span data-ttu-id="5b994-281">Tipo de arquivo (indicado pela propriedade de **extensão** ).</span><span class="sxs-lookup"><span data-stu-id="5b994-281">File type (indicated by the **Extension** property).</span></span>

<span data-ttu-id="5b994-282">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="5b994-282">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="5b994-283">**FSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="5b994-283">**FSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b994-284">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5b994-284">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b994-285">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5b994-285">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b994-286">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema de arquivos CIM**](cim-filesystem.md).**CreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome da classe do sistema de arquivos ")</span><span class="sxs-lookup"><span data-stu-id="5b994-286">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="5b994-287">Classe do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="5b994-287">Class of the file system.</span></span>

<span data-ttu-id="5b994-288">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="5b994-288">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="5b994-289">**FSName**</span><span class="sxs-lookup"><span data-stu-id="5b994-289">**FSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b994-290">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5b994-290">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b994-291">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5b994-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b994-292">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema de arquivos CIM**](cim-filesystem.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome do sistema de arquivos ")</span><span class="sxs-lookup"><span data-stu-id="5b994-292">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Name")</span></span>
</dt> </dl>

<span data-ttu-id="5b994-293">Nome do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="5b994-293">Name of the file system.</span></span>

<span data-ttu-id="5b994-294">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="5b994-294">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="5b994-295">**Grupo**</span><span class="sxs-lookup"><span data-stu-id="5b994-295">**Group**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b994-296">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5b994-296">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b994-297">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5b994-297">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b994-298">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| software WIN32REGISTRY \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ drivers. desc")</span><span class="sxs-lookup"><span data-stu-id="5b994-298">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|SOFTWARE\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\drivers.desc")</span></span>
</dt> </dl>

<span data-ttu-id="5b994-299">Codec representado por essa classe.</span><span class="sxs-lookup"><span data-stu-id="5b994-299">Codec represented by this class.</span></span>

<span data-ttu-id="5b994-300">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="5b994-300">The values are:</span></span>

<dl> <dd><span data-ttu-id="5b994-301">Sonoro</span><span class="sxs-lookup"><span data-stu-id="5b994-301">"Audio"</span></span></dd> <dd><span data-ttu-id="5b994-302">Monitor</span><span class="sxs-lookup"><span data-stu-id="5b994-302">"Video"</span></span></dd> </dl>

<dt>

<span id="Audio"></span><span id="audio"></span><span id="AUDIO"></span>

<span data-ttu-id="5b994-303">**Áudio** ("áudio")</span><span class="sxs-lookup"><span data-stu-id="5b994-303">**Audio** ("Audio")</span></span>


</dt> <dd></dd> <dt>

<span id="Video"></span><span id="video"></span><span id="VIDEO"></span>

<span data-ttu-id="5b994-304">**Vídeo** ("vídeo")</span><span class="sxs-lookup"><span data-stu-id="5b994-304">**Video** ("Video")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5b994-305">**Oculto**</span><span class="sxs-lookup"><span data-stu-id="5b994-305">**Hidden**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b994-306">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="5b994-306">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5b994-307">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5b994-307">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b994-308">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hidden")</span><span class="sxs-lookup"><span data-stu-id="5b994-308">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hidden")</span></span>
</dt> </dl>

<span data-ttu-id="5b994-309">Se for **true**, o arquivo ficará oculto.</span><span class="sxs-lookup"><span data-stu-id="5b994-309">If **True**, the file is hidden.</span></span>

<span data-ttu-id="5b994-310">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="5b994-310">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="5b994-311">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="5b994-311">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b994-312">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5b994-312">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5b994-313">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5b994-313">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b994-314">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="5b994-314">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="5b994-315">O objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="5b994-315">Object was installed.</span></span> <span data-ttu-id="5b994-316">Essa propriedade não requer um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="5b994-316">This property does not require a value to indicate that the object is installed.</span></span>

<span data-ttu-id="5b994-317">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5b994-317">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5b994-318">**InUseCount**</span><span class="sxs-lookup"><span data-stu-id="5b994-318">**InUseCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b994-319">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5b994-319">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5b994-320">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5b994-320">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b994-321">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("contagem de abertura de arquivo atual")</span><span class="sxs-lookup"><span data-stu-id="5b994-321">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Current File Open Count")</span></span>
</dt> </dl>

<span data-ttu-id="5b994-322">Número de "aberturas de arquivo" que estão atualmente ativos no arquivo.</span><span class="sxs-lookup"><span data-stu-id="5b994-322">Number of "file opens" that are currently active against the file.</span></span>

<span data-ttu-id="5b994-323">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="5b994-323">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="5b994-324">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="5b994-324">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="5b994-325">**LastAccessed**</span><span class="sxs-lookup"><span data-stu-id="5b994-325">**LastAccessed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b994-326">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5b994-326">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5b994-327">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5b994-327">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b994-328">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("último acesso")</span><span class="sxs-lookup"><span data-stu-id="5b994-328">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Accessed")</span></span>
</dt> </dl>

<span data-ttu-id="5b994-329">O último acesso ao arquivo foi acessado.</span><span class="sxs-lookup"><span data-stu-id="5b994-329">File was last accessed.</span></span>

<span data-ttu-id="5b994-330">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="5b994-330">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="5b994-331">**LastModified**</span><span class="sxs-lookup"><span data-stu-id="5b994-331">**LastModified**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b994-332">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5b994-332">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5b994-333">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5b994-333">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b994-334">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("última modificação")</span><span class="sxs-lookup"><span data-stu-id="5b994-334">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Modified")</span></span>
</dt> </dl>

<span data-ttu-id="5b994-335">O arquivo foi modificado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="5b994-335">File was last modified.</span></span>

<span data-ttu-id="5b994-336">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="5b994-336">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="5b994-337">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="5b994-337">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b994-338">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5b994-338">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b994-339">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5b994-339">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b994-340">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("fabricante")</span><span class="sxs-lookup"><span data-stu-id="5b994-340">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Manufacturer")</span></span>
</dt> </dl>

<span data-ttu-id="5b994-341">Cadeia de caracteres do fabricante do recurso de versão, se houver um.</span><span class="sxs-lookup"><span data-stu-id="5b994-341">Manufacturer string from version resource, if one is present.</span></span>

<span data-ttu-id="5b994-342">Esta propriedade é herdada [**do \_ arquivo**](cim-datafile.md)de propriedades CIM.</span><span class="sxs-lookup"><span data-stu-id="5b994-342">This property is inherited from [**CIM\_DataFile**](cim-datafile.md).</span></span>

</dd> <dt>

<span data-ttu-id="5b994-343">**Nome**</span><span class="sxs-lookup"><span data-stu-id="5b994-343">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b994-344">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5b994-344">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b994-345">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5b994-345">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b994-346">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5b994-346">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="5b994-347">Nome herdado que serve como uma chave de uma instância de arquivo lógico em um sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="5b994-347">Inherited name that serves as a key of a logical file instance within a file system.</span></span> <span data-ttu-id="5b994-348">Devem ser fornecidos nomes de caminho completos.</span><span class="sxs-lookup"><span data-stu-id="5b994-348">Full path names should be provided.</span></span>

<span data-ttu-id="5b994-349">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5b994-349">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="5b994-350">Exemplo: "C: \\ Windows \\ System \\win.ini"</span><span class="sxs-lookup"><span data-stu-id="5b994-350">Example: "C:\\Windows\\system\\win.ini"</span></span>

</dd> <dt>

<span data-ttu-id="5b994-351">**Caminho**</span><span class="sxs-lookup"><span data-stu-id="5b994-351">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b994-352">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5b994-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b994-353">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5b994-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b994-354">Qualificadores: [**fixo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Path")</span><span class="sxs-lookup"><span data-stu-id="5b994-354">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Path")</span></span>
</dt> </dl>

<span data-ttu-id="5b994-355">Caminho do arquivo.</span><span class="sxs-lookup"><span data-stu-id="5b994-355">Path of the file.</span></span> <span data-ttu-id="5b994-356">Isso inclui barras invertidas à esquerda e à direita.</span><span class="sxs-lookup"><span data-stu-id="5b994-356">This includes leading and trailing backslashes.</span></span>

<span data-ttu-id="5b994-357">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="5b994-357">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="5b994-358">Exemplo: " \\ sistema do Windows \\ \\ "</span><span class="sxs-lookup"><span data-stu-id="5b994-358">Example: "\\windows\\system\\"</span></span>

</dd> <dt>

<span data-ttu-id="5b994-359">**Seres**</span><span class="sxs-lookup"><span data-stu-id="5b994-359">**Readable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b994-360">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="5b994-360">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5b994-361">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5b994-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b994-362">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("legível")</span><span class="sxs-lookup"><span data-stu-id="5b994-362">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Readable")</span></span>
</dt> </dl>

<span data-ttu-id="5b994-363">O arquivo pode ser lido.</span><span class="sxs-lookup"><span data-stu-id="5b994-363">File can be read.</span></span>

<span data-ttu-id="5b994-364">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="5b994-364">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="5b994-365">**Status**</span><span class="sxs-lookup"><span data-stu-id="5b994-365">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b994-366">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5b994-366">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b994-367">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5b994-367">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b994-368">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="5b994-368">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="5b994-369">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="5b994-369">Current status of the object.</span></span> <span data-ttu-id="5b994-370">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="5b994-370">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="5b994-371">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="5b994-371">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="5b994-372">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="5b994-372">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="5b994-373">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="5b994-373">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="5b994-374">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="5b994-374">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="5b994-375">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5b994-375">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="5b994-376">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="5b994-376">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="5b994-377">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="5b994-377">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="5b994-378">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="5b994-378">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="5b994-379">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="5b994-379">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5b994-380">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="5b994-380">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="5b994-381">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="5b994-381">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="5b994-382">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="5b994-382">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="5b994-383">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="5b994-383">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="5b994-384">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="5b994-384">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="5b994-385">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="5b994-385">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="5b994-386">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="5b994-386">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="5b994-387">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="5b994-387">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="5b994-388">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="5b994-388">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5b994-389">**System**</span><span class="sxs-lookup"><span data-stu-id="5b994-389">**System**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b994-390">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="5b994-390">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5b994-391">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5b994-391">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b994-392">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("arquivo do sistema")</span><span class="sxs-lookup"><span data-stu-id="5b994-392">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System File")</span></span>
</dt> </dl>

<span data-ttu-id="5b994-393">Se for **true**, o arquivo será um arquivo do sistema.</span><span class="sxs-lookup"><span data-stu-id="5b994-393">If **True**, the file is a system file.</span></span>

<span data-ttu-id="5b994-394">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="5b994-394">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="5b994-395">**Versão**</span><span class="sxs-lookup"><span data-stu-id="5b994-395">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b994-396">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5b994-396">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b994-397">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5b994-397">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b994-398">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Version")</span><span class="sxs-lookup"><span data-stu-id="5b994-398">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Version")</span></span>
</dt> </dl>

<span data-ttu-id="5b994-399">Cadeia de caracteres de versão do recurso de versão, se houver um.</span><span class="sxs-lookup"><span data-stu-id="5b994-399">Version string from version resource, if one is present.</span></span>

<span data-ttu-id="5b994-400">Esta propriedade é herdada [**do \_ arquivo**](cim-datafile.md)de propriedades CIM.</span><span class="sxs-lookup"><span data-stu-id="5b994-400">This property is inherited from [**CIM\_DataFile**](cim-datafile.md).</span></span>

</dd> <dt>

<span data-ttu-id="5b994-401">**Gravável**</span><span class="sxs-lookup"><span data-stu-id="5b994-401">**Writeable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b994-402">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="5b994-402">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5b994-403">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5b994-403">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b994-404">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("gravável")</span><span class="sxs-lookup"><span data-stu-id="5b994-404">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Writeable")</span></span>
</dt> </dl>

<span data-ttu-id="5b994-405">Se **for true**, o arquivo poderá ser gravado.</span><span class="sxs-lookup"><span data-stu-id="5b994-405">If **True**, the file can be written.</span></span>

<span data-ttu-id="5b994-406">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="5b994-406">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5b994-407">Comentários</span><span class="sxs-lookup"><span data-stu-id="5b994-407">Remarks</span></span>

<span data-ttu-id="5b994-408">A classe de [**\_ arquivo**](cim-datafile.md)de **\_ codec do Win32** é derivada de CIM.</span><span class="sxs-lookup"><span data-stu-id="5b994-408">The **Win32\_CodecFile** class is derived from [**CIM\_DataFile**](cim-datafile.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5b994-409">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5b994-409">Requirements</span></span>



| <span data-ttu-id="5b994-410">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b994-410">Requirement</span></span> | <span data-ttu-id="5b994-411">Valor</span><span class="sxs-lookup"><span data-stu-id="5b994-411">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5b994-412">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5b994-412">Minimum supported client</span></span><br/> | <span data-ttu-id="5b994-413">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5b994-413">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5b994-414">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5b994-414">Minimum supported server</span></span><br/> | <span data-ttu-id="5b994-415">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5b994-415">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5b994-416">Namespace</span><span class="sxs-lookup"><span data-stu-id="5b994-416">Namespace</span></span><br/>                | <span data-ttu-id="5b994-417">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="5b994-417">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5b994-418">MOF</span><span class="sxs-lookup"><span data-stu-id="5b994-418">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5b994-419"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5b994-419"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5b994-420">DLL</span><span class="sxs-lookup"><span data-stu-id="5b994-420">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5b994-421"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b994-421"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b994-422">Confira também</span><span class="sxs-lookup"><span data-stu-id="5b994-422">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b994-423">**DataFile de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="5b994-423">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

<span data-ttu-id="5b994-424">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5b994-424">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

