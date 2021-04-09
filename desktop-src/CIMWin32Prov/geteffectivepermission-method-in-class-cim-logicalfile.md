---
description: Determina se o chamador tem as permissões agregadas no \_ objeto LogicalFile do CIM e o compartilhamento no qual reside o arquivo ou diretório, conforme especificado pelo argumento Permissions.
ms.assetid: 7b6845df-2427-44a8-bd91-9a4ba65caa51
ms.tgt_platform: multiple
title: Método GetEffectivePermission da classe CIM_LogicalFile (aclui. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.GetEffectivePermission
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8cc578436c5d116e202911d2bb68edf7369564a9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089104"
---
# <a name="geteffectivepermission-method-of-the-cim_logicalfile-class"></a><span data-ttu-id="7a84e-103">Método GetEffectivePermission da classe de \_ LogicalFile CIM</span><span class="sxs-lookup"><span data-stu-id="7a84e-103">GetEffectivePermission method of the CIM\_LogicalFile class</span></span>

<span data-ttu-id="7a84e-104">O método **GetEffectivePermission** determina se o chamador tem as permissões agregadas no objeto [**\_ LogicalFile do CIM**](cim-logicalfile.md) e o compartilhamento no qual reside o arquivo ou diretório, conforme especificado pelo argumento *Permissions* .</span><span class="sxs-lookup"><span data-stu-id="7a84e-104">The **GetEffectivePermission** method determines whether the caller has the aggregated permissions on the [**CIM\_LogicalFile**](cim-logicalfile.md) object, and the share on which the file or directory resides, as specified by the *Permissions* argument.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7a84e-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="7a84e-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="7a84e-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="7a84e-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="7a84e-107">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="7a84e-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="7a84e-108">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="7a84e-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="7a84e-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7a84e-109">Syntax</span></span>


```mof
boolean GetEffectivePermission(
  [in] uint32 Permissions
);
```



## <a name="parameters"></a><span data-ttu-id="7a84e-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7a84e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a84e-111">*Permissões* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="7a84e-111">*Permissions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a84e-112">Lista de permissões sobre as quais o usuário pode saber.</span><span class="sxs-lookup"><span data-stu-id="7a84e-112">List of permissions that the user can inquire about.</span></span>

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="7a84e-113"><span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>Do **arquivo \_ LER \_ os dados (arquivo) ou \_ \_ diretório de lista de arquivos (diretório)** (1)</span><span class="sxs-lookup"><span data-stu-id="7a84e-113"><span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>**FILE\_READ\_DATA (file) or FILE\_LIST\_DIRECTORY (directory)** (1)</span></span>


</dt> <dd>

<span data-ttu-id="7a84e-114">Concede o direito de ler dados do arquivo.</span><span class="sxs-lookup"><span data-stu-id="7a84e-114">Grants the right to read data from the file.</span></span> <span data-ttu-id="7a84e-115">Para um diretório, esse valor concede o direito de listar o conteúdo do diretório.</span><span class="sxs-lookup"><span data-stu-id="7a84e-115">For a directory, this value grants the right to list the contents of the directory.</span></span>

</dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="7a84e-116"><span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>Do **arquivo \_ GRAVAR \_ dados (arquivo) ou arquivo \_ Adicionar \_ arquivo (diretório)** (2)</span><span class="sxs-lookup"><span data-stu-id="7a84e-116"><span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>**FILE\_WRITE\_DATA (file) or FILE\_ADD\_FILE (directory)** (2)</span></span>


</dt> <dd>

<span data-ttu-id="7a84e-117">Concede o direito de gravar dados no arquivo.</span><span class="sxs-lookup"><span data-stu-id="7a84e-117">Grants the right to write data to the file.</span></span> <span data-ttu-id="7a84e-118">Para um diretório, esse valor concede o direito de criar um arquivo no diretório.</span><span class="sxs-lookup"><span data-stu-id="7a84e-118">For a directory, this value grants the right to create a file in the directory.</span></span>

</dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="7a84e-119"><span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>Do **arquivo \_ ACRESCENTAR \_ dados (arquivo) ou arquivo \_ Adicionar \_ subdiretório (diretório)** (4)</span><span class="sxs-lookup"><span data-stu-id="7a84e-119"><span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>**FILE\_APPEND\_DATA (file) or FILE\_ADD\_SUBDIRECTORY (directory)** (4)</span></span>


</dt> <dd>

<span data-ttu-id="7a84e-120">Concede o direito de acrescentar dados ao arquivo.</span><span class="sxs-lookup"><span data-stu-id="7a84e-120">Grants the right to append data to the file.</span></span> <span data-ttu-id="7a84e-121">Para um diretório, esse valor concede o direito de criar um subdiretório.</span><span class="sxs-lookup"><span data-stu-id="7a84e-121">For a directory, this value grants the right to create a subdirectory.</span></span>

</dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="7a84e-122"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>Do **arquivo \_ LER \_ ea** (8)</span><span class="sxs-lookup"><span data-stu-id="7a84e-122"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**FILE\_READ\_EA** (8)</span></span>


</dt> <dd>

<span data-ttu-id="7a84e-123">Concede o direito de ler atributos estendidos.</span><span class="sxs-lookup"><span data-stu-id="7a84e-123">Grants the right to read extended attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="7a84e-124"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>Do **arquivo \_ GRAVAR \_ ea** (16)</span><span class="sxs-lookup"><span data-stu-id="7a84e-124"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**FILE\_WRITE\_EA** (16)</span></span>


</dt> <dd>

<span data-ttu-id="7a84e-125">Concede o direito de gravar atributos estendidos.</span><span class="sxs-lookup"><span data-stu-id="7a84e-125">Grants the right to write extended attributes.</span></span>

</dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

<span data-ttu-id="7a84e-126"><span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>Do **arquivo \_ EXECUTAR (arquivo) ou \_ atravessamento de arquivo (diretório)** (32)</span><span class="sxs-lookup"><span data-stu-id="7a84e-126"><span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>**FILE\_EXECUTE (file) or FILE\_TRAVERSE (directory)** (32)</span></span>


</dt> <dd>

<span data-ttu-id="7a84e-127">Concede o direito de executar um arquivo.</span><span class="sxs-lookup"><span data-stu-id="7a84e-127">Grants the right to execute a file.</span></span> <span data-ttu-id="7a84e-128">Para um diretório, o diretório pode ser atravessado.</span><span class="sxs-lookup"><span data-stu-id="7a84e-128">For a directory, the directory can be traversed.</span></span>

</dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="7a84e-129"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>Do **arquivo \_ EXCLUIR \_ filho (diretório)** (64)</span><span class="sxs-lookup"><span data-stu-id="7a84e-129"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**FILE\_DELETE\_CHILD (directory)** (64)</span></span>


</dt> <dd>

<span data-ttu-id="7a84e-130">Concede o direito de excluir um diretório e todos os arquivos que ele contém, mesmo que os arquivos sejam somente leitura.</span><span class="sxs-lookup"><span data-stu-id="7a84e-130">Grants the right to delete a directory and all the files it contains, even if the files are read-only.</span></span>

</dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="7a84e-131"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>Do **arquivo \_ \_Atributos de leitura** (128)</span><span class="sxs-lookup"><span data-stu-id="7a84e-131"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**FILE\_READ\_ATTRIBUTES** (128)</span></span>


</dt> <dd>

<span data-ttu-id="7a84e-132">Concede o direito de ler atributos de arquivo.</span><span class="sxs-lookup"><span data-stu-id="7a84e-132">Grants the right to read file attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="7a84e-133"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>Do **arquivo \_ \_Atributos de gravação** (256)</span><span class="sxs-lookup"><span data-stu-id="7a84e-133"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**FILE\_WRITE\_ATTRIBUTES** (256)</span></span>


</dt> <dd>

<span data-ttu-id="7a84e-134">Concede o direito de alterar atributos de arquivo.</span><span class="sxs-lookup"><span data-stu-id="7a84e-134">Grants the right to change file attributes.</span></span>

</dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="7a84e-135"><span id="DELETE"></span><span id="delete"></span>**Excluir** (65536)</span><span class="sxs-lookup"><span data-stu-id="7a84e-135"><span id="DELETE"></span><span id="delete"></span>**DELETE** (65536)</span></span>


</dt> <dd>

<span data-ttu-id="7a84e-136">Concede acesso de exclusão.</span><span class="sxs-lookup"><span data-stu-id="7a84e-136">Grants delete access.</span></span>

</dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="7a84e-137"><span id="READ_CONTROL"></span><span id="read_control"></span>**Ler \_ CONTROLE** (131072)</span><span class="sxs-lookup"><span data-stu-id="7a84e-137"><span id="READ_CONTROL"></span><span id="read_control"></span>**READ\_CONTROL** (131072)</span></span>


</dt> <dd>

<span data-ttu-id="7a84e-138">Concede acesso de leitura ao descritor de segurança e ao proprietário.</span><span class="sxs-lookup"><span data-stu-id="7a84e-138">Grants read access to the security descriptor and owner.</span></span>

</dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="7a84e-139"><span id="WRITE_DAC"></span><span id="write_dac"></span>**Gravar \_ DAC** (262144)</span><span class="sxs-lookup"><span data-stu-id="7a84e-139"><span id="WRITE_DAC"></span><span id="write_dac"></span>**WRITE\_DAC** (262144)</span></span>


</dt> <dd>

<span data-ttu-id="7a84e-140">Concede acesso de gravação à ACL discricionária.</span><span class="sxs-lookup"><span data-stu-id="7a84e-140">Grants write access to the discretionary ACL.</span></span>

</dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="7a84e-141"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**Gravar \_ PROPRIETÁRIO** (524288)</span><span class="sxs-lookup"><span data-stu-id="7a84e-141"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**WRITE\_OWNER** (524288)</span></span>


</dt> <dd>

<span data-ttu-id="7a84e-142">Atribui o proprietário da gravação.</span><span class="sxs-lookup"><span data-stu-id="7a84e-142">Assigns the write owner.</span></span>

</dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="7a84e-143"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**Sincronizar** (1048576)</span><span class="sxs-lookup"><span data-stu-id="7a84e-143"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**SYNCHRONIZE** (1048576)</span></span>


</dt> <dd>

<span data-ttu-id="7a84e-144">Sincroniza o acesso e permite que um processo Aguarde um objeto para entrar no estado sinalizado.</span><span class="sxs-lookup"><span data-stu-id="7a84e-144">Synchronizes access and allows a process to wait for an object to enter the signaled state.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a84e-145">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7a84e-145">Return value</span></span>

<span data-ttu-id="7a84e-146">Retornará **true** se a chamada tiver a permissão necessária; caso contrário, retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="7a84e-146">Returns **True** if the call has the necessary permission; otherwise, it returns **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a84e-147">Comentários</span><span class="sxs-lookup"><span data-stu-id="7a84e-147">Remarks</span></span>

<span data-ttu-id="7a84e-148">Este método não está implementado no momento pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="7a84e-148">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="7a84e-149">Para usar esse método, você deve implementá-lo em seu próprio provedor.</span><span class="sxs-lookup"><span data-stu-id="7a84e-149">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="7a84e-150">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="7a84e-150">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="7a84e-151">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="7a84e-151">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a84e-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7a84e-152">Requirements</span></span>



| <span data-ttu-id="7a84e-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a84e-153">Requirement</span></span> | <span data-ttu-id="7a84e-154">Valor</span><span class="sxs-lookup"><span data-stu-id="7a84e-154">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7a84e-155">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7a84e-155">Minimum supported client</span></span><br/> | <span data-ttu-id="7a84e-156">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7a84e-156">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7a84e-157">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7a84e-157">Minimum supported server</span></span><br/> | <span data-ttu-id="7a84e-158">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7a84e-158">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7a84e-159">Namespace</span><span class="sxs-lookup"><span data-stu-id="7a84e-159">Namespace</span></span><br/>                | <span data-ttu-id="7a84e-160">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="7a84e-160">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7a84e-161">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7a84e-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a84e-162"><dt>Aclui. h</dt></span><span class="sxs-lookup"><span data-stu-id="7a84e-162"><dt>Aclui.h</dt></span></span> </dl>      |
| <span data-ttu-id="7a84e-163">MOF</span><span class="sxs-lookup"><span data-stu-id="7a84e-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7a84e-164"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7a84e-164"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7a84e-165">DLL</span><span class="sxs-lookup"><span data-stu-id="7a84e-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a84e-166"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a84e-166"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a84e-167">Confira também</span><span class="sxs-lookup"><span data-stu-id="7a84e-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a84e-168">**CIM \_ LogicalFile**</span><span class="sxs-lookup"><span data-stu-id="7a84e-168">**CIM\_LogicalFile**</span></span>](geteffectivepermission-method-in-class-cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="7a84e-169">**CIM \_ LogicalFile**</span><span class="sxs-lookup"><span data-stu-id="7a84e-169">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

