---
title: Gerenciador de Janelas da Área de Trabalho
description: O recurso de composição de área de trabalho, introduzido no Windows Vista, mudou fundamentalmente a maneira como os aplicativos exibem pixels na tela.
ms.assetid: VS|winui|~\winui\desktopwindowmanager\overviews\dwm_overview.htm
keywords:
- Gerenciador de Janelas da Área de Trabalho (DWM), sobre
- DWM (Gerenciador de Janelas da Área de Trabalho), sobre
- Gerenciador de Janelas da Área de Trabalho (DWM), composição
- DWM (Gerenciador de Janelas da Área de Trabalho), composição
- composição de área de trabalho
- composição
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8578001aebf1c73e6d400ffae383674a8432c399
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636132"
---
# <a name="desktop-window-manager"></a>Gerenciador de Janelas da Área de Trabalho

O recurso de composição de área de trabalho, introduzido no Windows Vista, mudou fundamentalmente a maneira como os aplicativos exibem pixels na tela. Quando a composição de área de trabalho está habilitada, as janelas individuais não são mais desenhadas diretamente na tela ou no dispositivo de exibição primário como faziam nas versões anteriores do Windows. Em vez disso, seu desenho é redirecionado para superfícies fora da tela na memória de vídeo, que são então renderizados em uma imagem de área de trabalho e apresentados na exibição.

A composição de área de trabalho é executada pelo Gerenciador de Janelas da Área de Trabalho (DWM). Por meio da composição de área de trabalho, o DWM habilita efeitos visuais na área de trabalho, bem como vários recursos, como quadros de janela de vidro, animações de transição de janela 3D, Windows Flip e Windows Flip3D e suporte de alta resolução.

O Gerenciador de Janelas da Área de Trabalho é executado como um serviço do Windows. Ele pode ser habilitado e desabilitado por meio do item do painel de controle ferramentas administrativas, em serviços, como Gerenciador de Janelas da Área de Trabalho Gerenciador de sessão.

Muitos dos recursos do DWM podem ser controlados ou acessados por um aplicativo por meio das APIs do DWM. A documentação a seguir descreve os recursos e os requisitos das APIs do DWM.

-   [Visões gerais do DWM](desktop-window-manager-overviews.md)
-   [Código de exemplo do DWM](dwm-samples.md)
-   [Referência do DWM](reference.md)

 

 




