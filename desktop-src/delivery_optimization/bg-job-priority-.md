---
title: Enumeração de BG_JOB_PRIORITY (Deliveryoptimization. h)
description: A enumeração BG_JOB_PRIORITY define os valores constantes que especificam o nível de prioridade de um trabalho.
ms.assetid: AF1F1F6D-473A-49E5-B24D-644A70DF304C
keywords:
- Enumeração de BG_JOB_PRIORITY
- Enumeração de BG_JOB_PRIORITY
topic_type:
- apiref
api_name:
- BG_JOB_PRIORITY
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 45b1f0f3029cc6157f2f100b3324165cfac1b03b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009233"
---
# <a name="bg_job_priority-enumeration"></a>Enumeração de BG_JOB_PRIORITY

A enumeração **BG_JOB_PRIORITY** define os valores constantes que especificam o nível de prioridade de um trabalho.

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  BG_JOB_PRIORITY_FOREGROUND,
  BG_JOB_PRIORITY_HIGH,
  BG_JOB_PRIORITY_NORMAL,
  BG_JOB_PRIORITY_LOW
} BG_JOB_PRIORITY;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="BG_JOB_PRIORITY_FOREGROUND"></span><span id="bg_job_priority_foreground"></span>**BG_JOB_PRIORITY_FOREGROUND**
</dt> <dd>

Transfere o trabalho em primeiro plano. As transferências de primeiro plano competem pela largura de banda da rede com outros aplicativos, o que pode impedir a experiência de rede do usuário. Esse é o nível de prioridade mais alto.

</dd> <dt>

<span id="BG_JOB_PRIORITY_HIGH"></span><span id="bg_job_priority_high"></span>**BG_JOB_PRIORITY_HIGH**
</dt> <dd>

Transfere o trabalho em segundo plano. As transferências em segundo plano usam uma pequena porcentagem da largura de banda da rede.

</dd> <dt>

<span id="BG_JOB_PRIORITY_NORMAL"></span><span id="bg_job_priority_normal"></span>**BG_JOB_PRIORITY_NORMAL**
</dt> <dd>

O comportamento DO é o mesmo para todos os trabalhos que não sejam de primeiro plano. Consulte os comentários em BG_JOB_PRIORITY_HIGH para obter detalhes.

</dd> <dt>

<span id="BG_JOB_PRIORITY_LOW"></span><span id="bg_job_priority_low"></span>**BG_JOB_PRIORITY_LOW**
</dt> <dd>

O comportamento DO é o mesmo para todos os trabalhos que não sejam de primeiro plano. Consulte os comentários em BG_JOB_PRIORITY_HIGH para obter detalhes.

</dd> </dl>

## <a name="remarks"></a>Comentários

Várias transferências de primeiro e segundo plano podem ocorrer simultaneamente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Método ibackgroundcopyjob:: getanteriority**](ibackgroundcopyjob-getpriority.md)
</dt> <dt>

[**Método ibackgroundcopyjob:: setanteriority**](ibackgroundcopyjob-setpriority.md)
</dt> </dl>

 

 





