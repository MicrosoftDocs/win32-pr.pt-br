---
title: Interfaces do provedor de protocolo RDP
description: Interfaces com suporte da API do provedor de protocolo RDP.
ms.assetid: 180c29d4-a305-45ac-8989-6226dccb75d5
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bde36cb70f937559dce20a73a485ec109a2cf6c6ae6c687655963c70e6ce22b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681226"
---
# <a name="remote-desktop-protocol-provider-interfaces"></a>Interfaces do provedor de protocolo RDP

As interfaces a seguir têm suporte da API do provedor de protocolo RDP.

## <a name="in-this-section"></a>Nesta seção

<dl> <dt>

[**IWRdsProtocolConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnection)
</dt> <dd>

Expõe métodos chamados pelo serviço de Serviços de Área de Trabalho Remota para configurar uma conexão de cliente.

</dd> <dt>

[**IWRdsProtocolConnectionCallback**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnectioncallback)
</dt> <dd>

Expõe métodos que fornecem informações sobre o status de uma conexão de cliente e que executam ações para o cliente. Essa interface é implementada pelo serviço de Serviços de Área de Trabalho Remota e chamada pelo protocolo.

</dd> <dt>

[**IWRdsProtocolLicenseConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollicenseconnection)
</dt> <dd>

Expõe métodos usados pelo serviço de Serviços de Área de Trabalho Remota para executar o handshake de licenciamento durante uma sequência de conexão.

</dd> <dt>

[**IWRdsProtocolListener**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistener)
</dt> <dd>

Expõe métodos que solicitam que o protocolo inicie e pare de escutar solicitações de conexão de cliente.

</dd> <dt>

[**IWRdsProtocolListenerCallback**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistenercallback)
</dt> <dd>

Expõe métodos que notificam o serviço de Serviços de Área de Trabalho Remota que um cliente conectou.

</dd> <dt>

[**IWRdsProtocolLogonErrorRedirector**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollogonerrorredirector)
</dt> <dd>

Expõe métodos chamados pelo serviço de Serviços de Área de Trabalho Remota para atualizar o status de logon e determinar como direcionar mensagens de erro de logon.

</dd> <dt>

[**IWRdsProtocolManager**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolmanager)
</dt> <dd>

Expõe métodos que o serviço Serviços de Área de Trabalho Remota usa para se comunicar com o provedor de protocolo.

</dd> <dt>

[**IWRdsProtocolSettings**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolsettings)
</dt> <dd>

Expõe métodos para recuperar e adicionar configurações relacionadas à política.

</dd> <dt>

[**IWRdsProtocolShadowCallback**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolshadowcallback)
</dt> <dd>

Expõe métodos chamados pelo protocolo para notificar o serviço de Serviços de Área de Trabalho Remota para iniciar ou parar o lado de destino de uma sombra.

</dd> <dt>

[**IWRdsProtocolShadowConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolshadowconnection)
</dt> <dd>

Expõe métodos que notificam o provedor de protocolo sobre o status de sombra da sessão.

</dd> <dt>

[**IWRdsRemoteFXGraphicsConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsremotefxgraphicsconnection)
</dt> <dd>

Expõe métodos relacionados à manipulação e à compreensão de elementos gráficos na conexão do cliente.

</dd> <dt>

[Interfaces do provedor de protocolo de desktop preteridas](deprecated-desktop-protocol-provider-interfaces.md)
</dt> <dd>

As interfaces a seguir foram preteridas e não devem mais ser usadas. Para novos projetos, use as interfaces de interfaces de provedor de protocolo RDP em vez disso.

</dd> </dl>

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência do provedor de protocolo RDP](custom-remote-protocol-reference.md)
</dt> <dt>

[Enumerações de provedor de protocolo RDP](custom-remote-protocol-enumerations.md)
</dt> <dt>

[Estruturas de provedor de protocolo RDP](custom-remote-protocol-structures.md)
</dt> <dt>

[Uniões de provedor de protocolo RDP](custom-remote-protocol-unions.md)
</dt> </dl>

 

 




