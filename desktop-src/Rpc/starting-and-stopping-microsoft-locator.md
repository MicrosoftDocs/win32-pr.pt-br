---
title: Iniciando e parando o Microsoft Locator
description: As bibliotecas de tempo de execução RPC iniciam automaticamente o Microsoft Locator quando necessário. Você pode parar e iniciar o localizador manualmente se, por exemplo, precisar limpar o banco de dados durante a depuração de um aplicativo distribuído.
ms.assetid: 06b50a9f-b640-45b2-86e2-2bcea6c16c5c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 433ffdb11e86b06ee53d9b01f7f7755758538f22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004803"
---
# <a name="starting-and-stopping-microsoft-locator"></a>Iniciando e parando o Microsoft Locator

As bibliotecas de tempo de execução RPC iniciam automaticamente o Microsoft Locator quando necessário. Você pode parar e iniciar o localizador manualmente se, por exemplo, precisar limpar o banco de dados durante a depuração de um aplicativo distribuído.

**Para parar e iniciar o Microsoft Locator**

1.  No painel de controle, clique no ícone serviços.

    A caixa de diálogo **Serviços** é exibida.

2.  Na caixa de diálogo **serviço** , selecione **Microsoft Locator** e, em seguida, clique em **Iniciar** ou **parar**.

Você também pode iniciar e parar o localizador da Microsoft na linha de comando digitando:

**NET \[ Start/Stop \] RpcLocator**

Somente um administrador pode iniciar o Microsoft Locator quando ele for interrompido. Se for interrompido, ele será reiniciado conforme necessário pelas bibliotecas de tempo de execução RPC.

 

 




