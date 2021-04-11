---
description: 'Depois de criar um buffer de profundidade, conforme descrito em criando um buffer de profundidade (Direct3D 9), habilite o buffer de profundidade chamando o método IDirect3DDevice9:: setrenderingstate.'
ms.assetid: a3c972dd-3630-4d21-a22b-64a68e9acd19
title: Habilitando o buffer de profundidade (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 935d4f2e1db164a3aac2a39627be88d71887cc14
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104295934"
---
# <a name="enabling-depth-buffering-direct3d-9"></a><span data-ttu-id="9d075-103">Habilitando o buffer de profundidade (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="9d075-103">Enabling Depth Buffering (Direct3D 9)</span></span>

<span data-ttu-id="9d075-104">Depois de criar um buffer de profundidade, conforme descrito em [criando um buffer de profundidade (Direct3D 9)](creating-a-depth-buffer.md), habilite o buffer de profundidade chamando o método [**IDirect3DDevice9:: setrenderingstate**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="9d075-104">After you create a depth buffer, as described in [Creating a Depth Buffer (Direct3D 9)](creating-a-depth-buffer.md), you enable depth buffering by calling the [**IDirect3DDevice9::SetRenderState**](/windows/desktop/api) method.</span></span> <span data-ttu-id="9d075-105">Defina o \_ estado de RENDERIZAÇÃO D3DRS ZENABLE para habilitar o buffer de profundidade.</span><span class="sxs-lookup"><span data-stu-id="9d075-105">Set the D3DRS\_ZENABLE render state to enable depth-buffering.</span></span> <span data-ttu-id="9d075-106">Use o \_ membro true do D3DZB do tipo enumerado [**D3DZBUFFERTYPE**](./d3dzbuffertype.md) (ou **true**) para habilitar o z-buffer, D3DZB \_ USEW para habilitar o w-buffer ou D3DZB \_ false (ou **false**) para desabilitar o buffer de profundidade.</span><span class="sxs-lookup"><span data-stu-id="9d075-106">Use the D3DZB\_TRUE member of the [**D3DZBUFFERTYPE**](./d3dzbuffertype.md) enumerated type (or **TRUE**) to enable z-buffering, D3DZB\_USEW to enable w-buffering, or D3DZB\_FALSE (or **FALSE**) to disable depth buffering.</span></span>

> [!Note]  
> <span data-ttu-id="9d075-107">Para usar o w-Buffering, seu aplicativo deve definir uma matriz de projeção compatível mesmo que ela não use o pipeline de transformação do Direct3D.</span><span class="sxs-lookup"><span data-stu-id="9d075-107">To use w-buffering, your application must set a compliant projection matrix even if it doesn't use the Direct3D transformation pipeline.</span></span> <span data-ttu-id="9d075-108">Para obter informações sobre como fornecer uma matriz de projeção apropriada, consulte [uma matriz de projeção amigável W](projection-transform.md)</span><span class="sxs-lookup"><span data-stu-id="9d075-108">For information about providing an appropriate projection matrix, see [A W-Friendly Projection Matrix](projection-transform.md)</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="9d075-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9d075-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9d075-110">Buffers de profundidade</span><span class="sxs-lookup"><span data-stu-id="9d075-110">Depth Buffers</span></span>](depth-buffers.md)
</dt> </dl>

 

 
