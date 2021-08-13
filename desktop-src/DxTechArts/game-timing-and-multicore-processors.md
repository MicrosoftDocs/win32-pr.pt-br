---
title: Tempo do jogo e processadores com vários núcleos
description: Este artigo sugere uma solução mais precisa e confiável para obter tempos de CPU de alta resolução usando as APIs Windows QueryPerformanceCounter e QueryPerformanceFrequency.
ms.assetid: 1512324d-dffa-3681-be3f-f63a3b8f11db
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed5e668e87a2645859838b1fdf9cfb35263381e9ce9c73fbe72232ad3d3a46cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118649344"
---
# <a name="game-timing-and-multicore-processors"></a>Tempo do jogo e processadores com vários núcleos

Com as tecnologias de gerenciamento de energia se tornando mais comuns nos computadores atuais, um método comumente usado para obter tempos de CPU de alta resolução, a instrução RDTSC, pode não funcionar conforme o esperado. Este artigo sugere uma solução mais precisa e confiável para obter tempos de CPU de alta resolução usando as APIs Windows [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) e [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency).

-   [Tela de fundo](#background)
-   [Recomendações](#recommendations)
-   [Compatibilidade do aplicativo](#application-compatibility)

## <a name="background"></a>Segundo plano

Desde a introdução do conjunto de instruções x86 P5, muitos desenvolvedores de jogos fizeram uso do contador de carimbo de data/hora de leitura, a instrução RDTSC, para executar o tempo de alta resolução. Os temporizadores Windows multimídia são precisos o suficiente para processamento de som e vídeo, mas com tempos de quadros de uma dezena de milissegundos ou menos, eles não têm resolução suficiente para fornecer informações de tempo delta. Muitos jogos ainda usam um temporizador multimídia na start-up para estabelecer a frequência da CPU e usam esse valor de frequência para dimensionar os resultados do RDTSC para obter o tempo preciso. Devido às limitações do RDTSC, a API do Windows expõe a maneira mais correta de acessar essa funcionalidade por meio das rotinas [**de QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) e [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency).

Esse uso do RDTSC para o tempo é prejudicado por estes problemas fundamentais:

-   Valores descontinuados. O uso do RDTSC assume diretamente que o thread está sempre em execução no mesmo processador. Sistemas multiprocessador e de núcleo duplo não garantem a sincronização de seus contadores de ciclo entre núcleos. Isso é rebaixado quando combinado com tecnologias modernas de gerenciamento de energia que ociosas e restauram vários núcleos em momentos diferentes, o que resulta na falta de sincronização dos núcleos. Para um aplicativo, isso geralmente resulta em falhas ou em possíveis falhas à medida que o thread salta entre os processadores e obtém valores de tempo que resultam em deltas grandes, deltas negativos ou tempo interrompido.
-   Disponibilidade de hardware dedicado. O RDTSC bloqueia as informações de tempo que o aplicativo solicita ao contador de ciclo do processador. Por muitos anos, essa era a melhor maneira de obter informações de tempo de alta precisão, mas as placas-mãe mais novas agora incluem dispositivos de tempo dedicados que fornecem informações de tempo de alta resolução sem as desvantagens do RDTSC.
-   Variabilidade da frequência da CPU. Muitas vezes, é feita a suposição de que a frequência da CPU é fixa durante a vida útil do programa. No entanto, com tecnologias modernas de gerenciamento de energia, essa é uma suposição incorreta. Embora inicialmente limitada a computadores laptop e outros dispositivos móveis, a tecnologia que altera a frequência da CPU está em uso em muitos computadores de área de trabalho de alto nível; desabilitar sua função para manter uma frequência consistente geralmente não é aceitável para os usuários.

## <a name="recommendations"></a>Recomendações

Os jogos precisam de informações precisas de tempo, mas você também precisa implementar o código de tempo de uma maneira que evite os problemas associados ao uso do RDTSC. Ao implementar o tempo de alta resolução, tome as seguintes etapas:

1.  Use [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) e [**QueryPerformanceFrequency em vez**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) de RDTSC. Essas APIs podem usar o RDTSC, mas podem usar dispositivos de tempo na placa-mãe ou alguns outros serviços do sistema que fornecem informações de tempo de alta resolução de alta qualidade. Embora o RDTSC seja muito mais rápido do que **QueryPerformanceCounter,** uma vez que a última é uma chamada à API, é uma API que pode ser chamada várias centenas de vezes por quadro sem nenhum impacto perceptível. (No entanto, os desenvolvedores devem tentar fazer com que seus jogos chamem **QueryPerformanceCounter** o menos possível para evitar qualquer penalidade de desempenho.)
2.  Ao calcular deltas, os valores devem ser fixados para garantir que os bugs nos valores de tempo não causem falhas ou cálculos instável relacionados ao tempo. O intervalo de fixação deve ser de 0 (para evitar valores delta negativos) a algum valor razoável com base na taxa de quadros mais baixa esperada. É provável que a fixação seja útil em qualquer depuração do aplicativo, mas lembre-se de fazer uma análise de desempenho ou executar o jogo em algum modo nãotimizado.
3.  Compute todo o tempo em um único thread. A computação do tempo em vários threads – por exemplo, com cada thread associado a um processador específico – reduz consideravelmente o desempenho de sistemas de vários núcleos.
4.  Defina esse thread único para permanecer em um único processador usando o [**setthreadAffinityMask**](/windows/win32/api/winbase/nf-winbase-setthreadaffinitymask)da API Windows. Normalmente, esse é o thread principal do jogo. Embora [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) e [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) normalmente se ajustem para vários processadores, bugs no BIOS ou nos drivers podem fazer com que essas rotinas retornem valores diferentes à medida que o thread se move de um processador para outro. Portanto, é melhor manter o thread em um único processador.

    Todos os outros threads devem operar sem coletar seus próprios dados de temporizador. Não recomendamos usar um thread de trabalho para calcular o tempo, pois isso se tornará um gargalo de sincronização. Em vez disso, os threads de trabalho devem ler osstamps de data/hora do thread principal e, como os threads de trabalho leem apenas os tempos de data/hora, não é necessário usar seções críticas.

5.  Chame [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) apenas uma vez, porque a frequência não será mudada enquanto o sistema estiver em execução.

## <a name="application-compatibility"></a>Compatibilidade de aplicativos

Muitos desenvolvedores fizeram suposições sobre o comportamento do RDTSC ao longo de muitos anos, portanto, é muito provável que alguns aplicativos existentes tenham problemas quando executados em um sistema com vários processadores ou núcleos devido à implementação de tempo. Esses problemas geralmente se manifestam como falha ou movimento lento. Não há uma solução fácil para aplicativos que não estão cientes do gerenciamento de energia, mas há um shim existente para forçar um aplicativo a sempre executar em um único processador em um sistema multiprocessador.

Para criar esse shim, baixe o arquivo de Compatibilidade de Aplicativos da Microsoft Toolkit do [Windows Compatibilidade de Aplicativos.](/archive/blogs/yongrhee/download-application-compatibility-toolkit-act-for-windows-10)

Usando o Administrador de Compatibilidade, parte do kit de ferramentas, crie um banco de dados do seu aplicativo e correções associadas. Crie um novo modo de compatibilidade para esse banco de dados e selecione a correção de compatibilidade **SingleProcAffinity** para forçar todos os threads do aplicativo a executar em um único processador/núcleo. Usando a ferramenta de linha de comando Fixpack.exe (também parte do kit de ferramentas), você pode converter esse banco de dados em um pacote instalável para instalação, teste e distribuição.

Para saber mais sobre como usar o Administrador de Compatibilidade, confira a documentação do kit de ferramentas. Para ver a sintaxe e exemplos de Fixpack.exe, confira sua ajuda de linha de comando.

Para obter informações orientadas ao cliente, consulte os seguintes artigos da base de dados de conhecimento da Ajuda e suporte da Microsoft:

-   [Programas que usam a função QueryPerformanceCounter](https://support.microsoft.com/kb/895980) podem ter um desempenho ruim no Windows Server 2003 e no Windows XP (artigo 895980)
-   [O desempenho do jogo pode ser ruim Windows](https://support.microsoft.com/kb/909944) computador baseado em XP que está usando um processador de núcleo duplo (artigo 909944)

 

 
