---
title: Estrutura de MPTHREAT_INFOEX_UNUSED (MpClient. h)
description: Estrutura fictícia para ameaças de tipo de modificação sem comportamento.
ms.assetid: 3C5305CD-D533-47B5-ADD3-BD8DA05F2046
keywords:
- Recursos do ambiente Windows herdado da estrutura de MPTHREAT_INFOEX_UNUSED
- Ponteiro de estrutura de PMPTHREAT_INFOEX_UNUSED recursos de ambiente herdados do Windows
topic_type:
- apiref
api_name:
- MPTHREAT_INFOEX_UNUSED
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fed78d904bd03fee17676dced7c828aaea8d319d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085841"
---
# <a name="mpthreat_infoex_unused-structure"></a>\_ \_ Estrutura não utilizada do MPTHREAT INFOEX

Estrutura fictícia para ameaças de tipo de modificação sem comportamento.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct tagMPTHREAT_INFOEX_UNUSED {
  DWORD dwNone;
} MPTHREAT_INFOEX_UNUSED, *PMPTHREAT_INFOEX_UNUSED;
```



## <a name="members"></a>Membros

<dl> <dt>

**dwNone**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd></dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





