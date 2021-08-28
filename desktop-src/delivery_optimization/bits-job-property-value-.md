---
title: BITS_JOB_PROPERTY_VALUE (Deliveryoptimization.h)
description: A BITS_JOB_PROPERTY_VALUE de dados fornece o valor da propriedade do trabalho DO com base no valor da enumeração BITS_JOB_PROPERTY_ID dados.
ms.assetid: C24D9EA1-2E72-4403-939A-7B01D7133FE7
keywords:
- BITS_JOB_PROPERTY_VALUE estrutura
- BITS_JOB_PROPERTY_VALUE estrutura
topic_type:
- apiref
api_name:
- BITS_JOB_PROPERTY_VALUE
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7f7366f993f23a16aa6c0d4486c33f45cd501962add9ab524a008aba51cd8ec9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755726"
---
# <a name="bits_job_property_value-structure"></a>BITS_JOB_PROPERTY_VALUE estrutura

A **BITS_JOB_PROPERTY_VALUE** de dados fornece o valor da propriedade do trabalho DO com base no valor da [**enumeração BITS_JOB_PROPERTY_ID**](bits-job-property-id.md) dados.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct {
  DWORD          Dword;
  GUID           ClsID;
  BOOL           Enable;
  UINT64         Uint64;
  BG_AUTH_TARGET Target;
} BITS_JOB_PROPERTY_VALUE;
```



## <a name="members"></a>Membros

<dl> <dt>

**Dword**
</dt> <dd>

Esse valor é retornado ao usar a ID da propriedade enum **BITS_JOB_PROPERTY_ID_COST_FLAGS** e é aplicado como a política de [transferência](https://www.bing.com/search?q=transfer+policy) no trabalho do DO.

</dd> <dt>

**Clsid**
</dt> <dd>

Esse valor é retornado ao usar a ID da propriedade enum **BITS_JOB_PROPERTY_NOTIFICATION_CLSID** e representa o CLSID do objeto de retorno de chamada a ser registrado com o trabalho DO.

</dd> <dt>

**Habilitar**
</dt> <dd>

Sem suporte.

</dd> <dt>

**Uint64**
</dt> <dd>

Sem suporte.

</dd> <dt>

**Target (destino)**
</dt> <dd>

Sem suporte.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, versão 1709 somente para \[ aplicativos da área de trabalho\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows Servidor, versão 1709 somente \[ aplicativos da área de trabalho\]<br/>                                     |
| Cabeçalho<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**BITS_JOB_PROPERTY_ID**](bits-job-property-id.md)
</dt> <dt>

[**BITS_JOB_TRANSFER_POLICY**](bits-job-transfer-policy-.md)
</dt> </dl>

 

 





