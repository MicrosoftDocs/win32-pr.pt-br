---
description: O método TakeOwnerShip Obtém a propriedade do arquivo lógico especificado no caminho do objeto.
ms.assetid: ef7d5ce7-99fb-464f-9739-ec9189148f94
ms.tgt_platform: multiple
title: Método TakeOwnerShip da classe CIM_DeviceFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile.TakeOwnerShip
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: d700940f3ee00cd4d65b8307c48ac7cc3ed28a2c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104456916"
---
# <a name="takeownership-method-of-the-cim_devicefile-class"></a><span data-ttu-id="dd0ae-103">Método TakeOwnerShip da classe CIM \_ devicefile</span><span class="sxs-lookup"><span data-stu-id="dd0ae-103">TakeOwnerShip method of the CIM\_DeviceFile class</span></span>

<span data-ttu-id="dd0ae-104">O método **TakeOwnership** Obtém a propriedade do arquivo lógico especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="dd0ae-104">The **TakeOwnerShip** method obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="dd0ae-105">Se o arquivo lógico for um diretório, esse método agirá de forma recursiva, assumindo a propriedade de todos os arquivos e subdiretórios contidos no diretório.</span><span class="sxs-lookup"><span data-stu-id="dd0ae-105">If the logical file is a directory, then this method will act recursively, taking ownership of all of the files and sub-directories that the directory contains.</span></span> <span data-ttu-id="dd0ae-106">Esse método é herdado [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="dd0ae-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dd0ae-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="dd0ae-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="dd0ae-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="dd0ae-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="dd0ae-109">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="dd0ae-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="dd0ae-110">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="dd0ae-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="dd0ae-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dd0ae-111">Syntax</span></span>


```mof
uint32 TakeOwnerShip();
```



## <a name="parameters"></a><span data-ttu-id="dd0ae-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dd0ae-112">Parameters</span></span>

<span data-ttu-id="dd0ae-113">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="dd0ae-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="dd0ae-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="dd0ae-114">Return value</span></span>

<span data-ttu-id="dd0ae-115">Retorna um valor de 0 (zero) em caso de êxito e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="dd0ae-115">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="dd0ae-116">**0**</span><span class="sxs-lookup"><span data-stu-id="dd0ae-116">**0**</span></span>
</dt> <dd>

<span data-ttu-id="dd0ae-117">Êxito.</span><span class="sxs-lookup"><span data-stu-id="dd0ae-117">Success.</span></span>

</dd> <dt>

<span data-ttu-id="dd0ae-118">**2**</span><span class="sxs-lookup"><span data-stu-id="dd0ae-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="dd0ae-119">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="dd0ae-119">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="dd0ae-120">**8**</span><span class="sxs-lookup"><span data-stu-id="dd0ae-120">**8**</span></span>
</dt> <dd>

<span data-ttu-id="dd0ae-121">Falha não especificada.</span><span class="sxs-lookup"><span data-stu-id="dd0ae-121">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="dd0ae-122">**9**</span><span class="sxs-lookup"><span data-stu-id="dd0ae-122">**9**</span></span>
</dt> <dd>

<span data-ttu-id="dd0ae-123">Objeto inválido.</span><span class="sxs-lookup"><span data-stu-id="dd0ae-123">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="dd0ae-124">**10**</span><span class="sxs-lookup"><span data-stu-id="dd0ae-124">**10**</span></span>
</dt> <dd>

<span data-ttu-id="dd0ae-125">O objeto já existe.</span><span class="sxs-lookup"><span data-stu-id="dd0ae-125">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="dd0ae-126">**11**</span><span class="sxs-lookup"><span data-stu-id="dd0ae-126">**11**</span></span>
</dt> <dd>

<span data-ttu-id="dd0ae-127">Sistema de arquivos não NTFS.</span><span class="sxs-lookup"><span data-stu-id="dd0ae-127">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="dd0ae-128">**12**</span><span class="sxs-lookup"><span data-stu-id="dd0ae-128">**12**</span></span>
</dt> <dd>

<span data-ttu-id="dd0ae-129">Plataforma não Windows.</span><span class="sxs-lookup"><span data-stu-id="dd0ae-129">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="dd0ae-130">**13**</span><span class="sxs-lookup"><span data-stu-id="dd0ae-130">**13**</span></span>
</dt> <dd>

<span data-ttu-id="dd0ae-131">A unidade não é a mesma.</span><span class="sxs-lookup"><span data-stu-id="dd0ae-131">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="dd0ae-132">**14**</span><span class="sxs-lookup"><span data-stu-id="dd0ae-132">**14**</span></span>
</dt> <dd>

<span data-ttu-id="dd0ae-133">O diretório não está vazio.</span><span class="sxs-lookup"><span data-stu-id="dd0ae-133">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="dd0ae-134">**15**</span><span class="sxs-lookup"><span data-stu-id="dd0ae-134">**15**</span></span>
</dt> <dd>

<span data-ttu-id="dd0ae-135">Violação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="dd0ae-135">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="dd0ae-136">**16**</span><span class="sxs-lookup"><span data-stu-id="dd0ae-136">**16**</span></span>
</dt> <dd>

<span data-ttu-id="dd0ae-137">Arquivo inicial inválido.</span><span class="sxs-lookup"><span data-stu-id="dd0ae-137">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="dd0ae-138">**17**</span><span class="sxs-lookup"><span data-stu-id="dd0ae-138">**17**</span></span>
</dt> <dd>

<span data-ttu-id="dd0ae-139">Privilégio não mantido.</span><span class="sxs-lookup"><span data-stu-id="dd0ae-139">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="dd0ae-140">**Abril**</span><span class="sxs-lookup"><span data-stu-id="dd0ae-140">**21**</span></span>
</dt> <dd>

<span data-ttu-id="dd0ae-141">Parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="dd0ae-141">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dd0ae-142">Comentários</span><span class="sxs-lookup"><span data-stu-id="dd0ae-142">Remarks</span></span>

<span data-ttu-id="dd0ae-143">Este método não está implementado no momento pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="dd0ae-143">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="dd0ae-144">Para usar esse método, você deve implementá-lo em seu próprio provedor.</span><span class="sxs-lookup"><span data-stu-id="dd0ae-144">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="dd0ae-145">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="dd0ae-145">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="dd0ae-146">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="dd0ae-146">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd0ae-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dd0ae-147">Requirements</span></span>



| <span data-ttu-id="dd0ae-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd0ae-148">Requirement</span></span> | <span data-ttu-id="dd0ae-149">Valor</span><span class="sxs-lookup"><span data-stu-id="dd0ae-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dd0ae-150">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dd0ae-150">Minimum supported client</span></span><br/> | <span data-ttu-id="dd0ae-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dd0ae-151">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="dd0ae-152">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dd0ae-152">Minimum supported server</span></span><br/> | <span data-ttu-id="dd0ae-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dd0ae-153">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="dd0ae-154">Namespace</span><span class="sxs-lookup"><span data-stu-id="dd0ae-154">Namespace</span></span><br/>                | <span data-ttu-id="dd0ae-155">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="dd0ae-155">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="dd0ae-156">MOF</span><span class="sxs-lookup"><span data-stu-id="dd0ae-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dd0ae-157"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dd0ae-157"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="dd0ae-158">DLL</span><span class="sxs-lookup"><span data-stu-id="dd0ae-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dd0ae-159"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dd0ae-159"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd0ae-160">Confira também</span><span class="sxs-lookup"><span data-stu-id="dd0ae-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd0ae-161">\_Dispositivo CIM</span><span class="sxs-lookup"><span data-stu-id="dd0ae-161">CIM\_DeviceFile</span></span>](takeownership-method-in-class-cim-devicefile.md)
</dt> <dt>

[<span data-ttu-id="dd0ae-162">**\_Dispositivo CIM**</span><span class="sxs-lookup"><span data-stu-id="dd0ae-162">**CIM\_DeviceFile**</span></span>](cim-devicefile.md)
</dt> </dl>

 

