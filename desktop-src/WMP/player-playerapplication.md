---
title: Player. playerApplication
description: a propriedade playerApplication recupera o objeto playerApplication quando um controle de Windows Media Player remoto está em execução.
ms.assetid: 09a8a63f-455f-4f81-8fdb-7de337139dea
keywords:
- Windows Media Player Player. playerApplication
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
ms.openlocfilehash: c47400fcba1cb1cd1679e747d4fdd49b155df921ec33a721f74df2ec25259600
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995846"
---
# <a name="playerplayerapplication"></a>Player. playerApplication

a propriedade **playerApplication** recupera o objeto **playerApplication** quando um controle de Windows Media Player remoto está em execução.

## <a name="syntax"></a>Syntax

**playerApplication**

## <a name="possible-values"></a>Valores possíveis

Essa propriedade é um objeto **PlayerApplication** somente leitura ou o valor nulo.

## <a name="remarks"></a>Comentários

essa propriedade é usada somente quando a comunicação remota do Windows Playercontrol de mídia. se o valor for nulo, o Windows de mídia Playercontrol não será inserido no modo remoto.

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

 

 





