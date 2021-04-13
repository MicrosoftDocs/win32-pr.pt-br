---
title: Funções de fonte e texto (OpenGL)
description: As funções a seguir podem ser usadas para gerenciar fontes e texto.
ms.assetid: 42e16967-1eeb-4d37-bbd6-33c473eb2757
keywords:
- Funções WGL, texto
- Funções do WGL, fonte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e205549346cccc2c44b7670db91530cfbc24017d
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104369120"
---
# <a name="font-and-text-functions-opengl"></a>Funções de fonte e texto (OpenGL)

As funções a seguir podem ser usadas para gerenciar fontes e texto.



| Função do Windows                                 | Descrição                                                                                                                                                                                                                      |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**wglUseFontBitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa)   | Cria um conjunto de listas de exibição de bitmaps de caracteres. Os caracteres são provenientes de uma fonte atual do contexto de dispositivo especificado. Os caracteres são especificados como uma execução consecutiva dentro do conjunto de glifos da fonte.                                      |
| [**wglUseFontOutlines**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) | Cria um conjunto de listas de exibição, com base nos glifos da fonte da estrutura de tópicos selecionada no momento de um contexto de dispositivo, para uso com o contexto de renderização atual. As listas de exibição são usadas para desenhar caracteres de 3-D de fontes TrueType. |



 

As funções **wglUseFontBitmaps** e **wglUseFontOutlines** usam um identificador para um contexto de dispositivo e usam a fonte atual desse contexto de dispositivo como uma fonte para os bitmaps. Portanto, é necessário definir a fonte do contexto do dispositivo e as propriedades da fonte antes de chamar **wglUseFontBitmaps** ou **wglUseFontOutlines**.

As funções [**wglUseFontBitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa) e [**wglUseFontOutlines**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) também usam um parâmetro que transforma o primeiro glifo na fonte em uma lista de exibição de bitmap e um parâmetro que especifica quantos glifos se transforma em listas de exibição. Em seguida, a função cria listas de exibição para a execução consecutiva especificada de glifos. Por exemplo:

-   Para criar um conjunto de listas de exibição de bitmap 224 para todos os glifos do conjunto de caracteres do Windows, defina esses dois parâmetros como 32 e 224, respectivamente.
-   Para criar um conjunto de listas de exibição de bitmap 256 para todos os glifos de conjunto de caracteres OEM, defina esses dois parâmetros como 0 e 256, respectivamente.
-   Para criar uma única lista de exibição de bitmap para qualquer glifo de conjunto de caracteres único, defina o segundo desses parâmetros como 1.

As funções **wglUseFontBitmaps** e **wglUseFontOutlines** representam um glifo nulo em uma fonte com uma lista de exibição vazia.

As listas de exibição criadas por uma chamada para **wglUseFontBitmaps** ou **wglUseFontOutlines** são automaticamente numeradas consecutivamente.

Depois de chamar a função [**wglUseFontBitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa) ou [**WglUseFontOutlines**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) , chame [**glCallLists**](glcalllists.md) para desenhar uma cadeia de caracteres. Consulte [desenho de texto em uma janela Double-Buffered OpenGL](drawing-text-in-a-double-buffered-opengl-window.md) para obter o código de exemplo. Nesse contexto, **glCallLists** usa cada caractere em uma cadeia de caracteres como um índice na matriz de listas de exibição numeradas consecutivamente criadas por **wglUseFontBitmaps** ou **wglUseFontOutlines**.

Quando você terminar de desenhar o texto, chame a função [**glDeleteLists**](gldeletelists.md) para liberar o conjunto contíguo de listas de exibição criadas por **wglUseFontBitmaps** e **wglUseFontOutlines**.

 

 




