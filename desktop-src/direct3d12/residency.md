---
title: Residência
description: Um objeto é considerado residente quando é acessível pela GPU.
ms.assetid: 956F80D7-EEC8-4D88-B251-EE325614F31E
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 257af2526120df5509a38fcc0c81984aa53a954f8eed6a8ce9194fa2aadb020a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989447"
---
# <a name="residency"></a>Residência

Um objeto é considerado residente *quando* é acessível pela GPU.

-   [Orçamento de residência](#residency-budget)
-   [Recursos de heap](#heap-resources)
-   [Prioridades de residência](#residency-priorities)
    -   [Algoritmo de prioridade padrão](#default-priority-algorithm)
-   [Gerenciamento de residência de programação](#programming-residency-management)
-   [Tópicos relacionados](#related-topics)

## <a name="residency-budget"></a>Orçamento de residência

As GPUs ainda não são suportadas com falha de página, portanto, os aplicativos devem fazer commit de dados na memória física enquanto a GPU pode acessá-los. Esse processo é conhecido como "fazendo algo residente" e deve ser feito para memória física do sistema e memória de vídeo discreta física. Em D3D12, a maioria dos objetos de API encapsula alguma quantidade de memória acessível por GPU. Essa memória acessível por GPU se tornou residente durante a criação do objeto de API e foi despejada na destruição de objeto de API.

A quantidade de memória física disponível para o processo é conhecida como o orçamento de memória de vídeo. O orçamento pode flutuar de forma perceptível à medida que os processos em segundo plano acionam e agem; e flutuam drasticamente quando o usuário muda para outro aplicativo. O aplicativo pode ser notificado quando o orçamento muda e sonda o orçamento atual e a quantidade de memória consumida no momento. Se um aplicativo não permanecer dentro de seu orçamento, o processo será congelado intermitentemente para permitir que outros aplicativos sejam executados e/ou as APIs de criação retornarão falha. A interface [**IDXGIAdapter3**](/windows/desktop/api/dxgi1_4/nn-dxgi1_4-idxgiadapter3) fornece os métodos pertencentes a essa funcionalidade, em particular [**QueryVideoMemoryInfo**](/windows/desktop/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-queryvideomemoryinfo) e [**RegisterVideoMemoryBudgetChangeNotificationEvent**](/windows/desktop/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-registervideomemorybudgetchangenotificationevent).

Os aplicativos são incentivados a usar uma reserva para indicar a quantidade de memória que eles não podem ficar. O ideal é que as configurações de gráficos "baixas" especificadas pelo usuário, ou algo ainda menor, sejam o valor certo para essa reserva. Definir uma reserva nunca dará a um aplicativo um orçamento mais alto do que receberia normalmente. Em vez disso, as informações de reserva ajudam o kernel do sistema operacional a minimizar rapidamente o impacto de grandes situações de pressão de memória. Nem mesmo a reserva estará disponível para o aplicativo quando o aplicativo não for o aplicativo em primeiro plano.

## <a name="heap-resources"></a>Recursos de heap

Embora muitos objetos de API encapsulam alguma memória acessível por GPU, os heaps & recursos devem ser a maneira mais significativa como os aplicativos consomem e gerenciam a memória física. Um heap é a unidade de nível mais baixo para gerenciar a memória física, portanto, é bom ter alguma familiaridade com suas propriedades de residência.

-   Os heaps não podem ser parcialmente residentes, mas existem soluções alternativas com recursos reservados.
-   Os heaps devem ser orçados como parte de um pool específico. Os adaptadores UMA têm um pool, enquanto adaptadores discretos têm dois pools. Embora seja verdade que o kernel pode deslocar alguns heaps em adaptadores discretos da memória de vídeo para a memória do sistema, ele faz isso apenas como um último recurso extremo. Os aplicativos não devem depender do comportamento de orçamento acima do kernel e devem se concentrar no bom gerenciamento de orçamento.
-   Os heaps podem ser despejados da residência, o que permite que seu conteúdo seja pageado para o disco. Mas a destruição de heaps é uma técnica mais confiável para liberar a residência em todas as arquiteturas de adaptador. Em adaptadores em que o *campoMaxGPUVirtualAddressBitsPerProcess* de [**D3D12 \_ FEATURE DATA \_ \_ GPU VIRTUAL ADDRESS \_ \_ \_ SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_gpu_virtual_address_support) está próximo ao tamanho do [**orçamento,**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-evict) a reação não recuperará a residência de forma confiável.
-   A criação do heap pode ser lenta; mas é otimizado para processamento de thread em segundo plano. É recomendável criar heaps em threads em segundo plano para evitar falhas no thread de renderização. No D3D12, vários threads podem chamar com segurança rotinas de criação simultaneamente.

D3D12 introduz mais flexibilidade e ortogonalidade em seu modelo de recurso para habilitar mais opções para aplicativos. Há três tipos de alto nível de recursos em D3D12: confirmado, colocado e reservado.

-   Os recursos confirmados criam um recurso e um heap ao mesmo tempo. O heap é implícito e não pode ser acessado diretamente. O heap é dimensionado adequadamente para localizar todo o recurso dentro do heap.
-   Os recursos colocados permitem o posicionamento de um recurso em um deslocamento não zero dentro de um heap. Os deslocamentos normalmente devem ser alinhados a 64KB; mas algumas exceções existem em ambas as direções. Os recursos MSAA exigem alinhamento de deslocamento de 4 MB e o alinhamento de deslocamento de 4KB está disponível para texturas pequenas. Os recursos colocados não podem ser realocados ou remapped para outro heap diretamente; mas eles habilitam a realocação simples dos dados de recurso entre heaps. Depois de criar um novo recurso colocado em um heap diferente e copiar os dados do recurso, novos descritores de recursos terão que ser usados para o novo local de dados do recurso.
-   Os recursos reservados só estão disponíveis quando o adaptador dá suporte à camada de recursos lado a lado 1 ou superior. Quando disponíveis, eles oferecem as técnicas de gerenciamento de residência mais avançadas disponíveis; mas nem todos os adaptadores atualmente são suportados por eles. Eles habilitam o remapeamento de um recurso sem a necessidade de regeneração de descritores de recursos, residência parcial no nível da mip, cenários esparsos de textura etc. Nem todos os tipos de recursos têm suporte mesmo quando recursos reservados estão disponíveis, portanto, um gerenciador de residência totalmente geral baseado em página ainda não é viável.

## <a name="residency-priorities"></a>Prioridades de residência

O Atualização do Windows 10 para Criadores permite que os desenvolvedores influenciam quais heaps e recursos serão preferenciais a permanecerem residentes quando a pressão de memória exigir que alguns de seus recursos sejam rebaixados. Isso ajuda os desenvolvedores a criar aplicativos com melhor desempenho aproveitando o conhecimento de que o runtime não pode inferir o uso da API. Espera-se que os desenvolvedores se tornem mais confortável e capazes de especificar prioridades à medida que eles fazem a transição do uso de recursos confirmados para recursos reserevados e lado a lado.

Aplicar essas prioridades deve ser mais fácil do que gerenciar dois orçamentos dinâmicos de memória, rebaixando e promovendo manualmente os recursos, pois os aplicativos já podem fazer isso. Portanto, o design da API de prioridade de residência é naturalmente desaloqueado com prioridades padrão razoáveis atribuídas a cada heap ou recurso conforme sua criação. Para obter mais informações, consulte [**ID3D12Device1::SetResidencyPriority**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device1-setresidencypriority) e a enumeração [**D3D12 \_ RESIDENCY \_ PRIORITY.**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_residency_priority)

Com prioridades, os desenvolvedores devem:

-   Aumente a prioridade de alguns heaps excepcionais para atenuar melhor o impacto de desempenho experiente desses heaps que estão sendo rebaixados mais cedo ou mais frequentemente do que seus padrões de acesso natural exigiriam. Espera-se que essa abordagem seja aproveitada por aplicativos portados de APIs gráficas, como Direct3D 11 ou OpenGL, que é um modelo de gerenciamento de recursos significativamente diferente do Direct3D 12.
-   Substitua quase todas as prioridades de heap pelo próprio esquema de bucketization do aplicativo, fixo, com base no conhecimento do programador sobre a frequência de acesso ou dinâmico; um esquema fixo é mais simples de gerenciar do que um dinâmico, mas pode ser menos eficaz e exigir a intevenção do programador à medida que os padrões de uso mudam ao longo do desenvolvimento. Espera-se que essa abordagem seja aproveitada por aplicativos que são construídos com o gerenciamento de recursos no estilo Direct3D 12 em mente, como aqueles que usam a biblioteca de residência (especialmente esquemas dinâmicos).

### <a name="default-priority-algorithm"></a>Algoritmo de prioridade padrão

Um aplicativo não pode especificar prioridades úteis para qualquer heap que ele tenta gerenciar sem primeiro fundamentar o algoritmo de prioridade padrão. Isso porque o valor da atribuição de uma prioridade específica a um heap é derivado de sua prioridade relativa a outros heaps priorizados que competem pela mesma memória.

A estratégia escolhida para gerar prioridades padrão é categorizar heaps em dois buckets, favorecendo (dando maior prioridade a) heaps que são presumidos como escritos com frequência pela GPU em heaps que não são.

O bucket de alta prioridade contém heaps e recursos criados com sinalizadores que os identificam como destinos de renderização, buffers de estêncil de profundidade ou UAVs (Exibições de Acesso Não Organizado). Esses valores de prioridade são atribuídos no intervalo começando em **D3D12 \_ RESIDENCY \_ PRIORITY \_ HIGH**; para priorizar ainda mais entre esses heaps e recursos, os 16 bits mais baixos da prioridade são definidos com o tamanho do heap ou recurso dividido por 10 MB (saturando-se de 0xFFFF para heaps extremamente grandes). Essa priorização adicional favorece heaps e recursos maiores.

O bucket de baixa prioridade contém todos os outros heaps e recursos, que são atribuídos a um valor de prioridade **de D3D12 \_ RESIDENCY \_ PRIORITY \_ NORMAL.** Nenhuma outra priorização entre esses heaps e recursos é tentada.

## <a name="programming-residency-management"></a>Gerenciamento de residência de programação

Aplicativos simples podem ser capazes de obter apenas criando recursos confirmados até sofrer falhas de memória inocessiva. Em caso de falha, o aplicativo pode destruir outros recursos ou objetos de API comprometidos para permitir que outras criações de recursos possam ser bem-sucedidas. No entanto, até mesmo aplicativos simples são altamente recomendados para observar alterações negativas no orçamento e destruir objetos de API não usadas aproximadamente uma vez por quadro.

A complexidade de um design de gerenciamento de residência vai crescer ao tentar otimizar para arquiteturas de adaptador ou incorporar prioridades de residência. Orçamento discreto e gerenciamento de dois pools de memória discreta serão mais complexos do que gerenciar apenas um e atribuir prioridades fixas em uma grande escala poderá se tornar uma carga de manutenção se os padrões de uso evoluirem. O estouro de texturas na memória do sistema adiciona mais complexidade, pois o recurso errado na memória do sistema pode afetar gravemente a taxa de quadros. Além disso, não há nenhuma funcionalidade simples para ajudar a identificar os recursos que se beneficiariam de largura de banda de GPU mais alta ou tolerar largura de banda de GPU menor.

Designs ainda mais complicados consultarão os recursos do adaptador atual. Essas informações estão disponíveis em [**D3D12 FEATURE \_ \_ DATA \_ GPU VIRTUAL ADDRESS \_ \_ \_ SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_gpu_virtual_address_support), [**D3D12 \_ FEATURE DATA \_ \_ ARCHITECTURE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_architecture), [**D3D12 \_ \_ TILED RESOURCES \_ TIER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_tiled_resources_tier)e [**D3D12 \_ RESOURCE HEAP \_ \_ TIER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_heap_tier).

Várias partes de um aplicativo provavelmente acabarão usando técnicas diferentes. Por exemplo, algumas texturas grandes e caminhos de código raramente exercícios podem usar recursos confirmados, enquanto muitas texturas podem ser designadas com uma propriedade de streaming e usar uma técnica geral de recurso colocado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**ID3D12Heap**](/windows/desktop/api/d3d12/nn-d3d12-id3d12heap)
</dt> <dt>

[Gerenciamento de memória](memory-management.md)
</dt> </dl>

 

 