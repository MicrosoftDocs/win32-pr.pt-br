---
description: As classes WMI que representam arquivos ou diretórios, como o arquivo de codec do Win32 filefile \_ ou CIM \_ , contêm uma propriedade AccessMask.
ms.assetid: 9020b337-d44f-4247-b623-68a1bcf35abb
ms.tgt_platform: multiple
title: Constantes de direitos de acesso de arquivo e diretório (WinNT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c0ddca31034ffde79fa9d9ff902a364cf07e311
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105773029"
---
# <a name="file-and-directory-access-rights-constants"></a><span data-ttu-id="4fc8f-103">Constantes de direitos de acesso de arquivo e diretório</span><span class="sxs-lookup"><span data-stu-id="4fc8f-103">File and Directory Access Rights Constants</span></span>

<span data-ttu-id="4fc8f-104">As classes WMI que representam arquivos ou diretórios, como o [**\_ arquivo**](/windows/desktop/CIMWin32Prov/cim-datafile)de [**\_ codec do Win32**](/windows/desktop/CIMWin32Prov/win32-codecfile) filefile ou CIM, contêm uma propriedade **AccessMask** .</span><span class="sxs-lookup"><span data-stu-id="4fc8f-104">WMI classes that represent files or directories, such as [**Win32\_CodecFile**](/windows/desktop/CIMWin32Prov/win32-codecfile) or [**CIM\_DataFile**](/windows/desktop/CIMWin32Prov/cim-datafile), contain an **AccessMask** property.</span></span> <span data-ttu-id="4fc8f-105">Essa propriedade contém configurações de bit que especificam os direitos de acesso que um usuário ou grupo deve ter para acessar ou operações específicas no arquivo.</span><span class="sxs-lookup"><span data-stu-id="4fc8f-105">This property contains bit settings that specify the access rights a user or group must have for specific access or operations on the file.</span></span> <span data-ttu-id="4fc8f-106">Para obter mais informações, consulte [segurança de arquivos e direitos de acesso](/windows/desktop/FileIO/file-security-and-access-rights) e [alterando a segurança de acesso em objetos protegíveis](changing-access-security-on-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="4fc8f-106">For more information, see [File Security and Access Rights](/windows/desktop/FileIO/file-security-and-access-rights) and [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span>

<span data-ttu-id="4fc8f-107">As classes de arquivo ou diretório que contêm uma propriedade **AccessMask** incluem:</span><span class="sxs-lookup"><span data-stu-id="4fc8f-107">The file or directory classes which contain an **AccessMask** property include:</span></span>

-   [<span data-ttu-id="4fc8f-108">**DataFile de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="4fc8f-108">**CIM\_DataFile**</span></span>](/windows/desktop/CIMWin32Prov/cim-datafile)
-   [<span data-ttu-id="4fc8f-109">**\_Diretório CIM**</span><span class="sxs-lookup"><span data-stu-id="4fc8f-109">**CIM\_Directory**</span></span>](/windows/desktop/CIMWin32Prov/cim-directory)
-   [<span data-ttu-id="4fc8f-110">**CIM \_ LogicalFile**</span><span class="sxs-lookup"><span data-stu-id="4fc8f-110">**CIM\_LogicalFile**</span></span>](/windows/desktop/CIMWin32Prov/cim-logicalfile)
-   [<span data-ttu-id="4fc8f-111">**Codec do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="4fc8f-111">**Win32\_CodecFile**</span></span>](/windows/desktop/CIMWin32Prov/win32-codecfile)
-   [<span data-ttu-id="4fc8f-112">**\_Diretório Win32**</span><span class="sxs-lookup"><span data-stu-id="4fc8f-112">**Win32\_Directory**</span></span>](/windows/desktop/CIMWin32Prov/win32-directory)
-   <span data-ttu-id="4fc8f-113">[**\_NTEventLogFile Win32**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4fc8f-113">[**Win32\_NTEventLogFile**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85))</span></span>
-   [<span data-ttu-id="4fc8f-114">**Compartilhamento do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="4fc8f-114">**Win32\_Share**</span></span>](/windows/desktop/CIMWin32Prov/win32-share)
-   [<span data-ttu-id="4fc8f-115">**Atalho do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="4fc8f-115">**Win32\_ShortcutFile**</span></span>](/windows/desktop/CIMWin32Prov/win32-shortcutfile)

<span data-ttu-id="4fc8f-116">A lista a seguir lista os valores para direitos de acesso de arquivo e diretório na propriedade **AccessMask** .</span><span class="sxs-lookup"><span data-stu-id="4fc8f-116">The following list lists the values for file and directory access rights in the **AccessMask** property.</span></span> <span data-ttu-id="4fc8f-117">Esta propriedade é um bitmap.</span><span class="sxs-lookup"><span data-stu-id="4fc8f-117">This property is a bitmap.</span></span>

<dl> <dt>

<span data-ttu-id="4fc8f-118"><span id="FILE_READ_DATA"></span><span id="file_read_data"></span>**\_dados de leitura de arquivo \_**</span><span class="sxs-lookup"><span data-stu-id="4fc8f-118"><span id="FILE_READ_DATA"></span><span id="file_read_data"></span>**FILE\_READ\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fc8f-119">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="4fc8f-119">1 (0x1)</span></span>
</dt> <dt>



<span data-ttu-id="4fc8f-120">Concede o direito de ler dados do arquivo.</span><span class="sxs-lookup"><span data-stu-id="4fc8f-120">Grants the right to read data from the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fc8f-121"><span id="FILE_LIST_DIRECTORY"></span><span id="file_list_directory"></span>**\_diretório de lista de arquivos \_**</span><span class="sxs-lookup"><span data-stu-id="4fc8f-121"><span id="FILE_LIST_DIRECTORY"></span><span id="file_list_directory"></span>**FILE\_LIST\_DIRECTORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fc8f-122">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="4fc8f-122">1 (0x1)</span></span>
</dt> <dt>



<span data-ttu-id="4fc8f-123">Concede o direito de ler dados do arquivo.</span><span class="sxs-lookup"><span data-stu-id="4fc8f-123">Grants the right to read data from the file.</span></span> <span data-ttu-id="4fc8f-124">Para um diretório, esse valor concede o direito de listar o conteúdo do diretório.</span><span class="sxs-lookup"><span data-stu-id="4fc8f-124">For a directory, this value grants the right to list the contents of the directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fc8f-125"><span id="FILE_WRITE_DATA"></span><span id="file_write_data"></span>**\_dados de gravação de arquivo \_**</span><span class="sxs-lookup"><span data-stu-id="4fc8f-125"><span id="FILE_WRITE_DATA"></span><span id="file_write_data"></span>**FILE\_WRITE\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fc8f-126">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="4fc8f-126">2 (0x2)</span></span>
</dt> <dt>



<span data-ttu-id="4fc8f-127">Concede o direito de gravar dados no arquivo.</span><span class="sxs-lookup"><span data-stu-id="4fc8f-127">Grants the right to write data to the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fc8f-128"><span id="FILE_ADD_FILE"></span><span id="file_add_file"></span>**ARQUIVO- \_ Adicionar \_ arquivo**</span><span class="sxs-lookup"><span data-stu-id="4fc8f-128"><span id="FILE_ADD_FILE"></span><span id="file_add_file"></span>**FILE\_ADD\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fc8f-129">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="4fc8f-129">2 (0x2)</span></span>
</dt> <dt>



<span data-ttu-id="4fc8f-130">Concede o direito de gravar dados no arquivo.</span><span class="sxs-lookup"><span data-stu-id="4fc8f-130">Grants the right to write data to the file.</span></span> <span data-ttu-id="4fc8f-131">Para um diretório, esse valor concede o direito de criar um arquivo no diretório.</span><span class="sxs-lookup"><span data-stu-id="4fc8f-131">For a directory, this value grants the right to create a file in the directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fc8f-132"><span id="FILE_APPEND_DATA"></span><span id="file_append_data"></span>**\_dados de acréscimo de arquivo \_**</span><span class="sxs-lookup"><span data-stu-id="4fc8f-132"><span id="FILE_APPEND_DATA"></span><span id="file_append_data"></span>**FILE\_APPEND\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fc8f-133">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="4fc8f-133">4 (0x4)</span></span>
</dt> <dt>



<span data-ttu-id="4fc8f-134">Concede o direito de acrescentar dados ao arquivo.</span><span class="sxs-lookup"><span data-stu-id="4fc8f-134">Grants the right to append data to the file.</span></span> <span data-ttu-id="4fc8f-135">Para um diretório, esse valor concede o direito de criar um subdiretório.</span><span class="sxs-lookup"><span data-stu-id="4fc8f-135">For a directory, this value grants the right to create a subdirectory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fc8f-136"><span id="FILE_ADD_SUBDIRECTORY"></span><span id="file_add_subdirectory"></span>**ARQUIVO \_ Adicionar \_ subdiretório**</span><span class="sxs-lookup"><span data-stu-id="4fc8f-136"><span id="FILE_ADD_SUBDIRECTORY"></span><span id="file_add_subdirectory"></span>**FILE\_ADD\_SUBDIRECTORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fc8f-137">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="4fc8f-137">4 (0x4)</span></span>
</dt> <dt>



<span data-ttu-id="4fc8f-138">Concede o direito de acrescentar dados ao arquivo.</span><span class="sxs-lookup"><span data-stu-id="4fc8f-138">Grants the right to append data to the file.</span></span> <span data-ttu-id="4fc8f-139">Para um diretório, esse valor concede o direito de criar um subdiretório.</span><span class="sxs-lookup"><span data-stu-id="4fc8f-139">For a directory, this value grants the right to create a subdirectory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fc8f-140"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**ARQUIVO de \_ leitura \_ ea**</span><span class="sxs-lookup"><span data-stu-id="4fc8f-140"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**FILE\_READ\_EA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fc8f-141">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="4fc8f-141">8 (0x8)</span></span>
</dt> <dt>



<span data-ttu-id="4fc8f-142">Concede o direito de ler atributos estendidos.</span><span class="sxs-lookup"><span data-stu-id="4fc8f-142">Grants the right to read extended attributes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fc8f-143"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**\_ea de gravação de arquivo \_**</span><span class="sxs-lookup"><span data-stu-id="4fc8f-143"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**FILE\_WRITE\_EA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fc8f-144">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="4fc8f-144">16 (0x10)</span></span>
</dt> <dt>



<span data-ttu-id="4fc8f-145">Concede o direito de gravar atributos estendidos.</span><span class="sxs-lookup"><span data-stu-id="4fc8f-145">Grants the right to write extended attributes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fc8f-146"><span id="FILE_EXECUTE"></span><span id="file_execute"></span>**\_Executar arquivo**</span><span class="sxs-lookup"><span data-stu-id="4fc8f-146"><span id="FILE_EXECUTE"></span><span id="file_execute"></span>**FILE\_EXECUTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fc8f-147">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="4fc8f-147">32 (0x20)</span></span>
</dt> <dt>



<span data-ttu-id="4fc8f-148">Concede o direito de executar um arquivo.</span><span class="sxs-lookup"><span data-stu-id="4fc8f-148">Grants the right to execute a file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fc8f-149"><span id="FILE_TRAVERSE"></span><span id="file_traverse"></span>**\_atravessamento de arquivo**</span><span class="sxs-lookup"><span data-stu-id="4fc8f-149"><span id="FILE_TRAVERSE"></span><span id="file_traverse"></span>**FILE\_TRAVERSE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fc8f-150">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="4fc8f-150">32 (0x20)</span></span>
</dt> <dt>



<span data-ttu-id="4fc8f-151">Concede o direito de executar um arquivo.</span><span class="sxs-lookup"><span data-stu-id="4fc8f-151">Grants the right to execute a file.</span></span> <span data-ttu-id="4fc8f-152">Para um diretório, o diretório pode ser atravessado.</span><span class="sxs-lookup"><span data-stu-id="4fc8f-152">For a directory, the directory can be traversed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fc8f-153"><span id="FILE_DELETE_CHILD"></span><span id="file_delete_child"></span>**\_excluir arquivo \_ filho**</span><span class="sxs-lookup"><span data-stu-id="4fc8f-153"><span id="FILE_DELETE_CHILD"></span><span id="file_delete_child"></span>**FILE\_DELETE\_CHILD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fc8f-154">64 (0x40)</span><span class="sxs-lookup"><span data-stu-id="4fc8f-154">64 (0x40)</span></span>
</dt> <dt>



<span data-ttu-id="4fc8f-155">Concede o direito de excluir um diretório e todos os arquivos que ele contém (seus filhos), mesmo que os arquivos sejam somente leitura.</span><span class="sxs-lookup"><span data-stu-id="4fc8f-155">Grants the right to delete a directory and all the files it contains (its children), even if the files are read-only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fc8f-156"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**\_atributos de leitura de arquivo \_**</span><span class="sxs-lookup"><span data-stu-id="4fc8f-156"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**FILE\_READ\_ATTRIBUTES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fc8f-157">128 (0x80)</span><span class="sxs-lookup"><span data-stu-id="4fc8f-157">128 (0x80)</span></span>
</dt> <dt>



<span data-ttu-id="4fc8f-158">Concede o direito de ler atributos de arquivo.</span><span class="sxs-lookup"><span data-stu-id="4fc8f-158">Grants the right to read file attributes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fc8f-159"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**\_atributos de gravação de arquivo \_**</span><span class="sxs-lookup"><span data-stu-id="4fc8f-159"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**FILE\_WRITE\_ATTRIBUTES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fc8f-160">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="4fc8f-160">256 (0x100)</span></span>
</dt> <dt>



<span data-ttu-id="4fc8f-161">Concede o direito de alterar atributos de arquivo.</span><span class="sxs-lookup"><span data-stu-id="4fc8f-161">Grants the right to change file attributes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fc8f-162"><span id="DELETE"></span><span id="delete"></span>**APAGAR**</span><span class="sxs-lookup"><span data-stu-id="4fc8f-162"><span id="DELETE"></span><span id="delete"></span>**DELETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fc8f-163">65536 (0x10000)</span><span class="sxs-lookup"><span data-stu-id="4fc8f-163">65536 (0x10000)</span></span>
</dt> <dt>



<span data-ttu-id="4fc8f-164">Concede o direito de excluir o objeto.</span><span class="sxs-lookup"><span data-stu-id="4fc8f-164">Grants the right to delete the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fc8f-165"><span id="READ_CONTROL"></span><span id="read_control"></span>**controle de leitura \_**</span><span class="sxs-lookup"><span data-stu-id="4fc8f-165"><span id="READ_CONTROL"></span><span id="read_control"></span>**READ\_CONTROL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fc8f-166">131072 (0x20000)</span><span class="sxs-lookup"><span data-stu-id="4fc8f-166">131072 (0x20000)</span></span>
</dt> <dt>



<span data-ttu-id="4fc8f-167">Concede o direito de ler as informações no descritor de segurança do objeto, sem incluir as informações na SACL.</span><span class="sxs-lookup"><span data-stu-id="4fc8f-167">Grants the right to read the information in the security descriptor for the object, not including the information in the SACL.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fc8f-168"><span id="WRITE_DAC"></span><span id="write_dac"></span>**GRAVAR \_ DAC**</span><span class="sxs-lookup"><span data-stu-id="4fc8f-168"><span id="WRITE_DAC"></span><span id="write_dac"></span>**WRITE\_DAC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fc8f-169">262144 (0x40000)</span><span class="sxs-lookup"><span data-stu-id="4fc8f-169">262144 (0x40000)</span></span>
</dt> <dt>



<span data-ttu-id="4fc8f-170">Concede o direito de modificar a DACL no descritor de segurança do objeto para o objeto.</span><span class="sxs-lookup"><span data-stu-id="4fc8f-170">Grants the right to modify the DACL in the object security descriptor for the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fc8f-171"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**proprietário da gravação \_**</span><span class="sxs-lookup"><span data-stu-id="4fc8f-171"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**WRITE\_OWNER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fc8f-172">524288 (0x80000)</span><span class="sxs-lookup"><span data-stu-id="4fc8f-172">524288 (0x80000)</span></span>
</dt> <dt>



<span data-ttu-id="4fc8f-173">Concede o direito de alterar o proprietário no descritor de segurança do objeto.</span><span class="sxs-lookup"><span data-stu-id="4fc8f-173">Grants the right to change the owner in the security descriptor for the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fc8f-174"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**NOVAMENTE**</span><span class="sxs-lookup"><span data-stu-id="4fc8f-174"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**SYNCHRONIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fc8f-175">1048576 (0x100000)</span><span class="sxs-lookup"><span data-stu-id="4fc8f-175">1048576 (0x100000)</span></span>
</dt> <dt>



<span data-ttu-id="4fc8f-176">Concede o direito de usar o objeto para sincronização.</span><span class="sxs-lookup"><span data-stu-id="4fc8f-176">Grants the right to use the object for synchronization.</span></span> <span data-ttu-id="4fc8f-177">Isso permite que um processo aguarde até que o objeto esteja no estado sinalizado.</span><span class="sxs-lookup"><span data-stu-id="4fc8f-177">This enables a process to wait until the object is in signaled state.</span></span> <span data-ttu-id="4fc8f-178">Alguns tipos de objeto não dão suporte a esse direito de acesso.</span><span class="sxs-lookup"><span data-stu-id="4fc8f-178">Some object types do not support this access right.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4fc8f-179">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4fc8f-179">Requirements</span></span>



| <span data-ttu-id="4fc8f-180">Requisito</span><span class="sxs-lookup"><span data-stu-id="4fc8f-180">Requirement</span></span> | <span data-ttu-id="4fc8f-181">Valor</span><span class="sxs-lookup"><span data-stu-id="4fc8f-181">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4fc8f-182">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4fc8f-182">Header</span></span><br/> | <dl> <span data-ttu-id="4fc8f-183"><dt>Winnt. h</dt></span><span class="sxs-lookup"><span data-stu-id="4fc8f-183"><dt>Winnt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4fc8f-184">Confira também</span><span class="sxs-lookup"><span data-stu-id="4fc8f-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fc8f-185">Constantes de segurança do WMI</span><span class="sxs-lookup"><span data-stu-id="4fc8f-185">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> <dt>

[<span data-ttu-id="4fc8f-186">Mantendo a segurança do WMI</span><span class="sxs-lookup"><span data-stu-id="4fc8f-186">Maintaining WMI Security</span></span>](maintaining-wmi-security.md)
</dt> </dl>

 

