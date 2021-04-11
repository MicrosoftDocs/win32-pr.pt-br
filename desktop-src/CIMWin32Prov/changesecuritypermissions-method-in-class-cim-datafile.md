---
description: Altera as permissões de segurança para o arquivo de dados lógicos especificado no caminho do objeto.
ms.assetid: b0a66411-f973-42ce-a3fe-25c31234a964
ms.tgt_platform: multiple
title: Método ChangeSecurityPermissions da classe CIM_DataFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.ChangeSecurityPermissions
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: faa2e3ce2f2454d76ff9e55cc10cf09e9b5f715e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089357"
---
# <a name="changesecuritypermissions-method-of-the-cim_datafile-class"></a><span data-ttu-id="25323-103">Método ChangeSecurityPermissions da classe de \_ datafilefiles CIM</span><span class="sxs-lookup"><span data-stu-id="25323-103">ChangeSecurityPermissions method of the CIM\_DataFile class</span></span>

<span data-ttu-id="25323-104">O método **ChangeSecurityPermissions** altera as permissões de segurança para o arquivo de dados lógicos especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="25323-104">The **ChangeSecurityPermissions** method changes the security permissions for the logical data file specified in the object path.</span></span> <span data-ttu-id="25323-105">Se o arquivo lógico for um diretório, esse método agirá de forma recursiva, alterando as permissões de segurança para todos os arquivos e subdiretórios que o diretório contém.</span><span class="sxs-lookup"><span data-stu-id="25323-105">If the logical file is a directory, then this method will act recursively, changing the security permissions for all of the files and sub-directories that the directory contains.</span></span> <span data-ttu-id="25323-106">Esse método é herdado [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="25323-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="25323-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="25323-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="25323-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="25323-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="25323-109">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="25323-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="25323-110">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="25323-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="25323-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="25323-111">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissions(
  [in] Win32_SecurityDescriptor SecurityDescriptor,
  [in] uint32                   Option
);
```



## <a name="parameters"></a><span data-ttu-id="25323-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="25323-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25323-113">*SecurityDescriptor* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="25323-113">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25323-114">Especifica as informações de segurança.</span><span class="sxs-lookup"><span data-stu-id="25323-114">Specifies the security information.</span></span>

> [!Note]  
> <span data-ttu-id="25323-115">Uma ACL (lista de controle de acesso) **nula** na estrutura do [**\_ descritor de segurança**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) concede acesso ilimitado.</span><span class="sxs-lookup"><span data-stu-id="25323-115">A **NULL** access control list (ACL) in the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure grants unlimited access.</span></span> <span data-ttu-id="25323-116">Para obter informações sobre as implicações de acesso ilimitado, consulte [criando um descritor de segurança para um novo objeto](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span><span class="sxs-lookup"><span data-stu-id="25323-116">For information about the implications of unlimited access, see [Creating a Security Descriptor for a New Object](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span></span>

 

</dd> <dt>

<span data-ttu-id="25323-117">*Opção* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="25323-117">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25323-118">Privilégio de segurança a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="25323-118">Security privilege to modify.</span></span> <span data-ttu-id="25323-119">Por exemplo, para alterar a segurança do proprietário e da DACL, use:</span><span class="sxs-lookup"><span data-stu-id="25323-119">For example, to change the owner and DACL security, use:</span></span>

`Option = 1 + 4`

<span data-ttu-id="25323-120">ou</span><span class="sxs-lookup"><span data-stu-id="25323-120">or</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span data-ttu-id="25323-121"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**Alterar \_ \_ \_ Informações de segurança do proprietário** (1)</span><span class="sxs-lookup"><span data-stu-id="25323-121"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE\_OWNER\_SECURITY\_INFORMATION** (1)</span></span>


</dt> <dd>

<span data-ttu-id="25323-122">Altere o proprietário do arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="25323-122">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span data-ttu-id="25323-123"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**Alterar \_ \_ \_ Informações de segurança do grupo** (2)</span><span class="sxs-lookup"><span data-stu-id="25323-123"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE\_GROUP\_SECURITY\_INFORMATION** (2)</span></span>


</dt> <dd>

<span data-ttu-id="25323-124">Altere o grupo do arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="25323-124">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span data-ttu-id="25323-125"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**Alterar \_ \_ \_ Informações de segurança da DACL** (4)</span><span class="sxs-lookup"><span data-stu-id="25323-125"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE\_DACL\_SECURITY\_INFORMATION** (4)</span></span>


</dt> <dd>

<span data-ttu-id="25323-126">Altere a ACL do arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="25323-126">Change the ACL of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span data-ttu-id="25323-127"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Alterar \_ \_ \_ Informações de segurança da SACL** (8)</span><span class="sxs-lookup"><span data-stu-id="25323-127"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE\_SACL\_SECURITY\_INFORMATION** (8)</span></span>


</dt> <dd>

<span data-ttu-id="25323-128">Altere a ACL do sistema do arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="25323-128">Change the system ACL of the logical file.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25323-129">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="25323-129">Return value</span></span>

<span data-ttu-id="25323-130">Retorna um valor 0 em caso de êxito e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="25323-130">Returns a value of 0 on success, and any other number to indicate an error.</span></span> <span data-ttu-id="25323-131">Para obter códigos de erro adicionais, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="25323-131">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="25323-132">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="25323-132">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="25323-133">**Êxito**</span><span class="sxs-lookup"><span data-stu-id="25323-133">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="25323-134">0</span><span class="sxs-lookup"><span data-stu-id="25323-134">0</span></span>

<span data-ttu-id="25323-135">Sucesso.</span><span class="sxs-lookup"><span data-stu-id="25323-135">Success.</span></span>

</dd> <dt>

<span data-ttu-id="25323-136">**Acesso negado**</span><span class="sxs-lookup"><span data-stu-id="25323-136">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="25323-137">2</span><span class="sxs-lookup"><span data-stu-id="25323-137">2</span></span>

<span data-ttu-id="25323-138">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="25323-138">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="25323-139">**Falha não especificada**</span><span class="sxs-lookup"><span data-stu-id="25323-139">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="25323-140">8</span><span class="sxs-lookup"><span data-stu-id="25323-140">8</span></span>

<span data-ttu-id="25323-141">Falha não especificada.</span><span class="sxs-lookup"><span data-stu-id="25323-141">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="25323-142">**Objeto inválido**</span><span class="sxs-lookup"><span data-stu-id="25323-142">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="25323-143">9</span><span class="sxs-lookup"><span data-stu-id="25323-143">9</span></span>

<span data-ttu-id="25323-144">Objeto inválido.</span><span class="sxs-lookup"><span data-stu-id="25323-144">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="25323-145">**O objeto já existe**</span><span class="sxs-lookup"><span data-stu-id="25323-145">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="25323-146">10</span><span class="sxs-lookup"><span data-stu-id="25323-146">10</span></span>

<span data-ttu-id="25323-147">O objeto já existe.</span><span class="sxs-lookup"><span data-stu-id="25323-147">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="25323-148">**Sistema de arquivos não NTFS**</span><span class="sxs-lookup"><span data-stu-id="25323-148">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="25323-149">11</span><span class="sxs-lookup"><span data-stu-id="25323-149">11</span></span>

</dd> <dt>

<span data-ttu-id="25323-150">**Plataforma não NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="25323-150">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="25323-151">12</span><span class="sxs-lookup"><span data-stu-id="25323-151">12</span></span>

<span data-ttu-id="25323-152">Plataforma não baseada no Windows NT.</span><span class="sxs-lookup"><span data-stu-id="25323-152">Platform not Windows NT-based.</span></span>

</dd> <dt>

<span data-ttu-id="25323-153">**A unidade não é a mesma**</span><span class="sxs-lookup"><span data-stu-id="25323-153">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="25323-154">13</span><span class="sxs-lookup"><span data-stu-id="25323-154">13</span></span>

<span data-ttu-id="25323-155">A unidade não é a mesma.</span><span class="sxs-lookup"><span data-stu-id="25323-155">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="25323-156">**Diretório não vazio**</span><span class="sxs-lookup"><span data-stu-id="25323-156">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="25323-157">14</span><span class="sxs-lookup"><span data-stu-id="25323-157">14</span></span>

<span data-ttu-id="25323-158">O diretório não está vazio.</span><span class="sxs-lookup"><span data-stu-id="25323-158">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="25323-159">**Violação de compartilhamento**</span><span class="sxs-lookup"><span data-stu-id="25323-159">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="25323-160">15</span><span class="sxs-lookup"><span data-stu-id="25323-160">15</span></span>

<span data-ttu-id="25323-161">Violação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="25323-161">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="25323-162">**Arquivo de início inválido**</span><span class="sxs-lookup"><span data-stu-id="25323-162">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="25323-163">16</span><span class="sxs-lookup"><span data-stu-id="25323-163">16</span></span>

<span data-ttu-id="25323-164">Arquivo inicial inválido.</span><span class="sxs-lookup"><span data-stu-id="25323-164">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="25323-165">**Privilégio não mantido**</span><span class="sxs-lookup"><span data-stu-id="25323-165">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="25323-166">17</span><span class="sxs-lookup"><span data-stu-id="25323-166">17</span></span>

<span data-ttu-id="25323-167">Privilégio não mantido.</span><span class="sxs-lookup"><span data-stu-id="25323-167">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="25323-168">**Parâmetro inválido**</span><span class="sxs-lookup"><span data-stu-id="25323-168">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="25323-169">21</span><span class="sxs-lookup"><span data-stu-id="25323-169">21</span></span>

<span data-ttu-id="25323-170">Parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="25323-170">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="25323-171">Comentários</span><span class="sxs-lookup"><span data-stu-id="25323-171">Remarks</span></span>

<span data-ttu-id="25323-172">O método **ChangeSecurityPermissions** no [**\_ arquivo CIM**](cim-datafile.md) é implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="25323-172">The **ChangeSecurityPermissions** method in [**CIM\_DataFile**](cim-datafile.md) is implemented by WMI.</span></span>

<span data-ttu-id="25323-173">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="25323-173">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="25323-174">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="25323-174">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="25323-175">Requisitos</span><span class="sxs-lookup"><span data-stu-id="25323-175">Requirements</span></span>



| <span data-ttu-id="25323-176">Requisito</span><span class="sxs-lookup"><span data-stu-id="25323-176">Requirement</span></span> | <span data-ttu-id="25323-177">Valor</span><span class="sxs-lookup"><span data-stu-id="25323-177">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="25323-178">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="25323-178">Minimum supported client</span></span><br/> | <span data-ttu-id="25323-179">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="25323-179">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="25323-180">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="25323-180">Minimum supported server</span></span><br/> | <span data-ttu-id="25323-181">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="25323-181">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="25323-182">Namespace</span><span class="sxs-lookup"><span data-stu-id="25323-182">Namespace</span></span><br/>                | <span data-ttu-id="25323-183">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="25323-183">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="25323-184">MOF</span><span class="sxs-lookup"><span data-stu-id="25323-184">MOF</span></span><br/>                      | <dl> <span data-ttu-id="25323-185"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="25323-185"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="25323-186">DLL</span><span class="sxs-lookup"><span data-stu-id="25323-186">DLL</span></span><br/>                      | <dl> <span data-ttu-id="25323-187"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="25323-187"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25323-188">Confira também</span><span class="sxs-lookup"><span data-stu-id="25323-188">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25323-189">**DataFile de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="25323-189">**CIM\_DataFile**</span></span>](changesecuritypermissions-method-in-class-cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="25323-190">**DataFile de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="25323-190">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="25323-191">Tarefas do WMI: arquivos e pastas</span><span class="sxs-lookup"><span data-stu-id="25323-191">WMI Tasks: Files and Folders</span></span>](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[<span data-ttu-id="25323-192">**Constantes de direitos de acesso de arquivo e diretório**</span><span class="sxs-lookup"><span data-stu-id="25323-192">**File and Directory Access Rights Constants**</span></span>](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

