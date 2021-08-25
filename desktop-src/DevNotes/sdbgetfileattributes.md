---
description: Recupera os dados de atributo para o arquivo especificado.
ms.assetid: 899b4af3-8185-4ce5-8e81-05ec3a446e42
title: Função SdbGetFileAttributes
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetFileAttributes
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: a75dd64bfbeaf027839c63227c594ada7602101d059cbbd9d10deb085152918d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103646"
---
# <a name="sdbgetfileattributes-function"></a>Função SdbGetFileAttributes

Recupera os dados de atributo para o arquivo especificado.

## <a name="syntax"></a>Sintaxe


```C++
BOOL WINAPI SdbGetFileAttributes(
  _In_  LPCTSTR   lpwszFileName,
  _Out_ PATTRINFO *ppAttrInfo,
  _Out_ LPDWORD   lpdwAttrCount
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lpwszFileName* \[ Em\]
</dt> <dd>

O caminho para o arquivo.

</dd> <dt>

*ppAttrInfo* \[ out\]
</dt> <dd>

Uma matriz de [**estruturas ATTRINFO**](attrinfo.md) que contêm os dados de atributo.

</dd> <dt>

*lpdwAttrCount* \[ out\]
</dt> <dd>

O número de atributos.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

A função retorna **TRUE em** caso de êxito **ou FALSE** em caso de falha.

## <a name="remarks"></a>Comentários

Quando terminar de usar os dados, livre-os usando a [**função SdbFreeFileAttributes.**](sdbfreefileattributes.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SdbFormatAttribute**](sdbformatattribute.md)
</dt> <dt>

[**SdbFreeFileAttributes**](sdbfreefileattributes.md)
</dt> </dl>

 

 




