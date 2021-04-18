---
description: Configura pontos de controle para a interpolação de Quadrangle esférica.
ms.assetid: c66227bd-8cc1-4173-9dc2-5aab9d57301e
title: Função D3DXQuaternionSquadSetup (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionSquadSetup
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4a0683bce3642b0300e68be348d8aed39b3c333d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105764453"
---
# <a name="d3dxquaternionsquadsetup-function-d3dx10mathh"></a>Função D3DXQuaternionSquadSetup (D3DX10Math. h)

Configura pontos de controle para a interpolação de Quadrangle esférica.

## <a name="syntax"></a>Sintaxe


```C++
void D3DXQuaternionSquadSetup(
  _In_       D3DXQUATERNION *pAOut,
  _In_       D3DXQUATERNION *pBOut,
  _In_       D3DXQUATERNION *pCOut,
  _In_ const D3DXQUATERNION *pQ0,
  _In_ const D3DXQUATERNION *pQ1,
  _In_ const D3DXQUATERNION *pQ2,
  _In_ const D3DXQUATERNION *pQ3
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pAOut* \[ no\]
</dt> <dd>

Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***

Ponteiro para AOut.

</dd> <dt>

*pBOut* \[ no\]
</dt> <dd>

Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***

Ponteiro para obre.

</dd> <dt>

*pCOut* \[ no\]
</dt> <dd>

Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***

Ponteiro para COut.

</dd> <dt>

*pQ0* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

Ponteiro para o ponto de controle de entrada, Q0.

</dd> <dt>

*pQ1* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

Ponteiro para o ponto de controle de entrada, Q1.

</dd> <dt>

*pQ2* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

Ponteiro para o ponto de controle de entrada, Q2.

</dd> <dt>

*pQ3* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

Ponteiro para o ponto de controle de entrada, Q3.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Nenhum.

## <a name="remarks"></a>Comentários

Essa função usa quatro pontos de controle, que são fornecidos para as entradas pQ0, pQ1, pQ2 e pQ3. Em seguida, a função altera esses valores para encontrar uma curva que flui ao longo do caminho mais curto. Os valores de q0, Q2 e Q3 são calculados conforme mostrado abaixo.


```
q0 = |Q0 + Q1| < |Q0 - Q1| ? -Q0 : Q0
q2 = |Q1 + Q2| < |Q1 - Q2| ? -Q2 : Q2
q3 = |Q2 + Q3| < |Q2 - Q3| ? -Q3 : Q3
```



Depois de calcular os novos valores de Q, os valores para AOut, obre e COut são calculados da seguinte maneira:

AOut = T1 \* e<sup> \[ -0,25 \ \* (\ ln \[ exp (Q1) \* T2 \] \ + \ ln \[ exp (Q1) \* q0 \] \) \ \] </sup>

Obre = T2 \* e<sup> \[ -0,25 \ \* (\ ln \[ exp (Q2) \* Q3 \] \ + \ f ln \[ exp (T2) \* Q1 \] \) \] \</sup>

COut = Q2

> [!Note]  
> Ln é o método de API [**D3DXQuaternionLn**](d3d10-d3dxquaternionln.md) e exp é o método de API [**D3DXQuaternionExp**](d3d10-d3dxquaternionexp.md).

 

Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) para qualquer entrada de Quaternion que ainda não esteja normalizada.

### <a name="examples"></a>Exemplos

O exemplo a seguir mostra como usar um conjunto de chaves quaternions (q0, Q1, T2, Q3) para computar os pontos Quadrangle internos (A, B, C). Isso garante que as tangentes sejam contínuas em segmentos adjacentes.


```
      A     B
Q0    Q1    Q2    Q3
```



O exemplo de código a seguir demonstra como você pode interpolar entre Q1 e Q2.


```
// Rotation about the z-axis
D3DXQUATERNION Q0 = D3DXQUATERNION(0,  0, 0.707f, -.707f);
D3DXQUATERNION Q1 = D3DXQUATERNION(0,  0, 0.000f, 1.000f);
D3DXQUATERNION Q2 = D3DXQUATERNION(0,  0, 0.707f, 0.707f);
D3DXQUATERNION Q3 = D3DXQUATERNION(0,  0, 1.000f, 0.000f);
D3DXQUATERNION A, B, C, Qt;
FLOAT time = 0.5f;

D3DXQuaternionSquadSetup(&A, &B, &C, &Q0, &Q1, &Q2, &Q3);
D3DXQuaternionSquad(&Qt, &Q1, &A, &B, &C, time);
```



> [!Note]
>
> -   C é +/-Q2, dependendo do resultado da função.
> -   Qt é o resultado da função.
>
> O resultado é uma rotação de 45 graus em volta do eixo z para time = 0,5.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
