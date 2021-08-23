---
title: Mensagem de EM_SETREADONLY (WinUser. h)
description: Define ou remove o estilo somente leitura (ES \_ ReadOnly) de um controle de edição. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.
ms.assetid: a10b3f57-0e67-4a0f-89f3-9c8ebd1514f8
keywords:
- controles de Windows de mensagem de EM_SETREADONLY
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
ms.openlocfilehash: d46726c1247f7ef93c00e495ca77ad3d337253705bd3018a0480fc9588c22f8d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119437506"
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

## <a name="return-value"></a>Valor retornado

Se a operação for concluída com sucesso, o valor de retorno será diferente de zero.

Se a operação falhar, o valor de retorno será zero.

## <a name="remarks"></a>Comentários

Quando um controle de edição tem o estilo [**es \_ ReadOnly**](edit-control-styles.md) , o usuário não pode alterar o texto dentro do controle de edição.

Para determinar se um controle de edição tem o estilo [**es \_ ReadOnly**](edit-control-styles.md) , use a função [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) com o \_ sinalizador de estilo GWL.

**Edição avançada:** Com suporte no Microsoft Rich Edit 1,0 e posterior. Para obter informações sobre a compatibilidade das versões de edição rica com as várias versões do sistema, consulte [sobre controles de edição avançados](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga)
</dt> </dl>

 

