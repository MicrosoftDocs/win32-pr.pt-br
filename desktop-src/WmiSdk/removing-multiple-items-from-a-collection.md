---
description: Se você tentar remover mais de um item em uma coleção, poderá descobrir que alguns itens não foram removidos.
ms.assetid: 7c82321e-059f-497c-8561-33c3e9306d41
ms.tgt_platform: multiple
title: Removendo vários itens de uma coleção WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17795378f5215977e5e7c2d0afd745c5d02fe6b294d062fcdbcf82f7ccc15351
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992436"
---
# <a name="removing-multiple-items-from-a-wmi-collection"></a>Removendo vários itens de uma coleção WMI

Se você tentar remover mais de um item em uma coleção, poderá descobrir que alguns itens não foram removidos. Não é possível iterar uma coleção ao remover itens, porque quando você remove um elemento de uma coleção, o ponteiro da coleção é movido para o próximo elemento. Por exemplo, uma tentativa de remover todos os itens de uma coleção resulta na remoção de todos os outros itens. Você pode ver esse problema ao remover itens com os métodos [**SWbemQualifierSet.Remove**](swbemqualifierset-remove.md) ou [**SWbemPropertySet.Remove.**](swbempropertyset-remove.md) Você pode evitar esse problema fazendo um loop pela coleção e colocando os nomes dos itens a remover em uma matriz. Em seguida, você pode fazer um loop pela matriz e excluir os itens nomeados na matriz. As coleções, como [**SWbemNamedValueSet,**](swbemnamedvalueset.md) [**SWbemPrivilegeSet**](swbemprivilegeset.md)e [**SWbemRefresher,**](swbemrefresher.md)também têm um método que exclui todos os itens no contêiner de atualização.

O script a seguir ilustra como remover vários itens de uma coleção.


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



Não é possível remover propriedades e qualificadores em uma instância de classe ou classe derivada que tenha propriedades herdadas. Essa tentativa de exclusão gera um erro e a propriedade ou qualificador não é removido; em vez disso, o WMI redefine a propriedade ou o qualificador para o valor padrão. No caso de uma classe derivada com propriedades herdadas, o WMI redefine a propriedade herdada para o valor padrão da propriedade na classe pai.

Para obter mais informações, consulte [Manipulando informações de classe e instância](manipulating-class-and-instance-information.md), [Acessando](accessing-a-collection.md)uma coleção e [Removendo](removing-a-single-item-from-a-collection.md)um único item de uma coleção .

 

 



