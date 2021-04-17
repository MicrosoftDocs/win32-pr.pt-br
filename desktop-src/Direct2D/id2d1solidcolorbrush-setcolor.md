---
title: Métodos setColor ID2D1SolidColorBrush
description: Especifica a cor deste pincel de cor sólida.
ms.assetid: 2900bf72-9641-419c-b0d7-334f14f8a474
keywords:
- Métodos setColor Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 580778135e840a69342ff34ffd8e415883317517
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105775643"
---
# <a name="id2d1solidcolorbrushsetcolor-methods"></a><span data-ttu-id="dc609-104">Métodos ID2D1SolidColorBrush:: setColor</span><span class="sxs-lookup"><span data-stu-id="dc609-104">ID2D1SolidColorBrush::SetColor methods</span></span>

<span data-ttu-id="dc609-105">Especifica a cor deste pincel de cor sólida.</span><span class="sxs-lookup"><span data-stu-id="dc609-105">Specifies the color of this solid color brush.</span></span>

### <a name="overload-list"></a><span data-ttu-id="dc609-106">Lista de sobrecargas</span><span class="sxs-lookup"><span data-stu-id="dc609-106">Overload list</span></span>



| <span data-ttu-id="dc609-107">Método</span><span class="sxs-lookup"><span data-stu-id="dc609-107">Method</span></span>                                                                          | <span data-ttu-id="dc609-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="dc609-108">Description</span></span>                                                |
|:--------------------------------------------------------------------------------|:-----------------------------------------------------------|
| <span data-ttu-id="dc609-109">[**SetColor (D2D1 de \_ cor \_ F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1solidcolorbrush-setcolor(constd2d1_color_f_))</span><span class="sxs-lookup"><span data-stu-id="dc609-109">[**SetColor(D2D1\_COLOR\_F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1solidcolorbrush-setcolor(constd2d1_color_f_))</span></span>  | <span data-ttu-id="dc609-110">Especifica a cor deste pincel de cor sólida.</span><span class="sxs-lookup"><span data-stu-id="dc609-110">Specifies the color of this solid-color brush.</span></span> <br/> |
| <span data-ttu-id="dc609-111">[**SetColor (D2D1 \_ cor \_ F \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1solidcolorbrush-setcolor(constd2d1_color_f))</span><span class="sxs-lookup"><span data-stu-id="dc609-111">[**SetColor(D2D1\_COLOR\_F\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1solidcolorbrush-setcolor(constd2d1_color_f))</span></span> | <span data-ttu-id="dc609-112">Especifica a cor deste pincel de cor sólida.</span><span class="sxs-lookup"><span data-stu-id="dc609-112">Specifies the color of this solid color brush.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="dc609-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="dc609-113">Remarks</span></span>

<span data-ttu-id="dc609-114">Para ajudar a criar cores, o Direct2D fornece a classe [**colorf**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) .</span><span class="sxs-lookup"><span data-stu-id="dc609-114">To help create colors, Direct2D provides the [**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) class.</span></span> <span data-ttu-id="dc609-115">Ele oferece vários métodos auxiliares para a criação de cores e fornece um conjunto ou cores predefinidas.</span><span class="sxs-lookup"><span data-stu-id="dc609-115">It offers several helper methods for creating colors and provides a set or predefined colors.</span></span>

## <a name="examples"></a><span data-ttu-id="dc609-116">Exemplos</span><span class="sxs-lookup"><span data-stu-id="dc609-116">Examples</span></span>

<span data-ttu-id="dc609-117">O código a seguir mostra como usar esse método.</span><span class="sxs-lookup"><span data-stu-id="dc609-117">The following code shows how to use this method.</span></span>


```C++
        m_pSolidColorBrush->SetColor(
            D2D1::ColorF(
                0.0f,
                intensity,
                1.0f - intensity
                ));

        hr = m_pRealization->Fill(
                m_pRT,
                m_pSolidColorBrush,
                m_useRealizations ?
                    REALIZATION_RENDER_MODE_DEFAULT :
                    REALIZATION_RENDER_MODE_FORCE_UNREALIZED
                );
```



## <a name="requirements"></a><span data-ttu-id="dc609-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dc609-118">Requirements</span></span>



| <span data-ttu-id="dc609-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc609-119">Requirement</span></span> | <span data-ttu-id="dc609-120">Valor</span><span class="sxs-lookup"><span data-stu-id="dc609-120">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="dc609-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="dc609-121">Library</span></span><br/> | <dl> <span data-ttu-id="dc609-122"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dc609-122"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="dc609-123">DLL</span><span class="sxs-lookup"><span data-stu-id="dc609-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="dc609-124"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dc609-124"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc609-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="dc609-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc609-126">**ID2D1SolidColorBrush**</span><span class="sxs-lookup"><span data-stu-id="dc609-126">**ID2D1SolidColorBrush**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush)
</dt> </dl>

 

