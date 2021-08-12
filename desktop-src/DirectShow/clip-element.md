---
description: O clipe verifica uma fonte de mídia.
ms.assetid: 40323e64-ad5f-4646-bad7-2a4e7d0ddcf6
title: Elemento clip
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b94ffdbd3d9b49d961cdefdd64de9a212858c5da4859c3beddb77db0ab732d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118655510"
---
# <a name="clip-element"></a>Elemento clip

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `clip` eifica uma fonte de mídia.

## <a name="attributes"></a>Atributos

[**clsid**](clsid-attribute.md), [**framerate**](framerate-attribute.md), [**lock**](lock-attribute.md), [**mlength**](mlength-attribute.md), [**mstart**](mstart-attribute.md), [**mstop**](mstop-attribute.md), [**mute**](mute-attribute.md), [**src**](src-attribute.md), [**start**](start-attribute.md), [**stop**](stop-attribute.md), [**stream**](stream-attribute.md), [**stretchmode**](stretchmode-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)

## <a name="parentchild-information"></a>Informações pai/filho



| Rótulo | Valor |
|----------|----------------------------------|
| Pai   | [**Faixa**](track-element.md)   |
| Children | [**Efeito**](effect-element.md) |



 

## <a name="remarks"></a>Comentários

O **atributo clsid** especifica o CLSID de um filtro de origem a ser usado como a origem. Não especifique os **atributos src** e **clsid** dentro do mesmo `clip` elemento.

Especifique pelo menos um atributo de hora de início (**start** ou **mstart**) e um atributo de tempo de parada (**stop** ou **mstop**). Se um dos atributos de hora de início não for especificado, o padrão será 0 (o início da linha do tempo para iniciar ou o início do clipe para **mstart**). Se um dos atributos de tempo de parada não for especificado, o DES assumirá uma taxa de reprodução normal e calculará o tempo de parada não especificado de acordo. Se ambos os horários de parada são especificados, a reprodução é mais rápida ou mais lenta do que o normal, se necessário.

No exemplo a seguir, a duração da linha do tempo é de sete segundos (**parar menos** **iniciar**). A taxa de reprodução normal é assumida, portanto, o tempo de parada de mídia assume como padrão 10 segundos (a duração mais **mstart**).


```
<clip start="2" stop="9" mstart="3" />
```



No próximo exemplo, a hora de início da mídia assume como padrão 0, forçando a duração da mídia a ser de 10 segundos. A duração da linha do tempo é de cinco segundos, portanto, o clipe é reproduzindo duas vezes a taxa normal.


```
<clip start="5" stop="10" mstop="10" />  
```



Se o **atributo src** especificar uma imagem still, o DES tentará carregar uma série de imagens ainda para criar uma animação. Por exemplo, se o **atributo src** for IMAGE001.BMP, o DES procura IMAGE002.BMP, IMAGE003.BMP, IMAGE004.BMP e assim por diante. Supondo que existam, eles são exibidos em ordem numérica sequencial, na taxa especificada pelo atributo **framerate.**

## <a name="examples"></a>Exemplos


```XML
<clip src="sample.avi" start="1:05" stop="1:42.5" mstart="30" />
```



## <a name="see-also"></a>Confira também

<dl> <dt>

[Elementos XTL](xtl-elements.md)
</dt> </dl>

 

 



