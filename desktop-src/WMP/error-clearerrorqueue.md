---
title: Erro. método clearErrorQueue
description: O método clearErrorQueue limpa os erros da fila de erros. | Erro. método clearErrorQueue
ms.assetid: 306f0700-88b1-4433-8abb-7d225e82060a
keywords:
- método clearErrorQueue Windows Media Player
- método clearErrorQueue Windows Media Player, classe Error
- Classe de erro do Windows Media Player, método clearErrorQueue
topic_type:
- apiref
api_name:
- Error.clearErrorQueue
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b756708b8f0643f86489c26dd921e87c408be8f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789551"
---
# <a name="errorclearerrorqueue-method"></a>Erro. método clearErrorQueue

O método **clearErrorQueue** limpa os erros da fila de erros.

## <a name="syntax"></a>Sintaxe


```JScript
Error.clearErrorQueue()
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método é útil para limpar a fila de erros depois que uma série de erros é processada.

Você deve definir *as configurações*. **enableErrorDialogs** como false se você optar por exibir mensagens de erro personalizadas.

## <a name="examples"></a>Exemplos

O exemplo de JScript a seguir usa *erro*. **clearErrorQueue** em um manipulador de eventos para esvaziar a fila de erros após a exibição de todas as descrições de erro. O objeto de **jogador** foi criado com ID = "Player".


```JScript
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = error()>

// Store the number of errors in the queue.
var max = Player.error.errorCount 

// Loop through the list of errors.
for (var i = 0; i < max; i++){
    // Get the error description for this item.
    var errDesc = Player.error.item(i).errorDescription;
    
    // Display the error message.
    alert(errDesc);
}

// Clear the error queue to prepare for the next group of errors.
Player.error.clearErrorQueue();

</SCRIPT>

```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto Error**](error-object.md)
</dt> </dl>

 

 





