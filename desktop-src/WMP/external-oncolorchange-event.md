---
title: Evento External.OnColorChange
description: Observação Este tópico descreve a funcionalidade projetada para uso por lojas online. | Evento External.OnColorChange
ms.assetid: f2cd44b1-c813-479b-b847-96ddb9572697
keywords:
- Evento External.OnColorChange Windows Media Player
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
ms.openlocfilehash: eae4ca15d4d7035fc342fa20263220560570d902e28b9245a6458ac59c40a4f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648746"
---
# <a name="externaloncolorchange-event"></a>Evento External.OnColorChange

> [!Note]  
> Este tópico descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

O **evento OnColorChange** ocorre quando a cor da interface do Windows Media Player usuário é modificada.

``` syntax
window.external.OnColorChange = FunctionName
```

## <a name="possible-values"></a>Valores possíveis

Essa é uma propriedade somente gravação que especifica o nome da função no script que Windows Media Player chamadas quando o evento ocorre.

## <a name="parameters"></a>Parâmetros

A função que trata esse evento não tem parâmetros.

## <a name="remarks"></a>Comentários

Os usuários podem alterar a cor da interface Windows Media Player usuário. Você pode usar esse evento para personalizar a aparência da página da Web hospedada para corresponder ao Player.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player série 9 ou posterior<br/>                                  |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto externo para lojas online do tipo 2**](external-object-for-type-2-online-stores.md)
</dt> </dl>

 

 





