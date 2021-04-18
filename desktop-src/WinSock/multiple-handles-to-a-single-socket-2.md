---
description: Como as duplicatas são os descritores de soquete e não os soquetes subjacentes, todos os Estados associados a um soquete são mantidos em comum em todos os descritores.
ms.assetid: f3a2cd5a-bc3a-4aeb-8606-7b8aa6afb105
title: Vários identificadores para um único soquete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2356f24a69d132f87e0f6543f61509ff12acba5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105807161"
---
# <a name="multiple-handles-to-a-single-socket"></a>Vários identificadores para um único soquete

Como as duplicatas são os descritores de soquete e não os soquetes subjacentes, todos os Estados associados a um soquete são mantidos em comum em todos os descritores. Por exemplo, uma operação [**WSPSetSockOpt**](/previous-versions/windows/hardware/network/ff566318(v=vs.85)) executada usando um descritor é posteriormente visível usando um [**WSPGetSockOpt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85)) de qualquer um ou de todos os descritores.

A notificação em soquetes compartilhados está sujeita às restrições usuais de [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) e [**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85)). A emissão de qualquer uma dessas chamadas usando qualquer um dos descritores compartilhados cancela qualquer registro de evento anterior para o soquete, independentemente do qual foi usado para fazer esse registro. Portanto, por exemplo, não seria possível ter o processo A receber \_ eventos de leitura FD e o processo B receber eventos de gravação FD \_ . Para situações em que tal coordenação rígida é necessária, é recomendável que os desenvolvedores considerem o uso de threads em vez de processos separados.

 

 
