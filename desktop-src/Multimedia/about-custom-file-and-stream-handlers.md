---
title: Sobre manipuladores de arquivo e fluxo personalizados
description: Sobre manipuladores de arquivo e fluxo personalizados
ms.assetid: 6a00c8db-3ac6-4826-a373-52b6b7d1652f
keywords:
- vídeo para Windows (VFW), manipuladores de arquivo personalizados
- vídeo para Windows (VFW), manipuladores de fluxo personalizados
- vídeo para Windows (VFW), manipuladores de arquivo
- vídeo para Windows (VFW), manipuladores de fluxo
- VFW (vídeo para Windows), manipuladores de arquivo personalizado
- VFW (vídeo para Windows), manipuladores de fluxo personalizados
- VFW (vídeo para Windows), manipuladores de arquivo
- VFW (vídeo para Windows), manipuladores de fluxo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 719c5312c5ba1e783e0cd4cdb81565f66241e4662772ca441283571f0335fb31
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145150"
---
# <a name="about-custom-file-and-stream-handlers"></a>Sobre manipuladores de arquivo e fluxo personalizados

Seu aplicativo pode usar um manipulador de arquivo personalizado para ler de um arquivo ou gravar em um arquivo que esteja em um formato não padrão. Para fazer isso, seu aplicativo simplesmente usa o nome do manipulador de arquivo ao abrir o arquivo ou alocar a interface de arquivo. Em seguida, a biblioteca AVIFile usa as funções do manipulador de arquivos, em vez daquelas de outro manipulador de arquivo. O formato não padrão aparece como dados AVI padrão para seu aplicativo ou para qualquer outro aplicativo usando seu manipulador de arquivo personalizado.

Da mesma forma, seu aplicativo pode usar um manipulador de fluxo personalizado para ler um fluxo que está em um formato não padrão. Um fluxo — se ele constitui áudio, vídeo, MIDI, texto ou dados personalizados — é um componente de um arquivo AVI. Por exemplo, um arquivo AVI que contém uma sequência de vídeo, uma trilha sonora em inglês e uma trilha sonora francesa consiste em três fluxos. Seu aplicativo pode especificar os fluxos em um arquivo AVI para processar e direcionar cada um desses fluxos para um manipulador que pode processar de forma ideal o tipo apropriado de dados de multimídia.

> [!Note]  
> Você deve posicionar os manipuladores de arquivo e fluxo personalizados em uma ou mais DLLs, separadas dos arquivos principais do aplicativo.

 

 

 




