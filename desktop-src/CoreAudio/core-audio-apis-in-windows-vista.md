---
description: APIs de áudio principais
ms.assetid: 87ca9a31-1bc8-47ea-be00-40159d30e189
title: APIs de áudio principais
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: 69c0c83700dabd3aa0298bcd6474b95c4c38bdf933c9867a4c639edee1e43379
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077640"
---
# <a name="core-audio-apis"></a>APIs de áudio principais

> [!NOTE]
> Para exemplos de código, consulte [Exemplos de SDK que usam as APIs de áudio principais](./sdk-samples-that-use-the-core-audio-apis.md).

Esta documentação fornece informações sobre apIs (interfaces de programação) de aplicativos de áudio principais para a família Windows microsoft de sistemas operacionais. Ele fornece diretrizes para desenvolvedores de software seguirem o desenvolvimento de aplicativos que usam as APIs de áudio principais no Windows Vista. Essas APIs eram novas no Windows Vista e não estão disponíveis em versões anteriores do Windows.

As APIs de áudio principais fornecem os meios para os aplicativos de áudio acessarem dispositivos de ponto de extremidade de áudio, como fones de ouvido e microfones. As APIs de áudio principais servem como base para APIs de áudio de nível superior, como Microsoft DirectSound e as funções waveXxx Windows **multimídia.** A maioria dos aplicativos se comunica com as APIs de nível superior, mas alguns aplicativos com requisitos especiais podem precisar se comunicar diretamente com as APIs de áudio principais.

A partir Windows 7, as APIs existentes foram aprimoradas e novas APIs foram adicionadas para dar suporte a novos cenários. As APIs de gerenciamento de fluxo e sessão foram aprimoradas para que o aplicativo agora possa enumerar e obter controle estendido sobre a sessão de áudio. Usando as novas APIs, o aplicativo pode implementar uma experiência de atenuação de fluxo personalizada. Novas APIs relacionadas ao dispositivo fornecem acesso às propriedades do driver dos dispositivos de ponto de extremidade.

Esta documentação inclui as seções a seguir.

| Seção                                                                    | Descrição                                                                       |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [Sobre as APIs Windows Core Audio](about-the-windows-core-audio-apis.md) | Fornece uma visão geral das Windows principais APIs de áudio e descreve conceitos básicos. |
| [Guia de programação](programming-guide.md)                                 | Descreve os principais recursos das PRINCIPAIS APIs de áudio e como usá-los.            |
| [Referência de programação](programming-reference.md)                         | Fornece informações de referência do C++ para as APIs de áudio principais.                       |

## <a name="related-topics"></a>Tópicos relacionados

[Tecnologias de mídia para Windows](/previous-versions/bg125389(v=msdn.10))

[Exemplos de SDK que usam as APIs de áudio principais](./sdk-samples-that-use-the-core-audio-apis.md)