---
title: Configurações de captura de vídeo
description: Configurações de captura de vídeo
ms.assetid: f5c887ca-9430-4221-8748-5b389247b7a4
keywords:
- Estrutura CAPTUREPARMS
- WM_CAP_GET_SEQUENCE_SETUP mensagem
- macro capCaptureGetSetup
- WM_CAP_SET_SEQUENCE_SETUP mensagem
- macro capCaptureSetSetup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b50eb26170c8b1594d288cec903ef0c05867a24db2d5a89a6ad60f66eef4fd0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118135584"
---
# <a name="video-capture-settings"></a>Configurações de captura de vídeo

A estrutura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) contém os parâmetros de controle para transmissão de vídeo de streaming. Essa estrutura controla vários aspectos do processo de captura e permite que você execute as seguintes tarefas:

-   Especifique a taxa de quadros.
-   Especifique o número de buffers de vídeo alocados.
-   Desabilitar e habilitar a captura de áudio.
-   Especifique o intervalo de tempo para a captura.
-   Especifique se um dispositivo MCI (VCR ou VIDEODISC) será usado durante a captura.
-   Especifique o teclado ou controle de mouse para encerrar o streaming.
-   Especifique o tipo de média de vídeo aplicado durante a captura.

Você pode recuperar as configurações de captura atuais na estrutura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) enviando a mensagem [**de \_ \_ configuração de \_ sequência \_ Get da Cap do WM**](wm-cap-get-sequence-setup.md) (ou a macro [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ) para uma janela de captura. Você pode definir uma ou mais configurações de captura atuais atualizando os membros apropriados da estrutura **CAPTUREPARMS** e, em seguida, enviando a mensagem de [**configuração da sequência do WM \_ Cap \_ set \_ Sequence \_**](wm-cap-set-sequence-setup.md) (ou a macro [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) ) e **CAPTUREPARMS** para uma janela de captura.

 

 




