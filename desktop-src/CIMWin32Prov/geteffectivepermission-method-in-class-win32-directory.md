---
description: Determina se o usuário tem todas as permissões necessárias especificadas no parâmetro Permissions para o objeto do \_ diretório Win32, o diretório e o compartilhamento onde o arquivo de entrada de diretório está localizado (se o arquivo ou diretório estiverem em um compartilhamento).
ms.assetid: ece22cb0-a4ca-4ad7-b6d3-213dda4ce5b1
ms.tgt_platform: multiple
title: Método GetEffectivePermission da classe Win32_Directory (aclui. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.GetEffectivePermission
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 807b7ef95ad03ce2a5b928c2fdc0828dbebe7d9d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646305"
---
# <a name="geteffectivepermission-method-of-the-win32_directory-class"></a><span data-ttu-id="eb6df-103">Método GetEffectivePermission da classe do \_ diretório Win32</span><span class="sxs-lookup"><span data-stu-id="eb6df-103">GetEffectivePermission method of the Win32\_Directory class</span></span>

<span data-ttu-id="eb6df-104">O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) [**GetEffectivePermission**](geteffectivepermission-method-in-class-win32-shortcutfile.md) determina se o usuário tem todas as permissões necessárias especificadas no parâmetro *Permissions* para o objeto de [**\_ diretório do Win32**](win32-directory.md) , diretório e compartilhamento onde o arquivo de entrada de diretório está localizado (se o arquivo ou diretório estiverem em um compartilhamento).</span><span class="sxs-lookup"><span data-stu-id="eb6df-104">The [**GetEffectivePermission**](geteffectivepermission-method-in-class-win32-shortcutfile.md) [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method determines whether the user has all of the required permissions specified in the *Permissions* parameter for the [**Win32\_Directory**](win32-directory.md) object, directory, and share where the directory entry file is located (if the file or directory are on a share).</span></span>

<span data-ttu-id="eb6df-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="eb6df-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="eb6df-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="eb6df-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="eb6df-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eb6df-107">Syntax</span></span>


```mof
boolean GetEffectivePermission(
  [in] uint32 Permissions
);
```



## <a name="parameters"></a><span data-ttu-id="eb6df-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eb6df-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb6df-109">*Permissões* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="eb6df-109">*Permissions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb6df-110">Bitmap de permissões que o chamador pode consultar.</span><span class="sxs-lookup"><span data-stu-id="eb6df-110">Bitmap of permissions that the caller can inquire about.</span></span>

<dt>

<span id="FILE_READ_DATA__file__FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="eb6df-111"><span id="FILE_READ_DATA__file__FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__FILE_LIST_DIRECTORY__DIRECTORY_"></span>Do **arquivo \_ LER \_ os dados (arquivo) \_ diretório de lista \_ de arquivos (diretório)** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="eb6df-111"><span id="FILE_READ_DATA__file__FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__FILE_LIST_DIRECTORY__DIRECTORY_"></span>**FILE\_READ\_DATA (file) FILE\_LIST\_DIRECTORY (directory)** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="eb6df-112">Concede o direito de ler dados do arquivo.</span><span class="sxs-lookup"><span data-stu-id="eb6df-112">Grants the right to read data from the file.</span></span> <span data-ttu-id="eb6df-113">Para um diretório, esse valor concede o direito de listar o conteúdo do diretório.</span><span class="sxs-lookup"><span data-stu-id="eb6df-113">For a directory, this value grants the right to list the contents of the directory.</span></span>

</dd> <dt>

<span id="FILE_WRITE_DATA__file__FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="eb6df-114"><span id="FILE_WRITE_DATA__file__FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__FILE_ADD_FILE__DIRECTORY_"></span>Do **arquivo \_ GRAVAR \_ dados (arquivo) arquivo \_ Adicionar \_ arquivo (diretório)** (2 (0x2))</span><span class="sxs-lookup"><span data-stu-id="eb6df-114"><span id="FILE_WRITE_DATA__file__FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__FILE_ADD_FILE__DIRECTORY_"></span>**FILE\_WRITE\_DATA (file) FILE\_ADD\_FILE (directory)** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="eb6df-115">Concede o direito de gravar dados no arquivo.</span><span class="sxs-lookup"><span data-stu-id="eb6df-115">Grants the right to write data to the file.</span></span> <span data-ttu-id="eb6df-116">Para um diretório, esse valor concede o direito de criar um arquivo no diretório.</span><span class="sxs-lookup"><span data-stu-id="eb6df-116">For a directory, this value grants the right to create a file in the directory.</span></span>

</dd> <dt>

<span id="FILE_APPEND_DATA__file__FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="eb6df-117"><span id="FILE_APPEND_DATA__file__FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>Do **arquivo \_ ACRESCENTAR \_ dados (arquivo) arquivo \_ Adicionar \_ subdiretório (diretório)** (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="eb6df-117"><span id="FILE_APPEND_DATA__file__FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>**FILE\_APPEND\_DATA (file) FILE\_ADD\_SUBDIRECTORY (directory)** (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="eb6df-118">Concede o direito de acrescentar dados ao arquivo.</span><span class="sxs-lookup"><span data-stu-id="eb6df-118">Grants the right to append data to the file.</span></span> <span data-ttu-id="eb6df-119">Para um diretório, esse valor concede o direito de criar um subdiretório.</span><span class="sxs-lookup"><span data-stu-id="eb6df-119">For a directory, this value grants the right to create a subdirectory.</span></span>

</dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="eb6df-120"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>Do **arquivo \_ LER \_ ea** (8 (0x8))</span><span class="sxs-lookup"><span data-stu-id="eb6df-120"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**FILE\_READ\_EA** (8 (0x8))</span></span>


</dt> <dd>

<span data-ttu-id="eb6df-121">Concede o direito de ler atributos estendidos.</span><span class="sxs-lookup"><span data-stu-id="eb6df-121">Grants the right to read extended attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="eb6df-122"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>Do **arquivo \_ GRAVAR \_ ea** (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="eb6df-122"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**FILE\_WRITE\_EA** (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="eb6df-123">Concede o direito de gravar atributos estendidos.</span><span class="sxs-lookup"><span data-stu-id="eb6df-123">Grants the right to write extended attributes.</span></span>

</dd> <dt>

<span id="FILE_EXECUTE__file_______FILE_TRAVERSE__directory_"></span><span id="file_execute__file_______file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE_______FILE_TRAVERSE__DIRECTORY_"></span>

<span data-ttu-id="eb6df-124"><span id="FILE_EXECUTE__file_______FILE_TRAVERSE__directory_"></span><span id="file_execute__file_______file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE_______FILE_TRAVERSE__DIRECTORY_"></span>Do **arquivo \_ EXECUTAR (arquivo) \_ atravessamento do arquivo (diretório)** (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="eb6df-124"><span id="FILE_EXECUTE__file_______FILE_TRAVERSE__directory_"></span><span id="file_execute__file_______file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE_______FILE_TRAVERSE__DIRECTORY_"></span>**FILE\_EXECUTE (file) FILE\_TRAVERSE (directory)** (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="eb6df-125">Concede o direito de executar um arquivo.</span><span class="sxs-lookup"><span data-stu-id="eb6df-125">Grants the right to execute a file.</span></span> <span data-ttu-id="eb6df-126">Para um diretório, o diretório pode ser atravessado.</span><span class="sxs-lookup"><span data-stu-id="eb6df-126">For a directory, the directory can be traversed.</span></span>

</dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="eb6df-127"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>Do **arquivo \_ EXCLUIR \_ filho (diretório)** (64 (0x40))</span><span class="sxs-lookup"><span data-stu-id="eb6df-127"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**FILE\_DELETE\_CHILD (directory)** (64 (0x40))</span></span>


</dt> <dd>

<span data-ttu-id="eb6df-128">Concede o direito de excluir um diretório e todos os arquivos que ele contém, mesmo que os arquivos sejam somente leitura.</span><span class="sxs-lookup"><span data-stu-id="eb6df-128">Grants the right to delete a directory and all of the files it contains, even if the files are read-only.</span></span>

</dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="eb6df-129"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>Do **arquivo \_ \_Atributos de leitura** (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="eb6df-129"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**FILE\_READ\_ATTRIBUTES** (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="eb6df-130">Concede o direito de ler atributos de arquivo.</span><span class="sxs-lookup"><span data-stu-id="eb6df-130">Grants the right to read file attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="eb6df-131"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>Do **arquivo \_ \_Atributos de gravação** (256 (0x100))</span><span class="sxs-lookup"><span data-stu-id="eb6df-131"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**FILE\_WRITE\_ATTRIBUTES** (256 (0x100))</span></span>


</dt> <dd>

<span data-ttu-id="eb6df-132">Concede o direito de alterar atributos de arquivo.</span><span class="sxs-lookup"><span data-stu-id="eb6df-132">Grants the right to change file attributes.</span></span>

</dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="eb6df-133"><span id="DELETE"></span><span id="delete"></span>**Excluir** (65536 (0x10000))</span><span class="sxs-lookup"><span data-stu-id="eb6df-133"><span id="DELETE"></span><span id="delete"></span>**DELETE** (65536 (0x10000))</span></span>


</dt> <dd>

<span data-ttu-id="eb6df-134">Concede acesso de exclusão.</span><span class="sxs-lookup"><span data-stu-id="eb6df-134">Grants delete access.</span></span>

</dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="eb6df-135"><span id="READ_CONTROL"></span><span id="read_control"></span>**Ler \_ CONTROLE** (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="eb6df-135"><span id="READ_CONTROL"></span><span id="read_control"></span>**READ\_CONTROL** (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="eb6df-136">Concede acesso de leitura ao descritor de segurança e ao proprietário.</span><span class="sxs-lookup"><span data-stu-id="eb6df-136">Grants read access to the security descriptor and owner.</span></span>

</dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="eb6df-137"><span id="WRITE_DAC"></span><span id="write_dac"></span>**Gravar \_ DAC** (262144 (0x40000))</span><span class="sxs-lookup"><span data-stu-id="eb6df-137"><span id="WRITE_DAC"></span><span id="write_dac"></span>**WRITE\_DAC** (262144 (0x40000))</span></span>


</dt> <dd>

<span data-ttu-id="eb6df-138">Concede acesso de gravação à lista de controle de acesso discricional (ACL).</span><span class="sxs-lookup"><span data-stu-id="eb6df-138">Grants write access to the discretionary access control list (ACL).</span></span>

</dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="eb6df-139"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**Gravar \_ PROPRIETÁRIO** (524288 (0x80000))</span><span class="sxs-lookup"><span data-stu-id="eb6df-139"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**WRITE\_OWNER** (524288 (0x80000))</span></span>


</dt> <dd>

<span data-ttu-id="eb6df-140">Atribui o proprietário da gravação.</span><span class="sxs-lookup"><span data-stu-id="eb6df-140">Assigns the write owner.</span></span>

</dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="eb6df-141"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**Sincronizar** (1048576 (0x100000))</span><span class="sxs-lookup"><span data-stu-id="eb6df-141"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**SYNCHRONIZE** (1048576 (0x100000))</span></span>


</dt> <dd>

<span data-ttu-id="eb6df-142">Sincroniza o acesso e permite que um processo Aguarde um objeto para entrar no estado sinalizado.</span><span class="sxs-lookup"><span data-stu-id="eb6df-142">Synchronizes access and allows a process to wait for an object to enter the signaled state.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb6df-143">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="eb6df-143">Return value</span></span>

<span data-ttu-id="eb6df-144">Retorna **true** quando o chamador tem as permissões especificadas e **false** quando o chamador não tem as permissões especificadas.</span><span class="sxs-lookup"><span data-stu-id="eb6df-144">Returns **True** when the caller has the specified permissions, and **false** when the caller does not have the specified permissions.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb6df-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eb6df-145">Requirements</span></span>



| <span data-ttu-id="eb6df-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb6df-146">Requirement</span></span> | <span data-ttu-id="eb6df-147">Valor</span><span class="sxs-lookup"><span data-stu-id="eb6df-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eb6df-148">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eb6df-148">Minimum supported client</span></span><br/> | <span data-ttu-id="eb6df-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="eb6df-149">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="eb6df-150">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eb6df-150">Minimum supported server</span></span><br/> | <span data-ttu-id="eb6df-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eb6df-151">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="eb6df-152">Namespace</span><span class="sxs-lookup"><span data-stu-id="eb6df-152">Namespace</span></span><br/>                | <span data-ttu-id="eb6df-153">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="eb6df-153">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="eb6df-154">parâmetro</span><span class="sxs-lookup"><span data-stu-id="eb6df-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="eb6df-155"><dt>Aclui. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb6df-155"><dt>Aclui.h</dt></span></span> </dl>      |
| <span data-ttu-id="eb6df-156">MOF</span><span class="sxs-lookup"><span data-stu-id="eb6df-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eb6df-157"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="eb6df-157"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="eb6df-158">DLL</span><span class="sxs-lookup"><span data-stu-id="eb6df-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eb6df-159"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb6df-159"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb6df-160">Confira também</span><span class="sxs-lookup"><span data-stu-id="eb6df-160">See also</span></span>

<dl> <dt>

<span data-ttu-id="eb6df-161">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="eb6df-161">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="eb6df-162">**\_Diretório Win32**</span><span class="sxs-lookup"><span data-stu-id="eb6df-162">**Win32\_Directory**</span></span>](win32-directory.md)
</dt> </dl>

 

