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
ms.openlocfilehash: 322cf3c8b5f40dc43304f95d08ff53a7c5c14217
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104499153"
---
# <a name="fast-binding-option-for-batch-writemodify-operations"></a>Opção de ligação rápida para operações de gravação/modificação em lote

Quando um objeto de serviço de diretório é associado a, a ADSI cria um objeto COM que representa o objeto de diretório especificado. Ao associar, a ADSI normalmente recuperará o atributo **objectClass** para que a ADSI possa expor as interfaces com apropriadas para essa classe de objeto. Por exemplo, um objeto de usuário exporia a interface [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) além das interfaces de base ADSI com suporte para todos os objetos. Para uma única operação, isso não deve afetar o desempenho. No entanto, se forem executadas operações em lote que exigem centenas ou milhares de associações em uma conexão lenta e essas operações estiverem gravando dados no serviço de diretório, poderá ser desejável trocar o suporte completo a objetos para uma ligação mais rápida. Isso é conhecido como uma ligação rápida e é realizado especificando o sinalizador do **ADS \_ Fast \_ BIND** quando [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) ou [**IADsOpenDSObject:: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) é chamado.

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

 

 