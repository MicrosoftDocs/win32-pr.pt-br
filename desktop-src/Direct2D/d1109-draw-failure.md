---
title: Falha de desenho D1109
ms.assetid: 76154839-719e-4c73-a80e-f9216f3468e3
description: Falha em uma chamada draw por um destino de renderização
keywords:
- D1109 Falha de desenho Direct2D
topic_type:
- apiref
api_name:
- D1109 Draw Failure
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 09d84f549b2361d2753ac40650ce057de9e4f84c
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549961"
---
# <a name="d1109-draw-failure"></a><span data-ttu-id="19d8e-104">D1109: Falha de desenho</span><span class="sxs-lookup"><span data-stu-id="19d8e-104">D1109: Draw Failure</span></span>

<span data-ttu-id="19d8e-105">Uma chamada draw por um recurso de destino de \[ *renderização com falha.* \]</span><span class="sxs-lookup"><span data-stu-id="19d8e-105">A Draw call by a render target failed \[*resource*\].</span></span> <span data-ttu-id="19d8e-106">Marcas \[ *tag1*, *tag2* \] .</span><span class="sxs-lookup"><span data-stu-id="19d8e-106">Tags \[*tag1*, *tag2*\].</span></span>

## <a name="placeholders"></a><span data-ttu-id="19d8e-107">Espaços reservados</span><span class="sxs-lookup"><span data-stu-id="19d8e-107">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="19d8e-108"><span id="resource"></span><span id="RESOURCE"></span>*Recurso*</span><span class="sxs-lookup"><span data-stu-id="19d8e-108"><span id="resource"></span><span id="RESOURCE"></span>*resource*</span></span>
</dt> <dd>

<span data-ttu-id="19d8e-109">O endereço do destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="19d8e-109">The address of the render target.</span></span>

</dd> <dt>

<span data-ttu-id="19d8e-110"><span id="tag1"></span><span id="TAG1"></span>*tag1*</span><span class="sxs-lookup"><span data-stu-id="19d8e-110"><span id="tag1"></span><span id="TAG1"></span>*tag1*</span></span>
</dt> <dd>

<span data-ttu-id="19d8e-111">O primeiro valor da marca (consulte [**SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) mais para obter informações).</span><span class="sxs-lookup"><span data-stu-id="19d8e-111">The first tag value (see [**SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) more for information).</span></span>

</dd> <dt>

<span data-ttu-id="19d8e-112"><span id="tag2"></span><span id="TAG2"></span>*tag2*</span><span class="sxs-lookup"><span data-stu-id="19d8e-112"><span id="tag2"></span><span id="TAG2"></span>*tag2*</span></span>
</dt> <dd>

<span data-ttu-id="19d8e-113">O segundo valor da marca (consulte [**SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) mais para obter informações).</span><span class="sxs-lookup"><span data-stu-id="19d8e-113">The second tag value (see [**SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) more for information).</span></span>

</dd> </dl> 

| &nbsp;      |  &nbsp; |
|-------------|---------|
| <span data-ttu-id="19d8e-114">Nível de erro</span><span class="sxs-lookup"><span data-stu-id="19d8e-114">Error Level</span></span> | <span data-ttu-id="19d8e-115">Aviso</span><span class="sxs-lookup"><span data-stu-id="19d8e-115">Warning</span></span> |



 

## <a name="possible-causes"></a><span data-ttu-id="19d8e-116">Possíveis causas</span><span class="sxs-lookup"><span data-stu-id="19d8e-116">Possible Causes</span></span>

<span data-ttu-id="19d8e-117">Há muitos motivos pelos quais uma chamada draw pode falhar.</span><span class="sxs-lookup"><span data-stu-id="19d8e-117">There are many reasons that a Draw call might fail.</span></span> <span data-ttu-id="19d8e-118">Para obter mais informações, consulte a documentação do SDK do Direct2D para o método que falhou.</span><span class="sxs-lookup"><span data-stu-id="19d8e-118">For more information, see the Direct2D SDK documentation for the method that failed.</span></span>

 

 