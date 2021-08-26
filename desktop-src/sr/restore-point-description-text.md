---
title: Texto de descrição do ponto de restauração
description: Quando um aplicativo chama a função SRSetRestorePoint, ele pode fornecer qualquer texto como uma descrição para o ponto de restauração; no entanto, a tabela a seguir mostra o texto de descrição recomendado.
ms.assetid: e6e1974b-c162-4019-9349-936f3786cb9b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd785d143d3eed243e5d80ec261f121817db6187013f70b6f6cc6be0b1c2b790
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111245"
---
# <a name="restore-point-description-text"></a>Texto de descrição do ponto de restauração

Quando um aplicativo chama a [**função SRSetRestorePoint,**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) ele pode fornecer qualquer texto como uma descrição para o ponto de restauração; no entanto, a tabela a seguir mostra o texto de descrição recomendado.



| Modificação do sistema                            | Tipo de ponto de restauração      | Descrição            |
|------------------------------------------------|-------------------------|------------------------|
| Instalação do aplicativo                       | INSTALAÇÃO DO \_ APLICATIVO    | AppName *instalado*    |
| Modificação do aplicativo (adicionar/remover recursos) | MODIFICAR \_ CONFIGURAÇÕES        | AppName *configurado*   |
| Remoção do aplicativo                            | \_DESINSTALAÇÃO DE APLICATIVO  | AppName *removido*      |
| Instalação do driver de dispositivo                     | INSTALAÇÃO \_ DO DRIVER DE \_ DISPOSITIVO | DriverName *instalado* |



 

Instaladores, como Windows Instalador e InstallShield, usam estas convenções para o texto de descrição:

-   O nome do produto segue o verbo; por exemplo, Installed *AppName*.
-   O nome do produto pode ser usado sozinho (*AppName*) ou o nome do produto e o nome da empresa podem ser usados (*MyCompany AppName*).

 

 




