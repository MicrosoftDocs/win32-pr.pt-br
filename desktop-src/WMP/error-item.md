---
title: Método Error.item
description: O método de item recupera um objeto ErrorItem da fila de erros.
ms.assetid: 3aca21ff-4c6b-4c24-a85d-3d015612a496
keywords:
- método item Windows Media Player
- método item Windows Media Player , classe Error
- Classe de erro Windows Media Player , método de item
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
ms.openlocfilehash: 5e9fbd9f402a659af27db42c34cb0c58e2097270b73eb0eeff382544979dc0a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118339691"
---
# <a name="erroritem-method"></a>Método Error.item

O **método de item** recupera um objeto **ErrorItem** da fila de erros.

## <a name="syntax"></a>Sintaxe


```JScript
retVal = Error.item(
  index
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*índice* \[ Em\]
</dt> <dd>

**Número** (**longo**) que contém o índice do **objeto ErrorItem** a ser recuperado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método retorna um **objeto ErrorItem.**

## <a name="remarks"></a>Comentários

Windows Media Player pode gerar vários erros em resposta a uma condição de erro. Esse método permite a recuperação de um erro específico na fila usando um número de índice. Os números de índice para a fila de erros começam com zero.

Você deve definir *Configurações*. **enableErrorDialogs** como false se você optar por exibir mensagens de erro personalizadas.

## <a name="examples"></a>Exemplos

O exemplo JScript a seguir usa o *erro*. **objeto** item em um manipulador de eventos para alertar o usuário sobre o erro mais recente. O **objeto** Player foi criado com ID = "Player".


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
| Versão<br/> | Windows Media Player versão 7.0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto Error**](error-object.md)
</dt> <dt>

[**Objeto ErrorItem**](erroritem-object.md)
</dt> </dl>

 

 





