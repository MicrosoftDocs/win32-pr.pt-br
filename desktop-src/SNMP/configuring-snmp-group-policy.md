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
# <a name="configuring-snmp-group-policy"></a><span data-ttu-id="3e3a6-103">Configurando Política de Grupo SNMP</span><span class="sxs-lookup"><span data-stu-id="3e3a6-103">Configuring SNMP Group Policy</span></span>

<span data-ttu-id="3e3a6-104">Se você usar o snap-in do MMC (console de gerenciamento Microsoft) para Política de Grupo para administrar as configurações de política baseadas no registro que se aplicam ao SNMP, pode haver uma ou mais das seguintes subchaves.</span><span class="sxs-lookup"><span data-stu-id="3e3a6-104">If you use the Microsoft Management Console (MMC) snap-in for Group Policy to administer registry-based policy settings that apply to SNMP, one or more of the following subkeys may exist.</span></span>

<span data-ttu-id="3e3a6-105">**HKEY \_ \_** \\  \\  \\  \\ **Parâmetros** SNMP de políticas \\  de software da máquina local ValidCommunities</span><span class="sxs-lookup"><span data-stu-id="3e3a6-105">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Policies**\\**SNMP**\\**Parameters**\\**ValidCommunities**</span></span>

<span data-ttu-id="3e3a6-106">**HKEY \_ \_** \\  \\  \\  \\ **Parâmetros** SNMP de políticas \\  de software da máquina local PermittedManagers</span><span class="sxs-lookup"><span data-stu-id="3e3a6-106">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Policies**\\**SNMP**\\**Parameters**\\**PermittedManagers**</span></span>

<span data-ttu-id="3e3a6-107">**HKEY \_ \_** \\  \\  \\  \\ **Parâmetros** SNMP de políticas \\  de software da máquina local TrapConfiguration</span><span class="sxs-lookup"><span data-stu-id="3e3a6-107">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Policies**\\**SNMP**\\**Parameters**\\**TrapConfiguration**</span></span>

<span data-ttu-id="3e3a6-108">Normalmente, somente os membros do grupo local Administradores podem acessar as seguintes subchaves do registro que armazenam dados de configuração para o serviço SNMP:</span><span class="sxs-lookup"><span data-stu-id="3e3a6-108">Typically, only members of the Administrators local group can access the following registry subkeys that store configuration data for the SNMP service:</span></span>

<span data-ttu-id="3e3a6-109">**HKEY \_ Sistema de \_ máquina local** \\  \\ **CurrentControlSet** \\ **Serviços** \\ **SNMP** \\ **parâmetros** \\ **ValidCommunities**</span><span class="sxs-lookup"><span data-stu-id="3e3a6-109">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**SNMP**\\**Parameters**\\**ValidCommunities**</span></span>

<span data-ttu-id="3e3a6-110">**HKEY \_ Sistema de \_ máquina local** \\  \\ **CurrentControlSet** \\ **Serviços** \\ **SNMP** \\ **parâmetros** \\ **PermittedManagers**</span><span class="sxs-lookup"><span data-stu-id="3e3a6-110">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**SNMP**\\**Parameters**\\**PermittedManagers**</span></span>

<span data-ttu-id="3e3a6-111">Para obter mais informações sobre configurações de política baseadas no registro, consulte [about política de grupo](/previous-versions/windows/desktop/Policy/about-group-policy).</span><span class="sxs-lookup"><span data-stu-id="3e3a6-111">For more information about registry-based policy settings, see [About Group Policy](/previous-versions/windows/desktop/Policy/about-group-policy).</span></span>

 

 