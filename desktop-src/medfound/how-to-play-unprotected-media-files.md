---
description: Este tutorial mostra como reproduzir arquivos de mídia usando o objeto Sessão de Mídia.
ms.assetid: cdd67082-8153-4f48-abc5-278be82ae082
title: Como reproduzir arquivos de mídia com Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65ba44212227be87e78d29c60a76bc3acdc2b1483b1029c62dd288bb7434b2a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117878851"
---
# <a name="how-to-play-media-files-with-media-foundation"></a>Como reproduzir arquivos de mídia com Media Foundation

Este tutorial mostra como reproduzir arquivos de mídia usando o [objeto Sessão de](media-session.md) Mídia.

## <a name="prerequisites"></a>Pré-requisitos

Antes de ler este tópico, você deve estar familiarizado com os seguintes Media Foundation conceitos:

-   [Sessão de mídia](media-session.md)
-   [Resolvedor de Origem](source-resolver.md)
-   [Topologias](topologies.md)
-   [Geradores de eventos de mídia](media-event-generators.md)
-   [Descritores de apresentação](presentation-descriptors.md)

> [!Note]  
> Este tópico não descreve como reproduzir arquivos protegidos pelo DRM (gerenciamento de direitos digitais). Para obter informações sobre o DRM Microsoft Media Foundation, [consulte How to Play Protected Media Files](how-to-play-protected-media-files.md).

 

## <a name="overview"></a>Visão geral

Os seguintes objetos são usados para reproduzir um arquivo de mídia com a Sessão de Mídia:

-   Uma *fonte de* mídia é um objeto que analisado um arquivo de mídia ou outra fonte de dados de mídia. A fonte de mídia cria *objetos de* fluxo para cada fluxo de áudio ou vídeo no arquivo. *Os decodificadores* convertem dados de mídia codificados em áudio e vídeo descompactados.
-   O *Resolvedor de Origem* cria uma fonte de mídia de uma URL.
-   O [EVR (Renderização de](enhanced-video-renderer.md) Vídeo Aprimorado) renderiza o vídeo na tela.
-   O [SAR (Streaming Audio Renderer)](streaming-audio-renderer.md) renderiza áudio para um locutor ou outro dispositivo de saída de áudio.
-   Uma *topologia* define o fluxo de dados da fonte de mídia para o EVR e o SAR.
-   A *Sessão de Mídia* controla o fluxo de dados e envia eventos de status para o aplicativo. O diagrama a seguir ilustra esse processo.

![diagrama mostrando a reprodução usando a sessão de mídia](images/session-playback.gif)

Veja a seguir uma delineia geral das etapas necessárias para reproduzir um arquivo de mídia usando a Sessão de Mídia:

1.  Chame a [**função MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) para inicializar a Media Foundation plataforma.
2.  Chame [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) para criar uma nova instância da Sessão de Mídia.
3.  Use o resolvedor de origem para criar uma fonte de mídia. Para obter mais informações, consulte [Usando o resolvedor de origem](using-the-source-resolver.md).
4.  Crie uma topologia que conecte a fonte de mídia ao EVR e à SAR. Nesta etapa, o aplicativo cria *uma* topologia parcial que não inclui os decodificadores. Para obter mais informações, consulte [Criando topologias de reprodução](creating-playback-topologies.md).
5.  Chame [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) para definir a topologia na Sessão de Mídia.
6.  Use a [**interface IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) para obter eventos da Sessão de Mídia.
7.  Chame [**IMFMediaSession::Start para**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) iniciar a reprodução. Depois que a reprodução é iniciada, você pode pausar chamando [**IMFMediaSession::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause)ou parando chamando [**IMFMediaSession::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop).
8.  Quando o aplicativo for final, libere recursos:

    1.  Chame [**IMFMediaSession::Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) para fechar a Sessão de Mídia. Esse método é assíncrono. Quando ela for concluída, a Sessão de Mídia enviará [um evento MESessionClosed.](mesessionclosed.md) Em seguida, é seguro executar as etapas restantes.
    2.  Chame [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) para desligar a fonte de mídia.
    3.  Chame [**IMFMediaSession::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown) para desligar a Sessão de Mídia.
    4.  Chame [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) para desligar a Media Foundation plataforma.

As seções a seguir mostram um exemplo de código completo:

-   [Etapa 1: Declarar a classe CPlayer](step-1--declare-the-cplayer-class.md)
-   [Etapa 2: Criar o objeto CPlayer](step-2--create-the-cplayer-object.md)
-   [Etapa 3: Abrir um arquivo de mídia](step-3--open-a-media-file.md)
-   [Etapa 4: Criar a sessão de mídia](step-4--create-the-media-session.md)
-   [Etapa 5: Manipular eventos de sessão de mídia](step-5--handle-media-session-events.md)
-   [Etapa 6: Controlar a reprodução](step-6--control-playback.md)
-   [Etapa 7: Desligar sessão de mídia](step-7--shut-down-the-media-session.md)
-   [Exemplo de reprodução de sessão de mídia](media-session-playback-example.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sessão de mídia](media-session.md)
</dt> <dt>

[Reprodução de áudio/vídeo](audio-video-playback.md)
</dt> </dl>

 

 



