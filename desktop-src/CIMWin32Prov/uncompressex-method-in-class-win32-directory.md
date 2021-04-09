---
description: Descompacta o arquivo de entrada de diretório lógico (ou diretório) especificado no caminho do objeto. Esse método é uma versão estendida do método uncompact.
ms.assetid: cd18d8b7-ab63-475c-a3a6-79611c9e032d
ms.tgt_platform: multiple
title: Método UncompressEx da classe Win32_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.UncompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a0fd02d0757745199249d64fa08d73f8b5ec65a0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089547"
---
# <a name="uncompressex-method-of-the-win32_directory-class"></a><span data-ttu-id="86378-104">Método UncompressEx da classe do \_ diretório Win32</span><span class="sxs-lookup"><span data-stu-id="86378-104">UncompressEx method of the Win32\_Directory class</span></span>

<span data-ttu-id="86378-105">O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **UncompressEx** descompacta o arquivo de entrada de diretório lógico (ou diretório) especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="86378-105">The **UncompressEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method uncompresses the logical directory entry file (or directory) specified in the object path.</span></span> <span data-ttu-id="86378-106">Esse método é uma versão estendida do método [**uncompact**](uncompress-method-in-class-win32-directory.md) .</span><span class="sxs-lookup"><span data-stu-id="86378-106">This method is an extended version of the [**Uncompress**](uncompress-method-in-class-win32-directory.md) method.</span></span>

<span data-ttu-id="86378-107">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="86378-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="86378-108">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="86378-108">For more information about using this method see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="86378-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="86378-109">Syntax</span></span>


```mof
uint32 UncompressEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="86378-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="86378-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86378-111">*StopFileName* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="86378-111">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="86378-112">Nome do arquivo/diretório em que o método **UncompressEx** falhou.</span><span class="sxs-lookup"><span data-stu-id="86378-112">Name of the file/directory where the **UncompressEx** method failed.</span></span> <span data-ttu-id="86378-113">Esse parâmetro será **NULL** se o método tiver sucesso.</span><span class="sxs-lookup"><span data-stu-id="86378-113">This parameter will be **NULL** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="86378-114">*StartFileName* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="86378-114">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="86378-115">Nomeia o arquivo/diretório filho a ser usado como ponto de partida para **UncompressEx**.</span><span class="sxs-lookup"><span data-stu-id="86378-115">Names the child file/directory to use as a starting point for **UncompressEx**.</span></span> <span data-ttu-id="86378-116">O parâmetro *StartFileName* normalmente é o parâmetro *StopFileName* que especifica o arquivo ou diretório no qual ocorreu um erro da chamada do método anterior.</span><span class="sxs-lookup"><span data-stu-id="86378-116">The *StartFileName* parameter is typically the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="86378-117">Se esse parâmetro for **nulo**, a operação será executada no arquivo ou diretório especificado na chamada de ExecMethod.</span><span class="sxs-lookup"><span data-stu-id="86378-117">If this parameter is **NULL**, the operation is performed on the file or directory specified in the ExecMethod call.</span></span>

<span data-ttu-id="86378-118">Se o *StartFileName* for usado, *recursivo* deverá ser definido como true também.</span><span class="sxs-lookup"><span data-stu-id="86378-118">If *StartFileName* is used, *Recursive* must be set to true as well.</span></span>

</dd> <dt>

<span data-ttu-id="86378-119">*Recursivo* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="86378-119">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="86378-120">Se **for true**, a alteração de propriedade será aplicada recursivamente aos arquivos e diretórios dentro do diretório especificado pela instância [**de \_ LogicalFile do CIM**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="86378-120">If **true**, the change of ownership will be applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span> <span data-ttu-id="86378-121">Observação: para instâncias de arquivo, o parâmetro de entrada *recursivo* é ignorado.</span><span class="sxs-lookup"><span data-stu-id="86378-121">Note: for file instances, the *Recursive* input parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86378-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="86378-122">Return value</span></span>

<span data-ttu-id="86378-123">Retorna um valor de 0 (zero) se o arquivo tiver sido descompactado com êxito e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="86378-123">Returns an value of 0 (zero) if the file was successfully decompressed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="86378-124">**0**</span><span class="sxs-lookup"><span data-stu-id="86378-124">**0**</span></span>
</dt> <dd>

<span data-ttu-id="86378-125">A solicitação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="86378-125">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="86378-126">**2**</span><span class="sxs-lookup"><span data-stu-id="86378-126">**2**</span></span>
</dt> <dd>

<span data-ttu-id="86378-127">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="86378-127">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="86378-128">**8**</span><span class="sxs-lookup"><span data-stu-id="86378-128">**8**</span></span>
</dt> <dd>

<span data-ttu-id="86378-129">Ocorreu uma falha não especificada.</span><span class="sxs-lookup"><span data-stu-id="86378-129">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="86378-130">**9**</span><span class="sxs-lookup"><span data-stu-id="86378-130">**9**</span></span>
</dt> <dd>

<span data-ttu-id="86378-131">O nome especificado não era válido.</span><span class="sxs-lookup"><span data-stu-id="86378-131">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="86378-132">**10**</span><span class="sxs-lookup"><span data-stu-id="86378-132">**10**</span></span>
</dt> <dd>

<span data-ttu-id="86378-133">O objeto especificado já existe.</span><span class="sxs-lookup"><span data-stu-id="86378-133">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="86378-134">**11**</span><span class="sxs-lookup"><span data-stu-id="86378-134">**11**</span></span>
</dt> <dd>

<span data-ttu-id="86378-135">O sistema de arquivos não é NTFS.</span><span class="sxs-lookup"><span data-stu-id="86378-135">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="86378-136">**12**</span><span class="sxs-lookup"><span data-stu-id="86378-136">**12**</span></span>
</dt> <dd>

<span data-ttu-id="86378-137">A plataforma não é o Windows.</span><span class="sxs-lookup"><span data-stu-id="86378-137">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="86378-138">**13**</span><span class="sxs-lookup"><span data-stu-id="86378-138">**13**</span></span>
</dt> <dd>

<span data-ttu-id="86378-139">A unidade não é a mesma.</span><span class="sxs-lookup"><span data-stu-id="86378-139">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="86378-140">**14**</span><span class="sxs-lookup"><span data-stu-id="86378-140">**14**</span></span>
</dt> <dd>

<span data-ttu-id="86378-141">O diretório não está vazio.</span><span class="sxs-lookup"><span data-stu-id="86378-141">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="86378-142">**15**</span><span class="sxs-lookup"><span data-stu-id="86378-142">**15**</span></span>
</dt> <dd>

<span data-ttu-id="86378-143">Houve uma violação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="86378-143">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="86378-144">**16**</span><span class="sxs-lookup"><span data-stu-id="86378-144">**16**</span></span>
</dt> <dd>

<span data-ttu-id="86378-145">O arquivo de inicialização especificado não era válido.</span><span class="sxs-lookup"><span data-stu-id="86378-145">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="86378-146">**17**</span><span class="sxs-lookup"><span data-stu-id="86378-146">**17**</span></span>
</dt> <dd>

<span data-ttu-id="86378-147">Um privilégio necessário para a operação não é mantido.</span><span class="sxs-lookup"><span data-stu-id="86378-147">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="86378-148">**Abril**</span><span class="sxs-lookup"><span data-stu-id="86378-148">**21**</span></span>
</dt> <dd>

<span data-ttu-id="86378-149">Um parâmetro especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="86378-149">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="86378-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="86378-150">Requirements</span></span>



| <span data-ttu-id="86378-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="86378-151">Requirement</span></span> | <span data-ttu-id="86378-152">Valor</span><span class="sxs-lookup"><span data-stu-id="86378-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="86378-153">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="86378-153">Minimum supported client</span></span><br/> | <span data-ttu-id="86378-154">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="86378-154">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="86378-155">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="86378-155">Minimum supported server</span></span><br/> | <span data-ttu-id="86378-156">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="86378-156">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="86378-157">Namespace</span><span class="sxs-lookup"><span data-stu-id="86378-157">Namespace</span></span><br/>                | <span data-ttu-id="86378-158">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="86378-158">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="86378-159">MOF</span><span class="sxs-lookup"><span data-stu-id="86378-159">MOF</span></span><br/>                      | <dl> <span data-ttu-id="86378-160"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="86378-160"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="86378-161">DLL</span><span class="sxs-lookup"><span data-stu-id="86378-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="86378-162"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="86378-162"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86378-163">Confira também</span><span class="sxs-lookup"><span data-stu-id="86378-163">See also</span></span>

<dl> <dt>

<span data-ttu-id="86378-164">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="86378-164">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="86378-165">**\_Diretório Win32**</span><span class="sxs-lookup"><span data-stu-id="86378-165">**Win32\_Directory**</span></span>](win32-directory.md)
</dt> </dl>

 

