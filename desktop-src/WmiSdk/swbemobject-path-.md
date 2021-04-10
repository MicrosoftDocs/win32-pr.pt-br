---
description: A \_ propriedade Path do objeto SWbemObject retorna um objeto SWbemObjectPath que representa o caminho do objeto da classe ou instância atual. Essa propriedade pode ser passada como um parâmetro para métodos que exigem um caminho de objeto.
ms.assetid: 85a55159-5f10-49b5-bc37-39d7b4dfccd7
ms.tgt_platform: multiple
title: Propriedade SWbemObject.Path_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Path_
- ISWbemObject.Path_
- ISWbemObject.get_Path_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 773f6f9bb04aa31290bc351550a45d849d74e06f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170190"
---
# <a name="swbemobjectpath_-property"></a><span data-ttu-id="26483-104">Propriedade SWbemObject. Path \_</span><span class="sxs-lookup"><span data-stu-id="26483-104">SWbemObject.Path\_ property</span></span>

<span data-ttu-id="26483-105">A **propriedade \_ Path** do objeto [**SWbemObject**](swbemobject.md) retorna um objeto [**SWbemObjectPath**](swbemobjectpath.md) que representa o caminho do objeto da classe ou instância atual.</span><span class="sxs-lookup"><span data-stu-id="26483-105">The **Path\_** property of the [**SWbemObject**](swbemobject.md) object returns an [**SWbemObjectPath**](swbemobjectpath.md) object that represents the object path of the current class or instance.</span></span> <span data-ttu-id="26483-106">Essa propriedade pode ser passada como um parâmetro para métodos que exigem um caminho de objeto.</span><span class="sxs-lookup"><span data-stu-id="26483-106">This property can be passed as a parameter to methods that require an object path.</span></span>

<span data-ttu-id="26483-107">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="26483-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="26483-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="26483-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="26483-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="26483-109">Syntax</span></span>


```VB
SWbemObject.Path_ As Object
```



## <a name="property-value"></a><span data-ttu-id="26483-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="26483-110">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="26483-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="26483-111">Remarks</span></span>

<span data-ttu-id="26483-112">Somente a propriedade [**Class**](swbemobjectpath-class.md) da instância [**SWbemObjectPath**](swbemobjectpath.md) retornada pode ser modificada.</span><span class="sxs-lookup"><span data-stu-id="26483-112">Only the [**Class**](swbemobjectpath-class.md) property of the returned [**SWbemObjectPath**](swbemobjectpath.md) instance can be modified.</span></span> <span data-ttu-id="26483-113">Se você tentar modificar qualquer outra propriedade ou tentar chamar os métodos [**SetAsClass**](swbemobjectpath-setasclass.md) ou [**SetAsSingleton**](swbemobjectpath-setassingleton.md), receberá um erro **wbemErrReadOnly** .</span><span class="sxs-lookup"><span data-stu-id="26483-113">If you try to modify any other property, or try to call the methods [**SetAsClass**](swbemobjectpath-setasclass.md) or [**SetAsSingleton**](swbemobjectpath-setassingleton.md), you will get a **wbemErrReadOnly** error.</span></span>

<span data-ttu-id="26483-114">Por isso, você não pode modificar o objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que é o valor da propriedade [**Keys**](swbemobjectpath-keys.md) da instância [**SWbemObjectPath**](swbemobjectpath.md) retornada.</span><span class="sxs-lookup"><span data-stu-id="26483-114">Because of this, you cannot modify the [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that is the value of the [**Keys**](swbemobjectpath-keys.md) property of the returned [**SWbemObjectPath**](swbemobjectpath.md) instance.</span></span> <span data-ttu-id="26483-115">Se você tentar chamar os métodos [**Add**](swbemnamedvalueset-add.md), [**Remove**](swbemnamedvalueset-remove.md)ou [**DeleteAll**](swbemnamedvalueset-deleteall.md) nesse valor, receberá um erro wbemErrReadOnly.</span><span class="sxs-lookup"><span data-stu-id="26483-115">If you try to call the [**Add**](swbemnamedvalueset-add.md), [**Remove**](swbemnamedvalueset-remove.md), or [**DeleteAll**](swbemnamedvalueset-deleteall.md) methods on this value, you will get a wbemErrReadOnly error.</span></span> <span data-ttu-id="26483-116">Além disso, você não pode modificar nenhum [**SWbemNamedValue**](swbemnamedvalue.md) obtido dessa coleção.</span><span class="sxs-lookup"><span data-stu-id="26483-116">Furthermore, you cannot modify any [**SWbemNamedValue**](swbemnamedvalue.md) obtained from this collection.</span></span> <span data-ttu-id="26483-117">As tentativas de modificar a propriedade **Value** retornam o mesmo código de erro.</span><span class="sxs-lookup"><span data-stu-id="26483-117">Attempts to modify the **Value** property return the same error code.</span></span>

<span data-ttu-id="26483-118">No entanto, se você chamar [**SWbemObject \_ . Clone**](swbemobject-clone-.md) para criar uma cópia, a propriedade [**SWbemObjectPath. Path**](swbemobjectpath-path.md) da cópia será totalmente modificável.</span><span class="sxs-lookup"><span data-stu-id="26483-118">However, if you call [**SWbemObject.Clone\_**](swbemobject-clone-.md) to create a copy, the [**SWbemObjectPath.Path**](swbemobjectpath-path.md) property of the copy is fully modifiable.</span></span>

## <a name="examples"></a><span data-ttu-id="26483-119">Exemplos</span><span class="sxs-lookup"><span data-stu-id="26483-119">Examples</span></span>

<span data-ttu-id="26483-120">O exemplo de código a seguir, obtido da [lista de todas as classes cimv2 do WMI](https://Gallery.TechNet.Microsoft.Com/5649568b-074e-4f5d-be52-e8b7d8fe4517) na galeria do TechNet, usa a propriedade Path \_ para listar todas as classes cimv2 do WMI.</span><span class="sxs-lookup"><span data-stu-id="26483-120">The following code sample, taken from [List All the WMI cimV2 Classes](https://Gallery.TechNet.Microsoft.Com/5649568b-074e-4f5d-be52-e8b7d8fe4517) in the TechNet Gallery, uses the Path\_ property to list all the WMI cimV2 classes.</span></span>


```VB
strComputer = "." 
Set objWMIService=GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & _  
    strComputer & "\root\cimv2") 
  
For Each objclass in objWMIService.SubclassesOf() 
    Wscript.Echo objClass.Path_.Class 
Next 
```



## <a name="requirements"></a><span data-ttu-id="26483-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="26483-121">Requirements</span></span>



| <span data-ttu-id="26483-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="26483-122">Requirement</span></span> | <span data-ttu-id="26483-123">Valor</span><span class="sxs-lookup"><span data-stu-id="26483-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="26483-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="26483-124">Minimum supported client</span></span><br/> | <span data-ttu-id="26483-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="26483-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="26483-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="26483-126">Minimum supported server</span></span><br/> | <span data-ttu-id="26483-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="26483-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="26483-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="26483-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="26483-129"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="26483-129"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="26483-130">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="26483-130">Type library</span></span><br/>             | <dl> <span data-ttu-id="26483-131"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="26483-131"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="26483-132">DLL</span><span class="sxs-lookup"><span data-stu-id="26483-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26483-133"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26483-133"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="26483-134">CLSID</span><span class="sxs-lookup"><span data-stu-id="26483-134">CLSID</span></span><br/>                    | <span data-ttu-id="26483-135">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="26483-135">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="26483-136">IID</span><span class="sxs-lookup"><span data-stu-id="26483-136">IID</span></span><br/>                      | <span data-ttu-id="26483-137">ISWbemObject de IID \_</span><span class="sxs-lookup"><span data-stu-id="26483-137">IID\_ISWbemObject</span></span><br/>                                                            |



 

 




