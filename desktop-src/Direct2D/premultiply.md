---
title: Efeito de premultiplicação
description: Use esse efeito para converter uma imagem de unpremultiplied alfa para alfa-geomultiplicado.
ms.assetid: 8A5F55C6-3AC7-48B4-87D8-C19D8B4EA0DD
keywords:
- efeito de premultiplicação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a01a8a9ba005ed688a96254856897b3514f05fd5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918765"
---
# <a name="premultiply-effect"></a><span data-ttu-id="7ba4c-104">Efeito de premultiplicação</span><span class="sxs-lookup"><span data-stu-id="7ba4c-104">Premultiply effect</span></span>

<span data-ttu-id="7ba4c-105">Use esse efeito para converter uma imagem de unpremultiplied alfa para alfa-geomultiplicado.</span><span class="sxs-lookup"><span data-stu-id="7ba4c-105">Use this effect to convert an image from unpremultiplied alpha to premultiplied alpha.</span></span> <span data-ttu-id="7ba4c-106">O efeito substitui cada pixel de entrada `P = {R, G, B, A}` por `P' = {R*A, G*A, B*A, A}` na saída.</span><span class="sxs-lookup"><span data-stu-id="7ba4c-106">The effect replaces each input pixel `P = {R, G, B, A}` with `P' = {R*A, G*A, B*A, A}` in the output.</span></span>

<span data-ttu-id="7ba4c-107">Esse efeito não tem propriedades.</span><span class="sxs-lookup"><span data-stu-id="7ba4c-107">This effect has no properties.</span></span>

<span data-ttu-id="7ba4c-108">O CLSID para esse efeito é CLSID \_ D2D1Premultiply.</span><span class="sxs-lookup"><span data-stu-id="7ba4c-108">The CLSID for this effect is CLSID\_D2D1Premultiply.</span></span>

## <a name="output-bitmap"></a><span data-ttu-id="7ba4c-109">Bitmap de saída</span><span class="sxs-lookup"><span data-stu-id="7ba4c-109">Output bitmap</span></span>

<span data-ttu-id="7ba4c-110">O tamanho do bitmap de saída é o mesmo que o tamanho do bitmap de entrada.</span><span class="sxs-lookup"><span data-stu-id="7ba4c-110">The output bitmap size is the same as the input bitmap size.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ba4c-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7ba4c-111">Requirements</span></span>



| <span data-ttu-id="7ba4c-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ba4c-112">Requirement</span></span> | <span data-ttu-id="7ba4c-113">Valor</span><span class="sxs-lookup"><span data-stu-id="7ba4c-113">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7ba4c-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7ba4c-114">Minimum supported client</span></span> | <span data-ttu-id="7ba4c-115">Windows 8 e atualização de plataforma para aplicativos de área de trabalho do Windows 7 \[ \| aplicativos da Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="7ba4c-115">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="7ba4c-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7ba4c-116">Minimum supported server</span></span> | <span data-ttu-id="7ba4c-117">Windows 8 e atualização de plataforma para aplicativos de área de trabalho do Windows 7 \[ \| aplicativos da Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="7ba4c-117">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="7ba4c-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7ba4c-118">Header</span></span>                   | <span data-ttu-id="7ba4c-119">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="7ba4c-119">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="7ba4c-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7ba4c-120">Library</span></span>                  | <span data-ttu-id="7ba4c-121">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="7ba4c-121">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="7ba4c-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7ba4c-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ba4c-123">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="7ba4c-123">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

 
