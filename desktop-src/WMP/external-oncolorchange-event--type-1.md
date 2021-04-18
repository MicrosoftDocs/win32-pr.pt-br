---
title: Evento external. OnColorChange (tipo 1)
description: Observação Este tópico descreve a funcionalidade projetada para uso por lojas online. | Evento external. OnColorChange (tipo 1)
ms.assetid: 45e6ec4a-e680-4d50-8fb7-410f12383eef
keywords:
- Evento external. OnColorChange (tipo 1) Windows Media Player
topic_type:
- apiref
api_name:
- External.OnColorChange Event (Type 1)
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11805cc154c60b8a765f46041f74d40929df418d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105783605"
---
# <a name="externaloncolorchange-event-type-1"></a>Evento external. OnColorChange (tipo 1)

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

[**Objeto externo para repositórios online do tipo 1**](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





