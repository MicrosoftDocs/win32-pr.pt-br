---
description: Libera o cache do banco de dados shim. Essa função deve ser chamada depois de instalar um novo banco de dados shim.
ms.assetid: 7e5bbdca-7b58-4c51-9cd1-105b05ee7fbe
title: Função ShimFlushCache
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShimFlushCache
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: ecf1291b7fdcfb43170ec7e269fa140c321fafdbc09989fc7ee2b392f11c1160
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075910"
---
# <a name="shimflushcache-function"></a>Função ShimFlushCache

Libera o cache do banco de dados shim. Essa função deve ser chamada depois de instalar um novo banco de dados shim.

## <a name="syntax"></a>Sintaxe


```C++
BOOL WINAPI ShimFlushCache(
  _In_opt_ HWND      hwnd,
  _In_opt_ HINSTANCE hInstance,
  _In_opt_ LPCSTR    lpszCmdLine,
  _In_     int       nCmdShow
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hwnd* \[ in, opcional\]
</dt> <dd>

Nãousado; deve ser 0.

</dd> <dt>

*hInstance* \[ in, opcional\]
</dt> <dd>

Nãousado; deve ser 0.

</dd> <dt>

*lpszCmdLine* \[ in, opcional\]
</dt> <dd>

Nãousado; deve ser 0.

</dd> <dt>

*nCmdShow* \[ Em\]
</dt> <dd>

Nãousado; deve ser 0.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

A função retorna **TRUE em** caso de êxito **ou FALSE** em caso de falha.

## <a name="remarks"></a>Comentários

O chamador deve ser um administrador.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**BaseFlushAppcompatCache**](baseflushappcompatcache.md)
</dt> </dl>

 

 




