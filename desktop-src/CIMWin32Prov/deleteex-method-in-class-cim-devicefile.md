---
description: Método DeleteEx da classe CIM_DeviceFile – o método DeleteEx exclui o arquivo lógico (ou diretório) especificado no caminho do objeto. Esse método é uma versão estendida do método Delete e é herdado de CIM \_ LogicalFile.
ms.assetid: ef4d08cd-7287-47be-bcfc-edc248ac5c9b
ms.tgt_platform: multiple
title: Método DeleteEx da classe CIM_DeviceFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile.DeleteEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e21fb57558d7704bf98740de8634bc91289e0038
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089593"
---
# <a name="deleteex-method-of-the-cim_devicefile-class"></a><span data-ttu-id="572ca-104">Método DeleteEx da classe CIM \_ devicefile</span><span class="sxs-lookup"><span data-stu-id="572ca-104">DeleteEx method of the CIM\_DeviceFile class</span></span>

<span data-ttu-id="572ca-105">O método **DeleteEx** exclui o arquivo lógico (ou diretório) especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="572ca-105">The **DeleteEx** method deletes the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="572ca-106">Esse método é uma versão estendida do método [**delete**](delete-method-in-class-cim-devicefile.md) e é herdado de [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="572ca-106">This method is an extended version of the [**Delete**](delete-method-in-class-cim-devicefile.md) method and is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="572ca-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="572ca-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="572ca-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="572ca-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="572ca-109">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="572ca-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="572ca-110">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="572ca-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="572ca-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="572ca-111">Syntax</span></span>


```mof
uint32 DeleteEx(
  [out] string REF StopFileName,
  [in]  string     StartFileName
);
```



## <a name="parameters"></a><span data-ttu-id="572ca-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="572ca-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="572ca-113">*StopFileName* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="572ca-113">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="572ca-114">Cadeia de caracteres que representa o nome do arquivo (ou diretório) em que o método falhou.</span><span class="sxs-lookup"><span data-stu-id="572ca-114">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="572ca-115">Esse parâmetro será nulo se o método tiver sucesso.</span><span class="sxs-lookup"><span data-stu-id="572ca-115">This parameter is null if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="572ca-116">*StartFileName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="572ca-116">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="572ca-117">Cadeia de caracteres que representa o arquivo filho (ou diretório) a ser usado como ponto de partida para esse método.</span><span class="sxs-lookup"><span data-stu-id="572ca-117">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="572ca-118">Normalmente, o parâmetro **StartFileName** é o parâmetro **StopFileName** que especifica o arquivo ou diretório no qual ocorreu um erro da chamada do método anterior.</span><span class="sxs-lookup"><span data-stu-id="572ca-118">Typically, the **StartFileName** parameter is the **StopFileName** parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="572ca-119">Se esse parâmetro for nulo, a operação será executada no arquivo ou diretório especificado na chamada de [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="572ca-119">If this parameter is null, the operation is performed on the file or directory specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="572ca-120">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="572ca-120">Return value</span></span>

<span data-ttu-id="572ca-121">Retorna um valor de 0 (zero) em caso de êxito e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="572ca-121">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="572ca-122">0</span><span class="sxs-lookup"><span data-stu-id="572ca-122">0</span></span>

<span data-ttu-id="572ca-123">Sucesso.</span><span class="sxs-lookup"><span data-stu-id="572ca-123">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="572ca-124">2</span><span class="sxs-lookup"><span data-stu-id="572ca-124">2</span></span>

<span data-ttu-id="572ca-125">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="572ca-125">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="572ca-126">8</span><span class="sxs-lookup"><span data-stu-id="572ca-126">8</span></span>

<span data-ttu-id="572ca-127">Falha não especificada.</span><span class="sxs-lookup"><span data-stu-id="572ca-127">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="572ca-128">9</span><span class="sxs-lookup"><span data-stu-id="572ca-128">9</span></span>

<span data-ttu-id="572ca-129">Objeto inválido.</span><span class="sxs-lookup"><span data-stu-id="572ca-129">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="572ca-130">10</span><span class="sxs-lookup"><span data-stu-id="572ca-130">10</span></span>

<span data-ttu-id="572ca-131">O objeto já existe.</span><span class="sxs-lookup"><span data-stu-id="572ca-131">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="572ca-132">11</span><span class="sxs-lookup"><span data-stu-id="572ca-132">11</span></span>

<span data-ttu-id="572ca-133">Sistema de arquivos não NTFS.</span><span class="sxs-lookup"><span data-stu-id="572ca-133">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="572ca-134">12</span><span class="sxs-lookup"><span data-stu-id="572ca-134">12</span></span>

<span data-ttu-id="572ca-135">Plataforma não Windows.</span><span class="sxs-lookup"><span data-stu-id="572ca-135">Platform not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="572ca-136">13</span><span class="sxs-lookup"><span data-stu-id="572ca-136">13</span></span>

<span data-ttu-id="572ca-137">A unidade não é a mesma.</span><span class="sxs-lookup"><span data-stu-id="572ca-137">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="572ca-138">14</span><span class="sxs-lookup"><span data-stu-id="572ca-138">14</span></span>

<span data-ttu-id="572ca-139">O diretório não está vazio.</span><span class="sxs-lookup"><span data-stu-id="572ca-139">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="572ca-140">15</span><span class="sxs-lookup"><span data-stu-id="572ca-140">15</span></span>

<span data-ttu-id="572ca-141">Violação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="572ca-141">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="572ca-142">16</span><span class="sxs-lookup"><span data-stu-id="572ca-142">16</span></span>

<span data-ttu-id="572ca-143">Arquivo inicial inválido.</span><span class="sxs-lookup"><span data-stu-id="572ca-143">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="572ca-144">17</span><span class="sxs-lookup"><span data-stu-id="572ca-144">17</span></span>

<span data-ttu-id="572ca-145">Privilégio não mantido.</span><span class="sxs-lookup"><span data-stu-id="572ca-145">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="572ca-146">21</span><span class="sxs-lookup"><span data-stu-id="572ca-146">21</span></span>

<span data-ttu-id="572ca-147">Parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="572ca-147">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="572ca-148">Comentários</span><span class="sxs-lookup"><span data-stu-id="572ca-148">Remarks</span></span>

<span data-ttu-id="572ca-149">Este método não está implementado no momento pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="572ca-149">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="572ca-150">Para usar esse método, você deve implementá-lo em seu próprio provedor.</span><span class="sxs-lookup"><span data-stu-id="572ca-150">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="572ca-151">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="572ca-151">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="572ca-152">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="572ca-152">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="572ca-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="572ca-153">Requirements</span></span>



| <span data-ttu-id="572ca-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="572ca-154">Requirement</span></span> | <span data-ttu-id="572ca-155">Valor</span><span class="sxs-lookup"><span data-stu-id="572ca-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="572ca-156">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="572ca-156">Minimum supported client</span></span><br/> | <span data-ttu-id="572ca-157">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="572ca-157">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="572ca-158">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="572ca-158">Minimum supported server</span></span><br/> | <span data-ttu-id="572ca-159">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="572ca-159">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="572ca-160">Namespace</span><span class="sxs-lookup"><span data-stu-id="572ca-160">Namespace</span></span><br/>                | <span data-ttu-id="572ca-161">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="572ca-161">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="572ca-162">MOF</span><span class="sxs-lookup"><span data-stu-id="572ca-162">MOF</span></span><br/>                      | <dl> <span data-ttu-id="572ca-163"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="572ca-163"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="572ca-164">DLL</span><span class="sxs-lookup"><span data-stu-id="572ca-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="572ca-165"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="572ca-165"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="572ca-166">Consulte também</span><span class="sxs-lookup"><span data-stu-id="572ca-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="572ca-167">\_Dispositivo CIM</span><span class="sxs-lookup"><span data-stu-id="572ca-167">CIM\_DeviceFile</span></span>](deleteex-method-in-class-cim-devicefile.md)
</dt> <dt>

[<span data-ttu-id="572ca-168">**\_Dispositivo CIM**</span><span class="sxs-lookup"><span data-stu-id="572ca-168">**CIM\_DeviceFile**</span></span>](cim-devicefile.md)
</dt> </dl>

 

