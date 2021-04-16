---
description: Compacta o arquivo de entrada de diretório lógico (ou diretório) especificado no caminho do objeto (esse método é uma versão estendida do método compress).
ms.assetid: 6b6e559c-4ca6-49d4-b255-5e1511fdf2e2
ms.tgt_platform: multiple
title: Método CompressEx da classe Win32_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.CompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3ee300919efa388d27ae9d594bc2b6c27def88e6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811161"
---
# <a name="compressex-method-of-the-win32_directory-class"></a><span data-ttu-id="14808-103">Método CompressEx da classe do \_ diretório Win32</span><span class="sxs-lookup"><span data-stu-id="14808-103">CompressEx method of the Win32\_Directory class</span></span>

<span data-ttu-id="14808-104">O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **CompressEx** compacta o arquivo de entrada de diretório lógico (ou diretório) especificado no caminho do objeto (esse método é uma versão estendida do método [**compress**](compress-method-in-class-win32-directory.md) ).</span><span class="sxs-lookup"><span data-stu-id="14808-104">The **CompressEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method compresses the logical directory entry file (or directory) specified in the object path (this method is an extended version of the [**Compress**](compress-method-in-class-win32-directory.md) method).</span></span>

<span data-ttu-id="14808-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="14808-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="14808-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="14808-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="14808-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="14808-107">Syntax</span></span>


```mof
uint32 CompressEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="14808-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="14808-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14808-109">*StopFileName* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="14808-109">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="14808-110">Nome do arquivo ou diretório em que o método **CompressEx** falhou.</span><span class="sxs-lookup"><span data-stu-id="14808-110">Name of the file or directory where the **CompressEx** method failed.</span></span> <span data-ttu-id="14808-111">Esse parâmetro será **NULL** se o método tiver sucesso.</span><span class="sxs-lookup"><span data-stu-id="14808-111">This parameter will be **NULL** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="14808-112">*StartFileName* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="14808-112">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="14808-113">Nomeia o arquivo ou diretório filho a ser usado como ponto de partida para **CompressEx**.</span><span class="sxs-lookup"><span data-stu-id="14808-113">Names the child file or directory to use as a starting point for **CompressEx**.</span></span> <span data-ttu-id="14808-114">O parâmetro *StartFileName* normalmente é o parâmetro *StopFileName* que especifica o arquivo ou diretório no qual ocorreu um erro da chamada do método anterior.</span><span class="sxs-lookup"><span data-stu-id="14808-114">The *StartFileName* parameter is typically the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="14808-115">Se esse parâmetro for **nulo**, a operação será executada no arquivo ou diretório especificado na chamada de **ExecMethod** .</span><span class="sxs-lookup"><span data-stu-id="14808-115">If this parameter is **NULL**, the operation is performed on the file or directory specified in the **ExecMethod** call.</span></span>

<span data-ttu-id="14808-116">Se o *StartFileName* for usado, *recursivo* deverá ser definido como true também.</span><span class="sxs-lookup"><span data-stu-id="14808-116">If *StartFileName* is used, *Recursive* must be set to true as well.</span></span>

</dd> <dt>

<span data-ttu-id="14808-117">*Recursivo* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="14808-117">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="14808-118">Se **for true**, a alteração de propriedade será aplicada recursivamente aos arquivos e diretórios dentro do diretório especificado pela instância [**de \_ LogicalFile do CIM**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="14808-118">If **true**, the change of ownership will be applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span>

> [!Note]  
> <span data-ttu-id="14808-119">Para instâncias de arquivo, o parâmetro de entrada *recursivo* é ignorado.</span><span class="sxs-lookup"><span data-stu-id="14808-119">For file instances, the *Recursive* input parameter is ignored.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14808-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="14808-120">Return value</span></span>

<span data-ttu-id="14808-121">Retorna um valor de 0 (zero) se o arquivo tiver sido compactado com êxito e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="14808-121">Returns a value of 0 (zero) if the file was successfully compressed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="14808-122">**0**</span><span class="sxs-lookup"><span data-stu-id="14808-122">**0**</span></span>
</dt> <dd>

<span data-ttu-id="14808-123">A solicitação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="14808-123">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="14808-124">**2**</span><span class="sxs-lookup"><span data-stu-id="14808-124">**2**</span></span>
</dt> <dd>

<span data-ttu-id="14808-125">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="14808-125">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="14808-126">**8**</span><span class="sxs-lookup"><span data-stu-id="14808-126">**8**</span></span>
</dt> <dd>

<span data-ttu-id="14808-127">Ocorreu uma falha não especificada.</span><span class="sxs-lookup"><span data-stu-id="14808-127">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="14808-128">**9**</span><span class="sxs-lookup"><span data-stu-id="14808-128">**9**</span></span>
</dt> <dd>

<span data-ttu-id="14808-129">O nome especificado não era válido.</span><span class="sxs-lookup"><span data-stu-id="14808-129">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="14808-130">**10**</span><span class="sxs-lookup"><span data-stu-id="14808-130">**10**</span></span>
</dt> <dd>

<span data-ttu-id="14808-131">O objeto especificado já existe.</span><span class="sxs-lookup"><span data-stu-id="14808-131">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="14808-132">**11**</span><span class="sxs-lookup"><span data-stu-id="14808-132">**11**</span></span>
</dt> <dd>

<span data-ttu-id="14808-133">O sistema de arquivos não é um NTFS.</span><span class="sxs-lookup"><span data-stu-id="14808-133">The file system is not an NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="14808-134">**12**</span><span class="sxs-lookup"><span data-stu-id="14808-134">**12**</span></span>
</dt> <dd>

<span data-ttu-id="14808-135">A plataforma não é o Windows.</span><span class="sxs-lookup"><span data-stu-id="14808-135">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="14808-136">**13**</span><span class="sxs-lookup"><span data-stu-id="14808-136">**13**</span></span>
</dt> <dd>

<span data-ttu-id="14808-137">A unidade não é a mesma.</span><span class="sxs-lookup"><span data-stu-id="14808-137">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="14808-138">**14**</span><span class="sxs-lookup"><span data-stu-id="14808-138">**14**</span></span>
</dt> <dd>

<span data-ttu-id="14808-139">O diretório não está vazio.</span><span class="sxs-lookup"><span data-stu-id="14808-139">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="14808-140">**15**</span><span class="sxs-lookup"><span data-stu-id="14808-140">**15**</span></span>
</dt> <dd>

<span data-ttu-id="14808-141">Houve uma violação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="14808-141">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="14808-142">**16**</span><span class="sxs-lookup"><span data-stu-id="14808-142">**16**</span></span>
</dt> <dd>

<span data-ttu-id="14808-143">O arquivo de inicialização especificado não era válido.</span><span class="sxs-lookup"><span data-stu-id="14808-143">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="14808-144">**17**</span><span class="sxs-lookup"><span data-stu-id="14808-144">**17**</span></span>
</dt> <dd>

<span data-ttu-id="14808-145">Um privilégio necessário para a operação não é mantido.</span><span class="sxs-lookup"><span data-stu-id="14808-145">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="14808-146">**Abril**</span><span class="sxs-lookup"><span data-stu-id="14808-146">**21**</span></span>
</dt> <dd>

<span data-ttu-id="14808-147">Um parâmetro especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="14808-147">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="14808-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="14808-148">Requirements</span></span>



| <span data-ttu-id="14808-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="14808-149">Requirement</span></span> | <span data-ttu-id="14808-150">Valor</span><span class="sxs-lookup"><span data-stu-id="14808-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="14808-151">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="14808-151">Minimum supported client</span></span><br/> | <span data-ttu-id="14808-152">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="14808-152">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="14808-153">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="14808-153">Minimum supported server</span></span><br/> | <span data-ttu-id="14808-154">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="14808-154">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="14808-155">Namespace</span><span class="sxs-lookup"><span data-stu-id="14808-155">Namespace</span></span><br/>                | <span data-ttu-id="14808-156">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="14808-156">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="14808-157">MOF</span><span class="sxs-lookup"><span data-stu-id="14808-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="14808-158"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="14808-158"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="14808-159">DLL</span><span class="sxs-lookup"><span data-stu-id="14808-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="14808-160"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="14808-160"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14808-161">Confira também</span><span class="sxs-lookup"><span data-stu-id="14808-161">See also</span></span>

<dl> <dt>

<span data-ttu-id="14808-162">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="14808-162">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="14808-163">**\_Diretório Win32**</span><span class="sxs-lookup"><span data-stu-id="14808-163">**Win32\_Directory**</span></span>](win32-directory.md)
</dt> </dl>

 

