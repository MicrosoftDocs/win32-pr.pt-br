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
ms.openlocfilehash: d64fcf9f787587165c12e675d79cfca641b0ab5086a5cce6b13029da46def974
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956295"
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

Essa função retornará **TRUE** se a função for bem-sucedida; caso contrário, retornará **FALSE.**

## <a name="remarks"></a>Comentários

Exstrace.dll é um componente opcional que é instalado com o protocolo SMTP e o protocolo NNTP.

Essa função não tem nenhuma biblioteca de importação ou arquivo de header associado; você deve chamá-lo usando [**as funções LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**e GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Exstrace.dll</dt> </dl> |



 

 
