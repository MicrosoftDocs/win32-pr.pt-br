---
description: Obtém a propriedade do arquivo de entrada de diretório lógico especificado no caminho do objeto. Esse método é uma versão estendida do método TakeOwnerShip.
ms.assetid: 73726207-e885-4957-bff8-6903c4b99278
ms.tgt_platform: multiple
title: Método TakeOwnerShipEx da classe Win32_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.TakeOwnerShipEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2e391e942e581d0f80d46b0f59b9b273d7bff499
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105755663"
---
# <a name="takeownershipex-method-of-the-win32_directory-class"></a><span data-ttu-id="61bbd-104">Método TakeOwnerShipEx da classe do \_ diretório Win32</span><span class="sxs-lookup"><span data-stu-id="61bbd-104">TakeOwnerShipEx method of the Win32\_Directory class</span></span>

<span data-ttu-id="61bbd-105">O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **TakeOwnerShipEx** Obtém a propriedade do arquivo de entrada de diretório lógico especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="61bbd-105">The **TakeOwnerShipEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method obtains ownership of the logical directory entry file specified in the object path.</span></span> <span data-ttu-id="61bbd-106">Esse método é uma versão estendida do método [**TakeOwnership**](takeownership-method-in-class-win32-directory.md) .</span><span class="sxs-lookup"><span data-stu-id="61bbd-106">This method is an extended version of the [**TakeOwnerShip**](takeownership-method-in-class-win32-directory.md) method.</span></span> <span data-ttu-id="61bbd-107">Se o arquivo lógico for, na verdade, um diretório, esse método agirá recursivamente, assumindo a propriedade de todos os arquivos e subdiretórios contidos no diretório.</span><span class="sxs-lookup"><span data-stu-id="61bbd-107">If the logical file is actually a directory, then this method acts recursively, taking ownership of all of the files and subdirectories the directory contains.</span></span>

<span data-ttu-id="61bbd-108">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="61bbd-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="61bbd-109">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="61bbd-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="61bbd-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="61bbd-110">Syntax</span></span>


```mof
uint32 TakeOwnerShipEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="61bbd-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="61bbd-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61bbd-112">*StopFileName* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="61bbd-112">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="61bbd-113">Nome do arquivo ou diretório em que o método **TakeOwnerShipEx** falhou.</span><span class="sxs-lookup"><span data-stu-id="61bbd-113">Name of the file or directory where the **TakeOwnerShipEx** method failed.</span></span> <span data-ttu-id="61bbd-114">Esse parâmetro será **nulo** se o método tiver sucesso.</span><span class="sxs-lookup"><span data-stu-id="61bbd-114">This parameter is **NULL** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="61bbd-115">*StartFileName* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="61bbd-115">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="61bbd-116">Nomeia o arquivo ou diretório filho a ser usado como ponto de partida para **TakeOwnerShipEx**.</span><span class="sxs-lookup"><span data-stu-id="61bbd-116">Names the child file or directory to use as a starting point for **TakeOwnerShipEx**.</span></span> <span data-ttu-id="61bbd-117">O parâmetro *StartFileName* normalmente é o parâmetro *StopFileName* que especifica o arquivo ou diretório no qual ocorreu um erro da chamada do método anterior.</span><span class="sxs-lookup"><span data-stu-id="61bbd-117">The *StartFileName* parameter is typically the *StopFileName* parameter that specifies the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="61bbd-118">Se esse parâmetro for **nulo**, a operação será executada no arquivo ou diretório especificado na chamada de [**ExecMethod**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="61bbd-118">If this parameter is **NULL**, the operation is performed on the file or directory specified in the [**ExecMethod**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execmethod) call.</span></span>

<span data-ttu-id="61bbd-119">Se o *StartFileName* for usado, *recursivo* deverá ser definido como true também.</span><span class="sxs-lookup"><span data-stu-id="61bbd-119">If *StartFileName* is used, *Recursive* must be set to true as well.</span></span>

</dd> <dt>

<span data-ttu-id="61bbd-120">*Recursivo* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="61bbd-120">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="61bbd-121">Se for **true**, a alteração de propriedade será aplicada recursivamente aos arquivos e diretórios dentro do diretório especificado pela instância de [**\_ LogicalFile do CIM**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="61bbd-121">If **True**, the change of ownership is applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span>

> [!Note]  
> <span data-ttu-id="61bbd-122">Para instâncias de arquivo, o parâmetro de entrada *recursivo* é ignorado.</span><span class="sxs-lookup"><span data-stu-id="61bbd-122">For file instances, the *Recursive* input parameter is ignored.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61bbd-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="61bbd-123">Return value</span></span>

<span data-ttu-id="61bbd-124">Retorna um valor inteiro de 0 (zero) em caso de êxito e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="61bbd-124">Returns an integer value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="61bbd-125">**0**</span><span class="sxs-lookup"><span data-stu-id="61bbd-125">**0**</span></span>
</dt> <dd>

<span data-ttu-id="61bbd-126">A solicitação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="61bbd-126">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="61bbd-127">**2**</span><span class="sxs-lookup"><span data-stu-id="61bbd-127">**2**</span></span>
</dt> <dd>

<span data-ttu-id="61bbd-128">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="61bbd-128">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="61bbd-129">**8**</span><span class="sxs-lookup"><span data-stu-id="61bbd-129">**8**</span></span>
</dt> <dd>

<span data-ttu-id="61bbd-130">Ocorreu uma falha não especificada.</span><span class="sxs-lookup"><span data-stu-id="61bbd-130">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="61bbd-131">**9**</span><span class="sxs-lookup"><span data-stu-id="61bbd-131">**9**</span></span>
</dt> <dd>

<span data-ttu-id="61bbd-132">O nome especificado não era válido.</span><span class="sxs-lookup"><span data-stu-id="61bbd-132">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="61bbd-133">**10**</span><span class="sxs-lookup"><span data-stu-id="61bbd-133">**10**</span></span>
</dt> <dd>

<span data-ttu-id="61bbd-134">O objeto especificado já existe.</span><span class="sxs-lookup"><span data-stu-id="61bbd-134">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="61bbd-135">**11**</span><span class="sxs-lookup"><span data-stu-id="61bbd-135">**11**</span></span>
</dt> <dd>

<span data-ttu-id="61bbd-136">O sistema de arquivos não é NTFS.</span><span class="sxs-lookup"><span data-stu-id="61bbd-136">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="61bbd-137">**12**</span><span class="sxs-lookup"><span data-stu-id="61bbd-137">**12**</span></span>
</dt> <dd>

<span data-ttu-id="61bbd-138">A plataforma não é o Windows.</span><span class="sxs-lookup"><span data-stu-id="61bbd-138">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="61bbd-139">**13**</span><span class="sxs-lookup"><span data-stu-id="61bbd-139">**13**</span></span>
</dt> <dd>

<span data-ttu-id="61bbd-140">A unidade não é a mesma.</span><span class="sxs-lookup"><span data-stu-id="61bbd-140">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="61bbd-141">**14**</span><span class="sxs-lookup"><span data-stu-id="61bbd-141">**14**</span></span>
</dt> <dd>

<span data-ttu-id="61bbd-142">O diretório não está vazio.</span><span class="sxs-lookup"><span data-stu-id="61bbd-142">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="61bbd-143">**15**</span><span class="sxs-lookup"><span data-stu-id="61bbd-143">**15**</span></span>
</dt> <dd>

<span data-ttu-id="61bbd-144">Houve uma violação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="61bbd-144">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="61bbd-145">**16**</span><span class="sxs-lookup"><span data-stu-id="61bbd-145">**16**</span></span>
</dt> <dd>

<span data-ttu-id="61bbd-146">O arquivo de inicialização especificado não era válido.</span><span class="sxs-lookup"><span data-stu-id="61bbd-146">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="61bbd-147">**17**</span><span class="sxs-lookup"><span data-stu-id="61bbd-147">**17**</span></span>
</dt> <dd>

<span data-ttu-id="61bbd-148">Um privilégio necessário para a operação não é mantido.</span><span class="sxs-lookup"><span data-stu-id="61bbd-148">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="61bbd-149">**Abril**</span><span class="sxs-lookup"><span data-stu-id="61bbd-149">**21**</span></span>
</dt> <dd>

<span data-ttu-id="61bbd-150">Um parâmetro especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="61bbd-150">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="61bbd-151">Exemplos</span><span class="sxs-lookup"><span data-stu-id="61bbd-151">Examples</span></span>

<span data-ttu-id="61bbd-152">O código de script Visual Basic a seguir chama o método [**TakeOwnerShipEx**](takeownershipex-method-in-class-cim-directory.md) para apropriar-se da pasta C: \\ Temp.</span><span class="sxs-lookup"><span data-stu-id="61bbd-152">The following Visual Basic Script code calls the [**TakeOwnerShipEx**](takeownershipex-method-in-class-cim-directory.md) method to take ownership of the C:\\temp folder.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 
' Obtain the definition of the class.
Set objShare = objWMIService.Get("Win32_Directory")
' Obtain an InParameters object specific
' to the method.
Set objInParam = objShare.Methods_("TakeOwnerShipEx").inParameters.SpawnInstance_()

' Add the input parameters.
objInParam.Properties_.Item("Recursive") =  true

' Execute the method and obtain the return status.
' The OutParameters object in objOutParams
' is created by the provider.
Set objOutParams = objWMIService.ExecMethod("Win32_Directory.Name='C:\Temp'", "TakeOwnerShipEx", objInParam)
wscript.echo objOutParams.ReturnValue
```



## <a name="requirements"></a><span data-ttu-id="61bbd-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61bbd-153">Requirements</span></span>



| <span data-ttu-id="61bbd-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="61bbd-154">Requirement</span></span> | <span data-ttu-id="61bbd-155">Valor</span><span class="sxs-lookup"><span data-stu-id="61bbd-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="61bbd-156">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="61bbd-156">Minimum supported client</span></span><br/> | <span data-ttu-id="61bbd-157">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="61bbd-157">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="61bbd-158">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="61bbd-158">Minimum supported server</span></span><br/> | <span data-ttu-id="61bbd-159">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="61bbd-159">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="61bbd-160">Namespace</span><span class="sxs-lookup"><span data-stu-id="61bbd-160">Namespace</span></span><br/>                | <span data-ttu-id="61bbd-161">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="61bbd-161">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="61bbd-162">MOF</span><span class="sxs-lookup"><span data-stu-id="61bbd-162">MOF</span></span><br/>                      | <dl> <span data-ttu-id="61bbd-163"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="61bbd-163"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="61bbd-164">DLL</span><span class="sxs-lookup"><span data-stu-id="61bbd-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="61bbd-165"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="61bbd-165"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61bbd-166">Confira também</span><span class="sxs-lookup"><span data-stu-id="61bbd-166">See also</span></span>

<dl> <dt>

<span data-ttu-id="61bbd-167">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="61bbd-167">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="61bbd-168">**\_Diretório Win32**</span><span class="sxs-lookup"><span data-stu-id="61bbd-168">**Win32\_Directory**</span></span>](win32-directory.md)
</dt> </dl>

 

