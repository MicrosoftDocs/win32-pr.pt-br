---
title: Erros de Waveform-Audio
description: Erros de Waveform-Audio
ms.assetid: c898552a-a60a-4deb-ab4a-ed74b08a7d05
keywords:
- Valores de retorno de MCIERR, formato de onda-erros de áudio
- referência de multimídia, erros de wave-áudio
- referência para multimídia, erros de wave-áudio
- MCI (Media Control interface), erros de wave-áudio
- MCI (interface de controle de mídia), erros de formato de onda-áudio
- referência de erros MCI, wave-áudio
- Referência MCI, erros de áudio de onda
- MCI (interface de controle de mídia), erros
- MCI (interface de controle de mídia), erros
- referência para MCI, erros
- Referência de MCI, erros
- formato de onda-erros de áudio
- Formato de onda MCI-erros de áudio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faf64e8cd4ec6d061422bcf14d17dfb4c4317ee4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005113"
---
# <a name="waveform-audio-errors"></a>Erros de Waveform-Audio

Os seguintes valores de retorno adicionais são definidos para dispositivos MCI Wave-Audio:



| Valor                             | Significado                                                                                                                                                             |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MCIERR \_ Wave \_ INPUTSINUSE         | Todos os dispositivos de forma de onda que podem gravar arquivos no formato atual estão em uso. Aguarde até que um desses dispositivos seja gratuito; em seguida, tente novamente.                              |
| MCIERR \_ Wave \_ INPUTSUNSUITABLE    | Nenhum dispositivo de forma de onda instalado pode gravar arquivos no formato atual. Use a opção drivers do painel de controle para instalar um dispositivo de gravação de formato de onda adequado. |
| MCIERR \_ Wave \_ INPUTUNSPECIFIED    | Você pode especificar qualquer dispositivo de gravação de formato de onda compatível.                                                                                                           |
| MCIERR \_ Wave \_ OUTPUTSINUSE        | Todos os dispositivos de forma de onda que podem reproduzir arquivos no formato atual estão em uso. Aguarde até que um desses dispositivos seja gratuito; em seguida, tente novamente.                                |
| MCIERR \_ Wave \_ OUTPUTSUNSUITABLE   | Nenhum dispositivo de forma de onda instalado pode reproduzir arquivos no formato atual. Use a opção drivers do painel de controle para instalar um dispositivo de formato de onda adequado.             |
| MCIERR \_ Wave \_ OUTPUTUNSPECIFIED   | Você pode especificar qualquer dispositivo de reprodução de formato de onda compatível.                                                                                                            |
| MCIERR \_ Wave \_ SETINPUTINUSE       | O dispositivo de formato de onda atual está em uso. Aguarde até que o dispositivo seja gratuito; em seguida, tente definir o dispositivo novamente para gravação.                                              |
| MCIERR \_ Wave \_ SETINPUTUNSUITABLE  | O dispositivo que você está usando para registrar uma forma de onda não pode reconhecer o formato de dados.                                                                                     |
| MCIERR \_ Wave \_ SETOUTPUTINUSE      | O dispositivo de formato de onda atual está em uso. Aguarde até que o dispositivo seja gratuito; em seguida, tente definir o dispositivo novamente para reprodução.                                               |
| MCIERR \_ Wave \_ SETOUTPUTUNSUITABLE | O dispositivo que você está usando para reproduzir uma forma de onda não pode reconhecer o formato de dados.                                                                                   |



 

 

 




