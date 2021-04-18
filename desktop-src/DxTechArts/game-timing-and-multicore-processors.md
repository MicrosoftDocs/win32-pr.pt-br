---
title: Tempo do jogo e processadores com vários núcleos
description: Este artigo sugere uma solução mais precisa e confiável para obter tempos de CPU de alta resolução usando as APIs do Windows QueryPerformanceCounter e QueryPerformanceFrequency.
ms.assetid: 1512324d-dffa-3681-be3f-f63a3b8f11db
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c5c511f558b59e94945e63c44db225f34ac2583
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105767661"
---
# <a name="game-timing-and-multicore-processors"></a>Tempo do jogo e processadores com vários núcleos

Com as tecnologias de gerenciamento de energia que se tornam mais comuns nos computadores atuais, um método comumente usado para obter intervalos de CPU de alta resolução, a instrução RDTSC, pode não funcionar mais conforme o esperado. Este artigo sugere uma solução mais precisa e confiável para obter tempos de CPU de alta resolução usando as APIs do Windows [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) e [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency).

-   [Tela de fundo](#background)
-   [Recomendações](#recommendations)
-   [Compatibilidade de aplicativos](#application-compatibility)

## <a name="background"></a>Tela de fundo

Desde a introdução do conjunto de instruções do P5 x86, muitos desenvolvedores de jogos fizeram o uso do contador de carimbo de data/hora de leitura, a instrução RDTSC, para executar o tempo de alta resolução. Os temporizadores de multimídia do Windows são precisos o suficiente para o processamento de som e vídeo, mas com horários de quadros de dezenas de milissegundos ou menos, eles não têm resolução suficiente para fornecer informações em tempo Delta. Muitos jogos ainda usam um temporizador de multimídia na inicialização para estabelecer a frequência da CPU e usam esse valor de frequência para dimensionar os resultados de RDTSC para obter um tempo preciso. Devido às limitações do RDTSC, a API do Windows expõe a maneira mais correta de acessar essa funcionalidade por meio das rotinas de [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) e [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency).

Esse uso de RDTSC para o tempo sofre contra esses problemas fundamentais:

-   Valores descontínuos. Usar o RDTSC diretamente pressupõe que o thread esteja sempre em execução no mesmo processador. Os sistemas multiprocessador e dual-core não garantem a sincronização de seus contadores de ciclo entre os núcleos. Isso é exacerbado quando combinado com as tecnologias de gerenciamento de energia modernas que estão ociosas e restauram vários núcleos em momentos diferentes, o que resulta em normalmente os núcleos estarem fora de sincronização. Para um aplicativo, isso geralmente resulta em falhas ou em falhas potenciais, uma vez que o thread salta entre os processadores e obtém valores de tempo que resultam em deltas grandes, deltas negativos ou tempo interrompido.
-   Disponibilidade de hardware dedicado. RDTSC bloqueia as informações de tempo que o aplicativo solicita ao contador de ciclo do processador. Por muitos anos, essa foi a melhor maneira de obter informações de tempo de alta precisão, mas as motherboards mais novas agora estão incluindo dispositivos de tempo dedicados que fornecem informações de tempo de alta resolução sem as desvantagens do RDTSC.
-   Variabilidade da frequência da CPU. A pressuposição costuma ser feita de forma que a frequência da CPU seja fixa durante o ciclo de vida do programa. No entanto, com as tecnologias de gerenciamento de energia modernas, essa é uma suposição incorreta. Embora inicialmente limitado a computadores laptop e outros dispositivos móveis, a tecnologia que altera a frequência da CPU está em uso em vários PCs de área de trabalho de ponta; desabilitar sua função para manter uma frequência consistente geralmente não é aceitável para os usuários.

## <a name="recommendations"></a>Recomendações

Os jogos precisam de informações de tempo precisas, mas você também precisa implementar o código de tempo de forma a evitar os problemas associados ao uso do RDTSC. Ao implementar o tempo de alta resolução, execute as seguintes etapas:

1.  Use [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) e [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) em vez de RDTSC. Essas APIs podem fazer uso de RDTSC, mas, em vez disso, podem usar um dispositivo de tempo na placa-mãe ou outros serviços do sistema que fornecem informações de tempo de alta resolução de alta qualidade. Embora o RDTSC seja muito mais rápido do que o **QueryPerformanceCounter**, como o último é uma chamada à API, é uma API que pode ser chamada várias centenas de vezes por quadro sem qualquer impacto perceptível. (No entanto, os desenvolvedores devem tentar fazer com que seus jogos chamem **QueryPerformanceCounter** o mínimo possível para evitar qualquer penalidade de desempenho.)
2.  Ao computar deltas, os valores devem ser clamped para garantir que qualquer bug nos valores de tempo não cause panes ou cálculos relacionados ao tempo instável. O intervalo de fixe deve ser de 0 (para evitar valores Delta negativos) a um valor razoável com base na taxa de quadros esperada mais baixa. O fixação MSS provavelmente será útil em qualquer depuração do seu aplicativo, mas lembre-se de mantê-lo em mente se estiver fazendo análise de desempenho ou executando o jogo em algum modo não otimizado.
3.  Computar todo o tempo em um único thread. Computação de tempo em vários threads — por exemplo, com cada thread associado a um processador específico — reduz significativamente o desempenho de sistemas de vários núcleos.
4.  Defina esse thread único para permanecer em um único processador usando a API do Windows [**SetThreadAffinityMask**](/windows/win32/api/winbase/nf-winbase-setthreadaffinitymask). Normalmente, esse é o thread principal do jogo. Embora [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) e [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) normalmente se ajustem a vários processadores, os bugs no BIOS ou nos drivers podem resultar nessas rotinas retornando valores diferentes conforme o thread passa de um processador para outro. Portanto, é melhor manter o thread em um único processador.

    Todos os outros threads devem operar sem a coleta de seus próprios dados de timer. Não recomendamos o uso de um thread de trabalho para calcular o tempo, pois isso se tornará um afunilamento de sincronização. Em vez disso, os threads de trabalho devem ler carimbos de data/hora do thread principal e, como os threads de trabalho só lêem carimbos de data/hora, não há necessidade de usar seções críticas.

5.  Chame [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) apenas uma vez, porque a frequência não será alterada enquanto o sistema estiver em execução.

## <a name="application-compatibility"></a>Compatibilidade de aplicativos

Muitos desenvolvedores fizeram suposições sobre o comportamento de RDTSC por muitos anos, portanto, é bem provável que alguns aplicativos existentes apresentem problemas quando executados em um sistema com vários processadores ou núcleos devido à implementação de tempo. Esses problemas normalmente serão manifestados como um movimento de movimento lento ou de falha. Não há facilidade de solução para aplicativos que não reconheçam o gerenciamento de energia, mas há um Shim existente para forçar um aplicativo a ser sempre executado em um único processador em um sistema multiprocessador.

Para criar esse Shim, baixe o Microsoft Application Compatibility Toolkit da [compatibilidade de aplicativos do Windows](/archive/blogs/yongrhee/download-application-compatibility-toolkit-act-for-windows-10).

Usando o administrador de compatibilidade, parte do kit de ferramentas, crie um banco de dados do seu aplicativo e correções associadas. Crie um novo modo de compatibilidade para esse banco de dados e selecione a correção de compatibilidade **SingleProcAffinity** para forçar a execução de todos os threads do aplicativo em um único processador/núcleo. Usando a ferramenta de linha de comando Fixpack.exe (também parte do kit de ferramentas), você pode converter esse banco de dados em um pacote instalável para instalação, teste e distribuição.

Para obter instruções sobre como usar o administrador de compatibilidade, consulte a documentação do kit de ferramentas. Para obter a sintaxe e exemplos de uso de Fixpack.exe, consulte sua ajuda de linha de comando.

Para obter informações orientadas ao cliente, consulte os seguintes artigos da base de dados de conhecimento da Microsoft ajuda e suporte:

-   [Programas que o usuário a função QueryPerformanceCounter pode executar de maneira insatisfatória no Windows Server 2003 e no Windows XP](https://support.microsoft.com/kb/895980) (artigo 895980)
-   [O desempenho do jogo pode ser ruim em um computador baseado no Windows XP que esteja usando um processador de núcleo duplo](https://support.microsoft.com/kb/909944) (artigo 909944)

 

 