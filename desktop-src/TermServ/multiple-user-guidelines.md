---
title: Diretrizes de vários usuários
description: Diretrizes para o desenvolvimento de aplicativos para vários usuários em um Serviços de Área de Trabalho Remota ambiente.
ms.assetid: c7acbedb-3bf2-4519-ab11-a50bf071e757
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bc598042530ab59c0c8932522185ce5a9d0d3dce04cabce44239c3c81b79d59
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119988846"
---
# <a name="multiple-user-guidelines"></a>Diretrizes de vários usuários

As seções a seguir fornecem diretrizes para o desenvolvimento de aplicativos para vários usuários em um Serviços de Área de Trabalho Remota ambiente.

## <a name="in-this-section"></a>Nesta seção

<dl> <dt>

[Instalação do aplicativo](application-setup-in-a-terminal-services-environment.md)
</dt> <dd>

A instalação de um aplicativo para um único usuário pode criar problemas em um ambiente de Serviços de Área de Trabalho Remota multiusuário.

</dd> <dt>

[Armazenar informações específicas do usuário](storing-user-specific-information.md)
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

Como sempre, bloqueie arquivos e bancos de dados ao fazer alterações para evitar a perda inadvertida de dados.

Seu aplicativo não deve bloquear nenhum arquivo de aplicativo em tempo de executar que não sejam arquivos por usuário. Arquivos em tempo de execução bloqueados podem impedir a execução de várias instâncias do aplicativo ou processos no aplicativo, como assistentes. Uma boa maneira de testar quais arquivos são arquivos de aplicativo em tempo de executar é controlar quais arquivos são instalados pela configuração do aplicativo. Arquivos por usuário raramente são instalados pela instalação; portanto, a maioria dos arquivos instalados pela instalação são arquivos de aplicativo em tempo de executar.

 

 




