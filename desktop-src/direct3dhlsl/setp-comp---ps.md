---
title: setp_comp-PS
description: Defina o registro de predicado. | setp_comp-PS
ms.assetid: a9acb685-f9aa-41f1-8ef1-6d104cb76a09
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d278a6104a6c47d84623b185f78b921d61899f296eeaa557a6c6c6d5344097b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119487076"
---
# <a name="setp_comp---ps"></a>setp \_ comp-PS

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

    

     

-   DST é o [predicado Register](dx9-graphics-reference-asm-ps-registers-predicate.md) Register, P0.
-   src0 é um registro de origem.
-   src1 é um registro de origem.

## <a name="remarks"></a>Comentários



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| comp de setp \_            |      |      |      |      |      | x    | x     | x    | x     |



 

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

O registro de hora de verão deve ser o registro de predicado.

## <a name="applying-the-predicate-register"></a>Aplicando o registro de predicado

Depois que o registro de predicado tiver sido inicializado com setp \_ comp, ele poderá ser usado para controlar uma instrução por componente. Esta é a sintaxe:


```
([!]p0[.swizzle]) instruction dest, src0, ...
```



Em que:

-   \[!\] é um booliano opcional não
-   P0 é o registro de predicado
-   \[. swizzle \] é um swizzle opcional a ser aplicado ao conteúdo do predicado Register antes de usá-lo para mascarar a instrução. Os swizzles disponíveis são:. xyzw (padrão quando nenhum especificado) ou qualquer replicar swizzle:. x/. r,. y/. g,. z/. b ou. a/. w.
-   instrução é qualquer instrução aritmetic ou de textura. Essa não pode ser uma instrução de controle de fluxo estática ou dinâmica.
-   dest, src0,... os registros são exigidos pela instrução

Supondo que o registro de predicado tenha sido configurado com valores de componente (true, true, false, false), ele pode ser aplicado a esta instrução:


```
(p0) add r1, r2, r3
```



para executar um componente 2, adicione.


```
r1.x = r2.x + r3.x
r1.y = r2.y + r3.y
```



Os componentes z e w de R1 não serão escritos, pois o registro de predicado continha false nos componentes z e w.

A aplicação do predicado Register a uma instrução aritmética ou de textura aumenta sua contagem de Slots de instrução em 1.

O registro de predicado também pode ser aplicado às instruções [Pred-PS](if-pred---ps.md), [callnz Pred-PS](callnz-pred---ps.md) e [breakp-PS](break-p---ps.md) . Essas instruções de controle de fluxo não têm nenhum aumento na contagem de Slots de instrução ao usar o registro de predicado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




