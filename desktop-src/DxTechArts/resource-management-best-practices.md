---
title: Práticas recomendadas de gerenciamento de recursos
description: Este artigo aborda as práticas recomendadas para lidar com recursos geralmente, como os recursos gerenciados e não gerenciados se comportam e fornece alguns detalhes sobre como os recursos são normalmente tratados pelo tempo de execução e pelos drivers.
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

As texturas gerenciadas, também conhecidas como gerenciamento automático de textura, estão disponíveis no DirectX desde a versão 6, com várias revisões e aprimoramentos feitos nas versões subsequentes. No lançamento da API do Direct3D 9, o gerenciamento automático de recursos inclui suporte para texturas, buffers de vértices e buffers de índice, tudo com uma interface compartilhada consistente. Usando o Direct3D Resource Manager, os aplicativos podem simplificar bastante a manipulação de situações de dispositivo perdido e podem contar com o sistema para lidar com uma quantidade razoável de comprometimento excessivo dos recursos de memória de vídeo.

Os desenvolvedores às vezes têm dificuldades em usar recursos gerenciados, em parte devido à natureza abstrata do sistema. Embora muitos cenários comuns de recursos sejam uma boa opção para recursos gerenciados, alguns casos têm melhor desempenho ao usar recursos não gerenciados. Este artigo aborda as práticas recomendadas para lidar com recursos geralmente, como os recursos gerenciados e não gerenciados se comportam e fornece alguns detalhes sobre como os recursos são normalmente tratados pelo tempo de execução e pelos drivers.

Este artigo aborda estes conceitos:

-   [Memória de vídeo](#video-memory)
-   [Recursos gerenciados](#managed-resources)
-   [Recursos gerenciados por driver](#driver-managed-resources)
-   [Recursos padrão](#default-resources)
    -   [Usando recursos gerenciados e padrão](#using-both-managed-and-default-resources)
    -   [Recursos padrão dinâmicos](#dynamic-default-resources)
-   [Recursos de memória do sistema](#system-memory-resources)
-   [Recomendações geral](#general-recommendations)
-   [Tópicos relacionados](#related-topics)

## <a name="video-memory"></a>Memória de vídeo

Para que o sistema de vídeo Use um recurso, ele deve estar localizado na memória que está acessível para a GPU. A memória de vídeo local fornece o melhor desempenho para a GPU, e determinados recursos (como destinos de renderização e buffers de profundidade/estêncil) devem estar localizados em memória de vídeo local. Com o advento do AGP, a GPU também pode acessar uma parte da memória do sistema diretamente. Essa área de memória, conhecida como a abertura do AGP, é conhecida como memória de vídeo não local e não está disponível para outras finalidades. A memória de vídeo não local pode ser lida e gravada pela CPU, que normalmente não tem acesso de alto desempenho à memória de vídeo local e, portanto, é ideal para uso como um recurso de memória compartilhada. Um ponto importante a ser lembrado sobre a memória AGP é que, como a memória de vídeo local, é invalidado em situações de dispositivo perdido e ativos persistentes localizados nele devem ser restaurados.

**Figura 1. Relação da GPU, CPU, vídeo RAM e RAM do sistema**

![relação da GPU, CPU, vídeo RAM e RAM do sistema](images/managingresources1.gif)

Algumas soluções de vídeo integradas usam uma (arquitetura de memória unificada), em que a memória principal é endereçável por todos os componentes dos sistemas. O Direct3D dá suporte a uma, sem a necessidade de qualquer alteração no aplicativo, utilizando as mesmas dicas das configurações de memória de vídeo local. Para esses sistemas, os recursos estão sempre localizados na memória do sistema, e o driver é responsável por garantir que os recursos funcionem da mesma forma que em uma arquitetura mais tradicional, aproveitando as propriedades de uma e qualquer comportamento específico da implementação de hardware.

**Figura 2. GPU e CPU têm acesso igual à RAM do sistema em uma arquitetura de memória unificada**

![GPU e CPU têm acesso igual à RAM do sistema em uma arquitetura de memória unificada](images/managingresources2.gif)

## <a name="managed-resources"></a>Recursos gerenciados

A maioria de seus recursos deve ser criada como recursos gerenciados no POOL \_ gerenciado. Todos os seus recursos serão criados na memória do sistema e, em seguida, copiados conforme necessário na memória de vídeo. As situações de dispositivo perdido serão tratadas automaticamente da cópia de memória do sistema. Como nem todos os recursos gerenciados são necessários para se ajustar à memória de vídeo de uma só vez, é possível confirmar excessivamente a memória em que um conjunto de recursos de trabalho de memória de vídeo menor é tudo o que é necessário para renderizar em qualquer determinado quadro. Observe que é provável que a maioria dessa memória do sistema de armazenamento de backup seja paginada para o disco ao longo do tempo, motivo pelo qual a operação de redefinição pode ser lenta devido à necessidade de paginar esses dados de volta para restaurar a memória de vídeo perdida.

O tempo de execução mantém um carimbo de data/hora na última vez em que um recurso é usado e quando uma alocação de memória de vídeo falha para carregar um recurso gerenciado necessário, ele libera recursos com base nesse carimbo de data/hora de maneira LRU. O uso [**de**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3dresource9-setpriority) settevence tem precedência sobre o carimbo de data/hora, de modo que os recursos mais usados devem ser definidos com um valor de prioridade mais alto. O Direct3D 9,0 tem informações limitadas sobre a memória de vídeo gerenciada pelo driver, de modo que o tempo de execução pode precisar remover vários recursos para criar uma região grande o suficiente para que a alocação tenha sucesso. As prioridades adequadas podem ajudar a eliminar situações em que algo é removido e, em seguida, é necessário novamente logo depois disso. O aplicativo também pode chamar [**EvictManagedResources**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-evictmanagedresources) para forçar a remoção de todos os recursos gerenciados. Novamente, essa pode ser uma operação demorada para recarregar todos os recursos necessários para o próximo quadro, mas é muito útil para transições de nível em que o conjunto de trabalho muda significativamente e para remover a fragmentação da memória de vídeo.

Um número de quadros também é mantido para permitir que o tempo de execução detecte se o recurso escolhido para remoção foi usado no início do quadro atual, o que implica uma situação ultrapaginação em que mais recursos estão em uso em um único quadro do que se ajustará à memória de vídeo. Isso dispara a política de substituição para mudar para uma forma MRU em vez de LRU para o restante do quadro, pois isso tende a executar um pouco melhor sob tais condições. Esse comportamento de ultrapaginação afetará significativamente o desempenho de renderização. Observe que a noção do quadro atual está vinculada ao [**EndScene**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-endscene), de modo que qualquer aplicativo que faça uso de recursos gerenciados precisa fazer chamadas regulares para esse método.

Os desenvolvedores que buscam encontrar mais informações sobre como os recursos gerenciados estão se comportando em seus aplicativos podem usar a consulta de evento RESOURCEMANAGER por meio da interface [**IDirect3DQuery9**](/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dquery9) . Isso só funciona ao usar os tempos de execução de depuração, portanto, essas informações não podem ser dependentes pelo aplicativo, mas fornecem detalhes aprofundados sobre os recursos gerenciados pelo tempo de execução.

Embora entender como o Gerenciador de recursos funciona pode ajudar ao ajustar e depurar seus aplicativos, é importante não vincular seu aplicativo muito bem aos detalhes da implementação do tempo de execução atual ou dos drivers. As revisões do driver ou as alterações no hardware podem alterar significativamente o comportamento, e as versões futuras do Direct3D terão um gerenciamento de recursos consideravelmente melhorado e sofisticado.

## <a name="driver-managed-resources"></a>Driver-Managed recursos

Os drivers do Direct3D são gratuitos para implementar o recurso de texturas gerenciadas por Driver, indicado por D3DCAPS2 \_ CANMANAGERESOURCE, que permite que o driver manipule o gerenciamento de recursos em vez do tempo de execução. Para o driver (raro) que implementa esse recurso, o comportamento exato do Gerenciador de recursos do driver pode variar muito e você deve entrar em contato com o fornecedor do driver para obter detalhes sobre como isso funciona para sua implementação. Como alternativa, você pode garantir que o Gerenciador de tempo de execução sempre seja usado, especificando D3DCREATE \_ desabilitar \_ \_ o gerenciamento de driver ao criar o dispositivo.

## <a name="default-resources"></a>Recursos padrão

Embora os recursos gerenciados sejam simples, eficientes e fáceis de usar, há ocasiões em que usar a memória de vídeo diretamente é preferencial ou até mesmo necessário. Esses recursos são criados na \_ categoria padrão do pool. Fazer uso desses recursos causa complicações adicionais para seu aplicativo. O código é necessário para lidar com a situação de dispositivo perdido para todos os \_ recursos padrão do pool, e as considerações de desempenho devem ser levadas em conta ao copiar dados neles. Falha ao especificar \_ o uso de WRITEONLY ou fazer um bloqueáveis de destino de renderização também pode impor sérias penalidades de desempenho.

A chamada de **bloqueio** em um recurso de pool \_ padrão é mais provável que a GPU seja interrompida do que trabalhar com um \_ recurso gerenciado por pool, a menos que use determinados sinalizadores de dica. Dependendo do local do recurso, o ponteiro retornado poderia ser um buffer de memória do sistema temporário ou pode ser um ponteiro diretamente na memória AGP. Se for um buffer de memória do sistema temporário, os dados precisarão ser transferidos para a memória de vídeo após a chamada de **desbloqueio** . Se o recurso de vídeo não for somente gravação, os dados precisarão ser transferidos para o buffer temporário durante o **bloqueio**. Se for uma área de memória AGP, as cópias temporárias serão evitadas, mas o comportamento de cache necessário poderá resultar em um desempenho lento.

Deve-se tomar cuidado para gravar uma linha de cache cheia de dados em qualquer ponteiro para a memória de abertura AGP para evitar a penalidade de gravação, o que induzi um ciclo de leitura/gravação, e o acesso sequencial da área de memória é preferencial. Se seu aplicativo precisar fazer acesso aleatório aos dados durante a criação e você não quiser usar um recurso gerenciado para o buffer, você deverá trabalhar com uma cópia de memória do sistema em vez disso. Depois que os dados tiverem sido criados, você poderá transmitir o resultado para a memória de recursos bloqueados para evitar o pagamento de uma alta penalidade para a operação de combinação de gravação de cache.

O \_ sinalizador bloquear NoOverwrite pode ser usado para acrescentar dados de maneira eficiente para alguns recursos, mas, teoricamente, várias chamadas de **bloqueio** e **desbloqueio** para o mesmo recurso podem ser evitadas. Fazer uso adequado dos vários sinalizadores de bloqueio é importante para o desempenho ideal, assim como o uso de um padrão amigável de acesso a dados para o cache ao preencher a memória bloqueada.

### <a name="using-both-managed-and-default-resources"></a>Usando recursos gerenciados e padrão

A combinação de alocações de recursos gerenciados e padrão de POOL \_ pode causar a fragmentação da memória de vídeo e confundir a exibição do tempo de execução da memória de vídeo disponível para recursos gerenciados. Idealmente, você deve criar todos os \_ recursos padrão de pool antes de usar \_ os recursos gerenciados por pool ou fazer uso da chamada [**EvictManagedResources**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-evictmanagedresources) antes de alocar recursos não gerenciados. Lembre-se de que todas as alocações feitas do padrão de POOL \_ que residem na memória de vídeo vinculam a memória durante a vida útil do recurso que está indisponível para uso pelo Gerenciador de recursos ou por qualquer outra finalidade.

Observe que, diferentemente das versões anteriores do Direct3D, o tempo de execução da versão 9 remove automaticamente alguns recursos gerenciados antes de desistir de uma alocação de recursos não gerenciado com falha para uma falta de memória de vídeo, mas isso pode potencialmente criar fragmentação adicional e até mesmo forçar um recurso em um local abaixo do ideal (por exemplo, ter uma textura estática na memória de vídeo não local) Novamente, é melhor alocar todos os recursos não gerenciados necessários antecipadamente e antes de usar qualquer recurso gerenciado.

### <a name="dynamic-default-resources"></a>Recursos padrão dinâmicos

Os dados gerados e atualizados a uma alta frequência não têm necessidade de armazenamento de backup, pois todas as informações serão recriadas ao restaurar o dispositivo. Esses dados normalmente são mais bem criados no \_ padrão de pool, especificando a \_ dica dinâmica de uso, para que o driver possa tomar decisões de otimização ao colocar o recurso, sabendo que ele será atualizado com frequência. Isso normalmente significa colocar o recurso em memória de vídeo não local e, portanto, normalmente é muito mais lento para a GPU acessar do que a memória de vídeo local. Para arquiteturas de uma, o driver pode escolher um posicionamento específico para que os recursos dinâmicos otimizem para o acesso de gravação da CPU.

Esse uso é típico para soluções de revestimento de software e sistemas de partículas baseados em CPU que preenchem buffers de vértice/índice e o sinalizador de descarte de bloqueio \_ garantirá que as vagas não sejam criadas nos casos em que o recurso ainda esteja em uso no quadro anterior. O uso de um recurso gerenciado, nesse caso, atualizaria um buffer de memória do sistema, que seria então copiado para memória de vídeo e, em seguida, usado apenas para um ou dois quadros antes de ser substituído. Para sistemas com memória de vídeo não local, a cópia extra é eliminada pelo uso adequado desse padrão dinâmico.

As texturas padrão não podem ser bloqueadas e só podem ser atualizadas por meio de [**UpdateSurface**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-updatesurface) ou [**UpdateTexture**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-updatetexture). Alguns sistemas dão suporte a texturas dinâmicas, que podem ser bloqueadas e usam o padrão de descarte de bloqueio \_ , mas um bit de recursos (D3DCAPS2 \_ DYNAMICTEXTURES) deve ser verificado antes de usar esses recursos. Para texturas altamente dinâmicas (vídeo ou procedimento), o aplicativo poderia criar recursos de POOL e de SYSTEMMEM de pool correspondentes \_ \_ e manipular atualizações de memória de vídeo usando o **UpdateTexture**. Para atualizações muito frequentes e parciais, o paradigma **UpdateTexture** é provavelmente a melhor opção.

Assim como os recursos dinâmicos podem ser, tenha cuidado ao projetar sistemas que dependam muito do envio dinâmico. Os recursos estáticos devem ser colocados no POOL \_ gerenciado para garantir uma boa utilização da memória de vídeo local e fazer uso mais eficiente de barramento limitado e largura de banda de memória principal. Para recursos que são semiestáticos, você pode descobrir que o custo de um upload ocasional para a memória de vídeo local é muito menor do que o tráfego de barramento constante gerado, tornando-os dinâmicos.

## <a name="system-memory-resources"></a>Recursos de memória do sistema

Os recursos também podem ser criados no POOL \_ SYSTEMMEM. Embora eles não possam ser usados pelo pipeline de gráficos, eles podem ser usados como fontes para atualizar \_ os recursos padrão do pool usando [**UpdateSurface**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-updatesurface) ou [**UpdateTexture**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-updatetexture). Seu comportamento de bloqueio é simples, embora as paralisações possam ocorrer se estiverem em uso por um dos métodos mencionados anteriormente.

Embora eles residam na memória do sistema, \_ os recursos do pool SYSTEMMEM são limitados aos mesmos formatos e capacidades (como o tamanho máximo) com suporte do driver de dispositivo. O \_ tipo de recurso Scratch do pool é outra forma de recurso de memória do sistema que pode utilizar todos os formatos e funcionalidades com suporte no tempo de execução, mas não pode ser acessado pelo dispositivo. Os recursos transitórios são destinados principalmente para uso por ferramentas de conteúdo.

**Figura 3. Recursos de memória em RAM de vídeo, abertura de AGP e RAM do sistema**

![recursos de memória em RAM de vídeo, abertura de AGP e RAM do sistema](images/managingresources3.gif)

## <a name="general-recommendations"></a>Recomendações gerais

Obter os detalhes da implementação técnica do gerenciamento de recursos correto será um longo caminho para atingir suas metas de desempenho para seu aplicativo. Planejar como os recursos são apresentados ao Direct3D e o design arquitetônico em relação à obtenção dos dados carregados em tempo hábil é uma tarefa mais complicada. Recomendamos várias práticas recomendadas ao tomar essas decisões para seu aplicativo:

-   Pré-processar todos os seus recursos. Depender da conversão e da otimização do tempo de carga dispendioso para seus recursos é conveniente durante o desenvolvimento, mas isso coloca uma grande carga de desempenho nos computadores dos usuários. Os recursos previamente processados são mais rápidos de carregar, mais rápidos de usar e oferecem a você a opção de fazer um trabalho off-line sofisticado.
-   Evite criar muitos recursos por quadro. As interações de driver necessárias podem serializar a CPU e a GPU, e as operações envolvidas são pesadas, pois elas geralmente exigem transições de kernel. Espalhe a criação em vários quadros ou reutilize recursos sem criá-los/liberá-los. O ideal é que você aguarde vários quadros antes de bloquear ou liberar recursos que foram usados recentemente para renderizar.
-   No final do quadro, não se esqueça de desassociar todos os canais de recursos (ou seja, fontes de fluxo, estágios de textura e índices atuais). Isso garantirá que as referências de pendente aos recursos sejam removidas antes que façam com que o Gerenciador de recursos Mantenha os recursos residentes que, na verdade, não estão mais em uso.
-   Para texturas, use formatos compactados (por exemplo, DXTn) com os mapas MIP e considere usar um Atlas de textura. Isso reduz significativamente os requisitos de largura de banda e pode reduzir o tamanho geral dos recursos, tornando-os mais eficientes.
-   Para Geometry, use a geometria indexada, pois isso ajuda a compactar os recursos de buffer de vértice, e o hardware de vídeo moderno é muito otimizado em relação à reutilização de vértices. Ao fazer uso de sombreadores de vértice programáveis, você pode compactar as informações de vértice e expandi-las durante o processamento de vértice. Novamente, isso ajuda a reduzir os requisitos de largura de banda e torna os recursos de buffer de vértice mais eficientes.
-   Evite a otimização excessiva de seu gerenciamento de recursos. Revisões futuras de drivers, hardware e sistema operacional podem causar problemas de compatibilidade se o aplicativo for ajustado muito para uma combinação particularmente. Como a maioria dos aplicativos é limitada por CPU, o gerenciamento caro baseado em CPU geralmente causa mais problemas de desempenho do que é resolvido.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gerenciando recursos](/windows/desktop/direct3d9/managing-resources)
</dt> <dt>

[Dispositivos perdidos](/windows/desktop/direct3d9/lost-devices)
</dt> <dt>

[Otimizações de desempenho](/windows/desktop/direct3d9/performance-optimizations)
</dt> <dt>

[Recursos de textura compactados](/windows/desktop/direct3d9/compressed-texture-resources)
</dt> <dt>

[Consultas](/windows/desktop/direct3d9/queries)
</dt> <dt>

[**D3DUSAGE**](/windows/desktop/direct3d9/d3dusage)
</dt> <dt>

[**D3DPOOL**](/windows/desktop/direct3d9/d3dpool)
</dt> <dt>

[D3DCREATE](/windows/desktop/direct3d9/d3dcreate)
</dt> </dl>

 

 