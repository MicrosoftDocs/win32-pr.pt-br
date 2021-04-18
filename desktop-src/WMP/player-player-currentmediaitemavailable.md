---
title: Evento Player. CurrentMediaItemAvailable
description: O evento CurrentMediaItemAvailable ocorre quando um item de metadados gráfico no item de mídia atual fica disponível. | Evento Player. CurrentMediaItemAvailable
ms.assetid: dc692b14-67d3-4867-8f99-ddfcf7d1610c
keywords:
- Evento CurrentMediaItemAvailable do Windows Media Player
- Evento CurrentMediaItemAvailable Windows Media Player, classe Player
- Classe de jogador Windows Media Player, evento CurrentMediaItemAvailable
topic_type:
- apiref
api_name:
- Player.CurrentMediaItemAvailable
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7f25d085c354cf18966ec37f822a080db56cf16
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760630"
---
# <a name="playercurrentmediaitemavailable-event"></a>Evento Player. CurrentMediaItemAvailable

O evento **CurrentMediaItemAvailable** ocorre quando um item de metadados gráfico no item de mídia atual fica disponível.

## <a name="syntax"></a>Sintaxe


```JScript
Player.CurrentMediaItemAvailable(
  bstrItemName
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrItemName* 
</dt> <dd>

**Cadeia de caracteres** que contém o nome do item de mídia atual.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

Como a reprodução pode começar antes que um item de mídia seja totalmente baixado, todos os gráficos de metadados contidos no item de mídia (como arte de capa do álbum) podem não estar disponíveis quando começam a ser reproduzidos. Esse evento alerta quando um item gráfico de metadados termina o download. Em seguida, você pode recuperar o objeto de **mídia** passando o valor de *BstrItemName* para a *mediacollection*. método **getByName** , depois do qual você pode acessar o item gráfico de metadados usando *mídia*. **getItemInfoByType** e especificando o **WM/Picture** para o nome do atributo.

O valor dos parâmetros de evento é especificado pelo Windows Media Player e pode ser acessado ou transmitido para um método em um arquivo JScript importado usando o nome de parâmetro fornecido. Esse nome de parâmetro deve ser digitado exatamente como mostrado, incluindo a capitalização.

**Windows Media Player 10 Mobile:** Não há suporte para esse evento.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto de mídia**](media-object.md)
</dt> <dt>

[**Media. getItemInfoByType**](media-getiteminfobytype.md)
</dt> <dt>

[**Mediacollection. getByName**](mediacollection-getbyname.md)
</dt> <dt>

[**Objeto de jogador**](player-object.md)
</dt> </dl>

 

 





