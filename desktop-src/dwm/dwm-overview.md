---
title: Gerenciador de Janelas da Área de Trabalho
description: O recurso de composição da área de trabalho, introduzido no Windows Vista, mudou fundamentalmente a maneira como os aplicativos exibem pixels na tela.
ms.assetid: VS|winui|~\winui\desktopwindowmanager\overviews\dwm_overview.htm
keywords:
- Gerenciador de Janelas da Área de Trabalho (DWM), sobre
- DWM (Gerenciador de Janelas da Área de Trabalho),sobre
- Gerenciador de Janelas da Área de Trabalho (DWM), composição
- DWM (Gerenciador de Janelas da Área de Trabalho),composição
- composição da área de trabalho
- Composição
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8259be171f225cc955546314febdff5395a47318499b830ee855bc8b985b025
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119456036"
---
# <a name="desktop-window-manager"></a>Gerenciador de Janelas da Área de Trabalho

O recurso de composição da área de trabalho, introduzido no Windows Vista, mudou fundamentalmente a maneira como os aplicativos exibem pixels na tela. Quando a composição da área de trabalho está habilitada, as janelas individuais não são mais desenhadas diretamente para a tela ou o dispositivo de exibição primário, como nas versões anteriores do Windows. Em vez disso, o desenho é redirecionado para superfícies fora da tela na memória de vídeo, que são renderizadas em uma imagem da área de trabalho e apresentadas na exibição.

A composição da área de trabalho é executada Gerenciador de Janelas da Área de Trabalho (DWM). Por meio da composição da área de trabalho, o DWM permite efeitos visuais na área de trabalho, bem como vários recursos, como quadros de janela de vidro, animações de transição de janela 3D, Windows Flip e Windows Flip3D e suporte de alta resolução.

O Gerenciador de Janelas da Área de Trabalho é executado como um Windows serviço. Ele pode ser habilitado e desabilitado por meio do item Ferramentas Administrativas Painel de Controle, em Serviços, como Gerenciador de Janelas da Área de Trabalho Session Manager.

Muitos dos recursos DWM podem ser controlados ou acessados por um aplicativo por meio das APIs DWM. A documentação a seguir descreve os recursos e requisitos das APIs DWM.

-   [Visão geral do DWM](desktop-window-manager-overviews.md)
-   [Código de exemplo DWM](dwm-samples.md)
-   [Referência de DWM](reference.md)

 

 




