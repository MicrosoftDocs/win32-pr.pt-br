---
description: Define um conjunto de propriedades de iluminação.
ms.assetid: 25ce9d72-949c-41fc-8e3b-146d6a2de0dc
title: Estrutura D3DLIGHT9 (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DLIGHT9
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 3e38cd5b6cfaba4822ddecf121aa2b03c86e2a3a899e464df18bfa473322f41f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118804833"
---
# <a name="d3dlight9-structure"></a>Estrutura D3DLIGHT9

Define um conjunto de propriedades de iluminação.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct D3DLIGHT9 {
  D3DLIGHTTYPE  Type;
  D3DCOLORVALUE Diffuse;
  D3DCOLORVALUE Specular;
  D3DCOLORVALUE Ambient;
  D3DVECTOR     Position;
  D3DVECTOR     Direction;
  float         Range;
  float         Falloff;
  float         Attenuation0;
  float         Attenuation1;
  float         Attenuation2;
  float         Theta;
  float         Phi;
} D3DLIGHT9, *LPD3DLIGHT;
```



## <a name="members"></a>Membros

<dl> <dt>

**Tipo**
</dt> <dd>

Tipo: **[ **D3DLIGHTTYPE**](./d3dlighttype.md)**

</dd> <dd>

Tipo da fonte de luz. Esse valor é um dos membros do tipo enumerado [**D3DLIGHTTYPE**](./d3dlighttype.md) .

</dd> <dt>

**Difusa**
</dt> <dd>

Tipo: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

Cor difusa emitida pela luz. Esse membro é uma estrutura [**D3DCOLORVALUE**](d3dcolorvalue.md) .

</dd> <dt>

**Especular**
</dt> <dd>

Tipo: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

Cor especulada emitida pela luz. Esse membro é uma estrutura [**D3DCOLORVALUE**](d3dcolorvalue.md) .

</dd> <dt>

**Ambiente**
</dt> <dd>

Tipo: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

Cor de ambiente emitida pela luz. Esse membro é uma estrutura [**D3DCOLORVALUE**](d3dcolorvalue.md) .

</dd> <dt>

**Posição**
</dt> <dd>

Tipo: **[ **D3DVECTOR**](d3dvector.md)**

</dd> <dd>

Posição da luz no espaço do mundo, especificada por uma estrutura [**D3DVECTOR**](d3dvector.md) . Esse membro não tem significado para luzes direcionais e é ignorado nesse caso.

</dd> <dt>

**Direção**
</dt> <dd>

Tipo: **[ **D3DVECTOR**](d3dvector.md)**

</dd> <dd>

Direção em que a luz está apontando no espaço do mundo, especificada por uma estrutura [**D3DVECTOR**](d3dvector.md) . Esse membro tem significado apenas para rotas direcionais e Spotlights. Este vetor não precisa ser normalizado, mas deve ter um comprimento diferente de zero.

</dd> <dt>

**Intervalo**
</dt> <dd>

Tipo: **float**

</dd> <dd>

Distância além da qual a luz não tem efeito. O valor máximo permitido para esse membro é a raiz quadrada de FLT \_ Max. Esse membro não afeta as luzes direcionais.

</dd> <dt>

**Queda**
</dt> <dd>

Tipo: **float**

</dd> <dd>

Diminuir a iluminação entre o cone interno de um Spotlight (o ângulo especificado por teta) e a borda externa do cone externo (o ângulo especificado por Phi).

O efeito de queda na iluminação é sutil. Além disso, uma pequena penalidade de desempenho é incorrida com a formação da curva de queda. Por esses motivos, a maioria dos desenvolvedores define esse valor como 1,0.

</dd> <dt>

**Attenuation0**
</dt> <dd>

Tipo: **float**

</dd> <dd>

Valor que especifica como a intensidade de luz é alterada à distância. Os valores de atenuação são ignorados para luzes direcionais. Esse membro representa uma constante de atenuação. Para obter informações sobre atenuação, consulte [Propriedades claras (Direct3D 9)](light-properties.md). Os valores válidos para esse membro variam de 0,0 a infinito. Para luzes não-direcionais, os três valores de atenuação não devem ser definidos como 0,0 ao mesmo tempo.

</dd> <dt>

**Attenuation1**
</dt> <dd>

Tipo: **float**

</dd> <dd>

Valor que especifica como a intensidade de luz é alterada à distância. Os valores de atenuação são ignorados para luzes direcionais. Esse membro representa uma constante de atenuação. Para obter informações sobre atenuação, consulte [Propriedades claras (Direct3D 9)](light-properties.md). Os valores válidos para esse membro variam de 0,0 a infinito. Para luzes não-direcionais, os três valores de atenuação não devem ser definidos como 0,0 ao mesmo tempo.

</dd> <dt>

**Attenuation2**
</dt> <dd>

Tipo: **float**

</dd> <dd>

Valor que especifica como a intensidade de luz é alterada à distância. Os valores de atenuação são ignorados para luzes direcionais. Esse membro representa uma constante de atenuação. Para obter informações sobre atenuação, consulte [Propriedades claras (Direct3D 9)](light-properties.md). Os valores válidos para esse membro variam de 0,0 a infinito. Para luzes não-direcionais, os três valores de atenuação não devem ser definidos como 0,0 ao mesmo tempo.

</dd> <dt>

**Teta**
</dt> <dd>

Tipo: **float**

</dd> <dd>

Ângulo, em radianos, do cone interno de um Spotlight-ou seja, o cone de destaque totalmente iluminado. Esse valor deve estar no intervalo de 0 até o valor especificado por Phi.

</dd> <dt>

**PI**
</dt> <dd>

Tipo: **float**

</dd> <dd>

Ângulo, em radianos, definindo a borda externa do cone externo do Spotlight. Pontos fora deste cone não estão acesos pelo Spotlight. Esse valor deve estar entre 0 e PI.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas do Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**Getleve**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getlight)
</dt> <dt>

[**SetLight**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight)
</dt> </dl>

 

 
