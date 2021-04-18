---
description: Se você tentar remover mais de um item de uma coleção, você verá que alguns itens não são removidos.
ms.assetid: 7c82321e-059f-497c-8561-33c3e9306d41
ms.tgt_platform: multiple
title: Removendo vários itens de uma coleção de WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c44203f3279163a1de595cac8a00270dccd31c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105785939"
---
# <a name="removing-multiple-items-from-a-wmi-collection"></a><span data-ttu-id="294df-103">Removendo vários itens de uma coleção de WMI</span><span class="sxs-lookup"><span data-stu-id="294df-103">Removing Multiple Items from a WMI Collection</span></span>

<span data-ttu-id="294df-104">Se você tentar remover mais de um item de uma coleção, você verá que alguns itens não são removidos.</span><span class="sxs-lookup"><span data-stu-id="294df-104">If you attempt to remove more than one item in a collection, you may find that some items are not removed.</span></span> <span data-ttu-id="294df-105">Não é possível iterar uma coleção durante a remoção de itens, porque quando você remove um elemento de uma coleção, o ponteiro da coleção é movido para o próximo elemento.</span><span class="sxs-lookup"><span data-stu-id="294df-105">You cannot iterate a collection while removing items, because when you remove an element from a collection, the collection pointer is moved on to the next element.</span></span> <span data-ttu-id="294df-106">Por exemplo, uma tentativa de remover todos os itens de uma coleção resulta na remoção de todos os outros itens.</span><span class="sxs-lookup"><span data-stu-id="294df-106">For example, an attempt to remove all of the items from a collection results in the removal of every other item.</span></span> <span data-ttu-id="294df-107">Você pode ver esse problema ao remover itens com os métodos [**SWbemQualifierSet. Remove**](swbemqualifierset-remove.md) ou [**SWbemPropertySet. Remove**](swbempropertyset-remove.md) .</span><span class="sxs-lookup"><span data-stu-id="294df-107">You may see this problem when you are removing items with the [**SWbemQualifierSet.Remove**](swbemqualifierset-remove.md) or [**SWbemPropertySet.Remove**](swbempropertyset-remove.md) methods.</span></span> <span data-ttu-id="294df-108">Você pode evitar esse problema fazendo um loop pela coleção e colocando os nomes dos itens a serem removidos em uma matriz.</span><span class="sxs-lookup"><span data-stu-id="294df-108">You can avoid this problem by looping through the collection and putting the names of the items to remove in an array.</span></span> <span data-ttu-id="294df-109">Em seguida, você pode executar um loop na matriz e excluir os itens nomeados na matriz.</span><span class="sxs-lookup"><span data-stu-id="294df-109">You then can loop through the array and delete the items named in the array.</span></span> <span data-ttu-id="294df-110">As coleções, como [**SWbemNamedValueSet**](swbemnamedvalueset.md), [**SWbemPrivilegeSet**](swbemprivilegeset.md)e [**SWbemRefresher**](swbemrefresher.md), também têm um método que exclui todos os itens no contêiner do atualizador.</span><span class="sxs-lookup"><span data-stu-id="294df-110">The collections, such as [**SWbemNamedValueSet**](swbemnamedvalueset.md), [**SWbemPrivilegeSet**](swbemprivilegeset.md), and [**SWbemRefresher**](swbemrefresher.md), also have a method that deletes all items in the refresher container.</span></span>

<span data-ttu-id="294df-111">O script a seguir ilustra como remover vários itens de uma coleção.</span><span class="sxs-lookup"><span data-stu-id="294df-111">The following script illustrates how to remove several items from a collection.</span></span>


```VB
Const WBEM_CIMTYPE_STRING = 8    ' Value for string data type
Dim names()
Redim names (0)
set objSWbemService = GetObject("winmgmts:root\default")
set objClass = ObjSWbemService.Get()

Wscript.Echo "Creating class NewClass"
objClass.Path_.Class = "NewClass"
For i = 1 to 5
    objClass.Properties_.Add "Prop" & i, WBEM_CIMTYPE_STRING
Next
objClass.Put_
Getprops()

' Get all the property names in an array
For Each oprop in objClass.properties_
    Redim Preserve names(Ubound(names)+1)
    names(Ubound(names)-1) = oprop.name
Next
Wscript.Echo "Remove first 3 properties using array of names:"

For i = Lbound(names) to Ubound(names)-1
    If (i < 3) Then
       Wscript.Echo "Removing " & names(i)
       objClass.Properties_.Remove names(i)
    End If
Next

objClass.Put_
Wscript.Echo "Result:"
Getprops()

Sub Getprops()
    Wscript.Echo "Number of properties = " _
        & objClass.Properties_.Count
    For Each oprop in objClass.Properties_
        Wscript.Echo oprop.name
    Next
End Sub
```



Não é possível remover propriedades e qualificadores em uma instância de classe ou classe derivada que tenha propriedades herdadas. Essa tentativa de exclusão gera um erro e a propriedade ou o qualificador não é removido; em vez disso, o WMI redefine a propriedade ou o qualificador para o valor padrão. <span data-ttu-id="294df-114">No caso de uma classe derivada com propriedades herdadas, o WMI redefine a propriedade herdada como o valor padrão da propriedade na classe pai.</span><span class="sxs-lookup"><span data-stu-id="294df-114">In the case of a derived class with inherited properties, WMI resets the inherited property to the default value of the property in the parent class.</span></span>

<span data-ttu-id="294df-115">Para obter mais informações, consulte [manipulando informações de classe e instância](manipulating-class-and-instance-information.md), [acessando uma coleção](accessing-a-collection.md)e [removendo um único item de uma coleção](removing-a-single-item-from-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="294df-115">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md), [Accessing a Collection](accessing-a-collection.md), and [Removing a Single Item from a Collection](removing-a-single-item-from-a-collection.md).</span></span>

 

 



