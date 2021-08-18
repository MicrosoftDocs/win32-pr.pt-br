---
description: A suavização Microsoft ClearType é um método de suavização que melhora a resolução de exibição de fonte em relação à suavização tradicional.
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

A suavização Microsoft ClearType é um método de suavização que melhora a resolução de exibição de fonte em relação à suavização tradicional. Ele melhora drasticamente a capacidade de leitura em monitores de COLOR LCD com uma interface digital, como aqueles em laptops e telas de área de trabalho simples de alta qualidade. A capacidade de leitura em telas CRT também é um pouco aprimorada.

No entanto, ClearType depende da orientação e da ordenação das faixas de LCD. Atualmente, ClearType é implementado somente para LCDs com faixas verticais ordenadas RGB. Em particular, isso afeta os PCs de tablet, em que a exibição pode ser orientada em qualquer direção e as telas que podem ser transformadas de paisagem em retrato.

A antialiação ClearType é permitida:

-   Para cores de 16, 24 e 32 bits (desabilitada para 256 cores ou menos)
-   Para DC de tela e DC de memória (não para DC de impressora)
-   Para fontes TrueType e fontes OpenType com contornos trueType

A antialiação ClearType está desabilitada:

-   No cliente do servidor terminal
-   Para fontes de bitmap, fontes de vetor, fontes de dispositivo, fontes do tipo 1 ou fontes OpenType postscript sem contornos de TrueType
-   Se a fonte tiver ajustado bitmaps inseridos, somente para os tamanhos de fonte que contêm os bitmaps inseridos

Para ativar a suavização ClearType, chame [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) uma vez para ativar a suavização de fonte e, em seguida, uma segunda vez para definir o tipo de suavização como \_ FONTSMOO SMOOTHCLEARTYPE, conforme mostrado no exemplo de código a seguir:


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



Você pode ajustar a aparência do texto alterando o valor de contraste usado no algoritmo ClearType. O padrão é 1.400, mas pode ser qualquer valor de 1.000 a 2.200. Dependendo do dispositivo de exibição e da sensibilidade do usuário às cores, um valor de contraste maior ou menor pode melhorar a capacidade de leitura. Para alterar o contraste, chame [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) com SPI \_ SETFONTSMOOTHINGCONTRAST. O código a seguir define o valor de contraste como 1.600.


```C++
SystemParametersInfo(SPI_SETFONTSMOOTHINGCONTRAST,
                     0,
                     (PVOID)1600,
                     SPIF_UPDATEINIFILE | SPIF_SENDCHANGE); 
```



Você deve considerar os seguintes detalhes para compatibilidade do aplicativo:

-   A renderização de texto com ClearType é um pouco mais lenta do que com a antialização padrão.
-   Os aplicativos não devem usar XOR para exibir o texto selecionado. Os aplicativos devem definir a cor da tela de fundo e repetir o texto selecionado.
-   Os aplicativos não devem pintar o mesmo texto sobre si mesmo no modo transparente. Se isso ocorrer, os pixels de borda que são anticiados serão mesclados por cores em vez de com a cor da tela de fundo. Isso resulta em bordas escuradas e coloridas.
-   Os aplicativos não devem pintar texto pintando os caracteres individualmente quando estão no modo opaco porque a borda de um caractere pode ser recortada pelo caractere a seguir. Isso ocorre porque um caractere suavizado com ClearType pode ter uma largura A ou C negativa em que o caractere regular tem uma largura positiva A ou C. Apenas a largura B do caractere tem a garantia de ser a mesma. Da mesma forma, os aplicativos devem ter cuidado se o texto suavizado estiver ao lado do texto não escrito.
-   Se um aplicativo renderizar texto e manipular o bitmap, a suavização de fonte deverá ser desligada definindo o membro **lfQuality** da estrutura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) como NONANTIALIASED \_ QUALITY. Por exemplo, um jogo pode adicionar um efeito de sombra de bitmap ou o texto renderizado em um bitmap pode ser dimensionado para produzir uma visualização digital.
-   Se o usuário estiver executando no modo retrato (ou seja, a faixa de monitoramento estiver horizontal), a antialização ClearType deverá ser desabilitada.

O *parâmetro fdwQuality* em [**CreateFont**](/windows/desktop/api/Wingdi/nf-wingdi-createfonta) e o membro **lfQuality** de [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) aceitam o sinalizador CLEARTYPE \_ QUALITY. A rasterização de fontes criadas com esse sinalizador usará o rasterizador ClearType. Esse sinalizador não tem efeito sobre versões anteriores do sistema operacional.

 

 
