---
title: Enumerando objetos
description: Para exibir o objeto filho de um contêiner, como uma UO (unidade organizacional), enumere o objeto de contêiner.
ms.assetid: 06995281-d269-42ce-839f-2938a2f6af22
ms.tgt_platform: multiple
keywords:
- Enumerando objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c26b78f084f95ac59c909b326be10d42c4a6696a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822220"
---
# <a name="enumerating-objects"></a>Enumerando objetos

Para exibir o objeto filho de um contêiner, como uma UO (unidade organizacional), enumere o objeto de contêiner. Para tornar uma analogia com um sistema de arquivos, o objeto filho corresponderia aos arquivos no diretório, enquanto o contêiner, que é o objeto pai, corresponderia ao próprio diretório. Você também pode usar a operação enumerar quando desejar obter o objeto pai de um objeto.

Ao enumerar um objeto, você realmente se associa a um objeto no diretório e uma interface [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) é retornada em cada objeto.

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



Você pode filtrar os tipos de objetos retornados da enumeração. Por exemplo, para exibir apenas usuários e grupos, use o exemplo de código a seguir antes da enumeração.


```VB
Ou.Filter = Array("user", "group")
```



Se você tiver uma referência de objeto, poderá obter o pai do objeto usando a propriedade [**pai**](iads-property-methods.md) [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) . O exemplo de código a seguir mostra como associar ao objeto pai.


```VB
parentPath = obj.Parent
Set parent = GetObject(parentPath)
```



Para obter mais informações, consulte [Enumerando objetos ADSI](enumerating-adsi-objects.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Pesquisando objetos](searching-for-objects.md)
</dt> </dl>

 

 




