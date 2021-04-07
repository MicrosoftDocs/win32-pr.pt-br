---
description: A interface IUpdateInstaller define as propriedades a seguir.
ms.assetid: 876a2150-40a1-42a3-bc9a-05dec94fccd3
title: Propriedades de IUpdateInstaller
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77df235c49e7b6f27b0f93ec3b0c4def12135065
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827227"
---
# <a name="iupdateinstaller-properties"></a>Propriedades de IUpdateInstaller

A interface [**IUpdateInstaller**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstaller) define as propriedades a seguir.



| Propriedade                                                                                      | Descrição                                                                                                                           |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**AllowSourcePrompts**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_allowsourceprompts)                             | Obtém e define um valor booliano que indica se os prompts de origem devem ser mostrados ao usuário ao instalar as atualizações.                  |
| [**ClientApplicationID**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_clientapplicationid)                           | Obtém e define o aplicativo cliente atual.                                                                                         |
| [**IsBusy**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_isbusy)                                                     | Obtém um valor booliano que indica se uma instalação ou desinstalação está em andamento em um computador em um momento específico.        |
| [**Isforced**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_isforced)                                                 | Obtém ou define um valor booliano que indica se uma atualização deve ser forçada ou desinstalada.                                       |
| [**ParentHwnd**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_parenthwnd)                                             | Obtém e define um identificador para a janela pai que pode conter uma caixa de diálogo.                                                            |
| [**ParentWindow**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_parentwindow)                                         | Obtém e define a interface que representa a janela pai que pode conter uma caixa de diálogo.                                          |
| [**RebootRequiredBeforeInstallation**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_rebootrequiredbeforeinstallation) | Obtém um valor booliano que indica se uma reinicialização do sistema é necessária antes de instalar ou desinstalar atualizações.                   |
| [**Atualizações**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_updates)                                                   | Obtém e define uma interface que contém uma coleção somente leitura das atualizações que são especificadas para instalação ou desinstalação. |



 

 

 



