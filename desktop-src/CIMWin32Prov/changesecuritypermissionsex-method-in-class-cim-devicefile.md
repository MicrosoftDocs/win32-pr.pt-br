---
description: Altera as permissões de segurança para o arquivo de dispositivo especificado no caminho do objeto (esse método é uma versão estendida do método ChangeSecurityPermissions).
ms.assetid: 5ad54470-6961-4c0d-9d2a-d3eaf81d75f4
ms.tgt_platform: multiple
title: Método ChangeSecurityPermissionsEx da classe CIM_DeviceFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile.ChangeSecurityPermissionsEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5f2c7261844542f6414052517432c2e8ff3f1194
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089341"
---
# <a name="changesecuritypermissionsex-method-of-the-cim_devicefile-class"></a><span data-ttu-id="823ca-103">Método ChangeSecurityPermissionsEx da classe CIM \_ devicefile</span><span class="sxs-lookup"><span data-stu-id="823ca-103">ChangeSecurityPermissionsEx method of the CIM\_DeviceFile class</span></span>

<span data-ttu-id="823ca-104">O método **ChangeSecurityPermissionsEx** altera as permissões de segurança para o arquivo de dispositivo especificado no caminho do objeto (esse método é uma versão estendida do método [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-cim-devicefile.md) ).</span><span class="sxs-lookup"><span data-stu-id="823ca-104">The **ChangeSecurityPermissionsEx** method changes the security permissions for the device file specified in the object path (this method is an extended version of the [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-cim-devicefile.md) method).</span></span> <span data-ttu-id="823ca-105">Se o arquivo lógico for um diretório, esse método agirá recursivamente, alterando as permissões de segurança para todos os arquivos e subdiretórios que o diretório contém.</span><span class="sxs-lookup"><span data-stu-id="823ca-105">If the logical file is a directory, then this method acts recursively, changing the security permissions for all of the files and sub-directories that the directory contains.</span></span> <span data-ttu-id="823ca-106">Esse método é herdado [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="823ca-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="823ca-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="823ca-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="823ca-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="823ca-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="823ca-109">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="823ca-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="823ca-110">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="823ca-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="823ca-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="823ca-111">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissionsEx(
  [in]           Win32_SecurityDescriptor SecurityDescriptor,
  [in]           uint32                   Option,
  [out]          string                   StopFileName,
  [in, optional] string                   StartFileName,
  [in, optional] boolean                  Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="823ca-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="823ca-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="823ca-113">*SecurityDescriptor* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="823ca-113">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="823ca-114">Especifica as informações de segurança.</span><span class="sxs-lookup"><span data-stu-id="823ca-114">Specifies the security information.</span></span>

> [!Caution]  
> <span data-ttu-id="823ca-115">Uma ACL **nula** na estrutura [**do \_ descritor de segurança**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) concede acesso ilimitado.</span><span class="sxs-lookup"><span data-stu-id="823ca-115">A **NULL** ACL in the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure grants unlimited access.</span></span>

 

</dd> <dt>

<span data-ttu-id="823ca-116">*Opção* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="823ca-116">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="823ca-117">Privilégio de segurança a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="823ca-117">Security privilege to modify.</span></span> <span data-ttu-id="823ca-118">Por exemplo, para alterar a segurança do proprietário e da DACL, use</span><span class="sxs-lookup"><span data-stu-id="823ca-118">For example, to change the owner and DACL security, use</span></span>

`Option = 1 + 4`

<span data-ttu-id="823ca-119">ou</span><span class="sxs-lookup"><span data-stu-id="823ca-119">or</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span data-ttu-id="823ca-120"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**Alterar \_ \_ \_ Informações de segurança do proprietário** (1)</span><span class="sxs-lookup"><span data-stu-id="823ca-120"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE\_OWNER\_SECURITY\_INFORMATION** (1)</span></span>


</dt> <dd>

<span data-ttu-id="823ca-121">Altere o proprietário do arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="823ca-121">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span data-ttu-id="823ca-122"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**Alterar \_ \_ \_ Informações de segurança do grupo** (2)</span><span class="sxs-lookup"><span data-stu-id="823ca-122"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE\_GROUP\_SECURITY\_INFORMATION** (2)</span></span>


</dt> <dd>

<span data-ttu-id="823ca-123">Altere o grupo do arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="823ca-123">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span data-ttu-id="823ca-124"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**Alterar \_ \_ \_ Informações de segurança da DACL** (4)</span><span class="sxs-lookup"><span data-stu-id="823ca-124"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE\_DACL\_SECURITY\_INFORMATION** (4)</span></span>


</dt> <dd>

<span data-ttu-id="823ca-125">Altere a ACL do arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="823ca-125">Change the ACL of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span data-ttu-id="823ca-126"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Alterar \_ \_ \_ Informações de segurança da SACL** (8)</span><span class="sxs-lookup"><span data-stu-id="823ca-126"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE\_SACL\_SECURITY\_INFORMATION** (8)</span></span>


</dt> <dd>

<span data-ttu-id="823ca-127">Altere a ACL do sistema do arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="823ca-127">Change the system ACL of the logical file.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="823ca-128">*StopFileName* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="823ca-128">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="823ca-129">Cadeia de caracteres que representa o nome do arquivo (ou diretório) em que o método falhou.</span><span class="sxs-lookup"><span data-stu-id="823ca-129">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="823ca-130">Esse parâmetro será **nulo** se o método tiver sucesso.</span><span class="sxs-lookup"><span data-stu-id="823ca-130">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="823ca-131">*StartFileName* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="823ca-131">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="823ca-132">Arquivo filho (ou diretório) a ser usado como ponto de partida para este método.</span><span class="sxs-lookup"><span data-stu-id="823ca-132">Child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="823ca-133">Normalmente, o parâmetro *StartFileName* é o parâmetro *StopFileName* que especifica o arquivo ou diretório no qual ocorreu um erro da chamada do método anterior.</span><span class="sxs-lookup"><span data-stu-id="823ca-133">Typically, the *StartFileName* parameter is the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="823ca-134">Se esse parâmetro for **nulo**, a operação será executada no arquivo (ou diretório) especificado na chamada de [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="823ca-134">If this parameter is **null**, the operation is performed on the file (or directory) specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="823ca-135">*Recursivo* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="823ca-135">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="823ca-136">Se **for true**, o método também será aplicado recursivamente a arquivos e diretórios dentro do diretório especificado pela instância do [**\_ dispositivo CIM**](cim-devicefile.md) .</span><span class="sxs-lookup"><span data-stu-id="823ca-136">If **TRUE**, the method is also applied recursively to files and directories within the directory specified by the [**CIM\_DeviceFile**](cim-devicefile.md) instance.</span></span> <span data-ttu-id="823ca-137">Para instâncias de arquivo, esse parâmetro é ignorado.</span><span class="sxs-lookup"><span data-stu-id="823ca-137">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="823ca-138">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="823ca-138">Return value</span></span>

<span data-ttu-id="823ca-139">Retorna um valor de 0 (zero) em caso de êxito e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="823ca-139">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="823ca-140">0</span><span class="sxs-lookup"><span data-stu-id="823ca-140">0</span></span>

<span data-ttu-id="823ca-141">Sucesso.</span><span class="sxs-lookup"><span data-stu-id="823ca-141">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="823ca-142">2</span><span class="sxs-lookup"><span data-stu-id="823ca-142">2</span></span>

<span data-ttu-id="823ca-143">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="823ca-143">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="823ca-144">8</span><span class="sxs-lookup"><span data-stu-id="823ca-144">8</span></span>

<span data-ttu-id="823ca-145">Falha não especificada.</span><span class="sxs-lookup"><span data-stu-id="823ca-145">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="823ca-146">9</span><span class="sxs-lookup"><span data-stu-id="823ca-146">9</span></span>

<span data-ttu-id="823ca-147">Objeto inválido.</span><span class="sxs-lookup"><span data-stu-id="823ca-147">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="823ca-148">10</span><span class="sxs-lookup"><span data-stu-id="823ca-148">10</span></span>

<span data-ttu-id="823ca-149">O objeto já existe.</span><span class="sxs-lookup"><span data-stu-id="823ca-149">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="823ca-150">11</span><span class="sxs-lookup"><span data-stu-id="823ca-150">11</span></span>

<span data-ttu-id="823ca-151">Sistema de arquivos não NTFS.</span><span class="sxs-lookup"><span data-stu-id="823ca-151">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="823ca-152">12</span><span class="sxs-lookup"><span data-stu-id="823ca-152">12</span></span>

<span data-ttu-id="823ca-153">Plataforma não Windows.</span><span class="sxs-lookup"><span data-stu-id="823ca-153">Platform not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="823ca-154">13</span><span class="sxs-lookup"><span data-stu-id="823ca-154">13</span></span>

<span data-ttu-id="823ca-155">A unidade não é a mesma.</span><span class="sxs-lookup"><span data-stu-id="823ca-155">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="823ca-156">14</span><span class="sxs-lookup"><span data-stu-id="823ca-156">14</span></span>

<span data-ttu-id="823ca-157">O diretório não está vazio.</span><span class="sxs-lookup"><span data-stu-id="823ca-157">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="823ca-158">15</span><span class="sxs-lookup"><span data-stu-id="823ca-158">15</span></span>

<span data-ttu-id="823ca-159">Violação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="823ca-159">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="823ca-160">16</span><span class="sxs-lookup"><span data-stu-id="823ca-160">16</span></span>

<span data-ttu-id="823ca-161">Arquivo inicial inválido.</span><span class="sxs-lookup"><span data-stu-id="823ca-161">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="823ca-162">17</span><span class="sxs-lookup"><span data-stu-id="823ca-162">17</span></span>

<span data-ttu-id="823ca-163">Privilégio não mantido.</span><span class="sxs-lookup"><span data-stu-id="823ca-163">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="823ca-164">21</span><span class="sxs-lookup"><span data-stu-id="823ca-164">21</span></span>

<span data-ttu-id="823ca-165">Parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="823ca-165">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="823ca-166">Comentários</span><span class="sxs-lookup"><span data-stu-id="823ca-166">Remarks</span></span>

<span data-ttu-id="823ca-167">Este método não está implementado no momento pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="823ca-167">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="823ca-168">Para usar esse método, você deve implementá-lo em seu próprio provedor.</span><span class="sxs-lookup"><span data-stu-id="823ca-168">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="823ca-169">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="823ca-169">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="823ca-170">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="823ca-170">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="823ca-171">Requisitos</span><span class="sxs-lookup"><span data-stu-id="823ca-171">Requirements</span></span>



| <span data-ttu-id="823ca-172">Requisito</span><span class="sxs-lookup"><span data-stu-id="823ca-172">Requirement</span></span> | <span data-ttu-id="823ca-173">Valor</span><span class="sxs-lookup"><span data-stu-id="823ca-173">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="823ca-174">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="823ca-174">Minimum supported client</span></span><br/> | <span data-ttu-id="823ca-175">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="823ca-175">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="823ca-176">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="823ca-176">Minimum supported server</span></span><br/> | <span data-ttu-id="823ca-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="823ca-177">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="823ca-178">Namespace</span><span class="sxs-lookup"><span data-stu-id="823ca-178">Namespace</span></span><br/>                | <span data-ttu-id="823ca-179">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="823ca-179">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="823ca-180">MOF</span><span class="sxs-lookup"><span data-stu-id="823ca-180">MOF</span></span><br/>                      | <dl> <span data-ttu-id="823ca-181"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="823ca-181"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="823ca-182">DLL</span><span class="sxs-lookup"><span data-stu-id="823ca-182">DLL</span></span><br/>                      | <dl> <span data-ttu-id="823ca-183"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="823ca-183"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="823ca-184">Confira também</span><span class="sxs-lookup"><span data-stu-id="823ca-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="823ca-185">\_Dispositivo CIM</span><span class="sxs-lookup"><span data-stu-id="823ca-185">CIM\_DeviceFile</span></span>](changesecuritypermissionsex-method-in-class-cim-devicefile.md)
</dt> <dt>

[<span data-ttu-id="823ca-186">**\_Dispositivo CIM**</span><span class="sxs-lookup"><span data-stu-id="823ca-186">**CIM\_DeviceFile**</span></span>](cim-devicefile.md)
</dt> </dl>

 

