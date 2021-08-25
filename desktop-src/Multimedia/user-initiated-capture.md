---
title: User-Initiated captura
description: User-Initiated captura
ms.assetid: e0d245f3-ac79-42c4-9969-8c9ec66eac62
keywords:
- WM_CAP_GET_SEQUENCE_SETUP mensagem
- macro capCaptureGetSetup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ca015726aabe7c171f37590a98e60774c34a09c219ef445af3e30f199d5030b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119892446"
---
# <a name="user-initiated-capture"></a>User-Initiated captura

Você pode recuperar o valor atual do sinalizador de captura iniciado pelo usuário usando a mensagem [**WM CAP GET SEQUENCE \_ \_ \_ \_ SETUP**](wm-cap-get-sequence-setup.md) (ou a [**macro capCaptureGetSetup).**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) O valor do sinalizador é armazenado no **membro fMakeUserHitOKToCapture** da [**estrutura CAPTUREPARMS.**](/windows/win32/api/vfw/ns-vfw-captureparms) Você pode fornecer ao usuário controle preciso sobre quando iniciar uma sessão de captura definindo esse membro como **TRUE.** O AVICap exibe uma caixa de diálogo depois de alocar todos os buffers de vídeo e áudio para uma sessão de captura. Isso permite que o usuário elimine atrasos de captura devido à inicialização de software. Se seu aplicativo usar um pequeno número de buffers de vídeo, essa caixa de diálogo provavelmente será desnecessária. O valor padrão é **FALSE**.

 

 




