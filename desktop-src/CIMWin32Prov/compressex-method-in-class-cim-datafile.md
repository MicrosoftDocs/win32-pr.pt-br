---
description: Usa a compactação NTFS para compactar o arquivo lógico (ou diretório) que é especificado no caminho do objeto. Esse método é herdado do \_ LogicalFile CIM.
ms.assetid: 553b6a90-d16c-4abb-9015-66fe8e1606f6
ms.tgt_platform: multiple
title: Método CompressEx da classe CIM_DataFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.CompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 070a15a0fb134c92e7c436e071e09b7cc09fa5dc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104163936"
---
# <a name="compressex-method-of-the-cim_datafile-class"></a><span data-ttu-id="84117-104">Método CompressEx da classe de \_ datafilefiles CIM</span><span class="sxs-lookup"><span data-stu-id="84117-104">CompressEx method of the CIM\_DataFile class</span></span>

<span data-ttu-id="84117-105">O método **CompressEx** usa a compactação NTFS para compactar o arquivo lógico (ou diretório) que é especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="84117-105">The **CompressEx** method uses NTFS compression to compress the logical file (or directory) that is specified in the object path.</span></span> <span data-ttu-id="84117-106">Esse método é herdado [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="84117-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span> <span data-ttu-id="84117-107">Esse método é uma versão estendida do método [**compress**](compress-method-in-class-cim-datafile.md) e é herdado de [CIM \_ LogicalFile](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="84117-107">This method is an extended version of the [**Compress**](compress-method-in-class-cim-datafile.md) method and is inherited from [CIM\_LogicalFile](/windows/desktop/WmiSdk/calling-a-method).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="84117-108">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="84117-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="84117-109">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="84117-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="84117-110">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="84117-110">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="84117-111">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="84117-111">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="84117-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="84117-112">Syntax</span></span>


```mof
uint32 CompressEx(
  [out] string  StopFileName,
  [in]  string  StartFileName,
  [in]  boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="84117-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="84117-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84117-114">*StopFileName* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="84117-114">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="84117-115">Cadeia de caracteres que representa o nome do arquivo (ou diretório) em que o método falhou.</span><span class="sxs-lookup"><span data-stu-id="84117-115">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="84117-116">Esse parâmetro será nulo se o método tiver sucesso.</span><span class="sxs-lookup"><span data-stu-id="84117-116">This parameter is null if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="84117-117">*StartFileName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="84117-117">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84117-118">Cadeia de caracteres que representa o arquivo filho (ou diretório) a ser usado como ponto de partida para esse método.</span><span class="sxs-lookup"><span data-stu-id="84117-118">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="84117-119">Normalmente, o parâmetro *StartFileName* é o parâmetro *StopFileName* que especifica o arquivo ou diretório no qual ocorreu um erro da chamada de método anterior.</span><span class="sxs-lookup"><span data-stu-id="84117-119">Typically, the *StartFileName* parameter is the *StopFileName* parameter that specifies the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="84117-120">Se esse parâmetro for nulo, a operação será executada no arquivo ou diretório especificado na chamada de **ExecMethod** .</span><span class="sxs-lookup"><span data-stu-id="84117-120">If this parameter is null, the operation is performed on the file or directory specified in the **ExecMethod** call.</span></span>

<span data-ttu-id="84117-121">Se o *StartFileName* for usado, *recursivo* deverá ser definido como true também.</span><span class="sxs-lookup"><span data-stu-id="84117-121">If *StartFileName* is used, *Recursive* must be set to true as well.</span></span>

</dd> <dt>

<span data-ttu-id="84117-122">*Recursivo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="84117-122">*Recursive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84117-123">Se **for true**, o método também será aplicado recursivamente a arquivos e diretórios dentro do diretório especificado pela instância de [**\_ arquivo**](cim-datafile.md) de arquivos CIM.</span><span class="sxs-lookup"><span data-stu-id="84117-123">If **TRUE**, the method is also applied recursively to files and directories within the directory specified by the [**CIM\_DataFile**](cim-datafile.md) instance.</span></span> <span data-ttu-id="84117-124">Para instâncias de arquivo, esse parâmetro é ignorado.</span><span class="sxs-lookup"><span data-stu-id="84117-124">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84117-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="84117-125">Return value</span></span>

<span data-ttu-id="84117-126">Retorna um valor de 0 (zero) em caso de êxito e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="84117-126">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span> <span data-ttu-id="84117-127">Para obter códigos de erro adicionais, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="84117-127">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="84117-128">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="84117-128">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="84117-129">**0**</span><span class="sxs-lookup"><span data-stu-id="84117-129">**0**</span></span>
</dt> <dd>

<span data-ttu-id="84117-130">Êxito.</span><span class="sxs-lookup"><span data-stu-id="84117-130">Success.</span></span>

</dd> <dt>

<span data-ttu-id="84117-131">**2**</span><span class="sxs-lookup"><span data-stu-id="84117-131">**2**</span></span>
</dt> <dd>

<span data-ttu-id="84117-132">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="84117-132">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="84117-133">**8**</span><span class="sxs-lookup"><span data-stu-id="84117-133">**8**</span></span>
</dt> <dd>

<span data-ttu-id="84117-134">Falha não especificada.</span><span class="sxs-lookup"><span data-stu-id="84117-134">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="84117-135">**9**</span><span class="sxs-lookup"><span data-stu-id="84117-135">**9**</span></span>
</dt> <dd>

<span data-ttu-id="84117-136">Objeto inválido.</span><span class="sxs-lookup"><span data-stu-id="84117-136">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="84117-137">**10**</span><span class="sxs-lookup"><span data-stu-id="84117-137">**10**</span></span>
</dt> <dd>

<span data-ttu-id="84117-138">O objeto já existe.</span><span class="sxs-lookup"><span data-stu-id="84117-138">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="84117-139">**11**</span><span class="sxs-lookup"><span data-stu-id="84117-139">**11**</span></span>
</dt> <dd>

<span data-ttu-id="84117-140">Sistema de arquivos não NTFS.</span><span class="sxs-lookup"><span data-stu-id="84117-140">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="84117-141">**12**</span><span class="sxs-lookup"><span data-stu-id="84117-141">**12**</span></span>
</dt> <dd>

<span data-ttu-id="84117-142">Plataforma não Windows.</span><span class="sxs-lookup"><span data-stu-id="84117-142">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="84117-143">**13**</span><span class="sxs-lookup"><span data-stu-id="84117-143">**13**</span></span>
</dt> <dd>

<span data-ttu-id="84117-144">A unidade não é a mesma.</span><span class="sxs-lookup"><span data-stu-id="84117-144">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="84117-145">**14**</span><span class="sxs-lookup"><span data-stu-id="84117-145">**14**</span></span>
</dt> <dd>

<span data-ttu-id="84117-146">O diretório não está vazio.</span><span class="sxs-lookup"><span data-stu-id="84117-146">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="84117-147">**15**</span><span class="sxs-lookup"><span data-stu-id="84117-147">**15**</span></span>
</dt> <dd>

<span data-ttu-id="84117-148">Violação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="84117-148">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="84117-149">**16**</span><span class="sxs-lookup"><span data-stu-id="84117-149">**16**</span></span>
</dt> <dd>

<span data-ttu-id="84117-150">Arquivo inicial inválido.</span><span class="sxs-lookup"><span data-stu-id="84117-150">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="84117-151">**17**</span><span class="sxs-lookup"><span data-stu-id="84117-151">**17**</span></span>
</dt> <dd>

<span data-ttu-id="84117-152">Privilégio não mantido.</span><span class="sxs-lookup"><span data-stu-id="84117-152">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="84117-153">**Abril**</span><span class="sxs-lookup"><span data-stu-id="84117-153">**21**</span></span>
</dt> <dd>

<span data-ttu-id="84117-154">Parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="84117-154">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="84117-155">Comentários</span><span class="sxs-lookup"><span data-stu-id="84117-155">Remarks</span></span>

<span data-ttu-id="84117-156">O método **CompressEx** no [**\_ arquivo CIM**](cim-datafile.md) é implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="84117-156">The **CompressEx** method in [**CIM\_DataFile**](cim-datafile.md) is implemented by WMI.</span></span>

<span data-ttu-id="84117-157">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="84117-157">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="84117-158">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="84117-158">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="84117-159">Requisitos</span><span class="sxs-lookup"><span data-stu-id="84117-159">Requirements</span></span>



| <span data-ttu-id="84117-160">Requisito</span><span class="sxs-lookup"><span data-stu-id="84117-160">Requirement</span></span> | <span data-ttu-id="84117-161">Valor</span><span class="sxs-lookup"><span data-stu-id="84117-161">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="84117-162">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="84117-162">Minimum supported client</span></span><br/> | <span data-ttu-id="84117-163">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="84117-163">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="84117-164">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="84117-164">Minimum supported server</span></span><br/> | <span data-ttu-id="84117-165">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="84117-165">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="84117-166">Namespace</span><span class="sxs-lookup"><span data-stu-id="84117-166">Namespace</span></span><br/>                | <span data-ttu-id="84117-167">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="84117-167">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="84117-168">MOF</span><span class="sxs-lookup"><span data-stu-id="84117-168">MOF</span></span><br/>                      | <dl> <span data-ttu-id="84117-169"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="84117-169"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="84117-170">DLL</span><span class="sxs-lookup"><span data-stu-id="84117-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84117-171"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="84117-171"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84117-172">Confira também</span><span class="sxs-lookup"><span data-stu-id="84117-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84117-173">DataFile de CIM \_</span><span class="sxs-lookup"><span data-stu-id="84117-173">CIM\_DataFile</span></span>](compressex-method-in-class-cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="84117-174">**DataFile de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="84117-174">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="84117-175">Tarefas do WMI: arquivos e pastas</span><span class="sxs-lookup"><span data-stu-id="84117-175">WMI Tasks: Files and Folders</span></span>](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[<span data-ttu-id="84117-176">**Constantes de direitos de acesso de arquivo e diretório**</span><span class="sxs-lookup"><span data-stu-id="84117-176">**File and Directory Access Rights Constants**</span></span>](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

