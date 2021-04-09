---
description: Usa chamadas sequenciais para recuperar todas as cadeias de caracteres dentro dos intervalos especificados.
ms.assetid: 4e819975-84a5-4b73-9a19-792d3607da9c
title: Função GetStringsFromBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetStringsFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 25fbc149a663ef68d1588218937568401f414ef7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920688"
---
# <a name="getstringsfromblob-function"></a>Função GetStringsFromBlob

A função **GetStringsFromBlob** usa chamadas sequenciais para recuperar todas as cadeias de caracteres dentro dos intervalos especificados.

## <a name="syntax"></a>Sintaxe


```C++
DWORD GetStringsFromBlob(
  _In_        HBLOB hBlob,
  _In_  const char  *pRequestedOwnerName,
  _In_  const char  *pRequestedCategoryName,
  _In_  const char  *pRequestedTagName,
  _Out_ const char  **ppReturnedOwnerName,
  _Out_ const char  **ppReturnedCategoryName,
  _Out_ const char  **ppReturnedTagName,
  _Out_ const char  **ppReturnedString,
  _Out_       DWORD *pRestartKey
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hBlob* \[ no\]
</dt> <dd>

Um identificador para o BLOB.

</dd> <dt>

*pRequestedOwnerName* \[ no\]
</dt> <dd>

Um ponteiro para a seção de proprietário da qual obter a cadeia de caracteres.

</dd> <dt>

*pRequestedCategoryName* \[ no\]
</dt> <dd>

Um ponteiro para a seção de categoria da qual obter a cadeia de caracteres.

</dd> <dt>

*pRequestedTagName* \[ no\]
</dt> <dd>

Um ponteiro para a marca da cadeia de caracteres solicitada.

</dd> <dt>

*ppReturnedOwnerName* \[ fora\]
</dt> <dd>

Um ponteiro para a variável que aponta para onde o nome do **proprietário** será retornado.

</dd> <dt>

*ppReturnedCategoryName* \[ fora\]
</dt> <dd>

Um ponteiro para a variável que aponta para onde o nome da **categoria** será retornado.

</dd> <dt>

*ppReturnedTagName* \[ fora\]
</dt> <dd>

Um ponteiro para a variável que aponta para onde o nome da **marca** será retornado.

</dd> <dt>

*ppReturnedString* \[ fora\]
</dt> <dd>

Um ponteiro para a variável que aponta para onde o nome da cadeia de caracteres será retornado.

</dd> <dt>

*pRestartKey* \[ fora\]
</dt> <dd>

Um ponteiro para a variável em que a chave de reinicialização será especificada e retornada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, o valor de retorno será NMERR com \_ êxito.

Se a função não for bem-sucedida, o valor de retorno será um valor NMERR que indica o problema.

Se uma combinação especificada de informações de **proprietário**, **categoria** e **marca** não existir, o valor de retorno será **a \_ entrada de blob NMERR não \_ \_ \_ \_ existir**.

Quando o BLOB é atravessado completamente dentro dos limites especificados inicialmente, a função retorna a **\_ entrada de blob NMERR \_ \_ \_ não \_ existe** e o parâmetro *pRestartKey* aponta para zero.

## <a name="remarks"></a>Comentários

Na chamada inicial para a função **GetStringsFromBlob** , o parâmetro *pRestartKey* aponta para uma variável que contém o valor zero. Os parâmetros de *busca* podem ser usados somente quando a chave de reinicialização for zero. Em chamadas subsequentes, quando *pRestartKey* tem valores diferentes de zero, os parâmetros de *busca* são ignorados. Na chamada inicial, tudo pode apontar para **NULL**, que configura a consulta para retornar cada entrada no BLOB, uma por chamada subsequente.

A especificação de um proprietário limita as cadeias de caracteres retornadas apenas ao proprietário. Uma limitação semelhante é verdadeira para categorias e marcas, com a limitação adicional de que, se uma categoria for especificada, um proprietário também deverá ser especificado e, se uma marca for especificada, uma categoria (e, portanto, um proprietário) deverá ser especificada.

Quando a chamada inicial para **GetStringsFromBlob** retorna, *pRestartKey* aponta para um novo valor, que deve ser especificado na próxima chamada para a função para obter o próximo valor.

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

[SetStringInBlob](setstringinblob.md)
</dt> <dt>

[GetBoolFromBlob](getboolfromblob.md)
</dt> <dt>

[GetClassIDFromBlob](getclassidfromblob.md)
</dt> <dt>

[GetDwordFromBlob](getdwordfromblob.md)
</dt> <dt>

[GetMacAddressFromBlob](getmacaddressfromblob.md)
</dt> <dt>

[GetNetworkInfoFromBlob](getnetworkinfofromblob.md)
</dt> <dt>

[GetNPPAddressFilterFromBlob](getnppaddressfilterfromblob.md)
</dt> <dt>

[GetNPPPatternFilterFromBlob](getnpppatternfilterfromblob.md)
</dt> <dt>

[GetNPPTriggerFromBlob](getnpptriggerfromblob.md)
</dt> <dt>

[GetStringFromBlob](getstringfromblob.md)
</dt> </dl>

 

 




