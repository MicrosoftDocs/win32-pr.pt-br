---
title: Por que usar DirectShow
description: Por que usar DirectShow
ms.assetid: 0ab33526-73d0-425e-a03f-29c74555f578
keywords:
- Windows SDK de formato de mídia, DirectShow
- Windows SDK de Formato de Mídia, hardware
- Windows SDK de formato de mídia,Windows modelo de driver (WDM)
- ASF (Advanced Systems Format), DirectShow
- ASF (formato de sistemas avançados), DirectShow
- ASF (Advanced Systems Format), hardware
- ASF (Formato de Sistemas Avançados), hardware
- ASF (Advanced Systems Format), Windows WDM (Driver Model)
- ASF (formato de sistemas avançados), Windows WDM (Driver Model)
- DirectShow, sobre
- DirectShow, hardware
- DirectShow,Windows modelo de driver (WDM)
- Windows Modelo de driver (WDM)
- WDM (Windows driver)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a5edce48be7a806011ba59ab5a2c5328840a18399f6f7eea65d649d52c62402
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119839416"
---
# <a name="why-use-directshow"></a>Por que usar DirectShow?

Há dois motivos principais pelos quais um aplicativo pode usar o DirectShow em vez do SDK de Formato de Mídia do Windows diretamente: para a conveniência da arquitetura de streaming DirectShow e para acesso ao hardware.

## <a name="convenience"></a>Conveniência

Com DirectShow de streaming, são necessários apenas algumas chamadas de método para reproduzir Windows áudio de mídia ou Windows de vídeo de mídia. A criação de arquivos também é simplificada. Basta especificar um perfil usando a interface **IConfigAsfWriter** no filtro e o DirectShow carregar automaticamente os componentes necessários para renderizar ou escrever os fluxos e fornece os mecanismos para transferir e sincronizar o fluxo de dados de mídia. DirectShow é especialmente útil ao converter conteúdo de formatos variados em Windows Formato de Mídia. Você pode criar DirectShow de filtro que decodificam uma ampla variedade de tipos de arquivo e compactação e, em seguida, alimentar os fluxos decodificados no filtro [Wm ASF Writer.](wm-asf-writer-filter.md) Por comparação, o exemplo UncompAVItoWMV neste SDK funciona apenas com arquivos AVI descompactados. Fluxos de texto e fluxos de dados arbitrários também podem ser criados e/ou renderizados por meio de DirectShow, mas isso pode exigir que você crie filtros de DirectShow personalizados para processar esses fluxos.

## <a name="access-to-hardware"></a>Acesso ao hardware

DirectShow é a única maneira de o código do aplicativo acessar dispositivos de hardware baseados em WDM (modelo de driver) baseados em Windows, como câmeras DV 1394, tuners de TV e webcams USB. Se o aplicativo precisar capturar dados diretamente de um dispositivo de hardware baseado em WDM e transcodificá-los para o Formato de Mídia do Windows e o SDK do Codificador de Mídia do Windows não atender às suas necessidades, DirectShow será a única alternativa. DirectShow também pode ser usado para acessar dispositivos herdados com base em Vídeo para Windows.

 

 




