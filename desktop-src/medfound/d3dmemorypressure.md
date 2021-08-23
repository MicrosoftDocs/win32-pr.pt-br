---
description: Essa estrutura contém dados para relatórios de pressão de memória.
ms.assetid: 42cf0922-53cc-48b9-8359-b88583ef5f1c
title: Estrutura D3DMEMORYPRESSURE (D3d9types.h) para Microsoft Media Foundation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DMEMORYPRESSURE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: ec6fdf0d27edb5e1cafa575664b07dfe0807c8d124e1b066161734e75247709f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119449416"
---
# <a name="d3dmemorypressure-structure-d3d9typesh-for-microsoft-media-foundation"></a>Estrutura D3DMEMORYPRESSURE (D3d9types.h) para Microsoft Media Foundation

Contém dados para relatórios de pressão de memória.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _D3DMEMORYPRESSURE {
  UINT64 BytesEvictedFromProcess;
  UINT64 SizeOfInefficientAllocation;
  DWORD  LevelOfEfficiency;
} D3DMEMORYPRESSURE;
```



## <a name="members"></a>Membros

<dl> <dt>

**BytesEvictedFromProcess**
</dt> <dd>

O número de bytes que foram despejados pelo processo durante a duração da consulta.

</dd> <dt>

**SizeOfInefficientAllocation**
</dt> <dd>

O número total de bytes colocados em segmentos de memória não adequados, devido ao espaço inadequado dentro dos segmentos de memória preferenciais.

</dd> <dt>

**LevelOfEfficiency**
</dt> <dd>

A eficiência geral das alocações de memória que foram colocadas na memória não ideal. O valor é expresso como um percentual. Por exemplo, o valor 95 indica que as alocações colocadas em segmentos de memória não preteridos são 95% eficientes. Esse número não deve ser considerado uma medida exata.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte | Windows 7 \[ aplicativos da área de trabalho\]                                                              |
| Servidor mínimo com suporte | Windows Somente aplicativos da área de trabalho do Server 2008 R2 \[\]                                                 |
| Cabeçalho                  | D3d9types.h (inclua D3d9.h) |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas de vídeo do Direct3D](direct3d-video-structures.md)
</dt> <dt>

[Relatório de pressão de memória](memory-pressure-reporting.md)
</dt> </dl>

 

 




