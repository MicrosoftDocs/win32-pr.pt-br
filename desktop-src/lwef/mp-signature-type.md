---
title: MP_SIGNATURE_TYPE enumeração (MpClient.h)
description: Possíveis tipos de assinatura.
ms.assetid: 44B195A8-866D-4B87-9576-54E00658F9B3
keywords:
- MP_SIGNATURE_TYPE de enumeração herdada Windows recursos de ambiente
- PMP_SIGNATURE_TYPE de enumeração herdado Windows recursos de ambiente
topic_type:
- apiref
api_name:
- MP_SIGNATURE_TYPE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3289f0cbc3eeb85f553adf97078b7d3c5c53a686e914f86a4edb80c5244f72af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117883709"
---
# <a name="mp_signature_type-enumeration"></a>\_Enumeração MP SIGNATURE \_ TYPE

Possíveis tipos de assinatura.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagMP_SIGNATURE_TYPE { 
  MP_SIGNATURE_ANTIMALWARE     = 0,
  MP_SIGNATURE_ANTIVIRUS       = 1,
  MP_SIGNATURE_ANTISPYWARE     = 2,
  MP_SIGNATURE_NIS             = 3,
  MP_SIGNATURE_TYPES_MAXVALUE  = 3
} MP_SIGNATURE_TYPE, *PMP_SIGNATURE_TYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="MP_SIGNATURE_ANTIMALWARE"></span><span id="mp_signature_antimalware"></span>**\_ANTIMALWARE DE ASSINATURA DO MP \_**
</dt> <dd>

Assinaturas antivírus e antispyware.

</dd> <dt>

<span id="MP_SIGNATURE_ANTIVIRUS"></span><span id="mp_signature_antivirus"></span>**MP \_ SIGNATURE \_ ANTIVÍRUS**
</dt> <dd>

Somente assinaturas antivírus.

</dd> <dt>

<span id="MP_SIGNATURE_ANTISPYWARE"></span><span id="mp_signature_antispyware"></span>**\_ANTISPYWARE DE ASSINATURA DO MP \_**
</dt> <dd>

Somente assinaturas antispyware.

</dd> <dt>

<span id="MP_SIGNATURE_NIS"></span><span id="mp_signature_nis"></span>**\_ \_ NIS DE ASSINATURA DO MP**
</dt> <dd>

Assinaturas NIS.

</dd> <dt>

<span id="MP_SIGNATURE_TYPES_MAXVALUE"></span><span id="mp_signature_types_maxvalue"></span>**TIPOS DE ASSINATURA DO MP \_ \_ \_ MAXVALUE**
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 





