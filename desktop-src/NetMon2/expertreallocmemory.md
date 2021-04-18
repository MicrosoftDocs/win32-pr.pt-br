---
description: A função ExpertReallocMemory aumenta ou diminui a quantidade de memória alocada por Monitor de Rede.
ms.assetid: 78b99a66-692a-4e83-8b0d-d68caf156bb6
title: Função ExpertReallocMemory (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertReallocMemory
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 8f562443f9ca66def7e053f5958b17e70af50140
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105752234"
---
# <a name="expertreallocmemory-function"></a>Função ExpertReallocMemory

A função **ExpertReallocMemory** aumenta ou diminui a quantidade de memória alocada por monitor de rede.

## <a name="syntax"></a>Sintaxe


```C++
LPVOID WINAPI ExpertReallocMemory(
  _In_  HEXPERTKEY hExpertKey,
  _In_  LPVOID     pOriginalMemory,
  _In_  SIZE_T     nBytes,
  _Out_ LPDWORD    pError
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hExpertKey* \[ no\]
</dt> <dd>

Identificador exclusivo passado para o especialista em [**executar**](run.md) ou [**Configurar**](configure.md).

</dd> <dt>

*pOriginalMemory* \[ no\]
</dt> <dd>

Ponteiro para a memória alocada por Monitor de Rede. O ponteiro *pOriginalMemory* pode ser retornado por uma chamada anterior para [**ExpertAllocMemory**](expertallocmemory.md) ou **ExpertReallocMemory**.

</dd> <dt>

*nbytes* \[ no\]
</dt> <dd>

Tamanho da memória realocada.

</dd> <dt>

*perror* \[ fora\]
</dt> <dd>

No retorno, um código de erro se a função falhar. Se o código de erro for NMERR \_ expert \_ Finalize, o especialista deverá limpar e retornar imediatamente.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, o valor de retorno será um ponteiro para a memória alocada.

Se a função não for bem-sucedida, o valor de retorno será **nulo** e *perror* (se for um valor não **nulo** ) indica o motivo da falha.

## <a name="remarks"></a>Comentários

É importante observar que um especialista deve usar as funções de alocação de memória Monitor de Rede para gerenciamento de memória. Se o seu especialista falhar durante o tempo de execução, usar essas funções permitirá Monitor de Rede liberar a memória alocada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




