---
title: Método Controls. fastReverse
description: O método fastReverse inicia a verificação rápida do item de mídia na direção inversa.
ms.assetid: 4fc61739-9006-4d62-b2c1-2b8e8830f2d9
keywords:
- método fastReverse Windows Media Player
- método fastReverse Windows Media Player, classe Controls
- Classe Controls Windows Media Player, método fastReverse
topic_type:
- apiref
api_name:
- Controls.fastReverse
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73e5a63c4299bf08c25e36e2d61924f3fb171792
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758232"
---
# <a name="controlsfastreverse-method"></a>Método Controls. fastReverse

O método **fastReverse** inicia a verificação rápida do item de mídia na direção inversa.

## <a name="syntax"></a>Sintaxe


```JScript
Controls.fastReverse()
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

O método **fastReverse** examina o clipe de forma inversa em cinco vezes a velocidade normal, exibindo apenas os quadros-chave se for um arquivo de vídeo. Invocar **fastReverse** altera as *configurações*. **taxa** de propriedade para 5,0. Se a **taxa** for alterada posteriormente, ou se **Play** ou **Stop** for chamado, o Windows Media Player deixará de ser revertido rapidamente.

Se o item fizer parte de uma lista de reprodução, o **fastReverse** para no início da faixa atual. Por exemplo, se Track 3 estiver em **fastReverse**, quando o início do Track 3 for atingido, o Windows Media Player não vai para o Track 2. A contagem de execuções não é incrementada ao chamar **fastReverse**.

Se você chamar **Fastforward** enquanto **fastReverse** estiver em vigor, **fastReverse** será interrompido e **Fastforward** será iniciado.

Esse método não funciona para transmissões ao vivo e certos tipos de mídia. Para determinar se você pode usar a inversão rápida em um clipe, chame **IsAvailable**("fastReverse").

## <a name="examples"></a>Exemplos

O exemplo a seguir cria um elemento de botão HTML que usa **fastReverse** para iniciar a reprodução rápida do item de mídia. O objeto de **jogador** foi criado com ID = "Player".


```JScript
<INPUT TYPE = "BUTTON"  ID = "REW"  NAME = "REW"  VALUE = "<<"  

    /* Run JScript when the BUTTON is clicked. 
       Check first to make sure fast-reverse mode is available
       for this particular media item */
    onClick = "if (Player.controls.isAvailable('FastReverse'))
        Player.controls.fastReverse();
">
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto Controls**](controls-object.md)
</dt> <dt>

[**Controls. fastForward**](controls-fastforward.md)
</dt> <dt>

[**Controls. IsAvailable**](controls-isavailable.md)
</dt> <dt>

[**Controls. Play**](controls-play.md)
</dt> <dt>

[**Controls. Stop**](controls-stop.md)
</dt> <dt>

[**Settings. Rate**](settings-rate.md)
</dt> </dl>

 

 





