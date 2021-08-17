---
title: texbeml-PS
description: Aplicar um ambiente de relevo falso – mapear transformação com correção de luminância. Isso é feito modificando os dados de endereço de textura do registro de destino, usando o endereço muito data (du, DV), uma matriz de ambiente de choque 2D e uma luminância.
ms.assetid: 345a0b77-8d4e-4a0b-a31a-1153f8cb5961
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c549e93829c3165d4921342d4e74a8dc15bc1518f7c88aa205f8afc889fae95e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118788060"
---
# <a name="texbeml---ps"></a>texbeml-PS

Aplicar um ambiente de relevo falso – mapear transformação com correção de luminância. Isso é feito modificando os dados de endereço de textura do registro de destino, usando o endereço muito data (du, DV), uma matriz de ambiente de choque 2D e uma luminância.

## <a name="syntax"></a>Syntax



| texbeml DST, src |
|------------------|



 

onde

-   DST é o registro de destino.
-   src é um registro de origem.

## <a name="remarks"></a>Comentários



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texbeml               | x    | x    | x    |      |      |      |       |      |       |



 

Os dados de cor vermelho e verde no registro src são interpretados como os dados de muito (du, DV). Os dados de cor azul no registro src são interpretados como os dados de luminância.

Essa instrução transforma os componentes vermelho e verde no registro de origem usando a matriz de mapeamento de ambiente de choque 2D. O resultado é adicionado ao conjunto de coordenadas de textura correspondente ao número de registro de destino. Uma correção de luminância é aplicada usando o valor de luminância e os valores de estágio de textura de tendência. O resultado é usado para exemplificar o estágio de textura atual.

Isso pode ser usado para uma variedade de técnicas com base no endereço muito, como o mapeamento de ambiente falso por pixel.

Essa operação sempre interpreta du e DV como quantidades assinadas. Para as versões 1 \_ e 1 \_ 1, o modificador de entrada de [dimensionamento assinado do registro de origem](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md) ( \_ BX2) não é permitido no argumento de entrada.

Essa instrução produz resultados definidos quando texturas de entrada contêm dados de formato misto. Para obter mais informações sobre formatos de superfície, consulte [D3DFORMAT](/windows/desktop/direct3d9/d3dformat).


```
// When using this instruction, texture registers must follow 
//   the following sequence:
// The texture assigned to stage tn contains the (du,dv) data
// The texture assigned to stage t(m) is sampled
tex     t(n)                    
texbeml t(m),  t(n)      where m > n
```



Este exemplo mostra os cálculos feitos dentro da instrução.


```
// 1. New values for texture addresses (u',v') are calculated
// 2. Sample the texture using (u',v')
// 3. Luminance correction is applied
```



u ' = TextureCoordinates (estágio m)<sub>u</sub> +

D3DTSS \_ BUMPENVMAT00 (estágio m) \* t (n)<sub>R</sub> +

D3DTSS \_ BUMPENVMAT10 (estágio m) \* t (n)<sub>G</sub>

v ' = TextureCoordinates (estágio m)<sub>v</sub> +

D3DTSS \_ BUMPENVMAT01 (estágio m) \* t (n)<sub>R</sub> +

D3DTSS \_ BUMPENVMAT11 (estágio m) \* t (n)<sub>G</sub>

t (m)<sub>RGBA</sub> = TextureSample (estágio m) usando (u ', v ') como coordenadas

t (m)<sub>RGBA</sub> = t (m)<sub>RGBA</sub>\*

\[(t (n)<sub>B</sub> \* D3DTSS \_ BUMPENVLSCALE (estágio m)) +

D3DTSS \_ BUMPENVLOFFSET (estágio m)\]

Os dados de registro que foram lidos por uma instrução [texbem](texbem---ps.md) ou texbeml não podem ser lidos mais tarde, exceto por outro texbem ou texbeml.


```
// This example demonstrates the validation error caused by 
//   t0 being reread
ps_1_1
tex t0
texbem t1, t0
add r0, t1, t0

(Instruction Error) (Statement 4) Register data that has been read by 
texbem or texbeml instruction cannot be read by other instructions
```



## <a name="examples"></a>Exemplos

Aqui está um sombreador de exemplo com os mapas de textura identificados e os estágios de textura identificados.


```
ps_1_1
tex t0              ; Define t0 to get a 2-tuple DuDv
texbeml t1, t0      ; Compute (u',v')
                    ; Apply luminance correction                    
                    ; Sample t1 using (u',v')
mov r0, t1          ; Output result
```



Este exemplo requer as seguintes texturas nos seguintes estágios de textura.

-   O estágio 0 recebe um mapa de relevo com os dados (du, DV) muito.
-   O estágio 1 recebe um mapa de textura com dados de cores.
-   texbeml define os dados de matriz no estágio de textura que é amostrado. Isso é diferente da funcionalidade do pipeline de função fixa em que os dados muito e as matrizes ocupam o mesmo estágio de textura.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 