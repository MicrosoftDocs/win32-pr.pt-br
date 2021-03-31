---
description: A interface IInstallationBehavior define as propriedades a seguir.
ms.assetid: abb8e247-44c4-491c-b8ea-9f32d7420c45
title: Propriedades de IInstallationBehavior
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 210f495c19c530a6507ffbd0584f647fc952ae46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920966"
---
# <a name="iinstallationbehavior-properties"></a>Propriedades de IInstallationBehavior

A interface [**IInstallationBehavior**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationbehavior) define as propriedades a seguir.



| Propriedade                                                                                 | Descrição                                                                                                                                                                    |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CanRequestUserInput**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationbehavior-get_canrequestuserinput)                 | Obtém um valor booliano thast indica se a instalação ou desinstalação de uma atualização pode solicitar entrada do usuário.                                                        |
| [**Impacto**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationbehavior-get_impact)                                           | Obtém uma enumeração [**InstallationImpact**](/windows/win32/api/wuapi/ne-wuapi-installationimpact) que indica como a instalação ou desinstalação da atualização afeta o computador.                 |
| [**RebootBehavior**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationbehavior-get_rebootbehavior)                           | Obtém uma enumeração [**InstallationRebootBehavior**](/windows/win32/api/wuapi/ne-wuapi-installationrebootbehavior) que especifica o comportamento de reinicialização que ocorre quando você instala ou desinstala a atualização. |
| [**RequiresNetworkConnectivity**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationbehavior-get_requiresnetworkconnectivity) | Obtém um valor booliano que indica se a instalação ou desinstalação de uma atualização requer conectividade de rede.                                                     |



 

 

 



