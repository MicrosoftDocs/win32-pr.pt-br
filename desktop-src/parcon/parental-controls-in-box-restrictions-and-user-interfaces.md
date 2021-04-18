---
description: Várias implementações de restrições são fornecidas.
ms.assetid: a00d9a3a-d052-492c-b9e7-3ecb1455a392
title: Controles dos pais In-Box restrições & interfaces do usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e5f155f8323fd6b006e510d75865ea25e278c70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105800115"
---
# <a name="parental-controls-in-box-restrictions--user-interfaces"></a>Controles dos pais In-Box restrições & interfaces do usuário

Várias implementações de restrições são fornecidas.

-   [Restrições da Web](#web-restrictions)
-   [Limites de tempo](#time-limits)
-   [Jogos](#games)
-   [Permitir e bloquear programas específicos](#allow-and-block-specific-programs)

## <a name="web-restrictions"></a>Restrições da Web

-   Filtro de conteúdo da Web na caixa usando um serviço de classificação dinâmica livre. Individualmente configurável por usuário controlado.
-   Filtra todo o tráfego HTTP quando habilitado, retorna uma página formatada personalizada se estiver bloqueada. Permite uma funcionalidade aceitável com todos os principais navegadores. Ao monitorar todas as solicitações HTTP Get e post de uma página, permite que partes individuais da página da Web sejam bloqueadas.
-   Altamente configurável usando a interface do usuário que permite ou bloqueia listas de URLs, predefinições de categorias de classificação simplificadas ou controle ActiveX de mais de 12 categorias, bem como uma política para bloquear downloads de arquivos.

> [!Note]  
> O bloqueio de download de arquivo real exige que os aplicativos implementem a restrição, conformidade com a configuração fornecida.

 

-   Implementado como um driver de WFP (plataforma de filtragem do Windows) se comunicando com o processo de monitoramento de segurança da família em execução nas sessões dos usuários. A implementação foi alterada de um filtro LSP (provedor de serviços em camadas) para um driver WFP (plataforma de filtragem do Windows) que se comunica com o processo de monitoramento de segurança da família em execução nas sessões dos usuários.

    **Windows 7 e Windows Vista:** Implementado como um filtro LSP (provedor de serviços em camadas) se comunicando com um serviço de direitos limitados para gerenciamento e monitoramento geral. O filtro permanece na cadeia de LSP quando desabilitado, mas passa todo o tráfego pelo. Essa implementação tem suporte apenas para os sistemas operacionais listados.

-   Os aplicativos podem fornecer a interface do usuário para mostrar o bloqueio parcial de página e honrar a política para bloquear downloads de arquivos. Eles também podem invocar uma API para permitir que o usuário solicite permissão para exibir uma página bloqueada. Essa substituição administrativa invoca um pequeno aplicativo que mostra as URLs tentadas e que solicita credenciais para permiti-las.
-   Uma API é fornecida para casos especiais em que um aplicativo precisa se registrar para ignorar a filtragem, ou URLs específicas devem ser sempre permitidas.
-   Como apenas um filtro de conteúdo da Web deve estar em execução por vez, terceiros podem se registrar como o filtro ativo e desabilitar o filtro na caixa. Essa extensibilidade, juntamente com a capacidade de mostrar um filtro de terceiros na interface do usuário, permite a substituição simples. Os filtros devem remover seu registro quando desinstalados.

## <a name="time-limits"></a>Limites de tempo

-   As restrições de tempo na caixa foram aprimoradas fornecendo a capacidade de controlar a quantidade total de tempo por dia que o computador pode ser usado (concessão de tempo), além da capacidade de controlar os tempos em que o computador pode ser usado (curfew), que estava disponível nas versões anteriores do Windows.
-   A interface do usuário para curfew permite o controle independente para cada dia da semana com granularidade de meia hora
-   A interface do usuário para a bonificação de tempo permite controles para dias da semana e fins de semana ou controle independente para cada dia das semanas com granularidade de 15 minutos
-   O mecanismo do FUS (Fast User switch) não é mais usado para forçar o bloqueio ou bloquear o logon do usuário controlado no período de tempo bloqueado. Um comutador para uma área de trabalho separada é usado para essas finalidades. Observe que o FUS preserva o estado do usuário quando bloqueado.

## <a name="games"></a>Jogos

-   Funciona em conjunto com o explorador de jogos.
-   Permite que os administradores controlem quais jogos podem ser reproduzidos por meio de uma interface do usuário sofisticada para selecionar um sistema e um nível de classificação de jogos (além de descritores, se estiverem presentes) e/ou especificamente permitir ou bloquear títulos.
-   Os metadados em classificações de jogos são obtidos de uma das duas maneiras:
    -   Os títulos com suporte implantam seus próprios arquivos de definição de jogo (GDFs).
    -   Aproximadamente 2000 títulos herdados são cobertos por um banco de dados na caixa.
-   Três mecanismos são usados para a imposição:
    -   Negue ACLs para acesso controlado de gravação do usuário à pasta do jogo.
    -   Término do processo para títulos herdados usando a tecnologia Shim da compatibilidade de aplicativos.
    -   Uso de API de verificação automática por títulos com suporte para bloquear a execução.
-   É recomendável conscientizar os eventos de limites de tempo explicados na seção acima.
-   A documentação do GDFs e do explorador de jogos será fornecida principalmente por meio de versões do SDK do DirectX.

## <a name="allow-and-block-specific-programs"></a>Permitir e bloquear programas específicos

-   Também conhecido como GAR (restrições gerais de aplicativo).
-   Desativada, por padrão. Se ativado, ele só permitirá que um usuário controlado execute aplicativos aprovados por um administrador, com exceções razoáveis.
-   A interface do usuário fornece uma lista de nomes de programa com caminhos correspondentes, cada um com uma caixa de seleção Permitir. Também é fornecido um botão procurar.
-   Implementado usando políticas de restrição de software (SRP), também conhecido como mais seguro:
    -   Impede a execução de todas as mídias (chaves USB, disquetes e assim por diante).
    -   Usa regras de caminho para especificar os programas que podem ser executados.
    -   As permissões de gravação de ACL NTFS são revogadas de qualquer coisa permitida para a execução do usuário controlado.
    -   Se bloqueado e subsequentemente substituído para permitir, o aplicativo deve ser reiniciado manualmente.
-   As exceções incluem:
    -   Todos os binários necessários para um subconjunto básico do Windows funcionar.
    -   Todos os arquivos executáveis que se registram usando uma API devem ser permitidos para um determinado usuário.
    -   Jogos especificados como sendo permitidos em restrições de jogos.
-   Observe que o comando RunAs é bloqueado pelo design de um usuário quando GAR está ativado.

 

 



