---
title: Método IMemoryAllocator Free
description: O método Free libera a memória alocada pelo método Allocate.
ms.assetid: 41f81cba-4431-4ff7-ac84-8ff5bea71b65
keywords:
- Método gratuito Estruturada Armazenamento
- Método gratuito Estruturado Armazenamento , interface IMemoryAllocator
- Interface IMemoryAllocator estruturada Armazenamento , método Gratuito
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
ms.openlocfilehash: f78690a37b5500f5e540cf4c2ef516b7c3ea89c219ba475dc5e5ac030f775d81
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119906166"
---
# <a name="imemoryallocatorfree-method"></a>Método IMemoryAllocator::Free

O **método** Free libera a memória alocada pelo [**método Allocate.**](imemoryallocator-allocate.md)

## <a name="syntax"></a>Sintaxe


```C++
virtual void Free(
   void* pv
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Pv* 
</dt> <dd>

Ponteiro para a memória a ser liberada.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Biblioteca<br/>                  | <dl> <dt>Ole32.lib</dt> </dl> |



 

 





