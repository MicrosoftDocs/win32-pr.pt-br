---
description: As funções de conjunto do Direct3D 10 não mantêm uma referência a um objeto Device-Child.
ms.assetid: 4f4e1af8-5830-4b2d-ba2e-dc2ec4e74a19
title: Contagem de referência (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6482918601f163bdea92291eb3927899ca797d29
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500844"
---
# <a name="reference-counting-direct3d-10"></a>Contagem de referência (Direct3D 10)

As funções de conjunto do Direct3D 10 não mantêm uma referência a um objeto Device-Child. Isso significa que cada aplicativo deve manter uma referência a um objeto de dispositivo-filho enquanto o objeto precisar ser associado ao pipeline. Quando a contagem de referência de um objeto cair para zero, o objeto será desassociado do pipeline e destruído. Esse estilo de chamada de referência também é conhecido como um bloqueio de referência fraca porque cada local de associação de pipeline contém uma referência fraca à interface/objeto que está associada a ele.

Por exemplo:


```
pDevice->CreateRasterizerState( ..., &pRasterizerState );
pDevice->RSSetState( pRasterizerState );
 
pDevice->RSGetState( &pCurRasterizerState );
// pCurRasterizerState will be equal to pRasterizerState.
pCurRasterizerState->Release();
 
pRasterizerState->Release();
// Following the final release, the object is unbound.
pDevice->RSGetState( &pCurRasterizerState );
// pCurRasterizerState will be equal to NULL.
```





|                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Diferenças entre o Direct3D 9 e o Direct3D 10:<br/> No Direct3D 9, as funções Set contêm uma referência aos objetos do dispositivo; nas funções do conjunto do Direct3D 10, não mantenha uma referência aos objetos do dispositivo filho.<br/> |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Recursos de API (Direct3D 10)](d3d10-graphics-programming-guide-api-features.md)
</dt> </dl>

 

 




