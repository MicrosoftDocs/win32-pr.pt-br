---
description: Método TakeOwnerShip da classe Win32_PageFile-o TakeOwnerShip&\# 8194; O método de classe WMI Obtém a propriedade do arquivo lógico especificado no caminho do objeto.
ms.assetid: c4f42d54-562c-4163-a5ec-e94f76932631
ms.tgt_platform: multiple
title: Método TakeOwnerShip da classe Win32_PageFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFile.TakeOwnerShip
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3aa0b2ec9f3805f1877f86bdf86d72b921d53ac9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086014"
---
# <a name="takeownership-method-of-the-win32_pagefile-class"></a><span data-ttu-id="8482a-103">Método TakeOwnerShip da classe de \_ arquivo de paginação Win32</span><span class="sxs-lookup"><span data-stu-id="8482a-103">TakeOwnerShip method of the Win32\_PageFile class</span></span>

<span data-ttu-id="8482a-104">O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **TakeOwnership** Obtém a propriedade do arquivo lógico especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="8482a-104">The **TakeOwnerShip** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="8482a-105">Se o arquivo lógico for realmente um diretório, o **TakeOwnership** agirá recursivamente, assumindo a propriedade de todos os arquivos e subdiretórios contidos no diretório.</span><span class="sxs-lookup"><span data-stu-id="8482a-105">If the logical file is actually a directory, then **TakeOwnerShip** acts recursively, taking ownership of all of the files and subdirectories the directory contains.</span></span>

<span data-ttu-id="8482a-106">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="8482a-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="8482a-107">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="8482a-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="8482a-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8482a-108">Syntax</span></span>


```mof
uint32 TakeOwnerShip();
```



## <a name="parameters"></a><span data-ttu-id="8482a-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8482a-109">Parameters</span></span>

<span data-ttu-id="8482a-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="8482a-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8482a-111">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="8482a-111">Return value</span></span>

<span data-ttu-id="8482a-112">Retorna um dos valores listados na lista a seguir ou qualquer outro valor para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="8482a-112">Returns one of the values listed in the following list or any other value to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="8482a-113">**0**</span><span class="sxs-lookup"><span data-stu-id="8482a-113">**0**</span></span>
</dt> <dd>

<span data-ttu-id="8482a-114">A solicitação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="8482a-114">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="8482a-115">**2**</span><span class="sxs-lookup"><span data-stu-id="8482a-115">**2**</span></span>
</dt> <dd>

<span data-ttu-id="8482a-116">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="8482a-116">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="8482a-117">**8**</span><span class="sxs-lookup"><span data-stu-id="8482a-117">**8**</span></span>
</dt> <dd>

<span data-ttu-id="8482a-118">Ocorreu uma falha não especificada.</span><span class="sxs-lookup"><span data-stu-id="8482a-118">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="8482a-119">**9**</span><span class="sxs-lookup"><span data-stu-id="8482a-119">**9**</span></span>
</dt> <dd>

<span data-ttu-id="8482a-120">O nome especificado não era válido.</span><span class="sxs-lookup"><span data-stu-id="8482a-120">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="8482a-121">**10**</span><span class="sxs-lookup"><span data-stu-id="8482a-121">**10**</span></span>
</dt> <dd>

<span data-ttu-id="8482a-122">O objeto especificado já existe.</span><span class="sxs-lookup"><span data-stu-id="8482a-122">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="8482a-123">**11**</span><span class="sxs-lookup"><span data-stu-id="8482a-123">**11**</span></span>
</dt> <dd>

<span data-ttu-id="8482a-124">O sistema de arquivos não é NTFS.</span><span class="sxs-lookup"><span data-stu-id="8482a-124">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="8482a-125">**12**</span><span class="sxs-lookup"><span data-stu-id="8482a-125">**12**</span></span>
</dt> <dd>

<span data-ttu-id="8482a-126">A plataforma não é o Windows.</span><span class="sxs-lookup"><span data-stu-id="8482a-126">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="8482a-127">**13**</span><span class="sxs-lookup"><span data-stu-id="8482a-127">**13**</span></span>
</dt> <dd>

<span data-ttu-id="8482a-128">A unidade não é a mesma.</span><span class="sxs-lookup"><span data-stu-id="8482a-128">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="8482a-129">**14**</span><span class="sxs-lookup"><span data-stu-id="8482a-129">**14**</span></span>
</dt> <dd>

<span data-ttu-id="8482a-130">O diretório não está vazio.</span><span class="sxs-lookup"><span data-stu-id="8482a-130">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="8482a-131">**15**</span><span class="sxs-lookup"><span data-stu-id="8482a-131">**15**</span></span>
</dt> <dd>

<span data-ttu-id="8482a-132">Houve uma violação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="8482a-132">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="8482a-133">**16**</span><span class="sxs-lookup"><span data-stu-id="8482a-133">**16**</span></span>
</dt> <dd>

<span data-ttu-id="8482a-134">O arquivo de inicialização especificado não era válido.</span><span class="sxs-lookup"><span data-stu-id="8482a-134">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="8482a-135">**17**</span><span class="sxs-lookup"><span data-stu-id="8482a-135">**17**</span></span>
</dt> <dd>

<span data-ttu-id="8482a-136">Um privilégio necessário para a operação não é mantido.</span><span class="sxs-lookup"><span data-stu-id="8482a-136">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="8482a-137">**Abril**</span><span class="sxs-lookup"><span data-stu-id="8482a-137">**21**</span></span>
</dt> <dd>

<span data-ttu-id="8482a-138">Um parâmetro especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="8482a-138">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8482a-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8482a-139">Requirements</span></span>



| <span data-ttu-id="8482a-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="8482a-140">Requirement</span></span> | <span data-ttu-id="8482a-141">Valor</span><span class="sxs-lookup"><span data-stu-id="8482a-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8482a-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8482a-142">Minimum supported client</span></span><br/> | <span data-ttu-id="8482a-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8482a-143">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8482a-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8482a-144">Minimum supported server</span></span><br/> | <span data-ttu-id="8482a-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8482a-145">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8482a-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="8482a-146">Namespace</span></span><br/>                | <span data-ttu-id="8482a-147">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="8482a-147">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8482a-148">MOF</span><span class="sxs-lookup"><span data-stu-id="8482a-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8482a-149"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8482a-149"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8482a-150">DLL</span><span class="sxs-lookup"><span data-stu-id="8482a-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8482a-151"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8482a-151"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8482a-152">Consulte também</span><span class="sxs-lookup"><span data-stu-id="8482a-152">See also</span></span>

<dl> <dt>

<span data-ttu-id="8482a-153">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8482a-153">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="8482a-154">**\_Arquivo de paginação Win32**</span><span class="sxs-lookup"><span data-stu-id="8482a-154">**Win32\_PageFile**</span></span>](win32-pagefile.md)
</dt> </dl>

 

