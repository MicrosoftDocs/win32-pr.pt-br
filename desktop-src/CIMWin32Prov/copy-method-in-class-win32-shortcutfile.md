---
description: Copia o arquivo de atalho lógico ou o diretório especificado no caminho do objeto para o local especificado pelo parâmetro de entrada.
ms.assetid: 1c8e9eac-340b-4c37-a52e-6cfade47ccf6
ms.tgt_platform: multiple
title: Método Copy da classe Win32_ShortcutFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ShortcutFile.Copy
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 58de9d1b2a88a7fa02504f5eac91e9a55e286304
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457032"
---
# <a name="copy-method-of-the-win32_shortcutfile-class"></a><span data-ttu-id="32b93-103">Método Copy da \_ classe shortcutfile do Win32</span><span class="sxs-lookup"><span data-stu-id="32b93-103">Copy method of the Win32\_ShortcutFile class</span></span>

<span data-ttu-id="32b93-104">O método **Copy** [WMI Class](/windows/desktop/WmiSdk/retrieving-a-class) copia o arquivo de atalho lógico ou o diretório especificado no caminho do objeto para o local especificado pelo parâmetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="32b93-104">The **Copy** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method copies the logical shortcut file or directory specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="32b93-105">Não haverá suporte para uma cópia se a substituição de um arquivo lógico existente for necessária.</span><span class="sxs-lookup"><span data-stu-id="32b93-105">A copy is not supported if overwriting an existing logical file is required.</span></span>

<span data-ttu-id="32b93-106">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="32b93-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="32b93-107">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="32b93-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="32b93-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="32b93-108">Syntax</span></span>


```mof
uint32 Copy(
  [in] string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="32b93-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="32b93-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32b93-110">*Nome do arquivo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="32b93-110">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32b93-111">Nome totalmente qualificado da cópia do arquivo (ou diretório).</span><span class="sxs-lookup"><span data-stu-id="32b93-111">Fully qualified name of the copy of the file (or directory).</span></span>

<span data-ttu-id="32b93-112">Exemplo: c: \\ temp \\ newdirectory</span><span class="sxs-lookup"><span data-stu-id="32b93-112">Example: c:\\temp\\newdirectory</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32b93-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="32b93-113">Return value</span></span>

<span data-ttu-id="32b93-114">Retorna o valor 0 (zero) se o arquivo foi copiado com êxito e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="32b93-114">Returns value of 0 (zero) if the file was successfully copied, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="32b93-115">**0**</span><span class="sxs-lookup"><span data-stu-id="32b93-115">**0**</span></span>
</dt> <dd>

<span data-ttu-id="32b93-116">A solicitação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="32b93-116">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="32b93-117">**2**</span><span class="sxs-lookup"><span data-stu-id="32b93-117">**2**</span></span>
</dt> <dd>

<span data-ttu-id="32b93-118">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="32b93-118">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="32b93-119">**8**</span><span class="sxs-lookup"><span data-stu-id="32b93-119">**8**</span></span>
</dt> <dd>

<span data-ttu-id="32b93-120">Ocorreu uma falha não especificada.</span><span class="sxs-lookup"><span data-stu-id="32b93-120">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="32b93-121">**9**</span><span class="sxs-lookup"><span data-stu-id="32b93-121">**9**</span></span>
</dt> <dd>

<span data-ttu-id="32b93-122">O nome especificado não era válido.</span><span class="sxs-lookup"><span data-stu-id="32b93-122">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="32b93-123">**10**</span><span class="sxs-lookup"><span data-stu-id="32b93-123">**10**</span></span>
</dt> <dd>

<span data-ttu-id="32b93-124">O objeto especificado já existe.</span><span class="sxs-lookup"><span data-stu-id="32b93-124">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="32b93-125">**11**</span><span class="sxs-lookup"><span data-stu-id="32b93-125">**11**</span></span>
</dt> <dd>

<span data-ttu-id="32b93-126">O sistema de arquivos não é NTFS.</span><span class="sxs-lookup"><span data-stu-id="32b93-126">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="32b93-127">**12**</span><span class="sxs-lookup"><span data-stu-id="32b93-127">**12**</span></span>
</dt> <dd>

<span data-ttu-id="32b93-128">A plataforma não é o Windows.</span><span class="sxs-lookup"><span data-stu-id="32b93-128">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="32b93-129">**13**</span><span class="sxs-lookup"><span data-stu-id="32b93-129">**13**</span></span>
</dt> <dd>

<span data-ttu-id="32b93-130">A unidade não é a mesma.</span><span class="sxs-lookup"><span data-stu-id="32b93-130">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="32b93-131">**14**</span><span class="sxs-lookup"><span data-stu-id="32b93-131">**14**</span></span>
</dt> <dd>

<span data-ttu-id="32b93-132">O diretório não está vazio.</span><span class="sxs-lookup"><span data-stu-id="32b93-132">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="32b93-133">**15**</span><span class="sxs-lookup"><span data-stu-id="32b93-133">**15**</span></span>
</dt> <dd>

<span data-ttu-id="32b93-134">Houve uma violação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="32b93-134">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="32b93-135">**16**</span><span class="sxs-lookup"><span data-stu-id="32b93-135">**16**</span></span>
</dt> <dd>

<span data-ttu-id="32b93-136">O arquivo de inicialização especificado não era válido.</span><span class="sxs-lookup"><span data-stu-id="32b93-136">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="32b93-137">**17**</span><span class="sxs-lookup"><span data-stu-id="32b93-137">**17**</span></span>
</dt> <dd>

<span data-ttu-id="32b93-138">Um privilégio necessário para a operação não é mantido.</span><span class="sxs-lookup"><span data-stu-id="32b93-138">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="32b93-139">**Abril**</span><span class="sxs-lookup"><span data-stu-id="32b93-139">**21**</span></span>
</dt> <dd>

<span data-ttu-id="32b93-140">Um parâmetro especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="32b93-140">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="32b93-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="32b93-141">Requirements</span></span>



| <span data-ttu-id="32b93-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="32b93-142">Requirement</span></span> | <span data-ttu-id="32b93-143">Valor</span><span class="sxs-lookup"><span data-stu-id="32b93-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="32b93-144">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="32b93-144">Minimum supported client</span></span><br/> | <span data-ttu-id="32b93-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="32b93-145">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="32b93-146">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="32b93-146">Minimum supported server</span></span><br/> | <span data-ttu-id="32b93-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="32b93-147">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="32b93-148">Namespace</span><span class="sxs-lookup"><span data-stu-id="32b93-148">Namespace</span></span><br/>                | <span data-ttu-id="32b93-149">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="32b93-149">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="32b93-150">MOF</span><span class="sxs-lookup"><span data-stu-id="32b93-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="32b93-151"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="32b93-151"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="32b93-152">DLL</span><span class="sxs-lookup"><span data-stu-id="32b93-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="32b93-153"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="32b93-153"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32b93-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="32b93-154">See also</span></span>

<dl> <dt>

<span data-ttu-id="32b93-155">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="32b93-155">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="32b93-156">**Atalho do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="32b93-156">**Win32\_ShortcutFile**</span></span>](win32-shortcutfile.md)
</dt> </dl>

 

