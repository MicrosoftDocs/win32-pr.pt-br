---
title: WINBIO_POLICY_SOURCE enumeração (Tipos \_ Winbio.h)
description: Lista as possíveis fontes de informações de política para a detecção de fraudes para fatores biométricos.
ms.assetid: 3DC3BB0B-1FD7-473C-8E0B-B7E0A4A44E9E
keywords:
- WINBIO_POLICY_SOURCE enumeração Windows API do Biometric Framework
- PWINBIO_POLICY_SOURCE de enumeração Windows API do Biometric Framework
topic_type:
- apiref
api_name:
- WINBIO_POLICY_SOURCE
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 962d4bc3e8cffb778df56d78a9ddaf0641f57f8f96c8f7b024745a4b879f2f81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118909925"
---
# <a name="winbio_policy_source-enumeration"></a>Enumeração WINBIO \_ POLICY \_ SOURCE

Lista as possíveis fontes de informações de política para a detecção de fraudes para fatores biométricos.

## <a name="syntax"></a>Sintaxe


```C++
typedef enum _WINBIO_POLICY_SOURCE { 
  WINBIO_POLICY_UNKNOWN  = 0x00000000,
  WINBIO_POLICY_DEFAULT  = 0x00000001,
  WINBIO_POLICY_LOCAL    = 0x00000002,
  WINBIO_POLICY_ADMIN    = 0x00000003
} WINBIO_POLICY_SOURCE, *PWINBIO_POLICY_SOURCE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WINBIO_POLICY_UNKNOWN"></span><span id="winbio_policy_unknown"></span>**POLÍTICA WINBIO \_ \_ DESCONHECIDA**
</dt> <dd>

A origem da política é desconhecida.

</dd> <dt>

<span id="WINBIO_POLICY_DEFAULT"></span><span id="winbio_policy_default"></span>**WINBIO \_ POLICY \_ DEFAULT**
</dt> <dd>

A política é a política padrão que o Windows Biometric Framework fornece.

</dd> <dt>

<span id="WINBIO_POLICY_LOCAL"></span><span id="winbio_policy_local"></span>**WINBIO \_ POLICY \_ LOCAL**
</dt> <dd>

A política que o usuário individual definiu para sua conta usando o **Configurações** aplicativo. Essa política substitui a política padrão.

</dd> <dt>

<span id="WINBIO_POLICY_ADMIN"></span><span id="winbio_policy_admin"></span>**ADMINISTRADOR DE POLÍTICA DO WINBIO \_ \_**
</dt> <dd>

Uma política de grupo que o administrador de IT definiu para a empresa. Usuários individuais não podem substituir essa política.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 10 somente aplicativos da área de trabalho\]<br/>                                                                                                                              |
| Servidor mínimo com suporte<br/> | \[Windows Server 2016 somente aplicativos da área de trabalho\]<br/>                                                                                                                     |
| parâmetro<br/>                   | <dl> <dt>Winbio \_ types.h (inclua Winbio.h para aplicativos cliente ou \_ adaptadores Winbio.h para adaptadores)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**AÇÃO DE POLÍTICA \_ WINBIO ANTI \_ \_ SPOOF \_**](winbio-anti-spoof-policy-action.md)
</dt> </dl>

 

 





