---
title: Mensagem de TTM_SETMAXTIPWIDTH (commctrl. h)
description: Define a largura máxima para uma janela de dica de ferramenta.
ms.assetid: 3cfb6011-d0c3-4a57-aead-d4ec09a057cc
keywords:
- controles de Windows de mensagem de TTM_SETMAXTIPWIDTH
topic_type:
- apiref
api_name:
- TTM_SETMAXTIPWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d344a3abcbe2b3bf57a71c8020d383f76ab1922b9009cd69411912d4468fa19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119433756"
---
# <a name="ttm_setmaxtipwidth-message"></a>\_Mensagem TTM SETMAXTIPWIDTH

Define a largura máxima para uma janela de dica de ferramenta.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Largura máxima da janela de dica de ferramenta ou-1 para permitir qualquer largura.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna a largura máxima da dica de ferramenta anterior.

## <a name="remarks"></a>Comentários

O valor de largura máximo não indica a largura real de uma janela de dica de ferramenta. Em vez disso, se uma cadeia de dica de ferramenta exceder a largura máxima, o controle quebrará o texto em várias linhas, usando espaços para determinar as quebras de linha. Se o texto não puder ser segmentado em várias linhas, ele será exibido em uma única linha, o que pode exceder a largura máxima da dica de ferramenta.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TTM \_ GETMAXTIPWIDTH**](ttm-getmaxtipwidth.md)
</dt> </dl>

 

 





