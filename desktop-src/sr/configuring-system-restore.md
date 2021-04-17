---
title: Configurando a restauração do sistema
description: A restauração do sistema usa Instrumentação de Gerenciamento do Windows (WMI) para fornecer uma maneira programável de configurar e usar sua funcionalidade. Ele expõe duas classes, SystemRestore e SystemRestoreConfig, no namespace root \\ padrão.
ms.assetid: b510c5b7-71ec-47f9-b567-45fde8c79f57
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 323f75cd80f7838e643922d8b9ffa7bf2b121945
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366253"
---
# <a name="configuring-system-restore"></a>Configurando a restauração do sistema

A restauração do sistema usa [Instrumentação de gerenciamento do Windows](/windows/desktop/WmiSdk/wmi-start-page) (WMI) para fornecer uma maneira programável de configurar e usar sua funcionalidade. Ele expõe duas classes, [**SystemRestore**](systemrestore.md) e [**SystemRestoreConfig**](systemrestoreconfig.md), no namespace root \\ padrão.

A classe [**SystemRestore**](systemrestore.md) fornece métodos para as seguintes tarefas:

-   Desabilitando e habilitando o monitoramento
-   Listando pontos de restauração disponíveis
-   Iniciando uma restauração no sistema local
-   Recuperando o status da última restauração do sistema

A classe [**SystemRestoreConfig**](systemrestoreconfig.md) fornece propriedades para controlar a frequência da criação do ponto de restauração agendado e a quantidade de espaço em disco consumida pela restauração do sistema em cada unidade.

Ambas as classes podem ser acessadas remotamente usando técnicas padrão de WMI. Para obter uma descrição completa do WMI, consulte [Instrumentação de gerenciamento do Windows](/windows/desktop/WmiSdk/wmi-start-page).

 

 