---
title: Configuração de descompactador e Descompactador Descompactador
description: Configuração de descompactador e Descompactador Descompactador
ms.assetid: 677241d2-3ddd-423a-a1e7-b5fa3ce0a4eb
keywords:
- VCM (gerenciador de compactação de vídeo), configurando os vcms
- VCM (gerenciador de compactação de vídeo), configurando os vcs
- ICM_CONFIGURE mensagem
- Macro ICQueryConfigure
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8905ea35d65fc3eda3ddee130039503d8e26555665aae9efa517cb399349475
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144969"
---
# <a name="compressor-and-decompressor-configuration"></a>Configuração de descompactador e Descompactador Descompactador

Seu aplicativo pode configurar o descompactador ou o descompactador automaticamente ou pode permitir que o usuário os configure. Se for prático, permita que o usuário configure o descompactador ou o descompactador; isso o libera de considerar todas as opções para o descompactador ou o descompactador.

O usuário pode configurar o compactador ou o descompactador usando uma caixa de diálogo de configuração. Você pode enviar a [**mensagem ICM \_ CONFIGURAR**](icm-configure.md) para o VCM (ou usar a macro [**ICQueryConfigure)**](/windows/desktop/api/Vfw/nf-vfw-icqueryconfigure) para determinar se um descompactador ou um descompactador pode exibir uma caixa de diálogo de configuração. Em caso afirmacional, ICM a mensagem CONFIGURE (ou use a \_ macro [**ICConfigure)**](/windows/desktop/api/Vfw/nf-vfw-icconfigure) para exibi-la.

Seu aplicativo pode enviar as [**mensagens ICM \_ GETSTATE**](icm-getstate.md) e [**ICM \_ SETSTATE**](icm-setstate.md) (ou usar as macros [**ICGetStateSize,**](/windows/desktop/api/Vfw/nf-vfw-icgetstatesize) [**ICGetState**](/windows/desktop/api/Vfw/nf-vfw-icgetstate)e [**ICSetState)**](/windows/desktop/api/Vfw/nf-vfw-icsetstate) para obter e definir o status de um compactador ou descompactador. Se o aplicativo criar ou modificar o status, ele deverá obter o layout dos dados de descompactador ou descompactador antes de restaurar seu status. Como alternativa, se seu aplicativo obtiver o status de umimpactador ou descompactador e usá-lo para restaurar o status em uma sessão subsequente, ele deverá garantir que ele restaure apenas as informações de status obtidas do grupo ou do descompactador que está usando no momento.

 

 




