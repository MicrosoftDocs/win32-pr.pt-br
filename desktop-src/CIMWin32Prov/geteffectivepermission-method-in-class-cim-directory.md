---
description: Determina se o chamador tem as permissões agregadas no objeto de \_ diretório CIM e o compartilhamento no qual reside o arquivo ou diretório, conforme especificado pelo argumento de permissão. Esse método é herdado do \_ LogicalFile CIM.
ms.assetid: b3dc1e3c-5c99-46ba-93c4-15fbf18e98e8
ms.tgt_platform: multiple
title: Método GetEffectivePermission da classe CIM_Directory (aclui. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.GetEffectivePermission
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 436a30517b7f3306ef8be2426385fe385947296e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826305"
---
# <a name="geteffectivepermission-method-of-the-cim_directory-class"></a><span data-ttu-id="d5cd2-104">Método GetEffectivePermission da classe de \_ diretório CIM</span><span class="sxs-lookup"><span data-stu-id="d5cd2-104">GetEffectivePermission method of the CIM\_Directory class</span></span>

<span data-ttu-id="d5cd2-105">O método **GetEffectivePermission** determina se o chamador tem as permissões agregadas no objeto [**de \_ diretório CIM**](cim-directory.md) e o compartilhamento no qual reside o arquivo ou diretório, conforme especificado pelo argumento de **permissão** .</span><span class="sxs-lookup"><span data-stu-id="d5cd2-105">The **GetEffectivePermission** method determines whether the caller has the aggregated permissions on the [**CIM\_Directory**](cim-directory.md) object, and the share on which the file or directory resides, as specified by the **Permission** argument.</span></span> <span data-ttu-id="d5cd2-106">Esse método é herdado [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="d5cd2-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d5cd2-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="d5cd2-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="d5cd2-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="d5cd2-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="d5cd2-109">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="d5cd2-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="d5cd2-110">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="d5cd2-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="d5cd2-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d5cd2-111">Syntax</span></span>


```mof
boolean GetEffectivePermission(
  [in] uint32 Permissions
);
```



## <a name="parameters"></a><span data-ttu-id="d5cd2-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d5cd2-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5cd2-113">*Permissões* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="d5cd2-113">*Permissions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5cd2-114">Lista de permissões sobre as quais o usuário pode saber.</span><span class="sxs-lookup"><span data-stu-id="d5cd2-114">List of permissions that the user can inquire about.</span></span>

<dt>

<span id="FILE_READ_DATA__file__FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="d5cd2-115"><span id="FILE_READ_DATA__file__FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__FILE_LIST_DIRECTORY__DIRECTORY_"></span>Do **arquivo \_ LER \_ os dados (arquivo) \_ diretório de lista \_ de arquivos (diretório)** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="d5cd2-115"><span id="FILE_READ_DATA__file__FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__FILE_LIST_DIRECTORY__DIRECTORY_"></span>**FILE\_READ\_DATA (file) FILE\_LIST\_DIRECTORY (directory)** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="d5cd2-116">Concede o direito de ler dados do arquivo.</span><span class="sxs-lookup"><span data-stu-id="d5cd2-116">Grants the right to read data from the file.</span></span> <span data-ttu-id="d5cd2-117">Para um diretório, esse valor concede o direito de listar o conteúdo do diretório.</span><span class="sxs-lookup"><span data-stu-id="d5cd2-117">For a directory, this value grants the right to list the contents of the directory.</span></span>

</dd> <dt>

<span id="FILE_WRITE_DATA__file__FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="d5cd2-118"><span id="FILE_WRITE_DATA__file__FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__FILE_ADD_FILE__DIRECTORY_"></span>Do **arquivo \_ GRAVAR \_ dados (arquivo) arquivo \_ Adicionar \_ arquivo (diretório)** (2 (0x2))</span><span class="sxs-lookup"><span data-stu-id="d5cd2-118"><span id="FILE_WRITE_DATA__file__FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__FILE_ADD_FILE__DIRECTORY_"></span>**FILE\_WRITE\_DATA (file) FILE\_ADD\_FILE (directory)** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="d5cd2-119">Concede o direito de gravar dados no arquivo.</span><span class="sxs-lookup"><span data-stu-id="d5cd2-119">Grants the right to write data to the file.</span></span> <span data-ttu-id="d5cd2-120">Para um diretório, esse valor concede o direito de criar um arquivo no diretório.</span><span class="sxs-lookup"><span data-stu-id="d5cd2-120">For a directory, this value grants the right to create a file in the directory.</span></span>

</dd> <dt>

<span id="FILE_APPEND_DATA__file__FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="d5cd2-121"><span id="FILE_APPEND_DATA__file__FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>Do **arquivo \_ ACRESCENTAR \_ dados (arquivo) arquivo \_ Adicionar \_ subdiretório (diretório)** (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="d5cd2-121"><span id="FILE_APPEND_DATA__file__FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>**FILE\_APPEND\_DATA (file) FILE\_ADD\_SUBDIRECTORY (directory)** (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="d5cd2-122">Concede o direito de acrescentar dados ao arquivo.</span><span class="sxs-lookup"><span data-stu-id="d5cd2-122">Grants the right to append data to the file.</span></span> <span data-ttu-id="d5cd2-123">Para um diretório, esse valor concede o direito de criar um subdiretório.</span><span class="sxs-lookup"><span data-stu-id="d5cd2-123">For a directory, this value grants the right to create a subdirectory.</span></span>

</dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="d5cd2-124"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>Do **arquivo \_ LER \_ ea** (8 (0x8))</span><span class="sxs-lookup"><span data-stu-id="d5cd2-124"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**FILE\_READ\_EA** (8 (0x8))</span></span>


</dt> <dd>

<span data-ttu-id="d5cd2-125">Concede o direito de ler atributos estendidos.</span><span class="sxs-lookup"><span data-stu-id="d5cd2-125">Grants the right to read extended attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="d5cd2-126"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>Do **arquivo \_ GRAVAR \_ ea** (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="d5cd2-126"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**FILE\_WRITE\_EA** (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="d5cd2-127">Concede o direito de gravar atributos estendidos.</span><span class="sxs-lookup"><span data-stu-id="d5cd2-127">Grants the right to write extended attributes.</span></span>

</dd> <dt>

<span id="FILE_EXECUTE__file__FILE_TRAVERSE__directory_"></span><span id="file_execute__file__file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__FILE_TRAVERSE__DIRECTORY_"></span>

<span data-ttu-id="d5cd2-128"><span id="FILE_EXECUTE__file__FILE_TRAVERSE__directory_"></span><span id="file_execute__file__file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__FILE_TRAVERSE__DIRECTORY_"></span>Do **arquivo \_ EXECUTAR (arquivo) \_ atravessamento do arquivo (diretório)** (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="d5cd2-128"><span id="FILE_EXECUTE__file__FILE_TRAVERSE__directory_"></span><span id="file_execute__file__file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__FILE_TRAVERSE__DIRECTORY_"></span>**FILE\_EXECUTE (file) FILE\_TRAVERSE (directory)** (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="d5cd2-129">Concede o direito de executar um arquivo.</span><span class="sxs-lookup"><span data-stu-id="d5cd2-129">Grants the right to execute a file.</span></span> <span data-ttu-id="d5cd2-130">Para um diretório, o diretório pode ser atravessado.</span><span class="sxs-lookup"><span data-stu-id="d5cd2-130">For a directory, the directory can be traversed.</span></span>

</dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="d5cd2-131"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>Do **arquivo \_ EXCLUIR \_ filho (diretório)** (64 (0x40))</span><span class="sxs-lookup"><span data-stu-id="d5cd2-131"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**FILE\_DELETE\_CHILD (directory)** (64 (0x40))</span></span>


</dt> <dd>

<span data-ttu-id="d5cd2-132">Concede o direito de excluir um diretório e todos os arquivos que ele contém, mesmo que os arquivos sejam somente leitura.</span><span class="sxs-lookup"><span data-stu-id="d5cd2-132">Grants the right to delete a directory and all the files it contains, even if the files are read-only.</span></span>

</dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="d5cd2-133"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>Do **arquivo \_ \_Atributos de leitura** (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="d5cd2-133"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**FILE\_READ\_ATTRIBUTES** (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="d5cd2-134">Concede o direito de ler atributos de arquivo.</span><span class="sxs-lookup"><span data-stu-id="d5cd2-134">Grants the right to read file attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="d5cd2-135"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>Do **arquivo \_ \_Atributos de gravação** (256 (0x100))</span><span class="sxs-lookup"><span data-stu-id="d5cd2-135"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**FILE\_WRITE\_ATTRIBUTES** (256 (0x100))</span></span>


</dt> <dd>

<span data-ttu-id="d5cd2-136">Concede o direito de alterar atributos de arquivo.</span><span class="sxs-lookup"><span data-stu-id="d5cd2-136">Grants the right to change file attributes.</span></span>

</dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="d5cd2-137"><span id="DELETE"></span><span id="delete"></span>**Excluir** (65536 (0x10000))</span><span class="sxs-lookup"><span data-stu-id="d5cd2-137"><span id="DELETE"></span><span id="delete"></span>**DELETE** (65536 (0x10000))</span></span>


</dt> <dd>

<span data-ttu-id="d5cd2-138">Concede acesso de exclusão.</span><span class="sxs-lookup"><span data-stu-id="d5cd2-138">Grants delete access.</span></span>

</dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="d5cd2-139"><span id="READ_CONTROL"></span><span id="read_control"></span>**Ler \_ CONTROLE** (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="d5cd2-139"><span id="READ_CONTROL"></span><span id="read_control"></span>**READ\_CONTROL** (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="d5cd2-140">Concede acesso de leitura ao descritor de segurança e ao proprietário.</span><span class="sxs-lookup"><span data-stu-id="d5cd2-140">Grants read access to the security descriptor and owner.</span></span>

</dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="d5cd2-141"><span id="WRITE_DAC"></span><span id="write_dac"></span>**Gravar \_ DAC** (262144 (0x40000))</span><span class="sxs-lookup"><span data-stu-id="d5cd2-141"><span id="WRITE_DAC"></span><span id="write_dac"></span>**WRITE\_DAC** (262144 (0x40000))</span></span>


</dt> <dd>

<span data-ttu-id="d5cd2-142">Concede acesso de gravação à ACL discricionária.</span><span class="sxs-lookup"><span data-stu-id="d5cd2-142">Grants write access to the discretionary ACL.</span></span>

</dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="d5cd2-143"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**Gravar \_ PROPRIETÁRIO** (524288 (0x80000))</span><span class="sxs-lookup"><span data-stu-id="d5cd2-143"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**WRITE\_OWNER** (524288 (0x80000))</span></span>


</dt> <dd>

<span data-ttu-id="d5cd2-144">Atribui o proprietário da gravação.</span><span class="sxs-lookup"><span data-stu-id="d5cd2-144">Assigns the write owner.</span></span>

</dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="d5cd2-145"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**Sincronizar** (1048576 (0x100000))</span><span class="sxs-lookup"><span data-stu-id="d5cd2-145"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**SYNCHRONIZE** (1048576 (0x100000))</span></span>


</dt> <dd>

<span data-ttu-id="d5cd2-146">Sincroniza o acesso e permite que um processo Aguarde um objeto para entrar no estado sinalizado.</span><span class="sxs-lookup"><span data-stu-id="d5cd2-146">Synchronizes access and allows a process to wait for an object to enter the signaled state.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5cd2-147">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d5cd2-147">Return value</span></span>

<span data-ttu-id="d5cd2-148">Retornará **true** se a chamada tiver a permissão necessária; caso contrário, retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="d5cd2-148">Returns **True** if the call has the necessary permission; otherwise, it returns **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5cd2-149">Comentários</span><span class="sxs-lookup"><span data-stu-id="d5cd2-149">Remarks</span></span>

<span data-ttu-id="d5cd2-150">Este método não está implementado no momento pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="d5cd2-150">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="d5cd2-151">Para usar esse método, você deve implementá-lo em seu próprio provedor.</span><span class="sxs-lookup"><span data-stu-id="d5cd2-151">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="d5cd2-152">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="d5cd2-152">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="d5cd2-153">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="d5cd2-153">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5cd2-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5cd2-154">Requirements</span></span>



| <span data-ttu-id="d5cd2-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5cd2-155">Requirement</span></span> | <span data-ttu-id="d5cd2-156">Valor</span><span class="sxs-lookup"><span data-stu-id="d5cd2-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d5cd2-157">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d5cd2-157">Minimum supported client</span></span><br/> | <span data-ttu-id="d5cd2-158">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d5cd2-158">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d5cd2-159">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d5cd2-159">Minimum supported server</span></span><br/> | <span data-ttu-id="d5cd2-160">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d5cd2-160">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d5cd2-161">Namespace</span><span class="sxs-lookup"><span data-stu-id="d5cd2-161">Namespace</span></span><br/>                | <span data-ttu-id="d5cd2-162">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="d5cd2-162">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d5cd2-163">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d5cd2-163">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5cd2-164"><dt>Aclui. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5cd2-164"><dt>Aclui.h</dt></span></span> </dl>      |
| <span data-ttu-id="d5cd2-165">MOF</span><span class="sxs-lookup"><span data-stu-id="d5cd2-165">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d5cd2-166"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d5cd2-166"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d5cd2-167">DLL</span><span class="sxs-lookup"><span data-stu-id="d5cd2-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d5cd2-168"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d5cd2-168"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5cd2-169">Confira também</span><span class="sxs-lookup"><span data-stu-id="d5cd2-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5cd2-170">**\_Diretório CIM**</span><span class="sxs-lookup"><span data-stu-id="d5cd2-170">**CIM\_Directory**</span></span>](geteffectivepermission-method-in-class-cim-directory.md)
</dt> <dt>

[<span data-ttu-id="d5cd2-171">**\_Diretório CIM**</span><span class="sxs-lookup"><span data-stu-id="d5cd2-171">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> </dl>

 

