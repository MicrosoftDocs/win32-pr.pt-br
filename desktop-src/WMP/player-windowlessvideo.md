---
title: Player.windowlessVideo
description: A propriedade windowlessVideo especifica ou recupera um valor que indica se o controle Windows Media Player renderiza o vídeo no modo sem janela.
ms.assetid: 314a75a3-d096-4cd4-a747-e31367e0e265
keywords:
- Player.windowlessVideo Windows Media Player
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
ms.openlocfilehash: 733f8488d1d45f4c7e9794e64e2b3a70b41722048eac82d5d8eb6eb2f1d91cd2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118572073"
---
# <a name="playerwindowlessvideo"></a>Player.windowlessVideo

A **propriedade windowlessVideo** especifica ou recupera um valor que indica se o controle Windows Media Player renderiza o vídeo no modo sem janela.

## <a name="syntax"></a>Sintaxe

*player*. **windowlessVideo**

## <a name="possible-values"></a>Valores possíveis

Essa propriedade é um **booliana** que é especificado em tempo de design e é somente leitura depois disso.



| Valor | Descrição                                      |
|-------|--------------------------------------------------|
| true  | O vídeo é renderizado no modo sem janelas.        |
| false | Padrão. O vídeo é renderizado no modo em janelas. |



 

## <a name="remarks"></a>Comentários

Por padrão, um controle Windows Media Player inserido renderiza o vídeo em sua própria janela na área do cliente. Quando **windowlessVideo** é definido como true, o controle Player renderiza o vídeo diretamente na área do cliente, para que você possa aplicar efeitos especiais ou colocar o vídeo em camadas com texto.

No Windows Vista, renderizar vídeo no modo sem janela pode prejudicar o desempenho.

Não há suporte para a propriedade **windowlessVideo** no Netscape Navigator. Definir um valor para essa propriedade no Navegador pode gerar resultados inesperados.

**Windows Media Player 10 Mobile:** Não há suporte para essa propriedade.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player para Windows XP ou posterior.<br/>                           |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



 

 





