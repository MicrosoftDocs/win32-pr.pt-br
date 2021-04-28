---
description: Método ChangeSecurityPermissions da classe CIM_Directory – altera as permissões de segurança para o arquivo de entrada de diretório lógico especificado no caminho do objeto.
ms.assetid: d3caeec1-fecc-4463-9349-d82869c11927
ms.tgt_platform: multiple
title: Método ChangeSecurityPermissions da classe CIM_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.ChangeSecurityPermissions
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 389ed5b7b0a43981c5eeb3d66a73bd19cbd99d88
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108091064"
---
# <a name="changesecuritypermissions-method-of-the-cim_directory-class"></a><span data-ttu-id="2fc2b-103">Método ChangeSecurityPermissions da classe de \_ diretório CIM</span><span class="sxs-lookup"><span data-stu-id="2fc2b-103">ChangeSecurityPermissions method of the CIM\_Directory class</span></span>

<span data-ttu-id="2fc2b-104">O método **ChangeSecurityPermissions** altera as permissões de segurança para o arquivo de entrada de diretório lógico especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="2fc2b-104">The **ChangeSecurityPermissions** method changes the security permissions for the logical directory entry file specified in the object path.</span></span> <span data-ttu-id="2fc2b-105">Se o arquivo lógico for um diretório, esse método agirá de forma recursiva, alterando as permissões de segurança para todos os arquivos e subdiretórios que o diretório contém.</span><span class="sxs-lookup"><span data-stu-id="2fc2b-105">If the logical file is a directory, then this method will act recursively, changing the security permissions for all of the files and sub-directories that the directory contains.</span></span> <span data-ttu-id="2fc2b-106">Esse método é herdado [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="2fc2b-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2fc2b-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="2fc2b-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="2fc2b-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="2fc2b-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="2fc2b-109">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="2fc2b-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="2fc2b-110">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="2fc2b-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="2fc2b-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2fc2b-111">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissions(
  [in] Win32_SecurityDescriptor SecurityDescriptor,
  [in] uint32                   Option
);
```



## <a name="parameters"></a><span data-ttu-id="2fc2b-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2fc2b-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2fc2b-113">*SecurityDescriptor* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2fc2b-113">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2fc2b-114">Especifica informações de segurança.</span><span class="sxs-lookup"><span data-stu-id="2fc2b-114">Specifies security information.</span></span>

> [!Note]  
> <span data-ttu-id="2fc2b-115">Uma ACL (lista de controle de acesso) **nula** na estrutura do [**\_ descritor de segurança**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) concede acesso ilimitado.</span><span class="sxs-lookup"><span data-stu-id="2fc2b-115">A **NULL** access control list (ACL) in the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure grants unlimited access.</span></span>

 

</dd> <dt>

<span data-ttu-id="2fc2b-116">*Opção* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2fc2b-116">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2fc2b-117">Privilégio de segurança a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="2fc2b-117">Security privilege to modify.</span></span> <span data-ttu-id="2fc2b-118">Por exemplo, para alterar a segurança do proprietário e da DACL, use:</span><span class="sxs-lookup"><span data-stu-id="2fc2b-118">For example, to change the owner and DACL security, use:</span></span>

`Option = 1 + 4`

<span data-ttu-id="2fc2b-119">ou</span><span class="sxs-lookup"><span data-stu-id="2fc2b-119">or</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span data-ttu-id="2fc2b-120"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**Alterar \_ \_ \_ Informações de segurança do proprietário** (1)</span><span class="sxs-lookup"><span data-stu-id="2fc2b-120"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE\_OWNER\_SECURITY\_INFORMATION** (1)</span></span>


</dt> <dd>

<span data-ttu-id="2fc2b-121">Altere o proprietário do arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="2fc2b-121">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span data-ttu-id="2fc2b-122"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**Alterar \_ \_ \_ Informações de segurança do grupo** (2)</span><span class="sxs-lookup"><span data-stu-id="2fc2b-122"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE\_GROUP\_SECURITY\_INFORMATION** (2)</span></span>


</dt> <dd>

<span data-ttu-id="2fc2b-123">Altere o grupo do arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="2fc2b-123">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span data-ttu-id="2fc2b-124"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**Alterar \_ \_ \_ Informações de segurança da DACL** (4)</span><span class="sxs-lookup"><span data-stu-id="2fc2b-124"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE\_DACL\_SECURITY\_INFORMATION** (4)</span></span>


</dt> <dd>

<span data-ttu-id="2fc2b-125">Altere a ACL do arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="2fc2b-125">Change the ACL of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span data-ttu-id="2fc2b-126"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Alterar \_ \_ \_ Informações de segurança da SACL** (8)</span><span class="sxs-lookup"><span data-stu-id="2fc2b-126"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE\_SACL\_SECURITY\_INFORMATION** (8)</span></span>


</dt> <dd>

<span data-ttu-id="2fc2b-127">Altere a ACL do sistema do arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="2fc2b-127">Change the system ACL of the logical file.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2fc2b-128">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="2fc2b-128">Return value</span></span>

<span data-ttu-id="2fc2b-129">Retorna um valor de 0 (zero) em caso de êxito e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="2fc2b-129">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="2fc2b-130">0</span><span class="sxs-lookup"><span data-stu-id="2fc2b-130">0</span></span>

<span data-ttu-id="2fc2b-131">Sucesso.</span><span class="sxs-lookup"><span data-stu-id="2fc2b-131">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="2fc2b-132">2</span><span class="sxs-lookup"><span data-stu-id="2fc2b-132">2</span></span>

<span data-ttu-id="2fc2b-133">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="2fc2b-133">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="2fc2b-134">8</span><span class="sxs-lookup"><span data-stu-id="2fc2b-134">8</span></span>

<span data-ttu-id="2fc2b-135">Falha não especificada.</span><span class="sxs-lookup"><span data-stu-id="2fc2b-135">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="2fc2b-136">9</span><span class="sxs-lookup"><span data-stu-id="2fc2b-136">9</span></span>

<span data-ttu-id="2fc2b-137">Objeto inválido.</span><span class="sxs-lookup"><span data-stu-id="2fc2b-137">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="2fc2b-138">10</span><span class="sxs-lookup"><span data-stu-id="2fc2b-138">10</span></span>

<span data-ttu-id="2fc2b-139">O objeto já existe.</span><span class="sxs-lookup"><span data-stu-id="2fc2b-139">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="2fc2b-140">11</span><span class="sxs-lookup"><span data-stu-id="2fc2b-140">11</span></span>

<span data-ttu-id="2fc2b-141">Sistema de arquivos não NTFS.</span><span class="sxs-lookup"><span data-stu-id="2fc2b-141">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="2fc2b-142">12</span><span class="sxs-lookup"><span data-stu-id="2fc2b-142">12</span></span>

<span data-ttu-id="2fc2b-143">Plataforma não Windows.</span><span class="sxs-lookup"><span data-stu-id="2fc2b-143">Platform not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="2fc2b-144">13</span><span class="sxs-lookup"><span data-stu-id="2fc2b-144">13</span></span>

<span data-ttu-id="2fc2b-145">A unidade não é a mesma.</span><span class="sxs-lookup"><span data-stu-id="2fc2b-145">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="2fc2b-146">14</span><span class="sxs-lookup"><span data-stu-id="2fc2b-146">14</span></span>

<span data-ttu-id="2fc2b-147">O diretório não está vazio.</span><span class="sxs-lookup"><span data-stu-id="2fc2b-147">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="2fc2b-148">15</span><span class="sxs-lookup"><span data-stu-id="2fc2b-148">15</span></span>

<span data-ttu-id="2fc2b-149">Violação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="2fc2b-149">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="2fc2b-150">16</span><span class="sxs-lookup"><span data-stu-id="2fc2b-150">16</span></span>

<span data-ttu-id="2fc2b-151">Arquivo inicial inválido.</span><span class="sxs-lookup"><span data-stu-id="2fc2b-151">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="2fc2b-152">17</span><span class="sxs-lookup"><span data-stu-id="2fc2b-152">17</span></span>

<span data-ttu-id="2fc2b-153">Privilégio não mantido.</span><span class="sxs-lookup"><span data-stu-id="2fc2b-153">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="2fc2b-154">21</span><span class="sxs-lookup"><span data-stu-id="2fc2b-154">21</span></span>

<span data-ttu-id="2fc2b-155">Parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="2fc2b-155">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2fc2b-156">Comentários</span><span class="sxs-lookup"><span data-stu-id="2fc2b-156">Remarks</span></span>

<span data-ttu-id="2fc2b-157">Este método não está implementado no momento pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="2fc2b-157">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="2fc2b-158">Para usar esse método, você deve implementá-lo em seu próprio provedor.</span><span class="sxs-lookup"><span data-stu-id="2fc2b-158">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="2fc2b-159">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="2fc2b-159">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="2fc2b-160">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="2fc2b-160">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="2fc2b-161">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2fc2b-161">Requirements</span></span>



| <span data-ttu-id="2fc2b-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="2fc2b-162">Requirement</span></span> | <span data-ttu-id="2fc2b-163">Valor</span><span class="sxs-lookup"><span data-stu-id="2fc2b-163">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2fc2b-164">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2fc2b-164">Minimum supported client</span></span><br/> | <span data-ttu-id="2fc2b-165">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2fc2b-165">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2fc2b-166">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2fc2b-166">Minimum supported server</span></span><br/> | <span data-ttu-id="2fc2b-167">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2fc2b-167">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2fc2b-168">Namespace</span><span class="sxs-lookup"><span data-stu-id="2fc2b-168">Namespace</span></span><br/>                | <span data-ttu-id="2fc2b-169">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="2fc2b-169">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2fc2b-170">MOF</span><span class="sxs-lookup"><span data-stu-id="2fc2b-170">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2fc2b-171"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2fc2b-171"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2fc2b-172">DLL</span><span class="sxs-lookup"><span data-stu-id="2fc2b-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2fc2b-173"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2fc2b-173"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2fc2b-174">Consulte também</span><span class="sxs-lookup"><span data-stu-id="2fc2b-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fc2b-175">\_Diretório CIM</span><span class="sxs-lookup"><span data-stu-id="2fc2b-175">CIM\_Directory</span></span>](changesecuritypermissions-method-in-class-cim-directory.md)
</dt> <dt>

[<span data-ttu-id="2fc2b-176">**\_Diretório CIM**</span><span class="sxs-lookup"><span data-stu-id="2fc2b-176">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> </dl>

 

