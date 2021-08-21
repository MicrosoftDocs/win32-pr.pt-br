---
title: Monikers de classe
description: Embora as classes normalmente sejam identificadas diretamente com CLSIDs para funções como CoCreateInstance ou CoGetClassObject, as classes agora também podem ser identificadas com um moniker chamado de moniker de classe.
ms.assetid: 63f5d256-cb61-4673-b5d6-da5c1d89dfa5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 499a117372cd7364fc52b3503b30175a4be11afb9e28e3dd32adbf1007185f85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048684"
---
# <a name="class-monikers"></a>Monikers de classe

Embora as classes normalmente sejam identificadas diretamente com CLSIDs para funções como [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) ou [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject), as classes agora também podem ser identificadas com um moniker chamado de *moniker de classe*. Os monikers de classe são associados ao objeto de classe da classe para a qual eles são criados.

A capacidade de identificar classes com um moniker dá suporte a operações úteis que, de outra forma, são difíceis. Por exemplo, o arquivo monikers tradicionalmente suportava a ligação avançada somente para a classe associada à classe de arquivo à qual eles foram referenciados; um moniker para um arquivo de Excel seria associado a uma instância de um objeto Excel, e um moniker a uma imagem GIF seria associado a uma instância do manipulador GIF atualmente registrado. Um moniker de classe permite que você indique a classe que deseja usar para manipular um arquivo por meio de composição com um moniker de arquivo. um moniker de classe para uma classe de gráfico 3d composta com um moniker para um arquivo de Excel gera um moniker que é associado a uma instância do objeto de gráfico 3d e inicializa o objeto com o conteúdo do arquivo de Excel.

Os monikers de classe são, portanto, mais úteis em composição com outros tipos de monikers, como moniker de arquivo ou monikers de item.

Os monikers de classe também podem ser compostos à direita dos monikers que dão suporte à associação à interface [**IClassActivator**](/windows/desktop/api/ObjIdl/nn-objidl-iclassactivator) . Quando composta dessa maneira, **IClassActivator** simplesmente dá acesso ao objeto de classe e às instâncias da classe por meio de [**IClassActivator:: GetClassObject**](/windows/desktop/api/ObjIdl/nf-objidl-iclassactivator-getclassobject). Os monikers de classe podem ser identificados por meio de [**IMoniker:: IsSystemMoniker**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-issystemmoniker), que retorna MKSYS \_ CLASSMONIKER em *pdwMksys*.

Os programadores normalmente criam monikers de classe usando a função [**CreateClassMoniker**](/windows/desktop/api/Objbase/nf-objbase-createclassmoniker) ou por meio de [**MkParseDisplayName**](/windows/desktop/api/Objbase/nf-objbase-mkparsedisplayname). (Consulte [**IMoniker::P arsedisplayname**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-parsedisplayname) para obter detalhes.)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Anti-moniker](anti-monikers.md)
</dt> <dt>

[Monikers compostos](composite-monikers.md)
</dt> <dt>

[Monikers de arquivo](file-monikers.md)
</dt> <dt>

[Monikers de item](item-monikers.md)
</dt> <dt>

[Monikers de ponteiro](pointer-monikers.md)
</dt> </dl>

 

 




