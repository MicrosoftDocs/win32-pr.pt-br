---
title: Verifique se o texto é exibido com a direção de leitura correta
description: Algumas linguagens, como árabe e Hebraico, exigem uma direção de leitura da direita para a esquerda.
ms.assetid: fa9a3dd6-575a-4877-a488-22845c6726c8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5d97eee49a830986718c04b4adab7443e488093
ms.sourcegitcommit: 43b2f5209d67eae96b17c03bac2a2afab1f4d30a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103641817"
---
# <a name="ensure-text-is-displayed-with-the-correct-reading-direction"></a><span data-ttu-id="b7a1c-103">Verifique se o texto é exibido com a direção de leitura correta</span><span class="sxs-lookup"><span data-stu-id="b7a1c-103">Ensure text is displayed with the correct reading direction</span></span>

<span data-ttu-id="b7a1c-104">Algumas linguagens, como árabe e Hebraico, exigem uma direção de leitura da direita para a esquerda.</span><span class="sxs-lookup"><span data-stu-id="b7a1c-104">Some languages, such as Arabic and Hebrew, require a right-to-left reading direction.</span></span> <span data-ttu-id="b7a1c-105">Para um objeto de formato de texto [DirectWrite](direct-write-portal.md) , a direção de leitura padrão é da esquerda para a direita.</span><span class="sxs-lookup"><span data-stu-id="b7a1c-105">For a [DirectWrite](direct-write-portal.md) text format object, the default reading direction is left-to-right.</span></span> <span data-ttu-id="b7a1c-106">O DirectWrite não infere automaticamente a direção de leitura da localidade, portanto, você deve fazer isso por conta própria.</span><span class="sxs-lookup"><span data-stu-id="b7a1c-106">DirectWrite does not automatically infer the reading direction from the locale, so you must do this yourself.</span></span>

<span data-ttu-id="b7a1c-107">Primeiro, obtenha os sinalizadores de estilo estendidos para a janela para a qual o texto será renderizado usando a macro GetWindowStyleEx definida em windowsx. h.</span><span class="sxs-lookup"><span data-stu-id="b7a1c-107">First, get the extended style flags for the window that the text will be rendered to by using the GetWindowStyleEx macro defined in windowsx.h.</span></span>


```C++
// Get the window extended style flagsfor the current window.
DWORD dwStyle = GetWindowExStyle(hwnd_);
```



<span data-ttu-id="b7a1c-108">A macro retorna um valor DWORD constituído de vários sinalizadores combinados com operações or bits.</span><span class="sxs-lookup"><span data-stu-id="b7a1c-108">The macro returns a DWORD value made up of several flags combined with bitwise OR operations.</span></span> <span data-ttu-id="b7a1c-109">Você deve determinar se os sinalizadores específicos que afetam a direção de leitura estão lá.</span><span class="sxs-lookup"><span data-stu-id="b7a1c-109">You must determine if the specific flags affecting reading direction are there.</span></span>

<span data-ttu-id="b7a1c-110">Há dois sinalizadores diferentes relacionados à direção de leitura: WS \_ ex \_ LAYOUTRTL e WS \_ ex \_ RTLREADING.</span><span class="sxs-lookup"><span data-stu-id="b7a1c-110">There are 2 different flags that are related to the reading direction: WS\_EX\_LAYOUTRTL and WS\_EX\_RTLREADING.</span></span>

<span data-ttu-id="b7a1c-111">Use o operador AND de bit e a (&) com a variável dwStyle e a \_ macro WS ex \_ LAYOUTRTL para armazenar um valor bool que indica se o layout é espelhado.</span><span class="sxs-lookup"><span data-stu-id="b7a1c-111">Use the bitwise AND operator (&) with the dwStyle variable and the WS\_EX\_LAYOUTRTL macro to store a BOOL value that indicates if the layout is mirrored.</span></span>


```C++
// Is the WS_EX_LAYOUTRTL flag present?
BOOL bWSLayout = dwStyle & WS_EX_LAYOUTRTL;
```



<span data-ttu-id="b7a1c-112">Faça a mesma coisa para o \_ sinalizador WS ex \_ RTLREADING.</span><span class="sxs-lookup"><span data-stu-id="b7a1c-112">Do the same thing for the WS\_EX\_RTLREADING flag.</span></span>


```C++
// Is the WS_EX_RLTREADING flag present?
BOOL bWSReading = dwStyle & WS_EX_RTLREADING;
```



<span data-ttu-id="b7a1c-113">Defina a direção de leitura usando o método [**IDWriteTextFormat:: SetReadingDirection**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-setreadingdirection) .</span><span class="sxs-lookup"><span data-stu-id="b7a1c-113">Set the reading direction by using the [**IDWriteTextFormat::SetReadingDirection**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-setreadingdirection) method.</span></span> <span data-ttu-id="b7a1c-114">O padrão é da esquerda para a direita, portanto, você só precisa definir a direção de leitura se ela for da direita para a esquerda.</span><span class="sxs-lookup"><span data-stu-id="b7a1c-114">The default is left-to-right, so you only need to set the reading direction if it is right-to-left.</span></span>

> [!Note]  
> <span data-ttu-id="b7a1c-115">\_O WS ex \_ LAYOUTRTL espelha todo o layout e implica a direção de leitura da direita para a esquerda, portanto, defina a direção de leitura somente se um desses sinalizadores estiver presente.</span><span class="sxs-lookup"><span data-stu-id="b7a1c-115">WS\_EX\_LAYOUTRTL mirrors the whole layout and implies right-to-left reading direction, so set the reading direction only if one of these flags is present.</span></span> <span data-ttu-id="b7a1c-116">Se ambos estiverem presentes, eles cancelarão um ao outro e a direção de leitura do formato de texto deverá ser da esquerda para a direita.</span><span class="sxs-lookup"><span data-stu-id="b7a1c-116">If both are present, they cancel one another out and the reading direction for the text format should be left-to-right.</span></span>

 


```C++
// If either the WS_EX_LAYOUTRTL flag or the WS_EX_RLTREADING flag is present,
// but NOT BOTH, set the reading direction to right to left.
if ((bWSLayout && !bWSReading)
||  (!bWSLayout && bWSReading))
{
    pTextFormat_->SetReadingDirection(DWRITE_READING_DIRECTION_RIGHT_TO_LEFT);
}
```



 

 
