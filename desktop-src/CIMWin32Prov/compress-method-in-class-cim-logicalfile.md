---
description: O método compress compacta o arquivo lógico (ou diretório) especificado no caminho do objeto.
ms.assetid: 4a26beaf-388b-4f37-b4ee-ef3a7d15d2b6
ms.tgt_platform: multiple
title: Método compress da classe CIM_LogicalFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.Compress
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 12938001d62920916e75d70ad632170c3e92bd51
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826194"
---
# <a name="compress-method-of-the-cim_logicalfile-class"></a><span data-ttu-id="f53ab-103">Método compress da \_ classe LogicalFile do CIM</span><span class="sxs-lookup"><span data-stu-id="f53ab-103">Compress method of the CIM\_LogicalFile class</span></span>

<span data-ttu-id="f53ab-104">O método **compress** compacta o arquivo lógico (ou diretório) especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="f53ab-104">The **Compress** method compresses the logical file (or directory) specified in the object path.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f53ab-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="f53ab-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="f53ab-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="f53ab-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="f53ab-107">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="f53ab-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="f53ab-108">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="f53ab-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="f53ab-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f53ab-109">Syntax</span></span>


```mof
uint32 Compress();
```



## <a name="parameters"></a><span data-ttu-id="f53ab-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f53ab-110">Parameters</span></span>

<span data-ttu-id="f53ab-111">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="f53ab-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f53ab-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f53ab-112">Return value</span></span>

<span data-ttu-id="f53ab-113">Retorna um valor de 0 (zero) em caso de êxito e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="f53ab-113">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="f53ab-114">**Êxito**</span><span class="sxs-lookup"><span data-stu-id="f53ab-114">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="f53ab-115">0</span><span class="sxs-lookup"><span data-stu-id="f53ab-115">0</span></span>

<span data-ttu-id="f53ab-116">Sucesso.</span><span class="sxs-lookup"><span data-stu-id="f53ab-116">Success.</span></span>

</dd> <dt>

<span data-ttu-id="f53ab-117">**Acesso negado**</span><span class="sxs-lookup"><span data-stu-id="f53ab-117">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="f53ab-118">2</span><span class="sxs-lookup"><span data-stu-id="f53ab-118">2</span></span>

<span data-ttu-id="f53ab-119">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="f53ab-119">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="f53ab-120">**Falha não especificada**</span><span class="sxs-lookup"><span data-stu-id="f53ab-120">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="f53ab-121">8</span><span class="sxs-lookup"><span data-stu-id="f53ab-121">8</span></span>

<span data-ttu-id="f53ab-122">Falha não especificada.</span><span class="sxs-lookup"><span data-stu-id="f53ab-122">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="f53ab-123">**Objeto inválido**</span><span class="sxs-lookup"><span data-stu-id="f53ab-123">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="f53ab-124">9</span><span class="sxs-lookup"><span data-stu-id="f53ab-124">9</span></span>

<span data-ttu-id="f53ab-125">Objeto inválido.</span><span class="sxs-lookup"><span data-stu-id="f53ab-125">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="f53ab-126">**O objeto já existe**</span><span class="sxs-lookup"><span data-stu-id="f53ab-126">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="f53ab-127">10</span><span class="sxs-lookup"><span data-stu-id="f53ab-127">10</span></span>

<span data-ttu-id="f53ab-128">O objeto já existe.</span><span class="sxs-lookup"><span data-stu-id="f53ab-128">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="f53ab-129">**Sistema de arquivos não NTFS**</span><span class="sxs-lookup"><span data-stu-id="f53ab-129">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="f53ab-130">11</span><span class="sxs-lookup"><span data-stu-id="f53ab-130">11</span></span>

<span data-ttu-id="f53ab-131">Sistema de arquivos não NTFS.</span><span class="sxs-lookup"><span data-stu-id="f53ab-131">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="f53ab-132">**Plataforma não NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="f53ab-132">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="f53ab-133">12</span><span class="sxs-lookup"><span data-stu-id="f53ab-133">12</span></span>

<span data-ttu-id="f53ab-134">Plataforma não Windows.</span><span class="sxs-lookup"><span data-stu-id="f53ab-134">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="f53ab-135">**A unidade não é a mesma**</span><span class="sxs-lookup"><span data-stu-id="f53ab-135">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="f53ab-136">13</span><span class="sxs-lookup"><span data-stu-id="f53ab-136">13</span></span>

<span data-ttu-id="f53ab-137">A unidade não é a mesma.</span><span class="sxs-lookup"><span data-stu-id="f53ab-137">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="f53ab-138">**Diretório não vazio**</span><span class="sxs-lookup"><span data-stu-id="f53ab-138">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="f53ab-139">14</span><span class="sxs-lookup"><span data-stu-id="f53ab-139">14</span></span>

<span data-ttu-id="f53ab-140">O diretório não está vazio.</span><span class="sxs-lookup"><span data-stu-id="f53ab-140">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="f53ab-141">**Violação de compartilhamento**</span><span class="sxs-lookup"><span data-stu-id="f53ab-141">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="f53ab-142">15</span><span class="sxs-lookup"><span data-stu-id="f53ab-142">15</span></span>

<span data-ttu-id="f53ab-143">Violação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="f53ab-143">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="f53ab-144">**Arquivo de início inválido**</span><span class="sxs-lookup"><span data-stu-id="f53ab-144">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="f53ab-145">16</span><span class="sxs-lookup"><span data-stu-id="f53ab-145">16</span></span>

<span data-ttu-id="f53ab-146">Arquivo inicial inválido.</span><span class="sxs-lookup"><span data-stu-id="f53ab-146">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="f53ab-147">**Privilégio não mantido**</span><span class="sxs-lookup"><span data-stu-id="f53ab-147">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="f53ab-148">17</span><span class="sxs-lookup"><span data-stu-id="f53ab-148">17</span></span>

<span data-ttu-id="f53ab-149">Privilégio não mantido.</span><span class="sxs-lookup"><span data-stu-id="f53ab-149">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="f53ab-150">**Parâmetro inválido**</span><span class="sxs-lookup"><span data-stu-id="f53ab-150">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="f53ab-151">21</span><span class="sxs-lookup"><span data-stu-id="f53ab-151">21</span></span>

<span data-ttu-id="f53ab-152">Parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="f53ab-152">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f53ab-153">Comentários</span><span class="sxs-lookup"><span data-stu-id="f53ab-153">Remarks</span></span>

<span data-ttu-id="f53ab-154">Este método não está implementado no momento pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="f53ab-154">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="f53ab-155">Para usar esse método, você deve implementá-lo em seu próprio provedor.</span><span class="sxs-lookup"><span data-stu-id="f53ab-155">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="f53ab-156">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="f53ab-156">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="f53ab-157">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="f53ab-157">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f53ab-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f53ab-158">Requirements</span></span>



| <span data-ttu-id="f53ab-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="f53ab-159">Requirement</span></span> | <span data-ttu-id="f53ab-160">Valor</span><span class="sxs-lookup"><span data-stu-id="f53ab-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f53ab-161">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f53ab-161">Minimum supported client</span></span><br/> | <span data-ttu-id="f53ab-162">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f53ab-162">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f53ab-163">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f53ab-163">Minimum supported server</span></span><br/> | <span data-ttu-id="f53ab-164">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f53ab-164">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f53ab-165">Namespace</span><span class="sxs-lookup"><span data-stu-id="f53ab-165">Namespace</span></span><br/>                | <span data-ttu-id="f53ab-166">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="f53ab-166">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f53ab-167">MOF</span><span class="sxs-lookup"><span data-stu-id="f53ab-167">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f53ab-168"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f53ab-168"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f53ab-169">DLL</span><span class="sxs-lookup"><span data-stu-id="f53ab-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f53ab-170"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f53ab-170"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f53ab-171">Confira também</span><span class="sxs-lookup"><span data-stu-id="f53ab-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f53ab-172">CIM \_ LogicalFile</span><span class="sxs-lookup"><span data-stu-id="f53ab-172">CIM\_LogicalFile</span></span>](compress-method-in-class-cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="f53ab-173">**CIM \_ LogicalFile**</span><span class="sxs-lookup"><span data-stu-id="f53ab-173">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

