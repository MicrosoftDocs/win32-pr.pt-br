---
description: Recupera informações sobre a chave do Registro especificada em um hive do registro offline.
ms.assetid: b565c55c-acc2-4880-91eb-7bd9188e4749
title: Função ORQueryInfoKey (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORQueryInfoKey
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: b38a0dd35b1fe1755fbcbc3bcac3da379ee57e6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756105"
---
# <a name="orqueryinfokey-function"></a>Função ORQueryInfoKey

Recupera informações sobre a chave do Registro especificada em um hive do registro offline.

## <a name="syntax"></a>Sintaxe


```C++
DWORD ORQueryInfoKey(
  _In_        ORHKEY    Handle,
  _Out_opt_   PWSTR     lpClass,
  _Inout_opt_ PDWORD    lpcClass,
  _Out_opt_   PDWORD    lpcSubKeys,
  _Out_opt_   PDWORD    lpcMaxSubKeyLen,
  _Out_opt_   PDWORD    lpcMaxClassLen,
  _Out_opt_   PDWORD    lpcValues,
  _Out_opt_   PDWORD    lpcMaxValueNameLen,
  _Out_opt_   PDWORD    lpcMaxValueLen,
  _Out_opt_   PDWORD    lpcbSecurityDescriptor,
  _Out_opt_   PFILETIME lpftLastWriteTime
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Identificador* \[ do no\]
</dt> <dd>

Um identificador para uma chave do registro aberta em um hive do registro offline.

</dd> <dt>

*lpClass* \[ out, opcional\]
</dt> <dd>

Um ponteiro para um buffer que recebe a classe de chave. Este parâmetro pode ser **NULL**.

</dd> <dt>

*lpcClass* \[ entrada, saída, opcional\]
</dt> <dd>

Um ponteiro para uma variável que especifica o tamanho do buffer apontado pelo parâmetro *lpClass* , em caracteres.

O tamanho deve incluir o caractere nulo de terminação. Quando a função retorna, essa variável contém o tamanho da cadeia de caracteres de classe que é armazenada no buffer. A contagem retornada não inclui o caractere nulo de terminação. Se o buffer não for grande o suficiente, a função retornará um erro com \_ mais \_ dados, e a variável conterá o tamanho da cadeia de caracteres, em caracteres, sem contar o caractere nulo de terminação.

Se *lpClass* for **nulo**, *lpcClass* poderá ser **nulo**.

Se o parâmetro *lpClass* for um endereço válido, mas o parâmetro *lpcClass* não for (por exemplo, se o parâmetro *lpcClass* for **nulo**), a função retornará um parâmetro de erro \_ inválido \_ .

</dd> <dt>

*lpcSubKeys* \[ out, opcional\]
</dt> <dd>

Um ponteiro para uma variável que recebe o número de subchaves que estão contidas na chave especificada. Este parâmetro pode ser **NULL**.

</dd> <dt>

*lpcMaxSubKeyLen* \[ out, opcional\]
</dt> <dd>

Um ponteiro para uma variável que recebe o tamanho da subchave da chave com o nome mais longo, em caracteres Unicode, sem incluir o caractere nulo de terminação. Este parâmetro pode ser **NULL**.

</dd> <dt>

*lpcMaxClassLen* \[ out, opcional\]
</dt> <dd>

Um ponteiro para uma variável que recebe o tamanho da cadeia de caracteres mais longa que especifica uma classe de subchave, em caracteres Unicode. A contagem retornada não inclui o caractere nulo de terminação. Este parâmetro pode ser **NULL**.

</dd> <dt>

*lpcValues* \[ out, opcional\]
</dt> <dd>

Um ponteiro para uma variável que recebe o número de valores associados à chave. Este parâmetro pode ser **NULL**.

</dd> <dt>

*lpcMaxValueNameLen* \[ out, opcional\]
</dt> <dd>

Um ponteiro para uma variável que recebe o tamanho do nome de valor mais longo da chave, em caracteres Unicode. O tamanho não inclui o caractere nulo de terminação. Este parâmetro pode ser **NULL**.

</dd> <dt>

*lpcMaxValueLen* \[ out, opcional\]
</dt> <dd>

Um ponteiro para uma variável que recebe o tamanho do componente de dados mais longo entre os valores da chave, em bytes. Este parâmetro pode ser **NULL**.

</dd> <dt>

*lpcbSecurityDescriptor* \[ out, opcional\]
</dt> <dd>

Um ponteiro para uma variável que recebe o tamanho do descritor de segurança da chave, em bytes. Este parâmetro pode ser **NULL**.

</dd> <dt>

*lpftLastWriteTime* \[ out, opcional\]
</dt> <dd>

Um ponteiro para uma estrutura [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) que recebe a última hora de gravação. Este parâmetro pode ser **NULL**.

A função define os membros da estrutura [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) para indicar a última vez que a chave ou qualquer uma de suas entradas de valor é modificada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, o valor de retorno será \_ êxito no erro.

Se a função falhar, o valor de retorno será um código de erro diferente de zero definido em Winerror. h. Você pode usar a função [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) com a \_ mensagem de formato \_ do \_ sinalizador do sistema para obter uma descrição genérica do erro.

Se o buffer *lpClass* for muito pequeno para receber o nome da classe, a função retornará um erro \_ mais \_ dados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|---------------------------------------------------------------------------------------|
| Redistribuível<br/> | Biblioteca de registro offline do Windows versão 1,0 ou posterior<br/>                      |
| parâmetro<br/>          | <dl> <dt>Offreg. h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime)
</dt> <dt>

[**ORCreateKey**](orcreatekey.md)
</dt> <dt>

[**OROpenKey**](oropenkey.md)
</dt> <dt>

[**ORDeleteKey**](ordeletekey.md)
</dt> </dl>

 

 
