---
title: Buffers de áudio
description: Buffers de áudio
ms.assetid: e18e9ff4-e8e9-4013-a800-1a30335026ff
keywords:
- WM_CAP_GET_SEQUENCE_SETUP mensagem
- macro capCaptureGetSetup
- WM_CAP_SET_SEQUENCE_SETUP mensagem
- macro capCaptureSetSetup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7993e3dc89abda520c0f1c5bda90f3eb209aca31e36071a304af01fb420d821e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692096"
---
# <a name="audio-buffers"></a>Buffers de áudio

Você pode controlar a parte de áudio de uma operação de captura de três maneiras:

-   Incluir ou excluir áudio da operação de captura.
-   Solicite um número específico de buffers de áudio.
-   Solicite que os buffers de áudio tenham um tamanho específico.

Você pode recuperar as configurações para buffers de áudio usando a mensagem de [**\_ \_ \_ \_ configuração de sequência Get da Cap do WM**](wm-cap-get-sequence-setup.md) (ou a macro [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ). O membro **fCaptureAudio** da estrutura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) especifica se o áudio é incluído ou excluído da operação de captura. O número atual solicitado de buffers de áudio é armazenado no membro **wNumAudioRequested** e o tamanho atual do buffer de áudio é armazenado no membro **dwAudioBufferSize** . Você pode especificar se deseja incluir a captura de áudio, especificar o tamanho e o número de buffers de áudio atualizando esses membros e enviar a estrutura **CAPTUREPARMS** atualizada para a janela de captura usando a mensagem de [**configuração da sequência do WM \_ Cap \_ set \_ \_ Sequence**](wm-cap-set-sequence-setup.md) (ou a macro [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) ).

Por padrão, o áudio é incluído na operação de captura e quatro buffers de áudio são alocados. O valor padrão de **fCaptureAudio** é **true**. O tamanho de buffer padrão (o valor de **dwAudioBufferSize**) pode conter 0,5 segundos de dados de áudio ou 10K, o que for maior.

 

 




