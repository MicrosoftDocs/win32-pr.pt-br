---
description: Exclui o arquivo de atalho lógico (ou diretório) especificado no caminho do objeto.
ms.assetid: 278cd856-bb8d-4494-b43c-f0858366e136
ms.tgt_platform: multiple
title: Método DeleteEx da classe Win32_ShortcutFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ShortcutFile.DeleteEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: bbe382ca57c4bdef36b19742313965c8bac68fd3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756045"
---
# <a name="deleteex-method-of-the-win32_shortcutfile-class"></a><span data-ttu-id="3ba41-103">Método DeleteEx da \_ classe shortcutfile do Win32</span><span class="sxs-lookup"><span data-stu-id="3ba41-103">DeleteEx method of the Win32\_ShortcutFile class</span></span>

<span data-ttu-id="3ba41-104">O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **DeleteEx** exclui o arquivo de atalho lógico (ou diretório) especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="3ba41-104">The **DeleteEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method deletes the logical shortcut file (or directory) specified in the object path.</span></span> <span data-ttu-id="3ba41-105">**DeleteEx** é uma versão estendida do método [**delete**](delete-method-in-class-win32-directory.md) .</span><span class="sxs-lookup"><span data-stu-id="3ba41-105">**DeleteEx** is an extended version of the [**Delete**](delete-method-in-class-win32-directory.md) method.</span></span>

<span data-ttu-id="3ba41-106">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="3ba41-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="3ba41-107">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="3ba41-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="3ba41-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3ba41-108">Syntax</span></span>


```mof
uint32 DeleteEx(
  [out]          string StopFileName,
  [in, optional] string StartFileName
);
```



## <a name="parameters"></a><span data-ttu-id="3ba41-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3ba41-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ba41-110">*StopFileName* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="3ba41-110">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3ba41-111">Nome do arquivo ou diretório em que o método **DeleteEx** falhou.</span><span class="sxs-lookup"><span data-stu-id="3ba41-111">Name of the file or directory where the **DeleteEx** method failed.</span></span> <span data-ttu-id="3ba41-112">Esse parâmetro será **nulo** se o método tiver sucesso.</span><span class="sxs-lookup"><span data-stu-id="3ba41-112">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="3ba41-113">*StartFileName* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="3ba41-113">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3ba41-114">Nomeia o arquivo ou diretório filho a ser usado como ponto de partida para **DeleteEx**.</span><span class="sxs-lookup"><span data-stu-id="3ba41-114">Names the child file or directory to use as a starting point for **DeleteEx**.</span></span> <span data-ttu-id="3ba41-115">O parâmetro *StartFileName* normalmente é o parâmetro *StopFileName* que especifica o arquivo ou diretório no qual ocorreu um erro da chamada do método anterior.</span><span class="sxs-lookup"><span data-stu-id="3ba41-115">The *StartFileName* parameter is typically the *StopFileName* parameter that specifies the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="3ba41-116">Se esse parâmetro for **nulo**, a operação será executada no arquivo ou diretório especificado na chamada de ExecMethod.</span><span class="sxs-lookup"><span data-stu-id="3ba41-116">If this parameter is **NULL**, the operation is performed on the file or directory specified in the ExecMethod call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ba41-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3ba41-117">Return value</span></span>

<span data-ttu-id="3ba41-118">Retorna um valor de 0 (zero) se o arquivo foi excluído com êxito e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="3ba41-118">Returns a value of 0 (zero) if the file was successfully deleted, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="3ba41-119">**0**</span><span class="sxs-lookup"><span data-stu-id="3ba41-119">**0**</span></span>
</dt> <dd>

<span data-ttu-id="3ba41-120">A solicitação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="3ba41-120">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="3ba41-121">**2**</span><span class="sxs-lookup"><span data-stu-id="3ba41-121">**2**</span></span>
</dt> <dd>

<span data-ttu-id="3ba41-122">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="3ba41-122">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="3ba41-123">**8**</span><span class="sxs-lookup"><span data-stu-id="3ba41-123">**8**</span></span>
</dt> <dd>

<span data-ttu-id="3ba41-124">Ocorreu uma falha não especificada.</span><span class="sxs-lookup"><span data-stu-id="3ba41-124">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="3ba41-125">**9**</span><span class="sxs-lookup"><span data-stu-id="3ba41-125">**9**</span></span>
</dt> <dd>

<span data-ttu-id="3ba41-126">O nome especificado não era válido.</span><span class="sxs-lookup"><span data-stu-id="3ba41-126">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="3ba41-127">**10**</span><span class="sxs-lookup"><span data-stu-id="3ba41-127">**10**</span></span>
</dt> <dd>

<span data-ttu-id="3ba41-128">O objeto especificado já existe.</span><span class="sxs-lookup"><span data-stu-id="3ba41-128">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="3ba41-129">**11**</span><span class="sxs-lookup"><span data-stu-id="3ba41-129">**11**</span></span>
</dt> <dd>

<span data-ttu-id="3ba41-130">O sistema de arquivos não é NTFS.</span><span class="sxs-lookup"><span data-stu-id="3ba41-130">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="3ba41-131">**12**</span><span class="sxs-lookup"><span data-stu-id="3ba41-131">**12**</span></span>
</dt> <dd>

<span data-ttu-id="3ba41-132">A plataforma não é o Windows.</span><span class="sxs-lookup"><span data-stu-id="3ba41-132">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="3ba41-133">**13**</span><span class="sxs-lookup"><span data-stu-id="3ba41-133">**13**</span></span>
</dt> <dd>

<span data-ttu-id="3ba41-134">A unidade não é a mesma.</span><span class="sxs-lookup"><span data-stu-id="3ba41-134">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="3ba41-135">**14**</span><span class="sxs-lookup"><span data-stu-id="3ba41-135">**14**</span></span>
</dt> <dd>

<span data-ttu-id="3ba41-136">O diretório não está vazio.</span><span class="sxs-lookup"><span data-stu-id="3ba41-136">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="3ba41-137">**15**</span><span class="sxs-lookup"><span data-stu-id="3ba41-137">**15**</span></span>
</dt> <dd>

<span data-ttu-id="3ba41-138">Houve uma violação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="3ba41-138">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="3ba41-139">**16**</span><span class="sxs-lookup"><span data-stu-id="3ba41-139">**16**</span></span>
</dt> <dd>

<span data-ttu-id="3ba41-140">O arquivo de inicialização especificado não era válido.</span><span class="sxs-lookup"><span data-stu-id="3ba41-140">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="3ba41-141">**17**</span><span class="sxs-lookup"><span data-stu-id="3ba41-141">**17**</span></span>
</dt> <dd>

<span data-ttu-id="3ba41-142">Um privilégio necessário para a operação não é mantido.</span><span class="sxs-lookup"><span data-stu-id="3ba41-142">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="3ba41-143">**Abril**</span><span class="sxs-lookup"><span data-stu-id="3ba41-143">**21**</span></span>
</dt> <dd>

<span data-ttu-id="3ba41-144">Um parâmetro especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="3ba41-144">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3ba41-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3ba41-145">Requirements</span></span>



| <span data-ttu-id="3ba41-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ba41-146">Requirement</span></span> | <span data-ttu-id="3ba41-147">Valor</span><span class="sxs-lookup"><span data-stu-id="3ba41-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3ba41-148">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3ba41-148">Minimum supported client</span></span><br/> | <span data-ttu-id="3ba41-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3ba41-149">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3ba41-150">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3ba41-150">Minimum supported server</span></span><br/> | <span data-ttu-id="3ba41-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3ba41-151">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3ba41-152">Namespace</span><span class="sxs-lookup"><span data-stu-id="3ba41-152">Namespace</span></span><br/>                | <span data-ttu-id="3ba41-153">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="3ba41-153">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3ba41-154">MOF</span><span class="sxs-lookup"><span data-stu-id="3ba41-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3ba41-155"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3ba41-155"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3ba41-156">DLL</span><span class="sxs-lookup"><span data-stu-id="3ba41-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ba41-157"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3ba41-157"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ba41-158">Confira também</span><span class="sxs-lookup"><span data-stu-id="3ba41-158">See also</span></span>

<dl> <dt>

<span data-ttu-id="3ba41-159">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3ba41-159">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="3ba41-160">**Atalho do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="3ba41-160">**Win32\_ShortcutFile**</span></span>](win32-shortcutfile.md)
</dt> </dl>

 

