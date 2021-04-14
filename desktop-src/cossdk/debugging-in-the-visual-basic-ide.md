---
description: O uso do ambiente de desenvolvimento integrado (IDE) da Microsoft Visual Basic para depuração oferece Visual Basic aos desenvolvedores acesso a ferramentas familiares e à facilidade de uso.
ms.assetid: d31efc97-c286-434d-93f5-77b34ec16205
title: Depuração no IDE Visual Basic
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74574fdb289e1ad334337f17943c6961b95bf288
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370392"
---
# <a name="debugging-in-the-visual-basic-ide"></a>Depuração no IDE Visual Basic

O uso do ambiente de desenvolvimento integrado (IDE) da Microsoft Visual Basic para depuração oferece Visual Basic aos desenvolvedores acesso a ferramentas familiares e à facilidade de uso. Embora muitos componentes eventualmente precisem ser mais totalmente depurados usando o ambiente de Microsoft Visual C++, uma estratégia pode ser primeiro depurar o máximo de funcionalidade possível com Visual Basic. Por exemplo, talvez você queira usar o Visual Basic IDE para depuração no COM+ quando ainda não estiver Depurando vários threads, rastreamento de componentes, chamadas remotas ou isolamento de processo.

Em geral, ao usar o ambiente de Visual Basic para depuração, você primeiro compila o projeto e adiciona a DLL a um aplicativo COM+. Em seguida, defina a compatibilidade binária para o projeto, referenciando a DLL que você criou e inicie o projeto para iniciar a depuração.

## <a name="general-guidelines-for-debugging-in-the-visual-basic-environment"></a>Diretrizes gerais para depuração no ambiente de Visual Basic

-   Enquanto você estiver Depurando usando Visual Basic, o COM+ tratará os componentes de Visual Basic como se eles pertencessem a um aplicativo de biblioteca, mesmo se os componentes estiverem registrados como pertencentes a um aplicativo de servidor. Como ele é executado como um aplicativo de biblioteca, os ícones de componente na ferramenta administrativa serviços de componentes não giram conforme os componentes são depurados.
-   Se você alterar os atributos de transação em um componente durante a depuração ou fizer uma alteração de código-fonte que exija Visual Basic para gerar um novo CLSID ou ProgID, certifique-se de excluir e reinstalar o aplicativo COM+ que contém o componente. Se você tiver definido a compatibilidade binária para o componente, você será avisado de que as alterações ocorreram.

## <a name="notes-on-debugging-within-a-com-application"></a>Observações sobre depuração em um aplicativo COM+

-   Se você fizer alterações no Visual Basic IDE nas interfaces do componente, nomes de classe, nomes de projeto, suporte transacional ou outras configurações, poderá haver incompatibilidade entre os dados de configuração no Gerenciador de serviços de componentes e a configuração real em execução no depurador de Visual Basic.
-   Não exporte um aplicativo COM+ enquanto estiver depurando um componente no aplicativo. O COM+ tratará o ambiente de desenvolvimento de Visual Basic como o componente.
-   Se você estiver executando um componente fora do depurador e decidir iniciar a depuração, uma instância do componente ainda poderá estar em execução no COM+ quando você iniciá-lo no depurador. O COM+ detectará essa condição e tentará desligar silenciosamente a instância que ela controla. Para evitar esse problema, remova o componente da ferramenta administrativa serviços de componentes antes de começar a depuração.

**Para depurar usando o ambiente de Visual Basic**

1.  Abra o projeto de componente no Visual Basic.

2.  Compile seu componente e, em seguida, defina a compatibilidade binária em seu projeto para o componente compilado.

3.  Defina a propriedade MTSTransactionMode com um valor diferente de 0-NotAnMTSObject. Quando você inicia o projeto, essa configuração solicita Visual Basic para ativar o componente no COM+.

4.  No menu **projeto** , clique em **Propriedades** e, em seguida, insira o programa iniciar na guia **depuração** . O programa iniciar é o executável do cliente que chama esse componente.

    > [!Note]  
    > O programa de início deve ser local para o componente que você está depurando.

     

5.  Pressione a tecla F5 para iniciar a depuração do componente.

Depois de pressionar F5, Visual Basic iniciará o aplicativo cliente e executará o componente no modo de depuração. Você pode inserir pontos de interrupção no código do componente e definir inspeções em variáveis.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Suporte à depuração de Visual Basic COM+ em contraste com o MTS](com--visual-basic-debugging-support-contrasted-with-mts.md)
</dt> <dt>

[Depurando componentes de Visual Basic compilados](debugging-compiled-visual-basic-components.md)
</dt> </dl>

 

 



