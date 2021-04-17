---
title: Método Controls. fastForward
description: O método fastForward inicia a reprodução rápida do item de mídia na direção de encaminhamento. | Método Controls. fastForward
ms.assetid: 69cee803-f76b-4a8c-a2c2-1870665afaf9
keywords:
- método fastForward Windows Media Player
- método fastForward Windows Media Player, classe Controls
- Classe Controls Windows Media Player, método fastForward
topic_type:
- apiref
api_name:
- Controls.fastForward
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20d033b8b025955e57a9c3ebed00a6d7a92a666e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813180"
---
# <a name="controlsfastforward-method"></a>Método Controls. fastForward

O método **Fastforward** inicia a reprodução rápida do item de mídia na direção de encaminhamento.

## <a name="syntax"></a>Sintaxe


```JScript
Controls.fastForward()
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

O método **Fastforward** reproduz o clipe em cinco vezes a velocidade normal. Invocar **Fastforward** altera as *configurações*. **taxa** de propriedade para 5,0. Se a **taxa** for alterada posteriormente, ou se **Play** ou **Stop** for chamado, o Windows Media Player cessará o encaminhamento rápido.

O método **Fastforward** não funciona para transmissões ao vivo e certos tipos de mídia. Para determinar se você pode avançar rapidamente em um clipe, chame **IsAvailable**("Fastforward").

## <a name="examples"></a>Exemplos

O exemplo a seguir cria um elemento de botão HTML que usa **Fastforward** para iniciar a reprodução rápida do item de mídia. O objeto de **jogador** foi criado com ID = "Player".


```JScript
<INPUT TYPE = "BUTTON"  ID = "FF"  NAME = "FF"  VALUE = ">>"  

    /* Execute JScript when the BUTTON is clicked. 
       Check first to make sure fast-forward mode is available
       for this particular media item */
    onClick = "if (Player.controls.isAvailable('FastForward'))
        Player.controls.fastForward();
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

[**Controls. IsAvailable**](controls-isavailable.md)
</dt> <dt>

[**Controls. Play**](controls-play.md)
</dt> <dt>

[**Controls. Stop**](controls-stop.md)
</dt> <dt>

[**Settings. Rate**](settings-rate.md)
</dt> </dl>

 

 





