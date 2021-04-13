---
description: O método TakeOwnerShip Obtém a propriedade do arquivo lógico especificado no caminho do objeto. Se o arquivo lógico for um diretório, esse método agirá recursivamente, assumindo a propriedade de todos os arquivos e subdiretórios contidos no diretório.
ms.assetid: 5db62da0-ac93-4a8c-af17-306e02bfa756
ms.tgt_platform: multiple
title: Método TakeOwnerShip da classe CIM_LogicalFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.TakeOwnerShip
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7cdd9515a5e947a3e707464dcbd524c875f7785f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500791"
---
# <a name="takeownership-method-of-the-cim_logicalfile-class"></a><span data-ttu-id="759fd-104">Método TakeOwnerShip da classe de \_ LogicalFile CIM</span><span class="sxs-lookup"><span data-stu-id="759fd-104">TakeOwnerShip method of the CIM\_LogicalFile class</span></span>

<span data-ttu-id="759fd-105">O método **TakeOwnership** Obtém a propriedade do arquivo lógico especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="759fd-105">The **TakeOwnerShip** method obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="759fd-106">Se o arquivo lógico for um diretório, esse método agirá recursivamente, assumindo a propriedade de todos os arquivos e subdiretórios contidos no diretório.</span><span class="sxs-lookup"><span data-stu-id="759fd-106">If the logical file is a directory, then this method acts recursively, taking ownership of all files and sub-directories that the directory contains.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="759fd-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="759fd-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="759fd-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="759fd-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="759fd-109">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="759fd-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="759fd-110">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="759fd-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="759fd-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="759fd-111">Syntax</span></span>


```mof
uint32 TakeOwnerShip();
```



## <a name="parameters"></a><span data-ttu-id="759fd-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="759fd-112">Parameters</span></span>

<span data-ttu-id="759fd-113">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="759fd-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="759fd-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="759fd-114">Return value</span></span>

<span data-ttu-id="759fd-115">Retorna um valor de 0 (zero) em caso de êxito e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="759fd-115">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="759fd-116">**Êxito**</span><span class="sxs-lookup"><span data-stu-id="759fd-116">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="759fd-117">0</span><span class="sxs-lookup"><span data-stu-id="759fd-117">0</span></span>

<span data-ttu-id="759fd-118">Sucesso.</span><span class="sxs-lookup"><span data-stu-id="759fd-118">Success.</span></span>

</dd> <dt>

<span data-ttu-id="759fd-119">**Acesso negado**</span><span class="sxs-lookup"><span data-stu-id="759fd-119">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="759fd-120">2</span><span class="sxs-lookup"><span data-stu-id="759fd-120">2</span></span>

<span data-ttu-id="759fd-121">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="759fd-121">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="759fd-122">**Falha não especificada**</span><span class="sxs-lookup"><span data-stu-id="759fd-122">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="759fd-123">8</span><span class="sxs-lookup"><span data-stu-id="759fd-123">8</span></span>

<span data-ttu-id="759fd-124">Falha não especificada.</span><span class="sxs-lookup"><span data-stu-id="759fd-124">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="759fd-125">**Objeto inválido**</span><span class="sxs-lookup"><span data-stu-id="759fd-125">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="759fd-126">9</span><span class="sxs-lookup"><span data-stu-id="759fd-126">9</span></span>

<span data-ttu-id="759fd-127">Objeto inválido.</span><span class="sxs-lookup"><span data-stu-id="759fd-127">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="759fd-128">**O objeto já existe**</span><span class="sxs-lookup"><span data-stu-id="759fd-128">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="759fd-129">10</span><span class="sxs-lookup"><span data-stu-id="759fd-129">10</span></span>

<span data-ttu-id="759fd-130">O objeto já existe.</span><span class="sxs-lookup"><span data-stu-id="759fd-130">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="759fd-131">**Sistema de arquivos não NTFS**</span><span class="sxs-lookup"><span data-stu-id="759fd-131">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="759fd-132">11</span><span class="sxs-lookup"><span data-stu-id="759fd-132">11</span></span>

<span data-ttu-id="759fd-133">Sistema de arquivos não NTFS.</span><span class="sxs-lookup"><span data-stu-id="759fd-133">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="759fd-134">**Plataforma não NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="759fd-134">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="759fd-135">12</span><span class="sxs-lookup"><span data-stu-id="759fd-135">12</span></span>

<span data-ttu-id="759fd-136">Plataforma não Windows.</span><span class="sxs-lookup"><span data-stu-id="759fd-136">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="759fd-137">**A unidade não é a mesma**</span><span class="sxs-lookup"><span data-stu-id="759fd-137">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="759fd-138">13</span><span class="sxs-lookup"><span data-stu-id="759fd-138">13</span></span>

<span data-ttu-id="759fd-139">A unidade não é a mesma.</span><span class="sxs-lookup"><span data-stu-id="759fd-139">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="759fd-140">**Diretório não vazio**</span><span class="sxs-lookup"><span data-stu-id="759fd-140">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="759fd-141">14</span><span class="sxs-lookup"><span data-stu-id="759fd-141">14</span></span>

<span data-ttu-id="759fd-142">O diretório não está vazio.</span><span class="sxs-lookup"><span data-stu-id="759fd-142">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="759fd-143">**Violação de compartilhamento**</span><span class="sxs-lookup"><span data-stu-id="759fd-143">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="759fd-144">15</span><span class="sxs-lookup"><span data-stu-id="759fd-144">15</span></span>

<span data-ttu-id="759fd-145">Violação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="759fd-145">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="759fd-146">**Arquivo de início inválido**</span><span class="sxs-lookup"><span data-stu-id="759fd-146">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="759fd-147">16</span><span class="sxs-lookup"><span data-stu-id="759fd-147">16</span></span>

<span data-ttu-id="759fd-148">Arquivo inicial inválido.</span><span class="sxs-lookup"><span data-stu-id="759fd-148">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="759fd-149">**Privilégio não mantido**</span><span class="sxs-lookup"><span data-stu-id="759fd-149">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="759fd-150">17</span><span class="sxs-lookup"><span data-stu-id="759fd-150">17</span></span>

<span data-ttu-id="759fd-151">Privilégio não mantido.</span><span class="sxs-lookup"><span data-stu-id="759fd-151">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="759fd-152">**Parâmetro inválido**</span><span class="sxs-lookup"><span data-stu-id="759fd-152">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="759fd-153">21</span><span class="sxs-lookup"><span data-stu-id="759fd-153">21</span></span>

<span data-ttu-id="759fd-154">Parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="759fd-154">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="759fd-155">Comentários</span><span class="sxs-lookup"><span data-stu-id="759fd-155">Remarks</span></span>

<span data-ttu-id="759fd-156">Este método não está implementado no momento pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="759fd-156">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="759fd-157">Para usar esse método, você deve implementá-lo em seu próprio provedor.</span><span class="sxs-lookup"><span data-stu-id="759fd-157">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="759fd-158">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="759fd-158">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="759fd-159">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="759fd-159">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="759fd-160">Requisitos</span><span class="sxs-lookup"><span data-stu-id="759fd-160">Requirements</span></span>



| <span data-ttu-id="759fd-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="759fd-161">Requirement</span></span> | <span data-ttu-id="759fd-162">Valor</span><span class="sxs-lookup"><span data-stu-id="759fd-162">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="759fd-163">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="759fd-163">Minimum supported client</span></span><br/> | <span data-ttu-id="759fd-164">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="759fd-164">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="759fd-165">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="759fd-165">Minimum supported server</span></span><br/> | <span data-ttu-id="759fd-166">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="759fd-166">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="759fd-167">Namespace</span><span class="sxs-lookup"><span data-stu-id="759fd-167">Namespace</span></span><br/>                | <span data-ttu-id="759fd-168">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="759fd-168">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="759fd-169">MOF</span><span class="sxs-lookup"><span data-stu-id="759fd-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="759fd-170"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="759fd-170"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="759fd-171">DLL</span><span class="sxs-lookup"><span data-stu-id="759fd-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="759fd-172"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="759fd-172"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="759fd-173">Confira também</span><span class="sxs-lookup"><span data-stu-id="759fd-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="759fd-174">CIM \_ LogicalFile</span><span class="sxs-lookup"><span data-stu-id="759fd-174">CIM\_LogicalFile</span></span>](takeownership-method-in-class-cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="759fd-175">**CIM \_ LogicalFile**</span><span class="sxs-lookup"><span data-stu-id="759fd-175">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

