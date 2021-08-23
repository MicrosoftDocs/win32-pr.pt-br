---
title: UDM_SETACCEL mensagem (Commctrl.h)
description: Define a aceleração para um controle de cima para baixo.
ms.assetid: af1d0a34-13ba-4bda-82f5-d7afab6bb1ed
keywords:
- UDM_SETACCEL controles de Windows mensagem
topic_type:
- apiref
api_name:
- UDM_SETACCEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc746e33c14de0dd177ecc31fc237be7cb8be36280bb2a5ceadff31d2b286ec1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957735"
---
# <a name="udm_setaccel-message"></a>Mensagem UDM \_ SETACCEL

Define a aceleração para um controle de cima para baixo.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Número de [**estruturas UDACCEL**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel) especificadas por *aAccels.*

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma matriz de [**estruturas UDACCEL**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel) que contêm informações de aceleração. Os elementos devem ser classificação em ordem crescente com base no **membro nSec.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna **TRUE se** for bem-sucedido ou FALSE **caso** contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**UDM \_ GETACCEL**](udm-getaccel.md)
</dt> </dl>

 

 





