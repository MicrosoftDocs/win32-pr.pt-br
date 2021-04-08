---
description: A \_ classe CIM devicefile representa um tipo de arquivo lógico, que representa um dispositivo.
ms.assetid: b07f039c-8ab0-4e13-96d5-3621da19e66d
ms.tgt_platform: multiple
title: Classe CIM_DeviceFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile
- CIM_DeviceFile.AccessMask
- CIM_DeviceFile.Archive
- CIM_DeviceFile.Caption
- CIM_DeviceFile.Compressed
- CIM_DeviceFile.CompressionMethod
- CIM_DeviceFile.CreationClassName
- CIM_DeviceFile.CreationDate
- CIM_DeviceFile.CSCreationClassName
- CIM_DeviceFile.CSName
- CIM_DeviceFile.Description
- CIM_DeviceFile.Drive
- CIM_DeviceFile.EightDotThreeFileName
- CIM_DeviceFile.Encrypted
- CIM_DeviceFile.EncryptionMethod
- CIM_DeviceFile.Extension
- CIM_DeviceFile.FileName
- CIM_DeviceFile.FileSize
- CIM_DeviceFile.FileType
- CIM_DeviceFile.FSCreationClassName
- CIM_DeviceFile.FSName
- CIM_DeviceFile.Hidden
- CIM_DeviceFile.InstallDate
- CIM_DeviceFile.InUseCount
- CIM_DeviceFile.LastAccessed
- CIM_DeviceFile.LastModified
- CIM_DeviceFile.Name
- CIM_DeviceFile.Path
- CIM_DeviceFile.Readable
- CIM_DeviceFile.Status
- CIM_DeviceFile.System
- CIM_DeviceFile.Writeable
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 476f0ecd212247e1fc96db3efedcc0c18a6a2e06
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920459"
---
# <a name="cim_devicefile-class"></a><span data-ttu-id="5d77e-103">\_Classe de dispositivo CIM</span><span class="sxs-lookup"><span data-stu-id="5d77e-103">CIM\_DeviceFile class</span></span>

<span data-ttu-id="5d77e-104">A classe **CIM \_ devicefile** representa um tipo de arquivo lógico, que representa um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5d77e-104">The **CIM\_DeviceFile** class represents a type of logical file, which represents a device.</span></span> <span data-ttu-id="5d77e-105">Essa convenção é útil para sistemas operacionais que gerenciam dispositivos usando um modelo de e/s de fluxo de bytes.</span><span class="sxs-lookup"><span data-stu-id="5d77e-105">This convention is useful for operating systems that manage devices using a byte stream I/O model.</span></span> <span data-ttu-id="5d77e-106">O dispositivo lógico associado a esse arquivo é especificado usando a relação de [**\_ DeviceAccessedByFile do CIM**](cim-deviceaccessedbyfile.md) .</span><span class="sxs-lookup"><span data-stu-id="5d77e-106">The logical device that is associated with this file is specified using the [**CIM\_DeviceAccessedByFile**](cim-deviceaccessedbyfile.md) relationship.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5d77e-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="5d77e-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="5d77e-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="5d77e-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="5d77e-109">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="5d77e-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="5d77e-110">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="5d77e-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d77e-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5d77e-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{4333BD60-E3D1-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_DeviceFile : CIM_LogicalFile
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
  boolean  Hidden;
  datetime InstallDate;
  uint64   InUseCount;
  datetime LastAccessed;
  datetime LastModified;
  string   Name;
  string   Path;
  boolean  Readable;
  string   Status;
  boolean  System;
  boolean  Writeable;
};
```

## <a name="members"></a><span data-ttu-id="5d77e-112">Membros</span><span class="sxs-lookup"><span data-stu-id="5d77e-112">Members</span></span>

<span data-ttu-id="5d77e-113">A classe **CIM \_ devicefile** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="5d77e-113">The **CIM\_DeviceFile** class has these types of members:</span></span>

-   [<span data-ttu-id="5d77e-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="5d77e-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="5d77e-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5d77e-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="5d77e-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="5d77e-116">Methods</span></span>

<span data-ttu-id="5d77e-117">A classe **CIM \_ devicefile** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="5d77e-117">The **CIM\_DeviceFile** class has these methods.</span></span>



| <span data-ttu-id="5d77e-118">Método</span><span class="sxs-lookup"><span data-stu-id="5d77e-118">Method</span></span>                                                                                            | <span data-ttu-id="5d77e-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="5d77e-119">Description</span></span>                                                                                                                                              |
|:--------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5d77e-120">**ChangeSecurityPermissions**</span><span class="sxs-lookup"><span data-stu-id="5d77e-120">**ChangeSecurityPermissions**</span></span>](changesecuritypermissions-method-in-class-cim-devicefile.md)     | <span data-ttu-id="5d77e-121">Altera as permissões de segurança para o arquivo lógico especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="5d77e-121">Changes the security permissions for the logical file specified in the object path.</span></span> <span data-ttu-id="5d77e-122">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="5d77e-122">Not implemented by WMI.</span></span><br/>                                   |
| [<span data-ttu-id="5d77e-123">**ChangeSecurityPermissionsEx**</span><span class="sxs-lookup"><span data-stu-id="5d77e-123">**ChangeSecurityPermissionsEx**</span></span>](changesecuritypermissionsex-method-in-class-cim-devicefile.md) | <span data-ttu-id="5d77e-124">Altera as permissões de segurança para o arquivo lógico especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="5d77e-124">Changes the security permissions for the logical file specified in the object path.</span></span> <span data-ttu-id="5d77e-125">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="5d77e-125">Not implemented by WMI.</span></span><br/>                                   |
| [<span data-ttu-id="5d77e-126">**Compactar**</span><span class="sxs-lookup"><span data-stu-id="5d77e-126">**Compress**</span></span>](compress-method-in-class-cim-devicefile.md)                                       | <span data-ttu-id="5d77e-127">Compacta o arquivo lógico (ou diretório) especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="5d77e-127">Compresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="5d77e-128">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="5d77e-128">Not implemented by WMI.</span></span><br/>                                              |
| [<span data-ttu-id="5d77e-129">**CompressEx**</span><span class="sxs-lookup"><span data-stu-id="5d77e-129">**CompressEx**</span></span>](compressex-method-in-class-cim-devicefile.md)                                   | <span data-ttu-id="5d77e-130">Compacta o arquivo lógico (ou diretório) especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="5d77e-130">Compresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="5d77e-131">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="5d77e-131">Not implemented by WMI.</span></span><br/>                                              |
| [<span data-ttu-id="5d77e-132">**CopiarObjeto**</span><span class="sxs-lookup"><span data-stu-id="5d77e-132">**Copy**</span></span>](copy-method-in-class-cim-devicefile.md)                                               | <span data-ttu-id="5d77e-133">Copia o arquivo lógico (ou diretório) especificado no caminho do objeto para o local especificado pelo parâmetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="5d77e-133">Copies the logical file (or directory) specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="5d77e-134">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="5d77e-134">Not implemented by WMI.</span></span><br/> |
| [<span data-ttu-id="5d77e-135">**CopyEx**</span><span class="sxs-lookup"><span data-stu-id="5d77e-135">**CopyEx**</span></span>](copyex-method-in-class-cim-devicefile.md)                                           | <span data-ttu-id="5d77e-136">Copia o arquivo lógico (ou diretório) especificado no caminho do objeto para o local especificado pelo parâmetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="5d77e-136">Copies the logical file (or directory) specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="5d77e-137">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="5d77e-137">Not implemented by WMI.</span></span><br/> |
| [<span data-ttu-id="5d77e-138">**Apagar**</span><span class="sxs-lookup"><span data-stu-id="5d77e-138">**Delete**</span></span>](delete-method-in-class-cim-devicefile.md)                                           | <span data-ttu-id="5d77e-139">Exclui o arquivo lógico (ou diretório) especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="5d77e-139">Deletes the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="5d77e-140">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="5d77e-140">Not implemented by WMI.</span></span><br/>                                                 |
| [<span data-ttu-id="5d77e-141">**DeleteEx**</span><span class="sxs-lookup"><span data-stu-id="5d77e-141">**DeleteEx**</span></span>](deleteex-method-in-class-cim-devicefile.md)                                       | <span data-ttu-id="5d77e-142">Exclui o arquivo lógico (ou diretório) especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="5d77e-142">Deletes the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="5d77e-143">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="5d77e-143">Not implemented by WMI.</span></span><br/>                                                 |
| [<span data-ttu-id="5d77e-144">**GetEffectivePermission**</span><span class="sxs-lookup"><span data-stu-id="5d77e-144">**GetEffectivePermission**</span></span>](geteffectivepermission-method-in-class-cim-devicefile.md)           | <span data-ttu-id="5d77e-145">Determina se o chamador tem as permissões agregadas especificadas pelo argumento de **permissão** .</span><span class="sxs-lookup"><span data-stu-id="5d77e-145">Determines whether the caller has the aggregated permissions specified by the **Permission** argument.</span></span> <span data-ttu-id="5d77e-146">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="5d77e-146">Not implemented by WMI.</span></span><br/>                |
| [<span data-ttu-id="5d77e-147">**Renomear**</span><span class="sxs-lookup"><span data-stu-id="5d77e-147">**Rename**</span></span>](rename-method-in-class-cim-devicefile.md)                                           | <span data-ttu-id="5d77e-148">Renomeia o arquivo lógico (ou diretório) especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="5d77e-148">Renames the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="5d77e-149">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="5d77e-149">Not implemented by WMI.</span></span><br/>                                                 |
| [<span data-ttu-id="5d77e-150">**TakeOwnerShip**</span><span class="sxs-lookup"><span data-stu-id="5d77e-150">**TakeOwnerShip**</span></span>](takeownership-method-in-class-cim-devicefile.md)                             | <span data-ttu-id="5d77e-151">Obtém a propriedade do arquivo lógico especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="5d77e-151">Obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="5d77e-152">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="5d77e-152">Not implemented by WMI.</span></span><br/>                                                   |
| [<span data-ttu-id="5d77e-153">**TakeOwnerShipEx**</span><span class="sxs-lookup"><span data-stu-id="5d77e-153">**TakeOwnerShipEx**</span></span>](takeownershipex-method-in-class-cim-devicefile.md)                         | <span data-ttu-id="5d77e-154">Obtém a propriedade do arquivo lógico especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="5d77e-154">Obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="5d77e-155">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="5d77e-155">Not implemented by WMI.</span></span><br/>                                                   |
| [<span data-ttu-id="5d77e-156">**Descompactar**</span><span class="sxs-lookup"><span data-stu-id="5d77e-156">**Uncompress**</span></span>](uncompress-method-in-class-cim-devicefile.md)                                   | <span data-ttu-id="5d77e-157">Descompacta o arquivo lógico (ou diretório) especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="5d77e-157">Uncompresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="5d77e-158">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="5d77e-158">Not implemented by WMI.</span></span><br/>                                            |
| [<span data-ttu-id="5d77e-159">**UncompressEx**</span><span class="sxs-lookup"><span data-stu-id="5d77e-159">**UncompressEx**</span></span>](uncompressex-method-in-class-cim-devicefile.md)                               | <span data-ttu-id="5d77e-160">Descompacta o arquivo lógico (ou diretório) especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="5d77e-160">Uncompresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="5d77e-161">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="5d77e-161">Not implemented by WMI.</span></span><br/>                                            |



 

### <a name="properties"></a><span data-ttu-id="5d77e-162">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5d77e-162">Properties</span></span>

<span data-ttu-id="5d77e-163">A classe **CIM \_ devicefile** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="5d77e-163">The **CIM\_DeviceFile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5d77e-164">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="5d77e-164">**AccessMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d77e-165">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5d77e-165">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5d77e-166">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d77e-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d77e-167">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("direitos de acesso")</span><span class="sxs-lookup"><span data-stu-id="5d77e-167">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Access Rights")</span></span>
</dt> </dl>

<span data-ttu-id="5d77e-168">Matriz de bits que representa os direitos de acesso ao arquivo ou diretório fornecido pelo usuário ou grupo em cujo nome a instância é retornada.</span><span class="sxs-lookup"><span data-stu-id="5d77e-168">Bit array that represents the access rights to the given file or directory held by the user or group on whose behalf the instance is returned.</span></span> <span data-ttu-id="5d77e-169">Em volumes FAT, **o \_ acesso completo** é retornado, o que indica que nenhuma segurança foi definida no objeto.</span><span class="sxs-lookup"><span data-stu-id="5d77e-169">On FAT volumes, **FULL\_ACCESS** is returned, which indicates that no security has been set on the object.</span></span>

<span data-ttu-id="5d77e-170">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="5d77e-170">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="5d77e-171"><span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>Do **arquivo \_ LER \_ os dados (arquivo) ou \_ \_ diretório de lista de arquivos (diretório)** (1)</span><span class="sxs-lookup"><span data-stu-id="5d77e-171"><span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>**FILE\_READ\_DATA (file) or FILE\_LIST\_DIRECTORY (directory)** (1)</span></span>


</dt> <dd>

<span data-ttu-id="5d77e-172">Concede o direito de ler dados do arquivo.</span><span class="sxs-lookup"><span data-stu-id="5d77e-172">Grants the right to read data from the file.</span></span> <span data-ttu-id="5d77e-173">Para um diretório, esse valor concede o direito de listar o conteúdo do diretório.</span><span class="sxs-lookup"><span data-stu-id="5d77e-173">For a directory, this value grants the right to list the contents of the directory.</span></span>

</dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="5d77e-174"><span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>Do **arquivo \_ GRAVAR \_ dados (arquivo) ou arquivo \_ Adicionar \_ arquivo (diretório)** (2)</span><span class="sxs-lookup"><span data-stu-id="5d77e-174"><span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>**FILE\_WRITE\_DATA (file) or FILE\_ADD\_FILE (directory)** (2)</span></span>


</dt> <dd>

<span data-ttu-id="5d77e-175">Concede o direito de gravar dados no arquivo.</span><span class="sxs-lookup"><span data-stu-id="5d77e-175">Grants the right to write data to the file.</span></span> <span data-ttu-id="5d77e-176">Para um diretório, esse valor concede o direito de criar um arquivo no diretório.</span><span class="sxs-lookup"><span data-stu-id="5d77e-176">For a directory, this value grants the right to create a file in the directory.</span></span>

</dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="5d77e-177"><span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>Do **arquivo \_ ACRESCENTAR \_ dados (arquivo) ou arquivo \_ Adicionar \_ subdiretório (diretório)** (4)</span><span class="sxs-lookup"><span data-stu-id="5d77e-177"><span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>**FILE\_APPEND\_DATA (file) or FILE\_ADD\_SUBDIRECTORY (directory)** (4)</span></span>


</dt> <dd>

<span data-ttu-id="5d77e-178">Concede o direito de acrescentar dados ao arquivo.</span><span class="sxs-lookup"><span data-stu-id="5d77e-178">Grants the right to append data to the file.</span></span> <span data-ttu-id="5d77e-179">Para um diretório, esse valor concede o direito de criar um subdiretório.</span><span class="sxs-lookup"><span data-stu-id="5d77e-179">For a directory, this value grants the right to create a subdirectory.</span></span>

</dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="5d77e-180"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>Do **arquivo \_ LER \_ ea** (8)</span><span class="sxs-lookup"><span data-stu-id="5d77e-180"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**FILE\_READ\_EA** (8)</span></span>


</dt> <dd>

<span data-ttu-id="5d77e-181">Concede o direito de ler atributos estendidos.</span><span class="sxs-lookup"><span data-stu-id="5d77e-181">Grants the right to read extended attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="5d77e-182"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>Do **arquivo \_ GRAVAR \_ ea** (16)</span><span class="sxs-lookup"><span data-stu-id="5d77e-182"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**FILE\_WRITE\_EA** (16)</span></span>


</dt> <dd>

<span data-ttu-id="5d77e-183">Concede o direito de gravar atributos estendidos.</span><span class="sxs-lookup"><span data-stu-id="5d77e-183">Grants the right to write extended attributes.</span></span>

</dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

<span data-ttu-id="5d77e-184"><span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>Do **arquivo \_ EXECUTAR (arquivo) ou \_ atravessamento de arquivo (diretório)** (32)</span><span class="sxs-lookup"><span data-stu-id="5d77e-184"><span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>**FILE\_EXECUTE (file) or FILE\_TRAVERSE (directory)** (32)</span></span>


</dt> <dd>

<span data-ttu-id="5d77e-185">Concede o direito de executar um arquivo.</span><span class="sxs-lookup"><span data-stu-id="5d77e-185">Grants the right to execute a file.</span></span> <span data-ttu-id="5d77e-186">Para um diretório, o diretório pode ser atravessado.</span><span class="sxs-lookup"><span data-stu-id="5d77e-186">For a directory, the directory can be traversed.</span></span>

</dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="5d77e-187"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>Do **arquivo \_ EXCLUIR \_ filho (diretório)** (64)</span><span class="sxs-lookup"><span data-stu-id="5d77e-187"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**FILE\_DELETE\_CHILD (directory)** (64)</span></span>


</dt> <dd>

<span data-ttu-id="5d77e-188">Concede o direito de excluir um diretório e todos os arquivos que ele contém (seus filhos), mesmo que os arquivos sejam somente leitura.</span><span class="sxs-lookup"><span data-stu-id="5d77e-188">Grants the right to delete a directory and all the files it contains (its children), even if the files are read-only.</span></span>

</dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="5d77e-189"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>Do **arquivo \_ \_Atributos de leitura** (128)</span><span class="sxs-lookup"><span data-stu-id="5d77e-189"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**FILE\_READ\_ATTRIBUTES** (128)</span></span>


</dt> <dd>

<span data-ttu-id="5d77e-190">Concede o direito de ler atributos de arquivo.</span><span class="sxs-lookup"><span data-stu-id="5d77e-190">Grants the right to read file attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="5d77e-191"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>Do **arquivo \_ \_Atributos de gravação** (256)</span><span class="sxs-lookup"><span data-stu-id="5d77e-191"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**FILE\_WRITE\_ATTRIBUTES** (256)</span></span>


</dt> <dd>

<span data-ttu-id="5d77e-192">Concede o direito de alterar atributos de arquivo.</span><span class="sxs-lookup"><span data-stu-id="5d77e-192">Grants the right to change file attributes.</span></span>

</dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="5d77e-193"><span id="DELETE"></span><span id="delete"></span>**Excluir** (65536)</span><span class="sxs-lookup"><span data-stu-id="5d77e-193"><span id="DELETE"></span><span id="delete"></span>**DELETE** (65536)</span></span>


</dt> <dd>

<span data-ttu-id="5d77e-194">Concede acesso de exclusão.</span><span class="sxs-lookup"><span data-stu-id="5d77e-194">Grants delete access.</span></span>

</dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="5d77e-195"><span id="READ_CONTROL"></span><span id="read_control"></span>**Ler \_ CONTROLE** (131072)</span><span class="sxs-lookup"><span data-stu-id="5d77e-195"><span id="READ_CONTROL"></span><span id="read_control"></span>**READ\_CONTROL** (131072)</span></span>


</dt> <dd>

<span data-ttu-id="5d77e-196">Concede acesso de leitura ao descritor de segurança e ao proprietário.</span><span class="sxs-lookup"><span data-stu-id="5d77e-196">Grants read access to the security descriptor and owner.</span></span>

</dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="5d77e-197"><span id="WRITE_DAC"></span><span id="write_dac"></span>**Gravar \_ DAC** (262144)</span><span class="sxs-lookup"><span data-stu-id="5d77e-197"><span id="WRITE_DAC"></span><span id="write_dac"></span>**WRITE\_DAC** (262144)</span></span>


</dt> <dd>

<span data-ttu-id="5d77e-198">Concede acesso de gravação à ACL discricionária.</span><span class="sxs-lookup"><span data-stu-id="5d77e-198">Grants write access to the discretionary ACL.</span></span>

</dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="5d77e-199"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**Gravar \_ PROPRIETÁRIO** (524288)</span><span class="sxs-lookup"><span data-stu-id="5d77e-199"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**WRITE\_OWNER** (524288)</span></span>


</dt> <dd>

<span data-ttu-id="5d77e-200">Atribui o proprietário da gravação.</span><span class="sxs-lookup"><span data-stu-id="5d77e-200">Assigns the write owner.</span></span>

</dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="5d77e-201"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**Sincronizar** (1048576)</span><span class="sxs-lookup"><span data-stu-id="5d77e-201"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**SYNCHRONIZE** (1048576)</span></span>


</dt> <dd>

<span data-ttu-id="5d77e-202">Sincroniza o acesso e permite que um processo Aguarde um objeto para entrar no estado sinalizado.</span><span class="sxs-lookup"><span data-stu-id="5d77e-202">Synchronizes access and allows a process to wait for an object to enter the signaled state.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5d77e-203">**Arquivar**</span><span class="sxs-lookup"><span data-stu-id="5d77e-203">**Archive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d77e-204">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="5d77e-204">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5d77e-205">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d77e-205">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d77e-206">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("deve ser arquivado")</span><span class="sxs-lookup"><span data-stu-id="5d77e-206">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Should Be Archived")</span></span>
</dt> </dl>

<span data-ttu-id="5d77e-207">Se **for true**, o arquivo deverá ser arquivado.</span><span class="sxs-lookup"><span data-stu-id="5d77e-207">If **True**, the file should be archived.</span></span>

<span data-ttu-id="5d77e-208">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="5d77e-208">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="5d77e-209">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="5d77e-209">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d77e-210">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5d77e-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d77e-211">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d77e-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d77e-212">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="5d77e-212">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="5d77e-213">Breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="5d77e-213">Short textual description of the object.</span></span>

<span data-ttu-id="5d77e-214">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5d77e-214">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5d77e-215">**Compactado**</span><span class="sxs-lookup"><span data-stu-id="5d77e-215">**Compressed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d77e-216">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="5d77e-216">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5d77e-217">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d77e-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d77e-218">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("compactado")</span><span class="sxs-lookup"><span data-stu-id="5d77e-218">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compressed")</span></span>
</dt> </dl>

<span data-ttu-id="5d77e-219">Se **for true**, o arquivo será compactado.</span><span class="sxs-lookup"><span data-stu-id="5d77e-219">If **True**, the file is compressed.</span></span>

<span data-ttu-id="5d77e-220">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="5d77e-220">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="5d77e-221">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="5d77e-221">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d77e-222">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5d77e-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d77e-223">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d77e-223">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d77e-224">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("método de compactação")</span><span class="sxs-lookup"><span data-stu-id="5d77e-224">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compression Method")</span></span>
</dt> </dl>

<span data-ttu-id="5d77e-225">Cadeia de caracteres de forma livre que indica o algoritmo ou a ferramenta usada para compactar o arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="5d77e-225">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="5d77e-226">Se o esquema de compactação for desconhecido ou não estiver descrito, use "desconhecido".</span><span class="sxs-lookup"><span data-stu-id="5d77e-226">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="5d77e-227">Se o arquivo lógico estiver compactado, mas o esquema de compactação for desconhecido ou não estiver descrito, use "compactado".</span><span class="sxs-lookup"><span data-stu-id="5d77e-227">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="5d77e-228">Se o arquivo lógico não estiver compactado, use "não compactado".</span><span class="sxs-lookup"><span data-stu-id="5d77e-228">If the logical file is not compressed, use "Not Compressed".</span></span>

<span data-ttu-id="5d77e-229">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="5d77e-229">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="5d77e-230">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="5d77e-230">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d77e-231">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5d77e-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d77e-232">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d77e-232">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d77e-233">Qualificadores: [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nome da classe")</span><span class="sxs-lookup"><span data-stu-id="5d77e-233">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="5d77e-234">Nome da classe.</span><span class="sxs-lookup"><span data-stu-id="5d77e-234">Name of the class.</span></span>

<span data-ttu-id="5d77e-235">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="5d77e-235">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="5d77e-236">**CreationDate**</span><span class="sxs-lookup"><span data-stu-id="5d77e-236">**CreationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d77e-237">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5d77e-237">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5d77e-238">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d77e-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d77e-239">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("data de criação")</span><span class="sxs-lookup"><span data-stu-id="5d77e-239">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Creation Date")</span></span>
</dt> </dl>

<span data-ttu-id="5d77e-240">Data de criação do arquivo.</span><span class="sxs-lookup"><span data-stu-id="5d77e-240">File's creation date.</span></span>

<span data-ttu-id="5d77e-241">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="5d77e-241">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="5d77e-242">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="5d77e-242">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d77e-243">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5d77e-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d77e-244">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d77e-244">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d77e-245">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema de arquivos CIM**](cim-filesystem.md).**CSCreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome da classe do sistema de computador ")</span><span class="sxs-lookup"><span data-stu-id="5d77e-245">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSCreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="5d77e-246">Classe do sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="5d77e-246">Class of the computer system.</span></span>

<span data-ttu-id="5d77e-247">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="5d77e-247">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="5d77e-248">**CSName**</span><span class="sxs-lookup"><span data-stu-id="5d77e-248">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d77e-249">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5d77e-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d77e-250">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d77e-250">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d77e-251">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema de arquivos CIM**](cim-filesystem.md).**CSName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome do sistema de computador ")</span><span class="sxs-lookup"><span data-stu-id="5d77e-251">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Name")</span></span>
</dt> </dl>

<span data-ttu-id="5d77e-252">Nome do sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="5d77e-252">Name of the computer system.</span></span>

<span data-ttu-id="5d77e-253">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="5d77e-253">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="5d77e-254">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="5d77e-254">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d77e-255">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5d77e-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d77e-256">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d77e-256">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d77e-257">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="5d77e-257">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="5d77e-258">Descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="5d77e-258">Textual description of the object.</span></span>

<span data-ttu-id="5d77e-259">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5d77e-259">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5d77e-260">**Unidade**</span><span class="sxs-lookup"><span data-stu-id="5d77e-260">**Drive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d77e-261">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5d77e-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d77e-262">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d77e-262">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d77e-263">Qualificadores: [**fixo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("drive")</span><span class="sxs-lookup"><span data-stu-id="5d77e-263">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Drive")</span></span>
</dt> </dl>

<span data-ttu-id="5d77e-264">Letra da unidade (incluindo os dois-pontos que segue a letra da unidade) do arquivo.</span><span class="sxs-lookup"><span data-stu-id="5d77e-264">Drive letter (including the colon that follows the drive letter) of the file.</span></span> <span data-ttu-id="5d77e-265">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="5d77e-265">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="5d77e-266">Exemplo: "c:"</span><span class="sxs-lookup"><span data-stu-id="5d77e-266">Example: "c:"</span></span>

</dd> <dt>

<span data-ttu-id="5d77e-267">**EightDotThreeFileName**</span><span class="sxs-lookup"><span data-stu-id="5d77e-267">**EightDotThreeFileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d77e-268">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5d77e-268">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d77e-269">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d77e-269">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d77e-270">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("oito pontos três nome de arquivo")</span><span class="sxs-lookup"><span data-stu-id="5d77e-270">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Eight Dot Three File Name")</span></span>
</dt> </dl>

<span data-ttu-id="5d77e-271">Nome de arquivo compatível com DOS para o arquivo.</span><span class="sxs-lookup"><span data-stu-id="5d77e-271">DOS-compatible file name for the file.</span></span> <span data-ttu-id="5d77e-272">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="5d77e-272">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="5d77e-273">Exemplo: "c: \\ progra ~ 1"</span><span class="sxs-lookup"><span data-stu-id="5d77e-273">Example: "c:\\progra~1"</span></span>

</dd> <dt>

<span data-ttu-id="5d77e-274">**Criptografado**</span><span class="sxs-lookup"><span data-stu-id="5d77e-274">**Encrypted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d77e-275">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="5d77e-275">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5d77e-276">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d77e-276">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d77e-277">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encrypted")</span><span class="sxs-lookup"><span data-stu-id="5d77e-277">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encrypted")</span></span>
</dt> </dl>

<span data-ttu-id="5d77e-278">Se **for true**, o arquivo será criptografado.</span><span class="sxs-lookup"><span data-stu-id="5d77e-278">If **True**, the file is encrypted.</span></span>

<span data-ttu-id="5d77e-279">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="5d77e-279">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="5d77e-280">**EncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="5d77e-280">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d77e-281">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5d77e-281">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d77e-282">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d77e-282">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d77e-283">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("método de criptografia")</span><span class="sxs-lookup"><span data-stu-id="5d77e-283">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encryption Method")</span></span>
</dt> </dl>

<span data-ttu-id="5d77e-284">Cadeia de caracteres de forma livre que identifica o algoritmo ou a ferramenta usada para criptografar um arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="5d77e-284">Free-form string that identifies the algorithm or tool used to encrypt a logical file.</span></span> <span data-ttu-id="5d77e-285">Se o esquema de criptografia não for indulged (por motivos de segurança, por exemplo), use "desconhecido".</span><span class="sxs-lookup"><span data-stu-id="5d77e-285">If the encryption scheme is not indulged (for security reasons, for example), use "Unknown".</span></span> <span data-ttu-id="5d77e-286">Se o arquivo estiver criptografado, mas seu esquema de criptografia for desconhecido ou não for divulgado, use "Encrypted".</span><span class="sxs-lookup"><span data-stu-id="5d77e-286">If the file is encrypted, but either its encryption scheme is unknown or not disclosed, use "Encrypted".</span></span> <span data-ttu-id="5d77e-287">Se o arquivo lógico não estiver criptografado, use "não criptografado".</span><span class="sxs-lookup"><span data-stu-id="5d77e-287">If the logical file is not encrypted, use "Not Encrypted".</span></span>

<span data-ttu-id="5d77e-288">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="5d77e-288">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="5d77e-289">**Extensão**</span><span class="sxs-lookup"><span data-stu-id="5d77e-289">**Extension**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d77e-290">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5d77e-290">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d77e-291">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d77e-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d77e-292">Qualificadores: [**fixo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("extensão de arquivo")</span><span class="sxs-lookup"><span data-stu-id="5d77e-292">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Extension")</span></span>
</dt> </dl>

<span data-ttu-id="5d77e-293">Extensão de nome de arquivo sem o ponto anterior (ponto).</span><span class="sxs-lookup"><span data-stu-id="5d77e-293">File name extension without the preceding period (dot).</span></span>

<span data-ttu-id="5d77e-294">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="5d77e-294">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="5d77e-295">Exemplo: "txt", "MOF", "mdb"</span><span class="sxs-lookup"><span data-stu-id="5d77e-295">Example: "txt", "mof", "mdb"</span></span>

</dd> <dt>

<span data-ttu-id="5d77e-296">**FileName**</span><span class="sxs-lookup"><span data-stu-id="5d77e-296">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d77e-297">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5d77e-297">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d77e-298">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d77e-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d77e-299">Qualificadores: [**fixo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nome do arquivo")</span><span class="sxs-lookup"><span data-stu-id="5d77e-299">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Name")</span></span>
</dt> </dl>

<span data-ttu-id="5d77e-300">Nome do arquivo sem a extensão de nome de arquivo.</span><span class="sxs-lookup"><span data-stu-id="5d77e-300">File name without the file name extension.</span></span>

<span data-ttu-id="5d77e-301">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="5d77e-301">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="5d77e-302">Exemplo: "mydatafile"</span><span class="sxs-lookup"><span data-stu-id="5d77e-302">Example: "MyDataFile"</span></span>

</dd> <dt>

<span data-ttu-id="5d77e-303">**Tamanho**</span><span class="sxs-lookup"><span data-stu-id="5d77e-303">**FileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d77e-304">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5d77e-304">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5d77e-305">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d77e-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d77e-306">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("tamanho"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="5d77e-306">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Size"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="5d77e-307">Tamanho do arquivo, em bytes.</span><span class="sxs-lookup"><span data-stu-id="5d77e-307">Size of the file, in bytes.</span></span>

<span data-ttu-id="5d77e-308">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="5d77e-308">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="5d77e-309">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="5d77e-309">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="5d77e-310">**Talvez**</span><span class="sxs-lookup"><span data-stu-id="5d77e-310">**FileType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d77e-311">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5d77e-311">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d77e-312">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d77e-312">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d77e-313">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("tipo de arquivo")</span><span class="sxs-lookup"><span data-stu-id="5d77e-313">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Type")</span></span>
</dt> </dl>

<span data-ttu-id="5d77e-314">Descritor que representa o tipo de arquivo (indicado pela propriedade de **extensão** ).</span><span class="sxs-lookup"><span data-stu-id="5d77e-314">Descriptor that represents the file type (indicated by the **Extension** property).</span></span>

<span data-ttu-id="5d77e-315">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="5d77e-315">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="5d77e-316">**FSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="5d77e-316">**FSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d77e-317">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5d77e-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d77e-318">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d77e-318">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d77e-319">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema de arquivos CIM**](cim-filesystem.md).**CreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome da classe do sistema de arquivos ")</span><span class="sxs-lookup"><span data-stu-id="5d77e-319">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="5d77e-320">Classe do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="5d77e-320">Class of the file system.</span></span>

<span data-ttu-id="5d77e-321">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="5d77e-321">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="5d77e-322">**FSName**</span><span class="sxs-lookup"><span data-stu-id="5d77e-322">**FSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d77e-323">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5d77e-323">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d77e-324">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d77e-324">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d77e-325">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema de arquivos CIM**](cim-filesystem.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome do sistema de arquivos ")</span><span class="sxs-lookup"><span data-stu-id="5d77e-325">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Name")</span></span>
</dt> </dl>

<span data-ttu-id="5d77e-326">Nome do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="5d77e-326">Name of the file system.</span></span>

<span data-ttu-id="5d77e-327">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="5d77e-327">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="5d77e-328">**Oculto**</span><span class="sxs-lookup"><span data-stu-id="5d77e-328">**Hidden**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d77e-329">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="5d77e-329">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5d77e-330">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d77e-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d77e-331">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hidden")</span><span class="sxs-lookup"><span data-stu-id="5d77e-331">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hidden")</span></span>
</dt> </dl>

<span data-ttu-id="5d77e-332">Se for **true**, o arquivo ficará oculto.</span><span class="sxs-lookup"><span data-stu-id="5d77e-332">If **True**, the file is hidden.</span></span>

<span data-ttu-id="5d77e-333">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="5d77e-333">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="5d77e-334">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="5d77e-334">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d77e-335">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5d77e-335">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5d77e-336">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d77e-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d77e-337">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="5d77e-337">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="5d77e-338">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="5d77e-338">Date and time when the object was installed.</span></span> <span data-ttu-id="5d77e-339">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="5d77e-339">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="5d77e-340">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5d77e-340">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5d77e-341">**InUseCount**</span><span class="sxs-lookup"><span data-stu-id="5d77e-341">**InUseCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d77e-342">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5d77e-342">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5d77e-343">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d77e-343">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d77e-344">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("contagem de abertura de arquivo atual")</span><span class="sxs-lookup"><span data-stu-id="5d77e-344">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Current File Open Count")</span></span>
</dt> </dl>

<span data-ttu-id="5d77e-345">Número de "aberturas de arquivo" que estão atualmente ativos no arquivo.</span><span class="sxs-lookup"><span data-stu-id="5d77e-345">Number of "file opens" that are currently active against the file.</span></span>

<span data-ttu-id="5d77e-346">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="5d77e-346">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="5d77e-347">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="5d77e-347">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="5d77e-348">**LastAccessed**</span><span class="sxs-lookup"><span data-stu-id="5d77e-348">**LastAccessed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d77e-349">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5d77e-349">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5d77e-350">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d77e-350">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d77e-351">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("último acesso")</span><span class="sxs-lookup"><span data-stu-id="5d77e-351">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Accessed")</span></span>
</dt> </dl>

<span data-ttu-id="5d77e-352">Data e hora em que o arquivo foi acessado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="5d77e-352">Date and time that the file was last accessed.</span></span>

<span data-ttu-id="5d77e-353">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="5d77e-353">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="5d77e-354">**LastModified**</span><span class="sxs-lookup"><span data-stu-id="5d77e-354">**LastModified**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d77e-355">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5d77e-355">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5d77e-356">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d77e-356">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d77e-357">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("última modificação")</span><span class="sxs-lookup"><span data-stu-id="5d77e-357">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Modified")</span></span>
</dt> </dl>

<span data-ttu-id="5d77e-358">Data e hora em que o arquivo foi modificado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="5d77e-358">Date and time that the file was last modified.</span></span>

<span data-ttu-id="5d77e-359">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="5d77e-359">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="5d77e-360">**Nome**</span><span class="sxs-lookup"><span data-stu-id="5d77e-360">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d77e-361">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5d77e-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d77e-362">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d77e-362">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d77e-363">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5d77e-363">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="5d77e-364">Nome herdado que serve como uma chave de uma instância de arquivo lógico em um sistema de arquivos (forneça nomes de caminho completos).</span><span class="sxs-lookup"><span data-stu-id="5d77e-364">Inherited name that serves as a key of a logical file instance within a file system (provide full path names).</span></span>

<span data-ttu-id="5d77e-365">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5d77e-365">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="5d77e-366">Exemplo: "C: \\ Windows \\ System \\win.ini"</span><span class="sxs-lookup"><span data-stu-id="5d77e-366">Example: "C:\\Windows\\system\\win.ini"</span></span>

</dd> <dt>

<span data-ttu-id="5d77e-367">**Caminho**</span><span class="sxs-lookup"><span data-stu-id="5d77e-367">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d77e-368">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5d77e-368">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d77e-369">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d77e-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d77e-370">Qualificadores: [**fixo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Path")</span><span class="sxs-lookup"><span data-stu-id="5d77e-370">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Path")</span></span>
</dt> </dl>

<span data-ttu-id="5d77e-371">Caminho do arquivo, incluindo barras invertidas à esquerda e à direita.</span><span class="sxs-lookup"><span data-stu-id="5d77e-371">Path of the file including leading and trailing backslashes.</span></span> <span data-ttu-id="5d77e-372">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="5d77e-372">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="5d77e-373">Exemplo: " \\ sistema do Windows \\ \\ "</span><span class="sxs-lookup"><span data-stu-id="5d77e-373">Example: "\\windows\\system\\"</span></span>

</dd> <dt>

<span data-ttu-id="5d77e-374">**Seres**</span><span class="sxs-lookup"><span data-stu-id="5d77e-374">**Readable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d77e-375">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="5d77e-375">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5d77e-376">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d77e-376">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d77e-377">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("legível")</span><span class="sxs-lookup"><span data-stu-id="5d77e-377">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Readable")</span></span>
</dt> </dl>

<span data-ttu-id="5d77e-378">Se **for true**, o arquivo poderá ser lido.</span><span class="sxs-lookup"><span data-stu-id="5d77e-378">If **True**, the file can be read.</span></span>

<span data-ttu-id="5d77e-379">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="5d77e-379">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="5d77e-380">**Status**</span><span class="sxs-lookup"><span data-stu-id="5d77e-380">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d77e-381">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5d77e-381">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d77e-382">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d77e-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d77e-383">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="5d77e-383">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="5d77e-384">Cadeia de caracteres que indica o status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="5d77e-384">String that indicates the current status of the object.</span></span> <span data-ttu-id="5d77e-385">Pode ser definido um status operacional e não operacional.</span><span class="sxs-lookup"><span data-stu-id="5d77e-385">Operational and nonoperational status can be defined.</span></span> <span data-ttu-id="5d77e-386">O status operacional pode incluir "OK", "degradado" e "Pred falha".</span><span class="sxs-lookup"><span data-stu-id="5d77e-386">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="5d77e-387">"Pred Fail" indica que um elemento está funcionando corretamente, mas está prevendo uma falha (por exemplo, uma unidade de disco rígido habilitada para inteligente).</span><span class="sxs-lookup"><span data-stu-id="5d77e-387">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="5d77e-388">O status não operacional pode incluir "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="5d77e-388">Nonoperational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="5d77e-389">O "serviço" pode ser aplicado durante o espelhamento de disco – reprateando, recarregando uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="5d77e-389">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="5d77e-390">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="5d77e-390">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="5d77e-391">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5d77e-391">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="5d77e-392">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="5d77e-392">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="5d77e-393">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="5d77e-393">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="5d77e-394">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="5d77e-394">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="5d77e-395">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="5d77e-395">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5d77e-396">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="5d77e-396">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="5d77e-397">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="5d77e-397">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="5d77e-398">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="5d77e-398">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="5d77e-399">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="5d77e-399">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="5d77e-400">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="5d77e-400">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="5d77e-401">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="5d77e-401">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="5d77e-402">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="5d77e-402">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="5d77e-403">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="5d77e-403">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="5d77e-404">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="5d77e-404">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5d77e-405">**System**</span><span class="sxs-lookup"><span data-stu-id="5d77e-405">**System**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d77e-406">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="5d77e-406">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5d77e-407">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d77e-407">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d77e-408">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("arquivo do sistema")</span><span class="sxs-lookup"><span data-stu-id="5d77e-408">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System File")</span></span>
</dt> </dl>

<span data-ttu-id="5d77e-409">Se for **true**, o arquivo será um arquivo do sistema.</span><span class="sxs-lookup"><span data-stu-id="5d77e-409">If **True**, the file is a system file.</span></span>

<span data-ttu-id="5d77e-410">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="5d77e-410">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="5d77e-411">**Gravável**</span><span class="sxs-lookup"><span data-stu-id="5d77e-411">**Writeable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d77e-412">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="5d77e-412">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5d77e-413">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d77e-413">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d77e-414">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("gravável")</span><span class="sxs-lookup"><span data-stu-id="5d77e-414">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Writeable")</span></span>
</dt> </dl>

<span data-ttu-id="5d77e-415">Se **for true**, o arquivo poderá ser gravado.</span><span class="sxs-lookup"><span data-stu-id="5d77e-415">If **True**, the file can be written.</span></span>

<span data-ttu-id="5d77e-416">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="5d77e-416">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5d77e-417">Comentários</span><span class="sxs-lookup"><span data-stu-id="5d77e-417">Remarks</span></span>

<span data-ttu-id="5d77e-418">A classe de **\_ dispositivo CIM** é derivada de [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="5d77e-418">The **CIM\_DeviceFile** class is derived from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="5d77e-419">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="5d77e-419">WMI does not implement this class.</span></span>

<span data-ttu-id="5d77e-420">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="5d77e-420">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="5d77e-421">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="5d77e-421">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d77e-422">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d77e-422">Requirements</span></span>



| <span data-ttu-id="5d77e-423">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d77e-423">Requirement</span></span> | <span data-ttu-id="5d77e-424">Valor</span><span class="sxs-lookup"><span data-stu-id="5d77e-424">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5d77e-425">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5d77e-425">Minimum supported client</span></span><br/> | <span data-ttu-id="5d77e-426">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5d77e-426">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5d77e-427">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5d77e-427">Minimum supported server</span></span><br/> | <span data-ttu-id="5d77e-428">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5d77e-428">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5d77e-429">Namespace</span><span class="sxs-lookup"><span data-stu-id="5d77e-429">Namespace</span></span><br/>                | <span data-ttu-id="5d77e-430">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="5d77e-430">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5d77e-431">MOF</span><span class="sxs-lookup"><span data-stu-id="5d77e-431">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5d77e-432"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5d77e-432"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5d77e-433">DLL</span><span class="sxs-lookup"><span data-stu-id="5d77e-433">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5d77e-434"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5d77e-434"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d77e-435">Confira também</span><span class="sxs-lookup"><span data-stu-id="5d77e-435">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d77e-436">**CIM \_ LogicalFile**</span><span class="sxs-lookup"><span data-stu-id="5d77e-436">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

