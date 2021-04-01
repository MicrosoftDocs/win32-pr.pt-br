---
title: Configurando Política de Grupo SNMP
description: Se você usar o snap-in do MMC (console de gerenciamento Microsoft) para Política de Grupo para administrar as configurações de política baseadas no registro que se aplicam ao SNMP, pode haver uma ou mais das seguintes subchaves.
ms.assetid: de21d2f5-3337-47ba-afcf-347e289873d3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 817797dbc0e67f6006e12751beca533cbbec3656
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084780"
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

 

 