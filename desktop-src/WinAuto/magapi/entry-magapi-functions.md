---
title: Funções (API de ampliação)
description: Esta seção contém informações de referência sobre as funções da API de ampliação.
ms.assetid: 82b7d82b-b8cd-4f80-ad30-f7db20c57742
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: 33418b0d74ec55b7e67cdf5a6130cbd867186dac
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/26/2021
ms.locfileid: "105816048"
---
# <a name="magnification-api-functions"></a>Funções da API de ampliação

Esta seção contém informações de referência sobre as funções da API de ampliação.

## <a name="in-this-section"></a>Nesta seção

| Tópico | Descrição |
|:---|:---|
| [**MagGetColorEffect**](/windows/win32/api/Magnification/nf-magnification-maggetcoloreffect)<br/> | Obtém a matriz de transformação de cor para um controle de lupa.<br/> |
| [**MagGetFullscreenColorEffect**](/windows/win32/api/Magnification/nf-magnification-maggetfullscreencoloreffect)<br/>  |  Recupera a matriz de transformação de cor associada à lupa de tela inteira.<br/> |
| [**MagGetFullscreenTransform**](/windows/win32/api/Magnification/nf-magnification-maggetfullscreentransform)<br/>  | Recupera as configurações de ampliação para a lupa de tela inteira.<br/>  |
| [***MagGetImageScalingCallback** _](/windows/win32/api/Magnification/nf-magnification-maggetimagescalingcallback)<br/>  | _ * Preterido no Windows 7 e posterior * *<br/>Recupera a função de retorno de chamada registrada que implementa uma transformação personalizada para o dimensionamento de imagem. <br/> |
| [**MagGetInputTransform**](/windows/win32/api/Magnification/nf-magnification-maggetinputtransform)<br/>  | Recupera a transformação de entrada atual para a entrada de caneta e toque, representada como um retângulo de origem e um retângulo de destino.<br/>  |
| [**MagGetWindowFilterList**](/windows/win32/api/Magnification/nf-magnification-maggetwindowfilterlist)<br/>  | Recupera a lista de janelas que são ampliadas ou excluídas da ampliação.<br/>  |
| [**MagGetWindowSource**](/windows/win32/api/Magnification/nf-magnification-maggetwindowsource)<br/>  | Obtém o retângulo da área que está sendo ampliada.<br/>  |
| [**MagGetWindowTransform**](/windows/win32/api/Magnification/nf-magnification-maggetwindowtransform)<br/>  | Recupera a matriz de transformação associada a um controle de lupa. <br/>  |
| [***MagImageScalingCallback** _](/windows/win32/api/Magnification/nc-magnification-magimagescalingcallback)<br/>  | _ * Preterido no Windows 7 e posterior * *<br/>Protótipo para uma função de retorno de chamada que implementa uma transformação personalizada para o dimensionamento da imagem.<br/>  |
| [**MagInitialize**](/windows/win32/api/Magnification/nf-magnification-maginitialize)<br/>  | Cria e inicializa os objetos de tempo de execução da lupa. <br/>  |
| [**MagSetColorEffect**](/windows/win32/api/Magnification/nf-magnification-magsetcoloreffect)<br/>  | >define a matriz de transformação de cor para um controle de lupa.<br/>  |
| [**MagSetFullscreenColorEffect**](/windows/win32/api/Magnification/nf-magnification-magsetfullscreencoloreffect)<br/>  | Altera a matriz de transformação de cor associada à lupa de tela inteira.<br/>  |
| [**MagSetFullscreenTransform**](/windows/win32/api/Magnification/nf-magnification-magsetfullscreentransform)<br/>  | Altera as configurações de ampliação para a lupa de tela inteira.<br/>  |
| [***MagSetImageScalingCallback** _](/windows/win32/api/Magnification/nf-magnification-magsetimagescalingcallback)<br/>  | _ * Preterido no Windows 7 e posterior * *<br/>Define a função de retorno de chamada para o dimensionamento e a filtragem de imagens externas.<br/>  |
| [**MagSetInputTransform**](/windows/win32/api/Magnification/nf-magnification-magsetinputtransform)<br/>  | Define a transformação de entrada ativa atual para a entrada de caneta e toque, representada como um retângulo de origem e um retângulo de destino.<br/>  |
| [**MagSetWindowFilterList**](/windows/win32/api/Magnification/nf-magnification-magsetwindowfilterlist)<br/>  | Define a lista de janelas a serem ampliadas ou a lista de janelas a serem excluídas da ampliação.<br/>  |
| [**MagSetWindowSource**](/windows/win32/api/Magnification/nf-magnification-magsetwindowsource)<br/>  | Define o retângulo de origem para a janela de ampliação.<br/>  |
| [**MagSetWindowTransform**](/windows/win32/api/Magnification/nf-magnification-magsetwindowtransform)<br/>  | Define a matriz de transformação para um controle de lupa. <br/>  |
| [**MagShowSystemCursor**](/windows/win32/api/Magnification/nf-magnification-magshowsystemcursor)<br/>  | Mostra ou oculta o cursor do sistema.<br/>  |
| [**MagUninitialize**](/windows/win32/api/Magnification/nf-magnification-maguninitialize)<br/>  | Destrói os objetos de tempo de execução da lupa.<br/>  |

## <a name="related-topics"></a>Tópicos relacionados

[Referência](entry-magapi-ref.md)
