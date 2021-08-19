---
title: Enumerando grupos em um domínio
description: Os grupos podem ser colocados em qualquer contêiner ou unidade organizacional (UO) em um domínio, bem como na raiz do domínio.
ms.assetid: 7f9d3c90-b6f4-4bfa-960f-58f380aa487c
ms.tgt_platform: multiple
keywords:
- Enumerando grupos em um AD de domínio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3723122ef2ab70a7396b2b2821c96a20b4d92419c1e10d1c00b11ff903cb6719
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118429842"
---
# <a name="enumerating-groups-in-a-domain"></a>Enumerando grupos em um domínio

Os grupos podem ser colocados em qualquer contêiner ou unidade organizacional (UO) em um domínio, bem como na raiz do domínio. Isso significa que os grupos podem estar em vários locais na hierarquia de diretórios. Portanto, você tem duas opções para enumerar grupos:

1.  Enumerar os grupos contidos diretamente em um contêiner, UO ou na raiz do domínio.

    A vincular explicitamente ao objeto de contêiner que contém os grupos a enumerar, definir um filtro que contém "grupos" como a classe usando a propriedade [**IADsContainer.Filter**](/windows/desktop/api/iads/nn-iads-iadscontainer) e usar o método [**IADsContainer::get \_ \_ NewEnum**](/windows/desktop/api/iads/nf-iads-iadscontainer-get__newenum) para enumerar os objetos de grupo.

    Essa técnica enumera grupos contidos diretamente em um contêiner ou objeto de UO. Se o contêiner contiver outros contêineres que possam conter outros grupos, você deverá se vincular a esses contêineres e enumerar recursivamente os grupos nesses contêineres. Para manipular os objetos de grupo e ler somente propriedades específicas, use a pesquisa profunda descrita na Opção 2.

    Como a enumeração retorna ponteiros para objetos COM ADSI que representam cada objeto de grupo, você pode chamar [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para obter ponteiros de interface [**IADs,**](/windows/desktop/api/iads/nn-iads-iads) [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup)e [**IADsPropertyList**](/windows/desktop/api/iads/nn-iads-iadspropertylist) para o objeto de grupo; ou seja, você pode obter ponteiros de interface para cada objeto de grupo enumerado em um contêiner sem precisar se vincular explicitamente a cada objeto de grupo. Para executar operações em todos os grupos diretamente dentro de um contêiner, a enumeração não requer associação a cada grupo para chamar **métodos IADs** ou **IADsGroup.** Para recuperar propriedades específicas de grupos, use [**IDirectorySearch,**](/windows/desktop/api/iads/nn-iads-idirectorysearch) conforme descrito na segunda opção.

    Uma exceção a isso ocorre quando você tenta enumerar um grupo que contém membros que são entidades de segurança wellKnown, como Todos, Usuários autenticados, LOTE e assim por diante. Como você não pode se vincular a esses tipos de objetos, eles não são listados quando você enumera grupos no escopo do WinNT, mesmo que possa parecer associado, porque determinados métodos IADs, como Class, ADsPath e Name, retornam resultados corretos quando invocados em membros enumerados.

2.  Execute uma pesquisa profunda para "objectCategory=group" para localizar todos os grupos em uma árvore.

    Primeiro, a bind ao objeto de contêiner em que iniciar a pesquisa. Por exemplo, para encontrar todos os grupos em um domínio, a bind à raiz do domínio; para encontrar todos os grupos na floresta, a vincular ao catálogo global e pesquisar na raiz do GC.

    Em seguida, [**use IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) para consultar usando um filtro de pesquisa que contém (objectCategory=group) e a preferência de pesquisa **de ADS SCOPE \_ \_ SUBTREE**.

    > [!Note]  
    > Você pode executar uma pesquisa com uma preferência de pesquisa **DE ESCOPO DE ADS \_ \_ ONELEVEL** para limitar a pesquisa ao conteúdo direto do objeto de contêiner ao qual você se limitou.

     

    [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) recupera apenas os valores de propriedades específicas de grupos. Para recuperar valores, use **IDirectorySearch**. Para manipular os objetos de grupo retornados de uma pesquisa, ou seja, para usar [**iads**](/windows/desktop/api/iads/nn-iads-iads) ou métodos [**IADsGroup,**](/windows/desktop/api/iads/nn-iads-iadsgroup) agrupe explicitamente a eles. Para fazer isso, especifique **distinguishedName** como uma das propriedades a retornar da pesquisa e use os nomes diferenciados retornados para se vincular a cada grupo retornado na pesquisa.

    Somente propriedades específicas são recuperadas. Você não pode recuperar todos os atributos sem especificar explicitamente todos os atributos possíveis da classe de grupo.

 

 