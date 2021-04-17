---
description: Obtém a propriedade do arquivo de atalho lógico especificado no caminho do objeto. Esse método é uma versão estendida do método TakeOwnerShip.
ms.assetid: 1345562c-343e-4e3a-b6ed-3b64a7260c89
ms.tgt_platform: multiple
title: Método TakeOwnerShipEx da classe Win32_ShortcutFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ShortcutFile.TakeOwnerShipEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 69988c7995ee295297c92bbabf0ee83059304a94
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753974"
---
# <a name="takeownershipex-method-of-the-win32_shortcutfile-class"></a><span data-ttu-id="4f12d-104">Método TakeOwnerShipEx da \_ classe shortcutfile do Win32</span><span class="sxs-lookup"><span data-stu-id="4f12d-104">TakeOwnerShipEx method of the Win32\_ShortcutFile class</span></span>

<span data-ttu-id="4f12d-105">O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **TakeOwnerShipEx** Obtém a propriedade do arquivo de atalho lógico especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="4f12d-105">The **TakeOwnerShipEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method obtains ownership of the logical shortcut file specified in the object path.</span></span> <span data-ttu-id="4f12d-106">Esse método é uma versão estendida do método [**TakeOwnership**](takeownership-method-in-class-win32-directory.md) .</span><span class="sxs-lookup"><span data-stu-id="4f12d-106">This method is an extended version of the [**TakeOwnerShip**](takeownership-method-in-class-win32-directory.md) method.</span></span> <span data-ttu-id="4f12d-107">Se o arquivo lógico for, na verdade, um diretório, esse método agirá recursivamente, assumindo a propriedade de todos os arquivos e subdiretórios contidos no diretório.</span><span class="sxs-lookup"><span data-stu-id="4f12d-107">If the logical file is actually a directory, then this method acts recursively, taking ownership of all of the files and subdirectories the directory contains.</span></span>

<span data-ttu-id="4f12d-108">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="4f12d-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="4f12d-109">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="4f12d-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="4f12d-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4f12d-110">Syntax</span></span>


```mof
uint32 TakeOwnerShipEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="4f12d-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4f12d-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f12d-112">*StopFileName* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="4f12d-112">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4f12d-113">Nome do arquivo ou diretório em que o método **TakeOwnerShipEx** falhou.</span><span class="sxs-lookup"><span data-stu-id="4f12d-113">Name of the file or directory where the **TakeOwnerShipEx** method failed.</span></span> <span data-ttu-id="4f12d-114">Esse parâmetro será **NULL** se o método tiver sucesso.</span><span class="sxs-lookup"><span data-stu-id="4f12d-114">This parameter will be **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="4f12d-115">*StartFileName* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="4f12d-115">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4f12d-116">Nomeia o arquivo ou diretório filho a ser usado como ponto de partida para **TakeOwnerShipEx**.</span><span class="sxs-lookup"><span data-stu-id="4f12d-116">Names the child file or directory to use as a starting point for **TakeOwnerShipEx**.</span></span> <span data-ttu-id="4f12d-117">O parâmetro *StartFileName* normalmente é o parâmetro *StopFileName* que especifica o arquivo ou diretório no qual ocorreu um erro da chamada do método anterior.</span><span class="sxs-lookup"><span data-stu-id="4f12d-117">The *StartFileName* parameter is typically the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="4f12d-118">Se esse parâmetro for **nulo**, a operação será executada no arquivo ou diretório especificado na chamada de ExecMethod.</span><span class="sxs-lookup"><span data-stu-id="4f12d-118">If this parameter is **NULL**, the operation is performed on the file or directory specified in the ExecMethod call.</span></span>

</dd> <dt>

<span data-ttu-id="4f12d-119">*Recursivo* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="4f12d-119">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4f12d-120">Se **for true**, a alteração de propriedade será aplicada recursivamente aos arquivos e diretórios dentro do diretório especificado pela instância [**de \_ LogicalFile do CIM**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="4f12d-120">If **true**, the change of ownership will be applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span>

> [!Note]  
> <span data-ttu-id="4f12d-121">Para instâncias de arquivo, o parâmetro *recursivo* é ignorado.</span><span class="sxs-lookup"><span data-stu-id="4f12d-121">For file instances, the *Recursive* parameter is ignored.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f12d-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4f12d-122">Return value</span></span>

<span data-ttu-id="4f12d-123">Retorna um valor de 0 (zero) em caso de êxito e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="4f12d-123">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="4f12d-124">**0**</span><span class="sxs-lookup"><span data-stu-id="4f12d-124">**0**</span></span>
</dt> <dd>

<span data-ttu-id="4f12d-125">A solicitação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="4f12d-125">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="4f12d-126">**2**</span><span class="sxs-lookup"><span data-stu-id="4f12d-126">**2**</span></span>
</dt> <dd>

<span data-ttu-id="4f12d-127">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="4f12d-127">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="4f12d-128">**8**</span><span class="sxs-lookup"><span data-stu-id="4f12d-128">**8**</span></span>
</dt> <dd>

<span data-ttu-id="4f12d-129">Ocorreu uma falha não especificada.</span><span class="sxs-lookup"><span data-stu-id="4f12d-129">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="4f12d-130">**9**</span><span class="sxs-lookup"><span data-stu-id="4f12d-130">**9**</span></span>
</dt> <dd>

<span data-ttu-id="4f12d-131">O nome especificado não era válido.</span><span class="sxs-lookup"><span data-stu-id="4f12d-131">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="4f12d-132">**10**</span><span class="sxs-lookup"><span data-stu-id="4f12d-132">**10**</span></span>
</dt> <dd>

<span data-ttu-id="4f12d-133">O objeto especificado já existe.</span><span class="sxs-lookup"><span data-stu-id="4f12d-133">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="4f12d-134">**11**</span><span class="sxs-lookup"><span data-stu-id="4f12d-134">**11**</span></span>
</dt> <dd>

<span data-ttu-id="4f12d-135">O sistema de arquivos não é NTFS.</span><span class="sxs-lookup"><span data-stu-id="4f12d-135">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="4f12d-136">**12**</span><span class="sxs-lookup"><span data-stu-id="4f12d-136">**12**</span></span>
</dt> <dd>

<span data-ttu-id="4f12d-137">A plataforma não é o Windows.</span><span class="sxs-lookup"><span data-stu-id="4f12d-137">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="4f12d-138">**13**</span><span class="sxs-lookup"><span data-stu-id="4f12d-138">**13**</span></span>
</dt> <dd>

<span data-ttu-id="4f12d-139">A unidade não é a mesma.</span><span class="sxs-lookup"><span data-stu-id="4f12d-139">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="4f12d-140">**14**</span><span class="sxs-lookup"><span data-stu-id="4f12d-140">**14**</span></span>
</dt> <dd>

<span data-ttu-id="4f12d-141">O diretório não está vazio.</span><span class="sxs-lookup"><span data-stu-id="4f12d-141">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="4f12d-142">**15**</span><span class="sxs-lookup"><span data-stu-id="4f12d-142">**15**</span></span>
</dt> <dd>

<span data-ttu-id="4f12d-143">Houve uma violação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="4f12d-143">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="4f12d-144">**16**</span><span class="sxs-lookup"><span data-stu-id="4f12d-144">**16**</span></span>
</dt> <dd>

<span data-ttu-id="4f12d-145">O arquivo de inicialização especificado não era válido.</span><span class="sxs-lookup"><span data-stu-id="4f12d-145">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="4f12d-146">**17**</span><span class="sxs-lookup"><span data-stu-id="4f12d-146">**17**</span></span>
</dt> <dd>

<span data-ttu-id="4f12d-147">Um privilégio necessário para a operação não é mantido.</span><span class="sxs-lookup"><span data-stu-id="4f12d-147">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="4f12d-148">**Abril**</span><span class="sxs-lookup"><span data-stu-id="4f12d-148">**21**</span></span>
</dt> <dd>

<span data-ttu-id="4f12d-149">Um parâmetro especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="4f12d-149">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4f12d-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4f12d-150">Requirements</span></span>



| <span data-ttu-id="4f12d-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f12d-151">Requirement</span></span> | <span data-ttu-id="4f12d-152">Valor</span><span class="sxs-lookup"><span data-stu-id="4f12d-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4f12d-153">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4f12d-153">Minimum supported client</span></span><br/> | <span data-ttu-id="4f12d-154">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4f12d-154">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4f12d-155">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4f12d-155">Minimum supported server</span></span><br/> | <span data-ttu-id="4f12d-156">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4f12d-156">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4f12d-157">Namespace</span><span class="sxs-lookup"><span data-stu-id="4f12d-157">Namespace</span></span><br/>                | <span data-ttu-id="4f12d-158">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="4f12d-158">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4f12d-159">MOF</span><span class="sxs-lookup"><span data-stu-id="4f12d-159">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4f12d-160"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4f12d-160"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4f12d-161">DLL</span><span class="sxs-lookup"><span data-stu-id="4f12d-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f12d-162"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f12d-162"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f12d-163">Confira também</span><span class="sxs-lookup"><span data-stu-id="4f12d-163">See also</span></span>

<dl> <dt>

<span data-ttu-id="4f12d-164">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4f12d-164">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="4f12d-165">**Atalho do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="4f12d-165">**Win32\_ShortcutFile**</span></span>](win32-shortcutfile.md)
</dt> </dl>

 

