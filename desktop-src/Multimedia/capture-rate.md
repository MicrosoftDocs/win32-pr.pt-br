---
title: Taxa de captura
description: Taxa de captura
ms.assetid: 70cac7ac-0f7e-431e-a099-b075ba5fb039
keywords:
- WM_CAP_GET_SEQUENCE_SETUP mensagem
- macro capCaptureGetSetup
- Estrutura CAPTUREPARMS
- WM_CAP_SET_SEQUENCE_SETUP mensagem
- macro capCaptureSetSetup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93be9e94f5f9085d25c6ad85a30b115d13349169
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005519"
---
# <a name="capture-rate"></a>Taxa de captura

A taxa de captura é o número de quadros capturados a cada segundo de uma sessão de captura. Você pode recuperar a taxa de captura atual usando a mensagem de [**\_ \_ \_ \_ configuração de sequência Get da Cap do WM**](wm-cap-get-sequence-setup.md) (ou a macro [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ). A taxa de captura atual é armazenada no membro **dwRequestMicroSecPerFrame** da estrutura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) . Você pode definir a taxa de captura especificando o número de microssegundos entre os quadros sucessivos como o valor desse membro e, em seguida, enviando a estrutura **CAPTUREPARMS** atualizada para a janela de captura usando a mensagem de [**configuração da sequência do WM \_ Cap \_ set \_ \_ Sequence**](wm-cap-set-sequence-setup.md) (ou a macro [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) ). O valor padrão de **dwRequestMicroSecPerFrame** é 66667, que corresponde a 15 quadros por segundo.

 

 




