---
title: Player. versionInfo
description: A propriedade versionInfo recupera um valor de cadeia de caracteres que especifica a versão do Windows Media Player.
ms.assetid: 4b644de2-fcb9-407b-9eea-3eb683a17150
keywords:
- Player. versionInfo Windows Media Player
topic_type:
- apiref
api_name:
- Player.versionInfo
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b44a94fa2df6d5e7d46108ec971fd84481688eb6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105763330"
---
# <a name="playerversioninfo"></a>Player. versionInfo

A propriedade **versionInfo** recupera um valor de cadeia de caracteres que especifica a versão do Windows Media Player.

## <a name="syntax"></a>Syntax

*Player* . **versionInfo**

## <a name="possible-values"></a>Valores possíveis

Essa propriedade é uma **cadeia de caracteres** somente leitura no seguinte formato: "*X*. 0,0. *Aaaa*", em que *X* representa o número de versão principal e *yyyy* representa o número de Build.

## <a name="examples"></a>Exemplos

O exemplo a seguir cria um elemento de botão HTML que, quando clicado, exibe uma caixa de mensagem contendo as informações de versão do Windows Media Player. O objeto de **jogador** foi criado com ID = "Player".


```
<INPUT TYPE = "BUTTON"  ID = "VERSION"  VALUE = "Show Version"
    onClick = "
        /* Build the message containing the version info. */
        var message = 'Windows Media Player Version: ';
        message += '\n';
        message += Player.versionInfo;
 
        /* Display the message box. */
        alert(message);
">

```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto de jogador**](player-object.md)
</dt> </dl>

 

 





