---
title: Funções de fonte e texto (OpenGL)
description: As funções a seguir podem ser usadas para gerenciar fontes e texto.
ms.assetid: 42e16967-1eeb-4d37-bbd6-33c473eb2757
keywords:
- Funções WGL, texto
- Funções WGL, fonte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1341dab969178a08e43c1af0a32c4cac817072ad2d5315cd051df2c87ac3c3fc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082436"
---
# <a name="font-and-text-functions-opengl"></a>Funções de fonte e texto (OpenGL)

As funções a seguir podem ser usadas para gerenciar fontes e texto.



| Windows Função                                 | Descrição                                                                                                                                                                                                                      |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**wglUseFontBitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa)   | Cria um conjunto de listas de exibição de bitmap de caracteres. Os caracteres vêm da fonte atual de um contexto de dispositivo especificado. Os caracteres são especificados como uma sequência consecutiva no conjunto de glifos da fonte.                                      |
| [**wglUseFontOutlines**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) | Cria um conjunto de listas de exibição, com base nos glifos da fonte de contorno selecionada no momento de um contexto de dispositivo, para uso com o contexto de renderização atual. As listas de exibição são usadas para desenhar caracteres 3D de fontes TrueType. |



 

As **funções wglUseFontBitmaps** e **wglUseFontOutlines** usam um handle para um contexto de dispositivo e usam a fonte atual desse contexto de dispositivo como uma fonte para os bitmaps. Portanto, é necessário definir a fonte do contexto do dispositivo e as propriedades da fonte antes de chamar **wglUseFontBitmaps** ou **wglUseFontOutlines**.

As [**funções wglUseFontBitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa) e [**wglUseFontOutlines**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) também têm um parâmetro que transforma o primeiro glifo na fonte em uma lista de exibição de bitmap e um parâmetro que especifica quantos glifos transformar em listas de exibição. Em seguida, a função cria listas de exibição para a sequência de glifos especificada. Por exemplo:

-   Para criar um conjunto de 224 listas de exibição de bitmap para todos os glifos do conjunto de caracteres Windows, de definir esses dois parâmetros como 32 e 224, respectivamente.
-   Para criar um conjunto de 256 listas de exibição de bitmap para todos os glifos do conjunto de caracteres OEM, de definir esses dois parâmetros como 0 e 256, respectivamente.
-   Para criar uma lista de exibição de bitmap único para qualquer glifo de conjunto de caracteres único, de definido o segundo desses parâmetros como 1.

As **funções wglUseFontBitmaps** e **wglUseFontOutlines** representam um glifo nulo em uma fonte com uma lista de exibição vazia.

As listas de exibição criadas por uma chamada para **wglUseFontBitmaps** ou **wglUseFontOutlines** são numeradas automaticamente consecutivamente.

Depois de chamar a [**função wglUseFontBitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa) ou [**wglUseFontOutlines,**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) chame [**glCallLists**](glcalllists.md) para desenhar uma cadeia de caracteres. Consulte [Desenhando texto em uma Double-Buffered OpenGL para](drawing-text-in-a-double-buffered-opengl-window.md) ver o código de exemplo. Nesse contexto, **glCallLists** usa cada caractere em uma cadeia de caracteres como um índice na matriz de listas de exibição numeradas consecutivamente criadas por **wglUseFontBitmaps** ou **wglUseFontOutlines**.

Quando terminar de desenhar texto, chame a função [**glDeleteLists**](gldeletelists.md) para liberar o conjunto contíguo de listas de exibição criadas por **wglUseFontBitmaps** e **wglUseFontOutlines**.

 

 




