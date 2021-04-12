---
title: Exposição dos recursos do lado do HLSL
description: A nova sintaxe de HLSL (linguagem de sombreamento de alto nível) da Microsoft é necessária para dar suporte a recursos de lado do sombreado no modelo de Shader
ms.assetid: B6CE51E6-1BA9-4D15-9654-86FE9BAAF585
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2b266b98045b38645e1e8d24ed0014a5f448a38
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454186"
---
# <a name="hlsl-tiled-resources-exposure"></a>Exposição dos recursos do lado do HLSL

A nova sintaxe de HLSL (linguagem de sombreamento de alto nível) da Microsoft é necessária para dar suporte a recursos de lado do [sombreado no modelo de Shader](/windows/desktop/direct3dhlsl/d3d11-graphics-reference-sm5)

A nova sintaxe HLSL é permitida somente em dispositivos com suporte a recursos de lado. Cada método HLSL relevante para os recursos ao lado do quadro na tabela a seguir aceita um (feedback) ou dois (fixe e comentários nesta ordem) parâmetros opcionais adicionais. Por exemplo, um método de **Amostra** é:

**Exemplo (amostra, local \[ , deslocamento \[ , fixe \[ , comentários \] \] \] )**

Um exemplo de um método de **Amostra** é [**Texture2D.Sample(S,float,int,float,uint)**](/windows/desktop/direct3dhlsl/t2darray-sample-s-float-int-float-uint-).

Os parâmetros de deslocamento, vinculação e feedback são opcionais. Você deve especificar todos os parâmetros opcionais até aquele que você precisa, que é consistente com as regras do C++ para argumentos de função padrão. Por exemplo, se for necessário o status de feedback, parâmetros de compensação e vinculação precisam ser fornecidos explicitamente à **Amostra**, mesmo que eles talvez não sejam logicamente necessários.

O parâmetro de vinculação é um valor flutuante escalar. O valor literal de vinculação = 0.0f indica que a operação de vinculação não é executada.

O parâmetro de feedback é uma variável **uint** que você pode fornecer para o acesso à memória consultando a função intrínseca [**CheckAccessFullyMapped**](/windows/desktop/direct3dhlsl/checkaccessfullymapped). Você não deve modificar ou interpretar o valor do parâmetro de feedback; porém, o compilador não fornece qualquer análise avançada e diagnóstico para detectar se você modificou o valor.

Veja aqui a sintaxe de [**CheckAccessFullyMapped**](/windows/desktop/direct3dhlsl/checkaccessfullymapped):

**bool CheckAccessFullyMapped(em uint FeedbackVar);**

[**CheckAccessFullyMapped**](/windows/desktop/direct3dhlsl/checkaccessfullymapped) interpreta o valor de *FeedbackVar* e retorna true se todos os dados que estão sendo acessados foram mapeados no recurso; caso contrário, **CheckAccessFullyMapped** retorna false.

Se o parâmetro de feedback ou vinculação estiver presente, o compilador emite uma variante de instrução básica. Por exemplo, um exemplo de um recurso de lado-a-botão gera a `sample_cl_s` instrução. Se nem a vinculação nem o feedback forem especificados, o compilador emite a instrução básica, para que não haja nenhuma alteração do comportamento atual. O valor de vinculação de 0.0f indica que nenhuma vinculação é realizada; dessa forma, o compilador de driver adicional pode continuar adaptando a instrução para o hardware de destino. Se o feedback for um registro NULL em uma instrução, o feedback não é utilizado; dessa forma, o compilador de driver pode continuar adaptando a instrução para a arquitetura de destino.

Se o compilador HLSL infere que vinculação é 0.0f e feedback não é utilizado, o compilador emite a instrução básica correspondente (por exemplo, `sample` em vez de `sample_cl_s`).

Se um acesso a recursos de lado ladrilho consistir em várias instruções de código de byte constituintes, por exemplo, para recursos estruturados, o compilador agregará valores de Comentários individuais por meio da operação ou para produzir o valor de comentários final. Portanto, você pode ver um único valor de feedback para tal acesso complexo.

Esta é a tabela resumida dos métodos HLSL que são alterados para dar suporte a feedback e/ou vinculação. Tudo isso funciona em recursos ao lado e fora do lado da região de todas as dimensões. Os recursos sem ladrilhos sempre parecem estar totalmente mapeados.



| [Objetos HLSL](/windows/desktop/direct3dhlsl/d3d11-graphics-reference-sm5-objects)                                                                                                                                                                                                                                | Os métodos intrínsecos com a opção de comentários ( \* ) – também tem a opção fixe                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \[\]TEXTURE2D RW<br/> \[\]TEXTURE2DARRAY RW<br/> TextureCUBE<br/> TextureCUBEArray<br/>                                                                                                                                                                                    | Coletar<br/> GatherRed<br/> GatherGreen<br/> GatherBlue<br/> GatherAlpha<br/> GatherCmp<br/> GatherCmpRed<br/> GatherCmpGreen<br/> GatherCmpBlue<br/> GatherCmpAlpha<br/> |
| \[\]TEXTURE1D RW<br/> \[\]TEXTURE1DARRAY RW<br/> \[\]TEXTURE2D RW<br/> \[\]TEXTURE2DARRAY RW<br/> \[\]TEXTURE3D RW<br/> TextureCUBE<br/> TextureCUBEArray<br/>                                                                                              | Nova\*<br/> SampleBias\*<br/> SampleCmp\*<br/> SampleCmpLevelZero<br/> SampleGrad\*<br/> SampleLevel<br/>                                                                                      |
| \[\]TEXTURE1D RW<br/> \[\]TEXTURE1DARRAY RW<br/> \[\]TEXTURE2D RW<br/> Texture2DMS<br/> \[\]TEXTURE2DARRAY RW<br/> Texture2DArrayMS<br/> \[\]TEXTURE3D RW<br/> \[Buffer de RW \]<br/> \[\]BYTEADDRESSBUFFER RW<br/> \[\]STRUCTUREDBUFFER RW<br/> | Carregamento                                                                                                                                                                                                                                 |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Acesso ao pipeline para recursos lado a lado](pipeline-access-to-tiled-resources.md)
</dt> </dl>

 

