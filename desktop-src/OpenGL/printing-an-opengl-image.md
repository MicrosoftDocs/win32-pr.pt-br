---
title: Imprimindo uma imagem OpenGL
description: Você pode imprimir imagens OpenGL renderizadas em metaarquivos avançados.
ms.assetid: 6099cbe2-82f9-46ec-a3ca-74486c111639
keywords:
- OpenGL no Windows, imprimindo
- Imprimindo imagens OpenGL OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ca0c5260a084796915a7564f793f0e252b5228c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105749230"
---
# <a name="printing-an-opengl-image"></a>Imprimindo uma imagem OpenGL

Você pode imprimir imagens OpenGL renderizadas em metaarquivos avançados. Quando você renderiza para um dispositivo de impressora (HDC), ele deve ser apoiado por um spooler de metarquivo. O OpenGL usa memória para profundidade, cor e outros buffers para armazenar a saída de gráficos em uma impressora. Como a resolução de impressora típica requer uma quantidade significativa de memória para armazenar a saída de gráficos, a impressão de uma imagem OpenGL pode exigir mais memória do que está disponível no sistema. Para superar essa limitação, a implementação atual do OpenGL imprime gráficos OpenGL em bandas. No entanto, isso aumenta o tempo necessário para imprimir imagens OpenGL.

Antes de imprimir uma imagem OpenGL, você deve chamar a função [StartDoc](/windows/desktop/api/wingdi/nf-wingdi-startdoca) para concluir a inicialização de um DC (contexto de dispositivo de impressora). Depois de chamar **StartDoc**, você pode criar contextos de RENDERIZAÇÃO (HGLRC) para renderizar para o dispositivo de impressora. Se você criar contextos de renderização antes de chamar **StartDoc**, não será possível determinar se um metarquivo está no spool.

O exemplo de código a seguir mostra como imprimir uma imagem OpenGL:

``` syntax
HDC            hDC;
DOCINFO        di;
HGLRC          hglrc;

// Call StartDoc to start the document 
StartDoc( hDC, &di );

// Prepare the printer driver to accept data 
StartPage(hDC);

// Create a rendering context using the metafile DC 
hglrc = wglCreateContext ( hDCmetafile );

// Do OpenGL rendering operations here 
    . . .
wglMakeCurrent(NULL, NULL); // Get rid of rendering context 
    . . .
EndPage(hDC); // Finish writing to the page 
EndDoc(hDC); // End the print job
```

Para obter mais informações sobre como usar [metarquivos, consulte Enhanced Metafile Operations](/windows/desktop/gdi/enhanced-metafile-operations).

 

 