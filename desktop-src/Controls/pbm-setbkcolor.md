---
title: PBM_SETBKCOLOR mensagem (Commctrl.h)
description: Define a cor da tela de fundo na barra de progresso.
ms.assetid: e28af958-babb-4c2e-9202-89b608c22f8e
keywords:
- PBM_SETBKCOLOR controles Windows mensagem
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
ms.openlocfilehash: 54bdee330aba5a4ff96fc5b26fa7f99553ff8331dd8822fcd350fbae5813c813
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986176"
---
# <a name="pbm_setbkcolor-message"></a>Mensagem PBM \_ SETBKCOLOR

Define a cor da tela de fundo na barra de progresso.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

**Valor COLORREF** que especifica a nova cor da tela de fundo. Especifique o valor \_ CLR DEFAULT para fazer com que a barra de progresso use sua cor de plano de fundo padrão.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna a cor da tela de fundo anterior ou CLR \_ DEFAULT se a cor da tela de fundo for a cor padrão.

## <a name="remarks"></a>Comentários

Quando os estilos visuais estão habilitados, essa mensagem não tem nenhum efeito.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





