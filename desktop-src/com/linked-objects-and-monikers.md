---
title: Objetos vinculados e monikers
description: Objetos vinculados, como objetos incorporados, dependem de um manipulador de objeto para se comunicar com aplicativos de servidor.
ms.assetid: f72557b9-cd24-4d96-8144-94a5344ec2ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7c14f4cc74ee84fbf745e730d77203ebb4f43b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104160319"
---
# <a name="linked-objects-and-monikers"></a>Objetos vinculados e monikers

Objetos vinculados, como objetos incorporados, dependem de um manipulador de objeto para se comunicar com aplicativos de servidor. O próprio objeto vinculado, no entanto, gerencia a nomenclatura e o acompanhamento de fontes de link. O objeto vinculado age como um servidor em processo. Por exemplo, quando ativado, um objeto vinculado localiza e inicia o aplicativo de servidor OLE que é a origem do link.

O manipulador de um objeto vinculado é composto de dois componentes principais: o componente de manipulador e o componente de vinculação. O componente de manipulador contém partes de controle e de comunicação remota e funções como um manipulador para um objeto incorporado. O componente de vinculação tem seu próprio controlador e cache e fornece acesso ao armazenamento estruturado do objeto. O controlador de componentes de vinculação dá suporte à nomeação de origem por meio do uso de monikers e associação, o processo de localizar e executar a origem do link. (Para obter mais informações sobre monikers e associação, consulte [a Component Object Model](the-component-object-model.md).)

Quando um usuário cria inicialmente um objeto vinculado ou carrega um existente do armazenamento, o contêiner carrega uma instância do componente de vinculação na memória, juntamente com o manipulador de objetos. O componente de vinculação fornece interfaces – mais notavelmente [**IOleLink**](/windows/desktop/api/OleIdl/nn-oleidl-iolelink)– que identificam o objeto como um link e permitem que ele gerencie a nomenclatura, o controle e a atualização de sua origem de link.

Ao implementar a interface [**IOleLink**](/windows/desktop/api/OleIdl/nn-oleidl-iolelink) , um objeto vinculado fornece seu contêiner com funções que dão suporte à vinculação. Somente objetos vinculados implementam **IOleLink** e, ao consultar essa interface, um contêiner pode determinar se um determinado objeto é inserido ou vinculado. A função mais importante fornecida pelo **IOleLink** permite que um contêiner seja vinculado à origem do objeto vinculado, ou seja, ative a conexão com o documento que armazena os dados nativos do objeto vinculado. O **IOleLink** também define funções para gerenciar informações sobre o objeto vinculado, como dados de apresentação em cache e o local da origem do link.

Quando um documento composto que contém um objeto vinculado é salvo, os dados do link são salvos com a origem do link, não com o contêiner. Somente informações sobre seu nome e local são salvas junto com o documento composto. Esse comportamento está em contraste com o de um objeto incorporado, cujos dados são armazenados junto com o de seu contêiner.

Os aplicativos de contêiner podem fornecer informações sobre seus objetos incorporados, de modo que os últimos, ou partes deles, possam atuar como fontes de link. Ao implementar o suporte para vincular aos objetos incorporados do contêiner, você pode tornar as incorporações aninhadas possíveis, aliviando o usuário de ter que rastrear os originais de cada objeto de inserção ao qual um link é desejado. Por exemplo, se um usuário quiser inserir uma planilha do Microsoft Excel no Microsoft Word e a planilha contiver um bitmap criado no Paintbrush, o usuário poderá vincular a uma cópia do bitmap contido na planilha, e não ao original.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Documentos compostos](compound-documents.md)
</dt> <dt>

[Servidores em processo](in-process-servers.md)
</dt> <dt>

[Manipuladores de objetos](object-handlers.md)
</dt> </dl>

 

 




