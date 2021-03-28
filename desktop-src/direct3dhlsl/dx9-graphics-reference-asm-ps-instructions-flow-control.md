---
title: Limitações de controle de fluxo
description: As instruções de controle de fluxo do sombreador de pixel têm limites que afetam o número de níveis de aninhamento que podem ser incluídos nas instruções. Além disso, há algumas limitações para implementar o controle de fluxo por pixel com instruções de gradiente.
ms.assetid: 17a902cd-16a4-4065-9249-01f9b1f40506
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 34891e29a1bb27aead629db2cc7473c7d4329af5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103823040"
---
# <a name="flow-control-limitations"></a>Limitações de controle de fluxo

As instruções de controle de fluxo do sombreador de pixel têm limites que afetam o número de níveis de aninhamento que podem ser incluídos nas instruções. Além disso, há algumas limitações para implementar o controle de fluxo por pixel com instruções de gradiente.

> [!Note]  
> Ao usar os \* \_ perfis de \_ sombreador HLSL de 4% do \_ nível \_ 9 \_ x, você usa implicitamente os perfis do [Shader Model 2. x](dx-graphics-hlsl-sm2.md) para dar suporte ao hardware compatível com Direct3D 9. Os perfis do modelo de sombreador 2. x dão suporte a um comportamento de controle de fluxo mais limitado que o [sombreador modelo 4. x](dx-graphics-hlsl-sm4.md) e perfis posteriores.

 

-   [Contagens de profundidade de instrução do sombreador de pixel](#pixel-shader-instruction-depth-counts)
-   [Interação do controle de fluxo de Per-Pixel com gradientes de tela](#interaction-of-per-pixel-flow-control-with-screen-gradients)

## <a name="pixel-shader-instruction-depth-counts"></a>Contagens de profundidade de instrução do sombreador de pixel

\_o PS 2 \_ 0 não oferece suporte ao controle de fluxo. As limitações para as outras versões de sombreador de pixel estão listadas abaixo.

### <a name="instruction-depth-count-for-ps_2_x"></a>Contagem de profundidade de instrução para PS \_ 2 \_ x

Cada instrução conta com base em um ou mais limites de profundidade de aninhamento. A tabela a seguir lista a contagem de profundidade que cada instrução adiciona ou subtrai da profundidade existente.



| Instrução                              | Aninhamento estático                       | Aninhamento dinâmico                                                           | aninhamento de loop/representante | aninhamento de chamadas |
|------------------------------------------|--------------------------------------|---------------------------------------------------------------------------|------------------|--------------|
| [se bool-PS](if-bool---ps.md)         | 1                                    | 0                                                                         | 0                | 0            |
| [Se \_ comp-PS](if-comp---ps.md)        | 0                                    | 1                                                                         | 0                | 0            |
| [se Pred-PS](if-pred---ps.md)         | 0                                    | 1                                                                         | 0                | 0            |
| [else-PS](else---ps.md)               | 0                                    | 0                                                                         | 0                | 0            |
| [endif-PS](endif---ps.md)             | -1 ([se bool-PS](if-bool---ps.md)) | -1 ([se Pred-PS](if-pred---ps.md) ou [se \_ comp-PS](if-comp---ps.md)) | 0                | 0            |
| [Rep-PS](rep---ps.md)                 | 0                                    | 0                                                                         | 1                | 0            |
| [endrep-PS](endrep---ps.md)           | 0                                    | 0                                                                         | -1               | 0            |
| [-PS de interrupção](break---ps.md)             | 0                                    | 0                                                                         | 0                | 0            |
| [interromper \_ comp-PS](break-comp---ps.md)  | 0                                    | 1,-1                                                                     | 0                | 0            |
| [breakp-PS](break-p---ps.md)          | 0                                    | 0                                                                         | 0                | 0            |
| [Call-PS](call---ps.md)               | 0                                    | 0                                                                         | 0                | 1            |
| [callnz bool-PS](callnz-bool---ps.md) | 0                                    | 0                                                                         | 0                | 1            |
| [callnz Pred-PS](callnz-pred---ps.md) | 0                                    | 1                                                                         | 0                | 1            |
| [RET-PS](ret---ps.md)                 | 0                                    | -1 ([callnz Pred-PS](callnz-pred---ps.md))                              | 0                | -1           |
| [setp \_ comp-PS](setp-comp---ps.md)    | 0                                    | 0                                                                         | 0                | 0            |



 

### <a name="nesting-depth"></a>Profundidade de aninhamento

Profundidade de aninhamento define o número de instruções que podem ser chamadas de dentro umas das outras. Cada tipo de instrução tem um ou mais limites de aninhamento, conforme indicado na tabela a seguir.



| Tipo de instrução | Máximo                                                                                   |
|------------------|-------------------------------------------------------------------------------------------|
| Aninhamento estático   | 24 if (D3DCAPS9. D3DPSHADERCAPS2 \_ 0. StaticFlowControlDepth > 0); caso contrário, 0            |
| Aninhamento dinâmico  | 0 a 24, consulte D3DCAPS9. D3DPSHADERCAPS2 \_ 0. DynamicFlowControlDepth                          |
| aninhamento do representante      | 0 a 4, consulte D3DCAPS9. D3DPSHADERCAPS2 \_ 0. StaticFlowControlDepth                            |
| aninhamento de chamadas     | 0 a 4, consulte D3DCAPS9. D3DPSHADERCAPS2 \_ 0. StaticFlowControlDepth (independente do limite do representante) |



 

### <a name="instruction-depth-count-for-ps_2_sw"></a>Contagem de profundidade de instrução para o \_ SW PS 2 \_

Cada instrução conta com base em um ou mais limites de profundidade de aninhamento. Esta tabela mostra a contagem de profundidade que cada instrução adiciona ou subtrai da profundidade existente.



| Instrução                              | Aninhamento estático                       | Aninhamento dinâmico                                                           | aninhamento de loop/representante | aninhamento de chamadas |
|------------------------------------------|--------------------------------------|---------------------------------------------------------------------------|------------------|--------------|
| [se bool-PS](if-bool---ps.md)         | 1                                    | 0                                                                         | 0                | 0            |
| [se Pred-PS](if-pred---ps.md)         | 0                                    | 1                                                                         | 0                | 0            |
| [Se \_ comp-PS](if-comp---ps.md)        | 0                                    | 1                                                                         | 0                | 0            |
| [else-PS](else---ps.md)               | 0                                    | 0                                                                         | 0                | 0            |
| [endif-PS](endif---ps.md)             | -1 ([se bool-PS](if-bool---ps.md)) | -1 ([se Pred-PS](if-pred---ps.md) ou [se \_ comp-PS](if-comp---ps.md)) | 0                | 0            |
| [Rep-PS](rep---ps.md)                 | 0                                    | 0                                                                         | 1                | 0            |
| [endrep-PS](endrep---ps.md)           | 0                                    | 0                                                                         | -1               | 0            |
| [loop-PS](loop---ps.md)               | N/D                                  | N/D                                                                       | N/D              | N/D          |
| [ENDLOOP-PS](endloop---ps.md)         | N/D                                  | N/D                                                                       | N/D              | N/D          |
| [-PS de interrupção](break---ps.md)             | 0                                    | 0                                                                         | 0                | 0            |
| [interromper \_ comp-PS](break-comp---ps.md)  | 0                                    | 1,-1                                                                     | 0                | 0            |
| [breakp-PS](break-p---ps.md)          | 0                                    | 0                                                                         | 0                | 0            |
| [Call-PS](call---ps.md)               | 0                                    | 0                                                                         | 0                | 1            |
| [callnz bool-PS](callnz-bool---ps.md) | 0                                    | 0                                                                         | 0                | 1            |
| [callnz Pred-PS](callnz-pred---ps.md) | 0                                    | 1                                                                         | 0                | 1            |
| [RET-PS](ret---ps.md)                 | 0                                    | -1 ([callnz Pred-PS](callnz-pred---ps.md))                              | 0                | -1           |
| [setp \_ comp-PS](setp-comp---ps.md)    | 0                                    | 0                                                                         | 0                | 0            |



 

### <a name="nesting-depth"></a>Profundidade de aninhamento

Profundidade de aninhamento define o número de instruções que podem ser chamadas de dentro umas das outras. Cada tipo de instrução tem um ou mais limites de aninhamento, conforme indicado na tabela a seguir.



| Tipo de instrução | Máximo |
|------------------|---------|
| Aninhamento estático   | 24      |
| Aninhamento dinâmico  | 24      |
| aninhamento do representante      | 4       |
| aninhamento de chamadas     | 4       |



 

### <a name="instruction-depth-count-for-ps_3_0"></a>Contagem de profundidade de instrução para PS \_ 3 \_ 0

Cada instrução conta com base em um ou mais limites de profundidade de aninhamento. Esta tabela mostra a contagem de profundidade que cada instrução adiciona ou subtrai da profundidade existente.



| Instrução                              | Aninhamento estático                       | Aninhamento dinâmico                                                           | aninhamento de loop/representante | aninhamento de chamadas |
|------------------------------------------|--------------------------------------|---------------------------------------------------------------------------|------------------|--------------|
| [se bool-PS](if-bool---ps.md)         | 1                                    | 0                                                                         | 0                | 0            |
| [se Pred-PS](if-pred---ps.md)         | 0                                    | 1                                                                         | 0                | 0            |
| [Se \_ comp-PS](if-comp---ps.md)        | 0                                    | 1                                                                         | 0                | 0            |
| [else-PS](else---ps.md)               | 0                                    | 0                                                                         | 0                | 0            |
| [endif-PS](endif---ps.md)             | -1 ([se bool-PS](if-bool---ps.md)) | -1 ([se Pred-PS](if-pred---ps.md) ou [se \_ comp-PS](if-comp---ps.md)) | 0                | 0            |
| [Rep-PS](rep---ps.md)                 | 0                                    | 0                                                                         | 1                | 0            |
| [endrep-PS](endrep---ps.md)           | 0                                    | 0                                                                         | -1               | 0            |
| [loop-PS](loop---ps.md)               | 0                                    | 0                                                                         | 1                | 0            |
| [ENDLOOP-PS](endloop---ps.md)         | 0                                    | 0                                                                         | -1               | 0            |
| [-PS de interrupção](break---ps.md)             | 0                                    | 0                                                                         | 0                | 0            |
| [interromper \_ comp-PS](break-comp---ps.md)  | 0                                    | 1,-1                                                                     | 0                | 0            |
| [breakp-PS](break-p---ps.md)          | 0                                    | 0                                                                         | 0                | 0            |
| [Call-PS](call---ps.md)               | 0                                    | 0                                                                         | 0                | 1            |
| [callnz bool-PS](callnz-bool---ps.md) | 0                                    | 0                                                                         | 0                | 1            |
| [callnz Pred-PS](callnz-pred---ps.md) | 0                                    | 1                                                                         | 0                | 1            |
| [RET-PS](ret---ps.md)                 | 0                                    | -1 ([callnz Pred-PS](callnz-pred---ps.md))                              | 0                | -1           |
| [setp \_ comp-PS](setp-comp---ps.md)    | 0                                    | 0                                                                         | 0                | 0            |



 

### <a name="nesting-depth"></a>Profundidade de aninhamento

Profundidade de aninhamento define o número de instruções que podem ser chamadas de dentro umas das outras. Cada tipo de instrução tem um ou mais limites de aninhamento, conforme indicado na tabela a seguir.



| Tipo de instrução | Máximo |
|------------------|---------|
| Aninhamento estático   | 24      |
| Aninhamento dinâmico  | 24      |
| aninhamento de loop/representante | 4       |
| aninhamento de chamadas     | 4       |



 

### <a name="instruction-depth-count-for-ps_3_sw"></a>Contagem de profundidade de instrução para o \_ software PS 3 \_

Cada instrução conta com base em um ou mais limites de profundidade de aninhamento. Esta tabela mostra a contagem de profundidade que cada instrução adiciona ou subtrai da profundidade existente.



| Instrução                              | Aninhamento estático                       | Aninhamento dinâmico                                                           | aninhamento de loop/representante | aninhamento de chamadas |
|------------------------------------------|--------------------------------------|---------------------------------------------------------------------------|------------------|--------------|
| [se bool-PS](if-bool---ps.md)         | 1                                    | 0                                                                         | 0                | 0            |
| [se Pred-PS](if-pred---ps.md)         | 0                                    | 1                                                                         | 0                | 0            |
| [Se \_ comp-PS](if-comp---ps.md)        | 0                                    | 1                                                                         | 0                | 0            |
| [else-PS](else---ps.md)               | 0                                    | 0                                                                         | 0                | 0            |
| [endif-PS](endif---ps.md)             | -1 ([se bool-PS](if-bool---ps.md)) | -1 ([se Pred-PS](if-pred---ps.md) ou [se \_ comp-PS](if-comp---ps.md)) | 0                | 0            |
| [Rep-PS](rep---ps.md)                 | 0                                    | 0                                                                         | 1                | 0            |
| [endrep-PS](endrep---ps.md)           | 0                                    | 0                                                                         | -1               | 0            |
| [loop-PS](loop---ps.md)               | 0                                    | 0                                                                         | 1                | 0            |
| [ENDLOOP-PS](endloop---ps.md)         | 0                                    | 0                                                                         | -1               | 0            |
| [-PS de interrupção](break---ps.md)             | 0                                    | 0                                                                         | 0                | 0            |
| [interromper \_ comp-PS](break-comp---ps.md)  | 0                                    | 1,-1                                                                     | 0                | 0            |
| [breakp-PS](break-p---ps.md)          | 0                                    | 0                                                                         | 0                | 0            |
| [Call-PS](call---ps.md)               | 0                                    | 0                                                                         | 0                | 1            |
| [callnz bool-PS](callnz-bool---ps.md) | 0                                    | 0                                                                         | 0                | 1            |
| [callnz Pred-PS](callnz-pred---ps.md) | 0                                    | 1                                                                         | 0                | 1            |
| [RET-PS](ret---ps.md)                 | 0                                    | -1 ([callnz Pred-PS](callnz-pred---ps.md))                              | 0                | -1           |
| [setp \_ comp-PS](setp-comp---ps.md)    | 0                                    | 0                                                                         | 0                | 0            |



 

### <a name="nesting-depth"></a>Profundidade de aninhamento

Profundidade de aninhamento define o número de instruções que podem ser chamadas de dentro umas das outras. Cada tipo de instrução tem um ou mais limites de aninhamento, conforme indicado na tabela a seguir.



| Tipo de instrução | Máximo |
|------------------|---------|
| Aninhamento estático   | 24      |
| Aninhamento dinâmico  | 24      |
| aninhamento de loop/representante | 4       |
| aninhamento de chamadas     | 4       |



 

## <a name="interaction-of-per-pixel-flow-control-with-screen-gradients"></a>Interação do controle de fluxo de Per-Pixel com gradientes de tela

O conjunto de instruções do sombreador de pixel inclui várias instruções que produzem ou usam gradientes de quantidades com relação ao espaço de tela x e y. O uso mais comum para gradientes é computar cálculos de nível de detalhes para amostragem de textura e, no caso de filtragem de anisotropic, selecionando amostras ao longo do eixo de anisotropy. Normalmente, as implementações de hardware executam o sombreador de pixel em vários pixels simultaneamente (como uma grade 2x2), para que os gradientes das quantidades computadas no sombreador possam ser razoavelmente aproximados como deltas dos valores no mesmo ponto de execução em pixels adjacentes.

Quando o controle de fluxo está presente em um sombreador, o resultado de um cálculo de gradiente solicitado dentro de um determinado caminho de ramificação é ambíguo quando pixels adjacentes podem executar caminhos de controle de fluxo separados. Portanto, é considerado ilegal usar qualquer operação de sombreador de pixel que solicite a ocorrência de um cálculo de gradiente em um local que esteja dentro de uma construção de controle de fluxo que pode variar em pixels para um determinado primitivo ser rasterizado.

Todas as instruções de sombreador de pixel são particionadas nessas operações que são permitidas e em aquelas que não são permitidas dentro do controle de fluxo:

-   Cenário A: operações que não são permitidas dentro do controle de fluxo que podem variar entre os pixels em um primitivo. Isso inclui as operações listadas na tabela a seguir. 

    | Instrução                                                                                                      | É permitido no controle de fluxo quando:                       |
    |------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
    | [texld-PS \_ 2 \_ 0 e up](texld---ps-2-0.md), [texldb-PS](texldb---ps.md) e [texldp-PS](texldp---ps.md) | Um registro temporário é usado para a coordenada de textura. |
    | [DSX-PS](dsx---ps.md) e [DSY-PS](dsy---ps.md)                                                            | Um registro temporário é usado para o operando.            |

    

     

-   Cenário B: operações que são permitidas em qualquer lugar. Isso inclui as operações listadas na tabela a seguir. 

    | Instrução                                                                                                      | É permitido em qualquer lugar quando:                                                                                             |
    |------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
    | [texld-PS \_ 2 \_ 0 e up](texld---ps-2-0.md), [texldb-PS](texldb---ps.md) e [texldp-PS](texldp---ps.md) | Uma quantidade somente leitura é usada para a coordenada de textura (pode variar por pixel, como coordenadas de textura interpoladas). |
    | [DSX-PS](dsx---ps.md) e [DSY-PS](dsy---ps.md)                                                            | Uma quantidade somente leitura é usada para o operando de entrada (pode variar por pixel, como coordenadas de textura interpoladas).      |
    | [texldl-PS](texldl---ps.md)                                                                                   | O usuário fornece o nível de detalhe como um argumento, portanto, não há gradientes e, portanto, não há nenhum problema com o controle de fluxo.       |
    | [texldd-PS](texldd---ps.md)                                                                                   | O usuário fornece gradientes como argumentos de entrada, portanto, não há nenhum problema com o controle de fluxo.                                 |

    

     

Essas restrições são estritamente impostas na validação do sombreador. Os cenários que têm uma condição de ramificação semelhante a ela poderiam ramificar consistentemente em um primitivo, embora um operando na expressão de condição seja uma quantidade computada por pixel-sombreado, mas ainda assim se enquadrasse no cenário A e não é permitido. Da mesma forma, os cenários em que os gradientes são solicitados em alguma quantidade x computada por sombreador de dentro do controle de fluxo dinâmico, ainda que ele pareça que x não é modificado em nenhum dos branches, ainda que se enquadrasse no cenário A e não é permitido.

O predicação está incluído nessas restrições no controle de fluxo, para que as implementações permaneçam livres para trocar trivialmente a implementação de instruções de Branch com instruções predicadas.

O usuário pode usar as instruções dos cenários A e B juntos. Por exemplo, suponha que o usuário precise de um exemplo de textura anisotropic dada uma coordenada de textura computada de sombreador; no entanto, a carga de textura só é necessária para pixels que satisfaçam a alguma condição por pixel. Para atender a esses requisitos, o usuário pode computar a coordenada de textura para todos os pixels, fora do controle de fluxo variável por pixel, computando os gradientes imediatamente usando as instruções [DSX-PS](dsx---ps.md) e [DSY-PS](dsy---ps.md) . Em seguida, em um bloco per- [PS](if-bool---ps.md) / [endif-PS](endif---ps.md) , o usuário pode usar [texldd-PS](texldd---ps.md) (carga de textura com gradientes fornecidos pelo usuário), passando os gradientes pré-calculados. Outra maneira de descrever esse padrão de uso é que, embora todos os pixels no primitivo tivessem que computar as coordenadas de textura e estejam envolvidos no cálculo de gradiente, somente os pixels que precisavam fazer uma amostra de uma textura realmente faziam isso.

Independentemente dessas regras, a carga ainda está no usuário para garantir que, antes de computar qualquer gradiente (ou executar um exemplo de textura que calcule implicitamente um gradiente), o registro que contém os dados de origem deve ter sido inicializado para todos os caminhos de execução com antecedência. A inicialização de registros temporários não é validada ou imposta em geral.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




