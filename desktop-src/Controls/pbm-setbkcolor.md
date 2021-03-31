---
title: Mensagem de PBM_SETBKCOLOR (commctrl. h)
description: Define a cor do plano de fundo na barra de progresso.
ms.assetid: e28af958-babb-4c2e-9202-89b608c22f8e
keywords:
- Controles de PBM_SETBKCOLOR de mensagens do Windows
topic_type:
- apiref
api_name:
- PBM_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ddfaf84695221cf998275d76a9d2d67773150da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644909"
---
# <a name="pbm_setbkcolor-message"></a>Mensagem do SETBKCOLOR do PBM \_

Define a cor do plano de fundo na barra de progresso.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Valor **COLORREF** que especifica a nova cor do plano de fundo. Especifique o \_ valor padrão do CLR para fazer com que a barra de progresso Use sua cor de plano de fundo padrão.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna a cor do plano de fundo anterior ou o \_ padrão CLR se a cor do plano de fundo for a cor padrão.

## <a name="remarks"></a>Comentários

Quando os estilos visuais são habilitados, essa mensagem não tem nenhum efeito.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





