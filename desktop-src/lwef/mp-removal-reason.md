---
title: Enumeração de MP_REMOVAL_REASON (MpClient. h)
description: Motivo da remoção da assinatura FastPath.
ms.assetid: A09B4903-E53C-4DA1-BD0B-6DE0124FCAB3
keywords:
- recursos do ambiente de Windows herdado de enumeração de MP_REMOVAL_REASON
- Windows recursos de ambiente herdados do ponteiro de enumeração PMP_REMOVAL_REASON
topic_type:
- apiref
api_name:
- MP_REMOVAL_REASON
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bf4e0ad95ba67a1335ec6915d400b7a8ca219c37bb302036af0a5dca2cf7479
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117883756"
---
# <a name="mp_removal_reason-enumeration"></a>Enumeração do motivo da \_ remoção de MP \_

Motivo da remoção da assinatura FastPath.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagMP_REMOVAL_REASON { 
  MP_REMOVAL_UNKNOWN    = 0,
  MP_REMOVAL_MANUAL     = 1,
  MP_REMOVAL_AUTOMATIC  = 2
} MP_REMOVAL_REASON, *PMP_REMOVAL_REASON;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="MP_REMOVAL_UNKNOWN"></span><span id="mp_removal_unknown"></span>**remoção de MP \_ \_ desconhecida**
</dt> <dd>

Desconhecido.

</dd> <dt>

<span id="MP_REMOVAL_MANUAL"></span><span id="mp_removal_manual"></span>**\_manual de remoção de MP \_**
</dt> <dd>

Manual.

</dd> <dt>

<span id="MP_REMOVAL_AUTOMATIC"></span><span id="mp_removal_automatic"></span>**\_remoção \_ automática de MP**
</dt> <dd>

Automático.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8 \[ somente aplicativos da área de trabalho\]<br/>                                            |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





