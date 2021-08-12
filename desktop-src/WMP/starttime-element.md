---
title: Elemento STARTtime
description: o elemento starttime define um índice de tempo a partir do qual Windows Media Player começará a renderizar o fluxo.
ms.assetid: 9b0199c8-5c95-4b4e-a943-e3bd037bf0bc
keywords:
- Windows Media Player do elemento STARTtime
topic_type:
- apiref
api_name:
- STARTTIME Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9138b05b949098c59996c69143059de5cb5b25cafcd8da7d922de120d586b356
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118568788"
---
# <a name="starttime-element"></a>Elemento STARTtime

o elemento **starttime** define um índice de tempo a partir do qual Windows Media Player começará a renderizar o fluxo.

``` syntax
<STARTTIME
   VALUE = "hh:mm:ss.fract"
/>
```

## <a name="attributes"></a>Atributos

**Valor** (obrigatório)

o índice de tempo (em horas, minutos, segundos e centésimos de um segundo) do qual Windows Media Player começa a reproduzir um fluxo definido no elemento associado.

## <a name="parentchild-elements"></a>Elementos pai/filho



| Hierarquia       | Elementos           |
|-----------------|--------------------|
| Elementos pai | **entrada**, **ref** |
| Elementos filho  | Nenhum               |



 

## <a name="remarks"></a>Comentários

esse elemento define um índice de tempo no conteúdo em que Windows Media Player é iniciar a renderização do fluxo. Esse elemento só pode ser usado com conteúdo armazenado sob demanda que foi indexado.

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

[**Windows Referência de elementos de metarquivo de mídia**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Referência de metarquivo de mídia**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





