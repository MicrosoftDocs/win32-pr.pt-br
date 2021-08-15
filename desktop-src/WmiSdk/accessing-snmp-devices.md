---
description: Permite que os aplicativos cliente acessem informações de SNMP por meio do WMI.
ms.assetid: d9e3fd1d-8320-4407-9a9e-e2eb5dd62fef
ms.tgt_platform: multiple
title: Acessando dispositivos SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3acf8fd67ee9153167cd328b7a50f6aafc5853327a64baf80c3b2e20b663d3ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118320298"
---
# <a name="accessing-snmp-devices"></a>Acessando dispositivos SNMP

O provedor SNMP (Simple Network Management Protocol) permite que aplicativos cliente acessem informações de SNMP por meio do WMI. O [provedor SNMP](snmp-provider.md) atua como um gateway para sistemas e dispositivos que usam SNMP para gerenciamento. Somente o computador de gerenciamento ou de monitoramento deve estar executando o WMI porque ele pode ler de qualquer dispositivo habilitado para SNMP.

> [!Note]  
> Para obter mais informações sobre como instalar o provedor, consulte [Configurando o ambiente SNMP WMI](setting-up-the-wmi-snmp-environment.md).

 

As variáveis de objeto de MIB (base de informações de gerenciamento) SNMP podem ser lidas e gravadas, e as interceptações SNMP podem ser mapeadas automaticamente para eventos WMI, que podem ser definidas para operações de criação, exclusão ou atualização arbitrárias para dados além das interceptações definidas pela MIB. Esse recurso do WMI funciona como uma extensão dos recursos SNMP padrão. Para obter mais informações, consulte [monitorando eventos](monitoring-events.md).

as ferramentas descritas nos tópicos a seguir foram projetadas para uso por Windows scripts e programadores C/C++. Recomendamos a familiaridade com o WMI, o SNMPv1 e o SNMPv2C e o conhecimento prático sobre conceitos de rede e de gerenciamento de rede.

Para obter mais informações sobre como usar o WMI com SNMP, consulte [Configurando o ambiente SNMP WMI](setting-up-the-wmi-snmp-environment.md).

 

 



