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
ms.openlocfilehash: b0ad32bd3983301687b0eb0bb01f0fd932a43944
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005444"
---
# <a name="measuring-video-quality"></a>Medindo a qualidade do vídeo

Uma maneira de medir a qualidade do vídeo é limitar o número de quadros capturados retirados durante a operação de captura. Quando a captura de streaming for concluída, o valor de qualidade será comparado com a taxa de quadros descartados para o total de quadros. Se a porcentagem de quadros descartados for maior que o valor do membro **wPercentDropForError** da estrutura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) , AVICap enviará uma mensagem de erro para a função de retorno de chamada de erro se ela estiver instalada.

Você pode recuperar o limite atual de quadros descartados (expresso como um percentual) usando a mensagem de [**\_ \_ \_ \_ configuração de sequência Get da Cap do WM**](wm-cap-get-sequence-setup.md) (ou a macro [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ). Você pode definir um novo limite especificando um percentual como o valor do membro **wPercentDropForError** da estrutura **CAPTUREPARMS** e, em seguida, enviando a estrutura atualizada para a janela de captura usando a mensagem [**de \_ configuração de sequência do WM Cap \_ set \_ Sequence \_**](wm-cap-set-sequence-setup.md) (ou a macro [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) ). O valor padrão de **wPercentDropForError** é 10%.

 

 




