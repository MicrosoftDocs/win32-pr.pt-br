---
title: Status da janela de captura
description: Status da janela de captura
ms.assetid: c3f80cac-30b2-42f0-8a9c-4053728c558b
keywords:
- WM_CAP_GET_STATUS mensagem
- macro capGetStatus
- Estrutura CAPSTATUS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e6019009c8510abe3429c1043527156c55f0c4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005912"
---
# <a name="capture-window-status"></a>Status da janela de captura

Você pode recuperar o status atual de uma janela de captura usando a mensagem de [**\_ \_ \_ status Get do WM Cap**](wm-cap-get-status.md) (ou a macro [**capGetStatus**](/windows/desktop/api/Vfw/nf-vfw-capgetstatus) ). Essa mensagem recupera uma cópia da estrutura [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) com os valores atuais de seus membros. A estrutura **CAPSTATUS** contém informações sobre as dimensões da imagem, a posição da rolagem e se a sobreposição ou visualização da imagem está habilitada. Como as informações representadas em **CAPSTATUS** são dinâmicas, o aplicativo deve atualizar o conteúdo da estrutura sempre que o tamanho ou o formato do fluxo de vídeo capturado pode ter mudado (como após a exibição do formato de vídeo do driver de captura).

Alterar as dimensões da janela de captura não tem nenhum efeito sobre as dimensões do fluxo de vídeo capturado real. A caixa de diálogo formato exibida pelo driver de dispositivo de captura de vídeo controla as dimensões do fluxo de vídeo capturado.

 

 




