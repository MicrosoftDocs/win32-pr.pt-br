---
title: Gerenciando blocos de dados por sondagem
description: Gerenciando blocos de dados por sondagem
ms.assetid: 0a517f1d-4993-49b8-be86-bc63e5687cba
keywords:
- áudio de onda, blocos de dados de sondagem
- blocos de dados de áudio, sondagem
- blocos de dados de áudio de sondagem
- Estrutura WAVEHDR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7e5580ff64425eae1bc6650268b065e60b90f43
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007409"
---
# <a name="managing-data-blocks-by-polling"></a>Gerenciando blocos de dados por sondagem

Além de usar uma função de retorno de chamada, você pode sondar o membro **dwFlags** de uma estrutura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) para determinar quando um dispositivo de áudio é concluído com um bloco de dados. Às vezes, é melhor sondar **dwFlags** do que esperar que outro mecanismo receba mensagens dos drivers. Por exemplo, depois de chamar a função [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset) para liberar blocos de dados pendentes, você pode sondar imediatamente para certificar-se de que os blocos de dados foram liberados antes de chamar [**waveOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader) e liberar a memória para o bloco de dados.

Você pode usar o \_ sinalizador WHDR Done para testar o membro **dwFlags** . Assim que o sinalizador WHDR \_ concluído é definido no membro **dwFlags** da estrutura **WAVEHDR** , o driver é concluído com o bloco de dados.

 

 