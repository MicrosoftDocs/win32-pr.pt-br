---
description: Descompacta o arquivo de atalho lógico (ou diretório) especificado no caminho do objeto.
ms.assetid: e120391a-3839-4f8c-aca3-473d7f8b30bf
ms.tgt_platform: multiple
title: Descompactar método da classe Win32_ShortcutFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ShortcutFile.Uncompress
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 48267f519dce9ae5d78581050255bd8e8b02222c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646510"
---
# <a name="uncompress-method-of-the-win32_shortcutfile-class"></a><span data-ttu-id="2c57e-103">Descompactar o método da \_ classe shortcutfile do Win32</span><span class="sxs-lookup"><span data-stu-id="2c57e-103">Uncompress method of the Win32\_ShortcutFile class</span></span>

<span data-ttu-id="2c57e-104">O método **uncompactar** [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) descompacta o arquivo de atalho lógico (ou diretório) especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="2c57e-104">The **Uncompress** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method uncompresses the logical shortcut file (or directory) specified in the object path.</span></span>

<span data-ttu-id="2c57e-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="2c57e-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="2c57e-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="2c57e-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="2c57e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2c57e-107">Syntax</span></span>


```mof
uint32 Uncompress();
```



## <a name="parameters"></a><span data-ttu-id="2c57e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2c57e-108">Parameters</span></span>

<span data-ttu-id="2c57e-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="2c57e-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2c57e-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2c57e-110">Return value</span></span>

<span data-ttu-id="2c57e-111">Retorna um valor de 0 (zero) se o arquivo tiver sido descompactado com êxito e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="2c57e-111">Returns a value of 0 (zero) if the file was successfully decompressed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="2c57e-112">**0**</span><span class="sxs-lookup"><span data-stu-id="2c57e-112">**0**</span></span>
</dt> <dd>

<span data-ttu-id="2c57e-113">A solicitação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="2c57e-113">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="2c57e-114">**2**</span><span class="sxs-lookup"><span data-stu-id="2c57e-114">**2**</span></span>
</dt> <dd>

<span data-ttu-id="2c57e-115">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="2c57e-115">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="2c57e-116">**8**</span><span class="sxs-lookup"><span data-stu-id="2c57e-116">**8**</span></span>
</dt> <dd>

<span data-ttu-id="2c57e-117">Ocorreu uma falha não especificada.</span><span class="sxs-lookup"><span data-stu-id="2c57e-117">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="2c57e-118">**9**</span><span class="sxs-lookup"><span data-stu-id="2c57e-118">**9**</span></span>
</dt> <dd>

<span data-ttu-id="2c57e-119">O nome especificado não era válido.</span><span class="sxs-lookup"><span data-stu-id="2c57e-119">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="2c57e-120">**10**</span><span class="sxs-lookup"><span data-stu-id="2c57e-120">**10**</span></span>
</dt> <dd>

<span data-ttu-id="2c57e-121">O objeto especificado já existe.</span><span class="sxs-lookup"><span data-stu-id="2c57e-121">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="2c57e-122">**11**</span><span class="sxs-lookup"><span data-stu-id="2c57e-122">**11**</span></span>
</dt> <dd>

<span data-ttu-id="2c57e-123">O sistema de arquivos não é NTFS.</span><span class="sxs-lookup"><span data-stu-id="2c57e-123">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="2c57e-124">**12**</span><span class="sxs-lookup"><span data-stu-id="2c57e-124">**12**</span></span>
</dt> <dd>

<span data-ttu-id="2c57e-125">A plataforma não é o Windows.</span><span class="sxs-lookup"><span data-stu-id="2c57e-125">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="2c57e-126">**13**</span><span class="sxs-lookup"><span data-stu-id="2c57e-126">**13**</span></span>
</dt> <dd>

<span data-ttu-id="2c57e-127">A unidade não é a mesma.</span><span class="sxs-lookup"><span data-stu-id="2c57e-127">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="2c57e-128">**14**</span><span class="sxs-lookup"><span data-stu-id="2c57e-128">**14**</span></span>
</dt> <dd>

<span data-ttu-id="2c57e-129">O diretório não está vazio.</span><span class="sxs-lookup"><span data-stu-id="2c57e-129">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="2c57e-130">**15**</span><span class="sxs-lookup"><span data-stu-id="2c57e-130">**15**</span></span>
</dt> <dd>

<span data-ttu-id="2c57e-131">Houve uma violação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="2c57e-131">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="2c57e-132">**16**</span><span class="sxs-lookup"><span data-stu-id="2c57e-132">**16**</span></span>
</dt> <dd>

<span data-ttu-id="2c57e-133">O arquivo de inicialização especificado não era válido.</span><span class="sxs-lookup"><span data-stu-id="2c57e-133">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="2c57e-134">**17**</span><span class="sxs-lookup"><span data-stu-id="2c57e-134">**17**</span></span>
</dt> <dd>

<span data-ttu-id="2c57e-135">Um privilégio necessário para a operação não é mantido.</span><span class="sxs-lookup"><span data-stu-id="2c57e-135">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="2c57e-136">**Abril**</span><span class="sxs-lookup"><span data-stu-id="2c57e-136">**21**</span></span>
</dt> <dd>

<span data-ttu-id="2c57e-137">Um parâmetro especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="2c57e-137">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2c57e-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2c57e-138">Requirements</span></span>



| <span data-ttu-id="2c57e-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c57e-139">Requirement</span></span> | <span data-ttu-id="2c57e-140">Valor</span><span class="sxs-lookup"><span data-stu-id="2c57e-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2c57e-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2c57e-141">Minimum supported client</span></span><br/> | <span data-ttu-id="2c57e-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2c57e-142">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2c57e-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2c57e-143">Minimum supported server</span></span><br/> | <span data-ttu-id="2c57e-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2c57e-144">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2c57e-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="2c57e-145">Namespace</span></span><br/>                | <span data-ttu-id="2c57e-146">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="2c57e-146">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2c57e-147">MOF</span><span class="sxs-lookup"><span data-stu-id="2c57e-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2c57e-148"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2c57e-148"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2c57e-149">DLL</span><span class="sxs-lookup"><span data-stu-id="2c57e-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c57e-150"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c57e-150"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c57e-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="2c57e-151">See also</span></span>

<dl> <dt>

<span data-ttu-id="2c57e-152">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2c57e-152">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="2c57e-153">**Atalho do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="2c57e-153">**Win32\_ShortcutFile**</span></span>](win32-shortcutfile.md)
</dt> </dl>

 

