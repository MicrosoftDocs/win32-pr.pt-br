---
title: Usando o Microsoft Locator
description: O Microsoft Locator é o serviço de nome padrão. A biblioteca de tempo de execução RPC usa-a para encontrar programas de servidor em sistemas de host de servidor.
ms.assetid: 8481de50-4e72-432d-aef7-524f18f5c9c4
keywords:
- RPC de chamada de procedimento remoto, tarefas, usando o Microsoft Locator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f64a5c54c09ee344ffdba46f9f44a546ab866557bc861b206868ad6d3992896b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010734"
---
# <a name="using-microsoft-locator"></a>Usando o Microsoft Locator

O Microsoft Locator é o serviço de nome padrão. A biblioteca de tempo de execução RPC usa-a para encontrar programas de servidor em sistemas de host de servidor.

**Observação**  o localizador de RPC da Microsoft não tem suporte no Windows Vista e em sistemas operacionais posteriores.

antes do Windows 2000, o Microsoft Locator não fornece entradas de serviço de nome persistentes. Todas as entradas no serviço de nome foram armazenadas em um cache de memória no computador host do programa do servidor. O localizador usou um mecanismo de difusão para descobrir o local dos servidores conforme solicitado pelos clientes. Sempre que o sistema host for desligado, todas as entradas de serviço de nome foram perdidas.

a partir do lançamento do Windows 2000, o Microsoft Locator agora oferece suporte a entradas de serviço de nome persistentes. Para fazer isso, o sistema emprega um serviço de diretório distribuído para armazenar entradas de serviço de nome. Esse mecanismo tem várias vantagens:

-   **Persistência.** Os programas de servidor não são mais necessários para exportar suas informações de associação para o serviço de nome cada vez que eles são iniciados. O serviço de nome agora armazena as informações até que o programa do servidor no administrador de rede a remova explicitamente.
-   **Redução.** Ao eliminar a maior parte da difusão de entradas de serviço de nome, o localizador reduz o tráfego de rede. Ele também localiza entradas de serviço de nome mais rapidamente.
-   **Interoperabilidade entre domínios.** Agora, os clientes podem fazer solicitações de serviço de nome em vários domínios.

As versões atuais do Microsoft Locator são compatíveis com versões anteriores. por exemplo, um sistema de host de servidor executando o localizador que acompanha o Windows 2000 pode operar corretamente em uma rede que contém sistemas de host de servidor que executam o localizador fornecido com Windows NT 4,0.

com o lançamento do Windows 2000, o Microsoft Locator agora dá suporte a entradas de serviço de nome para grupos de usuários. Ele também fornece a capacidade de criar perfis de usuário.

Além disso, a versão atual do Microsoft Locator oferece suporte ao uso de listas de controle de acesso em entradas de serviço de nome. Essa capacidade melhora a segurança da rede.

O suporte a Plug and Play agora está incluído no Microsoft Locator. Portanto, ele pode manipular Plug and Play eventos de forma transparente, como alterações de domínio. Para obter mais informações, consulte [**RpcNsBindingExportPnP**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexportpnpa) e [**RpcNsBindingUnexportPnP**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingunexportpnpa).

 

 




