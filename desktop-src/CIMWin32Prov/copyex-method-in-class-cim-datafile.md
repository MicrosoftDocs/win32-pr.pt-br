---
description: O método CopyEx copia o arquivo lógico (ou diretório) que é especificado no caminho do objeto para o local especificado pelo parâmetro FileName.
ms.assetid: e52c1a0f-e34c-4a61-9e54-ed172976cb61
ms.tgt_platform: multiple
title: Método CopyEx da classe CIM_DataFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.CopyEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a83f1556aeeafbb5cc95eddbd84806bdaef0be14
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105762765"
---
# <a name="copyex-method-of-the-cim_datafile-class"></a><span data-ttu-id="02766-103">Método CopyEx da classe de \_ datafilefiles CIM</span><span class="sxs-lookup"><span data-stu-id="02766-103">CopyEx method of the CIM\_DataFile class</span></span>

<span data-ttu-id="02766-104">O método **CopyEx** copia o arquivo lógico (ou diretório) que é especificado no caminho do objeto para o local especificado pelo parâmetro *filename* .</span><span class="sxs-lookup"><span data-stu-id="02766-104">The **CopyEx** method copies the logical file (or directory) that is specified in the object path to the location specified by the *FileName* parameter.</span></span> <span data-ttu-id="02766-105">Não haverá suporte para uma cópia se ela exigir a substituição de um arquivo lógico existente.</span><span class="sxs-lookup"><span data-stu-id="02766-105">A copy is not supported if it requires overwriting an existing logical file.</span></span> <span data-ttu-id="02766-106">Esse método é uma versão estendida do método [**Copy**](copy-method-in-class-cim-datafile.md) e é herdado de [CIM \_ LogicalFile](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="02766-106">This method is an extended version of the [**Copy**](copy-method-in-class-cim-datafile.md) method and is inherited from [CIM\_LogicalFile](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="02766-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="02766-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="02766-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="02766-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="02766-109">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="02766-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="02766-110">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="02766-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="02766-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="02766-111">Syntax</span></span>


```mof
uint32 CopyEx(
  [in]  string     FileName,
  [out] string REF StopFileName,
  [in]  string     StartFileName,
  [in]  boolean    Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="02766-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="02766-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02766-113">*Nome do arquivo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="02766-113">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02766-114">Nome totalmente qualificado do arquivo de destino (ou diretório).</span><span class="sxs-lookup"><span data-stu-id="02766-114">Fully qualified name of the destination file (or directory).</span></span>

<span data-ttu-id="02766-115">Exemplo: "c: \\ temp \\ newdirectory"</span><span class="sxs-lookup"><span data-stu-id="02766-115">Example: "c:\\temp\\newdirectory"</span></span>

</dd> <dt>

<span data-ttu-id="02766-116">*StopFileName* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="02766-116">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="02766-117">Cadeia de caracteres que representa o nome do arquivo (ou diretório) em que o método falhou.</span><span class="sxs-lookup"><span data-stu-id="02766-117">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="02766-118">Esse parâmetro será **NULL** se o método tiver sucesso.</span><span class="sxs-lookup"><span data-stu-id="02766-118">This parameter will be **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="02766-119">*StartFileName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="02766-119">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02766-120">Cadeia de caracteres que representa o arquivo filho (ou diretório) a ser usado como ponto de partida para esse método.</span><span class="sxs-lookup"><span data-stu-id="02766-120">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="02766-121">Normalmente, o parâmetro *StartFileName* é o parâmetro *StopFileName* que especifica o arquivo (ou diretório) no qual ocorreu um erro da chamada de método anterior.</span><span class="sxs-lookup"><span data-stu-id="02766-121">Typically, the *StartFileName* parameter is the *StopFileName* parameter specifying the file (or directory) at which an error occurred from the previous method call.</span></span> <span data-ttu-id="02766-122">Se esse parâmetro for **nulo**, a operação será executada no arquivo (ou diretório) especificado na chamada de [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="02766-122">If this parameter is **null**, the operation is performed on the file (or directory) specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

<span data-ttu-id="02766-123">Se o *StartFileName* for usado, *recursivo* deverá ser definido como true também.</span><span class="sxs-lookup"><span data-stu-id="02766-123">If *StartFileName* is used, *Recursive* must be set to true as well.</span></span>

</dd> <dt>

<span data-ttu-id="02766-124">*Recursivo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="02766-124">*Recursive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02766-125">Se for TRUE, o método também será aplicado recursivamente a arquivos e diretórios dentro do diretório especificado pela instância de [**\_ arquivo**](cim-datafile.md) de arquivos CIM.</span><span class="sxs-lookup"><span data-stu-id="02766-125">If TRUE, the method is also applied recursively to files and directories within the directory specified by the [**CIM\_DataFile**](cim-datafile.md) instance.</span></span> <span data-ttu-id="02766-126">Para instâncias de arquivo, esse parâmetro é ignorado.</span><span class="sxs-lookup"><span data-stu-id="02766-126">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02766-127">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="02766-127">Return value</span></span>

<span data-ttu-id="02766-128">Retorna um valor de 0 (zero) em caso de êxito e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="02766-128">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span> <span data-ttu-id="02766-129">Para obter códigos de erro adicionais, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="02766-129">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="02766-130">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="02766-130">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="02766-131">0</span><span class="sxs-lookup"><span data-stu-id="02766-131">0</span></span>

<span data-ttu-id="02766-132">Sucesso.</span><span class="sxs-lookup"><span data-stu-id="02766-132">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="02766-133">2</span><span class="sxs-lookup"><span data-stu-id="02766-133">2</span></span>

<span data-ttu-id="02766-134">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="02766-134">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="02766-135">8</span><span class="sxs-lookup"><span data-stu-id="02766-135">8</span></span>

<span data-ttu-id="02766-136">Falha não especificada.</span><span class="sxs-lookup"><span data-stu-id="02766-136">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="02766-137">9</span><span class="sxs-lookup"><span data-stu-id="02766-137">9</span></span>

<span data-ttu-id="02766-138">Objeto inválido.</span><span class="sxs-lookup"><span data-stu-id="02766-138">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="02766-139">10</span><span class="sxs-lookup"><span data-stu-id="02766-139">10</span></span>

<span data-ttu-id="02766-140">O objeto já existe.</span><span class="sxs-lookup"><span data-stu-id="02766-140">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="02766-141">11</span><span class="sxs-lookup"><span data-stu-id="02766-141">11</span></span>

<span data-ttu-id="02766-142">Sistema de arquivos não NTFS.</span><span class="sxs-lookup"><span data-stu-id="02766-142">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="02766-143">12</span><span class="sxs-lookup"><span data-stu-id="02766-143">12</span></span>

<span data-ttu-id="02766-144">Plataforma não Windows.</span><span class="sxs-lookup"><span data-stu-id="02766-144">Platform not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="02766-145">13</span><span class="sxs-lookup"><span data-stu-id="02766-145">13</span></span>

<span data-ttu-id="02766-146">A unidade não é a mesma.</span><span class="sxs-lookup"><span data-stu-id="02766-146">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="02766-147">14</span><span class="sxs-lookup"><span data-stu-id="02766-147">14</span></span>

<span data-ttu-id="02766-148">O diretório não está vazio.</span><span class="sxs-lookup"><span data-stu-id="02766-148">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="02766-149">15</span><span class="sxs-lookup"><span data-stu-id="02766-149">15</span></span>

<span data-ttu-id="02766-150">Violação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="02766-150">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="02766-151">16</span><span class="sxs-lookup"><span data-stu-id="02766-151">16</span></span>

<span data-ttu-id="02766-152">Arquivo inicial inválido.</span><span class="sxs-lookup"><span data-stu-id="02766-152">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="02766-153">17</span><span class="sxs-lookup"><span data-stu-id="02766-153">17</span></span>

<span data-ttu-id="02766-154">Privilégio não mantido.</span><span class="sxs-lookup"><span data-stu-id="02766-154">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="02766-155">21</span><span class="sxs-lookup"><span data-stu-id="02766-155">21</span></span>

<span data-ttu-id="02766-156">Parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="02766-156">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="02766-157">Comentários</span><span class="sxs-lookup"><span data-stu-id="02766-157">Remarks</span></span>

<span data-ttu-id="02766-158">O método **CopyEx** no [**\_ arquivo CIM**](cim-datafile.md) é implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="02766-158">The **CopyEx** method in [**CIM\_DataFile**](cim-datafile.md) is implemented by WMI.</span></span>

<span data-ttu-id="02766-159">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="02766-159">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="02766-160">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="02766-160">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="02766-161">Requisitos</span><span class="sxs-lookup"><span data-stu-id="02766-161">Requirements</span></span>



| <span data-ttu-id="02766-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="02766-162">Requirement</span></span> | <span data-ttu-id="02766-163">Valor</span><span class="sxs-lookup"><span data-stu-id="02766-163">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="02766-164">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="02766-164">Minimum supported client</span></span><br/> | <span data-ttu-id="02766-165">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="02766-165">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="02766-166">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="02766-166">Minimum supported server</span></span><br/> | <span data-ttu-id="02766-167">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="02766-167">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="02766-168">Namespace</span><span class="sxs-lookup"><span data-stu-id="02766-168">Namespace</span></span><br/>                | <span data-ttu-id="02766-169">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="02766-169">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="02766-170">MOF</span><span class="sxs-lookup"><span data-stu-id="02766-170">MOF</span></span><br/>                      | <dl> <span data-ttu-id="02766-171"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="02766-171"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="02766-172">DLL</span><span class="sxs-lookup"><span data-stu-id="02766-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="02766-173"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="02766-173"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02766-174">Confira também</span><span class="sxs-lookup"><span data-stu-id="02766-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02766-175">**DataFile de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="02766-175">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="02766-176">Tarefas do WMI: arquivos e pastas</span><span class="sxs-lookup"><span data-stu-id="02766-176">WMI Tasks: Files and Folders</span></span>](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[<span data-ttu-id="02766-177">**Constantes de direitos de acesso de arquivo e diretório**</span><span class="sxs-lookup"><span data-stu-id="02766-177">**File and Directory Access Rights Constants**</span></span>](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

