---
title: Objetos vinculados e monikers
description: Objetos vinculados, como objetos inseridos, dependem de um manipulador de objetos para se comunicar com aplicativos de servidor.
ms.assetid: f72557b9-cd24-4d96-8144-94a5344ec2ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fb8107a5c98ae407cc8e6198d782f75b092110232ae23f41a42dcaefae31758
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736489"
---
# <a name="linked-objects-and-monikers"></a>Objetos vinculados e monikers

Objetos vinculados, como objetos inseridos, dependem de um manipulador de objetos para se comunicar com aplicativos de servidor. No entanto, o próprio objeto vinculado gerencia o nome e o acompanhamento de fontes de link. O objeto vinculado atua como um servidor em processo. Por exemplo, quando ativado, um objeto vinculado localiza e inicia o aplicativo de servidor OLE que é a origem do link.

O manipulador de um objeto vinculado é feito de dois componentes principais: o componente do manipulador e o componente de vinculação. O componente do manipulador contém as partes e funções de controle e de remoção muito semelhantes a um manipulador para um objeto inserido. O componente de vinculação tem seu próprio controlador e cache e fornece acesso ao armazenamento estruturado do objeto. O controlador de componentes de vinculação dá suporte ao nome de origem por meio do uso de monikers e da associação, o processo de localização e execução da origem do link. (Para obter mais informações sobre monikers e associação, consulte [The Component Object Model](the-component-object-model.md).)

Quando um usuário cria inicialmente um objeto vinculado ou carrega um existente do armazenamento, o contêiner carrega uma instância do componente de vinculação na memória, juntamente com o manipulador de objetos. O componente de vinculação fornece interfaces – mais notavelmente [**IOleLink**](/windows/desktop/api/OleIdl/nn-oleidl-iolelink)– que identificam o objeto como um link e permitem que ele gerencie a nomeação, o acompanhamento e a atualização de sua fonte de link.

Ao implementar a interface [**IOleLink,**](/windows/desktop/api/OleIdl/nn-oleidl-iolelink) um objeto vinculado fornece seu contêiner com funções que suportam vinculação. Somente objetos vinculados **implementam IOleLink** e, consultando essa interface, um contêiner pode determinar se um determinado objeto é inserido ou vinculado. A função mais importante fornecida por **IOleLink** permite que um contêiner seja associado à origem do objeto vinculado, ou seja, para ativar a conexão com o documento que armazena os dados nativos do objeto vinculado. **IOleLink** também define funções para gerenciar informações sobre o objeto vinculado, como dados de apresentação armazenados em cache e o local da origem do link.

Quando um documento composto que contém um objeto vinculado é salvo, os dados do link são salvos com a origem do link, não com o contêiner. Somente informações sobre seu nome e local são salvas junto com o documento composto. Esse comportamento é diferente do de um objeto inserido, cujos dados são armazenados junto com o de seu contêiner.

Os aplicativos de contêiner podem fornecer informações sobre seus objetos inseridos, de forma que os últimos, ou partes deles, possam atuar como fontes de link. Ao implementar o suporte para vincular aos objetos inseridos do contêiner, você possibilita incorporaçãos aninhadas, aliviando o usuário de ter que rastrear os originais de cada objeto de incorporação ao qual um link é desejado. Por exemplo, se um usuário quiser inserir uma planilha do Microsoft Excel no Microsoft Word e a planilha contiver um bitmap criado no Paintbrush, o usuário poderá vincular a uma cópia do bitmap contido na planilha em vez do original.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Documentos compostos](compound-documents.md)
</dt> <dt>

[Servidores em processo](in-process-servers.md)
</dt> <dt>

[Manipuladores de objetos](object-handlers.md)
</dt> </dl>

 

 




