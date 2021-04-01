---
description: O atributo stretchmode especifica como alongar uma imagem que não corresponde às dimensões de saída.
ms.assetid: 9a26bb8b-2b1c-424a-ae30-e175c60c76a1
title: Atributo stretchmode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48a629a34dc1875a7f1d3669e32c53d0e8d3d29c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829372"
---
# <a name="stretchmode-attribute"></a>Atributo stretchmode

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `stretchmode` atributo especifica como alongar uma imagem que não corresponde às dimensões de saída.

## <a name="possible-values"></a>Valores possíveis

Deve ter um dos valores a seguir.

-   "Stretch": a imagem é ampliada para se ajustar ao tamanho do quadro de saída sem preservar a taxa de proporção. (Padrão)
-   "cortar": a imagem é cortada para se ajustar ao tamanho do quadro de saída.
-   "preserveaspectratio": a taxa de proporção original é preservada, com uma Letterbox preta ao longo da dimensão mais curta.
-   "preserveaspectrationoletterbox": a imagem é redimensionada para preencher o quadro de destino inteiro, preservando a taxa de proporção.

## <a name="applies-to"></a>Aplica-se A

[**clip**](clip-element.md)

## <a name="see-also"></a>Confira também

<dl> <dt>

[Atributos XTL](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineSrc:: setalongamode**](iamtimelinesrc-setstretchmode.md)
</dt> </dl>

 

 



