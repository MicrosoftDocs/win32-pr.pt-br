---
description: Obtém o período de tempo, em minutos, desde a última atividade do usuário.
ms.assetid: 2d1e68ad-6f65-4e64-afbf-505b2c9d3423
title: Função GetIdleMinutes
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetIdleMinutes
api_type:
- DllExport
api_location:
- Msidle.dll
ms.openlocfilehash: d3397de5d792181958891eef9693d29b2d7d4e56f9bbc7f7e1cfef19171625b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118404579"
---
# <a name="getidleminutes-function"></a>Função GetIdleMinutes

\[Essa função não tem suporte e pode ser alterada ou não estar disponível no futuro. Em vez disso, use a função **GetLastInputInfo** .\]

Obtém o período de tempo, em minutos, desde a última atividade do usuário.

## <a name="syntax"></a>Sintaxe


```C++
DWORD WINAPI GetIdleMinutes(
   DWORD dwReserved
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwReserved* 
</dt> <dd>

Esse parâmetro deve ser definido como zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o número de minutos desde a última atividade do usuário.

## <a name="remarks"></a>Comentários

Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) . Esta função não é exportada pelo nome; Especifique o ordinal 8 ao chamar **GetProcAddress**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|---------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msidle.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**GetLastInputInfo**](/windows/win32/api/winuser/nf-winuser-getlastinputinfo)
</dt> </dl>

 

 
