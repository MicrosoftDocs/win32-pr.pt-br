---
title: Glossário do Direct3D 12
description: Esses termos são diferentes do Direct3D 12.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 46B0F055-7E4F-4F8D-9915-3D195FD695B7
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a84b4b2e5a993b33b4c322b91682c8f9b5499bc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548303"
---
# <a name="direct3d-12-glossary"></a>Glossário do Direct3D 12

Esses termos são diferentes do Direct3D 12.

<dl> <dt>

<span id="direct3d12.directx_12_glossary_binding"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_BINDING"></span>**vinculação**
</dt> <dd>

O processo de anexar memória ao pipeline de gráficos. A associação de recursos, por exemplo, envolve a associação de um recurso, como uma textura ao pipeline, para uso na renderização de um objeto.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_buffer"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_BUFFER"></span>**completo**
</dt> <dd>

Um tipo de recurso do D3D que é sinônimo de uma alocação de memória contígua.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_bundle"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_BUNDLE"></span>**Commons**
</dt> <dd>

Um buffer de comando que a GPU (unidade de processamento gráfico) pode executar somente diretamente por meio de uma *lista de comandos diretas*. Um pacote herda todo o estado da GPU (exceto para o *objeto de estado de pipeline* definido e a topologia primitiva).

</dd> <dt>

<span id="direct3d12.directx_12_glossary_command_allocator"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_COMMAND_ALLOCATOR"></span>**alocador de comando**
</dt> <dd>

As alocações de memória subjacentes nas quais os comandos de GPU são armazenados. O objeto alocador de comando se aplica a *listas de comandos diretos* e *grupos*.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_command_list"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_COMMAND_LIST"></span>**lista de comandos**
</dt> <dd>

Uma lista de comandos corresponde a um conjunto de comandos que a GPU executa. Isso inclui comandos como definir estado, desenhar, limpar e copiar. A interface de lista de comandos D3D12 é significativamente diferente da interface de lista de comandos do D3D11. A interface de lista de comandos D3D12 contém APIs semelhantes às APIs de renderização de contexto de dispositivo D3D11.

Uma lista de comandos D3D12 não mapeia ou cancela recursos, altera mapeamentos de bloco, redimensiona pools de blocos, obtém dados de consulta, nem envia comandos implicitamente para a GPU para execução.

Ao contrário dos contextos adiados do D3D11, as listas de comandos do D3D12 dão suporte apenas a dois níveis de indireção. Uma *lista de comandos diretas* corresponde a um buffer de comando que a GPU pode executar. Um *pacote* pode ser executado somente diretamente por meio de uma lista de comandos direto.

Uma lista de comandos diretas não herda nenhum estado de GPU. Um pacote herda todo o estado da GPU (exceto para o objeto de estado de pipeline definido e a topologia primitiva).

A memória para uma lista de comandos é definida pelo *alocador de comando*. A finalidade das listas de comandos é que elas podem ser enviadas a uma GPU como uma única solicitação de renderização.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_command_queue"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_COMMAND_QUEUE"></span>**fila de comandos**
</dt> <dd>

Uma fila de *listas de comandos* que a GPU executa sucessivamente. Os aplicativos devem enviar explicitamente as *listas de comandos* a uma fila de comandos para execução. Normalmente, há três filas de comando: gráficos 3D, computação e cópia, correspondentes ao pipeline de gráficos 3D, ao mecanismo de computação e a um ou mais mecanismos de cópia na GPU.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_conservative_rasterization"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_CONSERVATIVE_RASTERIZATION"></span>**rasterização conservadora**
</dt> <dd>

A rasterização conservadora é um modo de operação para o estágio rasterizador do pipeline de gráficos do Direct3D. Ele desabilita a rasterização padrão baseada em amostra e, em vez disso, rasterizará um pixel coberto por qualquer valor por um primitivo. Uma distinção importante é que, embora qualquer cobertura produza um pixel rasterizado, essa cobertura não pode ser caracterizada pelo hardware e, portanto, a cobertura sempre aparece em binário para um sombreador de pixel: totalmente coberta ou não coberto. Ele é deixado para o código do sombreador de pixel para determinar a cobertura real.

A rasterização conservadora pode ajudar com problemas como colisão e detecção de ocorrências, compartimentalização e remoção de oclusão, em que a cor de um pixel é mais específica e os casos de borda podem ser eliminados. Consulte [rasterização conservadora](conservative-rasterization.md).

</dd> <dt>

<span id="direct3d12.directx_12_glossary_cbv"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_CBV"></span>**Exibição de buffer constante (CBV)**
</dt> <dd>

Os buffers de constantes contêm dados de constante de sombreador, como uma exibição de câmera, matrizes de projeção e matrizes mundiais. Uma "exibição de buffer constante" é a exibição específica do formato do buffer, como visto pelo pipeline de gráficos.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_default_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DEFAULT_HEAP"></span>**heap padrão**
</dt> <dd>

Um heap de modo de usuário que se concentra no suporte a tipos de recursos de GPU persistentes, incluindo recursos escritos por GPU.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_descriptor"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DESCRIPTOR"></span>**descritor**
</dt> <dd>

Os descritores são a unidade primária de associação para um único recurso no D3D12. Um descritor é um bloco de dados relativamente pequeno que descreve totalmente um objeto para a GPU, em um formato específico de GPU. Há muitos tipos diferentes de descritores: SRVs (exibições de recursos de sombreador), UAVs (exibições de acesso não ordenadas), CBVs (exibições de buffer constante) e amostras são alguns exemplos.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_descriptor_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DESCRIPTOR_HEAP"></span>**heap de descritores**
</dt> <dd>

Um heap de descritor é uma coleção de alocações contíguas de descritores, uma alocação para cada descritor. O ponto principal de um heap de descritor é abranger a quantidade de alocação de memória necessária para armazenar as especificações de descritor dos tipos de objetos que os sombreadores fazem referência para o maior número possível de uma janela de renderização (idealmente, um quadro inteiro de renderização ou mais).

</dd> <dt>

<span id="direct3d12.directx_12_glossary_descriptor_table"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DESCRIPTOR_TABLE"></span>**tabela de descritores**
</dt> <dd>

Uma tabela de descritores é logicamente uma matriz de descritores. Cada tabela de descritores armazena os descritores de um ou mais tipos, incluindo SRVs, UAVe, CBVs e amostras. Uma tabela de descritores não é uma alocação de memória; ela é simplesmente um deslocamento e um comprimento em um heap de descritor.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_direct_command_list"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DIRECT_COMMAND_LIST"></span>**lista de comandos diretos**
</dt> <dd>

Um buffer de comando que a GPU pode executar. Uma lista de comandos diretas não herda nenhum estado de GPU.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_fence"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_FENCE"></span>**ondula**
</dt> <dd>

Um mecanismo para sincronizar a GPU e a CPU. A GPU e a CPU podem ser instruídas a aguardar em um limite, esperando em vigor para o outro processador acompanhar. Consulte [sincronização de vários mecanismos](./user-mode-heap-synchronization.md).

</dd> <dt>

<span id="direct3d12.directx_12_glossary_hazard"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_HAZARD"></span>**risco, controle de riscos**
</dt> <dd>

Um risco ocorre quando um recurso foi usado para uma finalidade e o aplicativo pretende reutilizá-lo para outra finalidade. Para usar o recurso novamente, os caches intermediários precisarão ser liberados ou invalidados, os requisitos de compactação precisarão ser consistentes com o segundo uso e o recurso deverá estar no estado necessário para evitar a leitura do recurso depois que ele tiver sido gravado e invalidado para a finalidade pretendida.

O processo de manutenção de recursos e de evitar esses problemas de sincronização é conhecido como controle de risco. Se não houver nenhum controle de risco pelo driver, o aplicativo será responsável por isso. Na maioria das versões anteriores do DirectX, o controle de riscos foi manipulado pelo driver. Para melhorar o desempenho, os métodos sem controle de risco estão disponíveis no DirectX 12.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_hlsl"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_HLSL"></span>**Linguagem de sombreamento de alto nível (HLSL)**
</dt> <dd>

Uma linguagem de computador, semelhante, mas distinta de várias maneiras, que é usada para escrever código de sombreador. Os sombreadores de vértice, pixel, geometria, computação, domínio e envoltória são todos escritos usando HLSL. Um compilador converte a origem HLSL em um formato binário para consumir a GPU.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_multiengine"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_MULTIENGINE"></span>**multiengine**
</dt> <dd>

As diferentes instâncias e tipos de mecanismos em uma única GPU. Os tipos de mecanismos incluem: gráficos, computação e cópia.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_multigpu"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_MULTIGPU"></span>**MultiGPU**
</dt> <dd>

Uma configuração de hardware onde há mais de um adaptador gráfico. Os adaptadores separados, às vezes, são chamados de nós. Ter várias GPUs pode tornar a tarefa de sincronizá-las com a CPU e outra, consideravelmente mais complexa do que com uma única GPU.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_pipeline_state_object"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_PIPELINE_STATE_OBJECT"></span>**Objeto de estado de pipeline (PSO)**
</dt> <dd>

Uma parte significativa do estado da GPU. Esse estado inclui todos os sombreadores definidos atualmente e determinados objetos de estado de função fixa. A única maneira de alterar os Estados contidos no objeto de pipeline é alterar o objeto de pipeline vinculado no momento.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_predication"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_PREDICATION"></span>**predicação**
</dt> <dd>

Predicação é um recurso que habilita a GPU em vez da CPU para determinar não desenhar, copiar ou distribuir um objeto. Por exemplo, se uma caixa delimitadora de um objeto for totalmente obstruído por outro objeto ou a perspectiva tiver reduzido o objeto para menos do que o tamanho de um pixel, pode não haver nenhum ponto na tentativa de desenhar o objeto oculto. Consulte [predicação](predication.md).

</dd> <dt>

<span id="direct3d12.directx_12_glossary_rov"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_ROV"></span>**Exibição de ordem do rasterizador (ROV)**
</dt> <dd>

Pipelines gráficos padrão podem ter problemas para compor corretamente várias texturas que contêm transparência. Objetos como isolamentos de fio, fumaça, fogo, vegetação e transparência de uso de vidro colorido para obter o efeito desejado. Os problemas surgem quando várias texturas que contêm transparência estão alinhadas umas com as outras (fumaça na frente de uma cerca na frente de um prédio contendo vegetação, como um exemplo). As exibições ordenadas do rasterizador (ROVs) habilitam os algoritmos de OIT (transparência independente de ordem subjacente) para usar os recursos do hardware para tentar resolver a ordem de transparência corretamente. A transparência é manipulada pelo sombreador de pixel.

As exibições ordenadas do rasterizador (ROVs) permitem que o código do sombreador de pixel marque associações de UAV (exibição de acesso não ordenado) com uma declaração que altera os requisitos normais para a ordem dos resultados do pipeline de gráficos para UAVs.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_readback_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_READBACK_HEAP"></span>**heap de readback**
</dt> <dd>

Um heap de modo de usuário que se concentra na transferência de dados da GPU de volta para a CPU.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_resource"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE"></span>**Kit**
</dt> <dd>

Uma entidade que fornece dados para o pipeline e define o que é processado durante sua cena. Os recursos podem ser carregados a partir da mídia de jogo ou criados dinamicamente no momento de execução. Normalmente, os recursos incluem dados de textura, dados de vértice e dados de sombreador. A maioria dos aplicativos do Direct3D cria e destrói recursos extensivamente durante seu ciclo de vida.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_resource_barrier"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE_BARRIER"></span>**barreira de recurso**
</dt> <dd>

Uma barreira de recurso notifica o driver de que a sincronização de vários acessos a um único recurso pode ser necessária, por exemplo, leitura e gravação na mesma textura.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_resource_binding"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE_BINDING"></span>**Associação de recursos**
</dt> <dd>

A associação de recursos é o processo de vinculação de recursos (texturas, buffers de vértice, buffers de índice e assim por diante) ao pipeline de gráficos, permitindo que os sombreadores do pipeline processem o recurso correto.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_resource_heaps"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE_HEAPS"></span>**heaps de recursos**
</dt> <dd>

Heaps de recursos é um termo genérico para os heaps que são buffers de memória separados para manter recursos à medida que são transferidos para e da GPU. Uma transferência para a GPU requer um heap de carregamento, da GPU para a CPU requer um heap readback e um heap persistente para a GPU a ser mantido em vários quadros de renderização é chamado de heap padrão.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_root_signature"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_ROOT_SIGNATURE"></span>**assinatura de raiz**
</dt> <dd>

As assinaturas raiz definem todos os recursos que devem ser associados aos pipelines de gráficos ou de computação. Uma assinatura de raiz é configurada pelas listas de comandos de aplicativo e links para os recursos que os sombreadores exigem normalmente, há um gráfico e uma assinatura raiz de computação por aplicativo.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_sampler"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SAMPLER"></span>**cores**
</dt> <dd>

Um amostra é o código que lê de uma textura.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_srv"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SRV"></span>**Modo de Exibição de Recursos do sombreador (SRV)**
</dt> <dd>

Uma maneira específica de formato de examinar os dados em um recurso de sombreador, como uma textura.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_static_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_STATIC_HEAP"></span>**heap estático**
</dt> <dd>

Um heap de modo de usuário que se concentra em vários recursos somente leitura de GPU que normalmente são usados ao mesmo tempo e não são alterados com frequência.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_swap_chain"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SWAP_CHAIN"></span>**Cadeia de permuta**
</dt> <dd>

As cadeias de permuta controlam a rotação do buffer de fundo, formando a base da animação de gráficos. As cadeias de permuta são manipuladas pelo conjunto de APIs de nível baixo DXGI (consulte [visão geral do dxgi](../direct3ddxgi/d3d10-graphics-programming-guide-dxgi.md)).

</dd> <dt>

<span id="direct3d12.directx_12_glossary_swizzle"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SWIZZLE"></span>**swizzle**
</dt> <dd>

Uma técnica de localizar dados multidimensionais na memória, de modo que os dados da dimensionalidade próxima tendem a ter endereços próximos. Em particular, todos os dados de uma linha não estão localizados de forma contígua antes dos dados da próxima linha. Um "swizzle com parâmetros" descreve uma maneira padronizada para descrever os padrões de swizzle.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_static_texture"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_STATIC_TEXTURE"></span>**textura**
</dt> <dd>

Um tipo de recurso do D3D que é multidimensional e tem um layout de memória que é otimizado para acesso multidimensional da GPU. As texturas geralmente contêm a imagem bruta necessária para renderizar em uma superfície, antes que a iluminação e a mesclagem ocorram, mas possam conter outras formas de dados, como gradientes de cores e cores de referência. O Direct3D 12 dá suporte a uma, duas e três texturas dimensionais.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_tile"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_TILE"></span>**bloco**
</dt> <dd>

Uma página de memória de vídeo, semelhante a uma página de CPU/sistema de memória. A notação de bloco ajuda a distinguir o subsistema de memória virtual da GPU do subsistema de memória virtual da CPU. As GPUs fornecem recursos de memória virtual semelhantes à memória virtual do sistema. Algumas GPUs têm recursos de memória virtual compartilhados, que permitem o compartilhamento de algumas páginas do subsistema de memória virtual com a CPU e a GPU.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_tiled_resources"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_TILED_RESOURCES"></span>**recursos em ladrilho**
</dt> <dd>

Os recursos do lado do ladrilho são necessários, portanto, menos memória da GPU é desperdiçada, armazenando regiões de superfícies que o aplicativo sabe que não será acessado, e o hardware pode entender como filtrar por blocos adjacentes. Os recursos em ladrilho são grandes recursos lógicos, mas exigem pequenas quantidades de memória física.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_uav"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_UAV"></span>**Modo de exibição de acesso não ordenado (UAV)**
</dt> <dd>

Uma exibição de acesso não ordenada em um recurso (que inclui buffers, texturas e matrizes de textura, sem várias amostras), permite acesso de leitura/gravação não ordenado de forma temporal de vários threads. Isso significa que esse tipo de recurso pode ser lido/gravado simultaneamente por vários threads sem gerar conflitos de memória.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_upload_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_UPLOAD_HEAP"></span>**carregar heap**
</dt> <dd>

Um heap de modo de usuário que se concentra na transferência de dados da CPU para a GPU.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_user_mode_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_USER_MODE_HEAP"></span>**heap de modo de usuário**
</dt> <dd>

Uma coleção de alocações de memória grandes e contíguas que são recicladas sem reconhecimento de qualquer componente de kernel: os métodos de alocação e destruição não chamam métodos de alocação e destruição de kernel durante o estado Steady. Upload, readback e heaps padrão são variantes de heaps de modo de usuário.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_volume_tiled_resources"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_VOLUME_TILED_RESOURCES"></span>**recursos de sublado do volume**
</dt> <dd>

[Recursos de lado](/windows)triplo tridimensionais.

</dd> </dl>

 

 