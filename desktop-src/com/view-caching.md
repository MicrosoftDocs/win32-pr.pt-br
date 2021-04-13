---
title: Exibir cache
description: Exibir cache
ms.assetid: d19c111c-1367-43a2-97a9-35dc0ff5dcc8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 592c5bc2555e907cdc4e600465b807387c3a5548
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104366745"
---
# <a name="view-caching"></a>Exibir cache

Um aplicativo de contêiner deve ser capaz de obter uma apresentação de um objeto com a finalidade de exibi-lo ou imprimi-lo para os usuários quando o documento está aberto, mas o aplicativo de servidor do objeto não está em execução ou não está instalado no computador do usuário. No entanto, para supor que os servidores de todos os objetos que podem ser considerados em um documento sejam instalados no computador de cada usuário e sempre possam ser executados sob demanda. O manipulador de objetos padrão, que está disponível em todos os momentos, resolve esse dilema armazenando em cache as apresentações de objetos no armazenamento do documento e manipulando essas apresentações em qualquer plataforma, independentemente da disponibilidade do servidor de objetos em qualquer instalação específica do contêiner.

Os contêineres podem manter apresentações de desenho para um ou mais dispositivos de destino específicos, além do necessário para manter o objeto na tela. Além disso, se você portar o objeto de uma plataforma para outra, o OLE converterá automaticamente os formatos de dados do objeto para aqueles com suporte na nova plataforma. Por exemplo, se você mover um objeto do Windows para o Macintosh, o OLE converterá suas apresentações de metarquivo em formatos PICT.

Para apresentar uma representação precisa de um objeto incorporado ao usuário, o aplicativo de contêiner do objeto inicia uma caixa de diálogo com o manipulador de objetos, solicitando dados e instruções de desenho. Para poder atender às solicitações do contêiner, o manipulador deve implementar as interfaces [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject), [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2)e [**IOleCache**](/windows/desktop/api/OleIdl/nn-oleidl-iolecache) .

[**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) permite que um aplicativo de contêiner OLE obtenha dados e envie dados para seus objetos incorporados ou vinculados. Quando os dados são alterados em um objeto, essa interface fornece uma maneira para que o objeto torne seus novos dados disponíveis para seu contêiner e fornece ao contêiner uma maneira de atualizar os dados em sua cópia do objeto. (Para uma discussão sobre transferência de dados em geral, consulte o capítulo 4, Transferência de Dados.)

A interface [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2) é muito parecida com a interface [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) , exceto que ela solicita que um objeto se desenhe em um contexto de dispositivo, como uma tela, impressora ou metarquivo, em vez de mover ou copiar seus dados para a memória ou outra mídia de transferência. A finalidade da interface é habilitar um contêiner OLE para obter representações de ilustração alternativas de seus objetos incorporados, cujos dados ele já tem, evitando, assim, a sobrecarga de ter que transferir totalmente novas instâncias dos mesmos objetos de dados simplesmente para obter novas instruções de desenho. Em vez disso, a interface **IViewObject2** permite que o contêiner peça a um objeto para fornecer uma representação de sua própria forma de desenho em um contexto de dispositivo especificado pelo contêiner.

Ao chamar a interface [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2) , um aplicativo de contêiner também pode especificar que o objeto seja desenhado em um dispositivo de destino diferente daquele em que ele realmente será renderizado. Isso habilita o contêiner, conforme necessário, para gerar renderizações diferentes de um único objeto. Por exemplo, o chamador poderia pedir ao objeto para compor a si mesmo para uma impressora, mesmo que o desenho resultante seja renderizado na tela. O resultado, é claro, seria uma visualização de impressão do objeto.

A interface [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2)também fornece métodos que permitem que os contêineres se registrem para notificações de alteração de exibição. Assim como acontece com os conselhos de dados e OLE, uma conexão de exibição de consultoria permite que um contêiner atualize seus processamentos de um objeto por sua própria conveniência, em vez de responder a uma chamada do objeto. Por exemplo, se uma nova versão do aplicativo de servidor de um objeto fosse oferecer exibições adicionais dos mesmos dados, o manipulador padrão do objeto chamaria a implementação de cada contêiner de [**IAdviseSink:: OnViewChange**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-onviewchange) para informá-los de que as novas apresentações estavam disponíveis. O contêiner recuperaria essas informações do coletor de aviso somente quando necessário.

Como os contextos de dispositivo do Windows têm significado apenas em um único processo, você não pode passar ponteiros [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2) entre limites de processo. Como resultado, os servidores OLE local e remoto não precisam de nada para implementar a interface, o que não funcionaria corretamente, mesmo que tenha feito isso. Somente manipuladores de objeto e servidores em processo implementam a interface **IViewObject2**. O OLE fornece uma implementação padrão, que você pode usar em seus próprios servidores OLE em processo e manipuladores de objetos simplesmente agregando o manipulador padrão OLE. Ou você pode escrever sua própria implementação de **IViewObject2**.

Um objeto implementa a interface [**IOleCache**](/windows/desktop/api/OleIdl/nn-oleidl-iolecache) para permitir que o manipulador saiba quais recursos ele deve armazenar em cache. O manipulador de objetos também possui o cache e garante que ele seja mantido atualizado. Como o objeto incorporado entra no estado de execução, o manipulador configura as conexões de consultoria apropriadas no objeto de servidor, com ele atuando como o coletor. As implementações da interface [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) e [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2)operam fora dos dados armazenados em cache no lado do cliente. A implementação do manipulador de **IViewObject2** é responsável por determinar quais formatos de dados armazenar em cache para atender às solicitações de desenho do cliente. A implementação do manipulador de **IDataObject** é responsável por obter dados em vários formatos, etc., entre a memória e a instância de [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) subjacente do objeto inserido. Os manipuladores personalizados podem usar essas implementações agregando no manipulador padrão.

> [!Note]  
> A interface [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2) é uma extensão funcional simples de [**IViewObject**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject) e deve ser implementada em vez da última interface, que agora é obsoleta. Além de fornecer os métodos **IViewObject** , a interface **IViewObject2** fornece um único membro [**adicional, getestende, que**](/windows/desktop/api/OleIdl/nf-oleidl-iviewobject2-getextent)permite que um aplicativo de contêiner obtenha o tamanho da apresentação de um objeto do cache sem precisar primeiro mover o objeto para o estado em execução com uma chamada para [**IOleObject:: getextensão**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getextent).

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Documentos compostos](compound-documents.md)
</dt> </dl>

 

 