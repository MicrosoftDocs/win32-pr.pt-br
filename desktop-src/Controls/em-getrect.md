---
title: Mensagem de EM_GETRECT (WinUser. h)
description: Obtém o retângulo de formatação de um controle de edição.
ms.assetid: eef0150d-9b7a-4247-acbf-6fea2efd1dc3
keywords:
- Controles de EM_GETRECT de mensagens do Windows
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
ms.openlocfilehash: 1a8192fd4c3aa7fbe953a36217f6b1408f055d8d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824475"
---
# <a name="em_getrect-message"></a>\_Mensagem em GETrect

Obtém o [retângulo de formatação](about-edit-controls.md) de um controle de edição. O retângulo de formatação é o retângulo limitador no qual o controle desenha o texto. O retângulo de limitação é independente do tamanho da janela de controle de edição. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) que recebe o retângulo de formatação.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno não é significativo.

## <a name="remarks"></a>Comentários

Você pode modificar o retângulo de formatação de um controle de edição de várias linhas usando as mensagens [**em \_ SETRECTNP**](em-setrectnp.md) [**\_ SetRect**](em-setrect.md) e em.

Em determinadas condições, **em \_ GetRect** pode não retornar os valores exatos que em [**\_ SetRect**](em-setrect.md) ou em [**\_ SETRECTNP**](em-setrectnp.md) defini-lo será aproximadamente correto, mas pode ser desativado por alguns pixels.

**Edição avançada:** Com suporte no Microsoft Rich Edit 1,0 e posterior. O retângulo de formatação não inclui a barra de seleção, que é uma área desmarcada à esquerda de cada parágrafo. Quando clicado, a barra de seleção seleciona a linha. Para obter informações sobre a compatibilidade das versões de edição rica com as várias versões do sistema, consulte [sobre controles de edição avançados](about-rich-edit-controls.md).

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

[**em \_ SETRECTNP**](em-setrectnp.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**RECT**](/previous-versions//dd162897(v=vs.85))
</dt> </dl>

 

