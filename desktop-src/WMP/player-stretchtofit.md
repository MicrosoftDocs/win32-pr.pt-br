---
title: Player. stretchToFit
description: A propriedade stretchToFit especifica ou recupera um valor que indica se o vídeo exibido pelo controle do Windows Media Player é dimensionado automaticamente para se ajustar à janela de vídeo, quando a janela de vídeo é maior do que as dimensões da imagem de vídeo.
ms.assetid: 9ea02959-602e-4bac-a8aa-dce502d1bb54
keywords:
- Player. stretchToFit Windows Media Player
topic_type:
- apiref
api_name:
- Player.stretchToFit
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb7b68042cf2a5bd0e7f718d1e19641edecdf548
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105797641"
---
# <a name="playerstretchtofit"></a>Player. stretchToFit

A propriedade **stretchToFit** especifica ou recupera um valor que indica se o vídeo exibido pelo controle do Windows Media Player é dimensionado automaticamente para se ajustar à janela de vídeo, quando a janela de vídeo é maior do que as dimensões da imagem de vídeo.

## <a name="syntax"></a>Syntax

*Player*. **stretchToFit**

## <a name="possible-values"></a>Valores possíveis

Esta propriedade é um **booliano** de leitura/gravação.



| Valor | Descrição                                            |
|-------|--------------------------------------------------------|
| true  | O vídeo será alongado para se ajustar à janela.              |
| false | Padrão. O vídeo não será ampliado para se ajustar à janela. |



 

## <a name="remarks"></a>Comentários

Quando **stretchToFit** é definido como true, o controle do Windows Media Player mantém a taxa de proporção original do vídeo. Se a taxa de proporção do vídeo não corresponder à taxa de proporção da janela de vídeo, as áreas de máscara preta poderão aparecer na parte superior e inferior, ou à esquerda e à direita da imagem de vídeo.

Essa propriedade se aplica ao controle do Windows Media Player somente quando inserida em uma página da Web.

**Windows Media Player 10 Mobile:** Não há suporte para essa propriedade.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,1 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto de jogador**](player-object.md)
</dt> </dl>

 

 





