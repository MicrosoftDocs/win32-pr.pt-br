---
title: Direct2D e DPI alto
description: descreve como Direct2D acomoda a exibição de alto DPI.
ms.assetid: 1809ab0e-853f-4dac-be97-563c92b9caee
keywords:
- Direct2D, alto DPI
- DPI alto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec5c48f9a1b3552115ebbec8a54a6878716ef34675e41193ae08fb9cb8e55bc8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117825971"
---
# <a name="direct2d-and-high-dpi"></a>Direct2D e DPI alto

Escrever um aplicativo com reconhecimento de DPI é a chave para tornar uma interface do usuário uma aparência consistente em uma grande variedade de configurações de vídeo de alto DPI. Um aplicativo que não reconhece DPI, mas que está sendo executado em uma configuração de exibição de alto DPI pode ser afetado por vários artefatos visuais, incluindo o dimensionamento incorreto de elementos da interface do usuário, texto recortado e imagens borradas. Ao adicionar suporte em seu aplicativo para reconhecimento de DPI, você torna a apresentação da interface do usuário mais previsível, tornando-a mais visualmente atraente e mais fácil de ler para os usuários. felizmente, Direct2D facilita ainda mais a gravação de aplicativos que funcionam bem em alto DPI. Este tópico inclui as seções a seguir.

-   [Suporte de alto DPI no Direct2D](#high-dpi-support-in-direct2d)
-   [Windows 8 e DPI alto](#windows-8-and-high-dpi)
-   [O que é um DIP?](#what-is-a-dip)
-   [Tópicos relacionados](#related-topics)

## <a name="high-dpi-support-in-direct2d"></a>Suporte de alto DPI no Direct2D

Direct2D fornece os seguintes recursos para trabalhar com cenários de alto DPI:

-   Ele honra automaticamente o DPI do sistema ao criar um destino de renderização em janelas, desde que o manifesto do aplicativo indique que o aplicativo lida com o DPI corretamente. (Para obter informações sobre como declarar que seu aplicativo reconhece DPI, consulte [como garantir que seu aplicativo seja exibido corretamente em monitores de alto dpi](how-to--size-a-window-properly-for-high-dpi-displays.md).)
-   Ele expressa coordenadas em DIPs (pixels independentes de dispositivo), o que permite que o aplicativo seja dimensionado automaticamente quando a configuração de DPI é alterada.
-   Ele permite que os bitmaps tenham um DPI e dimensionam-os corretamente levando o DPI em conta. Esse recurso também pode ser usado para manter ícones em resoluções diferentes.
-   Ele expressa a maioria dos recursos em DIPs, o que torna os recursos automaticamente independentes da resolução.
-   Ele usa um espaço de coordenadas de ponto flutuante e uma suavização, de modo que qualquer conteúdo pode ser dimensionado para qualquer DPI arbitrária.

o pipeline de gráficos de Direct2D é projetado para dimensionar de 96 DPI para 1200DPI.

## <a name="windows-8-and-high-dpi"></a>Windows 8 e DPI alto

a partir do Windows 8, há recursos adicionais para suporte de alto DPI.

se o DPI do contexto do dispositivo for alto o suficiente, Direct2D alterar o limite usado para habilitar a anti-aliasing vertical do texto. Isso resulta em renderização de texto mais rápida em monitores de alto DPI. Além disso, você pode alternar o modo de unidade para pixels em vez de DIPs usando o método [**ID2D1DeviceContext:: Setunitmode**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-setunitmode) . Se você definir o modo de unidade como pixels e o contexto do dispositivo DPI para o DPI da tela, a otimização ainda estará habilitada.

## <a name="what-is-a-dip"></a>O que é um DIP?

Um DIP (pixel independente de dispositivo) é um pixel lógico que mapeia para os pixels do dispositivo físico por meio de um escalar, o DPI. DPI significa pontos por polegada, em que um ponto representa um pixel de dispositivo físico. (O nomenclatura vem da impressão, onde os pontos são o menor ponto de tinta que um processo de impressão pode produzir). Como um monitor padrão costumava ter 96 pontos por polegada, um DPI de 96 significava que um pixel independente de dispositivo (ou DIP) mapeou 1:1 com um pixel físico. Por exemplo, se o DPI fosse 96 \* 2 = 192, um único DIP abrange dois pixels físicos.

Há muitas razões pelas quais os aplicativos não manipulam necessariamente esse dimensionamento corretamente; uma das razões mais simples é que ele requer um trabalho extra para descobrir e usar esse valor escalar durante a renderização. no Direct2D, o dimensionamento é aplicado por padrão. devido a esse mapeamento, os pixels de dispositivo físico podem acabar em coordenadas de DIP fracionários, que é um dos motivos pelos quais Direct2D usa um espaço de coordenadas de ponto flutuante.

<dl> pixel físico = (DIP × DPI)/96  
</dl>

Para converter um pixel físico em um DIP, use esta fórmula:

<dl> DIP = (pixel físico × 96)/DPI  
</dl>

> [!Note]
>
> começando com Windows 8, você pode alternar o modo de unidade para pixels em vez de DIPs usando o método [**ID2D1DeviceContext:: setunitmode**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-setunitmode) .

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Como garantir que seu aplicativo seja exibido corretamente em monitores de alto DPI](how-to--size-a-window-properly-for-high-dpi-displays.md)
</dt> </dl>

 

 