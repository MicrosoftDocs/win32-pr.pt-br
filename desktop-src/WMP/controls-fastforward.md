---
title: Método Controls.fastForward
description: O método fastForward inicia a reprodução rápida do item de mídia na direção da frente. | Método Controls.fastForward
ms.assetid: 69cee803-f76b-4a8c-a2c2-1870665afaf9
keywords:
- Método fastForward Windows Media Player
- Método fastForward Windows Media Player classe , Controls
- Classe Controls Windows Media Player , método fastForward
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
ms.openlocfilehash: a8b35c2a31c26259a12638d09c968b90ea42f93c692bf4c24af9dc987a6df3bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118341812"
---
# <a name="controlsfastforward-method"></a>Método Controls.fastForward

O **método fastForward** inicia a reprodução rápida do item de mídia na direção da frente.

## <a name="syntax"></a>Sintaxe


```JScript
Controls.fastForward()
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

O **método fastForward** reproduz o clipe em cinco vezes a velocidade normal. Invocar **fastForward altera** o *Configurações*. **propriedade rate** para 5,0. Se **a** taxa for alterada posteriormente ou se **a reprodução** ou a parada for chamada, Windows Media Player interromperá o encaminhamento rápido. 

O **método fastForward** não funciona para transmissões ao vivo e determinados tipos de mídia. Para determinar se você pode avançar rapidamente em um clipe, chame **isAvailable**("FastForward").

## <a name="examples"></a>Exemplos

O exemplo a seguir cria um elemento HTML BUTTON que usa **fastForward** para iniciar a reprodução rápida do item de mídia. O **objeto** Player foi criado com ID = "Player".


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
| Versão<br/> | Windows Media Player versão 7.0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto Controls**](controls-object.md)
</dt> <dt>

[**Controls.isAvailable**](controls-isavailable.md)
</dt> <dt>

[**Controls.play**](controls-play.md)
</dt> <dt>

[**Controls.stop**](controls-stop.md)
</dt> <dt>

[**Configurações.rate**](settings-rate.md)
</dt> </dl>

 

 





