---
title: Mensagem de EM_SETWORDBREAKPROCEX (RichEdit. h)
description: Define o procedimento de quebra de palavra estendido para um controle de edição rico.
ms.assetid: 2b45f747-ae15-470b-a786-98d8135289da
keywords:
- Controles de EM_SETWORDBREAKPROCEX de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_SETWORDBREAKPROCEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5973836ae173c1a61537b7d3b085fe29c168971f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918279"
---
# <a name="em_setwordbreakprocex-message"></a>\_Mensagem em SETWORDBREAKPROCEX

Define o procedimento de quebra de palavra estendido para um controle de edição rico.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Esse parâmetro não é usado; Ele deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma função [*EditWordBreakProcEx*](/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex) ou **nulo** para usar o procedimento padrão.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa mensagem retorna o endereço do procedimento de quebra de palavra estendido anterior.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**EditWordBreakProcEx**](/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex)
</dt> <dt>

[**em \_ GETWORDBREAKPROCEX**](em-getwordbreakprocex.md)
</dt> </dl>

 

 





