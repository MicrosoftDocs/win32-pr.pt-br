---
title: Registro de cores
description: Esses registros de saída do sombreador de vértice contêm um valor de cor.
ms.assetid: fd36e207-7312-4c7e-b664-b2de9ba1ebcf
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 38ee29ebafd9e7374fa868c6d84ad45f6c07dedf
ms.sourcegitcommit: 3f366316c02c411c4c5e14620a699f6f30608634
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/04/2021
ms.locfileid: "104297823"
---
# <a name="color-register"></a><span data-ttu-id="0343f-103">Registro de cores</span><span class="sxs-lookup"><span data-stu-id="0343f-103">Color Register</span></span>

<span data-ttu-id="0343f-104">Esses registros de saída do sombreador de vértice contêm um valor de cor.</span><span class="sxs-lookup"><span data-stu-id="0343f-104">These vertex shader output registers contain a color value.</span></span> 

| <span data-ttu-id="0343f-105">Registre-se</span><span class="sxs-lookup"><span data-stu-id="0343f-105">Register</span></span> | <span data-ttu-id="0343f-106">Description</span><span class="sxs-lookup"><span data-stu-id="0343f-106">Description</span></span>              |
|----------|--------------------------|
| <span data-ttu-id="0343f-107">oD0</span><span class="sxs-lookup"><span data-stu-id="0343f-107">oD0</span></span>      | <span data-ttu-id="0343f-108">registro de cores difusas.</span><span class="sxs-lookup"><span data-stu-id="0343f-108">diffuse color register.</span></span>  |
| <span data-ttu-id="0343f-109">oD1</span><span class="sxs-lookup"><span data-stu-id="0343f-109">oD1</span></span>      | <span data-ttu-id="0343f-110">registro de cor especular.</span><span class="sxs-lookup"><span data-stu-id="0343f-110">specular color register.</span></span> |



 

<span data-ttu-id="0343f-111">O valor de oD0 é interpolado e gravado no registro de cor do sombreador de pixel 0 (V0).</span><span class="sxs-lookup"><span data-stu-id="0343f-111">The oD0 value is interpolated and is written to the pixel shader color register 0 (v0).</span></span> <span data-ttu-id="0343f-112">O valor de oD1 é interpolado e gravado no registro de cor do sombreador de pixel 1 (v1).</span><span class="sxs-lookup"><span data-stu-id="0343f-112">The oD1 value is interpolated and written to the pixel shader color register 1 (v1).</span></span> <span data-ttu-id="0343f-113">Para obter mais informações sobre registros de cores do sombreador de pixel, consulte o tópico [registro de cores de entrada](dx9-graphics-reference-asm-ps-registers-input-color.md) do sombreador de pixels.</span><span class="sxs-lookup"><span data-stu-id="0343f-113">For more information about pixel shader color registers, see the pixel shader [Input Color Register](dx9-graphics-reference-asm-ps-registers-input-color.md) topic.</span></span>

## <a name="remarks"></a><span data-ttu-id="0343f-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="0343f-114">Remarks</span></span>

<span data-ttu-id="0343f-115">Exemplo</span><span class="sxs-lookup"><span data-stu-id="0343f-115">Example</span></span>


```
min oD0, r0, c1.x    
```



## <a name="related-topics"></a><span data-ttu-id="0343f-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0343f-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0343f-117">Registros de sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="0343f-117">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




