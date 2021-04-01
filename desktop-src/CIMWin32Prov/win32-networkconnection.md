---
description: Representa uma conexão de rede ativa em um ambiente baseado no Windows.
ms.assetid: e16e5f13-ea28-4d75-9978-4ff2ef5e5506
ms.tgt_platform: multiple
title: Classe Win32_NetworkConnection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkConnection
- Win32_NetworkConnection.Caption
- Win32_NetworkConnection.Description
- Win32_NetworkConnection.InstallDate
- Win32_NetworkConnection.Status
- Win32_NetworkConnection.AccessMask
- Win32_NetworkConnection.Comment
- Win32_NetworkConnection.ConnectionState
- Win32_NetworkConnection.ConnectionType
- Win32_NetworkConnection.DisplayType
- Win32_NetworkConnection.LocalName
- Win32_NetworkConnection.Name
- Win32_NetworkConnection.Persistent
- Win32_NetworkConnection.ProviderName
- Win32_NetworkConnection.RemoteName
- Win32_NetworkConnection.RemotePath
- Win32_NetworkConnection.ResourceType
- Win32_NetworkConnection.UserName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 96d91008ff8ad2f947e6c9957d16c4f007d15e47
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646502"
---
# <a name="win32_networkconnection-class"></a><span data-ttu-id="8a5d7-103">\_Classe Win32 NetworkConnection</span><span class="sxs-lookup"><span data-stu-id="8a5d7-103">Win32\_NetworkConnection class</span></span>

<span data-ttu-id="8a5d7-104">A [classe WMI](../wmisdk/retrieving-a-class.md) **\_ NetworkConnection do Win32** representa uma conexão de rede ativa em um ambiente baseado no Windows.</span><span class="sxs-lookup"><span data-stu-id="8a5d7-104">The **Win32\_NetworkConnection** [WMI class](../wmisdk/retrieving-a-class.md)represents an active network connection in a Windows-based environment.</span></span>

<span data-ttu-id="8a5d7-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="8a5d7-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="8a5d7-106">As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.</span><span class="sxs-lookup"><span data-stu-id="8a5d7-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a5d7-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8a5d7-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4CD-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_NetworkConnection : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  uint32   AccessMask;
  string   Comment;
  string   ConnectionState;
  string   ConnectionType;
  string   DisplayType;
  string   LocalName;
  string   Name;
  boolean  Persistent;
  string   ProviderName;
  string   RemoteName;
  string   RemotePath;
  string   ResourceType;
  string   UserName;
};
```

## <a name="members"></a><span data-ttu-id="8a5d7-108">Membros</span><span class="sxs-lookup"><span data-stu-id="8a5d7-108">Members</span></span>

<span data-ttu-id="8a5d7-109">A classe **Win32 \_ NetworkConnection** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="8a5d7-109">The **Win32\_NetworkConnection** class has these types of members:</span></span>

-   [<span data-ttu-id="8a5d7-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8a5d7-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8a5d7-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8a5d7-111">Properties</span></span>

<span data-ttu-id="8a5d7-112">A classe **Win32 \_ NetworkConnection** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="8a5d7-112">The **Win32\_NetworkConnection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8a5d7-113">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="8a5d7-113">**AccessMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a5d7-114">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8a5d7-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8a5d7-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8a5d7-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a5d7-116">Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="8a5d7-116">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="8a5d7-117">Lista de direitos de acesso para determinado arquivo ou diretório mantido pelo usuário ou grupo em cujo nome a instância é retornada.</span><span class="sxs-lookup"><span data-stu-id="8a5d7-117">List of access rights to the given file or directory held by the user or group on whose behalf the instance is returned.</span></span> <span data-ttu-id="8a5d7-118">Em volumes FAT, o valor de **\_ acesso completo** é retornado, indicando que nenhuma segurança foi definida no objeto.</span><span class="sxs-lookup"><span data-stu-id="8a5d7-118">On FAT volumes, the **FULL\_ACCESS** value is returned instead, indicating no security has been set on the object.</span></span>

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="8a5d7-119"><span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>Do **arquivo \_ LER \_ os dados (arquivo) ou \_ \_ diretório de lista de arquivos (diretório)** (1)</span><span class="sxs-lookup"><span data-stu-id="8a5d7-119"><span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>**FILE\_READ\_DATA (file) or FILE\_LIST\_DIRECTORY (directory)** (1)</span></span>


</dt> <dd>

<span data-ttu-id="8a5d7-120">Concede o direito de ler dados do arquivo.</span><span class="sxs-lookup"><span data-stu-id="8a5d7-120">Grants the right to read data from the file.</span></span> <span data-ttu-id="8a5d7-121">Para um diretório, esse valor concede o direito de listar o conteúdo do diretório.</span><span class="sxs-lookup"><span data-stu-id="8a5d7-121">For a directory, this value grants the right to list the contents of the directory.</span></span>

</dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="8a5d7-122"><span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>Do **arquivo \_ GRAVAR \_ dados (arquivo) ou arquivo \_ Adicionar \_ arquivo (diretório)** (2)</span><span class="sxs-lookup"><span data-stu-id="8a5d7-122"><span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>**FILE\_WRITE\_DATA (file) or FILE\_ADD\_FILE (directory)** (2)</span></span>


</dt> <dd>

<span data-ttu-id="8a5d7-123">Concede o direito de gravar dados no arquivo.</span><span class="sxs-lookup"><span data-stu-id="8a5d7-123">Grants the right to write data to the file.</span></span> <span data-ttu-id="8a5d7-124">Para um diretório, esse valor concede o direito de criar um arquivo no diretório.</span><span class="sxs-lookup"><span data-stu-id="8a5d7-124">For a directory, this value grants the right to create a file in the directory.</span></span>

</dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY"></span><span id="file_append_data__file__or_file_add_subdirectory"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY"></span>

<span data-ttu-id="8a5d7-125"><span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY"></span><span id="file_append_data__file__or_file_add_subdirectory"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY"></span>Do **arquivo \_ ACRESCENTAR \_ dados (arquivo) ou arquivo \_ Adicionar \_ subdiretório** (4)</span><span class="sxs-lookup"><span data-stu-id="8a5d7-125"><span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY"></span><span id="file_append_data__file__or_file_add_subdirectory"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY"></span>**FILE\_APPEND\_DATA (file) or FILE\_ADD\_SUBDIRECTORY** (4)</span></span>


</dt> <dd>

<span data-ttu-id="8a5d7-126">Concede o direito de acrescentar dados ao arquivo.</span><span class="sxs-lookup"><span data-stu-id="8a5d7-126">Grants the right to append data to the file.</span></span> <span data-ttu-id="8a5d7-127">Para um diretório, esse valor concede o direito de criar um subdiretório.</span><span class="sxs-lookup"><span data-stu-id="8a5d7-127">For a directory, this value grants the right to create a subdirectory.</span></span>

</dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="8a5d7-128"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>Do **arquivo \_ LER \_ ea** (8)</span><span class="sxs-lookup"><span data-stu-id="8a5d7-128"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**FILE\_READ\_EA** (8)</span></span>


</dt> <dd>

<span data-ttu-id="8a5d7-129">Concede o direito de ler atributos estendidos.</span><span class="sxs-lookup"><span data-stu-id="8a5d7-129">Grants the right to read extended attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="8a5d7-130"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>Do **arquivo \_ GRAVAR \_ ea** (16)</span><span class="sxs-lookup"><span data-stu-id="8a5d7-130"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**FILE\_WRITE\_EA** (16)</span></span>


</dt> <dd>

<span data-ttu-id="8a5d7-131">Concede o direito de gravar atributos estendidos.</span><span class="sxs-lookup"><span data-stu-id="8a5d7-131">Grants the right to write extended attributes.</span></span>

</dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

<span data-ttu-id="8a5d7-132"><span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>Do **arquivo \_ EXECUTAR (arquivo) ou \_ atravessamento de arquivo (diretório)** (32)</span><span class="sxs-lookup"><span data-stu-id="8a5d7-132"><span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>**FILE\_EXECUTE (file) or FILE\_TRAVERSE (directory)** (32)</span></span>


</dt> <dd>

<span data-ttu-id="8a5d7-133">Concede o direito de executar um arquivo.</span><span class="sxs-lookup"><span data-stu-id="8a5d7-133">Grants the right to execute a file.</span></span> <span data-ttu-id="8a5d7-134">Para um diretório, o diretório pode ser atravessado.</span><span class="sxs-lookup"><span data-stu-id="8a5d7-134">For a directory, the directory can be traversed.</span></span>

</dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="8a5d7-135"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>Do **arquivo \_ EXCLUIR \_ filho (diretório)** (64)</span><span class="sxs-lookup"><span data-stu-id="8a5d7-135"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**FILE\_DELETE\_CHILD (directory)** (64)</span></span>


</dt> <dd>

<span data-ttu-id="8a5d7-136">Concede o direito de excluir um diretório e todos os arquivos que ele contém (seus filhos), mesmo que os arquivos sejam somente leitura.</span><span class="sxs-lookup"><span data-stu-id="8a5d7-136">Grants the right to delete a directory and all of the files it contains (its children), even if the files are read-only.</span></span>

</dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="8a5d7-137"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>Do **arquivo \_ \_Atributos de leitura** (128)</span><span class="sxs-lookup"><span data-stu-id="8a5d7-137"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**FILE\_READ\_ATTRIBUTES** (128)</span></span>


</dt> <dd>

<span data-ttu-id="8a5d7-138">Concede o direito de ler atributos de arquivo.</span><span class="sxs-lookup"><span data-stu-id="8a5d7-138">Grants the right to read file attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="8a5d7-139"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>Do **arquivo \_ \_Atributos de gravação** (256)</span><span class="sxs-lookup"><span data-stu-id="8a5d7-139"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**FILE\_WRITE\_ATTRIBUTES** (256)</span></span>


</dt> <dd>

<span data-ttu-id="8a5d7-140">Concede o direito de alterar atributos de arquivo.</span><span class="sxs-lookup"><span data-stu-id="8a5d7-140">Grants the right to change file attributes.</span></span>

</dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="8a5d7-141"><span id="DELETE"></span><span id="delete"></span>**Excluir** (65536)</span><span class="sxs-lookup"><span data-stu-id="8a5d7-141"><span id="DELETE"></span><span id="delete"></span>**DELETE** (65536)</span></span>


</dt> <dd>

<span data-ttu-id="8a5d7-142">Concede acesso de exclusão.</span><span class="sxs-lookup"><span data-stu-id="8a5d7-142">Grants delete access.</span></span>

</dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="8a5d7-143"><span id="READ_CONTROL"></span><span id="read_control"></span>**Ler \_ CONTROLE** (131072)</span><span class="sxs-lookup"><span data-stu-id="8a5d7-143"><span id="READ_CONTROL"></span><span id="read_control"></span>**READ\_CONTROL** (131072)</span></span>


</dt> <dd>

<span data-ttu-id="8a5d7-144">Concede acesso de leitura ao descritor de segurança e ao proprietário.</span><span class="sxs-lookup"><span data-stu-id="8a5d7-144">Grants read access to the security descriptor and owner.</span></span>

</dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="8a5d7-145"><span id="WRITE_DAC"></span><span id="write_dac"></span>**Gravar \_ DAC** (262144)</span><span class="sxs-lookup"><span data-stu-id="8a5d7-145"><span id="WRITE_DAC"></span><span id="write_dac"></span>**WRITE\_DAC** (262144)</span></span>


</dt> <dd>

<span data-ttu-id="8a5d7-146">Concede acesso de gravação à DACL (lista de controle de acesso discricionário).</span><span class="sxs-lookup"><span data-stu-id="8a5d7-146">Grants write access to the discretionary access control list (DACL).</span></span>

</dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="8a5d7-147"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**Gravar \_ PROPRIETÁRIO** (524288)</span><span class="sxs-lookup"><span data-stu-id="8a5d7-147"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**WRITE\_OWNER** (524288)</span></span>


</dt> <dd>

<span data-ttu-id="8a5d7-148">Atribui o proprietário da gravação.</span><span class="sxs-lookup"><span data-stu-id="8a5d7-148">Assigns the write owner.</span></span>

</dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="8a5d7-149"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**Sincronizar** (1048576)</span><span class="sxs-lookup"><span data-stu-id="8a5d7-149"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**SYNCHRONIZE** (1048576)</span></span>


</dt> <dd>

<span data-ttu-id="8a5d7-150">Sincroniza o acesso e permite que um processo Aguarde um objeto para entrar no estado sinalizado.</span><span class="sxs-lookup"><span data-stu-id="8a5d7-150">Synchronizes access and allows a process to wait for an object to enter the signaled state.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8a5d7-151">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="8a5d7-151">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a5d7-152">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8a5d7-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a5d7-153">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8a5d7-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a5d7-154">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="8a5d7-154">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="8a5d7-155">Uma breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="8a5d7-155">A short textual description of the object.</span></span>

<span data-ttu-id="8a5d7-156">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8a5d7-156">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8a5d7-157">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="8a5d7-157">**Comment**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a5d7-158">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8a5d7-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a5d7-159">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8a5d7-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a5d7-160">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Windows Networking estruturas \| [**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) \| *lpComment*")</span><span class="sxs-lookup"><span data-stu-id="8a5d7-160">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Windows Networking Structures\|[**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)\|*lpComment*")</span></span>
</dt> </dl>

<span data-ttu-id="8a5d7-161">Comentário fornecido pelo provedor de rede.</span><span class="sxs-lookup"><span data-stu-id="8a5d7-161">Comment supplied by the network provider.</span></span>

</dd> <dt>

<span data-ttu-id="8a5d7-162">**ConnectionState**</span><span class="sxs-lookup"><span data-stu-id="8a5d7-162">**ConnectionState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a5d7-163">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8a5d7-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a5d7-164">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8a5d7-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a5d7-165">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (20), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de gerenciamento de rede win32api \| [**usam \_ informações \_ 1**](/windows/win32/api/lmuse/ns-lmuse-use_info_1) \| **ui1 \_ status**")</span><span class="sxs-lookup"><span data-stu-id="8a5d7-165">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (20), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USE\_INFO\_1**](/windows/win32/api/lmuse/ns-lmuse-use_info_1)\|**ui1\_status**")</span></span>
</dt> </dl>

<span data-ttu-id="8a5d7-166">Estado atual da conexão de rede.</span><span class="sxs-lookup"><span data-stu-id="8a5d7-166">Current state of the network connection.</span></span>

<dt>

<span id="Connected"></span><span id="connected"></span><span id="CONNECTED"></span>

<span data-ttu-id="8a5d7-167">**Conectado** ("conectado")</span><span class="sxs-lookup"><span data-stu-id="8a5d7-167">**Connected** ("Connected")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="8a5d7-168">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="8a5d7-168">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="8a5d7-169">Em **pausa** ("pausado")</span><span class="sxs-lookup"><span data-stu-id="8a5d7-169">**Paused** ("Paused")</span></span>


</dt> <dd></dd> <dt>

<span id="Disconnected"></span><span id="disconnected"></span><span id="DISCONNECTED"></span>

<span data-ttu-id="8a5d7-170">**Desconectado** ("desconectado")</span><span class="sxs-lookup"><span data-stu-id="8a5d7-170">**Disconnected** ("Disconnected")</span></span>


</dt> <dd></dd> <dt>

<span id="Connecting"></span><span id="connecting"></span><span id="CONNECTING"></span>

<span data-ttu-id="8a5d7-171">**Conectando** ("conectando")</span><span class="sxs-lookup"><span data-stu-id="8a5d7-171">**Connecting** ("Connecting")</span></span>


</dt> <dd></dd> <dt>

<span id="Reconnecting"></span><span id="reconnecting"></span><span id="RECONNECTING"></span>

<span data-ttu-id="8a5d7-172">**Reconectando** ("reconectando")</span><span class="sxs-lookup"><span data-stu-id="8a5d7-172">**Reconnecting** ("Reconnecting")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8a5d7-173">**ConnectionType**</span><span class="sxs-lookup"><span data-stu-id="8a5d7-173">**ConnectionType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a5d7-174">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8a5d7-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a5d7-175">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8a5d7-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a5d7-176">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Windows Networking estruturas \| [**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) \| **dwScope**")</span><span class="sxs-lookup"><span data-stu-id="8a5d7-176">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Windows Networking Structures\|[**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)\|**dwScope**")</span></span>
</dt> </dl>

<span data-ttu-id="8a5d7-177">Tipo de persistência da conexão usada para conectar-se à rede.</span><span class="sxs-lookup"><span data-stu-id="8a5d7-177">Persistence type of the connection used for connecting to the network.</span></span>

<dt>

<span id="Current_Connection"></span><span id="current_connection"></span><span id="CURRENT_CONNECTION"></span>

<span data-ttu-id="8a5d7-178">**Conexão atual** ("conexão atual")</span><span class="sxs-lookup"><span data-stu-id="8a5d7-178">**Current Connection** ("Current Connection")</span></span>


</dt> <dd></dd> <dt>

<span id="Persistent_Connection"></span><span id="persistent_connection"></span><span id="PERSISTENT_CONNECTION"></span>

<span data-ttu-id="8a5d7-179">**Conexão persistente** ("conexão persistente")</span><span class="sxs-lookup"><span data-stu-id="8a5d7-179">**Persistent Connection** ("Persistent Connection")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8a5d7-180">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="8a5d7-180">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a5d7-181">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8a5d7-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a5d7-182">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8a5d7-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a5d7-183">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="8a5d7-183">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="8a5d7-184">Uma descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="8a5d7-184">A textual description of the object.</span></span>

<span data-ttu-id="8a5d7-185">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8a5d7-185">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8a5d7-186">**TipoDeExibição**</span><span class="sxs-lookup"><span data-stu-id="8a5d7-186">**DisplayType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a5d7-187">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8a5d7-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a5d7-188">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8a5d7-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a5d7-189">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Windows Networking estruturas \| [**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) \| **dwDisplayType**")</span><span class="sxs-lookup"><span data-stu-id="8a5d7-189">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Windows Networking Structures\|[**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)\|**dwDisplayType**")</span></span>
</dt> </dl>

<span data-ttu-id="8a5d7-190">O objeto de rede deve ser exibido em uma interface de usuário de navegação de rede.</span><span class="sxs-lookup"><span data-stu-id="8a5d7-190">Network object should be displayed in a network browsing user interface.</span></span>

<dt>

<span id="Domain"></span><span id="domain"></span><span id="DOMAIN"></span>

<span data-ttu-id="8a5d7-191">**Domínio** ("domínio")</span><span class="sxs-lookup"><span data-stu-id="8a5d7-191">**Domain** ("Domain")</span></span>


</dt> <dd></dd> <dt>

<span id="Generic"></span><span id="generic"></span><span id="GENERIC"></span>

<span data-ttu-id="8a5d7-192">**Genérico** ("genérico")</span><span class="sxs-lookup"><span data-stu-id="8a5d7-192">**Generic** ("Generic")</span></span>


</dt> <dd></dd> <dt>

<span id="Server"></span><span id="server"></span><span id="SERVER"></span>

<span data-ttu-id="8a5d7-193">**Servidor** ("servidor")</span><span class="sxs-lookup"><span data-stu-id="8a5d7-193">**Server** ("Server")</span></span>


</dt> <dd></dd> <dt>

<span id="Share"></span><span id="share"></span><span id="SHARE"></span>

<span data-ttu-id="8a5d7-194">**Compartilhamento** ("compartilhamento")</span><span class="sxs-lookup"><span data-stu-id="8a5d7-194">**Share** ("Share")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8a5d7-195">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="8a5d7-195">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a5d7-196">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8a5d7-196">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8a5d7-197">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8a5d7-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a5d7-198">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="8a5d7-198">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="8a5d7-199">Indica quando o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="8a5d7-199">Indicates when the object was installed.</span></span> <span data-ttu-id="8a5d7-200">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="8a5d7-200">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="8a5d7-201">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8a5d7-201">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8a5d7-202">**LocalName**</span><span class="sxs-lookup"><span data-stu-id="8a5d7-202">**LocalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a5d7-203">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8a5d7-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a5d7-204">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8a5d7-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a5d7-205">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Windows Networking estruturas \| [**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) \| **lpLocalName**")</span><span class="sxs-lookup"><span data-stu-id="8a5d7-205">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Windows Networking Structures\|[**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)\|**lpLocalName**")</span></span>
</dt> </dl>

<span data-ttu-id="8a5d7-206">Nome local do dispositivo de rede conectado.</span><span class="sxs-lookup"><span data-stu-id="8a5d7-206">Local name of the connected network device.</span></span>

<span data-ttu-id="8a5d7-207">Exemplo: "c: \\ Public"</span><span class="sxs-lookup"><span data-stu-id="8a5d7-207">Example: "c:\\public"</span></span>

</dd> <dt>

<span data-ttu-id="8a5d7-208">**Nome**</span><span class="sxs-lookup"><span data-stu-id="8a5d7-208">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a5d7-209">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8a5d7-209">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a5d7-210">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8a5d7-210">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a5d7-211">Qualificadores: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WIN32API \| Windows Networking estruturas \| [**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)")</span><span class="sxs-lookup"><span data-stu-id="8a5d7-211">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Windows Networking Structures\|[**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)")</span></span>
</dt> </dl>

<span data-ttu-id="8a5d7-212">Nome da conexão de rede atual.</span><span class="sxs-lookup"><span data-stu-id="8a5d7-212">Name of the current network connection.</span></span> <span data-ttu-id="8a5d7-213">É a combinação dos valores em **RemoteName** e **LocalName**.</span><span class="sxs-lookup"><span data-stu-id="8a5d7-213">It is the combination of the values in **RemoteName** and **LocalName**.</span></span>

<span data-ttu-id="8a5d7-214">Exemplo: " \\ \\ NTRELEASE (c: \\ Public)"</span><span class="sxs-lookup"><span data-stu-id="8a5d7-214">Example: "\\\\NTRELEASE (c:\\public)"</span></span>

</dd> <dt>

<span data-ttu-id="8a5d7-215">**Persistente**</span><span class="sxs-lookup"><span data-stu-id="8a5d7-215">**Persistent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a5d7-216">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="8a5d7-216">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8a5d7-217">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8a5d7-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a5d7-218">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| WNetEnumResource funções de rede do Windows \| [](/windows/win32/api/winnetwk/nf-winnetwk-wnetenumresourcea)")</span><span class="sxs-lookup"><span data-stu-id="8a5d7-218">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Windows Networking Functions\|[**WNetEnumResource**](/windows/win32/api/winnetwk/nf-winnetwk-wnetenumresourcea)")</span></span>
</dt> </dl>

<span data-ttu-id="8a5d7-219">A conexão será reconectada automaticamente pelo sistema operacional no próximo logon.</span><span class="sxs-lookup"><span data-stu-id="8a5d7-219">Connection will be reconnected automatically by the operating system on the next logon.</span></span>

</dd> <dt>

<span data-ttu-id="8a5d7-220">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="8a5d7-220">**ProviderName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a5d7-221">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8a5d7-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a5d7-222">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8a5d7-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a5d7-223">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Windows Networking estruturas \| [**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) \| **lpProvider**")</span><span class="sxs-lookup"><span data-stu-id="8a5d7-223">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Windows Networking Structures\|[**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)\|**lpProvider**")</span></span>
</dt> </dl>

<span data-ttu-id="8a5d7-224">Nome do provedor que possui o recurso.</span><span class="sxs-lookup"><span data-stu-id="8a5d7-224">Name of the provider that owns the resource.</span></span> <span data-ttu-id="8a5d7-225">Essa propriedade poderá ser **nula** se o nome do provedor for desconhecido.</span><span class="sxs-lookup"><span data-stu-id="8a5d7-225">This property can be **NULL** if the provider name is unknown.</span></span>

</dd> <dt>

<span data-ttu-id="8a5d7-226">**RemoteName**</span><span class="sxs-lookup"><span data-stu-id="8a5d7-226">**RemoteName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a5d7-227">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8a5d7-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a5d7-228">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8a5d7-228">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a5d7-229">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Windows Networking estruturas \| [**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) \| **lpRemoteName**")</span><span class="sxs-lookup"><span data-stu-id="8a5d7-229">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Windows Networking Structures\|[**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)\|**lpRemoteName**")</span></span>
</dt> </dl>

<span data-ttu-id="8a5d7-230">Nome do recurso de rede remota para um recurso de rede.</span><span class="sxs-lookup"><span data-stu-id="8a5d7-230">Remote network resource name for a network resource.</span></span> <span data-ttu-id="8a5d7-231">Para uma conexão atual ou persistente, **RemoteName** contém o nome de rede associado ao nome do valor na propriedade **LocalName** .</span><span class="sxs-lookup"><span data-stu-id="8a5d7-231">For a current or persistent connection, **RemoteName** contains the network name associated with the name of the value in the **LocalName** property.</span></span> <span data-ttu-id="8a5d7-232">O nome em **RemoteName** deve seguir as convenções de nomenclatura do provedor de rede.</span><span class="sxs-lookup"><span data-stu-id="8a5d7-232">The name in **RemoteName** must follow the network provider's naming conventions.</span></span>

<span data-ttu-id="8a5d7-233">Exemplo: " \\ \\ NTRELEASE"</span><span class="sxs-lookup"><span data-stu-id="8a5d7-233">Example: "\\\\NTRELEASE"</span></span>

</dd> <dt>

<span data-ttu-id="8a5d7-234">**RemotePath**</span><span class="sxs-lookup"><span data-stu-id="8a5d7-234">**RemotePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a5d7-235">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8a5d7-235">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a5d7-236">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8a5d7-236">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a5d7-237">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Windows Networking estruturas \| [**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) \| **lpRemoteName**")</span><span class="sxs-lookup"><span data-stu-id="8a5d7-237">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Windows Networking Structures\|[**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)\|**lpRemoteName**")</span></span>
</dt> </dl>

<span data-ttu-id="8a5d7-238">Caminho completo para o recurso de rede.</span><span class="sxs-lookup"><span data-stu-id="8a5d7-238">Full path to the network resource.</span></span>

<span data-ttu-id="8a5d7-239">Exemplo: " \\ \\ infosrv1 \\ Public"</span><span class="sxs-lookup"><span data-stu-id="8a5d7-239">Example: "\\\\infosrv1\\public"</span></span>

</dd> <dt>

<span data-ttu-id="8a5d7-240">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="8a5d7-240">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a5d7-241">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8a5d7-241">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a5d7-242">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8a5d7-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a5d7-243">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Windows Networking estruturas \| [**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) \| **dwType**")</span><span class="sxs-lookup"><span data-stu-id="8a5d7-243">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Windows Networking Structures\|[**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)\|**dwType**")</span></span>
</dt> </dl>

<span data-ttu-id="8a5d7-244">Tipo de recurso para o qual enumerar ou se conectar.</span><span class="sxs-lookup"><span data-stu-id="8a5d7-244">Type of resource to enumerate or connect to.</span></span>

<dt>

<span id="Disk"></span><span id="disk"></span><span id="DISK"></span>

<span data-ttu-id="8a5d7-245">**Disco** ("disco")</span><span class="sxs-lookup"><span data-stu-id="8a5d7-245">**Disk** ("Disk")</span></span>


</dt> <dd></dd> <dt>

<span id="Print"></span><span id="print"></span><span id="PRINT"></span>

<span data-ttu-id="8a5d7-246">**Imprimir** ("imprimir")</span><span class="sxs-lookup"><span data-stu-id="8a5d7-246">**Print** ("Print")</span></span>


</dt> <dd></dd> <dt>

<span id="Any"></span><span id="any"></span><span id="ANY"></span>

<span data-ttu-id="8a5d7-247">**Qualquer** ("qualquer")</span><span class="sxs-lookup"><span data-stu-id="8a5d7-247">**Any** ("Any")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8a5d7-248">**Status**</span><span class="sxs-lookup"><span data-stu-id="8a5d7-248">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a5d7-249">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8a5d7-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a5d7-250">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8a5d7-250">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a5d7-251">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="8a5d7-251">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="8a5d7-252">Cadeia de caracteres que indica o status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="8a5d7-252">String that indicates the current status of the object.</span></span> <span data-ttu-id="8a5d7-253">O status operacional e não operacional pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="8a5d7-253">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="8a5d7-254">O status operacional pode incluir "OK", "degradado" e "Pred falha".</span><span class="sxs-lookup"><span data-stu-id="8a5d7-254">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="8a5d7-255">"Pred Fail" indica que um elemento está funcionando corretamente, mas está prevendo uma falha (por exemplo, uma unidade de disco rígido habilitada para inteligente).</span><span class="sxs-lookup"><span data-stu-id="8a5d7-255">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="8a5d7-256">O status não operacional pode incluir "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="8a5d7-256">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="8a5d7-257">O "serviço" pode ser aplicado durante o espelhamento de disco – reprateando, recarregando uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="8a5d7-257">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="8a5d7-258">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="8a5d7-258">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="8a5d7-259">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8a5d7-259">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="8a5d7-260">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="8a5d7-260">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="8a5d7-261">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="8a5d7-261">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="8a5d7-262">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="8a5d7-262">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="8a5d7-263">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="8a5d7-263">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8a5d7-264">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="8a5d7-264">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="8a5d7-265">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="8a5d7-265">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="8a5d7-266">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="8a5d7-266">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="8a5d7-267">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="8a5d7-267">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="8a5d7-268">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="8a5d7-268">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="8a5d7-269">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="8a5d7-269">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="8a5d7-270">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="8a5d7-270">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="8a5d7-271">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="8a5d7-271">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="8a5d7-272">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="8a5d7-272">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8a5d7-273">**UserName**</span><span class="sxs-lookup"><span data-stu-id="8a5d7-273">**UserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a5d7-274">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8a5d7-274">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a5d7-275">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8a5d7-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a5d7-276">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| WNetGetUser funções de rede do Windows \| [](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetusera)")</span><span class="sxs-lookup"><span data-stu-id="8a5d7-276">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Windows Networking Functions\|[**WNetGetUser**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetusera)")</span></span>
</dt> </dl>

<span data-ttu-id="8a5d7-277">Nome de usuário ou o nome de usuário padrão usado para estabelecer uma conexão de rede.</span><span class="sxs-lookup"><span data-stu-id="8a5d7-277">User name or the default user name used to establish a network connection.</span></span>

<span data-ttu-id="8a5d7-278">Exemplo: "SYSTEM"</span><span class="sxs-lookup"><span data-stu-id="8a5d7-278">Example: "SYSTEM"</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8a5d7-279">Comentários</span><span class="sxs-lookup"><span data-stu-id="8a5d7-279">Remarks</span></span>

<span data-ttu-id="8a5d7-280">A classe **Win32 \_ NetworkConnection** é derivada de [**CIM \_ LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="8a5d7-280">The **Win32\_NetworkConnection** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

## <a name="examples"></a><span data-ttu-id="8a5d7-281">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8a5d7-281">Examples</span></span>

<span data-ttu-id="8a5d7-282">O exemplo de código VBScript a seguir recupera informações sobre a conexão de rede local.</span><span class="sxs-lookup"><span data-stu-id="8a5d7-282">The following VBScript code sample retrieves information on the local network connection.</span></span>


```VB
On Error Resume Next
strComputer = "."
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\Root\CIMv2")
Set colItems = objWMIService.ExecQuery("Select * from Win32_NetworkConnection",,48)
For Each objItem in colItems
    Wscript.Echo "AccessMask: " & objItem.AccessMask
    Wscript.Echo "Caption: " & objItem.Caption
    Wscript.Echo "Comment: " & objItem.Comment
    Wscript.Echo "ConnectionState: " & objItem.ConnectionState
    Wscript.Echo "ConnectionType: " & objItem.ConnectionType
    Wscript.Echo "Description: " & objItem.Description
    Wscript.Echo "DisplayType: " & objItem.DisplayType
    Wscript.Echo "InstallDate: " & objItem.InstallDate
    Wscript.Echo "LocalName: " & objItem.LocalName
    Wscript.Echo "Name: " & objItem.Name
    Wscript.Echo "Persistent: " & objItem.Persistent
    Wscript.Echo "ProviderName: " & objItem.ProviderName
    Wscript.Echo "RemoteName: " & objItem.RemoteName
    Wscript.Echo "RemotePath: " & objItem.RemotePath
    Wscript.Echo "ResourceType: " & objItem.ResourceType
    Wscript.Echo "Status: " & objItem.Status
    Wscript.Echo "UserName: " & objItem.UserName
Next
```



## <a name="requirements"></a><span data-ttu-id="8a5d7-283">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8a5d7-283">Requirements</span></span>



| <span data-ttu-id="8a5d7-284">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a5d7-284">Requirement</span></span> | <span data-ttu-id="8a5d7-285">Valor</span><span class="sxs-lookup"><span data-stu-id="8a5d7-285">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8a5d7-286">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8a5d7-286">Minimum supported client</span></span><br/> | <span data-ttu-id="8a5d7-287">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8a5d7-287">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8a5d7-288">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8a5d7-288">Minimum supported server</span></span><br/> | <span data-ttu-id="8a5d7-289">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8a5d7-289">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8a5d7-290">Namespace</span><span class="sxs-lookup"><span data-stu-id="8a5d7-290">Namespace</span></span><br/>                | <span data-ttu-id="8a5d7-291">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="8a5d7-291">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8a5d7-292">MOF</span><span class="sxs-lookup"><span data-stu-id="8a5d7-292">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8a5d7-293"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8a5d7-293"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8a5d7-294">DLL</span><span class="sxs-lookup"><span data-stu-id="8a5d7-294">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8a5d7-295"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8a5d7-295"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a5d7-296">Confira também</span><span class="sxs-lookup"><span data-stu-id="8a5d7-296">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a5d7-297">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="8a5d7-297">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

[<span data-ttu-id="8a5d7-298">Classes do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="8a5d7-298">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
