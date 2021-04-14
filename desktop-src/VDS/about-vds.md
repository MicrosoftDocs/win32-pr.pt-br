---
description: Sobre o VDS
ms.assetid: b2f7628c-b567-40a9-9ad7-6c47077af5fb
title: Sobre o VDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 911145fda8f2dd63c886530af3d8507c38d8e829
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/04/2021
ms.locfileid: "104565497"
---
# <a name="about-vds"></a>Sobre o VDS

\[A partir do Windows 8 e do Windows Server 2012, a interface com do [serviço de disco virtual](virtual-disk-service-portal.md) é substituída pela [API de gerenciamento de armazenamento do Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

O serviço de disco virtual é um serviço do Microsoft Windows que executa operações de consulta e configuração na solicitação de usuários finais, scripts e aplicativos. O serviço estende os recursos de armazenamento existentes dos sistemas operacionais Windows Server das seguintes maneiras:

-   Fornece uma API para os recursos existentes de gerenciamento de volume e disco no Windows.
-   Unifica o gerenciamento de volume e o gerenciamento de discos independentes de hardware (RAID) em uma única API.

O VDS não executa as seguintes atividades de gerenciamento de armazenamento:

-   Gerenciamento de subsistema de hardware, como monitoramento de temperatura ou monitoramento de estatísticas de desempenho para matrizes de disco.
-   Gerenciamento de malha de SAN (rede de área de armazenamento), como zoneamento de Host-Based adaptador (HBA) e segurança.

As seções a seguir descrevem a arquitetura do VDS, a função de provedores de VDS e a API.

## <a name="service-architecture"></a>Arquitetura de serviço

O VDS define três interfaces: uma única interface entre a camada de aplicativo e o serviço e duas interfaces entre os programas de serviço e provedor na camada de dados. A ilustração a seguir mostra o limite de aplicativo para serviço e o limite de serviço a provedor.

![Diagrama que mostra a arquitetura de serviço dividida nas seções ' aplicativos ', ' serviço de disco virtual ' e ' provedores de VDS '.](images/vdsoverview.png)

A arquitetura de N camadas permite que o VDS coordene com as funções do sistema de arquivos, sincronize as atividades do provedor e arbitra entre os aplicativos. Estando entre o aplicativo e o provedor, o VDS apresenta funcionalidade uniforme para aplicativos, embora alguns provedores subjacentes possam não ter tal uniformidade.

O serviço implementa funcionalidade comum: formatação de volumes, adição e remoção de letras de unidade ou pastas montadas, bem como gerenciamento de discos não alocados, discos sem informações de partição. O VDS também retorna notificações de eventos para aplicativos registrados. Para obter detalhes, consulte [notificações do VDS](vds-notification-model.md).

## <a name="role-of-providers"></a>Função de provedores

O VDS define duas interfaces de provedor, uma para um provedor de software e outra para um provedor de hardware. Cada provedor implementa uma parte diferente da API definida pelo VDS:

-   Um *provedor de software* é um programa baseado em host que é suportado por um driver de modo kernel na pilha de e/s de armazenamento. O tempo de execução do kernel do provedor interage com o Gerenciador de montagem no momento da inicialização ou o Gerenciador de Plug and Play (PnP) no momento da descoberta para reivindicar cada disco. Os provedores de software operam em volumes, discos e partições de disco.

    O VDS inclui dois tipos de provedor. O provedor de software básico gerencia discos básicos e não oferece nenhuma associação tolerante a falhas. O provedor de software dinâmico gerencia discos dinâmicos e oferece gerenciamento de falhas quando aplicável. O comportamento do provedor de software é consistente com o comportamento de discos básicos e dinâmicos no host. Por exemplo, se o sistema operacional de um determinado host oferecer suporte a discos dinâmicos tolerantes a falhas, o VDS também dará suporte a esse comportamento no host.

-   Um *provedor de hardware* implementa os métodos que são usados para gerenciar um subsistema de armazenamento — uma matriz de disco de hardware ou placa de adaptador que permite a criação de discos lógicos configurados para aprimorar o desempenho, a disponibilidade de dados ou a recuperação de dados. Muitos grandes fabricantes de gabinetes de RAID produziram um provedor de hardware projetado para uso com o VDS. Os consumidores de serviço devem obter um provedor de hardware e um hardware associado do fabricante.

    Os recursos de um provedor de hardware dependem dos recursos do hardware subjacente. Consequentemente, o grau para o qual cada fabricante implementa a API pode variar. Por exemplo, os fabricantes podem incluir métodos adicionais para otimizar as configurações, monitorar e ajustar dinamicamente o desempenho, automatizar o gerenciamento de falhas ou fornecer outras funcionalidades úteis.

    Os provedores de hardware oferecem várias opções de configuração que não estão disponíveis para os provedores de software. O mais notável é o modelo de configuração automagic, que apresenta uma exibição baseada em atributo de armazenamento para cada aplicativo. Dicas de associação, como "leituras mais rápidas" ou "recuperação rápida de falhas necessárias" substituem a complexidade de associar o armazenamento físico ao armazenamento virtual. Cada provedor de hardware executa mapeamento de extensão, alocação de espaço e seleção de tipo de associação com base nas dicas que são enviadas por um aplicativo. Para obter a descrição completa do provedor de hardware, incluindo as opções de configuração, consulte a documentação fornecida pelo fabricante do subsistema.

## <a name="application-programming-interface"></a>Interface de programação de aplicativo

Os aplicativos podem invocar métodos VDS para consultar e configurar discos baseados em host, armazenamento RAID ou ambos. Para obter uma visão geral da API, consulte o [modelo de objeto do VDS](vds-object-model.md).

Os aplicativos típicos para o VDS solucionam problemas de gerenciamento e monitoramento de configuração e variam de sistemas de gerenciamento de armazenamento dedicados a aplicativos de Back Office que buscam um melhor controle sobre a configuração ou o gerenciamento de falhas. Os aplicativos a seguir usam o VDS hoje:

-   O snap-in de gerenciamento de disco configura e gerencia os discos controlados por um computador host. Os administradores do sistema e os usuários finais podem consultar e configurar discos e volumes locais (ou remotos) com essa ferramenta de interface do usuário.
-   Diskpart.exe é um utilitário de linha de comando que configura e gerencia discos, volumes e partições.
-   Diskraid.exe é um utilitário de linha de comando que configura e gerencia subsistemas RAID de hardware. Esse utilitário pode interagir com qualquer hardware de armazenamento acompanhado por um provedor de hardware VDS.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Serviço de Disco Virtual](virtual-disk-service-portal.md)
</dt> <dt>

[Notificações do VDS](vds-notification-model.md)
</dt> <dt>

[Modelo de objeto VDS](vds-object-model.md)
</dt> </dl>

 

 
