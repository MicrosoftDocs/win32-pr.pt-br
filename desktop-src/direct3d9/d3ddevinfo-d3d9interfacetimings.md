---
description: Porcentagem de tempo de processamento de dados no driver. Essas estatísticas podem ajudar a identificar casos em que o driver está aguardando outros recursos.
ms.assetid: 2c613349-61eb-44aa-aa7b-3161dd1fc95e
title: Estrutura de D3DDEVINFO_D3D9INTERFACETIMINGS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_D3D9INTERFACETIMINGS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: dfd6303f3682e29090db41fa83b38fc67f99121e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105751108"
---
# <a name="d3ddevinfo_d3d9interfacetimings-structure"></a>\_Estrutura D3DDEVINFO D3D9INTERFACETIMINGS

Porcentagem de tempo de processamento de dados no driver. Essas estatísticas podem ajudar a identificar casos em que o driver está aguardando outros recursos.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct D3DDEVINFO_D3D9INTERFACETIMINGS {
  FLOAT WaitingForGPUToUseApplicationResourceTimePercent;
  FLOAT WaitingForGPUToAcceptMoreCommandsTimePercent;
  FLOAT WaitingForGPUToStayWithinLatencyTimePercent;
  FLOAT WaitingForGPUExclusiveResourceTimePercent;
  FLOAT WaitingForGPUOtherTimePercent;
} D3DDEVINFO_D3D9INTERFACETIMINGS, *LPD3DDEVINFO_D3D9INTERFACETIMINGS;
```



## <a name="members"></a>Membros

<dl> <dt>

**WaitingForGPUToUseApplicationResourceTimePercent**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Porcentagem de tempo que o driver gastou aguardando a GPU terminar usando um recurso bloqueado (e [D3DLOCK \_ DONOTWAIT](d3dlock.md) não foi especificado).

</dd> <dt>

**WaitingForGPUToAcceptMoreCommandsTimePercent**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Porcentagem de tempo que o driver gastou aguardando a GPU concluir o processamento de alguns comandos antes que o driver pudesse enviar mais. Isso indica que o driver ficou sem espaço para enviar comandos para a GPU.

</dd> <dt>

**WaitingForGPUToStayWithinLatencyTimePercent**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Porcentagem de tempo que o driver gastou aguardando a latência da GPU reduzir para menos de três quadros de renderização.

Se um aplicativo for limitado à GPU, o driver deverá paralisar a CPU até que a GPU fique dentro de três quadros. Isso impede que um aplicativo enfileirar muitos segundos de processamento de chamadas, o que pode aumentar consideravelmente a latência entre quando o usuário insere novos dados e quando o usuário vê os resultados dessa entrada. Em geral, o driver pode acompanhar o número de vezes que o [**presente**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) é chamado para impedir o enfileiramento de mais de três quadros de trabalho de renderização.

</dd> <dt>

**WaitingForGPUExclusiveResourceTimePercent**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Porcentagem de tempo que o driver gastou aguardando um recurso que não pode ser canalizado (que é operado em paralelo). Um aplicativo pode querer evitar o uso de um recurso não-pipeline por motivos de desempenho.

</dd> <dt>

**WaitingForGPUOtherTimePercent**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Porcentagem de tempo que o driver gastou esperando por outro processamento de GPU.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essas métricas ajudam a identificar quando um driver está aguardando e o que está aguardando. Porcentagens altas não são necessariamente um problema.

Essas métricas globais do sistema podem ou não ser implementadas. Dependendo do hardware específico, essas métricas podem não dar suporte a várias consultas simultaneamente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas do Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)
</dt> </dl>

 

 
