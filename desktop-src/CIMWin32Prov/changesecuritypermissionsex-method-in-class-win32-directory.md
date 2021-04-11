---
description: Altera as permissões de segurança para o arquivo de entrada de diretório especificado no caminho do objeto (esse método é uma versão estendida do método ChangeSecurityPermissions).
ms.assetid: 787e48af-7cb4-4d0b-a2f1-ffa696466ef2
ms.tgt_platform: multiple
title: Método ChangeSecurityPermissionsEx da classe Win32_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.ChangeSecurityPermissionsEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4bcadd4a4ad115a1a367db4f2a2f645eb6a4742c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164006"
---
# <a name="changesecuritypermissionsex-method-of-the-win32_directory-class"></a><span data-ttu-id="ef24e-103">Método ChangeSecurityPermissionsEx da classe do \_ diretório Win32</span><span class="sxs-lookup"><span data-stu-id="ef24e-103">ChangeSecurityPermissionsEx method of the Win32\_Directory class</span></span>

<span data-ttu-id="ef24e-104">O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **ChangeSecurityPermissionsEx** altera as permissões de segurança para o arquivo de entrada de diretório especificado no caminho do objeto (esse método é uma versão estendida do método [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-win32-directory.md) ).</span><span class="sxs-lookup"><span data-stu-id="ef24e-104">The **ChangeSecurityPermissionsEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method changes the security permissions for the directory entry file specified in the object path (this method is an extended version of the [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-win32-directory.md) method).</span></span> <span data-ttu-id="ef24e-105">Se o arquivo lógico for um diretório, esse método será recursivo e alterará as permissões de segurança de todos os arquivos e subdiretórios que o diretório contém.</span><span class="sxs-lookup"><span data-stu-id="ef24e-105">If the logical file is a directory, then this method is recursive, and changes the security permissions of all of the files and subdirectories that the directory contains.</span></span>

<span data-ttu-id="ef24e-106">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="ef24e-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="ef24e-107">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="ef24e-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="ef24e-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ef24e-108">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissionsEx(
  [in]           Win32_SecurityDescriptor SecurityDescriptor,
  [in]           uint32                   Option,
  [out]          string                   StopFileName,
  [in, optional] string                   StartFileName,
  [in, optional] boolean                  Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="ef24e-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ef24e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef24e-110">*SecurityDescriptor* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ef24e-110">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef24e-111">Expressão que resolve para uma instância do [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span><span class="sxs-lookup"><span data-stu-id="ef24e-111">Expression that resolves to an instance of [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span> <span data-ttu-id="ef24e-112">Esse parâmetro contém novas permissões de segurança para a instância [**do \_ arquivo de paginação Win32**](win32-pagefile.md).</span><span class="sxs-lookup"><span data-stu-id="ef24e-112">This parameter contains new security permissions for the instance of [**Win32\_PageFile**](win32-pagefile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef24e-113">*Opção* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ef24e-113">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef24e-114">Privilégio de segurança a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="ef24e-114">Security privilege to be modified.</span></span> <span data-ttu-id="ef24e-115">Por exemplo, para alterar a segurança do proprietário e da DACL (lista de controle de acesso discricionário), use o seguinte:</span><span class="sxs-lookup"><span data-stu-id="ef24e-115">For example, to change the owner and discretionary access control list (DACL) security, use the following:</span></span>

`Option = 1 + 4`

<span data-ttu-id="ef24e-116">– ou –</span><span class="sxs-lookup"><span data-stu-id="ef24e-116">-or-</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span data-ttu-id="ef24e-117"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**Alterar \_ \_ \_ Informações de segurança do proprietário** (1)</span><span class="sxs-lookup"><span data-stu-id="ef24e-117"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE\_OWNER\_SECURITY\_INFORMATION** (1)</span></span>


</dt> <dd>

<span data-ttu-id="ef24e-118">Altere o proprietário do arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="ef24e-118">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span data-ttu-id="ef24e-119"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**Alterar \_ \_ \_ Informações de segurança do grupo** (2)</span><span class="sxs-lookup"><span data-stu-id="ef24e-119"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE\_GROUP\_SECURITY\_INFORMATION** (2)</span></span>


</dt> <dd>

<span data-ttu-id="ef24e-120">Altere o grupo do arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="ef24e-120">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span data-ttu-id="ef24e-121"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**Alterar \_ \_ \_ Informações de segurança da DACL** (4)</span><span class="sxs-lookup"><span data-stu-id="ef24e-121"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE\_DACL\_SECURITY\_INFORMATION** (4)</span></span>


</dt> <dd>

<span data-ttu-id="ef24e-122">Altere a lista DACL do arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="ef24e-122">Change the DACL list of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span data-ttu-id="ef24e-123"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Alterar \_ \_ \_ Informações de segurança da SACL** (8)</span><span class="sxs-lookup"><span data-stu-id="ef24e-123"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE\_SACL\_SECURITY\_INFORMATION** (8)</span></span>


</dt> <dd>

<span data-ttu-id="ef24e-124">Altere a lista de controle de acesso do sistema (SACL) do arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="ef24e-124">Change the system access control list (SACL) of the logical file.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="ef24e-125">*StopFileName* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ef24e-125">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ef24e-126">Nome do arquivo ou diretório em que o método **ChangeSecurityPermissionsEx** falhou.</span><span class="sxs-lookup"><span data-stu-id="ef24e-126">Name of the file or directory where the **ChangeSecurityPermissionsEx** method failed.</span></span> <span data-ttu-id="ef24e-127">Esse parâmetro será nulo se o método tiver sucesso.</span><span class="sxs-lookup"><span data-stu-id="ef24e-127">This parameter is null if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="ef24e-128">*StartFileName* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="ef24e-128">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ef24e-129">Nomeia o arquivo ou diretório filho a ser usado como ponto de partida para **ChangeSecurityPermissionsEx**.</span><span class="sxs-lookup"><span data-stu-id="ef24e-129">Names the child file or directory to use as a starting point for **ChangeSecurityPermissionsEx**.</span></span> <span data-ttu-id="ef24e-130">Normalmente, o parâmetro *StartFileName* é o parâmetro *StopFileName* que especifica o arquivo ou diretório em que ocorreu um erro da chamada de método anterior.</span><span class="sxs-lookup"><span data-stu-id="ef24e-130">Typically, the *StartFileName* parameter is the *StopFileName* parameter that specifies the file or directory where an error occurred from the previous method call.</span></span> <span data-ttu-id="ef24e-131">Se esse parâmetro for nulo, a operação será executada no arquivo ou diretório especificado na chamada de **ExecMethod** .</span><span class="sxs-lookup"><span data-stu-id="ef24e-131">If this parameter is null, the operation is performed on the file or directory that is specified in the **ExecMethod** call.</span></span> <span data-ttu-id="ef24e-132">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="ef24e-132">This parameter is optional.</span></span>

<span data-ttu-id="ef24e-133">Se o *StartFileName* for usado, *recursivo* deverá ser definido como true também.</span><span class="sxs-lookup"><span data-stu-id="ef24e-133">If *StartFileName* is used, *Recursive* must be set to true as well.</span></span>

</dd> <dt>

<span data-ttu-id="ef24e-134">*Recursivo* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="ef24e-134">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ef24e-135">Se for **true**, a alteração de propriedade será aplicada recursivamente aos arquivos e diretórios dentro do diretório especificado pela instância de [**\_ LogicalFile do CIM**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="ef24e-135">If **true**, the change of ownership is applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span> <span data-ttu-id="ef24e-136">Para instâncias de arquivo, o parâmetro de entrada *recursivo* é ignorado.</span><span class="sxs-lookup"><span data-stu-id="ef24e-136">For file instances, the *Recursive* input parameter is ignored.</span></span> <span data-ttu-id="ef24e-137">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="ef24e-137">This parameter is optional.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef24e-138">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ef24e-138">Return value</span></span>

<span data-ttu-id="ef24e-139">Retorna um valor de 0 (zero) se as permissões forem alteradas e um número diferente para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="ef24e-139">Returns a value of 0 (zero) if the permissions are changed, and a different number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="ef24e-140">**Êxito**</span><span class="sxs-lookup"><span data-stu-id="ef24e-140">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="ef24e-141">0</span><span class="sxs-lookup"><span data-stu-id="ef24e-141">0</span></span>

<span data-ttu-id="ef24e-142">A solicitação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="ef24e-142">The request is successful.</span></span>

</dd> <dt>

<span data-ttu-id="ef24e-143">**Acesso negado**</span><span class="sxs-lookup"><span data-stu-id="ef24e-143">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="ef24e-144">2</span><span class="sxs-lookup"><span data-stu-id="ef24e-144">2</span></span>

<span data-ttu-id="ef24e-145">O acesso foi negado.</span><span class="sxs-lookup"><span data-stu-id="ef24e-145">Access is denied.</span></span>

</dd> <dt>

<span data-ttu-id="ef24e-146">**Falha não especificada**</span><span class="sxs-lookup"><span data-stu-id="ef24e-146">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="ef24e-147">8</span><span class="sxs-lookup"><span data-stu-id="ef24e-147">8</span></span>

<span data-ttu-id="ef24e-148">Ocorreu uma falha não especificada.</span><span class="sxs-lookup"><span data-stu-id="ef24e-148">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="ef24e-149">**Objeto inválido**</span><span class="sxs-lookup"><span data-stu-id="ef24e-149">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="ef24e-150">9</span><span class="sxs-lookup"><span data-stu-id="ef24e-150">9</span></span>

<span data-ttu-id="ef24e-151">O nome especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="ef24e-151">The specified name is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="ef24e-152">**O objeto já existe**</span><span class="sxs-lookup"><span data-stu-id="ef24e-152">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="ef24e-153">10</span><span class="sxs-lookup"><span data-stu-id="ef24e-153">10</span></span>

<span data-ttu-id="ef24e-154">O objeto especificado já existe.</span><span class="sxs-lookup"><span data-stu-id="ef24e-154">The specified object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="ef24e-155">**Sistema de arquivos não NTFS**</span><span class="sxs-lookup"><span data-stu-id="ef24e-155">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="ef24e-156">11</span><span class="sxs-lookup"><span data-stu-id="ef24e-156">11</span></span>

<span data-ttu-id="ef24e-157">O sistema de arquivos não é um sistema de arquivos NTFS.</span><span class="sxs-lookup"><span data-stu-id="ef24e-157">The file system is not an NTFS file system.</span></span>

</dd> <dt>

<span data-ttu-id="ef24e-158">**Plataforma não NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="ef24e-158">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="ef24e-159">12</span><span class="sxs-lookup"><span data-stu-id="ef24e-159">12</span></span>

<span data-ttu-id="ef24e-160">A plataforma não é o Windows.</span><span class="sxs-lookup"><span data-stu-id="ef24e-160">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="ef24e-161">**A unidade não é a mesma**</span><span class="sxs-lookup"><span data-stu-id="ef24e-161">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="ef24e-162">13</span><span class="sxs-lookup"><span data-stu-id="ef24e-162">13</span></span>

<span data-ttu-id="ef24e-163">A unidade não é a mesma.</span><span class="sxs-lookup"><span data-stu-id="ef24e-163">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="ef24e-164">**Diretório não vazio**</span><span class="sxs-lookup"><span data-stu-id="ef24e-164">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="ef24e-165">14</span><span class="sxs-lookup"><span data-stu-id="ef24e-165">14</span></span>

<span data-ttu-id="ef24e-166">O diretório não está vazio.</span><span class="sxs-lookup"><span data-stu-id="ef24e-166">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="ef24e-167">**Violação de compartilhamento**</span><span class="sxs-lookup"><span data-stu-id="ef24e-167">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="ef24e-168">15</span><span class="sxs-lookup"><span data-stu-id="ef24e-168">15</span></span>

<span data-ttu-id="ef24e-169">Há uma violação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="ef24e-169">There is a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="ef24e-170">**Arquivo de início inválido**</span><span class="sxs-lookup"><span data-stu-id="ef24e-170">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="ef24e-171">16</span><span class="sxs-lookup"><span data-stu-id="ef24e-171">16</span></span>

<span data-ttu-id="ef24e-172">O arquivo de início especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="ef24e-172">The specified start file is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="ef24e-173">**Privilégio não mantido**</span><span class="sxs-lookup"><span data-stu-id="ef24e-173">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="ef24e-174">17</span><span class="sxs-lookup"><span data-stu-id="ef24e-174">17</span></span>

<span data-ttu-id="ef24e-175">Um privilégio necessário para a operação não é mantido.</span><span class="sxs-lookup"><span data-stu-id="ef24e-175">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="ef24e-176">**Parâmetro inválido**</span><span class="sxs-lookup"><span data-stu-id="ef24e-176">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="ef24e-177">21</span><span class="sxs-lookup"><span data-stu-id="ef24e-177">21</span></span>

<span data-ttu-id="ef24e-178">Um parâmetro especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="ef24e-178">A specified parameter is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ef24e-179">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ef24e-179">Requirements</span></span>



| <span data-ttu-id="ef24e-180">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef24e-180">Requirement</span></span> | <span data-ttu-id="ef24e-181">Valor</span><span class="sxs-lookup"><span data-stu-id="ef24e-181">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ef24e-182">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ef24e-182">Minimum supported client</span></span><br/> | <span data-ttu-id="ef24e-183">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ef24e-183">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ef24e-184">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ef24e-184">Minimum supported server</span></span><br/> | <span data-ttu-id="ef24e-185">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ef24e-185">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ef24e-186">Namespace</span><span class="sxs-lookup"><span data-stu-id="ef24e-186">Namespace</span></span><br/>                | <span data-ttu-id="ef24e-187">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="ef24e-187">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ef24e-188">MOF</span><span class="sxs-lookup"><span data-stu-id="ef24e-188">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ef24e-189"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ef24e-189"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ef24e-190">DLL</span><span class="sxs-lookup"><span data-stu-id="ef24e-190">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef24e-191"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ef24e-191"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef24e-192">Confira também</span><span class="sxs-lookup"><span data-stu-id="ef24e-192">See also</span></span>

<dl> <dt>

<span data-ttu-id="ef24e-193">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ef24e-193">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="ef24e-194">**\_Diretório Win32**</span><span class="sxs-lookup"><span data-stu-id="ef24e-194">**Win32\_Directory**</span></span>](win32-directory.md)
</dt> </dl>

 

