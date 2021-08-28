---
title: Granularidade de partes de áudio e vídeo
description: Granularidade de partes de áudio e vídeo
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
ms.openlocfilehash: c8e8e03eb774e4173b86812c7cc4e9fb35d0ab2557d1ab9022bce3848ec7d13a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119892236"
---
# <a name="video-and-audio-chunk-granularity"></a>Granularidade de partes de áudio e vídeo

A granularidade da parte é um tamanho de bloco lógico para um arquivo AVI usado para escrever e recuperar partes de dados de áudio e vídeo. Ao escrever blocos de áudio e vídeo no disco, o AVICap adiciona partes de preenchimento (partes de "LIXO ELETRÔNICO" DO TIME) conforme necessário para preencher cada bloco lógico de dados.

Você pode recuperar a configuração de granularidade de partes atual usando a mensagem [**WM CAP GET SEQUENCE \_ \_ \_ \_ SETUP**](wm-cap-get-sequence-setup.md) (ou a [**macro capCaptureGetSetup).**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) A granularidade da parte atual é armazenada no **membro wChunkGranularity** da [**estrutura CAPTUREPARMS.**](/windows/win32/api/vfw/ns-vfw-captureparms) Você pode especificar uma nova granularidade de partes como o valor **de wChunkGranularity** e, em seguida, enviar a estrutura **CAPTUREPARMS** atualizada para a janela de captura usando a mensagem [**WM CAP SET SEQUENCE \_ \_ \_ \_ SETUP**](wm-cap-set-sequence-setup.md) (ou a macro [**capCaptureSetSetup).**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) Você também pode especificar zero para esse membro definir a granularidade da parte para o tamanho do setor do disco.

 

 




