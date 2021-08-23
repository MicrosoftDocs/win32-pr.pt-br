---
title: Arquitetura do Gerenciador de Listas de Rede
description: Arquitetura do Gerenciador de Listas de Rede
ms.assetid: d3d03891-7c61-4f7e-a2e2-ef13353e8688
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 108ecbb36c5421bc7e3057c43feb10f92400493b306ecb21502a541c1bb4cba6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119685637"
---
# <a name="network-list-manager-architecture"></a>Arquitetura do Gerenciador de Listas de Rede

O Gerenciador de Lista de Rede é executado como um serviço no contexto Svchost.exe e é iniciado durante o procedimento de inicialização do computador. O serviço Gerenciador de Lista de Rede mantém uma tabela de redes e atributos de rede disponíveis que são recuperados por aplicativos por meio da API do Gerenciador de Listas de Rede. O Gerenciador de Lista de Rede fornece funções básicas para filtrar e consultar o serviço Gerenciador de Listas de Rede para redes específicas e recuperar os atributos dessas redes. O diagrama a seguir mostra a arquitetura do Gerenciador de Lista de Rede e a interação entre o serviço Gerenciador de Listas de Rede e o aplicativo cliente.

![diagrama de arquitetura de reconhecimento de rede](images/architecture.png)

 

 




