---
title: Usando objectGUID para associar a um objeto
description: Um nome diferenciado de objeto será alterado se o objeto for renomeado ou movido, portanto o nome diferenciado não é um identificador de objeto confiável.
ms.assetid: 6c038005-3ecb-4c00-b1a3-a231d3aea64e
ms.tgt_platform: multiple
keywords:
- Usando objectGUID para associar a um AD de objeto
- AD do objectGUID
- objectGUID AD, usando para associar a um objeto
- Active Directory, usando, associação, usando objectGUID para associar ao objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 045c6194cf27b1697cc478b547105fb10335c219
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104007281"
---
# <a name="using-objectguid-to-bind-to-an-object"></a>Usando objectGUID para associar a um objeto

Um nome diferenciado de objeto será alterado se o objeto for renomeado ou movido, portanto o nome diferenciado não é um identificador de objeto confiável. Em Active Directory Domain Services, a propriedade **objectGUID** de um objeto nunca muda, mesmo que o objeto seja renomeado ou movido. Para obter mais informações sobre **objectGUID** e identificadores, consulte [nomes de objetos e identidades](object-names-and-identities.md).

O provedor LDAP Active Directory fornece um método para associar a um objeto usando o GUID do objeto. O formato da cadeia de vinculação é o seguinte:


```C++
LDAP://servername/<GUID=XXXXX>
```



Neste exemplo, "servername" é o nome do servidor de diretório e "XXXXX" é a representação de cadeia de caracteres do valor hexadecimal do GUID. O "servername" é opcional. A cadeia de caracteres GUID é especificada no formulário "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX". A cadeia de caracteres GUID também pode assumir a forma "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX", que é a mesma forma que a cadeia de caracteres produzida pela função [**StringFromGUID2**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2) , sem as chaves ao redor " {} ". Para obter mais informações e um exemplo de código que mostra como criar uma cadeia de caracteres vinculável de um GUID, consulte [exemplo de código para criar uma representação de cadeia de caracteres vinculável de um GUID](example-code-for-creating-a-bindable-string-representation-of-a-guid.md). A propriedade [**IADs. GUID**](/windows/desktop/ADSI/iads-property-methods) pode ser usada para recuperar a forma de cadeia de caracteres apropriada do GUID.

Ao vincular usando o GUID do objeto, não há suporte para alguns métodos e propriedades [**IADs**](/windows/desktop/api/iads/nn-iads-iads) e [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) . As seguintes propriedades **IADs** não são suportadas por objetos obtidos pela Associação usando o GUID do objeto:

-   [**ADsPath**](/windows/desktop/ADSI/iads-property-methods)
-   [**Nome**](/windows/desktop/ADSI/iads-property-methods)
-   [**Pai**](/windows/desktop/ADSI/iads-property-methods)

Os objetos **IADsContainer** a seguir não são compatíveis com aqueles obtidos pela Associação usando o GUID do objeto:

-   [**GetObject**](/windows/desktop/api/iads/nf-iads-iadscontainer-getobject)
-   [**Criar**](/windows/desktop/api/iads/nf-iads-iadscontainer-create)
-   [**Apagar**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete)
-   [**CopyHere**](/windows/desktop/api/iads/nf-iads-iadscontainer-copyhere)
-   [**MoveHere**](/windows/desktop/api/iads/nf-iads-iadscontainer-movehere)

Para usar esses métodos e propriedades após a associação a um objeto usando o GUID do objeto, use o método [**IADs. Get**](/windows/desktop/api/iads/nf-iads-iads-get) para recuperar o nome diferenciado do objeto e, em seguida, use o nome distinto para associar ao objeto novamente.

Se um aplicativo armazenar ou armazenar em cache identificadores ou referências a objetos armazenados no Active Directory Domain Services, o GUID do objeto será o melhor identificador a ser usado por vários motivos:

-   A propriedade **objectGUID** de no objeto nunca muda, mesmo que o objeto seja renomeado ou movido.
-   É fácil associar-se ao objeto usando o GUID do objeto.
-   Se o objeto for renomeado ou movido, a propriedade **objectGUID** fornecerá um único identificador que pode ser usado para localizar e identificar rapidamente o objeto, em vez de ter que compor uma consulta que tenha condições para todas as propriedades que identifiquem esse objeto.

 

 