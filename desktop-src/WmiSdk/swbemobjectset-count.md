---
description: Use a propriedade Count do objeto SWbemObjectSet para determinar quantos itens estão em uma coleção SWbemObjectSet. Esta propriedade é somente para leitura.
ms.assetid: ad3d1265-a11e-4962-b1f3-60092d2f79ef
ms.tgt_platform: multiple
title: Propriedade SWbemObjectSet. Count (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectSet.Count
- ISWbemObjectSet.Count
- ISWbemObjectSet.get_Count
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 3154e22bbdbc75080ceebdf8b1eef602cf5c3be3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105764388"
---
# <a name="swbemobjectsetcount-property"></a><span data-ttu-id="26d67-104">Propriedade SWbemObjectSet. Count</span><span class="sxs-lookup"><span data-stu-id="26d67-104">SWbemObjectSet.Count property</span></span>

<span data-ttu-id="26d67-105">Use a propriedade **Count** do objeto [**SWbemObjectSet**](swbemobjectset.md) para determinar quantos itens estão em uma coleção **SWbemObjectSet** .</span><span class="sxs-lookup"><span data-stu-id="26d67-105">Use the **Count** property of the [**SWbemObjectSet**](swbemobjectset.md) object to determine how many items are in an **SWbemObjectSet** collection.</span></span> <span data-ttu-id="26d67-106">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="26d67-106">This property is read-only.</span></span>

<span data-ttu-id="26d67-107">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="26d67-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="26d67-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="26d67-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="26d67-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="26d67-109">Syntax</span></span>


```VB
SWbemObjectSet.Count As Integer
```



## <a name="property-value"></a><span data-ttu-id="26d67-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="26d67-110">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="26d67-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="26d67-111">Remarks</span></span>

<span data-ttu-id="26d67-112">Um ponto a ser cuidadoso ao usar Count é que o WMI não mantém uma contagem em execução do número de itens em uma coleção.</span><span class="sxs-lookup"><span data-stu-id="26d67-112">One thing to be careful of when using Count is that WMI does not keep a running tally of the number of items in a collection.</span></span> <span data-ttu-id="26d67-113">Se você solicitar a contagem de uma coleção, o WMI não poderá responder instantaneamente com um número; em vez disso, ele deve contar literalmente os itens, enumerando a coleção inteira.</span><span class="sxs-lookup"><span data-stu-id="26d67-113">If you request Count for a collection, WMI cannot instantly respond with a number; instead, it must literally count the items, enumerating the entire collection.</span></span> <span data-ttu-id="26d67-114">Para uma coleção que tem relativamente poucos itens, como serviços, essa enumeração provavelmente levará menos de um segundo.</span><span class="sxs-lookup"><span data-stu-id="26d67-114">For a collection that has relatively few items, such as services, this enumeration likely takes less than a second.</span></span> <span data-ttu-id="26d67-115">A contagem do número de eventos em uma coleção de log de eventos, no entanto, pode demorar consideravelmente mais.</span><span class="sxs-lookup"><span data-stu-id="26d67-115">Counting the number of events in an event log collection, however, can take considerably longer.</span></span>

<span data-ttu-id="26d67-116">E, em seguida, suponha que você deseja exibir os valores de propriedade para cada evento na coleção.</span><span class="sxs-lookup"><span data-stu-id="26d67-116">And then suppose you want to display the property values for every event in the collection.</span></span> <span data-ttu-id="26d67-117">Nesse caso, o WMI terá que enumerar toda a coleção uma segunda vez.</span><span class="sxs-lookup"><span data-stu-id="26d67-117">If so, WMI will have to enumerate the entire collection a second time.</span></span>

> [!Note]  
> <span data-ttu-id="26d67-118">Se você tentar obter essa propriedade de um objeto [**SWbemObjectSet**](swbemobjectset.md) que é retornado de um método em que os sinalizadores especificados estão incluídos no sinalizador wbemFlagForwardOnly, você receberá um erro wbemErrFailed.</span><span class="sxs-lookup"><span data-stu-id="26d67-118">If you attempt to get this property from an [**SWbemObjectSet**](swbemobjectset.md) object that is returned from a method where the specified flags are included the wbemFlagForwardOnly flag, you will get an wbemErrFailed error.</span></span>

 

## <a name="examples"></a><span data-ttu-id="26d67-119">Exemplos</span><span class="sxs-lookup"><span data-stu-id="26d67-119">Examples</span></span>

<span data-ttu-id="26d67-120">Na maior parte, a única coisa que você fará com um SWbemObjectSet é enumerar todos os objetos contidos na coleção em si.</span><span class="sxs-lookup"><span data-stu-id="26d67-120">For the most part, the only thing you will ever do with an SWbemObjectSet is enumerate all the objects contained within the collection itself.</span></span> <span data-ttu-id="26d67-121">No entanto, a contagem de contagem que pode ser útil no script de administração do sistema.</span><span class="sxs-lookup"><span data-stu-id="26d67-121">However, the Count Count that can be useful in system administration scripting.</span></span> <span data-ttu-id="26d67-122">Como o nome implica, Count informa o número de itens na coleção.</span><span class="sxs-lookup"><span data-stu-id="26d67-122">As the name implies, Count tells you the number of items in the collection.</span></span> <span data-ttu-id="26d67-123">Por exemplo, esse script recupera uma coleção de todos os serviços instalados em um computador e, em seguida, ecoa o número total de serviços encontrados:</span><span class="sxs-lookup"><span data-stu-id="26d67-123">For example, this script retrieves a collection of all the services installed on a computer and then echoes the total number of services found:</span></span>


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colSWbemObjectSet = objSWbemServices.InstancesOf("Win32_Service")
Wscript.Echo "Services installed on target computer: " & colSWbemObjectSet.Count

```



<span data-ttu-id="26d67-124">O que torna a contagem útil é que ele pode informar se uma instância específica está disponível em um computador.</span><span class="sxs-lookup"><span data-stu-id="26d67-124">What makes Count useful is that it can tell you whether a specific instance is available on a computer.</span></span> <span data-ttu-id="26d67-125">Por exemplo, esse script recupera uma coleção de todos os serviços em um computador que tem o nome W3SVC.</span><span class="sxs-lookup"><span data-stu-id="26d67-125">For example, this script retrieves a collection of all the services on a computer that have the Name W3SVC.</span></span> <span data-ttu-id="26d67-126">Se a contagem for 0 (e for válida para que as coleções não tenham nenhuma instância), isso significará que o serviço W3SVC não está instalado no computador.</span><span class="sxs-lookup"><span data-stu-id="26d67-126">If the Count is 0 (and it is valid for collections to have no instances), that means the W3SVC service is not installed on the computer.</span></span>


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colSWbemObjectSet = objSWbemServices.ExecQuery _
    ("SELECT * FROM Win32_Service WHERE Name='w3svc'")
If colSWbemObjectSet.Count = 0 Then
    Wscript.Echo "W3SVC service is not installed on target computer."
Else
    For Each objSWbemObject In colSWbemObjectSet
        ' Perform task on World Wide Web Publishing service.
    Next
End If
```



## <a name="requirements"></a><span data-ttu-id="26d67-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="26d67-127">Requirements</span></span>



| <span data-ttu-id="26d67-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="26d67-128">Requirement</span></span> | <span data-ttu-id="26d67-129">Valor</span><span class="sxs-lookup"><span data-stu-id="26d67-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="26d67-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="26d67-130">Minimum supported client</span></span><br/> | <span data-ttu-id="26d67-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="26d67-131">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="26d67-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="26d67-132">Minimum supported server</span></span><br/> | <span data-ttu-id="26d67-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="26d67-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="26d67-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="26d67-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="26d67-135"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="26d67-135"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="26d67-136">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="26d67-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="26d67-137"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="26d67-137"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="26d67-138">DLL</span><span class="sxs-lookup"><span data-stu-id="26d67-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26d67-139"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26d67-139"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="26d67-140">CLSID</span><span class="sxs-lookup"><span data-stu-id="26d67-140">CLSID</span></span><br/>                    | <span data-ttu-id="26d67-141">\_SWBEMOBJECTSET CLSID</span><span class="sxs-lookup"><span data-stu-id="26d67-141">CLSID\_SWbemObjectSet</span></span><br/>                                                        |
| <span data-ttu-id="26d67-142">IID</span><span class="sxs-lookup"><span data-stu-id="26d67-142">IID</span></span><br/>                      | <span data-ttu-id="26d67-143">ISWbemObjectSet de IID \_</span><span class="sxs-lookup"><span data-stu-id="26d67-143">IID\_ISWbemObjectSet</span></span><br/>                                                         |



 

 




