---
description: Este tópico lista os métodos drawstring da classe Graphics. Para obter uma lista completa de métodos para a classe Graphics, consulte gráficos.
ms.assetid: b3568ed9-e359-4916-a83d-7553c021d197
title: Métodos gráficos. DrawString (Gdiplusgraphics. h)
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 275c256ec2c7284401d37794bccf368538cbdd80
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "104970807"
---
# <a name="graphicsdrawstring-methods"></a><span data-ttu-id="aecaa-104">Métodos gráficos. DrawString</span><span class="sxs-lookup"><span data-stu-id="aecaa-104">Graphics.DrawString methods</span></span>

<span data-ttu-id="aecaa-105">Este tópico lista os métodos drawstring da classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="aecaa-105">This topic lists the DrawString methods of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class.</span></span> <span data-ttu-id="aecaa-106">Para obter uma lista completa de métodos para a classe **Graphics** , consulte [**gráficos**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics).</span><span class="sxs-lookup"><span data-stu-id="aecaa-106">For a complete list of methods for the **Graphics** class, see [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics).</span></span>

### <a name="overload-list"></a><span data-ttu-id="aecaa-107">Lista de sobrecargas</span><span class="sxs-lookup"><span data-stu-id="aecaa-107">Overload list</span></span>



| <span data-ttu-id="aecaa-108">Método</span><span class="sxs-lookup"><span data-stu-id="aecaa-108">Method</span></span>                                                                                                                                                       | <span data-ttu-id="aecaa-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="aecaa-109">Description</span></span>                                                                                                                                                                                                   |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aecaa-110">[**DrawString (WCHAR \* , int, fonte \* , PointF&, pincel \* )**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush))</span><span class="sxs-lookup"><span data-stu-id="aecaa-110">[**DrawString(WCHAR\*,INT,Font\*,PointF&,Brush\*)**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush))</span></span>                                | <span data-ttu-id="aecaa-111">O método [**Graphics::D rawstring**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) desenha uma cadeia de caracteres com base em uma fonte e uma origem para a cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="aecaa-111">The [**Graphics::DrawString**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) method draws a string based on a font and an origin for the string.</span></span><br/>                        |
| <span data-ttu-id="aecaa-112">[**DrawString (WCHAR \* , int, fonte \* , RectF&, StringFormat \* , pincel \* )**](/previous-versions//ms535991(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="aecaa-112">[**DrawString(WCHAR\*,INT,Font\*,RectF&,StringFormat\*,Brush\*)**](/previous-versions//ms535991(v=vs.85))</span></span> | <span data-ttu-id="aecaa-113">O método [**Graphics::D rawstring**](/previous-versions//ms535991(v=vs.85)) desenha uma cadeia de caracteres com base em uma fonte, um retângulo de layout e um formato.</span><span class="sxs-lookup"><span data-stu-id="aecaa-113">The [**Graphics::DrawString**](/previous-versions//ms535991(v=vs.85)) method draws a string based on a font, a layout rectangle, and a format.</span></span> <br/> |
| <span data-ttu-id="aecaa-114">[**DrawString (WCHAR \* , int, fonte \* , PointF&, StringFormat \* , pincel \* )**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush))</span><span class="sxs-lookup"><span data-stu-id="aecaa-114">[**DrawString(WCHAR\*,INT,Font\*,PointF&,StringFormat\*,Brush\*)**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush))</span></span>    | <span data-ttu-id="aecaa-115">O método [**Graphics::D rawstring**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) desenha uma cadeia de caracteres com base em uma fonte, uma origem de cadeia de caracteres e um formato.</span><span class="sxs-lookup"><span data-stu-id="aecaa-115">The [**Graphics::DrawString**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) method draws a string based on a font, a string origin, and a format.</span></span><br/>         |



## <a name="requirements"></a><span data-ttu-id="aecaa-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aecaa-116">Requirements</span></span>



| <span data-ttu-id="aecaa-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="aecaa-117">Requirement</span></span> | <span data-ttu-id="aecaa-118">Valor</span><span class="sxs-lookup"><span data-stu-id="aecaa-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="aecaa-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="aecaa-119">Header</span></span><br/> | <dl> <span data-ttu-id="aecaa-120"><dt>Gdiplusgraphics. h</dt></span><span class="sxs-lookup"><span data-stu-id="aecaa-120"><dt>Gdiplusgraphics.h</dt></span></span> </dl> |



 

 
