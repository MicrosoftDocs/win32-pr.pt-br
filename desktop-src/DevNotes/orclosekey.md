---
description: Fecha um identificador para a chave do Registro especificada em um hive do registro offline.
ms.assetid: 01bb21b1-217b-4716-ae1e-466cf8383155
title: Função ORCloseKey (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORCloseKey
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 28f93c2bb1de61da072d7fde6d811463106be0c56f049b3ebf7e74f79ef740fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119572106"
---
# <a name="orclosekey-function"></a>Função ORCloseKey

Fecha um identificador para a chave do Registro especificada em um hive do registro offline.

## <a name="syntax"></a>Sintaxe


```C++
DWORD ORCloseKey(
  _In_ ORHKEY Handle
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Identificador* \[ do no\]
</dt> <dd>

Um identificador para uma chave do registro aberta em um hive do registro offline.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será \_ êxito no erro.

Se a função falhar, o valor de retorno será um código de erro diferente de zero definido em Winerror. h. Você pode usar a função [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) com a \_ mensagem de formato \_ do \_ sinalizador do sistema para obter uma descrição genérica do erro.

Se a chave especificada for a chave raiz do hive do registro, a função falhará com o parâmetro de erro \_ inválido \_ .

## <a name="remarks"></a>Comentários

O identificador de uma chave especificada não deve ser usado depois de ser fechado, pois ele não será mais válido. Os identificadores de chave não devem ser deixados abertos mais do que o necessário.

Use a função [**ORCloseHive**](orclosehive.md) para fechar um hive do registro offline.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|---------------------------------------------------------------------------------------|
| Redistribuível<br/> | Windows Biblioteca de registro offline versão 1,0 ou posterior<br/>                      |
| Cabeçalho<br/>          | <dl> <dt>Offreg. h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ORCloseHive**](orclosehive.md)
</dt> <dt>

[**ORCreateKey**](orcreatekey.md)
</dt> <dt>

[**ORDeleteKey**](ordeletekey.md)
</dt> <dt>

[**OROpenKey**](oropenkey.md)
</dt> </dl>

 

 
