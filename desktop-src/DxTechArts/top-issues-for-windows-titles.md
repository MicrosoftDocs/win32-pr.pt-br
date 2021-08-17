---
title: principais problemas de títulos de Windows
description: Este artigo destaca muitos dos problemas comuns que vimos nos jogos de PC da geração atual.
ms.assetid: 89b83473-1aa9-9a2d-8778-15cfb91cdea4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b89be8ad7a68c247d589f304ea77fa9b3e63e105739264e39f71794c705b66cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118396501"
---
# <a name="top-issues-for-windows-titles"></a>principais problemas de títulos de Windows

o grupo de relações do desenvolvedor de tecnologias de jogos e elementos gráficos do Microsoft Windows executa análise de desempenho para muitos jogos de Windows por ano. Durante essas sessões, obtemos experiência prática para se juntar aos comentários e consultas do desenvolvedor que recebemos diariamente. Ocasionalmente, ajudamos a rastrear uma falha misteriosa ou outro problema em um título, que nos dá mais informações sobre problemas que os desenvolvedores estão encontrando.

Este artigo destaca muitos dos problemas comuns que vimos nos jogos de PC da geração atual.

-   [Desempenho limitado à CPU](#cpu-limited-performance)
-   [Gerenciamento de lote insatisfatório](#poor-batch-management)
-   [Cópia de memória excessiva](#excessive-memory-copying)
-   [Uso excessivo do envio de desenho dinâmico](#excessive-use-of-dynamic-draw-submission)
-   [Alta sobrecarga no processamento de arquivos](#high-overhead-in-file-processing)
-   [Instalação lenta e frustrante](#slow-and-frustrating-installation)
-   [Falta de consideração da memória física](#lack-of-consideration-of-physical-memory)
-   [Excesso de confiança na conversão de taxa de amostragem de Real-Time áudio](#over-reliance-on-real-time-audio-sample-rate-conversion)
-   [Fragmentação da memória virtual](#fragmention-of-virtual-memory)
-   [Manipulação da palavra de controle de Floating-Point](#manipulation-of-the-floating-point-control-word)
-   [Instalação opcional do tempo de execução do DirectX](#optional-installation-of-the-directx-runtime)
-   [Uso excessivo da sincronização de threads](#excessive-use-of-thread-synchronization)
-   [Uso de RDTSC](#use-of-rdtsc)

## <a name="cpu-limited-performance"></a>Desempenho de CPU-Limited

A grande maioria dos jogos é limitada pelo desempenho da CPU em sistemas com GPUs (unidades de processamento gráfico) de alto desempenho. Isso às vezes é devido ao uso insatisfatório de envio em lote para envio de empates, mas, mais geralmente, isso se deve a outros sistemas de jogos consumindo uma grande parte dos ciclos de CPU disponíveis. Nos poucos casos em que vimos a GPU como a limitação, a causa é uma taxa de preenchimento muito alta ou a demanda do sombreador de pixel, em configurações de alta resolução ou baixo desempenho do sombreador de vértice por uma placa de vídeo.

Como a maioria dos títulos é limitada por CPU, o maior desempenho vence da otimização de sistemas de jogos com uso intensivo de CPU. Normalmente, os sistemas de ia ou de física e a lógica de detecção de colisão associada são os principais consumidores de ciclos de CPU que se comportam com aplicativos Microsoft Direct3D. Qualquer trabalho para melhorar esses sistemas pode melhorar o desempenho geral do jogo.

## <a name="poor-batch-management"></a>Gerenciamento de lote insatisfatório

Atingir um bom paralelismo com a GPU exige que os lotes de desenho contenham geometria suficiente – e os sombreadores tenham a complexidade certa — para manter a placa de vídeo ocupada, sem usar tantos lotes que o buffer de comando é inundado. Em hardware de geração atual, recomendamos aproximadamente 300 ou menos envios de lote de empates por quadro (menos em CPUs de desempenho inferior) para impedir que o processamento do driver do buffer de comando se torne um afunilamento de desempenho. Algumas outras chamadas de estado de API e combinações de driver podem resultar em um alto processamento de CPU (driver de compilação de sombreadores, por exemplo), portanto, é altamente recomendável analisar a rotina de desempenho.

## <a name="excessive-memory-copying"></a>Cópia de memória excessiva

Durante o desenvolvimento da maioria dos títulos de PC, os desenvolvedores usam estruturas de dados e cadeias de caracteres convenientes para o gerenciamento de conteúdo. O trabalho de CPU necessário para comparação de cadeias de caracteres, cópia e outras manipulações geralmente tem uma sobrecarga mensurável, especialmente ao levar em conta as ocorrências de desempenho associadas ao subsistema de cache e memória. Os planos devem ser feitos ao desenvolver esses sistemas para remover ou minimizar a dependência no processamento de cadeias de caracteres quando o produto entrar nas fases de teste e versão principais.

## <a name="excessive-use-of-dynamic-draw-submission"></a>Uso excessivo do envio de desenho dinâmico

O hardware de vídeo moderno funciona bem ao lidar com dados estáticos. Os adaptadores high-end geralmente têm uma quantidade muito grande de memória de vídeo, mas essa memória não pode ser efetivamente utilizada por dados dinâmicos.

Embora padrões de uso razoavelmente eficientes de buffers de vértice dinâmicos/buffers de índice possam ser implementados para conteúdo dinâmico, muitos títulos estão contratando esse idioma para o que é conteúdo estático de outra forma. Geralmente vemos isso com árvores de particionamento de espaço binário (BSP) e sistemas baseados em portal que armazenam geometria em uma estrutura de dados que não mapeia para o hardware e que devem ser processados em buffers para cada quadro. Colocar o máximo de conteúdo em recursos estáticos como possível pode reduzir significativamente a sobrecarga de largura de banda da transferência de dados para a placa de vídeo, fazer melhor uso do VRAM integrado e reduzir a sobrecarga de CPU/cache envolvida no processamento desse conteúdo.

## <a name="high-overhead-in-file-processing"></a>Alta sobrecarga no processamento de arquivos

Jogos de PC têm uma reputação de longos tempos de carregamento, em particular em comparação com os títulos de console com requisitos estritos de tempo de carregamento. Nossa análise da forma que muitos títulos usam o subsistema de arquivos revela alguns problemas comuns.

A sobrecarga de abrir um arquivo geralmente é muito maior do que os desenvolvedores esperam. Com os verificadores de vírus sob demanda em uso generalizado, e a funcionalidade adicional do NTFS, a abertura de um arquivo é uma operação bastante cara. Abrir vários arquivos ao mesmo tempo ou abrir e fechar o mesmo arquivo repetidamente é, portanto, um método insatisfatório de lidar com o gerenciamento de arquivos. Alguns jogos tentaram reduzir esse custo de desempenho testando a existência de um arquivo antes de abri-lo. A realidade é que o teste para a existência de um arquivo em NTFS requer a abertura do arquivo, portanto, o teste antes de abrir os resultados é o custo duas vezes.

Os jogos que permitem modificações de complemento ou mods, ou que ainda incluem scaffolding de desenvolvimento para verificar se há arquivos de dados de substituição, podem ter atrasos significativos no carregamento do jogo devido à verificação desses arquivos, mesmo quando esses arquivos não estão presentes. Recomendamos que os jogos verifiquem apenas esses arquivos quando executados com uma opção especial de linha de comando ou outro indicador de modo, para que somente os usuários que usam essa funcionalidade realmente paguem o custo de desempenho dessas verificações (geralmente extensas).

O desempenho adicional pode ser obtido no sistema de arquivos pelo seguinte:

-   Uso apropriado do sinalizador de arquivo de dicas do sistema de arquivos \_ \_ \_ e \_ \_ verificação SEQUENCIAl de sinalizador de arquivo \_
-   Dimensionando buffers para evitar uma grande quantidade de chamadas para as APIs de leitura/gravação do sistema operacional
-   Acessando arquivos de forma assíncrona
-   Carregando threads em segundo plano

Também é altamente recomendável converter dados offline (no momento da compilação ou da instalação) em vez de depender da conversão quando o jogo é executado pela primeira vez, pois isso impõe um imposto de desempenho significativo para cada usuário.

## <a name="slow-and-frustrating-installation"></a>Instalação lenta e frustrante

Outro problema comum que vimos é o tempo de instalação muito longo necessário para muitos jogos de PC modernos. Os instaladores solicitam ao usuário muitas vezes, às vezes simplesmente para dizer ao usuário, por exemplo, "você não precisa do DirectX instalado". Em geral, esses instaladores incorretos exigem que o usuário selecione **Avançar** ou **OK** muitas vezes antes de a instalação do jogo realmente começar. Depois de começar, vimos que alguns títulos levam uma hora ou mais antes que o usuário obtenha a oportunidade de jogar o jogo. Parecemos fortemente que a primeira hora da experiência de jogo não deve ser a instalação.

Recomendamos várias abordagens para lidar com a instalação. Primeiro, mantenha os prompts simples e mínimos. Segundo, projete seus dados de jogos de modo que alguns ou todos os arquivos de dados possam ser usados diretamente do disco de distribuição sempre que possível – unidades de DVD modernas têm largura de banda muito alta. Em terceiro lugar, considere a implementação da instalação sob demanda em seus títulos para reduzir ou eliminar o processo de instalação e permitir que os usuários entrem no jogo o mais rápido possível. (Para obter mais informações sobre a instalação sob demanda, consulte [install-sob demanda para jogos](/windows/desktop/DxTechArts/install-on-demand-for-games).)

Para obter mais recomendações sobre a instalação do jogo, consulte [simplificando a instalação do jogo](/windows/desktop/DxTechArts/simplifying-game-installation).

## <a name="lack-of-consideration-of-physical-memory"></a>Falta de consideração da memória física

Devido à grande variabilidade do hardware de PC no mercado, os títulos normalmente fazem uso de testes de configuração ad hoc para selecionar as configurações padrão para o nível de detalhes gráficos. Alguns dos títulos que vimos estão usando o tamanho da memória de vídeo nesses testes, mas falham em correlacioná-lo com o tamanho da memória física. Para lidar com situações de dispositivo perdido, a maior parte da memória de vídeo (o VRAM local no cartão e a abertura de memória AGP não local) deve ser apoiada pela memória física, seja pelo uso de recursos gerenciados ou estruturas de dados personalizadas. Algumas placas de vídeo de ponta têm tamanhos de VRAM que consomem o tamanho das memórias de CPU de low-end. Em situações em que o sistema tem memória física limitada em comparação com a placa de vídeo, a maior parte desse VRAM não pode ser efetivamente utilizada e as configurações de detalhes mais baixos devem ser configuradas.

## <a name="over-reliance-on-real-time-audio-sample-rate-conversion"></a>Conversão de taxa de amostragem de Over-Reliance em Real-Time áudio

Outra fonte comum de gravação de ciclo de CPU que vimos ocorre quando o sistema de áudio é necessário para converter a taxa de reprodução durante a combinação no buffer de hardware. com drivers de Windows Driver Model (WDM), o formato de buffer de hardware não está sob o controle de aplicativo direto, porque ele é um recurso de nível de kernel; em vez disso, o formato é selecionado com base no formato de qualidade mais alta de todas as fontes e nos recursos do hardware. por padrão, o Windows XP usa uma conversão de taxa de exemplo de alta qualidade para esse processo e, se a maioria dos exemplos de áudio exigir uma conversão de taxa, uma parte significativa dos ciclos de CPU será consumida.

É recomendável criar todos os buffers do DirectSound com a mesma taxa de amostragem. Se você fizer qualquer uso das funções do Microsoft Win32 **WaveOut** , deverá usar uma taxa de amostra consistente com elas também. Com os drivers WDM, os buffers serão todos misturados pelo kernel e, se você usar uma taxa de amostragem mais alta em alguns deles, as taxas de exemplo de todos os demais serão convertidas para correspondência. Observe que isso implica usar a mesma taxa de reprodução para todos os seus exemplos de áudio, incluindo quaisquer buffers de descompactação de áudio de streaming. a definição da taxa de buffer primária não tem nenhum efeito, a menos que você esteja direcionando Windows 98 ou Windows Millennium Edition.

> [!Note]  
> no Windows Vista e versões posteriores do sistema operacional, o DirectSound e o **waveout** usam a [API de sessão de áudio Windows (WASAPI)](/windows/desktop/CoreAudio/wasapi) para toda a saída de áudio.

 

## <a name="fragmention-of-virtual-memory"></a>Fragmentação da memória virtual

Vimos vários problemas recentes relacionados ao limite de 32 bits no espaço de memória do processo. Embora 2 GB de espaço de endereço virtual para processos de modo de usuário tenham sido mais do que o mais adequado historicamente, o maior uso de arquivos mapeados de memória grandes, alocadores de memória personalizados e tamanho de VRAM crescente (que deve ser mapeado no espaço de processo) começou a causar situações em que as alocações de espaço de memória virtual estão falhando. Algumas DLLs que não são da Microsoft estão usando locais de início fixo no meio do espaço de endereço virtual, que está causando a fragmentação que resulta em alocações com falha.

Esses problemas geralmente aparecem quando o jogo usa um esquema de alocação de memória personalizado que tenta alocar um grande bloco contínuo de espaço de memória virtual. Nossa recomendação é escrever alocadores de forma que eles solicitem mais partes de tamanho razoável do espaço de endereço virtual, conforme necessário. Por exemplo, solicitando 64 ou 256 MB por vez, mas não 1 GB. No entanto, deve-se ter cuidado para não causar mais fragmentação. O advento dos sistemas operacionais de 64 bits e do hardware ajudará muito nesses problemas no futuro, mas deve ser necessário tomar cuidado com os sistemas de 32 bits de geração atual.

## <a name="manipulation-of-the-floating-point-control-word"></a>Manipulação da palavra de controle de Floating-Point

Como um auxílio de depuração, alguns desenvolvedores estão habilitando exceções na FPU (unidade de ponto flutuante) por meio de manipulações da palavra de controle de ponto flutuante. Isso é altamente problemático e provavelmente causará falha no processo. Assim como a Convenção de chamada requer que o registro EBX seja preservado, a maioria do sistema supõe que o FPU está em um estado padrão, fornecerá resultados razoáveis e não gerará exceções. Os drivers e outros componentes do sistema geralmente computam resultados com base na suposição de que os valores de erro padrão serão exibidos nos registros para condições ruins, mas se as exceções estiverem habilitadas, elas ficarão sem tratamento e resultarão em falhas.

O Direct3D definirá a unidade de ponto flutuante para precisão única, de arredondamento para mais próxima como parte da inicialização para o thread de chamada, a menos que o \_ sinalizador de preservação de FPU D3DCREATE \_ seja usado, nesse caso, a palavra de controle de ponto flutuante é intocada. Como a palavra de controle é uma configuração por thread, garantir que todos os threads do aplicativo sejam definidos como modo de precisão única pode otimizar o desempenho. Lembre-se de que chamar [**\_ control87**](https://msdn.microsoft.com/library/e9b52ceh(v=VS.71).aspx) não é válido para codificação nativa x64, que usa exclusivamente a SSE e é extremamente caro na arquitetura baseada em PowerPC da CPU Xbox 360.

> [!Note]  
> Se você modificar a palavra de controle, use [**\_ \_ controlfps**](https://msdn.microsoft.com/library/c9676k6h(v=VS.80).aspx) e esteja ciente de que, para plataformas x64, você não pode alterar a precisão de ponto flutuante por meio da palavra de controle.

 

Em qualquer biblioteca em que precisamos ter regras de arredondamento diferentes ou outro comportamento , como lidar com sombreadores de vértice de software ou compilação, salvamos e restauramos a palavra de controle. Se um jogo precisar fazer uso de arredondamento não padrão ou exceções de FPU, ele deverá salvar e restaurar a palavra de controle de ponto flutuante e você deve ter certeza de que ele não chama nenhum código externo que não tenha sido comprovadamente seguro contra esses problemas, incluindo APIs do sistema.

## <a name="optional-installation-of-the-directx-runtime"></a>Instalação opcional do Runtime do DirectX

Vários jogos perguntem ao usuário se deve instalar o DirectX. Isso poderá causar problemas se o usuário assumir que o sistema tem o directX redistribuível mais recente instalado e ignorar a instalação e, posteriormente, a instalação continuará com êxito. Se o jogo exigir uma versão específica do D3DX ou outra funcionalidade atualizada que não foi instalada, o jogo não funcionará e o usuário ficará muito frustrado.

É altamente recomendável que o instalador do jogo instale silenciosamente os redistribuíveis do DirectX com base no que o jogo foi criado. O processo de instalação do DirectX foi projetado para verificar se algo precisa ser atualizado e retorna rapidamente, caso não precise. Portanto, não é necessário perguntar ao usuário sobre como instalar o DirectX.

Uma instalação silenciosa do DirectX pode ser feita executando este comando no pacote de instalação: **dxsetup.exe /silent**

Além disso, o tamanho real da pasta redistribuível pode ser configurado para incluir somente os arquivos de gabinete (.cab) que são realmente necessários para uso e plataformas de destino do jogo.

> [!Note]  
> Antes de usar **dxsetup**, leia [Configuração direta não tão .](https://walbourn.github.io/)

 

## <a name="excessive-use-of-thread-synchronization"></a>Uso excessivo da sincronização de thread

Ao criação de perfil de jogos, os principais pontos de acesso geralmente são considerados relacionados à entrada e saída de seções críticas. Com a predominância de CPUs de vários núcleos, o uso de multithreading em jogos aumentou drasticamente e muitas implementações dependem do uso intenso da sincronização de thread. O tempo de CPU para usar uma seção crítica, mesmo sem qualquer contenção, é bastante significativo e todas as outras formas de sincronização de thread são ainda mais caras. Portanto, é necessário ter cuidado para minimizar o uso desses primitivos.

Uma fonte comum de sincronização excessiva em jogos é o uso [de D3DCREATE \_ MULTITHREADED](/windows/desktop/direct3d9/d3dcreate). Esse sinalizador, ao tornar o Direct3D thread-safe para renderização de vários threads, assume uma abordagem muito conservadora, resultando em alta sobrecarga de sincronização. Os jogos devem evitar esse sinalizador. Em vez disso, arquitete o mecanismo para que toda a comunicação com o Direct3D seja de um único thread e qualquer comunicação entre threads seja manipulada diretamente. Para obter mais informações sobre como criar jogos multi-threaded, consulte o artigo [Codificando para](/windows/desktop/DxTechArts/coding-for-multiple-cores)vários núcleos no Xbox 360 e no Microsoft Windows .

## <a name="use-of-rdtsc"></a>Uso de RDTSC

O uso da instrução x86 **RDTSC** não é recomendado. **O RDTSC** não consegue calcular corretamente o tempo em alguns esquemas de gerenciamento de energia que alteram a frequência da CPU dinamicamente e em muitas CPUs de vários núcleos para as quais o contador de ciclo não está sincronizado entre núcleos. Em vez disso, os jogos devem usar a API [**QueryPerformanceCounter.**](/windows/desktop/api/profileapi/nf-profileapi-queryperformancecounter) Para obter mais informações sobre problemas com **o RDTSC** e implementar o tempo de alta resolução com **QueryPerformanceCounter**, consulte o artigo Tempo do jogo e processadores [multicore](/windows/desktop/DxTechArts/game-timing-and-multicore-processors).

 

 