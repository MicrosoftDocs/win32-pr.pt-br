---
title: PBM_SETSTEP mensagem (Commctrl.h)
description: Especifica o incremento da etapa para uma barra de progresso. O incremento da etapa é a quantidade pela qual a barra de progresso aumenta sua posição atual sempre que recebe uma mensagem \_ DE ETAPA DO PBM. Por padrão, o incremento da etapa é definido como 10.
ms.assetid: 75c1085b-6c7a-4c44-9a12-f9bf21f7d945
keywords:
- PBM_SETSTEP controles de Windows mensagem
topic_type:
- apiref
api_name:
- PBM_SETSTEP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b88508654565cb3af05dd768ef7ef1e54e5ef0ee80e0797bc45631f6e3fe6912
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119798766"
---
# <a name="pbm_setstep-message"></a>Mensagem PBM \_ SETSTEP

Especifica o incremento da etapa para uma barra de progresso. O incremento da etapa é a quantidade pela qual a barra de progresso aumenta sua posição atual sempre que recebe uma mensagem [**\_ DE ETAPA DO PBM.**](pbm-stepit.md) Por padrão, o incremento da etapa é definido como 10.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Novo incremento de etapa.

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o incremento da etapa anterior.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





