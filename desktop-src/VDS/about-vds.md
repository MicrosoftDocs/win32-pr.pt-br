---
description: Sobre VDS
ms.assetid: b2f7628c-b567-40a9-9ad7-6c47077af5fb
title: Sobre VDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1215251bf86c3ac4ba9a7a342a483de19653d20a21978715261b87aa7bea31a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118603706"
---
# <a name="about-vds"></a>Sobre VDS

\[Começando com Windows 8 e Windows Server 2012, a interface COM do Serviço de Disco [Virtual](virtual-disk-service-portal.md) é superada pelo [Windows Armazenamento API de Gerenciamento](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

O Serviço de Disco Virtual é um serviço microsoft Windows que executa operações de consulta e configuração na solicitação de usuários finais, scripts e aplicativos. O serviço estende os recursos de armazenamento existentes dos sistemas operacionais Windows Server das seguintes maneiras:

-   Fornece uma API para os recursos de gerenciamento de disco e volume existentes Windows.
-   Unifica o gerenciamento de volume e o gerenciamento raid (matriz redundante de discos independentes) de hardware em uma única API.

O VDS não executa as seguintes atividades de gerenciamento de armazenamento:

-   Gerenciamento de subsistema de hardware, como monitoramento de temperatura ou monitoramento de estatísticas de desempenho para matrizes de disco.
-   Armazenamento Gerenciamento de malha san (rede de área), como o zoneamento e a segurança do HBA (Adaptador Host-Based).

As seções a seguir descrevem a arquitetura do VDS, a função de provedores de VDS e a API.

## <a name="service-architecture"></a>Arquitetura de serviço

O VDS define três interfaces: uma única interface entre a camada de aplicativo e o serviço e duas interfaces entre os programas de serviço e provedor na camada de dados. A ilustração a seguir mostra o limite de aplicativo para serviço e o limite de serviço para provedor.

![Diagrama que mostra a arquitetura de serviço dividida nas seções 'Aplicativos', 'Serviço de Disco Virtual' e 'Provedores de VDS'.](images/vdsoverview.png)

A arquitetura de N camadas permite que o VDS coordene com as funções do sistema de arquivos, sincronibilizar atividades do provedor e fazer a replicação entre aplicativos. Estando entre o aplicativo e o provedor, o VDS apresenta uma funcionalidade uniforme para aplicativos, embora alguns provedores subjacentes possam não ter essa uniformidade.

O serviço implementa funcionalidades comuns: formatação de volumes, adição e remoção de letras de unidade ou pastas montadas, bem como o gerenciamento de discos não alocados – discos sem informações de partição. O VDS também retorna notificações de eventos para aplicativos registrados. Para obter detalhes, consulte [Notificações de VDS](vds-notification-model.md).

## <a name="role-of-providers"></a>Função de provedores

O VDS define duas interfaces de provedor, uma para um provedor de software e outra para um provedor de hardware. Cada provedor implementa uma parte diferente da API definida pelo VDS:

-   Um *provedor de software* é um programa baseado em host com suporte por um driver de modo kernel na pilha de E/S de armazenamento. O runtime do kernel do provedor interage com o Mount Manager no momento da inicialização ou com o PnP (Gerenciador de Plug and Play) no momento da descoberta para reivindicar cada disco. Os provedores de software operam em volumes, discos e partições de disco.

    O VDS inclui dois tipos de provedor. O provedor de software básico gerencia discos básicos e não oferece nenhuma associação tolerante a falhas. O provedor de software dinâmico gerencia discos dinâmicos e oferece gerenciamento de falhas quando aplicável. O comportamento do provedor de software é consistente com o comportamento de discos básicos e dinâmicos no host. Por exemplo, se o sistema operacional de um determinado host dá suporte a discos dinâmicos tolerantes a falhas, o VDS também dá suporte a esse comportamento no host.

-   Um provedor de *hardware* implementa os métodos usados para gerenciar um subsistema de armazenamento – uma matriz de disco de hardware ou placa de adaptador que permite a criação de discos lógicos configurados para aprimorar o desempenho, a disponibilidade de dados ou a recuperação de dados. Muitos grandes fabricantes de gabinete RAID produziram um provedor de hardware projetado para uso com VDS. Os consumidores de serviço devem obter um provedor de hardware e hardware associado do fabricante.

    Os recursos de um provedor de hardware dependem dos recursos do hardware subjacente. Consequentemente, o grau até o qual cada fabricante implementa a API pode variar. Por exemplo, os fabricantes podem incluir métodos adicionais para otimizar configurações, monitorar e ajustar dinamicamente o desempenho, automatizar o gerenciamento de falhas ou fornecer outras funcionalidades benéficas.

    Os provedores de hardware oferecem várias opções de configuração que não estão disponíveis para os provedores de software. O mais importante é o modelo de configuração automagética, que apresenta uma exibição baseada em atributo de armazenamento para cada aplicativo. Dicas de associação, como "principalmente leituras" ou "recuperação rápida de falhas necessárias" substituem a complexidade da associação do armazenamento físico ao armazenamento virtual. Cada provedor de hardware executa mapeamento de extensão, alocação de espaço e seleção de tipo de associação com base nas dicas enviadas por um aplicativo. Para ver a descrição completa do provedor de hardware, incluindo as opções de configuração, consulte a documentação fornecida pelo fabricante do subsistema.

## <a name="application-programming-interface"></a>Interface de Programação de Aplicativo

Os aplicativos podem invocar métodos VDS para consultar e configurar discos baseados em host, armazenamento RAID ou ambos. Para uma visão geral da API, consulte o [Modelo de Objeto VDS](vds-object-model.md).

Aplicativos típicos para VDS resolvem problemas de monitoramento e gerenciamento de configuração e variam de sistemas de gerenciamento de armazenamento dedicados a aplicativos de back-office que buscam um melhor controle sobre a configuração ou o gerenciamento de falhas. Os aplicativos a seguir usam o VDS hoje:

-   O snap-in Gerenciamento de Disco configura e gerencia discos controlados por um computador host. Os administradores do sistema e os usuários finais podem consultar e configurar discos e volumes locais (ou remotos) com essa ferramenta de interface do usuário.
-   Diskpart.exe é um utilitário de linha de comando que configura e gerencia discos, volumes e partições.
-   Diskraid.exe é um utilitário de linha de comando que configura e gerencia subsistemas RAID de hardware. Esse utilitário pode interagir com qualquer hardware de armazenamento que seja acompanhado por um provedor de hardware VDS.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Serviço de Disco Virtual](virtual-disk-service-portal.md)
</dt> <dt>

[Notificações de VDS](vds-notification-model.md)
</dt> <dt>

[Modelo de objeto VDS](vds-object-model.md)
</dt> </dl>

 

 
