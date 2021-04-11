---
title: Instalação do aplicativo
description: A instalação de um aplicativo para um único usuário pode criar problemas em um ambiente de Serviços de Área de Trabalho Remota multiusuário.
ms.assetid: 3e60e95a-3580-48aa-a9f9-8fd899aa7fca
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58f3c53f2370f4123352489ac747546e3335c558
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294361"
---
# <a name="application-setup"></a>Instalação do aplicativo

O procedimento de configuração automatizada para muitos aplicativos existentes pressupõe que o aplicativo está sendo instalado para um único usuário. Em um ambiente de Serviços de Área de Trabalho Remota multiusuário, essa suposição pode criar os seguintes problemas:

-   Se o procedimento de instalação atualizar o ambiente do registro e da área de trabalho para apenas um usuário, os usuários adicionais deverão reinstalar o pacote inteiro ou o administrador deverá copiar manualmente as informações do registro e da área de trabalho de um usuário para os outros usuários.
-   Com alguns procedimentos de instalação, você pode personalizar o aplicativo no momento da instalação excluindo recursos. Se o instalador inicial excluir parte do aplicativo, os usuários adicionais deverão reinstalar o aplicativo para obter os recursos excluídos.

Para evitar esses problemas, os procedimentos de instalação devem usar as seguintes diretrizes ao instalar um aplicativo em um servidor de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD):

-   Instale aplicativos no ambiente de usuário padrão comum a todos os usuários. Antes de instalar o aplicativo, execute o comando **Change User/install** console e, após a conclusão da instalação, execute o comando **Change User/execute** console. Use um script de compatibilidade Serviços de Área de Trabalho Remota para a instalação.
-   Dar suporte à personalização específica do usuário por meio do uso de perfis de usuário. Para fazer isso, crie um [formato de arquivo de modelo administrativo](/previous-versions/windows/desktop/Policy/administrative-template-file-format) para que um administrador possa configurar o registro para indicar os recursos disponíveis para cada usuário. Em seguida, em tempo de execução, o aplicativo pode habilitar ou desabilitar recursos dependendo das configurações nas configurações do registro do usuário atual. O aplicativo pode armazenar a configuração por usuário no hive **HKEY Current User** Registry e permitir que todos os usuários configurem o aplicativo de acordo com suas preferências.

 

 