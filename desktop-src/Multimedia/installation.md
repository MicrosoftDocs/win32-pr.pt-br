---
title: Instalação (multimídia do Windows)
description: Instalação
ms.assetid: 1f0e23ad-4db7-4f32-98d9-e672370db559
keywords:
- drivers instaláveis, instalando
- drivers instaláveis, DRV_INSTALL mensagem
- drivers instaláveis, DRV_REMOVE mensagem
- DRV_INSTALL mensagem
- DRV_REMOVE mensagem
- Mensagem DRVCONFIGINFO
- instalando drivers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4ebebd090c7499698c59c325d1ac0d487902454
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104369103"
---
# <a name="installation-windows-multimedia"></a>Instalação (multimídia do Windows)

Um driver instalável pode executar tarefas de instalação específicas do driver ao processar a [**\_ instalação do drv**](drv-install.md) e [**\_ remover**](drv-remove.md) as mensagens. Um aplicativo de instalação, como um aplicativo do painel de controle, envia as mensagens ao driver ao instalar ou remover o driver, respectivamente.

Ao processar a mensagem de instalação do DRV \_ , o driver normalmente verifica se o hardware necessário está presente e, em seguida, exibe a caixa de diálogo configuração para permitir que o usuário escolha as definições de configuração inicial para o driver e o hardware associado. A mensagem inclui o endereço de uma estrutura [**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) que contém os nomes da chave do registro e o valor associado ao driver; o driver verifica o valor do registro para obter informações de configuração padrão. Por fim, o driver também cria quaisquer chaves de registro e valores adicionais necessários para uma operação bem-sucedida.

Ao processar a mensagem de remoção de DRV \_ , o driver remove as chaves e os valores do registro que ele pode ter criado.

 

 
