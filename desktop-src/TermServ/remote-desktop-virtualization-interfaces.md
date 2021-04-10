---
title: Interfaces de virtualização Área de Trabalho Remota
description: A API de virtualização Área de Trabalho Remota dá suporte às seguintes interfaces.
ms.assetid: 150a3c9a-d504-4854-adaa-92e3a7e8ea70
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26674bfb4af3d858ed914ea48e210c7506d5f454
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294261"
---
# <a name="remote-desktop-virtualization-interfaces"></a>Interfaces de virtualização Área de Trabalho Remota

A API de virtualização Área de Trabalho Remota dá suporte às seguintes interfaces.

## <a name="in-this-section"></a>Nesta seção

<dl> <dt>

[**ITsSbBaseNotifySink**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbbasenotifysink)
</dt> <dd>

Expõe métodos que relatam status e mensagens de erro para Conexão de Área de Trabalho Remota Agente (agente de conexão RD).

</dd> <dt>

[**ITsSbClientConnection**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbclientconnection)
</dt> <dd>

Expõe métodos e propriedades que armazenam informações de estado sobre uma solicitação de conexão de entrada de um cliente Conexão de Área de Trabalho Remota (RDC).

</dd> <dt>

[**ITsSbClientConnectionPropertySet**](/windows/win32/api/sbtsv/nn-sbtsv-itssbclientconnectionpropertyset)
</dt> <dd>

Pode ser usado para definir propriedades personalizadas de uma conexão de cliente conforme apropriado.

</dd> <dt>

[**ITsSbEnvironment**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbenvironment)
</dt> <dd>

Expõe métodos e propriedades que contêm informações sobre o ambiente que hospeda o computador de destino. Essa interface pode ser usada para armazenar informações sobre um servidor físico que hospeda máquinas virtuais.

</dd> <dt>

[**ITsSbEnvironmentPropertySet**](/windows/win32/api/sbtsv/nn-sbtsv-itssbenvironmentpropertyset)
</dt> <dd>

Pode ser usado para definir propriedades personalizadas de um ambiente que hospeda computadores de destino conforme apropriado.

</dd> <dt>

[**ITsSbFilterPluginStore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbfilterpluginstore)
</dt> <dd>

Filtrar repositório de plug-in

</dd> <dt>

[**ITsSbGenericNotifySink**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbgenericnotifysink)
</dt> <dd>

Expõe métodos que relatam a conclusão e recebem o tempo de espera do agente de conexão de área de trabalho remota.

</dd> <dt>

[**ITsSbGlobalStore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbglobalstore)
</dt> <dd>

Expõe métodos que consultam computadores de destino, sessões, ambientes e farms que foram adicionados ao armazenamento do agente de conexão de área de trabalho remota.

</dd> <dt>

[**ITsSbLoadBalanceResult**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbloadbalanceresult)
</dt> <dd>

Expõe métodos e propriedades que armazenam o nome de destino retornado por um algoritmo de balanceamento de carga.

</dd> <dt>

[**ITsSbLoadBalancing**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbloadbalancing)
</dt> <dd>

Expõe métodos que você pode usar para fornecer um algoritmo de balanceamento de carga personalizado.

</dd> <dt>

[**ITsSbLoadBalancingNotifySink**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbloadbalancingnotifysink)
</dt> <dd>

Expõe métodos que retornam o resultado de um algoritmo de balanceamento de carga para o agente de conexão RD.

</dd> <dt>

[**ITsSbOrchestration**](/windows/desktop/api/sbtsv/nn-sbtsv-itssborchestration)
</dt> <dd>

Expõe os métodos que o agente de conexão RD usa para garantir que o destino esteja pronto antes que um cliente seja redirecionado para ele.

</dd> <dt>

[**ITsSbOrchestrationNotifySink**](/windows/desktop/api/sbtsv/nn-sbtsv-itssborchestrationnotifysink)
</dt> <dd>

Expõe métodos que retornam um objeto [**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget) para o agente de conexão RD depois que o destino é preparado com êxito para uma conexão.

</dd> <dt>

[**ITsSbPlacement**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbplacement)
</dt> <dd>

Expõe métodos que preparam o ambiente (o computador que hospeda a máquina virtual).

</dd> <dt>

[**ITsSbPlacementNotifySink**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbplacementnotifysink)
</dt> <dd>

Expõe métodos que retornam informações sobre ambientes para o agente de conexão RD.

</dd> <dt>

[**ITsSbPlugin**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbplugin)
</dt> <dd>

Expõe métodos que inicializam e encerram plug-ins.

</dd> <dt>

[**ITsSbPluginNotifySink**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbpluginnotifysink)
</dt> <dd>

Expõe métodos que notificam o agente de conexão RD sobre a inicialização ou o encerramento de um plug-in.

</dd> <dt>

[**ITsSbPluginPropertySet**](/windows/win32/api/sbtsv/nn-sbtsv-itssbpluginpropertyset)
</dt> <dd>

Pode ser usado para definir propriedades de plug-in personalizadas conforme apropriado.

</dd> <dt>

[**ITsSbPropertySet**](/windows/win32/api/sbtsv/nn-sbtsv-itssbpropertyset)
</dt> <dd>

Pode ser usado para definir propriedades personalizadas conforme apropriado.

</dd> <dt>

[**ITsSbProvider**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbprovider)
</dt> <dd>

Expõe métodos que criam implementações padrão de objetos que são usados na virtualização Área de Trabalho Remota.

</dd> <dt>

[**ITsSbProvisioning**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbprovisioning)
</dt> <dd>

Expõe métodos que criam e mantêm máquinas virtuais.

</dd> <dt>

[**ITsSbProvisioningPluginNotifySink**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbprovisioningpluginnotifysink)
</dt> <dd>

Expõe métodos que notificam o agente de conexão RD sobre o provisionamento de máquinas virtuais.

</dd> <dt>

[**ITsSbResourceNotification**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcenotification)
</dt> <dd>

Expõe os métodos que o agente de conexão RD usa para notificar os plug-ins de qualquer alteração de estado que ocorra nos objetos de conexão de sessão, destino e cliente.

</dd> <dt>

[**ITsSbResourceNotificationEx**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcenotificationex)
</dt> <dd>

Expõe os métodos que o agente de conexão RD usa para notificar os plug-ins de qualquer alteração de estado que ocorra nos objetos de conexão de sessão, destino e cliente.

</dd> <dt>

[**ITsSbResourcePlugin**](/windows/win32/api/sbtsv/nn-sbtsv-itssbresourceplugin)
</dt> <dd>

Expõe métodos que estendem os recursos do agente de conexão RD.

</dd> <dt>

[**ITsSbResourcePluginStore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore)
</dt> <dd>

Expõe métodos que permitem que os plug-ins de recursos armazenem objetos como sessões e destinos.

</dd> <dt>

[**ITsSbResourcePluginStoreEx**](itssbresourcepluginstoreex.md)
</dt> <dd>

Expõe métodos que permitem que os plug-ins de recursos armazenem objetos como sessões e destinos.

</dd> <dt>

[**ITsSbServiceNotification**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbservicenotification)
</dt> <dd>

Expõe os métodos que o agente de conexão RD usa para notificar os plug-ins de alterações de estado que ocorrem no próprio agente de conexão de área de trabalho remota.

</dd> <dt>

[**ITsSbSession**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbsession)
</dt> <dd>

Expõe propriedades que armazenam informações sobre uma sessão de usuário.

</dd> <dt>

[**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> <dd>

Expõe propriedades que armazenam informações de configuração e estado sobre um destino.

</dd> <dt>

[**ITsSbTargetEx**](itssbtargetex.md)
</dt> <dd>

Expõe propriedades que armazenam informações de configuração e estado sobre um destino.

</dd> <dt>

[**ITsSbTargetPropertySet**](/windows/win32/api/sbtsv/nn-sbtsv-itssbtargetpropertyset)
</dt> <dd>

Derive desta interface para definir um conjunto de propriedades de destino personalizado.

</dd> <dt>

[**ITsSbTaskInfo**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskinfo)
</dt> <dd>

Expõe as propriedades que o agente de Conexão de Área de Trabalho Remota usa para definir a fila de um plug-in.

</dd> <dt>

[**ITsSbTaskPlugin**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskplugin)
</dt> <dd>

Expõe métodos que atualizam a fila de tarefas para plug-ins do Conexão de Área de Trabalho Remota Broker.

</dd> <dt>

[**ITsSbTaskPluginNotifySink**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskpluginnotifysink)
</dt> <dd>

Expõe métodos que relatam status e mensagens de erro sobre tarefas para o agente de conexão RD.

</dd> <dt>

[**IWTSSBPlugin**](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin)
</dt> <dd>

Usado para estender os recursos do agente de sessão de serviços de terminal (agente de Sessão TS). Implemente essa interface quando desejar fornecer um plug-in que substitua a lógica de redirecionamento do agente de Sessão TS.

</dd> </dl>

 

 