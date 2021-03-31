---
title: Associação a objetos Active Directory
description: Antes de continuar com esse cenário, você deve entender como os objetos ADSI são nomeados em Active Directory e como associá-los. A associação de um objeto ADSI conecta o objeto ao serviço de diretório e permite que você acesse os métodos do objeto.
ms.assetid: 0d8d8f1c-786f-4d87-977c-91a167bcf118
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fa54f2015e0d5663db2917eb27b250f39eb4c0c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004877"
---
# <a name="binding-to-active-directory-objects"></a>Associação a objetos Active Directory

Antes de continuar com esse cenário, você deve entender como os objetos ADSI são nomeados em Active Directory e como associá-los. A associação de um objeto ADSI conecta o objeto ao serviço de diretório e permite que você acesse os métodos do objeto.

## <a name="adspath"></a>ADsPath

Um objeto ADSI é identificado exclusivamente por sua cadeia de caracteres de associação, que também é conhecida como ADsPath. Um ADsPath é uma combinação de um identificador programático (progID) do provedor ADSI e o DN (nome distinto) do objeto.

Este é o formato de um ADsPath:

"progID://DN"

-   pogID — o identificador programático do provedor ADSI, como LDAP ou WinNT.

-   ://— separa o progID do DN.

-   DN — o nome distinto do objeto ADSI, que é o caminho completo do objeto, onde o caminho consiste em nomes distintos relativos (RDNs).

Um RDN é o nome do objeto sem o caminho e é exclusivo de seus objetos irmãos. Um RDN consiste em uma ID e um valor de atributo, como "DC = Fabrikam", em que DC é o atributo e Fabrikam é o valor. O DC é uma ID de atributo RDN que significa componente de domínio.

Aqui está um exemplo de um ADsPath:

"LDAP://DC = Fabrikam, DC = com"

## <a name="binding-the-object"></a>Associando o objeto

Veja como você pode associar o objeto de domínio neste cenário:


```VB
Set dom = GetObject("LDAP://DC=Fabrikam,DC=Com")
```



Quando você executa este exemplo de código, a ADSI usa o DN para determinar os objetos ADSI a serem associados. Depois que a ADSI associa esses objetos, você pode acessar seus métodos. O exemplo de código anterior associa um objeto de domínio a [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) e [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer). Agora você pode usar métodos nessas interfaces, como [**Get**](/windows/desktop/api/Iads/nf-iads-iads-get), [**Put**](/windows/desktop/api/Iads/nf-iads-iads-put), [**Create**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create), [**delete**](/windows/desktop/api/Iads/nf-iads-iadscontainer-delete)e [**MoveHere**](/windows/desktop/api/Iads/nf-iads-iadscontainer-movehere).

Depois de associar um objeto de domínio, você pode imprimir alguns de seus atributos:


```VB
Debug.Print dom.Get("Name")
Debug.Print dom.Get("whenCreated")
```



Para obter mais informações sobre ADsPath, consulte [Binding String](binding-string.md). Para obter mais informações sobre associação, consulte [Binding to a ADSI Object](binding-to-an-adsi-object.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando uma unidade organizacional](creating-an-organizational-unit.md)
</dt> </dl>

 

 




