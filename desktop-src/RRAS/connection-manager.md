---
title: Gerenciador de Conexões
description: Os clientes que pretendem desenvolver discadores personalizados usando a API do serviço de acesso remoto podem querer investigar o Gerenciador de conexões da Microsoft e o kit de administração do Gerenciador de conexões.
ms.assetid: c3227aea-ba36-44f6-b69d-2c6aa4be360e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7959482542630b6dc90149971df08f7944f83fc
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104007176"
---
# <a name="connection-manager"></a>Gerenciador de Conexões

Os clientes que pretendem desenvolver discadores personalizados usando a API do serviço de acesso remoto podem querer investigar o Gerenciador de conexões da Microsoft e o kit de administração do Gerenciador de conexões. O Gerenciador de conexões é o cliente de acesso remoto gerenciado da Microsoft. Ele permite que um administrador crie um pacote de configuração de acesso remoto para ser distribuído aos usuários remotos do administrador. Para obter mais informações sobre o Gerenciador de conexões e o kit de administração do Gerenciador de conexões, consulte a ajuda online do Microsoft Windows 2000 Server e sistemas operacionais posteriores.

Você pode encontrar o código-fonte para uma ação personalizada do Gerenciador de conexões de exemplo no SDK (Kit de desenvolvimento de software) completo da plataforma. O SDK da plataforma pode ser baixado no [site da Microsoft](https://msdn.microsoft.com/windowsserver/bb980924.aspx). Após a instalação, o caminho para o código de exemplo é% install caminho% \\ Microsoft SDK \\ Samples \\ netds \\ RAS \\ ConnectionManager, em que% install caminho% designa o diretório de instalação base do SDK da plataforma (por exemplo, C: \\ arquivos de programas).

As ações personalizadas possibilitam que o cliente de acesso remoto execute ações específicas em vários pontos no processo de conexão. A ação personalizada demonstrada no exemplo ajusta automaticamente a configuração do servidor proxy para uma conexão com base no endereço do servidor da conexão. Os clientes podem usar este exemplo como um ponto de partida para a criação de suas próprias ações personalizadas.

 

 




