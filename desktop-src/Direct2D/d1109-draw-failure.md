---
title: Falha de desenho D1109
ms.assetid: 76154839-719e-4c73-a80e-f9216f3468e3
description: Uma chamada de empate por um destino de renderização falhou
keywords:
- D1109 de falha de desenho Direct2D
topic_type:
- apiref
api_name:
- D1109 Draw Failure
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 4b08dfb99d49dcb447443685e1fbfa01a2cbad1c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641794"
---
# <a name="d1109-draw-failure"></a><span data-ttu-id="95fe7-104">D1109: falha ao desenhar</span><span class="sxs-lookup"><span data-stu-id="95fe7-104">D1109: Draw Failure</span></span>

<span data-ttu-id="95fe7-105">Uma chamada de empate por um recurso com falha de destino de renderização \[  \] .</span><span class="sxs-lookup"><span data-stu-id="95fe7-105">A Draw call by a render target failed \[*resource*\].</span></span> <span data-ttu-id="95fe7-106">Marcas \[ *da tag1*, *tag2* \] .</span><span class="sxs-lookup"><span data-stu-id="95fe7-106">Tags \[*tag1*, *tag2*\].</span></span>

## <a name="placeholders"></a><span data-ttu-id="95fe7-107">Espaços reservados</span><span class="sxs-lookup"><span data-stu-id="95fe7-107">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="95fe7-108"><span id="resource"></span><span id="RESOURCE"></span>*Kit*</span><span class="sxs-lookup"><span data-stu-id="95fe7-108"><span id="resource"></span><span id="RESOURCE"></span>*resource*</span></span>
</dt> <dd>

<span data-ttu-id="95fe7-109">O endereço do destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="95fe7-109">The address of the render target.</span></span>

</dd> <dt>

<span data-ttu-id="95fe7-110"><span id="tag1"></span><span id="TAG1"></span>*da tag1*</span><span class="sxs-lookup"><span data-stu-id="95fe7-110"><span id="tag1"></span><span id="TAG1"></span>*tag1*</span></span>
</dt> <dd>

<span data-ttu-id="95fe7-111">O primeiro valor de marca (consulte [**settags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) para obter informações).</span><span class="sxs-lookup"><span data-stu-id="95fe7-111">The first tag value (see [**SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) more for information).</span></span>

</dd> <dt>

<span data-ttu-id="95fe7-112"><span id="tag2"></span><span id="TAG2"></span>*tag2*</span><span class="sxs-lookup"><span data-stu-id="95fe7-112"><span id="tag2"></span><span id="TAG2"></span>*tag2*</span></span>
</dt> <dd>

<span data-ttu-id="95fe7-113">O segundo valor de marca (consulte [**settags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) mais para obter informações).</span><span class="sxs-lookup"><span data-stu-id="95fe7-113">The second tag value (see [**SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) more for information).</span></span>

</dd> </dl> 

|             |         |
|-------------|---------|
| <span data-ttu-id="95fe7-114">Nível de erro</span><span class="sxs-lookup"><span data-stu-id="95fe7-114">Error Level</span></span> | <span data-ttu-id="95fe7-115">Aviso</span><span class="sxs-lookup"><span data-stu-id="95fe7-115">Warning</span></span> |



 

## <a name="possible-causes"></a><span data-ttu-id="95fe7-116">Possíveis causas</span><span class="sxs-lookup"><span data-stu-id="95fe7-116">Possible Causes</span></span>

<span data-ttu-id="95fe7-117">Há muitas razões pelas quais uma chamada de empate pode falhar.</span><span class="sxs-lookup"><span data-stu-id="95fe7-117">There are many reasons that a Draw call might fail.</span></span> <span data-ttu-id="95fe7-118">Para obter mais informações, consulte a documentação do SDK do Direct2D para o método que falhou.</span><span class="sxs-lookup"><span data-stu-id="95fe7-118">For more information, see the Direct2D SDK documentation for the method that failed.</span></span>

 

 