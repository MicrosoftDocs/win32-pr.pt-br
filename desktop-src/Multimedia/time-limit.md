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
ms.openlocfilehash: 878c76ab1e380fe878cd8c9493163bcb71e574cf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103637215"
---
# <a name="time-limit"></a>Limite de tempo

Você pode limitar a duração de uma operação de captura usando os membros **fLimitEnabled** e **WTimeLimit** da estrutura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) . O membro **fLimitEnabled** indica se a operação de captura deve ser demorada, enquanto **wTimeLimit** especifica a duração máxima da operação de captura.

Você pode recuperar os valores para **fLimitEnabled** e **wTimeLimit** usando a mensagem [**de \_ \_ configuração de \_ sequência \_ Get da Cap do WM**](wm-cap-get-sequence-setup.md) (ou a macro [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ). Você pode habilitar um temporizador para a operação de captura especificando **true** como o valor de **fLimitEnabled**, ou pode definir a duração da operação de captura especificando um valor, em segundos, para **wTimeLimit**. Depois de definir esses membros, envie a estrutura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) atualizada para a janela de captura usando a mensagem de [**configuração da sequência do WM \_ Cap \_ set \_ Sequence \_**](wm-cap-set-sequence-setup.md) (ou a macro [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) ). O valor padrão de **fLimitEnabled** é **false**.

 

 




