---
description: Inicializa o compartilhamento do IME.
ms.assetid: 7f58564e-d660-4936-b74c-af4eb93e2442
title: Função FInitIMEShare
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FInitIMEShare
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 0724bb6cb9e44dc86699a66da37616050ce54e18
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752925"
---
# <a name="finitimeshare-function"></a>Função FInitIMEShare

Inicializa o compartilhamento do IME.

## <a name="syntax"></a>Sintaxe


```C++
BOOL __cdecl FInitIMEShare(void);
```



## <a name="parameters"></a>Parâmetros

Essa função não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Caso contrário, a função retornará **true** ou **false** .

## <a name="remarks"></a>Comentários

Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

Essa função deve ser chamada antes de qualquer outra função de compartilhamento do IME ser chamada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Imeshare.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**EndIMEShare**](endimeshare.md)
</dt> </dl>

 

 
