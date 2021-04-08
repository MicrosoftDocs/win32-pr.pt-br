---
description: Altera as permissões de segurança para o arquivo de paginação lógica especificado no caminho do objeto.
ms.assetid: 3abdfa1d-49d8-4676-b7a5-3be528938ec4
ms.tgt_platform: multiple
title: Método ChangeSecurityPermissions da classe Win32_PageFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFile.ChangeSecurityPermissions
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: cc30d8780f7c0573b9a63ff83f16ad46b9d2a70f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920421"
---
# <a name="changesecuritypermissions-method-of-the-win32_pagefile-class"></a><span data-ttu-id="93e8b-103">Método ChangeSecurityPermissions da classe de \_ arquivo de paginação Win32</span><span class="sxs-lookup"><span data-stu-id="93e8b-103">ChangeSecurityPermissions method of the Win32\_PageFile class</span></span>

<span data-ttu-id="93e8b-104">O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **ChangeSecurityPermissions** altera as permissões de segurança para o arquivo de paginação lógica especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="93e8b-104">The **ChangeSecurityPermissions** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method changes the security permissions for the logical paging file specified in the object path.</span></span> <span data-ttu-id="93e8b-105">Se o arquivo lógico for um diretório, **ChangeSecurityPermissions** será recursivo e alterará as permissões de segurança de todos os arquivos e subdiretórios que o diretório contém.</span><span class="sxs-lookup"><span data-stu-id="93e8b-105">If the logical file is a directory, then **ChangeSecurityPermissions** is recursive, and changes the security permissions of all of the files and subdirectories that the directory contains.</span></span>

<span data-ttu-id="93e8b-106">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="93e8b-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="93e8b-107">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="93e8b-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="93e8b-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="93e8b-108">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissions(
  [in] Win32_SecurityDescriptor SecurityDescriptor,
  [in] uint32                   Option
);
```



## <a name="parameters"></a><span data-ttu-id="93e8b-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="93e8b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93e8b-110">*SecurityDescriptor* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="93e8b-110">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93e8b-111">Expressão que resolve para uma instância do [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span><span class="sxs-lookup"><span data-stu-id="93e8b-111">Expression that resolves to an instance of [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span> <span data-ttu-id="93e8b-112">Este descritor contém novas permissões de segurança para a instância do [**\_ arquivo de paginação Win32**](win32-pagefile.md).</span><span class="sxs-lookup"><span data-stu-id="93e8b-112">This descriptor contains new security permissions for the instance of [**Win32\_PageFile**](win32-pagefile.md).</span></span>

</dd> <dt>

<span data-ttu-id="93e8b-113">*Opção* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="93e8b-113">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93e8b-114">Privilégio de segurança a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="93e8b-114">Security privilege to be modified.</span></span> <span data-ttu-id="93e8b-115">Por exemplo, para alterar a segurança do proprietário e da DACL (lista de controle de acesso discricionário), use:</span><span class="sxs-lookup"><span data-stu-id="93e8b-115">For example, to change the owner and discretionary access control list (DACL) security, use:</span></span>

`Option = 1 + 4`

<span data-ttu-id="93e8b-116">– ou –</span><span class="sxs-lookup"><span data-stu-id="93e8b-116">-or-</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span data-ttu-id="93e8b-117"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**Alterar \_ \_ \_ Informações de segurança do proprietário** (1)</span><span class="sxs-lookup"><span data-stu-id="93e8b-117"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE\_OWNER\_SECURITY\_INFORMATION** (1)</span></span>


</dt> <dd>

<span data-ttu-id="93e8b-118">Altere o proprietário do arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="93e8b-118">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span data-ttu-id="93e8b-119"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**Alterar \_ \_ \_ Informações de segurança do grupo** (2)</span><span class="sxs-lookup"><span data-stu-id="93e8b-119"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE\_GROUP\_SECURITY\_INFORMATION** (2)</span></span>


</dt> <dd>

<span data-ttu-id="93e8b-120">Altere o grupo do arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="93e8b-120">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span data-ttu-id="93e8b-121"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**Alterar \_ \_ \_ Informações de segurança da DACL** (4)</span><span class="sxs-lookup"><span data-stu-id="93e8b-121"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE\_DACL\_SECURITY\_INFORMATION** (4)</span></span>


</dt> <dd>

<span data-ttu-id="93e8b-122">Altere a DACL do arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="93e8b-122">Change the DACL of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span data-ttu-id="93e8b-123"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Alterar \_ \_ \_ Informações de segurança da SACL** (8)</span><span class="sxs-lookup"><span data-stu-id="93e8b-123"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE\_SACL\_SECURITY\_INFORMATION** (8)</span></span>


</dt> <dd>

<span data-ttu-id="93e8b-124">Altere a lista de controle de acesso do sistema (SACL) do arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="93e8b-124">Change the system access control list (SACL) of the logical file.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93e8b-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="93e8b-125">Return value</span></span>

<span data-ttu-id="93e8b-126">Retorna um valor de 0 (zero) se as permissões forem alteradas e um número diferente para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="93e8b-126">Returns a value of 0 (zero) if the permissions are changed, and a different number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="93e8b-127">**Êxito**</span><span class="sxs-lookup"><span data-stu-id="93e8b-127">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="93e8b-128">0</span><span class="sxs-lookup"><span data-stu-id="93e8b-128">0</span></span>

<span data-ttu-id="93e8b-129">A solicitação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="93e8b-129">The request is successful.</span></span>

</dd> <dt>

<span data-ttu-id="93e8b-130">**Acesso negado**</span><span class="sxs-lookup"><span data-stu-id="93e8b-130">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="93e8b-131">2</span><span class="sxs-lookup"><span data-stu-id="93e8b-131">2</span></span>

<span data-ttu-id="93e8b-132">O acesso foi negado.</span><span class="sxs-lookup"><span data-stu-id="93e8b-132">Access is denied.</span></span>

</dd> <dt>

<span data-ttu-id="93e8b-133">**Falha não especificada**</span><span class="sxs-lookup"><span data-stu-id="93e8b-133">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="93e8b-134">8</span><span class="sxs-lookup"><span data-stu-id="93e8b-134">8</span></span>

<span data-ttu-id="93e8b-135">Ocorreu uma falha não especificada.</span><span class="sxs-lookup"><span data-stu-id="93e8b-135">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="93e8b-136">**Objeto inválido**</span><span class="sxs-lookup"><span data-stu-id="93e8b-136">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="93e8b-137">9</span><span class="sxs-lookup"><span data-stu-id="93e8b-137">9</span></span>

<span data-ttu-id="93e8b-138">O nome especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="93e8b-138">The specified name is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="93e8b-139">**O objeto já existe**</span><span class="sxs-lookup"><span data-stu-id="93e8b-139">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="93e8b-140">10</span><span class="sxs-lookup"><span data-stu-id="93e8b-140">10</span></span>

<span data-ttu-id="93e8b-141">O objeto especificado já existe.</span><span class="sxs-lookup"><span data-stu-id="93e8b-141">The specified object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="93e8b-142">**Sistema de arquivos não NTFS**</span><span class="sxs-lookup"><span data-stu-id="93e8b-142">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="93e8b-143">11</span><span class="sxs-lookup"><span data-stu-id="93e8b-143">11</span></span>

<span data-ttu-id="93e8b-144">O sistema de arquivos não é um sistema de arquivos NTFS.</span><span class="sxs-lookup"><span data-stu-id="93e8b-144">The file system is not an NTFS file system.</span></span>

</dd> <dt>

<span data-ttu-id="93e8b-145">**Plataforma não NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="93e8b-145">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="93e8b-146">12</span><span class="sxs-lookup"><span data-stu-id="93e8b-146">12</span></span>

<span data-ttu-id="93e8b-147">A plataforma não é o Windows.</span><span class="sxs-lookup"><span data-stu-id="93e8b-147">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="93e8b-148">**A unidade não é a mesma**</span><span class="sxs-lookup"><span data-stu-id="93e8b-148">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="93e8b-149">13</span><span class="sxs-lookup"><span data-stu-id="93e8b-149">13</span></span>

<span data-ttu-id="93e8b-150">A unidade não é a mesma.</span><span class="sxs-lookup"><span data-stu-id="93e8b-150">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="93e8b-151">**Diretório não vazio**</span><span class="sxs-lookup"><span data-stu-id="93e8b-151">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="93e8b-152">14</span><span class="sxs-lookup"><span data-stu-id="93e8b-152">14</span></span>

<span data-ttu-id="93e8b-153">O diretório não está vazio.</span><span class="sxs-lookup"><span data-stu-id="93e8b-153">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="93e8b-154">**Violação de compartilhamento**</span><span class="sxs-lookup"><span data-stu-id="93e8b-154">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="93e8b-155">15</span><span class="sxs-lookup"><span data-stu-id="93e8b-155">15</span></span>

<span data-ttu-id="93e8b-156">Há uma violação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="93e8b-156">There is a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="93e8b-157">**Arquivo de início inválido**</span><span class="sxs-lookup"><span data-stu-id="93e8b-157">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="93e8b-158">16</span><span class="sxs-lookup"><span data-stu-id="93e8b-158">16</span></span>

<span data-ttu-id="93e8b-159">O arquivo de início especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="93e8b-159">The specified start file is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="93e8b-160">**Privilégio não mantido**</span><span class="sxs-lookup"><span data-stu-id="93e8b-160">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="93e8b-161">17</span><span class="sxs-lookup"><span data-stu-id="93e8b-161">17</span></span>

<span data-ttu-id="93e8b-162">Um privilégio necessário para a operação está ausente.</span><span class="sxs-lookup"><span data-stu-id="93e8b-162">A privilege required for the operation is missing.</span></span>

</dd> <dt>

<span data-ttu-id="93e8b-163">**Parâmetro inválido**</span><span class="sxs-lookup"><span data-stu-id="93e8b-163">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="93e8b-164">21</span><span class="sxs-lookup"><span data-stu-id="93e8b-164">21</span></span>

<span data-ttu-id="93e8b-165">Um parâmetro especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="93e8b-165">A specified parameter is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="93e8b-166">Requisitos</span><span class="sxs-lookup"><span data-stu-id="93e8b-166">Requirements</span></span>



| <span data-ttu-id="93e8b-167">Requisito</span><span class="sxs-lookup"><span data-stu-id="93e8b-167">Requirement</span></span> | <span data-ttu-id="93e8b-168">Valor</span><span class="sxs-lookup"><span data-stu-id="93e8b-168">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="93e8b-169">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="93e8b-169">Minimum supported client</span></span><br/> | <span data-ttu-id="93e8b-170">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="93e8b-170">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="93e8b-171">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="93e8b-171">Minimum supported server</span></span><br/> | <span data-ttu-id="93e8b-172">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="93e8b-172">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="93e8b-173">Namespace</span><span class="sxs-lookup"><span data-stu-id="93e8b-173">Namespace</span></span><br/>                | <span data-ttu-id="93e8b-174">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="93e8b-174">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="93e8b-175">MOF</span><span class="sxs-lookup"><span data-stu-id="93e8b-175">MOF</span></span><br/>                      | <dl> <span data-ttu-id="93e8b-176"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="93e8b-176"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="93e8b-177">DLL</span><span class="sxs-lookup"><span data-stu-id="93e8b-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="93e8b-178"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="93e8b-178"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93e8b-179">Confira também</span><span class="sxs-lookup"><span data-stu-id="93e8b-179">See also</span></span>

<dl> <dt>

<span data-ttu-id="93e8b-180">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="93e8b-180">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="93e8b-181">**\_Arquivo de paginação Win32**</span><span class="sxs-lookup"><span data-stu-id="93e8b-181">**Win32\_PageFile**</span></span>](win32-pagefile.md)
</dt> </dl>

 

