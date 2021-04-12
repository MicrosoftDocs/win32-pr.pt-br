---
title: Efeito de Unpremultiply
description: Use esse efeito para converter uma imagem de alfa-geomultiplicado Alpha para unpremultiplied Alpha.
ms.assetid: A4FAF899-81DA-4BDA-98B4-DE63EC1664F5
keywords:
- efeito de unpremultiply
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5628ea646443a08abffa4549ad25147deb609acf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369817"
---
# <a name="unpremultiply-effect"></a><span data-ttu-id="83e7e-104">Efeito de Unpremultiply</span><span class="sxs-lookup"><span data-stu-id="83e7e-104">Unpremultiply effect</span></span>

<span data-ttu-id="83e7e-105">Use esse efeito para converter uma imagem de alfa-geomultiplicado Alpha para unpremultiplied Alpha.</span><span class="sxs-lookup"><span data-stu-id="83e7e-105">Use this effect to convert an image from premultiplied alpha to unpremultiplied alpha.</span></span> <span data-ttu-id="83e7e-106">O efeito substitui cada pixel de entrada `P = {R, G, B, A}` por `P' = {R/A, G/A, B/A, A}` na saída.</span><span class="sxs-lookup"><span data-stu-id="83e7e-106">The effect replaces each input pixel `P = {R, G, B, A}` with `P' = {R/A, G/A, B/A, A}` in the output.</span></span>

<span data-ttu-id="83e7e-107">Esse efeito não tem propriedades.</span><span class="sxs-lookup"><span data-stu-id="83e7e-107">This effect has no properties.</span></span>

<span data-ttu-id="83e7e-108">O CLSID para esse efeito é CLSID \_ D2D1Unpremultiply.</span><span class="sxs-lookup"><span data-stu-id="83e7e-108">The CLSID for this effect is CLSID\_D2D1Unpremultiply.</span></span>

## <a name="output-bitmap"></a><span data-ttu-id="83e7e-109">Bitmap de saída</span><span class="sxs-lookup"><span data-stu-id="83e7e-109">Output bitmap</span></span>

<span data-ttu-id="83e7e-110">O tamanho do bitmap de saída é o mesmo que o tamanho do bitmap de entrada.</span><span class="sxs-lookup"><span data-stu-id="83e7e-110">The output bitmap size is the same as the input bitmap size.</span></span>

## <a name="requirements"></a><span data-ttu-id="83e7e-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="83e7e-111">Requirements</span></span>



| <span data-ttu-id="83e7e-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="83e7e-112">Requirement</span></span> | <span data-ttu-id="83e7e-113">Valor</span><span class="sxs-lookup"><span data-stu-id="83e7e-113">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="83e7e-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="83e7e-114">Minimum supported client</span></span> | <span data-ttu-id="83e7e-115">Windows 8 e atualização de plataforma para aplicativos de área de trabalho do Windows 7 \[ \| aplicativos da Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="83e7e-115">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="83e7e-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="83e7e-116">Minimum supported server</span></span> | <span data-ttu-id="83e7e-117">Windows 8 e atualização de plataforma para aplicativos de área de trabalho do Windows 7 \[ \| aplicativos da Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="83e7e-117">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="83e7e-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="83e7e-118">Header</span></span>                   | <span data-ttu-id="83e7e-119">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="83e7e-119">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="83e7e-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="83e7e-120">Library</span></span>                  | <span data-ttu-id="83e7e-121">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="83e7e-121">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="83e7e-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="83e7e-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="83e7e-123">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="83e7e-123">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

 
