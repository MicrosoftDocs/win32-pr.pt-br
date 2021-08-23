---
title: EM_GETRECT mensagem (Winuser.h)
description: Obtém o retângulo de formatação de um controle de edição.
ms.assetid: eef0150d-9b7a-4247-acbf-6fea2efd1dc3
keywords:
- EM_GETRECT controles Windows mensagem
topic_type:
- apiref
api_name:
- EM_GETRECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1d4ad7dbab40a8d294d814e3524b54c5b11206c91608e9293bdf88df2a63f23
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119541036"
---
# <a name="em_getrect-message"></a>Mensagem \_ EM GETRECT

Obtém [o retângulo de formatação](about-edit-controls.md) de um controle de edição. O retângulo de formatação é o retângulo limitante no qual o controle desenha o texto. O retângulo de limitação é independente do tamanho da janela de controle de edição. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma [**estrutura RECT**](/previous-versions//dd162897(v=vs.85)) que recebe o retângulo de formatação.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno não é significativo.

## <a name="remarks"></a>Comentários

Você pode modificar o retângulo de formatação de um controle de edição multilinha usando as mensagens [**EM \_ SETRECT**](em-setrect.md) e [**EM \_ SETRECTNP.**](em-setrectnp.md)

Sob determinadas condições, **EM \_ GETRECT** pode não retornar os valores exatos definidos pelo [**EM \_ SETRECT**](em-setrect.md) ou [**EM \_ SETRECTNP,**](em-setrectnp.md) mas poderá estar desligado em alguns pixels.

**Edição rica:** Com suporte no Microsoft Rich Edit 1.0 e posterior. O retângulo de formatação não inclui a barra de seleção, que é uma área não marcada à esquerda de cada parágrafo. Quando clicado, a barra de seleção seleciona a linha. Para obter informações sobre a compatibilidade de versões de edição rich com as várias versões do sistema, consulte [Sobre controles de edição rich](about-rich-edit-controls.md).

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

[**EM \_ SETRECTNP**](em-setrectnp.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**Rect**](/previous-versions//dd162897(v=vs.85))
</dt> </dl>

 

