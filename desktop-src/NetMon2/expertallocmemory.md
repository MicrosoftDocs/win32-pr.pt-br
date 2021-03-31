---
description: A função ExpertAllocMemory aloca memória para o especialista.
ms.assetid: 9ada5d3f-5f1d-4d3a-b79a-d51e021240f6
title: Função ExpertAllocMemory (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertAllocMemory
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: b30aba5e2b448df141d0c82e6ec5a2b0d9b3303f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646801"
---
# <a name="expertallocmemory-function"></a>Função ExpertAllocMemory

A função **ExpertAllocMemory** aloca memória para o especialista.

## <a name="syntax"></a>Sintaxe


```C++
LPVOID WINAPI ExpertAllocMemory(
        HEXPERTKEY hExpertKey,
  _In_  SIZE_T     nBytes,
  _Out_ LPDWORD    pError
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hExpertKey* 
</dt> <dd>

Identificador de especialista exclusivo. Monitor de Rede passa *hExpertKey* para o especialista ao chamar a função [Run](run.md) .

</dd> <dt>

*nbytes* \[ no\]
</dt> <dd>

Memória alocada, medida em bytes.

</dd> <dt>

*perror* \[ fora\]
</dt> <dd>

Indicador de erro. Se a função falhar, o parâmetro *nbytes* conterá o código de erro. Se o código de erro for NMERR \_ expert \_ Finalize, o especialista deverá limpar e retornar imediatamente.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, o valor de retorno será um ponteiro para a memória alocada.

Se a função não for bem-sucedida, o valor de retorno será **nulo** e *perror* fornecerá um código de erro que indica o motivo da falha.

## <a name="remarks"></a>Comentários

É importante observar que um especialista deve usar as funções de alocação de memória Monitor de Rede (incluindo [ExpertReallocMemory](expertreallocmemory.md)) para o gerenciamento de memória. Se o seu especialista falhar durante o tempo de execução, usar essas funções permitirá Monitor de Rede liberar a memória alocada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




