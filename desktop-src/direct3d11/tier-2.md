---
title: Camada 2
description: Esta seção descreve o suporte de camada 2.
ms.assetid: 4A4AEF13-2F0F-482E-9262-256C257ED85A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58fa6e8ff3dba5780e3507bb2da5273e327a30e1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823868"
---
# <a name="tier-2"></a>Camada 2

Esta seção descreve o suporte de camada 2.

-   Hardware em nível de recurso mínimo 11.1.
-   Todos os recursos do nível anterior (sem as limitações específicas do [Nível 1](tier-1.md)) além de adições aos itens a seguir:
-   As instruções do sombreador para fixação de nível de detalhe e feedback de status mapeado estão disponíveis. Para obter mais informações, consulte [exposição de recursos de lado HLSL](hlsl-tiled-resources-exposure.md).
-   As leituras de blocos não mapeados retornam 0 em todos os componentes não ausentes do formato e o padrão para os componentes ausentes.
-   As gravações em blocos não mapeados são impedidas de chegar à memória, mas podem acabar parando em caches que as leituras subsequentes para o mesmo endereço podem ou não capturar.
-   A filtragem de textura com um volume que abrange blocos **NULOS** e não **NULOS** contribui para 0 (com padrões para componentes de formato ausentes) de texels em blocos **NULOS** na operação de filtragem geral. Alguns hardwares mais antigos não atender a esse requisito e retornam 0 (com padrões para componentes de formato ausentes) para o resultado de filtro completo se quaisquer texels (com peso diferente de zero) se enquadrarem em um bloco **NULO**. Nenhum outro hardware terá permissão para não atender ao requisito de incluir todos os texels (peso diferente de zero) na operação de filtragem.
-   Os acessos a texels **NULOS** fazem com que a operação [**CheckAccessFullyMapped**](/windows/desktop/direct3dhlsl/checkaccessfullymapped) no feedback de status de uma leitura de textura retorne false. Isso não depende de como o resultado do acesso à textura pode fazer com que a gravação seja mascarada no sombreador e de quantos componentes estão no formato da textura (a combinação deles pode dar a impressão de que a textura não precisa ser acessada).
-   Restrições de alinhamento para formas de bloco padrão: os mipmaps que preenchem pelo menos um bloco padrão em todas as dimensões usam garantidamente o agrupamento lado a lado padrão, com o restante considerado compactado como uma **unidade** em blocos N (N relatado ao aplicativo). O aplicativo pode mapear os blocos N para locais arbitrariamente separados em um pool de blocos, mas deve mapear todos ou nenhum dos blocos compactados. A compactação MIP é um conjunto exclusivo de blocos compactados por fatia de matriz.
-   Há suporte para a filtragem de redução mínima/máxima. Para obter informações sobre a filtragem de redução mín./máx., consulte recursos de [amostragem de textura de recursos de lado](tiled-resources-texture-sampling-features.md).
-   Os recursos de blocos gráficos com qualquer mipmaps menor que o tamanho do bloco padrão em qualquer dimensão não têm permissão para ter um tamanho de matriz maior que 1.
-   Limitações de como os blocos podem ser acessados quando há mapeamentos duplicados, descritos em [limitações de acesso de bloco com mapeamentos duplicados](tile-access-limitations-with-duplicate-mappings-.md), continuar a aplicar.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Recursos de azulejos recursos camadas](tiled-resources-features-tiers.md)
</dt> </dl>

 

 