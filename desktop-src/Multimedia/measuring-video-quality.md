---
title: Medindo a qualidade do vídeo
description: Medindo a qualidade do vídeo
ms.assetid: e1e76bed-a632-45e8-a8b3-13dd6969e85a
keywords:
- WM_CAP_GET_SEQUENCE_SETUP mensagem
- macro capCaptureGetSetup
- WM_CAP_SET_SEQUENCE_SETUP mensagem
- macro capCaptureSetSetup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95d3a4d28c12905722447189eabc494b220d737fc0c87f7a9ebc12948390920d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118373452"
---
# <a name="measuring-video-quality"></a>Medindo a qualidade do vídeo

Uma maneira de medir a qualidade do vídeo é limitar o número de quadros capturados descartados durante a operação de captura. Quando a captura de streaming for concluída, o valor de qualidade será comparado com a taxa de quadros descartados para o total de quadros. Se a porcentagem de quadros descartados for maior que o valor do membro **wPercentDropForError** da estrutura [**CAPTUREPARMS,**](/windows/win32/api/vfw/ns-vfw-captureparms) o AVICap enviará uma mensagem de erro para a função de retorno de chamada de erro se ela estiver instalada.

Você pode recuperar o limite atual de quadros descartados (expresso como um percentual) usando a mensagem [**WM CAP GET SEQUENCE \_ \_ \_ \_ SETUP**](wm-cap-get-sequence-setup.md) (ou a [**macro capCaptureGetSetup).**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) Você pode definir um novo limite especificando um percentual como o valor do membro **wPercentDropForError** da estrutura **CAPTUREPARMS** e, em seguida, enviando a estrutura atualizada para a janela de captura usando a mensagem [**WM CAP SET SEQUENCE \_ \_ \_ \_ SETUP**](wm-cap-set-sequence-setup.md) (ou a [**macro capCaptureSetSetup).**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) O valor padrão **de wPercentDropForError** é 10%.

 

 




