---
description: O atributo stretchmode especifica como alongar uma imagem que não corresponder às dimensões de saída.
ms.assetid: 9a26bb8b-2b1c-424a-ae30-e175c60c76a1
title: Atributo stretchmode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed398fbe193ef262bdfc9a28cf66bef3a5b11f759d90c460cc99342ec7cd66b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903866"
---
# <a name="stretchmode-attribute"></a>Atributo stretchmode

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `stretchmode` atributo especifica como alongar uma imagem que não corresponder às dimensões de saída.

## <a name="possible-values"></a>Valores possíveis

Deve ter um dos valores a seguir.

-   "stretch": a imagem é alongada para se ajustar ao tamanho do quadro de saída sem preservar a taxa de proporção. (Padrão)
-   "crop": a imagem é cortada para se ajustar ao tamanho do quadro de saída.
-   "preserveaspectratio": a taxa de proporção original é preservada, com uma caixa de letras preta ao longo da dimensão mais curta.
-   "preserveaspectrationoletterbox": a imagem é ressada para preencher todo o quadro de destino, preservando a taxa de proporção.

## <a name="applies-to"></a>Aplica-se A

[**clip**](clip-element.md)

## <a name="see-also"></a>Confira também

<dl> <dt>

[Atributos XTL](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineSrc::SetStretchMode**](iamtimelinesrc-setstretchmode.md)
</dt> </dl>

 

 



