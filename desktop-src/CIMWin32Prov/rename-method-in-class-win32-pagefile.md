---
description: Renomeia o arquivo de paginação especificado no caminho do objeto.
ms.assetid: 6a98e05f-337e-4224-a847-f01913031b20
ms.tgt_platform: multiple
title: Método Rename da classe Win32_PageFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFile.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7c9ba8162cd115a567e9e9010420c558061fed08
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754392"
---
# <a name="rename-method-of-the-win32_pagefile-class"></a><span data-ttu-id="d80bd-103">Método Rename da classe de \_ arquivo de paginação Win32</span><span class="sxs-lookup"><span data-stu-id="d80bd-103">Rename method of the Win32\_PageFile class</span></span>

<span data-ttu-id="d80bd-104">O método **renomear** [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) renomeia o arquivo de paginação especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="d80bd-104">The **Rename** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method renames the paging file specified in the object path.</span></span> <span data-ttu-id="d80bd-105">Não haverá suporte para renomear se o destino estiver em outra unidade ou se for necessário substituir um arquivo lógico existente.</span><span class="sxs-lookup"><span data-stu-id="d80bd-105">A rename is not supported if the destination is on another drive or if overwriting an existing logical file is required.</span></span>

<span data-ttu-id="d80bd-106">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="d80bd-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="d80bd-107">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="d80bd-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="d80bd-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d80bd-108">Syntax</span></span>


```mof
uint32 Rename(
  [in] string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="d80bd-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d80bd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d80bd-110">*Nome do arquivo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d80bd-110">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d80bd-111">Novo nome totalmente qualificado do arquivo (ou diretório).</span><span class="sxs-lookup"><span data-stu-id="d80bd-111">Fully qualified new name of the file (or directory).</span></span>

<span data-ttu-id="d80bd-112">Exemplo: c: \\ temp \\newfile.txt</span><span class="sxs-lookup"><span data-stu-id="d80bd-112">Example: c:\\temp\\newfile.txt</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d80bd-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d80bd-113">Return value</span></span>

<span data-ttu-id="d80bd-114">Retorna um valor de 0 (zero) se o arquivo tiver sido renomeado com êxito e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="d80bd-114">Returns a value of 0 (zero) if the file was successfully renamed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="d80bd-115">**0**</span><span class="sxs-lookup"><span data-stu-id="d80bd-115">**0**</span></span>
</dt> <dd>

<span data-ttu-id="d80bd-116">A solicitação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="d80bd-116">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="d80bd-117">**2**</span><span class="sxs-lookup"><span data-stu-id="d80bd-117">**2**</span></span>
</dt> <dd>

<span data-ttu-id="d80bd-118">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="d80bd-118">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="d80bd-119">**8**</span><span class="sxs-lookup"><span data-stu-id="d80bd-119">**8**</span></span>
</dt> <dd>

<span data-ttu-id="d80bd-120">Ocorreu uma falha não especificada.</span><span class="sxs-lookup"><span data-stu-id="d80bd-120">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="d80bd-121">**9**</span><span class="sxs-lookup"><span data-stu-id="d80bd-121">**9**</span></span>
</dt> <dd>

<span data-ttu-id="d80bd-122">O nome especificado não era válido.</span><span class="sxs-lookup"><span data-stu-id="d80bd-122">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="d80bd-123">**10**</span><span class="sxs-lookup"><span data-stu-id="d80bd-123">**10**</span></span>
</dt> <dd>

<span data-ttu-id="d80bd-124">O objeto especificado já existe.</span><span class="sxs-lookup"><span data-stu-id="d80bd-124">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="d80bd-125">**11**</span><span class="sxs-lookup"><span data-stu-id="d80bd-125">**11**</span></span>
</dt> <dd>

<span data-ttu-id="d80bd-126">O sistema de arquivos não é NTFS.</span><span class="sxs-lookup"><span data-stu-id="d80bd-126">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="d80bd-127">**12**</span><span class="sxs-lookup"><span data-stu-id="d80bd-127">**12**</span></span>
</dt> <dd>

<span data-ttu-id="d80bd-128">A plataforma não é o Windows.</span><span class="sxs-lookup"><span data-stu-id="d80bd-128">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="d80bd-129">**13**</span><span class="sxs-lookup"><span data-stu-id="d80bd-129">**13**</span></span>
</dt> <dd>

<span data-ttu-id="d80bd-130">A unidade não é a mesma.</span><span class="sxs-lookup"><span data-stu-id="d80bd-130">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="d80bd-131">**14**</span><span class="sxs-lookup"><span data-stu-id="d80bd-131">**14**</span></span>
</dt> <dd>

<span data-ttu-id="d80bd-132">O diretório não está vazio.</span><span class="sxs-lookup"><span data-stu-id="d80bd-132">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="d80bd-133">**15**</span><span class="sxs-lookup"><span data-stu-id="d80bd-133">**15**</span></span>
</dt> <dd>

<span data-ttu-id="d80bd-134">Houve uma violação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="d80bd-134">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="d80bd-135">**16**</span><span class="sxs-lookup"><span data-stu-id="d80bd-135">**16**</span></span>
</dt> <dd>

<span data-ttu-id="d80bd-136">O arquivo de inicialização especificado não era válido.</span><span class="sxs-lookup"><span data-stu-id="d80bd-136">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="d80bd-137">**17**</span><span class="sxs-lookup"><span data-stu-id="d80bd-137">**17**</span></span>
</dt> <dd>

<span data-ttu-id="d80bd-138">Um privilégio necessário para a operação não é mantido.</span><span class="sxs-lookup"><span data-stu-id="d80bd-138">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="d80bd-139">**Abril**</span><span class="sxs-lookup"><span data-stu-id="d80bd-139">**21**</span></span>
</dt> <dd>

<span data-ttu-id="d80bd-140">Um parâmetro especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="d80bd-140">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d80bd-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d80bd-141">Requirements</span></span>



| <span data-ttu-id="d80bd-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="d80bd-142">Requirement</span></span> | <span data-ttu-id="d80bd-143">Valor</span><span class="sxs-lookup"><span data-stu-id="d80bd-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d80bd-144">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d80bd-144">Minimum supported client</span></span><br/> | <span data-ttu-id="d80bd-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d80bd-145">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d80bd-146">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d80bd-146">Minimum supported server</span></span><br/> | <span data-ttu-id="d80bd-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d80bd-147">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d80bd-148">Namespace</span><span class="sxs-lookup"><span data-stu-id="d80bd-148">Namespace</span></span><br/>                | <span data-ttu-id="d80bd-149">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="d80bd-149">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d80bd-150">MOF</span><span class="sxs-lookup"><span data-stu-id="d80bd-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d80bd-151"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d80bd-151"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d80bd-152">DLL</span><span class="sxs-lookup"><span data-stu-id="d80bd-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d80bd-153"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d80bd-153"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d80bd-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="d80bd-154">See also</span></span>

<dl> <dt>

<span data-ttu-id="d80bd-155">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d80bd-155">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="d80bd-156">**\_Arquivo de paginação Win32**</span><span class="sxs-lookup"><span data-stu-id="d80bd-156">**Win32\_PageFile**</span></span>](win32-pagefile.md)
</dt> </dl>

 

