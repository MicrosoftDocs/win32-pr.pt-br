---
description: A função ExpertFreeMemory libera a memória adquirida por chamadas para as funções ExpertAllocMemory e ExpertReallocMemory.
ms.assetid: 0e7cc791-98dd-4522-afab-76ac9e74c715
title: Função ExpertFreeMemory (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertFreeMemory
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: cc26056a3ec3e8820c363d97f92c7eb382cd0622
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105757106"
---
# <a name="expertfreememory-function"></a>Função ExpertFreeMemory

A função **ExpertFreeMemory** libera a memória adquirida por chamadas para as funções [**ExpertAllocMemory**](expertallocmemory.md) e [**ExpertReallocMemory**](expertreallocmemory.md) .

## <a name="syntax"></a>Sintaxe


```C++
SIZE_T WINAPI ExpertFreeMemory(
       HEXPERTKEY hExpertKey,
  _In_ LPVOID     pMemory
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hExpertKey* 
</dt> <dd>

Identificador de especialista exclusivo. Monitor de Rede passa *hExpertKey* para o especialista ao chamar a função [Run](run.md) .

</dd> <dt>

*pMemory* \[ no\]
</dt> <dd>

Ponteiro para a memória que Monitor de Rede aloca. O ponteiro *pMemory* pode ser retornado por uma chamada anterior para [**ExpertAllocMemory**](expertallocmemory.md) ou [**ExpertReallocMemory**](expertreallocmemory.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida. o valor de retorno é NMERR \_ Success.

Se a função não for bem-sucedida, o valor de retorno indicará o motivo da falha. Se o valor de retorno for NMERR \_ expert \_ Finalize, o especialista limpará e retornará imediatamente.

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



 

 




