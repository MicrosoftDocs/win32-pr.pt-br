---
description: Renomeia o arquivo lógico (ou diretório) especificado no caminho do objeto. Não haverá suporte para renomear se o destino estiver em outra unidade ou se for necessário substituir um arquivo lógico existente.
ms.assetid: 728737a7-7cb8-4237-be03-16c4dac530b2
ms.tgt_platform: multiple
title: Método Rename da classe CIM_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 83429f3a5248b1d3be24832b26bf99213d442ce5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457127"
---
# <a name="rename-method-of-the-cim_directory-class"></a><span data-ttu-id="6e4e7-104">Método Rename da classe de \_ diretório CIM</span><span class="sxs-lookup"><span data-stu-id="6e4e7-104">Rename method of the CIM\_Directory class</span></span>

<span data-ttu-id="6e4e7-105">O método **renomear** renomeia o arquivo lógico (ou diretório) especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="6e4e7-105">The **Rename** method renames the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="6e4e7-106">Não haverá suporte para renomear se o destino estiver em outra unidade ou se for necessário substituir um arquivo lógico existente.</span><span class="sxs-lookup"><span data-stu-id="6e4e7-106">Renaming is not supported if the destination is on another drive or overwriting an existing logical file is required.</span></span>

<span data-ttu-id="6e4e7-107">Esse método é herdado [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6e4e7-107">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6e4e7-108">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="6e4e7-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="6e4e7-109">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="6e4e7-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="6e4e7-110">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="6e4e7-110">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="6e4e7-111">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="6e4e7-111">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="6e4e7-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6e4e7-112">Syntax</span></span>


```mof
uint32 Rename(
  [in] string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="6e4e7-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6e4e7-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e4e7-114">*Nome do arquivo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6e4e7-114">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e4e7-115">Novo nome totalmente qualificado do arquivo (ou diretório).</span><span class="sxs-lookup"><span data-stu-id="6e4e7-115">Fully qualified new name of the file (or directory).</span></span>

<span data-ttu-id="6e4e7-116">Exemplo: "c: \\ temp \\newname.txt"</span><span class="sxs-lookup"><span data-stu-id="6e4e7-116">Example: "c:\\temp\\newname.txt"</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e4e7-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6e4e7-117">Return value</span></span>

<span data-ttu-id="6e4e7-118">Retorna um valor de 0 (zero) em caso de êxito e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="6e4e7-118">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="6e4e7-119">**0**</span><span class="sxs-lookup"><span data-stu-id="6e4e7-119">**0**</span></span>
</dt> <dd>

<span data-ttu-id="6e4e7-120">Êxito.</span><span class="sxs-lookup"><span data-stu-id="6e4e7-120">Success.</span></span>

</dd> <dt>

<span data-ttu-id="6e4e7-121">**2**</span><span class="sxs-lookup"><span data-stu-id="6e4e7-121">**2**</span></span>
</dt> <dd>

<span data-ttu-id="6e4e7-122">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="6e4e7-122">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="6e4e7-123">**8**</span><span class="sxs-lookup"><span data-stu-id="6e4e7-123">**8**</span></span>
</dt> <dd>

<span data-ttu-id="6e4e7-124">Falha não especificada.</span><span class="sxs-lookup"><span data-stu-id="6e4e7-124">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="6e4e7-125">**9**</span><span class="sxs-lookup"><span data-stu-id="6e4e7-125">**9**</span></span>
</dt> <dd>

<span data-ttu-id="6e4e7-126">Objeto inválido.</span><span class="sxs-lookup"><span data-stu-id="6e4e7-126">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="6e4e7-127">**10**</span><span class="sxs-lookup"><span data-stu-id="6e4e7-127">**10**</span></span>
</dt> <dd>

<span data-ttu-id="6e4e7-128">O objeto já existe.</span><span class="sxs-lookup"><span data-stu-id="6e4e7-128">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="6e4e7-129">**11**</span><span class="sxs-lookup"><span data-stu-id="6e4e7-129">**11**</span></span>
</dt> <dd>

<span data-ttu-id="6e4e7-130">Sistema de arquivos não NTFS.</span><span class="sxs-lookup"><span data-stu-id="6e4e7-130">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="6e4e7-131">**12**</span><span class="sxs-lookup"><span data-stu-id="6e4e7-131">**12**</span></span>
</dt> <dd>

<span data-ttu-id="6e4e7-132">Plataforma não Windows.</span><span class="sxs-lookup"><span data-stu-id="6e4e7-132">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="6e4e7-133">**13**</span><span class="sxs-lookup"><span data-stu-id="6e4e7-133">**13**</span></span>
</dt> <dd>

<span data-ttu-id="6e4e7-134">A unidade não é a mesma.</span><span class="sxs-lookup"><span data-stu-id="6e4e7-134">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="6e4e7-135">**14**</span><span class="sxs-lookup"><span data-stu-id="6e4e7-135">**14**</span></span>
</dt> <dd>

<span data-ttu-id="6e4e7-136">O diretório não está vazio.</span><span class="sxs-lookup"><span data-stu-id="6e4e7-136">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="6e4e7-137">**15**</span><span class="sxs-lookup"><span data-stu-id="6e4e7-137">**15**</span></span>
</dt> <dd>

<span data-ttu-id="6e4e7-138">Violação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="6e4e7-138">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="6e4e7-139">**16**</span><span class="sxs-lookup"><span data-stu-id="6e4e7-139">**16**</span></span>
</dt> <dd>

<span data-ttu-id="6e4e7-140">Arquivo inicial inválido.</span><span class="sxs-lookup"><span data-stu-id="6e4e7-140">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="6e4e7-141">**17**</span><span class="sxs-lookup"><span data-stu-id="6e4e7-141">**17**</span></span>
</dt> <dd>

<span data-ttu-id="6e4e7-142">Privilégio não mantido.</span><span class="sxs-lookup"><span data-stu-id="6e4e7-142">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="6e4e7-143">**Abril**</span><span class="sxs-lookup"><span data-stu-id="6e4e7-143">**21**</span></span>
</dt> <dd>

<span data-ttu-id="6e4e7-144">Parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="6e4e7-144">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6e4e7-145">Comentários</span><span class="sxs-lookup"><span data-stu-id="6e4e7-145">Remarks</span></span>

<span data-ttu-id="6e4e7-146">Este método não está implementado no momento pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="6e4e7-146">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="6e4e7-147">Para usar esse método, você deve implementá-lo em seu próprio provedor.</span><span class="sxs-lookup"><span data-stu-id="6e4e7-147">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="6e4e7-148">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="6e4e7-148">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="6e4e7-149">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="6e4e7-149">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e4e7-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e4e7-150">Requirements</span></span>



| <span data-ttu-id="6e4e7-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e4e7-151">Requirement</span></span> | <span data-ttu-id="6e4e7-152">Valor</span><span class="sxs-lookup"><span data-stu-id="6e4e7-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6e4e7-153">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6e4e7-153">Minimum supported client</span></span><br/> | <span data-ttu-id="6e4e7-154">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6e4e7-154">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6e4e7-155">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6e4e7-155">Minimum supported server</span></span><br/> | <span data-ttu-id="6e4e7-156">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6e4e7-156">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6e4e7-157">Namespace</span><span class="sxs-lookup"><span data-stu-id="6e4e7-157">Namespace</span></span><br/>                | <span data-ttu-id="6e4e7-158">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="6e4e7-158">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6e4e7-159">MOF</span><span class="sxs-lookup"><span data-stu-id="6e4e7-159">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6e4e7-160"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6e4e7-160"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6e4e7-161">DLL</span><span class="sxs-lookup"><span data-stu-id="6e4e7-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6e4e7-162"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6e4e7-162"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e4e7-163">Confira também</span><span class="sxs-lookup"><span data-stu-id="6e4e7-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e4e7-164">\_Diretório CIM</span><span class="sxs-lookup"><span data-stu-id="6e4e7-164">CIM\_Directory</span></span>](rename-method-in-class-cim-directory.md)
</dt> <dt>

[<span data-ttu-id="6e4e7-165">**\_Diretório CIM**</span><span class="sxs-lookup"><span data-stu-id="6e4e7-165">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> </dl>

 

