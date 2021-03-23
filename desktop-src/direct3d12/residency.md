---
title: Residência
description: Um objeto é considerado residente quando ele é acessível pela GPU.
ms.assetid: 956F80D7-EEC8-4D88-B251-EE325614F31E
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b842ce5b3e89c3877f50036e747a90f14104bce
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548282"
---
# <a name="residency"></a>Residência

Um objeto é considerado *residente* quando ele é acessível pela GPU.

-   [Orçamento de residência](#residency-budget)
-   [Recursos de heap](#heap-resources)
-   [Prioridades de residência](#residency-priorities)
    -   [Algoritmo de prioridade padrão](#default-priority-algorithm)
-   [Gerenciamento de residência de programação](#programming-residency-management)
-   [Tópicos relacionados](#related-topics)

## <a name="residency-budget"></a>Orçamento de residência

As GPUs ainda não dão suporte à falha de página, portanto, os aplicativos devem confirmar dados na memória física enquanto a GPU puder acessá-la. Esse processo é conhecido como "tornar algo residente" e deve ser feito para a memória física do sistema e para a memória de vídeo discreta física. No D3D12, a maioria dos objetos de API encapsula uma quantidade de memória acessível por GPU. Essa memória acessível por GPU é tornada residente durante a criação do objeto de API e removida na destruição de objeto de API.

A quantidade de memória física disponível para o processo é conhecida como o orçamento de memória de vídeo. O orçamento pode flutuar visivelmente enquanto os processos em segundo plano são ativados e suspensos; e flutuar drasticamente quando o usuário mudar para outro aplicativo. O aplicativo pode ser notificado quando o orçamento for alterado e sondar o orçamento atual e a quantidade de memória consumida atualmente. Se um aplicativo não permanecer dentro de seu orçamento, o processo será congelado intermitentemente para permitir que outros aplicativos sejam executados e/ou as APIs de criação retornarão uma falha. A interface [**IDXGIAdapter3**](/windows/desktop/api/dxgi1_4/nn-dxgi1_4-idxgiadapter3) fornece os métodos que pertencem a essa funcionalidade, em particular [**QueryVideoMemoryInfo**](/windows/desktop/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-queryvideomemoryinfo) e [**RegisterVideoMemoryBudgetChangeNotificationEvent**](/windows/desktop/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-registervideomemorybudgetchangenotificationevent).

Os aplicativos são incentivados a usar uma reserva para denotar a quantidade de memória que não podem ir sem. Idealmente, as configurações de gráficos "baixas" especificadas pelo usuário, ou algo ainda menor, são o valor certo para tal reserva. A definição de uma reserva nunca proporcionará a um aplicativo um orçamento mais alto do que normalmente seria recebido. Em vez disso, as informações de reserva ajudam o kernel do sistema operacional a minimizar rapidamente o impacto de grandes situações de pressão de memória. Até mesmo a reserva não tem garantia de estar disponível para o aplicativo quando o aplicativo não é o aplicativo em primeiro plano.

## <a name="heap-resources"></a>Recursos de heap

Embora muitos objetos de API encapsulam alguma memória acessível por GPU, os heaps & recursos devem ser a maneira mais significativa que os aplicativos consomem e gerenciam a memória física. Um heap é a unidade de nível mais baixa para gerenciar a memória física, portanto, é bom ter alguma familiaridade com suas propriedades de residência.

-   Os heaps não podem se tornar parcialmente residentes, mas existem soluções reservadas com recursos reservados.
-   Os heaps devem ser orçados como parte de um determinado pool. Os adaptadores de uma têm um pool, enquanto os adaptadores discretos têm dois pools. Embora seja verdade que o kernel possa deslocar alguns heaps em adaptadores discretos da memória de vídeo para a memória do sistema, ele só faz isso como um último recurso extremo. Os aplicativos não devem depender do comportamento de orçamento excedente do kernel e devem se concentrar em um bom gerenciamento de orçamento em vez disso.
-   Os heaps podem ser removidos da residência, o que permite que seu conteúdo seja paginado para o disco. Mas, a destruição de heaps é uma técnica mais confiável para liberar residências em todas as arquiteturas de adaptadores. Em adaptadores em que o campo *theMaxGPUVirtualAddressBitsPerProcess* do [**\_ \_ \_ \_ \_ \_ suporte de endereço virtual de GPU de dados de recurso D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_gpu_virtual_address_support) está próximo do tamanho do orçamento, a [**remoção**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-evict) não recuperará de forma confiável a residência.
-   A criação de heap pode ser lenta; Mas é otimizado para processamento de thread em segundo plano. É recomendável criar heaps em threads em segundo plano para evitar a falha do thread de renderização. No D3D12, vários threads podem chamar com segurança as rotinas de criação simultaneamente.

O D3D12 apresenta mais flexibilidade e versatilidade em seu modelo de recursos para permitir mais opções para aplicativos. Há três tipos de recursos de alto nível no D3D12: confirmados, colocados e reservados.

-   Os recursos confirmados criam um recurso e um heap ao mesmo tempo. O heap é implícito e não pode ser acessado diretamente. O heap é dimensionado adequadamente para localizar o recurso inteiro dentro do heap.
-   Os recursos inseridos permitem o posicionamento de um recurso em um deslocamento diferente de zero em um heap. Os deslocamentos devem ser normalmente alinhados a 64 KB; Mas existem algumas exceções em ambas as direções. Os recursos de MSAA exigem um alinhamento de deslocamento de 4MB e o alinhamento de deslocamento de 4 KB está disponível para texturas pequenas. Os recursos inseridos não podem ser realocados ou remapeados para outro heap diretamente; Mas eles habilitam a realocação simples dos dados do recurso entre heaps. Depois de criar um novo recurso inserido em um heap diferente e copiar os dados do recurso, os novos descritores de recursos precisarão ser usados para o novo local de dados do recurso.
-   Os recursos reservados só estão disponíveis quando o adaptador dá suporte à camada 1 ou superior dos recursos do lado do ladrilho. Quando disponíveis, eles oferecem as técnicas de gerenciamento de residência mais avançadas disponíveis; Mas nem todos os adaptadores dão suporte a eles no momento. Eles habilitam o remapeamento de um recurso sem a necessidade de regeneração de descritores de recursos, residência de nível parcial de MIP e cenários de textura esparsa, etc. Nem todos os tipos de recursos têm suporte mesmo quando recursos reservados estão disponíveis, portanto, um Gerenciador de residência baseado em página totalmente geral ainda não é viável.

## <a name="residency-priorities"></a>Prioridades de residência

A atualização do Windows 10 para criadores permite que os desenvolvedores influenciem quais heaps e recursos serão preferidos para permanecerem residentes quando a pressão de memória exigir que alguns de seus recursos sejam rebaixados. Isso ajuda os desenvolvedores a criar aplicativos de melhor desempenho aproveitando o conhecimento de que o tempo de execução não pode inferir do uso da API. Espera-se que os desenvolvedores se tornem mais confortáveis e possam especificar prioridades à medida que eles fazem a transição do uso de recursos confirmados para reservado e recursos ao lado.

Aplicar essas prioridades deve ser mais fácil do que gerenciar dois orçamentos de memória dinâmica, rebaixando e promovendo manualmente os recursos bettween-los, já que os aplicativos já podem fazer isso. Portanto, o design da API de prioridade de residência é naturalmente refinado com prioridades padrão razoáveis atribuídas a cada heap ou recurso como seu criado. Para obter mais informações, consulte [**ID3D12Device1:: SetResidencyPriority**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device1-setresidencypriority) e a enumeração de [**prioridade de \_ residência \_ do D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_residency_priority) .

Com as prioridades, os desenvolvedores devem:

-   Aumente a prioridade de alguns heaps excepcionais para atenuar melhor o impacto no desempenho de que esses heaps estão sendo rebaixados antes ou com mais frequência do que os padrões de acesso natural exigiram. Espera-se que essa abordagem seja utilizada por aplicativos portados de APIs gráficas como Direct3D 11 ou OpenGL, que é o modelo de gerenciamento de recursos é significativamente diferente do Direct3D 12.
-   Substituir quase todas as prioridades de heap com o próprio esquema de bucketização do aplicativo, seja fixo, com base no conhecimento do programador de frequência de acesso ou dinâmico; um esquema fixo é mais simples de gerenciar do que um dinâmico, mas pode ser menos eficiente e exigir intevention de programador conforme os padrões de uso mudam no decorrer do desenvolvimento. Espera-se que essa abordagem seja utilizada por aplicativos criados com o gerenciamento de recursos do estilo Direct3D 12 em mente, como aqueles que usam a biblioteca de residência (especialmente esquemas dinâmicos).

### <a name="default-priority-algorithm"></a>Algoritmo de prioridade padrão

Um aplicativo não pode especificar prioridades úteis para qualquer heap que ele tente gerenciar sem primeiro se substanr o algoritmo de prioridade padrão. Isso ocorre porque o valor de atribuição de uma prioridade específica a um heap é derivado de sua prioridade relativa para outros heaps priorizados que conpetem para a mesma memória.

A estratégia escolhida para a geração de prioridades padrão é categorizar os heaps em dois buckets, favorecer (fornecendo prioridade mais alta para) os heaps que são considerados escritos com frequência pela GPU sobre heaps que não são.

O Bucket de alta prioridade contém heaps e recursos que são criados com sinalizadores que os identificam como destinos de renderização, buffers de estêncil de profundidade ou modos de exibição de acesso não ordenado (UAVs). Esses são os valores de prioridade atribuídos no intervalo a partir da **\_ prioridade de residência D3D12 \_ \_ alta**; para priorizar ainda mais entre esses recursos e heaps, os 16 bits mais baixos da prioridade são definidos como o tamanho do heap ou do recurso dividido por 10MB (saturação para 0xFFFF para heaps extremamente grandes). Essa priorização adicional favorece maiores heaps e recursos.

O Bucket de baixa prioridade contém todos os outros recursos e heaps, que recebem um valor de prioridade de **D3D12 de \_ prioridade de residência \_ \_ normal**. Não há tentativa de mais priorização entre esses heaps e recursos.

## <a name="programming-residency-management"></a>Gerenciamento de residência de programação

Aplicativos simples podem ser capazes de obter simplesmente criar recursos confirmados até que haja falhas de memória insuficiente. Após a falha, o aplicativo pode destruir outros recursos confirmados ou objetos de API para permitir que mais novas criações de recursos tenham êxito. Mas, até mesmo aplicativos simples são altamente recomendáveis para observar alterações de orçamento negativo e destruir objetos de API não utilizados, aproximadamente uma vez por quadro.

A complexidade de um design de gerenciamento de residência será exibida ao tentar otimizar para arquiteturas de adaptador ou incorporar prioridades de residência. O orçamento e o gerenciamento discretos de dois pools de memória discreta serão mais complexos do que o gerenciamento de apenas um, e a atribuição de prioridades fixas em uma ampla escala poderá se tornar uma carga de manutenção se o uso de padrões evoluir. Estourar texturas na memória do sistema aumenta a complexidade, pois o recurso incorreto na memória do sistema pode afetar seriamente a taxa de quadros. Além disso, não há uma funcionalidade simples para ajudar a identificar os recursos que se beneficiariam da maior largura de banda de GPU ou tolerar uma menor largura de banda de GPU.

Designs ainda mais complicados consultarão os recursos do adaptador atual. Essas informações estão disponíveis em [**\_ \_ \_ \_ \_ \_ suporte ao endereço virtual da GPU de dados de recursos do D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_gpu_virtual_address_support), [**\_ \_ \_ arquitetura de dados**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_architecture)de recursos do D3D12, [**\_ \_ \_ camada de recursos do lado do D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_tiled_resources_tier)e [**\_ \_ \_ camada de heap de recurso do D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_heap_tier).

Várias partes de um aplicativo provavelmente aparecerão usando técnicas diferentes. Por exemplo, algumas texturas grandes e caminhos de código raramente exercitados podem usar recursos confirmados, enquanto muitas texturas podem ser designadas com uma propriedade de streaming e usar uma técnica de recurso inserido geral.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**ID3D12Heap**](/windows/desktop/api/d3d12/nn-d3d12-id3d12heap)
</dt> <dt>

[Gerenciamento de memória](memory-management.md)
</dt> </dl>

 

 