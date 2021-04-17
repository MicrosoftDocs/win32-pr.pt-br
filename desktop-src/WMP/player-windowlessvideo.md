---
title: Player. windowlessVideo
description: A propriedade windowlessVideo especifica ou recupera um valor que indica se o controle do Windows Media Player renderiza o vídeo no modo sem janela.
ms.assetid: 314a75a3-d096-4cd4-a747-e31367e0e265
keywords:
- Player. windowlessVideo Windows Media Player
topic_type:
- apiref
api_name:
- Player.windowlessVideo
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93f4a8a2b70a42cd0893d463eccca0427dde6c43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105772981"
---
# <a name="playerwindowlessvideo"></a>Player. windowlessVideo

A propriedade **windowlessVideo** especifica ou recupera um valor que indica se o controle do Windows Media Player renderiza o vídeo no modo sem janela.

## <a name="syntax"></a>Syntax

*Player*. **windowlessVideo**

## <a name="possible-values"></a>Valores possíveis

Essa propriedade é um **booliano** que é especificado em tempo de design e é somente leitura daí em diante.



| Valor | Descrição                                      |
|-------|--------------------------------------------------|
| true  | O vídeo é renderizado no modo sem janela.        |
| false | Padrão. O vídeo é renderizado no modo de janela. |



 

## <a name="remarks"></a>Comentários

Por padrão, um controle do Windows Media Player inserido renderiza o vídeo em sua própria janela dentro da área do cliente. Quando **windowlessVideo** é definido como true, o controle de jogador renderiza o vídeo diretamente na área do cliente, para que você possa aplicar efeitos especiais ou colocar o vídeo em camadas com texto.

No Windows Vista, o vídeo de renderização no modo sem janela pode prejudicar o desempenho.

Não há suporte para a propriedade **windowlessVideo** no Netscape Navigator. Definir um valor para essa propriedade no navegador pode gerar resultados inesperados.

**Windows Media Player 10 Mobile:** Não há suporte para essa propriedade.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player para Windows XP ou posterior.<br/>                           |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



 

 





