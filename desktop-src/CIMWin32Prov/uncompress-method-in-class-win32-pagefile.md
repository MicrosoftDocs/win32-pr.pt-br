---
description: Descompacta o arquivo de paginação lógica (ou diretório) especificado no caminho do objeto.
ms.assetid: 9bd98ba8-068e-49af-8dd4-e5ee987eb31d
ms.tgt_platform: multiple
title: Descompactar método da classe Win32_PageFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFile.Uncompress
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 45a5b48ffa6b2249992b61eadf72f42f6d71969b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826633"
---
# <a name="uncompress-method-of-the-win32_pagefile-class"></a><span data-ttu-id="cbbf1-103">Descompactar o método da \_ classe de arquivo de paginação Win32</span><span class="sxs-lookup"><span data-stu-id="cbbf1-103">Uncompress method of the Win32\_PageFile class</span></span>

<span data-ttu-id="cbbf1-104">O método **uncompactar** [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) descompacta o arquivo de paginação lógica (ou diretório) especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="cbbf1-104">The **Uncompress** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method uncompresses the logical paging file (or directory) specified in the object path.</span></span>

<span data-ttu-id="cbbf1-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="cbbf1-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="cbbf1-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="cbbf1-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="cbbf1-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cbbf1-107">Syntax</span></span>


```mof
uint32 Uncompress();
```



## <a name="parameters"></a><span data-ttu-id="cbbf1-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cbbf1-108">Parameters</span></span>

<span data-ttu-id="cbbf1-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="cbbf1-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cbbf1-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cbbf1-110">Return value</span></span>

<span data-ttu-id="cbbf1-111">Retorna um valor de 0 (zero) se o arquivo tiver sido descompactado com êxito e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="cbbf1-111">Returns a value of 0 (zero) if the file was successfully decompressed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="cbbf1-112">**0**</span><span class="sxs-lookup"><span data-stu-id="cbbf1-112">**0**</span></span>
</dt> <dd>

<span data-ttu-id="cbbf1-113">A solicitação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="cbbf1-113">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="cbbf1-114">**2**</span><span class="sxs-lookup"><span data-stu-id="cbbf1-114">**2**</span></span>
</dt> <dd>

<span data-ttu-id="cbbf1-115">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="cbbf1-115">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="cbbf1-116">**8**</span><span class="sxs-lookup"><span data-stu-id="cbbf1-116">**8**</span></span>
</dt> <dd>

<span data-ttu-id="cbbf1-117">Ocorreu uma falha não especificada.</span><span class="sxs-lookup"><span data-stu-id="cbbf1-117">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="cbbf1-118">**9**</span><span class="sxs-lookup"><span data-stu-id="cbbf1-118">**9**</span></span>
</dt> <dd>

<span data-ttu-id="cbbf1-119">O nome especificado não era válido.</span><span class="sxs-lookup"><span data-stu-id="cbbf1-119">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="cbbf1-120">**10**</span><span class="sxs-lookup"><span data-stu-id="cbbf1-120">**10**</span></span>
</dt> <dd>

<span data-ttu-id="cbbf1-121">O objeto especificado já existe.</span><span class="sxs-lookup"><span data-stu-id="cbbf1-121">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="cbbf1-122">**11**</span><span class="sxs-lookup"><span data-stu-id="cbbf1-122">**11**</span></span>
</dt> <dd>

<span data-ttu-id="cbbf1-123">O sistema de arquivos não é NTFS.</span><span class="sxs-lookup"><span data-stu-id="cbbf1-123">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="cbbf1-124">**12**</span><span class="sxs-lookup"><span data-stu-id="cbbf1-124">**12**</span></span>
</dt> <dd>

<span data-ttu-id="cbbf1-125">A plataforma não é o Windows.</span><span class="sxs-lookup"><span data-stu-id="cbbf1-125">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="cbbf1-126">**13**</span><span class="sxs-lookup"><span data-stu-id="cbbf1-126">**13**</span></span>
</dt> <dd>

<span data-ttu-id="cbbf1-127">A unidade não é a mesma.</span><span class="sxs-lookup"><span data-stu-id="cbbf1-127">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="cbbf1-128">**14**</span><span class="sxs-lookup"><span data-stu-id="cbbf1-128">**14**</span></span>
</dt> <dd>

<span data-ttu-id="cbbf1-129">O diretório não está vazio.</span><span class="sxs-lookup"><span data-stu-id="cbbf1-129">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="cbbf1-130">**15**</span><span class="sxs-lookup"><span data-stu-id="cbbf1-130">**15**</span></span>
</dt> <dd>

<span data-ttu-id="cbbf1-131">Houve uma violação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="cbbf1-131">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="cbbf1-132">**16**</span><span class="sxs-lookup"><span data-stu-id="cbbf1-132">**16**</span></span>
</dt> <dd>

<span data-ttu-id="cbbf1-133">O arquivo de inicialização especificado não era válido.</span><span class="sxs-lookup"><span data-stu-id="cbbf1-133">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="cbbf1-134">**17**</span><span class="sxs-lookup"><span data-stu-id="cbbf1-134">**17**</span></span>
</dt> <dd>

<span data-ttu-id="cbbf1-135">Um privilégio necessário para a operação não é mantido.</span><span class="sxs-lookup"><span data-stu-id="cbbf1-135">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="cbbf1-136">**Abril**</span><span class="sxs-lookup"><span data-stu-id="cbbf1-136">**21**</span></span>
</dt> <dd>

<span data-ttu-id="cbbf1-137">Um parâmetro especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="cbbf1-137">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cbbf1-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cbbf1-138">Requirements</span></span>



| <span data-ttu-id="cbbf1-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="cbbf1-139">Requirement</span></span> | <span data-ttu-id="cbbf1-140">Valor</span><span class="sxs-lookup"><span data-stu-id="cbbf1-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cbbf1-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cbbf1-141">Minimum supported client</span></span><br/> | <span data-ttu-id="cbbf1-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cbbf1-142">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cbbf1-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cbbf1-143">Minimum supported server</span></span><br/> | <span data-ttu-id="cbbf1-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cbbf1-144">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cbbf1-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="cbbf1-145">Namespace</span></span><br/>                | <span data-ttu-id="cbbf1-146">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="cbbf1-146">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="cbbf1-147">MOF</span><span class="sxs-lookup"><span data-stu-id="cbbf1-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cbbf1-148"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cbbf1-148"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="cbbf1-149">DLL</span><span class="sxs-lookup"><span data-stu-id="cbbf1-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cbbf1-150"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cbbf1-150"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cbbf1-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="cbbf1-151">See also</span></span>

<dl> <dt>

<span data-ttu-id="cbbf1-152">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cbbf1-152">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="cbbf1-153">**\_Arquivo de paginação Win32**</span><span class="sxs-lookup"><span data-stu-id="cbbf1-153">**Win32\_PageFile**</span></span>](win32-pagefile.md)
</dt> </dl>

 

