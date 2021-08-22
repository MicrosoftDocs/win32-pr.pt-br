---
title: Renderização de imagem
description: Renderização de imagem
ms.assetid: de87f288-f1bd-471c-b594-e9dbde3cff0a
keywords:
- DrawDib, renderização de imagem
- DrawDib, desenho de DIBs
- Função DrawDibDraw
- Função DrawDibGetBuffer
- Função DrawDibUpdate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e7be73fbe37a28ab44116d2fb2e68acb6a9a3a385603af23dca0e14aa2de4d8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119690746"
---
# <a name="image-rendering"></a>Renderização de imagem

Depois de chamar o [**DrawDibOpen**](/windows/desktop/api/Vfw/nf-vfw-drawdibopen) para criar um controlador de domínio DrawDib (consulte [DrawDib Operations](drawdib-operations.md)), você pode desenhar uma DIB na tela usando a função [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) . **DrawDibDraw** pontilha os bitmaps de cor verdadeira ao exibi-los com adaptadores de vídeo de 8 bits.

O [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) também dá suporte aos compactadores de vídeo de forma transparente ao exibir bitmaps compactados. Você pode acessar o buffer que contém a imagem descompactada usando a função [**DrawDibGetBuffer**](/windows/desktop/api/Vfw/nf-vfw-drawdibgetbuffer) . **DrawDibGetBuffer** retorna **NULL** ao desenhar um bitmap descompactado. Você deve preparar seu aplicativo para manipular bitmaps compactados e descompactados.

Você pode atualizar uma imagem ou uma parte de uma imagem exibida pelo seu aplicativo usando a macro [**DrawDibUpdate**](/windows/desktop/api/Vfw/nf-vfw-drawdibupdate) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre as funções DrawDib](about-the-drawdib-functions.md)
</dt> </dl>

 

 




