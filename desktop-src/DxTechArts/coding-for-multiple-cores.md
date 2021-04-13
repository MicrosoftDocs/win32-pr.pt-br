---
title: Codificação para vários núcleos no Xbox 360 e no Windows
description: Este tópico fornece conselhos sobre como começar a usar a programação multithread.
ms.assetid: 661f13a6-c73d-8513-2bad-0ef9d1a361a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75899dacdfba829fc1a83e9393e6aa58574c9f30
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/21/2020
ms.locfileid: "104366903"
---
# <a name="coding-for-multicore-on-xbox-360-and-windows"></a>Codificação para vários núcleos no Xbox 360 e no Windows

Durante anos, o desempenho dos processadores aumentou constantemente, e jogos e outros programas têm aproveitado os benefícios dessa crescente capacidade, sem a necessidade de fazer nada de especial.

As regras foram alteradas. O desempenho de núcleos de processador único agora está aumentando muito lentamente, se houver. No entanto, o poder de computação disponível em um computador ou console típico continua crescendo. A diferença é que a maior parte desse lucro de desempenho agora vem de ter vários núcleos de processador em um único computador, geralmente em um único chip. A CPU do Xbox 360 tem três núcleos de processador em um chip, e aproximadamente 70% dos processadores de PC vendidos no 2006 eram vários núcleos.

Os aumentos no poder de processamento disponível são tão significativos quanto no passado, mas agora os desenvolvedores precisam escrever código multithread para usar essa potência. A programação multi-threaded traz novos desafios de design e programação. Este tópico fornece conselhos sobre como começar a usar a programação multithread.

## <a name="the-importance-of-good-design"></a>A importância de um bom design

O bom design de programa multithread é essencial, mas pode ser muito difícil. Se você mover aleatoriamente seus principais sistemas de jogos para threads diferentes, provavelmente descobrirá que cada thread passa a maior parte de seu tempo aguardando os outros threads. Esse tipo de design leva a uma maior complexidade e um esforço de depuração significativo, praticamente sem nenhum ganho de desempenho.

Toda vez que os threads precisam sincronizar ou compartilhar dados, há o potencial de corrupção de dados, sobrecarga de sincronização, deadlocks e complexidade. Portanto, seu design multithread precisa documentar claramente todos os pontos de sincronização e de comunicação, e ele deve minimizar esses pontos tanto quanto possível. Onde os threads precisam se comunicar, o esforço de codificação aumentará, o que pode reduzir a produtividade se afetar muito código-fonte.

A meta de design mais simples para multithreading é dividir o código em grandes partes independentes. Se, em seguida, você restringir essas partes para se comunicar apenas algumas vezes por quadro, verá um aumento significativo do multithreading, sem complexidade indevida.

## <a name="typical-threaded-tasks"></a>Tarefas em thread típicas

Alguns tipos de tarefas têm comprovado receptivos de serem colocados em threads separados. A lista a seguir não deve ser exaustiva, mas deve dar algumas ideias.

### <a name="rendering"></a>Renderização

Renderização — que pode incluir a movimentação do grafo de cena ou, possivelmente, chamar apenas funções de D3D — muitas vezes conta com 50% ou mais de tempo de CPU. Portanto, mover o processamento para outro thread pode ter benefícios significativos. O thread de atualização pode preencher algum tipo de buffer de descrição de renderização, que o thread de renderização pode processar.

O thread de atualização do jogo sempre é um quadro à frente do thread de renderização, o que significa que ele leva dois quadros antes que as ações do usuário apareçam na tela. Embora essa latência maior possa ser um problema, a taxa de quadros aumentada da divisão da carga de trabalho geralmente mantém a latência total aceitável.

Na maioria dos casos, toda a renderização ainda é feita em um único thread, mas é um thread diferente da atualização do jogo.

O \_ sinalizador MULTITHREAD D3DCREATE, às vezes, é usado para permitir a renderização em um thread e a criação de recursos em outros threads; esse sinalizador é ignorado no Xbox 360 e você deve evitar usá-lo no Windows. No Windows, a especificação desse sinalizador força o D3D a gastar uma quantidade significativa de tempo na sincronização, tornando o thread de renderização mais lento.

### <a name="file-decompression"></a>Descompactação de arquivo

Os tempos de carregamento são sempre muito longos e o streaming de dados na memória sem afetar a taxa de quadros pode ser desafiador. Se todos os dados forem compactados agressivamente no disco, a velocidade de transferência de dados do disco rígido ou do dísco óptico será menos provável de ser um fator limitante. Em um processador de thread único, geralmente não há tempo de processador suficiente disponível para compactação para ajudar a carregar tempos. No entanto, em um sistema multiprocessador, a descompactação de arquivo usa ciclos de CPU que, de outra forma, seriam desperdiçados; Ele melhora os tempos de carregamento e o streaming; e economiza espaço no disco.

Não use a descompactação de arquivo como uma substituição para o processamento que deve ser feito durante a produção. Por exemplo, se você dedicar um thread extra para analisar dados XML durante o carregamento de nível, você não está usando multithreading para melhorar a experiência do jogador.

Ao usar um thread de descompactação de arquivo, você ainda deve usar e/s de arquivo assíncrono e leituras grandes para maximizar a eficiência da leitura de dados.

### <a name="graphics-fluff"></a>Trivialidades de gráficos

Há muitos iguarias gráficos que melhoram a aparência do jogo, mas não são estritamente necessários. Isso inclui coisas como animações de nuvem geradas em procedimentos, simulações de tecido e de cabelo, ondas de procedimentos, vegetação de procedimentos, mais partículas ou física não cheia.

Como esses efeitos não afetam o jogo, eles não causam problemas de sincronização complicados – eles podem sincronizar com os outros threads uma vez por quadro ou com menos frequência. Além disso, em jogos para Windows, esses efeitos podem agregar valor para os jogadores com CPUs de vários núcleos, enquanto são omitidos silenciosamente em computadores de núcleo único, dando uma maneira fácil de dimensionar em uma ampla gama de recursos.

### <a name="physics"></a>Física

A física geralmente não pode ser colocada em um thread separado para ser executado em paralelo com a atualização do jogo, pois a atualização do jogo geralmente requer os resultados dos cálculos de física imediatamente. A alternativa para a física multithread é executá-la em vários processadores. Embora isso possa ser feito, é uma tarefa complexa que exige acesso frequente a estruturas de dados compartilhadas. Se você puder manter a carga de trabalho da sua física baixa o suficiente para se ajustar ao thread principal, sua tarefa será mais simples.

Bibliotecas que oferecem suporte à física em execução em vários threads estão disponíveis. No entanto, isso pode levar a um problema: quando o jogo está executando a física, ele usa vários threads, mas o restante do tempo que ele usa poucos. Executar a física em vários threads exigirá resolver isso para que a carga de trabalho seja distribuída uniformemente no quadro. Se você escrever um mecanismo de física multithread, deverá prestar atenção cuidadosa a todas as estruturas de dados, pontos de sincronização e balanceamento de carga.

## <a name="example-multithreaded-designs"></a>Exemplos de designs multithread

Os jogos para Windows precisam ser executados em computadores com números diferentes de núcleos de CPU. A maioria das máquinas de jogos ainda tem apenas um núcleo, embora o número de máquinas de dois núcleos esteja crescendo rapidamente. Um jogo típico do Windows pode dividir sua carga de trabalho em um thread para atualização e renderização, com threads de trabalho opcionais para adicionar funcionalidade extra. Além disso, alguns threads em segundo plano para fazer a e/s de arquivo e a rede provavelmente seriam usados. A Figura 1 mostra os threads, juntamente com os principais pontos de transferência de dados.

**Figura 1. Design de Threading em um jogo para Windows**

![design de Threading em um jogo para Windows](images/coding-for-multiple-cores-1.gif)

Um jogo típico do Xbox 360 pode usar threads de software adicionais com uso intensivo de CPU, portanto, ele pode dividir sua carga de trabalho em um thread de atualização, thread de renderização e três threads, como mostra a Figura 2.

**Figura 2. Design de Threading em um jogo para o Xbox 360**

![design de Threading em um jogo para o Xbox 360](images/coding-for-multiple-cores-2.gif)

Com exceção da e/s de arquivo e da rede, todas essas tarefas têm o potencial de ter uso intensivo de CPU para se beneficiarem do seu próprio thread de hardware. Essas tarefas também têm o potencial de ser independente o suficiente para que possam ser executadas em um quadro inteiro sem se comunicar.

O thread de atualização de jogo gerencia a entrada do controlador, ia e física, e prepara as instruções para os outros quatro threads. Essas instruções são colocadas em buffers de Propriedade do thread de atualização do jogo, portanto, nenhuma sincronização é necessária à medida que as instruções são geradas.

No final do quadro, o thread de atualização do jogo entrega os buffers de instruções para os quatro outros threads e, em seguida, começa a trabalhar no próximo quadro, preenchendo outro conjunto de buffers de instruções.

Como os threads de atualização e de renderização funcionam em atrelada entre si, seus buffers de comunicação são simplesmente armazenados em buffer duplo: a qualquer momento, o thread de atualização está preenchendo um buffer enquanto o thread de renderização está lendo do outro.

Os outros threads de trabalho não estão necessariamente ligados à taxa de quadros. A descompactação de dados pode levar muito menos do que um quadro ou pode levar muitos quadros. Até mesmo a simulação de tecido e cabelo pode não precisar ser executada exatamente na taxa de quadros porque atualizações menos frequentes podem ser bem aceitáveis. Portanto, esses três threads precisam de estruturas de dados diferentes para se comunicar com o thread de atualização e com o thread de renderização. Cada uma delas precisa de uma fila de entrada que possa conter solicitações de trabalho, e o thread de processamento precisa de uma fila de dados que possa conter os resultados produzidos pelos threads. Ao final de cada quadro, o thread de atualização adicionará um bloco de solicitações de trabalho às filas de threads de trabalho. Adicionar à lista apenas uma vez por quadro garante que o thread de atualização Minimize a sobrecarga de sincronização. Cada um dos threads de trabalho efetua pull das atribuições da fila de trabalho da forma mais rápida possível, usando um loop semelhante a este:


```C++
for(;;)
{
    while( WorkQueueNotEmpty() )
    {
        RemoveWorkItemFromWorkQueue();
        ProcessWorkItem();
        PutResultInDataQueue();
    }
    WaitForSingleObject( hWorkSemaphore ); 
}
```



Como os dados vão dos threads de atualização para os threads de trabalho e, em seguida, para o thread de renderização, pode haver um atraso de três ou mais quadros antes que algumas ações o façam na tela. No entanto, se você atribuir tarefas tolerantes à latência para os threads de trabalho, isso não deverá ser um problema.

Um design alternativo seria ter vários threads de trabalho desenhando da mesma fila de trabalho. Isso daria um balanceamento de carga automático e tornaria mais provável que todos os threads de trabalho permaneçam ocupados.

O thread de atualização do jogo deve tomar cuidado para não dar muito trabalho aos threads de trabalho ou, caso contrário, as filas de trabalho podem crescer continuamente. Como o thread de atualização gerencia isso depende do tipo de tarefas que os threads de trabalho estão fazendo.

## <a name="simultaneous-multithreading-and-number-of-threads"></a>Vários threads e número de threads simultâneos

Todos os threads não são criados como iguais. Dois threads de hardware podem estar em chips separados, no mesmo chip ou mesmo no mesmo núcleo. A configuração mais importante para programadores de jogos a serem cientes é dois threads de hardware em um núcleo – SMT (processos de multithreading simultâneos) ou tecnologia de Hyper-Threading (tecnologia HT).

Os threads de tecnologia SMT ou HT compartilham os recursos do núcleo da CPU. Como eles compartilham as unidades de execução, a velocidade máxima de execução de dois threads em vez de um é normalmente de 10 a 20%, em vez do percentual de 100 que é possível de dois threads de hardware independentes.

Os threads de tecnologia mais significativamente, SMT ou HT compartilham a instrução L1 e os caches de dados. Se seus padrões de acesso à memória forem incompatíveis, eles poderão acabar combatendo o cache e causando muitos erros de cache. Na pior das hipóteses, o desempenho total para o núcleo da CPU pode realmente diminuir quando um segundo thread é executado. No Xbox 360, esse é um problema bastante simples. A configuração do Xbox 360 é conhecida — três núcleos de CPU cada um com dois threads de hardware — e os desenvolvedores atribuem seus threads de software a threads de CPU específicos e podem medir para ver se seu design de Threading oferece desempenho extra.

No Windows, a situação é mais complicada. O número de threads e sua configuração variam de computador para computador, e a determinação da configuração é complicada. A função [**GetLogicalProcessorInformation**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformation) fornece informações sobre a relação entre diferentes threads de hardware, e essa função está disponível no Windows Vista, no Windows 7 e no Windows XP SP3. Portanto, por enquanto, você precisa usar a instrução CPUID e os algoritmos fornecidos pela Intel e AMD para decidir quantos threads "reais" estão disponíveis. Consulte as referências para obter mais informações.

O exemplo de CoreDetection no SDK do DirectX contém um código de exemplo que usa a função [**GetLogicalProcessorInformation**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformation) ou a instrução CPUID para retornar a topologia de núcleo da CPU. A instrução CPUID será usada se **GetLogicalProcessorInformation** não tiver suporte na plataforma atual. CoreDetection pode ser encontrado nos seguintes locais:

<dl> <dt>

<span id="Source_"></span><span id="source_"></span><span id="SOURCE_"></span>Original
</dt> <dd>

Raiz do SDK do *DirectX* \\ Exemplos de \\ CoreDetection de C++ \\ misc \\

</dd> <dt>

<span id="Executable_"></span><span id="executable_"></span><span id="EXECUTABLE_"></span>Executá
</dt> <dd>

Raiz do SDK do *DirectX* \\ Amostras \\ de \\ \\CoreDetection.exe misc \\ bin do C++

</dd> </dl>

A suposição mais segura é não ter mais de um thread com uso intensivo de CPU por núcleo de CPU. Ter mais threads com uso intensivo de CPU que os núcleos de CPU oferece pouco ou nenhum benefício e traz a sobrecarga extra e a complexidade de threads adicionais.

## <a name="creating-threads"></a>Criando threads

A criação de threads é uma operação bastante simples, mas há muitos erros potenciais. O código a seguir mostra a maneira apropriada de criar um thread, aguardando que ele seja encerrado e, em seguida, limpando.


```C++
const int stackSize = 65536;
HANDLE hThread = (HANDLE)_beginthreadex( 0, stackSize,
            ThreadFunction, 0, 0, 0 );
// Do work on main thread here.
// Wait for child thread to complete
WaitForSingleObject( hThread, INFINITE );
CloseHandle( hThread );

...

unsigned __stdcall ThreadFunction( void* data )
{
#if _XBOX_VER >= 200
    // On Xbox 360 you must explicitly assign
    // software threads to hardware threads.
    XSetThreadProcessor( GetCurrentThread(), 2 );
#endif
    // Do child thread work here.
    return 0;
}
```



Ao criar um thread, você tem a opção de especificar o tamanho da pilha para o thread filho ou especificar zero. nesse caso, o thread filho herdará o tamanho da pilha do thread pai. No Xbox 360, em que as pilhas são totalmente confirmadas quando o thread é iniciado, a especificação de zero pode perder memória significativa, pois muitos threads filho não precisarão tanto de pilha como o pai. No Xbox 360, também é importante que o tamanho da pilha seja um múltiplo de 64 KB.

Se você usar a função [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) para criar threads, o tempo de execução do C/C++ (CRT) não será inicializado corretamente no Windows. É recomendável usar a função [**\_ BEGINTHREADEX**](https://msdn.microsoft.com/library/ms397047(v=VS.70).aspx) do CRT em vez disso.

O valor de retorno de [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) ou [**\_ beginthreadex**](https://msdn.microsoft.com/library/ms397047(v=VS.70).aspx) é um identificador de thread. Esse thread pode ser usado para aguardar a finalização do thread filho, o que é muito mais simples e muito mais eficiente do que a rotação em um loop verificando o status do thread. Para aguardar até que o thread seja encerrado, basta chamar [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) com o identificador de thread.

Os recursos para o thread não serão liberados até que o thread seja encerrado e o identificador de thread tenha sido fechado. Portanto, é importante fechar o identificador de thread com [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) quando você terminar. Se você estiver aguardando o thread terminar com [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject), não se esqueça de fechar o identificador até que a espera seja concluída.

No Xbox 360, você deve atribuir explicitamente threads de software a um determinado thread de hardware usando **XSetThreadProcessor**. Caso contrário, todos os threads filho permanecerão no mesmo thread de hardware que o pai. No Windows, você pode usar o [**SetThreadAffinityMask**](/windows/win32/api/winbase/nf-winbase-setthreadaffinitymask) para sugerir fortemente para o sistema operacional em que threads de hardware seu thread deve ser executado. Essa técnica deve, em geral, ser evitada no Windows, já que você não sabe quais outros processos podem estar em execução no sistema. Normalmente, é melhor permitir que o Agendador do Windows atribua seus threads a threads de hardware ociosos.

A criação de threads é uma operação cara. Os threads devem ser criados e destruídos raramente. Se você quiser criar e destruir threads com frequência, use um pool de threads que esperam pelo trabalho em vez disso.

## <a name="synchronizing-threads"></a>Sincronizando threads

Para que vários threads funcionem juntos, você deve ser capaz de sincronizar threads, passar mensagens e solicitar acesso exclusivo aos recursos. O Windows e o Xbox 360 vêm com um rico conjunto de primitivos de sincronização. Para obter detalhes completos sobre esses primitivos de sincronização, consulte a documentação da plataforma.

### <a name="exclusive-access"></a>Acesso exclusivo

Obter acesso exclusivo a um recurso, estrutura de dados ou caminho de código é uma necessidade comum. Uma opção para obter acesso exclusivo é um mutex, cujo uso típico é mostrado aqui.


```C++
// Initialize
HANDLE mutex = CreateMutex( 0, FALSE, 0 );

// Use
void ManipulateSharedData()
{
    WaitForSingleObject( mutex, INFINITE );
    // Manipulate stuff...
    ReleaseMutex( mutex );
}

// Destroy
CloseHandle( mutex );
The kernel guarantees that, for a particular mutex, only one thread at a time can 
acquire it.
The main disadvantage to mutexes is that they are relatively expensive to acquire 
and release. A faster alternative is a critical section.
// Initialize
CRITICAL_SECTION cs;
InitializeCriticalSection( &cs );

// Use
void ManipulateSharedData()
{
    EnterCriticalSection( &cs );
    // Manipulate stuff...
    LeaveCriticalSection( &cs );
}

// Destroy
DeleteCriticalSection( &cs );
```



As seções críticas têm semântica semelhante a mutexes, mas podem ser usadas para sincronizar somente dentro de um processo, não entre processos. Sua principal vantagem é que eles são executados aproximadamente vinte vezes mais rápido do que os mutexes.

### <a name="events"></a>Eventos

Se dois threads — talvez um thread de atualização e um thread de renderização — estiverem usando um par de buffers de descrição de renderização, eles precisarão de uma maneira de indicar quando eles são concluídos com seu buffer específico. Isso pode ser feito associando um evento (alocado com [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa)) a cada buffer. Quando um thread é concluído com um buffer, ele pode usar [**SetEvent**](/windows/win32/api/synchapi/nf-synchapi-setevent) para sinalizar isso e pode chamar [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) no evento do outro buffer. Essa técnica extrapola facilmente a um buffer triplo de recursos.

### <a name="semaphores"></a>Semáforos

Um semáforo é usado para controlar quantos threads podem ser executados e é comumente usado para implementar filas de trabalho. Um thread adiciona trabalho a uma fila e usa [**ReleaseSemaphore**](/windows/win32/api/synchapi/nf-synchapi-releasesemaphore) sempre que adiciona um novo item à fila. Isso permite que um thread de trabalho seja liberado do pool de threads em espera. Os threads de trabalho apenas chamam [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject)e, quando eles são retornados, há um item de trabalho na fila para eles. Além disso, uma seção crítica ou outra técnica de sincronização deve ser usada para garantir o acesso seguro à fila de trabalho compartilhada.

### <a name="avoid-suspendthread"></a>Evitar SuspendThread

Às vezes, quando você deseja que um thread pare o que está fazendo, é tentador usar [**SuspendThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread) em vez dos primitivos de sincronização corretos. Essa é sempre uma ideia inadequada e pode facilmente causar deadlocks e outros problemas. **SuspendThread** também interage incorretamente com o depurador do Visual Studio. Evite **SuspendThread**. Em vez disso, use [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) .

### <a name="waitforsingleobject-and-waitformultipleobjects"></a>WaitForSingleObject e WaitForMultipleObjects

A função [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) é a função de sincronização mais comumente usada. No entanto, às vezes você deseja que um thread aguarde até que várias condições sejam atendidas simultaneamente ou até que um de um conjunto de condições seja atendido. Nesse caso, você deve usar [**WaitForMultipleObjects**](/windows/win32/api/synchapi/nf-synchapi-waitformultipleobjects).

### <a name="interlocked-functions-and-lockless-programming"></a>Funções intercadeados e programação de bloqueio

Há uma família de funções para executar operações simples de thread-safe sem usar bloqueios. Essas são as famílias de funções intercadeados, como [**InterlockedIncrement**](/windows/win32/api/winnt/nf-winnt-interlockedincrement). Essas funções, além de outras técnicas que usam uma configuração cuidadosa dos sinalizadores, são conhecidas como programação de bloqueio. A programação sem bloqueio pode ser extremamente complicada para fazer corretamente e é substancialmente mais difícil no Xbox 360 do que no Windows.

Para obter mais informações sobre programação sem bloqueios, consulte [considerações de programação de bloqueio para o Xbox 360 e o Microsoft Windows](./lockless-programming.md).

### <a name="minimizing-synchronization"></a>Minimizando a sincronização

Alguns métodos de sincronização são mais rápidos do que outros. No entanto, em vez de otimizar seu código escolhendo as técnicas de sincronização mais rápidas possíveis, geralmente é melhor sincronizar com menos frequência. Isso é mais rápido do que a sincronização com muita frequência e torna o código mais simples que é mais fácil de depurar.

Algumas operações, como a alocação de memória, podem precisar usar primitivos de sincronização para funcionar corretamente. Portanto, fazer alocações frequentes do heap compartilhado padrão resultará em uma sincronização frequente, o que perderá algum desempenho. Evitar alocações frequentes ou usar heaps por thread (usando HEAP \_ sem \_ serialização se você usar HeapCreate) pode evitar essa sincronização oculta.

Outra causa da sincronização oculta é o D3DCREATE \_ multithread, que faz com que o D3D no Windows Use a sincronização em várias operações. (O sinalizador é ignorado no Xbox 360.)

Os dados por thread, também conhecidos como armazenamento local de thread, podem ser uma maneira importante de evitar a sincronização. Visual C++ permite declarar variáveis globais como sendo por thread com a sintaxe **\_ \_ declspec (thread)** .


```C++
__declspec( thread ) int tls_i = 1;
```



Isso fornece a cada thread no processo sua própria cópia do TLS \_ i, que pode ser referenciado com segurança e eficiência sem a necessidade de sincronização.

A técnica de **\_ \_ declspec (thread)** não funciona com DLLs carregadas dinamicamente. Se você usar DLLs carregadas dinamicamente, será necessário usar a família de funções TLSAlloc para implementar o armazenamento local de thread.

## <a name="destroying-threads"></a>Destruindo threads

A única maneira segura de destruir um thread é fazer com que o próprio thread saia, seja retornando da função de thread principal ou fazendo com que a chamada de thread [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread) ou [**\_ endthreadex**](https://msdn.microsoft.com/library/hw264s73(v=VS.71).aspx). Se um thread for criado com [**\_ beginthreadex**](https://msdn.microsoft.com/library/ms397047(v=VS.70).aspx), ele deverá usar **\_ endthreadex** ou retornar da função de thread principal, pois o uso do **ExitThread** não liberará corretamente os recursos de CRT. Nunca chame a função [**TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread) , pois o thread não será limpo corretamente. Os threads sempre devem confirmar suicida — eles nunca devem ser Murdered.

## <a name="openmp"></a>OpenMP

O OpenMP é uma extensão de linguagem para adicionar multithread ao seu programa usando pragmas para guiar o compilador em paralelizar loops. O OpenMP tem suporte pelo Visual C++ 2005 no Windows e no Xbox 360 e pode ser usado em conjunto com o gerenciamento manual de threads. O OpenMP pode ser uma maneira conveniente de multithread partes do seu código, mas é improvável que seja a solução ideal, especialmente para jogos. O OpenMP pode ser mais aplicável a tarefas de produção de execução mais longa, como o processamento de arte e outros recursos. Para obter mais informações, consulte a documentação do Visual C++ ou vá para o [site](https://www.openmp.org/)de OpenMP.

## <a name="profiling"></a>Criação de perfil

A criação de perfil multithread é importante. É fácil terminar com interrupções longas em que os threads estão aguardando uns aos outros. Essas vagas podem ser difíceis de encontrar e diagnosticar. Para ajudar a identificá-los, considere adicionar instrumentação às suas chamadas de sincronização. Um criador de perfil de amostragem também pode ajudar a identificar esses problemas porque ele pode registrar informações de tempo sem alterá-los substancialmente.

## <a name="timing"></a>Timing

A instrução RDTSC é uma maneira de obter informações precisas sobre o tempo no Windows. Infelizmente, o RDTSC tem vários problemas que o tornam uma opção inadequada para o seu título de entrega. Os contadores RDTSC não são necessariamente sincronizados entre CPUs, portanto, quando o thread se move entre os threads de hardware, você pode obter diferenças grandes positivos ou negativas. Dependendo das configurações de gerenciamento de energia, a frequência na qual o contador RDTSC é incrementado também pode mudar à medida que seu jogo é executado. Para evitar essas dificuldades, você deve preferir [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) e [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) para o tempo de alta precisão em seu jogo de envio. Para obter mais informações sobre o tempo, consulte os [processadores de tempo de jogo e vários núcleos](./game-timing-and-multicore-processors.md).

## <a name="debugging"></a>Depuração

O Visual Studio dá suporte total à depuração multithread para Windows e Xbox 360. A janela threads do Visual Studio permite alternar entre threads a fim de ver as diferentes pilhas de chamadas e variáveis locais. A janela threads também permite congelar e descongelar Threads específicos.

No Xbox 360, você pode usar a Metavariável **\@ hwthread** na janela Watch para mostrar o thread de hardware no qual o thread de software selecionado no momento está em execução.

A janela threads é mais fácil de usar se você nomear seus threads de forma significativa. O Visual Studio e outros depuradores da Microsoft permitem que você nomeie seus threads. Implemente a seguinte função **SetThreadName** e chame-a de cada thread à medida que ela é iniciada.


```C++
typedef struct tagTHREADNAME_INFO
{
    DWORD dwType;     // must be 0x1000
    LPCSTR szName;    // pointer to name (in user address space)
    DWORD dwThreadID; // thread ID (-1 = caller thread)
    DWORD dwFlags;    // reserved for future use, must be zero
} THREADNAME_INFO;

void SetThreadName( DWORD dwThreadID, LPCSTR szThreadName )
{
    THREADNAME_INFO info;
    info.dwType = 0x1000;
    info.szName = szThreadName;
    info.dwThreadID = dwThreadID;
    info.dwFlags = 0;

    __try
    {
        RaiseException( 0x406D1388, 0,
                    sizeof(info) / sizeof(DWORD),
            (DWORD*)&info );
    }
    __except( EXCEPTION_CONTINUE_EXECUTION ) {
    }
}

// Example usage:
SetThreadName(-1, "Main thread");
```



O depurador de kernel (KD) e o WinDBG também oferecem suporte à depuração multithread.

## <a name="testing"></a>Teste

A programação multithread pode ser complicada e alguns bugs multissegmentados mostram apenas raramente, dificultando a localização e a correção. Uma das melhores maneiras de liberá-las é testar uma grande variedade de computadores, especialmente aqueles com quatro ou mais processadores. O código multithread que funciona perfeitamente em um computador de thread único pode falhar instantaneamente em um computador com quatro processadores. As características de desempenho e de tempo das CPUs AMD e Intel podem variar substancialmente, portanto, certifique-se de testar computadores com vários processadores com base em CPUs de ambos os fornecedores.

## <a name="windows-vista-and-windows-7-improvements"></a>Aprimoramentos do Windows Vista e do Windows 7

Para jogos visando as versões mais recentes do Windows, há várias APIs que podem simplificar a criação de aplicativos multithread escalonáveis. Isso é particularmente verdadeiro com a nova API ThreadPool e alguns primitivos syncrhonziation adicionais (variáveis de condição, o bloqueio de leitura/gravação fino e a inicialização única). Você pode encontrar uma visão geral dessas tecnologias nos seguintes artigos da MSDN Magazine:

-   [Melhorar a escalabilidade com novas APIs de pool de threads](/archive/msdn-magazine/2007/october/pooled-threads-improve-scalability-with-new-thread-pool-apis)
-   [Novos primitivos de sincronização no Windows Vista](/archive/msdn-magazine/2007/june/concurrency-synchronization-primitives-new-to-windows-vista)

Os aplicativos que usam os [recursos do Direct3D 11](../direct3d11/direct3d-11-features.md) nesses sistemas operacionais também podem aproveitar o novo design para a criação de objetos simultâneos e listas de comandos de contexto deferidas para uma melhor escalabilidade para renderização multi-threaded.

## <a name="summary"></a>Resumo

Com um design cuidadoso que minimiza as interações entre threads, você pode obter ganhos substanciais de desempenho de programação multithread sem adicionar complexidade excessiva ao seu código. Isso permitirá que o código de jogos passe pela próxima onda de aprimoramentos do processador e forneça experiências de jogos mais atraentes.

## <a name="references"></a>Referências

-   Jim Beveridge & Robert Weiner, *aplicativos multithreading no Win32*, Addison-Wesley, 1997
-   Chuck Walbourn, [tempo de jogo e processadores de vários núcleos](./game-timing-and-multicore-processors.md), Microsoft Corporation, 2005
-   Biblioteca MSDN: [ **GetLogicalProcessorInformation**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformation)
-   [OpenMP](https://www.openmp.org/)

 

 