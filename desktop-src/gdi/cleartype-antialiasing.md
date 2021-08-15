---
description: A suavização do Microsoft ClearType é um método de suavização que melhora a resolução da exibição da fonte sobre o anti-aliasing tradicional.
ms.assetid: b9896934-1e4f-4ae1-922a-ef30e0edf94f
title: Suavização de ClearType
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcc8444c1e1b594559f9c5b7f96529a0db00b20c6a10e560bc1dcb4574e079d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117888089"
---
# <a name="cleartype-antialiasing"></a>Suavização de ClearType

A suavização do Microsoft ClearType é um método de suavização que melhora a resolução da exibição da fonte sobre o anti-aliasing tradicional. Ele melhora drasticamente a legibilidade em monitores de LCD de cores com uma interface digital, como aquelas em laptops e monitores de área de trabalho plana de alta qualidade. A legibilidade em telas CRT também é um pouco melhor.

No entanto, o ClearType depende da orientação e da ordenação das faixas do LCD. Atualmente, o ClearType é implementado somente para LCDs com faixas verticais que são ordenadas como RGB. Em particular, isso afeta Tablet PCs, em que a exibição pode ser orientada em qualquer direção e as telas que podem ser transformadas de paisagem para retrato.

A suavização de ClearType é permitida:

-   Para a cor de 16, 24 e 32 bits (desabilitada para 256 cores ou menos)
-   Para o DC de tela e o DC de memória (não para o DC de impressora)
-   Para fontes TrueType e fontes OpenType com contornos TrueType

A suavização de ClearType está desabilitada:

-   Em cliente do Terminal Server
-   Para fontes de bitmap, fontes de vetor, fontes de dispositivo, fontes do tipo 1 ou fontes do PostScript OpenType sem contornos TrueType
-   Se a fonte ajustou bitmaps inseridos, somente para os tamanhos de fonte que contêm os bitmaps inseridos

Para ativar a suavização de ClearType, chame [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) uma vez para ativar a suavização de fontes e, em seguida, uma segunda vez para definir o tipo de suavização como Fe \_ FONTSMOOTHINGCLEARTYPE, conforme mostrado no exemplo de código a seguir:


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



Você pode ajustar a aparência do texto alterando o valor de contraste usado no algoritmo ClearType. O padrão é 1.400, mas pode ser qualquer valor de 1.000 a 2.200. Dependendo do dispositivo de vídeo e da sensibilidade do usuário às cores, um valor de contraste maior ou menor pode melhorar a legibilidade. Para alterar o contraste, chame [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) com SPI \_ SETFONTSMOOTHINGCONTRAST. O código a seguir define o valor de contraste como 1.600.


```C++
SystemParametersInfo(SPI_SETFONTSMOOTHINGCONTRAST,
                     0,
                     (PVOID)1600,
                     SPIF_UPDATEINIFILE | SPIF_SENDCHANGE); 
```



Você deve considerar os seguintes detalhes para a compatibilidade de aplicativos:

-   A renderização de texto com ClearType é um pouco mais lenta do que com a anti-aliasing padrão.
-   Os aplicativos não devem usar XOR para exibir o texto selecionado. Os aplicativos devem definir a cor da tela de fundo e exibir novamente o texto selecionado.
-   Os aplicativos não devem pintar o mesmo texto por cima dele no modo transparente. Se isso ocorrer, os pixels de borda com suavização de cor terão a mesclagem colorida, em vez de com a cor do plano de fundo. Isso resulta em bordas mais escurecidas e coloridas.
-   Os aplicativos não devem pintar o texto pintando os caracteres individualmente no modo opaco porque a borda de um caractere pode ser recortada pelo caractere a seguir. Isso ocorre porque um caractere que é suavizado com ClearType pode ter uma largura negativa a ou C, em que o caractere regular tem uma largura de A ou C positiva. Somente a largura B do caractere é garantida como sendo a mesma. Da mesma forma, os aplicativos devem ter cuidado se o texto suave estiver ao lado de um texto não suavizado.
-   Se um aplicativo renderiza texto e, em seguida, manipula o bitmap, a suavização de fontes deve ser desativada definindo o membro **lfQuality** da estrutura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) como NONANTIALIASED \_ Quality. Por exemplo, um jogo pode adicionar um efeito de sombra de bitmap ou o texto renderizado em um bitmap pode ser dimensionado para produzir um ThumbView.
-   Se o usuário estiver executando no modo retrato (ou seja, a distribuição do monitor é horizontal), a suavização de ClearType deve ser desabilitada.

O parâmetro *fdwQuality* em [**CreateFont**](/windows/desktop/api/Wingdi/nf-wingdi-createfonta) e o membro **lfQuality** de [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) aceitam o \_ sinalizador de qualidade ClearType. A rasterização das fontes criadas com esse sinalizador usará o rasterizador ClearType. Esse sinalizador não tem nenhum efeito nas versões anteriores do sistema operacional.

 

 
