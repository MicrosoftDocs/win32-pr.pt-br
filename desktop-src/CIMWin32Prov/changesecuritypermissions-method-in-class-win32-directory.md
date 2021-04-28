---
description: Método ChangeSecurityPermissions da classe Win32_Directory – altera as permissões de segurança para o arquivo de entrada de diretório lógico especificado no caminho do objeto.
ms.assetid: de2b3269-61e0-484c-8bea-00578422491f
ms.tgt_platform: multiple
title: Método ChangeSecurityPermissions da classe Win32_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.ChangeSecurityPermissions
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 98c6026497496ab758c71a8a0403557ad2cacc7f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108091054"
---
# <a name="changesecuritypermissions-method-of-the-win32_directory-class"></a><span data-ttu-id="ba0d9-103">Método ChangeSecurityPermissions da classe do \_ diretório Win32</span><span class="sxs-lookup"><span data-stu-id="ba0d9-103">ChangeSecurityPermissions method of the Win32\_Directory class</span></span>

<span data-ttu-id="ba0d9-104">O método de **classe WMI ChangeSecurityPermissions** altera as permissões de segurança para o arquivo de entrada de diretório lógico especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="ba0d9-104">The **ChangeSecurityPermissions WMI class** method changes the security permissions for the logical directory entry file specified in the object path.</span></span> <span data-ttu-id="ba0d9-105">Se o arquivo lógico for um diretório, **ChangeSecurityPermissions** será recursivo e alterará as permissões de segurança de todos os arquivos e subdiretórios que o diretório contém.</span><span class="sxs-lookup"><span data-stu-id="ba0d9-105">If the logical file is a directory, then **ChangeSecurityPermissions** is recursive, and changes the security permissions of all of the files and subdirectories that the directory contains.</span></span> <span data-ttu-id="ba0d9-106">A classe **ChangeSecurityPermissions** retornará um valor inteiro de 0 (zero) se as permissões forem alteradas e um número diferente para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="ba0d9-106">The **ChangeSecurityPermissions** class returns an integer value of 0 (zero) if the permissions are changed, and a different number to indicate an error.</span></span>

<span data-ttu-id="ba0d9-107">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="ba0d9-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="ba0d9-108">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="ba0d9-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="ba0d9-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ba0d9-109">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissions(
  [in] Win32_SecurityDescriptor SecurityDescriptor,
  [in] uint32                   Option
);
```



## <a name="parameters"></a><span data-ttu-id="ba0d9-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ba0d9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba0d9-111">*SecurityDescriptor* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ba0d9-111">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba0d9-112">Expressão que resolve para uma instância do [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span><span class="sxs-lookup"><span data-stu-id="ba0d9-112">Expression that resolves to an instance of [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span> <span data-ttu-id="ba0d9-113">Este descritor contém novas permissões de segurança para a instância do [**\_ arquivo de paginação Win32**](win32-pagefile.md).</span><span class="sxs-lookup"><span data-stu-id="ba0d9-113">This descriptor contains new security permissions for the instance of [**Win32\_PageFile**](win32-pagefile.md).</span></span>

</dd> <dt>

<span data-ttu-id="ba0d9-114">*Opção* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ba0d9-114">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba0d9-115">Privilégio de segurança a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="ba0d9-115">Security privilege to be modified.</span></span> <span data-ttu-id="ba0d9-116">Por exemplo, para alterar a segurança do proprietário e da DACL (lista de controle de acesso discricionário), use:</span><span class="sxs-lookup"><span data-stu-id="ba0d9-116">For example, to change the owner and discretionary access control list (DACL) security, use:</span></span>

`Option = 1 + 4`

<span data-ttu-id="ba0d9-117">-ou-</span><span class="sxs-lookup"><span data-stu-id="ba0d9-117">-or-</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span data-ttu-id="ba0d9-118"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**Alterar \_ \_ \_ Informações de segurança do proprietário** (1)</span><span class="sxs-lookup"><span data-stu-id="ba0d9-118"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE\_OWNER\_SECURITY\_INFORMATION** (1)</span></span>


</dt> <dd>

<span data-ttu-id="ba0d9-119">Altere o proprietário do arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="ba0d9-119">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span data-ttu-id="ba0d9-120"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**Alterar \_ \_ \_ Informações de segurança do grupo** (2)</span><span class="sxs-lookup"><span data-stu-id="ba0d9-120"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE\_GROUP\_SECURITY\_INFORMATION** (2)</span></span>


</dt> <dd>

<span data-ttu-id="ba0d9-121">Altere o grupo do arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="ba0d9-121">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span data-ttu-id="ba0d9-122"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**Alterar \_ \_ \_ Informações de segurança da DACL** (4)</span><span class="sxs-lookup"><span data-stu-id="ba0d9-122"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE\_DACL\_SECURITY\_INFORMATION** (4)</span></span>


</dt> <dd>

<span data-ttu-id="ba0d9-123">Alterar a DACL discricionária do arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="ba0d9-123">Change the discretionary DACL of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span data-ttu-id="ba0d9-124"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Alterar \_ \_ \_ Informações de segurança da SACL** (8)</span><span class="sxs-lookup"><span data-stu-id="ba0d9-124"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE\_SACL\_SECURITY\_INFORMATION** (8)</span></span>


</dt> <dd>

<span data-ttu-id="ba0d9-125">Altere a lista de controle de acesso do sistema (SACL) do arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="ba0d9-125">Change the system access control list (SACL) of the logical file.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba0d9-126">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="ba0d9-126">Return value</span></span>

<span data-ttu-id="ba0d9-127">Retorna um valor de 0 (zero) se as permissões forem alteradas e um número diferente para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="ba0d9-127">Returns a value of 0 (zero) if the permissions are changed, and a different number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="ba0d9-128">**Êxito**</span><span class="sxs-lookup"><span data-stu-id="ba0d9-128">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="ba0d9-129">0</span><span class="sxs-lookup"><span data-stu-id="ba0d9-129">0</span></span>

<span data-ttu-id="ba0d9-130">A solicitação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="ba0d9-130">The request is successful.</span></span>

</dd> <dt>

<span data-ttu-id="ba0d9-131">**Acesso negado**</span><span class="sxs-lookup"><span data-stu-id="ba0d9-131">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="ba0d9-132">2</span><span class="sxs-lookup"><span data-stu-id="ba0d9-132">2</span></span>

<span data-ttu-id="ba0d9-133">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="ba0d9-133">Access is denied.</span></span>

</dd> <dt>

<span data-ttu-id="ba0d9-134">**Falha não especificada**</span><span class="sxs-lookup"><span data-stu-id="ba0d9-134">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="ba0d9-135">8</span><span class="sxs-lookup"><span data-stu-id="ba0d9-135">8</span></span>

<span data-ttu-id="ba0d9-136">Ocorreu uma falha não especificada.</span><span class="sxs-lookup"><span data-stu-id="ba0d9-136">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="ba0d9-137">**Objeto inválido**</span><span class="sxs-lookup"><span data-stu-id="ba0d9-137">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="ba0d9-138">9</span><span class="sxs-lookup"><span data-stu-id="ba0d9-138">9</span></span>

<span data-ttu-id="ba0d9-139">O nome especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="ba0d9-139">The specified name is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="ba0d9-140">**O objeto já existe**</span><span class="sxs-lookup"><span data-stu-id="ba0d9-140">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="ba0d9-141">10</span><span class="sxs-lookup"><span data-stu-id="ba0d9-141">10</span></span>

<span data-ttu-id="ba0d9-142">O objeto especificado já existe.</span><span class="sxs-lookup"><span data-stu-id="ba0d9-142">The specified object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="ba0d9-143">**Sistema de arquivos não NTFS**</span><span class="sxs-lookup"><span data-stu-id="ba0d9-143">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="ba0d9-144">11</span><span class="sxs-lookup"><span data-stu-id="ba0d9-144">11</span></span>

<span data-ttu-id="ba0d9-145">O sistema de arquivos não é um sistema de arquivos NTFS.</span><span class="sxs-lookup"><span data-stu-id="ba0d9-145">The file system is not an NTFS file system.</span></span>

</dd> <dt>

<span data-ttu-id="ba0d9-146">**Plataforma não NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="ba0d9-146">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="ba0d9-147">12</span><span class="sxs-lookup"><span data-stu-id="ba0d9-147">12</span></span>

<span data-ttu-id="ba0d9-148">A plataforma não é o Windows.</span><span class="sxs-lookup"><span data-stu-id="ba0d9-148">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="ba0d9-149">**A unidade não é a mesma**</span><span class="sxs-lookup"><span data-stu-id="ba0d9-149">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="ba0d9-150">13</span><span class="sxs-lookup"><span data-stu-id="ba0d9-150">13</span></span>

<span data-ttu-id="ba0d9-151">A unidade não é a mesma.</span><span class="sxs-lookup"><span data-stu-id="ba0d9-151">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="ba0d9-152">**Diretório não vazio**</span><span class="sxs-lookup"><span data-stu-id="ba0d9-152">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="ba0d9-153">14</span><span class="sxs-lookup"><span data-stu-id="ba0d9-153">14</span></span>

<span data-ttu-id="ba0d9-154">O diretório não está vazio.</span><span class="sxs-lookup"><span data-stu-id="ba0d9-154">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="ba0d9-155">**Violação de compartilhamento**</span><span class="sxs-lookup"><span data-stu-id="ba0d9-155">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="ba0d9-156">15</span><span class="sxs-lookup"><span data-stu-id="ba0d9-156">15</span></span>

<span data-ttu-id="ba0d9-157">Há uma violação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="ba0d9-157">There is a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="ba0d9-158">**Arquivo de início inválido**</span><span class="sxs-lookup"><span data-stu-id="ba0d9-158">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="ba0d9-159">16</span><span class="sxs-lookup"><span data-stu-id="ba0d9-159">16</span></span>

<span data-ttu-id="ba0d9-160">O arquivo de início especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="ba0d9-160">The specified start file is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="ba0d9-161">**Privilégio não mantido**</span><span class="sxs-lookup"><span data-stu-id="ba0d9-161">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="ba0d9-162">17</span><span class="sxs-lookup"><span data-stu-id="ba0d9-162">17</span></span>

<span data-ttu-id="ba0d9-163">Um privilégio necessário para a operação não é mantido.</span><span class="sxs-lookup"><span data-stu-id="ba0d9-163">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="ba0d9-164">**Parâmetro inválido**</span><span class="sxs-lookup"><span data-stu-id="ba0d9-164">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="ba0d9-165">21</span><span class="sxs-lookup"><span data-stu-id="ba0d9-165">21</span></span>

<span data-ttu-id="ba0d9-166">Um parâmetro especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="ba0d9-166">A specified parameter is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ba0d9-167">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ba0d9-167">Requirements</span></span>



| <span data-ttu-id="ba0d9-168">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba0d9-168">Requirement</span></span> | <span data-ttu-id="ba0d9-169">Valor</span><span class="sxs-lookup"><span data-stu-id="ba0d9-169">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ba0d9-170">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ba0d9-170">Minimum supported client</span></span><br/> | <span data-ttu-id="ba0d9-171">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ba0d9-171">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ba0d9-172">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ba0d9-172">Minimum supported server</span></span><br/> | <span data-ttu-id="ba0d9-173">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ba0d9-173">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ba0d9-174">Namespace</span><span class="sxs-lookup"><span data-stu-id="ba0d9-174">Namespace</span></span><br/>                | <span data-ttu-id="ba0d9-175">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="ba0d9-175">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ba0d9-176">MOF</span><span class="sxs-lookup"><span data-stu-id="ba0d9-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ba0d9-177"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ba0d9-177"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ba0d9-178">DLL</span><span class="sxs-lookup"><span data-stu-id="ba0d9-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ba0d9-179"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ba0d9-179"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba0d9-180">Consulte também</span><span class="sxs-lookup"><span data-stu-id="ba0d9-180">See also</span></span>

<dl> <dt>

<span data-ttu-id="ba0d9-181">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ba0d9-181">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="ba0d9-182">**\_Diretório Win32**</span><span class="sxs-lookup"><span data-stu-id="ba0d9-182">**Win32\_Directory**</span></span>](win32-directory.md)
</dt> </dl>

 

