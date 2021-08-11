---
title: Opção de ligação rápida para operações de gravação/modificação em lote
description: Quando um objeto de serviço de diretório é associado a, a ADSI cria um objeto COM que representa o objeto de diretório especificado.
ms.assetid: cf41b0c4-7459-49cf-945b-8462c7d19947
ms.tgt_platform: multiple
keywords:
- Opção de ligação rápida para ADSI de operações de gravação/modificação em lote
- ADSI ADSI, usando a opção de ligação rápida para operações de gravação/modificação em lote
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46f27cbbe9ea76089ca1fd460f76c56d10e60664ae39ad28945440c6006acb9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118179895"
---
# <a name="fast-binding-option-for-batch-writemodify-operations"></a>Opção de ligação rápida para operações de gravação/modificação em lote

Quando um objeto de serviço de diretório é associado a, a ADSI cria um objeto COM que representa o objeto de diretório especificado. Ao associar, a ADSI normalmente recuperará o atributo **objectClass** para que a ADSI possa expor as interfaces com apropriadas para essa classe de objeto. Por exemplo, um objeto de usuário exporia a interface [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) além das interfaces de base ADSI com suporte para todos os objetos. Para uma única operação, isso não deve afetar o desempenho. No entanto, se forem executadas operações em lote que exigem centenas ou milhares de associações em uma conexão lenta e essas operações estiverem gravando dados no serviço de diretório, poderá ser desejável trocar o suporte completo a objetos para uma ligação mais rápida. isso é conhecido como uma ligação rápida e é realizado especificando o sinalizador de **\_ \_ associação de FAST de anúncios** quando [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) ou [**IADsOpenDSObject:: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) é chamado.

A ligação rápida tem as seguintes restrições:

-   A operação de associação deve ser executada com a função [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) ou o método [**IADsOpenDSObject:: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) . A operação de associação vai para o servidor de diretório uma vez em vez de duas vezes. A ADSI não recupera o atributo **objectClass** e, portanto, expõe apenas as interfaces ADSI base para o objeto.
-   As seguintes interfaces têm suporte para o objeto COM:

    -   [**IADs**](/windows/desktop/api/Iads/nn-iads-iads)
    -   [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer)
    -   [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject)
    -   [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)
    -   [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist)
    -   [**IADsObjectOptions**](/windows/desktop/api/Iads/nn-iads-iadsobjectoptions)
    -   [**ISupportErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo)
    -   [**IADsDeleteOps**](/windows/desktop/api/Iads/nn-iads-iadsdeleteops)

-   Se o método [**IADsContainer:: GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject) for usado para associar objetos filho, o objeto filho terá as mesmas características de ligação rápida que o pai.
-   A existência do objeto que está sendo associado não é verificada durante a operação de associação, portanto, as chamadas de método subsequentes falharão se o objeto não existir. Por isso, a ligação rápida só deve ser usada para objetos que são conhecidos como existentes, por exemplo, diretamente após a execução de uma consulta que retornava os nomes distintos dos objetos aos quais está sendo associado.
-   Extensões ADSI são expostas para objetos da classe **Top**. Portanto, somente as extensões para as interfaces ADSI base listadas acima são expostas.

 

 