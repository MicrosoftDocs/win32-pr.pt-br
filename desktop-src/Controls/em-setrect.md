---
title: Mensagem de EM_SETRECT (WinUser. h)
description: EM_SETRECT mensagem – define o retângulo de formatação de um controle de edição de várias linhas.
ms.assetid: 4f576e94-3bd3-4416-a960-b7f22da963ea
keywords:
- Controles de EM_SETRECT de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_SETRECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 042428a236b8e9a23f03cdcceaf5d76eb977efd8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085964"
---
# <a name="em_setrect-message"></a>\_Mensagem em SETrect

Define o [retângulo de formatação](about-edit-controls.md) de um controle de edição de várias linhas. O retângulo de formatação é o retângulo limitador no qual o controle desenha o texto. O retângulo de limitação é independente do tamanho da janela de controle de edição.

Essa mensagem é processada somente por controles de edição de várias linhas. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

**Edição avançada 2,0 e posterior:** Indica se *lParam* especifica coordenadas absolutas ou relativas. Um valor de zero indica coordenadas absolutas. Um valor de 1 indica deslocamentos relativos ao retângulo de formatação atual. (Os deslocamentos podem ser positivos ou negativos.)

**Editar controles e edição avançada 1,0:** Esse parâmetro não é usado e deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) que especifica as novas dimensões do retângulo. Se esse parâmetro for **NULL**, o retângulo de formatação será definido com seus valores padrão.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Essa mensagem não retorna um valor.

## <a name="remarks"></a>Comentários

Definir *lParam* como **nulo** não terá efeito se um dispositivo de toque estiver instalado ou se **em \_ SetRect** for enviado de um thread que tenha um gancho instalado (consulte [**SetWindowsHookEx**](/windows/desktop/api/winuser/nf-winuser-setwindowshookexa)). Nesses casos, *lParam* deve conter um ponteiro válido para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) .

A mensagem em **\_ SetRect** faz com que o texto do controle de edição seja redesenhado. Para alterar o tamanho do retângulo de formatação sem redesenhar o texto, use a mensagem [**em \_ SETRECTNP**](em-setrectnp.md) .

Quando um controle de edição é criado pela primeira vez, o retângulo de formatação é definido como um tamanho padrão. Você pode usar a mensagem com **\_ SetRect** para tornar o retângulo de formatação maior ou menor do que a janela de controle de edição.

Se o controle de edição não tiver uma barra de rolagem horizontal e o retângulo de formatação for definido como maior que a janela de controle de edição, as linhas de texto que excedem a largura da janela de controle de edição (mas menor que a largura do retângulo de formatação) serão recortadas em vez de encapsuladas.

Se o controle de edição contiver uma borda, o retângulo de formatação será reduzido pelo tamanho da borda. Se você estiver ajustando o retângulo retornado por uma mensagem em [**\_ GetRect**](em-getrect.md) , deverá remover o tamanho da borda antes de usar o retângulo com a mensagem de **\_ SetRect** .

**Edição avançada:** Com suporte no Microsoft Rich Edit 1,0 e posterior. O retângulo de formatação não inclui a barra de seleção, que é uma área desmarcada à esquerda de cada parágrafo. Quando o usuário clica na barra de seleção, a linha correspondente é selecionada. Para obter informações sobre a compatibilidade das versões de edição rica com as várias versões do sistema, consulte [sobre controles de edição avançados](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

**Referência**
</dt> <dt>

[**em \_ GETrect**](em-getrect.md)
</dt> <dt>

[**em \_ SETRECTNP**](em-setrectnp.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**RECT**](/previous-versions//dd162897(v=vs.85))
</dt> </dl>

 

