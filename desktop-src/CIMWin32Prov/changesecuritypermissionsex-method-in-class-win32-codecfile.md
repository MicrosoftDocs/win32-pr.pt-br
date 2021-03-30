---
description: Altera as permissões de segurança para o arquivo de codec especificado no caminho do objeto (esse método é uma versão estendida do método ChangeSecurityPermissions).
ms.assetid: 3eac4ae1-3c0e-4e81-8b23-9ad8698f723c
ms.tgt_platform: multiple
title: Método ChangeSecurityPermissionsEx da classe Win32_CodecFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile.ChangeSecurityPermissionsEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 549c55a5066bdaba4699ec76ed3b7be23eb28b96
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826349"
---
# <a name="changesecuritypermissionsex-method-of-the-win32_codecfile-class"></a><span data-ttu-id="17d94-103">Método ChangeSecurityPermissionsEx da classe de um codec do Win32 \_</span><span class="sxs-lookup"><span data-stu-id="17d94-103">ChangeSecurityPermissionsEx method of the Win32\_CodecFile class</span></span>

<span data-ttu-id="17d94-104">O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **ChangeSecurityPermissionsEx** altera as permissões de segurança para o arquivo de codec especificado no caminho do objeto (esse método é uma versão estendida do método [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-win32-directory.md) ).</span><span class="sxs-lookup"><span data-stu-id="17d94-104">The **ChangeSecurityPermissionsEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method changes the security permissions for the codec file specified in the object path (this method is an extended version of the [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-win32-directory.md) method).</span></span> <span data-ttu-id="17d94-105">Se o arquivo lógico for um diretório, esse método será recursivo e alterará as permissões de segurança de todos os arquivos e subdiretórios que o diretório contém.</span><span class="sxs-lookup"><span data-stu-id="17d94-105">If the logical file is a directory, then this method is recursive, and changes the security permissions of all the files and subdirectories that the directory contains.</span></span>

<span data-ttu-id="17d94-106">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="17d94-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="17d94-107">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="17d94-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="17d94-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="17d94-108">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissionsEx(
  [in]           Win32_SecurityDescriptor SecurityDescriptor,
  [in]           uint32                   Option,
  [out]          string                   StopFileName,
  [in, optional] string                   StartFileName,
  [in, optional] boolean                  Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="17d94-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="17d94-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17d94-110">*SecurityDescriptor* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="17d94-110">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17d94-111">Expressão que resolve para uma instância do [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span><span class="sxs-lookup"><span data-stu-id="17d94-111">Expression that resolves to an instance of [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span> <span data-ttu-id="17d94-112">Esse descritor contém novas permissões de segurança para a instância do [**\_ codec do Win32**](win32-codecfile.md).</span><span class="sxs-lookup"><span data-stu-id="17d94-112">This descriptor contains new security permissions for the instance of [**Win32\_CodecFile**](win32-codecfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="17d94-113">*Opção* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="17d94-113">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17d94-114">Privilégio de segurança real a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="17d94-114">Actual security privilege to be modified.</span></span> <span data-ttu-id="17d94-115">Por exemplo, para alterar a segurança do proprietário e da DACL (lista de controle de acesso discricionário), use o seguinte:</span><span class="sxs-lookup"><span data-stu-id="17d94-115">For example, to change the owner and discretionary access control list (DACL) security, use the following:</span></span>

`Option = 1 + 4`

<span data-ttu-id="17d94-116">– ou –</span><span class="sxs-lookup"><span data-stu-id="17d94-116">-or-</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span data-ttu-id="17d94-117"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**Alterar \_ \_ \_ Informações de segurança do proprietário** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="17d94-117"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE\_OWNER\_SECURITY\_INFORMATION** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="17d94-118">Altere o proprietário do arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="17d94-118">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span data-ttu-id="17d94-119"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**Alterar \_ \_ \_ Informações de segurança do grupo** (2 (0x2))</span><span class="sxs-lookup"><span data-stu-id="17d94-119"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE\_GROUP\_SECURITY\_INFORMATION** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="17d94-120">Altere o grupo do arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="17d94-120">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span data-ttu-id="17d94-121"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**Alterar \_ \_ \_ Informações de segurança da DACL** (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="17d94-121"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE\_DACL\_SECURITY\_INFORMATION** (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="17d94-122">Altere a DACL (lista de controle de acesso discricionário) do arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="17d94-122">Change the discretionary access control list (DACL) of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span data-ttu-id="17d94-123"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Alterar \_ \_ \_ Informações de segurança de SACL** (8 (0x8))</span><span class="sxs-lookup"><span data-stu-id="17d94-123"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE\_SACL\_SECURITY\_INFORMATION** (8 (0x8))</span></span>


</dt> <dd>

<span data-ttu-id="17d94-124">Altere a lista de controle de acesso do sistema (SACL) do arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="17d94-124">Change the system access control list (SACL) of the logical file.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="17d94-125">*StopFileName* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="17d94-125">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="17d94-126">Nome do arquivo ou diretório em que o método **ChangeSecurityPermissionsEx** falhou.</span><span class="sxs-lookup"><span data-stu-id="17d94-126">Name of the file or directory where the **ChangeSecurityPermissionsEx** method failed.</span></span> <span data-ttu-id="17d94-127">Esse parâmetro é nulo quando o método é executado com sucesso.</span><span class="sxs-lookup"><span data-stu-id="17d94-127">This parameter is null when the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="17d94-128">*StartFileName* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="17d94-128">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="17d94-129">Nomeia o arquivo ou diretório filho a ser usado como ponto de partida para **ChangeSecurityPermissionsEx**.</span><span class="sxs-lookup"><span data-stu-id="17d94-129">Names the child file or directory to use as a starting point for **ChangeSecurityPermissionsEx**.</span></span> <span data-ttu-id="17d94-130">Normalmente, o parâmetro *StartFileName* é o parâmetro *StopFileName* que especifica o arquivo ou diretório em que ocorreu um erro da chamada de método anterior.</span><span class="sxs-lookup"><span data-stu-id="17d94-130">Typically, the *StartFileName* parameter is the *StopFileName* parameter that specifies the file or directory where an error occurred from the previous method call.</span></span> <span data-ttu-id="17d94-131">Se esse parâmetro for nulo, a operação será executada no arquivo ou diretório especificado na chamada de [**ExecMethod**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="17d94-131">If this parameter is null, the operation is performed on the file or directory specified in the [**ExecMethod**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="17d94-132">*Recursivo* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="17d94-132">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="17d94-133">Se **for true**, as alterações de propriedade serão aplicadas recursivamente aos arquivos e diretórios no diretório especificado pela instância de [**\_ LogicalFile do CIM**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="17d94-133">If **true**, the changes of ownership are applied recursively to files and directories in the directory that the [**CIM\_LogicalFile**](cim-logicalfile.md) instance specifies.</span></span> <span data-ttu-id="17d94-134">Para instâncias de arquivo, o parâmetro de entrada *recursivo* é ignorado.</span><span class="sxs-lookup"><span data-stu-id="17d94-134">For file instances, the *Recursive* input parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17d94-135">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="17d94-135">Return value</span></span>

<span data-ttu-id="17d94-136">Retorna um valor de 0 (zero) se as permissões forem alteradas e um número diferente para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="17d94-136">Returns an value of 0 (zero) if the permissions are changed, and a different number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="17d94-137">**Êxito**</span><span class="sxs-lookup"><span data-stu-id="17d94-137">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="17d94-138">0</span><span class="sxs-lookup"><span data-stu-id="17d94-138">0</span></span>

<span data-ttu-id="17d94-139">A solicitação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="17d94-139">The request is successful.</span></span>

</dd> <dt>

<span data-ttu-id="17d94-140">**Acesso negado**</span><span class="sxs-lookup"><span data-stu-id="17d94-140">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="17d94-141">2</span><span class="sxs-lookup"><span data-stu-id="17d94-141">2</span></span>

<span data-ttu-id="17d94-142">O acesso foi negado.</span><span class="sxs-lookup"><span data-stu-id="17d94-142">Access is denied.</span></span>

</dd> <dt>

<span data-ttu-id="17d94-143">**Falha não especificada**</span><span class="sxs-lookup"><span data-stu-id="17d94-143">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="17d94-144">8</span><span class="sxs-lookup"><span data-stu-id="17d94-144">8</span></span>

<span data-ttu-id="17d94-145">Ocorreu uma falha não especificada.</span><span class="sxs-lookup"><span data-stu-id="17d94-145">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="17d94-146">**Objeto inválido**</span><span class="sxs-lookup"><span data-stu-id="17d94-146">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="17d94-147">9</span><span class="sxs-lookup"><span data-stu-id="17d94-147">9</span></span>

<span data-ttu-id="17d94-148">O nome especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="17d94-148">The specified name is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="17d94-149">**O objeto já existe**</span><span class="sxs-lookup"><span data-stu-id="17d94-149">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="17d94-150">10</span><span class="sxs-lookup"><span data-stu-id="17d94-150">10</span></span>

<span data-ttu-id="17d94-151">O objeto especificado já existe.</span><span class="sxs-lookup"><span data-stu-id="17d94-151">The specified object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="17d94-152">**Sistema de arquivos não NTFS**</span><span class="sxs-lookup"><span data-stu-id="17d94-152">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="17d94-153">11</span><span class="sxs-lookup"><span data-stu-id="17d94-153">11</span></span>

<span data-ttu-id="17d94-154">O sistema de arquivos não é um sistema de arquivos NTFS.</span><span class="sxs-lookup"><span data-stu-id="17d94-154">The file system is not an NTFS file system.</span></span>

</dd> <dt>

<span data-ttu-id="17d94-155">**Plataforma não NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="17d94-155">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="17d94-156">12</span><span class="sxs-lookup"><span data-stu-id="17d94-156">12</span></span>

<span data-ttu-id="17d94-157">A plataforma não é Windows NT ou Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="17d94-157">The platform is not Windows NT or Windows 2000.</span></span>

</dd> <dt>

<span data-ttu-id="17d94-158">**A unidade não é a mesma**</span><span class="sxs-lookup"><span data-stu-id="17d94-158">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="17d94-159">13</span><span class="sxs-lookup"><span data-stu-id="17d94-159">13</span></span>

<span data-ttu-id="17d94-160">A unidade não é a mesma.</span><span class="sxs-lookup"><span data-stu-id="17d94-160">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="17d94-161">**Diretório não vazio**</span><span class="sxs-lookup"><span data-stu-id="17d94-161">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="17d94-162">14</span><span class="sxs-lookup"><span data-stu-id="17d94-162">14</span></span>

<span data-ttu-id="17d94-163">O diretório não está vazio.</span><span class="sxs-lookup"><span data-stu-id="17d94-163">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="17d94-164">**Violação de compartilhamento**</span><span class="sxs-lookup"><span data-stu-id="17d94-164">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="17d94-165">15</span><span class="sxs-lookup"><span data-stu-id="17d94-165">15</span></span>

<span data-ttu-id="17d94-166">Há uma violação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="17d94-166">There is a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="17d94-167">**Arquivo de início inválido**</span><span class="sxs-lookup"><span data-stu-id="17d94-167">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="17d94-168">16</span><span class="sxs-lookup"><span data-stu-id="17d94-168">16</span></span>

<span data-ttu-id="17d94-169">O arquivo de início especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="17d94-169">The specified start file is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="17d94-170">**Privilégio não mantido**</span><span class="sxs-lookup"><span data-stu-id="17d94-170">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="17d94-171">17</span><span class="sxs-lookup"><span data-stu-id="17d94-171">17</span></span>

<span data-ttu-id="17d94-172">Um privilégio necessário para a operação não é mantido.</span><span class="sxs-lookup"><span data-stu-id="17d94-172">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="17d94-173">**Parâmetro inválido**</span><span class="sxs-lookup"><span data-stu-id="17d94-173">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="17d94-174">21</span><span class="sxs-lookup"><span data-stu-id="17d94-174">21</span></span>

<span data-ttu-id="17d94-175">Um parâmetro especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="17d94-175">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="17d94-176">Requisitos</span><span class="sxs-lookup"><span data-stu-id="17d94-176">Requirements</span></span>



| <span data-ttu-id="17d94-177">Requisito</span><span class="sxs-lookup"><span data-stu-id="17d94-177">Requirement</span></span> | <span data-ttu-id="17d94-178">Valor</span><span class="sxs-lookup"><span data-stu-id="17d94-178">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="17d94-179">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="17d94-179">Minimum supported client</span></span><br/> | <span data-ttu-id="17d94-180">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="17d94-180">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="17d94-181">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="17d94-181">Minimum supported server</span></span><br/> | <span data-ttu-id="17d94-182">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="17d94-182">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="17d94-183">Namespace</span><span class="sxs-lookup"><span data-stu-id="17d94-183">Namespace</span></span><br/>                | <span data-ttu-id="17d94-184">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="17d94-184">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="17d94-185">MOF</span><span class="sxs-lookup"><span data-stu-id="17d94-185">MOF</span></span><br/>                      | <dl> <span data-ttu-id="17d94-186"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="17d94-186"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="17d94-187">DLL</span><span class="sxs-lookup"><span data-stu-id="17d94-187">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17d94-188"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17d94-188"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17d94-189">Confira também</span><span class="sxs-lookup"><span data-stu-id="17d94-189">See also</span></span>

<dl> <dt>

<span data-ttu-id="17d94-190">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="17d94-190">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="17d94-191">**Codec do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="17d94-191">**Win32\_CodecFile**</span></span>](win32-codecfile.md)
</dt> </dl>

 

