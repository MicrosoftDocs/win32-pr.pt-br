---
description: Quando o Windows Installer processa o script de instalação para a instalação de um produto ou aplicativo, ele gera simultaneamente um script de reversão e salva uma cópia de todos os arquivos excluídos durante a instalação.
ms.assetid: 6c70e788-beb0-46db-94b0-1bbaac972acf
title: Reverter instalação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc958c7d5e1dead2cd3e3e0b6081e7c71cd9af7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091129"
---
# <a name="rollback-installation"></a>Reverter instalação

Quando o Windows Installer processa o script de instalação para a instalação de um produto ou aplicativo, ele gera simultaneamente um script de reversão e salva uma cópia de todos os arquivos excluídos durante a instalação. Esses arquivos são mantidos em um diretório de sistema oculto e são excluídos automaticamente quando a instalação é concluída com êxito. Se, no entanto, a instalação não for bem-sucedida, o instalador executará automaticamente uma reversão da instalação que retorna o sistema ao seu estado original.

A reversão automática de uma instalação malsucedida é o comportamento padrão do instalador. Para desabilitar a reversão durante uma instalação, use um dos seguintes:

-   [**Propriedade DISABLEROLLBACK**](-disablerollback.md)
-   [**Propriedade PROMPTROLLBACKCOST**](promptrollbackcost.md)
-   [Ação DisableRollback](disablerollback-action.md)
-   [DisableRollback](disablerollback.md)
-   [EnableRollback ControlEvent,](enablerollback-controlevent.md)

Sempre que a reversão é desabilitada, o instalador define a propriedade [**RollbackDisabled**](rollbackdisabled.md) .

Se uma instalação usar [ações personalizadas](custom-actions.md), será necessária a criação adicional do pacote de instalação para usar a funcionalidade de reversão. Para obter mais informações, consulte [Rollback Custom Actions](rollback-custom-actions.md).

 

 



