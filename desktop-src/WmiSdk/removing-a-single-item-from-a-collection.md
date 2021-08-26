---
description: Uma das principais finalidades de acessar uma coleção é remover um item da coleção. Você pode remover um item de uma coleção com uma chamada para o método SWbemPropertySet.Remove. Esse método não está disponível para SWbemObjectSet ou SWbemMethodSet.
ms.assetid: 4a71029c-9fe1-4348-9f78-daa345728e8d
ms.tgt_platform: multiple
title: Removendo um único item de uma coleção WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50364173aff9f28362878e84d5f3ddb496e430521dc5b1bb92bbc11e7e6b528c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119995896"
---
# <a name="removing-a-single-item-from-a-wmi-collection"></a>Removendo um único item de uma coleção WMI

Uma das principais finalidades de acessar uma coleção é remover um item da coleção. Você pode remover um item de uma coleção com uma chamada para o [**método SWbemPropertySet.Remove.**](swbempropertyset-remove.md) Esse método não está disponível para [**SWbemObjectSet**](swbemobjectset.md) ou [**SWbemMethodSet.**](swbemmethodset.md)

Os itens são removidos por nome [**de SWbemPropertySet,**](swbempropertyset.md) [**SWbemQualifierSet**](swbemqualifierset.md)e [**SWbemNamedValueSet**](swbemnamedvalueset.md). No entanto, os itens [**em SWbemRefresher**](swbemrefresher.md) são removidos por índice e [**de SWbemPrivilegeSet**](swbemprivilegeset.md) pela constante que representa o nome do privilégio.

**Para remover um item de uma coleção**

-   O exemplo de código a seguir mostra como remover o item com uma chamada para o [**método SWbemPropertySet.Remove.**](swbempropertyset-remove.md)

    ```VB
    oclass.Properties_.Remove "Prop2"
    ```

    

    O exemplo a seguir cria uma nova classe chamada "NewClass" no namespace padrão raiz e \\ adiciona três propriedades a ela. Em seguida, o script usa o código do exemplo anterior para excluir a segunda propriedade.

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

    

Para obter mais informações, consulte [Manipulando informações de classe e instância](manipulating-class-and-instance-information.md), [Acessando uma coleção](accessing-a-collection.md)e [Removendo vários itens de uma coleção](removing-multiple-items-from-a-collection.md).

 

 



