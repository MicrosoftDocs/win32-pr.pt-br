---
description: Verifica se os controles podem usar efeitos 3D.
ms.assetid: fb7b892f-2580-41ac-b2ef-938da3cc1dc2
title: Função Ctl3dEnabled
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dEnabled
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: d0eecec5650ecc00b69c0745e58a3e1d0f931a00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750925"
---
# <a name="ctl3denabled-function"></a>Função Ctl3dEnabled

Verifica se os controles podem usar efeitos 3D.

## <a name="syntax"></a>Sintaxe


```C++
BOOL Ctl3dEnabled(void);
```



## <a name="parameters"></a>Parâmetros

Essa função não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retornará **true** se os controles puderem usar efeitos 3D; caso contrário, retornará **false**.

## <a name="remarks"></a>Comentários

No Windows 4,0 ou posterior, **Ctl3dEnabled** e [**Ctl3dRegister**](ctl3dregister.md) retornam **false**.

Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



 

 
