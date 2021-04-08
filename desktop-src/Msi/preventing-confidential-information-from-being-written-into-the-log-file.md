---
description: Os desenvolvedores podem impedir que informações confidenciais, como senhas, sejam inseridas no arquivo de log durante uma instalação de Windows Installer.
ms.assetid: 950c3c56-3f16-4e1a-875f-d31f45065076
title: Impedir que informações confidenciais sejam gravadas no arquivo de log
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f17880f18ca08745ab1f4f764397e17b7af8827e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010900"
---
# <a name="preventing-confidential-information-from-being-written-into-the-log-file"></a>Impedir que informações confidenciais sejam gravadas no arquivo de log

Ao usar o Windows Installer, você pode impedir que informações confidenciais, por exemplo, senhas sejam inseridas no arquivo de log e fiquem visíveis.

-   O instalador nunca grava as informações na coluna senha da tabela de [instalação](serviceinstall-table.md) no log.
-   Você pode impedir que o instalador grave a propriedade associada a um controle de [edição](edit-control.md) no log definindo o [atributo de controle de senha](password-control-attribute.md). A propriedade associada a um controle de edição que tem o atributo de controle de senha ficará oculta, mesmo que a política de [depuração](debug.md) esteja definida com um valor de 7.
-   Você pode impedir que o instalador grave uma propriedade privada no log, incluindo a propriedade na propriedade [**MsiHiddenProperties**](msihiddenproperties.md) .
    > [!Note]  
    > Esse método pode tornar as informações confidenciais inseridas em uma linha de comando visíveis no log. Quando a política de [depuração](debug.md) for definida com um valor de 7, o instalador gravará as informações inseridas em uma linha de comando no log. Isso torna a propriedade inserida em uma linha de comando visível mesmo que a propriedade seja incluída na propriedade [**MsiHiddenProperties**](msihiddenproperties.md) .

     

-   Você pode impedir que as informações na coluna de destino da tabela [CustomAction](customaction-table.md) sejam gravadas no log, incluindo o sinalizador de bit HideTarget no campo Type da tabela CustomAction. O valor desse sinalizador é 8192 (0x2000). Para obter mais informações, consulte [opção personalizada de destino oculto](custom-action-hidden-target-option.md).

 

 



