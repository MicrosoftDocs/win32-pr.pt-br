---
title: Associação ao catálogo global
description: O catálogo global é um namespace que contém dados de diretório para todos os domínios em uma floresta.
ms.assetid: c3c131c7-d9dd-4dbd-a909-abd0ffd9f375
ms.tgt_platform: multiple
keywords:
- Associação ao AD do catálogo global
- AD de catálogo global, associando a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08fe40b944130f66617b0c111b361ca51cbef126
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104007359"
---
# <a name="binding-to-the-global-catalog"></a>Associação ao catálogo global

O catálogo global é um namespace que contém dados de diretório para todos os domínios em uma floresta. O catálogo global contém uma réplica parcial de cada diretório de domínio. Ele contém uma entrada para cada objeto na floresta da empresa, mas não contém todas as propriedades de cada objeto. Em vez disso, ele contém apenas as propriedades especificadas para inclusão no catálogo global.

O catálogo global é armazenado em servidores específicos em toda a empresa. Somente os controladores de domínio podem servir como servidores de catálogo global. Os administradores indicam se um determinado controlador de domínio contém um catálogo global usando o Active Directory sites e o Gerenciador de serviços.

Para associar ao catálogo global com a ADSI, use o moniker "GC:".

Há duas maneiras de se associar ao catálogo global para executar uma pesquisa em uma floresta:

-   Associe-se ao objeto raiz da empresa para pesquisar em todos os domínios na floresta.
-   Associar a um objeto específico para pesquisar o objeto e seus filhos. Por exemplo, se você associar a um domínio que tem dois domínios abaixo dele em uma árvore de domínio na floresta, poderá pesquisar entre esses três domínios. Lembre-se de que o nome distinto para o objeto a ser associado é exatamente o mesmo que o nome distinto usado para ligar ao namespace "LDAP:". Lembre-se de que "LDAP:" é uma réplica completa de um único domínio e que "GC:" é uma réplica parcial de todos os domínios na floresta.

Assim como no moniker "LDAP:", você pode usar a associação sem servidor ou associar a um servidor de catálogo global específico. Se estiver pesquisando na floresta atual, use a associação sem servidor. No entanto, se pesquisar em outra floresta, especifique um nome de domínio ou um servidor de catálogo global para associar, como mostrado nos exemplos a seguir.

Associar usando o nome de domínio:

``` syntax
GC://fabrikam.com
```

Associar usando o nome do servidor:

``` syntax
GC://servername
```

Você também pode associar a um objeto específico dentro do catálogo global. Para associar ao objeto Sales no domínio fabrikam, use o formato a seguir.

``` syntax
GC://fabrikam.com/DC=sales,DC=fabrikam,DC=com
```

Ou, para associar ao objeto Sales no servidor, use o formato a seguir.

``` syntax
GC://servername.fabrikam.com/DC=sales,DC=fabrikam,DC=com
```

**Para Pesquisar toda a floresta**

1.  Associe-se à raiz do namespace do catálogo global.
2.  Enumere o contêiner do catálogo global. O contêiner de catálogo global contém um único objeto que você pode usar para Pesquisar toda a floresta.
3.  Use o objeto no contêiner para executar a pesquisa. Em C/C++, chame [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para obter um ponteiro [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) no objeto para que você possa usar a interface **IDirectorySearch** para executar a pesquisa. Em Visual Basic, use o objeto retornado da enumeração em sua consulta ADO.

Para enumerar os servidores de catálogo global em um site, execute uma pesquisa de subárvore LDAP de "CN = <yoursite> , CN = sites <DN of the configurationNamingContext> ", usando a cadeia de caracteres de filtro a seguir.

``` syntax
(&(objectCategory=nTDSDSA)(options:1.2.840.113556.1.4.803:=1))
```

Esse filtro usa o **\_ bit de regra de correspondência LDAP \_ \_ \_ e** o operador de regra de correspondência (1.2.840.113556.1.4.803) para localizar objetos **nTDSDSA** que têm o bit de ordem inferior definido no bitmask do atributo **Options** . O bit de ordem inferior, que corresponde ao **NTDSDSA \_ opt \_ é \_** constante de GC definido em NTDSAPI. h, identifica o objeto **NTDSDSA** de um servidor de catálogo global. Para obter mais informações sobre regras de correspondência, consulte [sintaxe do filtro de pesquisa](/windows/desktop/ADSI/search-filter-syntax).

O pai do objeto **nTDSDSA** é o objeto Server, e a propriedade **dNSHostName** do objeto Server é o nome DNS do servidor de catálogo global.

Você não pode usar \# definir constantes como **NTDSDSA \_ opt \_ é \_** o bit de regra de correspondência de GC e **LDAP \_ \_ \_ \_ e** diretamente em uma cadeia de caracteres de filtro de pesquisa. No entanto, você pode usar essas constantes como argumentos para uma função, como [**swprintf \_ s**](/windows/win32/api/winuser/nf-winuser-wsprintfa) , para inserir os valores constantes em uma cadeia de caracteres de filtro.

O catálogo global não representa toda a estrutura de árvore da floresta. Por exemplo, você pode esperar que o exemplo de código a seguir Enumere todos os domínios na floresta e todos os objetos filho de cada domínio. Na realidade, o que ele realmente faz é enumerar todos os domínios na floresta, mas nenhum dos objetos de domínio enumerados contém quaisquer filhos. Essa é uma limitação do catálogo global.


```VB
Dim oGC As IADs
Dim oDomain As IADs
Dim oChild As IADs

Set oGC = GetObject("GC:")
For Each oDomain In oGC
    ' Print the name of the domain.
    Debug.Print oDomain.Name
    
    ' Enumerate the child objects of the domain.
    For Each oChild In oDomain
        Debug.Print oChild.Name
    Next
Next
```



Para corrigir isso, é necessário associar a cada objeto de domínio e, em seguida, enumerar os objetos filho de cada domínio. A técnica apropriada é mostrada no exemplo de código a seguir.


```VB
Dim oGC As IADs
Dim oDomainEnum As IADs
Dim oDomainBind As IADs
Dim oChild As IADs

Set oGC = GetObject("GC:")
For Each oDomainEnum In oGC
    ' Print the name of the domain.
    Debug.Print oDomainEnum.Name
    
    ' Bind to the domain.
    Set oDomainBind = GetObject("LDAP://" + oDomainEnum.Name)
    
    ' Enumerate the child objects of the domain.
    For Each oChild In oDomainBind
        Debug.Print oChild.Name
    Next
Next
```



Para obter mais informações e exemplos de código que mostram como pesquisar uma floresta inteira, consulte [exemplo de código para pesquisar uma floresta](example-code-for-searching-a-forest.md).

 

 