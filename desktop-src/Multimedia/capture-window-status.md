---
title: Status da Janela de Captura
description: Status da Janela de Captura
ms.assetid: c3f80cac-30b2-42f0-8a9c-4053728c558b
keywords:
- WM_CAP_GET_STATUS mensagem
- macro capGetStatus
- Estrutura CAPSTATUS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 367d35c3869adb6f4e960fa472e0cd6a22483c37fa981e886b3a78f0b7410029
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118375282"
---
# <a name="capture-window-status"></a>Status da Janela de Captura

Você pode recuperar o status atual de uma janela de captura usando a mensagem [**WM \_ CAP GET \_ \_ STATUS**](wm-cap-get-status.md) (ou a [**macro capGetStatus).**](/windows/desktop/api/Vfw/nf-vfw-capgetstatus) Essa mensagem recupera uma cópia da estrutura [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) com os valores atuais de seus membros. A **estrutura CAPSTATUS** contém informações sobre as dimensões da imagem, posição de rolagem e se a sobreposição ou visualização da imagem está habilitada. Como as informações representadas em **CAPSTATUS** são dinâmicas, seu aplicativo deve atualizar o conteúdo da estrutura sempre que o tamanho ou o formato do fluxo de vídeo capturado pode ter sido alterado (como depois de exibir o formato de vídeo do driver de captura).

Alterar as dimensões da janela de captura não tem efeito sobre as dimensões do fluxo de vídeo capturado real. A caixa de diálogo formato exibida pelo driver de dispositivo de captura de vídeo controla as dimensões do fluxo de vídeo capturado.

 

 




