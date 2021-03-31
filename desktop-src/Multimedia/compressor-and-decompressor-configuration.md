---
title: Configuração de compactador e descompactador
description: Configuração de compactador e descompactador
ms.assetid: 677241d2-3ddd-423a-a1e7-b5fa3ce0a4eb
keywords:
- VCM (Gerenciador de compactação de vídeo), configurando os compactadores
- VCM (Gerenciador de compactação de vídeo), configurando os compactadores
- ICM_CONFIGURE mensagem
- Macro ICQueryConfigure
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a38fbbeb852d09296e5be7929738c9d4d71f118e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916198"
---
# <a name="compressor-and-decompressor-configuration"></a>Configuração de compactador e descompactador

Seu aplicativo pode configurar o compactador ou o descompactador automaticamente, ou pode permitir que o usuário os configure. Se for prático, permita que o usuário configure o compressor ou o descompactador; Isso lhe libera de considerar todas as opções para o compressor ou o descompactador.

O usuário pode configurar o compressor ou o descompactador usando uma caixa de diálogo de configuração. Você pode enviar a mensagem de [**\_ configuração de ICM**](icm-configure.md) para VCM (ou usar a macro [**ICQueryConfigure**](/windows/desktop/api/Vfw/nf-vfw-icqueryconfigure) ) para determinar se um compactador ou descompactador pode exibir uma caixa de diálogo de configuração. Nesse caso, envie a \_ mensagem ICM configure (ou use a macro [**ICConfigure**](/windows/desktop/api/Vfw/nf-vfw-icconfigure) ) para exibi-la.

Seu aplicativo pode enviar as mensagens de [**ICM \_ GetState**](icm-getstate.md) e [**ICM \_ SetState**](icm-setstate.md) (ou usar as macros [**ICGetStateSize**](/windows/desktop/api/Vfw/nf-vfw-icgetstatesize), [**ICGetState**](/windows/desktop/api/Vfw/nf-vfw-icgetstate)e [**ICSetState**](/windows/desktop/api/Vfw/nf-vfw-icsetstate) ) para obter e definir o status de um compressor ou descompactador. Se o seu aplicativo criar ou modificar o status, ele deverá obter o layout dos dados do compressor ou do descompactador antes de restaurar seu status. Como alternativa, se seu aplicativo obtiver o status de um compressor ou descompactador e usá-lo para restaurar o status em uma sessão subsequente, ele deverá garantir que ele restaura apenas as informações de status obtidas do compressor ou descompactador que está usando no momento.

 

 




