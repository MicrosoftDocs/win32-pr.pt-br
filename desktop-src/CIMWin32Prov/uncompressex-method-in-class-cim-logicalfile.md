---
description: Descompacta o arquivo lógico (ou diretório) especificado no caminho do objeto. Esse método é uma versão estendida do método uncompact.
ms.assetid: 383475ba-77d4-4bfb-a241-9c37aa594a1e
ms.tgt_platform: multiple
title: Método UncompressEx da classe CIM_LogicalFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.UncompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1c514939425625c15f3b683e4dc10bd5e05cb511
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646508"
---
# <a name="uncompressex-method-of-the-cim_logicalfile-class"></a><span data-ttu-id="0062a-104">Método UncompressEx da classe de \_ LogicalFile CIM</span><span class="sxs-lookup"><span data-stu-id="0062a-104">UncompressEx method of the CIM\_LogicalFile class</span></span>

<span data-ttu-id="0062a-105">O método **UncompressEx** descompacta o arquivo lógico (ou diretório) especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="0062a-105">The **UncompressEx** method uncompresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="0062a-106">Esse método é uma versão estendida do método [**uncompact**](uncompress-method-in-class-cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="0062a-106">This method is an extended version of the [**Uncompress**](uncompress-method-in-class-cim-logicalfile.md) method.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0062a-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="0062a-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="0062a-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="0062a-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="0062a-109">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="0062a-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="0062a-110">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="0062a-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="0062a-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0062a-111">Syntax</span></span>


```mof
uint32 UncompressEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="0062a-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0062a-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0062a-113">*StopFileName* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="0062a-113">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0062a-114">Nome do arquivo (ou diretório) em que o método falhou.</span><span class="sxs-lookup"><span data-stu-id="0062a-114">Name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="0062a-115">Esse parâmetro será **nulo** se o método tiver sucesso.</span><span class="sxs-lookup"><span data-stu-id="0062a-115">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="0062a-116">*StartFileName* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="0062a-116">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0062a-117">Nome do arquivo filho (ou diretório) a ser usado como ponto de partida para o método.</span><span class="sxs-lookup"><span data-stu-id="0062a-117">Name of the child file (or directory) to use as a starting point for the method.</span></span> <span data-ttu-id="0062a-118">Normalmente, esse parâmetro é o parâmetro *StopFileName* que especifica o arquivo ou diretório no qual ocorreu um erro da chamada do método anterior.</span><span class="sxs-lookup"><span data-stu-id="0062a-118">Typically, this parameter is the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="0062a-119">Se esse parâmetro for **nulo**, a operação será executada no arquivo ou diretório especificado na chamada de [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="0062a-119">If this parameter is **null**, the operation is performed on the file or directory specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="0062a-120">*Recursivo* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="0062a-120">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0062a-121">Se **for true**, o método também será aplicado recursivamente a arquivos e diretórios dentro do diretório especificado pela instância de [**\_ LogicalFile do CIM**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="0062a-121">If **TRUE**, the method is also applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span> <span data-ttu-id="0062a-122">Para instâncias de arquivo, esse parâmetro é ignorado.</span><span class="sxs-lookup"><span data-stu-id="0062a-122">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0062a-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0062a-123">Return value</span></span>

<span data-ttu-id="0062a-124">Retorna um valor de 0 (zero) em caso de êxito e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="0062a-124">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="0062a-125">**Êxito**</span><span class="sxs-lookup"><span data-stu-id="0062a-125">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="0062a-126">0</span><span class="sxs-lookup"><span data-stu-id="0062a-126">0</span></span>

<span data-ttu-id="0062a-127">Sucesso.</span><span class="sxs-lookup"><span data-stu-id="0062a-127">Success.</span></span>

</dd> <dt>

<span data-ttu-id="0062a-128">**Acesso negado**</span><span class="sxs-lookup"><span data-stu-id="0062a-128">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="0062a-129">2</span><span class="sxs-lookup"><span data-stu-id="0062a-129">2</span></span>

<span data-ttu-id="0062a-130">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="0062a-130">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="0062a-131">**Falha não especificada**</span><span class="sxs-lookup"><span data-stu-id="0062a-131">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="0062a-132">8</span><span class="sxs-lookup"><span data-stu-id="0062a-132">8</span></span>

<span data-ttu-id="0062a-133">Falha não especificada.</span><span class="sxs-lookup"><span data-stu-id="0062a-133">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="0062a-134">**Objeto inválido**</span><span class="sxs-lookup"><span data-stu-id="0062a-134">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="0062a-135">9</span><span class="sxs-lookup"><span data-stu-id="0062a-135">9</span></span>

<span data-ttu-id="0062a-136">Objeto inválido.</span><span class="sxs-lookup"><span data-stu-id="0062a-136">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="0062a-137">**O objeto já existe**</span><span class="sxs-lookup"><span data-stu-id="0062a-137">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="0062a-138">10</span><span class="sxs-lookup"><span data-stu-id="0062a-138">10</span></span>

<span data-ttu-id="0062a-139">O objeto já existe.</span><span class="sxs-lookup"><span data-stu-id="0062a-139">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="0062a-140">**Sistema de arquivos não NTFS**</span><span class="sxs-lookup"><span data-stu-id="0062a-140">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="0062a-141">11</span><span class="sxs-lookup"><span data-stu-id="0062a-141">11</span></span>

<span data-ttu-id="0062a-142">Sistema de arquivos não NTFS.</span><span class="sxs-lookup"><span data-stu-id="0062a-142">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="0062a-143">**Plataforma não NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="0062a-143">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="0062a-144">12</span><span class="sxs-lookup"><span data-stu-id="0062a-144">12</span></span>

<span data-ttu-id="0062a-145">Plataforma não Windows.</span><span class="sxs-lookup"><span data-stu-id="0062a-145">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="0062a-146">**A unidade não é a mesma**</span><span class="sxs-lookup"><span data-stu-id="0062a-146">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="0062a-147">13</span><span class="sxs-lookup"><span data-stu-id="0062a-147">13</span></span>

<span data-ttu-id="0062a-148">A unidade não é a mesma.</span><span class="sxs-lookup"><span data-stu-id="0062a-148">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="0062a-149">**Diretório não vazio**</span><span class="sxs-lookup"><span data-stu-id="0062a-149">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="0062a-150">14</span><span class="sxs-lookup"><span data-stu-id="0062a-150">14</span></span>

<span data-ttu-id="0062a-151">O diretório não está vazio.</span><span class="sxs-lookup"><span data-stu-id="0062a-151">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="0062a-152">**Violação de compartilhamento**</span><span class="sxs-lookup"><span data-stu-id="0062a-152">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="0062a-153">15</span><span class="sxs-lookup"><span data-stu-id="0062a-153">15</span></span>

<span data-ttu-id="0062a-154">Violação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="0062a-154">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="0062a-155">**Arquivo de início inválido**</span><span class="sxs-lookup"><span data-stu-id="0062a-155">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="0062a-156">16</span><span class="sxs-lookup"><span data-stu-id="0062a-156">16</span></span>

<span data-ttu-id="0062a-157">Arquivo inicial inválido.</span><span class="sxs-lookup"><span data-stu-id="0062a-157">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="0062a-158">**Privilégio não mantido**</span><span class="sxs-lookup"><span data-stu-id="0062a-158">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="0062a-159">17</span><span class="sxs-lookup"><span data-stu-id="0062a-159">17</span></span>

<span data-ttu-id="0062a-160">Privilégio não mantido.</span><span class="sxs-lookup"><span data-stu-id="0062a-160">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="0062a-161">**Parâmetro inválido**</span><span class="sxs-lookup"><span data-stu-id="0062a-161">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="0062a-162">21</span><span class="sxs-lookup"><span data-stu-id="0062a-162">21</span></span>

<span data-ttu-id="0062a-163">Parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="0062a-163">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0062a-164">Comentários</span><span class="sxs-lookup"><span data-stu-id="0062a-164">Remarks</span></span>

<span data-ttu-id="0062a-165">Este método não está implementado no momento pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="0062a-165">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="0062a-166">Para usar esse método, você deve implementá-lo em seu próprio provedor.</span><span class="sxs-lookup"><span data-stu-id="0062a-166">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="0062a-167">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="0062a-167">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="0062a-168">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="0062a-168">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="0062a-169">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0062a-169">Requirements</span></span>



| <span data-ttu-id="0062a-170">Requisito</span><span class="sxs-lookup"><span data-stu-id="0062a-170">Requirement</span></span> | <span data-ttu-id="0062a-171">Valor</span><span class="sxs-lookup"><span data-stu-id="0062a-171">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0062a-172">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0062a-172">Minimum supported client</span></span><br/> | <span data-ttu-id="0062a-173">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0062a-173">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0062a-174">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0062a-174">Minimum supported server</span></span><br/> | <span data-ttu-id="0062a-175">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0062a-175">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0062a-176">Namespace</span><span class="sxs-lookup"><span data-stu-id="0062a-176">Namespace</span></span><br/>                | <span data-ttu-id="0062a-177">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="0062a-177">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0062a-178">MOF</span><span class="sxs-lookup"><span data-stu-id="0062a-178">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0062a-179"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0062a-179"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0062a-180">DLL</span><span class="sxs-lookup"><span data-stu-id="0062a-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0062a-181"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0062a-181"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0062a-182">Confira também</span><span class="sxs-lookup"><span data-stu-id="0062a-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0062a-183">CIM \_ LogicalFile</span><span class="sxs-lookup"><span data-stu-id="0062a-183">CIM\_LogicalFile</span></span>](uncompressex-method-in-class-cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="0062a-184">**CIM \_ LogicalFile**</span><span class="sxs-lookup"><span data-stu-id="0062a-184">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

