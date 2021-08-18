---
title: MPCOMPONENT_VERSION estrutura (MpClient.h)
description: Versão e tempo de atualização para um componente individual.
ms.assetid: 43468230-EE13-4630-8C09-F8DF983EF748
keywords:
- MPCOMPONENT_VERSION estrutura herdada Windows recursos de ambiente
- PMPCOMPONENT_VERSION de estrutura herdado Windows recursos de ambiente
topic_type:
- apiref
api_name:
- MPCOMPONENT_VERSION
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6092fe2f3ec7ba921b1ef3adfc9355feeeae67f2381836056f2af65b276921cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976066"
---
# <a name="mpcomponent_version-structure"></a>Estrutura MPCOMPONENT \_ VERSION

Versão e tempo de atualização para um componente individual.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct tagMPCOMPONENT_VERSION {
  ULONGLONG      Version;
  ULARGE_INTEGER UpdateTime;
} MPCOMPONENT_VERSION, *PMPCOMPONENT_VERSION;
```



## <a name="members"></a>Membros

<dl> <dt>

**Versão**
</dt> <dd>

Tipo: **ULONGLONG**

</dd> <dd>

Campo de versão. Cada **WORD** representa principal, secundário, build e revisão.

</dd> <dt>

**UpdateTime**
</dt> <dd>

Tipo: **ULARGE \_ INTEGER**

</dd> <dd>

Hora da última atualização do componente, no **formato FILETIME.**

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 





