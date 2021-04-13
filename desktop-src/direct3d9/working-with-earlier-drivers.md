---
description: Esta seção lista os problemas que podem ser encontrados ao trabalhar com o Direct3D 9 em drivers escritos para versões do Direct3D anteriores ao Direct3D 9.
ms.assetid: 891198e8-6c45-4f03-99bb-e24a4082b0d8
title: Trabalhando com drivers anteriores (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76567bc4778924835e20a476b03dc94ea77739fd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104370097"
---
# <a name="working-with-earlier-drivers-direct3d-9"></a><span data-ttu-id="cb761-103">Trabalhando com drivers anteriores (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="cb761-103">Working with Earlier Drivers (Direct3D 9)</span></span>

<span data-ttu-id="cb761-104">Esta seção lista os problemas que podem ser encontrados ao trabalhar com o Direct3D 9 em drivers escritos para versões do Direct3D anteriores ao Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="cb761-104">This section lists issues that can be encountered when working with Direct3D 9 on drivers written for versions of Direct3D earlier than Direct3D 9.</span></span>

-   <span data-ttu-id="cb761-105">Ao trabalhar com um dispositivo de HAL T&L, a intensidade de neblina é calculada, mas a operação de valor absoluto não é aplicada a esse valor.</span><span class="sxs-lookup"><span data-stu-id="cb761-105">When working with a T&L HAL device, the fog intensity is computed but the absolute value operation is not applied to this value.</span></span> <span data-ttu-id="cb761-106">Em vez disso, o valor será deixado negativo se for o que é calculado.</span><span class="sxs-lookup"><span data-stu-id="cb761-106">Rather, the value is left negative if that is what is computed.</span></span> <span data-ttu-id="cb761-107">A melhor maneira de evitar essa situação é configurar as transformações adequadamente.</span><span class="sxs-lookup"><span data-stu-id="cb761-107">The best way to avoid this situation is to set up transforms appropriately.</span></span> <span data-ttu-id="cb761-108">Um método menos preferencial é tornar os valores de sombra-início e de neblina negativos para correspondência.</span><span class="sxs-lookup"><span data-stu-id="cb761-108">A less-preferred method is to make the fog-start and fog-end values negative to match.</span></span>

<span data-ttu-id="cb761-109">Para verificar um driver do Direct3D 9, procure um valor diferente de zero para D3DDEVCAPS2 \_ STREAMOFFSET no membro DevCaps2 de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="cb761-109">To check for a Direct3D 9 driver, look for a nonzero value for D3DDEVCAPS2\_STREAMOFFSET in the DevCaps2 member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="related-topics"></a><span data-ttu-id="cb761-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="cb761-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cb761-111">Dicas de programação</span><span class="sxs-lookup"><span data-stu-id="cb761-111">Programming Tips</span></span>](programming-tips.md)
</dt> </dl>

 

 



