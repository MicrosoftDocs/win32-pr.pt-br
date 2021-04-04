---
description: Quando privilégios elevados não são necessários para instalar um pacote de Windows Installer, o autor do pacote pode suprimir a caixa de diálogo que o UAC (controle de conta de usuário) exibe para solicitar aos usuários a autorização do administrador.
ms.assetid: cab30f95-cc93-46db-aba5-741b44adb6de
title: Criando pacotes sem a caixa de diálogo UAC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58dcd44bf7d2250e12e7cafde46b57978b48cceb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103662065"
---
# <a name="authoring-packages-without-the-uac-dialog-box"></a>Criando pacotes sem a caixa de diálogo UAC

Quando privilégios elevados não são necessários para instalar um pacote de Windows Installer, o autor do pacote pode suprimir a caixa de diálogo que o UAC ( [*controle de conta de usuário*](u-gly.md) ) exibe para solicitar aos usuários a autorização do administrador.

Para suprimir a exibição da caixa de diálogo do UAC ao instalar o aplicativo, o autor do pacote deve fazer o seguinte:

-   Instale o aplicativo usando o Window Installer 4,0 ou posterior no Windows Vista.
-   Não dependa do uso de privilégios de sistema elevados para instalar o aplicativo no computador.
-   Instale o aplicativo no contexto por usuário e torne esse o contexto de instalação padrão do pacote. Se a propriedade [**AllUsers**](allusers.md) não estiver definida, o instalador instalará o pacote no contexto por usuário. Se você não incluir a propriedade **AllUsers** na tabela de [Propriedades](property-table.md), o instalador não definirá essa propriedade e, portanto, a instalação por usuário se tornará o contexto de instalação padrão. Você pode substituir esse padrão definindo a propriedade **AllUsers** na linha de comando.
-   Defina o bit 3 na propriedade de [**Resumo contagem de palavras**](word-count-summary.md) para indicar que privilégios elevados não são necessários para instalar o aplicativo.

 

 



