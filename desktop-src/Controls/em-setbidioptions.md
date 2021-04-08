---
title: Mensagem de EM_SETBIDIOPTIONS (RichEdit. h)
description: A \_ mensagem em SETbidioptions define o estado atual das opções bidirecionais no controle de edição rico.
ms.assetid: b518e423-317a-4654-9d9f-c501028e2a0a
keywords:
- Controles de EM_SETBIDIOPTIONS de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_SETBIDIOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84dc4b92f7a989ab5ef283b36708094a143475de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086193"
---
# <a name="em_setbidioptions-message"></a>\_Mensagem em SETbidioptions

A mensagem em **\_ setbidioptions** define o estado atual das opções bidirecionais no controle de edição rico.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Esse parâmetro não é usado; Ele deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**bidioptions**](/windows/desktop/api/Richedit/ns-richedit-bidioptions) que indica como definir o estado das opções bidirecionais no controle rich edit.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa mensagem não retorna um valor.

## <a name="remarks"></a>Comentários

O controle rich edit deve estar no modo de texto sem formatação ou em **\_ setbidioptions** não fará nada.

Em controles de texto sem formatação, em **\_ setbidioptions** determina automaticamente a direção do parágrafo e/ou o alinhamento com base nas regras de contexto. Essas regras deformam que a direção e/ou o alinhamento são derivados do primeiro caractere forte no controle. Um caractere forte é aquele do qual a direção do texto pode ser determinada (consulte Unicode Standard versão 2,0). A direção do parágrafo e/ou o alinhamento é aplicado ao formato padrão.

**Em \_ Setbidioptions** alterna apenas o formato de parágrafo padrão para RTL (da direita para a esquerda) se encontrar um caractere DPE,

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

[**em \_ GETbidioptions**](em-getbidioptions.md)
</dt> </dl>

 

 





