---
description: Resolvedor de origem
ms.assetid: 93eecf10-308b-4bb4-92f9-fd32d6ecdb04
title: Resolvedor de origem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6a844893b0348546d4fd174b0b24405812efcef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296525"
---
# <a name="source-resolver"></a>Resolvedor de origem

O resolvedor de origem utiliza um fluxo de bytes ou uma URL e cria a origem de mídia adequada para esse conteúdo. O resolvedor de origem é o modo padrão para os aplicativos criarem origens de mídia.

Internamente, o resolvedor de origem usa objetos de *manipuladores* :

-   Os *manipuladores de esquema* usam uma URL e criam uma origem de mídia ou um fluxo de bytes.
-   Os *manipuladores de fluxo de bytes* usam um fluxo de bytes e criam uma fonte de mídia.

Você pode implementar um manipulador personalizado e adicioná-lo ao registro. Os manipuladores de esquema são registrados pelo esquema de URL e os manipuladores de fluxo de bytes são registrados por extensão de nome de arquivo ou tipo MIME.

Este tópico contém as seguintes seções:

-   [Usando o resolvedor de origem](using-the-source-resolver.md)
-   [Configurando uma origem de mídia](configuring-a-media-source.md)
-   [Manipuladores de esquema e manipuladores de Byte-Stream](scheme-handlers-and-byte-stream-handlers.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Fontes de mídia](media-sources.md)
</dt> </dl>

 

 



