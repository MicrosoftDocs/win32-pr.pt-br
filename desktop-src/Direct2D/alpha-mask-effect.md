---
title: Efeito de máscara alfa
description: Esse efeito aplica uma máscara Alfa a uma imagem. Ele tem duas entradas, chamadas de destino e máscara. Os valores de cor na imagem de destino são multiplicados pelo canal alfa da imagem de máscara.
ms.assetid: fddad107-ec70-3a24-f4ae-9dc4f3716536
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87669608ab75ab7a655c072e174dbcd19df4bb39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086516"
---
# <a name="alpha-mask-effect"></a><span data-ttu-id="d823d-105">Efeito de máscara alfa</span><span class="sxs-lookup"><span data-stu-id="d823d-105">Alpha mask effect</span></span>

<span data-ttu-id="d823d-106">Esse efeito aplica uma máscara Alfa a uma imagem.</span><span class="sxs-lookup"><span data-stu-id="d823d-106">This effect applies an alpha mask to an image.</span></span> <span data-ttu-id="d823d-107">Ele tem duas entradas, chamadas de destino e máscara.</span><span class="sxs-lookup"><span data-stu-id="d823d-107">It has two inputs, named Destination and Mask.</span></span> <span data-ttu-id="d823d-108">Os valores de cor na imagem de destino são multiplicados pelo canal alfa da imagem de máscara.</span><span class="sxs-lookup"><span data-stu-id="d823d-108">Color values in the Destination image are multiplied by the alpha channel of the Mask image.</span></span>

<span data-ttu-id="d823d-109">O CLSID para esse efeito é CLSID \_ D2D1AlphaMask.</span><span class="sxs-lookup"><span data-stu-id="d823d-109">The CLSID for this effect is CLSID\_D2D1AlphaMask.</span></span>

## <a name="effect-properties"></a><span data-ttu-id="d823d-110">Propriedades do efeito</span><span class="sxs-lookup"><span data-stu-id="d823d-110">Effect properties</span></span>

<span data-ttu-id="d823d-111">Esse efeito não tem propriedades específicas de efeito.</span><span class="sxs-lookup"><span data-stu-id="d823d-111">This effect has no effect-specific properties.</span></span>

## <a name="requirements"></a><span data-ttu-id="d823d-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d823d-112">Requirements</span></span>



| <span data-ttu-id="d823d-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="d823d-113">Requirement</span></span> | <span data-ttu-id="d823d-114">Valor</span><span class="sxs-lookup"><span data-stu-id="d823d-114">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="d823d-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d823d-115">Minimum supported client</span></span> | <span data-ttu-id="d823d-116">Aplicativos do Windows 10 \[ Desktop aplicativos da \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="d823d-116">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="d823d-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d823d-117">Minimum supported server</span></span> | <span data-ttu-id="d823d-118">Aplicativos do Windows 10 \[ Desktop aplicativos da \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="d823d-118">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="d823d-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d823d-119">Header</span></span>                   | <span data-ttu-id="d823d-120">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="d823d-120">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="d823d-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d823d-121">Library</span></span>                  | <span data-ttu-id="d823d-122">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="d823d-122">d2d1.lib, dxguid.lib</span></span>                              |

## <a name="related-topics"></a><span data-ttu-id="d823d-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d823d-123">Related topics</span></span>

* [<span data-ttu-id="d823d-124">Interface ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="d823d-124">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)

