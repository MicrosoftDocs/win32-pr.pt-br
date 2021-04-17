---
description: Quando estiver pronto para depurar a funcionalidade COM+ em seus componentes do Microsoft Visual C++, você poderá configurar Visual C++ projeto ou a ferramenta administrativa serviços de componentes para iniciar o depurador.
ms.assetid: 206467ac-108a-49de-a884-66959dc77650
title: Componentes de depuração escritos em Visual C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a14e4b6324cc69531f09612c2af37fa03a036fd4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105790625"
---
# <a name="debugging-components-written-in-visual-c"></a>Componentes de depuração escritos em Visual C++

Quando estiver pronto para depurar a funcionalidade COM+ em seus componentes do Microsoft Visual C++, você poderá configurar Visual C++ projeto ou a ferramenta administrativa serviços de componentes para iniciar o depurador. Se você estiver usando Visual C++, poderá depurar com um cliente remoto usando o RPC OLE e a depuração Just-in-time (JIT). Se não for possível executar o cliente no depurador ou se o cliente estiver em execução em outra máquina, você poderá usar a configuração iniciar do COM+ **no depurador** . Você verá isso na ferramenta administrativa serviços de componentes como uma caixa de seleção na guia **avançado** da caixa de diálogo **Propriedades** do aplicativo com+.

Quando terminar a depuração, você deverá desligar os aplicativos COM+ que está depurando. Se um processo do servidor for deixado em execução, você poderá receber uma mensagem de erro na próxima vez que tentar criar uma DLL quando a DLL existente ainda estiver carregada na memória. Para desligar um aplicativo COM+, clique com o botão direito do mouse no aplicativo na árvore de console e clique em **desligar**.

> [!Note]  
> Se você estiver usando transações, talvez também queira aumentar o tempo limite da transação, cujo padrão é de 60 segundos. Você também pode especificar um valor de 0, especificando efetivamente um período de tempo limite de transação infinito. Usando a ferramenta administrativa serviços de componentes, altere a configuração de tempo limite da transação na guia **Opções** da janela **Propriedades do meu computador** .

 

## <a name="debugging-server-application-components-with-visual-c"></a>Depurando componentes de aplicativos de servidor com Visual C++

Ao depurar aplicativos de servidor COM+, talvez você queira depurar chamadas remotas carregando o cliente e o aplicativo de servidor no depurador. Com o Visual C++, você pode depurar chamadas remotas para seus componentes por meio das configurações JIT (just-in-time) e RPC do OLE. A configuração JIT faz com que o componente compilado inicie o depurador de Visual C++ quando ocorrer um erro; a configuração OLE RPC permite que o depurador passe do cliente para o componente conforme você percorre seu código.

Quando esses recursos estiverem habilitados, você poderá iniciar o cliente no depurador. Quando o cliente fizer uma chamada para seu componente, o depurador irá entrar no código do componente no processo do servidor, mesmo se o servidor estiver em um computador diferente na rede. Uma sessão de depuração é iniciada automaticamente no computador servidor, se necessário. Da mesma forma, a etapa única após a instrução return no código do componente retornará a depuração para a próxima instrução no código do cliente.

> [!Note]  
> Talvez seja possível salvar algumas etapas usando a configuração **Iniciar no depurador** do com+. Isso permite que você especifique o depurador de Visual C++ (ou outro) sem precisar fazer configurações de depuração especiais no ambiente de Visual C++. Você verá isso na ferramenta administrativa serviços de componentes como uma caixa de seleção na guia **avançado** da caixa de diálogo **Propriedades** do aplicativo com+. Para obter mais informações, consulte "depuração sem Visual C++" neste tópico.

 

Quando o aplicativo COM+ que contém o componente é um aplicativo de servidor, você deve começar encerrando o aplicativo usando a ferramenta administrativa serviços de componentes. Para fazer isso, clique com o botão direito do mouse no aplicativo COM+ na árvore de console e clique em **desligar**.

**Para habilitar a depuração de RPC no Visual C++**

1.  No Visual C++, no menu **ferramentas** , clique em **Opções**.

2.  Na caixa de diálogo **Opções** , na guia **depurar** , marque as caixas de seleção **depuração de RPC OLE** e **depuração Just-in-time** .

3.  Clique em **OK**.

Para iniciar a depuração, inicie o projeto de cliente no depurador.

Você também pode depurar seu componente sem iniciar o cliente no depurador. Nesse caso, o componente deve iniciar o depurador por conta própria. Para fazer isso, o projeto de componente deve especificar um executável para a sessão de depuração, juntamente com a ID do aplicativo COM+.

**Para habilitar um componente de aplicativo de servidor para iniciar o depurador de Visual C++**

1.  No menu **projeto** , clique em **configurações**.

2.  Na caixa de diálogo **configurações do projeto** , na caixa **configurações de** , selecione **depuração Win32**.

3.  Na guia **depurar** , na caixa **categoria** , selecione **geral**.

4.  Na caixa **executável para sessão de depuração** , insira o caminho totalmente qualificado para Dllhost.exe, seguido por um argumento ESPECIFICANDO a ID de aplicativo do aplicativo com+ que contém o componente.

    > [!Note]  
    > Usando a ferramenta administrativa serviços de componentes, você encontrará a ID do aplicativo na guia **geral** da caixa de diálogo **Propriedades** do aplicativo com+. A seguir está um exemplo:

     

    > [!Note]  
    > C: \\ WinNT \\ System32 \\Dllhost.exe/ProcessId: {applicationID}

     

5.  Clique em **OK**.

Agora você pode definir pontos de interrupção, iniciar o depurador e começar a fazer chamadas para seu componente.

## <a name="debugging-library-application-components-with-visual-c"></a>Depurando componentes de aplicativos de biblioteca com Visual C++

Para depurar componentes em um aplicativo de biblioteca, você deve configurar o projeto do cliente, pois o processo do cliente hospedará o aplicativo de biblioteca.

**Para habilitar a depuração de aplicativo de biblioteca com Visual C++**

1.  No Visual C++, no menu **projeto** , clique em **configurações**.

2.  Na caixa de diálogo **configurações do projeto** , na caixa **configurações de** , clique em **depuração Win32**.

3.  Na guia **depurar** , na caixa **categoria** , clique em **DLLs adicionais**.

4.  Na lista de **módulos** , adicione as DLLs de componentes em seu aplicativo de biblioteca. Isso permite que você defina pontos de interrupção antes que sua DLL seja realmente carregada.

5.  Clique em **OK**.

## <a name="debugging-without-visual-c"></a>Depuração sem Visual C++

Se você estiver ou não usando Visual C++ para depuração, poderá usar a configuração **Iniciar no depurador** para especificar o depurador no qual os componentes devem ser executados.

**Para especificar um depurador da ferramenta administrativa serviços de componentes**

1.  Na árvore de console, selecione o aplicativo de biblioteca COM+ que contém os componentes que você deseja depurar.

2.  Clique com o botão direito do mouse no aplicativo e clique em **Propriedades**.

3.  Na caixa de diálogo **Propriedades** do aplicativo, clique na guia **avançado** .

4.  Em **depuração**, marque a caixa de seleção **Iniciar no depurador** .

5.  Na caixa **caminho do depurador** , insira o caminho para o depurador que você deseja usar. Você também pode clicar em **procurar** para localizar o depurador. Veja a seguir um exemplo: C: \\ WinNT \\ System32 \\Ntsd.exe.

6.  Clique em **OK**.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Componentes de depuração escritos em Visual Basic](debugging-components-written-in-visual-basic.md)
</dt> </dl>

 

 



