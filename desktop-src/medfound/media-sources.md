---
description: Fontes de mídia
ms.assetid: 65132e7d-22f6-4209-bc58-f5ea86ebd514
title: Fontes de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c378d86495188321b37e6326d56ed75c4a5c6dacf3045eaaad717e8a8df6d12
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118062107"
---
# <a name="media-sources"></a>Fontes de mídia

*As fontes de* mídia são objetos que geram dados de mídia no Media Foundation pipeline. Esta seção descreve detalhadamente as APIs de origem de mídia. Leia esta seção se você estiver implementando uma fonte de mídia personalizada ou usando uma fonte de mídia fora do pipeline Media Foundation dados.

Se o aplicativo usar a camada de controle, ele precisará usar apenas um subconjunto limitado das APIs de origem de mídia. Para obter informações, consulte o tópico [Usando fontes de mídia com a sessão de mídia](using-media-sources-with-the-media-session.md).

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                                 | Descrição                                                                                                          |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [Modelo de objeto de origem de mídia](media-source-object-model.md)<br/>                                 | Este tópico descreve o modelo de objeto para fontes de mídia no Microsoft Media Foundation<br/>                     |
| [Descritores de apresentação](presentation-descriptors.md)<br/>                                   | Um *descritor de apresentação* é um objeto que contém a descrição de uma apresentação específica.<br/>      |
| [Eventos de origem de mídia](media-source-events.md)<br/>                                             | Este tópico lista os eventos que são enviados por fontes de mídia e fluxos de mídia.<br/>                             |
| [Escrevendo uma fonte de mídia personalizada](writing-a-custom-media-source.md)<br/>                         | Este tópico descreve como implementar uma fonte de mídia personalizada no Media Foundation.<br/>                          |
| [Estudo de caso: fonte de mídia MPEG-1](tutorial--writing-a-custom-media-source.md)<br/>             | Este tópico aborda detalhadamente o Exemplo de SDK de Origem de Mídia [MPEG-1.](mpeg1source-sample.md)<br/>        |
| [Provedores de metadados personalizados para arquivos de mídia](custom-metadata-providers-for-media-files.md)<br/> | Este tópico descreve como escrever um manipulador de propriedades do Shell personalizado para uma Media Foundation de mídia.<br/>    |
| [Resolvedor de Origem](source-resolver.md)<br/>                                                     | O resolvedor de origem utiliza um fluxo de bytes ou uma URL e cria a origem de mídia adequada para esse conteúdo.<br/> |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Media Foundation Pipeline](media-foundation-pipeline.md)
</dt> <dt>

[Provedores de metadados personalizados para arquivos de mídia](custom-metadata-providers-for-media-files.md)
</dt> <dt>

[Arquitetura Media Foundation](media-foundation-architecture.md)
</dt> </dl>

 

 




