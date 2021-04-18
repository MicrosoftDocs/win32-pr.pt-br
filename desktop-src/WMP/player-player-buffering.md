---
title: Evento Player. buffering
description: O evento de buffer ocorre quando o controle do Windows Media Player começa ou termina o armazenamento em buffer ou o download. | Evento Player. buffering
ms.assetid: a0a09bf7-19bc-4838-a403-924e8d83b48d
keywords:
- Evento de buffer do Windows Media Player
- Evento de buffer do Windows Media Player, classe de Player
- Classe de Player Windows Media Player, evento de buffer
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
ms.openlocfilehash: 3a73ac77f9b8e81162a6cc0f9220562caba26eae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105793259"
---
# <a name="playerbuffering-event"></a>Evento Player. buffering

O evento de **buffer** ocorre quando o controle do Windows Media Player começa ou termina o armazenamento em buffer ou o download.

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

## <a name="return-value"></a>Retornar valor

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

Use esse evento para determinar quando o buffer ou o download é iniciado ou interrompido. Você pode usar o mesmo bloco de eventos para ambos os casos e para testar a *rede*. **bufferingProgress** e *rede*. **downloadProgress** para determinar se o Windows Media Player está atualmente armazenando em buffer ou baixando conteúdo.

O valor dos parâmetros de evento é especificado pelo Windows Media Player e pode ser acessado ou transmitido para um método em um arquivo JScript importado usando o nome de parâmetro fornecido. Esse nome de parâmetro deve ser digitado exatamente como mostrado, incluindo a capitalização.

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

 

 





