---
title: Gerenciador de Conexões
description: Os clientes que pretendem desenvolver discadores personalizados usando a API do serviço de acesso remoto podem querer investigar o Gerenciador de conexões da Microsoft e o kit de administração do Gerenciador de conexões.
ms.assetid: c3227aea-ba36-44f6-b69d-2c6aa4be360e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc20979ecd99f904aef158738d49ce1e5bc5a25309288db83dfc99de05959234
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117791580"
---
# <a name="connection-manager"></a>Gerenciador de Conexões

Os clientes que pretendem desenvolver discadores personalizados usando a API do serviço de acesso remoto podem querer investigar o Gerenciador de conexões da Microsoft e o kit de administração do Gerenciador de conexões. O Gerenciador de conexões é o cliente de acesso remoto gerenciado da Microsoft. Ele permite que um administrador crie um pacote de configuração de acesso remoto para ser distribuído aos usuários remotos do administrador. para obter mais informações sobre o gerenciador de conexões e o Kit de administração do gerenciador de conexões, consulte a ajuda online do servidor Microsoft Windows 2000 e sistemas operacionais posteriores.

Você pode encontrar o código-fonte para uma ação personalizada do Gerenciador de conexões de exemplo no SDK (Kit de desenvolvimento de software) completo da plataforma. O SDK da plataforma pode ser baixado no [site da Microsoft](https://msdn.microsoft.com/windowsserver/bb980924.aspx). Após a instalação, o caminho para o código de exemplo é% install caminho% \\ Microsoft SDK \\ Samples \\ netds \\ RAS \\ ConnectionManager, em que% install caminho% designa o diretório de instalação base do SDK da plataforma (por exemplo, C: \\ arquivos de programas).

As ações personalizadas possibilitam que o cliente de acesso remoto execute ações específicas em vários pontos no processo de conexão. A ação personalizada demonstrada no exemplo ajusta automaticamente a configuração do servidor proxy para uma conexão com base no endereço do servidor da conexão. Os clientes podem usar este exemplo como um ponto de partida para a criação de suas próprias ações personalizadas.

 

 




