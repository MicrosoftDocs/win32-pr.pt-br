---
title: Fontes e texto (OpenGL)
description: A implementação da Microsoft do OpenGL no Windows dá suporte a gráficos GDI em uma janela OpenGL em buffer único.
ms.assetid: 25a45e1a-6c1e-416b-8993-daeefc1100f3
keywords:
- OpenGL em Windows,fontes
- OpenGL no Windows,texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 966298b6a8d8e5584e761570205a5d3e7be58be3a8dfeb488db2a6f523fc9a25
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082426"
---
# <a name="fonts-and-text-opengl"></a>Fontes e texto (OpenGL)

A implementação da Microsoft do OpenGL no Windows dá suporte a gráficos GDI em uma janela OpenGL em buffer único. Ele não dá suporte a gráficos GDI em uma janela OpenGL com buffer duplo. Portanto, você pode chamar apenas as funções de texto e fonte GDI padrão para desenhar texto em uma janela OpenGL com buffer único; você não pode chamar essas funções para desenhar texto em uma janela OpenGL com buffer duplo.

Há uma solução alternativa para essa restrição no texto em janelas com buffer duplo: crie listas de exibição openGL para imagens de bitmap de caracteres e execute essas listas de exibição para desenhar caracteres. Há três etapas principais nesse processo:

1.  Selecione uma fonte para um contexto de dispositivo, definindo as propriedades da fonte conforme desejado.
2.  Crie um conjunto de listas de exibição de bitmap com base nos glifos na fonte do contexto do dispositivo, uma lista de exibição para cada glifo que o aplicativo desenhará.
3.  Desenhar cada glifo em uma cadeia de caracteres usando essas listas de exibição de bitmap.

Para criar as listas de exibição, chame as funções [**wglUseFontBitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa) e [**wglUseFontOutlines.**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) Para desenhar caracteres em uma cadeia de caracteres usando essas listas de exibição, [**chame glCallLists**](glcalllists.md).

Para criar aplicativos fáceis de serem localizados e que usam recursos com moderação, a criação e o armazenamento dessas listas de exibição de imagem de glifo devem ser gerenciados com cuidado. Muitos idiomas, ao contrário do inglês, têm alfabetos cujos códigos de caractere variam em um conjunto relativamente grande de valores.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Funções de fonte e texto](font-and-text-functions.md)
</dt> </dl>

 

 




