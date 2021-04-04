---
title: Estrutura de BITS_JOB_PROPERTY_VALUE (Deliveryoptimization. h)
description: A BITS_JOB_PROPERTY_VALUE Union fornece o valor da propriedade da função do trabalho com base no valor da enumeração BITS_JOB_PROPERTY_ID.
ms.assetid: C24D9EA1-2E72-4403-939A-7B01D7133FE7
keywords:
- Estrutura de BITS_JOB_PROPERTY_VALUE
- Estrutura de BITS_JOB_PROPERTY_VALUE
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
ms.openlocfilehash: c48c1fe550db51b6b838379d44df21c95fa95e41
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085550"
---
# <a name="bits_job_property_value-structure"></a>Estrutura de BITS_JOB_PROPERTY_VALUE

A **BITS_JOB_PROPERTY_VALUE** Union fornece o valor da propriedade da função do trabalho com base no valor da enumeração [**BITS_JOB_PROPERTY_ID**](bits-job-property-id.md) .

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

**DWORD**
</dt> <dd>

Esse valor é retornado ao usar a ID de propriedade de enumeração **BITS_JOB_PROPERTY_ID_COST_FLAGS** e é aplicado como a [política de transferência](https://www.bing.com/search?q=transfer+policy) no trabalho.

</dd> <dt>

**ClsID**
</dt> <dd>

Esse valor é retornado ao usar a ID de propriedade de enumeração **BITS_JOB_PROPERTY_NOTIFICATION_CLSID** e representa o CLSID do objeto de retorno de chamada a ser registrado no trabalho do.

</dd> <dt>

**Habilitar**
</dt> <dd>

Não há suporte.

</dd> <dt>

**UInt64**
</dt> <dd>

Não há suporte.

</dd> <dt>

**Target (destino)**
</dt> <dd>

Não há suporte.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**BITS_JOB_PROPERTY_ID**](bits-job-property-id.md)
</dt> <dt>

[**BITS_JOB_TRANSFER_POLICY**](bits-job-transfer-policy-.md)
</dt> </dl>

 

 





