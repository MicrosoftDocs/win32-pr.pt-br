---
description: Cria um hive de registro offline que contém uma única chave de raiz vazia.
ms.assetid: 985cfea4-6f15-4d63-8e41-df2a490296a3
title: Função ORCreateHive (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORCreateHive
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 47454169bee21012010fd7deacec6c1faf3a7d8d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752169"
---
# <a name="orcreatehive-function"></a>Função ORCreateHive

Cria um hive de registro offline que contém uma única chave de raiz vazia.

## <a name="syntax"></a>Sintaxe


```C++
DWORD ORCreateHive(
  _Out_ PORHKEY phkResult
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*phkResult* \[ fora\]
</dt> <dd>

Aponta para uma variável para receber um identificador para a chave raiz do hive do registro offline recém-criado. Se o hive não puder ser criado, a função definirá esse parâmetro como **NULL**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, o valor de retorno será \_ êxito no erro.

Se a função falhar, o valor de retorno será um código de erro diferente de zero definido em Winerror. h. Você pode usar a função [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) com a \_ mensagem de formato \_ do \_ sinalizador do sistema para obter uma descrição genérica do erro.

Se não houver memória suficiente para criar o hive do registro, a função retornará um erro de \_ \_ memória insuficiente \_ .

## <a name="remarks"></a>Comentários

A função **ORCreateHive** cria um hive de registro offline vazio na memória. Use as funções [**ORCreateKey**](orcreatekey.md) e [**ORSetValue**](orsetvalue.md) para adicionar chaves e definir seus valores.

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

[**OROpenHive**](oropenhive.md)
</dt> <dt>

[**ORSaveHive**](orsavehive.md)
</dt> <dt>

[**ORSetValue**](orsetvalue.md)
</dt> </dl>

 

 
