---
description: Método TakeOwnerShip da classe CIM_Directory – o método TakeOwnerShip Obtém a propriedade do arquivo lógico especificado no caminho do objeto.
ms.assetid: 053647d0-3ba0-4cd4-a84a-a1a96ef7151c
ms.tgt_platform: multiple
title: Método TakeOwnerShip da classe CIM_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.TakeOwnerShip
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 12c328f30e56db348b018b73b02aa4320bf99505
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086054"
---
# <a name="takeownership-method-of-the-cim_directory-class"></a><span data-ttu-id="3f080-103">Método TakeOwnerShip da classe de \_ diretório CIM</span><span class="sxs-lookup"><span data-stu-id="3f080-103">TakeOwnerShip method of the CIM\_Directory class</span></span>

<span data-ttu-id="3f080-104">O método **TakeOwnership** Obtém a propriedade do arquivo lógico especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="3f080-104">The **TakeOwnerShip** method obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="3f080-105">Se o arquivo lógico for um diretório, esse método agirá recursivamente, assumindo a propriedade de todos os arquivos e subdiretórios contidos no diretório.</span><span class="sxs-lookup"><span data-stu-id="3f080-105">If the logical file is a directory, this method acts recursively, taking ownership of all of the files and sub-directories that the directory contains.</span></span> <span data-ttu-id="3f080-106">Esse método é herdado [**do \_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="3f080-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3f080-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="3f080-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="3f080-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="3f080-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="3f080-109">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="3f080-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="3f080-110">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="3f080-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="3f080-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3f080-111">Syntax</span></span>


```mof
uint32 TakeOwnerShip();
```



## <a name="parameters"></a><span data-ttu-id="3f080-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3f080-112">Parameters</span></span>

<span data-ttu-id="3f080-113">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="3f080-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3f080-114">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="3f080-114">Return value</span></span>

<span data-ttu-id="3f080-115">Retorna um valor de 0 (zero) em caso de êxito e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="3f080-115">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="3f080-116">**0**</span><span class="sxs-lookup"><span data-stu-id="3f080-116">**0**</span></span>
</dt> <dd>

<span data-ttu-id="3f080-117">Sucesso.</span><span class="sxs-lookup"><span data-stu-id="3f080-117">Success.</span></span>

</dd> <dt>

<span data-ttu-id="3f080-118">**2**</span><span class="sxs-lookup"><span data-stu-id="3f080-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="3f080-119">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="3f080-119">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="3f080-120">**8**</span><span class="sxs-lookup"><span data-stu-id="3f080-120">**8**</span></span>
</dt> <dd>

<span data-ttu-id="3f080-121">Falha não especificada.</span><span class="sxs-lookup"><span data-stu-id="3f080-121">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="3f080-122">**9**</span><span class="sxs-lookup"><span data-stu-id="3f080-122">**9**</span></span>
</dt> <dd>

<span data-ttu-id="3f080-123">Objeto inválido.</span><span class="sxs-lookup"><span data-stu-id="3f080-123">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="3f080-124">**10**</span><span class="sxs-lookup"><span data-stu-id="3f080-124">**10**</span></span>
</dt> <dd>

<span data-ttu-id="3f080-125">O objeto já existe.</span><span class="sxs-lookup"><span data-stu-id="3f080-125">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="3f080-126">**11**</span><span class="sxs-lookup"><span data-stu-id="3f080-126">**11**</span></span>
</dt> <dd>

<span data-ttu-id="3f080-127">Sistema de arquivos não NTFS.</span><span class="sxs-lookup"><span data-stu-id="3f080-127">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="3f080-128">**12**</span><span class="sxs-lookup"><span data-stu-id="3f080-128">**12**</span></span>
</dt> <dd>

<span data-ttu-id="3f080-129">A plataforma não é o Windows.</span><span class="sxs-lookup"><span data-stu-id="3f080-129">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="3f080-130">**13**</span><span class="sxs-lookup"><span data-stu-id="3f080-130">**13**</span></span>
</dt> <dd>

<span data-ttu-id="3f080-131">A unidade não é a mesma.</span><span class="sxs-lookup"><span data-stu-id="3f080-131">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="3f080-132">**14**</span><span class="sxs-lookup"><span data-stu-id="3f080-132">**14**</span></span>
</dt> <dd>

<span data-ttu-id="3f080-133">O diretório não está vazio.</span><span class="sxs-lookup"><span data-stu-id="3f080-133">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="3f080-134">**15**</span><span class="sxs-lookup"><span data-stu-id="3f080-134">**15**</span></span>
</dt> <dd>

<span data-ttu-id="3f080-135">Violação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="3f080-135">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="3f080-136">**16**</span><span class="sxs-lookup"><span data-stu-id="3f080-136">**16**</span></span>
</dt> <dd>

<span data-ttu-id="3f080-137">Arquivo inicial inválido.</span><span class="sxs-lookup"><span data-stu-id="3f080-137">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="3f080-138">**17**</span><span class="sxs-lookup"><span data-stu-id="3f080-138">**17**</span></span>
</dt> <dd>

<span data-ttu-id="3f080-139">Privilégio não mantido.</span><span class="sxs-lookup"><span data-stu-id="3f080-139">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="3f080-140">**Abril**</span><span class="sxs-lookup"><span data-stu-id="3f080-140">**21**</span></span>
</dt> <dd>

<span data-ttu-id="3f080-141">Parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="3f080-141">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3f080-142">Comentários</span><span class="sxs-lookup"><span data-stu-id="3f080-142">Remarks</span></span>

<span data-ttu-id="3f080-143">Este método não está implementado no momento pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="3f080-143">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="3f080-144">Para usar esse método, você deve implementá-lo em seu próprio provedor.</span><span class="sxs-lookup"><span data-stu-id="3f080-144">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="3f080-145">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="3f080-145">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="3f080-146">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="3f080-146">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="examples"></a><span data-ttu-id="3f080-147">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3f080-147">Examples</span></span>

<span data-ttu-id="3f080-148">O código de script Visual Basic a seguir chama o método **TakeOwnership** para apropriar-se da pasta C: \\ Temp.</span><span class="sxs-lookup"><span data-stu-id="3f080-148">The following Visual Basic Script code calls the **TakeOwnerShip** method to take ownership of the C:\\temp folder.</span></span>


```VB
strComputer = "." 

Set objWMIService = _
    GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 

' Obtain the definition of the class.
Set objShare = objWMIService.Get("Win32_Directory")

' Execute the method and obtain the return status.
' The OutParameters object in objOutParams
' is created by the provider.
Set objOutParams = objWMIService.ExecMethod( _
    "Win32_Directory.Name='C:\\temp'", "TakeOwnerShip")

wscript.echo objOutParams.ReturnValue
```



## <a name="requirements"></a><span data-ttu-id="3f080-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3f080-149">Requirements</span></span>



| <span data-ttu-id="3f080-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f080-150">Requirement</span></span> | <span data-ttu-id="3f080-151">Valor</span><span class="sxs-lookup"><span data-stu-id="3f080-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3f080-152">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3f080-152">Minimum supported client</span></span><br/> | <span data-ttu-id="3f080-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3f080-153">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3f080-154">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3f080-154">Minimum supported server</span></span><br/> | <span data-ttu-id="3f080-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3f080-155">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3f080-156">Namespace</span><span class="sxs-lookup"><span data-stu-id="3f080-156">Namespace</span></span><br/>                | <span data-ttu-id="3f080-157">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="3f080-157">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3f080-158">MOF</span><span class="sxs-lookup"><span data-stu-id="3f080-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3f080-159"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3f080-159"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3f080-160">DLL</span><span class="sxs-lookup"><span data-stu-id="3f080-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3f080-161"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3f080-161"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f080-162">Consulte também</span><span class="sxs-lookup"><span data-stu-id="3f080-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f080-163">\_Diretório CIM</span><span class="sxs-lookup"><span data-stu-id="3f080-163">CIM\_Directory</span></span>](takeownership-method-in-class-cim-directory.md)
</dt> <dt>

[<span data-ttu-id="3f080-164">**\_Diretório CIM**</span><span class="sxs-lookup"><span data-stu-id="3f080-164">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> </dl>

 

