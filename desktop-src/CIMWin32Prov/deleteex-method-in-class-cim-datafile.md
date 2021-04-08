---
description: O método DeleteEx exclui o arquivo lógico (ou diretório) especificado no caminho do objeto. Esse método é uma versão estendida do método Delete e é herdado de CIM \_ LogicalFile.
ms.assetid: 565d604f-01e0-4cd4-b182-9750c58bae5f
ms.tgt_platform: multiple
title: Método DeleteEx da classe CIM_DataFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.DeleteEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9af120c76e4ab8c53c945bd13aa62a2295385ac2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089115"
---
# <a name="deleteex-method-of-the-cim_datafile-class"></a><span data-ttu-id="ff54d-104">Método DeleteEx da classe de \_ datafilefiles CIM</span><span class="sxs-lookup"><span data-stu-id="ff54d-104">DeleteEx method of the CIM\_DataFile class</span></span>

<span data-ttu-id="ff54d-105">O método **DeleteEx** exclui o arquivo lógico (ou diretório) especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="ff54d-105">The **DeleteEx** method deletes the logical file (or directory) that is specified in the object path.</span></span> <span data-ttu-id="ff54d-106">Esse método é uma versão estendida do método [**delete**](delete-method-in-class-cim-datafile.md) e é herdado de [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="ff54d-106">This method is an extended version of the [**Delete**](delete-method-in-class-cim-datafile.md) method and is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ff54d-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="ff54d-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="ff54d-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="ff54d-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="ff54d-109">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="ff54d-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="ff54d-110">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="ff54d-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="ff54d-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ff54d-111">Syntax</span></span>


```mof
uint32 DeleteEx(
  [out] string REF StopFileName,
  [in]  string     StartFileName
);
```



## <a name="parameters"></a><span data-ttu-id="ff54d-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ff54d-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff54d-113">*StopFileName* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ff54d-113">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ff54d-114">Cadeia de caracteres que representa o nome do arquivo (ou diretório) em que o método falhou.</span><span class="sxs-lookup"><span data-stu-id="ff54d-114">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="ff54d-115">Esse parâmetro será nulo se o método tiver sucesso.</span><span class="sxs-lookup"><span data-stu-id="ff54d-115">This parameter is null if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="ff54d-116">*StartFileName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ff54d-116">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff54d-117">Cadeia de caracteres que representa o arquivo filho (ou diretório) a ser usado como ponto de partida para esse método.</span><span class="sxs-lookup"><span data-stu-id="ff54d-117">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="ff54d-118">Normalmente, o parâmetro *StartFileName* é o parâmetro *StopFileName* que especifica o arquivo ou diretório no qual ocorreu um erro da chamada do método anterior.</span><span class="sxs-lookup"><span data-stu-id="ff54d-118">Typically, the *StartFileName* parameter is the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="ff54d-119">Se esse parâmetro for nulo, a operação será executada no arquivo (ou diretório) especificado na chamada de [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="ff54d-119">If this parameter is null, the operation is performed on the file (or directory) specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff54d-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ff54d-120">Return value</span></span>

<span data-ttu-id="ff54d-121">Retorna um valor de 0 (zero) em caso de êxito e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="ff54d-121">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span> <span data-ttu-id="ff54d-122">Para obter códigos de erro adicionais, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="ff54d-122">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="ff54d-123">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="ff54d-123">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="ff54d-124">0</span><span class="sxs-lookup"><span data-stu-id="ff54d-124">0</span></span>

<span data-ttu-id="ff54d-125">Sucesso.</span><span class="sxs-lookup"><span data-stu-id="ff54d-125">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="ff54d-126">2</span><span class="sxs-lookup"><span data-stu-id="ff54d-126">2</span></span>

<span data-ttu-id="ff54d-127">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="ff54d-127">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="ff54d-128">8</span><span class="sxs-lookup"><span data-stu-id="ff54d-128">8</span></span>

<span data-ttu-id="ff54d-129">Falha não especificada.</span><span class="sxs-lookup"><span data-stu-id="ff54d-129">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="ff54d-130">9</span><span class="sxs-lookup"><span data-stu-id="ff54d-130">9</span></span>

<span data-ttu-id="ff54d-131">Objeto inválido.</span><span class="sxs-lookup"><span data-stu-id="ff54d-131">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="ff54d-132">10</span><span class="sxs-lookup"><span data-stu-id="ff54d-132">10</span></span>

<span data-ttu-id="ff54d-133">O objeto já existe.</span><span class="sxs-lookup"><span data-stu-id="ff54d-133">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="ff54d-134">11</span><span class="sxs-lookup"><span data-stu-id="ff54d-134">11</span></span>

<span data-ttu-id="ff54d-135">Sistema de arquivos não NTFS.</span><span class="sxs-lookup"><span data-stu-id="ff54d-135">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="ff54d-136">12</span><span class="sxs-lookup"><span data-stu-id="ff54d-136">12</span></span>

<span data-ttu-id="ff54d-137">Plataforma não Windows.</span><span class="sxs-lookup"><span data-stu-id="ff54d-137">Platform not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="ff54d-138">13</span><span class="sxs-lookup"><span data-stu-id="ff54d-138">13</span></span>

<span data-ttu-id="ff54d-139">A unidade não é a mesma.</span><span class="sxs-lookup"><span data-stu-id="ff54d-139">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="ff54d-140">14</span><span class="sxs-lookup"><span data-stu-id="ff54d-140">14</span></span>

<span data-ttu-id="ff54d-141">O diretório não está vazio.</span><span class="sxs-lookup"><span data-stu-id="ff54d-141">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="ff54d-142">15</span><span class="sxs-lookup"><span data-stu-id="ff54d-142">15</span></span>

<span data-ttu-id="ff54d-143">Violação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="ff54d-143">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="ff54d-144">16</span><span class="sxs-lookup"><span data-stu-id="ff54d-144">16</span></span>

<span data-ttu-id="ff54d-145">Arquivo inicial inválido.</span><span class="sxs-lookup"><span data-stu-id="ff54d-145">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="ff54d-146">17</span><span class="sxs-lookup"><span data-stu-id="ff54d-146">17</span></span>

<span data-ttu-id="ff54d-147">Privilégio não mantido.</span><span class="sxs-lookup"><span data-stu-id="ff54d-147">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="ff54d-148">21</span><span class="sxs-lookup"><span data-stu-id="ff54d-148">21</span></span>

<span data-ttu-id="ff54d-149">Parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="ff54d-149">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ff54d-150">Comentários</span><span class="sxs-lookup"><span data-stu-id="ff54d-150">Remarks</span></span>

<span data-ttu-id="ff54d-151">O método **DeleteEx** no [**\_ arquivo CIM**](cim-datafile.md) é implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="ff54d-151">The **DeleteEx** method in [**CIM\_DataFile**](cim-datafile.md) is implemented by WMI.</span></span>

<span data-ttu-id="ff54d-152">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="ff54d-152">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="ff54d-153">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="ff54d-153">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff54d-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ff54d-154">Requirements</span></span>



| <span data-ttu-id="ff54d-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff54d-155">Requirement</span></span> | <span data-ttu-id="ff54d-156">Valor</span><span class="sxs-lookup"><span data-stu-id="ff54d-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ff54d-157">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ff54d-157">Minimum supported client</span></span><br/> | <span data-ttu-id="ff54d-158">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ff54d-158">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ff54d-159">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ff54d-159">Minimum supported server</span></span><br/> | <span data-ttu-id="ff54d-160">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ff54d-160">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ff54d-161">Namespace</span><span class="sxs-lookup"><span data-stu-id="ff54d-161">Namespace</span></span><br/>                | <span data-ttu-id="ff54d-162">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="ff54d-162">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ff54d-163">MOF</span><span class="sxs-lookup"><span data-stu-id="ff54d-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ff54d-164"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ff54d-164"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ff54d-165">DLL</span><span class="sxs-lookup"><span data-stu-id="ff54d-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ff54d-166"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ff54d-166"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff54d-167">Confira também</span><span class="sxs-lookup"><span data-stu-id="ff54d-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff54d-168">DataFile de CIM \_</span><span class="sxs-lookup"><span data-stu-id="ff54d-168">CIM\_DataFile</span></span>](deleteex-method-in-class-cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="ff54d-169">**DataFile de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="ff54d-169">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="ff54d-170">Tarefas do WMI: arquivos e pastas</span><span class="sxs-lookup"><span data-stu-id="ff54d-170">WMI Tasks: Files and Folders</span></span>](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[<span data-ttu-id="ff54d-171">**Constantes de direitos de acesso de arquivo e diretório**</span><span class="sxs-lookup"><span data-stu-id="ff54d-171">**File and Directory Access Rights Constants**</span></span>](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

