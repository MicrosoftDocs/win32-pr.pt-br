---
description: Exclui uma sub-chave e seus valores de um hive de registro offline.
ms.assetid: 651795d3-4328-4281-9a7f-ba75b4ec4da1
title: Função ORDeleteKey (Offreg.h)
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
ms.openlocfilehash: 9f3be934eca97d88f4dfeb1b1576d9fcd06f5681351a2e85d8ae7f6ba31e8860
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119571926"
---
# <a name="ordeletekey-function"></a>Função ORDeleteKey

Exclui uma sub-chave e seus valores de um hive de registro offline.

## <a name="syntax"></a>Sintaxe


```C++
DWORD ORDeleteKey(
  _In_     ORHKEY Handle,
  _In_opt_ PCWSTR lpSubKey
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Manipular* \[ Em\]
</dt> <dd>

Um handle para uma chave aberta do Registro em um hive de registro offline. Esse handle é retornado pela [**função ORCreateKey**](orcreatekey.md) [**ou OROpenKey.**](oropenkey.md)

</dd> <dt>

*lpSubKey* \[ in, opcional\]
</dt> <dd>

O nome da chave a ser excluída. Ele deve ser uma sub-chave da chave que *o Identificador* identifica, mas não pode ter sub-chaves.

Se a sub-chave não existir, a função retornará ERROR \_ NOT \_ FOUND.

Se esse parâmetro for **NULL,** a função excluirá a chave especificada pelo *parâmetro* Handle. Se a chave especificada pelo parâmetro *Handle* for a chave raiz do hive, a função retornará ERROR \_ INVALID \_ PARAMETER.

Os nomes de chave não são sensíveis a minúsculas.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será ERROR \_ SUCCESS.

Se a função falhar, o valor de retorno será um código de erro não zero definido em Winerror.h. Você pode usar a [função FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) com o sinalizador FORMAT MESSAGE FROM SYSTEM para obter \_ uma \_ \_ descrição genérica do erro. Os códigos de erro possíveis incluem o seguinte:

-   Se a sub-chave especificada não existir, a função retornará ERROR \_ FILE \_ NOT \_ FOUND.
-   Se a sub-chave especificada for a chave raiz do hive do Registro, a função retornará ERROR \_ INVALID \_ PARAMETER.
-   Se a sub-chave especificada tiver sub-chaves, a função retornará ERROR \_ KEY \_ HAS \_ CHILDREN.

## <a name="remarks"></a>Comentários

Se a chave do Registro especificada existir, ela será marcada como excluída. Uma chave excluída não é removida até que o último alça para ela seja fechado.

A chave a ser excluída não deve ter sub-chaves. Para excluir uma chave e todas as suas sub-chaves, use a [**função OREnumKey**](orenumkey.md) para enumerar as sub-chaves e excluí-las individualmente.

Somente a [**função ORCloseKey**](orclosekey.md) pode ser chamada em uma chave excluída; todas as outras operações de registro offline falham. Se a chave excluída tiver sido criada explicitamente chamando [**ORCreateKey,**](orcreatekey.md)os recursos associados à chave serão liberados quando o último lidar com a chave excluída for fechado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|---------------------------------------------------------------------------------------|
| Redistribuível<br/> | Windows Biblioteca de Registro offline versão 1.0 ou posterior<br/>                      |
| Cabeçalho<br/>          | <dl> <dt>Offreg.h</dt> </dl>   |
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

 

 
