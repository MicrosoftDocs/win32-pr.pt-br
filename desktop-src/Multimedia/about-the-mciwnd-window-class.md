---
title: Sobre a classe de janela MCIWnd
description: Sobre a classe de janela MCIWnd
ms.assetid: 7dde7346-5853-4c8f-8788-bf74d01ece83
keywords:
- Classe de janela MCIWnd, sobre
- Função MCIWndCreate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07a75f9798c1bfe0ec4f67da0f990018143efd0285541b49a9035b9749a36de1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065656"
---
# <a name="about-the-mciwnd-window-class"></a>Sobre a classe de janela MCIWnd

A classe MCIWnd Window é fácil de usar. Usando uma única função, [**MCIWndCriar**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) seu aplicativo pode criar um controle que reproduz qualquer dispositivo que use a MCI (interface de controle de mídia). Esses dispositivos incluem áudio de CD, waveform-audio, MIDI e dispositivos de vídeo.

Automatizar a reprodução também é rápido e fácil. Usando apenas uma função e duas macros, um aplicativo pode criar uma janela MCIWnd com o dispositivo de mídia apropriado, reproduzir o dispositivo e fechar o dispositivo e a janela quando o conteúdo terminar de reproduzir.

> [!Note]  
> Alguns dispositivos reproduzem o conteúdo armazenado em arquivos. Outros dispositivos, como dispositivos de áudio DE CD, reproduzem o conteúdo armazenado em outro meio. Para fins de clareza, esta visão geral refere-se a ambas as circunstâncias como "reprodução do dispositivo".

 

 

 




