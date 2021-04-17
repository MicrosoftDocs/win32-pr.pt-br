---
title: Sobre a classe da janela MCIWnd
description: Sobre a classe da janela MCIWnd
ms.assetid: 7dde7346-5853-4c8f-8788-bf74d01ece83
keywords:
- Classe de janela MCIWnd, sobre
- Função MCIWndCreate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e459a0e7d93543af126287a776b64130595ad11
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364043"
---
# <a name="about-the-mciwnd-window-class"></a>Sobre a classe da janela MCIWnd

A classe de janela MCIWnd é fácil de usar. Usando uma única função, [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) seu aplicativo pode criar um controle que reproduza qualquer dispositivo que use a interface de controle de mídia (MCI). Esses dispositivos incluem áudio de CD, formato de onda-áudio, MIDI e dispositivos de vídeo.

Automatizar a reprodução também é rápido e fácil. Usando apenas uma função e duas macros, um aplicativo pode criar uma janela MCIWnd com o dispositivo de mídia apropriado, reproduzir o dispositivo e fechar o dispositivo e a janela quando o conteúdo tiver terminado a execução.

> [!Note]  
> Alguns dispositivos executam conteúdo armazenado em arquivos. Outros dispositivos, como dispositivos de CD de áudio, executam conteúdo que é armazenado em outra mídia. Para fins de clareza, essa visão geral se refere a ambas as circunstâncias como "reproduzir o dispositivo".

 

 

 




