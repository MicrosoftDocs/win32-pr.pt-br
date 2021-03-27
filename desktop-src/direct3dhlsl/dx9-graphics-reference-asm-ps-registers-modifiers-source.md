---
title: Modificadores de registro de origem do sombreador de pixel
description: Use modificadores de registro de origem para alterar o valor lido de um registro antes de uma instrução ser executada.
ms.assetid: b45d0919-7878-4184-ad4a-5623aae9d1f1
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 12cfee533a71408a445d97a63bbd8b76b281236b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292843"
---
# <a name="pixel-shader-source-register-modifiers"></a>Modificadores de registro de origem do sombreador de pixel

Use modificadores de registro de origem para alterar o valor lido de um registro antes de uma instrução ser executada. O conteúdo de um registro de origem permanece inalterado. Os modificadores são úteis para ajustar o intervalo de dados de registro em preparação para a instrução. Um conjunto de modificadores chamados seletores copia ou replica os dados de um único canal (r, g, b, a) para os outros canais.

## <a name="ps_1_1---ps_1_4"></a>PS \_ 1 \_ 1-PS \_ 1 \_ 4

Esta tabela identifica as versões que oferecem suporte a cada modificador:



| Modificadores de registro de origem                                                                                    | Syntax         | Versão |      |      |      |     |     |
|--------------------------------------------------------------------------------------------------------------|----------------|---------|------|------|------|-----|-----|
|                                                                                                              |                | 1\_1    | 1\_2 | 1 \_ 3 | 1\_4 |     |     |
| [Bias](dx9-graphics-reference-asm-ps-registers-modifiers-bias.md)                                           | registrar \_ diferença | X       | X    | X    | X    |     |     |
| [minúsculo](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md)                                       | 1-registrar   | X       | X    | X    | X    |     |     |
| [negate](dx9-graphics-reference-asm-ps-registers-modifiers-negate.md)                                       | \- Registr    | X       | X    | X    | X    |     |     |
| [escala por 2](dx9-graphics-reference-asm-ps-registers-modifiers-scale-x2.md)                                 | registrar \_ X2   |         |      |      | X    |     |     |
| [dimensionamento assinado](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md)                         | registrar \_ BX2  | X       | X    | X    | X    |     |     |
| [modificadores texld e texcrd](dx9-graphics-reference-asm-ps-registers-modifiers-ps-1-4.md)                   | registrar \_ d\*  | X       | X    | X    | X    |     |     |
| [swizzling de registro de origem](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) | registrar. xyzw  | X       | X    | X    | X    |     |     |



 

Modificadores de registro de origem só podem ser usados em instruções aritméticas. Eles não podem ser usados em instruções de endereço de textura. A exceção a isso é o modificador de [escala por 2](dx9-graphics-reference-asm-ps-registers-modifiers-scale-x2.md) . Para a versão 1 \_ 1, a escala assinada pode ser usada no argumento de origem de qualquer \* instrução texm. Para a versão 1 \_ 2 ou 1 \_ 3, a escala assinada pode ser usada no argumento de origem de qualquer instrução de endereço de textura.

Algumas restrições específicas de modificador:

-   O negar pode ser combinado com o modificador de tendência, dimensionamento assinado ou scalex2. Quando combinado, negar é executado por último.
-   Invert não pode ser combinado com nenhum outro modificador.
-   Invert, negação, tendência, dimensionamento assinado e scalex2 podem ser combinados com qualquer um dos seletores.
-   Os modificadores de registro de origem não devem ser usados em registros constantes porque eles causarão resultados indefinidos. Para a versão 1 \_ 4, os modificadores em constantes não são permitidos e ocorrerão falha na validação.

## <a name="ps_2_0-and-above"></a>PS \_ 2 \_ 0 e superior

Para a versão PS \_ 2 \_ 0 e superior, o número de modificadores foi simplificado.

### <a name="negate"></a>Negar

Negar o conteúdo do registro de origem.



| Modificador de componente | Description     |
|--------------------|-----------------|
| \- d               | Negação de origem |



 

O modificador de negação não pode ser usado no segundo registro de origem dessas instruções: [M3X2-PS](m3x2---ps.md), [m3x3-PS](m3x3---ps.md), [M3x4-PS](m3x4---ps.md), [m4x3-PS](m4x3---ps.md)e [m4x4-PS](m4x4---ps.md).



| Versões do sombreador de pixel | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|-------|------|-------|
| \-                    | x    | x    | x     | x    | x     |



 

### <a name="absolute-value"></a>Valor absoluto

Pegue o valor absoluto do registro.



| Versões do sombreador de pixel | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|-------|------|-------|
| abs                   |      |      |       | x    | x     |



 

Se qualquer sombreador da versão 3 ler um ou mais registros de flutuação constante (c \# ), um dos seguintes deve ser verdadeiro.

-   Todos os registros constantes de ponto flutuante devem usar o modificador ABS.
-   Nenhum dos registros constantes de ponto flutuante pode usar o modificador ABS.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Modificadores de registro do sombreador de pixel](dx9-graphics-reference-asm-ps-registers-modifiers.md)
</dt> </dl>

 

 




