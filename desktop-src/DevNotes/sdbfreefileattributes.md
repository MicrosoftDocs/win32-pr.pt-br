---
description: Libera os dados de atributo de arquivo especificados.
ms.assetid: c1a4dcf8-614f-49a5-a923-8d7d610e6406
title: Função SdbFreeFileAttributes
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbFreeFileAttributes
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 7e99180198f8f23ba6b6872502710b2af28aaff3999a9f315c33ef2d1874d987
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103666"
---
# <a name="sdbfreefileattributes-function"></a>Função SdbFreeFileAttributes

Libera os dados de atributo de arquivo especificados.

## <a name="syntax"></a>Sintaxe


```C++
BOOL WINAPI SdbFreeFileAttributes(
  _In_ PATTRINFO pFileAttributes
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pFileAttributes* \[ no\]
</dt> <dd>

Uma estrutura [**ATTRINFO**](attrinfo.md) retornada pela função [**SdbGetFileAttributes**](sdbgetfileattributes.md) .

</dd> </dl>

## <a name="return-value"></a>Valor retornado

A função retorna **true** em caso de êxito ou **false** em caso de falha.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SdbGetFileAttributes**](sdbgetfileattributes.md)
</dt> </dl>

 

 




