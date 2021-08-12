---
description: Adquire um bloqueio de leitor/leitor.
ms.assetid: fd212dd9-034b-4e0c-9111-e3460ea6f133
title: Método CShareLockNH::ExclusiveLock
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.ExclusiveLock
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: 16a5d2ba49d5ff1c25079a99a979d7a0fb4a51ee64d54fa4042152d7b010dc1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118667959"
---
# <a name="csharelocknhexclusivelock-method"></a>Método CShareLockNH::ExclusiveLock

Adquire um bloqueio de leitor/leitor.

## <a name="syntax"></a>Sintaxe


```C++
void ExclusiveLock();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Cada chamada para **ExclusiveLock** deve ser emparelhada com exatamente uma chamada para [**ExclusiveUnlock**](csharelocknh--exclusiveunlock.md) para evitar o risco de um deadlock.

Essa função não tem nenhuma biblioteca de importação ou arquivo de header associado; você deve chamá-lo usando [**as funções LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**e GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|-------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Rwnh.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ExclusiveUnlock**](csharelocknh--exclusiveunlock.md)
</dt> </dl>

 

 
