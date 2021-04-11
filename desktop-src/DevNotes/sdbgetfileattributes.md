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
ms.openlocfilehash: 651b9af34afdd2ffd767eba7ca4467ecfee081cf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104088813"
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

*lpwszFileName* \[ no\]
</dt> <dd>

O caminho para o arquivo.

</dd> <dt>

*ppAttrInfo* \[ fora\]
</dt> <dd>

Uma matriz de estruturas [**ATTRINFO**](attrinfo.md) que contêm os dados de atributo.

</dd> <dt>

*lpdwAttrCount* \[ fora\]
</dt> <dd>

O número de atributos.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

A função retorna **true** em caso de êxito ou **false** em caso de falha.

## <a name="remarks"></a>Comentários

Depois de concluir os dados, libere-os usando a função [**SdbFreeFileAttributes**](sdbfreefileattributes.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                         |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SdbFormatAttribute**](sdbformatattribute.md)
</dt> <dt>

[**SdbFreeFileAttributes**](sdbfreefileattributes.md)
</dt> </dl>

 

 




