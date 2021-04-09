---
description: Descompacta o arquivo de atalho lógico (ou diretório) especificado no caminho do objeto. Esse método é uma versão estendida do método uncompact.
ms.assetid: aa1c04d1-4cce-4096-bce3-b9c61b9a4eb7
ms.tgt_platform: multiple
title: Método UncompressEx da classe Win32_ShortcutFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ShortcutFile.UncompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e07e86be3666b06063ef81c896eab6ee7a918657
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089546"
---
# <a name="uncompressex-method-of-the-win32_shortcutfile-class"></a><span data-ttu-id="0f6ff-104">Método UncompressEx da \_ classe shortcutfile do Win32</span><span class="sxs-lookup"><span data-stu-id="0f6ff-104">UncompressEx method of the Win32\_ShortcutFile class</span></span>

<span data-ttu-id="0f6ff-105">O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **UncompressEx** descompacta o arquivo de atalho lógico (ou diretório) especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="0f6ff-105">The **UncompressEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method uncompresses the logical shortcut file (or directory) specified in the object path.</span></span> <span data-ttu-id="0f6ff-106">Esse método é uma versão estendida do método [**uncompact**](uncompress-method-in-class-win32-directory.md) .</span><span class="sxs-lookup"><span data-stu-id="0f6ff-106">This method is an extended version of the [**Uncompress**](uncompress-method-in-class-win32-directory.md) method.</span></span>

<span data-ttu-id="0f6ff-107">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="0f6ff-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="0f6ff-108">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="0f6ff-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="0f6ff-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0f6ff-109">Syntax</span></span>


```mof
uint32 UncompressEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="0f6ff-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0f6ff-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f6ff-111">*StopFileName* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="0f6ff-111">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0f6ff-112">Nome do arquivo ou diretório em que o método **UncompressEx** falhou.</span><span class="sxs-lookup"><span data-stu-id="0f6ff-112">Name of the file or directory where the **UncompressEx** method failed.</span></span> <span data-ttu-id="0f6ff-113">Esse parâmetro será **NULL** se o método tiver sucesso.</span><span class="sxs-lookup"><span data-stu-id="0f6ff-113">This parameter will be **NULL** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="0f6ff-114">*StartFileName* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="0f6ff-114">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0f6ff-115">Nomeia o arquivo ou diretório filho a ser usado como ponto de partida para **UncompressEx**.</span><span class="sxs-lookup"><span data-stu-id="0f6ff-115">Names the child file or directory to use as a starting point for **UncompressEx**.</span></span> <span data-ttu-id="0f6ff-116">O parâmetro *StartFileName* normalmente é o parâmetro *StopFileName* que especifica o arquivo ou diretório no qual ocorreu um erro da chamada do método anterior.</span><span class="sxs-lookup"><span data-stu-id="0f6ff-116">The *StartFileName* parameter is typically the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="0f6ff-117">Se esse parâmetro for **nulo**, a operação será executada no arquivo ou diretório especificado na chamada de ExecMethod.</span><span class="sxs-lookup"><span data-stu-id="0f6ff-117">If this parameter is **NULL**, the operation is performed on the file or directory specified in the ExecMethod call.</span></span>

</dd> <dt>

<span data-ttu-id="0f6ff-118">*Recursivo* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="0f6ff-118">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0f6ff-119">Se **for true**, a alteração de propriedade será aplicada recursivamente aos arquivos e diretórios dentro do diretório especificado pela instância [**de \_ LogicalFile do CIM**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="0f6ff-119">If **true**, the change of ownership will be applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span>

> [!Note]  
> <span data-ttu-id="0f6ff-120">Para instâncias de arquivo, o parâmetro *recursivo* é ignorado.</span><span class="sxs-lookup"><span data-stu-id="0f6ff-120">For file instances, the *Recursive* parameter is ignored.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f6ff-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0f6ff-121">Return value</span></span>

<span data-ttu-id="0f6ff-122">Retorna um valor de 0 (zero) se o arquivo tiver sido descompactado com êxito e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="0f6ff-122">Returns a value of 0 (zero) if the file was successfully decompressed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="0f6ff-123">**0**</span><span class="sxs-lookup"><span data-stu-id="0f6ff-123">**0**</span></span>
</dt> <dd>

<span data-ttu-id="0f6ff-124">A solicitação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="0f6ff-124">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="0f6ff-125">**2**</span><span class="sxs-lookup"><span data-stu-id="0f6ff-125">**2**</span></span>
</dt> <dd>

<span data-ttu-id="0f6ff-126">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="0f6ff-126">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="0f6ff-127">**8**</span><span class="sxs-lookup"><span data-stu-id="0f6ff-127">**8**</span></span>
</dt> <dd>

<span data-ttu-id="0f6ff-128">Ocorreu uma falha não especificada.</span><span class="sxs-lookup"><span data-stu-id="0f6ff-128">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="0f6ff-129">**9**</span><span class="sxs-lookup"><span data-stu-id="0f6ff-129">**9**</span></span>
</dt> <dd>

<span data-ttu-id="0f6ff-130">O nome especificado não era válido.</span><span class="sxs-lookup"><span data-stu-id="0f6ff-130">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="0f6ff-131">**10**</span><span class="sxs-lookup"><span data-stu-id="0f6ff-131">**10**</span></span>
</dt> <dd>

<span data-ttu-id="0f6ff-132">O objeto especificado já existe.</span><span class="sxs-lookup"><span data-stu-id="0f6ff-132">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="0f6ff-133">**11**</span><span class="sxs-lookup"><span data-stu-id="0f6ff-133">**11**</span></span>
</dt> <dd>

<span data-ttu-id="0f6ff-134">O sistema de arquivos não é NTFS.</span><span class="sxs-lookup"><span data-stu-id="0f6ff-134">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="0f6ff-135">**12**</span><span class="sxs-lookup"><span data-stu-id="0f6ff-135">**12**</span></span>
</dt> <dd>

<span data-ttu-id="0f6ff-136">A plataforma não é o Windows.</span><span class="sxs-lookup"><span data-stu-id="0f6ff-136">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="0f6ff-137">**13**</span><span class="sxs-lookup"><span data-stu-id="0f6ff-137">**13**</span></span>
</dt> <dd>

<span data-ttu-id="0f6ff-138">A unidade não é a mesma.</span><span class="sxs-lookup"><span data-stu-id="0f6ff-138">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="0f6ff-139">**14**</span><span class="sxs-lookup"><span data-stu-id="0f6ff-139">**14**</span></span>
</dt> <dd>

<span data-ttu-id="0f6ff-140">O diretório não está vazio.</span><span class="sxs-lookup"><span data-stu-id="0f6ff-140">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="0f6ff-141">**15**</span><span class="sxs-lookup"><span data-stu-id="0f6ff-141">**15**</span></span>
</dt> <dd>

<span data-ttu-id="0f6ff-142">Houve uma violação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="0f6ff-142">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="0f6ff-143">**16**</span><span class="sxs-lookup"><span data-stu-id="0f6ff-143">**16**</span></span>
</dt> <dd>

<span data-ttu-id="0f6ff-144">O arquivo de inicialização especificado não era válido.</span><span class="sxs-lookup"><span data-stu-id="0f6ff-144">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="0f6ff-145">**17**</span><span class="sxs-lookup"><span data-stu-id="0f6ff-145">**17**</span></span>
</dt> <dd>

<span data-ttu-id="0f6ff-146">Um privilégio necessário para a operação não é mantido.</span><span class="sxs-lookup"><span data-stu-id="0f6ff-146">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="0f6ff-147">**Abril**</span><span class="sxs-lookup"><span data-stu-id="0f6ff-147">**21**</span></span>
</dt> <dd>

<span data-ttu-id="0f6ff-148">Um parâmetro especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="0f6ff-148">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0f6ff-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0f6ff-149">Requirements</span></span>



| <span data-ttu-id="0f6ff-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f6ff-150">Requirement</span></span> | <span data-ttu-id="0f6ff-151">Valor</span><span class="sxs-lookup"><span data-stu-id="0f6ff-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0f6ff-152">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0f6ff-152">Minimum supported client</span></span><br/> | <span data-ttu-id="0f6ff-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0f6ff-153">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0f6ff-154">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0f6ff-154">Minimum supported server</span></span><br/> | <span data-ttu-id="0f6ff-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0f6ff-155">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0f6ff-156">Namespace</span><span class="sxs-lookup"><span data-stu-id="0f6ff-156">Namespace</span></span><br/>                | <span data-ttu-id="0f6ff-157">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="0f6ff-157">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0f6ff-158">MOF</span><span class="sxs-lookup"><span data-stu-id="0f6ff-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0f6ff-159"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0f6ff-159"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0f6ff-160">DLL</span><span class="sxs-lookup"><span data-stu-id="0f6ff-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f6ff-161"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f6ff-161"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f6ff-162">Confira também</span><span class="sxs-lookup"><span data-stu-id="0f6ff-162">See also</span></span>

<dl> <dt>

<span data-ttu-id="0f6ff-163">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0f6ff-163">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="0f6ff-164">**Atalho do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="0f6ff-164">**Win32\_ShortcutFile**</span></span>](win32-shortcutfile.md)
</dt> </dl>

 

