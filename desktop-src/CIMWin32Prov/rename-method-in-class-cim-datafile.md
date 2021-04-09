---
description: O método renomear renomeia o arquivo lógico (ou diretório) que é especificado no caminho do objeto.
ms.assetid: 3eaf9f4f-270e-41d0-86ae-c5edb1850ef5
ms.tgt_platform: multiple
title: Método Rename da classe CIM_DataFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: aea061990a6d3bd52a98dc9101102059767ecf9a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089484"
---
# <a name="rename-method-of-the-cim_datafile-class"></a><span data-ttu-id="2e1a7-103">Método Rename da classe de \_ datafilefiles CIM</span><span class="sxs-lookup"><span data-stu-id="2e1a7-103">Rename method of the CIM\_DataFile class</span></span>

<span data-ttu-id="2e1a7-104">O método **renomear** renomeia o arquivo lógico (ou diretório) que é especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="2e1a7-104">The **Rename** method renames the logical file (or directory) that is specified in the object path.</span></span> <span data-ttu-id="2e1a7-105">Não haverá suporte para renomear se o destino estiver em outra unidade ou se for necessário substituir um arquivo lógico existente.</span><span class="sxs-lookup"><span data-stu-id="2e1a7-105">A rename is not supported if the destination is on another drive or if overwriting an existing logical file is required.</span></span> <span data-ttu-id="2e1a7-106">Esse método é herdado [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="2e1a7-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2e1a7-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="2e1a7-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="2e1a7-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="2e1a7-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="2e1a7-109">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="2e1a7-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="2e1a7-110">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="2e1a7-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="2e1a7-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2e1a7-111">Syntax</span></span>


```mof
uint32 Rename(
  [in] string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="2e1a7-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2e1a7-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e1a7-113">*Nome do arquivo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2e1a7-113">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e1a7-114">Novo nome totalmente qualificado do arquivo (ou diretório).</span><span class="sxs-lookup"><span data-stu-id="2e1a7-114">Fully qualified new name of the file (or directory).</span></span>

<span data-ttu-id="2e1a7-115">Exemplo: "c: \\ temp \\newfile.txt"</span><span class="sxs-lookup"><span data-stu-id="2e1a7-115">Example: "c:\\temp\\newfile.txt"</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e1a7-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2e1a7-116">Return value</span></span>

<span data-ttu-id="2e1a7-117">Retorna um valor 0 em caso de êxito e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="2e1a7-117">Returns a value of 0 on success, and any other number to indicate an error.</span></span> <span data-ttu-id="2e1a7-118">Para obter códigos de erro adicionais, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="2e1a7-118">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="2e1a7-119">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="2e1a7-119">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="2e1a7-120">**0**</span><span class="sxs-lookup"><span data-stu-id="2e1a7-120">**0**</span></span>
</dt> <dd>

<span data-ttu-id="2e1a7-121">Êxito.</span><span class="sxs-lookup"><span data-stu-id="2e1a7-121">Success.</span></span>

</dd> <dt>

<span data-ttu-id="2e1a7-122">**2**</span><span class="sxs-lookup"><span data-stu-id="2e1a7-122">**2**</span></span>
</dt> <dd>

<span data-ttu-id="2e1a7-123">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="2e1a7-123">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="2e1a7-124">**8**</span><span class="sxs-lookup"><span data-stu-id="2e1a7-124">**8**</span></span>
</dt> <dd>

<span data-ttu-id="2e1a7-125">Falha não especificada.</span><span class="sxs-lookup"><span data-stu-id="2e1a7-125">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="2e1a7-126">**9**</span><span class="sxs-lookup"><span data-stu-id="2e1a7-126">**9**</span></span>
</dt> <dd>

<span data-ttu-id="2e1a7-127">Objeto inválido.</span><span class="sxs-lookup"><span data-stu-id="2e1a7-127">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="2e1a7-128">**10**</span><span class="sxs-lookup"><span data-stu-id="2e1a7-128">**10**</span></span>
</dt> <dd>

<span data-ttu-id="2e1a7-129">O objeto já existe.</span><span class="sxs-lookup"><span data-stu-id="2e1a7-129">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="2e1a7-130">**11**</span><span class="sxs-lookup"><span data-stu-id="2e1a7-130">**11**</span></span>
</dt> <dd>

<span data-ttu-id="2e1a7-131">Sistema de arquivos não NTFS.</span><span class="sxs-lookup"><span data-stu-id="2e1a7-131">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="2e1a7-132">**12**</span><span class="sxs-lookup"><span data-stu-id="2e1a7-132">**12**</span></span>
</dt> <dd>

<span data-ttu-id="2e1a7-133">Plataforma não Windows.</span><span class="sxs-lookup"><span data-stu-id="2e1a7-133">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="2e1a7-134">**13**</span><span class="sxs-lookup"><span data-stu-id="2e1a7-134">**13**</span></span>
</dt> <dd>

<span data-ttu-id="2e1a7-135">A unidade não é a mesma.</span><span class="sxs-lookup"><span data-stu-id="2e1a7-135">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="2e1a7-136">**14**</span><span class="sxs-lookup"><span data-stu-id="2e1a7-136">**14**</span></span>
</dt> <dd>

<span data-ttu-id="2e1a7-137">O diretório não está vazio.</span><span class="sxs-lookup"><span data-stu-id="2e1a7-137">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="2e1a7-138">**15**</span><span class="sxs-lookup"><span data-stu-id="2e1a7-138">**15**</span></span>
</dt> <dd>

<span data-ttu-id="2e1a7-139">Violação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="2e1a7-139">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="2e1a7-140">**16**</span><span class="sxs-lookup"><span data-stu-id="2e1a7-140">**16**</span></span>
</dt> <dd>

<span data-ttu-id="2e1a7-141">Arquivo inicial inválido.</span><span class="sxs-lookup"><span data-stu-id="2e1a7-141">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="2e1a7-142">**17**</span><span class="sxs-lookup"><span data-stu-id="2e1a7-142">**17**</span></span>
</dt> <dd>

<span data-ttu-id="2e1a7-143">Privilégio não mantido.</span><span class="sxs-lookup"><span data-stu-id="2e1a7-143">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="2e1a7-144">**Abril**</span><span class="sxs-lookup"><span data-stu-id="2e1a7-144">**21**</span></span>
</dt> <dd>

<span data-ttu-id="2e1a7-145">Parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="2e1a7-145">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2e1a7-146">Comentários</span><span class="sxs-lookup"><span data-stu-id="2e1a7-146">Remarks</span></span>

<span data-ttu-id="2e1a7-147">O método **Rename** no [**\_ arquivo CIM**](cim-datafile.md) é implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="2e1a7-147">The **Rename** method in [**CIM\_DataFile**](cim-datafile.md) is implemented by WMI.</span></span>

<span data-ttu-id="2e1a7-148">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="2e1a7-148">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="2e1a7-149">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="2e1a7-149">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e1a7-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e1a7-150">Requirements</span></span>



| <span data-ttu-id="2e1a7-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e1a7-151">Requirement</span></span> | <span data-ttu-id="2e1a7-152">Valor</span><span class="sxs-lookup"><span data-stu-id="2e1a7-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2e1a7-153">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2e1a7-153">Minimum supported client</span></span><br/> | <span data-ttu-id="2e1a7-154">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2e1a7-154">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2e1a7-155">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2e1a7-155">Minimum supported server</span></span><br/> | <span data-ttu-id="2e1a7-156">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2e1a7-156">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2e1a7-157">Namespace</span><span class="sxs-lookup"><span data-stu-id="2e1a7-157">Namespace</span></span><br/>                | <span data-ttu-id="2e1a7-158">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="2e1a7-158">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2e1a7-159">MOF</span><span class="sxs-lookup"><span data-stu-id="2e1a7-159">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2e1a7-160"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2e1a7-160"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2e1a7-161">DLL</span><span class="sxs-lookup"><span data-stu-id="2e1a7-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e1a7-162"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e1a7-162"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e1a7-163">Confira também</span><span class="sxs-lookup"><span data-stu-id="2e1a7-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e1a7-164">DataFile de CIM \_</span><span class="sxs-lookup"><span data-stu-id="2e1a7-164">CIM\_DataFile</span></span>](rename-method-in-class-cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="2e1a7-165">**DataFile de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="2e1a7-165">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="2e1a7-166">Tarefas do WMI: arquivos e pastas</span><span class="sxs-lookup"><span data-stu-id="2e1a7-166">WMI Tasks: Files and Folders</span></span>](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[<span data-ttu-id="2e1a7-167">**Constantes de direitos de acesso de arquivo e diretório**</span><span class="sxs-lookup"><span data-stu-id="2e1a7-167">**File and Directory Access Rights Constants**</span></span>](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

