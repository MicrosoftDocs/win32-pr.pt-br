---
description: Libera o cache do banco de dados Shim. Essa função deve ser chamada após a instalação de um novo banco de dados de Shim.
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
ms.openlocfilehash: 35e279c5036142ec87c5bad6d7c512388033bc94
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010082"
---
# <a name="shimflushcache-function"></a>Função ShimFlushCache

Libera o cache do banco de dados Shim. Essa função deve ser chamada após a instalação de um novo banco de dados de Shim.

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

*HWND* \[ em, opcional\]
</dt> <dd>

Não utilizado deve ser 0.

</dd> <dt>

*HINSTANCE* \[ em, opcional\]
</dt> <dd>

Não utilizado deve ser 0.

</dd> <dt>

*lpszCmdLine* \[ em, opcional\]
</dt> <dd>

Não utilizado deve ser 0.

</dd> <dt>

*nCmdShow* \[ no\]
</dt> <dd>

Não utilizado deve ser 0.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

A função retorna **true** em caso de êxito ou **false** em caso de falha.

## <a name="remarks"></a>Comentários

O chamador deve ser um administrador.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                         |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**BaseFlushAppcompatCache**](baseflushappcompatcache.md)
</dt> </dl>

 

 




