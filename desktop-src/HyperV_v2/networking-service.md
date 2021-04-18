---
description: O perfil de rede descreve os objetos usados para configurar o sistema para permitir que as máquinas virtuais se comuniquem pela rede.
ms.assetid: A5C4866B-0F65-47B5-8FC4-B92943842B86
title: Serviço de rede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc85b7a5121a3e7e42f333f829816184b57bd8eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105778579"
---
# <a name="networking-service"></a>Serviço de rede

O perfil de rede descreve os objetos usados para configurar o sistema para permitir que as máquinas virtuais se comuniquem pela rede. Os objetos de rede global, usados para configurar o comutador de rede no sistema operacional de gerenciamento, incluem as classes [**Msvm \_ VirtualEthernetSwitchManagementService**](msvm-virtualethernetswitchmanagementservice.md), [**Msvm \_ VirtualEthernetSwitch**](msvm-virtualethernetswitch.md)e [**Msvm \_ EthernetSwitchPort**](msvm-ethernetswitchport.md) . Os objetos de rede da máquina virtual, usados para configurar a NIC (placa de interface de rede) na máquina virtual, incluem as classes [**Msvm \_ EmulatedEthernetPort**](msvm-emulatedethernetport.md), [**Msvm \_ ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md)e [**Msvm \_ LANEndpoint**](msvm-lanendpoint.md) .

A raiz do perfil de rede global é a classe [**Msvm \_ VirtualEthernetSwitch**](msvm-virtualethernetswitch.md) . Essa classe representa um dispositivo de comutador virtual no sistema operacional de gerenciamento. **Msvm \_ VirtualEthernetSwitch** é associado a instâncias da classe [**\_ switchport Msvm**](https://www.bing.com/search?q=**Msvm\_SwitchPort**) , que representa as portas no comutador virtual. As instâncias das classes **Msvm \_ VirtualEthernetSwitch** e [**Msvm \_ EthernetSwitchPort**](msvm-ethernetswitchport.md) são criadas, excluídas e conectadas por meio da classe Msvm [**\_ VirtualEthernetSwitchManagementService**](msvm-virtualethernetswitchmanagementservice.md) (não mostrada na ilustração anterior).

O serviço de gerenciamento de comutador virtual (VSMS) representa o serviço de rede presente em um único host Hyper-V e contém métodos para [**Msvm \_ VirtualEthernetSwitchManagementService**](msvm-virtualethernetswitchmanagementservice.md) usados para controlar a definição, modificação e destruição de recursos de rede global, como comutadores virtuais, portas de comutador e portas Ethernet internas.

A representação do dispositivo NIC Ethernet na máquina virtual parece muito semelhante à de qualquer outro dispositivo, conforme descrito no serviço de gerenciamento de [**sistema virtual**](virtual-system-management-service.md). As classes [**Msvm \_ EmulatedEthernetPort**](msvm-emulatedethernetport.md) e [**Msvm \_ SyntheticEthernetPort**](msvm-syntheticethernetport.md) representam o dispositivo NIC virtual e são configuradas por meio de uma [**instância Msvm ResourceAllocationSettingData (RASD \_**](msvm-resourceallocationsettingdata.md) ) associada. A única característica incomum dessa representação é que, quando a máquina virtual é instanciada e, por sua vez, cria os dispositivos **Msvm \_ EmulatedEthernetPort** e **Msvm \_ SyntheticEthernetPort** , ele também cria uma instância Msvm [**\_ LANEndpoint**](msvm-lanendpoint.md) associada para a NIC virtual. Da mesma forma, quando a máquina virtual é salva ou desativada e as instâncias **Msvm \_ EmulatedEthernetPort** e **Msvm \_ SyntheticEthernetPort** são destruídas, a instância Msvm [**\_ VmLANEndpoint**](https://www.bing.com/search?q=**Msvm\_VmLANEndpoint**) associada também é destruída. A finalidade do **Msvm \_ LANEndpoint** é servir como uma ponte para conectar duas portas de rede entre si. Nesse caso, ele é usado para conectar uma NIC virtual a uma porta no dispositivo do comutador virtual. Em outras palavras, ele conecta as instâncias **Msvm \_ EmulatedEthernetPort** e **Msvm \_ SyntheticEthernetPort** na máquina virtual a uma instância de [**Msvm \_ EthernetSwitchPort**](msvm-ethernetswitchport.md) específica no comutador virtual. Para conectar um comutador externo, você deve associar a porta Ethernet física ao [**Msvm \_ comutador virtual**](https://www.bing.com/search?q=**Msvm\_VirtualSwitch**) por meio de [**BindExternalEthernetPort**](https://www.bing.com/search?q=**BindExternalEthernetPort**). De forma adversa, ao conectar um comutador à pilha de rede do host, ou NIC interna, use ConnectInternal para que uma máquina virtual se comunique com o host e não com o mundo exterior. [**Msvm \_ O ActiveConnection**](msvm-activeconnection.md) conecta uma porta de comutador ao [**Msvm \_ SwitchLANEndpoint**](https://www.bing.com/search?q=**Msvm\_SwitchLANEndpoint**) ao qual a porta está conectada dentro do Hyper-V. A existência desse objeto significa que a porta do comutador e o **Msvm \_ SwitchLANEndpoint** estão ativamente conectados e a porta Ethernet associada ao **Msvm \_ LANEndpoint** pode se comunicar com a rede por meio da porta do comutador.

 

 



