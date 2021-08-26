---
description: carrega uma versão especificada de uma .NET Framework DLL da biblioteca.
ms.assetid: f001774d-ea9a-4820-aec0-99ce958b1e1d
title: Função LoadLibraryShim
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadLibraryShim
api_type:
- DllExport
api_location:
- Mscoree.dll
ms.openlocfilehash: 123d4036713d6c1c5b7f7a08026d29d7d34126c28c5c2c1fceb94eb01baf9609
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001236"
---
# <a name="loadlibraryshim-function"></a>Função LoadLibraryShim

carrega uma versão especificada de uma .NET Framework DLL da biblioteca.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT LoadLibraryShim(
  _In_  LPCWSTR szDllName,
  _In_  LPCWSTR szVersion,
        LPVOID  pvReserved,
  _Out_ HMODULE *phModDll
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*szDllName* \[ no\]
</dt> <dd>

O nome da DLL a ser carregada a partir da .NET Framework.

</dd> <dt>

*szVersion* \[ no\]
</dt> <dd>

A versão da DLL a ser carregada. Se *szVersion* for **NULL**, a versão mais recente da DLL especificada será carregada.

</dd> <dt>

*pvReserved* 
</dt> <dd>

Reservado.

</dd> <dt>

*phModDll* \[ fora\]
</dt> <dd>

Um identificador para o módulo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se essa função for bem sucedido, ela retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

essa função é usada para carregar dlls de biblioteca incluídas no pacote redistribuível .NET Framework, não DLLs geradas pelo usuário.

Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Mscoree.dll</dt> </dl> |



 

 
