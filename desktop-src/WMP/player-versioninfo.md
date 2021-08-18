---
title: Player.versionInfo
description: A propriedade versionInfo recupera um valor string especificando a versão do Windows Media Player.
ms.assetid: 4b644de2-fcb9-407b-9eea-3eb683a17150
keywords:
- Player.versionInfo Windows Media Player
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
ms.openlocfilehash: 2251d610ad8a522155e37c8d416123c9d09faef5da2b4af4da75aeb745940f0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995826"
---
# <a name="playerversioninfo"></a>Player.versionInfo

A **propriedade versionInfo** recupera um valor string especificando a versão do Windows Media Player.

## <a name="syntax"></a>Syntax

*player* . **versionInfo**

## <a name="possible-values"></a>Valores possíveis

Essa propriedade é uma Cadeia de **Caracteres** somente leitura no seguinte formato: "*X*.0.0. *AAAA*" em *que X* representa o número de versão principal e *AAAA representa* o número de build.

## <a name="examples"></a>Exemplos

O exemplo a seguir cria um elemento HTML BUTTON que, quando clicado, exibe uma caixa de mensagem contendo as informações de versão para Windows Media Player. O **objeto** Player foi criado com ID = "Player".


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
| Versão<br/> | Windows Media Player versão 7.0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto Player**](player-object.md)
</dt> </dl>

 

 





