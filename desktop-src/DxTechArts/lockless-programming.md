---
title: Considerações sobre programação sem bloqueio para Xbox 360 e Microsoft Windows
description: Este artigo fornece uma visão geral de alguns dos problemas a serem considerados ao tentar usar técnicas de programação de bloqueio.
ms.assetid: 44700352-a791-7ef7-0858-146214b0e3da
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23bf8d66cada8aff00735fe6d6ac2d4f1369bc32
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/21/2020
ms.locfileid: "103917777"
---
# <a name="lockless-programming-considerations-for-xbox-360-and-microsoft-windows"></a>Considerações sobre programação sem bloqueio para Xbox 360 e Microsoft Windows

A programação sem bloqueios é uma maneira de compartilhar com segurança dados de alteração entre vários threads e não o custo de aquisição e liberação de bloqueios. Isso parece uma solução completa, mas a programação sem bloqueio é complexa e sutil e, às vezes, não oferece os benefícios que ele promete. A programação de bloqueio é particularmente complexa no Xbox 360.

A programação sem bloqueios é uma técnica válida para programação multithread, mas não deve ser usada com pouco cuidado. Antes de usá-lo, você deve entender as complexidades, e deve medir atentamente para garantir que realmente esteja dando a você os ganhos esperados. Em muitos casos, há soluções mais simples e mais rápidas, como o compartilhamento de dados com menos frequência, que deve ser usado em vez disso.

Usar a programação sem bloqueio de forma correta e segura exige um conhecimento significativo do seu hardware e do seu compilador. Este artigo fornece uma visão geral de alguns dos problemas a serem considerados ao tentar usar técnicas de programação de bloqueio.

## <a name="programming-with-locks"></a>Programando com bloqueios

Ao escrever código multi-threaded, é muitas vezes necessário compartilhar dados entre threads. Se vários threads estiverem lendo e gravando as estruturas de dados compartilhadas simultaneamente, a corrupção de memória poderá ocorrer. A maneira mais simples de resolver esse problema é usar bloqueios. Por exemplo, se ManipulateSharedData só deve ser executado por um thread por vez, uma seção crítica \_ pode ser usada para garantir isso, como no código a seguir:

``` syntax
// Initialize
CRITICAL_SECTION cs;
InitializeCriticalSection(&cs);

// Use
void ManipulateSharedData()
{
    EnterCriticalSection(&cs);
    // Manipulate stuff...
    LeaveCriticalSection(&cs);
}

// Destroy
DeleteCriticalSection(&cs);
```

Esse código é razoavelmente simples e direto, e é fácil dizer que está correto. No entanto, a programação com bloqueios vem com várias desvantagens em potencial. Por exemplo, se dois threads tentarem adquirir os mesmos dois bloqueios, mas adquiri-los em uma ordem diferente, você poderá ter um deadlock. Se um programa mantiver um bloqueio por muito tempo — devido a um design insatisfatório ou porque o thread foi trocado por um thread de prioridade mais alta — outros threads poderão ser bloqueados por um longo tempo. Esse risco é particularmente ótimo no Xbox 360 porque os threads de software são atribuídos a um thread de hardware pelo desenvolvedor, e o sistema operacional não os moverá para outro thread de hardware, mesmo se um estiver ocioso. O Xbox 360 também não tem proteção contra a inversão de prioridade, em que um thread de alta prioridade gira em um loop enquanto aguarda um thread de baixa prioridade liberar um bloqueio. Finalmente, se uma chamada de procedimento deferida ou uma rotina de serviço de interrupção tentar adquirir um bloqueio, você poderá obter um deadlock.

Apesar desses problemas, os primitivos de sincronização, como seções críticas, geralmente são a melhor maneira de coordenar vários threads. Se os primitivos de sincronização forem muito lentos, a melhor solução geralmente será usá-los com menos frequência. No entanto, para aqueles que podem arcar com a complexidade extra, outra opção é a programação de bloqueio.

## <a name="lockless-programming"></a>Programação de bloqueio

A programação sem bloqueio, como o nome sugere, é uma família de técnicas para a manipulação segura de dados compartilhados com a utilização de bloqueios. Há algoritmos de bloqueio disponíveis para passar mensagens, compartilhar listas e filas de dados e outras tarefas.

Ao fazer uma programação sem bloqueios, há dois desafios com os quais você deve lidar: operações não atômicas e reordenação.

## <a name="non-atomic-operations"></a>Operações não atômicas

Uma operação atômica é uma que é indivisível – uma em que outros threads são garantidos para nunca ver a operação quando ela é metade concluída. As operações atômicas são importantes para a programação de bloqueio, porque sem elas, outros threads podem ver valores de meia gravação ou estado inconsistente.

Em todos os processadores modernos, você pode assumir que leituras e gravações de tipos nativos alinhados naturalmente são atômicas. Desde que o barramento de memória seja pelo menos tão largo quanto o tipo que está sendo lido ou gravado, a CPU lê e grava esses tipos em uma única transação de barramento, tornando impossível para outros threads vê-los em um estado de metade concluída. Em x86 e x64, não há garantia de que leituras e gravações maiores que oito bytes são atômicas. Isso significa que leituras de 16 bytes e gravações de registros SSE (Streaming SIMD Extension) e operações de cadeia de caracteres podem não ser atômicas.

Leituras e gravações de tipos que não são naturalmente alinhados — por exemplo, escrever DWORDs que cruzam limites de quatro bytes — não têm garantia de ser atômica. A CPU pode precisar fazer essas leituras e gravações como várias transações de barramento, o que pode permitir que outro thread modifique ou veja os dados no meio da leitura ou gravação.

As operações de composição, como a sequência Read-Modify-Write, que ocorre quando você incrementa uma variável compartilhada, não são atômicas. No Xbox 360, essas operações são implementadas como várias instruções (LWZ, por e STW), e o thread pode ser trocado de MSRC durante por meio da sequência. Em x86 e x64, há uma única instrução (Inc) que pode ser usada para incrementar uma variável na memória. Se você usar essa instrução, incrementar uma variável é atômica em sistemas de processador único, mas ele ainda não é atômico em sistemas com vários processadores. A criação de sistemas com vários processadores baseados em x86 e x64 requer o uso do prefixo de bloqueio, o que impede que outro processador faça sua própria sequência de leitura-modificação-gravação entre a leitura e a gravação da instrução Inc.

O código a seguir mostra alguns exemplos:

``` syntax
// This write is not atomic because it is not natively aligned.
DWORD* pData = (DWORD*)(pChar + 1);
*pData = 0;

// This is not atomic because it is three separate operations.
++g_globalCounter;

// This write is atomic.
g_alignedGlobal = 0;

// This read is atomic.
DWORD local = g_alignedGlobal;
```

## <a name="guaranteeing-atomicity"></a>Garantindo a atomicidade

Você pode ter certeza de que está usando operações atômicas por uma combinação do seguinte:

-   Operações atômicas naturalmente
-   Bloqueios para encapsule as operações compostas
-   Funções do sistema operacional que implementam versões atômicas de operações de composição populares

Incrementar uma variável não é uma operação atômica e incrementar pode levar à corrupção de dados, se executado em vários threads.

``` syntax
// This will be atomic.
g_globalCounter = 0;

// This is not atomic and gives undefined behavior
// if executed on multiple threads
++g_globalCounter;
```

O Win32 vem com uma família de funções que oferecem versões atômicas de leitura-modificação-gravação de várias operações comuns. Essas são as InterlockedXxx da família de funções. Se todas as modificações da variável compartilhada usarem essas funções, as modificações serão seguras para thread.

``` syntax
// Incrementing our variable in a safe lockless way.
InterlockedIncrement(&g_globalCounter);
```

## <a name="reordering"></a>Reordenação

Um problema mais sutil é A reordenação. Leituras e gravações nem sempre ocorrem na ordem em que foram gravadas em seu código, e isso pode levar a problemas muito confusos. Em muitos algoritmos multi-threaded, um thread grava alguns dados e, em seguida, grava em um sinalizador que informa a outros threads que os dados estão prontos. Isso é conhecido como uma versão de gravação. Se as gravações forem reordenadas, outros threads poderão ver que o sinalizador está definido antes que possam ver os dados gravados.

Da mesma forma, em muitos casos, um thread lê de um sinalizador e, em seguida, lê alguns dados compartilhados se o sinalizador diz que o thread adquiriu o acesso aos dados compartilhados. Isso é conhecido como leitura-aquisição. Se as leituras forem reordenadas, os dados poderão ser lidos do armazenamento compartilhado antes do sinalizador, e os valores vistos podem não estar atualizados.

A reordenação de leituras e gravações pode ser feita pelo compilador e pelo processador. Os compiladores e os processadores fizeram essa reordenação por anos, mas em máquinas com um único processador ele era menos um problema. Isso ocorre porque a reorganização de CPU de leituras e gravações é invisível em máquinas com um único processador (para código que não é um driver de dispositivo que não faz parte de um driver de dispositivo), e a reorganização do compilador de leituras e gravações é menos provável de causar problemas em máquinas de processador único.

Se o compilador ou a CPU reorganizar as gravações mostradas no código a seguir, outro thread poderá ver que o sinalizador Alive está definido enquanto ainda vê os valores antigos para x ou y. A reorganização semelhante pode ocorrer durante a leitura.

Nesse código, um thread adiciona uma nova entrada à matriz Sprite:

``` syntax
// Create a new sprite by writing its position into an empty
// entry and then setting the ‘alive' flag. If ‘alive' is
// written before x or y then errors may occur.
g_sprites[nextSprite].x = x;
g_sprites[nextSprite].y = y;
g_sprites[nextSprite].alive = true;
```

Neste próximo bloco de código, outro thread lê a partir da matriz Sprite:

``` syntax
// Draw all sprites. If the reads of x and y are moved ahead of
// the read of ‘alive' then errors may occur.
for( int i = 0; i < numSprites; ++i )
{
    if( g_sprites[nextSprite].alive )
    {
        DrawSprite( g_sprites[nextSprite].x,
                g_sprites[nextSprite].y );
    }
}
```

Para tornar esse sistema Sprite seguro, precisamos impedir a reordenação do compilador e da CPU de leituras e gravações.

### <a name="understanding-cpu-rearrangement-of-writes"></a>Compreendendo a reorganização da CPU de gravações

Algumas CPUs reorganizam as gravações para que elas sejam visíveis externamente para outros processadores ou dispositivos em ordem não programada. Essa reorganização nunca é visível para um código de não driver de thread único, mas pode causar problemas no código multi-threaded.

### <a name="xbox-360"></a>Xbox 360

Embora a CPU 360 do Xbox não reordene as instruções, ela reorganiza as operações de gravação, que são concluídas após as próprias instruções. Essa reorganização de gravações é especificamente permitida pelo modelo de memória PowerPC.

As gravações no Xbox 360 não vão diretamente para o cache L2. Em vez disso, para melhorar a largura de banda de gravação do cache L2, elas passam por filas de armazenamento e, em seguida, para armazenar buffers de coleta. Os buffers de coleta de armazenamento permitem que os blocos de 64 bytes sejam gravados no cache L2 em uma única operação. Há oito buffers de coleta de armazenamento, que permitem a gravação eficiente em várias áreas de memória diferentes.

Os buffers de coleta de armazenamento normalmente são gravados no cache L2 na ordem FIFO (primeiro a entrar, primeiro a sair). No entanto, se a linha de cache de destino de uma gravação não estiver no cache L2, essa gravação poderá ser atrasada enquanto a linha de cache for buscada da memória.

Mesmo quando os buffers do Store-gather são gravados no cache L2 na ordem FIFO estrita, isso não garante que as gravações individuais sejam gravadas no cache L2 na ordem. Por exemplo, imagine que a CPU grava no local 0x1000, em seguida, no local 0x2000 e no local 0x1004. A primeira gravação aloca um buffer de coleta de armazenamento e o coloca na frente da fila. A segunda gravação aloca outro buffer de coleta de armazenamento e a coloca em seguida na fila. A terceira gravação adiciona seus dados ao primeiro buffer de coleta de armazenamento, que permanece na frente da fila. Assim, a terceira gravação acaba indo até o cache L2 antes da segunda gravação.

A reordenação causada por buffers de coleta de armazenamento é fundamentalmente imprevisível, especialmente porque ambos os threads em um núcleo compartilham buffers de coleta de armazenamento, tornando a alocação e o esvaziamento da Store-coletar buffers de forma altamente variável.

Este é um exemplo de como as gravações podem ser reordenadas. Pode haver outras possibilidades.

### <a name="x86-and-x64"></a>x86 e x64

Embora as CPUs x86 e x64 façam instruções de reordenação, elas geralmente não reordenam operações de gravação em relação a outras gravações. Há algumas exceções para a memória combinada de gravação. Além disso, as operações de cadeia de caracteres (MOVS e STOS) e as gravações SSE de 16 bytes podem ser reordenadas internamente, mas de outra forma, as gravações não são reordenadas em relação umas às outras.

### <a name="understanding-cpu-rearrangement-of-reads"></a>Entendendo a reorganização de leituras da CPU

Algumas CPUs reorganizam as leituras para que elas venham efetivamente do armazenamento compartilhado em ordem de não programa. Essa reorganização nunca é visível para um código de não driver de thread único, mas pode causar problemas no código multi-threaded.

### <a name="xbox-360"></a>Xbox 360

Os erros de cache podem fazer com que algumas leituras sejam atrasadas, o que efetivamente faz com que as leituras venham da memória compartilhada fora de ordem, e o tempo desses erros de cache é fundamentalmente imprevisível. A pré-busca e a previsão de ramificação também podem fazer com que os dados sejam provenientes da memória compartilhada fora de ordem. Esses são apenas alguns exemplos de como as leituras podem ser reordenadas. Pode haver outras possibilidades. Essa reorganização de leituras é especificamente permitida pelo modelo de memória PowerPC.

### <a name="x86-and-x64"></a>x86 e x64

Embora as CPUs x86 e x64 façam instruções de reordenação, elas geralmente não reordenam operações de leitura em relação a outras leituras. As operações de cadeia de caracteres (MOVS e STOS) e as leituras SSE de 16 bytes podem ser reordenadas internamente, mas do contrário, as leituras não são reordenadas em relação umas às outras.

### <a name="other-reordering"></a>Outra reordenação

Embora as CPUs x86 e x64 não reordenem as gravações em relação a outras gravações ou reordenem as leituras relativas a outras leituras, elas podem reordenar as leituras em relação às gravações. Especificamente, se um programa gravar em um local seguido da leitura de um local diferente, os dados de leitura poderão vir da memória compartilhada antes que os dados gravados o façam. Essa reordenação pode interromper alguns algoritmos, como os algoritmos de exclusão mútua do Dekker. No algoritmo do Dekker, cada thread define um sinalizador para indicar que ele deseja inserir a região crítica e, em seguida, verifica o sinalizador do outro thread para ver se o outro thread está na região crítica ou tentando inseri-lo. O código inicial é mostrado a seguir.

``` syntax
volatile bool f0 = false;
volatile bool f1 = false;

void P0Acquire()
{
    // Indicate intention to enter critical region
    f0 = true;
    // Check for other thread in or entering critical region
    while (f1)
    {
        // Handle contention.
    }
    // critical region
    ...
}


void P1Acquire()
{
    // Indicate intention to enter critical region
    f1 = true;
    // Check for other thread in or entering critical region
    while (f0)
    {
        // Handle contention.
    }
    // critical region
    ...
}
```

O problema é que a leitura de F1 no P0Acquire pode ler do armazenamento compartilhado antes que a gravação em F0 o torne para o armazenamento compartilhado. Enquanto isso, a leitura de F0 no P1Acquire pode ler do armazenamento compartilhado antes que a gravação para F1 o faça no armazenamento compartilhado. O efeito líquido é que ambos os threads definem seus sinalizadores como TRUE e os dois threads veem o sinalizador do outro thread como falso, para que ambos insiram a região crítica. Portanto, embora problemas com a reordenação em sistemas baseados em x86 e x64 sejam menos comuns do que no Xbox 360, eles definitivamente ainda podem acontecer. O algoritmo do Dekker não funcionará sem barreiras de memória de hardware em nenhuma dessas plataformas.

as CPUs x86 e x64 não reordenarão uma gravação antecipada de uma leitura anterior. CPUs x86 e x64 apenas reordenam leituras antecipadas de gravações anteriores se direcionarem locais diferentes.

As CPUs PowerPC podem reordenar as leituras à frente de gravações e podem reordenar as gravações antes de leituras, desde que sejam para endereços diferentes.

### <a name="reordering-summary"></a>Reordenando Resumo

A CPU do Xbox 360 Reordena as operações de memória de forma muito mais agressiva do que as CPUs x86 e x64, conforme mostrado na tabela a seguir. Para obter mais detalhes, consulte a documentação do processador.



| Reordenando atividade           | x86 e x64 | Xbox 360 |
|-------------------------------|-------------|----------|
| Leituras em movimento à frente de leituras   | Não          | Sim      |
| Gravações em movimento à frente de gravações | Não          | Sim      |
| Gravações em movimento à frente de leituras  | Não          | Sim      |
| Leituras em movimento à frente de gravações  | Sim         | Sim      |



 

## <a name="read-acquire-and-write-release-barriers"></a>Barreiras de Read-Acquire e Write-Release

As principais construções usadas para impedir a reordenação de leituras e gravações são chamadas de barreiras de leitura e aquisição de gravação. Uma leitura-aquisição é uma leitura de um sinalizador ou outra variável para obter a propriedade de um recurso, juntamente com uma barreira contra reordenação. Da mesma forma, um Write-Release é uma gravação de um sinalizador ou outra variável para deixar a propriedade de um recurso, acoplada a uma barreira contra reordenação.

As definições formais, cortesia de Herb Sutter, são:

-   Uma aquisição de leitura/execução antes de todas as leituras e gravações pelo mesmo thread que a segue em ordem de programa.
-   Uma versão de gravação é executada após todas as leituras e gravações pelo mesmo thread que a precede na ordem do programa.

Quando o código adquire a propriedade de alguma memória adquirindo um bloqueio ou puxando um item de uma lista compartilhada vinculada (sem um bloqueio), sempre há uma leitura envolvida — testando um sinalizador ou ponteiro para ver se a propriedade da memória foi adquirida. Essa leitura pode fazer parte de uma operação **InterlockedXxx** ; nesse caso, ela envolve uma leitura e uma gravação, mas é a leitura que indica se a propriedade foi obtida. Depois que a propriedade da memória é adquirida, os valores são normalmente lidos ou gravados nessa memória, e é muito importante que essas leituras e gravações sejam executadas após a aquisição da propriedade. Uma barreira de leitura/aquisição garante isso.

Quando a propriedade de alguma memória é liberada, liberando um bloqueio ou enviando um item para uma lista compartilhada vinculada, sempre há uma gravação envolvida que notifica outros threads de que a memória agora está disponível para eles. Embora seu código tenha propriedade da memória, ele provavelmente leu ou gravou nele, e é muito importante que essas leituras e gravações sejam executadas antes de liberar a propriedade. Uma barreira de gravação/liberação garante isso.

É mais simples considerar as barreiras de leitura e aquisição de gravação como operações únicas. No entanto, às vezes eles precisam ser construídos de duas partes: uma leitura ou gravação e uma barreira que não permite leituras ou gravações para se mover entre elas. Nesse caso, o posicionamento da barreira é crítico. Para uma barreira de aquisição de leitura, a leitura do sinalizador vem primeiro, depois a barreira e, em seguida, as leituras e gravações dos dados compartilhados. Para uma barreira de gravação, as leituras e gravações dos dados compartilhados são primeiro, depois, a barreira e, em seguida, a gravação do sinalizador.

``` syntax
// Read that acquires the data.
if( g_flag )
{
    // Guarantee that the read of the flag executes before
    // all reads and writes that follow in program order.
    BarrierOfSomeSort();

    // Now we can read and write the shared data.
    int localVariable = sharedData.y;
    sharedData.x = 0;

    // Guarantee that the write to the flag executes after all
    // reads and writes that precede it in program order.
    BarrierOfSomeSort();
    
    // Write that releases the data.
    g_flag = false;
}
```

A única diferença entre Read-Acquire e Write-Release é o local da barreira de memória. Uma aquisição de leitura tem a barreira após a operação de bloqueio e uma liberação de gravação tem a barreira antes. Em ambos os casos, a barreira está entre as referências à memória bloqueada e as referências ao bloqueio.

Para entender por que as barreiras são necessárias ao adquirir e ao liberar dados, é melhor (e mais preciso) considerar essas barreiras como garantia de sincronização com memória compartilhada, não com outros processadores. Se um processador usar uma versão de gravação para liberar uma estrutura de dados para a memória compartilhada e outro processador usar uma aquisição de leitura para obter acesso à estrutura de dados da memória compartilhada, o código funcionará corretamente. Se um dos processadores não usar a barreira apropriada, o compartilhamento de dados poderá falhar.

Usar a barreira certa para impedir o compilador e a reordenação de CPU para sua plataforma é essencial.

Uma das vantagens de usar os primitivos de sincronização fornecidos pelo sistema operacional é que todos eles incluem as barreiras de memória apropriadas.

## <a name="preventing-compiler-reordering"></a>Impedindo a reordenação do compilador

O trabalho de um compilador é otimizar agressivamente seu código para melhorar o desempenho. Isso inclui a reorganização de instruções onde quer que seja útil e onde quer que ele não altere o comportamento. Como o C++ Standard nunca menciona multithreading e como o compilador não sabe qual código precisa ser thread-safe, o compilador pressupõe que seu código é de thread único ao decidir quais reorganizados ele pode fazer com segurança. Portanto, você precisa informar ao compilador quando não for permitido reordenar as leituras e gravações.

Com Visual C++ você pode impedir a reordenação do compilador usando o [**\_ ReadWriteBarrier**](https://msdn.microsoft.com/library/f20w0x5e(v=VS.71).aspx)intrínseco do compilador. Onde você insere **\_ ReadWriteBarrier** em seu código, o compilador não moverá as leituras e as gravações entre elas.

``` syntax
#if _MSC_VER < 1400
    // With VC++ 2003 you need to declare _ReadWriteBarrier
    extern "C" void _ReadWriteBarrier();
#else
    // With VC++ 2005 you can get the declaration from intrin.h
#include <intrin.h>
#endif
// Tell the compiler that this is an intrinsic, not a function.
#pragma intrinsic(_ReadWriteBarrier)

// Create a new sprite by filling in a previously empty entry.
g_sprites[nextSprite].x = x;
g_sprites[nextSprite].y = y;
// Write-release, barrier followed by write.
// Guarantee that the compiler leaves the write to the flag
// after all reads and writes that precede it in program order.
_ReadWriteBarrier();
g_sprites[nextSprite].alive = true;
```

No código a seguir, outro thread lê a partir da matriz Sprite:

``` syntax
// Draw all sprites.
for( int i = 0; i < numSprites; ++i )
{

    // Read-acquire, read followed by barrier.
    if( g_sprites[nextSprite].alive )
    {
    
        // Guarantee that the compiler leaves the read of the flag
        // before all reads and writes that follow in program order.
        _ReadWriteBarrier();
        DrawSprite( g_sprites[nextSprite].x,
                g_sprites[nextSprite].y );
    }
}
```

É importante entender que o [**\_ ReadWriteBarrier**](https://msdn.microsoft.com/library/f20w0x5e(v=VS.71).aspx) não insere instruções adicionais e não impede que a CPU reorganize leituras e gravações — ela apenas impede que o compilador as reorganizem. Assim, o **\_ ReadWriteBarrier** é suficiente quando você implementa uma barreira de gravação em x86 e x64 (porque x86 e x64 não reordenam gravações e uma gravação normal é suficiente para liberar um bloqueio), mas na maioria dos outros casos, também é necessário impedir que a CPU reordene leituras e gravações.

Você também pode usar [**\_ ReadWriteBarrier**](https://msdn.microsoft.com/library/f20w0x5e(v=VS.71).aspx) ao gravar em memória combinada de gravação não armazenável em cache para evitar a reordenação de gravações. Nesse caso, o **\_ ReadWriteBarrier** ajuda a melhorar o desempenho, garantindo que as gravações ocorram na ordem linear preferida do processador.

Também é possível usar os intrínsecos [**\_ ReadBarrier**](https://msdn.microsoft.com/library/z055s48f(v=VS.80).aspx) e [**\_ WriteBarrier**](https://msdn.microsoft.com/library/65tt87y8(v=VS.80).aspx) para um controle mais preciso da reordenação do compilador. O compilador não moverá as leituras em um **\_ ReadBarrier** e não moverá gravações em um **\_ WriteBarrier**.

## <a name="preventing-cpu-reordering"></a>Impedindo a reordenação da CPU

A reordenação da CPU é mais sutil do que a reordenação do compilador. Você nunca pode vê-lo acontecer diretamente, você só vê bugs inexplicables. Para evitar a reordenação da CPU de leituras e gravações, você precisa usar instruções de barreira de memória, em alguns processadores. O nome de todas as finalidades para uma instrução de barreira de memória, no Xbox 360 e no Windows, é [**MemoryBarrier**](/windows/win32/api/winnt/nf-winnt-memorybarrier). Essa macro é implementada adequadamente para cada plataforma.

No Xbox 360, [**MemoryBarrier**](/windows/win32/api/winnt/nf-winnt-memorybarrier) é definido como **lwsync** (Lightweight Sync), também disponível por meio do **\_ \_ lwsync** intrínseco, que é definido em ppcintrinsics. h. **\_ \_ lwsync** também serve como uma barreira de memória do compilador, impedindo a reorganização de leituras e gravações pelo compilador.

A instrução **lwsync** é uma barreira de memória no Xbox 360 que sincroniza um núcleo de processador com o cache L2. Ele garante que todas as gravações antes de **lwsync** a transformem no cache L2 antes das gravações que se seguem. Ele também garante que todas as leituras que seguem **lwsync** não obtenham dados mais antigos do L2 do que as leituras anteriores. O tipo de reordenação que ele não impede é uma leitura à frente de uma gravação em um endereço diferente. Assim, o **lwsync** impõe a ordenação de memória que corresponde à ordenação de memória padrão em processadores x86 e x64. Para obter a ordenação de memória completa, é necessário ter uma instrução de sincronização mais cara (também conhecida como sincronização pesada), mas, na maioria dos casos, isso não é necessário. As opções de reordenação de memória no Xbox 360 são mostradas na tabela a seguir.



| Reordenação do Xbox 360           | Sem sincronização | lwsync | sync |
|-------------------------------|---------|--------|------|
| Leituras em movimento à frente de leituras   | Sim     | Não     | Não   |
| Gravações em movimento à frente de gravações | Sim     | Não     | Não   |
| Gravações em movimento à frente de leituras  | Sim     | Não     | Não   |
| Leituras em movimento à frente de gravações  | Sim     | Sim    | Não   |



 

O PowerPC também tem as instruções de sincronização **iSync** e **eieio** (que é usada para controlar a reordenação para memória de cache inibida). Essas instruções de sincronização não devem ser necessárias para fins de sincronização normais.

No Windows, [**MemoryBarrier**](/windows/win32/api/winnt/nf-winnt-memorybarrier) é definido em Winnt. h e fornece uma instrução de barreira de memória diferente, dependendo se você está compilando para x86 ou x64. A instrução de barreira de memória serve como uma barreira completa, impedindo todas as reordenação de leituras e gravações em toda a barreira. Assim, o **MemoryBarrier** no Windows oferece uma garantia de reordenação mais forte do que no Xbox 360.

No Xbox 360 e em muitas outras CPUs, há uma maneira adicional de que a reordenação de leitura pela CPU possa ser evitada. Se você ler um ponteiro e, em seguida, usar esse ponteiro para carregar outros dados, a CPU garante que as leituras do ponteiro não sejam mais antigas do que a leitura do ponteiro. Se o sinalizador de bloqueio for um ponteiro e se todas as leituras de dados compartilhados estiverem fora do ponteiro, o [**MemoryBarrier**](/windows/win32/api/winnt/nf-winnt-memorybarrier) poderá ser omitido para uma economia de desempenho modesto.

``` syntax
Data* localPointer = g_sharedPointer;
if( localPointer )
{
    // No import barrier is needed--all reads off of localPointer
    // are guaranteed to not be reordered past the read of
    // localPointer.
    int localVariable = localPointer->y;
    // A memory barrier is needed to stop the read of g_global
    // from being speculatively moved ahead of the read of
    // g_sharedPointer.
    int localVariable2 = g_global;
}
```

A instrução [**MemoryBarrier**](/windows/win32/api/winnt/nf-winnt-memorybarrier) só impede a reordenação de leituras e gravações na memória armazenável em cache. Se você alocar memória como PAGE \_ NoCache ou Page \_ WRITECOMBINE, uma técnica comum para autores de driver de dispositivo e desenvolvedores de jogos no Xbox 360, o **MemoryBarrier** não tem nenhum efeito sobre acesso a essa memória. A maioria dos desenvolvedores não precisa de sincronização de memória não armazenável em cache. Isso está além do escopo deste artigo.

## <a name="interlocked-functions-and-cpu-reordering"></a>Funções interligadas e reordenação de CPU

Às vezes, a leitura ou gravação que adquire ou libera um recurso é feita usando uma das funções **InterlockedXxx** . No Windows, isso simplifica as coisas; como no Windows, as funções **InterlockedXxx** são barreiras de memória total. Eles efetivamente têm uma barreira de memória de CPU antes e depois delas, o que significa que eles são uma barreira completa de leitura-aquisição ou gravação-liberação por si só.

No Xbox 360, as funções **InterlockedXxx** não contêm barreiras de memória de CPU. Eles impedem a reordenação de leituras e gravações do compilador, mas não a reordenação da CPU. Portanto, na maioria dos casos, ao usar as funções **InterlockedXxx** no Xbox 360, você deve precedê-las ou segui-las com um **\_ \_ lwsync**, para torná-las uma barreira Read-Acquire ou Write-Release. Para sua conveniência e facilitar a legibilidade, há versões de **aquisição** e **lançamento** de muitas das funções **InterlockedXxx** . Eles são fornecidos com uma barreira de memória interna. Por exemplo, [**InterlockedIncrementAcquire**](/previous-versions/windows/desktop/legacy/ms683618(v=vs.85)) faz um incremento intercadeado seguido por uma barreira de memória **\_ \_ lwsync** para fornecer a funcionalidade completa de leitura/aquisição.

É recomendável que você use as versões de **aquisição** e **lançamento** das funções **InterlockedXxx** (a maioria delas também estão disponíveis no Windows, sem penalidade de desempenho) para tornar sua intenção mais óbvia e facilitar a obtenção das instruções de barreira de memória no local correto. Qualquer uso de **InterlockedXxx** no Xbox 360 sem uma barreira de memória deve ser examinado com muito cuidado, pois geralmente é um bug.

Este exemplo demonstra como um thread pode passar tarefas ou outros dados para outro thread usando as versões de **aquisição** e **liberação** das funções **InterlockedXxxSList** . As funções **InterlockedXxxSList** são uma família de funções para manter uma lista compartilhada vinculada individualmente sem um bloqueio. Observe que as variantes de **aquisição** e **liberação** dessas funções não estão disponíveis no Windows, mas as versões regulares dessas funções são uma barreira de memória total no Windows.

``` syntax
// Declarations for the Task class go here.

// Add a new task to the list using lockless programming.
void AddTask( DWORD ID, DWORD data )
{
    Task* newItem = new Task( ID, data );
    InterlockedPushEntrySListRelease( g_taskList, newItem );
}

// Remove a task from the list, using lockless programming.
// This will return NULL if there are no items in the list.
Task* GetTask()
{
    Task* result = (Task*)
        InterlockedPopEntrySListAcquire( g_taskList );
    return result;
}
```

## <a name="volatile-variables-and-reordering"></a>Variáveis voláteis e reordenação

O padrão C++ diz que as leituras de variáveis voláteis não podem ser armazenadas em cache, gravações voláteis não podem ser atrasadas, e leituras e gravações voláteis não podem ser movidas além das outras. Isso é suficiente para a comunicação com dispositivos de hardware, que é a finalidade da palavra-chave volátil no padrão C++.

No entanto, as garantias do padrão não são suficientes para o uso de volatile para multithreading. O padrão C++ não interrompe o compilador de reordenar leituras e gravações não voláteis em relação a leituras e gravações voláteis e não diz nada sobre impedir a reordenação da CPU.

Visual C++ 2005 vai além do C++ padrão para definir a semântica amigável de vários threads para acesso de variável volátil. A partir do Visual C++ 2005, as leituras de variáveis voláteis são definidas para ter semântica de leitura/aquisição, e as gravações para variáveis voláteis são definidas para ter semântica de gravação/liberação. Isso significa que o compilador não reorganizará nenhuma leitura e gravação além delas e, no Windows, garantirá que a CPU também não faça isso.

É importante entender que essas novas garantias só se aplicam ao Visual C++ 2005 e a versões futuras do Visual C++. Os compiladores de outros fornecedores geralmente implementarão semânticas diferentes, sem garantias extras de Visual C++ 2005. Além disso, no Xbox 360, o compilador não insere nenhuma instrução para impedir que a CPU reordene leituras e gravações.

## <a name="example-of-a-lock-free-data-pipe"></a>Exemplo de um pipe de dados de Lock-Free

Um pipe é um constructo que permite que um ou mais threads gravem dados que são lidos por outros threads. Uma versão bloqueada de um pipe pode ser uma maneira elegante e eficiente de passar o trabalho do thread para o thread. O SDK do DirectX fornece **LockFreePipe**, um único leitor de bloqueio de gravador único, que está disponível em DXUTLockFreePipe. h. O mesmo **LockFreePipe** está disponível no SDK do Xbox 360 em AtgLockFreePipe. h.

**LockFreePipe** pode ser usado quando dois threads têm uma relação produtor/consumidor. O thread de produtor pode gravar dados no pipe para que o thread do consumidor processe em uma data posterior, sem nunca bloqueá-lo. Se o pipe for preenchido, as gravações falharão e o thread de produtor precisará tentar novamente mais tarde, mas isso só aconteceria se o thread de produtor estiver à frente. Se o pipe for esvaziado, as leituras falharão e o thread do consumidor precisará tentar novamente mais tarde, mas isso só aconteceria se não houver nenhum trabalho para o thread de consumidor fazer. Se os dois threads estiverem bem balanceados e o pipe for grande o suficiente, o pipe permitirá que eles passem dados sem problemas, sem atrasos ou blocos.

## <a name="xbox-360-performance"></a>Desempenho do Xbox 360

O desempenho das instruções e das funções de sincronização no Xbox 360 varia de acordo com o outro código em execução. A aquisição de bloqueios levará muito mais tempo se outro thread possuir o bloqueio no momento. As operações de [**InterlockedIncrement**](/windows/win32/api/winnt/nf-winnt-interlockedincrement) e de seção crítica levarão muito mais tempo se outros threads estiverem gravando na mesma linha de cache. O conteúdo das filas de armazenamento também pode afetar o desempenho. Portanto, todos esses números são apenas aproximações, gerados a partir de testes muito simples:

-   **lwsync** foi medido como levar 33-48 ciclos.
-   [**InterlockedIncrement**](/windows/win32/api/winnt/nf-winnt-interlockedincrement) foi medido como levar 225-260 ciclos.
-   A aquisição ou a liberação de uma seção crítica foi medida considerando cerca de 345 ciclos.
-   Adquirir ou liberar um mutex foi medido como cerca de 2350 ciclos.

## <a name="windows-performance"></a>Desempenho do Windows

O desempenho de instruções de sincronização e funções no Windows varia muito dependendo do tipo de processador e da configuração e do que o outro código está executando. Os sistemas com vários núcleos e vários soquetes geralmente demoram mais para executar instruções de sincronização e a aquisição de bloqueios leva muito mais tempo se outro thread possuir o bloqueio no momento.

No entanto, até mesmo algumas medidas geradas de testes muito simples são úteis:

-   [**MemoryBarrier**](/windows/win32/api/winnt/nf-winnt-memorybarrier) foi medido como levar 20-90 ciclos.
-   [**InterlockedIncrement**](/windows/win32/api/winnt/nf-winnt-interlockedincrement) foi medido como levar 36-90 ciclos.
-   A aquisição ou a liberação de uma seção crítica foi medida como levar 40-100 ciclos.
-   Adquirir ou liberar um mutex foi medido como cerca de 750-2500 ciclos.

Esses testes foram feitos no Windows XP em uma variedade de processadores diferentes. Os horários curtos estavam em um computador com um único processador e os tempos mais longos estavam em um computador com vários processadores.

Embora adquirir e liberar bloqueios seja mais caro do que usar a programação sem bloqueios, é ainda melhor compartilhar dados com menos frequência, evitando, assim, o custo total.

## <a name="performance-thoughts"></a>Pensamentos sobre o desempenho

A aquisição ou a liberação de uma seção crítica consiste em uma barreira de memória, uma operação **InterlockedXxx** e alguma verificação extra para lidar com a recursão e retornar a um mutex, se necessário. Você deve ter cuidado ao implementar sua própria seção crítica, pois a rotação em um loop aguardando que um bloqueio seja gratuito, sem voltar a um mutex, pode desperdiçar um desempenho considerável. Para seções críticas que são altamente contratadas, mas não são mantidas por longos, você deve considerar o uso de [**InitializeCriticalSectionAndSpinCount**](/windows/win32/api/synchapi/nf-synchapi-initializecriticalsectionandspincount) para que o sistema operacional seja girado por um tempo esperando pela seção crítica estar disponível em vez de ser imediatamente desreferenciado a um mutex se a seção crítica for de sua propriedade quando você tentar adquiri-la. Para identificar as seções críticas que podem se beneficiar de uma contagem de rotação, é necessário medir o comprimento da espera típica para um bloqueio específico.

Se um heap compartilhado for usado para alocações de memória — o comportamento padrão — cada alocação de memória e livre envolverá a aquisição de um bloqueio. À medida que o número de threads e o número de alocações aumenta, os níveis de desempenho são desativados e, eventualmente, começam a diminuir. O uso de heaps por thread ou a redução do número de alocações pode evitar esse afunilamento de bloqueio.

Se um thread estiver gerando dados e outro thread estiver consumindo dados, eles poderão acabar compartilhando dados com frequência. Isso pode acontecer se um thread estiver carregando recursos e outro thread estiver renderizando a cena. Se o thread de renderização fizer referência aos dados compartilhados em cada chamada de desenho, a sobrecarga de bloqueio será alta. Um desempenho muito melhor pode ser percebido se cada thread tiver estruturas de dados particulares que são sincronizadas uma vez por quadro ou menos.

Não há garantia de que os algoritmos sem bloqueio sejam mais rápidos do que os algoritmos que usam bloqueios. Você deve verificar se os bloqueios estão realmente causando problemas antes de tentar evitá-los, e você deve medir para ver se o seu código de bloqueio realmente melhora o desempenho.

## <a name="platform-differences-summary"></a>Resumo de diferenças de plataforma

-   As funções **InterlockedXxx** impedem a reordenação de leitura/gravação de CPU no Windows, mas não no Xbox 360.
-   A leitura e a gravação de variáveis voláteis usando o Visual Studio C++ 2005 evita a reordenação de leitura/gravação de CPU no Windows, mas no Xbox 360, ela impede apenas a reordenação de leitura/gravação do compilador.
-   As gravações são reordenadas no Xbox 360, mas não em x86 ou x64.
-   As leituras são reordenadas no Xbox 360, mas em x86 ou x64 elas são reordenadas apenas em relação às gravações, e somente se as leituras e gravações forem direcionadas a locais diferentes.

## <a name="recommendations"></a>Recomendações

-   Use bloqueios quando possível porque eles são mais fáceis de usar corretamente.
-   Evite o bloqueio com muita frequência, para que os custos de bloqueio não se tornem significativos.
-   Evite manter os bloqueios por muito tempo, a fim de evitar interrupções longas.
-   Use a programação sem bloqueio quando apropriado, mas certifique-se de que os ganhos justifiquem a complexidade.
-   Use a programação de bloqueio ou bloqueios de rotação em situações em que outros bloqueios são proibidos, como ao compartilhar dados entre chamadas de procedimento deferidas e código normal.
-   Use somente algoritmos de programação de bloqueio padrão que foram comprovados como corretos.
-   Ao fazer uma programação de bloqueio, certifique-se de usar as variáveis de sinalizador volátil e as instruções de barreira de memória, conforme necessário.
-   Ao usar o **InterlockedXxx** no Xbox 360, use as variantes de **aquisição** e **versão** .

## <a name="references"></a>Referências

-   Biblioteca MSDN. "[**volátil (C++)**](https://msdn.microsoft.com/library/12a04hfd(v=VS.71).aspx)". Referência da linguagem C++.
-   Vance Morrison. "[Entenda o impacto das técnicas de Low-Lock em aplicativos multissegmentados](/archive/msdn-magazine/2005/october/understanding-low-lock-techniques-in-multithreaded-apps)". MSDN Magazine, outubro de 2005.
-   Lyons, Michael. "[Modelo de armazenamento de PowerPC e programação de Aix](https://www-128.ibm.com/developerworks/eserver/articles/powerpc.mdl)". IBM developerWorks, 16 de novembro de 2005.
-   McKenney, Paul E. "[ordenação de memória em microprocessadores modernos, parte II](https://www.linuxjournal.com/article/8212)". Diário do Linux, setembro de 2005. \[Este artigo tem alguns detalhes do x86.\]
-   Intel Corporation. "[Classificação de memória da arquitetura Intel® 64](https://www.cs.cmu.edu/~410-f10/doc/Intel_Reordering_318147.pdf)". Agosto de 2007. \[Aplica-se aos processadores IA-32 e Intel 64.\]
-   Niebler, Eric. "[Relatório de corrida: reunião ad hoc em threads em C++](https://www.artima.com/cppsource/threads_meeting.html)". A fonte C++, 17 de outubro de 2006.
-   Hart, Thomas E. 2006. "[Tornar a sincronização de bloqueio rápida: implicações de desempenho da recuperação de memória](https://www.cs.toronto.edu/~tomhart/papers/hart_ipdps06.pdf)". Procedimentos do 2006 Internacional de processamento distribuído paralelo e Symposium (IPDPS 2006), ilha Rhodes, Grécia, 2006 de abril.

 

 