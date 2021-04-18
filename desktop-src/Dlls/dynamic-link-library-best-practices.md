---
description: A criação de DLLs apresenta vários desafios para os desenvolvedores.
ms.assetid: 44EFC4B5-7A2F-43A6-914E-D4EB7446AC35
title: Práticas recomendadas da biblioteca de Dynamic-Link
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88aba0999f3d0825c6d2f4df3afe09d766a82232
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105750868"
---
# <a name="dynamic-link-library-best-practices"></a>Práticas recomendadas da biblioteca de Dynamic-Link

* * Atualizado: * *

-   17 de maio de 2006

**APIs importantes**

-   [**DllMain**](dllmain.md)
-   [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa)
-   [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa)

A criação de DLLs apresenta vários desafios para os desenvolvedores. DLLs não têm controle de versão imposta pelo sistema. Quando existem várias versões de uma DLL em um sistema, a facilidade de ser substituída juntamente com a falta de um esquema de controle de versão cria conflitos de dependência e de API. A complexidade no ambiente de desenvolvimento, a implementação do carregador e as dependências de DLL criaram fragilidade em ordem de carregamento e comportamento do aplicativo. Por fim, muitos aplicativos dependem de DLLs e têm conjuntos complexos de dependências que devem ser respeitadas para que os aplicativos funcionem corretamente. Este documento fornece diretrizes para desenvolvedores de DLL para ajudar na criação de DLLs mais robustas, portáteis e extensíveis.

A sincronização incorreta no [**DllMain**](dllmain.md) pode fazer com que um aplicativo seja bloqueado ou tenha acesso a dados ou código em uma dll não inicializada. Chamar determinadas funções de no **DllMain** causa esses problemas.

![o que acontece quando uma biblioteca é carregada](images/fig1.png)

## <a name="general-best-practices"></a>Melhores práticas gerais

[**DllMain**](dllmain.md) é chamado enquanto o carregador de bloqueio é mantido. Portanto, as restrições significativas são impostas nas funções que podem ser chamadas dentro de **DllMain**. Assim, o **DllMain** foi projetado para executar tarefas de inicialização mínimas, usando um pequeno subconjunto da API do Microsoft® Windows®. Você não pode chamar nenhuma função em **DllMain** que tente adquirir o carregador de carregado direta ou indiretamente. Caso contrário, você apresentará a possibilidade de o aplicativo travar ou falhar. Um erro em uma implementação **DllMain** pode comprometer o processo inteiro e todos os seus threads.

O [**DllMain**](dllmain.md) ideal seria apenas um stub vazio. No entanto, considerando a complexidade de muitos aplicativos, isso geralmente é muito restritivo. Uma boa regra geral para **DllMain** é adiar o máximo de inicialização possível. A inicialização lenta aumenta a robustez do aplicativo porque essa inicialização não é executada enquanto o bloqueio do carregador é mantido. Além disso, a inicialização lenta permite que você use com segurança muito mais da API do Windows.

Algumas tarefas de inicialização não podem ser adiadas. Por exemplo, uma DLL que depende de um arquivo de configuração deve falhar ao ser carregada se o arquivo estiver malformado ou contiver lixo. Para esse tipo de inicialização, a DLL deve tentar a ação e falhar rapidamente, em vez de desperdiçar recursos, concluindo outro trabalho.

Você nunca deve executar as seguintes tarefas em [**DllMain**](dllmain.md):

-   Chame [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) ou [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) (direta ou indiretamente). Isso pode causar um deadlock ou uma falha.
-   Chame [**GetStringTypeA**](/windows/desktop/api/winnls/nf-winnls-getstringtypea), [**GetStringTypeEx**](/windows/win32/api/stringapiset/nf-stringapiset-getstringtypeexw)ou [**GetStringTypeW**](/windows/desktop/api/stringapiset/nf-stringapiset-getstringtypew) (direta ou indiretamente). Isso pode causar um deadlock ou uma falha.
-   Sincronizar com outros threads. Isso pode causar um deadlock.
-   Adquira um objeto de sincronização que pertença ao código que está aguardando para adquirir o bloqueio do carregador. Isso pode causar um deadlock.
-   Inicializar threads COM usando [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex). Em determinadas condições, essa função pode chamar [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa).
-   Chame as funções de registro. Essas funções são implementadas no Advapi32.dll. Se Advapi32.dll não for inicializado antes da DLL, a DLL poderá acessar a memória não inicializada e causar falha no processo.
-   Chame [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa). A criação de um processo pode carregar outra DLL.
-   Chame [**ExitThread**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibraryandexitthread). A saída de um thread durante a desanexação da DLL pode fazer com que o bloqueio do carregador seja adquirido novamente, causando um deadlock ou uma falha.
-   Chame [**CreateThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createthread). Criar um thread pode funcionar se você não sincronizar com outros threads, mas for arriscado.
-   Crie um pipe nomeado ou outro objeto nomeado (somente Windows 2000). No Windows 2000, os objetos nomeados são fornecidos pela DLL de serviços de terminal. Se essa DLL não for inicializada, as chamadas para a DLL poderão fazer com que o processo falhe.
-   Use a função de gerenciamento de memória do C Run-Time dinâmico (CRT). Se a DLL do CRT não for inicializada, as chamadas para essas funções poderão causar falha no processo.
-   Chame funções em User32.dll ou Gdi32.dll. Algumas funções carregam outra DLL, que pode não ser inicializada.
-   Use código gerenciado.

As seguintes tarefas são seguras para serem executadas no **DllMain**:

-   Inicializar estruturas de dados estáticos e membros em tempo de compilação.
-   Criar e inicializar objetos de sincronização.
-   Aloque memória e inicialize estruturas de dados dinâmicos (evitando as funções listadas acima).
-   Configurar o armazenamento local de threads (TLS).
-   Abra, leia de e grave em arquivos.
-   Chame funções em Kernel32.dll (exceto as funções listadas acima).
-   Definir ponteiros globais como nulos, colocando a inicialização de membros dinâmicos. No Microsoft Windows Vista™, você pode usar as funções de inicialização única para garantir que um bloco de código seja executado apenas uma vez em um ambiente multithread.

## <a name="deadlocks-caused-by-lock-order-inversion"></a>Deadlocks causados pela inversão da ordem de bloqueio

Quando você está implementando o código que usa vários objetos de sincronização, como bloqueios, é vital respeitar a ordem de bloqueio. Quando for necessário adquirir mais de um bloqueio por vez, você deve definir uma precedência explícita que seja chamada de hierarquia de bloqueio ou de bloqueio. Por exemplo, se o bloqueio A for adquirido antes do bloqueio B em algum lugar no código, e o bloqueio B for adquirido antes do bloqueio C em outro lugar no código, a ordem de bloqueio será a, B, C e essa ordem deverá ser seguida em todo o código. A inversão de ordem de bloqueio ocorre quando a ordem de bloqueio não é seguida — por exemplo, se o bloqueio B for adquirido antes do bloqueio A. A inversão de ordem de bloqueio pode causar deadlocks difíceis de depurar. Para evitar esses problemas, todos os threads devem adquirir bloqueios na mesma ordem.

É importante observar que o carregador chama [**DllMain**](dllmain.md) com o bloqueio de carregador já adquirido, portanto, o bloqueio do carregador deve ter a maior precedência na hierarquia de bloqueio. Observe também que o código só precisa adquirir os bloqueios necessários para a sincronização adequada; Ele não precisa adquirir todos os bloqueios que estão definidos na hierarquia. Por exemplo, se uma seção de código exigir apenas bloqueios A e C para uma sincronização adequada, o código deverá adquirir bloqueio A antes de adquirir o bloqueio C; Não é necessário que o código também adquira o bloqueio B. Além disso, o código de DLL não pode adquirir explicitamente o bloqueio de carregador. Se o código precisar chamar uma API como [**GetModuleFileName**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) que possa adquirir indiretamente o bloqueio do carregador e o código também precisar adquirir um bloqueio privado, o código deverá chamar **GetModuleFileName** antes de adquirir o bloqueio P, garantindo que a ordem de carregamento seja respeitada.

A Figura 2 é um exemplo que ilustra a inversão de ordem de bloqueio. Considere uma DLL cujo thread principal contém [**DllMain**](dllmain.md). O carregador de biblioteca adquire o bloqueio do carregador L e, em seguida, chama o **DllMain**. O thread principal cria objetos de sincronização A, B e G para serializar o acesso às suas estruturas de dados e, em seguida, tenta adquirir o bloqueio G. Um thread de trabalho que já adquiriu com êxito o bloqueio G chama uma função como GetModuleHandle que tenta adquirir o bloqueio do carregador L. Assim, o thread de trabalho é bloqueado em L e o thread principal é bloqueado em G, resultando em um deadlock.

![deadlock causado por inversão de ordem de bloqueio](images/fig2.png)

Para evitar deadlocks causados pela inversão de ordem de bloqueio, todos os threads devem tentar adquirir objetos de sincronização na ordem de carga definida em todos os momentos.

## <a name="best-practices-for-synchronization"></a>Práticas recomendadas para sincronização

Considere uma DLL que cria threads de trabalho como parte de sua inicialização. Após a limpeza da DLL, é necessário sincronizar com todos os threads de trabalho para garantir que as estruturas de dados estejam em um estado consistente e, em seguida, encerrar os threads de trabalho. Hoje, não há uma maneira simples de resolver completamente o problema de sincronizar e desligar as DLLs de forma limpa em um ambiente multithread. Esta seção descreve as práticas recomendadas atuais para a sincronização de threads durante o desligamento de DLL.

Sincronização de threads no [**DllMain**](dllmain.md) durante a saída do processo

-   No momento em que [**DllMain**](dllmain.md) é chamado na saída do processo, todos os threads do processo foram limpos forçosamente e há uma chance de que o espaço de endereço seja inconsistente. A sincronização não é necessária nesse caso. Em outras palavras, o manipulador de \_ desanexação de processo dll ideal \_ está vazio.
-   O Windows Vista garante que as estruturas de dados principais (variáveis de ambiente, diretório atual, heap de processo e assim por diante) estejam em um estado consistente. No entanto, outras estruturas de dados podem ser corrompidas, portanto a memória de limpeza não é segura.
-   O estado persistente que precisa ser salvo deve ser liberado para o armazenamento permanente.

Sincronização de threads em **DllMain** para \_ desanexar thread de dll \_ durante o descarregamento de dll

-   Quando a DLL é descarregada, o espaço de endereço não é jogado fora. Portanto, espera-se que a DLL execute um desligamento normal. Isso inclui a sincronização de threads, os identificadores abertos, o estado persistente e os recursos alocados.
-   A sincronização de threads é complicada porque aguardar a saída de threads no [**DllMain**](dllmain.md) pode causar um deadlock. Por exemplo, a DLL A mantém o bloqueio do carregador. Ele sinaliza ao thread T para sair e aguarda até que o thread saia. O thread T sai e o carregador tenta adquirir o bloqueio do carregador para chamar o **DllMain** da dll a com a \_ desanexação do thread de dll \_ . Isso causa um deadlock. Para minimizar o risco de um deadlock:
    -   A DLL A Obtém uma \_ \_ mensagem de desanexação de thread de dll em seu [**DllMain**](dllmain.md) e define um evento para thread T, sinalizando-a para sair.
    -   O thread T conclui sua tarefa atual, se apresenta a um estado consistente, sinaliza a DLL A e aguarda infinitamente. Observe que as rotinas de verificação de consistência devem seguir as mesmas restrições que o [**DllMain**](dllmain.md) para evitar o deadlock.
    -   A DLL A encerra o T, sabendo que ele está em um estado consistente.

Se uma DLL for descarregada depois que todos os seus threads tiverem sido criados, mas antes de começarem a execução, os threads poderão falhar. Se a DLL criou threads em seu **DllMain** como parte de sua inicialização, alguns threads podem não ter concluído a inicialização e sua \_ mensagem de anexação de thread de dll \_ ainda está aguardando para ser entregue à dll. Nessa situação, se a DLL for descarregada, ela começará a encerrar os threads. No entanto, alguns threads podem ser bloqueados por trás do bloqueio do carregador. Suas \_ mensagens de anexação de thread de dll \_ são processadas após o cancelamento do mapeamento da dll, causando a falha do processo.

## <a name="recommendations"></a>Recomendações

Estas são as diretrizes recomendadas:

-   Use Application Verifier para capturar os erros mais comuns em [**DllMain**](dllmain.md).
-   Se estiver usando um bloqueio privado dentro de [**DllMain**](dllmain.md), defina uma hierarquia de bloqueio e use-a consistentemente. O bloqueio do carregador deve estar na parte inferior desta hierarquia.
-   Verifique se nenhuma chamada depende de outra DLL que talvez ainda não tenha sido totalmente carregada.
-   Executar inicializações simples estaticamente no tempo de compilação, em vez de em [**DllMain**](dllmain.md).
-   Adie todas as chamadas em [**DllMain**](dllmain.md) que podem esperar até mais tarde.
-   Adie as tarefas de inicialização que podem esperar até mais tarde. Determinadas condições de erro devem ser detectadas antecipadamente para que o aplicativo possa manipular erros normalmente. No entanto, há compensações entre essa detecção antecipada e a perda de robustez que pode resultar dela. Geralmente, a inicialização desreferenciada é a melhor.

 

 
