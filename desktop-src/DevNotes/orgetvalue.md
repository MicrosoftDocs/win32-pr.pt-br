---
description: Recupera o tipo e os dados para o valor do registro especificado em um hive do registro offline.
ms.assetid: 83604743-cb59-42a1-9951-620ad5bd8de7
title: Função ORGetValue (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORGetValue
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: fc364e208e9c243754edf8731f077ec48e9133d4a95ba86b5a1f99971192b51e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120058646"
---
# <a name="orgetvalue-function"></a>Função ORGetValue

Recupera o tipo e os dados para o valor do registro especificado em um hive do registro offline.

## <a name="syntax"></a>Sintaxe


```C++
DWORD ORGetValue(
  _In_        ORHKEY Handle,
  _In_opt_    PCWSTR lpSubKey,
  _In_opt_    PCWSTR lpValue,
  _Out_opt_   PDWORD pdwType,
  _Out_opt_   PVOID  pvData,
  _Inout_opt_ PDWORD pcbData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Identificador* \[ do no\]
</dt> <dd>

Um identificador para uma chave do registro aberta em um hive do registro offline.

</dd> <dt>

*lpSubKey* \[ em, opcional\]
</dt> <dd>

O nome da chave do Registro. Essa chave deve ser uma subchave da chave especificada pelo parâmetro *Handle* . Este parâmetro pode ser **NULL**.

Os nomes de chave não diferenciam maiúsculas de minúsculas.

</dd> <dt>

*lpValue* \[ em, opcional\]
</dt> <dd>

O nome do valor do registro. Se esse parâmetro for **nulo** ou uma cadeia de caracteres vazia, "", a função recuperará o tipo e os dados para o valor padrão ou não nomeado da chave, se houver. Para obter mais informações, consulte [limites de tamanho do elemento do registro](../sysinfo/registry-element-size-limits.md).

As chaves não têm um valor padrão ou não nomeado automaticamente. Os valores não nomeados podem ser de qualquer tipo.

Os nomes de valores não diferenciam maiúsculas de minúsculas.

</dd> <dt>

*pdwType* \[ out, opcional\]
</dt> <dd>

Um ponteiro para uma variável que recebe um código que indica o tipo de dados armazenados no valor especificado. Para obter uma lista dos possíveis códigos de tipo, consulte [tipos de valor do registro](../sysinfo/registry-value-types.md). Esse parâmetro poderá ser **nulo** se o tipo não for necessário.

</dd> <dt>

*pvData* \[ out, opcional\]
</dt> <dd>

Um ponteiro para um buffer que recebe os dados do valor. Esse parâmetro poderá ser **nulo** se os dados não forem necessários.

Se os dados forem uma cadeia de caracteres, a função verificará se há um caractere nulo de terminação. Se um não for encontrado, a cadeia de caracteres será armazenada com um terminador nulo se o buffer for grande o suficiente para acomodar o caractere extra. Caso contrário, a função falhará e retornará \_ mais dados de erro \_ .

</dd> <dt>

*pcbData* \[ entrada, saída, opcional\]
</dt> <dd>

Um ponteiro para uma variável que especifica o tamanho do buffer apontado pelo parâmetro *pvData* , em bytes. Quando a função retorna, essa variável contém o tamanho dos dados copiados para *pvData*.

O parâmetro *pcbData* poderá ser **nulo** somente se *pvData* for **nulo**.

Se os dados tiverem o \_ tipo reg sz, Reg \_ multi sz \_ ou reg \_ expande- \_ sz, esse tamanho incluirá qualquer caractere nulo de encerramento ou caracteres. Para obter mais informações, consulte Comentários.

Se o buffer especificado pelo parâmetro *pvData* não for grande o suficiente para manter os dados, a função retornará um erro \_ mais \_ dados e armazenará o tamanho de buffer necessário na variável apontada por *pcbData*. Nesse caso, o conteúdo do buffer *pvData* é indefinido.

Se *pvData* for **nulo** e *pcbData* for não **nulo**, a função retornará êxito de erro \_ e armazenará o tamanho dos dados, em bytes, na variável apontada por *pcbData*. Isso permite que um aplicativo determine a melhor maneira de alocar um buffer para os dados do valor.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será \_ êxito no erro.

Se a função falhar, o valor de retorno será um código de erro diferente de zero definido em Winerror. h. Você pode usar a função [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) com a \_ mensagem de formato \_ do \_ sinalizador do sistema para obter uma descrição genérica do erro.

## <a name="remarks"></a>Comentários

Um aplicativo normalmente chama a função [**OREnumValue**](orenumvalue.md) para determinar os nomes de valor e, em seguida, chama a função **ORGetValue** para recuperar os dados para os nomes.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|---------------------------------------------------------------------------------------|
| Redistribuível<br/> | Windows Biblioteca de registro offline versão 1,0 ou posterior<br/>                      |
| Cabeçalho<br/>          | <dl> <dt>Offreg. h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ORCreateKey**](orcreatekey.md)
</dt> <dt>

[**OREnumKey**](orenumkey.md)
</dt> <dt>

[**OREnumValue**](orenumvalue.md)
</dt> <dt>

[**OROpenKey**](oropenkey.md)
</dt> <dt>

[**ORQueryInfoKey**](orqueryinfokey.md)
</dt> </dl>

 

 
