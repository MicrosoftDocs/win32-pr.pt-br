---
title: Controls. IsAvailable
description: A propriedade IsAvailable indica se um tipo especificado de informação está disponível ou se uma ação especificada pode ser executada. | Controls. IsAvailable
ms.assetid: d2bfaa67-eac9-4fc4-9424-636ddb4b35d6
keywords:
- Controles. isdisponível Windows Media Player
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
ms.openlocfilehash: 61afa07596a55208be63bd29759fd5f9f3e10170
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105763362"
---
# <a name="controlsisavailable"></a>Controls. IsAvailable

A propriedade **IsAvailable** indica se um tipo especificado de informação está disponível ou se uma ação especificada pode ser executada.

``` syntax
player.controls.isAvailable(
        name
        )
```

## <a name="parameters"></a>Parâmetros

*name*

**Cadeia de caracteres** que contém um dos valores a seguir.



| String          | Descrição                                                                                                                                                       |
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| currentItem     | Determina se o usuário pode definir a propriedade **currentItem** .                                                                                                 |
| currentMarker   | Determina se o usuário pode buscar um marcador específico.                                                                                                        |
| currentPosition | Determina se o usuário pode buscar uma posição específica no arquivo. Alguns arquivos não dão suporte à busca.                                                       |
| fastForward     | Determina se o arquivo dá suporte ao encaminhamento rápido e se essa funcionalidade pode ser invocada. Muitos tipos de arquivo (ou transmissões ao vivo) não dão suporte a fastForward. |
| fastReverse     | Determina se o arquivo dá suporte a fastReverse e se essa funcionalidade pode ser invocada. Muitos tipos de arquivo (ou transmissões ao vivo) não dão suporte a fastReverse.     |
| Próximo            | Determina se o usuário pode buscar a próxima entrada em uma lista de reprodução.                                                                                             |
| pause           | Determina se o método **Pause** está disponível.                                                                                                             |
| jogar            | Determina se o método **Play** está disponível.                                                                                                              |
| previous        | Determina se o usuário pode buscar a entrada anterior em uma lista de reprodução.                                                                                         |
| Etapa            | Determina se o método **Step** está disponível durante a reprodução.                                                                                              |
| parar            | Determina se o método **Stop** está disponível.                                                                                                              |



 

## <a name="return-values"></a>Valores de retorno

Esse método retorna um valor **booliano** .

## <a name="examples"></a>Exemplos

O exemplo a seguir cria um elemento de botão HTML que busca a posição inicial do item de mídia atual. O código JScript usa **IsAvailable** para verificar se o arquivo dá suporte à operação de busca. O objeto de **jogador** foi criado com ID = "Player".


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
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/>                               |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto Controls**](controls-object.md)
</dt> </dl>

 

 





