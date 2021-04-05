---
description: O método CompressEx compacta o arquivo lógico (ou diretório) especificado no caminho do objeto. Esse método é uma versão estendida do método compress.
ms.assetid: 7d119865-c246-4cb5-9de4-48a4c42efd90
ms.tgt_platform: multiple
title: Método CompressEx da classe CIM_LogicalFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.CompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7570cbe3ebc00708023a18da42ef35ff3306d3b0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826188"
---
# <a name="compressex-method-of-the-cim_logicalfile-class"></a><span data-ttu-id="f95d8-104">Método CompressEx da classe de \_ LogicalFile CIM</span><span class="sxs-lookup"><span data-stu-id="f95d8-104">CompressEx method of the CIM\_LogicalFile class</span></span>

<span data-ttu-id="f95d8-105">O método **CompressEx** compacta o arquivo lógico (ou diretório) especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="f95d8-105">The **CompressEx** method compresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="f95d8-106">Esse método é uma versão estendida do método [**compress**](compress-method-in-class-cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="f95d8-106">This method is an extended version of the [**Compress**](compress-method-in-class-cim-logicalfile.md) method.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f95d8-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="f95d8-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="f95d8-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="f95d8-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="f95d8-109">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="f95d8-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="f95d8-110">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="f95d8-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="f95d8-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f95d8-111">Syntax</span></span>


```mof
uint32 CompressEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="f95d8-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f95d8-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f95d8-113">*StopFileName* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="f95d8-113">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f95d8-114">Nome do arquivo (ou diretório) em que o método falhou.</span><span class="sxs-lookup"><span data-stu-id="f95d8-114">Name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="f95d8-115">Esse parâmetro será nulo se o método tiver sucesso.</span><span class="sxs-lookup"><span data-stu-id="f95d8-115">This parameter is null if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="f95d8-116">*StartFileName* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="f95d8-116">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f95d8-117">Arquivo filho (ou diretório) a ser usado como ponto de partida para o método.</span><span class="sxs-lookup"><span data-stu-id="f95d8-117">Child file (or directory) to use as a starting point for the method.</span></span> <span data-ttu-id="f95d8-118">Normalmente, esse parâmetro é o parâmetro *StopFileName* que especifica o arquivo ou diretório no qual ocorreu um erro da chamada do método anterior.</span><span class="sxs-lookup"><span data-stu-id="f95d8-118">Typically, this parameter is the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="f95d8-119">Se esse parâmetro for nulo, a operação será executada no arquivo (ou diretório) especificado na chamada de [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="f95d8-119">If this parameter is null, the operation is performed on the file (or directory) specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="f95d8-120">*Recursivo* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="f95d8-120">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f95d8-121">Se **for true**, o método também será aplicado recursivamente a arquivos e diretórios dentro do diretório especificado pela instância de [**\_ LogicalFile do CIM**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="f95d8-121">If **TRUE**, the method is also applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span> <span data-ttu-id="f95d8-122">Para instâncias de arquivo, esse parâmetro é ignorado.</span><span class="sxs-lookup"><span data-stu-id="f95d8-122">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f95d8-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f95d8-123">Return value</span></span>

<span data-ttu-id="f95d8-124">Retorna um valor de 0 (zero) em caso de êxito e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="f95d8-124">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="f95d8-125">**Êxito**</span><span class="sxs-lookup"><span data-stu-id="f95d8-125">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="f95d8-126">0</span><span class="sxs-lookup"><span data-stu-id="f95d8-126">0</span></span>

<span data-ttu-id="f95d8-127">Sucesso.</span><span class="sxs-lookup"><span data-stu-id="f95d8-127">Success.</span></span>

</dd> <dt>

<span data-ttu-id="f95d8-128">**Acesso negado**</span><span class="sxs-lookup"><span data-stu-id="f95d8-128">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="f95d8-129">2</span><span class="sxs-lookup"><span data-stu-id="f95d8-129">2</span></span>

<span data-ttu-id="f95d8-130">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="f95d8-130">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="f95d8-131">**Falha não especificada**</span><span class="sxs-lookup"><span data-stu-id="f95d8-131">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="f95d8-132">8</span><span class="sxs-lookup"><span data-stu-id="f95d8-132">8</span></span>

<span data-ttu-id="f95d8-133">Falha não especificada.</span><span class="sxs-lookup"><span data-stu-id="f95d8-133">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="f95d8-134">**Objeto inválido**</span><span class="sxs-lookup"><span data-stu-id="f95d8-134">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="f95d8-135">9</span><span class="sxs-lookup"><span data-stu-id="f95d8-135">9</span></span>

<span data-ttu-id="f95d8-136">Objeto inválido.</span><span class="sxs-lookup"><span data-stu-id="f95d8-136">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="f95d8-137">**O objeto já existe**</span><span class="sxs-lookup"><span data-stu-id="f95d8-137">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="f95d8-138">10</span><span class="sxs-lookup"><span data-stu-id="f95d8-138">10</span></span>

<span data-ttu-id="f95d8-139">O objeto já existe.</span><span class="sxs-lookup"><span data-stu-id="f95d8-139">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="f95d8-140">**Sistema de arquivos não NTFS**</span><span class="sxs-lookup"><span data-stu-id="f95d8-140">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="f95d8-141">11</span><span class="sxs-lookup"><span data-stu-id="f95d8-141">11</span></span>

<span data-ttu-id="f95d8-142">Sistema de arquivos não NTFS.</span><span class="sxs-lookup"><span data-stu-id="f95d8-142">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="f95d8-143">**Plataforma não NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="f95d8-143">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="f95d8-144">12</span><span class="sxs-lookup"><span data-stu-id="f95d8-144">12</span></span>

<span data-ttu-id="f95d8-145">Plataforma não Windows.</span><span class="sxs-lookup"><span data-stu-id="f95d8-145">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="f95d8-146">**A unidade não é a mesma**</span><span class="sxs-lookup"><span data-stu-id="f95d8-146">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="f95d8-147">13</span><span class="sxs-lookup"><span data-stu-id="f95d8-147">13</span></span>

<span data-ttu-id="f95d8-148">A unidade não é a mesma.</span><span class="sxs-lookup"><span data-stu-id="f95d8-148">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="f95d8-149">**Diretório não vazio**</span><span class="sxs-lookup"><span data-stu-id="f95d8-149">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="f95d8-150">14</span><span class="sxs-lookup"><span data-stu-id="f95d8-150">14</span></span>

<span data-ttu-id="f95d8-151">O diretório não está vazio.</span><span class="sxs-lookup"><span data-stu-id="f95d8-151">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="f95d8-152">**Violação de compartilhamento**</span><span class="sxs-lookup"><span data-stu-id="f95d8-152">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="f95d8-153">15</span><span class="sxs-lookup"><span data-stu-id="f95d8-153">15</span></span>

<span data-ttu-id="f95d8-154">Violação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="f95d8-154">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="f95d8-155">**Arquivo de início inválido**</span><span class="sxs-lookup"><span data-stu-id="f95d8-155">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="f95d8-156">16</span><span class="sxs-lookup"><span data-stu-id="f95d8-156">16</span></span>

<span data-ttu-id="f95d8-157">Arquivo inicial inválido.</span><span class="sxs-lookup"><span data-stu-id="f95d8-157">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="f95d8-158">**Privilégio não mantido**</span><span class="sxs-lookup"><span data-stu-id="f95d8-158">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="f95d8-159">17</span><span class="sxs-lookup"><span data-stu-id="f95d8-159">17</span></span>

<span data-ttu-id="f95d8-160">Privilégio não mantido.</span><span class="sxs-lookup"><span data-stu-id="f95d8-160">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="f95d8-161">**Parâmetro inválido**</span><span class="sxs-lookup"><span data-stu-id="f95d8-161">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="f95d8-162">21</span><span class="sxs-lookup"><span data-stu-id="f95d8-162">21</span></span>

<span data-ttu-id="f95d8-163">Parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="f95d8-163">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f95d8-164">Comentários</span><span class="sxs-lookup"><span data-stu-id="f95d8-164">Remarks</span></span>

<span data-ttu-id="f95d8-165">Este método não está implementado no momento pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="f95d8-165">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="f95d8-166">Para usar esse método, você deve implementá-lo em seu próprio provedor.</span><span class="sxs-lookup"><span data-stu-id="f95d8-166">To use this method, you must implement it in your own provider.</span></span>

## <a name="requirements"></a><span data-ttu-id="f95d8-167">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f95d8-167">Requirements</span></span>



| <span data-ttu-id="f95d8-168">Requisito</span><span class="sxs-lookup"><span data-stu-id="f95d8-168">Requirement</span></span> | <span data-ttu-id="f95d8-169">Valor</span><span class="sxs-lookup"><span data-stu-id="f95d8-169">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f95d8-170">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f95d8-170">Minimum supported client</span></span><br/> | <span data-ttu-id="f95d8-171">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f95d8-171">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f95d8-172">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f95d8-172">Minimum supported server</span></span><br/> | <span data-ttu-id="f95d8-173">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f95d8-173">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f95d8-174">Namespace</span><span class="sxs-lookup"><span data-stu-id="f95d8-174">Namespace</span></span><br/>                | <span data-ttu-id="f95d8-175">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="f95d8-175">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f95d8-176">MOF</span><span class="sxs-lookup"><span data-stu-id="f95d8-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f95d8-177"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f95d8-177"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f95d8-178">DLL</span><span class="sxs-lookup"><span data-stu-id="f95d8-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f95d8-179"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f95d8-179"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f95d8-180">Confira também</span><span class="sxs-lookup"><span data-stu-id="f95d8-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f95d8-181">CIM \_ LogicalFile</span><span class="sxs-lookup"><span data-stu-id="f95d8-181">CIM\_LogicalFile</span></span>](compressex-method-in-class-cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="f95d8-182">**CIM \_ LogicalFile**</span><span class="sxs-lookup"><span data-stu-id="f95d8-182">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

