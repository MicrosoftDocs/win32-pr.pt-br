---
description: Inicia o monitoramento de inatividade.
ms.assetid: fed5e4ae-2c2b-4b00-9230-b71aec9335c8
title: Função BeginIdleDetection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BeginIdleDetection
api_type:
- DllExport
api_location:
- Msidle.dll
ms.openlocfilehash: 06cd016dc4102ef2f5b0f351aa4836a7f9980645
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756514"
---
# <a name="beginidledetection-function"></a>Função BeginIdleDetection

\[Essa função não tem suporte e pode ser alterada ou não estar disponível no futuro. Em vez disso, use a função **GetLastInputInfo** .\]

Inicia o monitoramento de inatividade.

## <a name="syntax"></a>Sintaxe


```C++
DWORD WINAPI BeginIdleDetection(
   _IDLECALLBACK pfnCallback,
   DWORD         dwIdleMin,
   DWORD         dwReserved
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pfnCallback* 
</dt> <dd>

A função que é chamada quando o estado ocioso é alterado. Esse retorno de chamada é definido da seguinte maneira:

``` syntax
typedef void (WINAPI* _IDLECALLBACK) (DWORD dwState);

#define STATE_USER_IDLE_BEGIN       1
#define STATE_USER_IDLE_END         2
```

</dd> <dt>

*dwIdleMin* 
</dt> <dd>

O número de minutos de inatividade antes que a chamada seja feita para a função de chamada de retorno.

</dd> <dt>

*dwReserved* 
</dt> <dd>

Esse parâmetro deve ser definido como zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará 0 se a função tiver sucesso; caso contrário, ele retornará um código de erro. Por exemplo, se *dwReserved* for algo diferente de 0, **\_ \_ dados inválidos de erro** serão retornados.

## <a name="remarks"></a>Comentários

Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) . Esta função não é exportada pelo nome; Especifique o ordinal 3 ao chamar **GetProcAddress**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|---------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msidle.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**GetLastInputInfo**](/windows/win32/api/winuser/nf-winuser-getlastinputinfo)
</dt> </dl>

 

 
