---
title: Evento Player. OpenStateChange
description: O evento OpenStateChange ocorre quando a propriedade OpenState muda de valor. | Evento Player. OpenStateChange
ms.assetid: b6b840ab-72c7-4150-a259-1e7d8afcec81
keywords:
- Evento OpenStateChange do Windows Media Player
- Evento OpenStateChange Windows Media Player, classe Player
- Classe de jogador Windows Media Player, evento OpenStateChange
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
ms.openlocfilehash: 020a25a811623b9f7d7dd8f316c470cada6a142b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105762948"
---
# <a name="playeropenstatechange-event"></a>Evento Player. OpenStateChange

O evento **OpenStateChange** ocorre quando a propriedade **OpenState** muda de valor.

## <a name="syntax"></a>Sintaxe


```JScript
Player.OpenStateChange(
  NewState
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*NewState* 
</dt> <dd>

**Número** (**longo**) que especifica o novo estado aberto. Consulte [OpenState](player-openstate.md) para obter uma tabela de valores.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

O Windows Media Player pode passar por vários Estados abertos enquanto tenta abrir um arquivo de rede, como localizar o servidor, conectar-se ao servidor e, finalmente, abrir o arquivo. Esse evento será acionado sempre que o estado aberto for alterado.

O valor dos parâmetros de evento é especificado pelo Windows Media Player e pode ser acessado ou transmitido para um método em um arquivo JScript importado usando o nome de parâmetro fornecido. Esse nome de parâmetro deve ser digitado exatamente como mostrado, incluindo a capitalização.

Não há garantia de que os Estados do Windows Media Player ocorram em uma ordem específica. Além disso, nem todo estado ocorre necessariamente durante uma sequência de eventos. Você não deve escrever código que dependa da ordem de estado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto de jogador**](player-object.md)
</dt> <dt>

[**Player. openState**](player-openstate.md)
</dt> </dl>

 

 





