---
description: O método de classe WMI TakeOwnerShip Obtém a propriedade do arquivo lógico especificado no caminho do objeto.
ms.assetid: 1112823b-0bb6-4dc0-a5c4-8d3839a47a3a
ms.tgt_platform: multiple
title: Método TakeOwnerShip da classe Win32_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.TakeOwnerShip
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c06441b7728ed8b9178e889cbd60c047f0f3a497
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500790"
---
# <a name="takeownership-method-of-the-win32_directory-class"></a><span data-ttu-id="77f77-103">Método TakeOwnerShip da classe do \_ diretório Win32</span><span class="sxs-lookup"><span data-stu-id="77f77-103">TakeOwnerShip method of the Win32\_Directory class</span></span>

<span data-ttu-id="77f77-104">O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **TakeOwnership** Obtém a propriedade do arquivo lógico especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="77f77-104">The **TakeOwnerShip** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="77f77-105">Se o arquivo lógico for realmente um diretório, o **TakeOwnership** agirá recursivamente, assumindo a propriedade de todos os arquivos e subdiretórios contidos no diretório.</span><span class="sxs-lookup"><span data-stu-id="77f77-105">If the logical file is actually a directory, then **TakeOwnerShip** acts recursively, taking ownership of all of the files and subdirectories the directory contains.</span></span>

<span data-ttu-id="77f77-106">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="77f77-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="77f77-107">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="77f77-107">For more information about using this method see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="77f77-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="77f77-108">Syntax</span></span>


```mof
uint32 TakeOwnerShip();
```



## <a name="parameters"></a><span data-ttu-id="77f77-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="77f77-109">Parameters</span></span>

<span data-ttu-id="77f77-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="77f77-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="77f77-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="77f77-111">Return value</span></span>

<span data-ttu-id="77f77-112">Retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="77f77-112">Returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="77f77-113">**0**</span><span class="sxs-lookup"><span data-stu-id="77f77-113">**0**</span></span>
</dt> <dd>

<span data-ttu-id="77f77-114">A solicitação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="77f77-114">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="77f77-115">**2**</span><span class="sxs-lookup"><span data-stu-id="77f77-115">**2**</span></span>
</dt> <dd>

<span data-ttu-id="77f77-116">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="77f77-116">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="77f77-117">**8**</span><span class="sxs-lookup"><span data-stu-id="77f77-117">**8**</span></span>
</dt> <dd>

<span data-ttu-id="77f77-118">Ocorreu uma falha não especificada.</span><span class="sxs-lookup"><span data-stu-id="77f77-118">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="77f77-119">**9**</span><span class="sxs-lookup"><span data-stu-id="77f77-119">**9**</span></span>
</dt> <dd>

<span data-ttu-id="77f77-120">O nome especificado não era válido.</span><span class="sxs-lookup"><span data-stu-id="77f77-120">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="77f77-121">**10**</span><span class="sxs-lookup"><span data-stu-id="77f77-121">**10**</span></span>
</dt> <dd>

<span data-ttu-id="77f77-122">O objeto especificado já existe.</span><span class="sxs-lookup"><span data-stu-id="77f77-122">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="77f77-123">**11**</span><span class="sxs-lookup"><span data-stu-id="77f77-123">**11**</span></span>
</dt> <dd>

<span data-ttu-id="77f77-124">O sistema de arquivos não é NTFS.</span><span class="sxs-lookup"><span data-stu-id="77f77-124">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="77f77-125">**12**</span><span class="sxs-lookup"><span data-stu-id="77f77-125">**12**</span></span>
</dt> <dd>

<span data-ttu-id="77f77-126">A plataforma não é o Windows.</span><span class="sxs-lookup"><span data-stu-id="77f77-126">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="77f77-127">**13**</span><span class="sxs-lookup"><span data-stu-id="77f77-127">**13**</span></span>
</dt> <dd>

<span data-ttu-id="77f77-128">A unidade não é a mesma.</span><span class="sxs-lookup"><span data-stu-id="77f77-128">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="77f77-129">**14**</span><span class="sxs-lookup"><span data-stu-id="77f77-129">**14**</span></span>
</dt> <dd>

<span data-ttu-id="77f77-130">O diretório não está vazio.</span><span class="sxs-lookup"><span data-stu-id="77f77-130">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="77f77-131">**15**</span><span class="sxs-lookup"><span data-stu-id="77f77-131">**15**</span></span>
</dt> <dd>

<span data-ttu-id="77f77-132">Houve uma violação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="77f77-132">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="77f77-133">**16**</span><span class="sxs-lookup"><span data-stu-id="77f77-133">**16**</span></span>
</dt> <dd>

<span data-ttu-id="77f77-134">O arquivo de inicialização especificado não era válido.</span><span class="sxs-lookup"><span data-stu-id="77f77-134">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="77f77-135">**17**</span><span class="sxs-lookup"><span data-stu-id="77f77-135">**17**</span></span>
</dt> <dd>

<span data-ttu-id="77f77-136">Um privilégio necessário para a operação não é mantido.</span><span class="sxs-lookup"><span data-stu-id="77f77-136">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="77f77-137">**Abril**</span><span class="sxs-lookup"><span data-stu-id="77f77-137">**21**</span></span>
</dt> <dd>

<span data-ttu-id="77f77-138">Um parâmetro especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="77f77-138">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="77f77-139">Exemplos</span><span class="sxs-lookup"><span data-stu-id="77f77-139">Examples</span></span>

<span data-ttu-id="77f77-140">O código de script Visual Basic a seguir chama o método [**TakeOwnership**](takeownership-method-in-class-cim-directory.md) para apropriar-se da pasta C: \\ Temp.</span><span class="sxs-lookup"><span data-stu-id="77f77-140">The following Visual Basic Script code calls the [**TakeOwnerShip**](takeownership-method-in-class-cim-directory.md) method to take ownership of the C:\\temp folder.</span></span>


```VB
strComputer = "." 

Set objWMIService = _
    GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 

' Obtain the definition of the class.
Set objShare = objWMIService.Get("Win32_Directory")

' Execute the method and obtain the return status.
' The OutParameters object in objOutParams
' is created by the provider.
Set objOutParams = objWMIService.ExecMethod( _
    "Win32_Directory.Name='C:\\temp'", "TakeOwnerShip")

wscript.echo objOutParams.ReturnValue
```



## <a name="requirements"></a><span data-ttu-id="77f77-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77f77-141">Requirements</span></span>



| <span data-ttu-id="77f77-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="77f77-142">Requirement</span></span> | <span data-ttu-id="77f77-143">Valor</span><span class="sxs-lookup"><span data-stu-id="77f77-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="77f77-144">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="77f77-144">Minimum supported client</span></span><br/> | <span data-ttu-id="77f77-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="77f77-145">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="77f77-146">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="77f77-146">Minimum supported server</span></span><br/> | <span data-ttu-id="77f77-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="77f77-147">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="77f77-148">Namespace</span><span class="sxs-lookup"><span data-stu-id="77f77-148">Namespace</span></span><br/>                | <span data-ttu-id="77f77-149">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="77f77-149">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="77f77-150">MOF</span><span class="sxs-lookup"><span data-stu-id="77f77-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="77f77-151"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="77f77-151"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="77f77-152">DLL</span><span class="sxs-lookup"><span data-stu-id="77f77-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="77f77-153"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="77f77-153"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77f77-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="77f77-154">See also</span></span>

<dl> <dt>

<span data-ttu-id="77f77-155">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="77f77-155">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="77f77-156">**\_Diretório Win32**</span><span class="sxs-lookup"><span data-stu-id="77f77-156">**Win32\_Directory**</span></span>](win32-directory.md)
</dt> </dl>

 

