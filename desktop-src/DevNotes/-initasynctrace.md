---
description: Inicializa o rastreamento.
ms.assetid: d2708e29-920d-4b13-8917-a6f2065ba58c
title: Função InitAsyncTrace
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InitAsyncTrace
api_type:
- DllExport
api_location:
- Exstrace.dll
ms.openlocfilehash: f79137fe4e832a193bafa59a573e5eb541884a2c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747487"
---
# <a name="initasynctrace-function"></a>Função InitAsyncTrace

Inicializa o rastreamento.

## <a name="syntax"></a>Sintaxe


```C++
BOOL InitAsyncTrace(void);
```



## <a name="parameters"></a>Parâmetros

Essa função não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Essa função retornará **true** se a função tiver sucesso; caso contrário, retornará **false**.

## <a name="remarks"></a>Comentários

Exstrace.dll é um componente opcional que é instalado com o protocolo SMTP e o protocolo NNTP (Network News Transfer Protocol).

Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Exstrace.dll</dt> </dl> |



 

 
