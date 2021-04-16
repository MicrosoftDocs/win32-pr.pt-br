---
description: Copia o arquivo de codec lógico ou o diretório especificado no caminho do objeto para o local especificado pelo parâmetro de entrada.
ms.assetid: 77e67b01-561b-4233-899d-fa4bbf75ecf8
ms.tgt_platform: multiple
title: Método Copy da classe Win32_CodecFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile.Copy
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e3bd6621c065192eb45176444257f1c29c897201
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105750323"
---
# <a name="copy-method-of-the-win32_codecfile-class"></a><span data-ttu-id="f0227-103">Método Copy da classe do \_ codec do Win32</span><span class="sxs-lookup"><span data-stu-id="f0227-103">Copy method of the Win32\_CodecFile class</span></span>

<span data-ttu-id="f0227-104">O método **Copy** [WMI Class](/windows/desktop/WmiSdk/retrieving-a-class) copia o arquivo de codec lógico ou o diretório especificado no caminho do objeto para o local especificado pelo parâmetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="f0227-104">The **Copy** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method copies the logical codec file or directory specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="f0227-105">Não haverá suporte para uma cópia se a substituição de um arquivo lógico existente for necessária.</span><span class="sxs-lookup"><span data-stu-id="f0227-105">A copy is not supported if overwriting an existing logical file is required.</span></span>

<span data-ttu-id="f0227-106">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="f0227-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="f0227-107">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="f0227-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="f0227-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f0227-108">Syntax</span></span>


```mof
uint32 Copy(
   string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="f0227-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f0227-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0227-110">*FileName*</span><span class="sxs-lookup"><span data-stu-id="f0227-110">*FileName*</span></span> 
</dt> <dd>

<span data-ttu-id="f0227-111">Nome totalmente qualificado da cópia do arquivo (ou diretório).</span><span class="sxs-lookup"><span data-stu-id="f0227-111">Fully qualified name of the copy of the file (or directory).</span></span> <span data-ttu-id="f0227-112">Exemplo: c: \\ temp \\ newdirectory.</span><span class="sxs-lookup"><span data-stu-id="f0227-112">Example: c:\\temp\\newdirectory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0227-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f0227-113">Return value</span></span>

<span data-ttu-id="f0227-114">Retorna um valor de 0 (zero) se o arquivo foi copiado com êxito e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="f0227-114">Returns an value of 0 (zero) if the file was successfully copied, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="f0227-115">**0**</span><span class="sxs-lookup"><span data-stu-id="f0227-115">**0**</span></span>
</dt> <dd>

<span data-ttu-id="f0227-116">A solicitação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="f0227-116">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="f0227-117">**2**</span><span class="sxs-lookup"><span data-stu-id="f0227-117">**2**</span></span>
</dt> <dd>

<span data-ttu-id="f0227-118">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="f0227-118">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="f0227-119">**8**</span><span class="sxs-lookup"><span data-stu-id="f0227-119">**8**</span></span>
</dt> <dd>

<span data-ttu-id="f0227-120">Ocorreu uma falha não especificada.</span><span class="sxs-lookup"><span data-stu-id="f0227-120">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="f0227-121">**9**</span><span class="sxs-lookup"><span data-stu-id="f0227-121">**9**</span></span>
</dt> <dd>

<span data-ttu-id="f0227-122">O nome especificado não era válido.</span><span class="sxs-lookup"><span data-stu-id="f0227-122">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="f0227-123">**10**</span><span class="sxs-lookup"><span data-stu-id="f0227-123">**10**</span></span>
</dt> <dd>

<span data-ttu-id="f0227-124">O objeto especificado já existe.</span><span class="sxs-lookup"><span data-stu-id="f0227-124">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="f0227-125">**11**</span><span class="sxs-lookup"><span data-stu-id="f0227-125">**11**</span></span>
</dt> <dd>

<span data-ttu-id="f0227-126">O sistema de arquivos não é NTFS.</span><span class="sxs-lookup"><span data-stu-id="f0227-126">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="f0227-127">**12**</span><span class="sxs-lookup"><span data-stu-id="f0227-127">**12**</span></span>
</dt> <dd>

<span data-ttu-id="f0227-128">A plataforma não é o Windows.</span><span class="sxs-lookup"><span data-stu-id="f0227-128">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="f0227-129">**13**</span><span class="sxs-lookup"><span data-stu-id="f0227-129">**13**</span></span>
</dt> <dd>

<span data-ttu-id="f0227-130">A unidade não é a mesma.</span><span class="sxs-lookup"><span data-stu-id="f0227-130">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="f0227-131">**14**</span><span class="sxs-lookup"><span data-stu-id="f0227-131">**14**</span></span>
</dt> <dd>

<span data-ttu-id="f0227-132">O diretório não está vazio.</span><span class="sxs-lookup"><span data-stu-id="f0227-132">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="f0227-133">**15**</span><span class="sxs-lookup"><span data-stu-id="f0227-133">**15**</span></span>
</dt> <dd>

<span data-ttu-id="f0227-134">Houve uma violação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="f0227-134">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="f0227-135">**16**</span><span class="sxs-lookup"><span data-stu-id="f0227-135">**16**</span></span>
</dt> <dd>

<span data-ttu-id="f0227-136">O arquivo de inicialização especificado não era válido.</span><span class="sxs-lookup"><span data-stu-id="f0227-136">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="f0227-137">**17**</span><span class="sxs-lookup"><span data-stu-id="f0227-137">**17**</span></span>
</dt> <dd>

<span data-ttu-id="f0227-138">Um privilégio necessário para a operação não é mantido.</span><span class="sxs-lookup"><span data-stu-id="f0227-138">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="f0227-139">**Abril**</span><span class="sxs-lookup"><span data-stu-id="f0227-139">**21**</span></span>
</dt> <dd>

<span data-ttu-id="f0227-140">Um parâmetro especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="f0227-140">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f0227-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f0227-141">Requirements</span></span>



| <span data-ttu-id="f0227-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0227-142">Requirement</span></span> | <span data-ttu-id="f0227-143">Valor</span><span class="sxs-lookup"><span data-stu-id="f0227-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f0227-144">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f0227-144">Minimum supported client</span></span><br/> | <span data-ttu-id="f0227-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f0227-145">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f0227-146">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f0227-146">Minimum supported server</span></span><br/> | <span data-ttu-id="f0227-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f0227-147">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f0227-148">Namespace</span><span class="sxs-lookup"><span data-stu-id="f0227-148">Namespace</span></span><br/>                | <span data-ttu-id="f0227-149">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="f0227-149">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f0227-150">MOF</span><span class="sxs-lookup"><span data-stu-id="f0227-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f0227-151"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f0227-151"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f0227-152">DLL</span><span class="sxs-lookup"><span data-stu-id="f0227-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f0227-153"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f0227-153"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0227-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="f0227-154">See also</span></span>

<dl> <dt>

<span data-ttu-id="f0227-155">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f0227-155">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="f0227-156">**Codec do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="f0227-156">**Win32\_CodecFile**</span></span>](win32-codecfile.md)
</dt> </dl>

 

