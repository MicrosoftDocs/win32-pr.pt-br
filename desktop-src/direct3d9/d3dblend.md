---
description: Define o modo de combinação com suporte.
ms.assetid: 60ff384c-15a0-4c6f-9e2c-59fdea76b7a1
title: Enumeração D3DBLEND (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DBLEND
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 55edb432913720f58860d4f5cb87d8da9b9a8681
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343381"
---
# <a name="d3dblend-enumeration"></a>Enumeração D3DBLEND

Define o modo de combinação com suporte.

## <a name="syntax"></a>Sintaxe


```C++
typedef enum D3DBLEND { 
  D3DBLEND_ZERO             = 1,
  D3DBLEND_ONE              = 2,
  D3DBLEND_SRCCOLOR         = 3,
  D3DBLEND_INVSRCCOLOR      = 4,
  D3DBLEND_SRCALPHA         = 5,
  D3DBLEND_INVSRCALPHA      = 6,
  D3DBLEND_DESTALPHA        = 7,
  D3DBLEND_INVDESTALPHA     = 8,
  D3DBLEND_DESTCOLOR        = 9,
  D3DBLEND_INVDESTCOLOR     = 10,
  D3DBLEND_SRCALPHASAT      = 11,
  D3DBLEND_BOTHSRCALPHA     = 12,
  D3DBLEND_BOTHINVSRCALPHA  = 13,
  D3DBLEND_BLENDFACTOR      = 14,
  D3DBLEND_INVBLENDFACTOR   = 15,
  D3DBLEND_SRCCOLOR2        = 16,
  D3DBLEND_INVSRCCOLOR2     = 17,
  D3DBLEND_FORCE_DWORD      = 0x7fffffff
} D3DBLEND, *LPD3DBLEND;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DBLEND_ZERO"></span><span id="d3dblend_zero"></span>**D3DBLEND \_ ZERO**
</dt> <dd>

O fator blend é (0, 0, 0, 0).

</dd> <dt>

<span id="D3DBLEND_ONE"></span><span id="d3dblend_one"></span>**D3DBLEND \_ ONE**
</dt> <dd>

O fator blend é (1, 1, 1, 1).

</dd> <dt>

<span id="D3DBLEND_SRCCOLOR"></span><span id="d3dblend_srccolor"></span>**D3DBLEND \_ SRCCOLOR**
</dt> <dd>

O fator blend é (Rs, Gs, Bs, As).

</dd> <dt>

<span id="D3DBLEND_INVSRCCOLOR"></span><span id="d3dblend_invsrccolor"></span>**D3DBLEND \_ INVSRCCOLOR**
</dt> <dd>

O fator blend é (1 - Rs, 1 - Gs, 1 - Bs, 1 - As).

</dd> <dt>

<span id="D3DBLEND_SRCALPHA"></span><span id="d3dblend_srcalpha"></span>**D3DBLEND \_ SRCALPHA**
</dt> <dd>

O fator blend é (As, As, As, As).

</dd> <dt>

<span id="D3DBLEND_INVSRCALPHA"></span><span id="d3dblend_invsrcalpha"></span>**D3DBLEND \_ INVSRCALPHA**
</dt> <dd>

O fator blend é ( 1 - As, 1 - As, 1 - As, 1 - As).

</dd> <dt>

<span id="D3DBLEND_DESTALPHA"></span><span id="d3dblend_destalpha"></span>**D3DBLEND \_ DESTALPHA**
</dt> <dd>

O fator blend é (A<sub>d</sub> A<sub>d</sub> A<sub>d</sub> A<sub>d</sub>).

</dd> <dt>

<span id="D3DBLEND_INVDESTALPHA"></span><span id="d3dblend_invdestalpha"></span>**D3DBLEND \_ INVDESTALPHA**
</dt> <dd>

O fator blend é (1 - A<sub>d</sub> 1 - A<sub>d</sub> 1 - A<sub>d</sub> 1 - A<sub>d</sub>).

</dd> <dt>

<span id="D3DBLEND_DESTCOLOR"></span><span id="d3dblend_destcolor"></span>**D3DBLEND \_ DESTCOLOR**
</dt> <dd>

O fator de mistura é (R<sub>d</sub>, G<sub>d</sub>, B<sub>d</sub>, A<sub>d</sub>).

</dd> <dt>

<span id="D3DBLEND_INVDESTCOLOR"></span><span id="d3dblend_invdestcolor"></span>**D3DBLEND \_ INVDESTCOLOR**
</dt> <dd>

O fator de mistura é (1-R<sub>d</sub>, 1-G<sub>d</sub>, 1-B<sub>d</sub>, 1-a<sub>d</sub>).

</dd> <dt>

<span id="D3DBLEND_SRCALPHASAT"></span><span id="d3dblend_srcalphasat"></span>**D3DBLEND \_ SRCALPHASAT**
</dt> <dd>

O fator de mistura é (f, f, f, 1); em que f = min (as, 1 a<sub>d</sub>).

</dd> <dt>

<span id="D3DBLEND_BOTHSRCALPHA"></span><span id="d3dblend_bothsrcalpha"></span>**D3DBLEND \_ BOTHSRCALPHA**
</dt> <dd>

**Obsoleto**. A partir do DirectX 6, você pode obter o mesmo efeito definindo os fatores de mesclagem de origem e de destino como D3DBLEND \_ SRCALPHA e D3DBLEND \_ INVSRCALPHA em chamadas separadas.

</dd> <dt>

<span id="D3DBLEND_BOTHINVSRCALPHA"></span><span id="d3dblend_bothinvsrcalpha"></span>**D3DBLEND \_ BOTHINVSRCALPHA**
</dt> <dd>

**Obsoleto**. O fator de mistura de origem é (1-como, 1-como, 1-como, 1-como) e o fator de mesclagem de destino é (como, como, como, como); a seleção de mesclagem de destino é substituída. Esse modo de mesclagem tem suporte apenas para o \_ estado de RENDERIZAÇÃO D3DRS SRCBLEND.

</dd> <dt>

<span id="D3DBLEND_BLENDFACTOR"></span><span id="d3dblend_blendfactor"></span>**D3DBLEND \_ BLENDFACTOR**
</dt> <dd>

Fator de mistura de cor constante usado pelo misturador de buffer de quadro. Esse modo de mesclagem só terá suporte se D3DPBLENDCAPS \_ BLENDFACTOR estiver definido nos membros **SrcBlendCaps** ou **DestBlendCaps** de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).

</dd> <dt>

<span id="D3DBLEND_INVBLENDFACTOR"></span><span id="d3dblend_invblendfactor"></span>**D3DBLEND \_ INVBLENDFACTOR**
</dt> <dd>

Fator de mistura de cor constante invertido usado pelo misturador de buffer de quadro. Esse modo de mesclagem só terá suporte se o \_ bit D3DPBLENDCAPS BLENDFACTOR for definido nos membros **SrcBlendCaps** ou **DestBlendCaps** de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).

</dd> <dt>

<span id="D3DBLEND_SRCCOLOR2"></span><span id="d3dblend_srccolor2"></span>**D3DBLEND \_ SRCCOLOR2**
</dt> <dd>

O fator blend é (PSOutColor \[ 1 \] <sub>r,</sub>PSOutColor \[ 1 \] <sub>g,</sub>PSOutColor \[ 1 \] <sub>b</sub>, não usado). Consulte [Renderizar mesclagem de destino.](#render-target-blending)

Diferenças entre o Direct3D 9 e o Direct3D 9Ex:

- Esse sinalizador está disponível apenas no Direct3D 9Ex.



 

</dd> <dt>

<span id="D3DBLEND_INVSRCCOLOR2"></span><span id="d3dblend_invsrccolor2"></span>**D3DBLEND \_ INVSRCCOLOR2**
</dt> <dd>

O fator blend é (1 - PSOutColor \[ 1 \] <sub>r</sub>, 1 - PSOutColor \[ 1 \] <sub>g</sub>, 1 - PSOutColor \[ 1 \] <sub>b</sub>, não usado)). Consulte [Renderizar mesclagem de destino.](#render-target-blending)


Diferenças entre o Direct3D 9 e o Direct3D 9Ex:

- Esse sinalizador está disponível apenas no Direct3D 9Ex.



 

</dd> <dt>

<span id="D3DBLEND_FORCE_DWORD"></span><span id="d3dblend_force_dword"></span>**D3DBLEND \_ FORCE \_ DWORD**
</dt> <dd>

Força essa enumeração a compilar para 32 bits de tamanho. Sem esse valor, alguns compiladores permitiriam que essa enumeração fosse compilada para um tamanho diferente de 32 bits. Este valor não é usado.

</dd> </dl>

## <a name="remarks"></a>Comentários

Nas descrições do membro anterior, os valores RGBA da origem e do destino são indicados pelos subscritos s e d.

Os valores nesse tipo enumerado são usados pelos seguintes estados de renderização:

-   D3DRS \_ DESTBLEND
-   D3DRS \_ SRCBLEND
-   D3DRS \_ DESTBLENDALPHA
-   D3DRS \_ SRCBLENDALPHA

Consulte [ **D3DRENDERSTATETYPE**](./d3drenderstatetype.md)

### <a name="render-target-blending"></a>Renderizar a mesclagem de destino

O Direct3D 9Ex aprimorou os recursos de renderização de texto. A renderização de fontes de tipo limpar normalmente exigiria duas passagens. Para eliminar a segunda passagem, um sombreador de pixel pode ser usado para produzir duas cores, que podemos chamar PSOutColor \[ 0 \] e PSOutColor \[ 1 \] . A primeira cor conterá os componentes padrão de 3 cores (RGB). A segunda cor conterá três componentes alfa (um para cada componente da primeira cor).

Esses novos modos de mesclagem são usados apenas para renderização de texto no primeiro destino de renderização.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Enumerações do Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 
