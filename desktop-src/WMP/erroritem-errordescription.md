---
title: ErrorItem.errorDescription
description: A propriedade errorDescription recupera uma descrição do erro.
ms.assetid: 7fd16c3d-1460-41b5-81ca-2636d7a1d0d1
keywords:
- ErrorItem.errorDescription Windows Media Player
topic_type:
- apiref
api_name:
- ErrorItem.errorDescription
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5740adcef0b6eb86290ea392d0659abb0ccc3d51b0b0b1b3203105de67fb692
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119862786"
---
# <a name="erroritemerrordescription"></a>ErrorItem.errorDescription

A **propriedade errorDescription** recupera uma descrição do erro.

``` syntax
player.error.item(
        index
        ).errorDescription
```

## <a name="possible-values"></a>Valores possíveis

Essa propriedade é uma Cadeia de Caracteres somente **leitura.**

## <a name="remarks"></a>Comentários

Você deve definir *Configurações*. **enableErrorDialogs** como false se você optar por exibir mensagens de erro personalizadas.

## <a name="examples"></a>Exemplos

O exemplo JScript a seguir *usa ErrorItem*. **errorDescription em** um manipulador de eventos para exibir a mensagem de erro para o usuário. O **objeto** Player foi criado com ID = "Player".


```JScript
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = error()>

// Get the error description for the first error item.
errDesc = Player.error.item(0).errorDescription;

// Display the error code.
var message = "Error: " + errDesc";
message += "<BR>";
message += "Use your BACK button to return ";
message += "to the previous page.";
document.write(message);

</SCRIPT>

```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7.0 ou posterior<br/>                               |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto ErrorItem**](erroritem-object.md)
</dt> </dl>

 

 





