---
description: O método Copy copia o arquivo lógico (ou diretório) especificado no caminho do objeto para o local especificado pelo parâmetro de entrada.
ms.assetid: 6c1c6172-80a2-4779-903a-935f8c7091a5
ms.tgt_platform: multiple
title: Método Copy da classe CIM_DeviceFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile.Copy
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: dc8bb7878f4967dbc58adf6163c92c0d2bd67713
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826444"
---
# <a name="copy-method-of-the-cim_devicefile-class"></a><span data-ttu-id="3379b-103">Método Copy da classe CIM \_ devicefile</span><span class="sxs-lookup"><span data-stu-id="3379b-103">Copy method of the CIM\_DeviceFile class</span></span>

<span data-ttu-id="3379b-104">O método **Copy** copia o arquivo lógico (ou diretório) especificado no caminho do objeto para o local especificado pelo parâmetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="3379b-104">The **Copy** method copies the logical file (or directory) specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="3379b-105">Não haverá suporte para uma cópia se ela exigir a substituição de um arquivo lógico existente.</span><span class="sxs-lookup"><span data-stu-id="3379b-105">A copy is not supported if it requires overwriting an existing logical file.</span></span> <span data-ttu-id="3379b-106">Esse método é herdado [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="3379b-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3379b-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="3379b-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="3379b-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="3379b-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="3379b-109">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="3379b-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="3379b-110">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="3379b-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="3379b-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3379b-111">Syntax</span></span>


```mof
uint32 Copy(
  [in] string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="3379b-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3379b-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3379b-113">*Nome do arquivo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3379b-113">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3379b-114">Nome totalmente qualificado da cópia do arquivo de destino (ou diretório).</span><span class="sxs-lookup"><span data-stu-id="3379b-114">Fully qualified name of the destination file (or directory) copy.</span></span>

<span data-ttu-id="3379b-115">Exemplo: "c: \\ temp \\ newdirectory"</span><span class="sxs-lookup"><span data-stu-id="3379b-115">Example: "c:\\temp\\newdirectory"</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3379b-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3379b-116">Return value</span></span>

<span data-ttu-id="3379b-117">Retorna um valor de 0 (zero) em caso de êxito e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="3379b-117">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="3379b-118">**0**</span><span class="sxs-lookup"><span data-stu-id="3379b-118">**0**</span></span>
</dt> <dd>

<span data-ttu-id="3379b-119">Sucesso.</span><span class="sxs-lookup"><span data-stu-id="3379b-119">Success.</span></span>

</dd> <dt>

<span data-ttu-id="3379b-120">**2**</span><span class="sxs-lookup"><span data-stu-id="3379b-120">**2**</span></span>
</dt> <dd>

<span data-ttu-id="3379b-121">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="3379b-121">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="3379b-122">**8**</span><span class="sxs-lookup"><span data-stu-id="3379b-122">**8**</span></span>
</dt> <dd>

<span data-ttu-id="3379b-123">Falha não especificada.</span><span class="sxs-lookup"><span data-stu-id="3379b-123">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="3379b-124">**9**</span><span class="sxs-lookup"><span data-stu-id="3379b-124">**9**</span></span>
</dt> <dd>

<span data-ttu-id="3379b-125">Objeto inválido.</span><span class="sxs-lookup"><span data-stu-id="3379b-125">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="3379b-126">**10**</span><span class="sxs-lookup"><span data-stu-id="3379b-126">**10**</span></span>
</dt> <dd>

<span data-ttu-id="3379b-127">O objeto já existe.</span><span class="sxs-lookup"><span data-stu-id="3379b-127">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="3379b-128">**11**</span><span class="sxs-lookup"><span data-stu-id="3379b-128">**11**</span></span>
</dt> <dd>

<span data-ttu-id="3379b-129">Sistema de arquivos não NTFS.</span><span class="sxs-lookup"><span data-stu-id="3379b-129">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="3379b-130">**12**</span><span class="sxs-lookup"><span data-stu-id="3379b-130">**12**</span></span>
</dt> <dd>

<span data-ttu-id="3379b-131">Plataforma não Windows.</span><span class="sxs-lookup"><span data-stu-id="3379b-131">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="3379b-132">**13**</span><span class="sxs-lookup"><span data-stu-id="3379b-132">**13**</span></span>
</dt> <dd>

<span data-ttu-id="3379b-133">A unidade não é a mesma.</span><span class="sxs-lookup"><span data-stu-id="3379b-133">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="3379b-134">**14**</span><span class="sxs-lookup"><span data-stu-id="3379b-134">**14**</span></span>
</dt> <dd>

<span data-ttu-id="3379b-135">O diretório não está vazio.</span><span class="sxs-lookup"><span data-stu-id="3379b-135">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="3379b-136">**15**</span><span class="sxs-lookup"><span data-stu-id="3379b-136">**15**</span></span>
</dt> <dd>

<span data-ttu-id="3379b-137">Violação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="3379b-137">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="3379b-138">**16**</span><span class="sxs-lookup"><span data-stu-id="3379b-138">**16**</span></span>
</dt> <dd>

<span data-ttu-id="3379b-139">Arquivo inicial inválido.</span><span class="sxs-lookup"><span data-stu-id="3379b-139">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="3379b-140">**17**</span><span class="sxs-lookup"><span data-stu-id="3379b-140">**17**</span></span>
</dt> <dd>

<span data-ttu-id="3379b-141">Privilégio não mantido.</span><span class="sxs-lookup"><span data-stu-id="3379b-141">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="3379b-142">**Abril**</span><span class="sxs-lookup"><span data-stu-id="3379b-142">**21**</span></span>
</dt> <dd>

<span data-ttu-id="3379b-143">Parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="3379b-143">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3379b-144">Comentários</span><span class="sxs-lookup"><span data-stu-id="3379b-144">Remarks</span></span>

<span data-ttu-id="3379b-145">Este método não está implementado no momento pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="3379b-145">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="3379b-146">Para usar esse método, você deve implementá-lo em seu próprio provedor.</span><span class="sxs-lookup"><span data-stu-id="3379b-146">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="3379b-147">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="3379b-147">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="3379b-148">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="3379b-148">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="3379b-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3379b-149">Requirements</span></span>



| <span data-ttu-id="3379b-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="3379b-150">Requirement</span></span> | <span data-ttu-id="3379b-151">Valor</span><span class="sxs-lookup"><span data-stu-id="3379b-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3379b-152">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3379b-152">Minimum supported client</span></span><br/> | <span data-ttu-id="3379b-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3379b-153">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3379b-154">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3379b-154">Minimum supported server</span></span><br/> | <span data-ttu-id="3379b-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3379b-155">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3379b-156">Namespace</span><span class="sxs-lookup"><span data-stu-id="3379b-156">Namespace</span></span><br/>                | <span data-ttu-id="3379b-157">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="3379b-157">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3379b-158">MOF</span><span class="sxs-lookup"><span data-stu-id="3379b-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3379b-159"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3379b-159"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3379b-160">DLL</span><span class="sxs-lookup"><span data-stu-id="3379b-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3379b-161"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3379b-161"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3379b-162">Confira também</span><span class="sxs-lookup"><span data-stu-id="3379b-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3379b-163">\_Dispositivo CIM</span><span class="sxs-lookup"><span data-stu-id="3379b-163">CIM\_DeviceFile</span></span>](copy-method-in-class-cim-devicefile.md)
</dt> <dt>

[<span data-ttu-id="3379b-164">**\_Dispositivo CIM**</span><span class="sxs-lookup"><span data-stu-id="3379b-164">**CIM\_DeviceFile**</span></span>](cim-devicefile.md)
</dt> </dl>

 

