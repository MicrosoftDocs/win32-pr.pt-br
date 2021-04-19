---
title: Player. playerApplication
description: A propriedade playerApplication recupera o objeto PlayerApplication quando um controle remoto do Windows Media Player está em execução.
ms.assetid: 09a8a63f-455f-4f81-8fdb-7de337139dea
keywords:
- Player. playerApplication Windows Media Player
topic_type:
- apiref
api_name:
- Player.playerApplication
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 401ebaae52efb746e7119419774d87d72c642fc4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105807316"
---
# <a name="playerplayerapplication"></a>Player. playerApplication

A propriedade **playerApplication** recupera o objeto **playerApplication** quando um controle remoto do Windows Media Player está em execução.

## <a name="syntax"></a>Syntax

**playerApplication**

## <a name="possible-values"></a>Valores possíveis

Essa propriedade é um objeto **PlayerApplication** somente leitura ou o valor nulo.

## <a name="remarks"></a>Comentários

Essa propriedade é usada somente quando você faz a comunicação remota do Windows Media Playercontrol. Se o valor for NULL, o Playercontrol de mídia do Windows não será inserido no modo remoto.

Essa propriedade só pode ser acessada em código C++ ou em código de script em capas por meio da variável global playerApplication.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Atributos globais**](global-attributes.md)
</dt> <dt>

[**Objeto de jogador**](player-object.md)
</dt> <dt>

[**Objeto PlayerApplication**](playerapplication-object.md)
</dt> <dt>

[**Estabelecer comunicação remota do controle do Windows Media Player**](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 





