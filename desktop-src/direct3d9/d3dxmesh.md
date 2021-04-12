---
description: Sinalizadores usados para especificar as opções de criação para uma malha.
ms.assetid: c94e19ab-8024-4a28-9d1a-6d57707c3a52
title: Enumeração D3DXMESH (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMESH
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 602eb38f2113b54ee02477faf3bdd15a6a924abc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298486"
---
# <a name="d3dxmesh-enumeration"></a>Enumeração D3DXMESH

Sinalizadores usados para especificar as opções de criação para uma malha.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DXMESH { 
  D3DXMESH_32BIT                  = 0x001,
  D3DXMESH_DONOTCLIP              = 0x002,
  D3DXMESH_POINTS                 = 0x004,
  D3DXMESH_RTPATCHES              = 0x008,
  D3DXMESH_NPATCHES               = 0x4000,
  D3DXMESH_VB_SYSTEMMEM           = 0x010,
  D3DXMESH_VB_MANAGED             = 0x020,
  D3DXMESH_VB_WRITEONLY           = 0x040,
  D3DXMESH_VB_DYNAMIC             = 0x080,
  D3DXMESH_VB_SOFTWAREPROCESSING  = 0x8000,
  D3DXMESH_IB_SYSTEMMEM           = 0x100,
  D3DXMESH_IB_MANAGED             = 0x200,
  D3DXMESH_IB_WRITEONLY           = 0x400,
  D3DXMESH_IB_DYNAMIC             = 0x800,
  D3DXMESH_IB_SOFTWAREPROCESSING  = 0x10000,
  D3DXMESH_VB_SHARE               = 0x1000,
  D3DXMESH_USEHWONLY              = 0x2000,
  D3DXMESH_SYSTEMMEM              = 0x110,
  D3DXMESH_MANAGED                = 0x220,
  D3DXMESH_WRITEONLY              = 0x440,
  D3DXMESH_DYNAMIC                = 0x880,
  D3DXMESH_SOFTWAREPROCESSING     = 0x18000
} D3DXMESH, *LPD3DXMESH;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DXMESH_32BIT"></span><span id="d3dxmesh_32bit"></span>**D3DXMESH \_ 32 bits**
</dt> <dd>

A malha tem índices de 32 bits em vez de índices de 16 bits. Consulte Observações.

</dd> <dt>

<span id="D3DXMESH_DONOTCLIP"></span><span id="d3dxmesh_donotclip"></span>**D3DXMESH \_ DONOTCLIP**
</dt> <dd>

Use o sinalizador de uso [**D3DUSAGE \_ DONOTCLIP**](d3dusage.md) para os buffers de vértice e de índice.

</dd> <dt>

<span id="D3DXMESH_POINTS"></span><span id="d3dxmesh_points"></span>**Pontos de D3DXMESH \_**
</dt> <dd>

Use o sinalizador de uso de [**\_ pontos D3DUSAGE**](d3dusage.md) para os buffers de vértice e de índice.

</dd> <dt>

<span id="D3DXMESH_RTPATCHES"></span><span id="d3dxmesh_rtpatches"></span>**D3DXMESH \_ RTPATCHES**
</dt> <dd>

Use o sinalizador de uso [**D3DUSAGE \_ RTPATCHES**](d3dusage.md) para os buffers de vértice e de índice.

</dd> <dt>

<span id="D3DXMESH_NPATCHES"></span><span id="d3dxmesh_npatches"></span>**D3DXMESH \_ NPATCHES**
</dt> <dd>

A especificação desse sinalizador faz com que o vértice e o buffer do índice da malha sejam criados com o sinalizador [**D3DUSAGE \_ NPATCHES**](d3dusage.md) . Isso será necessário se o objeto de malha for renderizado usando o aprimoramento de N-patch usando o Direct3D.

</dd> <dt>

<span id="D3DXMESH_VB_SYSTEMMEM"></span><span id="d3dxmesh_vb_systemmem"></span>**D3DXMESH \_ VB \_ SYSTEMMEM**
</dt> <dd>

Use o sinalizador de uso [**D3DPOOL \_ SYSTEMMEM**](./d3dpool.md) para os buffers de vértice.

</dd> <dt>

<span id="D3DXMESH_VB_MANAGED"></span><span id="d3dxmesh_vb_managed"></span>**Gerenciado por D3DXMESH \_ VB \_**
</dt> <dd>

Use o sinalizador de uso [**\_ gerenciado D3DPOOL**](./d3dpool.md) para buffers de vértice.

</dd> <dt>

<span id="D3DXMESH_VB_WRITEONLY"></span><span id="d3dxmesh_vb_writeonly"></span>**D3DXMESH \_ VB \_ WRITEONLY**
</dt> <dd>

Use o sinalizador de uso de [**\_ WRITEONLY D3DUSAGE**](d3dusage.md) para buffers de vértice.

</dd> <dt>

<span id="D3DXMESH_VB_DYNAMIC"></span><span id="d3dxmesh_vb_dynamic"></span>**D3DXMESH \_ VB \_ Dynamic**
</dt> <dd>

Use o sinalizador de uso [**\_ dinâmico D3DUSAGE**](d3dusage.md) para buffers de vértice.

</dd> <dt>

<span id="D3DXMESH_VB_SOFTWAREPROCESSING"></span><span id="d3dxmesh_vb_softwareprocessing"></span>**D3DXMESH \_ VB \_ SOFTWAREPROCESSING**
</dt> <dd>

Use o sinalizador de uso [**D3DUSAGE \_ SOFTWAREPROCESSING**](d3dusage.md) para os buffers de vértice.

</dd> <dt>

<span id="D3DXMESH_IB_SYSTEMMEM"></span><span id="d3dxmesh_ib_systemmem"></span>**D3DXMESH \_ IB \_ SYSTEMMEM**
</dt> <dd>

Use o sinalizador de uso [**D3DPOOL \_ SYSTEMMEM**](./d3dpool.md) para buffers de índice.

</dd> <dt>

<span id="D3DXMESH_IB_MANAGED"></span><span id="d3dxmesh_ib_managed"></span>**D3DXMESH \_ IB \_ gerenciado**
</dt> <dd>

Use o sinalizador de uso [**\_ gerenciado D3DPOOL**](./d3dpool.md) para buffers de índice.

</dd> <dt>

<span id="D3DXMESH_IB_WRITEONLY"></span><span id="d3dxmesh_ib_writeonly"></span>**D3DXMESH \_ IB \_ WRITEONLY**
</dt> <dd>

Use o sinalizador de uso de [**\_ WRITEONLY D3DUSAGE**](d3dusage.md) para buffers de índice.

</dd> <dt>

<span id="D3DXMESH_IB_DYNAMIC"></span><span id="d3dxmesh_ib_dynamic"></span>**D3DXMESH \_ IB \_ Dynamic**
</dt> <dd>

Use o sinalizador de uso [**\_ dinâmico D3DUSAGE**](d3dusage.md) para buffers de índice.

</dd> <dt>

<span id="D3DXMESH_IB_SOFTWAREPROCESSING"></span><span id="d3dxmesh_ib_softwareprocessing"></span>**D3DXMESH \_ IB \_ SOFTWAREPROCESSING**
</dt> <dd>

Use o sinalizador de uso [**D3DUSAGE \_ SOFTWAREPROCESSING**](d3dusage.md) para buffers de índice.

</dd> <dt>

<span id="D3DXMESH_VB_SHARE"></span><span id="d3dxmesh_vb_share"></span>**\_Compartilhamento D3DXMESH VB \_**
</dt> <dd>

Força as malhas clonadas a compartilhar buffers de vértice.

</dd> <dt>

<span id="D3DXMESH_USEHWONLY"></span><span id="d3dxmesh_usehwonly"></span>**D3DXMESH \_ USEHWONLY**
</dt> <dd>

Use somente o processamento de hardware. Para o dispositivo de modo misto, esse sinalizador fará com que o sistema Use hardware (se houver suporte no hardware) ou usará como padrão o processamento de software.

</dd> <dt>

<span id="D3DXMESH_SYSTEMMEM"></span><span id="d3dxmesh_systemmem"></span>**D3DXMESH \_ SYSTEMMEM**
</dt> <dd>

Equivalente a especificar D3DXMESH \_ VB \_ SYSTEMMEM e D3DXMESH \_ IB \_ SYSTEMMEM.

</dd> <dt>

<span id="D3DXMESH_MANAGED"></span><span id="d3dxmesh_managed"></span>**\_Gerenciado D3DXMESH**
</dt> <dd>

Equivalente a especificar o D3DXMESH \_ VB \_ gerenciado e o D3DXMESH \_ IB \_ gerenciados.

</dd> <dt>

<span id="D3DXMESH_WRITEONLY"></span><span id="d3dxmesh_writeonly"></span>**\_WRITEONLY D3DXMESH**
</dt> <dd>

Equivalente a especificar ambos D3DXMESH \_ VB \_ WRITEONLY e D3DXMESH \_ IB \_ WriteOnly.

</dd> <dt>

<span id="D3DXMESH_DYNAMIC"></span><span id="d3dxmesh_dynamic"></span>**D3DXMESH \_ dinâmico**
</dt> <dd>

Equivalente a especificar o D3DXMESH \_ VB \_ Dynamic e D3DXMESH \_ IB \_ Dynamic.

</dd> <dt>

<span id="D3DXMESH_SOFTWAREPROCESSING"></span><span id="d3dxmesh_softwareprocessing"></span>**D3DXMESH \_ SOFTWAREPROCESSING**
</dt> <dd>

Equivalente a especificar D3DXMESH \_ VB \_ SOFTWAREPROCESSING e D3DXMESH \_ IB \_ SOFTWAREPROCESSING.

</dd> </dl>

## <a name="remarks"></a>Comentários

Uma malha de 32 bits (D3DXMESH \_ 32bit) pode teoricamente dar suporte a (2 ^ 32)-1 rostos e vértices. No entanto, a alocação de memória para uma malha grande em um sistema operacional de 32 bits não é prática.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Enumerações D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 
