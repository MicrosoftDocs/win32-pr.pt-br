---
description: Enumera os valores para a chave de registro aberta especificada em um hive de registro offline. A função recupera informações de um valor sob a chave especificada cada vez que a função é chamada.
ms.assetid: 592a404f-a35d-4d89-ad1e-d572787bcb12
title: Função OREnumValue (Offreg. h)
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
ms.openlocfilehash: b8049a5d16a88dc87bf4c0f6f5e8ef18b30beadc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753059"
---
# <a name="orenumvalue-function"></a>Função OREnumValue

Enumera os valores para a chave de registro aberta especificada em um hive de registro offline. A função recupera informações de um valor sob a chave especificada cada vez que a função é chamada.

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

*Identificador* \[ do no\]
</dt> <dd>

Um identificador para uma chave do registro aberta em um hive do registro offline.

</dd> <dt>

*dwIndex* \[ no\]
</dt> <dd>

O índice do valor a ser recuperado. Esse parâmetro deve ser zero para a primeira chamada para a função e, em seguida, ser incrementado para chamadas subsequentes.

Como os valores não são ordenados, qualquer valor novo terá um índice arbitrário. Isso significa que a função pode retornar valores em qualquer ordem.

</dd> <dt>

*lpValueName* \[ fora\]
</dt> <dd>

Um ponteiro para um buffer que recebe o nome do valor como uma cadeia de caracteres terminada em nulo. Esse buffer deve ser grande o suficiente para incluir o caractere nulo de terminação.

Para obter mais informações, consulte [limites de tamanho do elemento do registro](../sysinfo/registry-element-size-limits.md).

</dd> <dt>

*lpcValueName* \[ entrada, saída\]
</dt> <dd>

Um ponteiro para uma variável que especifica o tamanho do buffer apontado pelo parâmetro *lpValueName* , em caracteres. Quando a função retorna, a variável recebe o número de caracteres armazenados no buffer, sem incluir o caractere nulo de terminação.

</dd> <dt>

*lpType* \[ out, opcional\]
</dt> <dd>

Um ponteiro para uma variável que recebe um código que indica o tipo de dados armazenados no valor especificado. Para obter uma lista dos possíveis códigos de tipo, consulte [tipos de valor do registro](../sysinfo/registry-value-types.md). O parâmetro *lpType* poderá ser **nulo** se o código de tipo não for necessário.

</dd> <dt>

*lpData* \[ out, opcional\]
</dt> <dd>

Um ponteiro para um buffer que recebe os dados para a entrada de valor. Esse parâmetro poderá ser **nulo** se os dados não forem necessários.

Se *lpData* for **nulo** e *lpcbData* for não **nulo**, a função armazenará o tamanho dos dados, em bytes, na variável apontada por *lpcbData*. Isso permite que um aplicativo determine a melhor maneira de alocar um buffer para os dados.

</dd> <dt>

*lpcbData* \[ entrada, saída, opcional\]
</dt> <dd>

Um ponteiro para uma variável que especifica o tamanho do buffer apontado pelo parâmetro *lpData* , em bytes. Quando a função retorna, a variável recebe o número de bytes armazenados no buffer.

Esse parâmetro poderá ser **nulo** somente se *lpData* for **nulo**.

Se os dados tiverem o \_ tipo reg sz, Reg \_ multi sz \_ ou reg \_ expande- \_ sz, esse tamanho incluirá qualquer caractere nulo de encerramento ou caracteres. Para obter mais informações, consulte Comentários.

Se o buffer especificado por *lpData* não for grande o suficiente para manter os dados, a função retornará um erro \_ mais \_ dados e armazenará o tamanho de buffer necessário na variável apontada por *lpcbData*. Nesse caso, o conteúdo de *lpData* é indefinido.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, o valor de retorno será \_ êxito no erro.

Se a função falhar, o valor de retorno será um código de erro diferente de zero definido em Winerror. h. Você pode usar a função [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) com a \_ mensagem de formato \_ do \_ sinalizador do sistema para obter uma descrição genérica do erro.

Se o buffer *lpData* for muito pequeno para receber o valor, a função retornará um erro com \_ mais \_ dados.

## <a name="remarks"></a>Comentários

Para enumerar valores, um aplicativo deve chamar inicialmente a função **OREnumValue** com o parâmetro *dwIndex* definido como zero. O aplicativo deve incrementar *dwIndex* e chamar a função **OREnumValue** até que não haja mais valores (até que a função retorne \_ um erro sem \_ mais \_ itens).

O aplicativo também pode definir *dwIndex* como o índice do último valor na primeira chamada para a função e decrementar o índice até que o valor com o índice 0 seja enumerado. Para recuperar o índice do último valor, use a função [**ORQueryInfoKey**](orqueryinfokey.md) .

Ao usar **OREnumValue**, um aplicativo não deve chamar nenhuma função de registro offline que possa alterar a chave que está sendo consultada.

Se os dados tiverem o \_ tipo reg sz, Reg \_ multi sz \_ ou reg \_ expandem \_ sz, a cadeia de caracteres poderá não ter sido armazenada com os caracteres de terminação de nulo apropriados. Portanto, mesmo que a função retorne o êxito do erro \_ , o aplicativo deve garantir que a cadeia de caracteres seja encerrada corretamente antes de usá-la; caso contrário, ela poderá substituir um buffer. (Observe que REG \_ As \_ cadeias de caracteres de vários sz devem ter dois personagens de terminação nulo.)

Para determinar o tamanho máximo do nome e dos buffers de dados, use a função [**ORQueryInfoKey**](orqueryinfokey.md) .

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

[**OREnumKey**](orenumkey.md)
</dt> <dt>

[**OROpenKey**](oropenkey.md)
</dt> <dt>

[**ORQueryInfoKey**](orqueryinfokey.md)
</dt> </dl>

 

 
