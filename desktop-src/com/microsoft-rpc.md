---
title: Microsoft RPC
description: Microsoft RPC
ms.assetid: a9ca629a-2766-43d5-89da-73d0628b3c5e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed515b1ca8e58e8e9daaa2bb037dbb9c33ad1d6bb15bd7dc42abd52771e8267a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130168"
---
# <a name="microsoft-rpc"></a>Microsoft RPC

O Microsoft RPC é um modelo para programação em um ambiente de computação distribuído. O objetivo do RPC é fornecer comunicação transparente para que o cliente pareça estar se comunicando diretamente com o servidor. A implementação do RPC pela Microsoft é compatível com o RPC do DCE (Ambiente de Computação Distribuída) do OSF (Open Software Foundation).

Você pode configurar o RPC para usar um ou mais transportes, um ou mais serviços de nome e um ou mais servidores de segurança. As interfaces para esses provedores são manipuladas pelo RPC. Como o Microsoft RPC foi projetado para trabalhar com vários provedores, você pode escolher os provedores que funcionam melhor para sua rede. O transporte é responsável por transmitir os dados pela rede. O serviço de nome recebe um nome de objeto, como um moniker, e localiza seu local na rede. O servidor de segurança oferece aos aplicativos a opção de negar acesso a usuários e/ou grupos específicos. Consulte [Regras de design de interface](interface-design-rules.md) para obter informações mais detalhadas sobre a segurança do aplicativo.

Além das bibliotecas de tempo de executar RPC, o Microsoft RPC inclui a IDL (Linguagem de Definição de Interface) e seu compilador. Embora o arquivo IDL seja uma parte padrão do RPC, a Microsoft o aprimorou para estender sua funcionalidade para dar suporte a interfaces COM personalizadas. O compilador linguagem IDL da Microsoft (MIDL) usa o arquivo IDL que descreve sua interface personalizada para gerar vários arquivos discutidos em Criando e registrando uma [DLL proxy.](building-and-registering-a-proxy-dll.md)

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

[Esboço](stub.md)
</dt> </dl>

 

 




