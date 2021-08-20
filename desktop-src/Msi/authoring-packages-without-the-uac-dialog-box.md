---
description: Quando privilégios elevados não são necessários para instalar um pacote do instalador do Windows, o autor do pacote pode suprimir a caixa de diálogo que o UAC (Controle de Conta de Usuário) exibe para solicitar autorização de administrador aos usuários.
ms.assetid: cab30f95-cc93-46db-aba5-741b44adb6de
title: Caixa de diálogo De autor de pacotes sem o UAC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5064589a49327db263158b10ff9377e0f7b69232b0e3679d5bd86c7bd2f2e3f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066086"
---
# <a name="authoring-packages-without-the-uac-dialog-box"></a>Caixa de diálogo De autor de pacotes sem o UAC

Quando privilégios elevados não são necessários para instalar um pacote do instalador do Windows, o autor do pacote pode suprimir a caixa de diálogo que o UAC [*(Controle*](u-gly.md) de Conta de Usuário) exibe para solicitar aos usuários a autorização do administrador.

Para suprimir a exibição da caixa de diálogo UAC ao instalar o aplicativo, o autor do pacote deve fazer o seguinte:

-   Instale o aplicativo usando o Window Installer 4.0 ou posterior no Windows Vista.
-   Não dependa do uso de privilégios elevados do sistema para instalar o aplicativo no computador.
-   Instale o aplicativo no contexto por usuário e faça com que esse seja o contexto de instalação padrão do pacote. Se a [**propriedade ALLUSERS**](allusers.md) não estiver definida, o instalador instalará o pacote no contexto por usuário. Se você não incluir a **propriedade ALLUSERS** na tabela [Property](property-table.md), o instalador não definirá essa propriedade e, portanto, a instalação por usuário se tornará o contexto de instalação padrão. Você pode substituir esse padrão definindo a **propriedade ALLUSERS** na linha de comando.
-   De definir Bit 3 na propriedade [**Resumo**](word-count-summary.md) da Contagem de Palavras para indicar que privilégios elevados não são necessários para instalar o aplicativo.

 

 



