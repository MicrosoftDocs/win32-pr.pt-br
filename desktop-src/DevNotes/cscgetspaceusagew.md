---
description: Recupera informações sobre o espaço usado pelo cache Arquivos Offline.
ms.assetid: 3a6fa548-0e9a-4138-a5ec-cde0aeb2b811
title: Função CSCGetSpaceUsageW
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSCGetSpaceUsageW
api_type:
- DllExport
api_location:
- Cscmig.dll
ms.openlocfilehash: 8dd6d12c4e0267c97b93a812a4b66d3bd14a408dff0191686d4949ccbc958723
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118667949"
---
# <a name="cscgetspaceusagew-function"></a>Função CSCGetSpaceUsageW

\[Essa função não tem suporte e não deve ser usada.\]

Recupera informações sobre o espaço usado pelo cache Arquivos Offline.

## <a name="syntax"></a>Sintaxe


```C++
BOOL WINAPI CSCGetSpaceUsageW(
  _Inout_ LPTSTR  lptzLocation,
  _In_    DWORD   dwSize,
  _Inout_ LPDWORD lpdwMaxSpaceHigh,
  _Inout_ LPDWORD lpdwMaxSpaceLow,
  _Inout_ LPDWORD lpdwCurrentSpaceHigh,
  _Inout_ LPDWORD lpdwCurrentSpaceLow,
  _Inout_ LPDWORD lpcntTotalFiles,
  _Inout_ LPDWORD lpcntTotalDirs
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lptzLocation* \[ entrada, saída\]
</dt> <dd>

O local do diretório do cache.

</dd> <dt>

*dwSize* \[ no\]
</dt> <dd>

O tamanho do buffer *lptzLocation* , em caracteres.

</dd> <dt>

*lpdwMaxSpaceHigh* \[ entrada, saída\]
</dt> <dd>

A **DWORD** de ordem superior do número máximo de bytes disponíveis no cache.

</dd> <dt>

*lpdwMaxSpaceLow* \[ entrada, saída\]
</dt> <dd>

A **DWORD** de ordem inferior do número máximo de bytes disponíveis no cache.

</dd> <dt>

*lpdwCurrentSpaceHigh* \[ entrada, saída\]
</dt> <dd>

A **DWORD** de ordem superior do número atual de bytes disponíveis no cache.

</dd> <dt>

*lpdwCurrentSpaceLow* \[ entrada, saída\]
</dt> <dd>

A **DWORD** de ordem inferior do número atual de bytes disponíveis no cache.

</dd> <dt>

*lpcntTotalFiles* \[ entrada, saída\]
</dt> <dd>

O número total de arquivos no cache.

</dd> <dt>

*lpcntTotalDirs* \[ entrada, saída\]
</dt> <dd>

O número total de diretórios no cache.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Essa função retornará **true** se tiver sucesso; caso contrário, retornará **false**.

## <a name="remarks"></a>Comentários

Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|---------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Cscmig.dll</dt> </dl> |



 

 
