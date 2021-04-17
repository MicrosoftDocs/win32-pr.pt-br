---
description: Enumera as subchaves da chave do registro aberta especificada em um hive do registro offline. A função recupera informações sobre uma subchave cada vez que ela é chamada.
ms.assetid: 46d13c37-473a-4772-992c-a565ad702fb9
title: Função OREnumKey (Offreg. h)
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
ms.openlocfilehash: 24278bc59c75f32aed92c2ea5b5428f6ef6d9b45
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748905"
---
# <a name="orenumkey-function"></a>Função OREnumKey

Enumera as subchaves da chave do registro aberta especificada em um hive do registro offline. A função recupera informações sobre uma subchave cada vez que ela é chamada.

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

*Identificador* \[ do no\]
</dt> <dd>

Um identificador para uma chave do registro aberta em um hive do registro offline.

</dd> <dt>

*dwIndex* \[ no\]
</dt> <dd>

O índice da subchave a ser recuperada. Esse parâmetro deve ser zero para a primeira chamada para a função e, em seguida, incrementado para chamadas subsequentes.

Como as subchaves não são ordenadas, qualquer subnovação terá um índice arbitrário. Isso significa que a função pode retornar subchaves em qualquer ordem.

</dd> <dt>

*lpName* \[ fora\]
</dt> <dd>

Um ponteiro para um buffer que recebe o nome da subchave, incluindo o caractere nulo de terminação. A função copia apenas o nome da subchave, não a hierarquia de chave completa, para o buffer. Se a função falhar, nenhuma informação será copiada para esse buffer.

Para obter mais informações, consulte [limites de tamanho do elemento do registro](../sysinfo/registry-element-size-limits.md).

</dd> <dt>

*lpcName* \[ entrada, saída\]
</dt> <dd>

Um ponteiro para uma variável que especifica o tamanho do buffer especificado pelo parâmetro *lpName* , em **WCHARs**. Esse tamanho deve incluir o caractere nulo de terminação. Se a função for realizada com sucesso, a variável apontada por *lpcName* conterá o número de caracteres armazenados no buffer, sem incluir o caractere nulo de terminação.

</dd> <dt>

*lpClass* \[ out, opcional\]
</dt> <dd>

Um ponteiro para um buffer que recebe a cadeia de caracteres de classe terminada em nulo da subchave enumerada. Este parâmetro pode ser **NULL**.

</dd> <dt>

*lpcClass* \[ entrada, saída, opcional\]
</dt> <dd>

Um ponteiro para uma variável que especifica o tamanho do buffer especificado pelo parâmetro *lpClass* , em **WCHARs**. O tamanho deve incluir o caractere nulo de terminação. Se a função for realizada com sucesso, *lpcClass* conterá o número de caracteres armazenados no buffer, sem incluir o caractere nulo de terminação. Esse parâmetro poderá ser **nulo** somente se *lpClass* for **nulo**.

</dd> <dt>

*lpftLastWriteTime* \[ out, opcional\]
</dt> <dd>

Um ponteiro para a estrutura [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) que recebe a hora em que a subchave enumerada foi gravada pela última vez. Este parâmetro pode ser **NULL**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, o valor de retorno será \_ êxito no erro.

Se a função falhar, o valor de retorno será um código de erro diferente de zero definido em Winerror. h. Você pode usar a função [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) com a \_ mensagem de formato \_ do \_ sinalizador do sistema para obter uma descrição genérica do erro. Os códigos de erro possíveis incluem o seguinte:

-   Se o buffer *lpName* for muito pequeno para receber o nome da chave, a função retornará um erro com \_ mais \_ dados.
-   Se não houver mais subchaves disponíveis, a função retornará \_ um erro sem \_ mais \_ itens.

## <a name="remarks"></a>Comentários

Para enumerar subchaves, um aplicativo deve chamar inicialmente a função **OREnumKey** com o parâmetro *dwIndex* definido como zero. O aplicativo deve incrementar o parâmetro *dwIndex* e chamar **OREnumKey** até que não haja mais subchaves (o que significa que a função retorna \_ um erro sem \_ mais \_ itens).

O aplicativo também pode definir *dwIndex* para o índice da última subchave na primeira chamada para a função e decrementar o índice até que a subchave com o índice 0 seja enumerada. Para recuperar o índice da última subchave, use a função [**ORQueryInfoKey**](/windows/win32/api/winreg/nf-winreg-regqueryinfokeya) .

Embora um aplicativo esteja usando a função **OREnumKey** , ele não deve fazer chamadas para nenhuma das funções de registro offline que possam alterar a chave que está sendo enumerada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|---------------------------------------------------------------------------------------|
| Redistribuível<br/> | Biblioteca de registro offline do Windows versão 1,0 ou posterior<br/>                      |
| parâmetro<br/>          | <dl> <dt>Offreg. h</dt> </dl>   |
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

 

 
