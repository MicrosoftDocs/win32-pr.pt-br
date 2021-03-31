---
title: Usando canais autenticados seguros
description: Usando canais autenticados seguros
ms.assetid: ca4ab93c-0a3e-4fb5-be7f-a8f4eea3c9b7
keywords:
- Windows Media Gerenciador de Dispositivos, autenticação
- Gerenciador de Dispositivos, autenticação
- aplicativos de área de trabalho, autenticação
- provedores de serviços, autenticação
- Guia de programação, autenticação
- autenticação
- Windows Media Gerenciador de Dispositivos, comunicação segura
- Gerenciador de Dispositivos, comunicação segura
- aplicativos de área de trabalho, comunicação segura
- provedores de serviços, comunicação segura
- Guia de programação, comunicação segura
- comunicação segura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f88c271cecc2e9252a3f7af0540beef3dc57d2b9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005147"
---
# <a name="using-secure-authenticated-channels"></a>Usando canais autenticados seguros

O Windows Media Gerenciador de Dispositivos permite a autenticação e a comunicação segura entre os componentes, fornecendo duas classes auxiliares, [CSecureChannelClient](csecurechannelclient-class.md) (para aplicativos) e [CSecureChannelServer](csecurechannelserver-class.md) (para provedores de serviço) e uma interface, [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) (para ambos). Juntos, eles compõem uma API para o uso de canais autenticados seguros (SAC). O SAC lida com as três tarefas a seguir para provedores de serviços ou aplicativos usando o Windows Media Gerenciador de Dispositivos:

-   [Autenticação de componente](component-authentication.md)
-   [Criptografia e descriptografia](encryption-and-decryption.md)
-   [Autenticação de mensagens](message-authentication.md)

Um aplicativo ou provedor de serviços deve tratar da autenticação, criptografia e descriptografia de componentes; a autenticação de mensagens é opcional.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Tarefas comuns a aplicativos e provedores de serviços**](tasks-common-to-applications-and-service-providers.md)
</dt> </dl>

 

 




