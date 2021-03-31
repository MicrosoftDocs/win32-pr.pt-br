---
description: A estrutura CONFIGUREDEXPERT associa um especialista aos seus dados de configuração.
ms.assetid: 96a6650b-6d6f-495e-83bb-385d44ff015d
title: Estrutura CONFIGUREDEXPERT (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CONFIGUREDEXPERT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 3f3d40bf5d38c6b5151691a7d15bd93bef01eee5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169707"
---
# <a name="configuredexpert-structure"></a>Estrutura CONFIGUREDEXPERT

A estrutura **CONFIGUREDEXPERT** associa um especialista aos seus dados de configuração.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct {
  HEXPERT       hExpert;
  DWORD         StartupFlags;
  PEXPERTCONFIG pConfig;
} CONFIGUREDEXPERT, *PCONFIGUREDEXPERT;
```



## <a name="members"></a>Membros

<dl> <dt>

**hExpert**
</dt> <dd>

Lide com um especialista.

</dd> <dt>

**StartupFlags**
</dt> <dd>

Os valores do sinalizador de inicialização do especialista.

</dd> <dt>

**pConfig**
</dt> <dd>

Ponteiro para uma estrutura [**EXPERTCONFIG**](expertconfig.md) .

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




