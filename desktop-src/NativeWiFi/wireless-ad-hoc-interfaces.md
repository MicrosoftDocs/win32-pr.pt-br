---
description: A interface de programação ad hoc sem fio é composta pelas seguintes interfaces.
ms.assetid: 8e975750-cfcc-4e36-a3d1-539b7c077459
title: Interfaces ad hoc sem fio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcc4fe481a5be1ff428396e5fd9b199f5a291fbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105810301"
---
# <a name="wireless-ad-hoc-interfaces"></a>Interfaces ad hoc sem fio

A interface de programação ad hoc sem fio é composta pelas seguintes interfaces.



| Nome da Interface                                                                       | Descrição                                                                                            |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**IDot11AdHocInterface**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocinterface)                                 | Representa uma NIC (placa de interface de rede) sem fio.                                                    |
| [**IDot11AdHocInterfaceNotificationSink**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocinterfacenotificationsink) | Define as notificações com suporte pelo [**IDot11AdHocInterface**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocinterface).           |
| [**IDot11AdHocManager**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocmanager)                                     | Cria e gerencia redes ad hoc 802,11.                                                            |
| [**IDot11AdHocManagerNotificationSink**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocmanagernotificationsink)     | Define as notificações com suporte pela interface [**IDot11AdHocManager**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocmanager) . |
| [**IDot11AdHocNetwork**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocnetwork)                                     | Representa um destino de rede ad hoc disponível no intervalo de conexão.                            |
| [**IDot11AdHocNetworkNotificationSink**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocnetworknotificationsink)     | Define as notificações com suporte pela interface [**IDot11AdHocNetwork**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocnetwork) . |
| [**IDot11AdHocSecuritySettings**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocsecuritysettings)                   | Especifica as configurações de segurança para uma rede ad hoc sem fio.                                         |
| [**IEnumDot11AdHocInterfaces**](/windows/desktop/api/adhoc/nn-adhoc-ienumdot11adhocinterfaces)                       | Representa a coleção de interfaces de rede ad hoc 802,11 visíveis no momento.                       |
| [**IEnumDot11AdHocNetworks**](/windows/desktop/api/adhoc/nn-adhoc-ienumdot11adhocnetworks)                           | Representa a coleção de redes ad hoc 802,11 visíveis no momento.                                 |
| [**IEnumDot11AdHocSecuritySettings**](/windows/desktop/api/adhoc/nn-adhoc-ienumdot11adhocsecuritysettings)           | Representa a coleção de configurações de segurança associadas a cada rede ad hoc sem fio visível.   |



 

> [!Note]  
> O modo ad hoc pode não estar disponível em versões futuras do Windows. A partir do Windows 8.1 e do Windows Server 2012 R2, use [Wi-Fi Direct](about-the-wi-fi-direct-api.md) .

 

 

 



