---
title: EM_SETRECTNP mensagem (Winuser.h)
description: EM_SETRECTNP mensagem – define o retângulo de formatação de um controle de edição multilinha.
ms.assetid: 1ab497ca-023f-4c26-b92d-b441a0d7b90c
keywords:
- EM_SETRECTNP controles Windows mensagem
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
ms.openlocfilehash: 60341a41706f012064d3b7cbc79aa019f1492c3a8d535866fa51fc7ea8dfd437
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117831127"
---
# <a name="em_setrectnp-message"></a>Mensagem \_ EM SETRECTNP

Define o [retângulo de formatação](about-edit-controls.md) de um controle de edição multilinha. A **mensagem EM \_ SETRECTNP** é idêntica à mensagem [**EM \_ SETRECT,**](em-setrect.md) exceto que **EM \_ SETRECTNP** não *redesenha* a janela de controle de edição.

O retângulo de formatação é o retângulo limitante no qual o controle desenha o texto. O retângulo de limitação é independente do tamanho da janela de controle de edição.

Essa mensagem é processada somente por controles de edição multilinha. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

**Rich Edit 3.0 e posterior:** Indica se o novo retângulo contém coordenadas absolutas ou relativas. Um valor de zero indica coordenadas absolutas. Um valor de 1 indica deslocamentos relativos ao retângulo de formatação atual. (Os deslocamentos podem ser positivos ou negativos.)

**Editar controles:** Esse parâmetro não é usado e deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma [**estrutura RECT**](/previous-versions//dd162897(v=vs.85)) que especifica as novas dimensões do retângulo. Se esse parâmetro for **NULL,** o retângulo de formatação será definido como seus valores padrão.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Essa mensagem não retorna um valor.

## <a name="remarks"></a>Comentários

**Edição rica:** Com suporte no Microsoft Rich Edit 3.0 e posterior. Para obter informações sobre a compatibilidade de versões de edição rich com as várias versões do sistema, consulte [Sobre controles de edição rich](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**EM \_ SETRECT**](em-setrect.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**Rect**](/previous-versions//dd162897(v=vs.85))
</dt> </dl>

 

