---
title: Afinidade de processador no WOW64
description: o Windows de 32 bits dá suporte a um máximo de 32 processadores. Portanto, as funções como GetProcessAffinityMask simulam um computador com processadores 32 quando chamados sob WOW64.
ms.assetid: f50a03e8-1c23-4eb0-a1ff-471c28d6b611
keywords:
- afinidade do processador – programação de 64 bits do Windows
- Programação WOW64 de 64 bits do Windows, afinidade do processador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c60ad6cf5055737dc39abd735211c5b4ec4ab9d7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641377"
---
# <a name="processor-affinity-under-wow64"></a>Afinidade de processador no WOW64

o Windows de 32 bits dá suporte a um máximo de 32 processadores. Portanto, as funções como [**GetProcessAffinityMask**](/windows/desktop/api/winbase/nf-winbase-getprocessaffinitymask) simulam um computador com processadores 32 quando chamados sob WOW64.

A máscara de afinidade é obtida com a execução de uma operação or bits ou de bit superior da máscara dos principais 32 de bits com o bit 32 inferior. Portanto, se um thread tiver afinidade para os processadores 0, 1 e 32, o WOW64 relatará a afinidade como 0 e 1, porque o processador 32 é mapeado para o processador 0. As funções que definem a afinidade do processador, como [**SetThreadAffinityMask**](/windows/desktop/api/winbase/nf-winbase-setthreadaffinitymask), restringem os processadores aos primeiros 32 processadores em WOW64.

Para obter mais informações sobre a afinidade do processador, consulte [vários processadores](/windows/desktop/ProcThread/multiple-processors).

 

 