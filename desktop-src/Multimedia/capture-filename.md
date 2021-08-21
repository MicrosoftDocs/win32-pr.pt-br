---
title: Nome do arquivo de captura
description: Nome do arquivo de captura
ms.assetid: b17ecdd4-899e-4e94-98f2-496f93491e06
keywords:
- WM_CAP_FILE_SET_CAPTURE_FILE mensagem
- macro capFileSetCaptureFile
- WM_CAP_FILE_GET_CAPTURE_FILE mensagem
- macro capFileGetCaptureFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47e48ecd727accccb868d0f78c68a833ac6ec6655bada23db8a56f2a9aeaffd1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118941591"
---
# <a name="capture-filename"></a>Nome do arquivo de captura

O AVICap, por padrão, roteia dados de fluxo de vídeo e áudio de uma janela de captura para um arquivo chamado CAPTURE.AVI no diretório raiz da unidade atual. Você pode especificar um nome de arquivo alternativo enviando a mensagem do [**arquivo de captura do conjunto de arquivos do WM \_ Cap \_ \_ \_ \_**](wm-cap-file-set-capture-file.md) (ou a macro [**capFileSetCaptureFile**](/windows/desktop/api/Vfw/nf-vfw-capfilesetcapturefile) ) para uma janela de captura. Essa mensagem Especifica o nome do arquivo; Ele não cria, aloca ou abre o arquivo. Você pode recuperar o nome de arquivo de captura atual enviando a mensagem do [**\_ \_ \_ \_ \_ arquivo de captura do arquivo do WM Cap**](wm-cap-file-get-capture-file.md) (ou a macro [**capFileGetCaptureFile**](/windows/desktop/api/Vfw/nf-vfw-capfilegetcapturefile) ) para uma janela de captura.

 

 




