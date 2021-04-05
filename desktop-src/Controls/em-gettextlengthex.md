---
title: Mensagem de EM_GETTEXTLENGTHEX (RichEdit. h)
description: Calcula o comprimento do texto de várias maneiras. Ele é geralmente chamado antes de criar um buffer para receber o texto do controle.
ms.assetid: 42c89b7b-e48d-4517-9993-ce58ff9e4e40
keywords:
- Controles de EM_GETTEXTLENGTHEX de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_GETTEXTLENGTHEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de2d91674e07ef60c2ce95535983a31cf380f9e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824362"
---
# <a name="em_gettextlengthex-message"></a>\_Mensagem em GETTEXTLENGTHEX

Calcula o comprimento do texto de várias maneiras. Ele é geralmente chamado antes de criar um buffer para receber o texto do controle.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Ponteiro para uma estrutura [**GETTEXTLENGTHEX**](/windows/desktop/api/Richedit/ns-richedit-gettextlengthex) que recebe as informações de comprimento do texto.

</dd> <dt>

*lParam* 
</dt> <dd>

Esse parâmetro não é usado; Ele deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

A mensagem retorna o número de **TCHAR** s no controle de edição, dependendo da configuração dos sinalizadores na estrutura [**GETTEXTLENGTHEX**](/windows/desktop/api/Richedit/ns-richedit-gettextlengthex) . Se sinalizadores incompatíveis tiverem sido definidos no membro **flags** , a mensagem retornará E \_ INVALIDARG.

## <a name="remarks"></a>Comentários

Essa mensagem é uma maneira rápida e fácil de determinar o número de caracteres na versão Unicode do controle rich edit. No entanto, para uma página de código de destino não-Unicode, você poderá converter potencialmente em uma combinação de caracteres de byte único e de byte duplo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**GETTEXTLENGTHEX**](/windows/desktop/api/Richedit/ns-richedit-gettextlengthex)
</dt> </dl>

 

 





