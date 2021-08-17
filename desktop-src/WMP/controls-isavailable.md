---
title: Controls.isAvailable
description: A propriedade isAvailable indica se um tipo especificado de informações está disponível ou se uma ação especificada pode ser executada. | Controls.isAvailable
ms.assetid: d2bfaa67-eac9-4fc4-9424-636ddb4b35d6
keywords:
- Controls.isAvailable Windows Media Player
topic_type:
- apiref
api_name:
- Controls.isAvailable
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 502343b7654241a00e9efb33acc6f5de842c6fb6bad650f24839a5fe7febf9b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135739"
---
# <a name="controlsisavailable"></a>Controls.isAvailable

A **propriedade isAvailable** indica se um tipo especificado de informações está disponível ou se uma ação especificada pode ser executada.

``` syntax
player.controls.isAvailable(
        name
        )
```

## <a name="parameters"></a>Parâmetros

*name*

**Cadeia de** caracteres que contém um dos valores a seguir.



| String          | Descrição                                                                                                                                                       |
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Currentitem     | Determina se o usuário pode definir a **propriedade currentItem.**                                                                                                 |
| Currentmarker   | Determina se o usuário pode buscar um marcador específico.                                                                                                        |
| Currentposition | Determina se o usuário pode buscar uma posição específica no arquivo. Alguns arquivos não são suportados para busca.                                                       |
| Fastforward     | Determina se o arquivo dá suporte ao encaminhamento rápido e se essa funcionalidade pode ser invocada. Muitos tipos de arquivo (ou fluxos ao vivo) não são suportados por fastForward. |
| fastReverse     | Determina se o arquivo dá suporte a fastReverse e se essa funcionalidade pode ser invocada. Muitos tipos de arquivo (ou fluxos ao vivo) não são suportados por fastReverse.     |
| Próximo            | Determina se o usuário pode buscar a próxima entrada em uma playlist.                                                                                             |
| pause           | Determina se o **método pause** está disponível.                                                                                                             |
| jogar            | Determina se o **método play** está disponível.                                                                                                              |
| previous        | Determina se o usuário pode buscar a entrada anterior em uma playlist.                                                                                         |
| Etapa            | Determina se o método **de etapa** está disponível durante a reprodução.                                                                                              |
| parar            | Determina se o **método stop** está disponível.                                                                                                              |



 

## <a name="return-values"></a>Valores de retorno

Esse método retorna um **valor booliana.**

## <a name="examples"></a>Exemplos

O exemplo a seguir cria um elemento HTML BUTTON que busca a posição inicial do item de mídia atual. O JScript código usa **isAvailable para** verificar se o arquivo dá suporte à operação de busca. O **objeto** Player foi criado com ID = "Player".


```JScript
<INPUT TYPE = "BUTTON"  ID = "START"  NAME = "START"  VALUE = "Seek To Zero"

    /* If supported, seek to position zero. */
    onClick = "if (Player.controls.isAvailable('CurrentPosition'))
        Player.controls.currentPosition = 0;
">
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7.0 ou posterior<br/>                               |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto Controls**](controls-object.md)
</dt> </dl>

 

 





