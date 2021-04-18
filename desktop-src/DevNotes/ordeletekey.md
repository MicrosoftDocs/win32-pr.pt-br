---
description: Exclui uma subchave e seus valores de um hive do registro offline.
ms.assetid: 651795d3-4328-4281-9a7f-ba75b4ec4da1
title: Função ORDeleteKey (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORDeleteKey
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: a122be2e738bb16730eee31772fc2c1c0671eddb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751951"
---
# <a name="ordeletekey-function"></a>Função ORDeleteKey

Exclui uma subchave e seus valores de um hive do registro offline.

## <a name="syntax"></a>Sintaxe


```C++
DWORD ORDeleteKey(
  _In_     ORHKEY Handle,
  _In_opt_ PCWSTR lpSubKey
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Identificador* \[ do no\]
</dt> <dd>

Um identificador para uma chave do registro aberta em um hive do registro offline. Esse identificador é retornado pela função [**ORCreateKey**](orcreatekey.md) ou [**OROpenKey**](oropenkey.md) .

</dd> <dt>

*lpSubKey* \[ em, opcional\]
</dt> <dd>

O nome da chave a ser excluída. Ele deve ser uma subchave da chave que o *identificador* identifica, mas não pode ter subchaves.

Se a subchave não existir, a função retornará o erro \_ não \_ encontrado.

Se esse parâmetro for **NULL**, a função excluirá a chave especificada pelo parâmetro *Handle* . Se a chave especificada pelo parâmetro *Handle* for a chave raiz do hive, a função retornará um parâmetro de erro \_ inválido \_ .

Os nomes de chave não diferenciam maiúsculas de minúsculas.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, o valor de retorno será \_ êxito no erro.

Se a função falhar, o valor de retorno será um código de erro diferente de zero definido em Winerror. h. Você pode usar a função [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) com a \_ mensagem de formato \_ do \_ sinalizador do sistema para obter uma descrição genérica do erro. Os códigos de erro possíveis incluem o seguinte:

-   Se a subchave especificada não existir, a função retornará o \_ arquivo de erro \_ não \_ encontrado.
-   Se a subchave especificada for a chave raiz do hive do registro, a função retornará um parâmetro de erro \_ inválido \_ .
-   Se a subchave especificada tiver subchaves, a função retornará a chave de erro \_ \_ tem \_ filhos.

## <a name="remarks"></a>Comentários

Se a chave do Registro especificada existir, ela será marcada como excluída. Uma chave excluída não é removida até que o último identificador seja fechado.

A chave a ser excluída não deve ter subchaves. Para excluir uma chave e todas as suas subchaves, use a função [**OREnumKey**](orenumkey.md) para enumerar as subchaves e excluí-las individualmente.

Somente a função [**ORCloseKey**](orclosekey.md) pode ser chamada em uma chave excluída; todas as outras operações de registro offline falham. Se a chave excluída tiver sido explicitamente criada chamando [**ORCreateKey**](orcreatekey.md), os recursos associados à chave serão liberados quando o último identificador da chave excluída for fechado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|---------------------------------------------------------------------------------------|
| Redistribuível<br/> | Biblioteca de registro offline do Windows versão 1,0 ou posterior<br/>                      |
| parâmetro<br/>          | <dl> <dt>Offreg. h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ORCloseKey**](orclosekey.md)
</dt> <dt>

[**ORCreateKey**](orcreatekey.md)
</dt> <dt>

[**OREnumKey**](orenumkey.md)
</dt> <dt>

[**OROpenKey**](oropenkey.md)
</dt> </dl>

 

 
