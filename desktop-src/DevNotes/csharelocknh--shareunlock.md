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
ms.openlocfilehash: 80c4311f4bf66000440dac38da6300888a8e5d59
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755407"
---
# <a name="csharelocknhshareunlock-method"></a>Método CShareLockNH:: ShareUnlock

Libera um bloqueio compartilhado.

## <a name="syntax"></a>Sintaxe


```C++
void ShareUnlock();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

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

 

 
