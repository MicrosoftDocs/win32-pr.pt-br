---
description: Copia o arquivo lógico (ou diretório) especificado no caminho do objeto para o local especificado pelo parâmetro FileName.
ms.assetid: 534d8b73-fc22-4a42-b8e6-24a54353bb14
ms.tgt_platform: multiple
title: Método CopyEx da classe CIM_LogicalFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.CopyEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: ec7c44ec3fc01074a0f4af70249236aa366d64bf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749319"
---
# <a name="copyex-method-of-the-cim_logicalfile-class"></a><span data-ttu-id="c7d15-103">Método CopyEx da classe de \_ LogicalFile CIM</span><span class="sxs-lookup"><span data-stu-id="c7d15-103">CopyEx method of the CIM\_LogicalFile class</span></span>

<span data-ttu-id="c7d15-104">O método **CopyEx** copia o arquivo lógico (ou diretório) especificado no caminho do objeto para o local especificado pelo parâmetro *filename* .</span><span class="sxs-lookup"><span data-stu-id="c7d15-104">The **CopyEx** method copies the logical file (or directory) specified in the object path to the location specified by the *FileName* parameter.</span></span> <span data-ttu-id="c7d15-105">Não haverá suporte para uma cópia se a substituição de um arquivo lógico existente for necessária.</span><span class="sxs-lookup"><span data-stu-id="c7d15-105">A copy is not supported if overwriting an existing logical file is required.</span></span> <span data-ttu-id="c7d15-106">Esse método é uma versão estendida do método [**Copy**](copy-method-in-class-cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="c7d15-106">This method is an extended version of the [**Copy**](copy-method-in-class-cim-logicalfile.md) method.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c7d15-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="c7d15-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="c7d15-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="c7d15-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="c7d15-109">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="c7d15-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="c7d15-110">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="c7d15-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="c7d15-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c7d15-111">Syntax</span></span>


```mof
uint32 CopyEx(
  [in]           string  FileName,
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="c7d15-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c7d15-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7d15-113">*Nome do arquivo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c7d15-113">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7d15-114">Nome totalmente qualificado do arquivo de destino (ou diretório).</span><span class="sxs-lookup"><span data-stu-id="c7d15-114">Fully qualified name of the destination file (or directory).</span></span>

<span data-ttu-id="c7d15-115">Exemplo: "c: \\ temp \\ newdirectory"</span><span class="sxs-lookup"><span data-stu-id="c7d15-115">Example: "c:\\temp\\newdirectory"</span></span>

</dd> <dt>

<span data-ttu-id="c7d15-116">*StopFileName* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="c7d15-116">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c7d15-117">Cadeia de caracteres que representa o nome do arquivo (ou diretório) em que o método falhou.</span><span class="sxs-lookup"><span data-stu-id="c7d15-117">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="c7d15-118">Esse parâmetro será **nulo** se o método tiver sucesso.</span><span class="sxs-lookup"><span data-stu-id="c7d15-118">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="c7d15-119">*StartFileName* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="c7d15-119">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c7d15-120">Cadeia de caracteres que nomeia o arquivo filho (ou diretório) a ser usado como ponto de partida para esse método.</span><span class="sxs-lookup"><span data-stu-id="c7d15-120">String that names the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="c7d15-121">Normalmente, o parâmetro *StartFileName* é o parâmetro *StopFileName* que especifica o arquivo (ou diretório) no qual ocorreu um erro da chamada de método anterior.</span><span class="sxs-lookup"><span data-stu-id="c7d15-121">Typically, the *StartFileName* parameter is the *StopFileName* parameter specifying the file (or directory) at which an error occurred from the previous method call.</span></span> <span data-ttu-id="c7d15-122">Se esse parâmetro for **nulo**, a operação será executada no arquivo ou diretório especificado na chamada de [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="c7d15-122">If this parameter is **null**, the operation is performed on the file or directory specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="c7d15-123">*Recursivo* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="c7d15-123">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c7d15-124">Se for TRUE, o método também será aplicado recursivamente a arquivos e diretórios dentro do diretório especificado pela instância de [**\_ LogicalFile do CIM**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="c7d15-124">If TRUE, the method is also applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span> <span data-ttu-id="c7d15-125">Para instâncias de arquivo, esse parâmetro é ignorado.</span><span class="sxs-lookup"><span data-stu-id="c7d15-125">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7d15-126">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c7d15-126">Return value</span></span>

<span data-ttu-id="c7d15-127">Retorna um valor de 0 (zero) em caso de êxito e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="c7d15-127">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="c7d15-128">**Êxito**</span><span class="sxs-lookup"><span data-stu-id="c7d15-128">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="c7d15-129">0</span><span class="sxs-lookup"><span data-stu-id="c7d15-129">0</span></span>

<span data-ttu-id="c7d15-130">Sucesso.</span><span class="sxs-lookup"><span data-stu-id="c7d15-130">Success.</span></span>

</dd> <dt>

<span data-ttu-id="c7d15-131">**Acesso negado**</span><span class="sxs-lookup"><span data-stu-id="c7d15-131">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="c7d15-132">2</span><span class="sxs-lookup"><span data-stu-id="c7d15-132">2</span></span>

<span data-ttu-id="c7d15-133">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="c7d15-133">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="c7d15-134">**Falha não especificada**</span><span class="sxs-lookup"><span data-stu-id="c7d15-134">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="c7d15-135">8</span><span class="sxs-lookup"><span data-stu-id="c7d15-135">8</span></span>

<span data-ttu-id="c7d15-136">Falha não especificada.</span><span class="sxs-lookup"><span data-stu-id="c7d15-136">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="c7d15-137">**Objeto inválido**</span><span class="sxs-lookup"><span data-stu-id="c7d15-137">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="c7d15-138">9</span><span class="sxs-lookup"><span data-stu-id="c7d15-138">9</span></span>

<span data-ttu-id="c7d15-139">Objeto inválido.</span><span class="sxs-lookup"><span data-stu-id="c7d15-139">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="c7d15-140">**O objeto já existe**</span><span class="sxs-lookup"><span data-stu-id="c7d15-140">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="c7d15-141">10</span><span class="sxs-lookup"><span data-stu-id="c7d15-141">10</span></span>

<span data-ttu-id="c7d15-142">O objeto já existe.</span><span class="sxs-lookup"><span data-stu-id="c7d15-142">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="c7d15-143">**Sistema de arquivos não NTFS**</span><span class="sxs-lookup"><span data-stu-id="c7d15-143">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="c7d15-144">11</span><span class="sxs-lookup"><span data-stu-id="c7d15-144">11</span></span>

<span data-ttu-id="c7d15-145">Sistema de arquivos não NTFS.</span><span class="sxs-lookup"><span data-stu-id="c7d15-145">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="c7d15-146">**Plataforma não NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="c7d15-146">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="c7d15-147">12</span><span class="sxs-lookup"><span data-stu-id="c7d15-147">12</span></span>

<span data-ttu-id="c7d15-148">Plataforma não Windows.</span><span class="sxs-lookup"><span data-stu-id="c7d15-148">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="c7d15-149">**A unidade não é a mesma**</span><span class="sxs-lookup"><span data-stu-id="c7d15-149">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="c7d15-150">13</span><span class="sxs-lookup"><span data-stu-id="c7d15-150">13</span></span>

<span data-ttu-id="c7d15-151">A unidade não é a mesma.</span><span class="sxs-lookup"><span data-stu-id="c7d15-151">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="c7d15-152">**Diretório não vazio**</span><span class="sxs-lookup"><span data-stu-id="c7d15-152">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="c7d15-153">14</span><span class="sxs-lookup"><span data-stu-id="c7d15-153">14</span></span>

<span data-ttu-id="c7d15-154">O diretório não está vazio.</span><span class="sxs-lookup"><span data-stu-id="c7d15-154">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="c7d15-155">**Violação de compartilhamento**</span><span class="sxs-lookup"><span data-stu-id="c7d15-155">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="c7d15-156">15</span><span class="sxs-lookup"><span data-stu-id="c7d15-156">15</span></span>

<span data-ttu-id="c7d15-157">Violação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="c7d15-157">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="c7d15-158">**Arquivo de início inválido**</span><span class="sxs-lookup"><span data-stu-id="c7d15-158">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="c7d15-159">16</span><span class="sxs-lookup"><span data-stu-id="c7d15-159">16</span></span>

<span data-ttu-id="c7d15-160">Arquivo inicial inválido.</span><span class="sxs-lookup"><span data-stu-id="c7d15-160">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="c7d15-161">**Privilégio não mantido**</span><span class="sxs-lookup"><span data-stu-id="c7d15-161">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="c7d15-162">17</span><span class="sxs-lookup"><span data-stu-id="c7d15-162">17</span></span>

<span data-ttu-id="c7d15-163">Privilégio não mantido.</span><span class="sxs-lookup"><span data-stu-id="c7d15-163">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="c7d15-164">**Parâmetro inválido**</span><span class="sxs-lookup"><span data-stu-id="c7d15-164">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="c7d15-165">21</span><span class="sxs-lookup"><span data-stu-id="c7d15-165">21</span></span>

<span data-ttu-id="c7d15-166">Parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="c7d15-166">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c7d15-167">Comentários</span><span class="sxs-lookup"><span data-stu-id="c7d15-167">Remarks</span></span>

<span data-ttu-id="c7d15-168">Este método não está implementado no momento pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="c7d15-168">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="c7d15-169">Para usar esse método, você deve implementá-lo em seu próprio provedor.</span><span class="sxs-lookup"><span data-stu-id="c7d15-169">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="c7d15-170">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="c7d15-170">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="c7d15-171">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="c7d15-171">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7d15-172">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c7d15-172">Requirements</span></span>



| <span data-ttu-id="c7d15-173">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7d15-173">Requirement</span></span> | <span data-ttu-id="c7d15-174">Valor</span><span class="sxs-lookup"><span data-stu-id="c7d15-174">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c7d15-175">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c7d15-175">Minimum supported client</span></span><br/> | <span data-ttu-id="c7d15-176">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c7d15-176">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c7d15-177">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c7d15-177">Minimum supported server</span></span><br/> | <span data-ttu-id="c7d15-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c7d15-178">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c7d15-179">Namespace</span><span class="sxs-lookup"><span data-stu-id="c7d15-179">Namespace</span></span><br/>                | <span data-ttu-id="c7d15-180">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="c7d15-180">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c7d15-181">MOF</span><span class="sxs-lookup"><span data-stu-id="c7d15-181">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c7d15-182"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c7d15-182"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c7d15-183">DLL</span><span class="sxs-lookup"><span data-stu-id="c7d15-183">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7d15-184"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7d15-184"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7d15-185">Confira também</span><span class="sxs-lookup"><span data-stu-id="c7d15-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7d15-186">CIM \_ LogicalFile</span><span class="sxs-lookup"><span data-stu-id="c7d15-186">CIM\_LogicalFile</span></span>](copyex-method-in-class-cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="c7d15-187">**CIM \_ LogicalFile**</span><span class="sxs-lookup"><span data-stu-id="c7d15-187">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

