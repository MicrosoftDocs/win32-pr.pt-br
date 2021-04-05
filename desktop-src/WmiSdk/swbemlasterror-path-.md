---
description: A \_ propriedade Path do objeto SWbemLastError retorna um objeto SWbemObjectPath que representa o caminho do objeto da classe ou instância atual. Essa propriedade pode ser passada como um parâmetro para métodos que exigem um caminho de objeto.
ms.assetid: 5472e463-54cb-4ba2-8c00-08b70013e38d
ms.tgt_platform: multiple
title: Propriedade SWbemLastError.Path_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLastError.Path_
- ISWbemLastError.Path_
- ISWbemLastError.get_Path_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c979fd76ffb4ee97f62362d53fac4151de17bae6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011234"
---
# <a name="swbemlasterrorpath_-property"></a><span data-ttu-id="f5829-104">Propriedade SWbemLastError. Path \_</span><span class="sxs-lookup"><span data-stu-id="f5829-104">SWbemLastError.Path\_ property</span></span>

<span data-ttu-id="f5829-105">A **propriedade \_ Path** do objeto [**SWbemLastError**](swbemlasterror.md) retorna um objeto [**SWbemObjectPath**](swbemobjectpath.md) que representa o caminho do objeto da classe ou instância atual.</span><span class="sxs-lookup"><span data-stu-id="f5829-105">The **Path\_** property of the [**SWbemLastError**](swbemlasterror.md) object returns an [**SWbemObjectPath**](swbemobjectpath.md) object that represents the object path of the current class or instance.</span></span> <span data-ttu-id="f5829-106">Essa propriedade pode ser passada como um parâmetro para métodos que exigem um caminho de objeto.</span><span class="sxs-lookup"><span data-stu-id="f5829-106">This property can be passed as a parameter to methods that require an object path.</span></span>

<span data-ttu-id="f5829-107">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="f5829-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="f5829-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="f5829-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5829-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f5829-109">Syntax</span></span>


```VB
SWbemLastError.Path_ As Object
```



## <a name="property-value"></a><span data-ttu-id="f5829-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="f5829-110">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="f5829-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="f5829-111">Remarks</span></span>

<span data-ttu-id="f5829-112">Somente a propriedade [**Class**](swbemobjectpath-class.md) da instância [**SWbemObjectPath**](swbemobjectpath.md) retornada pode ser modificada.</span><span class="sxs-lookup"><span data-stu-id="f5829-112">Only the [**Class**](swbemobjectpath-class.md) property of the returned [**SWbemObjectPath**](swbemobjectpath.md) instance can be modified.</span></span> <span data-ttu-id="f5829-113">Se você tentar modificar qualquer outra propriedade ou tentar chamar os métodos [**SetAsClass**](swbemobjectpath-setasclass.md) ou [**SetAsSingleton**](swbemobjectpath-setassingleton.md) , obterá um erro de **wbemErrReadOnly**.</span><span class="sxs-lookup"><span data-stu-id="f5829-113">If you try to modify any other property, or try to call the [**SetAsClass**](swbemobjectpath-setasclass.md) or [**SetAsSingleton**](swbemobjectpath-setassingleton.md) methods, you get an error of **wbemErrReadOnly**.</span></span>

<span data-ttu-id="f5829-114">Por isso, você não pode modificar o objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que é o valor da propriedade [**Keys**](swbemobjectpath-keys.md) da instância [**SWbemObjectPath**](swbemobjectpath.md) retornada.</span><span class="sxs-lookup"><span data-stu-id="f5829-114">Because of this, you cannot modify the [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that is the value of the [**Keys**](swbemobjectpath-keys.md) property of the returned [**SWbemObjectPath**](swbemobjectpath.md) instance.</span></span> <span data-ttu-id="f5829-115">Se você tentar chamar os métodos [**Add**](swbemnamedvalueset-add.md), [**Remove**](swbemnamedvalueset-remove.md)ou [**DeleteAll**](swbemnamedvalueset-deleteall.md) nesse valor, obterá um erro **wbemErrReadOnly** .</span><span class="sxs-lookup"><span data-stu-id="f5829-115">If you try to call the [**Add**](swbemnamedvalueset-add.md), [**Remove**](swbemnamedvalueset-remove.md), or [**DeleteAll**](swbemnamedvalueset-deleteall.md) methods on this value, you get a **wbemErrReadOnly** error.</span></span> <span data-ttu-id="f5829-116">Além disso, você não pode modificar nenhum [**SWbemNamedValue**](swbemnamedvalue.md) obtido dessa coleção.</span><span class="sxs-lookup"><span data-stu-id="f5829-116">Furthermore, you cannot modify any [**SWbemNamedValue**](swbemnamedvalue.md) obtained from this collection.</span></span> <span data-ttu-id="f5829-117">As tentativas de modificar a propriedade [**Value**](swbemnamedvalue-value.md) retornam o mesmo código de erro.</span><span class="sxs-lookup"><span data-stu-id="f5829-117">Attempts to modify the [**Value**](swbemnamedvalue-value.md) property return the same error code.</span></span>

<span data-ttu-id="f5829-118">No entanto, se você chamar [**SWbemObject \_ . Clone**](swbemobject-clone-.md) para criar uma cópia, a propriedade [**\_ Path**](swbemobject-path-.md) da cópia será totalmente modificável.</span><span class="sxs-lookup"><span data-stu-id="f5829-118">However, if you call [**SWbemObject.Clone\_**](swbemobject-clone-.md) to create a copy, the [**Path\_**](swbemobject-path-.md) property of the copy is fully modifiable.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5829-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f5829-119">Requirements</span></span>



| <span data-ttu-id="f5829-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5829-120">Requirement</span></span> | <span data-ttu-id="f5829-121">Valor</span><span class="sxs-lookup"><span data-stu-id="f5829-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f5829-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f5829-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f5829-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f5829-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f5829-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f5829-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f5829-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f5829-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f5829-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f5829-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5829-127"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5829-127"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="f5829-128">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="f5829-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="f5829-129"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f5829-129"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f5829-130">DLL</span><span class="sxs-lookup"><span data-stu-id="f5829-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f5829-131"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5829-131"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="f5829-132">CLSID</span><span class="sxs-lookup"><span data-stu-id="f5829-132">CLSID</span></span><br/>                    | <span data-ttu-id="f5829-133">\_SWBEMLASTERROR CLSID</span><span class="sxs-lookup"><span data-stu-id="f5829-133">CLSID\_SWbemLastError</span></span><br/>                                                        |
| <span data-ttu-id="f5829-134">IID</span><span class="sxs-lookup"><span data-stu-id="f5829-134">IID</span></span><br/>                      | <span data-ttu-id="f5829-135">ISWbemLastError de IID \_</span><span class="sxs-lookup"><span data-stu-id="f5829-135">IID\_ISWbemLastError</span></span><br/>                                                         |



 

 




