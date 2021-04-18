---
description: Operações de bloqueio de Pseudoblocking no Windows Sockets (Winsock).
ms.assetid: fa8f29f1-bb4f-4814-ab8a-52d3c83232bb
title: Pseudo-bloqueio e verdadeiro bloqueio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 082992aba884aebec30d35bc65d2cb6c49e29051
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105807202"
---
# <a name="pseudo-blocking-and-true-blocking"></a>Pseudo-bloqueio e verdadeiro bloqueio

Em 16 ambientes do Windows, o sistema operacional não dá suporte ao bloqueio verdadeiro. Portanto, uma operação de bloqueio que não pode ser concluída imediatamente é manipulada da seguinte maneira:

-   O provedor de serviços inicia a operação e, em seguida, insere um loop durante o qual ele despacha qualquer mensagem do Windows (produzindo o processador para outro thread, se necessário)
-   Em seguida, ele verifica a conclusão da função do Windows Sockets.
-   Se a função tiver sido concluída, ou se [**WSPCancelBlockingCall**](/previous-versions/windows/desktop/legacy/ms742269(v=vs.85)) tiver sido invocado, o loop será encerrado e a função de bloqueio é concluída com um resultado apropriado.

Isso é o que se destina ao pseudodispositivo do termo, e o loop mencionado acima é conhecido como o gancho de bloqueio padrão.

 

 
