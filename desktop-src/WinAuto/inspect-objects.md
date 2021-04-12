---
title: Ferramentas de acessibilidade – inspecionar
description: Inspecione (Inspect.exe) é uma ferramenta baseada no Windows que permite que você selecione qualquer elemento de interface do usuário e exiba os dados de acessibilidade do elemento.
ms.assetid: 38edacbc-cf24-4818-b029-561b21e3704c
keywords:
- Ferramenta inspecionar
- Acessibilidade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1770c6c4db812ea7d2880c50fcc72cd0edc15022
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104365653"
---
# <a name="accessibility-tools---inspect"></a>Ferramentas de acessibilidade – inspecionar

**Inspecione** (Inspect.exe) é uma ferramenta baseada no Windows que permite que você selecione qualquer elemento de interface do usuário e exiba os dados de acessibilidade do elemento. Você pode exibir propriedades de automação da interface do usuário da Microsoft e padrões de controle, bem como propriedades do Microsoft Acessibilidade Ativa. **Inspecionar** também permite testar a estrutura de navegação dos elementos de automação na árvore de automação da interface do usuário e os objetos acessíveis na hierarquia do Microsoft acessibilidade ativa.

O **inspecionar** é instalado com o SDK (Software Development Kit) do Windows. (Ele também está disponível em versões anteriores do SDK do Windows.) Ele está localizado na \\ pasta bin \\ < *version* > \\ < > do caminho de instalação do SDK (Inspect.exe).

> [!NOTE]
> **Inspecionar** é uma ferramenta herdada. Em vez disso, recomendamos o uso de [informações de acessibilidade](https://accessibilityinsights.io/) .

## <a name="requirements"></a>Requisitos

A **inspeção** pode ser usada para examinar dados de acessibilidade em sistemas que não têm a automação da interface do usuário, mas só pode examinar as propriedades do Microsoft acessibilidade ativa. Para examinar a automação da interface do usuário, a automação da interface do usuário deve estar presente no sistema. Para obter mais informações, consulte a seção "requisitos" da [automação da interface do usuário](entry-uiauto-win32.md).

O **inspecionar** é instalado como parte do conjunto geral de ferramentas no SDK do Windows, ele não é distribuído como um download separado. O SDK do Windows inclui todas as ferramentas relacionadas à acessibilidade documentadas nesta seção. [Obtenha o SDK do Windows.](https://developer.microsoft.com/) (Há também um arquivo de download do SDK vinculado dessa página, se você precisar de uma versão anterior.)

Para executar o **inspecionar**, localize Inspect.exe \\ na \\ < pasta bin *version* > \\ < > e execute-o (normalmente, você não precisa executar como administrador).

## <a name="the-inspect-window"></a>A janela Inspecionar

A janela **inspecionar** tem várias partes principais:

- Barra de título. Exibe o identificador de janela de **inspeção** (HWND).
- Barra de menus. Fornece acesso para **inspecionar** a funcionalidade.
- Barra. Fornece acesso para **inspecionar** a funcionalidade.
- Exibição de árvore. Apresenta a estrutura hierárquica dos elementos da interface do usuário como um controle de exibição de árvore que você pode usar para navegar entre os elementos.
- Exibição de dados. Exibe todas as propriedades de acessibilidade expostas para o elemento de interface do usuário selecionado.

Os comandos disponíveis na barra de menus também estão disponíveis na barra de ferramentas. A imagem a seguir mostra a ferramenta **Inspect** consultando as propriedades de Automação da Interface do Usuário no elemento do menu **Edit** no Bloco de Notas.

![captura de tela mostrando a interface do usuário para a ferramenta inspecionar](images/inspect.png)

## <a name="using-inspect"></a>Usando inspecionar

Quando você começa a **inspeção**, a exibição de **árvore** mostra o local do elemento de interface do usuário selecionado no momento na hierarquia do elemento e a exibição de **dados** mostra as informações de Propriedade do elemento da interface do usuário selecionado. Você pode navegar pela interface do usuário para exibir informações de acessibilidade sobre cada elemento na interface do usuário. Por padrão, **Inspecione** rastreia o foco do teclado ou do mouse. Conforme as alterações de foco, a exibição de **dados** é atualizada com as informações de Propriedade do elemento com foco.

Para navegar entre os elementos da interface do usuário, você pode usar qualquer um dos seguintes:

- O mouse
- O teclado
- O controle de exibição de árvore no modo de exibição de **árvore**
- As opções de navegação no menu de **navegação**
- As opções de navegação na barra de ferramentas

As três últimas opções permitem que você navegue pela hierarquia de árvore da interface do usuário. A estrutura dessa árvore pode diferir ligeiramente entre a automação da interface do usuário e os modos de Acessibilidade Ativa da Microsoft.

## <a name="verifying-accessibility-property-information"></a>Verificando informações de propriedade de acessibilidade

A exibição de **dados** mostra as informações de Propriedade do elemento de interface do usuário selecionado no momento. Você pode configurar a **inspeção** para mostrar informações sobre todas as propriedades de acessibilidade ou um subconjunto dessas propriedades. Você também pode especificar outras opções de exibição, como se a **inspeção** deve permanecer sobre outras interfaces do usuário ou se a **inspeção** deve realçar um retângulo delimitador em volta do elemento selecionado. Depois de configurar o **inspecionar** para funcionar da maneira desejada, você pode começar a navegar entre elementos da interface do usuário e exibir informações de propriedade. **Inspecione** salva as definições de configuração quando ele fecha e as usa para inicializar a próxima sessão de **inspeção** .

### <a name="configure-property-settings"></a>Definir configurações de propriedade

1. No menu **Opções** , selecione **configurações...** ou selecione a **caixa de diálogo Mostrar configurações** na barra de ferramentas.
2. Na lista **Exibir na janela principal** , selecione as propriedades que você deseja exibir na exibição de **dados** de **inspecionar**.
3. Na lista de **dicas de ferramenta exibir em informações** , selecione as propriedades que você deseja exibir em uma dica de ferramenta.
4. Para exibir as propriedades que o elemento de interface do usuário pode não dar suporte, marque a caixa **Exibir Propriedades sem suporte** .
5. Clique em **OK**.

### <a name="to-configure-viewing-options"></a>Para configurar opções de exibição

- No menu **Opções** ou na barra de ferramentas, você pode selecionar as seguintes opções de exibição.

| Quando essa opção é selecionada | **Inspecionar** faz isso                                                                                                                                                                                                              |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Sempre no início                | Aparece na parte superior de qualquer outra janela na tela.                                                                                                                                                                                  |
| Modo MSAA                    | Exibe informações sobre a propriedade do Microsoft Acessibilidade Ativa.                                                                                                                                                                      |
| Modo de automação da interface do usuário           | Exibe informações de propriedade de automação da interface do usuário.                                                                                                                                                                                       |
| Exibição somente do Windows visível    | Disponível somente no modo MSAA.                                                                                                                                                                                                       |
| Exibição bruta                     | Apresenta a [exibição bruta](uiauto-treeoverview.md) da árvore de automação da interface do usuário ou árvore MSAA no modo de exibição de **árvore** .                                                                                                             |
| Exibição de controle                 | Apresenta a [exibição de controle](uiauto-treeoverview.md) da árvore de automação da interface do usuário no modo de exibição de **árvore** . Disponível somente no modo de automação da interface do usuário.                                                                            |
| Exibição de conteúdo                 | Apresenta a [exibição de conteúdo](uiauto-treeoverview.md) da árvore de automação da interface do usuário no modo de exibição de **árvore** . Disponível somente no modo de automação da interface do usuário.                                                                            |
| Barra de ferramentas de foco ativa         | Ativa botões da barra de ferramentas ao focalizar o mouse, em vez de exigir um clique do mouse.                                                                                                                                                      |
| Aviso sonoro sobre erro                | Emite avisos sonoros quando um erro é detectado durante uma operação de automação de interface do usuário ou MSAA.                                                                                                                                                          |
| \_Sinalizador SPI SCREENREADER       | Assume que um leitor de tela está presente. Esse sinalizador indica que um aplicativo deve fornecer informações textualmente em vez de graficamente. Você não deve assumir que esse sinalizador está definido simplesmente porque um leitor de tela está presente.         |
| Mostrar retângulo de realce     | Realça um retângulo em volta do elemento com foco.                                                                                                                                                                              |
| Mostrar realce do cursor         | Realça o cursor. Disponível somente no modo MSAA.                                                                                                                                                                                 |
| Mostrar dica de ferramenta de informações     | Mostra informações de propriedade em uma dica de ferramenta.                                                                                                                                                                                           |
| Monitorar foco                  | Segue o foco do teclado. Quando selecionado, um gancho de evento de foco assíncrono é instalado e move o cursor para a parte superior esquerda do elemento com o foco. Isso faz com que a **inspeção** atualize suas propriedades em aproximadamente um segundo. |
| Cursor de inspeção                  | Segue o cursor. Disponível somente no modo MSAA.                                                                                                                                                                                    |
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
