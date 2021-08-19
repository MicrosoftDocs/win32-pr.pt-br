---
title: Valores de retorno do MCIERR
description: Valores de retorno do MCIERR
ms.assetid: 61f7b128-b4f7-4385-9daf-e2bc9fb36e24
keywords:
- Windows multimídia, valores de retorno do MCIERR
- multimídia, valores de retorno do MCIERR
- referência multimídia, valores de retorno do MCIERR
- referência para multimídia, valores de retorno do MCIERR
- Valores de retorno do MCIERR, sobre
- Função mciSendCommand
- Função mciSendString
- Windows multimídia, erros
- multimídia, erros
- referência de multimídia, erros
- referência para multimídia, erros
- MCI (Interface de Controle de Mídia), valores de retorno do MCIERR
- MCI (Interface de Controle de Mídia), valores de retorno do MCIERR
- referência para valores de retorno MCI,MCIERR
- Referência de MCI, valores de retorno do MCIERR
- MCI (Interface de Controle de Mídia), erros
- MCI (Interface de Controle de Mídia), erros
- referência para MCI, erros
- Referência de MCI, erros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57fc8426b264f68d7a6ab793e365d529774c931e72d89536b40b22592728a2ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119783406"
---
# <a name="mcierr-return-values"></a>Valores de retorno do MCIERR

As [**funções mciSendCommand**](/previous-versions//dd757160(v=vs.85)) e [**mciSendString**](/previous-versions//dd757161(v=vs.85)) retornarão zero se elas são bem-sucedidas; caso contrário, eles retornarão **um valor DWORD** que contém um dos seguintes valores de erro na palavra baixa.

-   [Erros gerais de MCI](general-mci-errors.md)
-   [Erros mciSendString](mcisendstring-errors.md)
-   [Erros de vídeo digital](digital-video-errors.md)
-   [Erros do Sequencer](sequencer-errors.md)
-   [Erros de waveform-audio](waveform-audio-errors.md)

Você pode obter uma descrição dos valores de retorno individuais passando os valores de retorno para a [**função mciGetErrorString.**](/previous-versions//dd757158(v=vs.85))

 

 