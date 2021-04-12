---
description: Altera as permissões de segurança para o arquivo de dispositivo lógico especificado no caminho do objeto.
ms.assetid: 4b3e1a0e-3c9e-45bb-8c7b-cbbc8f9d1265
ms.tgt_platform: multiple
title: Método ChangeSecurityPermissions da classe CIM_DeviceFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile.ChangeSecurityPermissions
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 73a772c17695a537e4a9a8518bf05b052c0417f6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457084"
---
# <a name="changesecuritypermissions-method-of-the-cim_devicefile-class"></a><span data-ttu-id="c6175-103">Método ChangeSecurityPermissions da classe CIM \_ devicefile</span><span class="sxs-lookup"><span data-stu-id="c6175-103">ChangeSecurityPermissions method of the CIM\_DeviceFile class</span></span>

<span data-ttu-id="c6175-104">O método **ChangeSecurityPermissions** altera as permissões de segurança para o arquivo de dispositivo lógico especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="c6175-104">The **ChangeSecurityPermissions** method changes the security permissions for the logical device file specified in the object path.</span></span> <span data-ttu-id="c6175-105">Se o arquivo lógico for um diretório, esse método agirá de forma recursiva, alterando as permissões de segurança para todos os arquivos e subdiretórios que o diretório contém.</span><span class="sxs-lookup"><span data-stu-id="c6175-105">If the logical file is a directory, then this method will act recursively, changing the security permissions for all of the files and sub-directories that the directory contains.</span></span> <span data-ttu-id="c6175-106">Esse método é herdado [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="c6175-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c6175-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="c6175-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="c6175-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="c6175-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="c6175-109">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="c6175-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="c6175-110">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="c6175-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="c6175-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c6175-111">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissions(
  [in] Win32_SecurityDescriptor SecurityDescriptor,
  [in] uint32                   Option
);
```



## <a name="parameters"></a><span data-ttu-id="c6175-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c6175-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6175-113">*SecurityDescriptor* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c6175-113">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6175-114">Especifica as informações de segurança.</span><span class="sxs-lookup"><span data-stu-id="c6175-114">Specifies the security information.</span></span>

> [!Caution]  
> <span data-ttu-id="c6175-115">Uma ACL (lista de controle de acesso) **nula** na estrutura do [**\_ descritor de segurança**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) concede acesso ilimitado.</span><span class="sxs-lookup"><span data-stu-id="c6175-115">A **NULL** access control list (ACL) in the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure grants unlimited access.</span></span>

 

</dd> <dt>

<span data-ttu-id="c6175-116">*Opção* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c6175-116">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6175-117">Privilégio de segurança a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="c6175-117">Security privilege to modify.</span></span> <span data-ttu-id="c6175-118">Por exemplo, para alterar a segurança do proprietário e da DACL, use:</span><span class="sxs-lookup"><span data-stu-id="c6175-118">For example, to change the owner and DACL security, use:</span></span>

`Option = 1 + 4`

<span data-ttu-id="c6175-119">ou</span><span class="sxs-lookup"><span data-stu-id="c6175-119">or</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span data-ttu-id="c6175-120"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**Alterar \_ \_ \_ Informações de segurança do proprietário** (1)</span><span class="sxs-lookup"><span data-stu-id="c6175-120"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE\_OWNER\_SECURITY\_INFORMATION** (1)</span></span>


</dt> <dd>

<span data-ttu-id="c6175-121">Altere o proprietário do arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="c6175-121">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span data-ttu-id="c6175-122"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**Alterar \_ \_ \_ Informações de segurança do grupo** (2)</span><span class="sxs-lookup"><span data-stu-id="c6175-122"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE\_GROUP\_SECURITY\_INFORMATION** (2)</span></span>


</dt> <dd>

<span data-ttu-id="c6175-123">Altere o grupo do arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="c6175-123">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span data-ttu-id="c6175-124"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**Alterar \_ \_ \_ Informações de segurança da DACL** (4)</span><span class="sxs-lookup"><span data-stu-id="c6175-124"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE\_DACL\_SECURITY\_INFORMATION** (4)</span></span>


</dt> <dd>

<span data-ttu-id="c6175-125">Altere a ACL do arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="c6175-125">Change the ACL of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span data-ttu-id="c6175-126"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Alterar \_ \_ \_ Informações de segurança da SACL** (8)</span><span class="sxs-lookup"><span data-stu-id="c6175-126"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE\_SACL\_SECURITY\_INFORMATION** (8)</span></span>


</dt> <dd>

<span data-ttu-id="c6175-127">Altere a ACL do sistema do arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="c6175-127">Change the system ACL of the logical file.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6175-128">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c6175-128">Return value</span></span>

<span data-ttu-id="c6175-129">Retorna um valor de 0 (zero) em caso de êxito e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="c6175-129">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="c6175-130">**Êxito**</span><span class="sxs-lookup"><span data-stu-id="c6175-130">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="c6175-131">0</span><span class="sxs-lookup"><span data-stu-id="c6175-131">0</span></span>

<span data-ttu-id="c6175-132">Sucesso.</span><span class="sxs-lookup"><span data-stu-id="c6175-132">Success.</span></span>

</dd> <dt>

<span data-ttu-id="c6175-133">**Acesso negado**</span><span class="sxs-lookup"><span data-stu-id="c6175-133">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="c6175-134">2</span><span class="sxs-lookup"><span data-stu-id="c6175-134">2</span></span>

<span data-ttu-id="c6175-135">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="c6175-135">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="c6175-136">**Falha não especificada**</span><span class="sxs-lookup"><span data-stu-id="c6175-136">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="c6175-137">8</span><span class="sxs-lookup"><span data-stu-id="c6175-137">8</span></span>

<span data-ttu-id="c6175-138">Falha não especificada.</span><span class="sxs-lookup"><span data-stu-id="c6175-138">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="c6175-139">**Objeto inválido**</span><span class="sxs-lookup"><span data-stu-id="c6175-139">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="c6175-140">9</span><span class="sxs-lookup"><span data-stu-id="c6175-140">9</span></span>

<span data-ttu-id="c6175-141">Objeto inválido.</span><span class="sxs-lookup"><span data-stu-id="c6175-141">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="c6175-142">**O objeto já existe**</span><span class="sxs-lookup"><span data-stu-id="c6175-142">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="c6175-143">10</span><span class="sxs-lookup"><span data-stu-id="c6175-143">10</span></span>

<span data-ttu-id="c6175-144">O objeto já existe.</span><span class="sxs-lookup"><span data-stu-id="c6175-144">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="c6175-145">**Sistema de arquivos não NTFS**</span><span class="sxs-lookup"><span data-stu-id="c6175-145">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="c6175-146">11</span><span class="sxs-lookup"><span data-stu-id="c6175-146">11</span></span>

<span data-ttu-id="c6175-147">Sistema de arquivos não NTFS.</span><span class="sxs-lookup"><span data-stu-id="c6175-147">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="c6175-148">**Plataforma não NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="c6175-148">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="c6175-149">12</span><span class="sxs-lookup"><span data-stu-id="c6175-149">12</span></span>

<span data-ttu-id="c6175-150">Plataforma não Windows.</span><span class="sxs-lookup"><span data-stu-id="c6175-150">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="c6175-151">**A unidade não é a mesma**</span><span class="sxs-lookup"><span data-stu-id="c6175-151">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="c6175-152">13</span><span class="sxs-lookup"><span data-stu-id="c6175-152">13</span></span>

<span data-ttu-id="c6175-153">A unidade não é a mesma.</span><span class="sxs-lookup"><span data-stu-id="c6175-153">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="c6175-154">**Diretório não vazio**</span><span class="sxs-lookup"><span data-stu-id="c6175-154">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="c6175-155">14</span><span class="sxs-lookup"><span data-stu-id="c6175-155">14</span></span>

<span data-ttu-id="c6175-156">O diretório não está vazio.</span><span class="sxs-lookup"><span data-stu-id="c6175-156">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="c6175-157">**Violação de compartilhamento**</span><span class="sxs-lookup"><span data-stu-id="c6175-157">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="c6175-158">15</span><span class="sxs-lookup"><span data-stu-id="c6175-158">15</span></span>

<span data-ttu-id="c6175-159">Violação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="c6175-159">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="c6175-160">**Arquivo de início inválido**</span><span class="sxs-lookup"><span data-stu-id="c6175-160">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="c6175-161">16</span><span class="sxs-lookup"><span data-stu-id="c6175-161">16</span></span>

<span data-ttu-id="c6175-162">Arquivo inicial inválido.</span><span class="sxs-lookup"><span data-stu-id="c6175-162">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="c6175-163">**Privilégio não mantido**</span><span class="sxs-lookup"><span data-stu-id="c6175-163">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="c6175-164">17</span><span class="sxs-lookup"><span data-stu-id="c6175-164">17</span></span>

<span data-ttu-id="c6175-165">Privilégio não mantido.</span><span class="sxs-lookup"><span data-stu-id="c6175-165">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="c6175-166">**Parâmetro inválido**</span><span class="sxs-lookup"><span data-stu-id="c6175-166">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="c6175-167">21</span><span class="sxs-lookup"><span data-stu-id="c6175-167">21</span></span>

<span data-ttu-id="c6175-168">Parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="c6175-168">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c6175-169">Comentários</span><span class="sxs-lookup"><span data-stu-id="c6175-169">Remarks</span></span>

<span data-ttu-id="c6175-170">Este método não está implementado no momento pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="c6175-170">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="c6175-171">Para usar esse método, você deve implementá-lo em seu próprio provedor.</span><span class="sxs-lookup"><span data-stu-id="c6175-171">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="c6175-172">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="c6175-172">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="c6175-173">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="c6175-173">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6175-174">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c6175-174">Requirements</span></span>



| <span data-ttu-id="c6175-175">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6175-175">Requirement</span></span> | <span data-ttu-id="c6175-176">Valor</span><span class="sxs-lookup"><span data-stu-id="c6175-176">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c6175-177">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c6175-177">Minimum supported client</span></span><br/> | <span data-ttu-id="c6175-178">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c6175-178">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c6175-179">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c6175-179">Minimum supported server</span></span><br/> | <span data-ttu-id="c6175-180">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c6175-180">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c6175-181">Namespace</span><span class="sxs-lookup"><span data-stu-id="c6175-181">Namespace</span></span><br/>                | <span data-ttu-id="c6175-182">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="c6175-182">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c6175-183">MOF</span><span class="sxs-lookup"><span data-stu-id="c6175-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c6175-184"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c6175-184"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c6175-185">DLL</span><span class="sxs-lookup"><span data-stu-id="c6175-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c6175-186"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c6175-186"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6175-187">Confira também</span><span class="sxs-lookup"><span data-stu-id="c6175-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6175-188">**\_Dispositivo CIM**</span><span class="sxs-lookup"><span data-stu-id="c6175-188">**CIM\_DeviceFile**</span></span>](changesecuritypermissions-method-in-class-cim-devicefile.md)
</dt> <dt>

[<span data-ttu-id="c6175-189">**\_Dispositivo CIM**</span><span class="sxs-lookup"><span data-stu-id="c6175-189">**CIM\_DeviceFile**</span></span>](cim-devicefile.md)
</dt> </dl>

 

