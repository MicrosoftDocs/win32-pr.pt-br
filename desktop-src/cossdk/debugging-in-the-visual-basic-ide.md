---
description: Usar o Microsoft Visual Basic IDE (ambiente de desenvolvimento integrado) para Visual Basic depuração fornece aos desenvolvedores acesso a ferramentas conhecidas e facilidade de uso.
ms.assetid: d31efc97-c286-434d-93f5-77b34ec16205
title: Depuração no Visual Basic IDE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 284e97a766256cd281b3515bdd142d15ff5208e2c1a1555438c428daeca8f3a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118548005"
---
# <a name="debugging-in-the-visual-basic-ide"></a>Depuração no Visual Basic IDE

Usar o Microsoft Visual Basic IDE (ambiente de desenvolvimento integrado) para Visual Basic depuração fornece aos desenvolvedores acesso a ferramentas conhecidas e facilidade de uso. Embora muitos componentes eventualmente precisem ser mais totalmente depurados usando o ambiente Microsoft Visual C++, uma estratégia pode ser depurar primeiro o máximo de funcionalidade possível com Visual Basic. Por exemplo, talvez você queira usar o IDE do Visual Basic para depuração no COM+ quando ainda não estiver depurando multithreading, acompanhamento de componentes, chamadas remotas ou isolamento de processo.

Em geral, ao usar o ambiente Visual Basic para depuração, primeiro você compila o projeto e adiciona a DLL a um aplicativo COM+. Em seguida, defina a compatibilidade binária para o projeto, referenciando a DLL que você fez e inicie o projeto para iniciar a depuração.

## <a name="general-guidelines-for-debugging-in-the-visual-basic-environment"></a>Diretrizes gerais para depuração no Visual Basic ambiente

-   Enquanto você está depurando usando Visual Basic, o COM+ trata os componentes Visual Basic como se pertencesse a um aplicativo de biblioteca, mesmo que os componentes sejam registrados como pertencentes a um aplicativo de servidor. Como ele é executado como um aplicativo de biblioteca, os ícones de componente na ferramenta administrativa dos Serviços de Componentes não giram conforme os componentes são depurados.
-   Se você alterar atributos de transação em um componente durante a depuração ou fizer uma alteração de código-fonte que exija que o Visual Basic gere um novo CLSID ou ProgID, exclua e reinstale o aplicativo COM+ que contém o componente. Se você tiver definido a compatibilidade binária para o componente, será avisado de que ocorreram alterações.

## <a name="notes-on-debugging-within-a-com-application"></a>Observações sobre a depuração em um aplicativo COM+

-   Se você fizer alterações no IDE do Visual Basic nas interfaces do componente, nomes de classe, nomes de projeto, suporte transacional ou outras configurações, poderá haver incompatibilidades entre os dados de configuração no explorador de Serviços de Componentes e a configuração real em execução no depurador Visual Basic.
-   Não exporte um aplicativo COM+ enquanto estiver depurando um componente no aplicativo. O COM+ tratará o Visual Basic de desenvolvimento como o componente.
-   Se você estiver executando um componente fora do depurador e, em seguida, decidir iniciar a depuração, uma instância do componente ainda poderá estar em execução no COM+ quando você a iniciar no depurador. O COM+ detectará essa condição e tentará desligar silenciosamente a instância que controla. Para evitar esse problema, remova o componente da ferramenta administrativa serviços de componentes antes de começar a depuração.

**Para depurar usando o Visual Basic ambiente**

1.  Abra o projeto de componente Visual Basic.

2.  Compile seu componente e depure a compatibilidade binária em seu projeto para o componente compilado.

3.  De definir a propriedade MTSTransactionMode como um valor diferente de 0 – NotAnMTSObject. Quando você inicia o projeto, essa configuração solicita Visual Basic ativar o componente no COM+.

4.  No menu **Project,** clique em **Propriedades** e, em seguida, insira o programa iniciar na **guia Depuração.** O programa inicial é o executável do cliente que chama esse componente.

    > [!Note]  
    > O programa inicial deve ser local para o componente que você está depurando.

     

5.  Pressione a tecla F5 para começar a depurar o componente.

Depois de pressionar F5, Visual Basic o aplicativo cliente e executa o componente no modo de depuração. Você pode colocar pontos de interrupção no código do componente e definir inspeçãos em variáveis.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Suporte à depuração de Visual Basic COM+ contrastado com o MTS](com--visual-basic-debugging-support-contrasted-with-mts.md)
</dt> <dt>

[Depurando componentes Visual Basic compilados](debugging-compiled-visual-basic-components.md)
</dt> </dl>

 

 



