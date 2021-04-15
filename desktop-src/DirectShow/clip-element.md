---
description: O clipe epecifies uma fonte de mídia.
ms.assetid: 40323e64-ad5f-4646-bad7-2a4e7d0ddcf6
title: Elemento de clipe
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9fe975113f370b13e50ba695d6fb3388a43c3a74
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456443"
---
# <a name="clip-element"></a>Elemento de clipe

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `clip` epecifies uma origem de mídia.

## <a name="attributes"></a>Atributos

[**CLSID**](clsid-attribute.md), [**taxa de quadros**](framerate-attribute.md), [**bloqueio**](lock-attribute.md), [**mLength**](mlength-attribute.md), [**mStart**](mstart-attribute.md), [**mstop**](mstop-attribute.md), [**mudo**](mute-attribute.md), [**src**](src-attribute.md), [**Iniciar**](start-attribute.md), [**parar**](stop-attribute.md), [**transmitir**](stream-attribute.md), [**stretchmode**](stretchmode-attribute.md), [**UserData**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)

## <a name="parentchild-information"></a>Informações de pai/filho



|          |                                  |
|----------|----------------------------------|
| Pai   | [**controles**](track-element.md)   |
| Children | [**funciona**](effect-element.md) |



 

## <a name="remarks"></a>Comentários

O atributo **CLSID** especifica o CLSID de um filtro de origem a ser usado como a origem. Não especifique os atributos **src** e **CLSID** dentro do mesmo `clip` elemento.

Especifique pelo menos um atributo de tempo de início (**Start** ou **mStart**) e um atributo de tempo de parada (**Stop** ou **mstop**). Se um dos atributos de tempo de inicialização não for especificado, o padrão será 0 (o início da linha do tempo para **início** ou o início do clipe para **mStart**). Se um dos atributos de tempo de parada não for especificado, o DES assumirá uma taxa de reprodução normal e calculará a hora de parada não especificada adequadamente. Se ambas as horas de parada forem especificadas, a reprodução será mais rápida ou mais lenta do que o normal, se necessário.

No exemplo a seguir, a duração da linha do tempo é de sete segundos (**parar** menos **Iniciar**). A taxa de reprodução normal é assumida, portanto, o padrão da hora de parada da mídia é de 10 segundos (a duração mais **mStart**).


```
<clip start="2" stop="9" mstart="3" />
```



No próximo exemplo, a hora de início da mídia usa como padrão 0, forçando a duração da mídia a ser de 10 segundos. A duração da linha do tempo é de cinco segundos, portanto, o clipe é reproduzido com duas vezes a taxa normal.


```
<clip start="5" stop="10" mstop="10" />  
```



Se o atributo **src** especificar uma imagem ainda, o des tentará carregar uma série de imagens ainda para criar uma animação. Por exemplo, se o atributo **src** for IMAGE001.BMP, o des procurará IMAGE002.BMP, IMAGE003.BMP, IMAGE004.BMP e assim por diante. Supondo que eles existam, eles são exibidos em ordem numérica sequencial, na taxa especificada pelo atributo de **taxa de quadros** .

## <a name="examples"></a>Exemplos


```XML
<clip src="sample.avi" start="1:05" stop="1:42.5" mstart="30" />
```



## <a name="see-also"></a>Confira também

<dl> <dt>

[Elementos XTL](xtl-elements.md)
</dt> </dl>

 

 



