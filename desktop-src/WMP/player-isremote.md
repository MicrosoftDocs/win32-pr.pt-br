---
title: Player. IsRemote
description: A propriedade IsRemote recupera um valor que indica se o controle do Windows Media Player está sendo executado no modo remoto.
ms.assetid: bfeab968-affb-4d5d-b88b-5caf50d34cee
keywords:
- Player. IsRemote Windows Media Player
topic_type:
- apiref
api_name:
- Player.isRemote
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7c8d97ba212e032db16b43299d2a3a8a836f9b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747253"
---
# <a name="playerisremote"></a>Player. IsRemote

A propriedade **IsRemote** recupera um valor que indica se o controle do Windows Media Player está sendo executado no modo remoto.

## <a name="syntax"></a>Syntax

*Player* . **IsRemote**

## <a name="possible-values"></a>Valores possíveis

Esta propriedade é um **booliano** somente leitura.



| Valor | Descrição                                   |
|-------|-----------------------------------------------|
| true  | O controle do player está sendo executado no modo remoto. |
| false | O controle do player está sendo executado no modo local.  |



 

## <a name="remarks"></a>Comentários

**Windows Media Player 10 Mobile:** Essa propriedade sempre retorna false.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto de jogador**](player-object.md)
</dt> <dt>

[**Estabelecer comunicação remota do controle do Windows Media Player**](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 





