---
description: Define uma cadeia de caracteres em um determinado local dentro de um BLOB.
ms.assetid: 645e6b8b-aaaf-429f-ad2f-bf4364ef4e80
title: Função SetStringInBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetStringInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 37278b9111818957e6d5fb3032f1bf33ad3a6ec3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164619"
---
# <a name="setstringinblob-function"></a>Função SetStringInBlob

A função **SetStringInBlob** define uma cadeia de caracteres em um determinado local dentro de um blob.

## <a name="syntax"></a>Sintaxe


```C++
DWORD SetStringInBlob(
  _In_       HBLOB hBlob,
  _In_ const char  *pOwnerName,
  _In_ const char  *pCategoryName,
  _In_ const char  *pTagName,
  _In_ const char  *pString
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hBlob* \[ no\]
</dt> <dd>

Um identificador para o BLOB.

</dd> <dt>

*pOwnerName* \[ no\]
</dt> <dd>

Um ponteiro para a seção de **proprietário** do blob, em que a cadeia de caracteres é definida.

</dd> <dt>

*pCategoryName* \[ no\]
</dt> <dd>

Um ponteiro para a seção de **categoria** do blob, em que a cadeia de caracteres é definida.

</dd> <dt>

*pTagName* \[ no\]
</dt> <dd>

Um ponteiro para a **marca** da cadeia de caracteres solicitada.

</dd> <dt>

*pString* \[ no\]
</dt> <dd>

Um ponteiro para a variável em que um ponteiro para a cadeia de caracteres será retornado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, o valor de retorno será NMERR com \_ êxito.

Se a função não for bem-sucedida, o valor de retorno será um valor NMERR que indica o problema.

Se as informações de **proprietário**, **categoria** ou **marca** especificadas não existirem, o valor de retorno será \_ NMERR \_ blob \_ \_ \_ inexistente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Npptools. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[GetStringFromBlob](getstringfromblob.md)
</dt> <dt>

[SetBoolInBlob](setboolinblob.md)
</dt> <dt>

[SetClassIDInBlob](setclassidinblob.md)
</dt> <dt>

[SetDwordInBlob](setdwordinblob.md)
</dt> <dt>

[SetMacAddressInBlob](setmacaddressinblob.md)
</dt> <dt>

[SetNetworkInfoInBlob](setnetworkinfoinblob.md)
</dt> <dt>

[SetNPPAddressFilterInBlob](setnppaddressfilterinblob.md)
</dt> <dt>

[SetNPPPatternFilterInBlob](setnpppatternfilterinblob.md)
</dt> <dt>

[SetNPPTriggerInBlob](setnpptriggerinblob.md)
</dt> </dl>

 

 




