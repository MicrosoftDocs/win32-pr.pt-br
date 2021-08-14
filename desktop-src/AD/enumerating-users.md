---
title: Enumerando usuários
description: Ao contrário Windows NT domínios 4.0, Windows 2000 usuários podem ser colocados em qualquer contêiner ou UO (unidade organizacional) em um domínio, bem como na raiz do domínio.
ms.assetid: 4a35af7a-f43b-4cf9-a030-77f6c2518ae7
ms.tgt_platform: multiple
keywords:
- Enumerando o AD de Usuários
- users AD , enumerando um usuário
- Active Directory, usando usuários, enumerando um usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa43034c6c006c9c70531f25e2a838ecfc30520e9b42e0b9599e5714a29f225e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118191336"
---
# <a name="enumerating-users"></a>Enumerando usuários

Ao contrário Windows NT domínios 4.0, Windows 2000 usuários podem ser colocados em qualquer contêiner ou UO (unidade organizacional) em um domínio, bem como na raiz do domínio. Isso significa que os usuários podem estar em vários locais na hierarquia de diretórios. Portanto, você tem duas opções para enumerar usuários:

-   Enumerar os usuários diretamente contidos em um contêiner, UO ou na raiz do domínio:

    A vincular explicitamente ao objeto de contêiner que contém os usuários que você está interessado em enumerar, definir um filtro que contém "usuário" como a classe usando a propriedade [**IADsContainer.Filter**](/windows/desktop/ADSI/iadscontainer-property-methods) e usar o [**método IADsContainer::get \_ \_ NewEnum**](/windows/desktop/api/iads/nf-iads-iadscontainer-get__newenum) para enumerar os objetos de usuário.

    Essa técnica pode ser usada para enumerar usuários que estão diretamente contidos em um contêiner ou objeto de UO. Se o contêiner contiver outros contêineres que possam conter outros usuários, você deverá se vincular a esses contêineres e enumerar recursivamente os usuários nesses contêineres. Se não for necessário manipular os objetos de usuário e precisar apenas ler propriedades específicas, use a pesquisa profunda descrita na Opção 2.

    Como a enumeração retorna ponteiros para objetos COM ADSI que representam cada objeto de usuário, você pode chamar [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para obter ponteiros de interface [**IADs,**](/windows/desktop/api/iads/nn-iads-iads) [**IADsUser**](/windows/desktop/api/iads/nn-iads-iadsuser)e [**IADsPropertyList**](/windows/desktop/api/iads/nn-iads-iadspropertylist) para o objeto de usuário. Isso significa que você pode obter ponteiros de interface para cada objeto de usuário enumerado em um contêiner sem precisar se vincular explicitamente a cada objeto de usuário. Para executar operações em todos os usuários diretamente dentro de um contêiner, a enumeração evita a vinculação a cada usuário para chamar **iads** ou **métodos IADsUser.** Para recuperar propriedades específicas de usuários, use [**IDirectorySearch,**](/windows/desktop/api/iads/nn-iads-idirectorysearch) conforme descrito na opção 2.

-   Execute uma pesquisa profunda para (&(objectClass=user)(objectCategory=person)) para localizar todos os usuários em uma árvore:

    Primeiro, a bind ao objeto de contêiner em que iniciar a pesquisa. Por exemplo, para encontrar todos os usuários em um domínio, a bind à raiz do domínio; para encontrar todos os usuários na floresta, a vincular ao catálogo global e pesquisar na raiz do GC.

    Em seguida, use [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) para consultar usando um filtro de pesquisa que contém (&(objectClass=user)(objectCategory=person)) e a preferência de pesquisa de ADS \_ SCOPE \_ SUBTREE.

    Você pode executar uma pesquisa com uma preferência de pesquisa DE ESCOPO DE ADS ONELEVEL para limitar a pesquisa ao conteúdo direto do objeto de contêiner ao qual \_ \_ você se limitou.

    [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) recupera apenas os valores de propriedades específicas dos usuários. Para recuperar valores, use **IDirectorySearch**. Para manipular os objetos de usuário retornados de uma pesquisa, ou seja, você deseja usar [**iads**](/windows/desktop/api/iads/nn-iads-iads) ou métodos [**IADsUser,**](/windows/desktop/api/iads/nn-iads-iadsuser) você deve se vincular explicitamente a eles. Para fazer isso, especifique **distinguishedName** como uma das propriedades a retornar da pesquisa e use os nomes diferenciados retornados para se vincular a cada usuário retornado na pesquisa.

    Somente propriedades específicas são recuperadas. Você não pode recuperar todos os atributos sem especificar explicitamente todos os atributos possíveis da classe de usuário.

 

 