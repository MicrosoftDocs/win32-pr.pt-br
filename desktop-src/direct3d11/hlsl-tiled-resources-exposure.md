---
title: Exposição de recursos lado a lado HLSL
description: A nova sintaxe HLSL (Microsoft High Level Shader Language) é necessária para dar suporte a recursos lado a lado no Modelo de Sombreador 5.
ms.assetid: B6CE51E6-1BA9-4D15-9654-86FE9BAAF585
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c66ded502bebefc1061028115a12026f67c26cad89ddc57f98a5ae6fee923591
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119633326"
---
# <a name="hlsl-tiled-resources-exposure"></a>Exposição de recursos lado a lado HLSL

Nova sintaxe HLSL (Microsoft High Level Shader Language) é necessária para dar suporte a recursos lado a lado no [Modelo de Sombreador 5](/windows/desktop/direct3dhlsl/d3d11-graphics-reference-sm5).

A nova sintaxe HLSL é permitida somente em dispositivos com suporte a recursos lado a lado. Cada método HLSL relevante para recursos lado a lado na tabela a seguir aceita um (comentários) ou dois parâmetros opcionais adicionais (fixação e comentários nessa ordem). Por exemplo, um método de **Amostra** é:

**Sample(sampler, location \[ , offset \[ , fixe , feedback \[ \] \] \] )**

Um exemplo de um método de **Amostra** é [**Texture2D.Sample(S,float,int,float,uint)**](/windows/desktop/direct3dhlsl/t2darray-sample-s-float-int-float-uint-).

Os parâmetros de deslocamento, vinculação e feedback são opcionais. Você deve especificar todos os parâmetros opcionais até aquele que você precisa, que é consistente com as regras do C++ para argumentos de função padrão. Por exemplo, se for necessário o status de feedback, parâmetros de compensação e vinculação precisam ser fornecidos explicitamente à **Amostra**, mesmo que eles talvez não sejam logicamente necessários.

O parâmetro de vinculação é um valor flutuante escalar. O valor literal de vinculação = 0.0f indica que a operação de vinculação não é executada.

O parâmetro de feedback é uma variável **uint** que você pode fornecer para o acesso à memória consultando a função intrínseca [**CheckAccessFullyMapped**](/windows/desktop/direct3dhlsl/checkaccessfullymapped). Você não deve modificar ou interpretar o valor do parâmetro de feedback; porém, o compilador não fornece qualquer análise avançada e diagnóstico para detectar se você modificou o valor.

Veja aqui a sintaxe de [**CheckAccessFullyMapped**](/windows/desktop/direct3dhlsl/checkaccessfullymapped):

**bool CheckAccessFullyMapped(em uint FeedbackVar);**

[**CheckAccessFullyMapped**](/windows/desktop/direct3dhlsl/checkaccessfullymapped) interpreta o valor de *FeedbackVar* e retorna true se todos os dados que estão sendo acessados foram mapeados no recurso; caso contrário, **CheckAccessFullyMapped** retorna false.

Se o parâmetro de feedback ou vinculação estiver presente, o compilador emite uma variante de instrução básica. Por exemplo, o exemplo de um recurso lado a lado gera a `sample_cl_s` instrução . Se nem a vinculação nem o feedback forem especificados, o compilador emite a instrução básica, para que não haja nenhuma alteração do comportamento atual. O valor de vinculação de 0.0f indica que nenhuma vinculação é realizada; dessa forma, o compilador de driver adicional pode continuar adaptando a instrução para o hardware de destino. Se o feedback for um registro NULL em uma instrução, o feedback não é utilizado; dessa forma, o compilador de driver pode continuar adaptando a instrução para a arquitetura de destino.

Se o compilador HLSL infere que vinculação é 0.0f e feedback não é utilizado, o compilador emite a instrução básica correspondente (por exemplo, `sample` em vez de `sample_cl_s`).

Se um acesso a recursos lado a lado consiste em várias instruções de código de byte constituintes, por exemplo, para recursos estruturados, o compilador agrega valores de comentários individuais por meio da operação OR para produzir o valor de comentários final. Portanto, você pode ver um único valor de feedback para tal acesso complexo.

Esta é a tabela resumida dos métodos HLSL que são alterados para dar suporte a feedback e/ou vinculação. Todos eles funcionam em recursos lado a lado e não lado a lado de todas as dimensões. Recursos não lado a lado sempre parecem estar totalmente mapeados.



| [Objetos HLSL](/windows/desktop/direct3dhlsl/d3d11-graphics-reference-sm5-objects)                                                                                                                                                                                                                                | Métodos intrínsecos com a opção de comentários ( \* ) – também tem a opção de fixação                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \[Textura de \] RW2D<br/> \[RW \] Texture2DArray<br/> TextureCUBE<br/> TextureCUBEArray<br/>                                                                                                                                                                                    | Coletar<br/> GatherRed<br/> GatherGreen<br/> GatherBlue<br/> GatherAlpha<br/> GatherCmp<br/> GatherCmpRed<br/> GatherCmpGreen<br/> GatherCmpBlue<br/> GatherCmpAlpha<br/> |
| \[RW \] Texture1D<br/> \[RW \] Texture1DArray<br/> \[Textura de \] RW2D<br/> \[RW \] Texture2DArray<br/> \[Textura \] RW3D<br/> TextureCUBE<br/> TextureCUBEArray<br/>                                                                                              | Amostra\*<br/> SampleBias\*<br/> SampleCmp\*<br/> SampleCmpLevelZero<br/> SampleGrad\*<br/> SampleLevel<br/>                                                                                      |
| \[RW \] Texture1D<br/> \[RW \] Texture1DArray<br/> \[Textura de \] RW2D<br/> Texture2DMS<br/> \[RW \] Texture2DArray<br/> Texture2DArrayMS<br/> \[Textura \] RW3D<br/> \[RW \] Buffer<br/> \[ByteAddressBuffer do RW \]<br/> \[RW \] StructuredBuffer<br/> | Carregar                                                                                                                                                                                                                                 |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Acesso de pipeline a recursos lado a lado](pipeline-access-to-tiled-resources.md)
</dt> </dl>

 

