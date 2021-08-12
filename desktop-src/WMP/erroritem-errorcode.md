---
title: ErrorItem. errorCode
description: A propriedade errorCode recupera o código de erro atual.
ms.assetid: 1495ec34-0995-40c6-bfd0-f3695784e057
keywords:
- Windows Media Player ErrorItem. errorCode
topic_type:
- apiref
api_name:
- ErrorItem.errorCode
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f426bbaf1092b64cdb3578cb681282c9b27d9d2e2e23a69d50f9c065353ad104
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118577700"
---
# <a name="erroritemerrorcode"></a>ErrorItem. errorCode

A propriedade **ErrorCode** recupera o código de erro atual.

``` syntax
player.error.item(
        index
        ).errorCode
```

## <a name="possible-values"></a>Valores possíveis

Essa propriedade é um **número** somente leitura (**Long**).

## <a name="remarks"></a>Comentários

você deve definir *Configurações*. **enableErrorDialogs** como false se você optar por exibir mensagens de erro personalizadas.

## <a name="examples"></a>Exemplos

o exemplo a seguir JScript usa *ErrorItem*. **ErrorCode** em um manipulador de eventos para exibir o código de erro para o usuário. O objeto de **jogador** foi criado com ID = "Player".


```JScript
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = error()>

// Get the error code for the first error item.
errNum = Player.error.item(0).errorCode;

// Display the error information.
var message = "Error number: " + errNum);
message += "<BR>";
message += "Use your BACK button to return ";
message += "to the previous page.";
document.write(message);

</SCRIPT>

```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto ErrorItem**](erroritem-object.md)
</dt> <dt>

[**ErrorItem. errorDescription**](erroritem-errordescription.md)
</dt> </dl>

 

 





