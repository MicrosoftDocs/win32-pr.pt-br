---
description: O método DeleteEx exclui o arquivo lógico (ou diretório) especificado no caminho do objeto. Esse método é uma versão estendida do método Delete.
ms.assetid: 53785f2e-8796-446c-8228-9abc2d9a0d68
ms.tgt_platform: multiple
title: Método DeleteEx da classe CIM_LogicalFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.DeleteEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e4f9799513111ff53bb97c14feaf70c922dfb085
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500887"
---
# <a name="deleteex-method-of-the-cim_logicalfile-class"></a><span data-ttu-id="83928-104">Método DeleteEx da classe de \_ LogicalFile CIM</span><span class="sxs-lookup"><span data-stu-id="83928-104">DeleteEx method of the CIM\_LogicalFile class</span></span>

<span data-ttu-id="83928-105">O método **DeleteEx** exclui o arquivo lógico (ou diretório) especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="83928-105">The **DeleteEx** method deletes the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="83928-106">Esse método é uma versão estendida do método [**delete**](delete-method-in-class-cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="83928-106">This method is an extended version of the [**Delete**](delete-method-in-class-cim-logicalfile.md) method.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="83928-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="83928-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="83928-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="83928-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="83928-109">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="83928-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="83928-110">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="83928-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="83928-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="83928-111">Syntax</span></span>


```mof
uint32 DeleteEx(
  [out]          string StopFileName,
  [in, optional] string StartFileName
);
```



## <a name="parameters"></a><span data-ttu-id="83928-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="83928-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83928-113">*StopFileName* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="83928-113">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="83928-114">Cadeia de caracteres que representa o nome do arquivo (ou diretório) em que o método falhou.</span><span class="sxs-lookup"><span data-stu-id="83928-114">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="83928-115">Esse parâmetro será nulo se o método tiver sucesso.</span><span class="sxs-lookup"><span data-stu-id="83928-115">This parameter is null if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="83928-116">*StartFileName* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="83928-116">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="83928-117">Cadeia de caracteres que nomeia o arquivo filho (ou diretório) a ser usado como ponto de partida para o método.</span><span class="sxs-lookup"><span data-stu-id="83928-117">String that names the child file (or directory) to use as a starting point for the method.</span></span> <span data-ttu-id="83928-118">Normalmente, esse parâmetro é o parâmetro *StopFileName* que especifica o arquivo ou diretório no qual ocorreu um erro da chamada do método anterior.</span><span class="sxs-lookup"><span data-stu-id="83928-118">Typically, this parameter is the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="83928-119">Se esse parâmetro for nulo, a operação será executada no arquivo ou diretório especificado na chamada de [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="83928-119">If this parameter is null, the operation is performed on the file or directory specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83928-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="83928-120">Return value</span></span>

<span data-ttu-id="83928-121">Retorna um valor de 0 (zero) em caso de êxito e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="83928-121">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="83928-122">**Êxito**</span><span class="sxs-lookup"><span data-stu-id="83928-122">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="83928-123">0</span><span class="sxs-lookup"><span data-stu-id="83928-123">0</span></span>

<span data-ttu-id="83928-124">Sucesso.</span><span class="sxs-lookup"><span data-stu-id="83928-124">Success.</span></span>

</dd> <dt>

<span data-ttu-id="83928-125">**Acesso negado**</span><span class="sxs-lookup"><span data-stu-id="83928-125">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="83928-126">2</span><span class="sxs-lookup"><span data-stu-id="83928-126">2</span></span>

<span data-ttu-id="83928-127">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="83928-127">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="83928-128">**Falha não especificada**</span><span class="sxs-lookup"><span data-stu-id="83928-128">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="83928-129">8</span><span class="sxs-lookup"><span data-stu-id="83928-129">8</span></span>

<span data-ttu-id="83928-130">Falha não especificada.</span><span class="sxs-lookup"><span data-stu-id="83928-130">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="83928-131">**Objeto inválido**</span><span class="sxs-lookup"><span data-stu-id="83928-131">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="83928-132">9</span><span class="sxs-lookup"><span data-stu-id="83928-132">9</span></span>

<span data-ttu-id="83928-133">Objeto inválido.</span><span class="sxs-lookup"><span data-stu-id="83928-133">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="83928-134">**O objeto já existe**</span><span class="sxs-lookup"><span data-stu-id="83928-134">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="83928-135">10</span><span class="sxs-lookup"><span data-stu-id="83928-135">10</span></span>

<span data-ttu-id="83928-136">O objeto já existe.</span><span class="sxs-lookup"><span data-stu-id="83928-136">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="83928-137">**Sistema de arquivos não NTFS**</span><span class="sxs-lookup"><span data-stu-id="83928-137">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="83928-138">11</span><span class="sxs-lookup"><span data-stu-id="83928-138">11</span></span>

<span data-ttu-id="83928-139">Sistema de arquivos não NTFS.</span><span class="sxs-lookup"><span data-stu-id="83928-139">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="83928-140">**Plataforma não NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="83928-140">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="83928-141">12</span><span class="sxs-lookup"><span data-stu-id="83928-141">12</span></span>

<span data-ttu-id="83928-142">Plataforma não Windows.</span><span class="sxs-lookup"><span data-stu-id="83928-142">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="83928-143">**A unidade não é a mesma**</span><span class="sxs-lookup"><span data-stu-id="83928-143">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="83928-144">13</span><span class="sxs-lookup"><span data-stu-id="83928-144">13</span></span>

<span data-ttu-id="83928-145">A unidade não é a mesma.</span><span class="sxs-lookup"><span data-stu-id="83928-145">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="83928-146">**Diretório não vazio**</span><span class="sxs-lookup"><span data-stu-id="83928-146">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="83928-147">14</span><span class="sxs-lookup"><span data-stu-id="83928-147">14</span></span>

<span data-ttu-id="83928-148">O diretório não está vazio.</span><span class="sxs-lookup"><span data-stu-id="83928-148">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="83928-149">**Violação de compartilhamento**</span><span class="sxs-lookup"><span data-stu-id="83928-149">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="83928-150">15</span><span class="sxs-lookup"><span data-stu-id="83928-150">15</span></span>

<span data-ttu-id="83928-151">Violação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="83928-151">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="83928-152">**Arquivo de início inválido**</span><span class="sxs-lookup"><span data-stu-id="83928-152">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="83928-153">16</span><span class="sxs-lookup"><span data-stu-id="83928-153">16</span></span>

<span data-ttu-id="83928-154">Arquivo inicial inválido.</span><span class="sxs-lookup"><span data-stu-id="83928-154">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="83928-155">**Privilégio não mantido**</span><span class="sxs-lookup"><span data-stu-id="83928-155">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="83928-156">17</span><span class="sxs-lookup"><span data-stu-id="83928-156">17</span></span>

<span data-ttu-id="83928-157">Privilégio não mantido.</span><span class="sxs-lookup"><span data-stu-id="83928-157">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="83928-158">**Parâmetro inválido**</span><span class="sxs-lookup"><span data-stu-id="83928-158">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="83928-159">21</span><span class="sxs-lookup"><span data-stu-id="83928-159">21</span></span>

<span data-ttu-id="83928-160">Parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="83928-160">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="83928-161">Comentários</span><span class="sxs-lookup"><span data-stu-id="83928-161">Remarks</span></span>

<span data-ttu-id="83928-162">Este método não está implementado no momento pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="83928-162">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="83928-163">Para usar esse método, você deve implementá-lo em seu próprio provedor.</span><span class="sxs-lookup"><span data-stu-id="83928-163">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="83928-164">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="83928-164">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="83928-165">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="83928-165">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="83928-166">Requisitos</span><span class="sxs-lookup"><span data-stu-id="83928-166">Requirements</span></span>



| <span data-ttu-id="83928-167">Requisito</span><span class="sxs-lookup"><span data-stu-id="83928-167">Requirement</span></span> | <span data-ttu-id="83928-168">Valor</span><span class="sxs-lookup"><span data-stu-id="83928-168">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="83928-169">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="83928-169">Minimum supported client</span></span><br/> | <span data-ttu-id="83928-170">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="83928-170">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="83928-171">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="83928-171">Minimum supported server</span></span><br/> | <span data-ttu-id="83928-172">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="83928-172">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="83928-173">Namespace</span><span class="sxs-lookup"><span data-stu-id="83928-173">Namespace</span></span><br/>                | <span data-ttu-id="83928-174">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="83928-174">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="83928-175">MOF</span><span class="sxs-lookup"><span data-stu-id="83928-175">MOF</span></span><br/>                      | <dl> <span data-ttu-id="83928-176"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="83928-176"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="83928-177">DLL</span><span class="sxs-lookup"><span data-stu-id="83928-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="83928-178"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="83928-178"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83928-179">Confira também</span><span class="sxs-lookup"><span data-stu-id="83928-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83928-180">CIM \_ LogicalFile</span><span class="sxs-lookup"><span data-stu-id="83928-180">CIM\_LogicalFile</span></span>](deleteex-method-in-class-cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="83928-181">**CIM \_ LogicalFile**</span><span class="sxs-lookup"><span data-stu-id="83928-181">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

