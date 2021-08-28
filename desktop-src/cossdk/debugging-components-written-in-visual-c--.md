---
description: Quando estiver pronto para depurar a funcionalidade COM+ em seus componentes do Microsoft Visual C++, você poderá configurar um projeto Visual C++ ou a ferramenta administrativa dos Serviços de Componentes para iniciar o depurador.
ms.assetid: 206467ac-108a-49de-a884-66959dc77650
title: Componentes de depuração gravados Visual C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d90bcb1b38fd2a1fb48d123c912de53e037c5aa059f40984cdf4a13f991b1d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117916845"
---
# <a name="debugging-components-written-in-visual-c"></a>Componentes de depuração gravados Visual C++

Quando estiver pronto para depurar a funcionalidade COM+ em seus componentes do Microsoft Visual C++, você poderá configurar um projeto Visual C++ ou a ferramenta administrativa dos Serviços de Componentes para iniciar o depurador. Se você estiver usando Visual C++, poderá depurar com um cliente remoto usando o OLE RPC e a depuração JIT (Just-In-Time). Se não for possível executar seu cliente no depurador ou se o cliente estiver em execução em outro computador, você poderá usar a configuração Iniciar com+ no **depurador.** Você encontrará isso na ferramenta administrativa serviços de  componentes como uma caixa de seleção na guia Avançado da caixa de diálogo Propriedades **do** aplicativo COM+.

Quando terminar a depuração, você deverá desligar os aplicativos COM+ que está depurando. Se um processo de servidor for deixado em execução, você poderá receber uma mensagem de erro na próxima vez que tentar criar uma DLL quando a DLL existente ainda estiver carregada na memória. Para desligar um aplicativo COM+, clique com o botão direito do mouse no aplicativo na árvore de console e clique **em Desligar**.

> [!Note]  
> Se você estiver usando transações, talvez também queira aumentar o tempo de tempo de transação, que assume como padrão 60 segundos. Você também pode especificar um valor de 0, especificando efetivamente um período de tempo de tempo de transação infinito. Usando a ferramenta administrativa Serviços de Componentes,  altere a configuração de tempo-de-tempo de transação na guia Opções da **janela Meu Computador** Propriedades.

 

## <a name="debugging-server-application-components-with-visual-c"></a>Depurando componentes de aplicativo do servidor com Visual C++

Ao depurar aplicativos de servidor COM+, talvez você queira depurar chamadas remotas carregando o cliente e o aplicativo de servidor no depurador. Com Visual C++, você pode depurar chamadas remotas para seus componentes por meio das configurações JIT (Just-In-Time) e OLE RPC. A configuração JIT faz com que o componente compilado inicie o Visual C++ depurador quando ocorrer um erro; a configuração OLE RPC permite que o depurador seja passo a passo do cliente para o componente à medida que você passa pelo código.

Quando esses recursos estão habilitados, você pode iniciar seu cliente no depurador. Quando o cliente faz uma chamada para o componente, o depurador entra no código do componente no processo do servidor, mesmo se o servidor estiver em um computador diferente na rede. Uma sessão de depuração é iniciada automaticamente no computador do servidor, se necessário. Da mesma forma, uma única etapa após a instrução de retorno no código do componente retornará a depuração para a próxima instrução no código do cliente.

> [!Note]  
> Você pode salvar algumas etapas usando a configuração Iniciar com+ **no depurador.** Isso permite que você especifique o Visual C++ (ou outro) depurador sem precisar fazer configurações especiais de depuração no ambiente Visual C++ aplicativo. Você encontrará isso na ferramenta administrativa serviços de  componentes como uma caixa de seleção na guia Avançado da caixa de diálogo Propriedades **do** aplicativo COM+. Para obter mais informações, consulte "Depurando sem Visual C++" neste tópico.

 

Quando o aplicativo COM+ que contém o componente for um aplicativo de servidor, você deverá começar desligando o aplicativo usando a ferramenta administrativa serviços de componentes. Para fazer isso, clique com o botão direito do mouse no aplicativo COM+ na árvore de console e clique **em Desligar**.

**Para habilitar a depuração de RPC Visual C++**

1.  No Visual C++, no menu **Ferramentas,** clique em **Opções**.

2.  Na caixa **de** diálogo Opções, na guia **Depurar,** marque as caixas de seleção **Depuração OLE RPC** e **Depuração just-in-time.**

3.  Clique em **OK**.

Para iniciar a depuração, inicie o projeto cliente no depurador.

Você também pode depurar seu componente sem iniciar seu cliente no depurador. Nesse caso, o componente deve iniciar o depurador por conta própria. Para fazer isso, seu projeto de componente deve especificar um executável para a sessão de depuração, juntamente com a ID do aplicativo COM+.

**Para habilitar um componente de aplicativo de servidor para iniciar o Visual C++ depurador**

1.  No menu **Project,** clique **em Configurações**.

2.  Na caixa **de Project Configurações,** na **caixa Configurações For,** selecione **Win32 Depurar**.

3.  Na guia **Depurar** , na caixa **Categoria** , selecione **Geral**.

4.  Na caixa **Executável** para sessão de depuração, insira o caminho totalmente qualificado para Dllhost.exe, seguido por um argumento que especifica a ID do aplicativo COM+ que contém o componente.

    > [!Note]  
    > Usando a ferramenta administrativa Serviços de Componentes, você encontrará a ID  do aplicativo na guia **Geral** da caixa de diálogo Propriedades do aplicativo COM+. A seguir está um exemplo:

     

    > [!Note]  
    > C: \\ Winnt \\ System32 \\Dllhost.exe /ProcessID:{applicationID}

     

5.  Clique em **OK**.

Agora você pode definir pontos de interrupção, iniciar o depurador e começar a fazer chamadas ao componente.

## <a name="debugging-library-application-components-with-visual-c"></a>Componentes do aplicativo de biblioteca de depuração com Visual C++

Para depurar componentes em um aplicativo de biblioteca, você deve configurar o projeto do cliente porque o processo do cliente hospedará o aplicativo de biblioteca.

**Para habilitar a depuração de aplicativos de biblioteca com Visual C++**

1.  No Visual C++, no menu **Project,** clique **em Configurações**.

2.  Na caixa **Project Configurações** de diálogo, na **caixa Configurações For,** clique em **Win32 Depurar**.

3.  Na guia **Depurar** , na caixa **Categoria** , clique em **DLLs adicionais**.

4.  Na lista **Módulos,** adicione as DLLs do componente em seu aplicativo de biblioteca. Isso permite definir pontos de interrupção antes que sua DLL seja realmente carregada.

5.  Clique em **OK**.

## <a name="debugging-without-visual-c"></a>Depuração sem Visual C++

Se você está usando o Visual C++ para depuração, use a configuração Iniciar no **depurador** para especificar o depurador no qual os componentes devem ser executados.

**Para especificar um depurador da ferramenta administrativa dos Serviços de Componentes**

1.  Na árvore de console, selecione o aplicativo de biblioteca COM+ que contém os componentes que você deseja depurar.

2.  Clique com o botão direito do mouse no aplicativo e clique em **Propriedades.**

3.  Na caixa de diálogo **Propriedades do** aplicativo, clique na **guia** Avançado.

4.  Em **Depurando**, marque a **caixa de seleção Iniciar no depurador.**

5.  Na caixa **Caminho do depurador,** insira o caminho para o depurador que você deseja usar. Você também pode clicar **em Procurar** para localizar o depurador. Veja a seguir um exemplo: C: \\ Winnt \\ System32 \\Ntsd.exe.

6.  Clique em **OK**.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Componentes de depuração gravados Visual Basic](debugging-components-written-in-visual-basic.md)
</dt> </dl>

 

 



