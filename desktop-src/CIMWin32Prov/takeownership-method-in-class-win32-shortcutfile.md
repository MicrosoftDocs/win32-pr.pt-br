---
description: TakeOwnerShip&\# 8194; O método de classe WMI Obtém a propriedade do arquivo lógico especificado no caminho do objeto.
ms.assetid: 1a8ff156-50b2-4550-abcc-7a6ae0e4630f
ms.tgt_platform: multiple
title: Método TakeOwnerShip da classe Win32_ShortcutFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ShortcutFile.TakeOwnerShip
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5da7a237ae1943e65bc1cc757d5c4a16c6df8900
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920186"
---
# <a name="takeownership-method-of-the-win32_shortcutfile-class"></a><span data-ttu-id="fb4ab-103">Método TakeOwnerShip da \_ classe shortcutfile do Win32</span><span class="sxs-lookup"><span data-stu-id="fb4ab-103">TakeOwnerShip method of the Win32\_ShortcutFile class</span></span>

<span data-ttu-id="fb4ab-104">O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **TakeOwnership** Obtém a propriedade do arquivo lógico especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="fb4ab-104">The **TakeOwnerShip** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="fb4ab-105">Se o arquivo lógico for realmente um diretório, o **TakeOwnership** agirá recursivamente, assumindo a propriedade de todos os arquivos e subdiretórios contidos no diretório.</span><span class="sxs-lookup"><span data-stu-id="fb4ab-105">If the logical file is actually a directory, then **TakeOwnerShip** acts recursively, taking ownership of all the files and subdirectories the directory contains.</span></span>

<span data-ttu-id="fb4ab-106">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="fb4ab-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="fb4ab-107">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="fb4ab-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="fb4ab-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fb4ab-108">Syntax</span></span>


```mof
uint32 TakeOwnerShip();
```



## <a name="parameters"></a><span data-ttu-id="fb4ab-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fb4ab-109">Parameters</span></span>

<span data-ttu-id="fb4ab-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="fb4ab-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fb4ab-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fb4ab-111">Return value</span></span>

<span data-ttu-id="fb4ab-112">Retorna um dos valores inteiros a seguir.</span><span class="sxs-lookup"><span data-stu-id="fb4ab-112">Returns one of the following integer values.</span></span>

<dl> <dt>

<span data-ttu-id="fb4ab-113">**0**</span><span class="sxs-lookup"><span data-stu-id="fb4ab-113">**0**</span></span>
</dt> <dd>

<span data-ttu-id="fb4ab-114">A solicitação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="fb4ab-114">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="fb4ab-115">**2**</span><span class="sxs-lookup"><span data-stu-id="fb4ab-115">**2**</span></span>
</dt> <dd>

<span data-ttu-id="fb4ab-116">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="fb4ab-116">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="fb4ab-117">**8**</span><span class="sxs-lookup"><span data-stu-id="fb4ab-117">**8**</span></span>
</dt> <dd>

<span data-ttu-id="fb4ab-118">Ocorreu uma falha não especificada.</span><span class="sxs-lookup"><span data-stu-id="fb4ab-118">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="fb4ab-119">**9**</span><span class="sxs-lookup"><span data-stu-id="fb4ab-119">**9**</span></span>
</dt> <dd>

<span data-ttu-id="fb4ab-120">O nome especificado não era válido.</span><span class="sxs-lookup"><span data-stu-id="fb4ab-120">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="fb4ab-121">**10**</span><span class="sxs-lookup"><span data-stu-id="fb4ab-121">**10**</span></span>
</dt> <dd>

<span data-ttu-id="fb4ab-122">O objeto especificado já existe.</span><span class="sxs-lookup"><span data-stu-id="fb4ab-122">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="fb4ab-123">**11**</span><span class="sxs-lookup"><span data-stu-id="fb4ab-123">**11**</span></span>
</dt> <dd>

<span data-ttu-id="fb4ab-124">O sistema de arquivos não é NTFS.</span><span class="sxs-lookup"><span data-stu-id="fb4ab-124">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="fb4ab-125">**12**</span><span class="sxs-lookup"><span data-stu-id="fb4ab-125">**12**</span></span>
</dt> <dd>

<span data-ttu-id="fb4ab-126">A plataforma não é o Windows.</span><span class="sxs-lookup"><span data-stu-id="fb4ab-126">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="fb4ab-127">**13**</span><span class="sxs-lookup"><span data-stu-id="fb4ab-127">**13**</span></span>
</dt> <dd>

<span data-ttu-id="fb4ab-128">A unidade não é a mesma.</span><span class="sxs-lookup"><span data-stu-id="fb4ab-128">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="fb4ab-129">**14**</span><span class="sxs-lookup"><span data-stu-id="fb4ab-129">**14**</span></span>
</dt> <dd>

<span data-ttu-id="fb4ab-130">O diretório não está vazio.</span><span class="sxs-lookup"><span data-stu-id="fb4ab-130">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="fb4ab-131">**15**</span><span class="sxs-lookup"><span data-stu-id="fb4ab-131">**15**</span></span>
</dt> <dd>

<span data-ttu-id="fb4ab-132">Houve uma violação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="fb4ab-132">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="fb4ab-133">**16**</span><span class="sxs-lookup"><span data-stu-id="fb4ab-133">**16**</span></span>
</dt> <dd>

<span data-ttu-id="fb4ab-134">O arquivo de inicialização especificado não era válido.</span><span class="sxs-lookup"><span data-stu-id="fb4ab-134">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="fb4ab-135">**17**</span><span class="sxs-lookup"><span data-stu-id="fb4ab-135">**17**</span></span>
</dt> <dd>

<span data-ttu-id="fb4ab-136">Um privilégio necessário para a operação não é mantido.</span><span class="sxs-lookup"><span data-stu-id="fb4ab-136">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="fb4ab-137">**Abril**</span><span class="sxs-lookup"><span data-stu-id="fb4ab-137">**21**</span></span>
</dt> <dd>

<span data-ttu-id="fb4ab-138">Um parâmetro especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="fb4ab-138">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fb4ab-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb4ab-139">Requirements</span></span>



| <span data-ttu-id="fb4ab-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb4ab-140">Requirement</span></span> | <span data-ttu-id="fb4ab-141">Valor</span><span class="sxs-lookup"><span data-stu-id="fb4ab-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fb4ab-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fb4ab-142">Minimum supported client</span></span><br/> | <span data-ttu-id="fb4ab-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fb4ab-143">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fb4ab-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fb4ab-144">Minimum supported server</span></span><br/> | <span data-ttu-id="fb4ab-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fb4ab-145">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fb4ab-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="fb4ab-146">Namespace</span></span><br/>                | <span data-ttu-id="fb4ab-147">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="fb4ab-147">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="fb4ab-148">MOF</span><span class="sxs-lookup"><span data-stu-id="fb4ab-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fb4ab-149"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fb4ab-149"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="fb4ab-150">DLL</span><span class="sxs-lookup"><span data-stu-id="fb4ab-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb4ab-151"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb4ab-151"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb4ab-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="fb4ab-152">See also</span></span>

<dl> <dt>

<span data-ttu-id="fb4ab-153">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fb4ab-153">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="fb4ab-154">**Atalho do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="fb4ab-154">**Win32\_ShortcutFile**</span></span>](win32-shortcutfile.md)
</dt> </dl>

 

