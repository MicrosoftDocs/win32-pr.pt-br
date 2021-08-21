---
title: Exibir Caching
description: Exibir Caching
ms.assetid: d19c111c-1367-43a2-97a9-35dc0ff5dcc8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b155c0a9d3229db85a52b0589c4854bdee9a2e8e4171e231480036c512af737
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047674"
---
# <a name="view-caching"></a>Exibir Caching

Um aplicativo de contêiner deve ser capaz de obter uma apresentação de um objeto com a finalidade de exibi-lo ou imprimi-lo para os usuários quando o documento estiver aberto, mas o aplicativo de servidor do objeto não estiver em execução ou não estiver instalado no computador do usuário. No entanto, pressupõe-se que os servidores para todos os objetos que podem ser encontrados conceavelmente em um documento sejam instalados no computador de cada usuário e sempre possam ser executados sob demanda não é realista. O manipulador de objetos padrão, que está disponível em todos os momentos, resolve esse problema armazenando em cache as apresentações de objeto no armazenamento do documento e manipulando essas apresentações em qualquer plataforma, independentemente da disponibilidade do servidor de objetos em qualquer instalação específica do contêiner.

Os contêineres podem manter apresentações de desenho para um ou mais dispositivos de destino específicos, além do necessário para manter o objeto na tela. Além disso, se você portar o objeto de uma plataforma para outra, o OLE converterá automaticamente os formatos de dados do objeto em aqueles com suporte na nova plataforma. Por exemplo, se você mover um objeto de Windows para o Macintosh, o OLE converterá suas apresentações de metarquivo em formatos PICT.

Para apresentar uma representação precisa de um objeto inserido ao usuário, o aplicativo de contêiner do objeto inicia uma caixa de diálogo com o manipulador de objetos, solicitando dados e desenhando instruções. Para atender às solicitações do contêiner, o manipulador deve implementar as interfaces [**IDataObject,**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2)e [**IOleCache.**](/windows/desktop/api/OleIdl/nn-oleidl-iolecache)

[**IDataObject permite**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) que um aplicativo de contêiner OLE receba dados e envie dados para seus objetos inseridos ou vinculados. Quando os dados mudam em um objeto, essa interface fornece uma maneira para o objeto disponibilizar seus novos dados para seu contêiner e fornece ao contêiner uma maneira de atualizar os dados em sua cópia do objeto. (Para uma discussão sobre transferência de dados em geral, consulte Capítulo 4, Transferência de Dados.)

A interface [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2) é muito parecido com a interface [**IDataObject,**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) exceto pelo fato de que ele solicita que um objeto se desenromine em um contexto de dispositivo, como uma tela, uma impressora ou um metadado, em vez de mover ou copiar seus dados para a memória ou alguma outra mídia de transferência. A finalidade da interface é permitir que um contêiner OLE obtenha representações de imagens alternativas de seus objetos inseridos, cujos dados ela já tem, evitando assim a sobrecarga de ter que transferir instâncias totalmente novas dos mesmos objetos de dados simplesmente para obter novas instruções de desenho. Em vez disso, a interface **IViewObject2** permite que o contêiner peça a um objeto que forneça uma representação gráfica de si mesmo desenhando em um contexto de dispositivo especificado pelo contêiner.

Ao chamar a interface [**IViewObject2,**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2) um aplicativo de contêiner também pode especificar que o objeto se desenha em um dispositivo de destino diferente do que será renderizado de fato. Isso permite que o contêiner, conforme necessário, gere renderizações diferentes de um único objeto. Por exemplo, o chamador pode solicitar que o objeto se componha para uma impressora, mesmo que o desenho resultante seja renderizado na tela. O resultado, é claro, seria uma visualização de impressão do objeto .

A interface [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2)também fornece métodos que permitem que os contêineres se registrem para notificações de exibição-alteração. Assim como com os dados e os avisos OLE, uma conexão de consultoria de exibição permite que um contêiner atualize suas renderizações de um objeto por sua própria conveniência, em vez de responder a uma chamada do objeto . Por exemplo, se uma nova versão do aplicativo de servidor de um objeto oferecer exibições adicionais dos mesmos dados, o manipulador padrão do objeto chamará a implementação de cada contêiner de [**IAdviseSink::OnViewChange**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-onviewchange) para que eles saibam que as novas apresentações estavam disponíveis. O contêiner recuperaria essas informações do sink de consultoria somente quando necessário.

Como Windows contextos de dispositivo têm significado apenas dentro de um único processo, você não pode passar ponteiros [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2) entre os limites do processo. Como resultado, os servidores locais e remotos OLE não precisam implementar a interface, o que não funcionaria corretamente, mesmo que eles funcionasse. Somente manipuladores de objetos e servidores em processo implementam a interface **IViewObject2.** O OLE fornece uma implementação padrão, que você pode usar em seus próprios servidores em processo OLE e manipuladores de objetos simplesmente agregando o manipulador padrão OLE. Ou você pode escrever sua própria implementação de **IViewObject2.**

Um objeto implementa a interface [**IOleCache**](/windows/desktop/api/OleIdl/nn-oleidl-iolecache) para permitir que o manipulador saiba quais funcionalidades ele deve armazenar em cache. O manipulador de objetos também possui o cache e garante que ele seja mantido atualizado. À medida que o objeto inserido entra no estado de execução, o manipulador configura as conexões de consultoria apropriadas no objeto de servidor, com ele mesmo atuando como o sink. As implementações de interface [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) e [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2)operam sem dados armazenados em cache no lado do cliente. A implementação do manipulador de **IViewObject2** é responsável por determinar quais formatos de dados armazenar em cache para atender às solicitações de desenho do cliente. A implementação do manipulador de **IDataObject** é responsável por obter dados em vários formatos, etc., entre a memória e a instância [**de IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) subjacente do objeto inserido. Manipuladores personalizados podem usar essas implementações agregando no manipulador padrão.

> [!Note]  
> A interface [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2) é uma extensão funcional simples de [**IViewObject**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject) e deve ser implementada em vez da última interface, que agora está obsoleta. Além de fornecer os métodos **IViewObject,** a interface **IViewObject2** fornece um único membro adicional, [**GetExtent**](/windows/desktop/api/OleIdl/nf-oleidl-iviewobject2-getextent), que permite que um aplicativo de contêiner receba o tamanho da apresentação de um objeto do cache sem primeiro precisar mover o objeto para o estado de execução com uma chamada para [**IOleObject::GetExtent**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getextent).

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Documentos compostos](compound-documents.md)
</dt> </dl>

 

 