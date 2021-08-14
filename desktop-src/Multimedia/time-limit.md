---
title: Limite de tempo
description: Limite de tempo
ms.assetid: 7c07755b-ba4d-4ec0-82ee-f76a533c6c5b
keywords:
- Estrutura CAPTUREPARMS
- WM_CAP_GET_SEQUENCE_SETUP mensagem
- macro capCaptureGetSetup
- Estrutura CAPTUREPARMS
- WM_CAP_SET_SEQUENCE_SETUP mensagem
- macro capCaptureSetSetup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b6211edf3ce3fb86b4c0430c685ff05ff7f95c718c0a89e7ba782ae342feb18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117801260"
---
# <a name="time-limit"></a>Limite de tempo

Você pode limitar a duração de uma operação de captura usando os membros **fLimitEnabled** e **wTimeLimit** da [**estrutura CAPTUREPARMS.**](/windows/win32/api/vfw/ns-vfw-captureparms) O **membro fLimitEnabled** indica se a operação de captura deve ser timed, enquanto **wTimeLimit especifica** a duração máxima da operação de captura.

Você pode recuperar os valores para **fLimitEnabled** e **wTimeLimit** usando a mensagem [**WM CAP GET SEQUENCE \_ \_ \_ \_ SETUP**](wm-cap-get-sequence-setup.md) (ou a [**macro capCaptureGetSetup).**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) Você pode habilitar um temporizador para a operação de captura especificando **TRUE** como o valor **de fLimitEnabled** ou pode definir a duração da operação de captura especificando um valor, em segundos, para **wTimeLimit**. Depois de definir esses membros, envie a estrutura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) atualizada para a janela de captura usando a mensagem [**WM CAP SET SEQUENCE \_ \_ \_ \_ SETUP**](wm-cap-set-sequence-setup.md) (ou a [**macro capCaptureSetSetup).**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) O valor padrão de **fLimitEnabled** é **FALSE.**

 

 




