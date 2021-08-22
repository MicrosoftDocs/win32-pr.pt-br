---
description: A interface IUpdateInstaller define as propriedades a seguir.
ms.assetid: 876a2150-40a1-42a3-bc9a-05dec94fccd3
title: Propriedades de IUpdateInstaller
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49c6076e395e98ef21cd54fbf45ffdc5e57bc29fa8ceffc78c16d9a9a0d2bc4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049144"
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
| [**Actualiza**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_updates)                                                   | Obtém e define uma interface que contém uma coleção somente leitura das atualizações que são especificadas para instalação ou desinstalação. |



 

 

 



