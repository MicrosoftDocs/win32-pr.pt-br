---
description: Descompacta o arquivo de codec lógico (ou diretório) especificado no caminho do objeto. Esse método é uma versão estendida do método uncompact.
ms.assetid: 257c69fa-c4f7-48be-8317-55db4b01601b
ms.tgt_platform: multiple
title: Método UncompressEx da classe Win32_CodecFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile.UncompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 547062a85336681b78a6081646801e78e4713e3c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501067"
---
# <a name="uncompressex-method-of-the-win32_codecfile-class"></a><span data-ttu-id="24809-104">Método UncompressEx da classe de um codec do Win32 \_</span><span class="sxs-lookup"><span data-stu-id="24809-104">UncompressEx method of the Win32\_CodecFile class</span></span>

<span data-ttu-id="24809-105">O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **UncompressEx** descompacta o arquivo de codec lógico (ou diretório) especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="24809-105">The **UncompressEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method uncompresses the logical codec file (or directory) specified in the object path.</span></span> <span data-ttu-id="24809-106">Esse método é uma versão estendida do método [**uncompact**](uncompress-method-in-class-win32-directory.md) .</span><span class="sxs-lookup"><span data-stu-id="24809-106">This method is an extended version of the [**Uncompress**](uncompress-method-in-class-win32-directory.md) method.</span></span>

<span data-ttu-id="24809-107">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="24809-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="24809-108">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="24809-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="24809-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="24809-109">Syntax</span></span>


```mof
uint32 UncompressEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="24809-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="24809-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24809-111">*StopFileName* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="24809-111">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="24809-112">Nome do arquivo ou diretório em que o método **UncompressEx** falhou.</span><span class="sxs-lookup"><span data-stu-id="24809-112">Name of the file or directory where the **UncompressEx** method failed.</span></span> <span data-ttu-id="24809-113">Esse parâmetro será **NULL** se o método tiver sucesso.</span><span class="sxs-lookup"><span data-stu-id="24809-113">This parameter will be **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="24809-114">*StartFileName* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="24809-114">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="24809-115">Nomeia o arquivo ou diretório filho a ser usado como ponto de partida para **UncompressEx**. O parâmetro *StartFileName* normalmente é o parâmetro *StopFileName* que especifica o arquivo ou diretório no qual ocorreu um erro da chamada do método anterior.</span><span class="sxs-lookup"><span data-stu-id="24809-115">Names the child file or directory to use as a starting point for **UncompressEx**.The *StartFileName* parameter is typically the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="24809-116">Se esse parâmetro for **nulo**, a operação será executada no arquivo ou diretório especificado na chamada de **ExecMethod** .</span><span class="sxs-lookup"><span data-stu-id="24809-116">If this parameter is **NULL**, the operation is performed on the file or directory specified in the **ExecMethod** call.</span></span>

</dd> <dt>

<span data-ttu-id="24809-117">*Recursivo* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="24809-117">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="24809-118">Se **for true**, a alteração de propriedade será aplicada recursivamente aos arquivos e diretórios dentro do diretório especificado pela instância [**de \_ LogicalFile do CIM**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="24809-118">If **true**, the change of ownership will be applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span> <span data-ttu-id="24809-119">Observação: para instâncias de arquivo, o parâmetro de entrada *recursivo* é ignorado.</span><span class="sxs-lookup"><span data-stu-id="24809-119">Note: for file instances, the *Recursive* input parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24809-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="24809-120">Return value</span></span>

<span data-ttu-id="24809-121">Retorna um valor inteiro de 0 (zero) se o arquivo tiver sido descompactado com êxito e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="24809-121">Returns an integer value of 0 (zero) if the file was successfully decompressed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="24809-122">**0**</span><span class="sxs-lookup"><span data-stu-id="24809-122">**0**</span></span>
</dt> <dd>

<span data-ttu-id="24809-123">A solicitação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="24809-123">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="24809-124">**2**</span><span class="sxs-lookup"><span data-stu-id="24809-124">**2**</span></span>
</dt> <dd>

<span data-ttu-id="24809-125">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="24809-125">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="24809-126">**8**</span><span class="sxs-lookup"><span data-stu-id="24809-126">**8**</span></span>
</dt> <dd>

<span data-ttu-id="24809-127">Ocorreu uma falha não especificada.</span><span class="sxs-lookup"><span data-stu-id="24809-127">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="24809-128">**9**</span><span class="sxs-lookup"><span data-stu-id="24809-128">**9**</span></span>
</dt> <dd>

<span data-ttu-id="24809-129">O nome especificado não era válido.</span><span class="sxs-lookup"><span data-stu-id="24809-129">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="24809-130">**10**</span><span class="sxs-lookup"><span data-stu-id="24809-130">**10**</span></span>
</dt> <dd>

<span data-ttu-id="24809-131">O objeto especificado já existe.</span><span class="sxs-lookup"><span data-stu-id="24809-131">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="24809-132">**11**</span><span class="sxs-lookup"><span data-stu-id="24809-132">**11**</span></span>
</dt> <dd>

<span data-ttu-id="24809-133">O sistema de arquivos não é NTFS.</span><span class="sxs-lookup"><span data-stu-id="24809-133">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="24809-134">**12**</span><span class="sxs-lookup"><span data-stu-id="24809-134">**12**</span></span>
</dt> <dd>

<span data-ttu-id="24809-135">A plataforma não é o Windows.</span><span class="sxs-lookup"><span data-stu-id="24809-135">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="24809-136">**13**</span><span class="sxs-lookup"><span data-stu-id="24809-136">**13**</span></span>
</dt> <dd>

<span data-ttu-id="24809-137">A unidade não é a mesma.</span><span class="sxs-lookup"><span data-stu-id="24809-137">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="24809-138">**14**</span><span class="sxs-lookup"><span data-stu-id="24809-138">**14**</span></span>
</dt> <dd>

<span data-ttu-id="24809-139">O diretório não está vazio.</span><span class="sxs-lookup"><span data-stu-id="24809-139">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="24809-140">**15**</span><span class="sxs-lookup"><span data-stu-id="24809-140">**15**</span></span>
</dt> <dd>

<span data-ttu-id="24809-141">Houve uma violação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="24809-141">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="24809-142">**16**</span><span class="sxs-lookup"><span data-stu-id="24809-142">**16**</span></span>
</dt> <dd>

<span data-ttu-id="24809-143">O arquivo de inicialização especificado não era válido.</span><span class="sxs-lookup"><span data-stu-id="24809-143">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="24809-144">**17**</span><span class="sxs-lookup"><span data-stu-id="24809-144">**17**</span></span>
</dt> <dd>

<span data-ttu-id="24809-145">Um privilégio necessário para a operação não é mantido.</span><span class="sxs-lookup"><span data-stu-id="24809-145">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="24809-146">**Abril**</span><span class="sxs-lookup"><span data-stu-id="24809-146">**21**</span></span>
</dt> <dd>

<span data-ttu-id="24809-147">Um parâmetro especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="24809-147">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="24809-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="24809-148">Requirements</span></span>



| <span data-ttu-id="24809-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="24809-149">Requirement</span></span> | <span data-ttu-id="24809-150">Valor</span><span class="sxs-lookup"><span data-stu-id="24809-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="24809-151">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="24809-151">Minimum supported client</span></span><br/> | <span data-ttu-id="24809-152">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="24809-152">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="24809-153">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="24809-153">Minimum supported server</span></span><br/> | <span data-ttu-id="24809-154">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="24809-154">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="24809-155">Namespace</span><span class="sxs-lookup"><span data-stu-id="24809-155">Namespace</span></span><br/>                | <span data-ttu-id="24809-156">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="24809-156">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="24809-157">MOF</span><span class="sxs-lookup"><span data-stu-id="24809-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="24809-158"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="24809-158"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="24809-159">DLL</span><span class="sxs-lookup"><span data-stu-id="24809-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="24809-160"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="24809-160"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24809-161">Confira também</span><span class="sxs-lookup"><span data-stu-id="24809-161">See also</span></span>

<dl> <dt>

<span data-ttu-id="24809-162">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="24809-162">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="24809-163">**Codec do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="24809-163">**Win32\_CodecFile**</span></span>](win32-codecfile.md)
</dt> </dl>

 

