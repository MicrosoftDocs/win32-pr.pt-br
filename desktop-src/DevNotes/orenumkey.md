---
description: Enumera as sub-chaves da chave do Registro aberta especificada em um hive do Registro offline. A função recupera informações sobre uma sub-chave sempre que é chamada.
ms.assetid: 46d13c37-473a-4772-992c-a565ad702fb9
title: Função OREnumKey (Offreg.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OREnumKey
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: ab72c9b0df79d464f802a1c574b749d04a8a16e89645f25959681e7f03eea5ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120058706"
---
# <a name="orenumkey-function"></a>Função OREnumKey

Enumera as sub-chaves da chave do Registro aberta especificada em um hive do Registro offline. A função recupera informações sobre uma sub-chave sempre que é chamada.

## <a name="syntax"></a>Sintaxe


```C++
DWORD OREnumKey(
  _In_        ORHKEY    Handle,
  _In_        DWORD     dwIndex,
  _Out_       PWSTR     lpName,
  _Inout_     PDWORD    lpcName,
  _Out_opt_   PWSTR     lpClass,
  _Inout_opt_ PDWORD    lpcClass,
  _Out_opt_   PFILETIME lpftLastWriteTime
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Manipular* \[ Em\]
</dt> <dd>

Um handle para uma chave aberta do Registro em um hive de registro offline.

</dd> <dt>

*dwIndex* \[ Em\]
</dt> <dd>

O índice da sub-chave a ser recuperada. Esse parâmetro deve ser zero para a primeira chamada para a função e, em seguida, incrementado para chamadas subsequentes.

Como as sub-chaves não são ordenadas, qualquer nova sub-chave terá um índice arbitrário. Isso significa que a função pode retornar subkeys em qualquer ordem.

</dd> <dt>

*lpName* \[ out\]
</dt> <dd>

Um ponteiro para um buffer que recebe o nome da sub-chave, incluindo o caractere nulo de terminação. A função copia apenas o nome da sub-chave, não a hierarquia de chave completa, para o buffer. Se a função falhar, nenhuma informação será copiada para esse buffer.

Para obter mais informações, consulte [Limites de tamanho do elemento do Registro](../sysinfo/registry-element-size-limits.md).

</dd> <dt>

*lpcName* \[ in, out\]
</dt> <dd>

Um ponteiro para uma variável que especifica o tamanho do buffer especificado pelo parâmetro *lpName,* em **WCHARs.** Esse tamanho deve incluir o caractere nulo de terminação. Se a função for bem-sucedida, a variável apontada por *lpcName* conterá o número de caracteres armazenados no buffer, não incluindo o caractere nulo de terminação.

</dd> <dt>

*lpClass* \[ out, opcional\]
</dt> <dd>

Um ponteiro para um buffer que recebe a cadeia de caracteres de classe terminada em nulo da sub-chave enumerada. Este parâmetro pode ser **NULL**.

</dd> <dt>

*lpcClass* \[ in, out, opcional\]
</dt> <dd>

Um ponteiro para uma variável que especifica o tamanho do buffer especificado pelo parâmetro *lpClass,* em **WCHARs**. O tamanho deve incluir o caractere nulo de terminação. Se a função for bem-sucedida, *lpcClass* conterá o número de caracteres armazenados no buffer, não incluindo o caractere nulo de terminação. Esse parâmetro poderá ser **NULL** somente se *lpClass* for **NULL.**

</dd> <dt>

*lpftLastWriteTime* \[ out, opcional\]
</dt> <dd>

Um ponteiro para [a estrutura FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) que recebe a hora em que a sub-chave enumerada foi escrita pela última vez. Este parâmetro pode ser **NULL**.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será ERROR \_ SUCCESS.

Se a função falhar, o valor de retorno será um código de erro não zero definido em Winerror.h. Você pode usar a [função FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) com o sinalizador FORMAT MESSAGE FROM SYSTEM para obter \_ uma \_ \_ descrição genérica do erro. Os códigos de erro possíveis incluem o seguinte:

-   Se o buffer *lpName* for muito pequeno para receber o nome da chave, a função retornará ERROR \_ MORE \_ DATA.
-   Se não houver mais sub-chaves disponíveis, a função retornará ERROR \_ NO \_ MORE \_ ITEMS.

## <a name="remarks"></a>Comentários

Para enumerar subkeys, um aplicativo deve chamar inicialmente a **função OREnumKey** com o *parâmetro dwIndex* definido como zero. Em seguida, o aplicativo deve incrementar o parâmetro *dwIndex* e chamar **OREnumKey** até que não haja mais subkeys (o que significa que a função retorna ERROR \_ NO MORE \_ \_ ITEMS).

O aplicativo também pode definir *dwIndex* como o índice da última sub-chave na primeira chamada para a função e decrementar o índice até que a sub-chave com o índice 0 seja enumerada. Para recuperar o índice da última sub-chave, use a [**função ORQueryInfoKey.**](/windows/win32/api/winreg/nf-winreg-regqueryinfokeya)

Enquanto um aplicativo está usando a **função OREnumKey,** ele não deve fazer chamadas para nenhuma função de registro offline que possa alterar a chave que está sendo enumerada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|---------------------------------------------------------------------------------------|
| Redistribuível<br/> | Windows Biblioteca de Registro offline versão 1.0 ou posterior<br/>                      |
| Cabeçalho<br/>          | <dl> <dt>Offreg.h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ORCreateKey**](orcreatekey.md)
</dt> <dt>

[**ORDeleteKey**](ordeletekey.md)
</dt> <dt>

[**OROpenKey**](oropenkey.md)
</dt> <dt>

[**ORQueryInfoKey**](orqueryinfokey.md)
</dt> </dl>

 

 
