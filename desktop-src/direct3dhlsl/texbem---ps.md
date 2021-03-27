---
title: texbem-PS
description: Aplicar um ambiente de relevo falso – transformação de mapa. Isso é feito modificando os dados de endereço de textura do registro de destino, usando o endereço muito data (du, DV) e uma matriz de ambiente de relevo 2D.
ms.assetid: 8e773f4a-c7a2-4caf-973f-8f50dccc9c04
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f026819b268836fd7d4c1d550033ceefdf0bbbf9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104967186"
---
# <a name="texbem---ps"></a>texbem-PS

Aplicar um ambiente de relevo falso – transformação de mapa. Isso é feito modificando os dados de endereço de textura do registro de destino, usando o endereço muito data (du, DV) e uma matriz de ambiente de relevo 2D.

## <a name="syntax"></a>Syntax



| texbem DST, src |
|-----------------|



 

onde

-   DST é o registro de destino.
-   src é um registro de origem.

## <a name="remarks"></a>Comentários



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texbem                | x    | x    | x    |      |      |      |       |      |       |



 

Os dados de cor vermelho e verde no registro src são interpretados como os dados de muito (du, DV).

Essa instrução transforma os componentes vermelho e verde no registro de origem usando a matriz de mapeamento do ambiente de choque 2D. O resultado é adicionado ao conjunto de coordenadas de textura correspondente ao número de registro de destino e é usado para exemplificar o estágio de textura atual.

Essa operação sempre interpreta du e DV como quantidades assinadas. Para as versões 1 \_ e 1 \_ 1, o modificador de entrada de [dimensionamento assinado do registro de origem](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md) ( \_ BX2) não é permitido no argumento de entrada.

Essa instrução produz resultados definidos quando as texturas de entrada contêm dados de formato assinado. Os dados de formato misto só funcionarão se os dois primeiros canais contiverem dados assinados. Para obter mais informações sobre formatos de superfície, consulte [D3DFORMAT](/windows/desktop/direct3d9/d3dformat).

Isso pode ser usado para uma variedade de técnicas com base no endereço muito, incluindo mapeamento de ambiente falso por pixel e iluminação difusa (mapeamento de choque).

Ao usar essa instrução, os registros de textura devem seguir a sequência a seguir.


```
// The texture assigned to stage t(n) contains the (du,dv) data
// The texture assigned to stage t(m) is sampled
tex     t(n)                    
texbem  t(m),  t(n)      where m > n
```



Os cálculos feitos dentro da instrução são mostrados abaixo.


```
// 1. New values for texture addresses (u',v') are calculated
// 2. Sample the texture using (u',v')
```



u ' = TextureCoordinates (estágio m)<sub>u</sub> + D3DTSS \_ BUMPENVMAT00 (estágio m) \* t (n)<sub>R</sub> + D3DTSS \_ BUMPENVMAT10 (estágio m) \* t (n)<sub>G</sub> v ' = TextureCoordinates (estágio m)<sub>v</sub> + D3DTSS \_ BUMPENVMAT01 (estágio m) \* t (n)<sub>R</sub> + D3DTSS \_ BUMPENVMAT11 (estágio m) \* t (n)<sub>G</sub> t (m)<sub>RGBA</sub> = TextureSample (etapa m)

usando (u ', v ') como coordenadas

Os dados de registro que foram lidos por uma instrução texbem-PS ou [texbeml-PS](texbeml---ps.md) não podem ser lidos mais tarde, exceto por outro texbem-PS ou texbeml-PS.


```
// This example demonstrates the validation error caused by t0 being reread:
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
texbem t1, t0       ; Compute (u',v')
                    ; Sample t1 using (u',v')
mov r0, t1          ; Output result
```



texbem requer as seguintes texturas nos seguintes estágios de textura.

-   O estágio 0 recebe um mapa de relevo com os dados (du, DV) muito.
-   O estágio 1 usa um mapa de textura com dados de cores.
-   Essa instrução define os dados de matriz no estágio de textura que é amostrado.
-   Isso é diferente da funcionalidade do pipeline de função fixa em que os dados muito e as matrizes ocupam o mesmo estágio de textura.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 