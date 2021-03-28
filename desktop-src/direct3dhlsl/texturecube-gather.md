---
title: 'Métodos de coleta de TextureCube:: TextureCube'
description: 'Retorna os quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear. | Métodos de coleta de TextureCube:: TextureCube'
ms.assetid: 4891A62A-9D54-4F7E-92C2-9CDDF1453671
keywords:
- Coletar métodos HLSL
topic_type:
- apiref
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
api_location: ''
ms.openlocfilehash: ce58acc01ef87e6d53d829a5c84e7c9c0ff6afb9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968375"
---
# <a name="texturecubegather-methods"></a><span data-ttu-id="dd19f-105">Métodos TextureCube:: Reúna</span><span class="sxs-lookup"><span data-stu-id="dd19f-105">TextureCube::Gather methods</span></span>

<span data-ttu-id="dd19f-106">Retorna os quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear.</span><span class="sxs-lookup"><span data-stu-id="dd19f-106">Returns the four texel values that would be used in a bi-linear filtering operation.</span></span>

<span data-ttu-id="dd19f-107">Consulte a documentação em [gather4](./gather4--sm5---asm-.md) para obter mais informações descrevendo a instrução DXBC subjacente.</span><span class="sxs-lookup"><span data-stu-id="dd19f-107">See the documentation on [gather4](./gather4--sm5---asm-.md) for more information describing the underlying DXBC instruction.</span></span>

### <a name="overload-list"></a><span data-ttu-id="dd19f-108">Lista de sobrecargas</span><span class="sxs-lookup"><span data-stu-id="dd19f-108">Overload list</span></span>



| <span data-ttu-id="dd19f-109">Método</span><span class="sxs-lookup"><span data-stu-id="dd19f-109">Method</span></span>                                                     | <span data-ttu-id="dd19f-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="dd19f-110">Description</span></span>                                                                                                              |
|:-----------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dd19f-111">**Coleta (S, float)**</span><span class="sxs-lookup"><span data-stu-id="dd19f-111">**Gather(S,float)**</span></span>](dx-graphics-hlsl-to-gather.md)      | <span data-ttu-id="dd19f-112">Faz a amostragem de uma textura e retorna as quatro amostras (apenas o componente vermelho) que são usadas para interpolação bilinear.</span><span class="sxs-lookup"><span data-stu-id="dd19f-112">Samples a texture and returns the four samples (red component only) that are used for bilinear interpolation.</span></span><br/> |
| [<span data-ttu-id="dd19f-113">**Coletar (S, float, uint)**</span><span class="sxs-lookup"><span data-stu-id="dd19f-113">**Gather(S,float,uint)**</span></span>](tcube-gather-s-float-uint-.md) | <span data-ttu-id="dd19f-114">Obtém uma textura e retorna todos os quatro componentes junto com o status sobre a operação.</span><span class="sxs-lookup"><span data-stu-id="dd19f-114">Samples a texture and returns all four components along with status about the operation.</span></span><br/>                      |



## <a name="see-also"></a><span data-ttu-id="dd19f-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="dd19f-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd19f-116">**TextureCube**</span><span class="sxs-lookup"><span data-stu-id="dd19f-116">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

