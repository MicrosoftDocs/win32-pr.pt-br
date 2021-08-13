---
title: PBM_GETBARCOLOR mensagem (Commctrl.h)
description: Obtém a cor da barra de progresso.
ms.assetid: d046f7e4-e21e-4dd9-a7be-2bf820c3c492
keywords:
- PBM_GETBARCOLOR controles Windows mensagem
topic_type:
- apiref
api_name:
- PBM_GETBARCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cb42d878840ad05f0854ec7ca9cb50dc1b3be2a55b3b65ddf652d961b6d818b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119312436"
---
# <a name="pbm_getbarcolor-message"></a>Mensagem PBM \_ GETBARCOLOR

Obtém a cor da barra de progresso.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna a cor da barra de progresso.

## <a name="remarks"></a>Comentários

Essa é a cor definida pela mensagem [**PBM \_ SETBARCOLOR.**](pbm-setbarcolor.md) O valor padrão é CLR \_ DEFAULT, que é definido em commctrl.h.

Essa função afeta apenas o modo clássico, não qualquer estilo visual.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





