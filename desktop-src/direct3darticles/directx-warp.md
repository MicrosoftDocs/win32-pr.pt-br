---
title: Guia da plataforma de rasterização avançada do Windows (WARP)
description: Este artigo descreve a WARP (plataforma de rasterização avançada do Windows) e os seguintes aspectos de WARP.
ms.assetid: C40A96EB-64AA-46EB-85A9-7C996ABC8BFE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1c09c29dd7b935542f0238cde0a71cbc97fce23
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641585"
---
# <a name="windows-advanced-rasterization-platform-warp-guide"></a>Guia da plataforma de rasterização avançada do Windows (WARP)

Este artigo descreve a WARP (plataforma de rasterização avançada do Windows) e os seguintes aspectos de WARP.

-   [O que é WARP?](#what-is-warp)
-   [Benefícios da distorção](#warp-benefits)
    -   [Removendo a necessidade de Rasterizadores de software personalizados](#removing-the-need-for-custom-software-rasterizers)
    -   [Habilitando o desempenho máximo de hardware de gráficos](#enabling-maximum-performance-from-graphics-hardware)
    -   [Habilitando a renderização quando o hardware do Direct3D não está disponível](#enabling-rendering-when-direct3d-hardware-is-not-available)
    -   [Aproveitando os recursos existentes para renderização de software](#leveraging-existing-resources-for-software-rendering)
    -   [Habilitando cenários que não exigem hardware gráfico](#enabling-scenarios-that-do-not-require-graphics-hardware)
    -   [Concluindo a plataforma de gráficos DirectX](#completing-the-directx-graphics-platform)
-   [Recursos e requisitos de detorção](#warp-capabilities-and-requirements)
-   [Como usar WARP](#how-to-use-warp)
-   [Tipos de aplicativos recomendados para WARP](#recommended-application-types-for-warp)
    -   [Jogos casuais](#casual-games)
    -   [Aplicativos que não são de jogos existentes](#existing-non-gaming-applications)
    -   [Jogos de renderização avançada](#advanced-rendering-games)
    -   [Outros aplicativos](#other-applications)
-   [Arquitetura WARP e desempenho](#warp-architecture-and-performance)
-   [Conformidade com WARP](#warp-conformance)

## <a name="what-is-warp"></a>O que é WARP?

WARP é um rasterizador de software totalmente compatível e de alta velocidade. É um componente da tecnologia gráfica do DirectX que foi introduzido pelo tempo de execução do Direct3D 11. O tempo de execução do Direct3D 11 é instalado no Windows 7, no Windows Server 2008 R2 e no Windows Vista com a \[ atualização do KB971644 \] . O Windows 8, o Windows 10, o Windows Server 2012 & acima e o Windows RT incluem o tempo de execução do Direct3D 11,1, que tem uma versão atualizada de WARP. A atualização do Windows 10 outono Creators (1709) inclui uma versão de WARP que dá suporte a tempos de execução do Direct3D 11 e do Direct3D 12.

## <a name="warp-benefits"></a>Benefícios da distorção

WARP oferece os seguintes benefícios:

-   [Removendo a necessidade de Rasterizadores de software personalizados](#removing-the-need-for-custom-software-rasterizers)
-   [Habilitando o desempenho máximo de hardware de gráficos](#enabling-maximum-performance-from-graphics-hardware)
-   [Habilitando a renderização quando o hardware do Direct3D não está disponível](#enabling-rendering-when-direct3d-hardware-is-not-available)
-   [Aproveitando os recursos existentes para renderização de software](#leveraging-existing-resources-for-software-rendering)
-   [Habilitando cenários que não exigem hardware gráfico](#enabling-scenarios-that-do-not-require-graphics-hardware)
-   [Concluindo a plataforma de gráficos DirectX](#completing-the-directx-graphics-platform)

### <a name="removing-the-need-for-custom-software-rasterizers"></a>Removendo a necessidade de Rasterizadores de software personalizados

A distorção simplifica o desenvolvimento removendo a necessidade de criar um rasterizador de software personalizado e ajustar seu aplicativo para ele, em vez de ajustar seu aplicativo para hardware. Ao fornecer um rasterizador de software único e de uso geral, você não precisa mais escrever algoritmos de renderização de imagem de várias maneiras para executar hardware ou software com recursos e funcionalidades diferentes. Você ainda pode implementar algoritmos de várias maneiras para obter melhor desempenho ou dimensionamento; no entanto, você não precisa alterar a API ou a arquitetura de renderização usada para implementar esses algoritmos. Em vez disso, você pode se concentrar na criação de um grande aplicativo Direct3D 10 ou posterior que terá a mesma aparência e um bom desempenho no hardware ou no software.

### <a name="enabling-maximum-performance-from-graphics-hardware"></a>Habilitando o desempenho máximo de hardware de gráficos

Quando um aplicativo é ajustado para ser executado com eficiência no hardware, ele também será executado de forma eficiente em dewarp. O inverso também é verdadeiro; qualquer aplicativo que esteja ajustado para ser executado bem na distorção terá um bom desempenho no hardware. Os aplicativos que usam o Direct3D 10 e posterior podem não ser dimensionados de forma eficiente em hardwares diferentes. WARP tem perfis de desempenho semelhantes ao hardware, portanto, ajustar um aplicativo para lotes grandes, minimizar alterações de estado, remover pontos de sincronização ou bloqueios irá beneficiar o hardware e a deformação.

### <a name="enabling-rendering-when-direct3d-hardware-is-not-available"></a>Habilitando a renderização quando o hardware do Direct3D não está disponível

WARP permite a renderização rápida em várias situações em que as implementações de hardware são indesejáveis ou indisponíveis, incluindo:

-   Quando o usuário não tem nenhum hardware compatível com Direct3D
-   Quando um aplicativo é executado como um serviço ou em um ambiente de servidor
-   Quando um aplicativo deseja reservar os recursos de hardware do Direct3D para outros usos
-   Quando uma placa de vídeo não está instalada
-   Quando um driver de vídeo não está disponível ou não está funcionando corretamente
-   Quando uma placa de vídeo está sem memória, trava ou leva muitos recursos do sistema para inicializar

### <a name="leveraging-existing-resources-for-software-rendering"></a>Aproveitando os recursos existentes para renderização de software

Há uma enorme comunidade, muitos livros, sites, SDKs, exemplos, White papers, listas de endereçamento e outros recursos que podem ajudá-lo a aproveitar o Direct3D 10 e o processamento de imagens mais recente com base no sombreador. Com a distorção como um fallback de software, você pode usar o conhecimento existente sobre o hardware para melhorar o desempenho do seu aplicativo quando ele é executado com hardware ou software. Além disso, muitas ferramentas excelentes dos fornecedores de placas gráficas e do SDK do DirectX podem ajudá-lo a projetar, criar, desenvolver, depurar e analisar problemas de desempenho de aplicativos gráficos. Essas ferramentas e o conhecimento agora podem beneficiar o desenvolvimento de aplicativos direcionados ao hardware e ao software quando você usa WARP.

### <a name="enabling-scenarios-that-do-not-require-graphics-hardware"></a>Habilitando cenários que não exigem hardware gráfico

Vários algoritmos e aplicativos (algoritmos de processamento de imagens, impressão, comunicação remota, PCs virtuais e outros emuladores, renderização de fonte de alta qualidade, gráficos, grafos etc.) normalmente foram otimizados para a CPU porque não dependem do hardware. Com o WARP, você pode usar uma única arquitetura que executa esses algoritmos e aplicativos e que pode ser executada totalmente no software; Ainda assim, se a aceleração de hardware estiver disponível, você poderá tirar proveito dela.

### <a name="completing-the-directx-graphics-platform"></a>Concluindo a plataforma de gráficos DirectX

WARP permite que você acesse todos os recursos gráficos do Direct3D 10 e posteriores, mesmo em computadores sem hardware de gráficos Direct3D 10 e posteriores. Bits de funcionalidade removidos do Direct3D 10 (CAPS); ou seja, você não precisa mais verificar se os recursos gráficos estão disponíveis de hardware de gráficos porque o Direct3D 10 e posterior garante essa disponibilidade. Agora você pode usar todos os recursos de uma ampla gama de placas de vídeo sabendo que seu aplicativo se comportará e terá a mesma aparência em todos os lugares. Você pode dimensionar o desempenho desses aplicativos simplesmente desabilitando recursos gráficos caros em placas de vídeo low end ou renderizando para destinos menores.

## <a name="warp-capabilities-and-requirements"></a>Recursos e requisitos de detorção

A distorção dá suporte total a todos os recursos do Direct3D 10 e 10,1. Por exemplo, WARP dá suporte aos seguintes recursos mais importantes:

-   Todos os requisitos de precisão da especificação do Direct3D 10 e 10,1
-   Direct3D 11 quando usado com os níveis de recursos 9 \_ 1, 9 \_ 2, 9 \_ 3, 10 \_ 0 e 10 \_ 1 (para obter mais informações sobre os níveis de recursos, consulte [**nível de \_ recurso \_ do D3D**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level))
-   Todos os formatos de textura opcionais, como destinos de renderização de multiamostração e amostragem de superfícies flutuantes
-   Processamento com suavização de alta qualidade até 8x de anti-aliasing com multiamostragens (MSAA)
-   Filtragem de anisotropic
-   aplicativos de 32 bits e de 64 bits e aplicativos de 32 bits com reconhecimento de endereço grande

Quando você instala a [atualização de plataforma para o Windows 7](https://support.microsoft.com/kb/2670838) no Windows 7 SP1 ou no windows Server 2008 R2 SP1, esse sistema operacional inclui o tempo de execução do Direct3D 11,1 e uma versão de Warp que dá suporte ao Direct3D 11. x quando usado com [os níveis de recurso](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 \_ 1, 9 \_ 2, 9 \_ 3, 10 \_ 0, 10 \_ 1 e 11 \_ 0.

O Windows 8, o Windows 10, o Windows Server 2012 & acima e o Windows RT incluem o tempo de execução do Direct3D 11,1 e uma nova versão da WARP. Esta versão dá suporte ao Direct3D 11. x quando usado com [os níveis de recurso](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 \_ 1, 9 \_ 2, 9 \_ 3, 10 \_ 0, 10 \_ 1, 11 \_ 0 e 11 \_ 1.

A atualização do Windows 10 outono Creators (1709) inclui uma nova versão de WARP que dá suporte aos níveis de recurso do [Direct3D 12](../direct3d12/direct3d-12-graphics.md) 12 \_ 0 e 12 \_ 1. 

Os requisitos mínimos do computador para WARP são os mesmos para o Windows Vista, especificamente:

-   CPU mínima de 800 MHz
-   O MMX, o SSE ou o SSE2 não é necessário
-   Mínimo de 512 MB de RAM

## <a name="how-to-use-warp"></a>Como usar WARP

Os componentes do Direct3D 10, 10,1, 11 e 12 podem usar um tipo de driver adicional que você pode especificar ao criar o dispositivo (por exemplo, ao chamar a função [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice) ). Esse tipo de driver é [**d3d10 tipo de driver \_ \_ \_ Warp**](/windows/desktop/api/d3d10misc/ne-d3d10misc-d3d10_driver_type) ou Warp de [**tipo de \_ Driver \_ \_ D3D**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_driver_type). Quando você especifica esse tipo de driver, o tempo de execução cria um dispositivo de detorção e não inicializa um dispositivo de hardware.

Como WARP usa a mesma interface de software do Direct3D que o rasterizador de referência, qualquer aplicativo Direct3D que possa dar suporte à execução com o rasterizador de referência poderá ser testado usando WARPing. Para usar WARP, renomeie D3d10warp.dll para D3d10ref.dll e coloque-o na mesma pasta que o exemplo ou aplicativo. Em seguida, quando você alternar para ref, verá a renderização WARP.

Se você renomear WARP para D3d10ref.dll e colocá-lo em C: \\ arquivos de programas (x86) \\ Microsoft DirectX SDK (junho de 2010) \\ amostras \\ C++ \\ Direct3D \\ bin \\ x86, você pode executar todos os exemplos do DirectX em relação à deformação, clicando no botão "alternar ref" no exemplo ou executando o exemplo com/ref especificado na linha de comando.

## <a name="recommended-application-types-for-warp"></a>Tipos de aplicativos recomendados para WARP

Todos os aplicativos que podem usar o Direct3D podem usar WARP. Isso inclui os seguintes tipos de aplicativos:

-   [Jogos casuais](#casual-games)
-   [Aplicativos que não são de jogos existentes](#existing-non-gaming-applications)
-   [Jogos de renderização avançada](#advanced-rendering-games)
-   [Outros aplicativos](#other-applications)

### <a name="casual-games"></a>Jogos casuais

Os jogos normalmente têm requisitos de renderização simples. No entanto, eles também exigem o uso de efeitos visuais impressionantes que podem precisar de aceleração de hardware. A maioria dos títulos de jogos mais vendidos para o Windows são simulações ou jogos casuais, nenhum dos quais requer gráficos de alto desempenho. No entanto, os dois estilos de jogos se beneficiam muito de gráficos modernos baseados em sombreador e a capacidade de dimensionar em hardware.

### <a name="existing-non-gaming-applications"></a>Aplicativos que não são de jogos existentes

Uma grande quantidade de aplicativos gráficos requer um número mínimo de caminhos de código em sua camada de renderização. WARP permite que esses aplicativos implementem um único caminho de código Direct3D que pode ter como alvo um grande número de configurações de computador.

### <a name="advanced-rendering-games"></a>Jogos de renderização avançada

Os desenvolvedores de jogos podem querer isolar erros de renderização específicos de driver ou placa gráfica. Portanto, todos os jogos, até mesmo jogos altamente exigentes, podem se beneficiar da capacidade de processar o conteúdo usando WARP. Você pode usar WARP para validar se os artefatos visuais que você encontrar estão processando erros ou problemas com hardware ou drivers.

### <a name="other-applications"></a>Outros aplicativos

Os aplicativos de destino para WARP também incluem aqueles que podem não usar o Direct3D 10 ou Direct3D 10,1 no momento. Esses aplicativos de destino incluem aplicativos que devem sempre funcionar em todos os computadores, aplicativos de processamento de imagens que não gravam versões de CPU e GPU de algoritmos de processamento de imagens, algoritmos de processamento de imagens em que a velocidade ou o uso da GPU não é essencial, como impressão, e emuladores e ambientes virtuais que exibem gráficos 3D avançados.

## <a name="warp-architecture-and-performance"></a>Arquitetura WARP e desempenho

WARP é baseado na base de código do rasterizador de referência. Portanto, WARP usa a mesma interface de software para Direct3D 10 e posterior e DXGI. A distorção está incluída no Windows 7 na D3d10warp.dll, localizada em pastas de sistemas do Windows. Duas versões de WARP são instaladas em computadores de 64 bits, uma versão x86 e x64. A versão x64 pode ser executada mais rapidamente em determinadas circunstâncias porque o gerador de código contido na distorção pode aproveitar os registros adicionais que estão disponíveis quando os usuários executam aplicativos de 64 bits.

WARP contém os dois compiladores em tempo real de alta velocidade a seguir:

-   O compilador de linguagem intermediária de alto nível que converte o código de bytes HLSL e o estado de renderização atual em um fluxo otimizado de comandos de vetor para os estágios do sombreador de Geometry (GS), do sombreador de vértice (VS) e do sombreador de pixel (PS) do pipeline.
-   O gerador de código just-in-time de alto desempenho que pode usar esses comandos e gerar o código de assembly SSE2, SSE 4.1, x86, x64, ARM e arm64 otimizado.

WARP usa o pool de threads e o gerenciamento de tarefas complexo e o controle de dependência que foi introduzido no Windows Vista para permitir que todas as partes do pipeline de renderização sejam distribuídas com eficiência entre os núcleos de CPU disponíveis.

WARP usa renderização adiada. Ou seja, WARP pode renderizar comandos de renderização para que a rasterização ocorra somente quando dados suficientes estiverem disponíveis para usar todos os recursos de CPU com eficiência. O trabalho no thread do aplicativo principal é minimizado para permitir que o aplicativo envie comandos o mais rápido possível. Se um aplicativo também tiver vários threads e ele usar o pool de threads, o trabalho será distribuído uniformemente entre a distorção e o aplicativo.

O gerador de código WARP foi ajustado para fazer o melhor uso da arquitetura de CPU moderna. A distorção é executada em todos os computadores que podem executar o Windows Vista e sistemas operacionais posteriores, mesmo que o computador não ofereça suporte a SSE. No entanto, a distorção foi otimizada para computadores que dão suporte a SSE2. Ele também contém otimizações para arquiteturas específicas de processadores AMD e Intel, bem como suporte para as extensões SSE 4,1.

WARP não requer que o hardware de gráficos seja executado. Ele pode ser executado mesmo em situações em que o hardware não está disponível ou não pode ser inicializado.

Os aplicativos e exemplos criados e criados para execução em hardware Direct3D 10 e posteriores sem nenhum conhecimento de WARP provavelmente serão executados corretamente usando WARP. No entanto, recomendamos que você reduza as configurações de qualidade e a resolução o máximo possível para obter taxas de quadros utilizáveis. Você pode usar WARP para desenvolver e ajustar aplicativos que funcionam bem em hardware e software.

Como WARP usa vários núcleos de CPU, ele é executado melhor em CPUs de Quad Core modernas. A detorção também é executada significativamente mais rapidamente em computadores com as extensões SSE 4.1 instaladas. A Microsoft realizou testes e ajustes de desempenho significativos em computadores com oito ou mais núcleos e SSE 4.1, pois esses computadores high-end se tornarão mais comuns durante o tempo de vida do Windows 7 e sistemas operacionais posteriores.

Quando WARP é executado na CPU, ele é limitado em comparação a uma placa gráfica de várias maneiras. A velocidade do barramento frontal de uma CPU geralmente é maior ou menor que 10 GB/s. Por outro lado, uma placa gráfica geralmente tem memória dedicada que usa 20 a 100 GB/s ou mais de largura de banda gráfica. O hardware de gráficos também tem unidades de função fixas que podem executar tarefas complexas e caras, como filtragem de textura, descompactação de formato ou conversões, de forma assíncrona com pouca sobrecarga ou custo de energia. Executar essas operações em uma CPU típica é caro em termos de consumo de energia e ciclos de desempenho.

Os números de desempenho típicos para uma máquina Quad Core de 3,0 GHz Intel Penryn mostram que a distorção pode, em alguns casos, superar as GPUs de gráficos Direct3D 10 e posteriores integradas de baixo nível em vários benchmarks. O hardware de gráficos discretos de baixo nível geralmente é de 4 a 5 vezes mais rápido do que a WARP na execução desses parâmetros de comparação. Essas GPUs integradas ou discretas de low-end têm uso mínimo de recursos de CPU. As placas gráficas intermediárias ou de alto nível são significativamente mais rápidas do que a distorção para muitos aplicativos, especialmente quando um aplicativo pode aproveitar o paralelismo e a largura de banda de memória que essas placas gráficas fornecem.

A distorção não é uma substituição para o hardware de gráficos, particularmente, pois a execução do Direct3D 10 de baixo nível e do hardware discreto mais recente agora é barata. O objetivo da distorção é permitir que os aplicativos direcionem hardware de nível de Direct3D 10 sem ter caminhos de código significativamente diferentes ou requisitos de teste se eles são executados em hardware ou em software.

As duas tabelas a seguir mostram dados de exemplo WARP com várias CPUs e placas gráficas.

A primeira tabela mostra dados de exemplo de detorção com Direct3D 10 Crysis em execução em 800x600 com todas as configurações de qualidade em seus níveis mais baixos:

| CPU                         | Hora   | FPS de ave | FPS mín. | Quadro mín. | FPS máximo | Quadro máximo |
|-----------------------------|--------|---------|---------|-----------|---------|-----------|
| Core i7 8 Core @ 3,0 GHz     | 271,57 | 7.36    | 3,46    | 1966      | 15, 1   | 995       |
| Penryn 4 Core @ 3,0 GHz      | 351,35 | 5,69    | 2.49    | 1967      | 10,95   | 980       |
| Penryn 2 Core @ 3,0 GHz      | 573,98 | 3.48    | 1,35    | 1964      | 6,61    | 988       |
| Núcleo 2 Duo a 2,6 GHz         | 707,19 | 2,83    | 0.81    | 1959      | 5.18    | 982       |
| Core 2 Duo a 2,4 GHz         | 763,25 | 2.62    | 0.76    | 1964      | 4.70    | 984       |
| Núcleo 2 Duo a 2,1 GHz         | 908,87 | 2,20    | 0,64    | 1965      | 3.72    | 986       |
| Xeon 8 Core @ 2,0 GHz        | 424, 4 | 4,72    | 1,84    | 1967      | 9,56    | 988       |
| AMD FX74 4 núcleos a 3,0 GHz    | 583,12 | 3.43    | 1,41    | 1967      | 5,78    | 986       |
| Phenom 9550 4 core a 2,2 GHz | 664,69 | 3, 1    | 0,53    | 1959      | 5,46    | 987       |

A segunda tabela mostra os dados de exemplo que executam o mesmo teste em uma variedade de placas gráficas:

| Placa gráfica         | Hora   | FPS de ave | FPS mín. | Quadro mín. | FPS máximo | Quadro máximo |
|-----------------------|--------|---------|---------|-----------|---------|-----------|
| NVIDIA 8800 GTS       | 23,58  | 84,80   | 60,78   | 1957      | 130,83  | 1022      |
| NVIDIA 8500 GT        | 47,63  | 41,99   | 25,67   | 1986      | 72,57   | 991       |
| NVIDIA Quadro 290     | 67,16  | 29,78   | 18,19   | 1969      | 49,87   | 1017      |
| NVIDIA 8400 GS        | 59, 1  | 33,89   | 21,22   | 1962      | 51,82   | 1021      |
| ATI 3400              | 53,79  | 37,18   | 22,97   | 618       | 59,77   | 1021      |
| ATI 3200              | 67,19  | 29,77   | 18,91   | 1963      | 45,74   | 980       |
| ATI 2400 PRO          | 67, 4  | 29,83   | 17,97   | 606       | 45,91   | 987       |
| Intel DX10 integrado | 386,94 | 5.17    | 1,74    | 1974      | 16,22   | 995       |

## <a name="warp-conformance"></a>Conformidade com WARP

WARP transmite todos os testes de conformidade padrão do WHQL (Windows Hardware Quality Labs) para validar dispositivos de hardware Direct3D.

A detorção foi testada em um conjunto de aplicativos Direct3D 10 e Direct3D 10,1 e benchmarks e contra exemplos de SDK do DirectX, NVIDIA e AMD.

WARP usou a ferramenta de depuração e análise do [PIX](https://msdn.microsoft.com/library/ee417062(v=VS.85).aspx) para Windows em seu teste; A Microsoft tem uma grande biblioteca de capturas de quadro simples de aplicativos que são usados para comparar entre hardware e WARP. A maioria das imagens aparece quase idêntica entre hardware e distorção; onde as pequenas diferenças às vezes ocorrem, elas são encontradas dentro das tolerâncias definidas pela especificação do Direct3D 10.