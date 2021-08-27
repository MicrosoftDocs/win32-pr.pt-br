---
title: Criação de perfil de aplicativos DirectX
description: mostra como medir algumas das medidas de tempo de desempenho mais importantes para um aplicativo DirectX usando as ferramentas XPerf e GPUView que são fornecidas como parte do Toolkit de desempenho Windows.
ms.assetid: 4B2F7273-C9B0-4DD3-B559-6220CDE62129
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c923f2917dbb8695bcd624f4d998043e7218cf2f976b19b24ab4cff2bc65f398
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118665333"
---
# <a name="profiling-directx-apps"></a>Criação de perfil de aplicativos DirectX

isso mostra como medir algumas das medidas de tempo de desempenho mais importantes para um aplicativo do [DirectX](/previous-versions/windows/apps/jj262109(v=win.10)) usando as ferramentas **XPerf** e **GPUView** que são fornecidas como parte do Toolkit de desempenho Windows. Este não é um guia abrangente para entender as ferramentas, em vez de sua aplicabilidade específica para analisar o desempenho do aplicativo DirectX. Embora a maioria das técnicas discutidas aqui seja relevante para todos os aplicativos do DirectX, ela é mais relevante para aplicativos que usam cadeias de permuta e não para aplicativos do DirectX criados em XAML que usam animações SIS/VSIS e XAML. Nós o orientamos pelas principais medições de tempo de desempenho, como adquirir e instalar as ferramentas, além de fazer rastreamentos de medição de desempenho e analisá-las para entender afunilamentos de aplicativo.

## <a name="about-the-tools"></a>Sobre as ferramentas

### <a name="xperf"></a>**XPerf**

**XPerf** é um conjunto de ferramentas de análise de desempenho criado com base no rastreamento de eventos para Windows (ETW) criado para medir e analisar o desempenho e o uso de recursos detalhados do sistema e do aplicativo. a partir do Windows 8 essa ferramenta de linha de comando tem uma interface gráfica do usuário e é chamada de WPR (gravador de desempenho Windows) e o Windows o analisador de desempenho (WPA). mais informações sobre essas ferramentas podem ser encontradas na página da web para [Windows Toolkit de desempenho](/previous-versions/windows/it-pro/windows-8.1-and-8/hh162945(v=win.10)) (WPT): [Windows Toolkit de desempenho](/previous-versions/windows/it-pro/windows-8.1-and-8/hh162945(v=win.10)).

Um ETW coleta eventos de kernel solicitados e os salva em um arquivo chamado de arquivo de log de rastreamento de eventos (ETL). Esses eventos de kernel fornecem informações abrangentes sobre as características do aplicativo e do sistema ao executar o aplicativo. Os dados são coletados habilitando a captura de rastreamento, executando o cenário de aplicativo desejado que precisa de análise, interrompendo a captura que salva os dados em um arquivo ETL. Em seguida, você pode analisar o arquivo no mesmo ou em um computador diferente usando a ferramenta de linha de comando **xperf.exe** ou a ferramenta de análise de rastreamento do Visual **xperfview.exe**.

### <a name="gpuview"></a>GPUView

**GPUView** é uma ferramenta de desenvolvimento para determinar o desempenho da GPU (unidade de processamento gráfico) e da CPU. Ele analisa o desempenho em relação ao processamento de buffer de acesso direto à memória (DMA) e a todos os outros processamentos de vídeo no hardware de vídeo.

Para aplicativos [DirectX](/previous-versions/windows/apps/jj262109(v=win.10)) que dependem muito da GPU, o **GPUView** é uma ferramenta poderosa para entender a relação entre o trabalho realizado na CPU versus GPU. Para obter mais informações sobre **GPUView**, consulte [usando o GPUView](/windows-hardware/drivers/display/using-gpuview).

Semelhante ao **Xperf**, um rastreamento ETW é obtido pela primeira vez iniciando o serviço de rastreamento, exercitando o cenário que precisa de análise para o aplicativo em questão, interrompendo o serviço e salvando as informações em um arquivo ETL. **GPUView** apresenta os dados presentes no arquivo ETL em um formato gráfico.

Depois de instalar a ferramenta **GPUView** , é recomendável que você leia o tópico "exibição principal do **GPUView**" no menu "ajuda do **GPUView** ". Ele contém informações úteis sobre como interpretar a interface do usuário do **GPUView** .

## <a name="installing-the-tools"></a>Instalando as ferramentas

ambos os **XPerf** e **GPUView** estão incluídos no WPT (Toolkit de desempenho de Windows).

o **XPerf** é fornecido como parte do SDK (Software Development Kit) Windows para Windows. [baixe o SDK do Windows](https://dev.windows.com/downloads).

o **GPUView** está disponível no Kit de avaliação e implantação do Windows (Windows ADK). [baixe o Windows ADK](/windows-hardware/get-started/adk-install).

Após a instalação, você deve adicionar os diretórios que contêm **Xperf** e **GPUView** à variável "Path" do sistema.

Clique no botão Iniciar e digite "variáveis do sistema". O janela Propriedades do sistema é aberto. Clique em "editar as variáveis de ambiente do sistema". Selecione "variáveis de ambiente" na caixa de diálogo "Propriedades do sistema". A variável "Path" é encontrada em "variáveis do sistema". Acrescente o diretório que contém **xperf.exe** e **GPUView.exe** ao caminho. esses executáveis são encontrados no diretório "Windows Toolkit de desempenho" dentro dos "Windows Kits". o local padrão é: **C: \\ arquivos de programas (x86) \\ Windows Kits \\ 10 \\ Windows Toolkit de desempenho**.

## <a name="performance-time-measurements"></a>Medições de tempo de desempenho

A maioria dos aplicativos espera ser executada sem problemas e respondendo à entrada do usuário. No entanto, dependendo do cenário desejado, um aspecto do desempenho pode ser mais importante do que o outro. Por exemplo, para um aplicativo de leitor de notícias em execução em um Tablet PC sensível ao toque, o aspecto mais importante é exibir um único artigo por vez e deslocar/aplicar zoom/rolar para a mesma ou para um artigo diferente. Nesse cenário, a capacidade de renderizar todo o conteúdo em todos os quadros não é necessária. No entanto, a capacidade de percorrer o artigo de forma tranqüila sobre um gesto de toque é extremamente importante.

Em outra instância, um jogo ou um aplicativo de renderização de vídeo que usa muitas animações falha se os quadros são descartados. Nesse caso, a capacidade de apresentar conteúdo na tela sem interuption da entrada do usuário é extremamente importante.

Para entender qual parte do aplicativo é problemática, a primeira etapa é decidir sobre os cenários mais importantes. Depois que os principais aspectos do aplicativo são compreendidos e como eles serão exercitados, procurar problemas usando as ferramentas fica mais fácil.

Algumas das métricas de tempo de desempenho mais comuns são as seguintes:

### <a name="startup-time"></a>Tempo de inicialização

Tempo medido desde a inicialização do processo até o primeiro presente, atingindo a tela. Essa medida é mais útil quando o sistema está quente, o que significa que a medição é feita depois que o aplicativo é iniciado algumas vezes.

### <a name="cpu-time-per-frame"></a>Tempo de CPU por quadro

O tempo pelo qual a CPU processa ativamente a carga de trabalho do aplicativo para um quadro. Se o aplicativo estiver funcionando sem problemas, todo o processamento necessário para um quadro acontecerá dentro de um intervalo de sincronização de v. Com a taxa de atualização de 60 do monitor, isso é 16ms por quadro. Se o tempo/quadro da CPU for maior que 16ms, as otimizações de CPU poderão ser necessárias para produzir uma experiência de aplicativo livre de falha.

### <a name="gpu-time-per-frame"></a>Tempo de GPU por quadro

O tempo para o qual a GPU processa ativamente a carga de trabalho do aplicativo para um quadro. Um aplicativo é associado à GPU quando o tempo necessário para processar um quadro de dados é maior que 16ms.

Ser capaz de entender se um aplicativo está ligado à CPU ou à GPU restringirá a parte problemática do código.

## <a name="taking-performance-time-measurement-trace"></a>Obtendo rastreamento de medição de tempo de desempenho

Execute estas etapas para fazer um rastreamento:

1.  Abra uma janela de comando como administrador.
2.  Feche o aplicativo se ele já estiver em execução.
3.  altere os diretórios para o diretório *gpuview* dentro da pasta Windows Performance Toolkit.
4.  Digite "log. cmd" para iniciar o rastreamento de eventos. Essa opção registra os eventos mais interessantes. Outras opções disponíveis registram o escopo diferente dos eventos. Por exemplo, ' v ' ou modo de log detalhado captura todos os eventos dos quais o **GPUView** está ciente.
5.  Inicie o exemplo e exerça o exemplo de uma maneira que cubra o caminho de desempenho que você precisa analisar.
6.  Volte para as janelas de comando e digite "log. cmd" novamente para parar o registro em log.
7.  Isso gera um arquivo chamado "merged. etl" na pasta *gpuview* Você pode salvar esse arquivo em outro local e pode analisá-lo no mesmo computador ou em outro. Para exibir detalhes da captura de pilha, salve o arquivo de símbolo (. pdb) associado ao aplicativo.

## <a name="measurements"></a>Medidas


> [!Note]  
> As medidas para o exemplo de realização de geometria são obtidas em uma máquina quad core com uma placa gráfica DirectX11 integrada. As medidas variam dependendo da configuração do computador.

 

Esta seção demonstra como medir as medições de tempo de inicialização, CPU e GPU por quadro. Você pode capturar um rastreamento de desempenho para o mesmo exemplo em seu computador e ver as diferenças nas várias medições.

Para analisar o rastreamento no **GPUView**, abra o arquivo "merged. ELT" usando **GPUView.exe**.

### <a name="startup-time"></a>Tempo de inicialização

O tempo de inicialização é medido pelo tempo total gasto desde o início do aplicativo até que o conteúdo seja exibido pela primeira vez na tela.

A medição de tempo de inicialização é melhor obtida seguindo as etapas listadas na seção anterior com estas variações:

-   Se você tomar as medidas de inicialização na primeira vez em que iniciar o aplicativo, ele será chamado de inicialização a frio. Isso pode variar de medidas realizadas após a inicialização do aplicativo algumas vezes em uma pequena duração de tempo. Isso é chamado de inicialização a quente. Dependendo de quantos recursos um aplicativo cria na inicialização, pode haver uma grande diferença entre os dois tempos de inicialização. Dependendo das metas do aplicativo, a medição de uma ou outra pode ser desejável.
-   Ao registrar informações de desempenho, encerre o aplicativo assim que o primeiro quadro for exibido na tela.

### <a name="calculating-start-up-time-using-gpuview"></a>Calculando o tempo de inicialização usando **GPUView**

1.  No **GPUView**, role para baixo até o processo relevante, neste caso GeometryRealization.exe.

    ![Captura de tela que mostra um exemplo de processos no GPUView.](images/profile1.png)

2.  A fila de CPU de contexto representa a carga de trabalho de gráficos na fila do hardware, mas não necessariamente sendo processada pelo hardware. Quando o arquivo de rastreamento é aberto, ele mostra todos os eventos registrados entre o momento em que o rastreamento foi tirado. Para calcular o tempo de inicialização, selecione a região de interesse, Aplique zoom na parte inicial da primeira fila de CPU de contexto (esse é o que mostra a atividade) usando Ctrl + Z. Mais informações sobre os controles **GPUView** podem ser encontradas na seção arquivo de ajuda do **GPUView** "Resumo dos controles de **GPUView** ". A figura a seguir mostra apenas o processo de GeometryRealization.exe ampliado para a primeira parte da fila de CPU de contexto. A cor da fila de CPU de contexto é denotada pelo retângulo logo abaixo da fila e os mesmos pacotes de dados de cor na fila mostram o trabalho da GPU na fila no hardware. O pacote de padrão de hachura na fila de contexto mostra o pacote atual, o que significa que o aplicativo quer que o hardware apresente o conteúdo na tela.

    ![Captura de tela que mostra exemplos de ' contexto C P b fila '.](images/profile2.png)

3.  O tempo de inicialização é a hora em que o aplicativo é iniciado pela primeira vez (nesse caso, o módulo de ponto de entrada de thread de interface do usuário SHCORE.dll) até o momento em que o contexto aparece primeiro (marcado por um pacote de hachura). A figura aqui realça a área de interesse.

    > [!Note]  
    > As informações reais atuais são representadas na fila de inverter e, portanto, o tempo necessário é estendido até que o pacote presente seja realmente concluído na fila de inverter.

     

    A barra de status completa não está visível na figura abaixo, que também mostra o tempo decorrido entre as partes destacadas. Esse é o tempo de inicialização do aplicativo. Nesse caso, para o computador mencionado acima, ele começou a ser 240ms.

    ![Captura de tela que mostra áreas de interesse em relação ao tempo de inicialização no ' contexto C P b fila '.](images/profile3.png)

### <a name="cpu-and-gpu-time-per-frame"></a>CPU e tempo de GPU por quadro

Há algumas coisas a considerar ao medir o tempo de CPU. Procure as áreas no rastreamento em que você exercitau o cenário a ser analisado. Por exemplo, no exemplo de realização de geometria, um dos cenários analisados é a transição entre o processamento de primitivos 2048 e 8192, todos não reais (como em, a geometria não é mosaico a cada quadro). O rastreamento mostra claramente a diferença na atividade de CPU e GPU antes e depois da transição no número de primitivos.

Dois cenários estão sendo analisados para calcular a CPU e o tempo de GPU por quadro. Eles são os seguintes.

-   A transição da renderização de primitivos não reais de 2048 para 8192 primitivos não reais.
-   A transição da renderização de primitivos 8192 obtidos para 8192 primitivos não reais.

Em ambos os casos, foi observado que a taxa de quadros caiu drasticamente. Medindo o tempo de CPU e GPU, a relação entre os dois, bem como alguns outros padrões no rastreamento, pode fornecer informações úteis sobre áreas problemáticas no aplicativo.

### <a name="calculating-cpu-and-gpu-time-when-2048-primitives-are-being-rendered-unrealized"></a>Calculando a CPU e a hora da GPU quando os primitivos de 2048 estão sendo renderizados não reais

1.  Abra o arquivo de rastreamento usando **GPUView.exe**.
2.  Role para baixo até o processo de GeometryRealization.exe.
3.  Selecione uma área para calcular o tempo de CPU e ampliar-a usando CTRL + Z.

    ![Captura de tela que mostra uma área selecionada para calcular o tempo C P U no ' contexto da fila de CPU '.](images/profile4.png)

4.  Mostrar informações de sincronização de v alternando entre F8. Manter o zoom em até que seja fácil ver um valor vsync de dados de forma clara. As linhas azuis são onde os horários de sincronização de v. Normalmente, isso ocorre uma vez a cada 16 MS (60 fps), mas se o DWM estiver encontrando um problema de desempenho, ele será executado mais lentamente, assim ocorrerá uma vez a cada 32 ms (30 fps). Para ter uma noção de tempo, selecione de uma barra azul para a próxima e, em seguida, examine o número de MS relatadas no canto inferior direito da janela **GPUView** .

    ![Captura de tela que mostra um exemplo de tempos de sincronização de v.](images/profile5.png)

5.  Para medir o tempo de CPU por quadro, meça o período de tempo gasto por todos os threads envolvidos na renderização. Talvez seja válido restringir o thread que se espera que seja mais relevante do ponto de vista do desempenho. Por exemplo, no exemplo de realização de geometria, o conteúdo é animação e precisa ser renderizado na tela todos os quadros que tornam o thread da interface do usuário o mais importante. Depois de determinar qual thread examinar, meça o comprimento das barras nesse thread. A média de alguns deles gera um tempo de CPU por quadro. A figura abaixo mostra o tempo gasto no thread da interface do usuário. Ele também mostra que esse tempo se ajusta bem entre duas sincronizações em v consecutivas, o que significa que está atingindo 60FPS.

    ![Captura de tela que mostra o tempo gasto no thread U I.](images/profile6.png)

    Você também pode verificar examinando a fila inverter para o período de tempo correspondente, que mostra que o DWM é capaz de apresentar todos os quadros.

    ![Captura de tela que mostra um exemplo de "inverter fila".](images/profile7.png)

6.  A hora da GPU pode ser medida da mesma maneira que o tempo de CPU. Amplie a área relevante como no caso de medição do tempo de CPU. Meça o comprimento das barras na fila de hardware da GPU com a mesma cor que a cor da fila de CPU do contexto. Desde que as barras caibam nas sincronizações de v consecutivas, o aplicativo está funcionando perfeitamente em 60FPS.

    ![Captura de tela que mostra um exemplo de "fila de hardware de GPU" exibindo informações que um aplicativo está executando às 60 F P S.](images/profile8.png)

### <a name="calculating-cpu-and-gpu-time-when-8192-primitives-are-being-rendered-unrealized"></a>Calculando a CPU e a hora da GPU quando os primitivos de 8192 estão sendo renderizados não reais

1.  Se você seguir as mesmas etapas novamente, o rastreamento mostrará que todo o trabalho de CPU para um quadro não se ajusta entre um v-Sync e o próximo. Isso significa que o aplicativo está associado à CPU. O thread da interface do usuário está saturaçãondo a CPU.

    ![Captura de tela que mostra um exemplo do thread da interface do usuário saturação o C P U.](images/profile9.png)

    Olhando para a fila inverter, também é claro que o DWM não é capaz de apresentar todos os quadros.

    ![Captura de tela que mostra um exemplo da D W M que não pode apresentar todos os quadros.](images/profile10.png)

2.  Para analisar onde o tempo está sendo gasto, abra o rastreamento no **Xperf**. Para analisar o tempo de inicialização em **Xperf**, primeiro localize o intervalo de tempo em **GPUView**. Passe o mouse sobre a esquerda do intervalo e anote o tempo absoluto mostrado na parte inferior da janela **GPUView** . Em seguida, abra o mesmo arquivo. etl em **Xperf** e role para baixo até o grafo "amostragem de CPU por CPU", clique com o botão direito e selecione "selecionar intervalo..." Isso permite digitar o intervalo de interesse que foi descoberto examinando o rastreamento de GPU.

    ![captura de tela que mostra a amostragem de c p u por C p u em ' Windows análise de desempenho '.](images/profile11.png)

3.  Vá para o menu de rastreamento e verifique se "carregar símbolos" está marcado. Além disso, acesse Trace-> configurar caminhos de símbolo e digite o caminho do símbolo do aplicativo. Um arquivo de símbolo contém informações de depuração sobre um executável compilado em um banco de dados separado (. pdb). Esse arquivo é comumente chamado de PDB. Mais informações sobre arquivos de símbolo podem ser encontradas aqui: [arquivos de símbolos](/windows/desktop/Debug/symbol-files). Esse arquivo pode estar localizado na pasta "debug" do diretório do aplicativo.

4.  Para obter a análise de onde o tempo está sendo gasto no aplicativo, clique com o botão direito do mouse no intervalo selecionado na etapa anterior e clique em tabela de resumo. Para obter uma visão geral de quanto tempo é gasto em cada DLL, desmarque "pilha" no menu "colunas". Observe que a coluna "Count" mostra quantas amostras estão dentro da dll/função fornecida. Como aproximadamente um exemplo é obtido por MS, esse número pode ser usado como uma melhor estimativa de quanto tempo é gasto em cada DLL/função. Marcar o menu "pilha" do colunas fornecerá o tempo inclusivo gasto em cada função no grafo de chamada. Isso ajudará a dividir os pontos problemáticos ainda mais.

5.  As informações de rastreamento de pilha para primitivos de 2048 não reais revela que 30% do tempo de CPU é gasto no processo de realização de geometria. Isso em cerca de 36% do tempo está sendo gasto no mosaico e no traçado da geometria.

6.  As informações de rastreamento de pilha para primitivos de 8192 não reais revela que cerca de 60% do tempo de CPU (4 núcleos) é gasto na realização de geometria.

    ![Captura de tela que mostra informações de rastreamento de pilha para o C P U time.](images/profile12.png)

### <a name="calculating-cpu-time-when-8192-primitives-are-being-rendered-realized"></a>Calculando o tempo de CPU quando os primitivos de 8192 estão sendo processados

Fica claro dos perfis que o aplicativo está associado à CPU. Para reduzir o tempo gasto pela CPU, as geometrias podem ser criadas uma vez e armazenadas em cache. O conteúdo armazenado em cache pode ser renderizado a cada quadro sem incorrer no custo de mosaico Geometry por quadro. Ao examinar o rastreamento em **GPUView** para a parte realizada do aplicativo, é claro que o DWM é capaz de apresentar todos os quadros e o tempo de CPU foi reduzido drasticamente.

![Captura de tela que mostra um exemplo de um rastreamento em GPUView mostrando D W M é capaz de apresentar todos os quadros.](images/profile13.png)

A primeira parte do grafo mostra os primitivos 8192 obtidos. O tempo de CPU correspondente por quadro é capaz de se ajustar em duas sincronizações de v consecutivas. Na parte posterior do grafo, isso não é verdade.

Olhando para o **Xperf**, a CPU fica ociosa por mais tempo, com apenas 25% do tempo de CPU gasto no aplicativo de realização de geometria.

![captura de tela gpuview.](images/profile14.png)

## <a name="summary"></a>Resumo

**GPUView** e **Xperf** e ferramentas poderosas para analisar o desempenho de aplicativos do [DirectX](/previous-versions/windows/apps/jj262109(v=win.10)) . Este artigo é um dos principais para usar essas ferramentas e entender as medidas básicas de desempenho e as características do aplicativo. Além de entender o uso de ferramentas, é importante entender o aplicativo que está sendo analisado. Comece a encontrar respostas para perguntas como o que o aplicativo está tentando atingir? Quais threads no sistema são mais importantes? Quais compensações você pretende fazer? Ao analisar rastreamentos de desempenho, comece examinando os locais problemáticos óbvios. A CPU do aplicativo ou a GPU está associada? O aplicativo é capaz de apresentar todos os quadros? Ferramentas junto com uma compreensão do aplicativo podem fornecer informações muito úteis para entender, localizar e, finalmente, resolver problemas de desempenho.

 

 