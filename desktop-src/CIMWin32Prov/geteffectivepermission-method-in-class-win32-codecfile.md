---
description: Usa os valores definidos no parâmetro Permissions para determinar se o usuário tem as permissões especificadas definidas na propriedade AccessMask do objeto de codec do Win32 \_ que representa o arquivo de codec.
ms.assetid: 068dfcaf-037b-4516-b85a-8ba6558ba561
ms.tgt_platform: multiple
title: Método GetEffectivePermission da classe Win32_CodecFile (aclui. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile.GetEffectivePermission
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: cc2f24071d5ab864e06686f094707d9111ea07ab
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826304"
---
# <a name="geteffectivepermission-method-of-the-win32_codecfile-class"></a><span data-ttu-id="916aa-103">Método GetEffectivePermission da classe de um codec do Win32 \_</span><span class="sxs-lookup"><span data-stu-id="916aa-103">GetEffectivePermission method of the Win32\_CodecFile class</span></span>

<span data-ttu-id="916aa-104">O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) [**GetEffectivePermission**](geteffectivepermission-method-in-class-win32-shortcutfile.md) usa os valores definidos no *parâmetro Permissions* para determinar se o usuário tem as permissões especificadas definidas na propriedade **AccessMask** do objeto [**de \_ codec do Win32**](win32-codecfile.md) que representa o arquivo de codec.</span><span class="sxs-lookup"><span data-stu-id="916aa-104">The [**GetEffectivePermission**](geteffectivepermission-method-in-class-win32-shortcutfile.md) [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method uses the values set in the *Permissions* parameter to determine whether the user has the specified permissions set in the **AccessMask** property of the [**Win32\_CodecFile**](win32-codecfile.md) object that represents the codec file.</span></span> <span data-ttu-id="916aa-105">As permissões se aplicam ao arquivo, o diretório no qual o arquivo reside e o compartilhamento, se o diretório ou o arquivo estiverem em um compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="916aa-105">The permissions apply to the file, the directory in which the file resides, and the share, if either the directory or the file are in a share.</span></span>

<span data-ttu-id="916aa-106">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="916aa-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="916aa-107">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="916aa-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="916aa-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="916aa-108">Syntax</span></span>


```mof
boolean GetEffectivePermission(
  [in] uint32 Permissions
);
```



## <a name="parameters"></a><span data-ttu-id="916aa-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="916aa-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="916aa-110">*Permissões* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="916aa-110">*Permissions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="916aa-111">Bitmap de permissões que são definidas na propriedade **AccessMask** do objeto [**\_ codec do Win32**](win32-codecfile.md) .</span><span class="sxs-lookup"><span data-stu-id="916aa-111">Bitmap of permissions that are set in the **AccessMask** property of the [**Win32\_CodecFile**](win32-codecfile.md) object.</span></span>

<dt>

<span id="FILE_READ_DATA__file__FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="916aa-112"><span id="FILE_READ_DATA__file__FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__FILE_LIST_DIRECTORY__DIRECTORY_"></span>Do **arquivo \_ LER \_ os dados (arquivo) \_ diretório de lista \_ de arquivos (diretório)** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="916aa-112"><span id="FILE_READ_DATA__file__FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__FILE_LIST_DIRECTORY__DIRECTORY_"></span>**FILE\_READ\_DATA (file) FILE\_LIST\_DIRECTORY (directory)** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="916aa-113">Concede o direito de ler dados do arquivo.</span><span class="sxs-lookup"><span data-stu-id="916aa-113">Grants the right to read data from the file.</span></span> <span data-ttu-id="916aa-114">Para um diretório, esse valor concede o direito de listar o conteúdo do diretório.</span><span class="sxs-lookup"><span data-stu-id="916aa-114">For a directory, this value grants the right to list the contents of the directory.</span></span>

</dd> <dt>

<span id="FILE_WRITE_DATA__file__FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="916aa-115"><span id="FILE_WRITE_DATA__file__FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__FILE_ADD_FILE__DIRECTORY_"></span>Do **arquivo \_ GRAVAR \_ dados (arquivo) arquivo \_ Adicionar \_ arquivo (diretório)** (2 (0x2))</span><span class="sxs-lookup"><span data-stu-id="916aa-115"><span id="FILE_WRITE_DATA__file__FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__FILE_ADD_FILE__DIRECTORY_"></span>**FILE\_WRITE\_DATA (file) FILE\_ADD\_FILE (directory)** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="916aa-116">Concede o direito de gravar dados no arquivo.</span><span class="sxs-lookup"><span data-stu-id="916aa-116">Grants the right to write data to the file.</span></span> <span data-ttu-id="916aa-117">Para um diretório, esse valor concede o direito de criar um arquivo no diretório.</span><span class="sxs-lookup"><span data-stu-id="916aa-117">For a directory, this value grants the right to create a file in the directory.</span></span>

</dd> <dt>

<span id="FILE_APPEND_DATA__file__FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="916aa-118"><span id="FILE_APPEND_DATA__file__FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>Do **arquivo \_ ACRESCENTAR \_ dados (arquivo) arquivo \_ Adicionar \_ subdiretório (diretório)** (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="916aa-118"><span id="FILE_APPEND_DATA__file__FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>**FILE\_APPEND\_DATA (file) FILE\_ADD\_SUBDIRECTORY (directory)** (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="916aa-119">Concede o direito de acrescentar dados ao arquivo.</span><span class="sxs-lookup"><span data-stu-id="916aa-119">Grants the right to append data to the file.</span></span> <span data-ttu-id="916aa-120">Para um diretório, esse valor concede o direito de criar um subdiretório.</span><span class="sxs-lookup"><span data-stu-id="916aa-120">For a directory, this value grants the right to create a subdirectory.</span></span>

</dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="916aa-121"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>Do **arquivo \_ LER \_ ea** (8 (0x8))</span><span class="sxs-lookup"><span data-stu-id="916aa-121"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**FILE\_READ\_EA** (8 (0x8))</span></span>


</dt> <dd>

<span data-ttu-id="916aa-122">Concede o direito de ler atributos estendidos.</span><span class="sxs-lookup"><span data-stu-id="916aa-122">Grants the right to read extended attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="916aa-123"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>Do **arquivo \_ GRAVAR \_ ea** (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="916aa-123"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**FILE\_WRITE\_EA** (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="916aa-124">Concede o direito de gravar atributos estendidos.</span><span class="sxs-lookup"><span data-stu-id="916aa-124">Grants the right to write extended attributes.</span></span>

</dd> <dt>

<span id="FILE_EXECUTE__file__FILE_TRAVERSE__directory_"></span><span id="file_execute__file__file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__FILE_TRAVERSE__DIRECTORY_"></span>

<span data-ttu-id="916aa-125"><span id="FILE_EXECUTE__file__FILE_TRAVERSE__directory_"></span><span id="file_execute__file__file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__FILE_TRAVERSE__DIRECTORY_"></span>Do **arquivo \_ EXECUTAR (arquivo) \_ atravessamento do arquivo (diretório)** (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="916aa-125"><span id="FILE_EXECUTE__file__FILE_TRAVERSE__directory_"></span><span id="file_execute__file__file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__FILE_TRAVERSE__DIRECTORY_"></span>**FILE\_EXECUTE (file) FILE\_TRAVERSE (directory)** (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="916aa-126">Concede o direito de executar um arquivo.</span><span class="sxs-lookup"><span data-stu-id="916aa-126">Grants the right to execute a file.</span></span> <span data-ttu-id="916aa-127">Para um diretório, o diretório pode ser atravessado.</span><span class="sxs-lookup"><span data-stu-id="916aa-127">For a directory, the directory can be traversed.</span></span>

</dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="916aa-128"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>Do **arquivo \_ EXCLUIR \_ filho (diretório)** (64 (0x40))</span><span class="sxs-lookup"><span data-stu-id="916aa-128"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**FILE\_DELETE\_CHILD (directory)** (64 (0x40))</span></span>


</dt> <dd>

<span data-ttu-id="916aa-129">Concede o direito de excluir um diretório e todos os arquivos que ele contém, mesmo que os arquivos sejam somente leitura.</span><span class="sxs-lookup"><span data-stu-id="916aa-129">Grants the right to delete a directory and all of the files it contains, even if the files are read-only.</span></span>

</dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="916aa-130"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>Do **arquivo \_ \_Atributos de leitura** (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="916aa-130"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**FILE\_READ\_ATTRIBUTES** (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="916aa-131">Concede o direito de ler atributos de arquivo.</span><span class="sxs-lookup"><span data-stu-id="916aa-131">Grants the right to read file attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="916aa-132"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>Do **arquivo \_ \_Atributos de gravação** (256 (0x100))</span><span class="sxs-lookup"><span data-stu-id="916aa-132"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**FILE\_WRITE\_ATTRIBUTES** (256 (0x100))</span></span>


</dt> <dd>

<span data-ttu-id="916aa-133">Concede o direito de alterar atributos de arquivo.</span><span class="sxs-lookup"><span data-stu-id="916aa-133">Grants the right to change file attributes.</span></span>

</dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="916aa-134"><span id="DELETE"></span><span id="delete"></span>**Excluir** (65536 (0x10000))</span><span class="sxs-lookup"><span data-stu-id="916aa-134"><span id="DELETE"></span><span id="delete"></span>**DELETE** (65536 (0x10000))</span></span>


</dt> <dd>

<span data-ttu-id="916aa-135">Concede acesso de exclusão.</span><span class="sxs-lookup"><span data-stu-id="916aa-135">Grants delete access.</span></span>

</dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="916aa-136"><span id="READ_CONTROL"></span><span id="read_control"></span>**Ler \_ CONTROLE** (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="916aa-136"><span id="READ_CONTROL"></span><span id="read_control"></span>**READ\_CONTROL** (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="916aa-137">Concede acesso de leitura ao descritor de segurança e ao proprietário.</span><span class="sxs-lookup"><span data-stu-id="916aa-137">Grants read access to the security descriptor and owner.</span></span>

</dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="916aa-138"><span id="WRITE_DAC"></span><span id="write_dac"></span>**Gravar \_ DAC** (262144 (0x40000))</span><span class="sxs-lookup"><span data-stu-id="916aa-138"><span id="WRITE_DAC"></span><span id="write_dac"></span>**WRITE\_DAC** (262144 (0x40000))</span></span>


</dt> <dd>

<span data-ttu-id="916aa-139">Concede acesso de gravação à lista de controle de acesso discricional (ACL).</span><span class="sxs-lookup"><span data-stu-id="916aa-139">Grants write access to the discretionary access control list (ACL).</span></span>

</dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="916aa-140"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**Gravar \_ PROPRIETÁRIO** (524288 (0x80000))</span><span class="sxs-lookup"><span data-stu-id="916aa-140"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**WRITE\_OWNER** (524288 (0x80000))</span></span>


</dt> <dd>

<span data-ttu-id="916aa-141">Atribui o proprietário da gravação.</span><span class="sxs-lookup"><span data-stu-id="916aa-141">Assigns the write owner.</span></span>

</dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="916aa-142"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**Sincronizar** (1048576 (0x100000))</span><span class="sxs-lookup"><span data-stu-id="916aa-142"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**SYNCHRONIZE** (1048576 (0x100000))</span></span>


</dt> <dd>

<span data-ttu-id="916aa-143">Sincroniza o acesso e permite que um processo Aguarde um objeto para entrar no estado sinalizado.</span><span class="sxs-lookup"><span data-stu-id="916aa-143">Synchronizes access and allows a process to wait for an object to enter the signaled state.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="916aa-144">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="916aa-144">Return value</span></span>

<span data-ttu-id="916aa-145">Retorna **true** quando o chamador tem as permissões especificadas e **false** quando o chamador não tem as permissões especificadas.</span><span class="sxs-lookup"><span data-stu-id="916aa-145">Returns **True** when the caller has the specified permissions, and **false** when the caller does not have the specified permissions.</span></span>

## <a name="requirements"></a><span data-ttu-id="916aa-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="916aa-146">Requirements</span></span>



| <span data-ttu-id="916aa-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="916aa-147">Requirement</span></span> | <span data-ttu-id="916aa-148">Valor</span><span class="sxs-lookup"><span data-stu-id="916aa-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="916aa-149">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="916aa-149">Minimum supported client</span></span><br/> | <span data-ttu-id="916aa-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="916aa-150">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="916aa-151">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="916aa-151">Minimum supported server</span></span><br/> | <span data-ttu-id="916aa-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="916aa-152">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="916aa-153">Namespace</span><span class="sxs-lookup"><span data-stu-id="916aa-153">Namespace</span></span><br/>                | <span data-ttu-id="916aa-154">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="916aa-154">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="916aa-155">parâmetro</span><span class="sxs-lookup"><span data-stu-id="916aa-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="916aa-156"><dt>Aclui. h</dt></span><span class="sxs-lookup"><span data-stu-id="916aa-156"><dt>Aclui.h</dt></span></span> </dl>      |
| <span data-ttu-id="916aa-157">MOF</span><span class="sxs-lookup"><span data-stu-id="916aa-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="916aa-158"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="916aa-158"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="916aa-159">DLL</span><span class="sxs-lookup"><span data-stu-id="916aa-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="916aa-160"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="916aa-160"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="916aa-161">Confira também</span><span class="sxs-lookup"><span data-stu-id="916aa-161">See also</span></span>

<dl> <dt>

<span data-ttu-id="916aa-162">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="916aa-162">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="916aa-163">**Codec do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="916aa-163">**Win32\_CodecFile**</span></span>](win32-codecfile.md)
</dt> </dl>

 

