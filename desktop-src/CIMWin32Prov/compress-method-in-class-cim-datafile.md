---
description: Método compress da classe CIM_DataFile – usa a compactação NTFS para compactar o arquivo lógico (ou diretório) que é especificado no caminho do objeto. Esse método é herdado do \_ LogicalFile CIM.
ms.assetid: fce57569-8290-420e-a938-10ab08ac67c3
ms.tgt_platform: multiple
title: Método compress da classe CIM_DataFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.Compress
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3cc63ed3cafd676a0d865953c52a14e6247d4b70
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089774"
---
# <a name="compress-method-of-the-cim_datafile-class"></a><span data-ttu-id="b6a26-104">Método compress da \_ classe datafilefiles CIM</span><span class="sxs-lookup"><span data-stu-id="b6a26-104">Compress method of the CIM\_DataFile class</span></span>

<span data-ttu-id="b6a26-105">O método **compress** usa a compactação NTFS para compactar o arquivo lógico (ou diretório) que é especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="b6a26-105">The **Compress** method uses NTFS compression to compress the logical file (or directory) that is specified in the object path.</span></span> <span data-ttu-id="b6a26-106">Esse método é herdado [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="b6a26-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b6a26-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="b6a26-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b6a26-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="b6a26-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="b6a26-109">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="b6a26-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="b6a26-110">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="b6a26-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="b6a26-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b6a26-111">Syntax</span></span>


```mof
uint32 Compress();
```



## <a name="parameters"></a><span data-ttu-id="b6a26-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b6a26-112">Parameters</span></span>

<span data-ttu-id="b6a26-113">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="b6a26-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b6a26-114">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="b6a26-114">Return value</span></span>

<span data-ttu-id="b6a26-115">Retorna um valor de 0 (zero) em caso de êxito e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="b6a26-115">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span> <span data-ttu-id="b6a26-116">Para obter códigos de erro adicionais, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="b6a26-116">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="b6a26-117">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="b6a26-117">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="b6a26-118">**0**</span><span class="sxs-lookup"><span data-stu-id="b6a26-118">**0**</span></span>
</dt> <dd>

<span data-ttu-id="b6a26-119">Sucesso.</span><span class="sxs-lookup"><span data-stu-id="b6a26-119">Success.</span></span>

</dd> <dt>

<span data-ttu-id="b6a26-120">**2**</span><span class="sxs-lookup"><span data-stu-id="b6a26-120">**2**</span></span>
</dt> <dd>

<span data-ttu-id="b6a26-121">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="b6a26-121">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="b6a26-122">**8**</span><span class="sxs-lookup"><span data-stu-id="b6a26-122">**8**</span></span>
</dt> <dd>

<span data-ttu-id="b6a26-123">Falha não especificada.</span><span class="sxs-lookup"><span data-stu-id="b6a26-123">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="b6a26-124">**9**</span><span class="sxs-lookup"><span data-stu-id="b6a26-124">**9**</span></span>
</dt> <dd>

<span data-ttu-id="b6a26-125">Objeto inválido.</span><span class="sxs-lookup"><span data-stu-id="b6a26-125">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="b6a26-126">**10**</span><span class="sxs-lookup"><span data-stu-id="b6a26-126">**10**</span></span>
</dt> <dd>

<span data-ttu-id="b6a26-127">O objeto já existe.</span><span class="sxs-lookup"><span data-stu-id="b6a26-127">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="b6a26-128">**11**</span><span class="sxs-lookup"><span data-stu-id="b6a26-128">**11**</span></span>
</dt> <dd>

<span data-ttu-id="b6a26-129">Sistema de arquivos não NTFS.</span><span class="sxs-lookup"><span data-stu-id="b6a26-129">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="b6a26-130">**12**</span><span class="sxs-lookup"><span data-stu-id="b6a26-130">**12**</span></span>
</dt> <dd>

<span data-ttu-id="b6a26-131">Plataforma não Windows.</span><span class="sxs-lookup"><span data-stu-id="b6a26-131">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="b6a26-132">**13**</span><span class="sxs-lookup"><span data-stu-id="b6a26-132">**13**</span></span>
</dt> <dd>

<span data-ttu-id="b6a26-133">A unidade não é a mesma.</span><span class="sxs-lookup"><span data-stu-id="b6a26-133">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="b6a26-134">**14**</span><span class="sxs-lookup"><span data-stu-id="b6a26-134">**14**</span></span>
</dt> <dd>

<span data-ttu-id="b6a26-135">O diretório não está vazio.</span><span class="sxs-lookup"><span data-stu-id="b6a26-135">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="b6a26-136">**15**</span><span class="sxs-lookup"><span data-stu-id="b6a26-136">**15**</span></span>
</dt> <dd>

<span data-ttu-id="b6a26-137">Violação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="b6a26-137">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="b6a26-138">**16**</span><span class="sxs-lookup"><span data-stu-id="b6a26-138">**16**</span></span>
</dt> <dd>

<span data-ttu-id="b6a26-139">Arquivo inicial inválido.</span><span class="sxs-lookup"><span data-stu-id="b6a26-139">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="b6a26-140">**17**</span><span class="sxs-lookup"><span data-stu-id="b6a26-140">**17**</span></span>
</dt> <dd>

<span data-ttu-id="b6a26-141">Privilégio não mantido.</span><span class="sxs-lookup"><span data-stu-id="b6a26-141">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="b6a26-142">**Abril**</span><span class="sxs-lookup"><span data-stu-id="b6a26-142">**21**</span></span>
</dt> <dd>

<span data-ttu-id="b6a26-143">Parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="b6a26-143">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b6a26-144">Comentários</span><span class="sxs-lookup"><span data-stu-id="b6a26-144">Remarks</span></span>

<span data-ttu-id="b6a26-145">O método **compress** no [**\_ arquivo CIM**](cim-datafile.md) é implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="b6a26-145">The **Compress** method in [**CIM\_DataFile**](cim-datafile.md) is implemented by WMI.</span></span>

<span data-ttu-id="b6a26-146">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="b6a26-146">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b6a26-147">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="b6a26-147">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6a26-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b6a26-148">Requirements</span></span>



| <span data-ttu-id="b6a26-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6a26-149">Requirement</span></span> | <span data-ttu-id="b6a26-150">Valor</span><span class="sxs-lookup"><span data-stu-id="b6a26-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b6a26-151">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b6a26-151">Minimum supported client</span></span><br/> | <span data-ttu-id="b6a26-152">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b6a26-152">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b6a26-153">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b6a26-153">Minimum supported server</span></span><br/> | <span data-ttu-id="b6a26-154">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b6a26-154">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b6a26-155">Namespace</span><span class="sxs-lookup"><span data-stu-id="b6a26-155">Namespace</span></span><br/>                | <span data-ttu-id="b6a26-156">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="b6a26-156">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b6a26-157">MOF</span><span class="sxs-lookup"><span data-stu-id="b6a26-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b6a26-158"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b6a26-158"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b6a26-159">DLL</span><span class="sxs-lookup"><span data-stu-id="b6a26-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b6a26-160"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b6a26-160"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6a26-161">Consulte também</span><span class="sxs-lookup"><span data-stu-id="b6a26-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6a26-162">**DataFile de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="b6a26-162">**CIM\_DataFile**</span></span>](compress-method-in-class-cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="b6a26-163">**DataFile de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="b6a26-163">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="b6a26-164">Tarefas do WMI: arquivos e pastas</span><span class="sxs-lookup"><span data-stu-id="b6a26-164">WMI Tasks: Files and Folders</span></span>](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[<span data-ttu-id="b6a26-165">**Constantes de direitos de acesso de arquivo e diretório**</span><span class="sxs-lookup"><span data-stu-id="b6a26-165">**File and Directory Access Rights Constants**</span></span>](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

