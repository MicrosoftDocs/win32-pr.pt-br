---
title: Evento Player.OpenStateChange
description: O evento OpenStateChange ocorre quando a propriedade openState altera o valor. | Evento Player.OpenStateChange
ms.assetid: b6b840ab-72c7-4150-a259-1e7d8afcec81
keywords:
- Evento OpenStateChange Windows Media Player
- Evento OpenStateChange Windows Media Player , classe Player
- Classe player Windows Media Player evento , OpenStateChange
topic_type:
- apiref
api_name:
- Player.OpenStateChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b65436dee60a5207e09a57a39c32dc479ce110e1dafb07a7dbd7cab86e4f0a92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120003216"
---
# <a name="playeropenstatechange-event"></a>Evento Player.OpenStateChange

O **evento OpenStateChange** ocorre quando a **propriedade openState** altera o valor.

## <a name="syntax"></a>Sintaxe


```JScript
Player.OpenStateChange(
  NewState
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Newstate* 
</dt> <dd>

**Number** (**long**) especificando o novo estado aberto. Consulte [openState](player-openstate.md) para ver uma tabela de valores.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

Windows Media Player pode passar por vários estados abertos enquanto tenta abrir um arquivo de rede, como localizar o servidor, conectar-se ao servidor e, por fim, abrir o arquivo. Esse evento será acionado sempre que o estado aberto mudar.

O valor dos parâmetros de evento é especificado por Windows Media Player e pode ser acessado ou passado para um método em um arquivo JScript importado usando o nome do parâmetro especificado. Esse nome de parâmetro deve ser digitado exatamente como mostrado, incluindo a capitalização.

Windows Media Player não há garantia de que ocorrerão em qualquer ordem específica. Além disso, nem todos os estados ocorrem necessariamente durante uma sequência de eventos. Você não deve escrever código que depende da ordem de estado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7.0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto Player**](player-object.md)
</dt> <dt>

[**Player.openState**](player-openstate.md)
</dt> </dl>

 

 





