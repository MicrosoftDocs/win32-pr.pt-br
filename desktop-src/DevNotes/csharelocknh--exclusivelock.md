---
description: Adquire um bloqueio de leitor/gravador.
ms.assetid: fd212dd9-034b-4e0c-9111-e3460ea6f133
title: 'Método CShareLockNH:: ExclusiveLock'
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
ms.openlocfilehash: 8b35b544c10e6dde2887e75971d747feade5517e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749867"
---
# <a name="csharelocknhexclusivelock-method"></a>Método CShareLockNH:: ExclusiveLock

Adquire um bloqueio de leitor/gravador.

## <a name="syntax"></a>Sintaxe


```C++
void ExclusiveLock();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Cada chamada para **ExclusiveLock** deve ser emparelhada com exatamente uma chamada para [**ExclusiveUnlock**](csharelocknh--exclusiveunlock.md) para evitar o risco de um deadlock.

Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|-------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Rwnh.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ExclusiveUnlock**](csharelocknh--exclusiveunlock.md)
</dt> </dl>

 

 
