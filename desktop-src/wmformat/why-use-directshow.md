---
title: Por que usar o DirectShow
description: Por que usar o DirectShow
ms.assetid: 0ab33526-73d0-425e-a03f-29c74555f578
keywords:
- SDK do Windows Media Format, DirectShow
- SDK do Windows Media Format, hardware
- SDK do Windows Media Format, Windows Driver Model (WDM)
- ASF (Advanced Systems Format), DirectShow
- ASF (formato de sistemas avançados), DirectShow
- ASF (Advanced Systems Format), hardware
- ASF (formato de sistemas avançados), hardware
- ASF (Advanced Systems Format), Windows Driver Model (WDM)
- ASF (formato de sistemas avançados), Windows Driver Model (WDM)
- DirectShow, sobre
- DirectShow, hardware
- DirectShow, Windows Driver Model (WDM)
- Windows Driver Model (WDM)
- WDM (Windows Driver Model)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f90fa1de01a7b136b938f9b09cc7fb2b3c229fad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635859"
---
# <a name="why-use-directshow"></a>Por que usar o DirectShow?

Há dois motivos principais pelos quais um aplicativo pode usar o DirectShow em vez do SDK do Windows Media Format diretamente: para a conveniência da arquitetura de streaming do DirectShow e para acesso ao hardware.

## <a name="convenience"></a>Conveniência

Com a arquitetura de streaming do DirectShow, é necessário apenas algumas chamadas de método para reproduzir arquivos de vídeo do Windows Media Audio ou Windows Media. A criação de arquivos também é simplificada. Você simplesmente especifica um perfil usando a interface **IConfigAsfWriter** no filtro, e o DirectShow carrega automaticamente os componentes necessários para renderizar ou gravar os fluxos e fornece os mecanismos para transferir e sincronizar o fluxo de dados de mídia. O DirectShow é especialmente útil ao converter o conteúdo de formatos variados no formato de mídia do Windows. Você pode criar gráficos de filtro do DirectShow que decodifiquem uma ampla variedade de tipos de arquivo e compactação e, em seguida, alimentar os fluxos decodificados no filtro de [gravador ASF do WM](wm-asf-writer-filter.md) . Por comparação, o exemplo de UncompAVItoWMV neste SDK funciona apenas com arquivos AVI não compactados. Fluxos de texto e fluxos de dados arbitrários também podem ser criados e/ou renderizados por meio do DirectShow, mas isso pode exigir que você crie filtros personalizados do DirectShow para processar esses fluxos.

## <a name="access-to-hardware"></a>Acesso ao hardware

O DirectShow é a única maneira de o código do aplicativo acessar dispositivos de hardware baseados em Windows Driver Model (WDM), como câmeras de vídeo 1394, sintonizadores de TV e webcams USB. Se seu aplicativo precisar capturar dados diretamente de um dispositivo de hardware baseado em WDM e transcodificar para o Windows Media Format, e o SDK do Windows Media Encoder não atender às suas necessidades, o DirectShow será a única alternativa. O DirectShow também pode ser usado para acessar dispositivos herdados com base em vídeo para Windows.

 

 




