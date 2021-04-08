---
title: Captura de User-Initiated
description: Captura de User-Initiated
ms.assetid: e0d245f3-ac79-42c4-9969-8c9ec66eac62
keywords:
- WM_CAP_GET_SEQUENCE_SETUP mensagem
- macro capCaptureGetSetup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db44049ff64f6e0187ed38ca78ca0d3e1f36d6ab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822872"
---
# <a name="user-initiated-capture"></a>Captura de User-Initiated

Você pode recuperar o valor atual do sinalizador de captura iniciado pelo usuário usando a mensagem [**de \_ \_ configuração de \_ sequência \_ Get da Cap do WM**](wm-cap-get-sequence-setup.md) (ou a macro [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ). O valor do sinalizador é armazenado no membro **fMakeUserHitOKToCapture** da estrutura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) . Você pode fornecer ao usuário um controle preciso sobre quando iniciar uma sessão de captura definindo esse membro como **true**. AVICap exibe uma caixa de diálogo depois de alocar todos os buffers de áudio e vídeo para uma sessão de captura. Isso permite que o usuário elimine os atrasos de captura devido à inicialização do software. Se seu aplicativo usar um pequeno número de buffers de vídeo, essa caixa de diálogo provavelmente será desnecessária. O valor padrão é **false**.

 

 




