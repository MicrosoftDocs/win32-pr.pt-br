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
ms.openlocfilehash: 608fd7736093ae1f8d131ede777a691e467de9de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748910"
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

## <a name="return-value"></a>Retornar valor

Essa função retornará **true** se tiver sucesso; caso contrário, retornará **false**.

## <a name="remarks"></a>Comentários

Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|---------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Cscmig.dll</dt> </dl> |



 

 
