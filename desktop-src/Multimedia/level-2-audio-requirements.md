---
title: Requisitos de áudio de nível 2
description: Requisitos de áudio de nível 2
ms.assetid: 203648f2-9d20-438d-975b-b80e50b0fb9b
keywords:
- PC de multimídia (MPC), nível 2
- MPC (PC de multimídia), nível 2
- Conselho de marketing para PC multimídia, nível 2
- Nível de MPC 2, requisitos de áudio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5a2bc9398a25ac916352f41ad2ddc2325820354d1c7beb511b03b27004fadd9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118139827"
---
# <a name="level-2-audio-requirements"></a>Requisitos de áudio de nível 2

O subsistema de áudio de um PC que satisfaça a especificação de nível 2 inclui os seguintes itens:

-   Um driver de CD-ROM com saídas de CD-DA (áudio Red Book) e controle de volume
-   Um DAC de 16 bits com as seguintes características:
    -   Amostragem linear de PCM (modulação de código de pulso)
    -   Recurso de transferência em buffer de DMA ou FIFO com interrupção no buffer vazio
    -   Taxas de amostra obrigatórias de 44,1, 22, 5 e 11, 25 kHz
    -   Canais estéreo
    -   Uso de largura de banda de CPU de 10% ou menos ao gerar áudio de taxa de amostragem de 22, 5 ou 11, 25 kHz ou uma largura de banda de CPU de 15% ou menos ao gerar áudio de taxa de amostragem de 44,1 kHz

<!-- -->

-   Um ADC de 16 bits com as seguintes características:
    -   Amostragem de PCM linear
    -   Recurso de transferência em buffer de DMA ou FIFO com interrupção no buffer vazio
    -   Taxas de amostra obrigatórias de 44,1, 22, 5 e 11, 25 kHz
    -   Entrada do microfone

<!-- -->

-   Recursos internos do sintetizador com multivoz, multitimbral, seis notas de melodia simultâneas mais duas notas de percussive simultâneas
-   Combinação interna com os seguintes recursos:
    -   Pode combinar três fontes de áudio e apresentar a saída como um som estéreo, um sinal de áudio no nível de linha no painel de fundo
    -   As fontes de mixagem são áudio, sintetizador e DAC do CD Red Book
    -   Cada fonte de mixagem tem um controle de volume de 3 bits com um cônico logarítmica

 

 




