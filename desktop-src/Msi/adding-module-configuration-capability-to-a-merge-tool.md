---
description: Windows Installer desenvolvedores podem criar ferramentas que permitem que os usuários finais usem módulos de mesclagem configuráveis.
ms.assetid: 5857b788-f1dd-41d0-b0ee-0872494e3c2c
title: Adicionando a funcionalidade de configuração de módulo a uma ferramenta de mesclagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba04d297ad93cffc553670c648577f650cd21407
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103662073"
---
# <a name="adding-module-configuration-capability-to-a-merge-tool"></a>Adicionando a funcionalidade de configuração de módulo a uma ferramenta de mesclagem

Para permitir que os usuários finais usem módulos de mesclagem configuráveis, você pode criar ferramentas de mesclagem e configuração para fazer o seguinte:

-   As ferramentas de mesclagem devem chamar as funções no Mergemod.dll versão 2,0 para mesclar o módulo. As versões anteriores do Mergemod.dll não podem ser usadas para configurar módulos de mesclagem.
-   Os aplicativos de configuração do cliente devem interagir com o usuário do módulo de mesclagem para coletar as seleções do usuário para itens configuráveis.
-   As ferramentas de mesclagem devem expor informações de configuração criadas no módulo de mesclagem para o aplicativo cliente para que o cliente possa usar essas informações para consultar o usuário.
-   Quando uma ferramenta de mesclagem encontra um item configurável durante uma mesclagem, ela deve chamar a ferramenta de configuração do cliente para obter informações de personalização obtidas do usuário. A ferramenta de mesclagem deve fazer as alterações especificadas no módulo de mesclagem.
-   Os aplicativos de configuração devem permitir que o usuário forneça opções para itens configuráveis, mas todas as opções possíveis não precisam ser reveladas ao usuário. A ferramenta de mesclagem pode usar valores padrão para itens configuráveis que o usuário não seleciona.
-   Se um usuário não fornecer informações de personalização, as ferramentas de mesclagem deverão usar os valores de configuração padrão especificados no módulo de mesclagem.
-   Depois que um usuário fornece as seleções específicas da ferramenta de configuração, a ferramenta de mesclagem chama Mergemod.dll para executar a mesclagem.

 

 



