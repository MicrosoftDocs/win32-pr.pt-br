---
description: Enumera os valores para a chave do Registro aberta especificada em um hive do Registro offline. A função recupera informações para um valor sob a chave especificada sempre que a função é chamada.
ms.assetid: 592a404f-a35d-4d89-ad1e-d572787bcb12
title: Função OREnumValue (Offreg.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OREnumValue
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 57a65e8fd862215bd6281e487520857580cf6026b94b2ca375079f84407e4cc7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119331796"
---
# <a name="orenumvalue-function"></a>Função OREnumValue

Enumera os valores para a chave do Registro aberta especificada em um hive do Registro offline. A função recupera informações para um valor sob a chave especificada sempre que a função é chamada.

## <a name="syntax"></a>Sintaxe


```C++
DWORD OREnumValue(
  _In_        ORHKEY Handle,
  _In_        DWORD  dwIndex,
  _Out_       PWSTR  lpValueName,
  _Inout_     PDWORD lpcValueName,
  _Out_opt_   PDWORD lpType,
  _Out_opt_   PBYTE  lpData,
  _Inout_opt_ PDWORD lpcbData
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

O índice do valor a ser recuperado. Esse parâmetro deve ser zero para a primeira chamada para a função e, em seguida, ser incrementado para chamadas subsequentes.

Como os valores não são ordenados, qualquer novo valor terá um índice arbitrário. Isso significa que a função pode retornar valores em qualquer ordem.

</dd> <dt>

*lpValueName* \[ out\]
</dt> <dd>

Um ponteiro para um buffer que recebe o nome do valor como uma cadeia de caracteres terminada em nulo. Esse buffer deve ser grande o suficiente para incluir o caractere nulo de terminação.

Para obter mais informações, consulte [Limites de tamanho do elemento do Registro](../sysinfo/registry-element-size-limits.md).

</dd> <dt>

*lpcValueName* \[ in, out\]
</dt> <dd>

Um ponteiro para uma variável que especifica o tamanho do buffer apontado pelo parâmetro *lpValueName,* em caracteres. Quando a função retorna, a variável recebe o número de caracteres armazenados no buffer, não incluindo o caractere nulo de terminação.

</dd> <dt>

*lpType* \[ out, opcional\]
</dt> <dd>

Um ponteiro para uma variável que recebe um código que indica o tipo de dados armazenados no valor especificado. Para ver uma lista dos códigos de tipo possíveis, consulte [Tipos de valor do Registro](../sysinfo/registry-value-types.md). O *parâmetro lpType* poderá ser **NULL se** o código de tipo não for necessário.

</dd> <dt>

*lpData* \[ out, opcional\]
</dt> <dd>

Um ponteiro para um buffer que recebe os dados para a entrada de valor. Esse parâmetro poderá ser **NULL** se os dados não são necessários.

Se *lpData* for **NULL** e *lpcbData* for não **NULL,** a função armazenará o tamanho dos dados, em bytes, na variável apontada por *lpcbData*. Isso permite que um aplicativo determine a melhor maneira de alocar um buffer para os dados.

</dd> <dt>

*lpcbData* \[ in, out, opcional\]
</dt> <dd>

Um ponteiro para uma variável que especifica o tamanho do buffer apontado pelo parâmetro *lpData,* em bytes. Quando a função retorna, a variável recebe o número de bytes armazenados no buffer.

Esse parâmetro poderá ser **NULL** somente se *lpData* for **NULL.**

Se os dados têm o tipo REG SZ, REG MULTI SZ ou REG EXPAND SZ, esse tamanho inclui qualquer caractere \_ \_ \_ \_ \_ nulo de terminação ou caracteres. Para obter mais informações, consulte Comentários.

Se o buffer especificado por *lpData* não for grande o suficiente para armazenar os dados, a função retornará ERROR MORE DATA e armazenará o tamanho do buffer necessário na variável apontada por \_ \_ *lpcbData*. Nesse caso, o conteúdo de *lpData* é indefinido.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será ERROR \_ SUCCESS.

Se a função falhar, o valor de retorno será um código de erro não zero definido em Winerror.h. Você pode usar a [função FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) com o sinalizador FORMAT MESSAGE FROM SYSTEM para obter \_ uma \_ \_ descrição genérica do erro.

Se o buffer *lpData* for muito pequeno para receber o valor, a função retornará ERROR \_ MORE \_ DATA.

## <a name="remarks"></a>Comentários

Para enumerar valores, um aplicativo deve chamar inicialmente a **função OREnumValue** com o *parâmetro dwIndex* definido como zero. Em seguida, o aplicativo deve incrementar *dwIndex* e chamar a **função OREnumValue** até que não haja mais valores (até que a função retorne ERROR \_ NO MORE \_ \_ ITEMS).

O aplicativo também pode definir *dwIndex* como o índice do último valor na primeira chamada para a função e decrementar o índice até que o valor com o índice 0 seja enumerado. Para recuperar o índice do último valor, use a [**função ORQueryInfoKey.**](orqueryinfokey.md)

Ao usar **OREnumValue**, um aplicativo não deve chamar nenhuma função de registro offline que possa alterar a chave que está sendo consultada.

Se os dados têm o tipo REG SZ, REG MULTI SZ ou REG EXPAND SZ, a cadeia de caracteres pode não ter sido armazenada com os caracteres de \_ \_ \_ \_ \_ terminação nula adequados. Portanto, mesmo que a função retorne ERROR SUCCESS, o aplicativo deve garantir que a cadeia de caracteres seja terminada corretamente antes de usá-la; caso contrário, ela poderá substituir \_ um buffer. (Observe que REG \_ Cadeias \_ de caracteres MULTI SZ devem ter dois caracteres de terminação nula.)

Para determinar o tamanho máximo do nome e dos buffers de dados, use a [**função ORQueryInfoKey.**](orqueryinfokey.md)

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

[**OREnumKey**](orenumkey.md)
</dt> <dt>

[**OROpenKey**](oropenkey.md)
</dt> <dt>

[**ORQueryInfoKey**](orqueryinfokey.md)
</dt> </dl>

 

 
