---
title: Práticas recomendadas de gerenciamento de recursos
description: Este artigo aborda as práticas recomendadas para lidar com recursos em geral, como os recursos gerenciados e não gerenciados se comportam e fornece alguns detalhes sobre como os recursos normalmente são tratados pelo runtime e pelos drivers.
ms.assetid: 265ae0b2-f268-a4a4-551e-9d3dae886517
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bacf57c33ef765596ffa660ba884708ee000dd370c90edd3fcd158a9c526a7ac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119213207"
---
# <a name="resource-management-best-practices"></a>Práticas recomendadas de gerenciamento de recursos

As texturas gerenciadas, também conhecidas como gerenciamento automático de textura, estão disponíveis no DirectX desde a versão 6, com várias revisões e aprimoramentos feitos nas versões subsequentes. A partir do lançamento da API do Direct3D 9, o gerenciamento automático de recursos inclui suporte para texturas, buffers de vértice e buffers de índice, tudo isso com uma interface compartilhada consistente. Usando o gerenciador de recursos do Direct3D, os aplicativos podem simplificar muito a manipulação de situações de dispositivo perdido e podem contar com o sistema para lidar com uma quantidade razoável de excesso de compromisso de recursos de memória de vídeo.

Às vezes, os desenvolvedores têm dificuldades para usar recursos gerenciados, em parte devido à natureza abstrata do sistema. Embora muitos cenários comuns para recursos sejam uma boa maneira para recursos gerenciados, alguns casos têm um desempenho melhor ao usar recursos não gerenciados. Este artigo aborda as práticas recomendadas para lidar com recursos em geral, como os recursos gerenciados e não gerenciados se comportam e fornece alguns detalhes sobre como os recursos normalmente são tratados pelo runtime e pelos drivers.

Este artigo aborda estes conceitos:

-   [Memória de vídeo](#video-memory)
-   [Recursos gerenciados](#managed-resources)
-   [Recursos gerenciados por driver](#driver-managed-resources)
-   [Recursos padrão](#default-resources)
    -   [Usando recursos gerenciados e padrão](#using-both-managed-and-default-resources)
    -   [Recursos padrão dinâmicos](#dynamic-default-resources)
-   [Recursos de memória do sistema](#system-memory-resources)
-   [Geral Recomendações](#general-recommendations)
-   [Tópicos relacionados](#related-topics)

## <a name="video-memory"></a>Memória de vídeo

Para que o sistema de vídeo use um recurso, ele deve estar localizado na memória acessível para a GPU. A memória de vídeo local fornece o melhor desempenho para a GPU e determinados recursos (como destinos de renderização e buffers de profundidade/estêncil) devem estar localizados na memória de vídeo local. Com o advento do AGP, a GPU também pode acessar uma parte da memória do sistema diretamente. Essa área de memória, conhecida como abertura do AGP, é conhecida como memória de vídeo não local e não está disponível para outras finalidades. A memória de vídeo não local pode ser lida e escrita pela CPU, que normalmente não tem acesso de alto desempenho à memória de vídeo local e, portanto, é ideal para uso como um recurso de memória compartilhada. Uma coisa importante a ser lembrada sobre a memória AGP é que ela, como a memória de vídeo local, é invalidada em situações de dispositivo perdido e os ativos persistentes localizados lá devem ser restaurados.

**Figura 1. Relação entre GPU, CPU, RAM de vídeo e RAM do sistema**

![relação da GPU, cpu, ram de vídeo e ram do sistema](images/managingresources1.gif)

Algumas soluções de vídeo integradas usam uma UMA (arquitetura de memória unificada), em que a memória principal pode ser abordada por todos os componentes dos sistemas. O Direct3D dá suporte a UMA sem a necessidade de nenhuma alteração no aplicativo, utilizando as mesmas dicas que para configurações de memória de vídeo local. Para esses sistemas, os recursos estão sempre localizados na memória do sistema e o driver é responsável por garantir que os recursos funcionem da mesma forma que em uma arquitetura mais tradicional, aproveitando as propriedades de UMA e qualquer comportamento específico da implementação de hardware.

**Figura 2. GPU e CPU têm acesso igual à RAM do sistema em uma arquitetura de memória unificada**

![gpu e CPU têm acesso igual à RAM do sistema em uma arquitetura de memória unificada](images/managingresources2.gif)

## <a name="managed-resources"></a>Recursos gerenciados

A maioria dos seus recursos deve ser criada como recursos gerenciados no POOL \_ GERENCIADO. Todos os recursos serão criados na memória do sistema e copiados conforme necessário na memória de vídeo. As situações de dispositivo perdido serão tratadas automaticamente da cópia de memória do sistema. Como nem todos os recursos gerenciados são necessários para caber na memória de vídeo de uma só vez, você pode sobrecarrar a memória, em que um conjunto menor de recursos de trabalho de memória de vídeo é tudo o que é necessário para renderizar em qualquer quadro determinado. Observe que é provável que a maioria dessa memória do sistema de armazenamento de backup seja enviada para o disco ao longo do tempo, por isso a operação de redefinição pode ser lenta devido à necessidade de reajustar esses dados para restaurar a memória de vídeo perdida.

O runtime mantém um timestamp pela última vez em que um recurso é usado e, quando uma alocação de memória de vídeo falhar para carregar um recurso gerenciado necessário, ele liberará recursos com base nesse timestamp de maneira LRU. O uso [**de SetPriority**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3dresource9-setpriority) tem precedência sobre o timestamp, portanto, os recursos mais usados devem ser definidos como um valor de prioridade mais alto. O Direct3D 9.0 tem informações limitadas sobre a memória de vídeo gerenciada pelo driver, portanto, o runtime pode precisar ressalar vários recursos para criar uma região grande o suficiente para que a alocação seja bem-sucedida. As prioridades adequadas podem ajudar a eliminar situações em que algo é despejado e, em seguida, é necessário novamente logo em seguida. O aplicativo também pode chamar [**EvictManagedResources**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-evictmanagedresources) para forçar a remoção de todos os recursos gerenciados. Novamente, essa pode ser uma operação demorada para recarregar todos os recursos necessários para o próximo quadro, mas é muito útil para transições de nível em que o conjunto de trabalho muda significativamente e para remover a fragmentação de memória de vídeo.

Uma contagem de quadros também é mantida para permitir que o runtime detecte se o recurso que ele acabou de optar por ressalar foi usado no início do quadro atual, o que implica uma situação de desapropriação em que mais recursos estão em uso em um único quadro do que caberão na memória de vídeo. Isso dispara a política de substituição para alternar para um estilo MRU em vez de LRU para o restante do quadro, pois isso tende a ter um desempenho ligeiramente melhor sob essas condições. Esse comportamento de redução afetará significativamente o desempenho da renderização. Observe que a noção de quadro atual está vinculada a [**EndScene,**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-endscene)portanto, qualquer aplicativo que usa recursos gerenciados precisa fazer chamadas regulares para esse método.

Os desenvolvedores que buscam encontrar mais informações sobre como os recursos gerenciados estão se comportando em seu aplicativo podem usar a consulta de evento RESOURCEMANAGER por meio da interface [**IDirect3DQuery9.**](/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dquery9) Isso só funciona ao usar os runtimes de depuração, portanto, essas informações não podem depender do aplicativo, mas fornece detalhes detalhados sobre os recursos gerenciados pelo runtime.

Embora entenda como o gerenciador de recursos funciona pode ajudar ao ajustar e depurar seus aplicativos, é importante não ligar seu aplicativo muito fortemente aos detalhes de implementação do runtime ou drivers atuais. As revisões do driver ou alterações no hardware podem alterar significativamente o comportamento e versões futuras do Direct3D terão um gerenciamento de recursos significativamente aprimorado e sofisticado.

## <a name="driver-managed-resources"></a>Driver-Managed recursos

Os drivers Direct3D são livres para implementar a funcionalidade de texturas gerenciadas pelo driver, indicada por D3DCAPS2 CANMANAGERESOURCE, que permite ao driver lidar com o gerenciamento de recursos em vez do \_ runtime. Para o driver (raro) que implementa esse recurso, o comportamento exato do gerenciador de recursos do driver pode variar muito e você deve entrar em contato com o fornecedor do driver para obter detalhes sobre como isso funciona para sua implementação. Como alternativa, você pode garantir que o gerenciador de runtime seja sempre usado especificando D3DCREATE \_ DISABLE DRIVER MANAGEMENT ao criar o \_ \_ dispositivo.

## <a name="default-resources"></a>Recursos padrão

Embora os recursos gerenciados sejam simples, eficientes e fáceis de usar, há ocasiões em que o uso direto da memória de vídeo é preferencial ou até mesmo necessário. Esses recursos são criados na categoria POOL \_ DEFAULT. Fazer uso desses recursos causa complicações adicionais para seu aplicativo. O código é necessário para lidar com a situação de dispositivo perdido para todos os recursos PADRÃO do POOL e as considerações de desempenho devem ser levadas em conta ao copiar dados \_ para eles. A falha ao especificar USAGE \_ WRITEONLY ou tornar um destino de renderização bloqueável também pode impor penalidades de desempenho graves.

Chamar **Bloqueio** em um recurso PADRÃO DO POOL é mais provável que a GPU seja paralisada do que trabalhar com um recurso GERENCIADO DO POOL, a menos que use determinados sinalizadores \_ de \_ dica. Dependendo do local do recurso, o ponteiro retornado pode ser para um buffer de memória do sistema temporário ou pode ser um ponteiro diretamente na memória AGP. Se for um buffer de memória do sistema temporário, os dados precisarão ser transferidos para a memória de vídeo após a **chamada desbloquear.** Se o recurso de vídeo não for somente gravação, os dados deverão ser transferidos para o buffer temporário durante o **bloqueio**. Se for uma área de memória AGP, cópias temporárias serão evitadas, mas o comportamento de cache necessário pode resultar em desempenho lento.

É preciso ter cuidado para gravar uma linha de cache completa de dados em qualquer ponteiro para a memória de abertura do AGP para evitar a penalidade de assinatura de gravação, o que induz um ciclo de leitura/gravação e o acesso sequencial da área de memória é preferencial. Se seu aplicativo precisar fazer acesso aleatório aos dados durante a criação e você não quiser usar um recurso gerenciado para o buffer, deverá trabalhar com uma cópia de memória do sistema. Depois que os dados foram criados, você pode transmitir o resultado para a memória de recurso bloqueada para evitar pagar uma penalidade alta para a operação de combinação de gravação de cache.

O sinalizador LOCK NOOVERWRITE pode ser usado para anexar dados de maneira eficiente para alguns recursos, mas, idealmente, várias chamadas de Bloqueio e Desbloqueio para o mesmo recurso podem \_ ser evitadas.   Fazer o uso adequado dos vários sinalizadores de bloqueio é importante para o desempenho ideal, assim como o uso de um padrão amigável de cache de acesso a dados ao preencher a memória bloqueada.

### <a name="using-both-managed-and-default-resources"></a>Usando recursos gerenciados e padrão

Combinar alocações de recursos gerenciados e PADRÃO DO POOL pode causar fragmentação de memória de vídeo e confundir a exibição do runtime da memória de vídeo \_ disponível para recursos gerenciados. O ideal é criar todos os recursos PADRÃO do POOL antes de usar os recursos GERENCIADOS do POOL ou usar a chamada \_ \_ [**EvictManagedResources**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-evictmanagedresources) antes de alocar recursos não gerenciados. Lembre-se de que todas as alocações feitas do POOL DEFAULT que residem na memória de vídeo empatam a memória durante a vida útil do recurso que não está disponível para uso pelo gerenciador de recursos ou para \_ qualquer outra finalidade.

Observe que, ao contrário das versões anteriores do Direct3D, o runtime da versão 9 automaticamente ressalva alguns recursos gerenciados antes de abrir mão de uma alocação de recursos não gerenciada com falha por falta de memória de vídeo, mas isso pode potencialmente criar fragmentação adicional e até mesmo forçar um recurso em um local abaixo do ideal (por exemplo, ter uma textura estática na memória de vídeo não local). Novamente, é melhor alocar todos os recursos não gerenciados necessários antes e antes de usar os recursos gerenciados.

### <a name="dynamic-default-resources"></a>Recursos padrão dinâmicos

Os dados gerados e atualizados em uma alta frequência não precisam do armazenamento de back-back, pois todas as informações serão criadas novamente ao restaurar o dispositivo. Esses dados normalmente são criados melhor em POOL DEFAULT, especificando a dica USAGE DYNAMIC, para que o driver possa tomar decisões de otimização ao colocar o recurso, sabendo que eles serão atualizados com \_ \_ frequência. Normalmente, isso significa colocar o recurso na memória de vídeo não local e, portanto, geralmente é muito mais lento para a GPU acessar do que a memória de vídeo local. Para arquiteturas UMA, o driver pode escolher um posicionamento específico para recursos dinâmicos para otimizar o acesso de gravação da CPU.

Esse uso é típico para soluções de criação de software e sistemas de partícula baseados em CPU preenchendo buffers de vértice/índice, e o sinalizador LOCK DISCARD garantirá que as paradas não sejam criadas nos casos em que o recurso ainda está em uso do quadro \_ anterior. Usar um recurso gerenciado, nesse caso, atualizaria um buffer de memória do sistema, que seria copiado para a memória de vídeo e, em seguida, usado apenas para um quadro ou dois antes de ser substituído. Para sistemas com memória de vídeo não local, a cópia extra é eliminada pelo uso adequado desse padrão dinâmico.

As texturas padrão não podem ser bloqueadas e só podem ser atualizadas por meio [**de UpdateSurface**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-updatesurface) ou [**UpdateTexture.**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-updatetexture) Alguns sistemas suportam texturas dinâmicas, que podem ser bloqueadas e usam o padrão LOCK DISCARD, mas um bit de \_ funcionalidades (D3DCAPS2 DYNAMICTEXTURES) deve ser verificado antes de usar esses \_ recursos. Para texturas altamente dinâmicas (vídeo ou procedimento), seu aplicativo pode criar recursos POOL DEFAULT e \_ POOL SYSTEMMEM correspondentes e manipular atualizações de memória de vídeo usando \_ **UpdateTexture**. Para atualizações altamente frequentes e parciais, o **paradigma UpdateTexture** provavelmente é a melhor opção.

Tão útil quanto os recursos dinâmicos podem ser, tenha cuidado ao projetar sistemas que dependem muito do envio dinâmico. Os recursos estáticos devem ser colocados no POOL GERENCIADO para garantir a boa utilização da memória de vídeo local e para fazer uso mais eficiente da largura de banda de memória principal e do barramento \_ limitado. Para recursos semiestticos, você pode descobrir que o custo de um carregamento ocasional na memória de vídeo local é muito menor do que o tráfego constante de barramento gerado tornando-os dinâmicos.

## <a name="system-memory-resources"></a>Recursos de memória do sistema

Os recursos também podem ser criados no POOL \_ SYSTEMMEM. Embora não possam ser usados pelo pipeline de gráficos, eles podem ser usados como fontes para atualizar recursos PADRÃO do POOL usando \_ [**UpdateSurface**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-updatesurface) ou [**UpdateTexture.**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-updatetexture) Seu comportamento de bloqueio é simples, embora as paradas possam ocorrer se elas estão em uso por um dos métodos mencionados anteriormente.

Embora eles residam na memória do sistema, os recursos SYSTEMMEM do POOL são limitados aos mesmos formatos e funcionalidades (como tamanho máximo) com suporte \_ pelo driver de dispositivo. O tipo de recurso POOL SCRATCH é outra forma de recurso de memória do sistema que pode utilizar todos os formatos e funcionalidades com suporte pelo runtime, mas não pode ser acessado \_ pelo dispositivo. Os recursos de rascunho são destinados principalmente para uso por ferramentas de conteúdo.

**Figura 3. Recursos de memória em RAM de vídeo, abertura AGP e RAM do sistema**

![recursos de memória em ram de vídeo, aperture agp e ram do sistema](images/managingresources3.gif)

## <a name="general-recommendations"></a>Recomendações gerais

Obter os detalhes de implementação técnica do gerenciamento de recursos corretos vai muito longe para atingir suas metas de desempenho para seu aplicativo. Planejar como os recursos são apresentados ao Direct3D e o design arquitetônico sobre como carregar os dados em tempo hábil é uma tarefa mais complicada. Recomendamos várias práticas recomendadas ao tomar essas decisões para seu aplicativo:

-   Pré-processe todos os seus recursos. Depender de uma conversão cara de tempo de carregamento e otimização para seus recursos é conveniente durante o desenvolvimento, mas fazer isso coloca uma grande carga de desempenho nos computadores dos usuários. Os recursos pré-processados são mais rápidos de carregar, mais rápidos de usar e dão a você a opção de fazer um trabalho fora de linha sofisticado.
-   Evite criar muitos recursos por quadro. As interações de driver necessárias podem serializar a CPU e a GPU, e as operações envolvidas são pesadas, pois geralmente exigem transições de kernel. Spreading creation over several frames or reuse resources without creating/releasing them. Idealmente, você deve aguardar vários quadros antes de bloquear ou liberar recursos que foram usados recentemente para renderizar.
-   No final do quadro, desabine todos os canais de recursos (ou seja, fontes de fluxo, estágios de textura e índices atuais). Isso garantirá que as referências pendentes aos recursos sejam removidas antes de fazer com que o gerenciador de recursos mantenha os recursos residentes que, na verdade, não estão mais em uso.
-   Para texturas, use formatos compactados (por exemplo, DXTn) com mip-maps e considere usar um atlas de textura. Isso reduz consideravelmente os requisitos de largura de banda e pode reduzir o tamanho geral dos recursos, tornando-os mais eficientes.
-   Para geometria, use a geometria indexada, pois isso ajuda a compactar recursos de buffer de vértice, e o hardware de vídeo moderno é altamente otimizado em torno da reutilização de vértices. Ao fazer uso de sombreadores de vértice programáveis, você pode compactar as informações de vértice e expandi-la durante o processamento de vértice. Novamente, isso ajuda a reduzir os requisitos de largura de banda e torna os recursos de buffer de vértice mais eficientes.
-   Evite otimizar o gerenciamento de recursos em excesso. Futuras revisões de drivers, hardware e sistema operacional podem causar problemas de compatibilidade se o aplicativo estiver ajustado muito para uma combinação particularmente. Como a maioria dos aplicativos é vinculada à CPU, o gerenciamento caro baseado em CPU geralmente causa mais problemas de desempenho do que resolve.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gerenciando recursos](/windows/desktop/direct3d9/managing-resources)
</dt> <dt>

[Dispositivos perdidos](/windows/desktop/direct3d9/lost-devices)
</dt> <dt>

[Otimizações de desempenho](/windows/desktop/direct3d9/performance-optimizations)
</dt> <dt>

[Recursos de textura compactada](/windows/desktop/direct3d9/compressed-texture-resources)
</dt> <dt>

[Consultas](/windows/desktop/direct3d9/queries)
</dt> <dt>

[**D3DUSAGE**](/windows/desktop/direct3d9/d3dusage)
</dt> <dt>

[**D3DPOOL**](/windows/desktop/direct3d9/d3dpool)
</dt> <dt>

[D3DCREATE](/windows/desktop/direct3d9/d3dcreate)
</dt> </dl>

 

 