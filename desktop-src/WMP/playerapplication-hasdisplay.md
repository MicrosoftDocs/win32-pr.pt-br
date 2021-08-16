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
ms.openlocfilehash: e6cffddc08c154ced6d7cb72b18642b5ebb4960e539e5682d1cf6e8518b74831
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117747355"
---
# <a name="playerapplicationhasdisplay"></a>PlayerApplication.hasDisplay

A propriedade **hasDisplay** recupera um valor que indica se o vídeo pode ser exibido por meio do controle de Player remoto.

## <a name="syntax"></a>Syntax

*playerApplication*. **hasDisplay**

## <a name="possible-values"></a>Valores possíveis

Esta propriedade é um **booliano** somente leitura.

## <a name="remarks"></a>Comentários

essa propriedade é usada somente quando o controle de Windows Media Player de comunicação remota é usado.

vários controles de Windows Media Player podem ser executados remotamente ao mesmo tempo, mas o vídeo só pode ser exibido em um local de cada vez, seja no modo completo do Player ou em um dos controles de Windows Media Player remotos. Use essa propriedade para determinar se o controle atual é aquele pelo qual o vídeo pode ser exibido.

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

 

 





