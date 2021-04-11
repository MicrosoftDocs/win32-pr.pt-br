---
description: O método de classe WMI TakeOwnerShip Obtém a propriedade do arquivo lógico especificado no caminho do objeto.
ms.assetid: c8fa0706-1f7e-4e68-aea6-694ba24c16c3
ms.tgt_platform: multiple
title: Método TakeOwnerShip da classe Win32_CodecFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile.TakeOwnerShip
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1de05f444e99be9a1ebcb5d32fa0ba754cf34254
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104088940"
---
# <a name="takeownership-method-of-the-win32_codecfile-class"></a><span data-ttu-id="c6aa1-103">Método TakeOwnerShip da classe de um codec do Win32 \_</span><span class="sxs-lookup"><span data-stu-id="c6aa1-103">TakeOwnerShip method of the Win32\_CodecFile class</span></span>

<span data-ttu-id="c6aa1-104">O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **TakeOwnership** Obtém a propriedade do arquivo lógico especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="c6aa1-104">The **TakeOwnerShip** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="c6aa1-105">Se o arquivo lógico for realmente um diretório, o **TakeOwnership** agirá recursivamente, assumindo a propriedade de todos os arquivos e subdiretórios contidos no diretório.</span><span class="sxs-lookup"><span data-stu-id="c6aa1-105">If the logical file is actually a directory, then **TakeOwnerShip** acts recursively, taking ownership of all of the files and subdirectories the directory contains.</span></span>

<span data-ttu-id="c6aa1-106">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="c6aa1-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="c6aa1-107">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="c6aa1-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="c6aa1-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c6aa1-108">Syntax</span></span>


```mof
uint32 TakeOwnerShip();
```



## <a name="parameters"></a><span data-ttu-id="c6aa1-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c6aa1-109">Parameters</span></span>

<span data-ttu-id="c6aa1-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="c6aa1-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c6aa1-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c6aa1-111">Return value</span></span>

<span data-ttu-id="c6aa1-112">Retorna um dos valores inteiros a seguir.</span><span class="sxs-lookup"><span data-stu-id="c6aa1-112">Returns one of the following integer values.</span></span>

<dl> <dt>

<span data-ttu-id="c6aa1-113">**0**</span><span class="sxs-lookup"><span data-stu-id="c6aa1-113">**0**</span></span>
</dt> <dd>

<span data-ttu-id="c6aa1-114">A solicitação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="c6aa1-114">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="c6aa1-115">**2**</span><span class="sxs-lookup"><span data-stu-id="c6aa1-115">**2**</span></span>
</dt> <dd>

<span data-ttu-id="c6aa1-116">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="c6aa1-116">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="c6aa1-117">**8**</span><span class="sxs-lookup"><span data-stu-id="c6aa1-117">**8**</span></span>
</dt> <dd>

<span data-ttu-id="c6aa1-118">Ocorreu uma falha não especificada.</span><span class="sxs-lookup"><span data-stu-id="c6aa1-118">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="c6aa1-119">**9**</span><span class="sxs-lookup"><span data-stu-id="c6aa1-119">**9**</span></span>
</dt> <dd>

<span data-ttu-id="c6aa1-120">O nome especificado não era válido.</span><span class="sxs-lookup"><span data-stu-id="c6aa1-120">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="c6aa1-121">**10**</span><span class="sxs-lookup"><span data-stu-id="c6aa1-121">**10**</span></span>
</dt> <dd>

<span data-ttu-id="c6aa1-122">O objeto especificado já existe.</span><span class="sxs-lookup"><span data-stu-id="c6aa1-122">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="c6aa1-123">**11**</span><span class="sxs-lookup"><span data-stu-id="c6aa1-123">**11**</span></span>
</dt> <dd>

<span data-ttu-id="c6aa1-124">O sistema de arquivos não é NTFS.</span><span class="sxs-lookup"><span data-stu-id="c6aa1-124">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="c6aa1-125">**12**</span><span class="sxs-lookup"><span data-stu-id="c6aa1-125">**12**</span></span>
</dt> <dd>

<span data-ttu-id="c6aa1-126">A plataforma não é o Windows.</span><span class="sxs-lookup"><span data-stu-id="c6aa1-126">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="c6aa1-127">**13**</span><span class="sxs-lookup"><span data-stu-id="c6aa1-127">**13**</span></span>
</dt> <dd>

<span data-ttu-id="c6aa1-128">A unidade não é a mesma.</span><span class="sxs-lookup"><span data-stu-id="c6aa1-128">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="c6aa1-129">**14**</span><span class="sxs-lookup"><span data-stu-id="c6aa1-129">**14**</span></span>
</dt> <dd>

<span data-ttu-id="c6aa1-130">O diretório não está vazio.</span><span class="sxs-lookup"><span data-stu-id="c6aa1-130">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="c6aa1-131">**15**</span><span class="sxs-lookup"><span data-stu-id="c6aa1-131">**15**</span></span>
</dt> <dd>

<span data-ttu-id="c6aa1-132">Houve uma violação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="c6aa1-132">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="c6aa1-133">**16**</span><span class="sxs-lookup"><span data-stu-id="c6aa1-133">**16**</span></span>
</dt> <dd>

<span data-ttu-id="c6aa1-134">O arquivo de inicialização especificado não era válido.</span><span class="sxs-lookup"><span data-stu-id="c6aa1-134">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="c6aa1-135">**17**</span><span class="sxs-lookup"><span data-stu-id="c6aa1-135">**17**</span></span>
</dt> <dd>

<span data-ttu-id="c6aa1-136">Um privilégio necessário para a operação não é mantido.</span><span class="sxs-lookup"><span data-stu-id="c6aa1-136">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="c6aa1-137">**Abril**</span><span class="sxs-lookup"><span data-stu-id="c6aa1-137">**21**</span></span>
</dt> <dd>

<span data-ttu-id="c6aa1-138">Um parâmetro especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="c6aa1-138">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c6aa1-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c6aa1-139">Requirements</span></span>



| <span data-ttu-id="c6aa1-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6aa1-140">Requirement</span></span> | <span data-ttu-id="c6aa1-141">Valor</span><span class="sxs-lookup"><span data-stu-id="c6aa1-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c6aa1-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c6aa1-142">Minimum supported client</span></span><br/> | <span data-ttu-id="c6aa1-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c6aa1-143">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c6aa1-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c6aa1-144">Minimum supported server</span></span><br/> | <span data-ttu-id="c6aa1-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c6aa1-145">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c6aa1-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="c6aa1-146">Namespace</span></span><br/>                | <span data-ttu-id="c6aa1-147">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="c6aa1-147">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c6aa1-148">MOF</span><span class="sxs-lookup"><span data-stu-id="c6aa1-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c6aa1-149"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c6aa1-149"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c6aa1-150">DLL</span><span class="sxs-lookup"><span data-stu-id="c6aa1-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c6aa1-151"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c6aa1-151"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6aa1-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="c6aa1-152">See also</span></span>

<dl> <dt>

<span data-ttu-id="c6aa1-153">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c6aa1-153">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="c6aa1-154">**Codec do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="c6aa1-154">**Win32\_CodecFile**</span></span>](win32-codecfile.md)
</dt> </dl>

 

