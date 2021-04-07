---
title: Estrutura de MPCOMPONENT_VERSION (MpClient. h)
description: Versão e tempo de atualização para um componente individual.
ms.assetid: 43468230-EE13-4630-8C09-F8DF983EF748
keywords:
- Recursos do ambiente Windows herdado da estrutura de MPCOMPONENT_VERSION
- Ponteiro de estrutura de PMPCOMPONENT_VERSION recursos de ambiente herdados do Windows
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
ms.openlocfilehash: 9a1d4b5011bb185dc8ca0892e0a0e65bc4a7d8b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918395"
---
# <a name="mpcomponent_version-structure"></a>Estrutura de versão do MPCOMPONENT \_

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

Campo de versão. Cada **palavra** representa principal, secundária, compilação e revisão.

</dd> <dt>

**UpdateTime**
</dt> <dd>

Tipo: **ULARGE \_ inteiro**

</dd> <dd>

Hora da última atualização do componente, no formato **FILETIME** .

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





