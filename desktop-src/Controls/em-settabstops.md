---
title: EM_SETTABSTOPS mensagem (Winuser.h)
description: A mensagem EM \_ SETTABSTOPS define as paradas da guia em um controle de edição multilinha.
ms.assetid: d6fe2828-4ae9-4652-ace0-2f71e146f777
keywords:
- EM_SETTABSTOPS controles de Windows mensagem
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
ms.openlocfilehash: c2bf8285bbc8830f784b6cf2cf6671634bf4339a418c163bc3962150d6cb6674
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048076"
---
# <a name="em_settabstops-message"></a>Mensagem EM \_ SETTABSTOPS

A **mensagem EM \_ SETTABSTOPS** define as paradas da guia em um controle de edição multilinha. Quando o texto é copiado para o controle, qualquer caractere de tabulação no texto faz com que o espaço seja gerado até a próxima parada de tabulação.

Essa mensagem é processada somente por controles de edição multilinha. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O número de paradas de tabulação contidas na matriz. Se esse parâmetro for zero, o *parâmetro lParam* será ignorado e as paradas de tabulação padrão serão definidas a cada 32 unidades de modelo de caixa de diálogo. Se esse parâmetro for 1, as paradas de tabulação serão definidas em cada *n* unidades de modelo de caixa de diálogo, em que *n* é a distância apontada pelo *parâmetro lParam.* Se esse parâmetro for maior que 1, *lParam* será um ponteiro para uma matriz de paradas de tabulação.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma matriz de inteiros sem sinal especificando as paradas de tabulação, em unidades de modelo de caixa de diálogo. Se o *parâmetro wParam* for 1, esse parâmetro será um ponteiro para um inteiro sem sinal que contém a distância entre todas as paradas de tabulação, em unidades de modelo de caixa de diálogo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se todas as guias estão definidas, o valor de retorno é **TRUE.**

Se todas as guias não estão definidas, o valor de retorno é **FALSE.**

## <a name="remarks"></a>Comentários

A **mensagem EM \_ SETTABSTOPS** não redesenha automaticamente a janela de controle de edição. Se o aplicativo estiver alterando as paradas de tabulação para texto já no controle de edição, ele deverá chamar a [**função InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) para redesenhar a janela de controle de edição.

Os valores especificados na matriz estão em unidades de modelo de caixa de diálogo, que são as unidades independentes de dispositivo usadas em modelos de caixa de diálogo. Para converter medidas de unidades de modelo de caixa de diálogo em unidades de tela (pixels), use a [**função MapDialogRect.**](/windows/desktop/api/winuser/nf-winuser-mapdialogrect)

**Edição rica:** Com suporte no Microsoft Rich Edit 3.0 e posterior. Um controle de edição rico pode ter o número máximo de paradas de tabulação especificado por MAX \_ TAB \_ STOPS. Para obter informações sobre a compatibilidade de versões de edição rich com as várias versões do sistema, consulte [Sobre controles de edição rich](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Outros recursos**
</dt> <dt>

[**Invalidaterect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect)
</dt> <dt>

[**Mapdialogrect**](/windows/desktop/api/winuser/nf-winuser-mapdialogrect)
</dt> </dl>

 

