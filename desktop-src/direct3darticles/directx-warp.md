---
title: Windows Guia do WARP (Advanced Rasterization Platform)
description: Este artigo descreve Windows WARP (Advanced Rasterization Platform) e os seguintes aspectos do WARP.
ms.assetid: C40A96EB-64AA-46EB-85A9-7C996ABC8BFE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bab76fd68985069e6114cd7bbb0901eeba5d911eba574332b1dd2008f0375a5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119745985"
---
# <a name="windows-advanced-rasterization-platform-warp-guide"></a>Windows Guia do WARP (Advanced Rasterization Platform)

Este artigo descreve Windows WARP (Advanced Rasterization Platform) e os seguintes aspectos do WARP.

-   [O que é o WARP?](#what-is-warp)
-   [Benefícios do WARP](#warp-benefits)
    -   [Removendo a necessidade de rasterizadores de software personalizados](#removing-the-need-for-custom-software-rasterizers)
    -   [Habilitando o desempenho máximo do hardware gráfico](#enabling-maximum-performance-from-graphics-hardware)
    -   [Habilitando a renderização quando o hardware Direct3D não está disponível](#enabling-rendering-when-direct3d-hardware-is-not-available)
    -   [Aproveitando os recursos existentes para renderização de software](#leveraging-existing-resources-for-software-rendering)
    -   [Habilitando cenários que não exigem hardware gráfico](#enabling-scenarios-that-do-not-require-graphics-hardware)
    -   [Concluindo a plataforma de gráficos DirectX](#completing-the-directx-graphics-platform)
-   [Requisitos e funcionalidades de WARP](#warp-capabilities-and-requirements)
-   [Como usar o WARP](#how-to-use-warp)
-   [Tipos de aplicativo recomendados para WARP](#recommended-application-types-for-warp)
    -   [Jogos casuais](#casual-games)
    -   [Aplicativos não jogos existentes](#existing-non-gaming-applications)
    -   [Jogos de renderização avançada](#advanced-rendering-games)
    -   [Outros aplicativos](#other-applications)
-   [Arquitetura e desempenho de WARP](#warp-architecture-and-performance)
-   [Conformidade com WARP](#warp-conformance)

## <a name="what-is-warp"></a>O que é o WARP?

O WARP é um rasterizador de software de alta velocidade e totalmente compatível. É um componente da tecnologia de gráficos DirectX que foi introduzida pelo runtime do Direct3D 11. O runtime do Direct3D 11 é instalado no Windows 7, no Windows Server 2008 R2 e no Windows Vista com a atualização \[ KB971644. \] Windows 8, Windows 10, Windows Server 2012 & acima e Windows RT incluem o runtime do Direct3D 11.1, que tem uma versão atualizada do WARP. Windows 10 Fall Creators Update (1709) inclui uma versão do WARP que dá suporte a runtimes direct3D 11 e Direct3D 12.

## <a name="warp-benefits"></a>Benefícios do WARP

O WARP oferece os seguintes benefícios:

-   [Removendo a necessidade de rasterizadores de software personalizados](#removing-the-need-for-custom-software-rasterizers)
-   [Habilitando o desempenho máximo do hardware gráfico](#enabling-maximum-performance-from-graphics-hardware)
-   [Habilitando a renderização quando o hardware Direct3D não está disponível](#enabling-rendering-when-direct3d-hardware-is-not-available)
-   [Aproveitando os recursos existentes para renderização de software](#leveraging-existing-resources-for-software-rendering)
-   [Habilitando cenários que não exigem hardware gráfico](#enabling-scenarios-that-do-not-require-graphics-hardware)
-   [Concluindo a plataforma de gráficos DirectX](#completing-the-directx-graphics-platform)

### <a name="removing-the-need-for-custom-software-rasterizers"></a>Removendo a necessidade de rasterizadores de software personalizados

O WARP simplifica o desenvolvimento removendo a necessidade de criar um rasterizador de software personalizado e ajustar seu aplicativo para ele em vez de ajustar seu aplicativo para hardware. Ao fornecer um único rasterizador de software de uso geral, você não precisa mais escrever algoritmos de renderização de imagem de várias maneiras para ser executado em hardware ou software com recursos e funcionalidades diferentes. Você ainda pode implementar algoritmos de várias maneiras para obter um melhor desempenho ou dimensionamento; no entanto, você não precisa alterar a API ou a arquitetura de renderização usada para implementar esses algoritmos. Em vez disso, você pode se concentrar na criação de um ótimo aplicativo Direct3D 10 ou posterior que terá a mesma aparência e terá um bom desempenho no hardware ou no software.

### <a name="enabling-maximum-performance-from-graphics-hardware"></a>Habilitando o desempenho máximo do hardware gráfico

Quando um aplicativo é ajustado para ser executado com eficiência no hardware, ele também será executado com eficiência no WARP. O inverso também é verdadeiro; qualquer aplicativo ajustado para ser executado bem no WARP terá um bom desempenho no hardware. Aplicativos que usam o Direct3D 10 e posterior de forma ineficiente podem não ser dimensionados com eficiência em hardwares diferentes. O WARP tem perfis de desempenho semelhantes ao hardware, portanto, ajustar um aplicativo para lotes grandes, minimizar as alterações de estado, remover pontos de sincronização ou bloqueios beneficiará o hardware e o WARP.

### <a name="enabling-rendering-when-direct3d-hardware-is-not-available"></a>Habilitando a renderização quando o hardware Direct3D não está disponível

O WARP permite renderização rápida em uma variedade de situações em que as implementações de hardware são indesejáveis ou indisponíveis, incluindo:

-   Quando o usuário não tem nenhum hardware com capacidade para Direct3D
-   Quando um aplicativo é executado como um serviço ou em um ambiente de servidor
-   Quando um aplicativo deseja reservar os recursos de hardware direct3D para outros usos
-   Quando uma placa de vídeo não está instalada
-   Quando um driver de vídeo não está disponível ou não está funcionando corretamente
-   Quando uma placa de vídeo está sem memória, trava ou levaria muitos recursos do sistema para inicializar

### <a name="leveraging-existing-resources-for-software-rendering"></a>Aproveitando os recursos existentes para renderização de software

Há uma grande comunidade, muitos livros, sites, SDKs, exemplos, white papers, listas de emails e outros recursos que podem ajudá-lo a aproveitar a renderização de imagem baseada em sombreador do Direct3D 10 e posterior. Com o WARP como um fallback de software, você pode usar o conhecimento existente sobre hardware para melhorar o desempenho do seu aplicativo quando ele é executado com hardware ou software. Além disso, muitas excelentes ferramentas dos fornecedores de cartão gráfico e no SDK do DirectX podem ajudá-lo a projetar, criar, desenvolver, depurar e analisar problemas de desempenho de aplicativos gráficos. Essas ferramentas e conhecimento agora podem beneficiar o desenvolvimento de aplicativos destinados a hardware e software quando você usa o WARP.

### <a name="enabling-scenarios-that-do-not-require-graphics-hardware"></a>Habilitando cenários que não exigem hardware gráfico

Vários algoritmos e aplicativos (algoritmos de processamento de imagem, impressão, comunicação remot, PCs virtuais e outros emuladores, renderização de fonte de alta qualidade, gráficos, grafos e assim por diante) normalmente foram otimizados para a CPU porque não dependem do hardware. Com o WARP, você pode usar uma única arquitetura que executa esses algoritmos e aplicativos e que pode ser executado totalmente no software; ainda assim, se a aceleração de hardware estiver disponível, você poderá tirar proveito dela.

### <a name="completing-the-directx-graphics-platform"></a>Concluindo a plataforma de gráficos DirectX

O WARP permite que você acesse todos os recursos gráficos do Direct3D 10 e posteriores, mesmo em computadores sem hardware gráfico Do Direct3D 10 e posterior. Bits de funcionalidade removidos do Direct3D 10 (caps); ou seja, você não precisa mais verificar se os recursos gráficos estão disponíveis no hardware de gráficos porque o Direct3D 10 e posterior garante essa disponibilidade. Agora você pode usar todos os recursos de uma ampla variedade de placas de vídeo sabendo que seu aplicativo se comportará e terá a mesma aparência em todos os lugares. Você pode dimensionar o desempenho desses aplicativos simplesmente desabilitando recursos gráficos caros em placas de vídeo de baixa extremidade ou renderização para destinos menores.

## <a name="warp-capabilities-and-requirements"></a>Requisitos e funcionalidades de WARP

O WARP dá suporte total a todos os recursos do Direct3D 10 e 10.1. Por exemplo, o WARP dá suporte aos seguintes recursos mais importantes:

-   Todos os requisitos de precisão das especificações direct3D 10 e 10.1
-   Direct3D 11 quando usado com os níveis de recurso 9 \_ 1, 9 \_ 2, 9 \_ 3, 10 0 e \_ 10 1 (para obter mais informações sobre níveis de recursos, consulte \_ [**D3D \_ FEATURE \_ LEVEL**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level))
-   Todos os formatos de textura opcionais, como destinos de renderização multisample e amostragem de superfícies float
-   Renderização de alta qualidade e antialiased até 8x MSAA (antialiasing multisample)
-   Filtragem anisocar
-   Aplicativos de 32 bits e 64 bits e aplicativos de 32 bits com conhecimento de endereço grande

Ao instalar a Atualização da Plataforma [para Windows 7](https://support.microsoft.com/kb/2670838) no Windows 7 SP1 ou Windows Server 2008 R2 SP1, esse sistema operacional inclui o runtime do Direct3D 11.1 e uma versão do WARP que dá suporte ao Direct3D 11.x quando usado com os níveis [de](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) recurso 9 \_ 1, 9 \_ 2, \_ 9 3, 10 \_ 0, 10 1 e \_ 11 \_ 0.

Windows 8, Windows 10, Windows Server 2012 & acima e Windows RT incluem o runtime do Direct3D 11.1 e uma nova versão do WARP. Esta versão dá suporte ao Direct3D 11.x quando usado com os níveis de recurso [9](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) \_ 1, \_ 9 2, 9 \_ 3, 10 \_ 0, \_ 10 1, 11 0 e \_ 11 \_ 1.

Windows 10 Fall Creators Update (1709) inclui uma nova versão do WARP que dá suporte aos níveis de recurso 12 0 e 12 1 do [Direct3D 12.](../direct3d12/direct3d-12-graphics.md) \_ \_ 

Os requisitos mínimos do computador para o WARP são os mesmos do Windows Vista, especificamente:

-   CPU mínima de 800 MHz
-   MMX, SSE ou SSE2 não é necessário
-   Mínimo de 512 MB de RAM

## <a name="how-to-use-warp"></a>Como usar o WARP

Os componentes Direct3D 10, 10.1, 11 e 12 podem usar um tipo de driver adicional que você pode especificar ao criar o dispositivo (por exemplo, quando você chama a função [**D3D11CreateDevice).**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice) Esse tipo de driver é [**D3D10 \_ DRIVER \_ TYPE \_ WARP**](/windows/desktop/api/d3d10misc/ne-d3d10misc-d3d10_driver_type) ou [**D3D \_ DRIVER TYPE \_ \_ WARP**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_driver_type). Quando você especifica esse tipo de driver, o runtime cria um dispositivo WARP e não inicializa um dispositivo de hardware.

Como o WARP usa a mesma interface de software para Direct3D que o rasterizador de referência, qualquer aplicativo Direct3D que possa dar suporte à execução com o rasterizador de referência pode ser testado usando o WARP. Para usar o WARP, renomeie D3d10warp.dll para D3d10ref.dll e coloque-o na mesma pasta que o exemplo ou o aplicativo. Em seguida, ao alternar para ref, você verá a renderização DE DISTORÇÃO.

Se você renomear o WARP para D3d10ref.dll e colocar em C: Arquivos de Programas \\ (x86) \\ SDK do Microsoft DirectX (junho de 2010) Exemplos de \\ \\ C++ \\ Direct3D \\ Bin \\ x86, você poderá executar todos os exemplos do DirectX no WARP, seja clicando no botão "Alternar Ref" no exemplo ou executando o exemplo com /ref especificado na linha de comando.

## <a name="recommended-application-types-for-warp"></a>Tipos de aplicativo recomendados para WARP

Todos os aplicativos que podem usar o Direct3D podem usar o WARP. Isso inclui os seguintes tipos de aplicativos:

-   [Jogos casuais](#casual-games)
-   [Aplicativos não jogos existentes](#existing-non-gaming-applications)
-   [Jogos de renderização avançada](#advanced-rendering-games)
-   [Outros aplicativos](#other-applications)

### <a name="casual-games"></a>Jogos casuais

Normalmente, os jogos têm requisitos de renderização simples. No entanto, eles também exigem o uso de efeitos visuais incríveis que podem precisar de aceleração de hardware. A maioria dos títulos de jogos mais vendidos para Windows são simulações ou jogos casuais, nenhum dos quais requer gráficos de alto desempenho. No entanto, ambos os estilos de jogos se beneficiam muito de gráficos modernos baseados em sombreador e da capacidade de dimensionar em hardware.

### <a name="existing-non-gaming-applications"></a>Aplicativos não jogos existentes

Uma grande quantidade de aplicativos gráficos exige um número mínimo de caminhos de código em sua camada de renderização. O WARP permite que esses aplicativos implementem um único caminho de código Direct3D que pode ser destinado a um grande número de configurações de computador.

### <a name="advanced-rendering-games"></a>Jogos de renderização avançada

Os desenvolvedores de jogos podem querer isolar erros de renderização de cartão gráfico ou de driver específicos. Portanto, todos os jogos, mesmo jogos extremamente exigentes graficamente, podem se beneficiar da capacidade de renderizar seu conteúdo usando o WARP. Você pode usar o WARP para validar se os artefatos visuais encontrados são erros de renderização ou problemas com hardware ou drivers.

### <a name="other-applications"></a>Outros aplicativos

Os aplicativos de destino para WARP também incluem aqueles que podem não usar o Direct3D 10 ou o Direct3D 10.1 no momento. Esses aplicativos de destino incluem aplicativos que sempre devem funcionar em todos os computadores, aplicativos de processamento de imagem que não escrevem versões de CPU e GPU de algoritmos de processamento de imagem, algoritmos de processamento de imagem em que a velocidade ou o uso da GPU não é crítico, como impressão e emuladores e ambientes virtuais que exibem gráficos 3D avançados.

## <a name="warp-architecture-and-performance"></a>Arquitetura e desempenho de WARP

O WARP é baseado na base de código do rasterizador de referência. Portanto, o WARP usa a mesma interface de software para Direct3D 10 e posterior e DXGI. O WARP está incluído no Windows 7 no D3d10warp.dll, localizado em Windows de sistemas. Duas versões do WARP são instaladas em máquinas de 64 bits, uma versão x86 e x64. A versão x64 pode ser executado mais rapidamente em determinadas circunstâncias porque o gerador de código contido em WARP pode aproveitar os registros adicionais disponíveis quando os usuários executarem aplicativos de 64 bits.

O WARP contém os dois compiladores de alta velocidade e em tempo real a seguir:

-   O compilador de linguagem intermediária de alto nível que converte o código de byte de HLSL e o estado de renderização atual em um fluxo otimizado de comandos de vetor para os estágios de sombreador de geometria (GS), VS (sombreador de vértice) e PS (sombreador de pixel) do pipeline.
-   O gerador de código Just-In-Time de alto desempenho que pode usar esses comandos e gerar código de assembly SSE2, SSE4.1, x86, x64, arm e arm64 otimizados.

O WARP usa o pool de threads e o gerenciamento complexo de tarefas e o acompanhamento de dependência que foi introduzido no Windows Vista para permitir que todas as partes do pipeline de renderização sejam distribuídas com eficiência entre os núcleos de CPU disponíveis.

O WARP usa a renderização adiada. Ou seja, o WARP pode renderizar comandos em lote para que a rasterização ocorra somente quando dados suficientes estão disponíveis para usar todos os recursos de CPU com eficiência. O trabalho no thread principal do aplicativo é minimizado para permitir que o aplicativo envie comandos o mais rápido possível. Se um aplicativo também for multi-threaded e usar o pool de threads, o trabalho será distribuído uniformemente entre o WARP e o aplicativo.

O gerador de código WARP foi ajustado para fazer melhor uso da arquitetura de CPU moderna. O WARP é executado em todos os computadores que podem executar Windows Vista e sistemas operacionais posteriores, mesmo se o computador não dá suporte à SSE. No entanto, o WARP foi otimizado para computadores que têm suporte para SSE2. Ele também contém otimizações para arquiteturas específicas de processadores AMD e Intel, bem como suporte para as extensões SSE 4.1.

O WARP não exige a execução de hardware de gráficos. Ele pode ser executado mesmo em situações em que o hardware não está disponível ou não pode ser inicializado.

Aplicativos e exemplos que foram projetados e criados para ser executados no Hardware Direct3D 10 e posterior sem nenhum conhecimento do WARP provavelmente funcionarão bem usando o WARP. No entanto, recomendamos que você reduza as configurações de qualidade e a resolução tanto quanto possível para obter taxas de quadros usáveis. Você pode usar o WARP para desenvolver e ajustar aplicativos que são executados bem em hardware e software.

Como o WARP usa vários núcleos de CPU, ele tem o melhor desempenho em CPUs modernas de núcleo quad. O WARP também é executado significativamente mais rapidamente em computadores com extensões SSE4.1 instaladas. A Microsoft realizou testes e ajuste de desempenho significativos em computadores com oito ou mais núcleos e SSE4.1 porque esses computadores de alto nível se tornarão mais comuns durante o tempo de vida do Windows 7 e sistemas operacionais posteriores.

Quando o WARP está em execução na CPU, ele é limitado em comparação com uma placa gráfica de várias maneiras. A velocidade do barramento frontal de uma CPU normalmente é em torno ou abaixo de 10 GB/s. Por outro lado, uma placa gráfica geralmente tem memória dedicada que usa de 20 a 100 GB/s ou mais de largura de banda de gráficos. O hardware gráfico também tem unidades de função fixa que podem executar tarefas complexas e caras, como filtragem de textura, descompactação de formato ou conversões, de forma assíncrona com pouca sobrecarga ou custo de energia. Executar essas operações em uma CPU típica é caro em termos de consumo de energia e ciclos de desempenho.

Os números de desempenho típicos para um computador Intel Pen meio núcleo com base em 3,0 GHz mostram que o WARP pode, em alguns casos, superar o desempenho de GPUs gráficas integradas de baixo nível direct3D 10 e posteriores em vários parâmetros de comparação. O hardware gráfico discreto de baixo nível normalmente é de 4 a 5 vezes mais rápido do que o WARP na execução desses parâmetros de comparação. Essas GPUs integradas ou discretas de baixo nível têm uso mínimo de recursos de CPU. As placas gráficas de médio ou alto nível são significativamente mais rápidas do que o WARP para muitos aplicativos, especialmente quando um aplicativo pode aproveitar o paralelismo e a largura de banda de memória que essas placas gráficas fornecem.

O WARP não é uma substituição para hardware de gráficos, especialmente porque executar razoavelmente o Direct3D 10 de baixo nível e hardware discreto posterior agora é barato. O objetivo do WARP é permitir que os aplicativos sejam destinados ao hardware de nível 10 do Direct3D sem ter caminhos de código significativamente diferentes ou requisitos de teste, independentemente de eles executarem em hardware ou em software.

As duas tabelas a seguir mostram dados de exemplo de WARP com várias CPUs e placas gráficas.

A primeira tabela mostra dados de exemplo de WARP com o Direct3D 10 TheIs em execução a 800 x 600 com todas as configurações de qualidade em seus níveis mais baixos:

| CPU                         | Tempo   | Av. FPS | FPS mínimo | Quadro mínimo | FPS máximo | Quadro máximo |
|-----------------------------|--------|---------|---------|-----------|---------|-----------|
| Core i7 8 Core @ 3,0 GHz     | 271.57 | 7.36    | 3,46    | 1966      | 15.01   | 995       |
| Pen meio a 4 núcleos @ 3,0 GHz      | 351.35 | 5.69    | 2.49    | 1967      | 10.95   | 980       |
| Pen meio a 2 núcleos @ 3,0 GHz      | 573.98 | 3.48    | 1.35    | 1964      | 6.61    | 988       |
| Core 2 Duo @ 2,6 GHz         | 707.19 | 2.83    | 0.81    | 1959      | 5.18    | 982       |
| Core 2 Duo @ 2,4 GHz         | 763.25 | 2.62    | 0.76    | 1964      | 4.70    | 984       |
| Core 2 Duo @ 2,1 GHz         | 908.87 | 2,20    | 0.64    | 1965      | 3.72    | 986       |
| Xeon 8 Core @ 2,0 GHz        | 424, 4 | 4.72    | 1,84    | 1967      | 9,56    | 988       |
| AMD FX74 4 núcleos a 3,0 GHz    | 583,12 | 3.43    | 1,41    | 1967      | 5,78    | 986       |
| Phenom 9550 4 core a 2,2 GHz | 664,69 | 3,01    | 0,53    | 1959      | 5.46    | 987       |

A segunda tabela mostra os dados de exemplo que executam o mesmo teste em uma variedade de placas gráficas:

| Placa gráfica         | Tempo   | FPS de ave | FPS mín. | Quadro mín. | FPS máximo | Quadro máximo |
|-----------------------|--------|---------|---------|-----------|---------|-----------|
| NVIDIA 8800 GTS       | 23,58  | 84,80   | 60,78   | 1957      | 130,83  | 1022      |
| NVIDIA 8500 GT        | 47,63  | 41,99   | 25,67   | 1986      | 72,57   | 991       |
| NVIDIA Quadro 290     | 67,16  | 29,78   | 18,19   | 1969      | 49,87   | 1017      |
| NVIDIA 8400 GS        | 59, 1  | 33,89   | 21,22   | 1962      | 51,82   | 1021      |
| ATI 3400              | 53,79  | 37,18   | 22,97   | 618       | 59,77   | 1021      |
| ATI 3200              | 67,19  | 29,77   | 18,91   | 1963      | 45,74   | 980       |
| ATI 2400 PRO          | 67, 4  | 29,83   | 17,97   | 606       | 45,91   | 987       |
| Intel DX10 integrado | 386,94 | 5.17    | 1.74    | 1974      | 16,22   | 995       |

## <a name="warp-conformance"></a>Conformidade com WARP

WARP transmite todos os testes de conformidade do WHQL (Hardware Quality Labs) padrão Windows para validar dispositivos de Hardware Direct3D.

A detorção foi testada em um conjunto de aplicativos Direct3D 10 e Direct3D 10,1 e benchmarks e contra exemplos de SDK do DirectX, NVIDIA e AMD.

WARP usou a ferramenta de depuração e análise do [PIX](https://msdn.microsoft.com/library/ee417062(v=VS.85).aspx) para Windows em seu teste; A Microsoft tem uma grande biblioteca de capturas de quadro simples de aplicativos que são usados para comparar entre hardware e WARP. A maioria das imagens aparece quase idêntica entre hardware e distorção; onde as pequenas diferenças às vezes ocorrem, elas são encontradas dentro das tolerâncias definidas pela especificação do Direct3D 10.