---
title: Enumerando usuários
description: Ao contrário dos domínios do Windows NT 4,0, os usuários do Windows 2000 podem ser colocados em qualquer contêiner ou unidade organizacional (UO) em um domínio, bem como a raiz do domínio.
ms.assetid: 4a35af7a-f43b-4cf9-a030-77f6c2518ae7
ms.tgt_platform: multiple
keywords:
- Enumerando usuários do AD
- o AD dos usuários, enumerando um usuário
- Active Directory, usando, usuários, enumerando um usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e922d92f4313ed0238ff068f7ae1c0fbf693d497
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "105811201"
---
# <a name="enumerating-users"></a>Enumerando usuários

Ao contrário dos domínios do Windows NT 4,0, os usuários do Windows 2000 podem ser colocados em qualquer contêiner ou unidade organizacional (UO) em um domínio, bem como a raiz do domínio. Isso significa que os usuários podem estar em vários locais na hierarquia de diretórios. Portanto, você tem duas opções para enumerar usuários:

-   Enumere os usuários diretamente contidos em um contêiner, ou ou na raiz do domínio:

    Associe explicitamente ao objeto de contêiner que contém os usuários que você está interessado em enumerar, defina um filtro que contenha "user" como a classe usando a propriedade [**IADsContainer. Filter**](/windows/desktop/ADSI/iadscontainer-property-methods) e use o método [**IADsContainer:: get \_ \_ NewEnum**](/windows/desktop/api/iads/nf-iads-iadscontainer-get__newenum) para enumerar os objetos de usuário.

    Essa técnica pode ser usada para enumerar usuários que estão diretamente contidos em um contêiner ou objeto de UO. Se o contêiner contiver outros contêineres que potencialmente podem conter outros usuários, você deverá associar a esses contêineres e enumerar recursivamente os usuários nesses contêineres. Se não for necessário que você manipule os objetos de usuário e só precise ler propriedades específicas, use a pesquisa profunda descrita na opção 2.

    Como a enumeração retorna ponteiros para objetos COM ADSI que representam cada objeto de usuário, você pode chamar [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para obter os ponteiros de interface [**IADs**](/windows/desktop/api/iads/nn-iads-iads), [**IADsUser**](/windows/desktop/api/iads/nn-iads-iadsuser)e [**IADsPropertyList**](/windows/desktop/api/iads/nn-iads-iadspropertylist) para o objeto de usuário. Isso significa que você pode obter ponteiros de interface para cada objeto de usuário enumerado em um contêiner sem ter que associar explicitamente a cada objeto de usuário. Para executar operações em todos os usuários diretamente dentro de um contêiner, a enumeração evita que você precise se associar a cada usuário para chamar os métodos **IADs** ou **IADsUser** . Para recuperar propriedades específicas de usuários, use [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) conforme descrito na opção 2.

-   Execute uma pesquisa profunda para (& (objectClass = user) (objectCategory = Person)) para localizar todos os usuários em uma árvore:

    Primeiro, associe-se ao objeto de contêiner onde iniciar a pesquisa. Por exemplo, para localizar todos os usuários em um domínio, associe-se à raiz do domínio; para localizar todos os usuários na floresta, associe-se ao catálogo global e pesquise na raiz do GC.

    Em seguida, use [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) para consultar usando um filtro de pesquisa contendo (& (objectClass = user) (objectCategory = Person)) e a preferência de pesquisa da \_ subárvore de escopo ADS \_ .

    Você pode executar uma pesquisa com uma preferência de pesquisa de \_ escopo dos ADS \_ para limitar a pesquisa ao conteúdo direto do objeto de contêiner ao qual você está vinculado.

    [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) recupera apenas os valores de propriedades específicas dos usuários. Para recuperar valores, use **IDirectorySearch**. Para manipular os objetos de usuário retornados de uma pesquisa, ou seja, você deseja usar os métodos [**IADs**](/windows/desktop/api/iads/nn-iads-iads) ou [**IADsUser**](/windows/desktop/api/iads/nn-iads-iadsuser) , você deve associá-los explicitamente a eles. Para fazer isso, especifique **distinguishedName** como uma das propriedades a serem retornadas da pesquisa e use os nomes distintos retornados para associar a cada usuário retornado na pesquisa.

    Somente propriedades específicas são recuperadas. Não é possível recuperar todos os atributos sem especificar explicitamente todos os atributos possíveis da classe User.

 

 