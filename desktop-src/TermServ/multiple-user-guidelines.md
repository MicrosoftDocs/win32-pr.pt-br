---
title: Diretrizes de vários usuários
description: Diretrizes para o desenvolvimento de aplicativos para vários usuários em um ambiente de Serviços de Área de Trabalho Remota.
ms.assetid: c7acbedb-3bf2-4519-ab11-a50bf071e757
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a06db01da6d9413684e3197aa9758d6e5c04643f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105788032"
---
# <a name="multiple-user-guidelines"></a>Diretrizes de vários usuários

As seções a seguir fornecem diretrizes para o desenvolvimento de aplicativos para vários usuários em um ambiente de Serviços de Área de Trabalho Remota.

## <a name="in-this-section"></a>Nesta seção

<dl> <dt>

[Instalação do aplicativo](application-setup-in-a-terminal-services-environment.md)
</dt> <dd>

A instalação de um aplicativo para um único usuário pode criar problemas em um ambiente de Serviços de Área de Trabalho Remota multiusuário.

</dd> <dt>

[Armazenando informações específicas do usuário](storing-user-specific-information.md)
</dt> <dd>

Aplicativos devem armazenar informações específicas do usuário em locais específicos do usuário, separadamente de informações globais que se aplicam a todos os usuários.

</dd> <dt>

[Namespaces de objeto kernel](kernel-object-namespaces.md)
</dt> <dd>

Serviços de Área de Trabalho Remota usa vários namespaces para objetos kernel; um namespace global é usado principalmente por serviços em aplicativos cliente/servidor.

</dd> <dt>

[Endereços IP e nomes de computador](ip-addresses-and-computer-names.md)
</dt> <dd>

Não é seguro pressupor que o nome do computador ou o endereço IP atribuído ao computador está associados um único usuário, pois vários usuários podem ser conectados simultaneamente a um servidor de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD).

</dd> </dl>

Como sempre, bloqueie arquivos e bancos de dados ao fazer alterações para evitar a perda inadvertida de dado.

Seu aplicativo não deve bloquear nenhum arquivo de aplicativo em tempo de execução que não seja de arquivos por usuário. Arquivos de tempo de execução bloqueados podem manter várias instâncias do aplicativo ou os processos sob o aplicativo, como assistentes, de serem executados. Uma boa maneira de testar quais arquivos são arquivos de aplicativo em tempo de execução é controlar quais arquivos são instalados pela instalação do aplicativo. Arquivos por usuário raramente são instalados pela instalação; Portanto, a maioria dos arquivos instalados pela instalação são arquivos de aplicativo de tempo de execução.

 

 




