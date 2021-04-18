---
description: Tipos de aplicativos COM+
ms.assetid: 4b731f22-6837-4c03-9c8c-a76451369cf1
title: Tipos de aplicativos COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fb365863ee2b2fbe41997facdf21d84866af1f6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105800119"
---
# <a name="types-of-com-applications"></a>Tipos de aplicativos COM+

A seguir estão os quatro tipos básicos de aplicativos COM+:

-   **Aplicativos de servidor.** Um *aplicativo de servidor* com+ é executado em seu próprio processo. Os aplicativos de servidor podem dar suporte a todos os serviços COM+.
-   **Aplicativos de biblioteca.** Um *aplicativo de biblioteca* com+ é executado no processo do cliente que o cria. Mais especificamente, os componentes em um aplicativo de biblioteca sempre são carregados no processo do criador. Os aplicativos de biblioteca não são explicitamente associados a um processo de servidor. Eles podem usar a segurança baseada em função, mas não dão suporte a acesso remoto ou a componentes na fila.
-   **Proxies de aplicativo.** Um *proxy de aplicativo* é um conjunto de arquivos que contém informações de registro que permitem que um cliente acesse remotamente um aplicativo de servidor. Quando executado em um computador cliente, um arquivo de proxy de aplicativo grava informações sobre o aplicativo do servidor COM+, incluindo CLSIDs, ProgIDs, RemoteServerName e informações de marshaling, para o computador cliente. O aplicativo de servidor pode ser acessado remotamente do computador cliente.
-   **Aplicativos pré-instalados com+**. O COM+ inclui um conjunto de aplicativos pré-instalados que lidam com funções internas. Os aplicativos pré-instalados são listados na pasta aplicativos COM+ da ferramenta administrativa serviços de componentes, mas não podem ser modificados ou excluídos. Esses aplicativos incluem o seguinte:
    -   Utilitários .NET
    -   Aplicativo de editor de controle do Analyzer
    -   Gerenciador do COM+
    -   Ouvinte de fila de mensagens mortas do QC COM+
    -   Utilitários COM+
    -   Aplicativos de In-Process do IIS
    -   Aplicativos em pool fora do processo do IIS
    -   Aplicativo do sistema

## <a name="notes"></a>Observações

A partir do Windows Server 2003, é possível executar aplicativos COM+ mesmo se o aplicativo do sistema estiver desabilitado. Os aplicativos COM+ serão executados, porém sem os serviços geralmente fornecidos pelo aplicativo do sistema. Esses serviços incluem o uso da ferramenta administrativa serviços de componentes e do rastreamento de eventos do sistema.

Além do Windows Server 2003, o recurso de autenticação para o aplicativo de sistema COM+ inclui o valor EOAC \_ Disable \_ AAA. Esse valor, que desabilita as ativações de Activate-as-Activator (AAA), é usado com a função [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) ao iniciar o aplicativo do sistema. Definir o recurso de autenticação como EOAC \_ Disable \_ AAA permite que um aplicativo executado em uma conta com privilégios (como LocalSystem) ajude a impedir que sua identidade seja usada para iniciar componentes não confiáveis.

 

 
