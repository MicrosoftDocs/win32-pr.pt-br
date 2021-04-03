---
title: API do provedor de protocolo RDP
description: Você usa a API do provedor de protocolo RDP para criar um protocolo para fornecer comunicação entre o serviço de Serviços de Área de Trabalho Remota e vários clientes.
ms.assetid: dd14c569-195e-460e-a1c3-2a74d0f49ff5
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95aed1c6866f3078c3761ad8ec631ef23b43a9ae
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103915861"
---
# <a name="remote-desktop-protocol-provider-api"></a>API do provedor de protocolo RDP

Você usa a API do provedor de protocolo RDP para criar um protocolo para fornecer comunicação entre o serviço de Serviços de Área de Trabalho Remota e vários clientes.

Quando o Windows Server é carregado, o serviço de Serviços de Área de Trabalho Remota (também conhecido como Gerenciador de conexões remotas (RCM) é iniciado. O serviço também inicia objetos de escuta para os provedores de protocolo RDP que, por sua vez, escutam conexões de cliente. O serviço e os provedores de protocolo são objetos de modo de usuário que se comunicam usando as APIs discutidas nesta documentação. Os provedores de protocolo podem se comunicar com drivers de modo kernel usando controles de entrada/saída (IOCTLs). Isso é mostrado na ilustração a seguir.

![arquitetura de API de protocolo personalizado](images/protocol-architecture.png)

A Microsoft implementou o protocolo RDP (RDP) para fornecer comunicação entre o serviço Serviços de Área de Trabalho Remota e as conexões de cliente. Você pode criar seu próprio protocolo usando as interfaces, estruturas, uniões e tipos de enumeração que compõem a API do provedor de protocolo RDP. Para obter mais informações, consulte os tópicos a seguir.

<dl> <dt>

[Criando um provedor de protocolo RDP](creating-a-custom-remote-protocol.md)
</dt> <dd>

Informações sobre como criar um provedor de protocolo RDP. O Gerenciador de protocolo é implementado como um servidor COM e registrado em um local pesquisado quando o serviço de Serviços de Área de Trabalho Remota é iniciado.

</dd> <dt>

[Referência do provedor de protocolo RDP](custom-remote-protocol-reference.md)
</dt> <dd>

Contém interfaces, estruturas, uniões e tipos de enumeração que permitem que você crie um protocolo RDP personalizado (RDP).

</dd> </dl>

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre Serviços de Área de Trabalho Remota](about-terminal-services.md)
</dt> </dl>

 

 




