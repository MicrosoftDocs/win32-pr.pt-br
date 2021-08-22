---
description: Permite que um depurador examine as informações da tabela de funções dinâmicas.
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
ms.openlocfilehash: ff41aca0d268083132fd1a45371b0bb1ca026e5e6d693619ba1e2c2f9f2dd8f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118666726"
---
# <a name="rtlgetfunctiontablelisthead-function"></a>Função RtlGetFunctionTableListHead

\[Essa função pode ser alterada ou removida do Windows sem aviso prévio.\]

Permite que um depurador examine as informações da tabela de funções dinâmicas.

## <a name="syntax"></a>Sintaxe


```C++
PLIST_ENTRY RtlGetFunctionTableListHead(void);
```



## <a name="parameters"></a>Parâmetros

Essa função não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna um ponteiro para o líder da lista de tabelas de funções.

## <a name="remarks"></a>Comentários

Observe que o arquivo de Windows do WDK (Driver Kit) Ntdef.h é necessário para algumas definições. A biblioteca de importação associada, Ntdll.lib, está disponível no WDK. Você também pode usar as [**funções LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Ntdll.dll.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
