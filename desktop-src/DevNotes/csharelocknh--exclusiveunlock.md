---
description: Libera um bloqueio adquirido usando ExclusiveLock para o modo compartilhado.
ms.assetid: d38354f0-2eb3-4924-99b5-1331e587ce32
title: 'Método CShareLockNH:: ExclusiveUnlock'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.ExclusiveUnlock
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: 20d614f733b1668e3dea7619629cf2833f1d6af40384e679aea79a7a48279724
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118667832"
---
# <a name="csharelocknhexclusiveunlock-method"></a>Método CShareLockNH:: ExclusiveUnlock

Libera um bloqueio adquirido usando [**ExclusiveLock**](csharelocknh--exclusivelock.md) para o modo compartilhado.

## <a name="syntax"></a>Sintaxe


```C++
void ExclusiveUnlock();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Cada chamada para [**ExclusiveLock**](csharelocknh--exclusivelock.md) deve ser emparelhada com exatamente uma chamada para **ExclusiveUnlock** para evitar o risco de um deadlock.

Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|-------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Rwnh.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ExclusiveLock**](csharelocknh--exclusivelock.md)
</dt> </dl>

 

 
