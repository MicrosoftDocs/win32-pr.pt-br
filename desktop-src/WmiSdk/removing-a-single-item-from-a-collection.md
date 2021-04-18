---
description: Uma das principais finalidades de acessar uma coleção é remover um item da coleção. Você pode remover um item de uma coleção com uma chamada para o método SWbemPropertySet. Remove. Este método não está disponível para SWbemObjectSet ou SWbemMethodSet.
ms.assetid: 4a71029c-9fe1-4348-9f78-daa345728e8d
ms.tgt_platform: multiple
title: Removendo um único item de uma coleção WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6dabeb3ff2e7e70cf6fe25f1ddfb0b14032119d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789424"
---
# <a name="removing-a-single-item-from-a-wmi-collection"></a><span data-ttu-id="ea3e9-105">Removendo um único item de uma coleção WMI</span><span class="sxs-lookup"><span data-stu-id="ea3e9-105">Removing a Single Item from a WMI Collection</span></span>

<span data-ttu-id="ea3e9-106">Uma das principais finalidades de acessar uma coleção é remover um item da coleção.</span><span class="sxs-lookup"><span data-stu-id="ea3e9-106">One of the main purposes of accessing a collection is to remove an item from the collection.</span></span> <span data-ttu-id="ea3e9-107">Você pode remover um item de uma coleção com uma chamada para o método [**SWbemPropertySet. Remove**](swbempropertyset-remove.md) .</span><span class="sxs-lookup"><span data-stu-id="ea3e9-107">You can remove an item from a collection with a call to the [**SWbemPropertySet.Remove**](swbempropertyset-remove.md) method.</span></span> <span data-ttu-id="ea3e9-108">Este método não está disponível para [**SWbemObjectSet**](swbemobjectset.md) ou [**SWbemMethodSet**](swbemmethodset.md).</span><span class="sxs-lookup"><span data-stu-id="ea3e9-108">This method is not available for [**SWbemObjectSet**](swbemobjectset.md) or [**SWbemMethodSet**](swbemmethodset.md).</span></span>

<span data-ttu-id="ea3e9-109">Os itens são removidos pelo nome de [**SWbemPropertySet**](swbempropertyset.md), [**SWbemQualifierSet**](swbemqualifierset.md)e [**SWbemNamedValueSet**](swbemnamedvalueset.md).</span><span class="sxs-lookup"><span data-stu-id="ea3e9-109">Items are removed by name from [**SWbemPropertySet**](swbempropertyset.md), [**SWbemQualifierSet**](swbemqualifierset.md), and [**SWbemNamedValueSet**](swbemnamedvalueset.md).</span></span> <span data-ttu-id="ea3e9-110">No entanto, os itens em [**SWbemRefresher**](swbemrefresher.md) são removidos pelo índice e de [**SWbemPrivilegeSet**](swbemprivilegeset.md) pela constante que representa o nome do privilégio.</span><span class="sxs-lookup"><span data-stu-id="ea3e9-110">However, items in [**SWbemRefresher**](swbemrefresher.md) are removed by index and from [**SWbemPrivilegeSet**](swbemprivilegeset.md) by the constant that represents the privilege name.</span></span>

<span data-ttu-id="ea3e9-111">**Para remover um item de uma coleção**</span><span class="sxs-lookup"><span data-stu-id="ea3e9-111">**To remove an item from a collection**</span></span>

-   <span data-ttu-id="ea3e9-112">O exemplo de código a seguir mostra como remover o item com uma chamada para o método [**SWbemPropertySet. Remove**](swbempropertyset-remove.md) .</span><span class="sxs-lookup"><span data-stu-id="ea3e9-112">The following code example shows how to remove the item with a call to the [**SWbemPropertySet.Remove**](swbempropertyset-remove.md) method.</span></span>

    ```VB
    oclass.Properties_.Remove "Prop2"
    ```

    

    <span data-ttu-id="ea3e9-113">O exemplo a seguir cria uma nova classe chamada "NewClass" no \\ namespace raiz padrão e adiciona três propriedades a ela.</span><span class="sxs-lookup"><span data-stu-id="ea3e9-113">The following example creates a new class named "NewClass" in the root\\default namespace and adds three properties to it.</span></span> <span data-ttu-id="ea3e9-114">Em seguida, o script usa o código do exemplo anterior para excluir a segunda propriedade.</span><span class="sxs-lookup"><span data-stu-id="ea3e9-114">The script then uses the code from the previous example to delete the second property.</span></span>

    ```VB
    ' Obtain an empty class and name it
    Const WBEM_CIMTYPE_STRING = 8
    Set objSWbemService = GetObject("winmgmts:root\default")
    Set objClass = objSWbemService.get()
    Wscript.Echo "Creating class NewClass"
    objClass.Path_.Class = "NewClass"

    ' Add three properties 
    For i = 1 to 3
        objClass.Properties_.Add "Prop" & i, WBEM_CIMTYPE_STRING
    Next
    Getprops()

    ' Remove the Prop2 property
    objClass.Properties_.Remove "Prop2"
    Wscript.Echo "Second property removed "
    Getprops()

    ' Write the changes to the class back
    objClass.Put_

    Sub Getprops()
        Wscript.Echo "Number of Properties = " _
            & objClass.Properties_.Count
        For Each prop in objClass.Properties_
            Wscript.Echo prop.name
        Next
    End Sub
    ```

    

<span data-ttu-id="ea3e9-115">Para obter mais informações, consulte [manipulando informações de classe e instância](manipulating-class-and-instance-information.md), [acessando uma coleção](accessing-a-collection.md)e [removendo vários itens de uma coleção](removing-multiple-items-from-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="ea3e9-115">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md), [Accessing a Collection](accessing-a-collection.md), and [Removing Multiple Items from a Collection](removing-multiple-items-from-a-collection.md).</span></span>

 

 



