---
description: Remove um valor nomeado da chave do Registro especificada em um hive do registro offline.
ms.assetid: d2192607-34b8-4915-ac86-8ee206993071
title: Função ORDeleteValue (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORDeleteValue
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 717464b1ba44593a9b36ccf26e5df248cb95df9bfa40a7786896c87041e246d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045286"
---
# <a name="ordeletevalue-function"></a>Função ORDeleteValue

Remove um valor nomeado da chave do Registro especificada em um hive do registro offline.

## <a name="syntax"></a>Sintaxe


```C++
DWORD ORDeleteValue(
  _In_     ORHKEY Handle,
  _In_opt_ PCWSTR lpValueName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Identificador* \[ do no\]
</dt> <dd>

Um identificador para uma chave do registro aberta em um hive do registro offline.

</dd> <dt>

*lpValueName* \[ em, opcional\]
</dt> <dd>

O valor do registro a ser removido. Se esse parâmetro for **nulo** ou uma cadeia de caracteres vazia, o valor padrão sem nome definido pela função [**ORSetValue**](orsetvalue.md) será removido.

Os nomes de valores não diferenciam maiúsculas de minúsculas.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será \_ êxito no erro.

Se a função falhar, o valor de retorno será um código de erro diferente de zero definido em Winerror. h. Você pode usar a função [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) com a \_ mensagem de formato \_ do \_ sinalizador do sistema para obter uma descrição genérica do erro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|---------------------------------------------------------------------------------------|
| Redistribuível<br/> | Windows Biblioteca de registro offline versão 1,0 ou posterior<br/>                      |
| Cabeçalho<br/>          | <dl> <dt>Offreg. h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ORSetValue**](orsetvalue.md)
</dt> </dl>

 

 
