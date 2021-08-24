---
description: Manipuladores de menu de atalho, também conhecidos como manipuladores de menu de contexto ou manipuladores de verbo, são um tipo de manipulador de tipo de arquivo. Como todos esses manipuladores, eles são objetos COM (Component Object Model) em processo implementados como DLLs.
ms.assetid: cff79cdc-8a01-4575-9af7-2a485c6a8e46
title: Como Criar Manipuladores do Menu de Atalho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3a6b6f812772b884e12c45a48bae8075d90df28fb3b60f895cfd4c4263be74c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119715759"
---
# <a name="creating-shortcut-menu-handlers"></a>Como Criar Manipuladores do Menu de Atalho

Manipuladores de menu de atalho, também conhecidos como manipuladores de menu de contexto ou manipuladores de verbo, são um tipo de manipulador de tipo de arquivo. Esses manipuladores podem ser impelmented de uma maneira que os cause carregar em seu próprio processo ou no Gerenciador, ou em outros processos de terceiros. Tome cuidado ao criar manipuladores em processo, pois eles podem causar danos ao processo que os carrega.

> [!Note]  
> há considerações especiais para versões com base em 64 bits do Windows ao registrar manipuladores que funcionam no contexto de aplicativos de 32 bits: quando invocado no contexto de um aplicativo de diferentes períodos de leitura, o subsistema WOW64 redireciona o acesso ao sistema de arquivos para alguns caminhos. Se o manipulador de .exe for armazenado em um desses caminhos, ele não estará acessível neste contexto. Portanto, como uma solução alternativa, armazene seu .exe em um caminho que não seja redirecionado ou armazene uma versão de stub do seu .exe que inicia a versão real.

Este tópico é organizado da seguinte maneira:

-   [Verbos canônicos](#canonical-verbs)
-   [Verbos estendidos](#extended-verbs)
-   [Somente acesso programático a verbos](#programmaticaccessonly-verbs)
-   [Personalizando um menu de atalho usando verbos estáticos](#customizing-a-shortcut-menu-using-static-verbs)
    -   [Ativando o manipulador usando a interface IDropTarget](#activating-your-handler-using-the-idroptarget-interface)
    -   [Especificando a posição e a ordem de verbos estáticos](#specifying-the-position-and-order-of-static-verbs)
    -   [Posicionando verbos na parte superior ou inferior do menu](#positioning-verbs-at-the-top-or-bottom-of-the-menu)
    -   [Criando menus em cascata estáticos](#creating-static-cascading-menus)
    -   [Obtendo comportamento dinâmico para verbos estáticos usando sintaxe de consulta avançada](#getting-dynamic-behavior-for-static-verbs-by-using-advanced-query-syntax)
    -   [preterido: associação de verbos com comandos troca dinâmica de dados](#deprecated-associating-verbs-with-dynamic-data-exchange-commands)
-   [Concluindo tarefas de implementação de verbo](#completing-verb-implementation-tasks)
    -   [Personalizando o menu de atalho para objetos shell predefinidos](#customizing-the-shortcut-menu-for-predefined-shell-objects)
    -   [Estendendo um novo submenu](#extending-a-new-submenu)
    -   [Suprimindo verbos e controlando a visibilidade](#suppressing-verbs-and-controlling-visibility)
    -   [Empregando o modelo de seleção de verbo](#employing-the-verb-selection-model)
    -   [Usando atributos de item](#using-item-attributes)
    -   [Implementando verbos personalizados para pastas por meio de Desktop.ini](#implementing-custom-verbs-for-folders-through-desktopini)
-   [Tópicos relacionados](#related-topics)

## <a name="canonical-verbs"></a>Verbos canônicos

Os aplicativos são geralmente responsáveis por fornecer cadeias de caracteres de exibição localizadas para os verbos que eles definem. No entanto, para fornecer um grau de independência de idioma, o sistema define um conjunto padrão de verbos usados comumente chamados de verbos canônicos. Um verbo canônico nunca é exibido para o usuário e pode ser usado com qualquer idioma da interface do usuário. O sistema usa o nome canônico para gerar automaticamente uma cadeia de caracteres de exibição localizada corretamente. Por exemplo, a cadeia de caracteres de exibição do verbo aberto é definida como **aberta** em um sistema em inglês e para o equivalente em alemão em um sistema alemão.


| Verbo canônico | Descrição                                                          |
|----------------|----------------------------------------------------------------------|
| Aberto           | Abre o arquivo ou a pasta.                                            |
| Opennew        | Abre o arquivo ou a pasta em uma nova janela.                            |
| Imprimir          | Imprime o arquivo.                                                     |
| Imprimir em        | Permite que o usuário imprima um arquivo arrastando-o para um objeto de impressora. |
| Explorar        | abre Windows Explorer com a pasta selecionada.                     |
| Propriedades     | Abre a folha de propriedades do objeto.                                   |

> [!Note]  
> O verbo **Printto** também é canônico, mas nunca é exibido. Sua inclusão permite que o usuário imprima um arquivo arrastando-o para um objeto de impressora.

Os manipuladores de menu de atalho podem fornecer seus próprios verbos canônicos por meio de [**IContextMenu:: GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) com **GCS \_ VERBW** ou **GCS \_ verba**. O sistema usará os verbos canônicos como o segundo parâmetro (*lpOperation*) passado para [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea)e será o [**CMINVOKECOMMANDINFO**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo). membro **lpVerb** passado para o método [**IContextMenu:: InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) .

## <a name="extended-verbs"></a>Verbos estendidos

Quando o usuário clica com o botão direito do mouse em um objeto, o menu de atalho exibe os verbos padrão. Talvez você queira adicionar e dar suporte a comandos em alguns menus de atalho que não são exibidos em todos os menus de atalho. Por exemplo, você pode ter comandos que não são comumente usados ou que se destinam a usuários experientes. Por esse motivo, você também pode definir um ou mais verbos estendidos. Esses verbos são semelhantes aos verbos normais, mas são diferenciados de verbos normais pela maneira como são registrados. Para ter acesso a verbos estendidos, o usuário deve clicar com o botão direito do mouse em um objeto enquanto pressiona a tecla SHIFT. Quando o usuário faz isso, os verbos estendidos são exibidos além dos verbos padrão.

Você pode usar o registro para definir um ou mais verbos estendidos. Os comandos associados serão exibidos somente quando o usuário clicar com o botão direito do mouse em um objeto e também pressionar a tecla SHIFT. Para definir um verbo como estendido, adicione um valor de **\_ sz reg** "estendido" à subchave do verbo. O valor não deve ter nenhum dado associado a ele.

## <a name="programmatic-access-only"></a>Somente acesso programático

Esses verbos nunca são exibidos em um menu de contexto. Eles podem ser acessados usando [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) e especificando o campo **LpVerb** do parâmetro *pExecInfo* (um objeto [SHELLEXECUTEINFO](/windows/win32/api/shellapi/ns-shellapi-shellexecuteinfoa) ). Para definir um verbo como somente acesso programático, adicione um valor "ProgrammaticAccessOnly" **reg \_ sz** à subchave do verbo. O valor não deve ter nenhum dado associado a ele.

Você pode usar o registro para definir um ou mais verbos estendidos. Os comandos associados serão exibidos somente quando o usuário clicar com o botão direito do mouse em um objeto e também pressionar a tecla SHIFT. Para definir um verbo como estendido, adicione um valor de **\_ sz reg** "estendido" à subchave do verbo. O valor não deve ter nenhum dado associado a ele.

## <a name="customizing-a-shortcut-menu-using-static-verbs"></a>Personalizando um menu de atalho usando verbos estáticos

Depois de [escolher um verbo estático ou dinâmico para o menu de atalho](shortcut-choose-method.md) , você pode estender o menu de atalho para um tipo de arquivo registrando um verbo estático para o tipo de arquivo. Para fazer isso, adicione uma subchave de **shell** abaixo da subchave do ProgID do aplicativo associado ao tipo de arquivo. Opcionalmente, você pode definir um verbo padrão para o tipo de arquivo, tornando-o o valor padrão da subchave **shell** .

O verbo padrão é exibido primeiro no menu de atalho. Seu objetivo é fornecer ao shell um verbo que possa ser usado quando a função [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) for chamada, mas nenhum verbo for especificado. O shell não seleciona necessariamente o verbo padrão quando **ShellExecuteEx** é usado dessa maneira.

O Shell usa o primeiro verbo disponível na seguinte ordem:

1.  O verbo padrão
2.  O primeiro verbo no registro, se a ordem de verbo for especificada
3.  O verbo **abrir**
4.  O verbo **abrir com**

Se nenhum dos verbos listados estiver disponível, a operação falhará.

Crie uma subchave para cada verbo que você deseja adicionar na subchave do Shell. Cada uma dessas subchaves deve ter um valor **reg \_ sz** definido como a cadeia de caracteres de exibição do verbo (cadeia de caracteres localizada). Para cada subchave de verbo, crie uma subchave de comando com o valor padrão definido para a linha de comando para ativar os itens. Para verbos canônicos, como **abrir** e **Imprimir**, você pode omitir a cadeia de caracteres de exibição porque o sistema exibe automaticamente uma cadeia de caracteres localizada corretamente. Para verbos noncanonal, se você omitir a cadeia de caracteres de exibição, a cadeia de caracteres de verbo será exibida.

No exemplo de registro a seguir, observe que:

-   Como **doit** não é um verbo canônico, ele recebe um nome de exibição, que pode ser selecionado pressionando a tecla D.
-   O verbo **Printto** não aparece no menu de atalho. No entanto, sua inclusão no registro permite que o usuário imprima arquivos soltando-os em um ícone de impressora.
-   Uma subchave é mostrada para cada verbo. **%1** representa o nome do arquivo e **%2** o nome da impressora.

```
HKEY_CLASSES_ROOT
   .myp-ms
      (Default) = MyProgram.1
      MyProgram.1
         (Default) = My Program Application
         Shell
            (Default) = doit
            doit
               (Default) = &Do It
               command
                  (Default) = c:\MyDir\MyProgram.exe /d "%1"
            open
               command
                  (Default) = c:\MyDir\MyProgram.exe /d "%1"
            print
               command
                  (Default) = c:\MyDir\MyProgram.exe /p "%1"
            printto
               command
                  (Default) = c:\MyDir\MyProgram.exe /p "%1" "%2"
```

O diagrama a seguir ilustra a extensão do menu de atalho de acordo com as entradas de registro acima. Este **menu de atalho abriu**, **faz** e **imprime** verbos em seu menu, com o que **é** o verbo padrão.

![captura de tela do menu de atalho do verbo padrão Do it](images/context-menu/context-doitdefaultverb.png)

### <a name="activating-your-handler-using-the-idroptarget-interface"></a>Ativando o manipulador usando a interface IDropTarget

Dados Dinâmicos Exchange (DDE) foi preterido; em vez disso, use [**IDropTarget.**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) **IDropTarget é** mais robusto e tem melhor suporte de ativação porque usa a ativação COM do manipulador. No caso de seleção de vários itens, **IDropTarget** não está sujeito às restrições de tamanho do buffer encontradas no DDE e [**no CreateProcess.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) Além disso, os itens são passados para o aplicativo como um objeto de dados que pode ser convertido em uma matriz de itens usando a função [**SHCreateShellItemArrayFromDataObject.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject) Isso é mais simples e não perde informações de namespace como ocorre quando o item é convertido em um caminho para protocolos DDE ou de linha de comando.

Para obter mais informações sobre [**consultas IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) e Shell para atributos de associação de arquivo, consulte [Tipos percebidos e Registro de aplicativo](fa-perceivedtypes.md).

### <a name="specifying-the-position-and-order-of-static-verbs"></a>Especificando a posição e a ordem dos verbos estáticos

Normalmente, os verbos são ordenados em um menu de atalho com base em como são enumerados; A enumeração é baseada primeiro na ordem da matriz de associação e, em seguida, na ordem dos itens na matriz de associação, conforme definido pela ordem de classificação do registro.

Os verbos podem ser ordenados especificando o valor padrão da sub-chave shell para a entrada de associação. Esse valor padrão pode incluir um único item, que será exibido na posição superior do menu de atalho ou uma lista de itens separados por espaços ou vírgulas. No último caso, o primeiro item na lista é o item padrão e os outros verbos são exibidos imediatamente abaixo dele na ordem especificada.

Por exemplo, a seguinte entrada do Registro produz verbos de menu de atalho na seguinte ordem:

1.  Exibir
2.  Gadgets
3.  Personalização

```
HKEY_CLASSES_ROOT
   DesktopBackground
      Shell
         Display
         Gadgets
         Personalization
```

Da mesma forma, a seguinte entrada do Registro produz verbos de menu de atalho na seguinte ordem:

1.  Personalização
2.  Gadgets
3.  Exibir

```
HKEY_CLASSES_ROOT
   DesktopBackground
      Shell = "Personalization,Gadgets"
      Display
```

### <a name="positioning-verbs-at-the-top-or-bottom-of-the-menu"></a>Posicionando verbos na parte superior ou inferior do menu

O atributo do Registro a seguir pode ser usado para colocar um verbo na parte superior ou inferior do menu. Se houver vários verbos que especificam esse atributo, o último a fazer isso obtém prioridade:

``` syntax
Position=Top | Bottom 
```

### <a name="creating-static-cascading-menus"></a>Criando menus em cascata estáticos

No Windows 7 e posteriores, há suporte para a implementação do menu em cascata por meio das configurações do Registro. Antes Windows 7, a criação de menus em cascata era possível apenas por meio da implementação da interface [**IContextMenu.**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) No Windows 7 e posteriores, você deve recorrer a soluções baseadas em código COM somente quando os métodos estáticos não são suficientes.

A captura de tela a seguir fornece um exemplo de um menu em cascata.

![captura de tela mostrando um exemplo de um menu em cascata](images/file-assoc/filecascademenu2ndex.png)

No Windows 7 e posterior, há três maneiras de criar menus em cascata:

-   [Criando menus em cascata com a entrada do Registro SubCommands](#creating-cascading-menus-with-the-subcommands-registry-entry)
-   [Criando menus em cascata com a entrada do Registro ExtendedSubCommandsKey](#creating-cascading-menus-with-the-extendedsubcommandskey-registry-entry)
-   [Criando menus em cascata com a interface IExplorerCommand](#creating-cascading-menus-with-the-iexplorercommand-interface)

### <a name="creating-cascading-menus-with-the-subcommands-registry-entry"></a>Criando menus em cascata com a entrada do Registro SubCommands

No Windows 7 e posteriores, você pode usar a entrada SubCommands para criar menus em cascata usando o procedimento a seguir.

**Para criar um menu em cascata usando a entrada SubCommands**

1.  Crie uma sub-chave no shell progID raiz de CLASSES **\_ \_** \\ *HKEY* \\  para representar o menu em cascata. Neste exemplo, damos a essa sub-chave o nome *CascadeTest*. Verifique se o valor padrão da sub-chave *CascadeTest* está vazio e mostrado como **(valor não definido).**

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest
                (Default)
    ```

2.  À sub-chave *CascadeTest,* adicione uma entrada MUIVerb do tipo **REG \_ SZ** e atribua a ela o texto que aparecerá como seu nome no menu de atalho. Neste exemplo, atribuímos a ele "Testar Menu em Cascata".

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest
                (Default)
                MUIVerb = Test Cascade Menu
    ```

3.  À sub-chave *CascadeTest,* adicione uma entrada SubCommands do tipo **REG \_ SZ** que é atribuída à lista, demlimited por ponto e vírgula, dos verbos que devem aparecer no menu, na ordem de aparência. Por exemplo, aqui atribuímos vários verbos fornecidos pelo sistema:

    ```
    HKEY_CLASSES_ROOT
       *
          Shell
             CascadeTest
                SubCommands
                Windows.delete;Windows.properties;Windows.rename;Windows.cut;Windows.copy;Windows.paste
    ```

4.  No caso de verbos personalizados, implemente-os usando qualquer um dos métodos de implementação de verbo estático e liste-os na sub-chave **CommandStore,** conforme mostrado neste exemplo para um *verbo fictício VerbName*:

    ```
    HKEY_LOCAL_MACHINE
       Software
          Microsoft
             Windows
                CurrentVersion
                   Explorer
                      CommandStore
                         Shell
                            VerbName
                            command
                               (Default) = notepad.exe %1
    ```

> [!Note]  
> Esse método tem a vantagem de que os verbos personalizados podem ser registrados uma vez e reutilizados listando o nome do verbo na entrada SubCommands. No entanto, ele exige que o aplicativo tenha permissão para modificar o registro em **HKEY \_ LOCAL \_ MACHINE.**

 

### <a name="creating-cascading-menus-with-the-extendedsubcommandskey-registry-entry"></a>Criando menus em cascata com a entrada do Registro ExtendedSubCommandsKey

No Windows 7 e posteriores, você pode usar a entrada ExtendedSubCommandKey para criar menus em cascata estendidos: menus em cascata em menus em cascata.

A captura de tela a seguir é um exemplo de um menu em cascata estendido.

![captura de tela mostrando o menu estendido em cascata para dispositivos](images/file-assoc/extendedsubcommandskey.png)

Como **o HKEY \_ CLASSES \_ ROOT** é uma combinação de **HKEY CURRENT \_ \_ USER** e **HKEY LOCAL \_ \_ MACHINE**, você pode registrar todos os verbos personalizados na sub-chave Classes de Software do USUÁRIO ATUAL do **\_ \_** \\  \\  HKEY. A principal vantagem de fazer isso é que a permissão elevada não é necessária. Além disso, outras associações de arquivo podem reutilizar todo esse conjunto de verbos especificando a mesma subkey ExtendedSubCommandsKey. Se você não precisar reutilizar esse conjunto de verbos, poderá listar os verbos sob o pai, mas garantir que o valor Padrão do pai esteja vazio.

**Para criar um menu em cascata usando uma entrada ExtendedSubCommandsKey**

1.  Crie uma sub-chave no shell progID raiz de CLASSES **\_ \_** \\ *HKEY* \\  para representar o menu em cascata. Neste exemplo, damos a essa sub-chave o nome *CascadeTest2*. Verifique se o valor padrão da sub-chave *CascadeTest* está vazio e mostrado como **(valor não definido).**

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest2
                (Default)
    ```

2.  À sub-chave *CascadeTest,* adicione uma entrada MUIVerb do tipo **REG \_ SZ** e atribua a ela o texto que aparecerá como seu nome no menu de atalho. Neste exemplo, atribuímos a ele "Testar Menu em Cascata".

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest
                (Default)
                MUIVerb = Test Cascade Menu 2
    ```

3.  Na sub-chave *CascadeTest* que você criou, adicione uma sub-chave **ExtendedSubCommandsKey** e adicione os subcommands do documento (do tipo **REG \_ SZ);** por exemplo:

    ```
    HKEY_CLASSES_ROOT
       txtfile
          Shell
             Test Cascade Menu 2
                (Default)
                ExtendedSubCommandsKey
                   Layout
                   Properties
                   Select all
    ```

    Verifique se o valor padrão da sub-chave *do Menu em Cascata de Teste 2* está vazio e mostrado como **(valor não definido)**.

4.  Preencha os subverbs usando qualquer uma das implementações de verbo estático a seguir. Observe que a sub-chave CommandFlags representa valores EXPCMDFLAGS. Se você quiser adicionar um separador antes ou depois do item de menu em cascata, use ECF \_ SEPARATORBEFORE (0x20) ou ECF \_ SEPARATORAFTER (0x40). Para obter uma descrição desses Windows 7 e sinalizadores posteriores, consulte [**IExplorerCommand::GetFlags**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-getflags). ECF \_ SEPARATORBEFORE funciona apenas para os itens de menu de nível superior. MUIVerb é do tipo **REG \_ SZ** e CommandFlags é do tipo **REG \_ DWORD**.

    ```
    HKEY_CLASSES_ROOT
       txtile
          Shell
             Test Cascade Menu 2
                (Default)
                ExtendedSubCommandsKey
                   Shell
                      cmd1
                         MUIVerb = Notepad
                         command
                            (Default) = %SystemRoot%\system32\notepad.exe %1
                      cmd2
                         MUIVerb = Wordpad
                         CommandFlags = 0x20
                         command
                            (Default) = "C:\Program Files\Windows NT\Accessories\wordpad.exe" %1
    ```

A captura de tela a seguir é uma ilustração dos exemplos de entrada de chave do Registro anteriores.

![captura de tela mostrando um exemplo de um menu em cascata mostrando opções de bloco de notas e wordpad](images/file-assoc/testcascademenu2.png)

### <a name="creating-cascading-menus-with-the-iexplorercommand-interface"></a>Criando menus em cascata com a interface IExplorerCommand

Outra opção para adicionar verbos a um menu em cascata é por [**meio de IExplorerCommand::EnumSubCommands**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-enumsubcommands). Esse método permite que fontes de dados que fornecem seus comandos de módulo de comando por meio [**de IExplorerCommandProvider**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider) usem esses comandos como verbos em um menu de atalho. No Windows 7 e posterior, você pode fornecer a mesma implementação de verbo usando [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) como você pode com [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu).

As duas capturas de tela a seguir ilustram o uso de menus em cascata na **pasta Dispositivos.**

![Captura de tela que mostra um exemplo de um menu em cascata na pasta dispositivos.](images/file-assoc/filecascademenu.png)

A captura de tela a seguir ilustra outra implementação de um menu em cascata na **pasta Dispositivos.**

![captura de tela mostrando um exemplo de um menu em cascata na pasta dispositivos](images/file-assoc/cascadedevices2.png)

> [!Note]  
> Como [**o IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) dá suporte apenas à ativação em processo, é recomendável usar por fontes de dados do Shell que precisam compartilhar a implementação entre comandos e menus de atalho.

 

### <a name="getting-dynamic-behavior-for-static-verbs-by-using-advanced-query-syntax"></a>Obter comportamento dinâmico para verbos estáticos usando sintaxe de consulta avançada

A AQS (Sintaxe De Consulta Avançada) pode expressar uma condição que será avaliada usando propriedades do item para o que o verbo está sendo instautado. Esse sistema funciona apenas com propriedades rápidas. Essas são propriedades relatadas pela fonte de dados do Shell tão rapidamente, não retornando [***SHCOLSTATE \_ SLOW****](/windows/win32/api/shtypes/ne-shtypes-shcolstate) de [**IShellFolder2::GetDefaultColumnState.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdefaultcolumnstate)

Windows 7 e posteriores suportam valores canônicos que evitam problemas em builds localizados. A sintaxe canônica a seguir é necessária em builds localizados para aproveitar esse aprimoramento Windows 7.

``` syntax
System.StructuredQueryType.Boolean#True
```

Na seguinte entrada de registro de exemplo:

-   O **valor AppliesTo** controla se o verbo é exibido ou oculto.
-   O valor DefaultAppliesTo controla qual verbo é o padrão.
-   O valor HasLUAShield controla se uma blindagem UAC (Controle de Conta de Usuário) é exibida.

Neste exemplo, o **valor DefaultAppliesTo** torna esse verbo o padrão para qualquer arquivo com a palavra "exampleText1" em seu nome de arquivo. O **valor AppliesTo** habilita o verbo para qualquer arquivo com "exampleText1" no nome. O **valor HasLUAShield** exibe o blindagem para arquivos com "exampleText2" no nome.

```
HKEY_CLASSES_ROOT
   txtile
      shell
         test.verb
            DefaultAppliesTo = System.ItemName:"exampleText1"
            HasLUAShield = System.ItemName:"exampleText2"
            AppliesTo = System.ItemName:"exampleText1"
```

Adicione **a** sub-chave Command e um valor:

```
HKEY_CLASSES_ROOT
   txtile
      shell
         test.verb
            Command
               (Default) = %SystemRoot%\system32\notepad.exe %1
```

No registro Windows 7, confira Unidade **\_ \_ RAIZ de CLASSES HKEY** como um exemplo de \\  verbos bitlocker que empregam a seguinte abordagem:

-   AppliesTo = System.Volume.BitlockerProtection:=2
-   System.Volume.BitlockerRequiresAdmin:=System.StructuredQueryType.Boolean \# True

Para obter mais informações sobre o AQS, consulte [Sintaxe de consulta avançada.](../search/-search-3x-advancedquerysyntax.md)

### <a name="deprecated-associating-verbs-with-dynamic-data-exchange-commands"></a>Preterido: associando verbos a Dados Dinâmicos Exchange comandos

A DDE foi preterida; em vez disso, use [**IDropTarget.**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) O DDE é preterido porque depende de uma mensagem de janela de difusão para descobrir o servidor DDE. Um servidor DDE trava a mensagem da janela de transmissão e, portanto, trava as conversas DDE para outros aplicativos. É comum que um único aplicativo preso cause falhas subsequentes em toda a experiência do usuário.

O método [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) é mais robusto e tem melhor suporte à ativação porque usa a ativação com do manipulador. No caso de seleção de vários itens, **IDropTarget** não está sujeito às restrições de tamanho de buffer encontradas no DDE e no [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa). Além disso, os itens são passados para o aplicativo como um objeto de dados que pode ser convertido em uma matriz de itens usando a função [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject) . Fazer isso é mais simples e não perde as informações de namespace, pois ocorre quando o item é convertido em um caminho para protocolos DDE ou de linha de comando.

Para obter mais informações sobre [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) e consultas de Shell para atributos de associação de arquivo, consulte [tipos observados e registro de aplicativo](fa-perceivedtypes.md).

## <a name="completing-verb-implementation-tasks"></a>Concluindo tarefas de implementação de verbo

As tarefas a seguir para implementar verbos são relevantes para as implementações de verbo estáticos e dinâmicos. Para obter mais informações sobre verbos dinâmicos, consulte [Personalizando um menu de atalho usando verbos dinâmicos](shortcut-menu-using-dynamic-verbs.md).

### <a name="customizing-the-shortcut-menu-for-predefined-shell-objects"></a>Personalizando o menu de atalho para objetos shell predefinidos

Muitos objetos de shell predefinidos têm menus de atalho que podem ser personalizados. Registre o comando praticamente da mesma maneira que você registra tipos de arquivo típicos, mas use o nome do objeto predefinido como o nome do tipo de arquivo.

Uma lista de objetos predefinidos está na seção *objetos do Shell predefinidos* da [criação de manipuladores de extensão do Shell](handlers.md). Esses objetos de shell predefinidos cujos menus de atalho podem ser personalizados com a adição de verbos no registro são marcados na tabela com o verbo do Word.

### <a name="extending-a-new-submenu"></a>Estendendo um novo submenu

quando um usuário abre o menu **arquivo** no Windows Explorer, um dos comandos exibidos é **novo**. A seleção desse comando exibe um submenu. Por padrão, o submenu contém dois comandos, **pasta** e **atalho**, que permitem aos usuários criar subpastas e atalhos. Esse submenu pode ser estendido para incluir comandos de criação de arquivo para qualquer tipo de arquivo.

Para adicionar um comando de criação de arquivo ao **novo** submenu, os arquivos do aplicativo devem ter um tipo de arquivo associado. Inclua uma subchave **ShellNew** sob o nome do arquivo. Quando o comando **novo** do menu **arquivo** é selecionado, o Shell adiciona o tipo de arquivo ao **novo** submenu. A cadeia de caracteres de exibição do comando é a cadeia de caracteres descritiva que é atribuída ao ProgID do programa.

Para especificar o método de criação de arquivo, atribua um ou mais valores de dados à subchave **ShellNew** . Os valores disponíveis são listados na tabela a seguir.



| Valor da subchave ShellNew | Descrição                                                                                                                                                              |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Comando               | Executa um aplicativo. Esse valor **reg \_ sz** especifica o caminho do aplicativo a ser executado. Por exemplo, você pode defini-lo para iniciar um assistente.                  |
| Dados                  | Cria um arquivo que contém os dados especificados. Esse **valor \_ binário reg** especifica os dados do arquivo. **Os dados** serão ignorados se **Nullfile** ou **filename** forem especificados. |
| FileName              | Cria um arquivo que é uma cópia de um arquivo especificado. Esse valor **reg \_ sz** especifica o caminho totalmente qualificado do arquivo a ser copiado.                                   |
| Valor nulo              | Cria um arquivo vazio. **Nullfile** não tem um valor atribuído. Se **Nullfile** for especificado, os valores de registro de **Data** e **filename** serão ignorados.                    |



 

O exemplo de chave do registro a seguir e captura de tela ilustram o **novo** submenu para o tipo de arquivo. MYP-MS. Ele tem um comando, **aplicativo myprogram**.

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
      MyProgram.1
         ShellNew
         NullFile
```

A captura de tela ilustra o **novo** submenu. Quando um usuário seleciona o **aplicativo myprogram** no **novo** submenu, o Shell cria um arquivo chamado **novo myprogram Application. MYP-ms** e o passa para **MyProgram.exe**.

![captura de tela do Windows Explorer mostrando um novo comando "aplicativo myprogram" no submenu "novo"](images/context-menu/context-myprogramexe.png)

### <a name="creating-drag-and-drop-handlers"></a>Criando manipuladores do tipo "arrastar e soltar"

O procedimento básico para implementar um manipulador de arrastar e soltar é o mesmo que para manipuladores de menu de atalho convencionais. No entanto, os manipuladores de menu de atalho normalmente usam apenas o ponteiro [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) passado para o método [**IShellExtInit:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) do manipulador para extrair o nome do objeto. Um manipulador de arrastar e soltar pode implementar um manipulador de dados mais sofisticado para modificar o comportamento do objeto arrastado.

Quando um usuário clica com o botão direito do mouse em um objeto Shell para arrastar um objeto, um menu de atalho é exibido quando o usuário tenta descartar o objeto. A captura de tela a seguir ilustra um menu de atalho típico do tipo "arrastar e soltar".

![captura de tela do menu de atalho arrastar e soltar](images/context-menu/context-dragdrop.png)

Um manipulador de arrastar e soltar é um manipulador de menu de atalho que pode adicionar itens a esse menu de atalho. Os manipuladores de arrastar e soltar normalmente são registrados na subchave a seguir.

```
HKEY_CLASSES_ROOT
   Directory
      shellex
         DragDropHandlers
```

Adicione uma subchave sob a subchave **DragDropHandlers** chamada para o manipulador de arrastar e soltar e defina o valor padrão da subchave como a forma de cadeia de caracteres do GUID do identificador de classe (CLSID) do manipulador. O exemplo a seguir habilita o manipulador de arrastar e soltar **MyDD** .

```
HKEY_CLASSES_ROOT
   Directory
      shellex
         DragDropHandlers
            MyDD
               (Default) = {MyDD CLSID GUID}
```

### <a name="suppressing-verbs-and-controlling-visibility"></a>Suprimindo verbos e controlando a visibilidade

você pode usar Windows configurações de política para controlar a visibilidade do verbo. Os verbos podem ser suprimidos por meio de configurações de política adicionando um valor de **SuppressionPolicy** ou um valor de GUID **SuppressionPolicyEx** à subchave do registro do verbo. Defina o valor da subchave **SuppressionPolicy** para a ID da política. Se a política for ativada, o verbo e sua entrada de menu de atalho associada serão suprimidos. Para obter possíveis valores de ID de política, consulte a enumeração de [**restrições**](/windows/desktop/api/shlobj_core/ne-shlobj_core-restrictions) .

### <a name="employing-the-verb-selection-model"></a>Empregando o modelo de seleção de verbo

Os valores do registro devem ser definidos para verbos para lidar com situações em que um usuário pode selecionar um único item, vários itens ou uma seleção de um item. Um verbo requer valores de registro separados para cada uma dessas três situações às quais o verbo dá suporte. Os valores possíveis para o modelo de seleção de verbo são os seguintes:

-   Especifique o valor de MultiSelectModel para todos os verbos. Se o valor de MultiSelectModel não for especificado, ele será inferido do tipo de implementação de verbo que você escolheu. Para métodos baseados em COM (como DropTarget e ExecuteCommand), o **Player** é assumido e, para os outros métodos, o **documento** é assumido.
-   Especifique **single** para verbos que dão suporte a apenas uma única seleção.
-   Especifique o **Player** para verbos que dão suporte a qualquer número de itens.
-   Especifique o **documento** para verbos que criam uma janela de nível superior para cada item. Isso limita o número de itens ativados e ajuda a evitar a execução de recursos do sistema se o usuário abrir muitas janelas.

Quando o número de itens selecionados não corresponde ao modelo de seleção de verbo ou é maior que os limites padrão descritos na tabela a seguir, o verbo não aparece.



| Tipo de implementação de verbo | Documento | Jogador    |
|-----------------------------|----------|-----------|
| Herdada                      | 15 itens | 100 itens |
| COM                         | 15 itens | Sem limite  |



 

Veja a seguir as entradas de registro de exemplo usando o valor MultiSelectModel.

```
HKEY_CLASSES_ROOT
   Folder
      shell
         open
             = MultiSelectModel = Document
```

```
HKEY_CLASSES_ROOT
   ProgID
      shell
         verb
             = MultiSelectModel = Single | Document | Player
```

### <a name="using-item-attributes"></a>Usando atributos de item

Os valores de sinalizador [**SFGAO**](sfgao.md) dos atributos de Shell de um item podem ser testados para determinar se o verbo deve ser habilitado ou desabilitado.

Para usar esse recurso de atributo, adicione os seguintes valores de **reg \_ DWORD** no verbo:

-   O valor AttributeMask especifica o valor de [**SFGAO**](sfgao.md) dos valores de bits da máscara com a qual testar.
-   O valor AttributeValue especifica o valor [**SFGAO**](sfgao.md) dos bits que são testados.
-   O ImpliedSelectionModel Especifica zero para verbos de item ou zero para verbos no menu de atalho de segundo plano.

Na entrada de registro de exemplo a seguir, o AttributeMask é definido como [**SFGAO \_ ReadOnly**](sfgao.md) (0x40000).

```
HKEY_CLASSES_ROOT
   txtfile
      Shell
         test.verb2
            AttributeMask = 0x40000
            AttributeValue = 0x0
            ImpliedSelectionModel = 0x0
            command
               (Default) = %SystemRoot%\system32\notepad.exe %1
```

### <a name="implementing-custom-verbs-for-folders-through-desktopini"></a>Implementando verbos personalizados para pastas por meio de Desktop.ini

no Windows 7 e posterior, você pode adicionar verbos a uma pasta por meio de Desktop.ini. Para obter mais informações sobre Desktop.ini arquivos, consulte [como personalizar pastas com Desktop.ini](how-to-customize-folders-with-desktop-ini.md).

> [!Note]  
> Desktop.ini arquivos devem ser sempre marcados como ocultos do **sistema** para que  +   não sejam exibidos aos usuários.

 

**Para adicionar verbos personalizados para pastas por meio de um arquivo Desktop.ini, execute as seguintes etapas:**

1.  Crie uma pasta marcada como **Somente leitura ou** **Sistema**.
2.  Crie um Desktop.ini que inclui um \[ . ShellClassInfo \] DirectoryClass=Folder ProgID.
3.  No Registro, crie o ProgID da Pasta RAIZ de **\_ CLASSES \_ HKEY** \\  com um valor de CanUseForDirectory. O valor CanUseForDirectory evita o uso indevido de ProgIDs definidos para não participar da implementação de verbos personalizados para pastas por meio de Desktop.ini.
4.  Adicione verbos na **sub-chave ProgID** da pasta, por exemplo:

    ```
    HKEY_CLASSES_ROOT
       CustomFolderType
          Shell
             MyVerb
                command
                   (Default) = %SystemRoot%\system32\notepad.exe %1\desktop.ini
    ```

> [!Note]  
> Esses verbos podem ser o verbo padrão; nesse caso, clicar duas vezes na pasta ativa o verbo.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Práticas recomendadas para manipuladores de menu de atalho e vários verbos de seleção](verbs-best-practices.md)
</dt> <dt>

[Escolhendo um verbo estático ou dinâmico para o menu de atalho](shortcut-choose-method.md)
</dt> <dt>

[Personalização de um menu de atalho usando verbos dinâmicos](shortcut-menu-using-dynamic-verbs.md)
</dt> <dt>

[Menus de atalho (contexto) e manipuladores de menu de atalho](context-menu.md)
</dt> <dt>

[Verbos e associações de arquivo](fa-verbs.md)
</dt> <dt>

[Referência de menu de atalho](context-menu-reference.md)
</dt> </dl>

 

 
