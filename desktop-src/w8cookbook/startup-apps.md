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
ms.openlocfilehash: 75a12f01dac073712512206a5c432561b4a0b75e
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "103642932"
---
# <a name="startup-apps"></a>Aplicativos de inicialização

## <a name="platform"></a>Plataforma

**Clientes**   do   Windows 8  


## <a name="description"></a>Descrição

Uma das grandes opções com o Windows é a capacidade de iluminar vários fatores forma, desde desktops e laptops tradicionais até tablets de baixa potência. Para garantir que nossos clientes mútuos tenham uma ótima experiência em qualquer fator forma que escolherem com o Windows, duas métricas de sucesso-chave que precisam ser atendidas aumentam a vida útil da bateria e a excelente capacidade de resposta do PC. Para conseguir isso, foram feitas melhorias em várias áreas do Windows, incluindo ciclo de vida do processo, Estados de suspensão e aplicativos de inicialização (aplicativos com inicialização automatizada após a inicialização do computador). Este tópico destaca alguns dos impactos que os aplicativos de inicialização têm em um dispositivo Windows e fornece orientação aos desenvolvedores (ISV/IHV) e aos OEMs para reconsiderar os padrões de uso dos aplicativos de inicialização a fim de melhorar a vida útil da bateria e a capacidade de resposta para nossos clientes mútuos. Ele também descreve as alterações no Windows que colocam os usuários no controle de determinar qual dos aplicativos de inicialização realmente são executados.

Os aplicativos da Windows Store são projetados para aderir a novos padrões de consumo e capacidade de resposta da bateria, e o Windows gerencia seu ciclo de vida, suspendendo e/ou encerrando-os. No entanto, os aplicativos da área de trabalho projetados para versões anteriores do Windows não foram necessariamente projetados para preservar a vida útil da bateria ou serem sensíveis à atividade do usuário e podem afetar a capacidade de resposta do sistema (por exemplo, quando um aplicativo envia uma pulsação de 1 segundo regular para verificar se há atualizações ou pré-instalar antecipadamente a memória, caso precise dela mais tarde). Isso pode criar uma experiência ruim para o usuário que compra um Tablet PC com uma expectativa de vida útil de bateria e semanas de espera, mas descobre que a vida útil da bateria do Tablet s não atinge essas metas. Além disso, como os aplicativos de inicialização são executados em segundo plano, o número de aplicativos em execução no sistema pode ser significativamente mais do que o usuário está ciente e afetar a capacidade de resposta do sistema. Os aplicativos de inicialização são classificados para incluir aqueles que aproveitam esses mecanismos para iniciar:

-   Executar chaves do registro (HKLM, HKCU, nós do WOW64 incluídos)
-   Chaves do registro RunOnce
-   Pastas de inicialização no menu Iniciar para locais por usuário e público

Novas funcionalidades foram adicionadas ao Windows para garantir que os usuários finais estejam sempre no controle dos aplicativos executados em seus sistemas. A guia inicialização no Gerenciador de tarefas mostra uma lista de aplicativos de inicialização, juntamente com controles que permitem aos usuários desabilitar os aplicativos de inicialização. Para ajudar os usuários a determinar o que desabilitar, o Gerenciador de tarefas exibe uma medida de cada impacto de s do aplicativo de inicialização. O impacto é avaliado com base na CPU e no uso do disco s do aplicativo na inicialização. Os valores de impacto são determinados pela aplicação destes critérios:

-   **Alto impacto**   Aplicativos que usam mais de um segundo de tempo de CPU ou mais de 3 MB de e/s de disco na inicialização
-   **Impacto médio**   Aplicativos que usam 300 MS-1000 MS de tempo de CPU ou 300 KB-3 MB de e/s de disco
-   **Baixo impacto**   Aplicativos que usam menos de 300 MS de tempo de CPU e menos de 300 KB de e/s de disco

A Microsoft fornece ferramentas para ajudar os desenvolvedores de aplicativos a avaliar, analisar e tomar medidas para reduzir o impacto na inicialização e melhorar a experiência do usuário. O kit de avaliação e implantação fornece a capacidade de executar uma avaliação de desempenho de inicialização e medir o impacto dos aplicativos executados na inicialização. Os resultados da avaliação contêm informações detalhadas de análise e correção, quando aplicável, para os componentes de impacto superior na inicialização do Windows. Usando o analisador de desempenho do Windows, os desenvolvedores de aplicativos podem executar uma análise profunda para encontrar a causa raiz do impacto no desempenho e melhorar o desempenho de inicialização do Windows. Instale o Windows ADK [aqui](/previous-versions/windows/hh825494(v=win.10)).

## <a name="guidance"></a>Diretrizes

Os aplicativos de inicialização abrangem várias categorias, conforme descrito na tabela a seguir. Um conjunto de recomendações para desenvolvedores é mapeado para as categorias de aplicativos de inicialização para se alinhar com as alterações funcionais do Windows descritas acima.



Categorias de aplicativos de inicialização

Descrição

Recomendação

**Atualizadores**

Monitorar e atualizar usuários para atualizações online

**Tarefa de manutenção**

> [!Note]  
> Todas as atualizações devem ser tarefas de manutenção, sem nenhum requisito de interação da interface do usuário. Os aplicativos devem apenas se atualizar silenciosamente e reverter em caso de falha

<br/>

$ {ROWSPAN2} $**assistência de hardware**$ {remover} $  

Pontos de acesso alternativos

Fornecer acesso a recursos e aplicativos do Windows que são acessíveis por meio de outros pontos de acesso no Windows

**Remover**

> [!Note]  
> A chave é reduzir os recursos duplicados existentes no Windows

<br/>

Notificadores

Fornecer aos usuários notificações sobre seus dispositivos

**Remover**

> [!Note]  
> O Windows fornece notificações aos usuários sobre seus dispositivos

<br/>

**Pré-iniciadores**

Algumas das atividades preliminares necessárias para os aplicativos são descarregadas em um aplicativo de inicialização durante o logon do usuário

**Remover**

> [!Note]  
> O Windows 8 é otimizado para uma experiência rápida para lançamentos de aplicativos.

<br/>

$ {ROWSPAN4} $**Utility**$ {remover} $  

Sincronização de PC

Fornecer funcionalidade de sincronização em vários sistemas

**Inicialização** (atualizações em potencial na versão beta)

Recuperação de & de backup

Ponto de entrada para salvar e restaurar o estado de arquivos, configurações ou sistemas inteiros

**Aplicativo da Windows Store para interface com os usuários**

Telemetria

Coletar e enviar informações sobre a experiência do usuário e o ambiente

**Tarefa de manutenção**

Monitoramento de PC

Fornecer monitoramento e notificações de estado do sistema não solicitados que duplicam a funcionalidade de caixa de entrada existente

**Remover**

> [!Note]  
> A chave é reduzir os recursos duplicados existentes no Windows

<br/>

$ {ROWSPAN2} $**Security**$ {remove} $  

Filtros de & de controle dos pais

Impor regras e restrições estabelecidas para acesso e uso da Internet

**Inicialização**

Configuração e gerenciamento

Permitir que os usuários controlem as opções de diagnóstico e correção para o monitoramento de segurança do sistema notificar usuários de conclusões e ações de segurança

**Aplicativo da Windows Store para interface com os usuários**

**Comunicação & Internet** (im & VoIP)

Enviar e receber mensagens e chamadas

**Aplicativo da Windows Store**

**Música & MP3**

Reproduzir, armazenar e gerenciar música

**Aplicativo da Windows Store**

**Vídeo de & de fotos**

Detecte, registre, processe, armazene e gerencie fotos e vídeos

**Aplicativo da Windows Store**

**Jogos para PCs**

Iniciar jogos em vários domínios

**Aplicativo da Windows Store**

**Venda & anúncio**

Chame atenção para produtos e serviços disponíveis para compra

**Remover**



 

> [!Note]  
> As diretrizes de aplicativos de acessibilidade são cobertas por engajamentos diretos separados com ISVs. Consulte [*programação para facilidade de acesso*](../winauto/ease-of-access---assistive-technology-registration.md) para obter detalhes.

 

**Aplicativos da Windows Store**

Os aplicativos da Windows Store aprimoram a experiência do usuário introduzindo um espaço do Windows com novas coordenadas: um novo modelo de aplicativo, uma nova interface do usuário e uma Windows Store. Essas opções de estrutura de idioma e apresentação estão disponíveis para o desenvolvimento de aplicativos da Windows Store:

-   HTML/JavaScript/CSS
-   XAML/C #
-   XAML/C++

As informações agregadas para o desenvolvimento de aplicativos da Windows Store estão disponíveis no [centro de desenvolvimento do Windows](https://msdn.microsoft.com/windows/apps/).

Exemplos:

-   [Desenvolvendo jogos da Windows Store](/previous-versions/windows/apps/hh452744(v=win.10))
-   [Desenvolvendo aplicativos da Windows Store que usam mídia](/previous-versions/windows/apps/hh465132(v=win.10))

**Tarefas de manutenção automática**

A atividade de plano de fundo periódica deve ser projetada como tarefas de manutenção automáticas. Eles estão agendados no tempo ocioso do sistema para aumentar a capacidade de resposta e a eficiência energética dos computadores Windows. As tarefas de manutenção podem ser criadas e configuradas por um aplicativo de área de trabalho no momento da instalação, usando o SDK da área de trabalho. Consulte o tópico manutenção automática a seguir para obter detalhes.

## <a name="resources"></a>Recursos

-   [Diretrizes de acessibilidade](../winauto/ease-of-access---assistive-technology-registration.md)
-   [Central de Desenvolvimento do Windows](https://msdn.microsoft.com/windows/apps/)
-   [Windows ADK](/previous-versions/windows/hh825494(v=win.10))

 

