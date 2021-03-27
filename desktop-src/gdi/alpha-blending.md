---
description: A mesclagem alfa é usada para exibir um bitmap alfa, que é um bitmap que tem pixels transparentes ou semi-transparente.
ms.assetid: 52a044cc-a471-4951-adbe-32319b8e3129
title: Mistura alfa (GDI do Windows)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f68cb34d189fb80d23cbb5eeec9d9006aa93a1eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967719"
---
# <a name="alpha-blending-windows-gdi"></a><span data-ttu-id="e2780-103">Mistura alfa (GDI do Windows)</span><span class="sxs-lookup"><span data-stu-id="e2780-103">Alpha Blending (Windows GDI)</span></span>

<span data-ttu-id="e2780-104">A *mesclagem alfa* é usada para exibir um bitmap alfa, que é um bitmap que tem pixels transparentes ou semi-transparente.</span><span class="sxs-lookup"><span data-stu-id="e2780-104">*Alpha blending* is used to display an alpha bitmap, which is a bitmap that has transparent or semi-transparent pixels.</span></span> <span data-ttu-id="e2780-105">Além de um canal de cores vermelho, verde e azul, cada pixel em um bitmap alfa tem um componente de transparência conhecido como seu *canal alfa*.</span><span class="sxs-lookup"><span data-stu-id="e2780-105">In addition to a red, green, and blue color channel, each pixel in an alpha bitmap has a transparency component known as its *alpha channel*.</span></span> <span data-ttu-id="e2780-106">Normalmente, o canal alfa contém tantos bits quanto um canal de cores.</span><span class="sxs-lookup"><span data-stu-id="e2780-106">The alpha channel typically contains as many bits as a color channel.</span></span> <span data-ttu-id="e2780-107">Por exemplo, um canal alfa de 8 bits pode representar 256 níveis de transparência, de 0 (o bitmap inteiro é transparente) para 255 (todo o bitmap é opaco).</span><span class="sxs-lookup"><span data-stu-id="e2780-107">For example, an 8-bit alpha channel can represent 256 levels of transparency, from 0 (the entire bitmap is transparent) to 255 (the entire bitmap is opaque).</span></span>

<span data-ttu-id="e2780-108">Os mecanismos de mesclagem Alfa são invocados chamando [**AlphaBlend**](/windows/desktop/api/WinGdi/nf-wingdi-alphablend), que referencia a estrutura [**BLENDFUNCTION**](/windows/desktop/api/Wingdi/ns-wingdi-blendfunction) .</span><span class="sxs-lookup"><span data-stu-id="e2780-108">Alpha blending mechanisms are invoked by calling [**AlphaBlend**](/windows/desktop/api/WinGdi/nf-wingdi-alphablend), which references the [**BLENDFUNCTION**](/windows/desktop/api/Wingdi/ns-wingdi-blendfunction) structure.</span></span>

<span data-ttu-id="e2780-109">Os valores Alfa por pixel têm suporte apenas para BI RGB de 32-bpp \_ .</span><span class="sxs-lookup"><span data-stu-id="e2780-109">Alpha values per pixel are only supported for 32-bpp BI\_RGB.</span></span> <span data-ttu-id="e2780-110">Esta fórmula é definida como:</span><span class="sxs-lookup"><span data-stu-id="e2780-110">This formula is defined as:</span></span>


```C++
typedef struct {
  BYTE   Blue;
  BYTE   Green;
  BYTE   Red;
  BYTE   Alpha;
};
```



<span data-ttu-id="e2780-111">Isso é representado na memória, conforme mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="e2780-111">This is represented in memory as shown in the following table.</span></span>



|       |       |       |       |
|-------|-------|-------|-------|
| <span data-ttu-id="e2780-112">31:24</span><span class="sxs-lookup"><span data-stu-id="e2780-112">31:24</span></span> | <span data-ttu-id="e2780-113">23:16</span><span class="sxs-lookup"><span data-stu-id="e2780-113">23:16</span></span> | <span data-ttu-id="e2780-114">15:08</span><span class="sxs-lookup"><span data-stu-id="e2780-114">15:08</span></span> | <span data-ttu-id="e2780-115">07:00</span><span class="sxs-lookup"><span data-stu-id="e2780-115">07:00</span></span> |
| <span data-ttu-id="e2780-116">Alpha</span><span class="sxs-lookup"><span data-stu-id="e2780-116">Alpha</span></span> | <span data-ttu-id="e2780-117">Vermelho</span><span class="sxs-lookup"><span data-stu-id="e2780-117">Red</span></span>   | <span data-ttu-id="e2780-118">Verde</span><span class="sxs-lookup"><span data-stu-id="e2780-118">Green</span></span> | <span data-ttu-id="e2780-119">Azul</span><span class="sxs-lookup"><span data-stu-id="e2780-119">Blue</span></span>  |



 

<span data-ttu-id="e2780-120">Os bitmaps também podem ser exibidos com um fator de transparência aplicado ao bitmap inteiro.</span><span class="sxs-lookup"><span data-stu-id="e2780-120">Bitmaps may also be displayed with a transparency factor applied to the entire bitmap.</span></span> <span data-ttu-id="e2780-121">Qualquer formato de bitmap pode ser exibido com um valor alfa constante global definindo **SourceConstantAlpha** na estrutura [**BLENDFUNCTION**](/windows/desktop/api/Wingdi/ns-wingdi-blendfunction) .</span><span class="sxs-lookup"><span data-stu-id="e2780-121">Any bitmap format can be displayed with a global constant alpha value by setting **SourceConstantAlpha** in the [**BLENDFUNCTION**](/windows/desktop/api/Wingdi/ns-wingdi-blendfunction) structure.</span></span> <span data-ttu-id="e2780-122">O valor alfa da constante global tem 256 níveis de transparência, de 0 (o bitmap inteiro é completamente transparente) a 255 (o bitmap inteiro é completamente opaco).</span><span class="sxs-lookup"><span data-stu-id="e2780-122">The global constant alpha value has 256 levels of transparency, from 0 (entire bitmap is completely transparent) to 255 (entire bitmap is completely opaque).</span></span> <span data-ttu-id="e2780-123">O valor alfa global constante é combinado com o valor alfa por pixel.</span><span class="sxs-lookup"><span data-stu-id="e2780-123">The global constant alpha value is combined with the per-pixel alpha value.</span></span>

<span data-ttu-id="e2780-124">Para obter um exemplo, consulte [alpha blending a bitmap](alpha-blending-a-bitmap.md).</span><span class="sxs-lookup"><span data-stu-id="e2780-124">For an example, see [Alpha Blending a Bitmap](alpha-blending-a-bitmap.md).</span></span>

 

 



