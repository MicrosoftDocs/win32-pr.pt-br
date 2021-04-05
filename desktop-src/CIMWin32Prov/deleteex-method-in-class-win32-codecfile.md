---
description: Exclua o arquivo de codec de áudio ou vídeo lógico (ou diretório) especificado no caminho do objeto.
ms.assetid: df85c8a4-3be3-4bde-b36e-6bc8af6495a9
ms.tgt_platform: multiple
title: Método DeleteEx da classe Win32_CodecFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile.DeleteEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: df5527be497176f167ac368b872253fa3254a404
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826312"
---
# <a name="deleteex-method-of-the-win32_codecfile-class"></a><span data-ttu-id="b7541-103">Método DeleteEx da classe de um codec do Win32 \_</span><span class="sxs-lookup"><span data-stu-id="b7541-103">DeleteEx method of the Win32\_CodecFile class</span></span>

<span data-ttu-id="b7541-104">O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **DeleteEx** excluirá o arquivo de codec de áudio ou vídeo lógico (ou diretório) especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="b7541-104">The **DeleteEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method will delete the logical audio or video codec file (or directory) specified in the object path.</span></span> <span data-ttu-id="b7541-105">**DeleteEx** é uma versão estendida do método [**delete**](delete-method-in-class-win32-directory.md) .</span><span class="sxs-lookup"><span data-stu-id="b7541-105">**DeleteEx** is an extended version of the [**Delete**](delete-method-in-class-win32-directory.md) method.</span></span>

<span data-ttu-id="b7541-106">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="b7541-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="b7541-107">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="b7541-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="b7541-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b7541-108">Syntax</span></span>


```mof
uint32 DeleteEx(
  [out] string StopFileName,
  [in]  String StartFileName
);
```



## <a name="parameters"></a><span data-ttu-id="b7541-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b7541-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7541-110">*StopFileName* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b7541-110">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b7541-111">Nome do arquivo ou diretório em que o método **DeleteEx** falhou.</span><span class="sxs-lookup"><span data-stu-id="b7541-111">Name of the file or directory where the **DeleteEx** method failed.</span></span> <span data-ttu-id="b7541-112">Esse parâmetro será **NULL** se o método tiver sucesso.</span><span class="sxs-lookup"><span data-stu-id="b7541-112">This parameter will be **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="b7541-113">*StartFileName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b7541-113">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7541-114">Nomeia o arquivo ou diretório filho a ser usado como ponto de partida para **DeleteEx**.</span><span class="sxs-lookup"><span data-stu-id="b7541-114">Names the child file or directory to use as a starting point for **DeleteEx**.</span></span> <span data-ttu-id="b7541-115">O parâmetro *StartFileName* normalmente é o parâmetro *StopFileName* que especifica o arquivo ou diretório no qual ocorreu um erro da chamada do método anterior.</span><span class="sxs-lookup"><span data-stu-id="b7541-115">The *StartFileName* parameter is typically the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="b7541-116">Se esse parâmetro for **nulo**, a operação será executada no arquivo ou diretório especificado na chamada de **ExecMethod** .</span><span class="sxs-lookup"><span data-stu-id="b7541-116">If this parameter is **NULL**, the operation is performed on the file or directory specified in the **ExecMethod** call.</span></span> <span data-ttu-id="b7541-117">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="b7541-117">This parameter is optional.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7541-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b7541-118">Return value</span></span>

<span data-ttu-id="b7541-119">Retorna um valor inteiro de 0 (zero) se o arquivo foi excluído com êxito e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="b7541-119">Returns an integer value of 0 (zero) if the file was successfully deleted, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="b7541-120">**0**</span><span class="sxs-lookup"><span data-stu-id="b7541-120">**0**</span></span>
</dt> <dd>

<span data-ttu-id="b7541-121">A solicitação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="b7541-121">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="b7541-122">**2**</span><span class="sxs-lookup"><span data-stu-id="b7541-122">**2**</span></span>
</dt> <dd>

<span data-ttu-id="b7541-123">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="b7541-123">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="b7541-124">**8**</span><span class="sxs-lookup"><span data-stu-id="b7541-124">**8**</span></span>
</dt> <dd>

<span data-ttu-id="b7541-125">Ocorreu uma falha não especificada.</span><span class="sxs-lookup"><span data-stu-id="b7541-125">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="b7541-126">**9**</span><span class="sxs-lookup"><span data-stu-id="b7541-126">**9**</span></span>
</dt> <dd>

<span data-ttu-id="b7541-127">O nome especificado não era válido.</span><span class="sxs-lookup"><span data-stu-id="b7541-127">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="b7541-128">**10**</span><span class="sxs-lookup"><span data-stu-id="b7541-128">**10**</span></span>
</dt> <dd>

<span data-ttu-id="b7541-129">O objeto especificado já existe.</span><span class="sxs-lookup"><span data-stu-id="b7541-129">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="b7541-130">**11**</span><span class="sxs-lookup"><span data-stu-id="b7541-130">**11**</span></span>
</dt> <dd>

<span data-ttu-id="b7541-131">O sistema de arquivos não é NTFS.</span><span class="sxs-lookup"><span data-stu-id="b7541-131">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="b7541-132">**12**</span><span class="sxs-lookup"><span data-stu-id="b7541-132">**12**</span></span>
</dt> <dd>

<span data-ttu-id="b7541-133">A plataforma não é o Windows.</span><span class="sxs-lookup"><span data-stu-id="b7541-133">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="b7541-134">**13**</span><span class="sxs-lookup"><span data-stu-id="b7541-134">**13**</span></span>
</dt> <dd>

<span data-ttu-id="b7541-135">A unidade não é a mesma.</span><span class="sxs-lookup"><span data-stu-id="b7541-135">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="b7541-136">**14**</span><span class="sxs-lookup"><span data-stu-id="b7541-136">**14**</span></span>
</dt> <dd>

<span data-ttu-id="b7541-137">O diretório não está vazio.</span><span class="sxs-lookup"><span data-stu-id="b7541-137">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="b7541-138">**15**</span><span class="sxs-lookup"><span data-stu-id="b7541-138">**15**</span></span>
</dt> <dd>

<span data-ttu-id="b7541-139">Houve uma violação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="b7541-139">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="b7541-140">**16**</span><span class="sxs-lookup"><span data-stu-id="b7541-140">**16**</span></span>
</dt> <dd>

<span data-ttu-id="b7541-141">O arquivo de inicialização especificado não era válido.</span><span class="sxs-lookup"><span data-stu-id="b7541-141">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="b7541-142">**17**</span><span class="sxs-lookup"><span data-stu-id="b7541-142">**17**</span></span>
</dt> <dd>

<span data-ttu-id="b7541-143">Um privilégio necessário para a operação não é mantido.</span><span class="sxs-lookup"><span data-stu-id="b7541-143">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="b7541-144">**Abril**</span><span class="sxs-lookup"><span data-stu-id="b7541-144">**21**</span></span>
</dt> <dd>

<span data-ttu-id="b7541-145">Um parâmetro especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="b7541-145">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b7541-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b7541-146">Requirements</span></span>



| <span data-ttu-id="b7541-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7541-147">Requirement</span></span> | <span data-ttu-id="b7541-148">Valor</span><span class="sxs-lookup"><span data-stu-id="b7541-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b7541-149">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b7541-149">Minimum supported client</span></span><br/> | <span data-ttu-id="b7541-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b7541-150">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b7541-151">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b7541-151">Minimum supported server</span></span><br/> | <span data-ttu-id="b7541-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b7541-152">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b7541-153">Namespace</span><span class="sxs-lookup"><span data-stu-id="b7541-153">Namespace</span></span><br/>                | <span data-ttu-id="b7541-154">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="b7541-154">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b7541-155">MOF</span><span class="sxs-lookup"><span data-stu-id="b7541-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b7541-156"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b7541-156"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b7541-157">DLL</span><span class="sxs-lookup"><span data-stu-id="b7541-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b7541-158"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7541-158"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7541-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="b7541-159">See also</span></span>

<dl> <dt>

<span data-ttu-id="b7541-160">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b7541-160">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="b7541-161">**Codec do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="b7541-161">**Win32\_CodecFile**</span></span>](win32-codecfile.md)
</dt> </dl>

 

