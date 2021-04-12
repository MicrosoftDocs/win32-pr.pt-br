---
description: Há outras circunstâncias em que uma operação de leitura ou gravação pode ser concluída com menos do que o número solicitado de caracteres, mesmo que um tempo limite não tenha ocorrido.
ms.assetid: 05f84661-34ff-4e1f-9ec8-e4682138dfee
title: Erros de comunicação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eeace990620928ce898a3e8a31049a0083cdf07
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457016"
---
# <a name="communications-errors"></a>Erros de comunicação

Há outras circunstâncias em que uma operação de leitura ou gravação pode ser concluída com menos do que o número solicitado de caracteres, mesmo que um tempo limite não tenha ocorrido. A seguir estão alguns exemplos:

-   Alguns drivers dão suporte ao uso de caracteres especiais, que concluem uma operação de leitura imediatamente com apenas os caracteres que foram lidos até o ponto em que são recebidos.
-   A função [**PurgeComm**](/windows/desktop/api/Winbase/nf-winbase-purgecomm) pode ser chamada para finalizar prematuramente operações de leitura ou gravação pendentes. Essa função também pode excluir o conteúdo dos buffers de saída ou de entrada, ou ambos.
-   Se ocorrer um erro de comunicação durante uma operação de leitura ou gravação, todas as operações de e/s no recurso de comunicações serão encerradas. Condições de interrupção, erros de paridade ou erros de enquadramento são exemplos desses erros. Quando ocorre um erro, o processo deve chamar a função [**ClearCommError**](/windows/desktop/api/Winbase/nf-winbase-clearcommerror) para limpar o sinalizador de erro antes que ele possa iniciar operações de e/s adicionais. **ClearCommError** relata o erro específico que ocorreu e o status atual do dispositivo.

 

 



