---
description: O método SetClipVideoRect amplia a exibição de vídeo para o subrectangle especificado.
ms.assetid: 3940a382-8d53-4ff9-b024-38de1aa00f54
title: Método SetClipVideoRect
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e7741a2604ed1c2896b105295020893e23b447e3fa6f6ab7c53def92aa508c4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078866"
---
# <a name="setclipvideorect-method"></a>Método SetClipVideoRect

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

O `SetClipVideoRect` método amplia a exibição de vídeo para o subrectangle especificado.

``` syntax
MSWebDVD.SetClipVideoRect(oRect)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="oRect"></span><span id="orect"></span><span id="ORECT"></span>*oRect*
</dt> <dd>

Especifica um objeto [DVDRect,](dvdrect-object.md) que contém o retângulo de recorte.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Quando você definir um novo retângulo de recorte, o objeto ampliará essa área para caber nas dimensões de exibição geral do aplicativo. Isso cria o efeito de ampliar em uma área específica da tela. Para especificar o retângulo, crie um novo [objeto DVDRect](dvdrect-object.md) e preencha suas propriedades.

O retângulo mais comum para exibição de vídeo é 720 x 540.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**GetClipVideoRect**](getclipvideorect-method.md)
</dt> </dl>

 

 



