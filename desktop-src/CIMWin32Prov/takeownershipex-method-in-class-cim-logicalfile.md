---
description: Obtém a propriedade do arquivo lógico especificado no caminho do objeto. Esse método é uma versão estendida do método TakeOwnerShip.
ms.assetid: c01ab071-86e4-484d-aaed-4783b6c3bebf
ms.tgt_platform: multiple
title: Método TakeOwnerShipEx da classe CIM_LogicalFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.TakeOwnerShipEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2e7f08413440ec32037554476ced386c56827239
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105755190"
---
# <a name="takeownershipex-method-of-the-cim_logicalfile-class"></a><span data-ttu-id="515cf-104">Método TakeOwnerShipEx da classe de \_ LogicalFile CIM</span><span class="sxs-lookup"><span data-stu-id="515cf-104">TakeOwnerShipEx method of the CIM\_LogicalFile class</span></span>

<span data-ttu-id="515cf-105">O método **TakeOwnerShipEx** Obtém a propriedade do arquivo lógico especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="515cf-105">The **TakeOwnerShipEx** method obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="515cf-106">Esse método é uma versão estendida do método [**TakeOwnership**](takeownership-method-in-class-cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="515cf-106">This method is an extended version of the [**TakeOwnerShip**](takeownership-method-in-class-cim-logicalfile.md) method.</span></span> <span data-ttu-id="515cf-107">Se o arquivo lógico for um diretório, esse método agirá recursivamente, assumindo a propriedade de todos os arquivos e subdiretórios contidos no diretório.</span><span class="sxs-lookup"><span data-stu-id="515cf-107">If the logical file is a directory, then this method acts recursively, taking ownership of all files and sub-directories that the directory contains.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="515cf-108">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="515cf-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="515cf-109">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="515cf-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="515cf-110">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="515cf-110">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="515cf-111">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="515cf-111">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="515cf-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="515cf-112">Syntax</span></span>


```mof
uint32 TakeOwnerShipEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="515cf-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="515cf-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="515cf-114">*StopFileName* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="515cf-114">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="515cf-115">Cadeia de caracteres que representa o nome do arquivo (ou diretório) em que o método falhou.</span><span class="sxs-lookup"><span data-stu-id="515cf-115">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="515cf-116">Esse parâmetro será **nulo** se o método tiver sucesso.</span><span class="sxs-lookup"><span data-stu-id="515cf-116">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="515cf-117">*StartFileName* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="515cf-117">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="515cf-118">Cadeia de caracteres que nomeia o arquivo filho (ou diretório) a ser usado como ponto de partida para o método.</span><span class="sxs-lookup"><span data-stu-id="515cf-118">String that names the child file (or directory) to use as a starting point for the method.</span></span> <span data-ttu-id="515cf-119">Normalmente, esse parâmetro é o parâmetro *StopFileName* que especifica o arquivo ou diretório no qual ocorreu um erro da chamada do método anterior.</span><span class="sxs-lookup"><span data-stu-id="515cf-119">Typically, this parameter is the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="515cf-120">Se esse parâmetro for **nulo**, a operação será executada no arquivo (ou diretório) especificado na chamada de [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="515cf-120">If this parameter is **null**, the operation is performed on the file (or directory) specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="515cf-121">*Recursivo* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="515cf-121">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="515cf-122">Se **for true**, o método também será aplicado recursivamente a arquivos e diretórios dentro do diretório especificado pela instância de [**\_ LogicalFile do CIM**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="515cf-122">If **TRUE**, the method is also applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span> <span data-ttu-id="515cf-123">Para instâncias de arquivo, esse parâmetro é ignorado.</span><span class="sxs-lookup"><span data-stu-id="515cf-123">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="515cf-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="515cf-124">Return value</span></span>

<span data-ttu-id="515cf-125">Retorna um valor de 0 (zero) em caso de êxito e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="515cf-125">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="515cf-126">**Êxito**</span><span class="sxs-lookup"><span data-stu-id="515cf-126">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="515cf-127">0</span><span class="sxs-lookup"><span data-stu-id="515cf-127">0</span></span>

<span data-ttu-id="515cf-128">Sucesso.</span><span class="sxs-lookup"><span data-stu-id="515cf-128">Success.</span></span>

</dd> <dt>

<span data-ttu-id="515cf-129">**Acesso negado**</span><span class="sxs-lookup"><span data-stu-id="515cf-129">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="515cf-130">2</span><span class="sxs-lookup"><span data-stu-id="515cf-130">2</span></span>

<span data-ttu-id="515cf-131">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="515cf-131">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="515cf-132">**Falha não especificada**</span><span class="sxs-lookup"><span data-stu-id="515cf-132">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="515cf-133">8</span><span class="sxs-lookup"><span data-stu-id="515cf-133">8</span></span>

<span data-ttu-id="515cf-134">Falha não especificada.</span><span class="sxs-lookup"><span data-stu-id="515cf-134">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="515cf-135">**Objeto inválido**</span><span class="sxs-lookup"><span data-stu-id="515cf-135">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="515cf-136">9</span><span class="sxs-lookup"><span data-stu-id="515cf-136">9</span></span>

<span data-ttu-id="515cf-137">Objeto inválido.</span><span class="sxs-lookup"><span data-stu-id="515cf-137">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="515cf-138">**O objeto já existe**</span><span class="sxs-lookup"><span data-stu-id="515cf-138">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="515cf-139">10</span><span class="sxs-lookup"><span data-stu-id="515cf-139">10</span></span>

<span data-ttu-id="515cf-140">O objeto já existe.</span><span class="sxs-lookup"><span data-stu-id="515cf-140">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="515cf-141">**Sistema de arquivos não NTFS**</span><span class="sxs-lookup"><span data-stu-id="515cf-141">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="515cf-142">11</span><span class="sxs-lookup"><span data-stu-id="515cf-142">11</span></span>

<span data-ttu-id="515cf-143">Sistema de arquivos não NTFS.</span><span class="sxs-lookup"><span data-stu-id="515cf-143">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="515cf-144">**Plataforma não NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="515cf-144">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="515cf-145">12</span><span class="sxs-lookup"><span data-stu-id="515cf-145">12</span></span>

<span data-ttu-id="515cf-146">Plataforma não Windows.</span><span class="sxs-lookup"><span data-stu-id="515cf-146">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="515cf-147">**A unidade não é a mesma**</span><span class="sxs-lookup"><span data-stu-id="515cf-147">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="515cf-148">13</span><span class="sxs-lookup"><span data-stu-id="515cf-148">13</span></span>

<span data-ttu-id="515cf-149">A unidade não é a mesma.</span><span class="sxs-lookup"><span data-stu-id="515cf-149">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="515cf-150">**Diretório não vazio**</span><span class="sxs-lookup"><span data-stu-id="515cf-150">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="515cf-151">14</span><span class="sxs-lookup"><span data-stu-id="515cf-151">14</span></span>

<span data-ttu-id="515cf-152">O diretório não está vazio.</span><span class="sxs-lookup"><span data-stu-id="515cf-152">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="515cf-153">**Violação de compartilhamento**</span><span class="sxs-lookup"><span data-stu-id="515cf-153">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="515cf-154">15</span><span class="sxs-lookup"><span data-stu-id="515cf-154">15</span></span>

<span data-ttu-id="515cf-155">Violação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="515cf-155">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="515cf-156">**Arquivo de início inválido**</span><span class="sxs-lookup"><span data-stu-id="515cf-156">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="515cf-157">16</span><span class="sxs-lookup"><span data-stu-id="515cf-157">16</span></span>

<span data-ttu-id="515cf-158">Arquivo inicial inválido.</span><span class="sxs-lookup"><span data-stu-id="515cf-158">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="515cf-159">**Privilégio não mantido**</span><span class="sxs-lookup"><span data-stu-id="515cf-159">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="515cf-160">17</span><span class="sxs-lookup"><span data-stu-id="515cf-160">17</span></span>

<span data-ttu-id="515cf-161">Privilégio não mantido.</span><span class="sxs-lookup"><span data-stu-id="515cf-161">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="515cf-162">**Parâmetro inválido**</span><span class="sxs-lookup"><span data-stu-id="515cf-162">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="515cf-163">21</span><span class="sxs-lookup"><span data-stu-id="515cf-163">21</span></span>

<span data-ttu-id="515cf-164">Parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="515cf-164">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="515cf-165">Comentários</span><span class="sxs-lookup"><span data-stu-id="515cf-165">Remarks</span></span>

<span data-ttu-id="515cf-166">Este método não está implementado no momento pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="515cf-166">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="515cf-167">Para usar esse método, você deve implementá-lo em seu próprio provedor.</span><span class="sxs-lookup"><span data-stu-id="515cf-167">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="515cf-168">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="515cf-168">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="515cf-169">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="515cf-169">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="515cf-170">Requisitos</span><span class="sxs-lookup"><span data-stu-id="515cf-170">Requirements</span></span>



| <span data-ttu-id="515cf-171">Requisito</span><span class="sxs-lookup"><span data-stu-id="515cf-171">Requirement</span></span> | <span data-ttu-id="515cf-172">Valor</span><span class="sxs-lookup"><span data-stu-id="515cf-172">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="515cf-173">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="515cf-173">Minimum supported client</span></span><br/> | <span data-ttu-id="515cf-174">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="515cf-174">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="515cf-175">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="515cf-175">Minimum supported server</span></span><br/> | <span data-ttu-id="515cf-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="515cf-176">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="515cf-177">Namespace</span><span class="sxs-lookup"><span data-stu-id="515cf-177">Namespace</span></span><br/>                | <span data-ttu-id="515cf-178">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="515cf-178">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="515cf-179">MOF</span><span class="sxs-lookup"><span data-stu-id="515cf-179">MOF</span></span><br/>                      | <dl> <span data-ttu-id="515cf-180"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="515cf-180"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="515cf-181">DLL</span><span class="sxs-lookup"><span data-stu-id="515cf-181">DLL</span></span><br/>                      | <dl> <span data-ttu-id="515cf-182"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="515cf-182"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="515cf-183">Confira também</span><span class="sxs-lookup"><span data-stu-id="515cf-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="515cf-184">CIM \_ LogicalFile</span><span class="sxs-lookup"><span data-stu-id="515cf-184">CIM\_LogicalFile</span></span>](takeownershipex-method-in-class-cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="515cf-185">**CIM \_ LogicalFile**</span><span class="sxs-lookup"><span data-stu-id="515cf-185">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

