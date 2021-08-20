---
title: Instalação (Windows Multimídia)
description: Saiba mais sobre a Windows Multimídia, incluindo o processamento DRV_INSTALL e DRV_REMOVE mensagens.
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
ms.openlocfilehash: a01ef47952f3d5a62c0dce246bf24689d37f11326f0f3ec251f7afc19c822fa9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118140674"
---
# <a name="installation-windows-multimedia"></a>Instalação (Windows Multimídia)

Um driver instalável pode executar tarefas de instalação específicas do driver ao processar as mensagens [**DRV \_ INSTALL**](drv-install.md) e [**DRV \_ REMOVE.**](drv-remove.md) Um aplicativo de instalação, como um Painel de Controle, envia as mensagens ao driver ao instalar ou remover o driver, respectivamente.

Ao processar a mensagem DRV INSTALL, o driver normalmente verifica se o hardware necessário está presente e exibe a caixa de diálogo de configuração para permitir que o usuário escolha as definições de configuração iniciais para o driver e o \_ hardware associado. A mensagem inclui o endereço de uma estrutura [**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) que contém os nomes da chave do Registro e o valor associados ao driver; o driver verifica o valor do Registro para obter informações de configuração padrão. Por fim, o driver também cria quaisquer chaves e valores adicionais do Registro necessários para uma operação bem-sucedida.

Ao processar a mensagem DRV REMOVE, o driver remove todas as chaves do Registro e \_ os valores que ele pode ter criado.

 

 
