---
title: Instalação do aplicativo
description: Instalar um aplicativo para um único usuário pode criar problemas em um ambiente de Serviços de Área de Trabalho Remota multiusuário.
ms.assetid: 3e60e95a-3580-48aa-a9f9-8fd899aa7fca
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 743eff150edf5e9d213759ccef8c786bab98754b8e4dc2b968929ba3ad2d6709
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099586"
---
# <a name="application-setup"></a>Instalação do aplicativo

O procedimento de instalação automatizada para muitos aplicativos existentes pressu que o aplicativo está sendo instalado para um único usuário. Em um ambiente de Serviços de Área de Trabalho Remota multiusuário, essa suposição pode criar os seguintes problemas:

-   Se o procedimento de instalação atualizar o registro e o ambiente de área de trabalho de apenas um usuário, os usuários adicionais deverão reinstalar todo o pacote ou um administrador deverá copiar manualmente as informações do Registro e da área de trabalho de um usuário para os outros usuários.
-   Com alguns procedimentos de instalação, você pode personalizar o aplicativo no momento da instalação excluindo recursos. Se o instalador inicial excluir parte do aplicativo, os usuários adicionais deverão reinstalar o aplicativo para obter os recursos excluídos.

Para evitar esses problemas, os procedimentos de instalação devem usar as seguintes diretrizes ao instalar um aplicativo em um Host da Sessão da Área de Trabalho Remota (Host da Sessão RD) :

-   Instale aplicativos no ambiente de usuário padrão comum a todos os usuários. Antes de instalar o aplicativo, execute o comando alterar usuário **/instalar** console e, após a conclusão da instalação, execute o comando **alterar usuário /executar** console. Use um Serviços de Área de Trabalho Remota de compatibilidade para a instalação.
-   Dar suporte à personalização específica do usuário por meio do uso de perfis de usuário. Para fazer isso, crie um [Formato de](/previous-versions/windows/desktop/Policy/administrative-template-file-format) Arquivo de Modelo Administrativo para que um administrador possa configurar o Registro para indicar os recursos disponíveis para cada usuário. Em seguida, em tempo de operação, o aplicativo pode habilitar ou desabilitar recursos dependendo das configurações nas configurações do Registro do usuário atual. O aplicativo pode armazenar a configuração por usuário no hive do registro **HKEY CURRENT USER** e permitir que cada usuário configure o aplicativo de acordo com suas preferências.

 

 