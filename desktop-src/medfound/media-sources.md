---
description: Fontes de mídia
ms.assetid: 65132e7d-22f6-4209-bc58-f5ea86ebd514
title: Fontes de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbd69b63679ba73bc4049f37207b1d07940edada
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104172468"
---
# <a name="media-sources"></a>Fontes de mídia

As *fontes de mídia* são objetos que geram dados de mídia no pipeline de Media Foundation. Esta seção descreve as APIs de origem de mídia em detalhes. Leia esta seção se você estiver implementando uma fonte de mídia personalizada ou usando uma fonte de mídia fora do pipeline de Media Foundation.

Se seu aplicativo usar a camada de controle, ele precisará usar apenas um subconjunto limitado das APIs de origem de mídia. Para obter informações, consulte o tópico [usando fontes de mídia com a sessão de mídia](using-media-sources-with-the-media-session.md).

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                                 | Descrição                                                                                                          |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [Modelo de objeto de origem de mídia](media-source-object-model.md)<br/>                                 | Este tópico descreve o modelo de objeto para fontes de mídia no Microsoft Media Foundation<br/>                     |
| [Descritores de apresentação](presentation-descriptors.md)<br/>                                   | Um *descritor de apresentação* é um objeto que contém a descrição de uma apresentação específica.<br/>      |
| [Eventos de origem de mídia](media-source-events.md)<br/>                                             | Este tópico lista os eventos que são enviados por fontes de mídia e fluxos de mídia.<br/>                             |
| [Gravando uma fonte de mídia personalizada](writing-a-custom-media-source.md)<br/>                         | Este tópico descreve como implementar uma fonte de mídia personalizada no Media Foundation.<br/>                          |
| [Estudo de caso: fonte de mídia MPEG-1](tutorial--writing-a-custom-media-source.md)<br/>             | Este tópico faz uma análise detalhada do exemplo de SDK de [origem de mídia MPEG-1](mpeg1source-sample.md) .<br/>        |
| [Provedores de metadados personalizados para arquivos de mídia](custom-metadata-providers-for-media-files.md)<br/> | Este tópico descreve como gravar um manipulador de propriedades de shell personalizado para uma fonte de mídia Media Foundation.<br/>    |
| [Resolvedor de origem](source-resolver.md)<br/>                                                     | O resolvedor de origem utiliza um fluxo de bytes ou uma URL e cria a origem de mídia adequada para esse conteúdo.<br/> |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Pipeline de Media Foundation](media-foundation-pipeline.md)
</dt> <dt>

[Provedores de metadados personalizados para arquivos de mídia](custom-metadata-providers-for-media-files.md)
</dt> <dt>

[Arquitetura Media Foundation](media-foundation-architecture.md)
</dt> </dl>

 

 




