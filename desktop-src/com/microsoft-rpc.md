---
title: RPC da Microsoft
description: RPC da Microsoft
ms.assetid: a9ca629a-2766-43d5-89da-73d0628b3c5e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53be9d46368ae01aee25815327aafeaf7f44525b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634819"
---
# <a name="microsoft-rpc"></a>RPC da Microsoft

O Microsoft RPC é um modelo de programação em um ambiente de computação distribuído. O objetivo do RPC é fornecer comunicação transparente para que o cliente pareça estar diretamente se comunicando com o servidor. A implementação do RPC da Microsoft é compatível com o ambiente de computação distribuída (uso) do Open Software Foundation (DCE).

Você pode configurar o RPC para usar um ou mais transportes, um ou mais serviços de nome e um ou mais servidores de segurança. As interfaces para esses provedores são manipuladas pelo RPC. Como o Microsoft RPC foi projetado para funcionar com vários provedores, você pode escolher os provedores que funcionam melhor para sua rede. O transporte é responsável por transmitir os dados pela rede. O nome do serviço usa um nome de objeto, como um moniker, e localiza seu local na rede. O servidor de segurança oferece aos aplicativos a opção de negar acesso a usuários e/ou grupos específicos. Consulte [regras de design de interface](interface-design-rules.md) para obter informações mais detalhadas sobre a segurança do aplicativo.

Além das bibliotecas de tempo de execução RPC, o Microsoft RPC inclui o IDL (Interface Definition Language) e seu compilador. Embora o arquivo IDL seja uma parte padrão do RPC, a Microsoft o aprimorou para estender sua funcionalidade para dar suporte a interfaces COM personalizadas. O compilador de linguagem IDL da Microsoft (MIDL) usa o arquivo IDL que descreve sua interface personalizada para gerar vários arquivos discutidos na [criação e no registro de uma DLL de proxy](building-and-registering-a-proxy-dll.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Channel](channel.md)
</dt> <dt>

[Comunicação entre objetos](inter-object-communication.md)
</dt> <dt>

[Detalhes de marshaling](marshaling-details.md)
</dt> <dt>

[Proxy](proxy.md)
</dt> <dt>

[Gerenciador](stub.md)
</dt> </dl>

 

 




