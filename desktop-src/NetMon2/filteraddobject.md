---
description: A função FilterAddObject adiciona um único objeto a um filtro de exibição.
ms.assetid: 796216f4-a407-4a8c-98b3-8c3761d91913
title: Função FilterAddObject (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FilterAddObject
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2c7d814efbbc77816836d437161390b1e2af60e8bbf4932322dcbd606920be5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118938729"
---
# <a name="filteraddobject-function"></a>Função FilterAddObject

A **função FilterAddObject** adiciona um único objeto a um [*filtro de exibição*](d.md).

## <a name="syntax"></a>Sintaxe


```C++
DWORD WINAPI FilterAddObject(
  _In_  HFILTER        hFilter,
  _Out_ LPFILTEROBJECT lpFilterObject
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hFilter* \[ Em\]
</dt> <dd>

Manipular para o filtro de exibição.

</dd> <dt>

*lpFilterObject* \[ out\]
</dt> <dd>

Ponteiro para uma [estrutura FILTEROBJECT](filterobject.md) que define o objeto a ser adicionado ao filtro. Cada objeto pode ser um operador, valor ou propriedade.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será NMERR \_ SUCCESS.

Se a função não for bem-sucedida, o valor de retorno será um código de erro.



| Código de retorno                                                                                              | Descrição                                                                  |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <dt>**PARÂMETRO INVÁLIDO \_ NMERR \_**</dt> </dl> | O *parâmetro hFilter* tem um valor inválido.<br/>                     |
| <dl> <dt>**NMERR \_ \_ SEM \_ MEMÓRIA**</dt> </dl>    | Monitor de Rede não tem memória suficiente para criar o objeto.<br/> |



 

## <a name="remarks"></a>Comentários

[*Especialistas*](e.md) e [*analisadores podem*](p.md) chamar a **função FilterAddObject.**

A **função FilterAddObject** é chamada sempre que um objeto de filtro é adicionado ao filtro de exibição. O filtro de exibição é uma pilha de pós-fixação de objetos que podem ser um operador, valor ou propriedade.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[FILTEROBJECT](filterobject.md)
</dt> </dl>

 

 




