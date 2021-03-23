---
title: Visão geral das assinaturas raiz
description: Uma assinatura de raiz é configurada pelas listas de comandos de aplicativo e links para os recursos que os sombreadores precisam.
ms.assetid: 2E649DA2-6CAC-4C2A-A420-D4EC0DD6EA73
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85eb5882e4a893c2933c55281f21c49f2d7d50d7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548275"
---
# <a name="root-signatures-overview"></a>Visão geral das assinaturas raiz

Uma assinatura de raiz é configurada pelas listas de comandos de aplicativo e links para os recursos que os sombreadores precisam. A lista de comandos de gráficos tem uma assinatura de raiz de computação e de elementos gráficos. Uma lista de comandos de computação terá apenas uma assinatura de raiz de computação. Essas assinaturas raiz são independentes umas das outras.

-   [Parâmetros e argumentos raiz](#root-parameters-and-arguments)
-   [Constantes, descritores e tabelas raiz](#root-constants-descriptors-and-tables)
-   [Tópicos relacionados](#related-topics)

## <a name="root-parameters-and-arguments"></a>Parâmetros e argumentos raiz

Uma **assinatura de raiz** é semelhante a uma assinatura de função de API, ela determina os tipos de dados que os sombreadores devem esperar, mas não define a memória ou os dados reais. Um **parâmetro raiz** é uma entrada na assinatura raiz. Os valores reais dos parâmetros raiz definidos e alterados em tempo de execução são chamados de **argumentos raiz**. A alteração dos argumentos raiz altera os dados lidos pelos sombreadores.

## <a name="root-constants-descriptors-and-tables"></a>Constantes, descritores e tabelas raiz

A assinatura raiz pode conter três tipos de parâmetros; constantes raiz (constantes embutidas nos argumentos raiz), descritores de raiz (descritores embutidos nos argumentos raiz) e tabelas de descrição (ponteiros para um intervalo de descritores no heap de descrição).

As constantes raiz são valores embutidos de 32 bits que aparecem no sombreador como um buffer constante.

Os descritores raiz embutidos devem conter descritores que são acessados com mais frequência, porém são limitados a CBVs e buffers UAV ou de servidor brutos ou estruturados. Um tipo mais complexo, como uma textura de 2D SRV, não pode ser usado como um descritor de raiz. Os descritores raiz não incluem um limite de tamanho, portanto, não pode haver nenhuma verificação de limite fora de limites, ao contrário dos descritores de heaps, que incluem um tamanho.

As entradas da tabela de descritores dentro das assinaturas raiz contêm o descritor, o nome de associação do sombreador HLSL e o sinalizador de Consulte o [modelo do sombreador 5,1](/windows/desktop/direct3dhlsl/shader-model-5-1) para obter detalhes de nomes de sombreador. Em alguns hardwares, pode haver um lucro de desempenho apenas para tornar os descritores visíveis para os estágios do sombreador que os exigem (consulte a [**\_ \_ visibilidade do sombreador D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility)).

![entrada da tabela do descritor raiz](images/root-descriptor-table.png)

O layout da assinatura raiz é bastante flexível, com algumas restrições impostas em hardwares com menos capacidade. Independentemente do nível de hardware, os aplicativos sempre devem tentar tornar a assinatura raiz tão pequena quanto necessária para máxima eficiência. Os aplicativos podem compensar mais tabelas de descritores na assinatura raiz, mas menos espaço para as constantes raiz, ou vice-versa.

O conteúdo da assinatura raiz (as tabelas de descritores, as constantes raiz e os descritores raiz) que o aplicativo tem associado recebe controle de versão automaticamente pelo driver D3D12 sempre que qualquer parte do conteúdo é alterada entre chamadas de/dispatch (computação) de desenho (gráfico). Portanto, cada empate/expedição Obtém um conjunto completo exclusivo de estado de assinatura raiz.

O ideal é que existam grupos de PSOs (objetos de estado de pipeline) que compartilham a mesma assinatura raiz. Depois que uma assinatura de raiz é definida no pipeline, todas as associações que ele define (tabelas de descritores, descriprs, constantes) podem ser definidas ou alteradas individualmente, incluindo a herança em grupos.

Um aplicativo pode fazer sua própria compensação entre a quantidade de tabelas de descritores que desejam criar descritores embutidos (que levam mais espaço, mas removem um indireção), que são constantes embutidas (que não têm nenhum indireção) que desejam na assinatura raiz. Os aplicativos devem usar a assinatura raiz da maneira mais moderada possível, dependendo da memória controlada pelo aplicativo, como heaps e heaps de descritores que apontam para representar dados em massa.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Assinaturas raiz](root-signatures.md)
</dt> </dl>

 

 