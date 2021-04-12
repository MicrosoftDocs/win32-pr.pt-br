---
title: Fontes e texto (OpenGL)
description: A implementação da Microsoft do OpenGL no Windows dá suporte a gráficos GDI em uma janela OpenGL de buffer único.
ms.assetid: 25a45e1a-6c1e-416b-8993-daeefc1100f3
keywords:
- OpenGL no Windows, fontes
- OpenGL no Windows, texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6fba4ffe996bd88a6285f615ddacb31e57fc311
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104369119"
---
# <a name="fonts-and-text-opengl"></a>Fontes e texto (OpenGL)

A implementação da Microsoft do OpenGL no Windows dá suporte a gráficos GDI em uma janela OpenGL de buffer único. Ele não dá suporte a elementos gráficos GDI em uma janela OpenGL com buffer duplo. Portanto, você pode chamar apenas as funções de fonte e texto do GDI padrão para desenhar texto em uma janela OpenGL com buffer único; Você não pode chamar essas funções para desenhar texto em uma janela OpenGL com buffer duplo.

Há uma solução alternativa para essa restrição no texto em janelas com buffer duplo: criar listas de exibição OpenGL para imagens de bitmap de caracteres e, em seguida, executar essas listas de exibição para desenhar caracteres. Há três etapas principais neste processo:

1.  Selecione uma fonte para um contexto de dispositivo, definindo as propriedades da fonte conforme desejado.
2.  Crie um conjunto de listas de exibição de bitmap com base nos glifos na fonte do contexto do dispositivo, uma lista de exibição para cada glifo que o aplicativo irá desenhar.
3.  Desenhe cada glifo em uma cadeia de caracteres, usando essas listas de exibição de bitmap.

Para criar as listas de exibição, chame as funções [**wglUseFontBitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa) e [**wglUseFontOutlines**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) . Para desenhar caracteres em uma seqüência de caracteres usando as listas de exibição, chame [**glCallLists**](glcalllists.md).

Para criar aplicativos que são fáceis de localizar e que usam recursos com moderação, a criação e o armazenamento dessas listas de exibição de imagem de glifo devem ser gerenciados com cuidado. Muitas linguagens, ao contrário do inglês, têm alfabetos cujos códigos de caractere variam em um conjunto de valores relativamente grande.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Funções de fonte e texto](font-and-text-functions.md)
</dt> </dl>

 

 




