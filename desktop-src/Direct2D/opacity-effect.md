---
title: Efeito de opacidade
description: Esse efeito ajusta a opacidade de uma imagem multiplicando o canal alfa da entrada pelo valor de opacidade especificado. Ele tem uma única entrada.
ms.assetid: a4995228-e08f-b543-0af1-e0eedfe8ecb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfdc12aa8545f2742561490a3ddce799d6a1aa62
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105760294"
---
# <a name="opacity-effect"></a><span data-ttu-id="7d862-104">Efeito de opacidade</span><span class="sxs-lookup"><span data-stu-id="7d862-104">Opacity effect</span></span>

<span data-ttu-id="7d862-105">Esse efeito ajusta a opacidade de uma imagem multiplicando o canal alfa da entrada pelo valor de opacidade especificado.</span><span class="sxs-lookup"><span data-stu-id="7d862-105">This effect adjusts the opacity of an image by multiplying the alpha channel of the input by the specified opacity value.</span></span> <span data-ttu-id="7d862-106">Ele tem uma única entrada.</span><span class="sxs-lookup"><span data-stu-id="7d862-106">It has a single input.</span></span>

<span data-ttu-id="7d862-107">O CLSID para esse efeito é CLSID \_ D2D1Opacity.</span><span class="sxs-lookup"><span data-stu-id="7d862-107">The CLSID for this effect is CLSID\_D2D1Opacity.</span></span>

## <a name="effect-properties"></a><span data-ttu-id="7d862-108">Propriedades do efeito</span><span class="sxs-lookup"><span data-stu-id="7d862-108">Effect properties</span></span>



| <span data-ttu-id="7d862-109">Nome de exibição e enumeração de índice</span><span class="sxs-lookup"><span data-stu-id="7d862-109">Display name and index enumeration</span></span>              | <span data-ttu-id="7d862-110">Tipo e valor padrão</span><span class="sxs-lookup"><span data-stu-id="7d862-110">Type and default value</span></span> | <span data-ttu-id="7d862-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="7d862-111">Description</span></span>                                                                                                 |
|-------------------------------------------------|------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d862-112">Opacidade da opacidade D2D1 Opacity \_ \_ prop \_</span><span class="sxs-lookup"><span data-stu-id="7d862-112">Opacity D2D1\_OPACITY\_PROP\_OPACITY</span></span><br/> | <span data-ttu-id="7d862-113">FLOAT 1.0 f</span><span class="sxs-lookup"><span data-stu-id="7d862-113">FLOAT1.0f</span></span><br/>   | <span data-ttu-id="7d862-114">O multiplicador do canal alfa da imagem de entrada.</span><span class="sxs-lookup"><span data-stu-id="7d862-114">The multiplier to the input image's alpha channel.</span></span> <span data-ttu-id="7d862-115">O valor mínimo é 0,0 f e o valor máximo é 1,0 f.</span><span class="sxs-lookup"><span data-stu-id="7d862-115">The minimum value is 0.0f and the maximum value is 1.0f.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="7d862-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7d862-116">Requirements</span></span>



| <span data-ttu-id="7d862-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d862-117">Requirement</span></span> | <span data-ttu-id="7d862-118">Valor</span><span class="sxs-lookup"><span data-stu-id="7d862-118">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="7d862-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7d862-119">Minimum supported client</span></span> | <span data-ttu-id="7d862-120">Aplicativos do Windows 10 \[ Desktop aplicativos da \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="7d862-120">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="7d862-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7d862-121">Minimum supported server</span></span> | <span data-ttu-id="7d862-122">Aplicativos do Windows 10 \[ Desktop aplicativos da \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="7d862-122">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="7d862-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7d862-123">Header</span></span>                   | <span data-ttu-id="7d862-124">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="7d862-124">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="7d862-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7d862-125">Library</span></span>                  | <span data-ttu-id="7d862-126">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="7d862-126">d2d1.lib, dxguid.lib</span></span>                              |


## <a name="related-topics"></a><span data-ttu-id="7d862-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7d862-127">Related topics</span></span>

* [<span data-ttu-id="7d862-128">Interface ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="7d862-128">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
