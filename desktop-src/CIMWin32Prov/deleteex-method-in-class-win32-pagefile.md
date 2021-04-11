---
description: Exclui o arquivo de paginação lógica (ou diretório) especificado no caminho do objeto.
ms.assetid: ea31f92a-94b9-4d4d-abd9-6c304ac5caee
ms.tgt_platform: multiple
title: Método DeleteEx da classe Win32_PageFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFile.DeleteEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2f62875313f6be432ab191fc91bbac381627de3c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089113"
---
# <a name="deleteex-method-of-the-win32_pagefile-class"></a><span data-ttu-id="cc5a1-103">Método DeleteEx da classe de \_ arquivo de paginação Win32</span><span class="sxs-lookup"><span data-stu-id="cc5a1-103">DeleteEx method of the Win32\_PageFile class</span></span>

<span data-ttu-id="cc5a1-104">O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **DeleteEx** exclui o arquivo de paginação lógica (ou diretório) especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="cc5a1-104">The **DeleteEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method deletes the logical paging file (or directory) specified in the object path.</span></span> <span data-ttu-id="cc5a1-105">**DeleteEx** é uma versão estendida do método [**delete**](delete-method-in-class-win32-directory.md) .</span><span class="sxs-lookup"><span data-stu-id="cc5a1-105">**DeleteEx** is an extended version of the [**Delete**](delete-method-in-class-win32-directory.md) method.</span></span>

<span data-ttu-id="cc5a1-106">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="cc5a1-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="cc5a1-107">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="cc5a1-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="cc5a1-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cc5a1-108">Syntax</span></span>


```mof
uint32 DeleteEx(
  [out]          string StopFileName,
  [in, optional] string StartFileName
);
```



## <a name="parameters"></a><span data-ttu-id="cc5a1-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cc5a1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc5a1-110">*StopFileName* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="cc5a1-110">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cc5a1-111">Nome do arquivo ou diretório em que o método **DeleteEx** falhou.</span><span class="sxs-lookup"><span data-stu-id="cc5a1-111">Name of the file or directory where the **DeleteEx** method failed.</span></span> <span data-ttu-id="cc5a1-112">Esse parâmetro será **nulo** se o método tiver sucesso.</span><span class="sxs-lookup"><span data-stu-id="cc5a1-112">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="cc5a1-113">*StartFileName* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="cc5a1-113">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cc5a1-114">Nomeia o arquivo ou diretório filho a ser usado como ponto de partida para **DeleteEx**.</span><span class="sxs-lookup"><span data-stu-id="cc5a1-114">Names the child file or directory to use as a starting point for **DeleteEx**.</span></span> <span data-ttu-id="cc5a1-115">O parâmetro *StartFileName* normalmente é o parâmetro *StopFileName* que especifica o arquivo ou diretório no qual ocorreu um erro da chamada do método anterior.</span><span class="sxs-lookup"><span data-stu-id="cc5a1-115">The *StartFileName* parameter is typically the *StopFileName* parameter that specifies the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="cc5a1-116">Se esse parâmetro for **nulo**, a operação será executada no arquivo ou diretório especificado na chamada de ExecMethod.</span><span class="sxs-lookup"><span data-stu-id="cc5a1-116">If this parameter is **NULL**, the operation is performed on the file or directory specified in the ExecMethod call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc5a1-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cc5a1-117">Return value</span></span>

<span data-ttu-id="cc5a1-118">Retorna um valor de 0 (zero) se o arquivo foi excluído com êxito e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="cc5a1-118">Returns a value of 0 (zero) if the file was successfully deleted, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="cc5a1-119">**0**</span><span class="sxs-lookup"><span data-stu-id="cc5a1-119">**0**</span></span>
</dt> <dd>

<span data-ttu-id="cc5a1-120">A solicitação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="cc5a1-120">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="cc5a1-121">**2**</span><span class="sxs-lookup"><span data-stu-id="cc5a1-121">**2**</span></span>
</dt> <dd>

<span data-ttu-id="cc5a1-122">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="cc5a1-122">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="cc5a1-123">**8**</span><span class="sxs-lookup"><span data-stu-id="cc5a1-123">**8**</span></span>
</dt> <dd>

<span data-ttu-id="cc5a1-124">Ocorreu uma falha não especificada.</span><span class="sxs-lookup"><span data-stu-id="cc5a1-124">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="cc5a1-125">**9**</span><span class="sxs-lookup"><span data-stu-id="cc5a1-125">**9**</span></span>
</dt> <dd>

<span data-ttu-id="cc5a1-126">O nome especificado não era válido.</span><span class="sxs-lookup"><span data-stu-id="cc5a1-126">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="cc5a1-127">**10**</span><span class="sxs-lookup"><span data-stu-id="cc5a1-127">**10**</span></span>
</dt> <dd>

<span data-ttu-id="cc5a1-128">O objeto especificado já existe.</span><span class="sxs-lookup"><span data-stu-id="cc5a1-128">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="cc5a1-129">**11**</span><span class="sxs-lookup"><span data-stu-id="cc5a1-129">**11**</span></span>
</dt> <dd>

<span data-ttu-id="cc5a1-130">O sistema de arquivos não é NTFS.</span><span class="sxs-lookup"><span data-stu-id="cc5a1-130">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="cc5a1-131">**12**</span><span class="sxs-lookup"><span data-stu-id="cc5a1-131">**12**</span></span>
</dt> <dd>

<span data-ttu-id="cc5a1-132">A plataforma não é o Windows.</span><span class="sxs-lookup"><span data-stu-id="cc5a1-132">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="cc5a1-133">**13**</span><span class="sxs-lookup"><span data-stu-id="cc5a1-133">**13**</span></span>
</dt> <dd>

<span data-ttu-id="cc5a1-134">A unidade não é a mesma.</span><span class="sxs-lookup"><span data-stu-id="cc5a1-134">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="cc5a1-135">**14**</span><span class="sxs-lookup"><span data-stu-id="cc5a1-135">**14**</span></span>
</dt> <dd>

<span data-ttu-id="cc5a1-136">O diretório não está vazio.</span><span class="sxs-lookup"><span data-stu-id="cc5a1-136">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="cc5a1-137">**15**</span><span class="sxs-lookup"><span data-stu-id="cc5a1-137">**15**</span></span>
</dt> <dd>

<span data-ttu-id="cc5a1-138">Houve uma violação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="cc5a1-138">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="cc5a1-139">**16**</span><span class="sxs-lookup"><span data-stu-id="cc5a1-139">**16**</span></span>
</dt> <dd>

<span data-ttu-id="cc5a1-140">O arquivo de inicialização especificado não era válido.</span><span class="sxs-lookup"><span data-stu-id="cc5a1-140">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="cc5a1-141">**17**</span><span class="sxs-lookup"><span data-stu-id="cc5a1-141">**17**</span></span>
</dt> <dd>

<span data-ttu-id="cc5a1-142">Um privilégio necessário para a operação não é mantido.</span><span class="sxs-lookup"><span data-stu-id="cc5a1-142">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="cc5a1-143">**Abril**</span><span class="sxs-lookup"><span data-stu-id="cc5a1-143">**21**</span></span>
</dt> <dd>

<span data-ttu-id="cc5a1-144">Um parâmetro especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="cc5a1-144">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cc5a1-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cc5a1-145">Requirements</span></span>



| <span data-ttu-id="cc5a1-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc5a1-146">Requirement</span></span> | <span data-ttu-id="cc5a1-147">Valor</span><span class="sxs-lookup"><span data-stu-id="cc5a1-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cc5a1-148">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cc5a1-148">Minimum supported client</span></span><br/> | <span data-ttu-id="cc5a1-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cc5a1-149">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cc5a1-150">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cc5a1-150">Minimum supported server</span></span><br/> | <span data-ttu-id="cc5a1-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cc5a1-151">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cc5a1-152">Namespace</span><span class="sxs-lookup"><span data-stu-id="cc5a1-152">Namespace</span></span><br/>                | <span data-ttu-id="cc5a1-153">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="cc5a1-153">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="cc5a1-154">MOF</span><span class="sxs-lookup"><span data-stu-id="cc5a1-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cc5a1-155"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cc5a1-155"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="cc5a1-156">DLL</span><span class="sxs-lookup"><span data-stu-id="cc5a1-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cc5a1-157"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cc5a1-157"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc5a1-158">Confira também</span><span class="sxs-lookup"><span data-stu-id="cc5a1-158">See also</span></span>

<dl> <dt>

<span data-ttu-id="cc5a1-159">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cc5a1-159">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="cc5a1-160">**\_Arquivo de paginação Win32**</span><span class="sxs-lookup"><span data-stu-id="cc5a1-160">**Win32\_PageFile**</span></span>](win32-pagefile.md)
</dt> </dl>

 

