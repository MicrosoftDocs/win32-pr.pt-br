---
description: Para melhorar o desempenho de renderização, você pode excluir (ou remover) um primitivo que se rostos da câmera.
ms.assetid: b4b8ff3f-aa20-4422-8f6f-34cae25de0e6
title: Estado de remoção (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4bf9d8ed8ecea46dcfee146784dc97a38e42f0261b8f78bfc9d45ffaf99ddd6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119608026"
---
# <a name="culling-state-direct3d-9"></a>Estado de remoção (Direct3D 9)

Para melhorar o desempenho de renderização, você pode excluir (ou remover) um primitivo que se rostos da câmera. Para primitivos de um único lado, isso economiza tempo de renderização porque um back-face não está visível. Para habilitar a remoção, você precisa saber a ordem de contorno dos vértices (normalmente no sentido anti-horário). Este exemplo removerá qualquer primitiva cuja face de fundo esteja voltada para frente (dada uma ordem de enrolamento no sentido anti-horário):


```
SetRenderState(D3DRS_CULLMODE, D3DCULL_CCW);
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Processar Estados](render-states.md)
</dt> </dl>

 

 



