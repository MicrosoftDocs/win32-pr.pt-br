---
description: Impede que mais de um thread conclua a aquisição de um bloqueio.
ms.assetid: 9cdcc6d5-b2f1-4c88-b859-1c15a80e70a9
title: 'CShareLockNH: método artialLock de:P'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.PartialLock
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: 7eae3f0eb57d534ea352b7d1c1e0834ef54dfb42460dfe7b2edc4f6fc07fa013
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118162340"
---
# <a name="csharelocknhpartiallock-method"></a>CShareLockNH: método artialLock de:P

Impede que mais de um thread conclua a aquisição de um bloqueio.

## <a name="syntax"></a>Sintaxe


```C++
void PartialLock();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Embora **PartialLock** esteja em vigor, outros threads que chamam [**ShareLock**](csharelocknh--sharelock.md) podem entrar no bloqueio.

Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|-------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Rwnh.dll</dt> </dl> |



 

 
