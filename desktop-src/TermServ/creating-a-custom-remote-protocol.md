---
title: Criando um provedor de protocolo RDP
description: Informações sobre como criar um provedor de protocolo RDP. O Gerenciador de protocolo é implementado como um servidor COM e registrado em um local pesquisado quando o serviço de Serviços de Área de Trabalho Remota é iniciado.
ms.assetid: 9a3e6d5c-464f-4227-a06f-16eb8ed1079e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d41265a350b4d5c559731a09abc21aa4c81b9b29
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105759948"
---
# <a name="creating-a-remote-desktop-protocol-provider"></a>Criando um provedor de protocolo RDP

As seções a seguir contêm informações sobre como criar um provedor de protocolo RDP. O Gerenciador de protocolo é implementado como um servidor COM e registrado em um local pesquisado quando o serviço de Serviços de Área de Trabalho Remota é iniciado.

## <a name="in-this-section"></a>Nesta seção

<dl> <dt>

[Registrando o Gerenciador de protocolo](registering-the-custom-protocol.md)
</dt> <dd>

Você deve criar pelo menos uma entrada de valor de registro para o Gerenciador de protocolo para que o serviço de Serviços de Área de Trabalho Remota possa instanciá-lo.

</dd> <dt>

[Sequência de chamada de método](method-call-sequence.md)
</dt> <dd>

O serviço de Serviços de Área de Trabalho Remota e seu provedor de protocolo chamam uns aos outros em sequências claramente definidas.

</dd> </dl>

-   [Registrando o Gerenciador de protocolo](registering-the-custom-protocol.md)
-   [Sequência de chamada de método](method-call-sequence.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[API do provedor de protocolo RDP](custom-remote-desktop-protocols.md)
</dt> <dt>

[Usando Serviços de Área de Trabalho Remota](using-terminal-services.md)
</dt> </dl>

 

 




