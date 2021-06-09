---
title: Ferramentas de acessibilidade – Inspecionar
description: Inspecionar (Inspect.exe) é uma ferramenta baseada no Windows que permite selecionar qualquer elemento de interface do usuário e exibir os dados de acessibilidade do elemento.
ms.assetid: 38edacbc-cf24-4818-b029-561b21e3704c
keywords:
- Ferramenta inspecionar
- Acessibilidade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcef8efa9efc0241d0f813da01623a1c02e6d226
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/09/2021
ms.locfileid: "111827632"
---
# <a name="accessibility-tools---inspect"></a>Ferramentas de acessibilidade – Inspecionar

> [!Important]
> **Inspecionar** é uma ferramenta herdado. Em vez disso, [é recomendável usar o Accessibility Insights.](https://accessibilityinsights.io/)

**Inspecionar** (Inspect.exe) é uma ferramenta baseada no Windows que permite selecionar qualquer elemento de interface do usuário e exibir os dados de acessibilidade do elemento. Você pode exibir propriedades Automação da Interface do Usuário Microsoft e padrões de controle, bem como Microsoft Active Accessibility propriedades. **Inspecionar** também permite que você teste a estrutura de navegação dos elementos de automação na árvore Automação da Interface do Usuário e os objetos acessíveis na hierarquia Microsoft Active Accessibility dados.

## <a name="requirements"></a>Requisitos

Para examinar Automação da Interface do Usuário, Automação da Interface do Usuário deve estar presente no sistema. Para obter mais informações, consulte a seção "Requisitos" [do Automação da Interface do Usuário](entry-uiauto-win32.md).

**Inspecionar** é instalado como parte do conjunto geral de ferramentas no SDK (Software Development Kit do Windows (SDK do Windows)), ele não é distribuído como um download separado. O SDK do Windows inclui todas as ferramentas relacionadas à acessibilidade documentadas nesta seção.

[Baixe o SDK do Windows](https://developer.microsoft.com/en-us/windows/downloads/windows-10-sdk/).

> [!NOTE]
> Para versões mais antigas do SDK do Windows, consulte o [arquivo SDK do Windows emulador e](https://developer.microsoft.com/en-us/windows/downloads/sdk-archive/).

**Inspect.exe** está localizado na pasta bin version platform> do caminho de instalação do \\ \\ <  > \\ <  SDK (normalmente, você não precisa executar como administrador).

## <a name="the-inspect-window"></a>A janela Inspecionar

A **janela Inspecionar** tem várias partes principais:

- Barra de título. Exibe o **HWND (inspecione** o HWND).
- Barra de menus. Fornece acesso à **funcionalidade Inspecionar.**
- Toolbar. Fornece acesso à **funcionalidade Inspecionar.**
- Exibição de árvore. Apresenta a estrutura hierárquica dos elementos da interface do usuário como um controle de exibição de árvore que você pode usar para navegar entre os elementos.
- Exibição de dados. Exibe todas as propriedades de acessibilidade expostas para o elemento de interface do usuário selecionado.

Os comandos disponíveis na barra de menus também estão disponíveis na barra de ferramentas. A imagem a seguir mostra a ferramenta **Inspect** consultando as propriedades de Automação da Interface do Usuário no elemento do menu **Edit** no Bloco de Notas.

![captura de tela mostrando a interface do usuário para a ferramenta de inspeção](images/inspect.png)

## <a name="using-inspect"></a>Usando Inspecionar

Quando você inicia  **Inspecionar**, o Exibição de árvore mostra o local do  elemento de interface do usuário selecionado no momento na hierarquia de elementos e a exibição Dados mostra as informações de propriedade para o elemento de interface do usuário selecionado. Você pode navegar na interface do usuário para exibir informações de acessibilidade sobre cada elemento na interface do usuário. Por padrão, **Inspecionar rastreia** o foco do teclado ou do mouse. Conforme o foco muda, **a Exibição** de dados é atualizada com as informações de propriedade do elemento com foco.

Para navegar entre elementos da interface do usuário, você pode usar qualquer um dos seguintes:

- O mouse
- O teclado
- O controle de exibição de árvore no **Exibição de** árvore
- As opções de navegação no menu **De navegação**
- As opções de navegação na barra de ferramentas

As três últimas opções permitem que você navegue pela hierarquia de árvore da interface do usuário. A estrutura dessa árvore pode diferir ligeiramente entre Automação da Interface do Usuário e Microsoft Active Accessibility de dados.

## <a name="verifying-accessibility-property-information"></a>Verificando informações de propriedade de acessibilidade

A **exibição** Dados mostra as informações de propriedade do elemento de interface do usuário selecionado no momento. Você pode configurar **Inspecionar** para mostrar informações sobre todas as propriedades de acessibilidade ou um subconjunto dessas propriedades. Você também pode especificar outras opções de exibição, como se **Inspecionar**  deve permanecer sobre outras interfaces do usuário ou se Inspecionar deve realçar um retângulo delimitativo em torno do elemento selecionado. Depois de configurar **Inspecionar** para funcionar da maneira que você deseja, você pode começar a navegar entre elementos da interface do usuário e exibir informações de propriedade. **Inspecionar** salva as definições de configuração quando ela fecha e as usa para inicializar sua próxima **sessão de** Inspeção.

### <a name="configure-property-settings"></a>Definir configurações de propriedade

1. No menu **Opções,** selecione **Configurações...** ou mostrar caixa **de diálogo Configurações** na barra de ferramentas.
2. Na lista **Exibir na Janela Principal,** selecione as propriedades que você deseja exibir na **exibição Dados** de **Inspecionar**.
3. Na lista **Exibir na Dica de Ferramenta de** Informações, selecione as propriedades que você deseja exibir em uma dica de ferramenta.
4. Para exibir as propriedades às quais o elemento de interface do usuário pode não dar suporte, marque a caixa Exibir **propriedades sem** suporte.
5. Clique em **OK**.

### <a name="to-configure-viewing-options"></a>Para configurar opções de exibição

- No menu **Opções** ou na barra de ferramentas, você pode selecionar as seguintes opções de exibição.

| Quando essa opção é selecionada | **Inspecionar** faz isso                                                                                                                                                                                                              |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Always on Top                | Aparece na parte superior de qualquer outra janela na tela.                                                                                                                                                                                  |
| Modo MSAA                    | Exibe Microsoft Active Accessibility de propriedade.                                                                                                                                                                      |
| Automação da Interface do Usuário de Automação da Interface do Usuário           | Exibe Automação da Interface do Usuário de propriedade.                                                                                                                                                                                       |
| Exibição somente visível do Windows    | Disponível somente no modo MSAA.                                                                                                                                                                                                       |
| Exibição Bruta                     | Apresenta a [exibição bruta](uiauto-treeoverview.md) da árvore Automação da Interface do Usuário ou árvore MSAA na **exibição árvore.**                                                                                                             |
| Exibição de controle                 | Apresenta a [exibição de](uiauto-treeoverview.md) controle da árvore Automação da Interface do Usuário na **exibição árvore.** Disponível somente Automação da Interface do Usuário modo.                                                                            |
| Exibição de conteúdo                 | Apresenta a [exibição de](uiauto-treeoverview.md) conteúdo da Automação da Interface do Usuário no **exibição de** árvore. Disponível somente Automação da Interface do Usuário modo.                                                                            |
| Barra de Ferramentas de Foco Ativo         | Ativa os botões da barra de ferramentas ao passar o mouse, em vez de exigir um clique do mouse.                                                                                                                                                      |
| Aviso de erro                | Emitirá um aviso quando um erro for detectado durante uma operação Automação da Interface do Usuário ou MSAA.                                                                                                                                                          |
| Sinalizador SPI \_ SCREENREADER       | Supõe que um leitor de tela está presente. Esse sinalizador indica que um aplicativo deve fornecer informações textuticamente em vez de graficamente. Você não deve supor que esse sinalizador está definido simplesmente porque um leitor de tela está presente.         |
| Mostrar retângulo de realçada     | Realça um retângulo ao redor do elemento com foco.                                                                                                                                                                              |
| Mostrar Realçando a adoção         | Realça o a careta. Disponível somente no modo MSAA.                                                                                                                                                                                 |
| Mostrar dica de ferramenta de informações     | Mostra informações de propriedade em uma dica de ferramenta.                                                                                                                                                                                           |
| Observar o foco                  | Segue o foco do teclado. Quando selecionado, um gancho de evento de foco assíncrono é instalado e move o aro para a parte superior esquerda do elemento com o foco. Isso faz **com que a Inspeção** atualize suas propriedades em cerca de um segundo. |
| Observar a adoção                  | Segue o caret. Disponível somente no modo MSAA.                                                                                                                                                                                    |
| Cursor de inspeção                 | Segue o cursor.                                                                                                                                                                                                                |
| Assista a dicas de ferramenta               | Segue as dicas de ferramenta.                                                                                                                                                                                                              |
| Mostrar árvore                    | Exibe o modo de exibição de **árvore** .                                                                                                                                                                                                        |

## <a name="verifying-accessibility-navigation"></a>Verificando a navegação de acessibilidade

Depois de selecionar um elemento de interface do usuário usando **inspecionar**, você pode validar que o elemento expõe a navegação de automação do Windows correta para produtos de tecnologia assistencial.

### <a name="verify-accessibility-navigation"></a>Verificar navegação de acessibilidade

1. Abra **inspecionar** e o aplicativo que você deseja testar.
2. Selecione o elemento de interface do usuário do qual você deseja iniciar a navegação.
3. Na exibição de **dados** , verifique se o elemento expõe as propriedades corretas relacionadas à navegação.
4. Use o modo de exibição de **árvore** , o menu de **navegação** ou os botões de navegação na barra de ferramentas para navegar pela interface do usuário e verificar se cada elemento expõe as propriedades corretas relacionadas à navegação.
    > [!Note]  
    > As opções do menu de **navegação** e os botões da barra de ferramentas de navegação mudam dependendo de onde o elemento selecionado está na árvore.

## <a name="interacting-with-ui-elements"></a>Interagindo com elementos de interface do usuário

A automação do Windows expõe métodos que permitem que produtos de tecnologia assistencial interajam com um elemento de interface do usuário como se o mouse ou o teclado estivesse sendo usado (por exemplo, para clicar em um botão). O menu **inspecionar** ação permite que os testadores invoquem métodos de automação do Windows em um elemento (por exemplo, **Invoke. Invoke** chama o método [**IUIAutomationInvokePattern:: Invoke**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationinvokepattern-invoke) ).

### <a name="interact-with-ui-elements"></a>Interagir com elementos da interface do usuário

1. Abra **inspecionar** e o aplicativo que você deseja testar.
2. Selecione o elemento de interface do usuário com o qual você deseja interagir.
3. No menu **ação** ou na barra de ferramentas, selecione a ação que corresponde ao método de automação do Windows que você deseja invocar.

O menu **ação** contém os itens de **atualização** e **foco** , juntamente com outros itens que variam dependendo se o modo de automação da interface do usuário ou o modo MSAA está selecionado. No modo de automação da interface do usuário, os outros itens refletem os padrões de controle com suporte pelo elemento da interface do usuário selecionado no momento. No modo MSAA, os outros itens sempre consistem no seguinte:

| Ação                | Descrição                                                                                                           |
|-----------------------|-----------------------------------------------------------------------------------------------------------------------|
| Atualizar               | Atualiza a interface do usuário. Disponível no modo MSAA e de automação da interface do usuário.                                               |
| Ação Padrão        | Executa a ação padrão para o elemento.                                                                          |
| Foco                 | Define o foco no elemento. Disponível no modo MSAA e de automação da interface do usuário.                                                  |
| Selecionar                | Seleciona o elemento.                                                                                                  |
| Estender seleção      | Estende a seleção de elementos para incluir todos os elementos entre o primeiro elemento selecionado e o elemento atual. |
| Adicionar à seleção      | Seleciona o elemento atual (como um item de lista).                                                                    |
| Remover da seleção | Remove o elemento atual da seleção.                                                                       |
| SetAccValue           | Define o valor de Acessibilidade Ativa da Microsoft do elemento como a cadeia de caracteres especificada.                                 |
| Filho focado         | Navega para o filho do elemento que tem o foco no momento.                                                       |
| HitTest no cursor     | Navega para o filho do elemento especificado pelo cursor do mouse.                                                      |
| HitTest...            | Abre a caixa de diálogo **HitTest** .                                                                                     |



 

## <a name="keyboard-shortcuts"></a>Atalhos do teclado

Muitos dos itens de menu podem ser chamados com um atalho de teclado mesmo quando a **inspeção** não é o aplicativo ativo. No entanto, observe que as teclas de atalho estão em conflito com alguns aplicativos.

As teclas de atalho do teclado a seguir ativam as várias opções no menu:



| Para fazer isso                                                                                                                                       | Usar este atalho de teclado |
|--------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------|
| Invocar a ação padrão do objeto sob o cursor (ação padrão). Disponível somente no modo MSAA.                                       | CTRL+SHIFT+F2              |
| Selecione o objeto sob o cursor (SELECT). Disponível somente no modo MSAA.                                                                        | CTRL+SHIFT+F3              |
| Defina o foco do teclado para o objeto sob o cursor (foco).                                                                                   | CTRL + SHIFT + F4              |
| Mova para o objeto irmão anterior do outro no cursor. Este comando navega para objetos somente dentro de um contêiner (irmão anterior). | CTRL + SHIFT + F5              |
| Mover para o pai do objeto (pai).                                                                                                            | CTRL+SHIFT+F6              |
| Mover para o primeiro filho do objeto atual (primeiro filho).                                                                                     | CTRL + SHIFT + F7              |
| Mover para o próximo objeto irmão do outro no cursor. Este comando navega para objetos somente dentro de um contêiner (próximo irmão).         | CTRL + SHIFT + F8              |
| Mover para o último filho do objeto atual (último filho).                                                                                       | Ctrl+Shift+F9              |
| Mova para o objeto sob o cursor do mouse (HitTest no cursor). Disponível somente no modo MSAA.                                                      | CTRL+SHIFT+1               |
| Copie o conteúdo da exibição de dados para a área de transferência (copiar tudo).                                                                                  | CTRL+SHIFT+4               |
| Atualize o conteúdo da exibição de dados (atualizar).                                                                                                 | CTRL+SHIFT+5               |
| Assista ao objeto que tem foco (foco de inspeção).                                                                                                   | CTRL+SHIFT+6               |
| Mover para o objeto irmão à esquerda do cursor está sobre (esquerda). Disponível somente no modo MSAA.                                        | CTRL+SHIFT+7               |
| Mover para o objeto irmão acima do objeto no qual o cursor está acima (up). Disponível somente no modo MSAA.                                                | CTRL+SHIFT+8               |
| Mova para o objeto irmão abaixo do cursor que está acima (abaixo). Disponível somente no modo MSAA.                                                 | CTRL+SHIFT+9               |
| Mover para o objeto irmão à direita do cursor está sobre (direita). Disponível somente no modo MSAA.                                      | CTRL + SHIFT + 0               |

## <a name="related-topics"></a>Tópicos relacionados

- [Accessible Event Watcher](accessible-event-watcher.md)
- [Ferramentas de teste](testing-tools.md)
- [UI Accessibility Checker](ui-accessibility-checker.md)
- [Verificação da Automação da Interface do Usuário](ui-automation-verify.md)
- [AccScope](accscope.md)
