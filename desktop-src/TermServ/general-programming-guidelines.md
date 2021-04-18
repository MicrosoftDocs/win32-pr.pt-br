---
title: Diretrizes gerais de programação
description: Diretrizes para o desenvolvimento de aplicativos em um ambiente Serviços de Área de Trabalho Remota.
ms.assetid: 95b49db5-ba3c-4638-9087-6ee3972d8972
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d465c658e64959eb1bfd61cf3c43f6ffd2cc6b1d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105761802"
---
# <a name="general-programming-guidelines"></a>Diretrizes gerais de programação

As seções a seguir fornecem diretrizes gerais para o desenvolvimento de aplicativos em um ambiente Serviços de Área de Trabalho Remota.

## <a name="in-this-section"></a>Nesta seção

<dl> <dt>

[Camada de compatibilidade de aplicativos](application-compatibility-layer.md)
</dt> <dd>

Para executar aplicativos herdados em um ambiente Serviços de Área de Trabalho Remota, você pode usar a camada de compatibilidade de aplicativos Serviços de Área de Trabalho Remota.

</dd> <dt>

[Diretrizes de aplicativo cliente/servidor](client-server-application-guidelines.md)
</dt> <dd>

Aplicativos cliente/servidor não devem assumir que uma única conexão de computador é equivalente a uma única sessão de usuário.

</dd> <dt>

[Monitorando conexões de sessão e desconexões](monitoring-session-connections-and-disconnections.md)
</dt> <dd>

Para registrar um aplicativo com Serviços de Área de Trabalho Remota, armazene o nome do aplicativo de servidor do virtual Channel no registro adicionando uma subchave.

</dd> <dt>

[Diretrizes de hardware periférico](peripheral-hardware-guidelines.md)
</dt> <dd>

Se o dispositivo de hardware não for projetado para funcionar em uma sessão remota, os fornecedores deverão garantir que o software do driver de dispositivo force a desabilitação do redirecionamento do dispositivo usando uma política do sistema ou uma política de grupo.

</dd> <dt>

[Vinculação de tempo de execução para Wtsapi32.dll](run-time-linking-to-wtsapi32-dll.md)
</dt> <dd>

Seu aplicativo pode usar a API Serviços de Área de Trabalho Remota para vincular dinamicamente ao Wtsapi32.dll em tempo de execução. Para fazer isso, seu aplicativo deve chamar a função [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) para carregar Wtsapi32.dll.

</dd> </dl>

 

 