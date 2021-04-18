---
title: PlayerApplication.hasDisplay
description: A propriedade hasDisplay recupera um valor que indica se o vídeo pode ser exibido por meio do controle de Player remoto.
ms.assetid: f90c5470-f985-4b98-823f-7395f89b238b
keywords:
- PlayerApplication. hasDisplay Windows Media Player
topic_type:
- apiref
api_name:
- PlayerApplication.hasDisplay
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ef77cb42109decef6ab435aa031240f89b6cb98
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105814019"
---
# <a name="playerapplicationhasdisplay"></a>PlayerApplication.hasDisplay

A propriedade **hasDisplay** recupera um valor que indica se o vídeo pode ser exibido por meio do controle de Player remoto.

## <a name="syntax"></a>Syntax

*playerApplication*. **hasDisplay**

## <a name="possible-values"></a>Valores possíveis

Esta propriedade é um **booliano** somente leitura.

## <a name="remarks"></a>Comentários

Essa propriedade é usada somente quando você faz a comunicação remota do controle do Windows Media Player.

Vários controles do Windows Media Player podem ser executados remotamente ao mesmo tempo, mas o vídeo só pode ser exibido em um local de cada vez, seja no modo completo do Player ou em um dos controles remotos do Windows Media Player. Use essa propriedade para determinar se o controle atual é aquele pelo qual o vídeo pode ser exibido.

**Windows Media Player 10 Mobile:** Essa propriedade sempre retorna **true**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto PlayerApplication**](playerapplication-object.md)
</dt> <dt>

[**Estabelecer comunicação remota do controle do Windows Media Player**](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 





