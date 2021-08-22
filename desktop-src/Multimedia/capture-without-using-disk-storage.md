---
title: Capturar sem usar o disco Armazenamento
description: Capturar sem usar o disco Armazenamento
ms.assetid: 2e2f1b67-69be-424c-8a6f-d9db5eeb6088
keywords:
- WM_CAP_SEQUENCE_NOFILE mensagem
- macro capCaptureSequenceNoFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ea708bd99cc2c325623eb53d734fadb2acdd0112e3a727fae9bfa741b8d301e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691616"
---
# <a name="capture-without-using-disk-storage"></a>Capturar sem usar o disco Armazenamento

Você pode usar serviços de captura sem escrever os dados em um arquivo de disco usando a mensagem [**WM \_ CAP SEQUENCE \_ \_ NOFILE**](wm-cap-sequence-nofile.md) (ou a [**macro capCaptureSequenceNoFile).**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequencenofile) Essa mensagem é útil apenas em conjunto com funções de retorno de chamada que permitem que seu aplicativo use os dados de áudio e vídeo diretamente. Por exemplo, aplicativos de videoconferência podem usar essa mensagem para obter quadros de vídeo de streaming. As funções de retorno de chamada transfeririam as imagens capturadas para o computador remoto.

 

 




