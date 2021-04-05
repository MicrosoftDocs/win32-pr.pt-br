---
title: Mensagem de EM_SETREADONLY (WinUser. h)
description: Define ou remove o estilo somente leitura (ES \_ ReadOnly) de um controle de edição. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.
ms.assetid: a10b3f57-0e67-4a0f-89f3-9c8ebd1514f8
keywords:
- Controles de EM_SETREADONLY de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_SETREADONLY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0b224e11212077703ab62ab6a180875672c879e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085500"
---
# <a name="em_setreadonly-message"></a>\_Mensagem em SETreadonly

Define ou remove o estilo somente leitura ([**es \_ ReadOnly**](edit-control-styles.md)) de um controle de edição. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica se é para definir ou remover o estilo [**es \_ ReadOnly**](edit-control-styles.md) . Um valor **true** define o estilo **es \_ ReadOnly** ; um valor **false** remove o estilo **es \_ ReadOnly** .

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a operação for concluída com sucesso, o valor de retorno será diferente de zero.

Se a operação falhar, o valor de retorno será zero.

## <a name="remarks"></a>Comentários

Quando um controle de edição tem o estilo [**es \_ ReadOnly**](edit-control-styles.md) , o usuário não pode alterar o texto dentro do controle de edição.

Para determinar se um controle de edição tem o estilo [**es \_ ReadOnly**](edit-control-styles.md) , use a função [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) com o \_ sinalizador de estilo GWL.

**Edição avançada:** Com suporte no Microsoft Rich Edit 1,0 e posterior. Para obter informações sobre a compatibilidade das versões de edição rica com as várias versões do sistema, consulte [sobre controles de edição avançados](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga)
</dt> </dl>

 

