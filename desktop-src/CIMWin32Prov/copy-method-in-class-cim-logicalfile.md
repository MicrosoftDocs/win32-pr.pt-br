---
description: Método Copy da classe CIM_LogicalFile – o método Copy copia o arquivo lógico (ou diretório) especificado no caminho do objeto para o local especificado pelo parâmetro de entrada.
ms.assetid: 643946e4-5d32-4839-ae1f-80ec7cede429
ms.tgt_platform: multiple
title: Método Copy da classe CIM_LogicalFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.Copy
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 10ba9c28bde9d909d947e5a73241ce1aa8f1e956
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089724"
---
# <a name="copy-method-of-the-cim_logicalfile-class"></a><span data-ttu-id="795fb-103">Método Copy da \_ classe LogicalFile do CIM</span><span class="sxs-lookup"><span data-stu-id="795fb-103">Copy method of the CIM\_LogicalFile class</span></span>

<span data-ttu-id="795fb-104">O método **Copy** copia o arquivo lógico (ou diretório) especificado no caminho do objeto para o local especificado pelo parâmetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="795fb-104">The **Copy** method copies the logical file (or directory) specified in the object path to the location specified by the input parameter.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="795fb-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="795fb-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="795fb-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="795fb-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="795fb-107">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="795fb-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="795fb-108">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="795fb-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="795fb-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="795fb-109">Syntax</span></span>


```mof
uint32 Copy(
  [in] string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="795fb-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="795fb-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="795fb-111">*Nome do arquivo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="795fb-111">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="795fb-112">Nome totalmente qualificado do arquivo de destino (ou diretório).</span><span class="sxs-lookup"><span data-stu-id="795fb-112">Fully qualified name of the destination file (or directory).</span></span>

<span data-ttu-id="795fb-113">Exemplo: "c: \\ temp \\ newdirectory"</span><span class="sxs-lookup"><span data-stu-id="795fb-113">Example: "c:\\temp\\newdirectory"</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="795fb-114">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="795fb-114">Return value</span></span>

<span data-ttu-id="795fb-115">Retorna um valor de 0 (zero) em caso de êxito e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="795fb-115">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="795fb-116">**Êxito**</span><span class="sxs-lookup"><span data-stu-id="795fb-116">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="795fb-117">0</span><span class="sxs-lookup"><span data-stu-id="795fb-117">0</span></span>

<span data-ttu-id="795fb-118">Sucesso.</span><span class="sxs-lookup"><span data-stu-id="795fb-118">Success.</span></span>

</dd> <dt>

<span data-ttu-id="795fb-119">**Acesso negado**</span><span class="sxs-lookup"><span data-stu-id="795fb-119">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="795fb-120">2</span><span class="sxs-lookup"><span data-stu-id="795fb-120">2</span></span>

<span data-ttu-id="795fb-121">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="795fb-121">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="795fb-122">**Falha não especificada**</span><span class="sxs-lookup"><span data-stu-id="795fb-122">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="795fb-123">8</span><span class="sxs-lookup"><span data-stu-id="795fb-123">8</span></span>

<span data-ttu-id="795fb-124">Falha não especificada.</span><span class="sxs-lookup"><span data-stu-id="795fb-124">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="795fb-125">**Objeto inválido**</span><span class="sxs-lookup"><span data-stu-id="795fb-125">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="795fb-126">9</span><span class="sxs-lookup"><span data-stu-id="795fb-126">9</span></span>

<span data-ttu-id="795fb-127">Objeto inválido.</span><span class="sxs-lookup"><span data-stu-id="795fb-127">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="795fb-128">**O objeto já existe**</span><span class="sxs-lookup"><span data-stu-id="795fb-128">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="795fb-129">10</span><span class="sxs-lookup"><span data-stu-id="795fb-129">10</span></span>

<span data-ttu-id="795fb-130">O objeto já existe.</span><span class="sxs-lookup"><span data-stu-id="795fb-130">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="795fb-131">**Sistema de arquivos não NTFS**</span><span class="sxs-lookup"><span data-stu-id="795fb-131">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="795fb-132">11</span><span class="sxs-lookup"><span data-stu-id="795fb-132">11</span></span>

<span data-ttu-id="795fb-133">Sistema de arquivos não NTFS.</span><span class="sxs-lookup"><span data-stu-id="795fb-133">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="795fb-134">**Plataforma não NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="795fb-134">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="795fb-135">12</span><span class="sxs-lookup"><span data-stu-id="795fb-135">12</span></span>

<span data-ttu-id="795fb-136">Plataforma não Windows.</span><span class="sxs-lookup"><span data-stu-id="795fb-136">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="795fb-137">**A unidade não é a mesma**</span><span class="sxs-lookup"><span data-stu-id="795fb-137">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="795fb-138">13</span><span class="sxs-lookup"><span data-stu-id="795fb-138">13</span></span>

<span data-ttu-id="795fb-139">A unidade não é a mesma.</span><span class="sxs-lookup"><span data-stu-id="795fb-139">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="795fb-140">**Diretório não vazio**</span><span class="sxs-lookup"><span data-stu-id="795fb-140">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="795fb-141">14</span><span class="sxs-lookup"><span data-stu-id="795fb-141">14</span></span>

<span data-ttu-id="795fb-142">O diretório não está vazio.</span><span class="sxs-lookup"><span data-stu-id="795fb-142">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="795fb-143">**Violação de compartilhamento**</span><span class="sxs-lookup"><span data-stu-id="795fb-143">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="795fb-144">15</span><span class="sxs-lookup"><span data-stu-id="795fb-144">15</span></span>

<span data-ttu-id="795fb-145">Violação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="795fb-145">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="795fb-146">**Arquivo de início inválido**</span><span class="sxs-lookup"><span data-stu-id="795fb-146">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="795fb-147">16</span><span class="sxs-lookup"><span data-stu-id="795fb-147">16</span></span>

<span data-ttu-id="795fb-148">Arquivo inicial inválido.</span><span class="sxs-lookup"><span data-stu-id="795fb-148">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="795fb-149">**Privilégio não mantido**</span><span class="sxs-lookup"><span data-stu-id="795fb-149">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="795fb-150">17</span><span class="sxs-lookup"><span data-stu-id="795fb-150">17</span></span>

<span data-ttu-id="795fb-151">Privilégio não mantido.</span><span class="sxs-lookup"><span data-stu-id="795fb-151">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="795fb-152">**Parâmetro inválido**</span><span class="sxs-lookup"><span data-stu-id="795fb-152">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="795fb-153">21</span><span class="sxs-lookup"><span data-stu-id="795fb-153">21</span></span>

<span data-ttu-id="795fb-154">Parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="795fb-154">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="795fb-155">Comentários</span><span class="sxs-lookup"><span data-stu-id="795fb-155">Remarks</span></span>

<span data-ttu-id="795fb-156">Este método não está implementado no momento pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="795fb-156">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="795fb-157">Para usar esse método, você deve implementá-lo em seu próprio provedor.</span><span class="sxs-lookup"><span data-stu-id="795fb-157">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="795fb-158">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="795fb-158">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="795fb-159">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="795fb-159">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="795fb-160">Requisitos</span><span class="sxs-lookup"><span data-stu-id="795fb-160">Requirements</span></span>



| <span data-ttu-id="795fb-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="795fb-161">Requirement</span></span> | <span data-ttu-id="795fb-162">Valor</span><span class="sxs-lookup"><span data-stu-id="795fb-162">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="795fb-163">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="795fb-163">Minimum supported client</span></span><br/> | <span data-ttu-id="795fb-164">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="795fb-164">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="795fb-165">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="795fb-165">Minimum supported server</span></span><br/> | <span data-ttu-id="795fb-166">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="795fb-166">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="795fb-167">Namespace</span><span class="sxs-lookup"><span data-stu-id="795fb-167">Namespace</span></span><br/>                | <span data-ttu-id="795fb-168">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="795fb-168">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="795fb-169">MOF</span><span class="sxs-lookup"><span data-stu-id="795fb-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="795fb-170"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="795fb-170"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="795fb-171">DLL</span><span class="sxs-lookup"><span data-stu-id="795fb-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="795fb-172"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="795fb-172"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="795fb-173">Consulte também</span><span class="sxs-lookup"><span data-stu-id="795fb-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="795fb-174">CIM \_ LogicalFile</span><span class="sxs-lookup"><span data-stu-id="795fb-174">CIM\_LogicalFile</span></span>](copy-method-in-class-cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="795fb-175">**CIM \_ LogicalFile**</span><span class="sxs-lookup"><span data-stu-id="795fb-175">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

