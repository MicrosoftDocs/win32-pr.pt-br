---
description: Altera as permissões de segurança para o arquivo lógico especificado no caminho do objeto (esse método é uma versão estendida do método ChangeSecurityPermissions).
ms.assetid: 29155533-0898-4f8f-af08-f3ea46c8c1d3
ms.tgt_platform: multiple
title: Método ChangeSecurityPermissionsEx da classe CIM_LogicalFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.ChangeSecurityPermissionsEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: af2dc82ef54b6f32eee20f17cd61c0769cc64b1a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500915"
---
# <a name="changesecuritypermissionsex-method-of-the-cim_logicalfile-class"></a><span data-ttu-id="94fb5-103">Método ChangeSecurityPermissionsEx da classe de \_ LogicalFile CIM</span><span class="sxs-lookup"><span data-stu-id="94fb5-103">ChangeSecurityPermissionsEx method of the CIM\_LogicalFile class</span></span>

<span data-ttu-id="94fb5-104">O método **ChangeSecurityPermissionsEx** altera as permissões de segurança para o arquivo lógico especificado no caminho do objeto (esse método é uma versão estendida do método [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-cim-logicalfile.md) ).</span><span class="sxs-lookup"><span data-stu-id="94fb5-104">The **ChangeSecurityPermissionsEx** method changes the security permissions for the logical file specified in the object path (this method is an extended version of the [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-cim-logicalfile.md) method).</span></span> <span data-ttu-id="94fb5-105">Se o arquivo lógico for um diretório, esse método agirá de forma recursiva, alterando as permissões de segurança para todos os arquivos e subdiretórios que o diretório contém.</span><span class="sxs-lookup"><span data-stu-id="94fb5-105">If the logical file is a directory, then this method will act recursively, changing the security permissions for all of the files and sub-directories that the directory contains.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="94fb5-106">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="94fb5-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="94fb5-107">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="94fb5-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="94fb5-108">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="94fb5-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="94fb5-109">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="94fb5-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="94fb5-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="94fb5-110">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissionsEx(
  [in]           Win32_SecurityDescriptor SecurityDescriptor,
  [in]           uint32                   Option,
  [out]          string                   StopFileName,
  [in, optional] string                   StartFileName,
  [in, optional] boolean                  Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="94fb5-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="94fb5-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94fb5-112">*SecurityDescriptor* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="94fb5-112">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94fb5-113">Especifica as informações de segurança.</span><span class="sxs-lookup"><span data-stu-id="94fb5-113">Specifies the security information.</span></span>

</dd> <dt>

<span data-ttu-id="94fb5-114">*Opção* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="94fb5-114">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94fb5-115">Privilégio de segurança a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="94fb5-115">Security privilege to modify.</span></span> <span data-ttu-id="94fb5-116">Por exemplo, para alterar a segurança do proprietário e da DACL, use</span><span class="sxs-lookup"><span data-stu-id="94fb5-116">For example, to change the owner and DACL security, use</span></span>

`Option = 1 + 4`

<span data-ttu-id="94fb5-117">ou</span><span class="sxs-lookup"><span data-stu-id="94fb5-117">or</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="Change_Owner_Security_Information"></span><span id="change_owner_security_information"></span><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span>

<span data-ttu-id="94fb5-118"><span id="Change_Owner_Security_Information"></span><span id="change_owner_security_information"></span><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span>**Alterar \_ \_ \_ Informações de segurança do proprietário** (1)</span><span class="sxs-lookup"><span data-stu-id="94fb5-118"><span id="Change_Owner_Security_Information"></span><span id="change_owner_security_information"></span><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span>**Change\_Owner\_Security\_Information** (1)</span></span>


</dt> <dd>

<span data-ttu-id="94fb5-119">Altere o proprietário do arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="94fb5-119">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="Change_Group_Security_Information"></span><span id="change_group_security_information"></span><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span>

<span data-ttu-id="94fb5-120"><span id="Change_Group_Security_Information"></span><span id="change_group_security_information"></span><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span>**Alterar \_ \_ \_ Informações de segurança do grupo** (2)</span><span class="sxs-lookup"><span data-stu-id="94fb5-120"><span id="Change_Group_Security_Information"></span><span id="change_group_security_information"></span><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span>**Change\_Group\_Security\_Information** (2)</span></span>


</dt> <dd>

<span data-ttu-id="94fb5-121">Altere o grupo do arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="94fb5-121">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="Change_Dacl_Security_Information"></span><span id="change_dacl_security_information"></span><span id="CHANGE_DACL_SECURITY_INFORMATION"></span>

<span data-ttu-id="94fb5-122"><span id="Change_Dacl_Security_Information"></span><span id="change_dacl_security_information"></span><span id="CHANGE_DACL_SECURITY_INFORMATION"></span>**Alterar \_ \_ \_ Informações de segurança da DACL** (4)</span><span class="sxs-lookup"><span data-stu-id="94fb5-122"><span id="Change_Dacl_Security_Information"></span><span id="change_dacl_security_information"></span><span id="CHANGE_DACL_SECURITY_INFORMATION"></span>**Change\_Dacl\_Security\_Information** (4)</span></span>


</dt> <dd>

<span data-ttu-id="94fb5-123">Altere a ACL do arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="94fb5-123">Change the ACL of the logical file.</span></span>

</dd> <dt>

<span id="Change_Sacl_Security_Information"></span><span id="change_sacl_security_information"></span><span id="CHANGE_SACL_SECURITY_INFORMATION"></span>

<span data-ttu-id="94fb5-124"><span id="Change_Sacl_Security_Information"></span><span id="change_sacl_security_information"></span><span id="CHANGE_SACL_SECURITY_INFORMATION"></span>**Alterar \_ \_ \_ Informações de segurança da SACL** (8)</span><span class="sxs-lookup"><span data-stu-id="94fb5-124"><span id="Change_Sacl_Security_Information"></span><span id="change_sacl_security_information"></span><span id="CHANGE_SACL_SECURITY_INFORMATION"></span>**Change\_Sacl\_Security\_Information** (8)</span></span>


</dt> <dd>

<span data-ttu-id="94fb5-125">Altere a ACL do sistema do arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="94fb5-125">Change the system ACL of the logical file.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="94fb5-126">*StopFileName* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="94fb5-126">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="94fb5-127">Cadeia de caracteres que representa o nome do arquivo (ou diretório) em que o método falhou.</span><span class="sxs-lookup"><span data-stu-id="94fb5-127">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="94fb5-128">Esse parâmetro tem um valor de **NULL** se o método tiver sucesso.</span><span class="sxs-lookup"><span data-stu-id="94fb5-128">This parameter has a value of **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="94fb5-129">*StartFileName* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="94fb5-129">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="94fb5-130">Cadeia de caracteres que representa o arquivo filho (ou diretório) a ser usado como ponto de partida para esse método.</span><span class="sxs-lookup"><span data-stu-id="94fb5-130">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="94fb5-131">Normalmente, o parâmetro *StartFileName* é o parâmetro *StopFileName* que especifica o arquivo (ou diretório) no qual ocorreu um erro da chamada de método anterior.</span><span class="sxs-lookup"><span data-stu-id="94fb5-131">Typically, the *StartFileName* parameter is the *StopFileName* parameter specifying the file (or directory) at which an error occurred from the previous method call.</span></span> <span data-ttu-id="94fb5-132">Se o valor do parâmetro for **NULL**, a operação será executada no arquivo ou diretório especificado na chamada de [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="94fb5-132">If the parameter value is **null**, the operation is performed on the file or directory specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="94fb5-133">*Recursivo* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="94fb5-133">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="94fb5-134">Se **for true**, as permissões de segurança serão aplicadas recursivamente aos arquivos e diretórios dentro do diretório especificado pela instância de [**\_ LogicalFile do CIM**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="94fb5-134">If **TRUE**, the security permissions are applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span> <span data-ttu-id="94fb5-135">Para instâncias de arquivo, esse parâmetro é ignorado.</span><span class="sxs-lookup"><span data-stu-id="94fb5-135">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94fb5-136">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="94fb5-136">Return value</span></span>

<span data-ttu-id="94fb5-137">Retorna um valor de 0 (zero) em caso de êxito e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="94fb5-137">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="94fb5-138">**Êxito**</span><span class="sxs-lookup"><span data-stu-id="94fb5-138">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="94fb5-139">0</span><span class="sxs-lookup"><span data-stu-id="94fb5-139">0</span></span>

<span data-ttu-id="94fb5-140">Sucesso.</span><span class="sxs-lookup"><span data-stu-id="94fb5-140">Success.</span></span>

</dd> <dt>

<span data-ttu-id="94fb5-141">**Acesso negado**</span><span class="sxs-lookup"><span data-stu-id="94fb5-141">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="94fb5-142">2</span><span class="sxs-lookup"><span data-stu-id="94fb5-142">2</span></span>

<span data-ttu-id="94fb5-143">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="94fb5-143">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="94fb5-144">**Falha não especificada**</span><span class="sxs-lookup"><span data-stu-id="94fb5-144">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="94fb5-145">8</span><span class="sxs-lookup"><span data-stu-id="94fb5-145">8</span></span>

<span data-ttu-id="94fb5-146">Falha não especificada.</span><span class="sxs-lookup"><span data-stu-id="94fb5-146">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="94fb5-147">**Objeto inválido**</span><span class="sxs-lookup"><span data-stu-id="94fb5-147">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="94fb5-148">9</span><span class="sxs-lookup"><span data-stu-id="94fb5-148">9</span></span>

<span data-ttu-id="94fb5-149">Objeto inválido.</span><span class="sxs-lookup"><span data-stu-id="94fb5-149">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="94fb5-150">**O objeto já existe**</span><span class="sxs-lookup"><span data-stu-id="94fb5-150">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="94fb5-151">10</span><span class="sxs-lookup"><span data-stu-id="94fb5-151">10</span></span>

<span data-ttu-id="94fb5-152">O objeto já existe.</span><span class="sxs-lookup"><span data-stu-id="94fb5-152">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="94fb5-153">**Sistema de arquivos não NTFS**</span><span class="sxs-lookup"><span data-stu-id="94fb5-153">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="94fb5-154">11</span><span class="sxs-lookup"><span data-stu-id="94fb5-154">11</span></span>

<span data-ttu-id="94fb5-155">Sistema de arquivos não NTFS.</span><span class="sxs-lookup"><span data-stu-id="94fb5-155">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="94fb5-156">**Plataforma não NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="94fb5-156">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="94fb5-157">12</span><span class="sxs-lookup"><span data-stu-id="94fb5-157">12</span></span>

<span data-ttu-id="94fb5-158">Plataforma não Windows.</span><span class="sxs-lookup"><span data-stu-id="94fb5-158">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="94fb5-159">**A unidade não é a mesma**</span><span class="sxs-lookup"><span data-stu-id="94fb5-159">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="94fb5-160">13</span><span class="sxs-lookup"><span data-stu-id="94fb5-160">13</span></span>

<span data-ttu-id="94fb5-161">A unidade não é a mesma.</span><span class="sxs-lookup"><span data-stu-id="94fb5-161">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="94fb5-162">**Diretório não vazio**</span><span class="sxs-lookup"><span data-stu-id="94fb5-162">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="94fb5-163">14</span><span class="sxs-lookup"><span data-stu-id="94fb5-163">14</span></span>

<span data-ttu-id="94fb5-164">O diretório não está vazio.</span><span class="sxs-lookup"><span data-stu-id="94fb5-164">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="94fb5-165">**Violação de compartilhamento**</span><span class="sxs-lookup"><span data-stu-id="94fb5-165">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="94fb5-166">15</span><span class="sxs-lookup"><span data-stu-id="94fb5-166">15</span></span>

<span data-ttu-id="94fb5-167">Violação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="94fb5-167">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="94fb5-168">**Arquivo de início inválido**</span><span class="sxs-lookup"><span data-stu-id="94fb5-168">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="94fb5-169">16</span><span class="sxs-lookup"><span data-stu-id="94fb5-169">16</span></span>

<span data-ttu-id="94fb5-170">Arquivo inicial inválido.</span><span class="sxs-lookup"><span data-stu-id="94fb5-170">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="94fb5-171">**Privilégio não mantido**</span><span class="sxs-lookup"><span data-stu-id="94fb5-171">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="94fb5-172">17</span><span class="sxs-lookup"><span data-stu-id="94fb5-172">17</span></span>

<span data-ttu-id="94fb5-173">Privilégio não mantido.</span><span class="sxs-lookup"><span data-stu-id="94fb5-173">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="94fb5-174">**Parâmetro inválido**</span><span class="sxs-lookup"><span data-stu-id="94fb5-174">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="94fb5-175">21</span><span class="sxs-lookup"><span data-stu-id="94fb5-175">21</span></span>

<span data-ttu-id="94fb5-176">Parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="94fb5-176">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="94fb5-177">Comentários</span><span class="sxs-lookup"><span data-stu-id="94fb5-177">Remarks</span></span>

<span data-ttu-id="94fb5-178">Este método não está implementado no momento pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="94fb5-178">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="94fb5-179">Para usar esse método, você deve implementá-lo em seu próprio provedor.</span><span class="sxs-lookup"><span data-stu-id="94fb5-179">To use this method, you must implement it in your own provider.</span></span>

## <a name="requirements"></a><span data-ttu-id="94fb5-180">Requisitos</span><span class="sxs-lookup"><span data-stu-id="94fb5-180">Requirements</span></span>



| <span data-ttu-id="94fb5-181">Requisito</span><span class="sxs-lookup"><span data-stu-id="94fb5-181">Requirement</span></span> | <span data-ttu-id="94fb5-182">Valor</span><span class="sxs-lookup"><span data-stu-id="94fb5-182">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="94fb5-183">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="94fb5-183">Minimum supported client</span></span><br/> | <span data-ttu-id="94fb5-184">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="94fb5-184">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="94fb5-185">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="94fb5-185">Minimum supported server</span></span><br/> | <span data-ttu-id="94fb5-186">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="94fb5-186">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="94fb5-187">Namespace</span><span class="sxs-lookup"><span data-stu-id="94fb5-187">Namespace</span></span><br/>                | <span data-ttu-id="94fb5-188">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="94fb5-188">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="94fb5-189">MOF</span><span class="sxs-lookup"><span data-stu-id="94fb5-189">MOF</span></span><br/>                      | <dl> <span data-ttu-id="94fb5-190"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="94fb5-190"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="94fb5-191">DLL</span><span class="sxs-lookup"><span data-stu-id="94fb5-191">DLL</span></span><br/>                      | <dl> <span data-ttu-id="94fb5-192"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="94fb5-192"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94fb5-193">Confira também</span><span class="sxs-lookup"><span data-stu-id="94fb5-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94fb5-194">**CIM \_ LogicalFile**</span><span class="sxs-lookup"><span data-stu-id="94fb5-194">**CIM\_LogicalFile**</span></span>](changesecuritypermissionsex-method-in-class-cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="94fb5-195">**CIM \_ LogicalFile**</span><span class="sxs-lookup"><span data-stu-id="94fb5-195">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

