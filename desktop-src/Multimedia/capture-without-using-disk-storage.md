---
title: Capturar sem usar Armazenamento em Disco
description: Capturar sem usar Armazenamento em Disco
ms.assetid: 2e2f1b67-69be-424c-8a6f-d9db5eeb6088
keywords:
- WM_CAP_SEQUENCE_NOFILE mensagem
- macro capCaptureSequenceNoFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f76fa69fa8a827117dbc110a410cb40084614559
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105752628"
---
# <a name="capture-without-using-disk-storage"></a>Capturar sem usar Armazenamento em Disco

Você pode usar os serviços de captura sem gravar os dados em um arquivo de disco usando a mensagem [**\_ \_ \_ nofile da sequência do WM Cap**](wm-cap-sequence-nofile.md) (ou a macro [**capCaptureSequenceNoFile**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequencenofile) ). Essa mensagem é útil somente em conjunto com funções de retorno de chamada que permitem que seu aplicativo use os dados de vídeo e áudio diretamente. Por exemplo, aplicativos de videoconferência podem usar essa mensagem para obter quadros de vídeo de streaming. As funções de retorno de chamada transferirão as imagens capturadas para o computador remoto.

 

 




