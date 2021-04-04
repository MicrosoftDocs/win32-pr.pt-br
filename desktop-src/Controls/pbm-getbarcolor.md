---
title: Mensagem de PBM_GETBARCOLOR (commctrl. h)
description: Obtém a cor da barra de progresso.
ms.assetid: d046f7e4-e21e-4dd9-a7be-2bf820c3c492
keywords:
- Controles de PBM_GETBARCOLOR de mensagens do Windows
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
ms.openlocfilehash: 35586d3483d1d487f740a1a3d991c884c814f452
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085929"
---
# <a name="pbm_getbarcolor-message"></a>Mensagem do GETBARCOLOR do PBM \_

Obtém a cor da barra de progresso.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna a cor da barra de progresso.

## <a name="remarks"></a>Comentários

Essa é a cor definida pela mensagem [**\_ SETBARCOLOR do PBM**](pbm-setbarcolor.md) . O valor padrão é CLR \_ padrão, que é definido em commctrl. h.

Essa função afeta apenas o modo clássico, não qualquer estilo visual.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





