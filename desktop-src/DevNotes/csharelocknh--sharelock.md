---
description: Obtém um bloqueio compartilhado.
ms.assetid: dff9a842-573a-4530-820d-6fd9001e502a
title: 'Método CShareLockNH:: ShareLock'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.ShareLock
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: d0c77564deceab29a8bee0cbffbd477559117cbd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751556"
---
# <a name="csharelocknhsharelock-method"></a>Método CShareLockNH:: ShareLock

Obtém um bloqueio compartilhado.

## <a name="syntax"></a>Sintaxe


```C++
void ShareLock();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Cada chamada para **ShareLock** deve ser emparelhada com exatamente uma chamada para [**ShareUnlock**](csharelocknh--shareunlock.md). Somente um thread que chama **ShareLock** com êxito pode chamar **ShareUnlock**; caso contrário, pode ocorrer um deadlock.

Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|-------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Rwnh.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ShareUnlock**](csharelocknh--shareunlock.md)
</dt> </dl>

 

 
