---
title: Mensagem de EM_GETBIDIOPTIONS (RichEdit. h)
description: Indica o estado atual das opções bidirecionais no controle de edição rico.
ms.assetid: 055581c0-ae59-4601-a3e9-416705af429a
keywords:
- Controles de EM_GETBIDIOPTIONS de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_GETBIDIOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fade63ac94007bedbf58642dc7a9451eb158fc3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085678"
---
# <a name="em_getbidioptions-message"></a>\_Mensagem em GETbidioptions

Indica o estado atual das opções bidirecionais no controle de edição rico.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Esse parâmetro não é usado; Ele deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Uma estrutura [**bidioptions**](/windows/desktop/api/Richedit/ns-richedit-bidioptions) que recebe o estado atual das opções bidirecionais no controle rich edit.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa mensagem não retorna um valor.

## <a name="remarks"></a>Comentários

Essa mensagem define os valores dos membros **wMask** e **wEffects** como o valor do estado atual das opções bidirecionais no controle rich edit.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| Redistribuível<br/>          | Edição avançada 3,0<br/>                                                              |
| parâmetro<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**BIDIoptions**](/windows/desktop/api/Richedit/ns-richedit-bidioptions)
</dt> <dt>

[**em \_ SETbidioptions**](em-setbidioptions.md)
</dt> </dl>

 

 





