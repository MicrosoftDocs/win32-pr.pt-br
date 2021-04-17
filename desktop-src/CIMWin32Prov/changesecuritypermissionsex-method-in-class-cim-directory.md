---
description: Altera as permissões de segurança para o arquivo de entrada de diretório lógico especificado no caminho do objeto (esse método é uma versão estendida do método ChangeSecurityPermissions e é herdado de CIM \_ LogicalFile).
ms.assetid: 5c1f66ba-9aa1-47ca-8fcf-7663782544cd
ms.tgt_platform: multiple
title: Método ChangeSecurityPermissionsEx da classe CIM_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.ChangeSecurityPermissionsEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: f2d8ddf4c6ffdbd016db1e8c08d89f2dd6476ccf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105755460"
---
# <a name="changesecuritypermissionsex-method-of-the-cim_directory-class"></a><span data-ttu-id="8d085-103">Método ChangeSecurityPermissionsEx da classe de \_ diretório CIM</span><span class="sxs-lookup"><span data-stu-id="8d085-103">ChangeSecurityPermissionsEx method of the CIM\_Directory class</span></span>

<span data-ttu-id="8d085-104">O método **ChangeSecurityPermissionsEx** altera as permissões de segurança para o arquivo de entrada de diretório lógico especificado no caminho do objeto (esse método é uma versão estendida do método [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-cim-directory.md) e é herdado de [**CIM \_ LogicalFile**](cim-logicalfile.md)).</span><span class="sxs-lookup"><span data-stu-id="8d085-104">The **ChangeSecurityPermissionsEx** method changes the security permissions for the logical directory entry file specified in the object path (this method is an extended version of the [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-cim-directory.md) method and is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md)).</span></span> <span data-ttu-id="8d085-105">Se o arquivo lógico for um diretório, esse método agirá de forma recursiva, alterando as permissões de segurança para todos os arquivos e subdiretórios que o diretório contém.</span><span class="sxs-lookup"><span data-stu-id="8d085-105">If the logical file is a directory, then this method will act recursively, changing the security permissions for all of the files and sub-directories that the directory contains.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8d085-106">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="8d085-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="8d085-107">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="8d085-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="8d085-108">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="8d085-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="8d085-109">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="8d085-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="8d085-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8d085-110">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissionsEx(
  [in]           Win32_SecurityDescriptor SecurityDescriptor,
  [in]           uint32                   Option,
  [out]          string                   StopFileName,
  [in, optional] string                   StartFileName,
  [in, optional] boolean                  Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="8d085-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8d085-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d085-112">*SecurityDescriptor* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8d085-112">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d085-113">Especifica informações de segurança.</span><span class="sxs-lookup"><span data-stu-id="8d085-113">Specifies security information.</span></span>

> [!Note]  
> <span data-ttu-id="8d085-114">Uma ACL **nula** na estrutura [**do \_ descritor de segurança**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) concede acesso ilimitado.</span><span class="sxs-lookup"><span data-stu-id="8d085-114">A **NULL** ACL in the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure grants unlimited access.</span></span>

 

</dd> <dt>

<span data-ttu-id="8d085-115">*Opção* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8d085-115">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d085-116">Privilégio de segurança a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="8d085-116">Security privilege to modify.</span></span> <span data-ttu-id="8d085-117">Por exemplo, para alterar a segurança do proprietário e da DACL, use</span><span class="sxs-lookup"><span data-stu-id="8d085-117">For example, to change the owner and DACL security, use</span></span>

`Option = 1 + 4`

<span data-ttu-id="8d085-118">ou</span><span class="sxs-lookup"><span data-stu-id="8d085-118">or</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span data-ttu-id="8d085-119"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**Alterar \_ \_ \_ Informações de segurança do proprietário** (1)</span><span class="sxs-lookup"><span data-stu-id="8d085-119"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE\_OWNER\_SECURITY\_INFORMATION** (1)</span></span>


</dt> <dd>

<span data-ttu-id="8d085-120">Altere o proprietário do arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="8d085-120">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span data-ttu-id="8d085-121"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**Alterar \_ \_ \_ Informações de segurança do grupo** (2)</span><span class="sxs-lookup"><span data-stu-id="8d085-121"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE\_GROUP\_SECURITY\_INFORMATION** (2)</span></span>


</dt> <dd>

<span data-ttu-id="8d085-122">Altere o grupo do arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="8d085-122">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span data-ttu-id="8d085-123"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**Alterar \_ \_ \_ Informações de segurança da DACL** (4)</span><span class="sxs-lookup"><span data-stu-id="8d085-123"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE\_DACL\_SECURITY\_INFORMATION** (4)</span></span>


</dt> <dd>

<span data-ttu-id="8d085-124">Altere a ACL do arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="8d085-124">Change the ACL of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span data-ttu-id="8d085-125"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Alterar \_ \_ \_ Informações de segurança da SACL** (8)</span><span class="sxs-lookup"><span data-stu-id="8d085-125"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE\_SACL\_SECURITY\_INFORMATION** (8)</span></span>


</dt> <dd>

<span data-ttu-id="8d085-126">Altere a ACL do sistema do arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="8d085-126">Change the system ACL of the logical file.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="8d085-127">*StopFileName* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="8d085-127">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8d085-128">Cadeia de caracteres que representa o nome do arquivo (ou diretório) em que o método falhou.</span><span class="sxs-lookup"><span data-stu-id="8d085-128">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="8d085-129">Esse parâmetro tem um valor de **NULL** se o método tiver sucesso.</span><span class="sxs-lookup"><span data-stu-id="8d085-129">This parameter has a value of **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="8d085-130">*StartFileName* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="8d085-130">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8d085-131">Cadeia de caracteres que representa o arquivo filho (ou diretório) a ser usado como ponto de partida para esse método.</span><span class="sxs-lookup"><span data-stu-id="8d085-131">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="8d085-132">Normalmente, o parâmetro *StartFileName* é o parâmetro *StopFileName* que especifica o arquivo (ou diretório) no qual ocorreu um erro da chamada de método anterior.</span><span class="sxs-lookup"><span data-stu-id="8d085-132">Typically, the *StartFileName* parameter is the *StopFileName* parameter specifying the file (or directory) at which an error occurred from the previous method call.</span></span> <span data-ttu-id="8d085-133">Se o valor do parâmetro for **NULL**, a operação será executada no arquivo ou diretório especificado na chamada de [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="8d085-133">If the parameter value is **null**, the operation is performed on the file or directory specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="8d085-134">*Recursivo* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="8d085-134">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8d085-135">Se **for true**, o método também será aplicado recursivamente a arquivos e diretórios dentro do diretório especificado pela instância do [**\_ diretório CIM**](cim-directory.md) .</span><span class="sxs-lookup"><span data-stu-id="8d085-135">If **TRUE**, the method is also applied recursively to files and directories within the directory specified by the [**CIM\_Directory**](cim-directory.md) instance.</span></span> <span data-ttu-id="8d085-136">Para instâncias de arquivo, esse parâmetro é ignorado.</span><span class="sxs-lookup"><span data-stu-id="8d085-136">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d085-137">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8d085-137">Return value</span></span>

<span data-ttu-id="8d085-138">Retorna um valor de 0 (zero) em caso de êxito e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="8d085-138">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="8d085-139">0</span><span class="sxs-lookup"><span data-stu-id="8d085-139">0</span></span>

<span data-ttu-id="8d085-140">Sucesso.</span><span class="sxs-lookup"><span data-stu-id="8d085-140">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="8d085-141">2</span><span class="sxs-lookup"><span data-stu-id="8d085-141">2</span></span>

<span data-ttu-id="8d085-142">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="8d085-142">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="8d085-143">8</span><span class="sxs-lookup"><span data-stu-id="8d085-143">8</span></span>

<span data-ttu-id="8d085-144">Falha não especificada.</span><span class="sxs-lookup"><span data-stu-id="8d085-144">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="8d085-145">9</span><span class="sxs-lookup"><span data-stu-id="8d085-145">9</span></span>

<span data-ttu-id="8d085-146">Objeto inválido.</span><span class="sxs-lookup"><span data-stu-id="8d085-146">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="8d085-147">10</span><span class="sxs-lookup"><span data-stu-id="8d085-147">10</span></span>

<span data-ttu-id="8d085-148">O objeto já existe.</span><span class="sxs-lookup"><span data-stu-id="8d085-148">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="8d085-149">11</span><span class="sxs-lookup"><span data-stu-id="8d085-149">11</span></span>

<span data-ttu-id="8d085-150">Sistema de arquivos não NTFS.</span><span class="sxs-lookup"><span data-stu-id="8d085-150">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="8d085-151">12</span><span class="sxs-lookup"><span data-stu-id="8d085-151">12</span></span>

<span data-ttu-id="8d085-152">Plataforma não Windows.</span><span class="sxs-lookup"><span data-stu-id="8d085-152">Platform not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="8d085-153">13</span><span class="sxs-lookup"><span data-stu-id="8d085-153">13</span></span>

<span data-ttu-id="8d085-154">A unidade não é a mesma.</span><span class="sxs-lookup"><span data-stu-id="8d085-154">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="8d085-155">14</span><span class="sxs-lookup"><span data-stu-id="8d085-155">14</span></span>

<span data-ttu-id="8d085-156">O diretório não está vazio.</span><span class="sxs-lookup"><span data-stu-id="8d085-156">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="8d085-157">15</span><span class="sxs-lookup"><span data-stu-id="8d085-157">15</span></span>

<span data-ttu-id="8d085-158">Violação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="8d085-158">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="8d085-159">16</span><span class="sxs-lookup"><span data-stu-id="8d085-159">16</span></span>

<span data-ttu-id="8d085-160">Arquivo inicial inválido.</span><span class="sxs-lookup"><span data-stu-id="8d085-160">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="8d085-161">17</span><span class="sxs-lookup"><span data-stu-id="8d085-161">17</span></span>

<span data-ttu-id="8d085-162">Privilégio não mantido.</span><span class="sxs-lookup"><span data-stu-id="8d085-162">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="8d085-163">21</span><span class="sxs-lookup"><span data-stu-id="8d085-163">21</span></span>

<span data-ttu-id="8d085-164">Parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="8d085-164">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8d085-165">Comentários</span><span class="sxs-lookup"><span data-stu-id="8d085-165">Remarks</span></span>

<span data-ttu-id="8d085-166">Este método não está implementado no momento pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="8d085-166">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="8d085-167">Para usar esse método, você deve implementá-lo em seu próprio provedor.</span><span class="sxs-lookup"><span data-stu-id="8d085-167">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="8d085-168">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="8d085-168">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="8d085-169">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="8d085-169">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d085-170">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8d085-170">Requirements</span></span>



| <span data-ttu-id="8d085-171">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d085-171">Requirement</span></span> | <span data-ttu-id="8d085-172">Valor</span><span class="sxs-lookup"><span data-stu-id="8d085-172">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8d085-173">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8d085-173">Minimum supported client</span></span><br/> | <span data-ttu-id="8d085-174">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8d085-174">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8d085-175">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8d085-175">Minimum supported server</span></span><br/> | <span data-ttu-id="8d085-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8d085-176">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8d085-177">Namespace</span><span class="sxs-lookup"><span data-stu-id="8d085-177">Namespace</span></span><br/>                | <span data-ttu-id="8d085-178">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="8d085-178">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8d085-179">MOF</span><span class="sxs-lookup"><span data-stu-id="8d085-179">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8d085-180"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8d085-180"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8d085-181">DLL</span><span class="sxs-lookup"><span data-stu-id="8d085-181">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8d085-182"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8d085-182"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d085-183">Confira também</span><span class="sxs-lookup"><span data-stu-id="8d085-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d085-184">\_Diretório CIM</span><span class="sxs-lookup"><span data-stu-id="8d085-184">CIM\_Directory</span></span>](changesecuritypermissionsex-method-in-class-cim-directory.md)
</dt> <dt>

[<span data-ttu-id="8d085-185">**\_Diretório CIM**</span><span class="sxs-lookup"><span data-stu-id="8d085-185">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> </dl>

 

