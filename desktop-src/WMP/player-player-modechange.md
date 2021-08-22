---
title: Evento Player. ModeChange
description: o evento ModeChange ocorre quando um modo de Windows Media Player é alterado. | Evento Player. ModeChange
ms.assetid: 45b57660-b186-4c0f-8735-61134058b8c9
keywords:
- Windows Media Player de eventos ModeChange
- Windows Media Player de eventos ModeChange, classe Player
- classe de jogador Windows Media Player, evento ModeChange
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
ms.openlocfilehash: e4a1102d49064c602d04915f77eda7ecfa1c748d4aea000cef1271679da1ec62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054354"
---
# <a name="playermodechange-event"></a>Evento Player. ModeChange

o evento **ModeChange** ocorre quando um modo de Windows Media Player é alterado.

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

## <a name="return-value"></a>Valor retornado

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

o valor dos parâmetros de evento é especificado por Windows Media Player e pode ser acessado ou passado para um método em um arquivo de JScript importado usando o nome de parâmetro fornecido. Esse nome de parâmetro deve ser digitado exatamente como mostrado, incluindo a capitalização.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto de jogador**](player-object.md)
</dt> <dt>

[**Configurações. getmode**](settings-getmode.md)
</dt> <dt>

[**Configurações. setmode**](settings-setmode.md)
</dt> </dl>

 

 





