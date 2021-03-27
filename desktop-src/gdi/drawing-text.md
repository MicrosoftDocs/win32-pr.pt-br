---
description: Texto de desenho
ms.assetid: 8a06f659-4e08-4738-b7a9-956b599c1344
title: Texto de desenho (GDI do Windows)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7db44a756ff211bcae7605cb87bdac77005b34f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661612"
---
# <a name="drawing-text-windows-gdi"></a><span data-ttu-id="c28bf-103">Texto de desenho (GDI do Windows)</span><span class="sxs-lookup"><span data-stu-id="c28bf-103">Drawing Text (Windows GDI)</span></span>

<span data-ttu-id="c28bf-104">Depois que um aplicativo seleciona a fonte apropriada, define as opções de formatação de texto necessárias e computa os valores necessários de largura e altura de caractere para uma cadeia de texto, ele pode começar a desenhar caracteres e símbolos chamando qualquer uma das funções de saída de texto:</span><span class="sxs-lookup"><span data-stu-id="c28bf-104">After an application selects the appropriate font, sets the required text-formatting options, and computes the necessary character width and height values for a string of text, it can begin drawing characters and symbols by calling any of the text-output functions:</span></span>

-   [<span data-ttu-id="c28bf-105">DrawText</span><span class="sxs-lookup"><span data-stu-id="c28bf-105">DrawText</span></span>](/windows/desktop/api/Winuser/nf-winuser-drawtext)
-   [<span data-ttu-id="c28bf-106">DrawTextEx</span><span class="sxs-lookup"><span data-stu-id="c28bf-106">DrawTextEx</span></span>](/windows/desktop/api/Winuser/nf-winuser-drawtextexa)
-   [<span data-ttu-id="c28bf-107">ExtTextOut</span><span class="sxs-lookup"><span data-stu-id="c28bf-107">ExtTextOut</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta)
-   [<span data-ttu-id="c28bf-108">Semitextoout</span><span class="sxs-lookup"><span data-stu-id="c28bf-108">PolyTextOut</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polytextouta)
-   [<span data-ttu-id="c28bf-109">TabbedTextOut</span><span class="sxs-lookup"><span data-stu-id="c28bf-109">TabbedTextOut</span></span>](/windows/desktop/api/Winuser/nf-winuser-tabbedtextouta)
-   [<span data-ttu-id="c28bf-110">Texto</span><span class="sxs-lookup"><span data-stu-id="c28bf-110">TextOut</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-textouta)

<span data-ttu-id="c28bf-111">Quando um aplicativo chama uma dessas funções, o sistema operacional passa a chamada para o mecanismo de gráficos que, por sua vez, passa a chamada para o driver de dispositivo apropriado.</span><span class="sxs-lookup"><span data-stu-id="c28bf-111">When an application calls one of these functions, the operating system passes the call to the graphics engine, which in turn passes the call to the appropriate device driver.</span></span> <span data-ttu-id="c28bf-112">No nível de driver de dispositivo, todas essas chamadas têm suporte por uma ou mais chamadas para a própria função [ExtTextOut](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta) ou [TextOut](/windows/desktop/api/Wingdi/nf-wingdi-textouta) do driver.</span><span class="sxs-lookup"><span data-stu-id="c28bf-112">At the device driver level, all of these calls are supported by one or more calls to the driver's own [ExtTextOut](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta) or [TextOut](/windows/desktop/api/Wingdi/nf-wingdi-textouta) function.</span></span> <span data-ttu-id="c28bf-113">Um aplicativo obterá a execução mais rápida chamando [**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta), que é rapidamente convertido em uma chamada **ExtTextOut** para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c28bf-113">An application will achieve the fastest execution by calling [**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta), which is quickly converted into an **ExtTextOut** call for the device.</span></span> <span data-ttu-id="c28bf-114">No entanto, há instâncias em que um aplicativo deve chamar uma das outras três funções; por exemplo, para desenhar várias linhas de texto dentro das bordas de uma região retangular especificada, é mais eficiente chamar [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext).</span><span class="sxs-lookup"><span data-stu-id="c28bf-114">However, there are instances when an application should call one of the other three functions; for example, to draw multiple lines of text within the borders of a specified rectangular region, it is more efficient to call [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext).</span></span> <span data-ttu-id="c28bf-115">Para criar uma tabela de várias colunas com colunas justificadas de texto, é mais eficiente chamar [**TabbedTextOut**](/windows/win32/api/winuser/nf-winuser-tabbedtextouta).</span><span class="sxs-lookup"><span data-stu-id="c28bf-115">To create a multicolumn table with justified columns of text, it is more efficient to call [**TabbedTextOut**](/windows/win32/api/winuser/nf-winuser-tabbedtextouta).</span></span>

 

 
