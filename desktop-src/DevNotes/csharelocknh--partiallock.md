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
ms.openlocfilehash: 0b7b7d55c9fd8d979aa14f12939df922e7a89099
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751291"
---
# <a name="csharelocknhpartiallock-method"></a>CShareLockNH: método artialLock de:P

Impede que mais de um thread conclua a aquisição de um bloqueio.

## <a name="syntax"></a>Sintaxe


```C++
void PartialLock();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Embora **PartialLock** esteja em vigor, outros threads que chamam [**ShareLock**](csharelocknh--sharelock.md) podem entrar no bloqueio.

Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|-------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Rwnh.dll</dt> </dl> |



 

 
