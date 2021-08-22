---
title: Criando um Project de exemplo
description: Criando um Project de exemplo
ms.assetid: 9cbbd1a7-88e7-4947-8dca-e06e364102f7
keywords:
- Windows Media Player lojas online, criando projetos de exemplo
- lojas online, criando projetos de exemplo
- Digite 2 lojas online, criando projetos de exemplo
- Windows Media Player lojas online, projetos de exemplo
- lojas online, projetos de exemplo
- Digite 2 lojas online, projetos de exemplo
- Windows Media Player lojas online, assistente de projeto
- lojas online, assistente de projeto
- tipo 2 lojas online, assistente de projeto
- plug-ins, assistente de projeto
- plug-ins Windows Media Player, assistente de projeto
- Criando projetos de exemplo
- exemplos, tipo 2 lojas online
- Assistente de projeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b58af81123e257a7f71ad4be00e44c671f8ca3fa6f61b3719cd02ae1f928b7ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118579932"
---
# <a name="creating-a-sample-project"></a>Criando um Project de exemplo

Para criar um novo projeto usando o assistente de projeto, siga estas etapas:

1.  Abra o Microsoft Visual Studio.
2.  No menu **Arquivo**, aponte para **Novo** e clique em **Projeto**.
3.  na caixa de listagem **tipos de Project** , escolha **Visual C++ projetos**.
4.  na caixa de listagem **modelos** , escolha **Windows Media Player assistente de lojas Online**.
5.  Digite um nome e um local para o seu projeto.
6.  Clique em **OK** para iniciar o assistente de projeto.
7.  Selecione **tipo 2 (integração básica)** e clique em **Avançar**.
8.  Digite o nome amigável e a ID do distribuidor de conteúdo para seu serviço. Digite a URL da página da Web que remove o serviço do computador do usuário.
    > [!Note]  
    > O valor que você fornece para a ID do distribuidor de conteúdo não deve conter espaços. O assistente remove todos os espaços da cadeia de caracteres que você fornecer.

     

9.  Clique em **Concluir** para criar o projeto.

O assistente gera automaticamente um novo projeto C++ que cria um plug-in de loja online tipo 2 que implementa as interfaces **IWMPSubscriptionService** e **IWMPSubscriptionService2** . Cada vez que você executa o assistente, ele cria o mesmo projeto, mas o componente que é criado quando você compila o projeto tem uma ID de classe exclusiva. O nome do projeto, o nome amigável e a ID do distribuidor de conteúdo também podem ser diferentes dependendo dos valores que você forneceu quando executou o assistente. O projeto de exemplo registra o componente usando um nome de chave que corresponde ao valor fornecido para o nome amigável.

O exemplo usa o código Active Template Library (ATL) para fornecer implementações COM.

O assistente cria os seguintes arquivos para você:

-   *ProjectName* dll. cpp. Implementa as exportações da biblioteca de vínculo dinâmico (DLL), como a função principal do ponto de entrada da DLL. Também contém o mapa do objeto ATL e a declaração do módulo.
-   *ProjectName*. cpp. Contém implementações padrão para os métodos das interfaces IWMPSubscriptionService e IWMPSubscriptionService2. Também contém o código para definir as caixas de diálogo que o exemplo abre quando os métodos são chamados por Windows Media Player.
-   *ProjectName*. def. Declara as exportações de DLL.
-   StdAfx. cpp. Inclui cabeçalhos padrão.
-   WMP. h. o arquivo de cabeçalho Windows Media Player.
-   wmpplug. h. o arquivo de cabeçalho de plug-in Windows Media Player.
-   subscriptionservices. h. o Windows Media Player online armazena o arquivo de cabeçalho.
-   Resource. h. Contém definições de recurso.
-   **ProjectName**. h. Contém definições de classe para o objeto de loja online e as caixas de diálogo. Define a ID de classe do objeto e a constante de ID do distribuidor de conteúdo.
-   StdAfx. h. Contém inclusões de sistema padrão.
-   *ProjectName*. rc. O arquivo de script do recurso. Ele contém definições para os recursos e controles da caixa de diálogo. Isso também é onde a tabela de cadeia de caracteres é armazenada. A tabela de cadeia de caracteres contém o nome do projeto e constantes de cadeia de caracteres de nome amigável. normalmente, você trabalha com esse arquivo no editor de recursos Visual Studio, não como texto sem formatação.
-   *ProjectName*. rgs. O arquivo de script do registro. esse arquivo contém as informações usadas para adicionar a classe de componente ao registro para que Windows Media Player possa localizá-la. Você pode alterar o nome da chave para o serviço neste arquivo.

> [!Note]  
> Você deve definir o endereço base para sua DLL como 0x0F100000 para evitar conflitos com Windows Media Player.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Criando o plug-in para uma loja online tipo 2**](building-the-plug-in-for-a-type-2-online-store.md)
</dt> <dt>

[**Interface IWMPSubscriptionService**](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice)
</dt> <dt>

[**Interface IWMPSubscriptionService2**](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice2)
</dt> </dl>

 

 




