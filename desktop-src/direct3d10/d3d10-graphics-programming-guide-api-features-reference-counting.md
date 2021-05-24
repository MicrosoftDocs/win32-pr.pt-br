---
description: As funções de conjunto do Direct3D 10 não têm uma referência a um objeto filho do dispositivo.
ms.assetid: 4f4e1af8-5830-4b2d-ba2e-dc2ec4e74a19
title: Contagem de referência (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b3587466aa3ecaea5f3a77332c77654b0725bb1
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335450"
---
# <a name="reference-counting-direct3d-10"></a>Contagem de referência (Direct3D 10)

As funções de conjunto do Direct3D 10 não têm uma referência a um objeto filho do dispositivo. Isso significa que cada aplicativo deve conter uma referência a um objeto filho do dispositivo, desde que o objeto precise ser vinculado ao pipeline. Quando a contagem de referência de um objeto cair para zero, o objeto será desaconsudido do pipeline e destruído. Esse estilo de manter referência também é conhecido como retém de referência fraca porque cada local de associação de pipeline contém uma referência fraca à interface/objeto que está vinculado a ele.

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





Diferenças entre o Direct3D 9 e o Direct3D 10:

- No Direct3D 9, definir funções mantém uma referência aos objetos do dispositivo; nas funções de conjunto do Direct3D 10 não têm uma referência aos objetos filho do dispositivo.



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Recursos da API (Direct3D 10)](d3d10-graphics-programming-guide-api-features.md)
</dt> </dl>

 

 




