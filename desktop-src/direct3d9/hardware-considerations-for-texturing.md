---
description: O hardware atual não implementa necessariamente toda a funcionalidade habilitada pela interface Direct3D. Seu aplicativo deve testar o hardware do usuário e ajustar suas estratégias de renderização de acordo.
ms.assetid: 7b5f586c-616c-4351-b6b9-5c0179db5d8b
title: Considerações de hardware para texturing (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21f1ba8bea85cc3657478767aac7c7ffc2abebbd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825456"
---
# <a name="hardware-considerations-for-texturing-direct3d-9"></a><span data-ttu-id="01693-104">Considerações de hardware para texturing (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="01693-104">Hardware Considerations for Texturing (Direct3D 9)</span></span>

<span data-ttu-id="01693-105">O hardware atual não implementa necessariamente toda a funcionalidade habilitada pela interface Direct3D.</span><span class="sxs-lookup"><span data-stu-id="01693-105">Current hardware does not necessarily implement all the functionality that the Direct3D interface enables.</span></span> <span data-ttu-id="01693-106">Seu aplicativo deve testar o hardware do usuário e ajustar suas estratégias de renderização de acordo.</span><span class="sxs-lookup"><span data-stu-id="01693-106">Your application must test user hardware and adjust its rendering strategies accordingly.</span></span>

<span data-ttu-id="01693-107">Muitas placas aceleradoras 3D não dão suporte a valores iterados difuso como argumentos para unidades de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="01693-107">Many 3D accelerator cards do not support diffuse iterated values as arguments to blending units.</span></span> <span data-ttu-id="01693-108">No entanto, seu aplicativo pode introduzir dados de cores iterados quando executa a mesclagem de textura.</span><span class="sxs-lookup"><span data-stu-id="01693-108">However, your application can introduce iterated color data when it performs texture blending.</span></span>

<span data-ttu-id="01693-109">Alguns hardwares 3D podem não ter um estágio de mesclagem associado à primeira textura.</span><span class="sxs-lookup"><span data-stu-id="01693-109">Some 3D hardware may not have a blending stage associated with the first texture.</span></span> <span data-ttu-id="01693-110">Nesses adaptadores, seu aplicativo deve executar a mesclagem no segundo e terceiro estágios de textura no conjunto de texturas atuais.</span><span class="sxs-lookup"><span data-stu-id="01693-110">On these adapters, your application must perform blending in the second and third texture stages in the set of current textures.</span></span>

<span data-ttu-id="01693-111">Devido a limitações em grande parte do hardware de hoje, poucos adaptadores de vídeo podem executar a interpolação mipmap triline por meio da interface de mesclagem de várias texturas oferecida pelo [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span><span class="sxs-lookup"><span data-stu-id="01693-111">Because of limitations in much of today's hardware, few display adapters can perform trilinear mipmap interpolation through the multiple texture blending interface offered by [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span></span> <span data-ttu-id="01693-112">Seu aplicativo pode usar a mesclagem de textura de passagem para obter os mesmos efeitos ou degradar o \_ modo de filtro mipmap de ponto D3DTEXF, que é amplamente suportado.</span><span class="sxs-lookup"><span data-stu-id="01693-112">Your application can use multipass texture blending to achieve the same effects, or degrade to the D3DTEXF\_POINT mipmap filter mode, which is widely supported.</span></span>

## <a name="related-topics"></a><span data-ttu-id="01693-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="01693-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01693-114">Texturas do Direct3D</span><span class="sxs-lookup"><span data-stu-id="01693-114">Direct3D Textures</span></span>](direct3d-textures.md)
</dt> </dl>

 

 
