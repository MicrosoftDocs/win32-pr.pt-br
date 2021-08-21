---
description: O pipeline de gráficos do Direct3D 10 representa uma alteração de arquitetura fundamental, reconstruída desde o princípio em hardware e software para a próxima geração de jogos e aplicativos multimídia 3D.
ms.assetid: 2e24de6c-4f73-4844-b87f-3487ef069db6
title: Recursos da API (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 416018fcddf2643ba9fbc8e633ec2f636b8158ff329780a55205034e5dbbe240
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858656"
---
# <a name="api-features-direct3d-10"></a>Recursos da API (Direct3D 10)

O pipeline de gráficos do Direct3D 10 representa uma alteração de arquitetura fundamental, reconstruída desde o princípio em hardware e software para a próxima geração de jogos e aplicativos multimídia 3D. Ele usa o Windows WDDM (Display Driver Model), que permite aprimoramentos comportamentais e de desempenho, como memória de GPU virtual.

Os desenvolvedores familiarizados com o Direct3D 9 descobrirão uma série de aprimoramentos funcionais e melhorias de desempenho no Direct3D 10, incluindo:

-   A capacidade de processar primitivos inteiros no novo [estágio de sombreador de geometria.](/previous-versions//bb205146(v=vs.85))
-   A capacidade de gerar dados de vértice gerados pelo pipeline para a memória usando o [estágio stream-output](../direct3d11/d3d10-graphics-programming-guide-output-stream-stage.md).
-   Organização do estado do pipeline em cinco objetos de estado [imutáveis,](d3d10-graphics-programming-guide-api-features-state-objects.md)permitindo uma configuração rápida do pipeline.
-   Organização de constantes de sombreador em [buffers constantes,](d3d10-graphics-programming-guide-resources-types.md)minimizando a sobrecarga de largura de banda para fornecer dados de constante de sombreador.
-   A capacidade de executar a troca de material por primitivo e a instalação usando um sombreador de geometria.
-   Novos [tipos de recursos](d3d10-graphics-programming-guide-resources-types.md) (incluindo matrizes de textura que podem ser indexadas de sombreadores) e formatos de recurso.
-   Maior generalização do acesso a recursos usando uma [exibição](d3d10-graphics-programming-guide-resources-access-views.md).
-   Os bits de funcionalidade de hardware herdados (caps) foram removidos em favor de um conjunto avançado de funcionalidades garantidas, que tem como alvo o hardware de classe Direct3D 10 (mínimo).
-   [Runtime](d3d10-graphics-programming-guide-api-features-layers.md) em camadas – a API do Direct3D 10 é construída com camadas, começando com a funcionalidade básica no núcleo e criando funcionalidades opcionais e de assistência do desenvolvedor (depuração, etc.) em camadas externas.
-   Integração HLSL completa – todos os sombreadores direct3D 10 são escritos em HLSL e implementados com o núcleo do [sombreador comum.](../direct3dhlsl/dx-graphics-hlsl-common-core.md)
-   Um aumento no número de destinos de renderização, texturas e amostras. Também não há nenhum limite de comprimento do sombreador.
-   Operações de sombreador inteiro e bit a bit.
-   Readback de uma superfície de profundidade/estêncil ou um recurso multisampled, uma vez que ele não está mais vinculado como um destino de renderização.
-   Suporte multisampled alfa-to-coverage.

Há diferenças comportamentais adicionais que os desenvolvedores do Direct3D 9 também devem estar cientes (consulte Considerações sobre o [Direct3D 9 para Direct3D 10).](d3d10-graphics-programming-guide-d3d9-to-d3d10-considerations.md)

Aqui está uma lista de recursos do Direct3D 9 que não têm mais suporte ou foram revisados no Direct3D 10 (consulte [Recursos preterido).](d3d10-graphics-programming-guide-api-features-deprecated.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia de Programação para Direct3D 10](d3d10-graphics-programming-guide.md)
</dt> </dl>

 

 
