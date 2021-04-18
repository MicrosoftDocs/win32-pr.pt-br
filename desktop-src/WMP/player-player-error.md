---
title: Evento Player. Error
description: O evento de erro ocorre quando há uma condição de erro.
ms.assetid: 1e418a56-ae81-4ff0-b721-3390be08970d
keywords:
- Evento de erro do Windows Media Player
- Evento de erro Windows Media Player, classe Player
- Classe de Player Windows Media Player, evento de erro
topic_type:
- apiref
api_name:
- Player.Error
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a99411773994ad012155eea5a203ed341d50b460
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105773073"
---
# <a name="playererror-event"></a>Evento Player. Error

O evento de **erro** ocorre quando há uma condição de erro.

## <a name="syntax"></a>Sintaxe


```JScript
Player.Error()
```



## <a name="parameters"></a>Parâmetros

Este evento não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Esse evento não retorna um valor.

## <a name="examples"></a>Exemplos

O exemplo de JScript a seguir cria um manipulador de eventos para exibir o texto de descrição do primeiro erro na fila de erros. O objeto de **jogador** foi criado com ID = "Player".


```JScript
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = error()>

// Get the description of the first error. 
var errDesc = Player.error.item(0).errorDescription;

// Display the error description.
alert(errDesc);

</SCRIPT>

```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ErrorItem. errorDescription**](erroritem-errordescription.md)
</dt> <dt>

[**Erro. Item**](error-item.md)
</dt> <dt>

[**Objeto de jogador**](player-object.md)
</dt> </dl>

 

 





