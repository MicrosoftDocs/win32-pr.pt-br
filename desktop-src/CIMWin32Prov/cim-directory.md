---
description: A \_ classe de diretório CIM representa um tipo de arquivo que agrupa logicamente os arquivos de dados que ele contém e fornece informações de caminho para os arquivos agrupados.
ms.assetid: a9594f53-08f0-4a47-9edc-51686c80c5ea
ms.tgt_platform: multiple
title: Classe CIM_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory
- CIM_Directory.AccessMask
- CIM_Directory.Archive
- CIM_Directory.Caption
- CIM_Directory.Compressed
- CIM_Directory.CompressionMethod
- CIM_Directory.CreationClassName
- CIM_Directory.CreationDate
- CIM_Directory.CSCreationClassName
- CIM_Directory.CSName
- CIM_Directory.Description
- CIM_Directory.Drive
- CIM_Directory.EightDotThreeFileName
- CIM_Directory.Encrypted
- CIM_Directory.EncryptionMethod
- CIM_Directory.Extension
- CIM_Directory.FileName
- CIM_Directory.FileSize
- CIM_Directory.FileType
- CIM_Directory.FSCreationClassName
- CIM_Directory.FSName
- CIM_Directory.Hidden
- CIM_Directory.InstallDate
- CIM_Directory.InUseCount
- CIM_Directory.LastAccessed
- CIM_Directory.LastModified
- CIM_Directory.Name
- CIM_Directory.Path
- CIM_Directory.Readable
- CIM_Directory.Status
- CIM_Directory.System
- CIM_Directory.Writeable
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: cebab65cc067018b3a57aa5f6890fffad1cb4c7a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105769053"
---
# <a name="cim_directory-class"></a><span data-ttu-id="ca343-103">\_Classe de diretório CIM</span><span class="sxs-lookup"><span data-stu-id="ca343-103">CIM\_Directory class</span></span>

<span data-ttu-id="ca343-104">A classe de **\_ diretório CIM** representa um tipo de arquivo que agrupa logicamente os arquivos de dados que ele contém e fornece informações de caminho para os arquivos agrupados.</span><span class="sxs-lookup"><span data-stu-id="ca343-104">The **CIM\_Directory** class represents a file type that logically groups the data files that it contains and provides path information for the grouped files.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ca343-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="ca343-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="ca343-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="ca343-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="ca343-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="ca343-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="ca343-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="ca343-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca343-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ca343-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C55F-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("Directories (CIM)"), AMENDMENT]
class CIM_Directory : CIM_LogicalFile
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

## <a name="members"></a><span data-ttu-id="ca343-110">Membros</span><span class="sxs-lookup"><span data-stu-id="ca343-110">Members</span></span>

<span data-ttu-id="ca343-111">A classe de **\_ diretório CIM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="ca343-111">The **CIM\_Directory** class has these types of members:</span></span>

-   [<span data-ttu-id="ca343-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="ca343-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="ca343-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ca343-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ca343-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="ca343-114">Methods</span></span>

<span data-ttu-id="ca343-115">A classe de **\_ diretório CIM** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="ca343-115">The **CIM\_Directory** class has these methods.</span></span>



| <span data-ttu-id="ca343-116">Método</span><span class="sxs-lookup"><span data-stu-id="ca343-116">Method</span></span>                                                                                           | <span data-ttu-id="ca343-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="ca343-117">Description</span></span>                                                                                                                                              |
|:-------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ca343-118">**ChangeSecurityPermissions**</span><span class="sxs-lookup"><span data-stu-id="ca343-118">**ChangeSecurityPermissions**</span></span>](changesecuritypermissions-method-in-class-cim-directory.md)     | <span data-ttu-id="ca343-119">Altera as permissões de segurança para o arquivo lógico especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="ca343-119">Changes the security permissions for the logical file specified in the object path.</span></span> <span data-ttu-id="ca343-120">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="ca343-120">Not implemented by WMI.</span></span><br/>                                   |
| [<span data-ttu-id="ca343-121">**ChangeSecurityPermissionsEx**</span><span class="sxs-lookup"><span data-stu-id="ca343-121">**ChangeSecurityPermissionsEx**</span></span>](changesecuritypermissionsex-method-in-class-cim-directory.md) | <span data-ttu-id="ca343-122">Altera as permissões de segurança para o arquivo lógico especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="ca343-122">Changes the security permissions for the logical file specified in the object path.</span></span> <span data-ttu-id="ca343-123">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="ca343-123">Not implemented by WMI.</span></span><br/>                                   |
| [<span data-ttu-id="ca343-124">**Compactar**</span><span class="sxs-lookup"><span data-stu-id="ca343-124">**Compress**</span></span>](compress-method-in-class-cim-directory.md)                                       | <span data-ttu-id="ca343-125">Compacta o arquivo lógico (ou diretório) especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="ca343-125">Compresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="ca343-126">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="ca343-126">Not implemented by WMI.</span></span><br/>                                              |
| [<span data-ttu-id="ca343-127">**CompressEx**</span><span class="sxs-lookup"><span data-stu-id="ca343-127">**CompressEx**</span></span>](compressex-method-in-class-cim-directory.md)                                   | <span data-ttu-id="ca343-128">Compacta o arquivo lógico (ou diretório) especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="ca343-128">Compresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="ca343-129">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="ca343-129">Not implemented by WMI.</span></span><br/>                                              |
| [<span data-ttu-id="ca343-130">**Copiar**</span><span class="sxs-lookup"><span data-stu-id="ca343-130">**Copy**</span></span>](copy-method-in-class-cim-directory.md)                                               | <span data-ttu-id="ca343-131">Copia o arquivo lógico (ou diretório) especificado no caminho do objeto para o local especificado pelo parâmetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="ca343-131">Copies the logical file (or directory) specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="ca343-132">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="ca343-132">Not implemented by WMI.</span></span><br/> |
| [<span data-ttu-id="ca343-133">**CopyEx**</span><span class="sxs-lookup"><span data-stu-id="ca343-133">**CopyEx**</span></span>](copyex-method-in-class-cim-directory.md)                                           | <span data-ttu-id="ca343-134">Copia o arquivo lógico (ou diretório) especificado no caminho do objeto para o local especificado pelo parâmetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="ca343-134">Copies the logical file (or directory) specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="ca343-135">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="ca343-135">Not implemented by WMI.</span></span><br/> |
| [<span data-ttu-id="ca343-136">**Excluir**</span><span class="sxs-lookup"><span data-stu-id="ca343-136">**Delete**</span></span>](delete-method-in-class-cim-directory.md)                                           | <span data-ttu-id="ca343-137">Exclui o arquivo lógico (ou diretório) especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="ca343-137">Deletes the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="ca343-138">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="ca343-138">Not implemented by WMI.</span></span><br/>                                                 |
| [<span data-ttu-id="ca343-139">**DeleteEx**</span><span class="sxs-lookup"><span data-stu-id="ca343-139">**DeleteEx**</span></span>](deleteex-method-in-class-cim-directory.md)                                       | <span data-ttu-id="ca343-140">Exclui o arquivo lógico (ou diretório) especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="ca343-140">Deletes the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="ca343-141">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="ca343-141">Not implemented by WMI.</span></span><br/>                                                 |
| [<span data-ttu-id="ca343-142">**GetEffectivePermission**</span><span class="sxs-lookup"><span data-stu-id="ca343-142">**GetEffectivePermission**</span></span>](geteffectivepermission-method-in-class-cim-directory.md)           | <span data-ttu-id="ca343-143">Determina se o chamador tem as permissões agregadas especificadas pelo argumento de **permissão** .</span><span class="sxs-lookup"><span data-stu-id="ca343-143">Determines whether the caller has the aggregated permissions specified by the **Permission** argument.</span></span> <span data-ttu-id="ca343-144">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="ca343-144">Not implemented by WMI.</span></span><br/>                |
| [<span data-ttu-id="ca343-145">**Renomear**</span><span class="sxs-lookup"><span data-stu-id="ca343-145">**Rename**</span></span>](rename-method-in-class-cim-directory.md)                                           | <span data-ttu-id="ca343-146">Renomeia o arquivo lógico (ou diretório) especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="ca343-146">Renames the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="ca343-147">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="ca343-147">Not implemented by WMI.</span></span><br/>                                                 |
| [<span data-ttu-id="ca343-148">**TakeOwnerShip**</span><span class="sxs-lookup"><span data-stu-id="ca343-148">**TakeOwnerShip**</span></span>](takeownership-method-in-class-cim-directory.md)                             | <span data-ttu-id="ca343-149">Obtém a propriedade do arquivo lógico especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="ca343-149">Obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="ca343-150">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="ca343-150">Not implemented by WMI.</span></span><br/>                                                   |
| [<span data-ttu-id="ca343-151">**TakeOwnerShipEx**</span><span class="sxs-lookup"><span data-stu-id="ca343-151">**TakeOwnerShipEx**</span></span>](takeownershipex-method-in-class-cim-directory.md)                         | <span data-ttu-id="ca343-152">Obtém a propriedade do arquivo lógico especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="ca343-152">Obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="ca343-153">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="ca343-153">Not implemented by WMI.</span></span><br/>                                                   |
| [<span data-ttu-id="ca343-154">**Descompactar**</span><span class="sxs-lookup"><span data-stu-id="ca343-154">**Uncompress**</span></span>](uncompress-method-in-class-cim-directory.md)                                   | <span data-ttu-id="ca343-155">Descompacta o arquivo lógico (ou diretório) especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="ca343-155">Uncompresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="ca343-156">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="ca343-156">Not implemented by WMI.</span></span><br/>                                            |
| [<span data-ttu-id="ca343-157">**UncompressEx**</span><span class="sxs-lookup"><span data-stu-id="ca343-157">**UncompressEx**</span></span>](uncompressex-method-in-class-cim-directory.md)                               | <span data-ttu-id="ca343-158">Descompacta o arquivo lógico (ou diretório) especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="ca343-158">Uncompresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="ca343-159">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="ca343-159">Not implemented by WMI.</span></span><br/>                                            |



 

### <a name="properties"></a><span data-ttu-id="ca343-160">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ca343-160">Properties</span></span>

<span data-ttu-id="ca343-161">A classe de **\_ diretório CIM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="ca343-161">The **CIM\_Directory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ca343-162">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="ca343-162">**AccessMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca343-163">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ca343-163">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ca343-164">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ca343-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca343-165">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("direitos de acesso")</span><span class="sxs-lookup"><span data-stu-id="ca343-165">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Access Rights")</span></span>
</dt> </dl>

<span data-ttu-id="ca343-166">Bitmask que representa os direitos de acesso necessários para acessar ou executar operações específicas no diretório.</span><span class="sxs-lookup"><span data-stu-id="ca343-166">Bitmask that represents the access rights required to access or perform specific operations on the directory.</span></span> <span data-ttu-id="ca343-167">Para obter valores, consulte [**constantes de direitos de acesso de arquivo e diretório**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants).</span><span class="sxs-lookup"><span data-stu-id="ca343-167">For values, see [**File and Directory Access Rights Constants**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants).</span></span>

> [!Note]  
> <span data-ttu-id="ca343-168">Em volumes FAT, o valor de **\_ acesso completo** é retornado, o que indica que nenhuma segurança foi definida no objeto.</span><span class="sxs-lookup"><span data-stu-id="ca343-168">On FAT volumes, the **FULL\_ACCESS** value is returned instead, which indicates no security has been set on the object.</span></span>

 

<span data-ttu-id="ca343-169">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="ca343-169">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="ca343-170">Do **arquivo \_ LER \_ os dados (arquivo) ou \_ \_ diretório de lista de arquivos (diretório)** (1)</span><span class="sxs-lookup"><span data-stu-id="ca343-170">**FILE\_READ\_DATA (file) or FILE\_LIST\_DIRECTORY (directory)** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="ca343-171">Do **arquivo \_ GRAVAR \_ dados (arquivo) ou arquivo \_ Adicionar \_ arquivo (diretório)** (2)</span><span class="sxs-lookup"><span data-stu-id="ca343-171">**FILE\_WRITE\_DATA (file) or FILE\_ADD\_FILE (directory)** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="ca343-172">Do **arquivo \_ ACRESCENTAR \_ dados (arquivo) ou arquivo \_ Adicionar \_ subdiretório (diretório)** (4)</span><span class="sxs-lookup"><span data-stu-id="ca343-172">**FILE\_APPEND\_DATA (file) or FILE\_ADD\_SUBDIRECTORY (directory)** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="ca343-173">Do **arquivo \_ LER \_ ea** (8)</span><span class="sxs-lookup"><span data-stu-id="ca343-173">**FILE\_READ\_EA** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="ca343-174">Do **arquivo \_ GRAVAR \_ ea** (16)</span><span class="sxs-lookup"><span data-stu-id="ca343-174">**FILE\_WRITE\_EA** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

<span data-ttu-id="ca343-175">Do **arquivo \_ EXECUTAR (arquivo) ou \_ atravessamento de arquivo (diretório)** (32)</span><span class="sxs-lookup"><span data-stu-id="ca343-175">**FILE\_EXECUTE (file) or FILE\_TRAVERSE (directory)** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="ca343-176">Do **arquivo \_ EXCLUIR \_ filho (diretório)** (64)</span><span class="sxs-lookup"><span data-stu-id="ca343-176">**FILE\_DELETE\_CHILD (directory)** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="ca343-177">Do **arquivo \_ \_Atributos de leitura** (128)</span><span class="sxs-lookup"><span data-stu-id="ca343-177">**FILE\_READ\_ATTRIBUTES** (128)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="ca343-178">Do **arquivo \_ \_Atributos de gravação** (256)</span><span class="sxs-lookup"><span data-stu-id="ca343-178">**FILE\_WRITE\_ATTRIBUTES** (256)</span></span>


</dt> <dd></dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="ca343-179">**Excluir** (65536)</span><span class="sxs-lookup"><span data-stu-id="ca343-179">**DELETE** (65536)</span></span>


</dt> <dd></dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="ca343-180">**Ler \_ CONTROLE** (131072)</span><span class="sxs-lookup"><span data-stu-id="ca343-180">**READ\_CONTROL** (131072)</span></span>


</dt> <dd></dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="ca343-181">**Gravar \_ DAC** (262144)</span><span class="sxs-lookup"><span data-stu-id="ca343-181">**WRITE\_DAC** (262144)</span></span>


</dt> <dd></dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="ca343-182">**Gravar \_ PROPRIETÁRIO** (524288)</span><span class="sxs-lookup"><span data-stu-id="ca343-182">**WRITE\_OWNER** (524288)</span></span>


</dt> <dd></dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="ca343-183">**Sincronizar** (1048576)</span><span class="sxs-lookup"><span data-stu-id="ca343-183">**SYNCHRONIZE** (1048576)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ca343-184">**Arquivar**</span><span class="sxs-lookup"><span data-stu-id="ca343-184">**Archive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca343-185">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="ca343-185">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ca343-186">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ca343-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca343-187">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("deve ser arquivado")</span><span class="sxs-lookup"><span data-stu-id="ca343-187">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Should Be Archived")</span></span>
</dt> </dl>

<span data-ttu-id="ca343-188">Se **for true**, o arquivo deverá ser arquivado.</span><span class="sxs-lookup"><span data-stu-id="ca343-188">If **True**, the file should be archived.</span></span>

<span data-ttu-id="ca343-189">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="ca343-189">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca343-190">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="ca343-190">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca343-191">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ca343-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca343-192">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ca343-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca343-193">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="ca343-193">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="ca343-194">Breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="ca343-194">Short textual description of the object.</span></span>

<span data-ttu-id="ca343-195">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ca343-195">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca343-196">**Compactado**</span><span class="sxs-lookup"><span data-stu-id="ca343-196">**Compressed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca343-197">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="ca343-197">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ca343-198">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ca343-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca343-199">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("compactado")</span><span class="sxs-lookup"><span data-stu-id="ca343-199">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compressed")</span></span>
</dt> </dl>

<span data-ttu-id="ca343-200">Se **for true**, o arquivo será compactado.</span><span class="sxs-lookup"><span data-stu-id="ca343-200">If **True**, the file is compressed.</span></span>

<span data-ttu-id="ca343-201">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="ca343-201">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca343-202">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="ca343-202">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca343-203">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ca343-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca343-204">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ca343-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca343-205">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("método de compactação")</span><span class="sxs-lookup"><span data-stu-id="ca343-205">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compression Method")</span></span>
</dt> </dl>

<span data-ttu-id="ca343-206">Cadeia de caracteres de forma livre que indica o algoritmo ou a ferramenta usada para compactar o arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="ca343-206">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="ca343-207">Se o esquema de compactação for desconhecido ou não estiver descrito, use "desconhecido".</span><span class="sxs-lookup"><span data-stu-id="ca343-207">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="ca343-208">Se o arquivo lógico estiver compactado, mas o esquema de compactação for desconhecido ou não estiver descrito, use "compactado".</span><span class="sxs-lookup"><span data-stu-id="ca343-208">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="ca343-209">Se o arquivo lógico não estiver compactado, use "não compactado".</span><span class="sxs-lookup"><span data-stu-id="ca343-209">If the logical file is not compressed, use "Not Compressed".</span></span>

<span data-ttu-id="ca343-210">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="ca343-210">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca343-211">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="ca343-211">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca343-212">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ca343-212">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca343-213">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ca343-213">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca343-214">Qualificadores: [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nome da classe")</span><span class="sxs-lookup"><span data-stu-id="ca343-214">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="ca343-215">Nome da classe.</span><span class="sxs-lookup"><span data-stu-id="ca343-215">Name of the class.</span></span>

<span data-ttu-id="ca343-216">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="ca343-216">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca343-217">**CreationDate**</span><span class="sxs-lookup"><span data-stu-id="ca343-217">**CreationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca343-218">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ca343-218">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ca343-219">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ca343-219">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca343-220">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("data de criação")</span><span class="sxs-lookup"><span data-stu-id="ca343-220">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Creation Date")</span></span>
</dt> </dl>

<span data-ttu-id="ca343-221">Data e hora em que o arquivo foi criado.</span><span class="sxs-lookup"><span data-stu-id="ca343-221">Date and time that the file was created.</span></span>

<span data-ttu-id="ca343-222">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="ca343-222">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca343-223">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="ca343-223">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca343-224">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ca343-224">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca343-225">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ca343-225">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca343-226">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema de arquivos CIM**](cim-filesystem.md).**CSCreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome da classe do sistema de computador ")</span><span class="sxs-lookup"><span data-stu-id="ca343-226">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSCreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="ca343-227">Classe do sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="ca343-227">Class of the computer system.</span></span>

<span data-ttu-id="ca343-228">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="ca343-228">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca343-229">**CSName**</span><span class="sxs-lookup"><span data-stu-id="ca343-229">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca343-230">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ca343-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca343-231">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ca343-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca343-232">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema de arquivos CIM**](cim-filesystem.md).**CSName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome do sistema de computador ")</span><span class="sxs-lookup"><span data-stu-id="ca343-232">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Name")</span></span>
</dt> </dl>

<span data-ttu-id="ca343-233">Nome do sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="ca343-233">Name of the computer system.</span></span>

<span data-ttu-id="ca343-234">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="ca343-234">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca343-235">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="ca343-235">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca343-236">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ca343-236">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca343-237">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ca343-237">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca343-238">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="ca343-238">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="ca343-239">Descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="ca343-239">Textual description of the object.</span></span>

<span data-ttu-id="ca343-240">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ca343-240">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca343-241">**Unidade**</span><span class="sxs-lookup"><span data-stu-id="ca343-241">**Drive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca343-242">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ca343-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca343-243">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ca343-243">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca343-244">Qualificadores: [**fixo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("drive")</span><span class="sxs-lookup"><span data-stu-id="ca343-244">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Drive")</span></span>
</dt> </dl>

<span data-ttu-id="ca343-245">Letra da unidade (incluindo os dois-pontos que segue a letra da unidade) do arquivo.</span><span class="sxs-lookup"><span data-stu-id="ca343-245">Drive letter (including the colon that follows the drive letter) of the file.</span></span> <span data-ttu-id="ca343-246">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="ca343-246">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="ca343-247">Exemplo: "c:"</span><span class="sxs-lookup"><span data-stu-id="ca343-247">Example: "c:"</span></span>

</dd> <dt>

<span data-ttu-id="ca343-248">**EightDotThreeFileName**</span><span class="sxs-lookup"><span data-stu-id="ca343-248">**EightDotThreeFileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca343-249">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ca343-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca343-250">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ca343-250">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca343-251">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("oito pontos três nome de arquivo")</span><span class="sxs-lookup"><span data-stu-id="ca343-251">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Eight Dot Three File Name")</span></span>
</dt> </dl>

<span data-ttu-id="ca343-252">Nome de arquivo compatível com o DOS.</span><span class="sxs-lookup"><span data-stu-id="ca343-252">DOS-compatible file name.</span></span> <span data-ttu-id="ca343-253">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="ca343-253">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="ca343-254">Exemplo: "c: \\ progra ~ 1"</span><span class="sxs-lookup"><span data-stu-id="ca343-254">Example: "c:\\progra~1"</span></span>

</dd> <dt>

<span data-ttu-id="ca343-255">**Criptografado**</span><span class="sxs-lookup"><span data-stu-id="ca343-255">**Encrypted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca343-256">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="ca343-256">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ca343-257">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ca343-257">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca343-258">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encrypted")</span><span class="sxs-lookup"><span data-stu-id="ca343-258">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encrypted")</span></span>
</dt> </dl>

<span data-ttu-id="ca343-259">Se **for true**, o arquivo será criptografado.</span><span class="sxs-lookup"><span data-stu-id="ca343-259">If **True**, the file is encrypted.</span></span>

<span data-ttu-id="ca343-260">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="ca343-260">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca343-261">**EncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="ca343-261">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca343-262">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ca343-262">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca343-263">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ca343-263">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca343-264">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("método de criptografia")</span><span class="sxs-lookup"><span data-stu-id="ca343-264">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encryption Method")</span></span>
</dt> </dl>

<span data-ttu-id="ca343-265">Cadeia de caracteres de forma livre que identifica o algoritmo ou a ferramenta usada para criptografar um arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="ca343-265">Free-form string that identifies the algorithm or tool used to encrypt a logical file.</span></span> <span data-ttu-id="ca343-266">Se o esquema de criptografia não for indulged (por motivos de segurança, por exemplo), use "desconhecido".</span><span class="sxs-lookup"><span data-stu-id="ca343-266">If the encryption scheme is not indulged (for security reasons, for example), use "Unknown".</span></span> <span data-ttu-id="ca343-267">Se o arquivo estiver criptografado, mas seu esquema de criptografia for desconhecido ou não for divulgado, use "Encrypted".</span><span class="sxs-lookup"><span data-stu-id="ca343-267">If the file is encrypted, but either its encryption scheme is unknown or not disclosed, use "Encrypted".</span></span> <span data-ttu-id="ca343-268">Se o arquivo lógico não estiver criptografado, use "não criptografado".</span><span class="sxs-lookup"><span data-stu-id="ca343-268">If the logical file is not encrypted, use "Not Encrypted".</span></span>

<span data-ttu-id="ca343-269">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="ca343-269">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca343-270">**Extensão**</span><span class="sxs-lookup"><span data-stu-id="ca343-270">**Extension**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca343-271">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ca343-271">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca343-272">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ca343-272">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca343-273">Qualificadores: [**fixo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("extensão de arquivo")</span><span class="sxs-lookup"><span data-stu-id="ca343-273">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Extension")</span></span>
</dt> </dl>

<span data-ttu-id="ca343-274">Extensão de nome de arquivo sem o ponto anterior (ponto).</span><span class="sxs-lookup"><span data-stu-id="ca343-274">File name extension without the preceding period (dot).</span></span>

<span data-ttu-id="ca343-275">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="ca343-275">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="ca343-276">Exemplo: "txt", "MOF", "mdb"</span><span class="sxs-lookup"><span data-stu-id="ca343-276">Example: "txt", "mof", "mdb"</span></span>

</dd> <dt>

<span data-ttu-id="ca343-277">**FileName**</span><span class="sxs-lookup"><span data-stu-id="ca343-277">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca343-278">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ca343-278">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca343-279">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ca343-279">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca343-280">Qualificadores: [**fixo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nome do arquivo")</span><span class="sxs-lookup"><span data-stu-id="ca343-280">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Name")</span></span>
</dt> </dl>

<span data-ttu-id="ca343-281">Nome do arquivo sem a extensão de nome de arquivo.</span><span class="sxs-lookup"><span data-stu-id="ca343-281">File name without the file name extension.</span></span>

<span data-ttu-id="ca343-282">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="ca343-282">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="ca343-283">Exemplo: "mydatafile"</span><span class="sxs-lookup"><span data-stu-id="ca343-283">Example: "MyDataFile"</span></span>

</dd> <dt>

<span data-ttu-id="ca343-284">**Tamanho**</span><span class="sxs-lookup"><span data-stu-id="ca343-284">**FileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca343-285">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ca343-285">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ca343-286">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ca343-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca343-287">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("tamanho"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="ca343-287">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Size"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="ca343-288">Tamanho do arquivo, em bytes.</span><span class="sxs-lookup"><span data-stu-id="ca343-288">Size of the file, in bytes.</span></span>

<span data-ttu-id="ca343-289">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="ca343-289">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="ca343-290">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="ca343-290">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="ca343-291">**Talvez**</span><span class="sxs-lookup"><span data-stu-id="ca343-291">**FileType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca343-292">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ca343-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca343-293">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ca343-293">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca343-294">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("tipo de arquivo")</span><span class="sxs-lookup"><span data-stu-id="ca343-294">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Type")</span></span>
</dt> </dl>

<span data-ttu-id="ca343-295">Descritor que representa o tipo de arquivo (indicado pela propriedade de **extensão** ).</span><span class="sxs-lookup"><span data-stu-id="ca343-295">Descriptor that represents the file type (indicated by the **Extension** property).</span></span>

<span data-ttu-id="ca343-296">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="ca343-296">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca343-297">**FSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="ca343-297">**FSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca343-298">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ca343-298">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca343-299">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ca343-299">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca343-300">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema de arquivos CIM**](cim-filesystem.md).**CreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome da classe do sistema de arquivos ")</span><span class="sxs-lookup"><span data-stu-id="ca343-300">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="ca343-301">Classe do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="ca343-301">Class of the file system.</span></span>

<span data-ttu-id="ca343-302">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="ca343-302">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca343-303">**FSName**</span><span class="sxs-lookup"><span data-stu-id="ca343-303">**FSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca343-304">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ca343-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca343-305">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ca343-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca343-306">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema de arquivos CIM**](cim-filesystem.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome do sistema de arquivos ")</span><span class="sxs-lookup"><span data-stu-id="ca343-306">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Name")</span></span>
</dt> </dl>

<span data-ttu-id="ca343-307">Nome do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="ca343-307">Name of the file system.</span></span>

<span data-ttu-id="ca343-308">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="ca343-308">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca343-309">**Oculto**</span><span class="sxs-lookup"><span data-stu-id="ca343-309">**Hidden**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca343-310">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="ca343-310">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ca343-311">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ca343-311">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca343-312">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hidden")</span><span class="sxs-lookup"><span data-stu-id="ca343-312">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hidden")</span></span>
</dt> </dl>

<span data-ttu-id="ca343-313">Se for **true**, o arquivo ficará oculto.</span><span class="sxs-lookup"><span data-stu-id="ca343-313">If **True**, the file is hidden.</span></span>

<span data-ttu-id="ca343-314">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="ca343-314">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca343-315">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="ca343-315">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca343-316">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ca343-316">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ca343-317">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ca343-317">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca343-318">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="ca343-318">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="ca343-319">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="ca343-319">Date and time when the object was installed.</span></span> <span data-ttu-id="ca343-320">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="ca343-320">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="ca343-321">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ca343-321">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca343-322">**InUseCount**</span><span class="sxs-lookup"><span data-stu-id="ca343-322">**InUseCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca343-323">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ca343-323">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ca343-324">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ca343-324">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca343-325">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("contagem de abertura de arquivo atual")</span><span class="sxs-lookup"><span data-stu-id="ca343-325">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Current File Open Count")</span></span>
</dt> </dl>

<span data-ttu-id="ca343-326">Número de "aberturas de arquivo" que estão atualmente ativos no arquivo.</span><span class="sxs-lookup"><span data-stu-id="ca343-326">Number of "file opens" that are currently active against the file.</span></span>

<span data-ttu-id="ca343-327">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="ca343-327">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="ca343-328">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="ca343-328">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="ca343-329">**LastAccessed**</span><span class="sxs-lookup"><span data-stu-id="ca343-329">**LastAccessed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca343-330">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ca343-330">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ca343-331">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ca343-331">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca343-332">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("último acesso")</span><span class="sxs-lookup"><span data-stu-id="ca343-332">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Accessed")</span></span>
</dt> </dl>

<span data-ttu-id="ca343-333">Data e hora em que o arquivo foi acessado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="ca343-333">Date and time that the file was last accessed.</span></span>

<span data-ttu-id="ca343-334">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="ca343-334">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca343-335">**LastModified**</span><span class="sxs-lookup"><span data-stu-id="ca343-335">**LastModified**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca343-336">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ca343-336">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ca343-337">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ca343-337">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca343-338">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("última modificação")</span><span class="sxs-lookup"><span data-stu-id="ca343-338">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Modified")</span></span>
</dt> </dl>

<span data-ttu-id="ca343-339">Data e hora em que o arquivo foi modificado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="ca343-339">Date and time that the file was last modified.</span></span>

<span data-ttu-id="ca343-340">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="ca343-340">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca343-341">**Nome**</span><span class="sxs-lookup"><span data-stu-id="ca343-341">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca343-342">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ca343-342">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca343-343">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ca343-343">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca343-344">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ca343-344">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ca343-345">Nome herdado que serve como uma chave de uma instância de arquivo lógico em um sistema de arquivos (forneça nomes de caminho completos).</span><span class="sxs-lookup"><span data-stu-id="ca343-345">Inherited name that serves as a key of a logical file instance within a file system (provide full path names).</span></span>

<span data-ttu-id="ca343-346">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ca343-346">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="ca343-347">Exemplo: "C: \\ Windows \\ System \\win.ini"</span><span class="sxs-lookup"><span data-stu-id="ca343-347">Example: "C:\\Windows\\system\\win.ini"</span></span>

</dd> <dt>

<span data-ttu-id="ca343-348">**Caminho**</span><span class="sxs-lookup"><span data-stu-id="ca343-348">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca343-349">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ca343-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca343-350">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ca343-350">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca343-351">Qualificadores: [**fixo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Path")</span><span class="sxs-lookup"><span data-stu-id="ca343-351">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Path")</span></span>
</dt> </dl>

<span data-ttu-id="ca343-352">Caminho do arquivo, incluindo as barras invertidas à esquerda e à direita.</span><span class="sxs-lookup"><span data-stu-id="ca343-352">Path of the file including the leading and trailing backslashes.</span></span> <span data-ttu-id="ca343-353">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="ca343-353">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="ca343-354">Exemplo: " \\ sistema do Windows \\ \\ "</span><span class="sxs-lookup"><span data-stu-id="ca343-354">Example: "\\windows\\system\\"</span></span>

</dd> <dt>

<span data-ttu-id="ca343-355">**Seres**</span><span class="sxs-lookup"><span data-stu-id="ca343-355">**Readable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca343-356">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="ca343-356">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ca343-357">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ca343-357">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca343-358">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("legível")</span><span class="sxs-lookup"><span data-stu-id="ca343-358">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Readable")</span></span>
</dt> </dl>

<span data-ttu-id="ca343-359">Se **for true**, o arquivo poderá ser lido.</span><span class="sxs-lookup"><span data-stu-id="ca343-359">If **True**, the file can be read.</span></span>

<span data-ttu-id="ca343-360">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="ca343-360">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca343-361">**Status**</span><span class="sxs-lookup"><span data-stu-id="ca343-361">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca343-362">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ca343-362">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca343-363">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ca343-363">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca343-364">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="ca343-364">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="ca343-365">Cadeia de caracteres que indica o status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="ca343-365">String that indicates the current status of the object.</span></span>

<span data-ttu-id="ca343-366">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ca343-366">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="ca343-367">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="ca343-367">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="ca343-368">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="ca343-368">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="ca343-369">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="ca343-369">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="ca343-370">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="ca343-370">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ca343-371">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="ca343-371">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="ca343-372">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="ca343-372">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="ca343-373">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="ca343-373">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="ca343-374">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="ca343-374">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="ca343-375">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="ca343-375">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="ca343-376">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="ca343-376">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="ca343-377">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="ca343-377">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="ca343-378">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="ca343-378">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="ca343-379">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="ca343-379">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ca343-380">**System**</span><span class="sxs-lookup"><span data-stu-id="ca343-380">**System**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca343-381">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="ca343-381">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ca343-382">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ca343-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca343-383">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("arquivo do sistema")</span><span class="sxs-lookup"><span data-stu-id="ca343-383">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System File")</span></span>
</dt> </dl>

<span data-ttu-id="ca343-384">Se for **true**, o arquivo será um arquivo do sistema.</span><span class="sxs-lookup"><span data-stu-id="ca343-384">If **True**, the file is a system file.</span></span>

<span data-ttu-id="ca343-385">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="ca343-385">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca343-386">**Gravável**</span><span class="sxs-lookup"><span data-stu-id="ca343-386">**Writeable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca343-387">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="ca343-387">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ca343-388">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ca343-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca343-389">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("gravável")</span><span class="sxs-lookup"><span data-stu-id="ca343-389">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Writeable")</span></span>
</dt> </dl>

<span data-ttu-id="ca343-390">Se **for true**, o arquivo poderá ser gravado.</span><span class="sxs-lookup"><span data-stu-id="ca343-390">If **True**, the file can be written.</span></span>

<span data-ttu-id="ca343-391">Essa propriedade é herdada [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="ca343-391">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ca343-392">Comentários</span><span class="sxs-lookup"><span data-stu-id="ca343-392">Remarks</span></span>

<span data-ttu-id="ca343-393">A classe de **\_ diretório CIM** é derivada de [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="ca343-393">The **CIM\_Directory** class is derived from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="ca343-394">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="ca343-394">WMI does not implement this class.</span></span> <span data-ttu-id="ca343-395">Para obter mais informações sobre classes derivadas **do \_ diretório CIM**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="ca343-395">For more information about classes derived from **CIM\_Directory**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="ca343-396">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="ca343-396">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="ca343-397">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="ca343-397">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca343-398">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ca343-398">Requirements</span></span>



| <span data-ttu-id="ca343-399">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca343-399">Requirement</span></span> | <span data-ttu-id="ca343-400">Valor</span><span class="sxs-lookup"><span data-stu-id="ca343-400">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ca343-401">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ca343-401">Minimum supported client</span></span><br/> | <span data-ttu-id="ca343-402">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ca343-402">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ca343-403">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ca343-403">Minimum supported server</span></span><br/> | <span data-ttu-id="ca343-404">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ca343-404">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ca343-405">Namespace</span><span class="sxs-lookup"><span data-stu-id="ca343-405">Namespace</span></span><br/>                | <span data-ttu-id="ca343-406">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="ca343-406">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ca343-407">MOF</span><span class="sxs-lookup"><span data-stu-id="ca343-407">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ca343-408"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ca343-408"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ca343-409">DLL</span><span class="sxs-lookup"><span data-stu-id="ca343-409">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ca343-410"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ca343-410"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca343-411">Confira também</span><span class="sxs-lookup"><span data-stu-id="ca343-411">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca343-412">**CIM \_ LogicalFile**</span><span class="sxs-lookup"><span data-stu-id="ca343-412">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

