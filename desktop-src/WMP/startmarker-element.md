---
title: Elemento STARTMARKER
description: O elemento STARTMARKER especifica um marcador do qual o Windows Media Player começará a renderizar o fluxo.
ms.assetid: b5c2422b-a59c-43f7-bac3-5722418192dc
keywords:
- Elemento STARTMARKER do Windows Media Player
topic_type:
- apiref
api_name:
- STARTMARKER Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4c3b3afbc3ab4a922d17f6a0269ed89c22f4dfeb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761156"
---
# <a name="startmarker-element"></a>Elemento STARTMARKER

O elemento **STARTMARKER** especifica um marcador do qual o Windows Media Player começará a renderizar o fluxo.

``` syntax
<STARTMARKER
   NUMBER = "marker number"
   NAME = "marker name"
/>
```

## <a name="attributes"></a>Atributos

**AUTOMÁTICA**

O número de um marcador numérico no índice. O valor padrão é o início do conteúdo sob demanda ou a posição atual em um fluxo em tempo real.

**NOME**

O nome de um marcador nomeado no índice. O valor padrão é o início do conteúdo sob demanda ou a posição atual em um fluxo em tempo real.

## <a name="parentchild-elements"></a>Elementos pai/filho



| Hierarquia       | Elementos           |
|-----------------|--------------------|
| Elementos pai | **entrada**, **ref** |
| Elementos filho  | Nenhum               |



 

## <a name="remarks"></a>Comentários

Esse elemento Especifica o marcador do qual o Windows Media Player deve começar a renderizar o fluxo definido na **entrada** pai ou no elemento **ref** .

**Observação**

Use esse elemento com o atributo **Number** ou **Name** , mas não ambos.

Um **elemento STARTMARKER** definido em um elemento **ref** tem precedência sobre um elemento **STARTMARKER** definido dentro do elemento de **entrada** pai do elemento **ref** . Um elemento **STARTMARKER** também tem precedência sobre um elemento **StartTime** .

Se o marcador especificado por um elemento **STARTMARKER** ocorrer posteriormente no fluxo do que o marcador definido por um elemento de **marca de fim** , nenhum conteúdo será reproduzido, mas nenhum erro é gerado.

## <a name="examples"></a>Exemplos


```XML
<STARTMARKER NUMBER="14" />
<STARTMARKER NAME="Marker_StartHere" />
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

 

 





