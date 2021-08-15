---
description: Define as dimensões da janela de uma superfície de destino de renderização na qual um volume 3D projeta.
ms.assetid: fb2c6048-f837-497d-8e4f-e18942d37899
title: Estrutura D3DVIEWPORT9 (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DVIEWPORT9
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 40162e4350e5a68670023701f1cdae973fb8a7bac3a6d4f5c301136c4e8c2702
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118527262"
---
# <a name="d3dviewport9-structure"></a>Estrutura D3DVIEWPORT9

Define as dimensões da janela de uma superfície de destino de renderização na qual um volume 3D projeta.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct D3DVIEWPORT9 {
  DWORD X;
  DWORD Y;
  DWORD Width;
  DWORD Height;
  float MinZ;
  float MaxZ;
} D3DVIEWPORT9, *LPD3DVIEWPORT9;
```



## <a name="members"></a>Membros

<dl> <dt>

**X**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Coordenada de pixel do canto superior esquerdo do viewport na superfície de destino de renderização. A menos que você queira renderizar para um subconjunto da superfície, esse membro pode ser definido como 0.

</dd> <dt>

**S**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Coordenada de pixel do canto superior esquerdo do viewport na superfície de destino de renderização. A menos que você queira renderizar para um subconjunto da superfície, esse membro pode ser definido como 0.

</dd> <dt>

**Largura**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Dimensão de largura do volume do clipe, em pixels. A menos que você esteja renderizar apenas para um subconjunto da superfície, esse membro deve ser definido como a dimensão de largura da superfície de destino de renderização.

</dd> <dt>

**Altura**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Dimensão de altura do volume do clipe, em pixels. A menos que você esteja renderizar apenas para um subconjunto da superfície, esse membro deve ser definido como a dimensão de altura da superfície de destino de renderização.

</dd> <dt>

**Minz**
</dt> <dd>

Tipo: **float**

</dd> <dd>

Junto com MaxZ, valor que descreve o intervalo de valores de profundidade no qual uma cena deve ser renderizada, os valores mínimo e máximo do volume de clipe. A maioria dos aplicativos configura esse valor como 0,0. O recorte é executado após a aplicação da matriz de projeção.

</dd> <dt>

**MaxZ**
</dt> <dd>

Tipo: **float**

</dd> <dd>

Junto com MinZ, valor que descreve o intervalo de valores de profundidade no qual uma cena deve ser renderizada, os valores mínimo e máximo do volume de clipe. A maioria dos aplicativos configura esse valor como 1,0. O recorte é executado após a aplicação da matriz de projeção.

</dd> </dl>

## <a name="remarks"></a>Comentários

Os membros X, Y, Largura e Altura descrevem a posição e as dimensões do viewport na superfície de destino de renderização. Normalmente, os aplicativos são renderizar para toda a superfície de destino; Ao renderizar em uma superfície 640 x 480, esses membros devem ser 0, 0, 640 e 480, respectivamente. O MinZ e o MaxZ normalmente são definidos como 0,0 e 1,0, mas podem ser definidos como outros valores para obter efeitos específicos. Por exemplo, você pode defini-los como 0,0 para forçar o sistema a renderizar objetos em primeiro plano de uma cena ou ambos como 1,0 para forçar os objetos para a segundo plano.

Quando os parâmetros do viewport para um dispositivo mudam (devido a uma chamada para o método [**SetViewport),**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setviewport) o driver cria uma nova matriz de transformação.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetViewport**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getviewport)
</dt> <dt>

[**SetViewport**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setviewport)
</dt> </dl>

 

 
