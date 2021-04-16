---
description: Retorna o SWbemObject associado ao índice especificado na coleção.
ms.assetid: 75830f78-0489-4fae-bf9c-2eee8526232e
ms.tgt_platform: multiple
title: Método SWbemObjectSet. ItemIndex (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectSet.ItemIndex
- ISWbemObjectSet.ItemIndex
- ISWbemObjectSet.ItemIndex
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 606a09ebf54f0a31dbe14e10abd52a7e92d815d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105765636"
---
# <a name="swbemobjectsetitemindex-method"></a><span data-ttu-id="ccaae-103">Método SWbemObjectSet. ItemIndex</span><span class="sxs-lookup"><span data-stu-id="ccaae-103">SWbemObjectSet.ItemIndex method</span></span>

<span data-ttu-id="ccaae-104">O método **ItemIndex** retorna o [**SWbemObject**](swbemobject.md) associado ao índice especificado na coleção.</span><span class="sxs-lookup"><span data-stu-id="ccaae-104">The **ItemIndex** method returns the [**SWbemObject**](swbemobject.md) associated with the specified index into the collection.</span></span> <span data-ttu-id="ccaae-105">O índice indica a posição do elemento dentro da coleção.</span><span class="sxs-lookup"><span data-stu-id="ccaae-105">The index indicates the position of the element within the collection.</span></span> <span data-ttu-id="ccaae-106">A numeração da coleção começa em zero.</span><span class="sxs-lookup"><span data-stu-id="ccaae-106">Collection numbering starts at zero.</span></span>

## <a name="syntax"></a><span data-ttu-id="ccaae-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ccaae-107">Syntax</span></span>


```VB
objWbemObject = .ItemIndex( _
  ByVal lIndex _
)
```



## <a name="parameters"></a><span data-ttu-id="ccaae-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ccaae-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ccaae-109">*lIndex*</span><span class="sxs-lookup"><span data-stu-id="ccaae-109">*lIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="ccaae-110">Índice do item na coleção.</span><span class="sxs-lookup"><span data-stu-id="ccaae-110">Index of the item in the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ccaae-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ccaae-111">Return value</span></span>

<span data-ttu-id="ccaae-112">Se for bem-sucedido, o objeto [**SWbemObject**](swbemobject.md) solicitado retornará.</span><span class="sxs-lookup"><span data-stu-id="ccaae-112">If successful, the requested [**SWbemObject**](swbemobject.md) object returns.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ccaae-113">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="ccaae-113">Error codes</span></span>

<span data-ttu-id="ccaae-114">Após a conclusão do método [**Item**](swbemobjectset-item.md) , o objeto **Err** pode conter um dos códigos de erro abaixo.</span><span class="sxs-lookup"><span data-stu-id="ccaae-114">Upon completion of the [**Item**](swbemobjectset-item.md) method, the **Err** object may contain one of the error codes below.</span></span>

<dl> <dt>

<span data-ttu-id="ccaae-115">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="ccaae-115">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="ccaae-116">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="ccaae-116">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="ccaae-117">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="ccaae-117">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="ccaae-118">Foi especificado um parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="ccaae-118">Invalid parameter was specified.</span></span> <span data-ttu-id="ccaae-119">Esse erro será retornado se um número de índice negativo for fornecido.</span><span class="sxs-lookup"><span data-stu-id="ccaae-119">This error is returned if a negative index number is supplied.</span></span>

</dd> <dt>

<span data-ttu-id="ccaae-120">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="ccaae-120">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="ccaae-121">Não há memória suficiente para concluir a operação.</span><span class="sxs-lookup"><span data-stu-id="ccaae-121">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="ccaae-122">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="ccaae-122">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="ccaae-123">O item solicitado não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="ccaae-123">Requested item was not found.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ccaae-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="ccaae-124">Remarks</span></span>

<span data-ttu-id="ccaae-125">O método **ItemIndex** permite que os scripts de clientes WMI e aplicativos escritos em qualquer linguagem uma maneira uniforme de manipular uma coleção como uma matriz.</span><span class="sxs-lookup"><span data-stu-id="ccaae-125">The **ItemIndex** method allows WMI clients scripts and applications written in any language a uniform way to manipulate a collection like an array.</span></span> <span data-ttu-id="ccaae-126">Esse método pode ser usado com coleções [**SWbemObjectSet**](swbemobjectset.md) .</span><span class="sxs-lookup"><span data-stu-id="ccaae-126">This method can be used with [**SWbemObjectSet**](swbemobjectset.md) collections.</span></span> <span data-ttu-id="ccaae-127">Consultas, como [**SWbemServices. AssociatorsOf**](swbemservices-associatorsof.md), [**SWbemServices. References**](swbemservices-referencesto.md), [**SWbemServices. InstancesOf**](swbemservices-instancesof.md)ou [**SWbemServices.ExecQuery**](swbemservices-execquery.md) retornam coleções **SWbemObjectSet** .</span><span class="sxs-lookup"><span data-stu-id="ccaae-127">Queries, such as [**SWbemServices.AssociatorsOf**](swbemservices-associatorsof.md), [**SWbemServices.ReferencesTo**](swbemservices-referencesto.md), [**SWbemServices.InstancesOf**](swbemservices-instancesof.md), or [**SWbemServices.ExecQuery**](swbemservices-execquery.md) return **SWbemObjectSet** collections.</span></span> <span data-ttu-id="ccaae-128">O método **ItemIndex** não funciona com coleções que não contêm [**SWbemObjects**](swbemobject.md), como [**SWbemMethodSet**](swbemmethodset.md), [**SWbemNamedValueSet**](swbemnamedvalueset.md), [**SWbemPrivilegeSet**](swbemprivilegeset.md), [**SWbemPropertySet**](swbempropertyset.md)e [**SWbemQualifierSet**](swbemqualifierset.md).</span><span class="sxs-lookup"><span data-stu-id="ccaae-128">The **ItemIndex** method does not work with collections which do not contain [**SWbemObjects**](swbemobject.md), such as [**SWbemMethodSet**](swbemmethodset.md), [**SWbemNamedValueSet**](swbemnamedvalueset.md), [**SWbemPrivilegeSet**](swbemprivilegeset.md), [**SWbemPropertySet**](swbempropertyset.md), and [**SWbemQualifierSet**](swbemqualifierset.md).</span></span>

<span data-ttu-id="ccaae-129">**ItemIndex** também pode ser usado para obter a única instância de uma classe singleton.</span><span class="sxs-lookup"><span data-stu-id="ccaae-129">**ItemIndex** can also be used to obtain the single instance of a singleton class.</span></span>

## <a name="examples"></a><span data-ttu-id="ccaae-130">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ccaae-130">Examples</span></span>

<span data-ttu-id="ccaae-131">O exemplo de código VBScript a seguir consulta uma coleção de todas as instâncias de [**\_ processo do Win32**](/windows/desktop/CIMWin32Prov/win32-process) , em seguida, exibe os nomes dos três primeiros processos.</span><span class="sxs-lookup"><span data-stu-id="ccaae-131">The following VBScript code example queries for a collection of all the [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) instances then displays the names of the first three processes.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:\\" & _
    strComputer & "\root\cimv2")

set colProcesses = _
    objWMIService.Execquery("Select * from Win32_Process")
Wscript.Echo  colProcesses.ItemIndex(0).Name
Wscript.Echo  colProcesses.ItemIndex(1).Name
Wscript.Echo  colProcesses.ItemIndex(2).Name
```



<span data-ttu-id="ccaae-132">Há apenas uma instância do [**Win32 \_ OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem) para cada instalação do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="ccaae-132">Only one instance of [**Win32\_OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem) exists for each operating system installation.</span></span> <span data-ttu-id="ccaae-133">A criação do caminho [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) para obter a única instância é estranha, portanto, os scripts normalmente enumeram o sistema **\_ operacional do Win32** , embora apenas uma instância esteja disponível.</span><span class="sxs-lookup"><span data-stu-id="ccaae-133">Creating the [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) path to obtain the single instance is awkward so scripts normally enumerate **Win32\_OperatingSystem** even though only one instance is available.</span></span> <span data-ttu-id="ccaae-134">O exemplo de código VBScript a seguir mostra como usar o método **ItemIndex** para chegar a um **sistema \_ operacional Win32** sem usar um loop **for each** .</span><span class="sxs-lookup"><span data-stu-id="ccaae-134">The following VBScript code example shows how to use the **ItemIndex** method to get to the one **Win32\_OperatingSystem** without using a **For Each** loop.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

Set colOperatingSystems = objWMIService.ExecQuery _
    ("Select * from Win32_OperatingSystem")

Wscript.Echo "Caption: " & colOperatingSystems.ItemIndex(0).Caption
```



<span data-ttu-id="ccaae-135">O exemplo de código VBScript a seguir obtém instâncias associadas ao sistema [**\_ operacional Win32**](/windows/desktop/CIMWin32Prov/win32-operatingsystem), como [**Win32 \_ SystemOperatingSystem**](/windows/desktop/CIMWin32Prov/win32-systemoperatingsystem).</span><span class="sxs-lookup"><span data-stu-id="ccaae-135">The following VBScript code example gets instances associated with [**Win32\_OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem), such as [**Win32\_SystemOperatingSystem**](/windows/desktop/CIMWin32Prov/win32-systemoperatingsystem).</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:\\" & _
    strComputer & "\root\cimv2")

set colOS = _
    objWMIService.Execquery("Select * from Win32_OperatingSystem")
    Wscript.Echo  colOS.ItemIndex(0).Name

set colAssociators = colOS.ItemIndex(0).Associators_
    For Each Associator in colAssociators 
        Wscript.Echo Associator.Path_.RelPath  
    Next
```



<span data-ttu-id="ccaae-136">A saída de exemplo de código a seguir mostra as instâncias associadas ao sistema [**\_ operacional Win32**](/windows/desktop/CIMWin32Prov/win32-operatingsystem).</span><span class="sxs-lookup"><span data-stu-id="ccaae-136">The following code example output shows instances associated with [**Win32\_OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem).</span></span>

``` syntax
Windows Server 2008 
    |C:\Windows|\Device\Harddisk0\Partition1
Win32_ComputerSystem.Name="Test1"
Win32_AutochkSetting.SettingID="Windows Server 2008 
    |C:\\Windows|\\Device\\Harddisk0\\Partition1"
```

## <a name="requirements"></a><span data-ttu-id="ccaae-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ccaae-137">Requirements</span></span>



| <span data-ttu-id="ccaae-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="ccaae-138">Requirement</span></span> | <span data-ttu-id="ccaae-139">Valor</span><span class="sxs-lookup"><span data-stu-id="ccaae-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ccaae-140">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ccaae-140">Minimum supported client</span></span><br/> | <span data-ttu-id="ccaae-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ccaae-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ccaae-142">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ccaae-142">Minimum supported server</span></span><br/> | <span data-ttu-id="ccaae-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ccaae-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ccaae-144">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ccaae-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="ccaae-145"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ccaae-145"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="ccaae-146">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="ccaae-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="ccaae-147"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ccaae-147"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ccaae-148">DLL</span><span class="sxs-lookup"><span data-stu-id="ccaae-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ccaae-149"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ccaae-149"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="ccaae-150">CLSID</span><span class="sxs-lookup"><span data-stu-id="ccaae-150">CLSID</span></span><br/>                    | <span data-ttu-id="ccaae-151">\_SWBEMOBJECTSET CLSID</span><span class="sxs-lookup"><span data-stu-id="ccaae-151">CLSID\_SWbemObjectSet</span></span><br/>                                                        |
| <span data-ttu-id="ccaae-152">IID</span><span class="sxs-lookup"><span data-stu-id="ccaae-152">IID</span></span><br/>                      | <span data-ttu-id="ccaae-153">ISWbemObjectSet de IID \_</span><span class="sxs-lookup"><span data-stu-id="ccaae-153">IID\_ISWbemObjectSet</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="ccaae-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="ccaae-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccaae-155">**SWbemObjectSet**</span><span class="sxs-lookup"><span data-stu-id="ccaae-155">**SWbemObjectSet**</span></span>](swbemobjectset.md)
</dt> </dl>

 

