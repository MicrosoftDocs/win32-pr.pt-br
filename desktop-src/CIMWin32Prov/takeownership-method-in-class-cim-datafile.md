---
description: O método TakeOwnerShip Obtém a propriedade do arquivo lógico especificado no caminho do objeto.
ms.assetid: 0835c335-0ada-44c1-9e71-44ba2041d8e2
ms.tgt_platform: multiple
title: Método TakeOwnerShip da classe CIM_DataFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.TakeOwnerShip
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1ade501db9b6af21b3761b70f638faa20d699401
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920360"
---
# <a name="takeownership-method-of-the-cim_datafile-class"></a><span data-ttu-id="a9fa0-103">Método TakeOwnerShip da classe de \_ datafilefiles CIM</span><span class="sxs-lookup"><span data-stu-id="a9fa0-103">TakeOwnerShip method of the CIM\_DataFile class</span></span>

<span data-ttu-id="a9fa0-104">O método **TakeOwnership** Obtém a propriedade do arquivo lógico especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-104">The **TakeOwnerShip** method obtains ownership of the logical file that is specified in the object path.</span></span> <span data-ttu-id="a9fa0-105">Se o arquivo lógico for um diretório, esse método agirá de forma recursiva, assumindo a propriedade de todos os arquivos e subdiretórios contidos no diretório.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-105">If the logical file is a directory, then this method will act recursively, taking ownership of all files and sub-directories that the directory contains.</span></span> <span data-ttu-id="a9fa0-106">Esse método é herdado [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="a9fa0-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a9fa0-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a9fa0-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="a9fa0-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a9fa0-109">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="a9fa0-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="a9fa0-110">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="a9fa0-110">For more information about using this method see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="a9fa0-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a9fa0-111">Syntax</span></span>


```mof
uint32 TakeOwnerShip();
```



## <a name="parameters"></a><span data-ttu-id="a9fa0-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a9fa0-112">Parameters</span></span>

<span data-ttu-id="a9fa0-113">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a9fa0-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a9fa0-114">Return value</span></span>

<span data-ttu-id="a9fa0-115">Retorna um valor 0 em caso de êxito e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-115">Returns a value of 0 on success, and any other number to indicate an error.</span></span> <span data-ttu-id="a9fa0-116">Para obter códigos de erro adicionais, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="a9fa0-116">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="a9fa0-117">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="a9fa0-117">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="a9fa0-118">**0**</span><span class="sxs-lookup"><span data-stu-id="a9fa0-118">**0**</span></span>
</dt> <dd>

<span data-ttu-id="a9fa0-119">Êxito.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-119">Success.</span></span>

</dd> <dt>

<span data-ttu-id="a9fa0-120">**2**</span><span class="sxs-lookup"><span data-stu-id="a9fa0-120">**2**</span></span>
</dt> <dd>

<span data-ttu-id="a9fa0-121">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-121">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="a9fa0-122">**8**</span><span class="sxs-lookup"><span data-stu-id="a9fa0-122">**8**</span></span>
</dt> <dd>

<span data-ttu-id="a9fa0-123">Falha não especificada.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-123">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="a9fa0-124">**9**</span><span class="sxs-lookup"><span data-stu-id="a9fa0-124">**9**</span></span>
</dt> <dd>

<span data-ttu-id="a9fa0-125">Objeto inválido.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-125">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="a9fa0-126">**10**</span><span class="sxs-lookup"><span data-stu-id="a9fa0-126">**10**</span></span>
</dt> <dd>

<span data-ttu-id="a9fa0-127">O objeto já existe.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-127">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="a9fa0-128">**11**</span><span class="sxs-lookup"><span data-stu-id="a9fa0-128">**11**</span></span>
</dt> <dd>

<span data-ttu-id="a9fa0-129">Sistema de arquivos não NTFS.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-129">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="a9fa0-130">**12**</span><span class="sxs-lookup"><span data-stu-id="a9fa0-130">**12**</span></span>
</dt> <dd>

<span data-ttu-id="a9fa0-131">Plataforma não Windows.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-131">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="a9fa0-132">**13**</span><span class="sxs-lookup"><span data-stu-id="a9fa0-132">**13**</span></span>
</dt> <dd>

<span data-ttu-id="a9fa0-133">A unidade não é a mesma.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-133">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="a9fa0-134">**14**</span><span class="sxs-lookup"><span data-stu-id="a9fa0-134">**14**</span></span>
</dt> <dd>

<span data-ttu-id="a9fa0-135">O diretório não está vazio.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-135">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="a9fa0-136">**15**</span><span class="sxs-lookup"><span data-stu-id="a9fa0-136">**15**</span></span>
</dt> <dd>

<span data-ttu-id="a9fa0-137">Violação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-137">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="a9fa0-138">**16**</span><span class="sxs-lookup"><span data-stu-id="a9fa0-138">**16**</span></span>
</dt> <dd>

<span data-ttu-id="a9fa0-139">Arquivo inicial inválido.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-139">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="a9fa0-140">**17**</span><span class="sxs-lookup"><span data-stu-id="a9fa0-140">**17**</span></span>
</dt> <dd>

<span data-ttu-id="a9fa0-141">Privilégio não mantido.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-141">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="a9fa0-142">**Abril**</span><span class="sxs-lookup"><span data-stu-id="a9fa0-142">**21**</span></span>
</dt> <dd>

<span data-ttu-id="a9fa0-143">Parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-143">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a9fa0-144">Comentários</span><span class="sxs-lookup"><span data-stu-id="a9fa0-144">Remarks</span></span>

<span data-ttu-id="a9fa0-145">O método **TakeOwnership** no [**\_ arquivo CIM**](cim-datafile.md) é implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-145">The **TakeOwnerShip** method in [**CIM\_DataFile**](cim-datafile.md) is implemented by WMI.</span></span>

<span data-ttu-id="a9fa0-146">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-146">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a9fa0-147">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-147">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9fa0-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a9fa0-148">Requirements</span></span>



| <span data-ttu-id="a9fa0-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9fa0-149">Requirement</span></span> | <span data-ttu-id="a9fa0-150">Valor</span><span class="sxs-lookup"><span data-stu-id="a9fa0-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a9fa0-151">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a9fa0-151">Minimum supported client</span></span><br/> | <span data-ttu-id="a9fa0-152">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a9fa0-152">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a9fa0-153">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a9fa0-153">Minimum supported server</span></span><br/> | <span data-ttu-id="a9fa0-154">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a9fa0-154">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a9fa0-155">Namespace</span><span class="sxs-lookup"><span data-stu-id="a9fa0-155">Namespace</span></span><br/>                | <span data-ttu-id="a9fa0-156">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="a9fa0-156">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a9fa0-157">MOF</span><span class="sxs-lookup"><span data-stu-id="a9fa0-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a9fa0-158"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a9fa0-158"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a9fa0-159">DLL</span><span class="sxs-lookup"><span data-stu-id="a9fa0-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a9fa0-160"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a9fa0-160"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9fa0-161">Confira também</span><span class="sxs-lookup"><span data-stu-id="a9fa0-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9fa0-162">DataFile de CIM \_</span><span class="sxs-lookup"><span data-stu-id="a9fa0-162">CIM\_DataFile</span></span>](takeownership-method-in-class-cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="a9fa0-163">**DataFile de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="a9fa0-163">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="a9fa0-164">Tarefas do WMI: arquivos e pastas</span><span class="sxs-lookup"><span data-stu-id="a9fa0-164">WMI Tasks: Files and Folders</span></span>](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[<span data-ttu-id="a9fa0-165">**Constantes de direitos de acesso de arquivo e diretório**</span><span class="sxs-lookup"><span data-stu-id="a9fa0-165">**File and Directory Access Rights Constants**</span></span>](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

