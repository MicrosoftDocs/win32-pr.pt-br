---
title: Configurando Política de Grupo SNMP
description: Se você usar o snap-in do MMC (console de gerenciamento Microsoft) para Política de Grupo para administrar as configurações de política baseadas no registro que se aplicam ao SNMP, pode haver uma ou mais das seguintes subchaves.
ms.assetid: de21d2f5-3337-47ba-afcf-347e289873d3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e17bc3b1bac886a19791f57903920a11062072a81577a0a78ab01d461709ee3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009654"
---
# <a name="configuring-snmp-group-policy"></a>Configurando Política de Grupo SNMP

Se você usar o snap-in do MMC (console de gerenciamento Microsoft) para Política de Grupo para administrar as configurações de política baseadas no registro que se aplicam ao SNMP, pode haver uma ou mais das seguintes subchaves.

**HKEY \_ \_** \\  \\  \\  \\ **Parâmetros** SNMP de políticas \\  de software da máquina local ValidCommunities

**HKEY \_ \_** \\  \\  \\  \\ **Parâmetros** SNMP de políticas \\  de software da máquina local PermittedManagers

**HKEY \_ \_** \\  \\  \\  \\ **Parâmetros** SNMP de políticas \\  de software da máquina local TrapConfiguration

Normalmente, somente os membros do grupo local Administradores podem acessar as seguintes subchaves do registro que armazenam dados de configuração para o serviço SNMP:

**HKEY \_ Sistema de \_ máquina local** \\  \\ **CurrentControlSet** \\ **Serviços** \\ **SNMP** \\ **parâmetros** \\ **ValidCommunities**

**HKEY \_ Sistema de \_ máquina local** \\  \\ **CurrentControlSet** \\ **Serviços** \\ **SNMP** \\ **parâmetros** \\ **PermittedManagers**

Para obter mais informações sobre configurações de política baseadas no registro, consulte [about política de grupo](/previous-versions/windows/desktop/Policy/about-group-policy).

 

 