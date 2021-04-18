---
title: Evento Player. ModeChange
description: O evento ModeChange ocorre quando um modo do Windows Media Player é alterado. | Evento Player. ModeChange
ms.assetid: 45b57660-b186-4c0f-8735-61134058b8c9
keywords:
- Evento ModeChange do Windows Media Player
- Evento ModeChange Windows Media Player, classe Player
- Classe de jogador Windows Media Player, evento ModeChange
topic_type:
- apiref
api_name:
- Player.ModeChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb202672c7fce6705b8e86889c0ca44d7004a19e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760578"
---
# <a name="playermodechange-event"></a>Evento Player. ModeChange

O evento **ModeChange** ocorre quando um modo do Windows Media Player é alterado.

## <a name="syntax"></a>Sintaxe


```JScript
Player.ModeChange(
  ModeName,
  NewValue
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ModeName* 
</dt> <dd>

**Cadeia de caracteres** que indica o modo que foi alterado. Contém um dos seguintes valores.



| Valor   | Descrição                                         |
|---------|-----------------------------------------------------|
| ordem aleatória | As faixas são reproduzidas em ordem aleatória.                  |
| loop    | A sequência inteira de faixas é reproduzida repetidamente. |



 

</dd> <dt>

*NewValue* 
</dt> <dd>

**Booliano** que indica o novo estado do modo especificado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

O valor dos parâmetros de evento é especificado pelo Windows Media Player e pode ser acessado ou transmitido para um método em um arquivo JScript importado usando o nome de parâmetro fornecido. Esse nome de parâmetro deve ser digitado exatamente como mostrado, incluindo a capitalização.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto de jogador**](player-object.md)
</dt> <dt>

[**Settings. GetMode**](settings-getmode.md)
</dt> <dt>

[**Settings. setmode**](settings-setmode.md)
</dt> </dl>

 

 





