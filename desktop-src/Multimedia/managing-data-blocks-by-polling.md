---
title: Gerenciando blocos de dados por sondagem
description: Gerenciando blocos de dados por sondagem
ms.assetid: 0a517f1d-4993-49b8-be86-bc63e5687cba
keywords:
- áudio de forma de onda, blocos de dados de sondagem
- blocos de dados de áudio, sondagem
- sondando blocos de dados de áudio
- Estrutura WAVEHDR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17c84e75eccaf34ef16ccadefb4dae42931854a0c6c4278003fb5c01b0c551f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118139158"
---
# <a name="managing-data-blocks-by-polling"></a>Gerenciando blocos de dados por sondagem

Além de usar uma função de retorno de chamada, você pode sondar o membro **dwFlags** de uma estrutura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) para determinar quando um dispositivo de áudio é concluído com um bloco de dados. Às vezes, é melhor sondar **dwFlags do** que aguardar outro mecanismo receber mensagens dos drivers. Por exemplo, depois de chamar a função [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset) para liberar blocos de dados pendentes, você pode sondar imediatamente para ter certeza de que os blocos de dados foram liberados antes de chamar [**waveOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader) e liberar a memória para o bloco de dados.

Você pode usar o sinalizador WHDR \_ DONE para testar o membro **dwFlags.** Assim que o sinalizador WHDR DONE for definido no membro \_ **dwFlags** da estrutura **WAVEHDR,** o driver será concluído com o bloco de dados.

 

 