---
title: Mensagem de EM_PASTESPECIAL (RichEdit. h)
description: Cola um formato de área de transferência específico em um controle de edição rico.
ms.assetid: b4b9c1a7-943d-4dc8-bcb9-054c984b82ba
keywords:
- controles de Windows de mensagem de EM_PASTESPECIAL
topic_type:
- apiref
api_name:
- EM_PASTESPECIAL
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dc1af4dd0566cdf8e256b34f87fcc52ea855bc521c87cbe390e02b8b1cf7b06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118412797"
---
# <a name="em_pastespecial-message"></a>\_Mensagem em PASTESPECIAL

Cola um formato de área de transferência específico em um controle de edição rico.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica os [formatos da área de transferência](/windows/desktop/dataxchg/clipboard-formats).

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**REPASTESPECIAL**](/windows/desktop/api/Richedit/ns-richedit-repastespecial) ou **nulo**. Se um objeto estiver sendo colado, a estrutura **REPASTESPECIAL** será preenchida com o aspecto de exibição desejado. Se *lParam* for **nulo** ou o membro **dwAspect** for zero, o aspecto de exibição usado será o conteúdo do descritor de objeto.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Essa mensagem não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**REPASTESPECIAL**](/windows/desktop/api/Richedit/ns-richedit-repastespecial)
</dt> </dl>

 

