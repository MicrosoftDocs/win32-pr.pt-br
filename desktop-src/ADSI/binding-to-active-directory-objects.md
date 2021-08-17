---
title: Associação a objetos do Active Directory
description: Antes de continuar com esse cenário, você deve entender como os objetos ADSI são nomeados no Active Directory e como a bindá-los. A associação de um objeto ADSI conecta o objeto ao serviço de diretório e permite que você acesse os métodos do objeto.
ms.assetid: 0d8d8f1c-786f-4d87-977c-91a167bcf118
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0b473c9e3370c3d1739fc904b8c6409d756f62b5c358db200c3de821f55349f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962255"
---
# <a name="binding-to-active-directory-objects"></a>Associação a objetos do Active Directory

Antes de continuar com esse cenário, você deve entender como os objetos ADSI são nomeados no Active Directory e como a bindá-los. A associação de um objeto ADSI conecta o objeto ao serviço de diretório e permite que você acesse os métodos do objeto.

## <a name="adspath"></a>Adspath

Um objeto ADSI é identificado exclusivamente por sua cadeia de caracteres de associação, que também é conhecida como ADsPath. Um ADsPath é uma combinação de um progID (identificador programático) do provedor ADSI e o DN (nome diferenciado) do objeto.

Este é o formato de um ADsPath:

"progID://DN"

-   pogID — o identificador programático do provedor ADSI, como LDAP ou WinNT.

-   :// — separa o progID do DN.

-   DN — o nome diferenciado do objeto ADSI, que é o caminho completo do objeto , em que o caminho consiste em RDNs (nomes diferenciados relativos).

Um RDN é o nome do objeto sem o caminho e é exclusivo de seus objetos irmãos. Um RDN consiste em uma ID de atributo e valor, como "DC=Fabrikam", em que DC é o atributo e Fabrikam é o valor. DC é uma ID de atributo RDN que significa componente de domínio.

Veja um exemplo de ADsPath:

"LDAP://DC=Fabrikam,DC=Com"

## <a name="binding-the-object"></a>Associação do objeto

Veja como você pode vincular o objeto de domínio neste cenário:


```VB
Set dom = GetObject("LDAP://DC=Fabrikam,DC=Com")
```



Quando você executar este exemplo de código, a ADSI usará o DN para determinar os objetos ADSI a ser unidos. Depois que a ADSI vincular esses objetos, você poderá acessar seus métodos. O exemplo de código anterior vincula um objeto de domínio a [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) e [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer). Agora você pode usar métodos nessas interfaces, como [**Get,**](/windows/desktop/api/Iads/nf-iads-iads-get) [**Put,**](/windows/desktop/api/Iads/nf-iads-iads-put) [**Create,**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create) [**Delete**](/windows/desktop/api/Iads/nf-iads-iadscontainer-delete)e [**MoveHere.**](/windows/desktop/api/Iads/nf-iads-iadscontainer-movehere)

Depois de vincular um objeto de domínio, você pode imprimir alguns de seus atributos:


```VB
Debug.Print dom.Get("Name")
Debug.Print dom.Get("whenCreated")
```



Para obter mais informações sobre ADsPath, consulte Binding [String](binding-string.md). Para obter mais informações sobre associação, consulte [Associação a um objeto ADSI](binding-to-an-adsi-object.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando uma unidade organizacional](creating-an-organizational-unit.md)
</dt> </dl>

 

 




