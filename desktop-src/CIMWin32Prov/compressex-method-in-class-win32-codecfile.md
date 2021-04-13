---
description: Compacta o arquivo de codec lógico (ou diretório) especificado no caminho do objeto (esse método é uma versão estendida do método compress).
ms.assetid: e1ecf0de-3b81-443e-9936-326d7d2d9210
ms.tgt_platform: multiple
title: Método CompressEx da classe Win32_CodecFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile.CompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4ab2915a4f550c799fed8a58e5573e8264b92f1e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104456926"
---
# <a name="compressex-method-of-the-win32_codecfile-class"></a><span data-ttu-id="1d430-103">Método CompressEx da classe de um codec do Win32 \_</span><span class="sxs-lookup"><span data-stu-id="1d430-103">CompressEx method of the Win32\_CodecFile class</span></span>

<span data-ttu-id="1d430-104">O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **CompressEx** compacta o arquivo de codec lógico (ou diretório) especificado no caminho do objeto (esse método é uma versão estendida do método [**compress**](compress-method-in-class-win32-directory.md) ).</span><span class="sxs-lookup"><span data-stu-id="1d430-104">The **CompressEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method compresses the logical codec file (or directory) specified in the object path (this method is an extended version of the [**Compress**](compress-method-in-class-win32-directory.md) method).</span></span>

<span data-ttu-id="1d430-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="1d430-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="1d430-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="1d430-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="1d430-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1d430-107">Syntax</span></span>


```mof
uint32 CompressEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="1d430-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1d430-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d430-109">*StopFileName* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="1d430-109">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1d430-110">Nome do arquivo ou diretório em que o método **CompressEx** falhou.</span><span class="sxs-lookup"><span data-stu-id="1d430-110">Name of the file or directory where the **CompressEx** method failed.</span></span> <span data-ttu-id="1d430-111">Esse parâmetro será **NULL** se o método tiver sucesso.</span><span class="sxs-lookup"><span data-stu-id="1d430-111">This parameter will be **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="1d430-112">*StartFileName* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="1d430-112">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1d430-113">Nomeia o arquivo ou diretório filho a ser usado como ponto de partida para **CompressEx** . O parâmetro *StartFileName* normalmente é o parâmetro *StopFileName* que especifica o arquivo ou diretório no qual ocorreu um erro da chamada do método anterior.</span><span class="sxs-lookup"><span data-stu-id="1d430-113">Names the child file or directory to use as a starting point for **CompressEx** .The *StartFileName* parameter is typically the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="1d430-114">Se esse parâmetro for **nulo**, a operação será executada no arquivo ou diretório especificado na chamada de **ExecMethod** .</span><span class="sxs-lookup"><span data-stu-id="1d430-114">If this parameter is **NULL**, the operation is performed on the file or directory specified in the **ExecMethod** call.</span></span>

</dd> <dt>

<span data-ttu-id="1d430-115">*Recursivo* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="1d430-115">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1d430-116">Se **for true**, a alteração de propriedade será aplicada recursivamente aos arquivos e diretórios dentro do diretório especificado pela instância [**de \_ LogicalFile do CIM**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="1d430-116">If **true**, the change of ownership will be applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span> <span data-ttu-id="1d430-117">Observação: para instâncias de arquivo, o parâmetro de entrada *recursivo* é ignorado.</span><span class="sxs-lookup"><span data-stu-id="1d430-117">Note: for file instances, the *Recursive* input parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d430-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1d430-118">Return value</span></span>

<span data-ttu-id="1d430-119">Retorna um valor de 0 (zero) se o arquivo tiver sido compactado com êxito e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="1d430-119">Returns an value of 0 (zero) if the file was successfully compressed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="1d430-120">**0**</span><span class="sxs-lookup"><span data-stu-id="1d430-120">**0**</span></span>
</dt> <dd>

<span data-ttu-id="1d430-121">A solicitação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="1d430-121">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="1d430-122">**2**</span><span class="sxs-lookup"><span data-stu-id="1d430-122">**2**</span></span>
</dt> <dd>

<span data-ttu-id="1d430-123">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="1d430-123">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="1d430-124">**8**</span><span class="sxs-lookup"><span data-stu-id="1d430-124">**8**</span></span>
</dt> <dd>

<span data-ttu-id="1d430-125">Ocorreu uma falha não especificada.</span><span class="sxs-lookup"><span data-stu-id="1d430-125">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="1d430-126">**9**</span><span class="sxs-lookup"><span data-stu-id="1d430-126">**9**</span></span>
</dt> <dd>

<span data-ttu-id="1d430-127">O nome especificado não era válido.</span><span class="sxs-lookup"><span data-stu-id="1d430-127">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="1d430-128">**10**</span><span class="sxs-lookup"><span data-stu-id="1d430-128">**10**</span></span>
</dt> <dd>

<span data-ttu-id="1d430-129">O objeto especificado já existe.</span><span class="sxs-lookup"><span data-stu-id="1d430-129">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="1d430-130">**11**</span><span class="sxs-lookup"><span data-stu-id="1d430-130">**11**</span></span>
</dt> <dd>

<span data-ttu-id="1d430-131">O sistema de arquivos não é NTFS.</span><span class="sxs-lookup"><span data-stu-id="1d430-131">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="1d430-132">**12**</span><span class="sxs-lookup"><span data-stu-id="1d430-132">**12**</span></span>
</dt> <dd>

<span data-ttu-id="1d430-133">A plataforma não é o Windows.</span><span class="sxs-lookup"><span data-stu-id="1d430-133">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="1d430-134">**13**</span><span class="sxs-lookup"><span data-stu-id="1d430-134">**13**</span></span>
</dt> <dd>

<span data-ttu-id="1d430-135">A unidade não é a mesma.</span><span class="sxs-lookup"><span data-stu-id="1d430-135">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="1d430-136">**14**</span><span class="sxs-lookup"><span data-stu-id="1d430-136">**14**</span></span>
</dt> <dd>

<span data-ttu-id="1d430-137">O diretório não está vazio.</span><span class="sxs-lookup"><span data-stu-id="1d430-137">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="1d430-138">**15**</span><span class="sxs-lookup"><span data-stu-id="1d430-138">**15**</span></span>
</dt> <dd>

<span data-ttu-id="1d430-139">Houve uma violação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="1d430-139">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="1d430-140">**16**</span><span class="sxs-lookup"><span data-stu-id="1d430-140">**16**</span></span>
</dt> <dd>

<span data-ttu-id="1d430-141">O arquivo de inicialização especificado não era válido.</span><span class="sxs-lookup"><span data-stu-id="1d430-141">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="1d430-142">**17**</span><span class="sxs-lookup"><span data-stu-id="1d430-142">**17**</span></span>
</dt> <dd>

<span data-ttu-id="1d430-143">Um privilégio necessário para a operação não é mantido.</span><span class="sxs-lookup"><span data-stu-id="1d430-143">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="1d430-144">**Abril**</span><span class="sxs-lookup"><span data-stu-id="1d430-144">**21**</span></span>
</dt> <dd>

<span data-ttu-id="1d430-145">Um parâmetro especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="1d430-145">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1d430-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1d430-146">Requirements</span></span>



| <span data-ttu-id="1d430-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d430-147">Requirement</span></span> | <span data-ttu-id="1d430-148">Valor</span><span class="sxs-lookup"><span data-stu-id="1d430-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1d430-149">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1d430-149">Minimum supported client</span></span><br/> | <span data-ttu-id="1d430-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1d430-150">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1d430-151">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1d430-151">Minimum supported server</span></span><br/> | <span data-ttu-id="1d430-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1d430-152">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1d430-153">Namespace</span><span class="sxs-lookup"><span data-stu-id="1d430-153">Namespace</span></span><br/>                | <span data-ttu-id="1d430-154">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="1d430-154">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1d430-155">MOF</span><span class="sxs-lookup"><span data-stu-id="1d430-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1d430-156"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1d430-156"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1d430-157">DLL</span><span class="sxs-lookup"><span data-stu-id="1d430-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1d430-158"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d430-158"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d430-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="1d430-159">See also</span></span>

<dl> <dt>

<span data-ttu-id="1d430-160">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1d430-160">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="1d430-161">**Codec do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="1d430-161">**Win32\_CodecFile**</span></span>](win32-codecfile.md)
</dt> </dl>

 

