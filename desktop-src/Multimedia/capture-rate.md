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
ms.openlocfilehash: 855cff56e36d9a246e1f18ae5fc4e3c09a200a2114104424f053a8780881de93
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691656"
---
# <a name="capture-rate"></a>Taxa de captura

A taxa de captura é o número de quadros capturados a cada segundo de uma sessão de captura. Você pode recuperar a taxa de captura atual usando a mensagem de [**\_ \_ \_ \_ configuração de sequência Get da Cap do WM**](wm-cap-get-sequence-setup.md) (ou a macro [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ). A taxa de captura atual é armazenada no membro **dwRequestMicroSecPerFrame** da estrutura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) . Você pode definir a taxa de captura especificando o número de microssegundos entre os quadros sucessivos como o valor desse membro e, em seguida, enviando a estrutura **CAPTUREPARMS** atualizada para a janela de captura usando a mensagem de [**configuração da sequência do WM \_ Cap \_ set \_ \_ Sequence**](wm-cap-set-sequence-setup.md) (ou a macro [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) ). O valor padrão de **dwRequestMicroSecPerFrame** é 66667, que corresponde a 15 quadros por segundo.

 

 




