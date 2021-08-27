---
title: Associação ao Catálogo Global
description: O Catálogo Global é um namespace que contém dados de diretório para todos os domínios em uma floresta.
ms.assetid: c3c131c7-d9dd-4dbd-a909-abd0ffd9f375
ms.tgt_platform: multiple
keywords:
- Associação ao AD do Catálogo Global
- global catalog AD , associação a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4d094a0c07a40fa063b726d0ba1c5a15977873d
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881647"
---
# <a name="binding-to-the-global-catalog"></a>Associação ao Catálogo Global

O Catálogo Global é um namespace que contém dados de diretório para todos os domínios em uma floresta. O Catálogo Global contém uma réplica parcial de cada diretório de domínio. Ele contém uma entrada para cada objeto na floresta corporativa, mas não contém todas as propriedades de cada objeto. Em vez disso, ele contém apenas as propriedades especificadas para inclusão no Catálogo Global.

O Catálogo Global é armazenado em servidores específicos em toda a empresa. Somente controladores de domínio podem servir como servidores de Catálogo Global. Os administradores indicam se um determinado controlador de domínio contém um Catálogo Global usando o Gerenciador de Serviços e Sites do Active Directory.

Para se vincular ao Catálogo Global com ADSI, use o moniker "GC:".

Há duas maneiras de se vincular ao Catálogo Global para executar uma pesquisa em uma floresta:

-   A bind ao objeto raiz empresarial para pesquisar em todos os domínios na floresta.
-   A bind a um objeto específico para pesquisar esse objeto e seus filhos. Por exemplo, se você se vincular a um domínio que tem dois domínios abaixo dele em uma árvore de domínio na floresta, poderá pesquisar entre esses três domínios. Esteja ciente de que o nome diferenciado para o objeto ao qual se vincular é exatamente o mesmo que o nome diferenciado usado para se vincular ao namespace "LDAP:". Lembre-se de que "LDAP:" é uma réplica completa de um único domínio e que "GC:" é uma réplica parcial de todos os domínios na floresta.

Assim como no moniker "LDAP:", você pode usar a associação sem servidor ou a associação a um servidor de Catálogo Global específico. Se estiver pesquisando na floresta atual, use a associação sem servidor. No entanto, se estiver pesquisando em outra floresta, especifique um nome de domínio ou um servidor de Catálogo Global ao qual se vincular, como mostrado nos exemplos a seguir.

A bind usando o nome de domínio:

``` syntax
GC://fabrikam.com
```

A bind usando o nome do servidor:

``` syntax
GC://servername
```

Você também pode se vincular a um objeto específico dentro do Catálogo Global. Para se vincular ao objeto de vendas no domínio fabrikam, use o formato a seguir.

``` syntax
GC://fabrikam.com/DC=sales,DC=fabrikam,DC=com
```

Ou, para se vincular ao objeto de vendas no servidor, use o formato a seguir.

``` syntax
GC://servername.fabrikam.com/DC=sales,DC=fabrikam,DC=com
```

**Para pesquisar toda a floresta**

1.  A bind à raiz do namespace catálogo global.
2.  Enumerar o contêiner do Catálogo Global. O contêiner catálogo global contém um único objeto que você pode usar para pesquisar toda a floresta.
3.  Use o objeto no contêiner para executar a pesquisa. No C/C++, chame [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para obter um ponteiro [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) no objeto para que você possa usar a interface **IDirectorySearch** para executar a pesquisa. Em Visual Basic, use o objeto retornado da enumeração em sua consulta ADO.

Para enumerar os servidores do Catálogo Global em um site, execute uma pesquisa de subárvore LDAP de "cn= &lt; yoursite &gt; ,cn=sites, ", usando a cadeia de caracteres de filtro a <DN of the configurationNamingContext> seguir.

``` syntax
(&(objectCategory=nTDSDSA)(options:1.2.840.113556.1.4.803:=1))
```

Esse filtro usa o operador de regra de correspondência **BIT \_ \_ \_ \_ AND** DA REGRA DE CORRESPONDÊNCIA LDAP (1.2.840.113556.1.4.803) para encontrar objetos **nTDSDSA** que têm o bit de ordem baixa definido no bitmask do atributo **options.** O bit de ordem baixa, que corresponde à constante **NTDSDSA \_ OPT \_ IS \_ GC** definida em Ntdsapi.h, identifica o objeto **nTDSDSA** de um servidor de Catálogo Global. Para obter mais informações sobre regras de correspondência, consulte [Sintaxe de filtro de pesquisa](/windows/desktop/ADSI/search-filter-syntax).

O pai do objeto **nTDSDSA** é o objeto de servidor e a propriedade **dNSHostName** do objeto de servidor é o nome DNS do servidor de Catálogo Global.

Você não pode usar definir constantes como \# **NTDSDSA \_ OPT IS \_ \_ GC** e **LDAP \_ MATCHING RULE BIT \_ \_ \_ AND** diretamente em uma cadeia de caracteres de filtro de pesquisa. No entanto, você pode usar essas constantes como argumentos para uma função como [**swprintf \_ s**](/windows/win32/api/winuser/nf-winuser-wsprintfa) para inserir os valores constantes em uma cadeia de caracteres de filtro.

O catálogo global não representa toda a estrutura de árvore de floresta. Por exemplo, você pode esperar que o exemplo de código a seguir enumerasse todos os domínios na floresta e todos os objetos filho de cada domínio. Na realidade, o que ele realmente faz é enumerar todos os domínios na floresta, mas nenhum dos objetos de domínio enumerados contém nenhum filho. Essa é uma limitação do catálogo global.


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



Para corrigir isso, é necessário se vincular a cada objeto de domínio e enumerar os objetos filho de cada domínio. A técnica adequada é mostrada no exemplo de código a seguir.


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



Para obter mais informações e exemplos de código que mostram como pesquisar uma floresta inteira, consulte [Código de exemplo para pesquisar uma floresta.](example-code-for-searching-a-forest.md)

 

 
