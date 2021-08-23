---
title: Enumerando objetos
description: Para exibir o objeto filho de um contêiner, como uma UO (unidade organizacional), enumere o objeto de contêiner.
ms.assetid: 06995281-d269-42ce-839f-2938a2f6af22
ms.tgt_platform: multiple
keywords:
- Enumerando objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8e4bcead2d3fc8f98daeada89cdd10b3ad30bed855563efd89b3eebce8995f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118961945"
---
# <a name="enumerating-objects"></a>Enumerando objetos

Para exibir o objeto filho de um contêiner, como uma UO (unidade organizacional), enumere o objeto de contêiner. Para fazer uma analogia a um sistema de arquivos, o objeto filho corresponderia aos arquivos no diretório, enquanto o contêiner, que é o objeto pai, corresponderia ao próprio diretório. Você também pode usar a operação de enumeração quando quiser obter o objeto pai de um objeto .

Ao enumerar um objeto, você realmente se vincula a um objeto no diretório e uma interface [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) é retornada em cada objeto.

O exemplo de código a seguir mostra como enumerar os filhos de um contêiner.


```VB
Dim ou As IADs
' Bind to an object using its DN.
On Error GoTo Cleanup

Set ou = GetObject("LDAP://OU=Sales,DC=Fabrikam,DC=COM")

For each child in ou
    Debug.Print child.Name
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set ou = Nothing
```



Você pode filtrar os tipos de objetos retornados da enumeração . Por exemplo, para exibir apenas usuários e grupos, use o exemplo de código a seguir antes da enumeração .


```VB
Ou.Filter = Array("user", "group")
```



Se você tiver uma referência de objeto, poderá obter o pai do objeto usando a [**propriedade Pai IADs.**](/windows/desktop/api/Iads/nn-iads-iads) [](iads-property-methods.md) O exemplo de código a seguir mostra como se vincular ao objeto pai.


```VB
parentPath = obj.Parent
Set parent = GetObject(parentPath)
```



Para obter mais informações, consulte [Enumerando objetos ADSI](enumerating-adsi-objects.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Pesquisando objetos](searching-for-objects.md)
</dt> </dl>

 

 




