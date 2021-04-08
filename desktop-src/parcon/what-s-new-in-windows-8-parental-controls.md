---
description: Fornece uma visão geral das alterações para os controles dos pais do Windows introduzidos no Windows 8.
ms.assetid: 7EB33215-8F8B-4EA4-87E6-A98F0D014548
title: Novidades na segurança da família do Windows 8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2123ec7f0d9c3af66528c6c203a3e8ea64bd0384
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828216"
---
# <a name="whats-new-in-windows-8-family-safety"></a>O que há de novo na segurança da família Windows 8

## <a name="overview-of-parental-controls-changes-for-windows-8"></a>Visão geral das alterações de controles dos pais para o Windows 8

A finalidade deste documento é dar uma visão geral das alterações nos controles dos pais do Windows no Windows 8 e permitir que provedores de soluções de controle de pais de terceiros aproveitem essas alterações. Este documento pressupõe a familiaridade dos leitores com os controles dos pais para o Windows 7 e o Windows Vista e refletirá apenas as alterações feitas nessa funcionalidade no Windows 8 que são relevantes para o desenvolvimento de soluções de controle de pais de terceiros.

## <a name="key-design-decisions-for-windows-8-parental-controlfamily-safety-changes"></a>Principais decisões de design para alterações de segurança de família e controle de pais do Windows 8

Alterações nos controles dos pais introduzidos no Windows 8 continuam a meta abrangente de introduzir aprimoramentos de recursos e, ao mesmo tempo, promover a coexistência de soluções de controle de pais de terceiros com a funcionalidade na caixa. As alterações são:

-   Uso da segurança da família da Microsoft para fornecer gerenciamento remoto e monitoramento de atividades remotas.
-   Integração da filtragem da Web como parte das restrições da Microsoft integradas e da capacidade de exibir relatórios de atividade em um computador com Windows 8.
-   O recurso controles dos pais no painel de controle foi renomeado para proteção da família e será referido como tal em todo este documento.
-   As restrições de tempo na caixa foram aprimoradas fornecendo a capacidade de controlar a quantidade total de tempo por dia que o computador pode ser usado (concessão de tempo), além da capacidade de controlar os tempos em que o computador pode ser usado (curfew.) O curfew estava disponível em versões anteriores do Windows.
-   A funcionalidade de segurança da família do Windows 8 pode ser ativada durante o fluxo de criação de conta padrão.
-   Os recursos de extensibilidade de controles dos pais do Windows Vista e do Windows 7 têm o suporte da segurança da família do Windows 8, incluindo a capacidade de soluções de terceiros para substituir o filtro de conteúdo da Web ou para substituir a interface do usuário de configuração na caixa e ainda depender da implementação de tempo, do aplicativo, das restrições de jogos e do filtro de conteúdo da Web.
-   A ativação de provedor de terceiros desativa o gerenciamento remoto e relatórios de controles de segurança de família do Windows 8 por meio do site de segurança da família.
-   A extensibilidade de terceiros para a proteção de família tem suporte apenas para aplicativos de área de trabalho do Windows 8.

## <a name="family-safety-and-standard-account-creation-in-windows-8"></a>Segurança de família e criação de conta padrão no Windows 8

Como parte da criação de conta padrão no Windows 8, um administrador tem a capacidade de ativar o monitoramento da conta por segurança de família. Veja a seguir uma lista da funcionalidade e da capacidade do provedor de terceiros para controlá-la:

-   Na última tela do fluxo de criação de conta standard do Windows 8, um administrador recebe uma caixa de seleção para ativar a segurança da família para a conta recém-criada.
-   Se essa caixa de seleção estiver marcada, a proteção da família será ativada para a conta com as seguintes configurações:
    -   Relatório de atividades em
    -   Todas as restrições estão desativadas
-   Se o administrador usou um conta Microsoft para fazer logon no Windows, o computador com Windows 8 será configurado para gerenciamento remoto de configurações de segurança da família e relatórios de atividade de email. O site de segurança da família pode ser usado para gerenciar um computador remotamente.
-   Se o provedor de terceiros quiser que a caixa de seleção esteja presente em um fluxo de criação de conta padrão, o valor a seguir deverá estar presente entre os valores de registro do provedor. Para obter mais informações sobre detalhes de registro do provedor, consulte a seção de [registro do provedor](what-s-new-in-windows-7-parental-controls.md) no tópico novidades no controle dos pais do Windows 7.

    

    | Termo                                                                                                                         | Descrição                                                                                                                                                                                                                                                                                  |
    |------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span id="AddUserVisible"></span><span id="adduservisible"></span><span id="ADDUSERVISIBLE"></span>AddUserVisible<br/> | Um valor opcional de **DWORD** diferente que especifica que a opção de caixa de seleção para ativar o monitoramento de segurança de família para uma conta recém-criada deve ser visível durante a criação da conta padrão no Windows 8 depois que o provedor é selecionado como o provedor de segurança da família atual.<br/> |

    

     

-   Como os provedores de terceiros são projetados para substituir a interface do usuário de configuração na caixa para controles de segurança da família, por padrão, a instalação e a ativação de um provedor de terceiros resultarão na opção de caixa de seleção para ativar a segurança da família durante a criação da conta padrão, que não deve ser mostrada.

## <a name="family-safety-top-level-user-interface-changes-in-windows-8"></a>Alterações de interface de usuário de nível superior de segurança de família no Windows 8

O Windows 8 traz as seguintes alterações para a interface do usuário de nível superior do painel de controle dos controles dos pais:

-   Quando os controles de segurança da família na caixa são ativados para pelo menos uma conta padrão em um computador com Windows 8, é mostrado o link de comando gerenciar configurações no site de segurança da família, que permite que um administrador estabeleça o gerenciamento remoto de configurações de segurança da família de computadores com o Windows 8 por meio do site de segurança da família.
-   Quando um computador com Windows 8 está configurado para gerenciamento remoto por meio do site de segurança da família, o controle mais informações permite que um administrador desabilite o gerenciamento remoto de um computador com Windows 8 por meio do site de segurança da família.
-   A seção de controles só é visível quando pelo menos um provedor de terceiros é registrado com a proteção da família. A interface do usuário e a funcionalidade desta seção são idênticas à seção controles adicionais nos controles dos pais do Windows 7. Para obter mais informações, consulte a seção controles pai de alterações na interface do usuário de nível superior do tópico [controles dos pais do Windows 7](what-s-new-in-windows-7-parental-controls.md) .
-   Quando um provedor de terceiros é instalado e selecionado como o provedor atual, o gerenciamento remoto de configurações de segurança da família de computadores do Windows 8 por meio do site de segurança da família é desabilitado.

## <a name="family-safety-in-box-restrictions-changes-in-windows-8"></a>Segurança de família In-Box restrições de alterações no Windows 8

O Windows 8 traz as seguintes alterações para as restrições internas de segurança da família:

Restrições da Web

-   A implementação foi alterada de um filtro LSP (provedor de serviços em camadas) para um driver WFP (plataforma de filtragem do Windows) que se comunica com o processo de monitoramento de segurança da família em execução nas sessões de usuários.

Limites de tempo

-   As restrições de tempo na caixa foram aprimoradas fornecendo a capacidade de controlar a quantidade total de tempo por dia que o computador pode ser usado (concessão de tempo), além da capacidade de controlar os tempos em que o computador pode ser usado (curfew), que estava disponível nas versões anteriores do Windows.
-   A interface do usuário para curfew permite o controle independente para cada dia da semana com granularidade de meia hora.
-   A interface do usuário para a bonificação de tempo permite que os controles de dias da semana/fins de semana ou controle independente sejam controlados por todos os dias das semanas com granularidade de 15 minutos.
-   O mecanismo do FUS (Fast User switch) não é mais usado para forçar o bloqueio ou bloquear o logon do usuário controlado no período de tempo bloqueado. Um comutador para uma área de trabalho separada é usado para essas finalidades.
-   Os eventos de aviso de desconexão não estão mais disponíveis para os aplicativos assinarem.

## <a name="family-safety-api-changes-in-windows-8"></a>Alterações da API de segurança da família no Windows 8

As APIs usadas para a proteção da família expõem as configurações de diretiva e restrições integradas e o registro em log da funcionalidade.

Log

-   Os eventos personalizados não têm mais suporte no Visualizador de relatórios de atividades de segurança da família.

Gravação/leitura das configurações da API WMI

-   WpcUserSettings-anteriormente, as restrições de temporizador suportavam uma granularidade de 1 hora. No Windows 8, a propriedade existente representa a primeira meia hora para cada hora. Uma nova propriedade de meia hora foi adicionada para representar a segunda metade de cada hora. Uma nova propriedade adicional foi introduzida para representar a concessão de tempo diária.

Filtro de conteúdo da Web permissão/bloquear lista exportar/importar um formato

-   Não há mais suporte para a funcionalidade de exportação da lista de permissões/bloqueio de filtro de conteúdo da Web.

Esquema de provedor WMI de configurações de família

-   As seguintes adições foram feitas na classe WpcUserSettings para refletir os aprimoramentos de restrições de tempo:
    -   `[write: ToInstance ToSubClass, Description("Logon Half-Hours (30 minute offset) mask for this user"): ToInstance ToSubClass, read: ToInstance ToSubClass] uint32 LogonHalfHours[7];`
    -   `[write: ToInstance ToSubClass, Description("Daily minute allowance"): ToInstance ToSubClass, read: ToInstance ToSubClass] uint32 AllowanceMinutes[7];`

> [!Note]  
> O Windows 8 usa uma nova chave do registro para indicar que a API de segurança da família está habilitada para um determinado usuário.
>
> **HKLM** \\ **Microsoft** \\ **Software** \\ **Windows** \\ **CurrentVersion** \\ **Controles** \\ dos pais **Usuários** \\ do **{Userid}** \\ **Web** \\ do **Filtrar em**

 

A chave do registro a seguir tem suporte apenas para o Windows 7.

**HKLM** \\ **Microsoft** \\ **Software** \\ **Windows** \\ **CurrentVersion** \\ **Controles** \\ dos pais **Usuários** \\ do **{Userid}** \\ **Controles dos pais em**

Para ambas as chaves, um valor de "0x00" (**DWORD**) indica que o recurso está desabilitado para o usuário atual e um valor de "0x01" (**DWORD**) indica que o recurso está habilitado para o usuário atual. Ao tentar ler os valores dessas chaves, substitua o token "{userid}" pela ID do sistema do usuário.

 

 




