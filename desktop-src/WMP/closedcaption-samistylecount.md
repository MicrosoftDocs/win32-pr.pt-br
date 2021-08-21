---
title: ClosedCaption.SAMIStyleCount
description: A propriedade SAMIStyleCount recupera o número de estilos com suporte pelo arquivo SAMI atual.
ms.assetid: 57a85e5d-1598-4cb3-b47d-a6d8f22adfff
keywords:
- ClosedCaption.SAMIStyleCount Windows Media Player
topic_type:
- apiref
api_name:
- ClosedCaption.SAMIStyleCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6e5563e40fabfa2cc82dc24598414f312192f864ecacd6ed743834e12e06759
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118119517"
---
# <a name="closedcaptionsamistylecount"></a>ClosedCaption.SAMIStyleCount

A **propriedade SAMIStyleCount** recupera o número de estilos com suporte pelo arquivo SAMI atual.

``` syntax
player.closedCaption.SAMIStyleCount
```

## <a name="possible-values"></a>Valores possíveis

Essa propriedade é um Número somente **leitura** (**long**).

## <a name="remarks"></a>Comentários

Esse método não pode ser usado até que um arquivo de mídia digital seja aberto (*Player*.**openState** é igual a 13).

**Windows Media Player 10 Mobile:** Essa propriedade sempre retorna 0.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player Série 9 ou posterior.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Adicionando legendas fechadas à mídia digital**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Objeto ClosedCaption**](closedcaption-object.md)
</dt> <dt>

[**ClosedCaption.getSAMIStyleName**](closedcaption-getsamistylename.md)
</dt> <dt>

[**ClosedCaption.SAMIStyle**](closedcaption-samistyle.md)
</dt> </dl>

 

 





