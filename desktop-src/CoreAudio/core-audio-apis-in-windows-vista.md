---
description: APIs de áudio de núcleo
ms.assetid: 87ca9a31-1bc8-47ea-be00-40159d30e189
title: APIs de áudio de núcleo
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: 83488233240121ba2edcfd677484df67a452e479
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/20/2021
ms.locfileid: "105755822"
---
# <a name="core-audio-apis"></a>APIs de áudio de núcleo

> [!NOTE]
> Para obter exemplos de código, consulte [exemplos de SDK que usam as APIs de áudio de núcleo](/windows/win32/coreaudio/sdk-samples-that-use-the-core-audio-apis).

Esta documentação fornece informações sobre as APIs (interfaces de programação de aplicativo) de áudio principal para a família Microsoft Windows de sistemas operacionais. Ele fornece diretrizes para que os desenvolvedores de software acompanhem o desenvolvimento de aplicativos que usam as principais APIs de áudio no Windows Vista. Essas APIs eram novas no Windows Vista e não estão disponíveis em versões anteriores do Windows.

As APIs de áudio principais fornecem os meios para que os aplicativos de áudio acessem dispositivos de ponto de extremidade de áudio, como fones de ouvido e microfones. As principais APIs de áudio servem como base para APIs de áudio de nível superior, como o Microsoft DirectSound e as funções de **waveXxx** multimídia do Windows. A maioria dos aplicativos se comunica com as APIs de nível superior, mas alguns aplicativos com requisitos especiais talvez precisem se comunicar diretamente com as APIs de áudio principais.

A partir do Windows 7, as APIs existentes foram aprimoradas e novas APIs foram adicionadas para dar suporte a novos cenários. As APIs de gerenciamento de fluxo e de sessão foram aprimoradas para que o aplicativo agora possa enumerar e obter controle estendido sobre a sessão de áudio. Usando as novas APIs, o aplicativo pode implementar uma experiência de atenuação de fluxo personalizada. As novas APIs relacionadas ao dispositivo fornecem acesso às propriedades do driver dos dispositivos do ponto de extremidade.

Esta documentação inclui as seções a seguir.

| Seção                                                                    | Descrição                                                                       |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [Sobre as APIs de áudio do Windows Core](about-the-windows-core-audio-apis.md) | Fornece uma visão geral das APIs de áudio do Windows Core e descreve os conceitos básicos. |
| [Guia de programação](programming-guide.md)                                 | Descreve os principais recursos das principais APIs de áudio e como usá-las.            |
| [Referência de programação](programming-reference.md)                         | Fornece informações de referência do C++ para as APIs de áudio principal.                       |

## <a name="related-topics"></a>Tópicos relacionados

[Tecnologias de mídia para Windows](/previous-versions/bg125389(v=msdn.10))

[Exemplos de SDK que usam as APIs de áudio principal](/windows/win32/coreaudio/sdk-samples-that-use-the-core-audio-apis)
