---
description: A função ExpertReallocMemory aumenta ou diminui a quantidade de memória alocada por Monitor de Rede.
ms.assetid: 78b99a66-692a-4e83-8b0d-d68caf156bb6
title: Função ExpertReallocMemory (Netmon.h)
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
ms.openlocfilehash: be43fa99021ec5612a148ba42db1b11e1fd6d885fa64fa003c0dfa672688d555
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012254"
---
# <a name="expertreallocmemory-function"></a>Função ExpertReallocMemory

A **função ExpertReallocMemory** aumenta ou diminui a quantidade de memória alocada por Monitor de Rede.

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

*hExpertKey* \[ Em\]
</dt> <dd>

Identificador exclusivo passado para o especialista em [**Executar**](run.md) ou [**Configurar**](configure.md).

</dd> <dt>

*pOriginalMemory* \[ Em\]
</dt> <dd>

Ponteiro para a memória alocada por Monitor de Rede. O *ponteiro pOriginalMemory* pode ser retornado por uma chamada anterior para [**ExpertAllocMemory**](expertallocmemory.md) ou **ExpertReallocMemory.**

</dd> <dt>

*nBytes* \[ Em\]
</dt> <dd>

Tamanho da memória realocada.

</dd> <dt>

*pError* \[ out\]
</dt> <dd>

No retorno, um código de erro se a função falhar. Se o código de erro for NMERR \_ EXPERT \_ TERMINATE, o especialista deverá limpar e retornar imediatamente.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será um ponteiro para a memória alocada.

Se a função não for bem-sucedida, o valor de retorno será **NULL** e *pError* (se for um valor não **NULL)** indicará o motivo da falha.

## <a name="remarks"></a>Comentários

É importante observar que um especialista deve usar as funções de alocação Monitor de Rede memória para gerenciamento de memória. Se o especialista falhar durante o tempo de operação, o uso dessas funções permitirá Monitor de Rede liberar a memória alocada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




