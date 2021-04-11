---
title: Texto de descrição do ponto de restauração
description: Quando um aplicativo chama a função SRSetRestorePoint, ele pode fornecer qualquer texto como uma descrição para o ponto de restauração; no entanto, a tabela a seguir mostra o texto de descrição recomendado.
ms.assetid: e6e1974b-c162-4019-9349-936f3786cb9b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59e90fd1b7d5776c8c3798a68946382cc702b3bd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159915"
---
# <a name="restore-point-description-text"></a>Texto de descrição do ponto de restauração

Quando um aplicativo chama a função [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) , ele pode fornecer qualquer texto como uma descrição para o ponto de restauração; no entanto, a tabela a seguir mostra o texto de descrição recomendado.



| Modificação do sistema                            | Tipo de ponto de restauração      | Descrição            |
|------------------------------------------------|-------------------------|------------------------|
| Instalação do aplicativo                       | instalação do aplicativo \_    | *AppName* instalado    |
| Modificação do aplicativo (Adicionar/remover recursos) | MODIFICAR \_ configurações        | *AppName* configurado   |
| Remoção do aplicativo                            | desinstalação do aplicativo \_  | *AppName* removido      |
| Instalação do driver de dispositivo                     | \_instalação do driver de dispositivo \_ | *DriverName* instalado |



 

Instaladores, como o Windows Installer e o InstallShield, usam essas convenções para o texto de descrição:

-   O nome do produto segue o verbo; por exemplo, o *AppName* foi instalado.
-   O nome do produto pode ser usado sozinha (*AppName*) ou o nome do produto e o nome da empresa pode ser usado (*MyCompany AppName*).

 

 




