---
title: Mensagem de EM_GETSEL (WinUser. h)
description: Obtém as posições de caractere inicial e final (em TCHARs) da seleção atual em um controle de edição. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.
ms.assetid: cf12aaea-cfa7-4804-ae34-fd0992332288
keywords:
- controles de Windows de mensagem de EM_GETSEL
topic_type:
- apiref
api_name:
- EM_GETSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dca5f3cf1fdaa3c40dd1bb25ebbabb672474e76ae621a05cf52247c216adca17
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048796"
---
# <a name="em_getsel-message"></a>\_Mensagem em GETSEL

Obtém as posições de caractere inicial e final (em **TCHAR** s) da seleção atual em um controle de edição. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um ponteiro para um valor **DWORD** que recebe a posição inicial da seleção. Este parâmetro pode ser **NULL**.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para um valor **DWORD** que recebe a posição do primeiro caractere não selecionado após o final da seleção. Este parâmetro pode ser **NULL**.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é um valor de base zero com a posição inicial da seleção no [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) e a posição do primeiro **TCHAR** após o último **TCHAR** selecionado no [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)). Se um desses valores exceder 65.535, o valor de retorno será-1.

É melhor usar os valores retornados em *wParam* e *lParam* porque eles são valores completos de 32 bits.

## <a name="remarks"></a>Comentários

Se não houver seleção, os valores inicial e final serão a posição do cursor.

**Controles de edição avançados:** Você também pode usar a mensagem em [**\_ EXGETSEL**](em-exgetsel.md) para recuperar as mesmas informações. **Em \_ EXGETSEL** também retorna posições de caractere inicial e final como valores de 32 bits.

**Edição avançada:** Com suporte no Microsoft Rich Edit 1,0 e posterior. Para obter informações sobre a compatibilidade das versões de edição rica com as várias versões do sistema, consulte [sobre controles de edição avançados](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**em \_ EXGETSEL**](em-exgetsel.md)
</dt> <dt>

[**em \_ SETSEL**](em-setsel.md)
</dt> </dl>

 

