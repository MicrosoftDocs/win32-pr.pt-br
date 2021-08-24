---
title: setp_comp-vs
description: Defina o registro de predicado. | setp_comp-vs
ms.assetid: bfead3f8-f7fe-4fc1-939f-8e5fbc3e0adf
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 892acf44000e178e7ed6774a3841760db32e3ced4d8348a7f9e9c22969bf9024
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119671766"
---
# <a name="setp_comp---vs"></a>setp \_ comp-vs

Defina o registro de predicado.

## <a name="syntax"></a>Syntax



| setp \_ comp DST, src0, src1 |
|----------------------------|



 

Em que:

-   \_comp é uma comparação por canal entre os dois registros de origem. Pode ser um dos seguintes: 

    | Syntax | Comparação            |
    |--------|-----------------------|
    | \_gt   | Maior que          |
    | \_lt   | Menor que             |
    | \_GE   | Maior ou igual |
    | \_quivo   | Inferior ou igual    |
    | \_EQ   | Igual a              |
    | \_m   | É diferente de          |

    

     

-   DST é o [predicado Register](dx9-graphics-reference-asm-vs-registers-predicate.md) Register, P0.
-   src0 é um registro de origem.
-   src1 é um registro de origem.

## <a name="remarks"></a>Comentários



| Versões do sombreador de vértice | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| comp de setp \_             |      |      | x    | x     | x    | x     |



 

Essa instrução Opera como:


```
per channel in destination write mask
{
  dst.channel = src0.channel cmp src1.channel
}
```



Para cada canal que pode ser gravado de acordo com a máscara de gravação de destino, salve o resultado booliano da operação de comparação entre os canais correspondentes de src0 e src1 (depois que o modificador de origem swizzles tiver sido resolvido).

Os registros de origem permitem que swizzles de componente arbitrários sejam especificados.

O registro de destino permite máscaras de gravação arbitrárias.

O registro do dest deve ser o predicado Register.

## <a name="applying-the-predicate-register"></a>Aplicando o registro de predicado

Após o registro de predicado ter sido inicializado com setp, ele pode ser usado para controlar uma instrução por componente. Esta é a sintaxe:


```
([!]p0[.swizzle]) instruction dest, srcReg, ...
```



Em que:

-   \[!\] é um booliano opcional não
-   P0 é o registro de predicado
-   \[. swizzle \] é um swizzle opcional a ser aplicado ao conteúdo do predicado Register antes de usá-lo para mascarar a instrução. Os swizzles disponíveis são:. xyzw (padrão quando nenhum especificado) ou qualquer replicar swizzle:. x/. r,. y/. g,. z/. b ou. a/. w.
-   instrução é qualquer instrução aritmetic ou de textura. Essa não pode ser uma instrução de controle de fluxo estática ou dinâmica.
-   dest, srcReg,... os registros são exigidos pela instrução

Supondo que o registro de predicado tenha sido configurado com valores de componente (true, true, false, false), ele pode ser aplicado a esta instrução:


```
// given r0 = 0,0,1,1
// given r1 = 1,1,0,0
setp_le p0, r0, r1
(p0) add r2, r3, r4
```



para executar um componente 2, adicione.


```
r2.x = r3.x + r4.x
r2.y = r3.y + r4.y
```



Os componentes x e y do R2 não serão gravados, pois o registro de predicado continha false nos componentes z e w.

A aplicação do predicado Register a uma instrução aritmética ou de textura aumenta sua contagem de Slots de instrução em 1.

O registro de predicado também pode ser aplicado a instruções [If Pred-vs](if-pred---vs.md), [callnz Pred-vs](callnz-pred---vs.md) e [breakp-vs](breakp---vs.md) . Essas instruções de controle de fluxo não têm nenhum aumento na contagem de Slots de instrução ao usar o registro de predicado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de vértice](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




