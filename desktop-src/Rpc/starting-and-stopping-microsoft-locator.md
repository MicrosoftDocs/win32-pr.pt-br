---
title: Iniciando e parando o Microsoft Locator
description: As bibliotecas de tempo de execução RPC iniciam automaticamente o Microsoft Locator quando necessário. Você pode parar e iniciar o localizador manualmente se, por exemplo, precisar limpar o banco de dados durante a depuração de um aplicativo distribuído.
ms.assetid: 06b50a9f-b640-45b2-86e2-2bcea6c16c5c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e281419bc2a869d43863f946c1fcb172da2f86c04186ba775766233d4caa65c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120017546"
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

 

 




