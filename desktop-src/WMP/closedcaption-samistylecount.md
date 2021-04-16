---
title: ClosedCaption.SAMIStyleCount
description: A propriedade SAMIStyleCount recupera o número de estilos com suporte pelo arquivo SAMI atual.
ms.assetid: 57a85e5d-1598-4cb3-b47d-a6d8f22adfff
keywords:
- ClosedCaption. SAMIStyleCount Windows Media Player
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
ms.openlocfilehash: 3ab48fc6660065da1635b58b67784f2ab0ff91b8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761478"
---
# <a name="closedcaptionsamistylecount"></a>ClosedCaption.SAMIStyleCount

A propriedade **SAMIStyleCount** recupera o número de estilos com suporte pelo arquivo Sami atual.

``` syntax
player.closedCaption.SAMIStyleCount
```

## <a name="possible-values"></a>Valores possíveis

Essa propriedade é um **número** somente leitura (**Long**).

## <a name="remarks"></a>Comentários

Esse método não pode ser usado até que um arquivo de mídia digital esteja aberto (*Player*.**OpenState** é igual a 13).

**Windows Media Player 10 Mobile:** Essa propriedade sempre retorna 0.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Adicionando legendas ocultas à mídia digital**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Objeto ClosedCaption**](closedcaption-object.md)
</dt> <dt>

[**ClosedCaption.getSAMIStyleName**](closedcaption-getsamistylename.md)
</dt> <dt>

[**ClosedCaption. SAMIstyle**](closedcaption-samistyle.md)
</dt> </dl>

 

 





