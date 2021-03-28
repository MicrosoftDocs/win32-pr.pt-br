---
description: Você pode consultar e definir o alinhamento de texto para um contexto de dispositivo usando as funções GetTextAlign e SetTextAlign.
ms.assetid: 7fdfbadb-827a-4b42-9b9a-b9e46389e13c
title: Definindo o alinhamento de texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 538a8da060f9d854890ea004c855e2317986fd19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967874"
---
# <a name="setting-the-text-alignment"></a><span data-ttu-id="1c401-103">Definindo o alinhamento de texto</span><span class="sxs-lookup"><span data-stu-id="1c401-103">Setting the Text Alignment</span></span>

<span data-ttu-id="1c401-104">Você pode consultar e definir o alinhamento de texto para um contexto de dispositivo usando as funções [**GetTextAlign**](/windows/desktop/api/Wingdi/nf-wingdi-gettextalign) e [**SetTextAlign**](/windows/desktop/api/Wingdi/nf-wingdi-settextalign) .</span><span class="sxs-lookup"><span data-stu-id="1c401-104">You can query and set the text alignment for a device context by using the [**GetTextAlign**](/windows/desktop/api/Wingdi/nf-wingdi-gettextalign) and [**SetTextAlign**](/windows/desktop/api/Wingdi/nf-wingdi-settextalign) functions.</span></span> <span data-ttu-id="1c401-105">As configurações de alinhamento de texto determinam como o texto é posicionado em relação a um local especificado.</span><span class="sxs-lookup"><span data-stu-id="1c401-105">The text-alignment settings determine how text is positioned relative to a specified location.</span></span> <span data-ttu-id="1c401-106">O texto pode ser alinhado à direita ou à esquerda da posição ou centralizado sobre ele; Ele também pode ser alinhado acima ou abaixo do ponto.</span><span class="sxs-lookup"><span data-stu-id="1c401-106">Text can be aligned to the right or left of the position or centered over it; it can also be aligned above or below the point.</span></span>

<span data-ttu-id="1c401-107">O exemplo a seguir mostra um método para determinar qual sinalizador de alinhamento horizontal está definido:</span><span class="sxs-lookup"><span data-stu-id="1c401-107">The following example shows a method for determining which horizontal alignment flag is set:</span></span>


```C++
switch ((TA_LEFT | TA_RIGHT | TA_CENTER) & GetTextAlign(hdc)) 
{ 
    case TA_LEFT: 
       . 
       . 
       . 
    case TA_RIGHT: 
       . 
       . 
       . 
    case TA_CENTER: 
       . 
       . 
       . 
} 
```



<span data-ttu-id="1c401-108">Você também pode usar a função [**SetTextAlign**](/windows/desktop/api/Wingdi/nf-wingdi-settextalign) para atualizar a posição atual quando uma função de texto de saída é chamada.</span><span class="sxs-lookup"><span data-stu-id="1c401-108">You can also use the [**SetTextAlign**](/windows/desktop/api/Wingdi/nf-wingdi-settextalign) function to update the current position when a text-output function is called.</span></span> <span data-ttu-id="1c401-109">Por exemplo, os exemplos a seguir usam a função [**SetTextAlign**](/windows/win32/api/wingdi/nf-wingdi-settextalign) para atualizar a posição atual quando a função [**TextOut**](/windows/desktop/api/Wingdi/nf-wingdi-textouta) é chamada.</span><span class="sxs-lookup"><span data-stu-id="1c401-109">For instance, the following example uses the [**SetTextAlign**](/windows/win32/api/wingdi/nf-wingdi-settextalign) function to update the current position when the [**TextOut**](/windows/desktop/api/Wingdi/nf-wingdi-textouta) function is called.</span></span> <span data-ttu-id="1c401-110">Neste exemplo, o parâmetro *cArial* é um inteiro que especifica o número de fontes Arial.</span><span class="sxs-lookup"><span data-stu-id="1c401-110">In this example, the *cArial* parameter is an integer that specifies the number of Arial fonts.</span></span>


```C++
UINT uAlignPrev; 
char szCount[8];
HRESULT hr;
size_t * pcch; 
 
uAlignPrev = SetTextAlign(hdc, TA_UPDATECP); 
MoveToEx(hdc, 10, 50, (LPPOINT) NULL); 
TextOut(hdc, 0, 0, "Number of Arial fonts: ", 23); 
itoa(cArial, szCount, 10); 

hr = StringCchLength(szCount, 9, pcch);
if (FAILED(hr))
{
// TODO: write error handler 
}
 
TextOut(hdc, 0, 0, (LPSTR) szCount, *pcch); 
SetTextAlign(hdc, uAlignPrev); 
```



> [!Note]  
> <span data-ttu-id="1c401-111">Você não deve usar [**SetTextAlign**](/windows/win32/api/wingdi/nf-wingdi-settextalign) com ta \_ UPDATECP quando estiver usando [**ScriptStringOut**](/windows/win32/api/usp10/nf-usp10-scriptstringout), pois o texto selecionado não é renderizado corretamente.</span><span class="sxs-lookup"><span data-stu-id="1c401-111">You should not use [**SetTextAlign**](/windows/win32/api/wingdi/nf-wingdi-settextalign) with TA\_UPDATECP when you are using [**ScriptStringOut**](/windows/win32/api/usp10/nf-usp10-scriptstringout), because selected text is not rendered correctly.</span></span> <span data-ttu-id="1c401-112">Se você precisar usar esse sinalizador, poderá remover a definição e redefini-lo conforme necessário para evitar o problema.</span><span class="sxs-lookup"><span data-stu-id="1c401-112">If you must use this flag, you can unset and reset it as necessary to avoid the problem.</span></span>

 

 

 
