---
title: Funções e mensagens de driver instaláveis
description: Funções e mensagens de driver instaláveis
ms.assetid: f487705a-ae8e-4ea8-bfd5-9b0f6087ddbb
keywords:
- drivers instaláveis, funções
- drivers instaláveis, mensagens
- drivers instaláveis, função OpenDriver
- Função OpenDriver
- drivers instaláveis, mensagens personalizadas
- mensagens do driver
- mensagens de driver personalizado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c66e6ebaac73bf8eb779119750cb390481152c3f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103917264"
---
# <a name="installable-driver-functions-and-messages"></a>Funções e mensagens de driver instaláveis

Você pode abrir um driver instalável de um aplicativo usando a função [**OpenDriver**](/windows/win32/api/mmiscapi/nf-mmiscapi-opendriver) . Essa função cria uma instância do driver, carregando o driver na memória se nenhuma outra instância existir e retorna o identificador da nova instância. Ao abrir um driver instalável, você deve fornecer o caminho completo do driver ou os nomes da chave do registro e o valor associado ao driver.

Quando um driver estiver aberto, você poderá direcioná-lo para executar tarefas usando a função [**SendDriverMessage**](/windows/win32/api/mmiscapi/nf-mmiscapi-senddrivermessage) para enviar mensagens de driver ao driver. Por exemplo, você pode direcionar o driver para exibir sua caixa de diálogo de configuração enviando a mensagem de [**\_ Configurar drv**](drv-configure.md) . Antes de enviar essa mensagem, você deve determinar se o driver tem uma caixa de diálogo de configuração enviando a mensagem [**\_ QUERYCONFIGURE drv**](drv-queryconfigure.md) e verificando um valor de retorno diferente de zero. Muitos drivers fornecem um conjunto de mensagens personalizadas que você pode enviar para direcionar as operações do driver.

Se você precisar de acesso especial a um driver instalável, como o acesso a seus recursos, poderá recuperar o identificador de módulo do driver usando a função [**GetDriverModuleHandle**](/windows/win32/api/mmiscapi/nf-mmiscapi-getdrivermodulehandle) .

Quando você não precisar mais do driver instalável, poderá fechá-lo usando a função [**CloseDriver**](/windows/win32/api/mmiscapi/nf-mmiscapi-closedriver) .

Você pode usar as funções e mensagens de driver instaláveis para abrir e gerenciar qualquer driver instalável. No entanto, o curso recomendado de ação para abrir e gerenciar dispositivos multimídia é primeiro usar os serviços padrão (como [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen), [**waveOutMessage**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutmessage)e [**waveOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutclose) para dispositivos de saída de forma de onda), se existirem. Se os serviços padrão não existirem para um driver de multimídia, abra e gerencie o driver usando as funções e mensagens de driver instaláveis.

> [!Note]  
> As funções [**SendDriverMessage**](/windows/win32/api/mmiscapi/nf-mmiscapi-senddrivermessage) e [**GetDriverModuleHandle**](/windows/win32/api/mmiscapi/nf-mmiscapi-getdrivermodulehandle) são as funções preferenciais a serem usadas para enviar mensagens a um driver e para obter um identificador para uma instância de módulo. No entanto, a função [**DrvGetModuleHandle**](/windows/win32/api/mmiscapi/nf-mmiscapi-drvgetmodulehandle) mais antiga foi incluída para manter a compatibilidade com as versões anteriores do sistema operacional Windows.

 

 

 