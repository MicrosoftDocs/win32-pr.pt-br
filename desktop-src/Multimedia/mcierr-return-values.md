---
title: Valores de retorno de MCIERR
description: Valores de retorno de MCIERR
ms.assetid: 61f7b128-b4f7-4385-9daf-e2bc9fb36e24
keywords:
- Multimídia do Windows, valores de retorno do MCIERR
- multimídia, valores de retorno de MCIERR
- referência de multimídia, valores de retorno de MCIERR
- referência para multimídia, valores de retorno de MCIERR
- MCIERR valores de retorno, sobre
- função mciSendCommand
- função mciSendString
- Multimídia do Windows, erros
- multimídia, erros
- referência de multimídia, erros
- referência para multimídia, erros
- MCI (interface de controle de mídia), valores de retorno de MCIERR
- MCI (interface de controle de mídia), valores de retorno de MCIERR
- referência para MCI, MCIERR valores de retorno
- Referência de MCI, valores de retorno de MCIERR
- MCI (interface de controle de mídia), erros
- MCI (interface de controle de mídia), erros
- referência para MCI, erros
- Referência de MCI, erros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8912284b98b2aacb60905e3fef4dc32705a5656
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105758605"
---
# <a name="mcierr-return-values"></a>Valores de retorno de MCIERR

As funções [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) e [**mciSendString**](/previous-versions//dd757161(v=vs.85)) retornarão zero se forem bem-sucedidas; caso contrário, eles retornam um valor **DWORD** que contém um dos seguintes valores de erro na palavra inferior.

-   [Erros gerais de MCI](general-mci-errors.md)
-   [Erros de mciSendString](mcisendstring-errors.md)
-   [Erros de vídeo digital](digital-video-errors.md)
-   [Erros do Sequencer](sequencer-errors.md)
-   [Formato de onda-erros de áudio](waveform-audio-errors.md)

Você pode obter uma descrição de valores de retorno individuais passando os valores de retorno para a função [**mciGetErrorString**](/previous-versions//dd757158(v=vs.85)) .

 

 