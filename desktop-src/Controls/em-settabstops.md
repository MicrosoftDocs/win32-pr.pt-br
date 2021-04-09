---
title: Mensagem de EM_SETTABSTOPS (WinUser. h)
description: A \_ mensagem em SETtabstops define as paradas de tabulação em um controle de edição de várias linhas.
ms.assetid: d6fe2828-4ae9-4652-ace0-2f71e146f777
keywords:
- Controles de EM_SETTABSTOPS de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_SETTABSTOPS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48d076dea415f169eff46101fd7cfe632d73d976
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085733"
---
# <a name="em_settabstops-message"></a>\_Mensagem em SETtabstops

A mensagem em **\_ SetTabStops** define as paradas de tabulação em um controle de edição de várias linhas. Quando o texto é copiado para o controle, qualquer caractere de tabulação no texto faz com que o espaço seja gerado até a próxima parada de tabulação.

Essa mensagem é processada somente por controles de edição de várias linhas. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O número de paradas de tabulação contidas na matriz. Se esse parâmetro for zero, o parâmetro *lParam* será ignorado e as tabulações padrão serão definidas a cada unidades de modelo de caixa de diálogo de 32. Se esse parâmetro for 1, as paradas de tabulação serão definidas a cada *n* unidades de modelo de caixa de diálogo, em que *n* é a distância apontada pelo parâmetro *lParam* . Se esse parâmetro for maior que 1, *lParam* será um ponteiro para uma matriz de paradas de tabulação.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma matriz de inteiros sem sinal especificando as paradas de tabulação, em unidades de modelo de caixa de diálogo. Se o parâmetro *wParam* for 1, esse parâmetro será um ponteiro para um inteiro não assinado que contém a distância entre todas as paradas de tabulação, em unidades de modelo de caixa de diálogo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se todas as guias estiverem definidas, o valor de retorno será **true**.

Se todas as guias não estiverem definidas, o valor de retorno será **false**.

## <a name="remarks"></a>Comentários

A mensagem em **\_ SetTabStops** não redesenha automaticamente a janela de controle de edição. Se o aplicativo estiver alterando as paradas de tabulação para o texto já no controle de edição, ele deverá chamar a função [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) para redesenhar a janela de controle de edição.

Os valores especificados na matriz estão em unidades de modelo de caixa de diálogo, que são as unidades independentes de dispositivo usadas em modelos de caixas de diálogo. Para converter medidas de unidades de modelo de caixa de diálogo em unidades de tela (pixels), use a função [**MapDialogRect**](/windows/desktop/api/winuser/nf-winuser-mapdialogrect) .

**Edição avançada:** Com suporte no Microsoft Rich Edit 3,0 e posterior. Um controle de edição rico pode ter o número máximo de paradas de tabulação especificado pelo máximo de \_ paradas de tabulação \_ . Para obter informações sobre a compatibilidade das versões de edição rica com as várias versões do sistema, consulte [sobre controles de edição avançados](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Outros recursos**
</dt> <dt>

[**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect)
</dt> <dt>

[**MapDialogRect**](/windows/desktop/api/winuser/nf-winuser-mapdialogrect)
</dt> </dl>

 

