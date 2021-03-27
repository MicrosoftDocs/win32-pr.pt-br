---
Description: O valor COLORREF é usado para especificar uma cor RGB.
ms.assetid: b87d3de2-7a13-44ef-8253-c6851a75fa54
title: COLORREF (windef. h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: 6836cfcc1b18d0b20d5e347fb83206551b27de06
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "104989460"
---
# <a name="colorref"></a><span data-ttu-id="d5c29-103">COLORREF</span><span class="sxs-lookup"><span data-stu-id="d5c29-103">COLORREF</span></span>

<span data-ttu-id="d5c29-104">O valor COLORREF é usado para especificar uma cor [RGB](/windows/desktop/api/Wingdi/nf-wingdi-rgb) .</span><span class="sxs-lookup"><span data-stu-id="d5c29-104">The COLORREF value is used to specify an [RGB](/windows/desktop/api/Wingdi/nf-wingdi-rgb) color.</span></span>


```C++
typedef DWORD COLORREF;
typedef DWORD* LPCOLORREF;
```



## <a name="remarks"></a><span data-ttu-id="d5c29-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="d5c29-105">Remarks</span></span>

<span data-ttu-id="d5c29-106">Ao especificar uma cor [RGB](/windows/desktop/api/Wingdi/nf-wingdi-rgb) explícita, o valor de **COLORREF** tem o seguinte formato hexadecimal:</span><span class="sxs-lookup"><span data-stu-id="d5c29-106">When specifying an explicit [RGB](/windows/desktop/api/Wingdi/nf-wingdi-rgb) color, the **COLORREF** value has the following hexadecimal form:</span></span>

`0x00bbggrr`

<span data-ttu-id="d5c29-107">O byte de ordem inferior contém um valor para a intensidade relativa de vermelho; o segundo byte contém um valor para verde; e o terceiro byte contém um valor para Blue.</span><span class="sxs-lookup"><span data-stu-id="d5c29-107">The low-order byte contains a value for the relative intensity of red; the second byte contains a value for green; and the third byte contains a value for blue.</span></span> <span data-ttu-id="d5c29-108">O byte de ordem superior deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="d5c29-108">The high-order byte must be zero.</span></span> <span data-ttu-id="d5c29-109">O valor máximo de um único byte é 0xFF.</span><span class="sxs-lookup"><span data-stu-id="d5c29-109">The maximum value for a single byte is 0xFF.</span></span>

<span data-ttu-id="d5c29-110">Para criar um valor de cor **COLORREF** , use a macro [RGB](/windows/desktop/api/Wingdi/nf-wingdi-rgb) .</span><span class="sxs-lookup"><span data-stu-id="d5c29-110">To create a **COLORREF** color value, use the [RGB](/windows/desktop/api/Wingdi/nf-wingdi-rgb) macro.</span></span> <span data-ttu-id="d5c29-111">Para extrair os valores individuais dos componentes vermelho, verde e azul de um valor de cor, use as macros [**GetRValue**](/windows/desktop/api/Wingdi/nf-wingdi-getrvalue), [GetGValue](/windows/desktop/api/Wingdi/nf-wingdi-getgvalue)e [GetBValue](/windows/desktop/api/Wingdi/nf-wingdi-getbvalue) , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="d5c29-111">To extract the individual values for the red, green, and blue components of a color value, use the [**GetRValue**](/windows/desktop/api/Wingdi/nf-wingdi-getrvalue), [GetGValue](/windows/desktop/api/Wingdi/nf-wingdi-getgvalue), and [GetBValue](/windows/desktop/api/Wingdi/nf-wingdi-getbvalue) macros, respectively.</span></span>

## <a name="example"></a><span data-ttu-id="d5c29-112">Exemplo</span><span class="sxs-lookup"><span data-stu-id="d5c29-112">Example</span></span>

```cpp
// Color constants.
const COLORREF rgbRed   =  0x000000FF;
const COLORREF rgbGreen =  0x0000FF00;
const COLORREF rgbBlue  =  0x00FF0000;
const COLORREF rgbBlack =  0x00000000;
const COLORREF rgbWhite =  0x00FFFFFF;
```

<span data-ttu-id="d5c29-113">Exemplo de [exemplos clássicos do Windows](https://github.com/microsoft/Windows-classic-samples) no github.</span><span class="sxs-lookup"><span data-stu-id="d5c29-113">Example from [Windows Classic Samples](https://github.com/microsoft/Windows-classic-samples) on GitHub.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5c29-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5c29-114">Requirements</span></span>



| <span data-ttu-id="d5c29-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5c29-115">Requirement</span></span> | <span data-ttu-id="d5c29-116">Valor</span><span class="sxs-lookup"><span data-stu-id="d5c29-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5c29-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d5c29-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d5c29-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d5c29-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="d5c29-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d5c29-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d5c29-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d5c29-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d5c29-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="d5c29-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5c29-122"><dt>Windef. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d5c29-122"><dt>Windef.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5c29-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="d5c29-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5c29-124">Visão geral das cores</span><span class="sxs-lookup"><span data-stu-id="d5c29-124">Colors Overview</span></span>](colors.md)
</dt> <dt>

[<span data-ttu-id="d5c29-125">Estruturas de cores</span><span class="sxs-lookup"><span data-stu-id="d5c29-125">Color Structures</span></span>](color-structures.md)
</dt> <dt>

[<span data-ttu-id="d5c29-126">GetBValue</span><span class="sxs-lookup"><span data-stu-id="d5c29-126">GetBValue</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getbvalue)
</dt> <dt>

[<span data-ttu-id="d5c29-127">GetGValue</span><span class="sxs-lookup"><span data-stu-id="d5c29-127">GetGValue</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getgvalue)
</dt> <dt>

[<span data-ttu-id="d5c29-128">**GetRValue**</span><span class="sxs-lookup"><span data-stu-id="d5c29-128">**GetRValue**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getrvalue)
</dt> <dt>

[<span data-ttu-id="d5c29-129">RGB</span><span class="sxs-lookup"><span data-stu-id="d5c29-129">RGB</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-rgb)
</dt> </dl>

 

 




