---
title: Windows Toolkit de avaliação
description: Windows Toolkit de avaliação
ms.assetid: 9D0A4F42-F027-4032-8297-045937BD2B6E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d6eff172a59a7f0ee00f85a0cd8f237387aaa78
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482672"
---
# <a name="windows-assessment-toolkit"></a>Windows Toolkit de avaliação

## <a name="platforms"></a>Plataformas

**clientes** -Windows 7 \| Windows 8  

## <a name="description"></a>Descrição

o Toolkit de avaliação do Windows e o desempenho do Windows Toolkit constituem o Kit de avaliação e implantação do Windows (ADK). juntos, eles fornecem uma solução completa para avaliar o desempenho geral do computador e automatizar a implantação do sistema operacional Windows em novos computadores.

Este tópico se concentra no **Toolkit de avaliação**. Os resultados da avaliação são usados para diagnosticar possíveis problemas, de modo que o hardware e o software que você desenvolve sejam responsivos e tenham um impacto mínimo sobre a vida útil da bateria, o desempenho de inicialização e o tempo de desligamento. As mesmas avaliações estão disponíveis para parceiros OEM, parceiros ISV/IHV, entusiastas e outros membros da Comunidade, para estabelecer uma estrutura comum para medir, comparar e examinar aspectos de qualidade.

usando as ferramentas de avaliação de Windows, você pode medir diferentes aspectos do desempenho em vários cenários, desde o tempo de inicialização até o desempenho da vida útil da bateria até o streaming de vídeo de alta definição. As avaliações podem identificar possíveis problemas, comportamento inconsistente e áreas de realce a serem investigadas.

nas versões anteriores do Windows, várias ferramentas estavam disponíveis para medir a qualidade, incluindo o Velocity Test Suite (VTS/VOS), o FQTS (Fundamental quality tools suite) e o SPPTS (Power and Performance tools suite). a avaliação Toolkit combina a funcionalidade dessas ferramentas de diagnóstico de desempenho em um conjunto integrado de ferramentas que é mais fácil de usar e fornece resultados mais amplos e significativos.

a avaliação de Windows Toolkit maximiza a satisfação do consumidor ao:

-   ajudando você a avaliar a experiência geral de Windows, software e drivers de valor agregado e configurações de hardware
-   Fornecendo dados detalhados do sistema que podem ajudá-lo a identificar as causas raiz de problemas de qualidade
-   Reduzindo os custos revelando problemas durante o desenvolvimento
-   Gerando comparações de resultados de computadores diferentes ou do mesmo conjunto de computadores ao longo do tempo criando grafos de comparação de vários conjuntos de resultados
-   Gerando comentários em um formato padronizado que você pode usar para melhorar a qualidade de seus produtos

Objetivos comerciais importantes podem ser obtidos usando as avaliações Toolkit:

-   **Measure & Compare** – você pode usar os dados para comparar componentes (software, drivers ou ambos) com relação a outros componentes semelhantes para facilitar a tomada de decisão, as recomendações e a marcação de bancada da concorrência
-   **Melhorar a qualidade** – você pode trabalhar de forma independente ou com parceiros envolvidos para criar um componente (software, driver ou ambos) de acordo com os critérios de qualidade predefinidos
-   **Controlar qualidade**   Você pode criar um processo para controlar com eficiência a qualidade das versões dos componentes e detectar regressões após cada iteração

## <a name="usage-and-best-practices"></a>Uso e práticas recomendadas

As avaliações são uma combinação de arquivos XML e binários que induzem um conjunto específico de Estados em um computador, medem e registram a atividade e preservam os resultados gravados. Um trabalho é uma coleção de uma ou mais avaliações e suas configurações, executadas ao mesmo tempo em um computador. A plataforma de avaliação fornece a infraestrutura para execução consistente e exibição de trabalhos, avaliações e resultados. Os resultados geralmente incluem informações de diagnóstico e correção que ajudam a determinar as áreas que precisam de investigação e ação corretivas adicionais. Você pode:

-   executar avaliações em um único computador ou em uma pequena coleção de computadores com o **Console de avaliação do Windows** (Windows AC) <dl> Esse cenário é para os usuários que desejam exibir características de desempenho em uma ou várias configurações de computador diferentes. Windows AC é uma GUI (interface gráfica do usuário) usada para agrupar as avaliações, criar um trabalho, empacotar um trabalho, executar o trabalho e gerenciar os resultados do trabalho. Os resultados geralmente incluem ações recomendadas.  
    </dl>
-   Run assessments against multiple computers in a lab environment with **Windows Assessment Services** (Windows AS) <dl> Esse cenário é basicamente para usuários que desejam executar um conjunto de avaliações qualitativas em uma linha completa de desktops, laptops ou tablets em um ambiente de desenvolvimento.  
    </dl>

o Toolkit de avaliação oferece estes recursos:

-   Uma GUI (interface gráfica do usuário) simples e avaliações que podem ser usadas para avaliar um computador sem conhecimento técnico profundo do sistema
-   Resultados da avaliação, exibidos no console ou na interface do usuário, que geralmente incluem recomendações para ajudá-lo a melhorar o sistema
-   A capacidade de executar um trabalho pré-configurado com um clique
-   Configurações de avaliação predefinidas em cada avaliação de trabalho pré-configurada para que você possa executar um trabalho em vários computadores e ter certeza de que os resultados são comparáveis
-   Trabalhos que podem ser personalizados para incluir as avaliações que você deseja usar e as configurações que deseja usar
-   Sintaxe da linha de comando da plataforma de avaliação para script e automação de trabalhos
-   A capacidade de executar um trabalho, exibir os resultados, tomar as medidas de correção para melhorar o sistema e executar o trabalho novamente e comparar os novos resultados lado a lado com os resultados antigos para ver como o sistema melhorou

o Toolkit de avaliação normalmente é usado nestes cenários:




| Cenário | Descrição | 
|----------|-------------|
| "Caixa preta" | Execute um trabalho predefinido e examine os resultados de quaisquer valores incomuns ou indicações de problemas com drivers, uso de memória ou outras áreas que as avaliações abordam. | 
| Comparando resultados | <ol><li>Execute uma única avaliação usando as configurações recomendadas em qualquer computador que esteja executando um sistema operacional com suporte.</li><li>Use o Windows AC para empacotar o trabalho para ser executado em outro computador.</li><li>Salve os resultados em um compartilhamento para que você possa comparar os resultados.</li><li>Compare os resultados de qualquer computador Windows com aqueles de qualquer outro sistema operacional com suporte para identificar diferenças.</li></ol><br /> | 
| Limpar computador | Execute avaliações em um computador limpo que inclua apenas o sistema operacional para estabelecer os resultados do sistema de linha de base. | 
| Computador com componentes de hardware ou software adicionados | Adicione um novo hardware ou software ao sistema de computador limpo e execute novamente as avaliações para comparar os resultados com os resultados de computadores limpos. | 
| Criando avaliações | Use APIs públicas para desenvolver ou estender uma avaliação, ou integre avaliações com suas ferramentas e infraestrutura. | 




 

Essas avaliações podem ser usadas:



| Avaliação                                   | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Pré-validação de certificação de driver          | a avaliação de **pré-validação de certificação de Driver** verifica se os drivers em um sistema operacional Windows em execução se qualificam para o programa de certificação Windows. Os resultados incluem recomendações que ajudam a resolver problemas encontrados pela avaliação, como drivers não assinados ou assinaturas expiradas.                                                                                                                                                                                                                                                            |
| Verificação de driver                          | a avaliação de **verificação de Driver** verifica se uma imagem Windows offline ou um sistema operacional Windows em execução contém o conjunto correto de drivers. Os resultados incluem recomendações para ajudá-lo a resolver quaisquer problemas encontrados pela avaliação. Esses problemas podem incluir drivers ausentes, duplicados, mais antigos ou desnecessários.                                                                                                                                                                                                                                         |
| Manipulação de arquivos                                | A avaliação de **manipulação de arquivos** fornece uma maneira automatizada de exercitar operações de arquivo comuns e capturar métricas. As métricas medem as durações e a taxa de transferência para ajudá-lo a entender o desempenho de um computador nos cenários de manipulação de arquivos do usuário final. A avaliação de manipulação de arquivo usa um conjunto de cargas de trabalho para simular um usuário que está copiando, movendo, compactando, descompactando e excluindo arquivos e pastas em sistemas cliente.                                                                                                                                       |
| Manuseio de fotos                               | A avaliação de **manipulação de fotos** mede o desempenho do computador e a vida útil da bateria, simulando um usuário final que está exibindo e manipulando fotos.                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Criação de inicialização/guia do Internet Explorer          | A avaliação de **desempenho de inicialização do Internet Explorer** ajuda a identificar os componentes que podem afetar o tempo necessário para iniciar o Internet Explorer. A avaliação mede o tempo para processar totalmente uma página em branco, incluindo o tempo de carregamento do processo de IExplore.exe e os intervalos de criação de quadros e de criação de tabulação. Ele também mede o efeito de todas as extensões, suplementos e barras de ferramentas instaladas no sistema. Ele não mede nenhum desempenho de rede ou de navegação.                                                                                         |
| Ativar/desativar                                       | a avaliação de **transição On/Off** mede o desempenho dos cenários de desempenho Windows 8 inicialização, espera e hibernação.                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Desempenho de navegação do Internet Explorer       | A avaliação de **desempenho de navegação do Internet Explorer** mede a qualidade da experiência de navegação no Internet Explorer e avalia os recursos de hardware e gráfico de CPU. Três cargas de trabalho de navegação separadas são fornecidas para enfatizar o computador de várias maneiras.                                                                                                                                                                                                                                                                                                  |
| Desempenho de transcodificação de mídia                | A avaliação de **vídeo transcodificar** mede o processo de alteração de um arquivo de vídeo para um formato ou taxa de bits diferente. Essa avaliação executa uma série de operações de transcodificação com formatos e resoluções de arquivos de entrada e saída comuns                                                                                                                                                                                                                                                                                                                                           |
| Windows Desempenho da interface do usuário                       | a avaliação de **desempenho da interface do usuário Windows** avalia o desempenho de algumas experiências básicas na interface do usuário Windows. a avaliação mede a capacidade de resposta e a qualidade da renderização, enquanto a avaliação exercita as cargas de trabalho que simulam atividades do usuário, como usar a pesquisa e a transição do ambiente de aplicativo da loja Windows para a área de trabalho. Os resultados da capacidade de resposta são medidos em milissegundos. Números baixos significam que o computador é mais rápido e responsivo. Para renderização, os resultados mostram a taxa de quadros e o número de falhas que ocorrem. |
| Espaço de memória                             | Você pode usar a avaliação de **superfície de memória** para comparar quantitativamente uma imagem do sistema operacional de linha de base com outra imagem do sistema operacional. Em seguida, você pode identificar os componentes específicos que afetam a superfície de memória do sistema físico. Esses componentes podem incluir drivers, aplicativos de suplemento, pacotes de software pré-carregados e programas antivírus.                                                                                                                                                                                                           |
| Primeiro desempenho de inicialização                       | A **primeira avaliação de desempenho** de inicialização identifica problemas que afetam quanto tempo Windows demora para inicializar e exibir o tela inicial na primeira vez que o computador é iniciado. Os resultados ajudam os OEMs a diagnosticar o que causa atrasos e fornecem recomendações para melhorar a experiência.                                                                                                                                                                                                                                                                                      |
| Streaming de Mídia                              | A **avaliação de Desempenho de Mídia** de Streaming ajuda você a avaliar o desempenho de uma configuração de computador ao transmitir mídia usando Internet Explorer. Você pode usar os resultados da avaliação para entender, comparar e melhorar a experiência de mídia de streaming.                                                                                                                                                                                                                                                                                                                 |
| WinSAT Abrangente                         | O Windows Avaliação do Sistema **(WinSAT)** é usado para avaliar e melhorar o desempenho de um computador em vários componentes do sistema, incluindo CPU, memória, disco e gráficos. Os resultados de avaliação abrangentes do WinSAT expressam a capacidade da configuração de hardware de um computador em números. Pontuações mais altas geralmente significam que o computador avaliado tem um desempenho melhor e mais rápido do que um computador com uma pontuação inferior.                                                                                                                                                        |
| Eficiência de energia                            | O **trabalho eficiência de** energia fornece uma maneira automatizada para avaliar a vida útil da bateria de um computador. Usando cargas de trabalho, o trabalho de Eficiência de Energia também executa diagnósticos que avaliam se os componentes do sistema estão usando energia quando devem estar ociosos.                                                                                                                                                                                                                                                                                                               |
| MiniFilter Diagnostic Configurações               | A **opção Diagnóstico de MiniFiltro** é Internet Explorer avaliação de desempenho de inicialização, a avaliação de Manipulação de Arquivos e a avaliação de desempenho de inicialização (Windows 8). Selecionar essa opção nas avaliações que oferecem a opção de diagnóstico MiniFilter produz métricas que ajudam você a avaliar o impacto das operações de MiniFilter em vários cenários de avaliação.                                                                                                                                                                                  |
| Windows Media Player Desempenho e qualidade | A **Windows Media Player desempenho** e qualidade inicializa o WMP e reproduz vários clipes de mídia um após o outro para capturar métricas de desempenho e qualidade relacionadas à reprodução de mídia.                                                                                                                                                                                                                                                                                                                                                                          |



 

Outras ferramentas, como o Windows desempenho Toolkit, estão incluídas no ADK. Essas ferramentas fornecem informações detalhadas que permitem analisar e rastrear o desempenho do sistema e do aplicativo. Consulte a seção Recursos abaixo para obter mais informações.

## <a name="resources"></a>Recursos

**Vídeo:**

-   [Vídeos do ADK do Channel9 BUILD](https://channel9.msdn.com/Events/BUILD/BUILD2011?sort=status&direction=asc&term=&t=assessment+and+deployment+kit)

  
**Documentação:**

-   [Windows Kit de Avaliação e Implantação](/previous-versions/windows/hh825420(v=win.10))
-   [Windows Referência técnica Toolkit avaliação](/previous-versions/windows/it-pro/windows-8.1-and-8/hh825508(v=win.10))
-   [Mecanismo de execução de avaliação](/previous-versions/windows/desktop/axe/axe-access-portal)
-   [Windows Análise de desempenho](https://msdn.microsoft.com/performance/default.aspx)

  


 

