---
description: O método Copy copia o arquivo lógico (ou diretório) especificado no caminho do objeto para o local especificado pelo parâmetro de entrada.
ms.assetid: 71481cc8-9052-4c62-9c26-6887ea646ee1
ms.tgt_platform: multiple
title: Método Copy da classe CIM_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.Copy
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 02bca61e559cea9ee56b9d36b28d13c33e423f9a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089260"
---
# <a name="copy-method-of-the-cim_directory-class"></a><span data-ttu-id="c5758-103">Método Copy da classe de \_ diretório CIM</span><span class="sxs-lookup"><span data-stu-id="c5758-103">Copy method of the CIM\_Directory class</span></span>

<span data-ttu-id="c5758-104">O método **Copy** copia o arquivo lógico (ou diretório) especificado no caminho do objeto para o local especificado pelo parâmetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="c5758-104">The **Copy** method copies the logical file (or directory) specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="c5758-105">Não haverá suporte para uma cópia se a substituição de um arquivo lógico existente for necessária.</span><span class="sxs-lookup"><span data-stu-id="c5758-105">A copy is not supported if overwriting an existing logical file is required.</span></span> <span data-ttu-id="c5758-106">Esse método é herdado [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="c5758-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c5758-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="c5758-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="c5758-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="c5758-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="c5758-109">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="c5758-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="c5758-110">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="c5758-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="c5758-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c5758-111">Syntax</span></span>


```mof
uint32 Copy(
  [in] string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="c5758-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c5758-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5758-113">*Nome do arquivo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c5758-113">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5758-114">Nome totalmente qualificado da cópia do arquivo de destino (ou diretório).</span><span class="sxs-lookup"><span data-stu-id="c5758-114">Fully qualified name of the copy of the destination file (or directory).</span></span>

<span data-ttu-id="c5758-115">Exemplo: "c: \\ temp \\ newdirectory"</span><span class="sxs-lookup"><span data-stu-id="c5758-115">Example: "c:\\temp\\newdirectory"</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5758-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c5758-116">Return value</span></span>

<span data-ttu-id="c5758-117">Retorna um valor 0 em caso de êxito e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="c5758-117">Returns a value of 0 on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="c5758-118">**0**</span><span class="sxs-lookup"><span data-stu-id="c5758-118">**0**</span></span>
</dt> <dd>

<span data-ttu-id="c5758-119">Êxito.</span><span class="sxs-lookup"><span data-stu-id="c5758-119">Success.</span></span>

</dd> <dt>

<span data-ttu-id="c5758-120">**2**</span><span class="sxs-lookup"><span data-stu-id="c5758-120">**2**</span></span>
</dt> <dd>

<span data-ttu-id="c5758-121">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="c5758-121">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="c5758-122">**8**</span><span class="sxs-lookup"><span data-stu-id="c5758-122">**8**</span></span>
</dt> <dd>

<span data-ttu-id="c5758-123">Falha não especificada.</span><span class="sxs-lookup"><span data-stu-id="c5758-123">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="c5758-124">**9**</span><span class="sxs-lookup"><span data-stu-id="c5758-124">**9**</span></span>
</dt> <dd>

<span data-ttu-id="c5758-125">Objeto inválido.</span><span class="sxs-lookup"><span data-stu-id="c5758-125">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="c5758-126">**10**</span><span class="sxs-lookup"><span data-stu-id="c5758-126">**10**</span></span>
</dt> <dd>

<span data-ttu-id="c5758-127">O objeto já existe.</span><span class="sxs-lookup"><span data-stu-id="c5758-127">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="c5758-128">**11**</span><span class="sxs-lookup"><span data-stu-id="c5758-128">**11**</span></span>
</dt> <dd>

<span data-ttu-id="c5758-129">Sistema de arquivos não NTFS.</span><span class="sxs-lookup"><span data-stu-id="c5758-129">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="c5758-130">**12**</span><span class="sxs-lookup"><span data-stu-id="c5758-130">**12**</span></span>
</dt> <dd>

<span data-ttu-id="c5758-131">Plataforma não Windows.</span><span class="sxs-lookup"><span data-stu-id="c5758-131">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="c5758-132">**13**</span><span class="sxs-lookup"><span data-stu-id="c5758-132">**13**</span></span>
</dt> <dd>

<span data-ttu-id="c5758-133">A unidade não é a mesma.</span><span class="sxs-lookup"><span data-stu-id="c5758-133">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="c5758-134">**14**</span><span class="sxs-lookup"><span data-stu-id="c5758-134">**14**</span></span>
</dt> <dd>

<span data-ttu-id="c5758-135">O diretório não está vazio.</span><span class="sxs-lookup"><span data-stu-id="c5758-135">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="c5758-136">**15**</span><span class="sxs-lookup"><span data-stu-id="c5758-136">**15**</span></span>
</dt> <dd>

<span data-ttu-id="c5758-137">Violação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="c5758-137">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="c5758-138">**16**</span><span class="sxs-lookup"><span data-stu-id="c5758-138">**16**</span></span>
</dt> <dd>

<span data-ttu-id="c5758-139">Arquivo inicial inválido.</span><span class="sxs-lookup"><span data-stu-id="c5758-139">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="c5758-140">**17**</span><span class="sxs-lookup"><span data-stu-id="c5758-140">**17**</span></span>
</dt> <dd>

<span data-ttu-id="c5758-141">Privilégio não mantido.</span><span class="sxs-lookup"><span data-stu-id="c5758-141">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="c5758-142">**Abril**</span><span class="sxs-lookup"><span data-stu-id="c5758-142">**21**</span></span>
</dt> <dd>

<span data-ttu-id="c5758-143">Parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="c5758-143">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c5758-144">Comentários</span><span class="sxs-lookup"><span data-stu-id="c5758-144">Remarks</span></span>

<span data-ttu-id="c5758-145">Este método não está implementado no momento pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="c5758-145">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="c5758-146">Para usar esse método, você deve implementá-lo em seu próprio provedor.</span><span class="sxs-lookup"><span data-stu-id="c5758-146">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="c5758-147">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="c5758-147">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="c5758-148">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="c5758-148">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5758-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5758-149">Requirements</span></span>



| <span data-ttu-id="c5758-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5758-150">Requirement</span></span> | <span data-ttu-id="c5758-151">Valor</span><span class="sxs-lookup"><span data-stu-id="c5758-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c5758-152">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c5758-152">Minimum supported client</span></span><br/> | <span data-ttu-id="c5758-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c5758-153">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c5758-154">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c5758-154">Minimum supported server</span></span><br/> | <span data-ttu-id="c5758-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c5758-155">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c5758-156">Namespace</span><span class="sxs-lookup"><span data-stu-id="c5758-156">Namespace</span></span><br/>                | <span data-ttu-id="c5758-157">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="c5758-157">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c5758-158">MOF</span><span class="sxs-lookup"><span data-stu-id="c5758-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c5758-159"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c5758-159"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c5758-160">DLL</span><span class="sxs-lookup"><span data-stu-id="c5758-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c5758-161"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c5758-161"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5758-162">Confira também</span><span class="sxs-lookup"><span data-stu-id="c5758-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5758-163">\_Diretório CIM</span><span class="sxs-lookup"><span data-stu-id="c5758-163">CIM\_Directory</span></span>](copy-method-in-class-cim-directory.md)
</dt> <dt>

[<span data-ttu-id="c5758-164">**\_Diretório CIM**</span><span class="sxs-lookup"><span data-stu-id="c5758-164">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> </dl>

 

