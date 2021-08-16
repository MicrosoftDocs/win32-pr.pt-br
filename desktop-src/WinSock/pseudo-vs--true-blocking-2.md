---
description: operações de bloqueio de Pseudoblocking em Windows sockets (Winsock).
ms.assetid: fa8f29f1-bb4f-4814-ab8a-52d3c83232bb
title: Pseudo-bloqueio e verdadeiro bloqueio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 371935a2f8984ebd080da48492807b3f5ffa9286b991b16b516244ccf26ee093
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117740938"
---
# <a name="pseudo-blocking-and-true-blocking"></a>Pseudo-bloqueio e verdadeiro bloqueio

em 16 ambientes de Windows, o sistema operacional não dá suporte ao bloqueio verdadeiro; Portanto, uma operação de bloqueio que não pode ser concluída imediatamente é manipulada da seguinte maneira:

-   o provedor de serviços inicia a operação e, em seguida, insere um loop durante o qual ele despacha qualquer mensagem de Windows (produzindo o processador para outro thread, se necessário)
-   em seguida, ele verifica a conclusão da função Windows sockets.
-   Se a função tiver sido concluída, ou se [**WSPCancelBlockingCall**](/previous-versions/windows/desktop/legacy/ms742269(v=vs.85)) tiver sido invocado, o loop será encerrado e a função de bloqueio é concluída com um resultado apropriado.

Isso é o que se destina ao pseudodispositivo do termo, e o loop mencionado acima é conhecido como o gancho de bloqueio padrão.

 

 
