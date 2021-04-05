---
description: Copia o arquivo de entrada de diretório lógico ou o diretório especificado no caminho do objeto para o local especificado pelo parâmetro FileName. Esse método é uma versão estendida do método Copy.
ms.assetid: c15bd1ae-a60d-4875-a76e-99486820c42c
ms.tgt_platform: multiple
title: Método CopyEx da classe Win32_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.CopyEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 55f2fdb0aa4e8306e8ec0aa4f5f265c0a8ee6689
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826708"
---
# <a name="copyex-method-of-the-win32_directory-class"></a><span data-ttu-id="1f8d5-104">Método CopyEx da classe do \_ diretório Win32</span><span class="sxs-lookup"><span data-stu-id="1f8d5-104">CopyEx method of the Win32\_Directory class</span></span>

<span data-ttu-id="1f8d5-105">O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **CopyEx** copia o arquivo de entrada de diretório lógico ou o diretório especificado no caminho do objeto para o local especificado pelo parâmetro *filename* .</span><span class="sxs-lookup"><span data-stu-id="1f8d5-105">The **CopyEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method copies the logical directory entry file or directory specified in the object path to the location specified by the *FileName* parameter.</span></span> <span data-ttu-id="1f8d5-106">Esse método é uma versão estendida do método [**Copy**](copy-method-in-class-win32-directory.md) .</span><span class="sxs-lookup"><span data-stu-id="1f8d5-106">This method is an extended version of the [**Copy**](copy-method-in-class-win32-directory.md) method.</span></span> <span data-ttu-id="1f8d5-107">Não haverá suporte para uma cópia se a substituição de um arquivo lógico existente for necessária.</span><span class="sxs-lookup"><span data-stu-id="1f8d5-107">A copy is not supported if overwriting an existing logical file is required.</span></span>

<span data-ttu-id="1f8d5-108">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="1f8d5-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="1f8d5-109">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="1f8d5-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="1f8d5-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1f8d5-110">Syntax</span></span>


```mof
uint32 CopyEx(
  [in]           string  FileName,
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="1f8d5-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1f8d5-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f8d5-112">*Nome do arquivo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1f8d5-112">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f8d5-113">Nome totalmente qualificado da cópia do arquivo (ou diretório).</span><span class="sxs-lookup"><span data-stu-id="1f8d5-113">Fully qualified name of the copy of the file (or directory).</span></span> <span data-ttu-id="1f8d5-114">Exemplo: c: \\ temp \\ newdirectory.</span><span class="sxs-lookup"><span data-stu-id="1f8d5-114">Example: c:\\temp\\newdirectory.</span></span>

</dd> <dt>

<span data-ttu-id="1f8d5-115">*StopFileName* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="1f8d5-115">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1f8d5-116">Nome do arquivo ou diretório em que o método **CopyEx** falhou.</span><span class="sxs-lookup"><span data-stu-id="1f8d5-116">Name of the file or directory where the **CopyEx** method failed.</span></span> <span data-ttu-id="1f8d5-117">Esse parâmetro será **NULL** se o método tiver sucesso.</span><span class="sxs-lookup"><span data-stu-id="1f8d5-117">This parameter will be **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="1f8d5-118">*StartFileName* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="1f8d5-118">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1f8d5-119">Nomeia o arquivo ou diretório filho a ser usado como ponto de partida para **CopyEx**.</span><span class="sxs-lookup"><span data-stu-id="1f8d5-119">Names the child file or directory to use as a starting point for **CopyEx**.</span></span> <span data-ttu-id="1f8d5-120">O parâmetro *StartFileName* normalmente é o parâmetro *StopFileName* que especifica o arquivo ou diretório no qual ocorreu um erro da chamada do método anterior.</span><span class="sxs-lookup"><span data-stu-id="1f8d5-120">The *StartFileName* parameter is typically the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="1f8d5-121">Se esse parâmetro for **nulo**, a operação será executada no arquivo ou diretório especificado na chamada de **ExecMethod** .</span><span class="sxs-lookup"><span data-stu-id="1f8d5-121">If this parameter is **NULL**, the operation is performed on the file or directory specified in the **ExecMethod** call.</span></span>

<span data-ttu-id="1f8d5-122">Se o *StartFileName* for usado, *recursivo* deverá ser definido como true também.</span><span class="sxs-lookup"><span data-stu-id="1f8d5-122">If *StartFileName* is used, *Recursive* must be set to true as well.</span></span>

</dd> <dt>

<span data-ttu-id="1f8d5-123">*Recursivo* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="1f8d5-123">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1f8d5-124">Se **for true**, os arquivos e diretórios serão copiados recursivamente dentro do diretório especificado pela instância de [**\_ LogicalFile do CIM**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="1f8d5-124">If **true**, files and directories will be copied recursively within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span>

> [!Note]  
> <span data-ttu-id="1f8d5-125">Para instâncias de arquivo, o parâmetro de entrada *recursivo* é ignorado.</span><span class="sxs-lookup"><span data-stu-id="1f8d5-125">For file instances, the *Recursive* input parameter is ignored.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f8d5-126">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1f8d5-126">Return value</span></span>

<span data-ttu-id="1f8d5-127">Retorna um valor de 0 (zero) se o arquivo foi copiado com êxito e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="1f8d5-127">Returns a value of 0 (zero) if the file was successfully copied, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="1f8d5-128">**0**</span><span class="sxs-lookup"><span data-stu-id="1f8d5-128">**0**</span></span>
</dt> <dd>

<span data-ttu-id="1f8d5-129">A solicitação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="1f8d5-129">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="1f8d5-130">**2**</span><span class="sxs-lookup"><span data-stu-id="1f8d5-130">**2**</span></span>
</dt> <dd>

<span data-ttu-id="1f8d5-131">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="1f8d5-131">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="1f8d5-132">**8**</span><span class="sxs-lookup"><span data-stu-id="1f8d5-132">**8**</span></span>
</dt> <dd>

<span data-ttu-id="1f8d5-133">Ocorreu uma falha não especificada.</span><span class="sxs-lookup"><span data-stu-id="1f8d5-133">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="1f8d5-134">**9**</span><span class="sxs-lookup"><span data-stu-id="1f8d5-134">**9**</span></span>
</dt> <dd>

<span data-ttu-id="1f8d5-135">O nome especificado não era válido.</span><span class="sxs-lookup"><span data-stu-id="1f8d5-135">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="1f8d5-136">**10**</span><span class="sxs-lookup"><span data-stu-id="1f8d5-136">**10**</span></span>
</dt> <dd>

<span data-ttu-id="1f8d5-137">O objeto especificado já existe.</span><span class="sxs-lookup"><span data-stu-id="1f8d5-137">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="1f8d5-138">**11**</span><span class="sxs-lookup"><span data-stu-id="1f8d5-138">**11**</span></span>
</dt> <dd>

<span data-ttu-id="1f8d5-139">O sistema de arquivos não é NTFS.</span><span class="sxs-lookup"><span data-stu-id="1f8d5-139">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="1f8d5-140">**12**</span><span class="sxs-lookup"><span data-stu-id="1f8d5-140">**12**</span></span>
</dt> <dd>

<span data-ttu-id="1f8d5-141">A plataforma não é o Windows.</span><span class="sxs-lookup"><span data-stu-id="1f8d5-141">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="1f8d5-142">**13**</span><span class="sxs-lookup"><span data-stu-id="1f8d5-142">**13**</span></span>
</dt> <dd>

<span data-ttu-id="1f8d5-143">A unidade não é a mesma.</span><span class="sxs-lookup"><span data-stu-id="1f8d5-143">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="1f8d5-144">**14**</span><span class="sxs-lookup"><span data-stu-id="1f8d5-144">**14**</span></span>
</dt> <dd>

<span data-ttu-id="1f8d5-145">O diretório não está vazio.</span><span class="sxs-lookup"><span data-stu-id="1f8d5-145">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="1f8d5-146">**15**</span><span class="sxs-lookup"><span data-stu-id="1f8d5-146">**15**</span></span>
</dt> <dd>

<span data-ttu-id="1f8d5-147">Houve uma violação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="1f8d5-147">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="1f8d5-148">**16**</span><span class="sxs-lookup"><span data-stu-id="1f8d5-148">**16**</span></span>
</dt> <dd>

<span data-ttu-id="1f8d5-149">O arquivo de inicialização especificado não era válido.</span><span class="sxs-lookup"><span data-stu-id="1f8d5-149">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="1f8d5-150">**17**</span><span class="sxs-lookup"><span data-stu-id="1f8d5-150">**17**</span></span>
</dt> <dd>

<span data-ttu-id="1f8d5-151">Um privilégio necessário para a operação não é mantido.</span><span class="sxs-lookup"><span data-stu-id="1f8d5-151">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="1f8d5-152">**Abril**</span><span class="sxs-lookup"><span data-stu-id="1f8d5-152">**21**</span></span>
</dt> <dd>

<span data-ttu-id="1f8d5-153">Um parâmetro especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="1f8d5-153">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1f8d5-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1f8d5-154">Requirements</span></span>



| <span data-ttu-id="1f8d5-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f8d5-155">Requirement</span></span> | <span data-ttu-id="1f8d5-156">Valor</span><span class="sxs-lookup"><span data-stu-id="1f8d5-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1f8d5-157">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1f8d5-157">Minimum supported client</span></span><br/> | <span data-ttu-id="1f8d5-158">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1f8d5-158">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1f8d5-159">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1f8d5-159">Minimum supported server</span></span><br/> | <span data-ttu-id="1f8d5-160">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1f8d5-160">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1f8d5-161">Namespace</span><span class="sxs-lookup"><span data-stu-id="1f8d5-161">Namespace</span></span><br/>                | <span data-ttu-id="1f8d5-162">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="1f8d5-162">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1f8d5-163">MOF</span><span class="sxs-lookup"><span data-stu-id="1f8d5-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1f8d5-164"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1f8d5-164"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1f8d5-165">DLL</span><span class="sxs-lookup"><span data-stu-id="1f8d5-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1f8d5-166"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1f8d5-166"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f8d5-167">Confira também</span><span class="sxs-lookup"><span data-stu-id="1f8d5-167">See also</span></span>

<dl> <dt>

<span data-ttu-id="1f8d5-168">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1f8d5-168">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="1f8d5-169">**\_Diretório Win32**</span><span class="sxs-lookup"><span data-stu-id="1f8d5-169">**Win32\_Directory**</span></span>](win32-directory.md)
</dt> </dl>

 

