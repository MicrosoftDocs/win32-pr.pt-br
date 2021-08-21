---
description: Libera um bloqueio compartilhado.
ms.assetid: c2e9eb68-aacb-4196-b09e-d2748efb7fd6
title: 'Método CShareLockNH:: ShareUnlock'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.ShareUnlock
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: 2bf59b6e1aa0f6718cece105007a8ba502291c23868aca6ec55283dd7292f8b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118162181"
---
# <a name="csharelocknhshareunlock-method"></a>Método CShareLockNH:: ShareUnlock

Libera um bloqueio compartilhado.

## <a name="syntax"></a>Sintaxe


```C++
void ShareUnlock();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Cada chamada para [**ShareLock**](csharelocknh--sharelock.md) deve ser emparelhada com exatamente uma chamada para **ShareUnlock**. Somente um thread que chama **ShareLock** com êxito pode chamar **ShareUnlock**; caso contrário, pode ocorrer um deadlock.

Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|-------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Rwnh.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ShareLock**](csharelocknh--sharelock.md)
</dt> </dl>

 

 
