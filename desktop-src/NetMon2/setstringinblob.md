---
description: Define uma cadeia de caracteres em um determinado local dentro de um BLOB.
ms.assetid: 645e6b8b-aaaf-429f-ad2f-bf4364ef4e80
title: Função SetStringInBlob (Netmon.h)
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
ms.openlocfilehash: 293aabf86769a8cfa678df79a04b5158b9c1d19c80d660b144c4a33cbf32c56f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118363675"
---
# <a name="setstringinblob-function"></a>Função SetStringInBlob

A **função SetStringInBlob** define uma cadeia de caracteres em um determinado local dentro de um BLOB.

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

*hBlob* \[ Em\]
</dt> <dd>

Um alça para o BLOB.

</dd> <dt>

*pOwnerName* \[ Em\]
</dt> <dd>

Um ponteiro para a **seção Proprietário** do BLOB, em que a cadeia de caracteres está definida.

</dd> <dt>

*pCategoryName* \[ Em\]
</dt> <dd>

Um ponteiro para a **seção Categoria** do BLOB, em que a cadeia de caracteres está definida.

</dd> <dt>

*pTagName* \[ Em\]
</dt> <dd>

Um ponteiro para a **Marca da** cadeia de caracteres solicitada.

</dd> <dt>

*pString* \[ Em\]
</dt> <dd>

Um ponteiro para a variável em que um ponteiro para a cadeia de caracteres será retornado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será NMERR \_ SUCCESS.

Se a função não for bem-sucedida, o valor de retorno será um valor NMERR que indica o problema.

Se as informações **de Proprietário,** **Categoria** ou Marca especificadas não existirem, o valor de retorno será NMERR  \_ BLOB ENTRY NÃO \_ \_ \_ \_ EXISTE.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>Netmon.h</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Npptools.lib</dt> </dl> |
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

 

 




