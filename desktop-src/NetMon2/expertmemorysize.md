---
description: A função ExpertMemorySize retorna a quantidade de memória alocada pela função ExpertAllocMemory.
ms.assetid: 60d3f33d-dc03-4c39-98fa-ec093398b51b
title: Função ExpertMemorySize (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertMemorySize
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 57c83bc3e9535550086c9732b33a71a357e4da42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826839"
---
# <a name="expertmemorysize-function"></a>Função ExpertMemorySize

A função **ExpertMemorySize** retorna a quantidade de memória alocada pela função [ExpertAllocMemory](expertallocmemory.md) .

## <a name="syntax"></a>Sintaxe


```C++
SIZE_T WINAPI ExpertMemorySize(
  _In_ HEXPERTKEY hExpertKey,
  _In_ LPVOID     pOriginalMemory
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hExpertKey* \[ no\]
</dt> <dd>

Identificador de especialista exclusivo. Monitor de Rede passa *hExpertKey* para o especialista ao chamar a função [Run](run.md) .

</dd> <dt>

*pOriginalMemory* \[ no\]
</dt> <dd>

Ponteiro para o endereço de memória do especialista alocado pelo [ExpertAllocMemory](expertallocmemory.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

A função retorna a quantidade de memória alocada em bytes.

## <a name="remarks"></a>Comentários

Para obter informações sobre o tipo de dados de **tamanho \_ T** que o **ExpertMemorySize** retorna, consulte tipos de dados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




