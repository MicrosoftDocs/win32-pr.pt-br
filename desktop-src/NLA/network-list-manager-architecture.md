---
title: Arquitetura do Gerenciador de lista de rede
description: Arquitetura do Gerenciador de lista de rede
ms.assetid: d3d03891-7c61-4f7e-a2e2-ef13353e8688
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a567b103cfd5d9944aa33a799c2cc1bc4b983759
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916629"
---
# <a name="network-list-manager-architecture"></a>Arquitetura do Gerenciador de lista de rede

O Gerenciador de lista de rede é executado como um serviço no contexto de Svchost.exe e é iniciado durante o procedimento de inicialização do computador. O serviço Gerenciador de listas de rede mantém uma tabela de redes disponíveis e atributos de rede que são recuperados por aplicativos por meio da API do Gerenciador de listas de rede. O Gerenciador de lista de rede fornece funções básicas para filtrar e consultar o serviço Gerenciador de listas de rede para redes específicas e recuperar os atributos dessas redes. O diagrama a seguir mostra a arquitetura do Gerenciador de lista de rede e a interação entre o serviço Gerenciador de lista de rede e o aplicativo cliente.

![diagrama da arquitetura de reconhecimento de rede](images/architecture.png)

 

 




