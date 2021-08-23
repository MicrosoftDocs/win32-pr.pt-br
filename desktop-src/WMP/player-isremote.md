---
title: Player.isRemote
description: A propriedade isRemote recupera um valor que indica se o controle Windows Media Player está em execução no modo remoto.
ms.assetid: bfeab968-affb-4d5d-b88b-5caf50d34cee
keywords:
- Player.isRemote Windows Media Player
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
ms.openlocfilehash: 6afa0caf615563f4829f1a337f31521b1fb7dafd5ef6e2722f1d50c01dda1ba4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119616686"
---
# <a name="playerisremote"></a>Player.isRemote

A **propriedade isRemote** recupera um valor que indica se o controle Windows Media Player está em execução no modo remoto.

## <a name="syntax"></a>Syntax

*player* . **isRemote**

## <a name="possible-values"></a>Valores possíveis

Essa propriedade é um booliana **somente leitura.**



| Valor | Descrição                                   |
|-------|-----------------------------------------------|
| true  | O controle Player está em execução no modo remoto. |
| false | O controle Player está em execução no modo local.  |



 

## <a name="remarks"></a>Comentários

**Windows Media Player 10 Mobile:** Essa propriedade sempre retorna false.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player Série 9 ou posterior.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto Player**](player-object.md)
</dt> <dt>

[**Estabelecer comunicação remota do controle do Windows Media Player**](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 





