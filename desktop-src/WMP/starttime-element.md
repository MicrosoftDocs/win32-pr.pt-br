---
title: Elemento STARTtime
description: O elemento STARTtime define um índice de tempo do qual o Windows Media Player começará a renderizar o fluxo.
ms.assetid: 9b0199c8-5c95-4b4e-a943-e3bd037bf0bc
keywords:
- Elemento STARTtime Windows Media Player
topic_type:
- apiref
api_name:
- STARTTIME Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8a882da6c07ec76a94c8e214fe1da11c71680b0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105763788"
---
# <a name="starttime-element"></a>Elemento STARTtime

O elemento **StartTime** define um índice de tempo do qual o Windows Media Player começará a renderizar o fluxo.

``` syntax
<STARTTIME
   VALUE = "hh:mm:ss.fract"
/>
```

## <a name="attributes"></a>Atributos

**Valor** (obrigatório)

O índice de tempo (em horas, minutos, segundos e centésimos de segundo) do qual o Windows Media Player começa a reproduzir um fluxo definido no elemento associado.

## <a name="parentchild-elements"></a>Elementos pai/filho



| Hierarquia       | Elementos           |
|-----------------|--------------------|
| Elementos pai | **entrada**, **ref** |
| Elementos filho  | Nenhum               |



 

## <a name="remarks"></a>Comentários

Esse elemento define um índice de tempo no conteúdo em que o Windows Media Player é para iniciar a renderização do fluxo. Esse elemento só pode ser usado com conteúdo armazenado sob demanda que foi indexado.

## <a name="examples"></a>Exemplos


```XML
<STARTTIME VALUE="1:30.0" />
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------|
| Versão<br/> | Windows Media Player versão 70 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de elementos de metarquivo do Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Referência do metarquivo do Windows Media**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





