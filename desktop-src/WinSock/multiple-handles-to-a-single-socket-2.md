---
description: Como o que são duplicados são os descritores de soquete e não os soquetes subjacentes, todos os estados associados a um soquete são mantidos em comum em todos os descritores.
ms.assetid: f3a2cd5a-bc3a-4aeb-8606-7b8aa6afb105
title: Vários alças para um único soquete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05e402d19c3306158a905f2e9ddc263649e52d214a3d9441509e7a277f7d2800
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121396"
---
# <a name="multiple-handles-to-a-single-socket"></a>Vários alças para um único soquete

Como o que são duplicados são os descritores de soquete e não os soquetes subjacentes, todos os estados associados a um soquete são mantidos em comum em todos os descritores. Por exemplo, uma [**operação WSPSetSockOpt**](/previous-versions/windows/hardware/network/ff566318(v=vs.85)) executada usando um descritor é subsequentemente visível usando um [**WSPGetSockOpt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85)) de qualquer ou todos os descritores.

A notificação em soquetes compartilhados está sujeita às restrições usuais de [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) e [**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85)). A emissão de qualquer uma dessas chamadas usando qualquer um dos descritores compartilhados cancela qualquer registro de evento anterior para o soquete, independentemente de qual descritor foi usado para fazer esse registro. Portanto, por exemplo, não seria possível processar um evento de leitura FD de recebimento e processar \_ B receber eventos FD \_ WRITE. Para situações em que essa coordenação rígida é necessária, é sugerido que os desenvolvedores considerem o uso de threads em vez de processos separados.

 

 
