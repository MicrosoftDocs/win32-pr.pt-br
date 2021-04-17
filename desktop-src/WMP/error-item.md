---
title: Método Error. Item
description: O método item recupera um objeto ErrorItem da fila de erros.
ms.assetid: 3aca21ff-4c6b-4c24-a85d-3d015612a496
keywords:
- método de item Windows Media Player
- método de item Windows Media Player, classe de erro
- Classe de erro Windows Media Player, método de item
topic_type:
- apiref
api_name:
- Error.item
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5545df50fce05ff5a10a5f870d1ec07648434fe9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105762076"
---
# <a name="erroritem-method"></a>Método Error. Item

O método **Item** recupera um objeto **ErrorItem** da fila de erros.

## <a name="syntax"></a>Sintaxe


```JScript
retVal = Error.item(
  index
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*índice* \[ do no\]
</dt> <dd>

**Número** (**longo**) que contém o índice do objeto **ErrorItem** a ser recuperado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retorna um objeto **ErrorItem** .

## <a name="remarks"></a>Comentários

O Windows Media Player pode gerar vários erros em resposta a uma condição de erro. Esse método permite a recuperação de um erro específico na fila usando um número de índice. Os números de índice para a fila de erros começam com zero.

Você deve definir *as configurações*. **enableErrorDialogs** como false se você optar por exibir mensagens de erro personalizadas.

## <a name="examples"></a>Exemplos

O exemplo de JScript a seguir usa o *erro*. objeto de **Item** em um manipulador de eventos para alertar o usuário para o erro mais recente. O objeto de **jogador** foi criado com ID = "Player".


```JScript
<SCRIPT LANGUAGE="JScript"  FOR=Player EVENT=error()>

// Store the most recent error item number.
var max = Player.error.errorCount - 1 

// Store the most recent error in an error item object.
var errItem = Player.error.item(max);

// Use the error item object to store the error info.
errDesc = errItem.errorDescription;
errNum = errItem.errorCode;

// Display the error info.
alert(errNum + "\n" + errDesc);

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
</dt> <dt>

[**Objeto ErrorItem**](erroritem-object.md)
</dt> </dl>

 

 





