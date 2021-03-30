---
title: Granularidade da parte de vídeo e áudio
description: Granularidade da parte de vídeo e áudio
ms.assetid: 02c94de7-c7cb-4150-8b3e-0542d317c19b
keywords:
- Arquivos AVI, granularidade de partes
- Classe AVICap, partes de preenchimento
- WM_CAP_GET_SEQUENCE_SETUP mensagem
- macro capCaptureGetSetup
- WM_CAP_SET_SEQUENCE_SETUP mensagem
- macro capCaptureSetSetup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f2245b133fbf14bfd6403fa2f3d7e02ed328de6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916387"
---
# <a name="video-and-audio-chunk-granularity"></a>Granularidade da parte de vídeo e áudio

A granularidade da parte é um tamanho de bloco lógico para um arquivo AVI que é usado para gravar e recuperar partes de dados de áudio e vídeo. Ao gravar partes de áudio e vídeo em disco, o AVICap adiciona partes de preenchimento (partes "lixo eletrônico" do RIFF) conforme necessário para preencher cada bloco lógico de dados.

Você pode recuperar a configuração de granularidade de bloco atual usando a mensagem de [**\_ \_ \_ \_ configuração de sequência Get da Cap do WM**](wm-cap-get-sequence-setup.md) (ou a macro [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ). A granularidade de bloco atual é armazenada no membro **wChunkGranularity** da estrutura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) . Você pode especificar uma nova granularidade de bloco como o valor de **wChunkGranularity** e, em seguida, enviar a estrutura **CAPTUREPARMS** atualizada para a janela de captura usando a mensagem de [**configuração de sequência do WM \_ Cap \_ set \_ Sequence \_**](wm-cap-set-sequence-setup.md) (ou a macro [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) ). Você também pode especificar zero para esse membro para definir a granularidade da parte para o tamanho do setor do disco.

 

 




