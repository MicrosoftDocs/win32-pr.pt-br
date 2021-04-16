---
description: Exclui o arquivo de paginação lógica (ou diretório) especificado no caminho do objeto.
ms.assetid: cc36d621-597e-4343-8bf6-bfca7fa29276
ms.tgt_platform: multiple
title: Método Delete da classe Win32_PageFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFile.Delete
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e61155a321e4414c66f98843a79d935f38870bd5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105750955"
---
# <a name="delete-method-of-the-win32_pagefile-class"></a><span data-ttu-id="c7e54-103">Método Delete da classe de \_ arquivo de paginação Win32</span><span class="sxs-lookup"><span data-stu-id="c7e54-103">Delete method of the Win32\_PageFile class</span></span>

<span data-ttu-id="c7e54-104">O método **excluir** [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) exclui o arquivo de paginação lógica (ou diretório) especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="c7e54-104">The **Delete** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method deletes the logical paging file (or directory) specified in the object path.</span></span>

<span data-ttu-id="c7e54-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="c7e54-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="c7e54-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="c7e54-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="c7e54-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c7e54-107">Syntax</span></span>


```mof
uint32 Delete();
```



## <a name="parameters"></a><span data-ttu-id="c7e54-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c7e54-108">Parameters</span></span>

<span data-ttu-id="c7e54-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="c7e54-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c7e54-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c7e54-110">Return value</span></span>

<span data-ttu-id="c7e54-111">Retorna um valor de 0 (zero) se o arquivo foi excluído com êxito e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="c7e54-111">Returns a value of 0 (zero) if the file was successfully deleted, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="c7e54-112">**0**</span><span class="sxs-lookup"><span data-stu-id="c7e54-112">**0**</span></span>
</dt> <dd>

<span data-ttu-id="c7e54-113">A solicitação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="c7e54-113">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="c7e54-114">**2**</span><span class="sxs-lookup"><span data-stu-id="c7e54-114">**2**</span></span>
</dt> <dd>

<span data-ttu-id="c7e54-115">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="c7e54-115">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="c7e54-116">**8**</span><span class="sxs-lookup"><span data-stu-id="c7e54-116">**8**</span></span>
</dt> <dd>

<span data-ttu-id="c7e54-117">Ocorreu uma falha não especificada.</span><span class="sxs-lookup"><span data-stu-id="c7e54-117">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="c7e54-118">**9**</span><span class="sxs-lookup"><span data-stu-id="c7e54-118">**9**</span></span>
</dt> <dd>

<span data-ttu-id="c7e54-119">O nome especificado não era válido.</span><span class="sxs-lookup"><span data-stu-id="c7e54-119">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="c7e54-120">**10**</span><span class="sxs-lookup"><span data-stu-id="c7e54-120">**10**</span></span>
</dt> <dd>

<span data-ttu-id="c7e54-121">O objeto especificado já existe.</span><span class="sxs-lookup"><span data-stu-id="c7e54-121">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="c7e54-122">**11**</span><span class="sxs-lookup"><span data-stu-id="c7e54-122">**11**</span></span>
</dt> <dd>

<span data-ttu-id="c7e54-123">O sistema de arquivos não é NTFS.</span><span class="sxs-lookup"><span data-stu-id="c7e54-123">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="c7e54-124">**12**</span><span class="sxs-lookup"><span data-stu-id="c7e54-124">**12**</span></span>
</dt> <dd>

<span data-ttu-id="c7e54-125">A plataforma não é o Windows.</span><span class="sxs-lookup"><span data-stu-id="c7e54-125">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="c7e54-126">**13**</span><span class="sxs-lookup"><span data-stu-id="c7e54-126">**13**</span></span>
</dt> <dd>

<span data-ttu-id="c7e54-127">A unidade não é a mesma.</span><span class="sxs-lookup"><span data-stu-id="c7e54-127">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="c7e54-128">**14**</span><span class="sxs-lookup"><span data-stu-id="c7e54-128">**14**</span></span>
</dt> <dd>

<span data-ttu-id="c7e54-129">O diretório não está vazio.</span><span class="sxs-lookup"><span data-stu-id="c7e54-129">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="c7e54-130">**15**</span><span class="sxs-lookup"><span data-stu-id="c7e54-130">**15**</span></span>
</dt> <dd>

<span data-ttu-id="c7e54-131">Houve uma violação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="c7e54-131">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="c7e54-132">**16**</span><span class="sxs-lookup"><span data-stu-id="c7e54-132">**16**</span></span>
</dt> <dd>

<span data-ttu-id="c7e54-133">O arquivo de inicialização especificado não era válido.</span><span class="sxs-lookup"><span data-stu-id="c7e54-133">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="c7e54-134">**17**</span><span class="sxs-lookup"><span data-stu-id="c7e54-134">**17**</span></span>
</dt> <dd>

<span data-ttu-id="c7e54-135">Um privilégio necessário para a operação não é mantido.</span><span class="sxs-lookup"><span data-stu-id="c7e54-135">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="c7e54-136">**Abril**</span><span class="sxs-lookup"><span data-stu-id="c7e54-136">**21**</span></span>
</dt> <dd>

<span data-ttu-id="c7e54-137">Um parâmetro especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="c7e54-137">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c7e54-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c7e54-138">Requirements</span></span>



| <span data-ttu-id="c7e54-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7e54-139">Requirement</span></span> | <span data-ttu-id="c7e54-140">Valor</span><span class="sxs-lookup"><span data-stu-id="c7e54-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c7e54-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c7e54-141">Minimum supported client</span></span><br/> | <span data-ttu-id="c7e54-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c7e54-142">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c7e54-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c7e54-143">Minimum supported server</span></span><br/> | <span data-ttu-id="c7e54-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c7e54-144">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c7e54-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="c7e54-145">Namespace</span></span><br/>                | <span data-ttu-id="c7e54-146">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="c7e54-146">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c7e54-147">MOF</span><span class="sxs-lookup"><span data-stu-id="c7e54-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c7e54-148"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c7e54-148"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c7e54-149">DLL</span><span class="sxs-lookup"><span data-stu-id="c7e54-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7e54-150"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7e54-150"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7e54-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="c7e54-151">See also</span></span>

<dl> <dt>

<span data-ttu-id="c7e54-152">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c7e54-152">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="c7e54-153">**\_Arquivo de paginação Win32**</span><span class="sxs-lookup"><span data-stu-id="c7e54-153">**Win32\_PageFile**</span></span>](win32-pagefile.md)
</dt> </dl>

 

