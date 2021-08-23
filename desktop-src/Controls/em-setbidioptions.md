---
title: EM_SETBIDIOPTIONS mensagem (Richedit.h)
description: A mensagem EM \_ SETBIDIOPTIONS define o estado atual das opções bidirecionais no controle de edição rich.
ms.assetid: b518e423-317a-4654-9d9f-c501028e2a0a
keywords:
- EM_SETBIDIOPTIONS controles de Windows mensagem
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
ms.openlocfilehash: f22d03e1738fc688d34f55a6823f7ae95c2dfc41724e827cd31a184ac7cbdfce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119545016"
---
# <a name="em_setbidioptions-message"></a>Mensagem EM \_ SETBIDIOPTIONS

A **mensagem EM \_ SETBIDIOPTIONS** define o estado atual das opções bidirecionais no controle de edição rich.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Esse parâmetro não é usado; ele deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura BIDIOPTIONS**](/windows/desktop/api/Richedit/ns-richedit-bidioptions) que indica como definir o estado das opções bidirecionais no controle de edição rich.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Essa mensagem não retorna um valor.

## <a name="remarks"></a>Comentários

O controle de edição rich deve estar no modo de texto sem-texto **ou EM \_ SETBIDIOPTIONS** não fará nada.

Em controles de texto sem formatação, **EM \_ SETBIDIOPTIONS** determina automaticamente a direção do parágrafo e/ou o alinhamento com base nas regras de contexto. Essas regras determinam que a direção e/ou o alinhamento são derivados do primeiro caractere forte no controle . Um caractere forte é aquele do qual a direção do texto pode ser determinada (consulte Unicode Standard versão 2.0). A direção do parágrafo e/ou alinhamento é aplicada ao formato padrão.

**EM \_ SETBIDIOPTIONS alterna** apenas o formato de parágrafo padrão para RTL (da direita para a esquerda) se encontrar um caractere RTL,

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Redistribuível<br/>          | Rich Edit 3.0<br/>                                                              |
| Cabeçalho<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**BIDIOPTIONS**](/windows/desktop/api/Richedit/ns-richedit-bidioptions)
</dt> <dt>

[**EM \_ GETBIDIOPTIONS**](em-getbidioptions.md)
</dt> </dl>

 

 





