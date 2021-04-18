---
description: Permite que um depurador examine informações de tabela de funções dinâmicas.
ms.assetid: 32fd0dfd-ca7c-45e4-9d59-2b3318d7e13d
title: Função RtlGetFunctionTableListHead
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlGetFunctionTableListHead
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 3dde476ee9958952d85c66816a113b92529aa13e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105771771"
---
# <a name="rtlgetfunctiontablelisthead-function"></a>Função RtlGetFunctionTableListHead

\[Essa função pode ser alterada ou removida do Windows sem aviso prévio.\]

Permite que um depurador examine informações de tabela de funções dinâmicas.

## <a name="syntax"></a>Sintaxe


```C++
PLIST_ENTRY RtlGetFunctionTableListHead(void);
```



## <a name="parameters"></a>Parâmetros

Essa função não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna um ponteiro para o cabeçalho da lista de tabelas de funções.

## <a name="remarks"></a>Comentários

Observe que o arquivo de cabeçalho do WDK (Windows Driver Kit) Ntdef. h é necessário para algumas definições. A biblioteca de importação associada, ntdll. lib, está disponível no WDK. Você também pode usar as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Ntdll.dll.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
