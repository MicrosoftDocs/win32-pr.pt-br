---
description: A interface IInstallationJob define as propriedades a seguir.
ms.assetid: 74087098-bef0-41f8-8d7b-bbca1d000df8
title: Propriedades de IInstallationJob
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81b0083acd90b174349c105525676741c762aa05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647298"
---
# <a name="iinstallationjob-properties"></a>Propriedades de IInstallationJob

A interface [**IInstallationJob**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationjob) define as propriedades a seguir.



| Propriedade                                            | Descrição                                                                                                                                                                                                                            |
|-----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AsyncState**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-get_asyncstate)   | Obtém o objeto de estado específico do chamador que é passado para o método [**IUpdateInstaller. BeginInstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-begininstall) ou [**IUpdateInstaller. BeginUninstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-beginuninstall) .               |
| [**IsCompleted**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-get_iscompleted) | Obtém um valor que indica se uma chamada para o método [**IUpdateInstaller. BeginInstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-begininstall) ou [**IUpdateInstaller. BeginUninstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-beginuninstall) é completamente processada. |
| [**Atualizações**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-get_updates)         | Obtém uma interface que contém uma coleção somente leitura das atualizações que são especificadas na instalação ou desinstalação.                                                                                                        |



 

 

 



