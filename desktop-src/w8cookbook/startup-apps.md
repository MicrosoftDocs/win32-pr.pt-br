---
title: Aplicativos de inicialização
description: Aplicativos de inicialização
ms.assetid: 3519CB52-A6EC-4819-87FE-C144801BDD9F
keywords:
- aplicativo de inicialização
- tarefa em segundo plano
- Executar chave
- RunOnce
- pasta de inicialização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbc2dc2a73a08c3aebd265c209b407646e50a6cb1b7cba630884cf719330b8dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815046"
---
# <a name="startup-apps"></a>Aplicativos de inicialização

## <a name="platform"></a>Plataforma

**Clientes** Windows 8     


## <a name="description"></a>Descrição

Uma das grandes opções com Windows é a capacidade de acionar vários fatores formais, desde desktops e laptops tradicionais até tablets de baixa potência. Para garantir que nossos clientes mútuos tenham uma ótima experiência em qualquer fator forma que escolherem com o Windows, duas principais métricas de sucesso que precisam ser resolvidas são o aumento da vida útil da bateria e a excelente capacidade de resposta do computador. Para conseguir isso, foram feitas melhorias em várias áreas do Windows incluindo ciclo de vida do processo, estados de espera e aplicativos de inicialização (aplicativos com inicialização automatizada após a inicialização do computador). Este tópico destaca alguns dos impactos que os aplicativos de inicialização têm em um dispositivo Windows e fornece diretrizes aos desenvolvedores (ISV/IHV) e OEMs para repensar os padrões de uso dos aplicativos de inicialização a fim de melhorar a vida útil e a capacidade de resposta da bateria para nossos clientes mútuos. Ele também descreve as alterações no Windows que colocam os usuários no controle de determinar quais dos aplicativos de inicialização realmente podem ser executados.

Windows Os aplicativos da Store foram projetados para seguir os novos padrões de consumo e capacidade de resposta da bateria, e Windows gerencia seu ciclo de vida, suspendindo e/ou encerrando-os. No entanto, os aplicativos da área de trabalho projetados para versões anteriores do Windows não foram necessariamente projetados para preservar a vida útil da bateria ou ser sensíveis à atividade do usuário e podem afetar a capacidade de resposta do sistema (por exemplo, quando um aplicativo envia uma pulsação regular de 1 segundo para verificar se há atualizações ou pré-aloca a memória antecipadamente, caso precise dela mais tarde). Isso pode criar uma experiência ruim para o usuário que compra um computador tablet Windows com uma longa expectativa de vida da bateria e semanas de espera, mas descobre que a vida útil da bateria do tablet não atinge essas metas. Além disso, como os aplicativos de inicialização são executados em segundo plano, o número de aplicativos em execução no sistema pode ser significativamente maior do que o que o usuário está ciente e afetar a capacidade de resposta do sistema. Os aplicativos de inicialização são classificados para incluir aqueles que estão utilizando esses mecanismos para iniciar:

-   Executar chaves do Registro (HKLM, HKCU, nós wow64 incluídos)
-   Chaves do Registro RunOnce
-   Pastas de inicialização no menu Iniciar para locais públicos e por usuário

Uma nova funcionalidade foi adicionada ao Windows para garantir que os usuários finais sempre estão no controle dos aplicativos que são executados em seus sistemas. A guia Inicialização no Gerenciador de Tarefas mostra uma lista de aplicativos de inicialização, juntamente com controles que permitem aos usuários desabilitar aplicativos de inicialização. Para ajudar os usuários a determinar o que desabilitar, Gerenciador de Tarefas exibe uma medida do impacto de cada aplicativo de inicialização. O impacto é avaliado com base no uso da CPU e do disco de um aplicativo na inicialização. Os valores de impacto são determinados aplicando estes critérios:

-   **Alto impacto**   Aplicativos que usam mais de 1 segundo do tempo de CPU ou mais de 3 MB de E/S de disco na inicialização
-   **Impacto médio**   Aplicativos que usam 300 ms a 1000 ms de tempo de CPU ou 300 KB – 3 MB de E/S de disco
-   **Baixo impacto**   Aplicativos que usam menos de 300 ms de tempo de CPU e menos de 300 KB de E/S de disco

A Microsoft fornece ferramentas para ajudar os desenvolvedores de aplicativos a avaliar, analisar e tomar medidas para reduzir o impacto na inicialização e melhorar a experiência do usuário. O Kit de Avaliação e Implantação fornece a capacidade de executar uma avaliação de desempenho de inicialização e medir o impacto dos aplicativos executados na inicialização. Os resultados da avaliação contêm informações detalhadas de análise e correção, quando aplicável, para os componentes que mais impactam na Windows inicialização. Usando o Windows Performance Analyzer, os desenvolvedores de aplicativos podem executar uma análise profunda para encontrar a causa raiz do impacto no desempenho e melhorar Windows de inicialização. Instale o Windows ADK [aqui.](/previous-versions/windows/hh825494(v=win.10))

## <a name="guidance"></a>Orientação

Os aplicativos de inicialização abrangem várias categorias, conforme descrito na tabela abaixo. Um conjunto de recomendações para desenvolvedores é mapeado para as categorias de aplicativos de inicialização para alinhar com as Windows funcionais descritas acima.



Categorias de aplicativos de inicialização

Descrição

Recomendação

**Atualizadores**

Monitorar e atualizar usuários para atualizações online

**Tarefa de manutenção**

> [!Note]  
> Todas as atualizações devem ser tarefas de manutenção, sem nenhum requisito de interação da interface do usuário. Os aplicativos devem apenas se atualizar e reverter em caso de falha

<br/>

${ROWSPAN2}$**Assistência de Hardware**${REMOVE}$  

Pontos de acesso alternativos

Forneça acesso a Windows recursos e aplicativos acessíveis por meio de outros pontos de acesso no Windows

**Removerr**

> [!Note]  
> A chave é reduzir os recursos duplicados que existem no Windows

<br/>

Notificadores

Fornecer aos usuários notificações sobre seus dispositivos

**Removerr**

> [!Note]  
> Windows fornece notificações aos usuários sobre seus dispositivos

<br/>

**Pré-lançamentos**

Algumas das atividades preliminares necessárias para aplicativos são descarregadas para um aplicativo de inicialização durante o logon do usuário

**Removerr**

> [!Note]  
> Windows 8 é otimizado para uma experiência rápida para lançamentos de aplicativos.

<br/>

${ROWSPAN4}$**Utility**${REMOVE}$  

Sincronização de PC

Fornecer funcionalidade de sincronização em vários sistemas

**Inicialização** (atualizações potenciais no Beta)

Backup e recuperação

Ponto de entrada para salvar e restaurar o estado de arquivos, configurações ou sistemas inteiros

**Windows Aplicativo da Loja para intercalação com os usuários**

Telemetria

Coletar e enviar informações sobre a experiência do usuário e o ambiente

**Tarefa de manutenção**

Monitoramento de PC

Fornecer notificações e monitoramento de estado do sistema não solicitado que duplicam a funcionalidade de caixa de entrada existente

**Removerr**

> [!Note]  
> A chave é reduzir os recursos duplicados que existem no Windows

<br/>

${ROWSPAN2}$**Security**${REMOVE}$  

Filtros de & dos pais

Impor regras e restrições estabelecidas para acesso e uso da Internet

**Inicialização**

Configuração e gerenciamento

Permitir que os usuários controlem as opções de diagnóstico e correção para o monitoramento de segurança do sistema Notificar os usuários sobre descobertas e ações de segurança

**Windows Aplicativo da Loja para intercalação com os usuários**

**Internet & comunicação** (IM & VoIP)

Enviar e receber mensagens e chamadas

**Windows Aplicativo da Store**

**Música & MP3**

Reproduzir, armazenar e gerenciar música

**Windows Aplicativo da Store**

**Vídeo de & de fotos**

Detectar, registrar, renderizar, armazenar e gerenciar fotos e vídeos

**Windows Aplicativo da Store**

**Jogos para PC**

Iniciar jogos em vários domínios

**Windows Aplicativo da Store**

**Anúncio de & upsell**

Chamar a atenção para bens e serviços disponíveis para compra

**Removerr**



 

> [!Note]  
> As diretrizes de aplicativos de acessibilidade são abordadas por envolvimentos diretos separados com ISVs. Consulte [*Programação para Facilidade de Acesso*](../winauto/ease-of-access---assistive-technology-registration.md) para obter detalhes.

 

**Windows Aplicativos da Store**

Windows os aplicativos da loja aprimoram a experiência do usuário introduzindo um espaço de Windows com novas coordenadas: um novo modelo de aplicativo, uma nova interface do usuário e uma Windows Store. essas opções de estrutura de idioma e apresentação estão disponíveis para o desenvolvimento de aplicativos da loja Windows:

-   HTML/JavaScript/CSS
-   XAML/C #
-   XAML/C++

as informações agregadas para o desenvolvimento de aplicativos da loja Windows estão disponíveis no [Centro de Desenvolvimento Windows](https://msdn.microsoft.com/windows/apps/).

Exemplos:

-   [desenvolvendo Windows jogos de loja](/previous-versions/windows/apps/hh452744(v=win.10))
-   [desenvolvendo Windows aplicativo de loja que usa mídia](/previous-versions/windows/apps/hh465132(v=win.10))

**Tarefas de manutenção automática**

A atividade de plano de fundo periódica deve ser projetada como tarefas de manutenção automáticas. eles estão agendados no tempo ocioso do sistema para aumentar a capacidade de resposta e a eficiência de energia de computadores Windows. As tarefas de manutenção podem ser criadas e configuradas por um aplicativo de área de trabalho no momento da instalação, usando o SDK da área de trabalho. Consulte o tópico manutenção automática a seguir para obter detalhes.

## <a name="resources"></a>Recursos

-   [Diretrizes de acessibilidade](../winauto/ease-of-access---assistive-technology-registration.md)
-   [Central de Desenvolvimento do Windows](https://msdn.microsoft.com/windows/apps/)
-   [Windows ADK](/previous-versions/windows/hh825494(v=win.10))

 

