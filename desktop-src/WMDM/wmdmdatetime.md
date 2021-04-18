---
title: Estrutura WMDMDATETIME
description: A estrutura WMDMDATETIME contém uma data e hora do dia.
ms.assetid: 47f3994d-66c6-47e4-803d-0c98c70eccc8
keywords:
- Estrutura WMDMDATETIME Windows Media Gerenciador de Dispositivos
- Ponteiro de estrutura PWMDMDATETIME Windows Media Gerenciador de Dispositivos
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
ms.openlocfilehash: 07acf706aa63a21edd27fb2ac206db3039249055
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105781069"
---
# <a name="wmdmdatetime-structure"></a>Estrutura WMDMDATETIME

A estrutura **WMDMDATETIME** contém uma data e hora do dia.

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

**Wano**
</dt> <dd>

O Word que contém o ano de quatro dígitos.

</dd> <dt>

**Wmês**
</dt> <dd>

O Word que contém o mês (1-12).

</dd> <dt>

**WDIA**
</dt> <dd>

O Word que contém o dia do mês (1-31).

</dd> <dt>

**Whora**
</dt> <dd>

O Word que contém a hora (0-23).

</dd> <dt>

**Wminuto**
</dt> <dd>

O Word que contém o minuto (0-59).

</dd> <dt>

**Wsegundo**
</dt> <dd>

O Word que contém o segundo (0-59).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>WMDM. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMDSPStorage:: GetDate**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-getdate)
</dt> <dt>

[**IWMDMStorage:: GetDate**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getdate)
</dt> <dt>

[**WMDMRIGHTS**](wmdmrights.md)
</dt> <dt>

[**Estruturas**](structures.md)
</dt> </dl>

 

 





