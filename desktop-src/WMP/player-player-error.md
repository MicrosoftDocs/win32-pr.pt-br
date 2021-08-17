---
title: Evento Player. Error
description: O evento de erro ocorre quando há uma condição de erro.
ms.assetid: 1e418a56-ae81-4ff0-b721-3390be08970d
keywords:
- Windows Media Player de eventos de erro
- Windows Media Player de eventos de erro, classe de jogador
- Windows Media Player de classe de Player, evento de erro
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
ms.openlocfilehash: 6a7e4642eef19b4edc4b1aa5bc75022a307d279d0d60482af0c7e2f0a9368c06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134809"
---
# <a name="playererror-event"></a>Evento Player. Error

O evento de **erro** ocorre quando há uma condição de erro.

## <a name="syntax"></a>Sintaxe


```JScript
Player.Error()
```



## <a name="parameters"></a>Parâmetros

Este evento não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse evento não retorna um valor.

## <a name="examples"></a>Exemplos

o exemplo a seguir JScript cria um manipulador de eventos para exibir o texto de descrição do primeiro erro na fila de erros. O objeto de **jogador** foi criado com ID = "Player".


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

 

 





