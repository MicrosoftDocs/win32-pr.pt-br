---
description: Descompacta o arquivo de dados lógicos (ou diretório) especificado no caminho do objeto. Esse método é uma versão estendida do método uncompact e é herdado de CIM \_ LogicalFile.
ms.assetid: 30b62930-1d4a-47c0-8b57-b460edb5dbd0
ms.tgt_platform: multiple
title: Método UncompressEx da classe CIM_DataFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.UncompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0d11585a834ecc357447394ce09b73698bf2de86
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089551"
---
# <a name="uncompressex-method-of-the-cim_datafile-class"></a><span data-ttu-id="e41d6-104">Método UncompressEx da classe de \_ datafilefiles CIM</span><span class="sxs-lookup"><span data-stu-id="e41d6-104">UncompressEx method of the CIM\_DataFile class</span></span>

<span data-ttu-id="e41d6-105">O método **UncompressEx** descompacta o arquivo de dados lógicos (ou diretório) especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="e41d6-105">The **UncompressEx** method uncompresses the logical data file (or directory) that is specified in the object path.</span></span> <span data-ttu-id="e41d6-106">Esse método é uma versão estendida do método [**uncompact**](uncompress-method-in-class-cim-datafile.md) e é herdado de [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="e41d6-106">This method is an extended version of the [**Uncompress**](uncompress-method-in-class-cim-datafile.md) method and is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e41d6-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="e41d6-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e41d6-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="e41d6-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="e41d6-109">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="e41d6-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="e41d6-110">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="e41d6-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="e41d6-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e41d6-111">Syntax</span></span>


```mof
uint32 UncompressEx(
  [out] string  StopFileName,
  [in]  string  StartFileName,
  [in]  boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="e41d6-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e41d6-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e41d6-113">*StopFileName* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e41d6-113">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e41d6-114">Nome do arquivo (ou diretório) em que o método falhou.</span><span class="sxs-lookup"><span data-stu-id="e41d6-114">Name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="e41d6-115">Esse parâmetro será **nulo** se o método tiver sucesso.</span><span class="sxs-lookup"><span data-stu-id="e41d6-115">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="e41d6-116">*StartFileName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e41d6-116">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e41d6-117">Arquivo filho (ou diretório) a ser usado como ponto de partida para este método.</span><span class="sxs-lookup"><span data-stu-id="e41d6-117">Child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="e41d6-118">Normalmente, o parâmetro *StartFileName* é o parâmetro *StopFileName* que especifica o arquivo (ou diretório) no qual ocorreu um erro da chamada de método anterior.</span><span class="sxs-lookup"><span data-stu-id="e41d6-118">Typically, the *StartFileName* parameter is the *StopFileName* parameter specifying the file (or directory) at which an error occurred from the previous method call.</span></span> <span data-ttu-id="e41d6-119">Se esse parâmetro for **nulo**, a operação será executada no arquivo (ou diretório) especificado na chamada de [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="e41d6-119">If this parameter is **null**, the operation is performed on the file (or directory) specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

<span data-ttu-id="e41d6-120">Se o *StartFileName* for usado, *recursivo* deverá ser definido como true também.</span><span class="sxs-lookup"><span data-stu-id="e41d6-120">If *StartFileName* is used, *Recursive* must be set to true as well.</span></span>

</dd> <dt>

<span data-ttu-id="e41d6-121">*Recursivo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e41d6-121">*Recursive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e41d6-122">Se **for true**, o método também será aplicado recursivamente a arquivos e diretórios dentro do diretório especificado pela instância de [**\_ DataFile do CIM**](cim-datafile.md) .</span><span class="sxs-lookup"><span data-stu-id="e41d6-122">If **TRUE**, the method is also applied recursively to files and directories within the directory that is specified by the [**CIM\_DataFile**](cim-datafile.md) instance.</span></span> <span data-ttu-id="e41d6-123">Para instâncias de arquivo, esse parâmetro é ignorado.</span><span class="sxs-lookup"><span data-stu-id="e41d6-123">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e41d6-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e41d6-124">Return value</span></span>

<span data-ttu-id="e41d6-125">Retorna um valor de 0 (zero) em caso de êxito e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="e41d6-125">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span> <span data-ttu-id="e41d6-126">Para obter códigos de erro adicionais, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="e41d6-126">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="e41d6-127">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="e41d6-127">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="e41d6-128">**0**</span><span class="sxs-lookup"><span data-stu-id="e41d6-128">**0**</span></span>
</dt> <dd>

<span data-ttu-id="e41d6-129">Êxito.</span><span class="sxs-lookup"><span data-stu-id="e41d6-129">Success.</span></span>

</dd> <dt>

<span data-ttu-id="e41d6-130">**2**</span><span class="sxs-lookup"><span data-stu-id="e41d6-130">**2**</span></span>
</dt> <dd>

<span data-ttu-id="e41d6-131">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="e41d6-131">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="e41d6-132">**8**</span><span class="sxs-lookup"><span data-stu-id="e41d6-132">**8**</span></span>
</dt> <dd>

<span data-ttu-id="e41d6-133">Falha não especificada.</span><span class="sxs-lookup"><span data-stu-id="e41d6-133">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="e41d6-134">**9**</span><span class="sxs-lookup"><span data-stu-id="e41d6-134">**9**</span></span>
</dt> <dd>

<span data-ttu-id="e41d6-135">Objeto inválido.</span><span class="sxs-lookup"><span data-stu-id="e41d6-135">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="e41d6-136">**10**</span><span class="sxs-lookup"><span data-stu-id="e41d6-136">**10**</span></span>
</dt> <dd>

<span data-ttu-id="e41d6-137">O objeto já existe.</span><span class="sxs-lookup"><span data-stu-id="e41d6-137">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="e41d6-138">**11**</span><span class="sxs-lookup"><span data-stu-id="e41d6-138">**11**</span></span>
</dt> <dd>

<span data-ttu-id="e41d6-139">Sistema de arquivos não NTFS.</span><span class="sxs-lookup"><span data-stu-id="e41d6-139">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="e41d6-140">**12**</span><span class="sxs-lookup"><span data-stu-id="e41d6-140">**12**</span></span>
</dt> <dd>

<span data-ttu-id="e41d6-141">Plataforma não Windows.</span><span class="sxs-lookup"><span data-stu-id="e41d6-141">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="e41d6-142">**13**</span><span class="sxs-lookup"><span data-stu-id="e41d6-142">**13**</span></span>
</dt> <dd>

<span data-ttu-id="e41d6-143">A unidade não é a mesma.</span><span class="sxs-lookup"><span data-stu-id="e41d6-143">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="e41d6-144">**14**</span><span class="sxs-lookup"><span data-stu-id="e41d6-144">**14**</span></span>
</dt> <dd>

<span data-ttu-id="e41d6-145">O diretório não está vazio.</span><span class="sxs-lookup"><span data-stu-id="e41d6-145">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="e41d6-146">**15**</span><span class="sxs-lookup"><span data-stu-id="e41d6-146">**15**</span></span>
</dt> <dd>

<span data-ttu-id="e41d6-147">Violação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="e41d6-147">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="e41d6-148">**16**</span><span class="sxs-lookup"><span data-stu-id="e41d6-148">**16**</span></span>
</dt> <dd>

<span data-ttu-id="e41d6-149">Arquivo inicial inválido.</span><span class="sxs-lookup"><span data-stu-id="e41d6-149">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="e41d6-150">**17**</span><span class="sxs-lookup"><span data-stu-id="e41d6-150">**17**</span></span>
</dt> <dd>

<span data-ttu-id="e41d6-151">Privilégio não mantido.</span><span class="sxs-lookup"><span data-stu-id="e41d6-151">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="e41d6-152">**Abril**</span><span class="sxs-lookup"><span data-stu-id="e41d6-152">**21**</span></span>
</dt> <dd>

<span data-ttu-id="e41d6-153">Parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="e41d6-153">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e41d6-154">Comentários</span><span class="sxs-lookup"><span data-stu-id="e41d6-154">Remarks</span></span>

<span data-ttu-id="e41d6-155">O método **UncompressEx** no [**\_ arquivo CIM**](cim-datafile.md) é implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="e41d6-155">The **UncompressEx** method in [**CIM\_DataFile**](cim-datafile.md) is implemented by WMI.</span></span>

<span data-ttu-id="e41d6-156">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="e41d6-156">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e41d6-157">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="e41d6-157">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e41d6-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e41d6-158">Requirements</span></span>



| <span data-ttu-id="e41d6-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="e41d6-159">Requirement</span></span> | <span data-ttu-id="e41d6-160">Valor</span><span class="sxs-lookup"><span data-stu-id="e41d6-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e41d6-161">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e41d6-161">Minimum supported client</span></span><br/> | <span data-ttu-id="e41d6-162">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e41d6-162">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e41d6-163">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e41d6-163">Minimum supported server</span></span><br/> | <span data-ttu-id="e41d6-164">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e41d6-164">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e41d6-165">Namespace</span><span class="sxs-lookup"><span data-stu-id="e41d6-165">Namespace</span></span><br/>                | <span data-ttu-id="e41d6-166">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="e41d6-166">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e41d6-167">MOF</span><span class="sxs-lookup"><span data-stu-id="e41d6-167">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e41d6-168"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e41d6-168"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e41d6-169">DLL</span><span class="sxs-lookup"><span data-stu-id="e41d6-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e41d6-170"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e41d6-170"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e41d6-171">Confira também</span><span class="sxs-lookup"><span data-stu-id="e41d6-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e41d6-172">**DataFile de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="e41d6-172">**CIM\_DataFile**</span></span>](uncompressex-method-in-class-cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="e41d6-173">**DataFile de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="e41d6-173">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="e41d6-174">Tarefas do WMI: arquivos e pastas</span><span class="sxs-lookup"><span data-stu-id="e41d6-174">WMI Tasks: Files and Folders</span></span>](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[<span data-ttu-id="e41d6-175">**Constantes de direitos de acesso de arquivo e diretório**</span><span class="sxs-lookup"><span data-stu-id="e41d6-175">**File and Directory Access Rights Constants**</span></span>](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

