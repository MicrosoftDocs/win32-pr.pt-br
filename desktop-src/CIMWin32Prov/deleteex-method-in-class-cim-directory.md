---
description: Método DeleteEx da classe CIM_Directory – o método DeleteEx exclui o arquivo lógico (ou diretório) especificado no caminho do objeto. Esse método é uma versão estendida do método Delete e é herdado de CIM \_ LogicalFile.
ms.assetid: 5f924327-248c-47e2-b42e-50c83defce17
ms.tgt_platform: multiple
title: Método DeleteEx da classe CIM_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.DeleteEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4a3704507405ebb2d310ed7341cd1db174e00588
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097094"
---
# <a name="deleteex-method-of-the-cim_directory-class"></a><span data-ttu-id="94f71-104">Método DeleteEx da classe de \_ diretório CIM</span><span class="sxs-lookup"><span data-stu-id="94f71-104">DeleteEx method of the CIM\_Directory class</span></span>

<span data-ttu-id="94f71-105">O método **DeleteEx** exclui o arquivo lógico (ou diretório) especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="94f71-105">The **DeleteEx** method deletes the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="94f71-106">Esse método é uma versão estendida do método [**delete**](delete-method-in-class-cim-directory.md) e é herdado de [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="94f71-106">This method is an extended version of the [**Delete**](delete-method-in-class-cim-directory.md) method and is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="94f71-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="94f71-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="94f71-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="94f71-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="94f71-109">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="94f71-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="94f71-110">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="94f71-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="94f71-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="94f71-111">Syntax</span></span>


```mof
uint32 DeleteEx(
  [out] string REF StopFileName,
  [in]  string     StartFileName
);
```



## <a name="parameters"></a><span data-ttu-id="94f71-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="94f71-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94f71-113">*StopFileName* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="94f71-113">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="94f71-114">Cadeia de caracteres que representa o nome do arquivo (ou diretório) em que o método falhou.</span><span class="sxs-lookup"><span data-stu-id="94f71-114">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="94f71-115">Esse parâmetro será nulo se o método tiver sucesso.</span><span class="sxs-lookup"><span data-stu-id="94f71-115">This parameter is null if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="94f71-116">*StartFileName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="94f71-116">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94f71-117">Cadeia de caracteres que representa o arquivo filho (ou diretório) a ser usado como ponto de partida para esse método.</span><span class="sxs-lookup"><span data-stu-id="94f71-117">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="94f71-118">Normalmente, esse parâmetro é o parâmetro *StopFileName* que especifica o arquivo ou diretório no qual ocorreu um erro da chamada do método anterior.</span><span class="sxs-lookup"><span data-stu-id="94f71-118">Typically, this parameter is the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="94f71-119">Se esse parâmetro for nulo, a operação será executada no arquivo (ou diretório) especificado na chamada de [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="94f71-119">If this parameter is null, the operation is performed on the file (or directory) specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94f71-120">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="94f71-120">Return value</span></span>

<span data-ttu-id="94f71-121">Retorna um valor de 0 (zero) em caso de êxito e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="94f71-121">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="94f71-122">0</span><span class="sxs-lookup"><span data-stu-id="94f71-122">0</span></span>

<span data-ttu-id="94f71-123">Sucesso.</span><span class="sxs-lookup"><span data-stu-id="94f71-123">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="94f71-124">2</span><span class="sxs-lookup"><span data-stu-id="94f71-124">2</span></span>

<span data-ttu-id="94f71-125">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="94f71-125">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="94f71-126">8</span><span class="sxs-lookup"><span data-stu-id="94f71-126">8</span></span>

<span data-ttu-id="94f71-127">Falha não especificada.</span><span class="sxs-lookup"><span data-stu-id="94f71-127">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="94f71-128">9</span><span class="sxs-lookup"><span data-stu-id="94f71-128">9</span></span>

<span data-ttu-id="94f71-129">Objeto inválido.</span><span class="sxs-lookup"><span data-stu-id="94f71-129">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="94f71-130">10</span><span class="sxs-lookup"><span data-stu-id="94f71-130">10</span></span>

<span data-ttu-id="94f71-131">O objeto já existe.</span><span class="sxs-lookup"><span data-stu-id="94f71-131">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="94f71-132">11</span><span class="sxs-lookup"><span data-stu-id="94f71-132">11</span></span>

<span data-ttu-id="94f71-133">Sistema de arquivos não NTFS.</span><span class="sxs-lookup"><span data-stu-id="94f71-133">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="94f71-134">12</span><span class="sxs-lookup"><span data-stu-id="94f71-134">12</span></span>

<span data-ttu-id="94f71-135">Plataforma não Windows.</span><span class="sxs-lookup"><span data-stu-id="94f71-135">Platform not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="94f71-136">13</span><span class="sxs-lookup"><span data-stu-id="94f71-136">13</span></span>

<span data-ttu-id="94f71-137">A unidade não é a mesma.</span><span class="sxs-lookup"><span data-stu-id="94f71-137">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="94f71-138">14</span><span class="sxs-lookup"><span data-stu-id="94f71-138">14</span></span>

<span data-ttu-id="94f71-139">O diretório não está vazio.</span><span class="sxs-lookup"><span data-stu-id="94f71-139">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="94f71-140">15</span><span class="sxs-lookup"><span data-stu-id="94f71-140">15</span></span>

<span data-ttu-id="94f71-141">Violação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="94f71-141">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="94f71-142">16</span><span class="sxs-lookup"><span data-stu-id="94f71-142">16</span></span>

<span data-ttu-id="94f71-143">Arquivo inicial inválido.</span><span class="sxs-lookup"><span data-stu-id="94f71-143">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="94f71-144">17</span><span class="sxs-lookup"><span data-stu-id="94f71-144">17</span></span>

<span data-ttu-id="94f71-145">Privilégio não mantido.</span><span class="sxs-lookup"><span data-stu-id="94f71-145">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="94f71-146">21</span><span class="sxs-lookup"><span data-stu-id="94f71-146">21</span></span>

<span data-ttu-id="94f71-147">Parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="94f71-147">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="94f71-148">Comentários</span><span class="sxs-lookup"><span data-stu-id="94f71-148">Remarks</span></span>

<span data-ttu-id="94f71-149">Este método não está implementado no momento pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="94f71-149">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="94f71-150">Para usar esse método, você deve implementá-lo em seu próprio provedor.</span><span class="sxs-lookup"><span data-stu-id="94f71-150">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="94f71-151">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="94f71-151">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="94f71-152">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="94f71-152">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="94f71-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="94f71-153">Requirements</span></span>



| <span data-ttu-id="94f71-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="94f71-154">Requirement</span></span> | <span data-ttu-id="94f71-155">Valor</span><span class="sxs-lookup"><span data-stu-id="94f71-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="94f71-156">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="94f71-156">Minimum supported client</span></span><br/> | <span data-ttu-id="94f71-157">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="94f71-157">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="94f71-158">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="94f71-158">Minimum supported server</span></span><br/> | <span data-ttu-id="94f71-159">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="94f71-159">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="94f71-160">Namespace</span><span class="sxs-lookup"><span data-stu-id="94f71-160">Namespace</span></span><br/>                | <span data-ttu-id="94f71-161">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="94f71-161">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="94f71-162">MOF</span><span class="sxs-lookup"><span data-stu-id="94f71-162">MOF</span></span><br/>                      | <dl> <span data-ttu-id="94f71-163"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="94f71-163"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="94f71-164">DLL</span><span class="sxs-lookup"><span data-stu-id="94f71-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="94f71-165"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="94f71-165"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94f71-166">Consulte também</span><span class="sxs-lookup"><span data-stu-id="94f71-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94f71-167">\_Diretório CIM</span><span class="sxs-lookup"><span data-stu-id="94f71-167">CIM\_Directory</span></span>](deleteex-method-in-class-cim-directory.md)
</dt> <dt>

[<span data-ttu-id="94f71-168">**\_Diretório CIM**</span><span class="sxs-lookup"><span data-stu-id="94f71-168">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> </dl>

 

