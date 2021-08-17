---
title: Criando um provedor protocolo RDP dados
description: Informações sobre como criar um provedor protocolo RDP dados. O gerenciador de protocolo é implementado como um servidor COM e registrado em um local pesquisado quando o serviço Serviços de Área de Trabalho Remota é iniciado.
ms.assetid: 9a3e6d5c-464f-4227-a06f-16eb8ed1079e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28a7905bfcc623174aca9152f0807a867112aee1a0c54976db810b87f8b3408f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118856212"
---
# <a name="creating-a-remote-desktop-protocol-provider"></a>Criando um provedor protocolo RDP dados

As seções a seguir contêm informações sobre como criar um provedor protocolo RDP dados. O gerenciador de protocolo é implementado como um servidor COM e registrado em um local pesquisado quando o serviço Serviços de Área de Trabalho Remota é iniciado.

## <a name="in-this-section"></a>Nesta seção

<dl> <dt>

[Registrando o Gerenciador de Protocolos](registering-the-custom-protocol.md)
</dt> <dd>

Você deve criar pelo menos uma entrada de valor do Registro para o gerenciador de protocolos para que o serviço Serviços de Área de Trabalho Remota possa instaurá-la.

</dd> <dt>

[Sequência de chamada de método](method-call-sequence.md)
</dt> <dd>

O Serviços de Área de Trabalho Remota e seu provedor de protocolo chamam uns aos outros em sequências claramente definidas.

</dd> </dl>

-   [Registrando o Gerenciador de Protocolos](registering-the-custom-protocol.md)
-   [Sequência de chamada de método](method-call-sequence.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[API protocolo RDP provedor de serviços](custom-remote-desktop-protocols.md)
</dt> <dt>

[Usando Serviços de Área de Trabalho Remota](using-terminal-services.md)
</dt> </dl>

 

 




