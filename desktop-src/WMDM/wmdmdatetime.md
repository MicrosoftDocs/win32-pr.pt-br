---
title: Estrutura WMDMDATETIME
description: A estrutura WMDMDATETIME contém uma data e hora do dia.
ms.assetid: 47f3994d-66c6-47e4-803d-0c98c70eccc8
keywords:
- Estrutura WMDMDATETIME windows Media Gerenciador de Dispositivos
- Ponteiro de estrutura PWMDMDATETIME windows Media Gerenciador de Dispositivos
topic_type:
- apiref
api_name:
- WMDMDATETIME
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9648b4c2d1272dcf00d45277119b51f438dba23d9eaf5e7810451fb693e8cae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004626"
---
# <a name="wmdmdatetime-structure"></a>Estrutura WMDMDATETIME

A **estrutura WMDMDATETIME** contém uma data e hora do dia.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _WMDMDATETIME {
  WORD wYear;
  WORD wMonth;
  WORD wDay;
  WORD wHour;
  WORD wMinute;
  WORD wSecond;
} WMDMDATETIME, *PWMDMDATETIME;
```



## <a name="members"></a>Membros

<dl> <dt>

**wYear**
</dt> <dd>

Palavra que contém o ano de quatro dígitos.

</dd> <dt>

**wMonth**
</dt> <dd>

Palavra que contém o mês (1-12).

</dd> <dt>

**wDay**
</dt> <dd>

Palavra que contém o dia do mês (1-31).

</dd> <dt>

**wHour**
</dt> <dd>

Palavra que contém a hora (0-23).

</dd> <dt>

**wMinute**
</dt> <dd>

Palavra que contém o minuto (0-59).

</dd> <dt>

**wSecond**
</dt> <dd>

Palavra que contém o segundo (0-59).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmdm.idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMDSPStorage::GetDate**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-getdate)
</dt> <dt>

[**IWMDMStorage::GetDate**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getdate)
</dt> <dt>

[**WMDMRIGHTS**](wmdmrights.md)
</dt> <dt>

[**Estruturas**](structures.md)
</dt> </dl>

 

 





