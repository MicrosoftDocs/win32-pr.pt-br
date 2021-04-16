---
title: Métodos DrawText ID2D1RenderTarget
description: Desenha o texto especificado usando as informações de formato fornecidas por um objeto IDWriteTextFormat.
ms.assetid: 7cda7854-f9df-48d3-bc62-6aaee769e6f9
keywords:
- Métodos DrawText Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 5ace5c64dc90f057ff9fdfe5a79d664137c38030
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758556"
---
# <a name="id2d1rendertargetdrawtext-methods"></a><span data-ttu-id="1c5ab-104">ID2D1RenderTarget: métodos de rawText de:D</span><span class="sxs-lookup"><span data-stu-id="1c5ab-104">ID2D1RenderTarget::DrawText methods</span></span>

<span data-ttu-id="1c5ab-105">Desenha o texto especificado usando as informações de formato fornecidas por um objeto [**IDWriteTextFormat**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat) .</span><span class="sxs-lookup"><span data-stu-id="1c5ab-105">Draws the specified text using the format information provided by an [**IDWriteTextFormat**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat) object.</span></span>

### <a name="overload-list"></a><span data-ttu-id="1c5ab-106">Lista de sobrecargas</span><span class="sxs-lookup"><span data-stu-id="1c5ab-106">Overload list</span></span>



| <span data-ttu-id="1c5ab-107">Método</span><span class="sxs-lookup"><span data-stu-id="1c5ab-107">Method</span></span>                                                                                                                                                                                                                                                                               | <span data-ttu-id="1c5ab-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="1c5ab-108">Description</span></span>                                                                                                                                     |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c5ab-109">[**DrawText (WCHAR \* , IDWriteTextFormat \* , d2d1 \_ Rect \_ F&, ID2D1Brush \* , d2d1 \_ \_ \_ Opções de texto de desenho, \_ método de medição de texto DWRITE \_ \_ )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode))</span><span class="sxs-lookup"><span data-stu-id="1c5ab-109">[**DrawText(WCHAR\*,IDWriteTextFormat\*,D2D1\_RECT\_F&,ID2D1Brush\*,D2D1\_DRAW\_TEXT\_OPTIONS,DWRITE\_TEXT\_MEASURING\_METHOD)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode))</span></span>  | <span data-ttu-id="1c5ab-110">Desenha o texto especificado usando as informações de formato fornecidas por um objeto [**IDWriteTextFormat**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat) .</span><span class="sxs-lookup"><span data-stu-id="1c5ab-110">Draws the specified text using the format information provided by an [**IDWriteTextFormat**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat) object.</span></span><br/>  |
| <span data-ttu-id="1c5ab-111">[**DrawText (WCHAR \* , IDWriteTextFormat \* , d2d1 \_ Rect \_ F \* , ID2D1Brush \* , d2d1 \_ \_ \_ Opções de texto de desenho, \_ método de medição de texto DWRITE \_ \_ )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f_id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode))</span><span class="sxs-lookup"><span data-stu-id="1c5ab-111">[**DrawText(WCHAR\*,IDWriteTextFormat\*,D2D1\_RECT\_F\*,ID2D1Brush\*,D2D1\_DRAW\_TEXT\_OPTIONS,DWRITE\_TEXT\_MEASURING\_METHOD)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f_id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode))</span></span> | <span data-ttu-id="1c5ab-112">Desenha o texto especificado usando as informações de formato fornecidas por um objeto [**IDWriteTextFormat**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat) .</span><span class="sxs-lookup"><span data-stu-id="1c5ab-112">Draws the specified text using the format information provided by an [**IDWriteTextFormat**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat) object.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="1c5ab-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="1c5ab-113">Remarks</span></span>

<span data-ttu-id="1c5ab-114">Para desenhar texto com Direct2D, use o método [**ID2D1RenderTarget::D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) para texto que tenha um único formato ou o método [**ID2D1RenderTarget::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) quando você precisar de vários formatos, recursos OpenType avançados ou teste de clique.</span><span class="sxs-lookup"><span data-stu-id="1c5ab-114">To draw text with Direct2D, use the [**ID2D1RenderTarget::DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) method for text that has a single format, or the [**ID2D1RenderTarget::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) method when you need multiple formats, advanced OpenType features, or hit testing.</span></span> <span data-ttu-id="1c5ab-115">Esses métodos usam a API DirectWrite para fornecer exibição de texto de alta qualidade.</span><span class="sxs-lookup"><span data-stu-id="1c5ab-115">These methods use the DirectWrite API to provide high-quality text display.</span></span>

<span data-ttu-id="1c5ab-116">Esse método não retornará um código de erro se ele falhar.</span><span class="sxs-lookup"><span data-stu-id="1c5ab-116">This method doesn't return an error code if it fails.</span></span> <span data-ttu-id="1c5ab-117">Para determinar se uma operação de desenho (como **DrawText**) falhou, verifique o resultado retornado pelos métodos [**ID2D1RenderTarget:: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) ou [**ID2D1RenderTarget:: flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) .</span><span class="sxs-lookup"><span data-stu-id="1c5ab-117">To determine whether a drawing operation (such as **DrawText**) failed, check the result returned by the [**ID2D1RenderTarget::EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) or [**ID2D1RenderTarget::Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) methods.</span></span>

## <a name="examples"></a><span data-ttu-id="1c5ab-118">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1c5ab-118">Examples</span></span>

<span data-ttu-id="1c5ab-119">Para obter um exemplo, consulte [como desenhar texto](how-to--draw-text.md).</span><span class="sxs-lookup"><span data-stu-id="1c5ab-119">For an example, see [How to Draw Text](how-to--draw-text.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1c5ab-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1c5ab-120">Requirements</span></span>



| <span data-ttu-id="1c5ab-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c5ab-121">Requirement</span></span> | <span data-ttu-id="1c5ab-122">Valor</span><span class="sxs-lookup"><span data-stu-id="1c5ab-122">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="1c5ab-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1c5ab-123">Library</span></span><br/> | <dl> <span data-ttu-id="1c5ab-124"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1c5ab-124"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="1c5ab-125">DLL</span><span class="sxs-lookup"><span data-stu-id="1c5ab-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="1c5ab-126"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c5ab-126"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c5ab-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="1c5ab-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c5ab-128">**ID2D1RenderTarget**</span><span class="sxs-lookup"><span data-stu-id="1c5ab-128">**ID2D1RenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[<span data-ttu-id="1c5ab-129">**IDWriteTextFormat**</span><span class="sxs-lookup"><span data-stu-id="1c5ab-129">**IDWriteTextFormat**</span></span>](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat)
</dt> <dt>

[<span data-ttu-id="1c5ab-130">Como desenhar texto</span><span class="sxs-lookup"><span data-stu-id="1c5ab-130">How to Draw Text</span></span>](how-to--draw-text.md)
</dt> <dt>

[<span data-ttu-id="1c5ab-131">Visão geral de formatação e layout de texto</span><span class="sxs-lookup"><span data-stu-id="1c5ab-131">Text Formatting and Layout Overview</span></span>](/windows/desktop/DirectWrite/text-formatting-and-layout)
</dt> </dl>

 

