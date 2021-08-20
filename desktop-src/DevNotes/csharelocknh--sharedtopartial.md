---
description: Altera um bloqueio compartilhado para um bloqueio parcial.
ms.assetid: 82122671-b0bd-47ad-9a25-ee8ebd3779be
title: 'Método CShareLockNH:: SharedToPartial'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.SharedToPartial
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: 8f2cc895786655754a3fcf56c6efe745467c12328867b1dc021a257ba1519652
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118162201"
---
# <a name="csharelocknhsharedtopartial-method"></a>Método CShareLockNH:: SharedToPartial

Altera um bloqueio compartilhado para um bloqueio parcial.

## <a name="syntax"></a>Sintaxe


```C++
BOOL SharedToPartial();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retornará **true** se o bloqueio parcial for obtido; caso contrário, retornará **false** e o bloqueio permanecerá no modo compartilhado.

## <a name="remarks"></a>Comentários

Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|-------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Rwnh.dll</dt> </dl> |



 

 
