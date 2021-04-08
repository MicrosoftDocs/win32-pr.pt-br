---
title: Mensagem de EM_CANUNDO (WinUser. h)
description: Determina se há alguma ação em uma fila de desfazer do controle de edição. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.
ms.assetid: ae7ff372-b1f8-4ab7-9a7e-450aed3e0bc5
keywords:
- Controles de EM_CANUNDO de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_CANUNDO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 345367b25790051a444363bb9bbc02af3d6fb0fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085830"
---
# <a name="em_canundo-message"></a>\_Mensagem em CANundo

Determina se há alguma ação em uma fila de desfazer do controle de edição. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Não usado; deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Não usado; deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se houver ações na fila de desfazer do controle, o valor de retorno será diferente de zero.

Se a fila de desfazer estiver vazia, o valor de retorno será zero.

## <a name="remarks"></a>Comentários

Se a fila de desfazer não estiver vazia, você poderá enviar a mensagem em [**\_ desfazer**](em-undo.md) para o controle para desfazer a operação mais recente.

**Editar controles e edição avançada 1,0:** A fila de desfazer contém apenas a operação mais recente.

**Edição avançada 2,0 e posterior:** A fila de desfazer pode conter várias operações.

**Edição avançada:** Com suporte no Microsoft Rich Edit 1,0 e posterior. Para obter informações sobre a compatibilidade das versões de edição rica com as várias versões do sistema, consulte [sobre controles de edição avançados](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**em \_ desfazer**](em-undo.md)
</dt> </dl>

 

 





