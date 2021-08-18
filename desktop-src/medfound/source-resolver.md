---
description: Resolvedor de Origem
ms.assetid: 93eecf10-308b-4bb4-92f9-fd32d6ecdb04
title: Resolvedor de Origem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d90ac92cc9d30c5dfb46be60812fbe3156e0f26e396ed1bb9006752ae9db47bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034734"
---
# <a name="source-resolver"></a>Resolvedor de Origem

O resolvedor de origem utiliza um fluxo de bytes ou uma URL e cria a origem de mídia adequada para esse conteúdo. O resolvedor de origem é o modo padrão para os aplicativos criarem origens de mídia.

Internamente, o resolvedor de origem usa *objetos de* manipulador:

-   *Os manipuladores de esquema* levam uma URL e criam uma fonte de mídia ou um fluxo de byte.
-   *Manipuladores de fluxo de byte* levam um fluxo de byte e criam uma fonte de mídia.

Você pode implementar um manipulador personalizado e adicioná-lo ao Registro. Manipuladores de esquema são registrados por esquema de URL e manipuladores de fluxo de byte são registrados por extensão de nome de arquivo ou tipo MIME.

Este tópico contém as seguintes seções:

-   [Usando o resolvedor de origem](using-the-source-resolver.md)
-   [Configurando uma fonte de mídia](configuring-a-media-source.md)
-   [Manipuladores de esquema e Byte-Stream manipuladores](scheme-handlers-and-byte-stream-handlers.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Fontes de mídia](media-sources.md)
</dt> </dl>

 

 



