---
description: A função ExpertMemorySize retorna a quantidade de memória alocada pela função ExpertAllocMemory.
ms.assetid: 60d3f33d-dc03-4c39-98fa-ec093398b51b
title: Função ExpertMemorySize (Netmon.h)
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
ms.openlocfilehash: 69dae4ca2a7f7a9e3b2f77047475c5dd35f54a3394b4481c2f452a46e983c35e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119744266"
---
# <a name="expertmemorysize-function"></a>Função ExpertMemorySize

A **função ExpertMemorySize** retorna a quantidade de memória alocada pela [função ExpertAllocMemory.](expertallocmemory.md)

## <a name="syntax"></a>Sintaxe


```C++
SIZE_T WINAPI ExpertMemorySize(
  _In_ HEXPERTKEY hExpertKey,
  _In_ LPVOID     pOriginalMemory
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hExpertKey* \[ Em\]
</dt> <dd>

Identificador de especialista exclusivo. Monitor de Rede passa *hExpertKey* para o especialista quando ele chama a [função](run.md) Executar.

</dd> <dt>

*pOriginalMemory* \[ Em\]
</dt> <dd>

Ponteiro para o endereço de memória do especialista alocado por [ExpertAllocMemory.](expertallocmemory.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

A função retorna a quantidade de memória alocada em bytes.

## <a name="remarks"></a>Comentários

Para obter informações sobre o **tipo de dados SIZE \_ T** que **o ExpertMemorySize** retorna, consulte Tipos de dados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




