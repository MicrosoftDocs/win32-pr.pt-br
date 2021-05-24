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
# <a name="reference-counting-direct3d-10"></a><span data-ttu-id="632fc-103">Contagem de referência (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="632fc-103">Reference Counting (Direct3D 10)</span></span>

<span data-ttu-id="632fc-104">As funções de conjunto do Direct3D 10 não têm uma referência a um objeto filho do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="632fc-104">Direct3D 10 set functions do not hold a reference to a device-child object.</span></span> <span data-ttu-id="632fc-105">Isso significa que cada aplicativo deve conter uma referência a um objeto filho do dispositivo, desde que o objeto precise ser vinculado ao pipeline.</span><span class="sxs-lookup"><span data-stu-id="632fc-105">This means that each application must hold a reference to a device-child object for as long as the object needs to be bound to the pipeline.</span></span> <span data-ttu-id="632fc-106">Quando a contagem de referência de um objeto cair para zero, o objeto será desaconsudido do pipeline e destruído.</span><span class="sxs-lookup"><span data-stu-id="632fc-106">When the reference count of an object drops to zero, the object will be unbound from the pipeline and destroyed.</span></span> <span data-ttu-id="632fc-107">Esse estilo de manter referência também é conhecido como retém de referência fraca porque cada local de associação de pipeline contém uma referência fraca à interface/objeto que está vinculado a ele.</span><span class="sxs-lookup"><span data-stu-id="632fc-107">This style of reference holding is also known as weak-reference holding because each pipeline binding location holds a weak reference to the interface/object that is bound to it.</span></span>

<span data-ttu-id="632fc-108">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="632fc-108">For example:</span></span>


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





<span data-ttu-id="632fc-109">Diferenças entre o Direct3D 9 e o Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="632fc-109">Differences between Direct3D 9 and Direct3D 10:</span></span>

- <span data-ttu-id="632fc-110">No Direct3D 9, definir funções mantém uma referência aos objetos do dispositivo; nas funções de conjunto do Direct3D 10 não têm uma referência aos objetos filho do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="632fc-110">In Direct3D 9, set functions hold a reference to the device objects; in Direct3D 10 set functions do not hold a reference to the device-child objects.</span></span>



 

## <a name="related-topics"></a><span data-ttu-id="632fc-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="632fc-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="632fc-112">Recursos da API (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="632fc-112">API Features (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-api-features.md)
</dt> </dl>

 

 




