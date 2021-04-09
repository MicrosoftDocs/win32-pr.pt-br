---
description: O método renomear renomeia o arquivo lógico (ou diretório) especificado no caminho do objeto. Não haverá suporte para renomear se o destino estiver em outra unidade ou se for necessário substituir um arquivo lógico existente.
ms.assetid: 5a62ff64-d1d2-43a2-997c-0ad46896b31f
ms.tgt_platform: multiple
title: Método Rename da classe CIM_LogicalFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0da38020d7b22dceb6f1d061f8feaf858eeb5f04
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089479"
---
# <a name="rename-method-of-the-cim_logicalfile-class"></a><span data-ttu-id="b0bd1-104">Método Rename da classe de \_ LogicalFile CIM</span><span class="sxs-lookup"><span data-stu-id="b0bd1-104">Rename method of the CIM\_LogicalFile class</span></span>

<span data-ttu-id="b0bd1-105">O método **renomear** renomeia o arquivo lógico (ou diretório) especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="b0bd1-105">The **Rename** method renames the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="b0bd1-106">Não haverá suporte para renomear se o destino estiver em outra unidade ou se for necessário substituir um arquivo lógico existente.</span><span class="sxs-lookup"><span data-stu-id="b0bd1-106">Renaming is not supported if the destination is on another drive, or overwriting an existing logical file is required.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b0bd1-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="b0bd1-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b0bd1-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="b0bd1-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="b0bd1-109">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="b0bd1-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="b0bd1-110">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="b0bd1-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="b0bd1-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b0bd1-111">Syntax</span></span>


```mof
uint32 Rename(
  [in] string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="b0bd1-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b0bd1-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0bd1-113">*Nome do arquivo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b0bd1-113">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0bd1-114">Novo nome de arquivo (ou diretório) totalmente qualificado.</span><span class="sxs-lookup"><span data-stu-id="b0bd1-114">Fully qualified new file (or directory) name.</span></span>

<span data-ttu-id="b0bd1-115">Exemplo: "c: \\ temp \\newfile.txt"</span><span class="sxs-lookup"><span data-stu-id="b0bd1-115">Example: "c:\\temp\\newfile.txt"</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0bd1-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b0bd1-116">Return value</span></span>

<span data-ttu-id="b0bd1-117">Retorna um valor de 0 (zero) em caso de êxito e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="b0bd1-117">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="b0bd1-118">**Êxito**</span><span class="sxs-lookup"><span data-stu-id="b0bd1-118">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="b0bd1-119">0</span><span class="sxs-lookup"><span data-stu-id="b0bd1-119">0</span></span>

<span data-ttu-id="b0bd1-120">Sucesso.</span><span class="sxs-lookup"><span data-stu-id="b0bd1-120">Success.</span></span>

</dd> <dt>

<span data-ttu-id="b0bd1-121">**Acesso negado**</span><span class="sxs-lookup"><span data-stu-id="b0bd1-121">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="b0bd1-122">2</span><span class="sxs-lookup"><span data-stu-id="b0bd1-122">2</span></span>

<span data-ttu-id="b0bd1-123">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="b0bd1-123">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="b0bd1-124">**Falha não especificada**</span><span class="sxs-lookup"><span data-stu-id="b0bd1-124">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="b0bd1-125">8</span><span class="sxs-lookup"><span data-stu-id="b0bd1-125">8</span></span>

<span data-ttu-id="b0bd1-126">Falha não especificada.</span><span class="sxs-lookup"><span data-stu-id="b0bd1-126">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="b0bd1-127">**Objeto inválido**</span><span class="sxs-lookup"><span data-stu-id="b0bd1-127">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="b0bd1-128">9</span><span class="sxs-lookup"><span data-stu-id="b0bd1-128">9</span></span>

<span data-ttu-id="b0bd1-129">Objeto inválido.</span><span class="sxs-lookup"><span data-stu-id="b0bd1-129">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="b0bd1-130">**O objeto já existe**</span><span class="sxs-lookup"><span data-stu-id="b0bd1-130">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="b0bd1-131">10</span><span class="sxs-lookup"><span data-stu-id="b0bd1-131">10</span></span>

<span data-ttu-id="b0bd1-132">O objeto já existe.</span><span class="sxs-lookup"><span data-stu-id="b0bd1-132">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="b0bd1-133">**Sistema de arquivos não NTFS**</span><span class="sxs-lookup"><span data-stu-id="b0bd1-133">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="b0bd1-134">11</span><span class="sxs-lookup"><span data-stu-id="b0bd1-134">11</span></span>

<span data-ttu-id="b0bd1-135">Sistema de arquivos não NTFS.</span><span class="sxs-lookup"><span data-stu-id="b0bd1-135">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="b0bd1-136">**Plataforma não NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="b0bd1-136">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="b0bd1-137">12</span><span class="sxs-lookup"><span data-stu-id="b0bd1-137">12</span></span>

<span data-ttu-id="b0bd1-138">Plataforma não Windows.</span><span class="sxs-lookup"><span data-stu-id="b0bd1-138">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="b0bd1-139">**A unidade não é a mesma**</span><span class="sxs-lookup"><span data-stu-id="b0bd1-139">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="b0bd1-140">13</span><span class="sxs-lookup"><span data-stu-id="b0bd1-140">13</span></span>

<span data-ttu-id="b0bd1-141">A unidade não é a mesma.</span><span class="sxs-lookup"><span data-stu-id="b0bd1-141">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="b0bd1-142">**Diretório não vazio**</span><span class="sxs-lookup"><span data-stu-id="b0bd1-142">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="b0bd1-143">14</span><span class="sxs-lookup"><span data-stu-id="b0bd1-143">14</span></span>

<span data-ttu-id="b0bd1-144">O diretório não está vazio.</span><span class="sxs-lookup"><span data-stu-id="b0bd1-144">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="b0bd1-145">**Violação de compartilhamento**</span><span class="sxs-lookup"><span data-stu-id="b0bd1-145">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="b0bd1-146">15</span><span class="sxs-lookup"><span data-stu-id="b0bd1-146">15</span></span>

<span data-ttu-id="b0bd1-147">Violação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="b0bd1-147">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="b0bd1-148">**Arquivo de início inválido**</span><span class="sxs-lookup"><span data-stu-id="b0bd1-148">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="b0bd1-149">16</span><span class="sxs-lookup"><span data-stu-id="b0bd1-149">16</span></span>

<span data-ttu-id="b0bd1-150">Arquivo inicial inválido.</span><span class="sxs-lookup"><span data-stu-id="b0bd1-150">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="b0bd1-151">**Privilégio não mantido**</span><span class="sxs-lookup"><span data-stu-id="b0bd1-151">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="b0bd1-152">17</span><span class="sxs-lookup"><span data-stu-id="b0bd1-152">17</span></span>

<span data-ttu-id="b0bd1-153">Privilégio não mantido.</span><span class="sxs-lookup"><span data-stu-id="b0bd1-153">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="b0bd1-154">**Parâmetro inválido**</span><span class="sxs-lookup"><span data-stu-id="b0bd1-154">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="b0bd1-155">21</span><span class="sxs-lookup"><span data-stu-id="b0bd1-155">21</span></span>

<span data-ttu-id="b0bd1-156">Parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="b0bd1-156">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b0bd1-157">Comentários</span><span class="sxs-lookup"><span data-stu-id="b0bd1-157">Remarks</span></span>

<span data-ttu-id="b0bd1-158">Este método não está implementado no momento pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="b0bd1-158">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="b0bd1-159">Para usar esse método, você deve implementá-lo em seu próprio provedor.</span><span class="sxs-lookup"><span data-stu-id="b0bd1-159">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="b0bd1-160">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="b0bd1-160">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b0bd1-161">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="b0bd1-161">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0bd1-162">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b0bd1-162">Requirements</span></span>



| <span data-ttu-id="b0bd1-163">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0bd1-163">Requirement</span></span> | <span data-ttu-id="b0bd1-164">Valor</span><span class="sxs-lookup"><span data-stu-id="b0bd1-164">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b0bd1-165">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b0bd1-165">Minimum supported client</span></span><br/> | <span data-ttu-id="b0bd1-166">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b0bd1-166">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b0bd1-167">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b0bd1-167">Minimum supported server</span></span><br/> | <span data-ttu-id="b0bd1-168">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b0bd1-168">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b0bd1-169">Namespace</span><span class="sxs-lookup"><span data-stu-id="b0bd1-169">Namespace</span></span><br/>                | <span data-ttu-id="b0bd1-170">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="b0bd1-170">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b0bd1-171">MOF</span><span class="sxs-lookup"><span data-stu-id="b0bd1-171">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b0bd1-172"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b0bd1-172"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b0bd1-173">DLL</span><span class="sxs-lookup"><span data-stu-id="b0bd1-173">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b0bd1-174"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b0bd1-174"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0bd1-175">Confira também</span><span class="sxs-lookup"><span data-stu-id="b0bd1-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0bd1-176">CIM \_ LogicalFile</span><span class="sxs-lookup"><span data-stu-id="b0bd1-176">CIM\_LogicalFile</span></span>](rename-method-in-class-cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="b0bd1-177">**CIM \_ LogicalFile**</span><span class="sxs-lookup"><span data-stu-id="b0bd1-177">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

