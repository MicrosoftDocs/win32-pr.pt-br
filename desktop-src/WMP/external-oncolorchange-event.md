---
title: Evento external. OnColorChange
description: Observação Este tópico descreve a funcionalidade projetada para uso por lojas online. | Evento external. OnColorChange
ms.assetid: f2cd44b1-c813-479b-b847-96ddb9572697
keywords:
- Evento external. OnColorChange do Windows Media Player
topic_type:
- apiref
api_name:
- External.OnColorChange Event
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 029c8bb860443ed026737c7413be2bed8862c6d2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105788162"
---
# <a name="externaloncolorchange-event"></a>Evento external. OnColorChange

> [!Note]  
> Este tópico descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

O evento **OnColorChange** ocorre quando a cor da interface do usuário do Windows Media Player é alterada.

``` syntax
window.external.OnColorChange = FunctionName
```

## <a name="possible-values"></a>Valores possíveis

Essa é uma propriedade somente gravação que especifica o nome da função no script que o Windows Media Player chama quando o evento ocorre.

## <a name="parameters"></a>Parâmetros

A função que manipula esse evento não usa parâmetros.

## <a name="remarks"></a>Comentários

Os usuários podem alterar a cor da interface do usuário do Windows Media Player. Você pode usar esse evento para personalizar a aparência da página da web hospedada para corresponder ao Player.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior<br/>                                  |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto externo para lojas online do tipo 2**](external-object-for-type-2-online-stores.md)
</dt> </dl>

 

 





