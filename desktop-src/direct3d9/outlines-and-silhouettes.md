---
description: Você pode usar o buffer de estêncil para efeitos mais abstratos, como contornos e silhuetas.
ms.assetid: 8b9cd2b3-c1bf-4ac9-aae5-7fc0c9e049ff
title: Contornos e silhuetas (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46a282b650b96cdbb36dc252e1f31cb81d91f0bb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103645658"
---
# <a name="outlines-and-silhouettes-direct3d-9"></a>Contornos e silhuetas (Direct3D 9)

Você pode usar o buffer de estêncil para efeitos mais abstratos, como contornos e silhuetas.

Se seu aplicativo aplicar uma máscara de estêncil à imagem de um objeto primitivo com o mesmo formato, mas um pouco menor, a imagem resultante terá apenas o contorno do objeto primitivo. O app pode preencher a área com máscara de estêncil da imagem com uma cor sólida, dando à primitiva uma aparência em alto-relevo.

Se a máscara de estêncial tiver o mesmo tamanho e formato da primitiva que está sendo renderizado, a imagem resultante terá um buraco onde o primitivo deveria estar. Seu app poderá preencher o buraco com cor preta para produzir uma silhueta da primitiva.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Técnicas de buffer de estêncil](stencil-buffer-techniques.md)
</dt> </dl>

 

 



