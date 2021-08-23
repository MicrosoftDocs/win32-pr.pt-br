---
title: Buffers de vídeo
description: Buffers de vídeo
ms.assetid: 0dfe01ec-f997-4e5e-a73d-e6b712d0e19e
keywords:
- WM_CAP_GET_SEQUENCE_SETUP mensagem
- macro capCaptureGetSetup
- WM_CAP_SET_SEQUENCE_SETUP mensagem
- macro capCaptureSetSetup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46a6493d22a495a56084e89d2b067c1cf9a874752b44b81f636b5a184b895199
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119687686"
---
# <a name="video-buffers"></a>Buffers de vídeo

Os buffers usados com a captura de vídeo residem no heap de memória. O número de buffers usados em uma operação de captura pode variar e depender do valor do membro **wNumVideoRequested** da estrutura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) e da memória do sistema disponível.

Você pode recuperar o valor atual dos buffers de vídeo solicitados usando a mensagem [**WM CAP GET SEQUENCE \_ \_ \_ \_ SETUP**](wm-cap-get-sequence-setup.md) (ou a [**macro capCaptureGetSetup).**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) O número atual solicitado de buffers de vídeo é armazenado no **membro wNumVideoRequested** da **estrutura CAPTUREPARMS.** Você pode solicitar o posicionamento e o número de buffers atualizando esse membro e, em seguida, enviando a estrutura **CAPTUREPARMS** atualizada para a janela de captura usando a mensagem [**WM CAP SET SEQUENCE \_ \_ \_ \_ SETUP**](wm-cap-set-sequence-setup.md) (ou a [**macro capCaptureSetSetup).**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup)

 

 




