---
description: Converte os dados de atributo especificados em formato XML.
ms.assetid: 7a75726d-f1ec-4137-89c1-eccb4a78fc22
title: Função SdbFormatAttribute
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbFormatAttribute
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: e06bbaa288c7ecb0e85cd8a779100d547c33d687
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826072"
---
# <a name="sdbformatattribute-function"></a>Função SdbFormatAttribute

Converte os dados de atributo especificados em formato XML.

## <a name="syntax"></a>Sintaxe


```C++
BOOL WINAPI SdbFormatAttribute(
  _In_  PATTRINFO pAttrInfo,
  _Out_ LPTSTR    pchBuffer,
  _In_  DWORD     dwBufferSize
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pAttrInfo* \[ no\]
</dt> <dd>

Uma estrutura [**ATTRINFO**](attrinfo.md) .

</dd> <dt>

*pchBuffer* \[ fora\]
</dt> <dd>

O buffer de saída.

</dd> <dt>

*dwBufferSize* \[ no\]
</dt> <dd>

O tamanho do buffer *pchBuffer* , em caracteres.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

A função retornará **true** em caso de êxito ou **falso** se o buffer for muito pequeno ou se o atributo não for encontrado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                         |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**SdbGetFileAttributes**](sdbgetfileattributes.md)
</dt> </dl>

 

 




