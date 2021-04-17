---
description: Copia o arquivo de atalho lógico ou o diretório especificado no caminho do objeto para o local especificado pelo parâmetro FileName. Esse método é uma versão estendida do método Copy.
ms.assetid: 06b629bb-d35e-4bc2-b0e5-c6a981b6d968
ms.tgt_platform: multiple
title: Método CopyEx da classe Win32_ShortcutFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ShortcutFile.CopyEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6cbf1cbb622610a01a533195752b3532b25f8959
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105755843"
---
# <a name="copyex-method-of-the-win32_shortcutfile-class"></a><span data-ttu-id="e8da3-104">Método CopyEx da \_ classe shortcutfile do Win32</span><span class="sxs-lookup"><span data-stu-id="e8da3-104">CopyEx method of the Win32\_ShortcutFile class</span></span>

<span data-ttu-id="e8da3-105">O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **CopyEx** copia o arquivo de atalho lógico ou o diretório especificado no caminho do objeto para o local especificado pelo parâmetro *filename* .</span><span class="sxs-lookup"><span data-stu-id="e8da3-105">The **CopyEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method copies the logical shortcut file or directory specified in the object path to the location specified by the *FileName* parameter.</span></span> <span data-ttu-id="e8da3-106">Esse método é uma versão estendida do método [**Copy**](copy-method-in-class-win32-directory.md) .</span><span class="sxs-lookup"><span data-stu-id="e8da3-106">This method is an extended version of the [**Copy**](copy-method-in-class-win32-directory.md) method.</span></span> <span data-ttu-id="e8da3-107">Não haverá suporte para uma cópia se a substituição de um arquivo lógico existente for necessária.</span><span class="sxs-lookup"><span data-stu-id="e8da3-107">A copy is not supported if overwriting an existing logical file is required.</span></span>

<span data-ttu-id="e8da3-108">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="e8da3-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="e8da3-109">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="e8da3-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="e8da3-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e8da3-110">Syntax</span></span>


```mof
uint32 CopyEx(
  [in]           string  FileName,
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="e8da3-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e8da3-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8da3-112">*Nome do arquivo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e8da3-112">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8da3-113">Nome totalmente qualificado da cópia do arquivo (ou diretório).</span><span class="sxs-lookup"><span data-stu-id="e8da3-113">Fully qualified name of the copy of the file (or directory).</span></span>

<span data-ttu-id="e8da3-114">Exemplo: c: \\ temp \\ newdirectory.</span><span class="sxs-lookup"><span data-stu-id="e8da3-114">Example: c:\\temp\\newdirectory.</span></span>

</dd> <dt>

<span data-ttu-id="e8da3-115">*StopFileName* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e8da3-115">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e8da3-116">Nome do arquivo ou diretório em que o método **CopyEx** falhou.</span><span class="sxs-lookup"><span data-stu-id="e8da3-116">Name of the file or directory where the **CopyEx** method failed.</span></span> <span data-ttu-id="e8da3-117">Esse parâmetro será **nulo** se o método tiver sucesso.</span><span class="sxs-lookup"><span data-stu-id="e8da3-117">This parameter is **NULL** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="e8da3-118">*StartFileName* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="e8da3-118">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e8da3-119">Nomeia o arquivo ou diretório filho a ser usado como ponto de partida para **CopyEx**.</span><span class="sxs-lookup"><span data-stu-id="e8da3-119">Names the child file or directory to use as a starting point for **CopyEx**.</span></span> <span data-ttu-id="e8da3-120">O parâmetro *StartFileName* normalmente é o parâmetro *StopFileName* que especifica o arquivo ou diretório no qual ocorreu um erro da chamada do método anterior.</span><span class="sxs-lookup"><span data-stu-id="e8da3-120">The *StartFileName* parameter is typically the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="e8da3-121">Se esse parâmetro for **nulo**, a operação será executada no arquivo ou diretório especificado na chamada de ExecMethod.</span><span class="sxs-lookup"><span data-stu-id="e8da3-121">If this parameter is **NULL**, the operation is performed on the file or directory specified in the ExecMethod call.</span></span>

</dd> <dt>

<span data-ttu-id="e8da3-122">*Recursivo* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="e8da3-122">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e8da3-123">Se **for true**, a alteração de propriedade será aplicada recursivamente aos arquivos e diretórios dentro do diretório especificado pela instância [**de \_ LogicalFile do CIM**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="e8da3-123">If **true**, the change of ownership will be applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span>

> [!Note]  
> <span data-ttu-id="e8da3-124">Para instâncias de arquivo, o parâmetro de entrada *recursivo* é ignorado.</span><span class="sxs-lookup"><span data-stu-id="e8da3-124">For file instances, the *Recursive* input parameter is ignored.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8da3-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e8da3-125">Return value</span></span>

<span data-ttu-id="e8da3-126">Retorna um valor de 0 (zero) se o arquivo foi copiado com êxito e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="e8da3-126">Returns a value of 0 (zero) if the file was successfully copied, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="e8da3-127">**0**</span><span class="sxs-lookup"><span data-stu-id="e8da3-127">**0**</span></span>
</dt> <dd>

<span data-ttu-id="e8da3-128">A solicitação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="e8da3-128">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="e8da3-129">**2**</span><span class="sxs-lookup"><span data-stu-id="e8da3-129">**2**</span></span>
</dt> <dd>

<span data-ttu-id="e8da3-130">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="e8da3-130">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="e8da3-131">**8**</span><span class="sxs-lookup"><span data-stu-id="e8da3-131">**8**</span></span>
</dt> <dd>

<span data-ttu-id="e8da3-132">Ocorreu uma falha não especificada.</span><span class="sxs-lookup"><span data-stu-id="e8da3-132">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="e8da3-133">**9**</span><span class="sxs-lookup"><span data-stu-id="e8da3-133">**9**</span></span>
</dt> <dd>

<span data-ttu-id="e8da3-134">O nome especificado não era válido.</span><span class="sxs-lookup"><span data-stu-id="e8da3-134">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="e8da3-135">**10**</span><span class="sxs-lookup"><span data-stu-id="e8da3-135">**10**</span></span>
</dt> <dd>

<span data-ttu-id="e8da3-136">O objeto especificado já existe.</span><span class="sxs-lookup"><span data-stu-id="e8da3-136">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="e8da3-137">**11**</span><span class="sxs-lookup"><span data-stu-id="e8da3-137">**11**</span></span>
</dt> <dd>

<span data-ttu-id="e8da3-138">O sistema de arquivos não é NTFS.</span><span class="sxs-lookup"><span data-stu-id="e8da3-138">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="e8da3-139">**12**</span><span class="sxs-lookup"><span data-stu-id="e8da3-139">**12**</span></span>
</dt> <dd>

<span data-ttu-id="e8da3-140">A plataforma não é o Windows.</span><span class="sxs-lookup"><span data-stu-id="e8da3-140">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="e8da3-141">**13**</span><span class="sxs-lookup"><span data-stu-id="e8da3-141">**13**</span></span>
</dt> <dd>

<span data-ttu-id="e8da3-142">A unidade não é a mesma.</span><span class="sxs-lookup"><span data-stu-id="e8da3-142">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="e8da3-143">**14**</span><span class="sxs-lookup"><span data-stu-id="e8da3-143">**14**</span></span>
</dt> <dd>

<span data-ttu-id="e8da3-144">O diretório não está vazio.</span><span class="sxs-lookup"><span data-stu-id="e8da3-144">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="e8da3-145">**15**</span><span class="sxs-lookup"><span data-stu-id="e8da3-145">**15**</span></span>
</dt> <dd>

<span data-ttu-id="e8da3-146">Houve uma violação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="e8da3-146">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="e8da3-147">**16**</span><span class="sxs-lookup"><span data-stu-id="e8da3-147">**16**</span></span>
</dt> <dd>

<span data-ttu-id="e8da3-148">O arquivo de inicialização especificado não era válido.</span><span class="sxs-lookup"><span data-stu-id="e8da3-148">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="e8da3-149">**17**</span><span class="sxs-lookup"><span data-stu-id="e8da3-149">**17**</span></span>
</dt> <dd>

<span data-ttu-id="e8da3-150">Um privilégio necessário para a operação não é mantido.</span><span class="sxs-lookup"><span data-stu-id="e8da3-150">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="e8da3-151">**Abril**</span><span class="sxs-lookup"><span data-stu-id="e8da3-151">**21**</span></span>
</dt> <dd>

<span data-ttu-id="e8da3-152">Um parâmetro especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="e8da3-152">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e8da3-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e8da3-153">Requirements</span></span>



| <span data-ttu-id="e8da3-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8da3-154">Requirement</span></span> | <span data-ttu-id="e8da3-155">Valor</span><span class="sxs-lookup"><span data-stu-id="e8da3-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e8da3-156">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e8da3-156">Minimum supported client</span></span><br/> | <span data-ttu-id="e8da3-157">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e8da3-157">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e8da3-158">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e8da3-158">Minimum supported server</span></span><br/> | <span data-ttu-id="e8da3-159">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e8da3-159">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e8da3-160">Namespace</span><span class="sxs-lookup"><span data-stu-id="e8da3-160">Namespace</span></span><br/>                | <span data-ttu-id="e8da3-161">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="e8da3-161">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e8da3-162">MOF</span><span class="sxs-lookup"><span data-stu-id="e8da3-162">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e8da3-163"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e8da3-163"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e8da3-164">DLL</span><span class="sxs-lookup"><span data-stu-id="e8da3-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e8da3-165"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e8da3-165"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8da3-166">Confira também</span><span class="sxs-lookup"><span data-stu-id="e8da3-166">See also</span></span>

<dl> <dt>

<span data-ttu-id="e8da3-167">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e8da3-167">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="e8da3-168">**Atalho do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="e8da3-168">**Win32\_ShortcutFile**</span></span>](win32-shortcutfile.md)
</dt> </dl>

 

