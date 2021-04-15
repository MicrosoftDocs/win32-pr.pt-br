---
description: Altera as permissões de segurança para o arquivo de atalho lógico especificado no caminho do objeto.
ms.assetid: abd5aec8-4684-4b8d-8fdf-d3a7a5eec103
ms.tgt_platform: multiple
title: Método ChangeSecurityPermissions da classe Win32_ShortcutFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ShortcutFile.ChangeSecurityPermissions
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: ad2d482e0be93a1abec80fc710a1a43d7873dd99
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457070"
---
# <a name="changesecuritypermissions-method-of-the-win32_shortcutfile-class"></a><span data-ttu-id="d42a1-103">Método ChangeSecurityPermissions da \_ classe shortcutfile do Win32</span><span class="sxs-lookup"><span data-stu-id="d42a1-103">ChangeSecurityPermissions method of the Win32\_ShortcutFile class</span></span>

<span data-ttu-id="d42a1-104">O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **ChangeSecurityPermissions** altera as permissões de segurança para o arquivo de atalho lógico especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="d42a1-104">The **ChangeSecurityPermissions** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method changes the security permissions for the logical shortcut file specified in the object path.</span></span> <span data-ttu-id="d42a1-105">Se o arquivo lógico for um diretório, **ChangeSecurityPermissions** será recursivo e alterará as permissões de segurança de todos os arquivos e subdiretórios que o diretório contém.</span><span class="sxs-lookup"><span data-stu-id="d42a1-105">If the logical file is a directory, then **ChangeSecurityPermissions** is recursive, and changes the security permissions of all of the files and subdirectories that the directory contains.</span></span> <span data-ttu-id="d42a1-106">**ChangeSecurityPermissions** retornará um valor inteiro de 0 (zero) se as permissões forem alteradas e um número diferente para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="d42a1-106">**ChangeSecurityPermissions** returns an integer value of 0 (zero) if the permissions are changed, and a different number to indicate an error.</span></span>

<span data-ttu-id="d42a1-107">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="d42a1-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="d42a1-108">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="d42a1-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="d42a1-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d42a1-109">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissions(
  [in] Win32_SecurityDescriptor SecurityDescriptor,
  [in] uint32                   Option
);
```



## <a name="parameters"></a><span data-ttu-id="d42a1-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d42a1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d42a1-111">*SecurityDescriptor* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d42a1-111">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d42a1-112">Expressão que resolve para uma instância do [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span><span class="sxs-lookup"><span data-stu-id="d42a1-112">Expression that resolves to an instance of [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span> <span data-ttu-id="d42a1-113">Este descritor contém novas permissões de segurança para a instância do [**\_ arquivo de paginação Win32**](win32-pagefile.md).</span><span class="sxs-lookup"><span data-stu-id="d42a1-113">This descriptor contains new security permissions for the instance of [**Win32\_PageFile**](win32-pagefile.md).</span></span>

</dd> <dt>

<span data-ttu-id="d42a1-114">*Opção* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d42a1-114">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d42a1-115">Privilégio de segurança real a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="d42a1-115">Actual security privilege to be modified.</span></span> <span data-ttu-id="d42a1-116">Por exemplo, para alterar a segurança do proprietário e da DACL, use:</span><span class="sxs-lookup"><span data-stu-id="d42a1-116">For example, to change the owner and DACL security, use:</span></span>

`Option = 1 + 4`

<span data-ttu-id="d42a1-117">ou</span><span class="sxs-lookup"><span data-stu-id="d42a1-117">or</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span data-ttu-id="d42a1-118"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**Alterar \_ \_ \_ Informações de segurança do proprietário** (1)</span><span class="sxs-lookup"><span data-stu-id="d42a1-118"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE\_OWNER\_SECURITY\_INFORMATION** (1)</span></span>


</dt> <dd>

<span data-ttu-id="d42a1-119">Altere o proprietário do arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="d42a1-119">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span data-ttu-id="d42a1-120"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**Alterar \_ \_ \_ Informações de segurança do grupo** (2)</span><span class="sxs-lookup"><span data-stu-id="d42a1-120"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE\_GROUP\_SECURITY\_INFORMATION** (2)</span></span>


</dt> <dd>

<span data-ttu-id="d42a1-121">Altere o grupo do arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="d42a1-121">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span data-ttu-id="d42a1-122"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**Alterar \_ \_ \_ Informações de segurança da DACL** (4)</span><span class="sxs-lookup"><span data-stu-id="d42a1-122"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE\_DACL\_SECURITY\_INFORMATION** (4)</span></span>


</dt> <dd>

<span data-ttu-id="d42a1-123">Altere a DACL (lista de controle de acesso discricionário) do arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="d42a1-123">Change the discretionary access control list (DACL) of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span data-ttu-id="d42a1-124"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Alterar \_ \_ \_ Informações de segurança da SACL** (8)</span><span class="sxs-lookup"><span data-stu-id="d42a1-124"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE\_SACL\_SECURITY\_INFORMATION** (8)</span></span>


</dt> <dd>

<span data-ttu-id="d42a1-125">Altere a lista de controle de acesso do sistema (SACL) do arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="d42a1-125">Change the system access control list (SACL) of the logical file.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d42a1-126">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d42a1-126">Return value</span></span>

<span data-ttu-id="d42a1-127">Retorna um valor de 0 (zero) se as permissões forem alteradas e um número diferente para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="d42a1-127">Returns a value of 0 (zero) if the permissions are changed, and a different number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="d42a1-128">**Êxito**</span><span class="sxs-lookup"><span data-stu-id="d42a1-128">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="d42a1-129">0</span><span class="sxs-lookup"><span data-stu-id="d42a1-129">0</span></span>

<span data-ttu-id="d42a1-130">A solicitação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="d42a1-130">The request is successful.</span></span>

</dd> <dt>

<span data-ttu-id="d42a1-131">**Acesso negado**</span><span class="sxs-lookup"><span data-stu-id="d42a1-131">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="d42a1-132">2</span><span class="sxs-lookup"><span data-stu-id="d42a1-132">2</span></span>

<span data-ttu-id="d42a1-133">O acesso foi negado.</span><span class="sxs-lookup"><span data-stu-id="d42a1-133">Access is denied.</span></span>

</dd> <dt>

<span data-ttu-id="d42a1-134">**Falha não especificada**</span><span class="sxs-lookup"><span data-stu-id="d42a1-134">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="d42a1-135">8</span><span class="sxs-lookup"><span data-stu-id="d42a1-135">8</span></span>

<span data-ttu-id="d42a1-136">Ocorreu uma falha não especificada.</span><span class="sxs-lookup"><span data-stu-id="d42a1-136">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="d42a1-137">**Objeto inválido**</span><span class="sxs-lookup"><span data-stu-id="d42a1-137">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="d42a1-138">9</span><span class="sxs-lookup"><span data-stu-id="d42a1-138">9</span></span>

<span data-ttu-id="d42a1-139">O nome especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="d42a1-139">The specified name is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="d42a1-140">**O objeto já existe**</span><span class="sxs-lookup"><span data-stu-id="d42a1-140">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="d42a1-141">10</span><span class="sxs-lookup"><span data-stu-id="d42a1-141">10</span></span>

<span data-ttu-id="d42a1-142">O objeto especificado já existe.</span><span class="sxs-lookup"><span data-stu-id="d42a1-142">The specified object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="d42a1-143">**Sistema de arquivos não NTFS**</span><span class="sxs-lookup"><span data-stu-id="d42a1-143">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="d42a1-144">11</span><span class="sxs-lookup"><span data-stu-id="d42a1-144">11</span></span>

<span data-ttu-id="d42a1-145">O sistema de arquivos não é um sistema de arquivos NTFS.</span><span class="sxs-lookup"><span data-stu-id="d42a1-145">The file system is not an NTFS file system.</span></span>

</dd> <dt>

<span data-ttu-id="d42a1-146">**Plataforma não NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="d42a1-146">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="d42a1-147">12</span><span class="sxs-lookup"><span data-stu-id="d42a1-147">12</span></span>

<span data-ttu-id="d42a1-148">A plataforma não é o Windows.</span><span class="sxs-lookup"><span data-stu-id="d42a1-148">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="d42a1-149">**A unidade não é a mesma**</span><span class="sxs-lookup"><span data-stu-id="d42a1-149">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="d42a1-150">13</span><span class="sxs-lookup"><span data-stu-id="d42a1-150">13</span></span>

<span data-ttu-id="d42a1-151">A unidade não é a mesma.</span><span class="sxs-lookup"><span data-stu-id="d42a1-151">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="d42a1-152">**Diretório não vazio**</span><span class="sxs-lookup"><span data-stu-id="d42a1-152">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="d42a1-153">14</span><span class="sxs-lookup"><span data-stu-id="d42a1-153">14</span></span>

<span data-ttu-id="d42a1-154">O diretório não está vazio.</span><span class="sxs-lookup"><span data-stu-id="d42a1-154">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="d42a1-155">**Violação de compartilhamento**</span><span class="sxs-lookup"><span data-stu-id="d42a1-155">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="d42a1-156">15</span><span class="sxs-lookup"><span data-stu-id="d42a1-156">15</span></span>

<span data-ttu-id="d42a1-157">Há uma violação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="d42a1-157">There is a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="d42a1-158">**Arquivo de início inválido**</span><span class="sxs-lookup"><span data-stu-id="d42a1-158">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="d42a1-159">16</span><span class="sxs-lookup"><span data-stu-id="d42a1-159">16</span></span>

<span data-ttu-id="d42a1-160">O arquivo de início especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="d42a1-160">The specified start file is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="d42a1-161">**Privilégio não mantido**</span><span class="sxs-lookup"><span data-stu-id="d42a1-161">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="d42a1-162">17</span><span class="sxs-lookup"><span data-stu-id="d42a1-162">17</span></span>

<span data-ttu-id="d42a1-163">Um privilégio necessário para a operação não é mantido.</span><span class="sxs-lookup"><span data-stu-id="d42a1-163">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="d42a1-164">**Parâmetro inválido**</span><span class="sxs-lookup"><span data-stu-id="d42a1-164">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="d42a1-165">21</span><span class="sxs-lookup"><span data-stu-id="d42a1-165">21</span></span>

<span data-ttu-id="d42a1-166">Um parâmetro especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="d42a1-166">A specified parameter is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d42a1-167">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d42a1-167">Requirements</span></span>



| <span data-ttu-id="d42a1-168">Requisito</span><span class="sxs-lookup"><span data-stu-id="d42a1-168">Requirement</span></span> | <span data-ttu-id="d42a1-169">Valor</span><span class="sxs-lookup"><span data-stu-id="d42a1-169">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d42a1-170">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d42a1-170">Minimum supported client</span></span><br/> | <span data-ttu-id="d42a1-171">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d42a1-171">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d42a1-172">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d42a1-172">Minimum supported server</span></span><br/> | <span data-ttu-id="d42a1-173">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d42a1-173">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d42a1-174">Namespace</span><span class="sxs-lookup"><span data-stu-id="d42a1-174">Namespace</span></span><br/>                | <span data-ttu-id="d42a1-175">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="d42a1-175">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d42a1-176">MOF</span><span class="sxs-lookup"><span data-stu-id="d42a1-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d42a1-177"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d42a1-177"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d42a1-178">DLL</span><span class="sxs-lookup"><span data-stu-id="d42a1-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d42a1-179"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d42a1-179"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d42a1-180">Confira também</span><span class="sxs-lookup"><span data-stu-id="d42a1-180">See also</span></span>

<dl> <dt>

<span data-ttu-id="d42a1-181">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d42a1-181">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="d42a1-182">**Atalho do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="d42a1-182">**Win32\_ShortcutFile**</span></span>](win32-shortcutfile.md)
</dt> </dl>

 

