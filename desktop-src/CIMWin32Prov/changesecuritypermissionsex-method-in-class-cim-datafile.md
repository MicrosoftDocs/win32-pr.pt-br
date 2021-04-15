---
description: Altera as permissões de segurança para o arquivo de dados lógicos especificado no caminho do objeto (esse método é uma versão estendida do método ChangeSecurityPermissions).
ms.assetid: baf50a6e-f624-464e-946d-975aeba88ac2
ms.tgt_platform: multiple
title: Método ChangeSecurityPermissionsEx da classe CIM_DataFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.ChangeSecurityPermissionsEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3c97f9b17fd148a0686a96fb46f77694a2b78b21
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500986"
---
# <a name="changesecuritypermissionsex-method-of-the-cim_datafile-class"></a><span data-ttu-id="9cd5c-103">Método ChangeSecurityPermissionsEx da classe de \_ datafilefiles CIM</span><span class="sxs-lookup"><span data-stu-id="9cd5c-103">ChangeSecurityPermissionsEx method of the CIM\_DataFile class</span></span>

<span data-ttu-id="9cd5c-104">O método **ChangeSecurityPermissionsEx** altera as permissões de segurança para o arquivo de dados lógicos especificado no caminho do objeto (esse método é uma versão estendida do método [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-cim-datafile.md) ).</span><span class="sxs-lookup"><span data-stu-id="9cd5c-104">The **ChangeSecurityPermissionsEx** method changes the security permissions for the logical data file specified in the object path (this method is an extended version of the [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-cim-datafile.md) method).</span></span> <span data-ttu-id="9cd5c-105">Se o arquivo lógico for realmente um diretório, esse método agirá recursivamente, alterando as permissões de segurança para todos os arquivos e subdiretórios que o diretório contém.</span><span class="sxs-lookup"><span data-stu-id="9cd5c-105">If the logical file is actually a directory, then this method will act recursively, changing the security permissions for all of the files and sub-directories that the directory contains.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9cd5c-106">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="9cd5c-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="9cd5c-107">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="9cd5c-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="9cd5c-108">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="9cd5c-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="9cd5c-109">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="9cd5c-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="9cd5c-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9cd5c-110">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissionsEx(
  [in]           Win32_SecurityDescriptor SecurityDescriptor,
  [in]           uint32                   Option,
  [out]          string                   StopFileName,
  [in, optional] string                   StartFileName,
  [in, optional] boolean                  Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="9cd5c-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9cd5c-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9cd5c-112">*SecurityDescriptor* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9cd5c-112">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9cd5c-113">Especifica informações de segurança.</span><span class="sxs-lookup"><span data-stu-id="9cd5c-113">Specifies security information.</span></span>

> [!Note]  
> <span data-ttu-id="9cd5c-114">Uma ACL **nula** na estrutura [**do \_ descritor de segurança**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) concede acesso ilimitado.</span><span class="sxs-lookup"><span data-stu-id="9cd5c-114">A **NULL** ACL in the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure grants unlimited access.</span></span> <span data-ttu-id="9cd5c-115">Para obter mais informações sobre as implicações de acesso ilimitado, consulte [criando um descritor de segurança para um novo objeto](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span><span class="sxs-lookup"><span data-stu-id="9cd5c-115">For more information about the implications of unlimited access, see [Creating a Security Descriptor for a New Object](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span></span>

 

</dd> <dt>

<span data-ttu-id="9cd5c-116">*Opção* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9cd5c-116">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9cd5c-117">Privilégio de segurança a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="9cd5c-117">Security privilege to modify.</span></span> <span data-ttu-id="9cd5c-118">Por exemplo, para alterar a segurança do proprietário e da DACL, use:</span><span class="sxs-lookup"><span data-stu-id="9cd5c-118">For example, to change the owner and DACL security, use:</span></span>

<span data-ttu-id="9cd5c-119">`Option = 1 + 4` ou `Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`</span><span class="sxs-lookup"><span data-stu-id="9cd5c-119">`Option = 1 + 4` or `Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`</span></span>

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span data-ttu-id="9cd5c-120"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**Alterar \_ \_ \_ Informações de segurança do proprietário** (1)</span><span class="sxs-lookup"><span data-stu-id="9cd5c-120"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE\_OWNER\_SECURITY\_INFORMATION** (1)</span></span>


</dt> <dd>

<span data-ttu-id="9cd5c-121">Altere o proprietário do arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="9cd5c-121">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span data-ttu-id="9cd5c-122"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**Alterar \_ \_ \_ Informações de segurança do grupo** (2)</span><span class="sxs-lookup"><span data-stu-id="9cd5c-122"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE\_GROUP\_SECURITY\_INFORMATION** (2)</span></span>


</dt> <dd>

<span data-ttu-id="9cd5c-123">Altere o grupo do arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="9cd5c-123">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span data-ttu-id="9cd5c-124"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**Alterar \_ \_ \_ Informações de segurança da DACL** (4)</span><span class="sxs-lookup"><span data-stu-id="9cd5c-124"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE\_DACL\_SECURITY\_INFORMATION** (4)</span></span>


</dt> <dd>

<span data-ttu-id="9cd5c-125">Altere a ACL do arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="9cd5c-125">Change the ACL of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span data-ttu-id="9cd5c-126"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Alterar \_ \_ \_ Informações de segurança da SACL** (8)</span><span class="sxs-lookup"><span data-stu-id="9cd5c-126"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE\_SACL\_SECURITY\_INFORMATION** (8)</span></span>


</dt> <dd>

<span data-ttu-id="9cd5c-127">Altere a ACL do sistema do arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="9cd5c-127">Change the system ACL of the logical file.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="9cd5c-128">*StopFileName* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="9cd5c-128">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9cd5c-129">Cadeia de caracteres que representa o nome do arquivo (ou diretório) em que o método falhou.</span><span class="sxs-lookup"><span data-stu-id="9cd5c-129">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="9cd5c-130">Esse parâmetro será **nulo** se o método tiver sucesso.</span><span class="sxs-lookup"><span data-stu-id="9cd5c-130">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="9cd5c-131">*StartFileName* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="9cd5c-131">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9cd5c-132">Cadeia de caracteres que representa o arquivo filho (ou diretório) a ser usado como ponto de partida para esse método.</span><span class="sxs-lookup"><span data-stu-id="9cd5c-132">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="9cd5c-133">Normalmente, o parâmetro *StartFileName* é o parâmetro *StopFileName* que especifica o arquivo ou diretório no qual ocorreu um erro da chamada do método anterior.</span><span class="sxs-lookup"><span data-stu-id="9cd5c-133">Typically, the *StartFileName* parameter is the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="9cd5c-134">Se esse parâmetro for **nulo**, a operação será executada no arquivo (ou diretório) especificado na chamada de **ExecMethod** .</span><span class="sxs-lookup"><span data-stu-id="9cd5c-134">If this parameter is **null**, the operation is performed on the file (or directory) specified in the **ExecMethod** call.</span></span>

<span data-ttu-id="9cd5c-135">Se o *StartFileName* for usado, *recursivo* deverá ser definido como true também.</span><span class="sxs-lookup"><span data-stu-id="9cd5c-135">If *StartFileName* is used, *Recursive* must be set to true as well.</span></span>

</dd> <dt>

<span data-ttu-id="9cd5c-136">*Recursivo* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="9cd5c-136">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9cd5c-137">Se **for true**, o método também será aplicado recursivamente a arquivos e diretórios dentro do diretório especificado pela instância de [**\_ DataFile do CIM**](cim-datafile.md) .</span><span class="sxs-lookup"><span data-stu-id="9cd5c-137">If **True**, the method is also applied recursively to files and directories within the directory that is specified by the [**CIM\_DataFile**](cim-datafile.md) instance.</span></span> <span data-ttu-id="9cd5c-138">Para instâncias de arquivo, esse parâmetro é ignorado.</span><span class="sxs-lookup"><span data-stu-id="9cd5c-138">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9cd5c-139">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9cd5c-139">Return value</span></span>

<span data-ttu-id="9cd5c-140">Retorna um valor de 0 (zero) em caso de êxito e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="9cd5c-140">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span> <span data-ttu-id="9cd5c-141">Para obter códigos de erro adicionais, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="9cd5c-141">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="9cd5c-142">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="9cd5c-142">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="9cd5c-143">**Êxito**</span><span class="sxs-lookup"><span data-stu-id="9cd5c-143">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="9cd5c-144">0</span><span class="sxs-lookup"><span data-stu-id="9cd5c-144">0</span></span>

<span data-ttu-id="9cd5c-145">Sucesso.</span><span class="sxs-lookup"><span data-stu-id="9cd5c-145">Success.</span></span>

</dd> <dt>

<span data-ttu-id="9cd5c-146">**Acesso negado**</span><span class="sxs-lookup"><span data-stu-id="9cd5c-146">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="9cd5c-147">2</span><span class="sxs-lookup"><span data-stu-id="9cd5c-147">2</span></span>

<span data-ttu-id="9cd5c-148">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="9cd5c-148">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="9cd5c-149">**Falha não especificada**</span><span class="sxs-lookup"><span data-stu-id="9cd5c-149">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="9cd5c-150">8</span><span class="sxs-lookup"><span data-stu-id="9cd5c-150">8</span></span>

<span data-ttu-id="9cd5c-151">Falha não especificada.</span><span class="sxs-lookup"><span data-stu-id="9cd5c-151">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="9cd5c-152">**Objeto inválido**</span><span class="sxs-lookup"><span data-stu-id="9cd5c-152">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="9cd5c-153">9</span><span class="sxs-lookup"><span data-stu-id="9cd5c-153">9</span></span>

<span data-ttu-id="9cd5c-154">O nome de objeto especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="9cd5c-154">Object name specified is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="9cd5c-155">**O objeto já existe**</span><span class="sxs-lookup"><span data-stu-id="9cd5c-155">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="9cd5c-156">10</span><span class="sxs-lookup"><span data-stu-id="9cd5c-156">10</span></span>

<span data-ttu-id="9cd5c-157">O objeto já existe.</span><span class="sxs-lookup"><span data-stu-id="9cd5c-157">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="9cd5c-158">**Sistema de arquivos não NTFS**</span><span class="sxs-lookup"><span data-stu-id="9cd5c-158">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="9cd5c-159">11</span><span class="sxs-lookup"><span data-stu-id="9cd5c-159">11</span></span>

<span data-ttu-id="9cd5c-160">Sistema de arquivos não NTFS.</span><span class="sxs-lookup"><span data-stu-id="9cd5c-160">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="9cd5c-161">**Plataforma não NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="9cd5c-161">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="9cd5c-162">12</span><span class="sxs-lookup"><span data-stu-id="9cd5c-162">12</span></span>

<span data-ttu-id="9cd5c-163">Plataforma não Windows.</span><span class="sxs-lookup"><span data-stu-id="9cd5c-163">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="9cd5c-164">**A unidade não é a mesma**</span><span class="sxs-lookup"><span data-stu-id="9cd5c-164">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="9cd5c-165">13</span><span class="sxs-lookup"><span data-stu-id="9cd5c-165">13</span></span>

<span data-ttu-id="9cd5c-166">A unidade não é a mesma.</span><span class="sxs-lookup"><span data-stu-id="9cd5c-166">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="9cd5c-167">**Diretório não vazio**</span><span class="sxs-lookup"><span data-stu-id="9cd5c-167">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="9cd5c-168">14</span><span class="sxs-lookup"><span data-stu-id="9cd5c-168">14</span></span>

<span data-ttu-id="9cd5c-169">O diretório não está vazio.</span><span class="sxs-lookup"><span data-stu-id="9cd5c-169">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="9cd5c-170">**Violação de compartilhamento**</span><span class="sxs-lookup"><span data-stu-id="9cd5c-170">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="9cd5c-171">15</span><span class="sxs-lookup"><span data-stu-id="9cd5c-171">15</span></span>

<span data-ttu-id="9cd5c-172">Violação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="9cd5c-172">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="9cd5c-173">**Arquivo de início inválido**</span><span class="sxs-lookup"><span data-stu-id="9cd5c-173">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="9cd5c-174">16</span><span class="sxs-lookup"><span data-stu-id="9cd5c-174">16</span></span>

<span data-ttu-id="9cd5c-175">O arquivo de inicialização não é válido.</span><span class="sxs-lookup"><span data-stu-id="9cd5c-175">The start file is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="9cd5c-176">**Privilégio não mantido**</span><span class="sxs-lookup"><span data-stu-id="9cd5c-176">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="9cd5c-177">17</span><span class="sxs-lookup"><span data-stu-id="9cd5c-177">17</span></span>

<span data-ttu-id="9cd5c-178">Privilégio não mantido.</span><span class="sxs-lookup"><span data-stu-id="9cd5c-178">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="9cd5c-179">**Parâmetro inválido**</span><span class="sxs-lookup"><span data-stu-id="9cd5c-179">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="9cd5c-180">21</span><span class="sxs-lookup"><span data-stu-id="9cd5c-180">21</span></span>

<span data-ttu-id="9cd5c-181">Um parâmetro não é válido.</span><span class="sxs-lookup"><span data-stu-id="9cd5c-181">A parameter is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9cd5c-182">Comentários</span><span class="sxs-lookup"><span data-stu-id="9cd5c-182">Remarks</span></span>

<span data-ttu-id="9cd5c-183">O método **ChangeSecurityPermissionsEx** no [**\_ arquivo CIM**](cim-datafile.md) é implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="9cd5c-183">The **ChangeSecurityPermissionsEx** method in [**CIM\_DataFile**](cim-datafile.md) is implemented by WMI.</span></span>

<span data-ttu-id="9cd5c-184">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="9cd5c-184">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="9cd5c-185">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="9cd5c-185">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="9cd5c-186">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9cd5c-186">Requirements</span></span>



| <span data-ttu-id="9cd5c-187">Requisito</span><span class="sxs-lookup"><span data-stu-id="9cd5c-187">Requirement</span></span> | <span data-ttu-id="9cd5c-188">Valor</span><span class="sxs-lookup"><span data-stu-id="9cd5c-188">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9cd5c-189">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9cd5c-189">Minimum supported client</span></span><br/> | <span data-ttu-id="9cd5c-190">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9cd5c-190">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9cd5c-191">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9cd5c-191">Minimum supported server</span></span><br/> | <span data-ttu-id="9cd5c-192">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9cd5c-192">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9cd5c-193">Namespace</span><span class="sxs-lookup"><span data-stu-id="9cd5c-193">Namespace</span></span><br/>                | <span data-ttu-id="9cd5c-194">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="9cd5c-194">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9cd5c-195">MOF</span><span class="sxs-lookup"><span data-stu-id="9cd5c-195">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9cd5c-196"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9cd5c-196"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9cd5c-197">DLL</span><span class="sxs-lookup"><span data-stu-id="9cd5c-197">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9cd5c-198"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9cd5c-198"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9cd5c-199">Confira também</span><span class="sxs-lookup"><span data-stu-id="9cd5c-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9cd5c-200">**DataFile de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="9cd5c-200">**CIM\_DataFile**</span></span>](changesecuritypermissionsex-method-in-class-cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="9cd5c-201">**DataFile de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="9cd5c-201">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="9cd5c-202">Tarefas do WMI: arquivos e pastas</span><span class="sxs-lookup"><span data-stu-id="9cd5c-202">WMI Tasks: Files and Folders</span></span>](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[<span data-ttu-id="9cd5c-203">**Constantes de direitos de acesso de arquivo e diretório**</span><span class="sxs-lookup"><span data-stu-id="9cd5c-203">**File and Directory Access Rights Constants**</span></span>](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

