---
description: O método Zoom amplia a exibição de vídeo para dentro ou para fora, centralizado em um determinado conjunto de coordenadas de tela.
ms.assetid: 050f1264-8fbe-4322-970c-184275d5b219
title: Método de zoom
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2625e6c4facf006a0d904e49068853720e20c29e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104461289"
---
# <a name="zoom-method"></a>Método de zoom

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

O `Zoom` método amplia a exibição de vídeo para dentro ou para fora, centralizado em um determinado conjunto de coordenadas de tela.

``` syntax
MSWebDVD.Zoom(iXPos, iYPos, iZoomRatio)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="iXPos"></span><span id="ixpos"></span><span id="IXPOS"></span>*iXPos*
</dt> <dd>

Especifica a coordenada x no centro da área de zoom retangular como um inteiro.

</dd> <dt>

<span id="iYPos"></span><span id="iypos"></span><span id="IYPOS"></span>*iYPos*
</dt> <dd>

Especifica a coordenada y no centro do retângulo a ser ampliado como um inteiro.

</dd> <dt>

<span id="iZoomRatio"></span><span id="izoomratio"></span><span id="IZOOMRATIO"></span>*iZoomRatio*
</dt> <dd>

Especifica o fator de ampliação aplicado ao valor de zoom atual como um inteiro. O valor máximo total depende do que a sobreposição de hardware pode dar suporte; Normalmente, isso é um fator de 32 a 64 vezes o tamanho original.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

A nova taxa de zoom permanecerá em vigor até que seja restaurada ao tamanho original ou alterada novamente. Em outras palavras, duas chamadas para esse método especificando um *iZoomRatio* de dois resultarão em uma taxa de zoom quatro vezes maior do que o tamanho original do vídeo. Se o usuário tentar aplicar zoom além do que o hardware pode dar suporte, esse método terá sucesso, mas não fará nada.

O método [**SetClipVideoRect**](setclipvideorect-method.md) é outra maneira de ampliar; a única diferença entre os dois métodos é a maneira como o retângulo de zoom é especificado.

 

 



