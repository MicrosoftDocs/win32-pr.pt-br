---
title: Mensagem de BCM_GETSPLITINFO (commctrl. h)
description: Obtém informações para um controle de botão de divisão. Envie essa mensagem explicitamente ou usando o botão \_ GetSplitInfo macro.
ms.assetid: d608440d-b8d8-4e32-9128-08b7566b185c
keywords:
- controles de Windows de mensagem de BCM_GETSPLITINFO
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
ms.openlocfilehash: 1ee0771c8999c6a805931a93ed28c245082d18e538856fde42b69622ee73f9a8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921636"
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

## <a name="return-value"></a>Valor retornado

Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.

## <a name="remarks"></a>Comentários

Use esta mensagem somente com os estilos de botão [**BS \_ SPLITBUTTON**](button-styles.md) e [**BS \_ DEFSPLITBUTTON**](button-styles.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



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

 

 





