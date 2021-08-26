---
description: Um aplicativo de servidor COM+ pode ser criado como um serviço para ser iniciado automaticamente durante a inicialização do sistema ou manualmente por ativações.
ms.assetid: 56487746-328d-4435-af58-368aaa15b32a
title: Configurando um aplicativo de servidor do COM+ como um aplicativo de serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11ad6ec0af4ddf6d7ac7bf703209af2412e1ca4e128a942e7e1ecd089b69e278
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991186"
---
# <a name="configuring-a-com-server-application-as-a-service-application"></a>Configurando um aplicativo de servidor do COM+ como um aplicativo de serviço

Um aplicativo de servidor COM+ pode ser criado como um serviço para ser iniciado automaticamente durante a inicialização do sistema ou manualmente por ativações. Se o serviço não for iniciado, a opção de tratamento de erros especificará a severidade do erro e determinará a ação a ser executada. A opção de configurar um serviço para ser executado como a conta do sistema local também está disponível, bem como a opção de atribuir uma conta de usuário específica para a qual o aplicativo do servidor COM+ será executado. As dependências também podem ser selecionadas em uma lista de serviços registrados no computador usando os serviços de componentes. Isso determinará quais serviços devem ser executados antes que este serviço seja iniciado.

**Para configurar um aplicativo COM+ para ser executado como um serviço**

1.  Na árvore de console da ferramenta administrativa serviços de componentes, localize o aplicativo de servidor COM+ que você deseja executar como um serviço.

2.  Clique com o botão direito do mouse no aplicativo do servidor COM+ e clique em **Propriedades**.

3.  Na caixa de diálogo **Propriedades** , clique na guia **ativação** .

4.  Na caixa **tipo de ativação** , marque a caixa de seleção **Executar aplicativo como serviço NT** .

    > [!Note]  
    > A caixa de seleção **Executar aplicativo como serviço do NT** é habilitada somente para aplicativos de servidor e está desabilitada para aplicativos de biblioteca.

     

5.  Clique no botão **Configurar novo serviço** .

6.  Na caixa **tipo de inicialização** na caixa de diálogo **nome do serviço** , selecione **automático** ou **manual**.

7.  Adicional Para especificar a ação a ser tomada para um erro específico, selecione **ignorar**, **normal**, **grave** ou **crítico** na caixa **tratamento de erros** . O comportamento associado a cada opção é o seguinte:

    1.  **Ignorar**. O programa de inicialização registra o erro, mas continua a operação de inicialização.
    2.  **Normal**. O erro é registrado, uma caixa de mensagem é exibida e o programa de inicialização continua a operação de inicialização.
    3.  **Grave**. O erro é registrado e o sistema é reiniciado com a última configuração válida conhecida. Se for a última configuração válida que está sendo iniciada quando o erro for registrado, a operação de inicialização continuará.
    4.  **Crítica**. O erro é registrado e o sistema é reiniciado com a última configuração válida conhecida. Se for a última configuração válida que está sendo iniciada quando o erro for registrado, a operação de inicialização falhará.

8.  Adicional Para definir outros serviços como dependentes, selecione os serviços dependentes da lista na caixa **dependências** .

9.  Adicional Para indicar que o serviço deve ter permissão para interagir com a área de trabalho, marque a caixa de seleção **permitir que o serviço interaja com a área de trabalho** .

10. Clique em **Criar**.

11. Adicional Para atribuir o serviço a uma conta de usuário:

    1.  Na guia **identidade** , selecione **este usuário**.
    2.  Para selecionar o usuário, insira o nome de usuário na caixa **usuário** ou clique no botão **procurar** .
    3.  Digite a senha da conta de usuário na caixa **senha** .
    4.  Digite a mesma senha na caixa **Confirmar senha** .

 

 



