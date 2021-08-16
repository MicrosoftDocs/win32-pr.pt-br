---
description: Enumeração D3DXMESH – sinalizadores usados para especificar opções de criação para uma malha.
ms.assetid: c94e19ab-8024-4a28-9d1a-6d57707c3a52
title: Enumeração D3DXMESH (D3dx9mesh.h)
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
ms.openlocfilehash: 6b83389ae4d92027245877e24e01621f0d93f123dee9ff4f040586b3e7c5111d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118525263"
---
# <a name="d3dxmesh-enumeration"></a>Enumeração D3DXMESH

Sinalizadores usados para especificar opções de criação para uma malha.

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

<span id="D3DXMESH_32BIT"></span><span id="d3dxmesh_32bit"></span>**D3DXMESH \_ 32BIT**
</dt> <dd>

A malha tem índices de 32 bits em vez de índices de 16 bits. Consulte Observações.

</dd> <dt>

<span id="D3DXMESH_DONOTCLIP"></span><span id="d3dxmesh_donotclip"></span>**D3DXMESH \_ DONOTCLIP**
</dt> <dd>

Use o [**sinalizador de uso D3DUSAGE \_ DONOTCLIP**](d3dusage.md) para buffers de vértice e índice.

</dd> <dt>

<span id="D3DXMESH_POINTS"></span><span id="d3dxmesh_points"></span>**PONTOS D3DXMESH \_**
</dt> <dd>

Use o [**sinalizador de uso D3DUSAGE \_ POINTS**](d3dusage.md) para buffers de vértice e índice.

</dd> <dt>

<span id="D3DXMESH_RTPATCHES"></span><span id="d3dxmesh_rtpatches"></span>**D3DXMESH \_ RTPATCHES**
</dt> <dd>

Use o [**sinalizador de uso D3DUSAGE \_ RTPATCHES**](d3dusage.md) para buffers de vértice e índice.

</dd> <dt>

<span id="D3DXMESH_NPATCHES"></span><span id="d3dxmesh_npatches"></span>**D3DXMESH \_ NPATCHES**
</dt> <dd>

Especificar esse sinalizador faz com que o vértice e o buffer de índice da malha sejam criados com o sinalizador [**D3DUSAGE \_ NPATCHES.**](d3dusage.md) Isso será necessário se o objeto de malha for renderizado usando o aprimoramento de N patch usando o Direct3D.

</dd> <dt>

<span id="D3DXMESH_VB_SYSTEMMEM"></span><span id="d3dxmesh_vb_systemmem"></span>**D3DXMESH \_ VB \_ SYSTEMMEM**
</dt> <dd>

Use o [**sinalizador de uso D3DPOOL \_ SYSTEMMEM**](./d3dpool.md) para buffers de vértice.

</dd> <dt>

<span id="D3DXMESH_VB_MANAGED"></span><span id="d3dxmesh_vb_managed"></span>**D3DXMESH \_ VB \_ GERENCIADO**
</dt> <dd>

Use o sinalizador [**de uso GERENCIADO de D3DPOOL \_**](./d3dpool.md) para buffers de vértice.

</dd> <dt>

<span id="D3DXMESH_VB_WRITEONLY"></span><span id="d3dxmesh_vb_writeonly"></span>**D3DXMESH \_ VB \_ WRITEONLY**
</dt> <dd>

Use o [**sinalizador de uso \_ WRITEONLY D3DUSAGE**](d3dusage.md) para buffers de vértice.

</dd> <dt>

<span id="D3DXMESH_VB_DYNAMIC"></span><span id="d3dxmesh_vb_dynamic"></span>**D3DXMESH \_ VB \_ DYNAMIC**
</dt> <dd>

Use o [**sinalizador de \_ uso DINÂMICO D3DUSAGE**](d3dusage.md) para buffers de vértice.

</dd> <dt>

<span id="D3DXMESH_VB_SOFTWAREPROCESSING"></span><span id="d3dxmesh_vb_softwareprocessing"></span>**D3DXMESH \_ VB \_ SOFTWAREPROCESSING**
</dt> <dd>

Use o [**sinalizador de uso D3DUSAGE \_ SOFTWAREPROCESSING**](d3dusage.md) para buffers de vértice.

</dd> <dt>

<span id="D3DXMESH_IB_SYSTEMMEM"></span><span id="d3dxmesh_ib_systemmem"></span>**D3DXMESH \_ IB \_ SYSTEMMEM**
</dt> <dd>

Use o [**sinalizador de uso D3DPOOL \_ SYSTEMMEM**](./d3dpool.md) para buffers de índice.

</dd> <dt>

<span id="D3DXMESH_IB_MANAGED"></span><span id="d3dxmesh_ib_managed"></span>**D3DXMESH \_ IB \_ GERENCIADO**
</dt> <dd>

Use o sinalizador [**de uso gerenciado D3DPOOL \_**](./d3dpool.md) para buffers de índice.

</dd> <dt>

<span id="D3DXMESH_IB_WRITEONLY"></span><span id="d3dxmesh_ib_writeonly"></span>**D3DXMESH \_ IB \_ WRITEONLY**
</dt> <dd>

Use o [**sinalizador de uso \_ WRITEONLY D3DUSAGE**](d3dusage.md) para buffers de índice.

</dd> <dt>

<span id="D3DXMESH_IB_DYNAMIC"></span><span id="d3dxmesh_ib_dynamic"></span>**D3DXMESH \_ IB \_ DYNAMIC**
</dt> <dd>

Use o [**sinalizador de \_ uso DINÂMICO D3DUSAGE**](d3dusage.md) para buffers de índice.

</dd> <dt>

<span id="D3DXMESH_IB_SOFTWAREPROCESSING"></span><span id="d3dxmesh_ib_softwareprocessing"></span>**D3DXMESH \_ IB \_ SOFTWAREPROCESSING**
</dt> <dd>

Use o [**sinalizador de uso D3DUSAGE \_ SOFTWAREPROCESSING**](d3dusage.md) para buffers de índice.

</dd> <dt>

<span id="D3DXMESH_VB_SHARE"></span><span id="d3dxmesh_vb_share"></span>**D3DXMESH \_ VB \_ SHARE**
</dt> <dd>

Força as malhas clonadas a compartilhar buffers de vértice.

</dd> <dt>

<span id="D3DXMESH_USEHWONLY"></span><span id="d3dxmesh_usehwonly"></span>**D3DXMESH \_ USEHWONLY**
</dt> <dd>

Use somente processamento de hardware. Para dispositivos de modo misto, esse sinalizador fará com que o sistema use hardware (se tiver suporte em hardware) ou usará como padrão o processamento de software.

</dd> <dt>

<span id="D3DXMESH_SYSTEMMEM"></span><span id="d3dxmesh_systemmem"></span>**D3DXMESH \_ SYSTEMMEM**
</dt> <dd>

Equivalente a especificar SYSTEMMEM de VB do D3DXMESH e \_ \_ \_ SYSTEMMEM do IB do D3DXMESH. \_

</dd> <dt>

<span id="D3DXMESH_MANAGED"></span><span id="d3dxmesh_managed"></span>**D3DXMESH \_ GERENCIADO**
</dt> <dd>

Equivalente a especificar ODXMESH \_ VB MANAGED e \_ D3DXMESH \_ IB \_ MANAGED.

</dd> <dt>

<span id="D3DXMESH_WRITEONLY"></span><span id="d3dxmesh_writeonly"></span>**D3DXMESH \_ WRITEONLY**
</dt> <dd>

Equivalente a especificar WRITEONLY de VB D3DXMESH e \_ \_ D3DXMESH \_ IB \_ WRITEONLY.

</dd> <dt>

<span id="D3DXMESH_DYNAMIC"></span><span id="d3dxmesh_dynamic"></span>**D3DXMESH \_ DYNAMIC**
</dt> <dd>

Equivalente a especificar d3DXMESH \_ VB \_ DYNAMIC e D3DXMESH \_ IB \_ DYNAMIC.

</dd> <dt>

<span id="D3DXMESH_SOFTWAREPROCESSING"></span><span id="d3dxmesh_softwareprocessing"></span>**D3DXMESH \_ SOFTWAREPROCESSING**
</dt> <dd>

Equivalente a especificar software \_ VB D3DXMESHPROCESSING e \_ D3DXMESH \_ IB \_ SOFTWAREPROCESSING.

</dd> </dl>

## <a name="remarks"></a>Comentários

Uma malha de 32 bits (D3DXMESH 32BIT) pode, teoricamente, dar suporte \_ a (2^32)-1 faces e vértices. No entanto, alocar memória para uma malha grande em um sistema operacional de 32 bits não é prático.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx9mesh.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Enumerações D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 
