---
description: Indica a versão do CTL3D que está em execução no momento.
ms.assetid: 38c0842c-417f-4ca1-acc2-3bbadf45c804
title: Função Ctl3dGetVer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dGetVer
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: e548d8933538ea85ba94f6e120032453079d69ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751754"
---
# <a name="ctl3dgetver-function"></a>Função Ctl3dGetVer

Indica a versão do CTL3D que está em execução no momento.

## <a name="syntax"></a>Sintaxe


```C++
WORD Ctl3dGetVer(void);
```



## <a name="parameters"></a>Parâmetros

Essa função não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna um valor que contém o número de versão principal no byte de ordem superior e o número de versão secundária no byte de ordem inferior.

## <a name="remarks"></a>Comentários

Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



 

 
