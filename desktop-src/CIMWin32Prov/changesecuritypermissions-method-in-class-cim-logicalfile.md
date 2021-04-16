---
description: Altera as permissões de segurança para o arquivo lógico especificado no caminho do objeto.
ms.assetid: a3caa717-ad37-4e4f-9f4e-f37aed382fa4
ms.tgt_platform: multiple
title: Método ChangeSecurityPermissions da classe CIM_LogicalFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.ChangeSecurityPermissions
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 929e05047af203d8e2344afa8175228e3bd969fd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105750352"
---
# <a name="changesecuritypermissions-method-of-the-cim_logicalfile-class"></a><span data-ttu-id="50fca-103">Método ChangeSecurityPermissions da classe de \_ LogicalFile CIM</span><span class="sxs-lookup"><span data-stu-id="50fca-103">ChangeSecurityPermissions method of the CIM\_LogicalFile class</span></span>

<span data-ttu-id="50fca-104">O método **ChangeSecurityPermissions** altera as permissões de segurança para o arquivo lógico especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="50fca-104">The **ChangeSecurityPermissions** method changes the security permissions for the logical file specified in the object path.</span></span> <span data-ttu-id="50fca-105">Se o arquivo lógico for um diretório, o **ChangeSecurityPermissions** agirá recursivamente, alterando as permissões de segurança para todos os arquivos e subdiretórios que o diretório contém.</span><span class="sxs-lookup"><span data-stu-id="50fca-105">If the logical file is a directory, then **ChangeSecurityPermissions** will act recursively, changing the security permissions for all of the files and sub-directories that the directory contains.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="50fca-106">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="50fca-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="50fca-107">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="50fca-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="50fca-108">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="50fca-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="50fca-109">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="50fca-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="50fca-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="50fca-110">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissions(
  [in] Win32_SecurityDescriptor SecurityDescriptor,
  [in] uint32                   Option
);
```



## <a name="parameters"></a><span data-ttu-id="50fca-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="50fca-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50fca-112">*SecurityDescriptor* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="50fca-112">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50fca-113">Especifica informações de segurança.</span><span class="sxs-lookup"><span data-stu-id="50fca-113">Specifies security information.</span></span>

> [!Note]  
> <span data-ttu-id="50fca-114">Uma  ACL (lista de controle de acesso) nula [**no \_ descritor de segurança**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) concede acesso ilimitado.</span><span class="sxs-lookup"><span data-stu-id="50fca-114">A **NULL** access control list (ACL) in the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) grants unlimited access.</span></span>

 

</dd> <dt>

<span data-ttu-id="50fca-115">*Opção* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="50fca-115">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50fca-116">Privilégio de segurança a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="50fca-116">Security privilege to modify.</span></span> <span data-ttu-id="50fca-117">Por exemplo, para alterar a segurança do proprietário e da DACL, use:</span><span class="sxs-lookup"><span data-stu-id="50fca-117">For example, to change the owner and DACL security, use:</span></span>

`Option = 1 + 4`

<span data-ttu-id="50fca-118">ou</span><span class="sxs-lookup"><span data-stu-id="50fca-118">or</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="Change_Owner_Security_Information"></span><span id="change_owner_security_information"></span><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span>

<span data-ttu-id="50fca-119"><span id="Change_Owner_Security_Information"></span><span id="change_owner_security_information"></span><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span>**Alterar \_ \_ \_ Informações de segurança do proprietário** (1)</span><span class="sxs-lookup"><span data-stu-id="50fca-119"><span id="Change_Owner_Security_Information"></span><span id="change_owner_security_information"></span><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span>**Change\_Owner\_Security\_Information** (1)</span></span>


</dt> <dd>

<span data-ttu-id="50fca-120">Altere o proprietário do arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="50fca-120">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="Change_Group_Security_Information"></span><span id="change_group_security_information"></span><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span>

<span data-ttu-id="50fca-121"><span id="Change_Group_Security_Information"></span><span id="change_group_security_information"></span><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span>**Alterar \_ \_ \_ Informações de segurança do grupo** (2)</span><span class="sxs-lookup"><span data-stu-id="50fca-121"><span id="Change_Group_Security_Information"></span><span id="change_group_security_information"></span><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span>**Change\_Group\_Security\_Information** (2)</span></span>


</dt> <dd>

<span data-ttu-id="50fca-122">Altere o grupo do arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="50fca-122">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="Change_Dacl_Security_Information"></span><span id="change_dacl_security_information"></span><span id="CHANGE_DACL_SECURITY_INFORMATION"></span>

<span data-ttu-id="50fca-123"><span id="Change_Dacl_Security_Information"></span><span id="change_dacl_security_information"></span><span id="CHANGE_DACL_SECURITY_INFORMATION"></span>**Alterar \_ \_ \_ Informações de segurança da DACL** (4)</span><span class="sxs-lookup"><span data-stu-id="50fca-123"><span id="Change_Dacl_Security_Information"></span><span id="change_dacl_security_information"></span><span id="CHANGE_DACL_SECURITY_INFORMATION"></span>**Change\_Dacl\_Security\_Information** (4)</span></span>


</dt> <dd>

<span data-ttu-id="50fca-124">Altere a ACL do arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="50fca-124">Change the ACL of the logical file.</span></span>

</dd> <dt>

<span id="Change_Sacl_Security_Information"></span><span id="change_sacl_security_information"></span><span id="CHANGE_SACL_SECURITY_INFORMATION"></span>

<span data-ttu-id="50fca-125"><span id="Change_Sacl_Security_Information"></span><span id="change_sacl_security_information"></span><span id="CHANGE_SACL_SECURITY_INFORMATION"></span>**Alterar \_ \_ \_ Informações de segurança da SACL** (8)</span><span class="sxs-lookup"><span data-stu-id="50fca-125"><span id="Change_Sacl_Security_Information"></span><span id="change_sacl_security_information"></span><span id="CHANGE_SACL_SECURITY_INFORMATION"></span>**Change\_Sacl\_Security\_Information** (8)</span></span>


</dt> <dd>

<span data-ttu-id="50fca-126">Altere a ACL do sistema do arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="50fca-126">Change the system ACL of the logical file.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50fca-127">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="50fca-127">Return value</span></span>

<span data-ttu-id="50fca-128">Retorna um valor 0 em caso de êxito e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="50fca-128">Returns a value of 0 on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="50fca-129">**Êxito**</span><span class="sxs-lookup"><span data-stu-id="50fca-129">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="50fca-130">0</span><span class="sxs-lookup"><span data-stu-id="50fca-130">0</span></span>

<span data-ttu-id="50fca-131">Sucesso.</span><span class="sxs-lookup"><span data-stu-id="50fca-131">Success.</span></span>

</dd> <dt>

<span data-ttu-id="50fca-132">**Acesso negado**</span><span class="sxs-lookup"><span data-stu-id="50fca-132">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="50fca-133">2</span><span class="sxs-lookup"><span data-stu-id="50fca-133">2</span></span>

<span data-ttu-id="50fca-134">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="50fca-134">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="50fca-135">**Falha não especificada**</span><span class="sxs-lookup"><span data-stu-id="50fca-135">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="50fca-136">8</span><span class="sxs-lookup"><span data-stu-id="50fca-136">8</span></span>

<span data-ttu-id="50fca-137">Falha não especificada.</span><span class="sxs-lookup"><span data-stu-id="50fca-137">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="50fca-138">**Objeto inválido**</span><span class="sxs-lookup"><span data-stu-id="50fca-138">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="50fca-139">9</span><span class="sxs-lookup"><span data-stu-id="50fca-139">9</span></span>

<span data-ttu-id="50fca-140">Objeto inválido.</span><span class="sxs-lookup"><span data-stu-id="50fca-140">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="50fca-141">**O objeto já existe**</span><span class="sxs-lookup"><span data-stu-id="50fca-141">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="50fca-142">10</span><span class="sxs-lookup"><span data-stu-id="50fca-142">10</span></span>

<span data-ttu-id="50fca-143">O objeto já existe.</span><span class="sxs-lookup"><span data-stu-id="50fca-143">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="50fca-144">**Sistema de arquivos não NTFS**</span><span class="sxs-lookup"><span data-stu-id="50fca-144">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="50fca-145">11</span><span class="sxs-lookup"><span data-stu-id="50fca-145">11</span></span>

<span data-ttu-id="50fca-146">Sistema de arquivos não NTFS.</span><span class="sxs-lookup"><span data-stu-id="50fca-146">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="50fca-147">**Plataforma não NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="50fca-147">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="50fca-148">12</span><span class="sxs-lookup"><span data-stu-id="50fca-148">12</span></span>

<span data-ttu-id="50fca-149">Plataforma não Windows.</span><span class="sxs-lookup"><span data-stu-id="50fca-149">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="50fca-150">**A unidade não é a mesma**</span><span class="sxs-lookup"><span data-stu-id="50fca-150">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="50fca-151">13</span><span class="sxs-lookup"><span data-stu-id="50fca-151">13</span></span>

<span data-ttu-id="50fca-152">A unidade não é a mesma.</span><span class="sxs-lookup"><span data-stu-id="50fca-152">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="50fca-153">**Diretório não vazio**</span><span class="sxs-lookup"><span data-stu-id="50fca-153">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="50fca-154">14</span><span class="sxs-lookup"><span data-stu-id="50fca-154">14</span></span>

<span data-ttu-id="50fca-155">O diretório não está vazio.</span><span class="sxs-lookup"><span data-stu-id="50fca-155">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="50fca-156">**Violação de compartilhamento**</span><span class="sxs-lookup"><span data-stu-id="50fca-156">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="50fca-157">15</span><span class="sxs-lookup"><span data-stu-id="50fca-157">15</span></span>

<span data-ttu-id="50fca-158">Violação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="50fca-158">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="50fca-159">**Arquivo de início inválido**</span><span class="sxs-lookup"><span data-stu-id="50fca-159">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="50fca-160">16</span><span class="sxs-lookup"><span data-stu-id="50fca-160">16</span></span>

<span data-ttu-id="50fca-161">Arquivo inicial inválido.</span><span class="sxs-lookup"><span data-stu-id="50fca-161">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="50fca-162">**Privilégio não mantido**</span><span class="sxs-lookup"><span data-stu-id="50fca-162">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="50fca-163">17</span><span class="sxs-lookup"><span data-stu-id="50fca-163">17</span></span>

<span data-ttu-id="50fca-164">Privilégio não mantido.</span><span class="sxs-lookup"><span data-stu-id="50fca-164">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="50fca-165">**Parâmetro inválido**</span><span class="sxs-lookup"><span data-stu-id="50fca-165">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="50fca-166">21</span><span class="sxs-lookup"><span data-stu-id="50fca-166">21</span></span>

<span data-ttu-id="50fca-167">Parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="50fca-167">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="50fca-168">Comentários</span><span class="sxs-lookup"><span data-stu-id="50fca-168">Remarks</span></span>

<span data-ttu-id="50fca-169">Este método não está implementado no momento pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="50fca-169">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="50fca-170">Para usar esse método, você deve implementá-lo em seu próprio provedor.</span><span class="sxs-lookup"><span data-stu-id="50fca-170">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="50fca-171">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="50fca-171">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="50fca-172">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="50fca-172">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="50fca-173">Requisitos</span><span class="sxs-lookup"><span data-stu-id="50fca-173">Requirements</span></span>



| <span data-ttu-id="50fca-174">Requisito</span><span class="sxs-lookup"><span data-stu-id="50fca-174">Requirement</span></span> | <span data-ttu-id="50fca-175">Valor</span><span class="sxs-lookup"><span data-stu-id="50fca-175">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="50fca-176">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="50fca-176">Minimum supported client</span></span><br/> | <span data-ttu-id="50fca-177">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="50fca-177">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="50fca-178">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="50fca-178">Minimum supported server</span></span><br/> | <span data-ttu-id="50fca-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="50fca-179">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="50fca-180">Namespace</span><span class="sxs-lookup"><span data-stu-id="50fca-180">Namespace</span></span><br/>                | <span data-ttu-id="50fca-181">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="50fca-181">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="50fca-182">MOF</span><span class="sxs-lookup"><span data-stu-id="50fca-182">MOF</span></span><br/>                      | <dl> <span data-ttu-id="50fca-183"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="50fca-183"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="50fca-184">DLL</span><span class="sxs-lookup"><span data-stu-id="50fca-184">DLL</span></span><br/>                      | <dl> <span data-ttu-id="50fca-185"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="50fca-185"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50fca-186">Confira também</span><span class="sxs-lookup"><span data-stu-id="50fca-186">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50fca-187">**CIM \_ LogicalFile**</span><span class="sxs-lookup"><span data-stu-id="50fca-187">**CIM\_LogicalFile**</span></span>](changesecuritypermissions-method-in-class-cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="50fca-188">**CIM \_ LogicalFile**</span><span class="sxs-lookup"><span data-stu-id="50fca-188">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

