---
title: Método gratuito IMemoryAllocator
description: O método gratuito libera a memória alocada pelo método Allocate.
ms.assetid: 41f81cba-4431-4ff7-ac84-8ff5bea71b65
keywords:
- Armazenamento estruturado de método gratuito
- Armazenamento estruturado de método gratuito, interface IMemoryAllocator
- Armazenamento estruturado da interface IMemoryAllocator, método gratuito
topic_type:
- apiref
api_name:
- IMemoryAllocator.Free
api_location:
- Ole32.lib
- Ole32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c07731f60aba7d847c79467b2b2c166b363d807
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008966"
---
# <a name="imemoryallocatorfree-method"></a>Método IMemoryAllocator:: Free

O método **gratuito** libera a memória alocada pelo método [**ALLOCATE**](imemoryallocator-allocate.md) .

## <a name="syntax"></a>Sintaxe


```C++
virtual void Free(
   void* pv
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*PV* 
</dt> <dd>

Ponteiro para a memória a ser liberada.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Biblioteca<br/>                  | <dl> <dt>Ole32. lib</dt> </dl> |



 

 





