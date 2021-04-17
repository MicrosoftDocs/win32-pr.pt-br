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
ms.openlocfilehash: 4856649906e09f212d2f8992c9d4fb9b8f4c37d4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105782314"
---
# <a name="capture-filename"></a>Nome do arquivo de captura

O AVICap, por padrão, roteia dados de fluxo de vídeo e áudio de uma janela de captura para um arquivo chamado CAPTURE.AVI no diretório raiz da unidade atual. Você pode especificar um nome de arquivo alternativo enviando a mensagem do [**arquivo de captura do conjunto de arquivos do WM \_ Cap \_ \_ \_ \_**](wm-cap-file-set-capture-file.md) (ou a macro [**capFileSetCaptureFile**](/windows/desktop/api/Vfw/nf-vfw-capfilesetcapturefile) ) para uma janela de captura. Essa mensagem Especifica o nome do arquivo; Ele não cria, aloca ou abre o arquivo. Você pode recuperar o nome de arquivo de captura atual enviando a mensagem do [**\_ \_ \_ \_ \_ arquivo de captura do arquivo do WM Cap**](wm-cap-file-get-capture-file.md) (ou a macro [**capFileGetCaptureFile**](/windows/desktop/api/Vfw/nf-vfw-capfilegetcapturefile) ) para uma janela de captura.

 

 




