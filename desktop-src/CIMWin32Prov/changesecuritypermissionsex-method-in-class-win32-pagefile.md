---
description: Altera as permissões de segurança para o arquivo de paginação lógica especificado no caminho do objeto (esse método é uma versão estendida do método ChangeSecurityPermissions).
ms.assetid: a852a7e6-f26a-4bd9-bb15-e4cdd577697c
ms.tgt_platform: multiple
title: Método ChangeSecurityPermissionsEx da classe Win32_PageFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFile.ChangeSecurityPermissionsEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a01a214e626f9c64ccf460eb3f8c031d1b45ff85
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826348"
---
# <a name="changesecuritypermissionsex-method-of-the-win32_pagefile-class"></a><span data-ttu-id="6da93-103">Método ChangeSecurityPermissionsEx da classe de \_ arquivo de paginação Win32</span><span class="sxs-lookup"><span data-stu-id="6da93-103">ChangeSecurityPermissionsEx method of the Win32\_PageFile class</span></span>

<span data-ttu-id="6da93-104">O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **ChangeSecurityPermissionsEx** altera as permissões de segurança para o arquivo de paginação lógica especificado no caminho do objeto (esse método é uma versão estendida do método [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-win32-directory.md) ).</span><span class="sxs-lookup"><span data-stu-id="6da93-104">The **ChangeSecurityPermissionsEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method changes the security permissions for the logical paging file that is specified in the object path (this method is an extended version of the [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-win32-directory.md) method).</span></span> <span data-ttu-id="6da93-105">Se o arquivo lógico for um diretório, esse método será recursivo e alterará as permissões de segurança de todos os arquivos e subdiretórios que o diretório contém.</span><span class="sxs-lookup"><span data-stu-id="6da93-105">If the logical file is a directory, then this method is recursive, and changes the security permissions of all of the files and subdirectories that the directory contains.</span></span>

<span data-ttu-id="6da93-106">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="6da93-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="6da93-107">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="6da93-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="6da93-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6da93-108">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissionsEx(
  [in]           Win32_SecurityDescriptor SecurityDescriptor,
  [in]           uint32                   Option,
  [out]          string                   StopFileName,
  [in, optional] string                   StartFileName,
  [in, optional] boolean                  Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="6da93-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6da93-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6da93-110">*SecurityDescriptor* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6da93-110">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6da93-111">Expressão que resolve para uma instância do [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span><span class="sxs-lookup"><span data-stu-id="6da93-111">Expression that resolves to an instance of [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span> <span data-ttu-id="6da93-112">Esse parâmetro contém novas permissões de segurança para a instância [**do \_ arquivo de paginação Win32**](win32-pagefile.md).</span><span class="sxs-lookup"><span data-stu-id="6da93-112">This parameter contains new security permissions for the instance of [**Win32\_PageFile**](win32-pagefile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6da93-113">*Opção* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6da93-113">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6da93-114">Privilégio de segurança a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="6da93-114">Security privilege to be modified.</span></span> <span data-ttu-id="6da93-115">Por exemplo, para alterar a segurança do proprietário e da DACL (lista de controle de acesso discricionário), use o seguinte:</span><span class="sxs-lookup"><span data-stu-id="6da93-115">For example, to change the owner and discretionary access control list (DACL) security, use the following:</span></span>

`Option = 1 + 4`

<span data-ttu-id="6da93-116">– ou –</span><span class="sxs-lookup"><span data-stu-id="6da93-116">-or-</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span data-ttu-id="6da93-117"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**Alterar \_ \_ \_ Informações de segurança do proprietário** (1)</span><span class="sxs-lookup"><span data-stu-id="6da93-117"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE\_OWNER\_SECURITY\_INFORMATION** (1)</span></span>


</dt> <dd>

<span data-ttu-id="6da93-118">Altere o proprietário do arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="6da93-118">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span data-ttu-id="6da93-119"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**Alterar \_ \_ \_ Informações de segurança do grupo** (2)</span><span class="sxs-lookup"><span data-stu-id="6da93-119"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE\_GROUP\_SECURITY\_INFORMATION** (2)</span></span>


</dt> <dd>

<span data-ttu-id="6da93-120">Altere o grupo do arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="6da93-120">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span data-ttu-id="6da93-121"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**Alterar \_ \_ \_ Informações de segurança da DACL** (4)</span><span class="sxs-lookup"><span data-stu-id="6da93-121"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE\_DACL\_SECURITY\_INFORMATION** (4)</span></span>


</dt> <dd>

<span data-ttu-id="6da93-122">Altere a DACL do arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="6da93-122">Change the DACL of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span data-ttu-id="6da93-123"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Alterar \_ \_ \_ Informações de segurança da SACL** (8)</span><span class="sxs-lookup"><span data-stu-id="6da93-123"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE\_SACL\_SECURITY\_INFORMATION** (8)</span></span>


</dt> <dd>

<span data-ttu-id="6da93-124">Altere a lista de controle de acesso do sistema (SACL) do arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="6da93-124">Change the system access control (SACL) list of the logical file.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="6da93-125">*StopFileName* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="6da93-125">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6da93-126">Nome do arquivo ou diretório em que o método **ChangeSecurityPermissionsEx** falhou.</span><span class="sxs-lookup"><span data-stu-id="6da93-126">Name of the file or directory where the **ChangeSecurityPermissionsEx** method failed.</span></span> <span data-ttu-id="6da93-127">Esse parâmetro será **nulo** se o método tiver sucesso.</span><span class="sxs-lookup"><span data-stu-id="6da93-127">This parameter is **NULL** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="6da93-128">*StartFileName* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="6da93-128">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6da93-129">Nomeia o arquivo ou diretório filho a ser usado como ponto de partida para **ChangeSecurityPermissionsEx**.</span><span class="sxs-lookup"><span data-stu-id="6da93-129">Names the child file or directory to use as a starting point for **ChangeSecurityPermissionsEx**.</span></span> <span data-ttu-id="6da93-130">Normalmente, o parâmetro *StartFileName* é o parâmetro *StartFileName* que especifica o arquivo ou diretório em que ocorreu um erro da chamada de método anterior.</span><span class="sxs-lookup"><span data-stu-id="6da93-130">Typically, the *StartFileName* parameter is the *StartFileName* parameter that specifies the file or directory where an error occurred from the previous method call.</span></span> <span data-ttu-id="6da93-131">Se esse parâmetro for **nulo**, a operação será executada no arquivo ou diretório especificado na chamada de [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="6da93-131">If this parameter is **null**, the operation is performed on the file or directory specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="6da93-132">*Recursivo* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="6da93-132">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6da93-133">Se for **true**, a alteração de propriedade será aplicada recursivamente aos arquivos e diretórios no diretório especificado pela instância [**de \_ LogicalFile do CIM**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="6da93-133">If **true**, the change of ownership is applied recursively to files and directories in the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span>

> [!Note]  
> <span data-ttu-id="6da93-134">Para instâncias de arquivo, o parâmetro *recursivo* é ignorado.</span><span class="sxs-lookup"><span data-stu-id="6da93-134">For file instances, the *Recursive* parameter is ignored.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6da93-135">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6da93-135">Return value</span></span>

<span data-ttu-id="6da93-136">Retorna um valor de 0 (zero) se as permissões forem alteradas e um número diferente para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="6da93-136">Returns a value of 0 (zero) if the permissions are changed, and a different number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="6da93-137">**Êxito**</span><span class="sxs-lookup"><span data-stu-id="6da93-137">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="6da93-138">0</span><span class="sxs-lookup"><span data-stu-id="6da93-138">0</span></span>

<span data-ttu-id="6da93-139">A solicitação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="6da93-139">The request is successful.</span></span>

</dd> <dt>

<span data-ttu-id="6da93-140">**Acesso negado**</span><span class="sxs-lookup"><span data-stu-id="6da93-140">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="6da93-141">2</span><span class="sxs-lookup"><span data-stu-id="6da93-141">2</span></span>

<span data-ttu-id="6da93-142">O acesso foi negado.</span><span class="sxs-lookup"><span data-stu-id="6da93-142">Access is denied.</span></span>

</dd> <dt>

<span data-ttu-id="6da93-143">**Falha não especificada**</span><span class="sxs-lookup"><span data-stu-id="6da93-143">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="6da93-144">8</span><span class="sxs-lookup"><span data-stu-id="6da93-144">8</span></span>

<span data-ttu-id="6da93-145">Ocorreu uma falha não especificada.</span><span class="sxs-lookup"><span data-stu-id="6da93-145">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="6da93-146">**Objeto inválido**</span><span class="sxs-lookup"><span data-stu-id="6da93-146">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="6da93-147">9</span><span class="sxs-lookup"><span data-stu-id="6da93-147">9</span></span>

<span data-ttu-id="6da93-148">O nome especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="6da93-148">The name specified is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="6da93-149">**O objeto já existe**</span><span class="sxs-lookup"><span data-stu-id="6da93-149">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="6da93-150">10</span><span class="sxs-lookup"><span data-stu-id="6da93-150">10</span></span>

<span data-ttu-id="6da93-151">O objeto especificado já existe.</span><span class="sxs-lookup"><span data-stu-id="6da93-151">The specified object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="6da93-152">**Sistema de arquivos não NTFS**</span><span class="sxs-lookup"><span data-stu-id="6da93-152">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="6da93-153">11</span><span class="sxs-lookup"><span data-stu-id="6da93-153">11</span></span>

<span data-ttu-id="6da93-154">O sistema de arquivos não é um sistema de arquivos NTFS.</span><span class="sxs-lookup"><span data-stu-id="6da93-154">The file system is not an NTFS file system.</span></span>

</dd> <dt>

<span data-ttu-id="6da93-155">**Plataforma não NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="6da93-155">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="6da93-156">12</span><span class="sxs-lookup"><span data-stu-id="6da93-156">12</span></span>

<span data-ttu-id="6da93-157">A plataforma não é o Windows.</span><span class="sxs-lookup"><span data-stu-id="6da93-157">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="6da93-158">**A unidade não é a mesma**</span><span class="sxs-lookup"><span data-stu-id="6da93-158">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="6da93-159">13</span><span class="sxs-lookup"><span data-stu-id="6da93-159">13</span></span>

<span data-ttu-id="6da93-160">A unidade não é a mesma.</span><span class="sxs-lookup"><span data-stu-id="6da93-160">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="6da93-161">**Diretório não vazio**</span><span class="sxs-lookup"><span data-stu-id="6da93-161">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="6da93-162">14</span><span class="sxs-lookup"><span data-stu-id="6da93-162">14</span></span>

<span data-ttu-id="6da93-163">O diretório não está vazio.</span><span class="sxs-lookup"><span data-stu-id="6da93-163">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="6da93-164">**Violação de compartilhamento**</span><span class="sxs-lookup"><span data-stu-id="6da93-164">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="6da93-165">15</span><span class="sxs-lookup"><span data-stu-id="6da93-165">15</span></span>

<span data-ttu-id="6da93-166">Há uma violação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="6da93-166">There is a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="6da93-167">**Arquivo de início inválido**</span><span class="sxs-lookup"><span data-stu-id="6da93-167">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="6da93-168">16</span><span class="sxs-lookup"><span data-stu-id="6da93-168">16</span></span>

<span data-ttu-id="6da93-169">O arquivo de início especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="6da93-169">The specified start file is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="6da93-170">**Privilégio não mantido**</span><span class="sxs-lookup"><span data-stu-id="6da93-170">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="6da93-171">17</span><span class="sxs-lookup"><span data-stu-id="6da93-171">17</span></span>

<span data-ttu-id="6da93-172">Um privilégio necessário para a operação está ausente.</span><span class="sxs-lookup"><span data-stu-id="6da93-172">A privilege required for the operation is missing.</span></span>

</dd> <dt>

<span data-ttu-id="6da93-173">**Parâmetro inválido**</span><span class="sxs-lookup"><span data-stu-id="6da93-173">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="6da93-174">21</span><span class="sxs-lookup"><span data-stu-id="6da93-174">21</span></span>

<span data-ttu-id="6da93-175">Um parâmetro especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="6da93-175">A specified parameter is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6da93-176">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6da93-176">Requirements</span></span>



| <span data-ttu-id="6da93-177">Requisito</span><span class="sxs-lookup"><span data-stu-id="6da93-177">Requirement</span></span> | <span data-ttu-id="6da93-178">Valor</span><span class="sxs-lookup"><span data-stu-id="6da93-178">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6da93-179">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6da93-179">Minimum supported client</span></span><br/> | <span data-ttu-id="6da93-180">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6da93-180">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6da93-181">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6da93-181">Minimum supported server</span></span><br/> | <span data-ttu-id="6da93-182">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6da93-182">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6da93-183">Namespace</span><span class="sxs-lookup"><span data-stu-id="6da93-183">Namespace</span></span><br/>                | <span data-ttu-id="6da93-184">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="6da93-184">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6da93-185">MOF</span><span class="sxs-lookup"><span data-stu-id="6da93-185">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6da93-186"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6da93-186"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6da93-187">DLL</span><span class="sxs-lookup"><span data-stu-id="6da93-187">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6da93-188"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6da93-188"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6da93-189">Confira também</span><span class="sxs-lookup"><span data-stu-id="6da93-189">See also</span></span>

<dl> <dt>

<span data-ttu-id="6da93-190">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6da93-190">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="6da93-191">**\_Arquivo de paginação Win32**</span><span class="sxs-lookup"><span data-stu-id="6da93-191">**Win32\_PageFile**</span></span>](win32-pagefile.md)
</dt> </dl>

 

