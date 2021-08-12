---
description: Abre a chave do Registro especificada em um hive do registro offline.
ms.assetid: 4a4afbef-5107-4006-bd67-aecb5d3b5112
title: Função OROpenKey (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OROpenKey
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 4c0f641925fbc35fba6072ee395f67fad540dcd2ec5198b945ad658a723238b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118667089"
---
# <a name="oropenkey-function"></a>Função OROpenKey

Abre a chave do Registro especificada em um hive do registro offline.

## <a name="syntax"></a>Sintaxe


```C++
DWORD OROpenKey(
  _In_     ORHKEY  Handle,
  _In_opt_ PCWSTR  lpSubKeyName,
  _Out_    PORHKEY phkResult
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Identificador* \[ do no\]
</dt> <dd>

Um identificador para uma chave do registro aberta em um hive do registro offline.

</dd> <dt>

*lpSubKeyName* \[ em, opcional\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres UNICODE que contém o nome da chave do registro a ser aberta. Essa chave deve ser uma subchave da chave identificada pelo parâmetro *Handle* .

Os nomes de chave não diferenciam maiúsculas de minúsculas.

Se esse parâmetro for **nulo** ou um ponteiro para uma cadeia de caracteres vazia, a função retornará o mesmo identificador que foi passado. Se a chave especificada pelo parâmetro *Handle* for a chave raiz do hive, a função retornará um parâmetro de erro \_ inválido \_ .

Para obter mais informações, consulte [limites de tamanho do elemento do registro](../sysinfo/registry-element-size-limits.md).

</dd> <dt>

*phkResult* \[ fora\]
</dt> <dd>

Um ponteiro para uma variável que recebe um identificador para a chave aberta. Use a função [**ORCloseKey**](orclosekey.md) para fechar a chave depois de terminar de usar o identificador.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será \_ êxito no erro.

Se a função falhar, o valor de retorno será um código de erro diferente de zero definido em Winerror. h. Você pode usar a função [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) com a \_ mensagem de formato \_ do \_ sinalizador do sistema para obter uma descrição genérica do erro.

Se o identificador a ser retornado for um identificador para a chave raiz do hive, a função retornará um parâmetro de erro \_ inválido \_ .

Se a chave especificada tiver sido marcada como excluída, essa função retornará a chave de erro \_ \_ excluída.

## <a name="remarks"></a>Comentários

A função **OROpenKey** não pode ser usada para abrir a chave raiz em um hive do registro offline. Para obter um identificador para a chave raiz de um Hive, use a função [**OROpenHive**](oropenhive.md) para carregar o hive na memória.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|---------------------------------------------------------------------------------------|
| Redistribuível<br/> | Windows Biblioteca de registro offline versão 1,0 ou posterior<br/>                      |
| parâmetro<br/>          | <dl> <dt>Offreg. h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ORCloseKey**](orclosekey.md)
</dt> <dt>

[**ORCreateKey**](orcreatekey.md)
</dt> <dt>

[**ORDeleteKey**](ordeletekey.md)
</dt> <dt>

[**OROpenHive**](oropenhive.md)
</dt> </dl>

 

 
