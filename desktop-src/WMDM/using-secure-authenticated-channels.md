---
title: Usando canais autenticados seguros
description: Usando canais autenticados seguros
ms.assetid: ca4ab93c-0a3e-4fb5-be7f-a8f4eea3c9b7
keywords:
- Windows Mídia Gerenciador de Dispositivos, autenticação
- Gerenciador de Dispositivos, autenticação
- aplicativos da área de trabalho, autenticação
- provedores de serviços, autenticação
- guia de programação, autenticação
- autenticação
- Windows Mídia Gerenciador de Dispositivos, comunicação segura
- Gerenciador de Dispositivos, comunicação segura
- aplicativos da área de trabalho, comunicação segura
- provedores de serviços, comunicação segura
- guia de programação, comunicação segura
- comunicação segura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37a86eb364baca933eea1c81e587f99c9381786c5c3f62f2cefcfe3ceaed6e51
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124106"
---
# <a name="using-secure-authenticated-channels"></a>Usando canais autenticados seguros

Windows O Gerenciador de Dispositivos de mídia permite autenticação e comunicação segura entre componentes fornecendo duas classes auxiliares, [CSecureChannelClient](csecurechannelclient-class.md) (para aplicativos) e [CSecureChannelServer](csecurechannelserver-class.md) (para provedores de serviços) e uma [**interface, IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) (para ambos). Juntos, eles comem uma API para o uso de canais autenticados seguros (SAC). O SAC lida com as três tarefas a seguir para provedores de serviços ou aplicativos usando Windows mídia Gerenciador de Dispositivos:

-   [Autenticação de componente](component-authentication.md)
-   [Criptografia e descriptografia](encryption-and-decryption.md)
-   [Autenticação de mensagem](message-authentication.md)

Um aplicativo ou provedor de serviços deve lidar com autenticação, criptografia e descriptografia de componentes; A autenticação de mensagem é opcional.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Tarefas comuns a aplicativos e provedores de serviços**](tasks-common-to-applications-and-service-providers.md)
</dt> </dl>

 

 




