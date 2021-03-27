---
description: A suavização do Microsoft ClearType é um método de suavização que melhora a resolução da exibição da fonte sobre o anti-aliasing tradicional.
ms.assetid: b9896934-1e4f-4ae1-922a-ef30e0edf94f
title: Suavização de ClearType
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffbe7ae1a6c99fcee826c576b7671aea6e9ce6c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967706"
---
# <a name="cleartype-antialiasing"></a><span data-ttu-id="72c65-103">Suavização de ClearType</span><span class="sxs-lookup"><span data-stu-id="72c65-103">ClearType Antialiasing</span></span>

<span data-ttu-id="72c65-104">A suavização do Microsoft ClearType é um método de suavização que melhora a resolução da exibição da fonte sobre o anti-aliasing tradicional.</span><span class="sxs-lookup"><span data-stu-id="72c65-104">Microsoft ClearType antialiasing is a smoothing method that improves font display resolution over traditional antialiasing.</span></span> <span data-ttu-id="72c65-105">Ele melhora drasticamente a legibilidade em monitores de LCD de cores com uma interface digital, como aquelas em laptops e monitores de área de trabalho plana de alta qualidade.</span><span class="sxs-lookup"><span data-stu-id="72c65-105">It dramatically improves readability on color LCD monitors with a digital interface, such as those in laptops and high-quality flat desktop displays.</span></span> <span data-ttu-id="72c65-106">A legibilidade em telas CRT também é um pouco melhor.</span><span class="sxs-lookup"><span data-stu-id="72c65-106">Readability on CRT screens is also somewhat improved.</span></span>

<span data-ttu-id="72c65-107">No entanto, o ClearType depende da orientação e da ordenação das faixas do LCD.</span><span class="sxs-lookup"><span data-stu-id="72c65-107">However, ClearType is dependent on the orientation and ordering of the LCD stripes.</span></span> <span data-ttu-id="72c65-108">Atualmente, o ClearType é implementado somente para LCDs com faixas verticais que são ordenadas como RGB.</span><span class="sxs-lookup"><span data-stu-id="72c65-108">Currently, ClearType is implemented only for LCDs with vertical stripes that are ordered RGB.</span></span> <span data-ttu-id="72c65-109">Em particular, isso afeta Tablet PCs, em que a exibição pode ser orientada em qualquer direção e as telas que podem ser transformadas de paisagem para retrato.</span><span class="sxs-lookup"><span data-stu-id="72c65-109">In particular, this affects tablet PCs, where the display can be oriented in any direction, and those screens that can be turned from landscape to portrait.</span></span>

<span data-ttu-id="72c65-110">A suavização de ClearType é permitida:</span><span class="sxs-lookup"><span data-stu-id="72c65-110">ClearType antialiasing is allowed:</span></span>

-   <span data-ttu-id="72c65-111">Para a cor de 16, 24 e 32 bits (desabilitada para 256 cores ou menos)</span><span class="sxs-lookup"><span data-stu-id="72c65-111">For 16-, 24-, and 32-bit color (disabled for 256 colors or less)</span></span>
-   <span data-ttu-id="72c65-112">Para o DC de tela e o DC de memória (não para o DC de impressora)</span><span class="sxs-lookup"><span data-stu-id="72c65-112">For screen DC and memory DC (not for printer DC)</span></span>
-   <span data-ttu-id="72c65-113">Para fontes TrueType e fontes OpenType com contornos TrueType</span><span class="sxs-lookup"><span data-stu-id="72c65-113">For TrueType fonts and OpenType fonts with TrueType outlines</span></span>

<span data-ttu-id="72c65-114">A suavização de ClearType está desabilitada:</span><span class="sxs-lookup"><span data-stu-id="72c65-114">ClearType antialiasing is disabled:</span></span>

-   <span data-ttu-id="72c65-115">Em cliente do Terminal Server</span><span class="sxs-lookup"><span data-stu-id="72c65-115">Under terminal server client</span></span>
-   <span data-ttu-id="72c65-116">Para fontes de bitmap, fontes de vetor, fontes de dispositivo, fontes do tipo 1 ou fontes do PostScript OpenType sem contornos TrueType</span><span class="sxs-lookup"><span data-stu-id="72c65-116">For bitmap fonts, vector fonts, device fonts, Type 1 fonts, or Postscript OpenType fonts without TrueType outlines</span></span>
-   <span data-ttu-id="72c65-117">Se a fonte ajustou bitmaps inseridos, somente para os tamanhos de fonte que contêm os bitmaps inseridos</span><span class="sxs-lookup"><span data-stu-id="72c65-117">If the font has tuned embedded bitmaps, only for those font sizes that contain the embedded bitmaps</span></span>

<span data-ttu-id="72c65-118">Para ativar a suavização de ClearType, chame [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) uma vez para ativar a suavização de fontes e, em seguida, uma segunda vez para definir o tipo de suavização como Fe \_ FONTSMOOTHINGCLEARTYPE, conforme mostrado no exemplo de código a seguir:</span><span class="sxs-lookup"><span data-stu-id="72c65-118">To activate ClearType antialiasing, call [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) once to turn on font smoothing and then a second time to set the smoothing type to FE\_FONTSMOOTHINGCLEARTYPE, as shown in the following code sample:</span></span>


```C++
SystemParametersInfo(SPI_SETFONTSMOOTHING,
                     TRUE,
                     0,
                     SPIF_UPDATEINIFILE | SPIF_SENDCHANGE);
SystemParametersInfo(SPI_SETFONTSMOOTHINGTYPE,
                     0,
                     (PVOID)FE_FONTSMOOTHINGCLEARTYPE,
                     SPIF_UPDATEINIFILE | SPIF_SENDCHANGE); 
```



<span data-ttu-id="72c65-119">Você pode ajustar a aparência do texto alterando o valor de contraste usado no algoritmo ClearType.</span><span class="sxs-lookup"><span data-stu-id="72c65-119">You can adjust the appearance of text by changing the contrast value used in the ClearType algorithm.</span></span> <span data-ttu-id="72c65-120">O padrão é 1.400, mas pode ser qualquer valor de 1.000 a 2.200.</span><span class="sxs-lookup"><span data-stu-id="72c65-120">The default is 1,400, but it can be any value from 1,000 to 2,200.</span></span> <span data-ttu-id="72c65-121">Dependendo do dispositivo de vídeo e da sensibilidade do usuário às cores, um valor de contraste maior ou menor pode melhorar a legibilidade.</span><span class="sxs-lookup"><span data-stu-id="72c65-121">Depending on the display device and the user's sensitivity to colors, a higher or lower contrast value may improve readability.</span></span> <span data-ttu-id="72c65-122">Para alterar o contraste, chame [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) com SPI \_ SETFONTSMOOTHINGCONTRAST.</span><span class="sxs-lookup"><span data-stu-id="72c65-122">To change the contrast, call [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) with SPI\_SETFONTSMOOTHINGCONTRAST.</span></span> <span data-ttu-id="72c65-123">O código a seguir define o valor de contraste como 1.600.</span><span class="sxs-lookup"><span data-stu-id="72c65-123">The following code sets the contrast value to 1,600.</span></span>


```C++
SystemParametersInfo(SPI_SETFONTSMOOTHINGCONTRAST,
                     0,
                     (PVOID)1600,
                     SPIF_UPDATEINIFILE | SPIF_SENDCHANGE); 
```



<span data-ttu-id="72c65-124">Você deve considerar os seguintes detalhes para a compatibilidade de aplicativos:</span><span class="sxs-lookup"><span data-stu-id="72c65-124">You should consider the following details for application compatibility:</span></span>

-   <span data-ttu-id="72c65-125">A renderização de texto com ClearType é um pouco mais lenta do que com a anti-aliasing padrão.</span><span class="sxs-lookup"><span data-stu-id="72c65-125">Text rendering with ClearType is slightly slower than with standard antialiasing.</span></span>
-   <span data-ttu-id="72c65-126">Os aplicativos não devem usar XOR para exibir o texto selecionado.</span><span class="sxs-lookup"><span data-stu-id="72c65-126">Applications should not use XOR to display selected text.</span></span> <span data-ttu-id="72c65-127">Os aplicativos devem definir a cor da tela de fundo e exibir novamente o texto selecionado.</span><span class="sxs-lookup"><span data-stu-id="72c65-127">Applications should set the background color and redisplay the selected text.</span></span>
-   <span data-ttu-id="72c65-128">Os aplicativos não devem pintar o mesmo texto por cima dele no modo transparente.</span><span class="sxs-lookup"><span data-stu-id="72c65-128">Applications should not paint the same text on top of itself in transparent mode.</span></span> <span data-ttu-id="72c65-129">Se isso ocorrer, os pixels de borda com suavização de cor terão a mesclagem colorida, em vez de com a cor do plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="72c65-129">If this occurs, the edge pixels that are antialiased will color merge with themselves instead of with the background color.</span></span> <span data-ttu-id="72c65-130">Isso resulta em bordas mais escurecidas e coloridas.</span><span class="sxs-lookup"><span data-stu-id="72c65-130">This results in darkened and colorful edges.</span></span>
-   <span data-ttu-id="72c65-131">Os aplicativos não devem pintar o texto pintando os caracteres individualmente no modo opaco porque a borda de um caractere pode ser recortada pelo caractere a seguir.</span><span class="sxs-lookup"><span data-stu-id="72c65-131">Applications should not paint text by painting the characters individually when in opaque mode because the edge of a character may be clipped by the following character.</span></span> <span data-ttu-id="72c65-132">Isso ocorre porque um caractere que é suavizado com ClearType pode ter uma largura negativa a ou C, em que o caractere regular tem uma largura de A ou C positiva.</span><span class="sxs-lookup"><span data-stu-id="72c65-132">This occurs because a character that is smoothed with ClearType may have a negative A or C width where the regular character has a positive A or C width.</span></span> <span data-ttu-id="72c65-133">Somente a largura B do caractere é garantida como sendo a mesma.</span><span class="sxs-lookup"><span data-stu-id="72c65-133">Only the B width of the character is guaranteed to be the same.</span></span> <span data-ttu-id="72c65-134">Da mesma forma, os aplicativos devem ter cuidado se o texto suave estiver ao lado de um texto não suavizado.</span><span class="sxs-lookup"><span data-stu-id="72c65-134">Likewise, applications should be careful if smoothed text is next to unsmoothed text.</span></span>
-   <span data-ttu-id="72c65-135">Se um aplicativo renderiza texto e, em seguida, manipula o bitmap, a suavização de fontes deve ser desativada definindo o membro **lfQuality** da estrutura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) como NONANTIALIASED \_ Quality.</span><span class="sxs-lookup"><span data-stu-id="72c65-135">If an application renders text and then manipulates the bitmap, font smoothing should be turned off by setting the **lfQuality** member of the [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure to NONANTIALIASED\_QUALITY.</span></span> <span data-ttu-id="72c65-136">Por exemplo, um jogo pode adicionar um efeito de sombra de bitmap ou o texto renderizado em um bitmap pode ser dimensionado para produzir um ThumbView.</span><span class="sxs-lookup"><span data-stu-id="72c65-136">For example, a game may add a bitmap shadow effect, or text rendered into a bitmap may be scaled to produce a thumbview.</span></span>
-   <span data-ttu-id="72c65-137">Se o usuário estiver executando no modo retrato (ou seja, a distribuição do monitor é horizontal), a suavização de ClearType deve ser desabilitada.</span><span class="sxs-lookup"><span data-stu-id="72c65-137">If the user is running in portrait mode (that is, monitor striping is horizontal) ClearType antialiasing should be disabled.</span></span>

<span data-ttu-id="72c65-138">O parâmetro *fdwQuality* em [**CreateFont**](/windows/desktop/api/Wingdi/nf-wingdi-createfonta) e o membro **lfQuality** de [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) aceitam o \_ sinalizador de qualidade ClearType.</span><span class="sxs-lookup"><span data-stu-id="72c65-138">The *fdwQuality* parameter in [**CreateFont**](/windows/desktop/api/Wingdi/nf-wingdi-createfonta) and the **lfQuality** member of [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) accept the CLEARTYPE\_QUALITY flag.</span></span> <span data-ttu-id="72c65-139">A rasterização das fontes criadas com esse sinalizador usará o rasterizador ClearType.</span><span class="sxs-lookup"><span data-stu-id="72c65-139">Rasterization of fonts created with this flag will use the ClearType rasterizer.</span></span> <span data-ttu-id="72c65-140">Esse sinalizador não tem nenhum efeito nas versões anteriores do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="72c65-140">This flag has no effect on previous versions of the operating system.</span></span>

 

 
