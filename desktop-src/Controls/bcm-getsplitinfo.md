---
title: Mensagem de BCM_GETSPLITINFO (commctrl. h)
description: Obtém informações para um controle de botão de divisão. Envie essa mensagem explicitamente ou usando o botão \_ GetSplitInfo macro.
ms.assetid: d608440d-b8d8-4e32-9128-08b7566b185c
keywords:
- Controles de BCM_GETSPLITINFO de mensagens do Windows
topic_type:
- apiref
api_name:
- BCM_GETSPLITINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 162c5522fcb432e3d512f688ae24aa12d4d0d8e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918525"
---
# <a name="bcm_getsplitinfo-message"></a>\_Mensagem GETSPLITINFO do BCM

Obtém informações para um controle de botão de divisão. Envie essa mensagem explicitamente ou usando o [**botão \_ GetSplitInfo**](/windows/desktop/api/Commctrl/nf-commctrl-button_getsplitinfo) macro.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Deve ser zero.

</dd> <dt>

*lParam* \[ entrada, saída\]
</dt> <dd>

Um ponteiro para uma estrutura de [**\_ SPLITINFO de botão**](/windows/win32/api/commctrl/ns-commctrl-button_splitinfo) para receber informações sobre o botão. O chamador é responsável por alocar a memória para a estrutura. Defina o membro de **máscara** desta estrutura para determinar quais informações receber.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.

## <a name="remarks"></a>Comentários

Use esta mensagem somente com os estilos de botão [**BS \_ SPLITBUTTON**](button-styles.md) e [**BS \_ DEFSPLITBUTTON**](button-styles.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[Estilos de botão](button-styles.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Tipos de botão](button-types-and-styles.md)
</dt> </dl>

 

 





