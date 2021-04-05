---
title: Mensagem de EM_SETRECTNP (WinUser. h)
description: Define o retângulo de formatação de um controle de edição de várias linhas.
ms.assetid: 1ab497ca-023f-4c26-b92d-b441a0d7b90c
keywords:
- Controles de EM_SETRECTNP de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_SETRECTNP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e017bd4737c843c2452382918d71ef63345917cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918982"
---
# <a name="em_setrectnp-message"></a>\_Mensagem em SETRECTNP

Define o [retângulo de formatação](about-edit-controls.md) de um controle de edição de várias linhas. A mensagem em **\_ SETRECTNP** é idêntica à mensagem [**em \_ SetRect**](em-setrect.md) , exceto que em **\_ SETRECTNP** *não* redesenha a janela de controle de edição.

O retângulo de formatação é o retângulo limitador no qual o controle desenha o texto. O retângulo de limitação é independente do tamanho da janela de controle de edição.

Essa mensagem é processada somente por controles de edição de várias linhas. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

**Edição avançada 3,0 e posterior:** Indica se o novo retângulo contém coordenadas absolutas ou relativas. Um valor de zero indica coordenadas absolutas. Um valor de 1 indica deslocamentos relativos ao retângulo de formatação atual. (Os deslocamentos podem ser positivos ou negativos.)

**Controles de edição:** Esse parâmetro não é usado e deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) que especifica as novas dimensões do retângulo. Se esse parâmetro for **NULL**, o retângulo de formatação será definido com seus valores padrão.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa mensagem não retorna um valor.

## <a name="remarks"></a>Comentários

**Edição avançada:** Com suporte no Microsoft Rich Edit 3,0 e posterior. Para obter informações sobre a compatibilidade das versões de edição rica com as várias versões do sistema, consulte [sobre controles de edição avançados](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**em \_ SETrect**](em-setrect.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**RECT**](/previous-versions//dd162897(v=vs.85))
</dt> </dl>

 

