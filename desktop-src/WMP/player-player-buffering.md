---
title: Evento Player. buffering
description: o evento de buffer ocorre quando o controle de Windows Media Player começa ou termina o buffer ou o download. | Evento Player. buffering
ms.assetid: a0a09bf7-19bc-4838-a403-924e8d83b48d
keywords:
- Windows Media Player de eventos de buffer
- Windows Media Player de eventos de buffer, classe de jogador
- Windows Media Player de classe de Player, evento de buffer
topic_type:
- apiref
api_name:
- Player.Buffering
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0ac382315d37fcd36a5470ae3f7f07bf4454687b660a2311498b5b0866e32b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117747517"
---
# <a name="playerbuffering-event"></a>Evento Player. buffering

o evento de **buffer** ocorre quando o controle de Windows Media Player começa ou termina o buffer ou o download.

## <a name="syntax"></a>Sintaxe


```JScript
Player.Buffering(
  Start
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Iniciar* 
</dt> <dd>

**Booliano** que contém um dos valores a seguir.



| Valor | Descrição            |
|-------|------------------------|
| true  | O buffer foi iniciado. |
| false | O buffer foi encerrado.   |



 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

Use esse evento para determinar quando o buffer ou o download é iniciado ou interrompido. Você pode usar o mesmo bloco de eventos para ambos os casos e para testar a *rede*. **bufferingProgress** e *rede*. **downloadProgress** para determinar se Windows Media Player está atualmente armazenando em buffer ou baixando conteúdo.

o valor dos parâmetros de evento é especificado por Windows Media Player e pode ser acessado ou passado para um método em um arquivo de JScript importado usando o nome de parâmetro fornecido. Esse nome de parâmetro deve ser digitado exatamente como mostrado, incluindo a capitalização.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Network. bufferingProgress**](network-bufferingprogress.md)
</dt> <dt>

[**Network. downloadProgress**](network-downloadprogress.md)
</dt> <dt>

[**Objeto de jogador**](player-object.md)
</dt> </dl>

 

 





