---
description: Renomeia o arquivo de codec especificado no caminho do objeto.
ms.assetid: fd6ce02c-d513-4643-ac27-313c32732f1e
ms.tgt_platform: multiple
title: Método Rename da classe Win32_CodecFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a4eb931a0155518ad9644ebb1cce0b604be80602
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920505"
---
# <a name="rename-method-of-the-win32_codecfile-class"></a><span data-ttu-id="75e03-103">Método Rename da classe do \_ codec do Win32</span><span class="sxs-lookup"><span data-stu-id="75e03-103">Rename method of the Win32\_CodecFile class</span></span>

<span data-ttu-id="75e03-104">O método **renomear** [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) renomeia o arquivo de codec especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="75e03-104">The **Rename** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method renames the codec file specified in the object path.</span></span> <span data-ttu-id="75e03-105">Não haverá suporte para renomear se o destino estiver em outra unidade ou se for necessário substituir um arquivo lógico existente.</span><span class="sxs-lookup"><span data-stu-id="75e03-105">A rename is not supported if the destination is on another drive or if overwriting an existing logical file is required.</span></span>

<span data-ttu-id="75e03-106">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="75e03-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="75e03-107">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="75e03-107">For more information about using this method see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="75e03-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="75e03-108">Syntax</span></span>


```mof
uint32 Rename(
   string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="75e03-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="75e03-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75e03-110">*FileName*</span><span class="sxs-lookup"><span data-stu-id="75e03-110">*FileName*</span></span> 
</dt> <dd>

<span data-ttu-id="75e03-111">Novo nome totalmente qualificado do arquivo (ou diretório).</span><span class="sxs-lookup"><span data-stu-id="75e03-111">Fully qualified new name of the file (or directory).</span></span> <span data-ttu-id="75e03-112">Exemplo: c: \\ temp \\newfile.txt.</span><span class="sxs-lookup"><span data-stu-id="75e03-112">Example: c:\\temp\\newfile.txt.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75e03-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="75e03-113">Return value</span></span>

<span data-ttu-id="75e03-114">Retorna um valor inteiro de 0 (zero) se o arquivo tiver sido renomeado com êxito e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="75e03-114">Returns an integer value of 0 (zero) if the file was successfully renamed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="75e03-115">**0**</span><span class="sxs-lookup"><span data-stu-id="75e03-115">**0**</span></span>
</dt> <dd>

<span data-ttu-id="75e03-116">A solicitação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="75e03-116">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="75e03-117">**2**</span><span class="sxs-lookup"><span data-stu-id="75e03-117">**2**</span></span>
</dt> <dd>

<span data-ttu-id="75e03-118">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="75e03-118">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="75e03-119">**8**</span><span class="sxs-lookup"><span data-stu-id="75e03-119">**8**</span></span>
</dt> <dd>

<span data-ttu-id="75e03-120">Ocorreu uma falha não especificada.</span><span class="sxs-lookup"><span data-stu-id="75e03-120">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="75e03-121">**9**</span><span class="sxs-lookup"><span data-stu-id="75e03-121">**9**</span></span>
</dt> <dd>

<span data-ttu-id="75e03-122">O nome especificado não era válido.</span><span class="sxs-lookup"><span data-stu-id="75e03-122">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="75e03-123">**10**</span><span class="sxs-lookup"><span data-stu-id="75e03-123">**10**</span></span>
</dt> <dd>

<span data-ttu-id="75e03-124">O objeto especificado já existe.</span><span class="sxs-lookup"><span data-stu-id="75e03-124">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="75e03-125">**11**</span><span class="sxs-lookup"><span data-stu-id="75e03-125">**11**</span></span>
</dt> <dd>

<span data-ttu-id="75e03-126">O sistema de arquivos não é NTFS.</span><span class="sxs-lookup"><span data-stu-id="75e03-126">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="75e03-127">**12**</span><span class="sxs-lookup"><span data-stu-id="75e03-127">**12**</span></span>
</dt> <dd>

<span data-ttu-id="75e03-128">A plataforma não é o Windows.</span><span class="sxs-lookup"><span data-stu-id="75e03-128">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="75e03-129">**13**</span><span class="sxs-lookup"><span data-stu-id="75e03-129">**13**</span></span>
</dt> <dd>

<span data-ttu-id="75e03-130">A unidade não é a mesma.</span><span class="sxs-lookup"><span data-stu-id="75e03-130">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="75e03-131">**14**</span><span class="sxs-lookup"><span data-stu-id="75e03-131">**14**</span></span>
</dt> <dd>

<span data-ttu-id="75e03-132">O diretório não está vazio.</span><span class="sxs-lookup"><span data-stu-id="75e03-132">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="75e03-133">**15**</span><span class="sxs-lookup"><span data-stu-id="75e03-133">**15**</span></span>
</dt> <dd>

<span data-ttu-id="75e03-134">Houve uma violação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="75e03-134">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="75e03-135">**16**</span><span class="sxs-lookup"><span data-stu-id="75e03-135">**16**</span></span>
</dt> <dd>

<span data-ttu-id="75e03-136">O arquivo de inicialização especificado não era válido.</span><span class="sxs-lookup"><span data-stu-id="75e03-136">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="75e03-137">**17**</span><span class="sxs-lookup"><span data-stu-id="75e03-137">**17**</span></span>
</dt> <dd>

<span data-ttu-id="75e03-138">Um privilégio necessário para a operação não é mantido.</span><span class="sxs-lookup"><span data-stu-id="75e03-138">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="75e03-139">**Abril**</span><span class="sxs-lookup"><span data-stu-id="75e03-139">**21**</span></span>
</dt> <dd>

<span data-ttu-id="75e03-140">Um parâmetro especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="75e03-140">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="75e03-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="75e03-141">Requirements</span></span>



| <span data-ttu-id="75e03-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="75e03-142">Requirement</span></span> | <span data-ttu-id="75e03-143">Valor</span><span class="sxs-lookup"><span data-stu-id="75e03-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="75e03-144">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="75e03-144">Minimum supported client</span></span><br/> | <span data-ttu-id="75e03-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="75e03-145">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="75e03-146">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="75e03-146">Minimum supported server</span></span><br/> | <span data-ttu-id="75e03-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="75e03-147">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="75e03-148">Namespace</span><span class="sxs-lookup"><span data-stu-id="75e03-148">Namespace</span></span><br/>                | <span data-ttu-id="75e03-149">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="75e03-149">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="75e03-150">MOF</span><span class="sxs-lookup"><span data-stu-id="75e03-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="75e03-151"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="75e03-151"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="75e03-152">DLL</span><span class="sxs-lookup"><span data-stu-id="75e03-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="75e03-153"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="75e03-153"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75e03-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="75e03-154">See also</span></span>

<dl> <dt>

<span data-ttu-id="75e03-155">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="75e03-155">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="75e03-156">**Codec do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="75e03-156">**Win32\_CodecFile**</span></span>](win32-codecfile.md)
</dt> </dl>

 

