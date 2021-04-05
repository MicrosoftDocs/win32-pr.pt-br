---
title: Documentos compostos
description: Os documentos OLE compostos permitem que os usuários trabalhem em um único aplicativo para manipular dados gravados em vários formatos e derivados de várias fontes.
ms.assetid: d17dc0dd-3115-4830-8c6b-694a8d1accaa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76f12e0228b7c8c1d74e4ec33d8069490351f77f
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104084947"
---
# <a name="compound-documents"></a>Documentos compostos

Os documentos OLE compostos permitem que os usuários trabalhem em um único aplicativo para manipular dados gravados em vários formatos e derivados de várias fontes. Por exemplo, um usuário pode inserir em um documento de processamento de texto um grafo criado em um segundo aplicativo e um objeto de som criado em um terceiro aplicativo. Ativar o grafo faz com que o segundo aplicativo carregue sua interface do usuário ou pelo menos essa parte que contém as ferramentas necessárias para editar o objeto. Ativar o objeto de som faz com que o terceiro aplicativo o execute. Em ambos os casos, um usuário é capaz de manipular dados de fontes externas de dentro do contexto de um único documento.

A tecnologia de documento OLE composto está posicionada em uma base que consiste em COM, armazenamento estruturado e transferência de dados uniforme. Conforme resumido abaixo, cada uma dessas tecnologias principais desempenha uma função crítica em documentos compostos OLE:

<dl> <dt>

<span id="COM"></span><span id="com"></span>INTERFACES
</dt> <dd>

Um objeto de documento composto é essencialmente um objeto COM que pode ser inserido ou vinculado a um documento existente. Como um objeto COM, um objeto de documento composto expõe a interface [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) , por meio da qual os clientes podem obter ponteiros para suas outras interfaces, incluindo vários, como [**IOleObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleobject), [**IOleLink**](/windows/desktop/api/OleIdl/nn-oleidl-iolelink)e [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2), que fornecem recursos especiais exclusivos para objetos de documento compostos.

</dd> <dt>

<span id="Structured_Storage"></span><span id="structured_storage"></span><span id="STRUCTURED_STORAGE"></span>Armazenamento estruturado
</dt> <dd>

Um objeto de documento composto deve implementar o [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage) ou, opcionalmente, as interfaces [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) para gerenciar seu próprio armazenamento. Um contêiner usado para criar documentos compostos deve fornecer a interface [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) , por meio da qual os objetos armazenam e recuperam dados. Os contêineres quase sempre fornecem instâncias de **IStorage** obtidas da implementação dos arquivos compostos do OLE. Os contêineres também devem usar as interfaces **IPersistStorage** e/ou **IPersistStream** de um objeto.

</dd> <dt>

<span id="Uniform_Data_Transfer"></span><span id="uniform_data_transfer"></span><span id="UNIFORM_DATA_TRANSFER"></span>Transferência de Dados uniforme
</dt> <dd>

Os aplicativos que dão suporte a documentos compostos devem implementar [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) porque objetos incorporados e vinculados começam como dados que foram transferidos usando formatos de área de transferência OLE especiais, em vez de formatos de área de transferência padrão do Microsoft Windows. Em outras palavras, a formatação de dados como um objeto incorporado ou vinculado é simplesmente uma opção mais fornecida pelo modelo de transferência uniforme de dados do OLE.

</dd> </dl>

A tecnologia de documentos compostos do OLE beneficia os desenvolvedores de software e os usuários. Em vez de se sentir obrigada a CRAM cada recurso concebível em um único aplicativo, os desenvolvedores de software agora são gratuitos, se quiserem, para desenvolver aplicativos menores e mais focados que dependem de outros aplicativos para fornecer recursos adicionais. Nos casos em que um desenvolvedor de software decide fornecer um aplicativo com recursos além de seus principais recursos, o desenvolvedor pode implementar esses serviços adicionais como DLLs separadas, que são carregadas na memória somente quando seus serviços são necessários. Os usuários se beneficiam de softwares menores, mais rápidos e mais compatíveis que podem misturar e corresponder conforme necessário, manipulando todos os componentes necessários de dentro de um único documento mestre.

Para mais informações, consulte os seguintes tópicos:

-   [Contêineres e servidores](containers-and-servers.md)
-   [Vinculação e inserção](linking-and-embedding.md)
-   [Manipuladores de objetos](object-handlers.md)
-   [Servidores em processo](in-process-servers.md)
-   [Objetos vinculados e monikers](linked-objects-and-monikers.md)
-   [Notificações](notifications.md)
-   [Interfaces de documento composto](compound-document-interfaces.md)
-   [Estados de objeto](object-states.md)
-   [Implementando a ativação do In-Place](implementing-in-place-activation.md)
-   [Criando objetos vinculados e incorporados de dados existentes](creating-linked-and-embedded-objects-from-existing-data.md)
-   [Exibir cache](view-caching.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Transferência de Dados](data-transfer.md)
</dt> <dt>

[Armazenamento estruturado](/windows/desktop/Stg/structured-storage-start-page)
</dt> </dl>

 

 