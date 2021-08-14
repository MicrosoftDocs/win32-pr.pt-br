---
description: Pseudobloqueamento de operações de pseudobloqueamento Windows soquetes (Winsock).
ms.assetid: fa8f29f1-bb4f-4814-ab8a-52d3c83232bb
title: Pseudo bloqueio e bloqueio verdadeiro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 371935a2f8984ebd080da48492807b3f5ffa9286b991b16b516244ccf26ee093
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117740938"
---
# <a name="pseudo-blocking-and-true-blocking"></a>Pseudo bloqueio e bloqueio verdadeiro

Em 16 Windows ambientes, o bloqueio verdadeiro não é suportado pelo sistema operacional; portanto, uma operação de bloqueio que não pode ser concluída imediatamente é tratada da seguinte forma:

-   O provedor de serviços inicia a operação e, em seguida, insinua um loop durante o qual ele envia Windows mensagens ( yielding the processor to another thread, se necessário)
-   Em seguida, ele verifica a conclusão da função Windows Sockets.
-   Se a função tiver sido concluída ou se [**WSPCancelBlockingCall**](/previous-versions/windows/desktop/legacy/ms742269(v=vs.85)) tiver sido invocado, o loop será encerrado e a função de bloqueio será concluída com um resultado apropriado.

Isso é o que se refere ao termo pseudo bloqueio e o loop mencionado acima é conhecido como o gancho de bloqueio padrão.

 

 
