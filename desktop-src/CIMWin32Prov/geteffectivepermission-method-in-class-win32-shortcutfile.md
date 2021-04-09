---
description: Determina se o usuário tem todas as permissões necessárias especificadas no parâmetro Permissions para o objeto File, o diretório e o compartilhamento onde o arquivo de atalho está localizado, se o arquivo ou diretório estiver em um compartilhamento.
ms.assetid: 36f823c1-fa19-40a1-b750-41e1f73bdf01
ms.tgt_platform: multiple
title: Método GetEffectivePermission da classe Win32_ShortcutFile (aclui. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ShortcutFile.GetEffectivePermission
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 52b57318ac05212304024ead82026d6daf0d8ea4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089102"
---
# <a name="geteffectivepermission-method-of-the-win32_shortcutfile-class"></a><span data-ttu-id="f3322-103">Método GetEffectivePermission da \_ classe shortcutfile do Win32</span><span class="sxs-lookup"><span data-stu-id="f3322-103">GetEffectivePermission method of the Win32\_ShortcutFile class</span></span>

<span data-ttu-id="f3322-104">O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **GetEffectivePermission** determina se o usuário tem todas as permissões necessárias especificadas no parâmetro *Permissions* para o objeto File, o diretório e o compartilhamento onde o arquivo de atalho está localizado, se o arquivo ou diretório estiver em um compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="f3322-104">The **GetEffectivePermission** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method determines whether the user has all of the required permissions specified in the *Permissions* parameter for the file object, directory, and share where the shortcut file is located, if the file or directory is on a share.</span></span>

<span data-ttu-id="f3322-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="f3322-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="f3322-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="f3322-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="f3322-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f3322-107">Syntax</span></span>


```mof
boolean GetEffectivePermission(
  [in] uint32 Permissions
);
```



## <a name="parameters"></a><span data-ttu-id="f3322-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f3322-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3322-109">*Permissões* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="f3322-109">*Permissions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3322-110">Bitmap de permissões.</span><span class="sxs-lookup"><span data-stu-id="f3322-110">Bitmap of permissions.</span></span>

<dt>

<span id="FILE_READ_DATA__file__FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="f3322-111"><span id="FILE_READ_DATA__file__FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__FILE_LIST_DIRECTORY__DIRECTORY_"></span>Do **arquivo \_ LER \_ os dados (arquivo) \_ diretório de lista \_ de arquivos (diretório)** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="f3322-111"><span id="FILE_READ_DATA__file__FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__FILE_LIST_DIRECTORY__DIRECTORY_"></span>**FILE\_READ\_DATA (file) FILE\_LIST\_DIRECTORY (directory)** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="f3322-112">Concede o direito de ler dados do arquivo.</span><span class="sxs-lookup"><span data-stu-id="f3322-112">Grants the right to read data from the file.</span></span> <span data-ttu-id="f3322-113">Para um diretório, esse valor concede o direito de listar o conteúdo do diretório.</span><span class="sxs-lookup"><span data-stu-id="f3322-113">For a directory, this value grants the right to list the contents of the directory.</span></span>

</dd> <dt>

<span id="FILE_WRITE_DATA__file__FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="f3322-114"><span id="FILE_WRITE_DATA__file__FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__FILE_ADD_FILE__DIRECTORY_"></span>Do **arquivo \_ GRAVAR \_ dados (arquivo) arquivo \_ Adicionar \_ arquivo (diretório)** (2 (0x2))</span><span class="sxs-lookup"><span data-stu-id="f3322-114"><span id="FILE_WRITE_DATA__file__FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__FILE_ADD_FILE__DIRECTORY_"></span>**FILE\_WRITE\_DATA (file) FILE\_ADD\_FILE (directory)** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="f3322-115">Concede o direito de gravar dados no arquivo.</span><span class="sxs-lookup"><span data-stu-id="f3322-115">Grants the right to write data to the file.</span></span> <span data-ttu-id="f3322-116">Para um diretório, esse valor concede o direito de criar um arquivo no diretório.</span><span class="sxs-lookup"><span data-stu-id="f3322-116">For a directory, this value grants the right to create a file in the directory.</span></span>

</dd> <dt>

<span id="FILE_APPEND_DATA__file__FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="f3322-117"><span id="FILE_APPEND_DATA__file__FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>Do **arquivo \_ ACRESCENTAR \_ dados (arquivo) arquivo \_ Adicionar \_ subdiretório (diretório)** (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="f3322-117"><span id="FILE_APPEND_DATA__file__FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>**FILE\_APPEND\_DATA (file) FILE\_ADD\_SUBDIRECTORY (directory)** (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="f3322-118">Concede o direito de acrescentar dados ao arquivo.</span><span class="sxs-lookup"><span data-stu-id="f3322-118">Grants the right to append data to the file.</span></span> <span data-ttu-id="f3322-119">Para um diretório, esse valor concede o direito de criar um subdiretório.</span><span class="sxs-lookup"><span data-stu-id="f3322-119">For a directory, this value grants the right to create a subdirectory.</span></span>

</dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="f3322-120"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>Do **arquivo \_ LER \_ ea** (8 (0x8))</span><span class="sxs-lookup"><span data-stu-id="f3322-120"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**FILE\_READ\_EA** (8 (0x8))</span></span>


</dt> <dd>

<span data-ttu-id="f3322-121">Concede o direito de ler atributos estendidos.</span><span class="sxs-lookup"><span data-stu-id="f3322-121">Grants the right to read extended attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="f3322-122"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>Do **arquivo \_ GRAVAR \_ ea** (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="f3322-122"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**FILE\_WRITE\_EA** (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="f3322-123">Concede o direito de gravar atributos estendidos.</span><span class="sxs-lookup"><span data-stu-id="f3322-123">Grants the right to write extended attributes.</span></span>

</dd> <dt>

<span id="FILE_EXECUTE__file__FILE_TRAVERSE_directory_"></span><span id="file_execute__file__file_traverse_directory_"></span><span id="FILE_EXECUTE__FILE__FILE_TRAVERSE_DIRECTORY_"></span>

<span data-ttu-id="f3322-124"><span id="FILE_EXECUTE__file__FILE_TRAVERSE_directory_"></span><span id="file_execute__file__file_traverse_directory_"></span><span id="FILE_EXECUTE__FILE__FILE_TRAVERSE_DIRECTORY_"></span>Do **arquivo \_ EXECUTAR (arquivo) \_ atravessamento do arquivo (diretório)** (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="f3322-124"><span id="FILE_EXECUTE__file__FILE_TRAVERSE_directory_"></span><span id="file_execute__file__file_traverse_directory_"></span><span id="FILE_EXECUTE__FILE__FILE_TRAVERSE_DIRECTORY_"></span>**FILE\_EXECUTE (file) FILE\_TRAVERSE (directory)** (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="f3322-125">Concede o direito de executar um arquivo.</span><span class="sxs-lookup"><span data-stu-id="f3322-125">Grants the right to execute a file.</span></span> <span data-ttu-id="f3322-126">Para um diretório, o diretório pode ser atravessado.</span><span class="sxs-lookup"><span data-stu-id="f3322-126">For a directory, the directory can be traversed.</span></span>

</dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="f3322-127"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>Do **arquivo \_ EXCLUIR \_ filho (diretório)** (64 (0x40))</span><span class="sxs-lookup"><span data-stu-id="f3322-127"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**FILE\_DELETE\_CHILD (directory)** (64 (0x40))</span></span>


</dt> <dd>

<span data-ttu-id="f3322-128">Concede o direito de excluir um diretório e todos os arquivos que ele contém, mesmo que os arquivos sejam somente leitura.</span><span class="sxs-lookup"><span data-stu-id="f3322-128">Grants the right to delete a directory and all of the files it contains, even if the files are read-only.</span></span>

</dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="f3322-129"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>Do **arquivo \_ \_Atributos de leitura** (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="f3322-129"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**FILE\_READ\_ATTRIBUTES** (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="f3322-130">Concede o direito de ler atributos de arquivo.</span><span class="sxs-lookup"><span data-stu-id="f3322-130">Grants the right to read file attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="f3322-131"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>Do **arquivo \_ \_Atributos de gravação** (256 (0x100))</span><span class="sxs-lookup"><span data-stu-id="f3322-131"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**FILE\_WRITE\_ATTRIBUTES** (256 (0x100))</span></span>


</dt> <dd>

<span data-ttu-id="f3322-132">Concede o direito de alterar atributos de arquivo.</span><span class="sxs-lookup"><span data-stu-id="f3322-132">Grants the right to change file attributes.</span></span>

</dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="f3322-133"><span id="DELETE"></span><span id="delete"></span>**Excluir** (65536 (0x10000))</span><span class="sxs-lookup"><span data-stu-id="f3322-133"><span id="DELETE"></span><span id="delete"></span>**DELETE** (65536 (0x10000))</span></span>


</dt> <dd>

<span data-ttu-id="f3322-134">Concede acesso de exclusão.</span><span class="sxs-lookup"><span data-stu-id="f3322-134">Grants delete access.</span></span>

</dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="f3322-135"><span id="READ_CONTROL"></span><span id="read_control"></span>**Ler \_ CONTROLE** (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="f3322-135"><span id="READ_CONTROL"></span><span id="read_control"></span>**READ\_CONTROL** (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="f3322-136">Concede acesso de leitura ao descritor de segurança e ao proprietário.</span><span class="sxs-lookup"><span data-stu-id="f3322-136">Grants read access to the security descriptor and owner.</span></span>

</dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="f3322-137"><span id="WRITE_DAC"></span><span id="write_dac"></span>**Gravar \_ DAC** (262144 (0x40000))</span><span class="sxs-lookup"><span data-stu-id="f3322-137"><span id="WRITE_DAC"></span><span id="write_dac"></span>**WRITE\_DAC** (262144 (0x40000))</span></span>


</dt> <dd>

<span data-ttu-id="f3322-138">Concede acesso de gravação à DACL (lista de controle de acesso discricionário).</span><span class="sxs-lookup"><span data-stu-id="f3322-138">Grants write access to the discretionary access control list (DACL).</span></span>

</dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="f3322-139"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**Gravar \_ PROPRIETÁRIO** (524288 (0x80000))</span><span class="sxs-lookup"><span data-stu-id="f3322-139"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**WRITE\_OWNER** (524288 (0x80000))</span></span>


</dt> <dd>

<span data-ttu-id="f3322-140">Atribui o proprietário da gravação.</span><span class="sxs-lookup"><span data-stu-id="f3322-140">Assigns the write owner.</span></span>

</dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="f3322-141"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**Sincronizar** (1048576 (0x100000))</span><span class="sxs-lookup"><span data-stu-id="f3322-141"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**SYNCHRONIZE** (1048576 (0x100000))</span></span>


</dt> <dd>

<span data-ttu-id="f3322-142">Sincroniza o acesso e permite que um processo Aguarde um objeto para entrar no estado sinalizado.</span><span class="sxs-lookup"><span data-stu-id="f3322-142">Synchronizes access and allows a process to wait for an object to enter the signaled state.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3322-143">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f3322-143">Return value</span></span>

<span data-ttu-id="f3322-144">Retornará **true** se o usuário tiver as permissões especificadas e **false** se o usuário não tiver as permissões especificadas.</span><span class="sxs-lookup"><span data-stu-id="f3322-144">Returns **True** if the user has the specified permissions, and **false** if the user does not have the specified permissions.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3322-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f3322-145">Requirements</span></span>



| <span data-ttu-id="f3322-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3322-146">Requirement</span></span> | <span data-ttu-id="f3322-147">Valor</span><span class="sxs-lookup"><span data-stu-id="f3322-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f3322-148">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f3322-148">Minimum supported client</span></span><br/> | <span data-ttu-id="f3322-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f3322-149">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f3322-150">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f3322-150">Minimum supported server</span></span><br/> | <span data-ttu-id="f3322-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f3322-151">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f3322-152">Namespace</span><span class="sxs-lookup"><span data-stu-id="f3322-152">Namespace</span></span><br/>                | <span data-ttu-id="f3322-153">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="f3322-153">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f3322-154">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f3322-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3322-155"><dt>Aclui. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3322-155"><dt>Aclui.h</dt></span></span> </dl>      |
| <span data-ttu-id="f3322-156">MOF</span><span class="sxs-lookup"><span data-stu-id="f3322-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f3322-157"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f3322-157"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f3322-158">DLL</span><span class="sxs-lookup"><span data-stu-id="f3322-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f3322-159"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f3322-159"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3322-160">Confira também</span><span class="sxs-lookup"><span data-stu-id="f3322-160">See also</span></span>

<dl> <dt>

<span data-ttu-id="f3322-161">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f3322-161">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="f3322-162">**Atalho do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="f3322-162">**Win32\_ShortcutFile**</span></span>](win32-shortcutfile.md)
</dt> </dl>

 

