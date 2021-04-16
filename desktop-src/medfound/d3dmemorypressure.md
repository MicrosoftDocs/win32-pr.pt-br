---
description: Esta estrutura contém dados para relatórios de pressão de memória.
ms.assetid: 42cf0922-53cc-48b9-8359-b88583ef5f1c
title: Estrutura D3DMEMORYPRESSURE (D3d9types. h) para Microsoft Media Foundation
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
ms.openlocfilehash: 7400c4822b61a84ab288f0424cfa84e825e69dc9
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/02/2021
ms.locfileid: "106188027"
---
# <a name="d3dmemorypressure-structure-d3d9typesh-for-microsoft-media-foundation"></a>Estrutura D3DMEMORYPRESSURE (D3d9types. h) para Microsoft Media Foundation

Contém dados para o relatório de pressão de memória.

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

O número de bytes que foram removidos pelo processo durante a duração da consulta.

</dd> <dt>

**SizeOfInefficientAllocation**
</dt> <dd>

O número total de bytes colocados em segmentos de memória não ideais, devido a espaço inadequado dentro dos segmentos de memória preferenciais.

</dd> <dt>

**LevelOfEfficiency**
</dt> <dd>

A eficiência geral das alocações de memória que foram colocadas na memória não ideal. O valor é expresso como uma porcentagem. Por exemplo, o valor 95 indica que as alocações colocadas em segmentos de memória não preferenciais são 95% eficiente. Esse número não deve ser considerado uma medida exata.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte | \[Somente aplicativos de área de trabalho do Windows 7\]                                                              |
| Servidor mínimo com suporte | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]                                                 |
| parâmetro                  | D3d9types. h (incluir D3d9. h) |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas de vídeo do Direct3D](direct3d-video-structures.md)
</dt> <dt>

[Relatório de pressão de memória](memory-pressure-reporting.md)
</dt> </dl>

 

 




