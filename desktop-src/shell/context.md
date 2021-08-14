---
description: Clicar com o botão direito do mouse em um objeto normalmente causa a exibição de um menu de atalho. Esse menu contém uma lista de comandos que o usuário pode selecionar para executar várias ações no objeto . Esta seção é uma introdução aos menus de atalho para objetos do sistema de arquivos.
ms.assetid: d951d1e8-0f88-49c4-8373-e6db0e18cd72
title: Estendendo menus de atalho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d046805ebc787f5cad2bfaa40538c51b826c3f0541f3ec1afad508202a4a25fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118460643"
---
# <a name="extending-shortcut-menus"></a>Estendendo menus de atalho

Clicar com o botão direito do mouse em um objeto normalmente causa a exibição de um *menu de atalho*. Esse menu contém uma lista de comandos que o usuário pode selecionar para executar várias ações no objeto . Esta seção é uma introdução aos menus de atalho para objetos do sistema de arquivos.

-   [Menus de atalho para objetos do sistema de arquivos](#shortcut-menus-for-file-system-objects)
-   [Verbos do menu de atalho](#shortcut-menu-verbs)
    -   [Verbos canônicos](#canonical-verbs)
    -   [Verbos estendidos](#extended-verbs)
-   [Estendendo o menu de atalho para um tipo de arquivo](#extending-the-shortcut-menu-for-a-file-type)
-   [Estendendo o menu de atalho para objetos shell predefinidos](#extending-the-shortcut-menu-for-predefined-shell-objects)
-   [Registrando um aplicativo para lidar com tipos de arquivo arbitrários](#registering-an-application-to-handle-arbitrary-file-types)
-   [Estendendo o novo submenu](#extending-the-new-submenu)

Informações adicionais estão disponíveis aqui:

-   [Como definir verbos estendidos](how-to-define-extended-verbs.md)
-   [Como associar verbos a comandos DDE](how-to-associate-verbs-with-dde-commands.md)

## <a name="shortcut-menus-for-file-system-objects"></a>Menus de atalho para objetos do sistema de arquivos

Quando um usuário clica com o botão direito do mouse em um objeto, como um arquivo, que é exibido no Windows Explorer ou na área de trabalho, um menu de atalho é exibido com uma lista de comandos. Em seguida, o usuário pode executar uma ação no arquivo, como abri-lo ou excluí-lo, selecionando o comando apropriado.

Como os menus de atalho geralmente são usados para gerenciamento de arquivos, o Shell fornece um conjunto de comandos padrão, como Recortar e Copiar, que aparecem no menu de atalho de qualquer arquivo. Observe que, embora Abrir com seja um comando padrão, ele não é exibido para alguns tipos de arquivo padrão, como .wav. A ilustração a seguir do diretório Meus Documentos de exemplo, que também foi usado como um exemplo em Personalização de [ícones](icon.md), mostra um menu de atalho padrão que foi exibido clicando com o botão direito do mouse MyDocs4.xyz.

![captura de tela do menu de atalho padrão para objetos do sistema de arquivos](images/context1.jpg)

O motivo pelo MyDocs4.xyz mostra um menu de atalho padrão é que ele não é membro de um tipo de [arquivo registrado](fa-file-types.md). Por outro lado, .txt é um tipo de arquivo registrado. Se você clicar com o botão direito do mouse em um dos arquivos .txt, verá um menu de atalho com dois comandos adicionais em sua seção superior: **Abrir** e **Imprimir**.

![captura de tela do menu de atalho personalizado para objetos do sistema de arquivos](images/context2.jpg)

Depois que um tipo de arquivo é registrado, você pode estender seu menu de atalho com comandos adicionais. Eles são exibidos acima dos comandos padrão quando qualquer arquivo desse tipo é clicado com o botão direito do mouse. Embora a maioria dos comandos adicionados dessa  maneira sejam comuns, como Imprimir ou Abrir **,** você pode adicionar qualquer comando que um usuário possa achar útil.

Tudo o que é necessário para estender o menu de atalho para um tipo de arquivo é criar uma entrada do Registro para cada comando. Uma abordagem mais sofisticada é implementar um manipulador de *menu* de atalho , que permite estender o menu de atalho para um tipo de arquivo em uma base de arquivo por arquivo. Para obter mais informações, consulte [Criando manipuladores de menu de contexto](context-menu-handlers.md).

## <a name="shortcut-menu-verbs"></a>Verbos do menu de atalho

Cada comando no menu de atalho é identificado no Registro pelo *verbo*. Esses verbos são os mesmos usados pelo [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) ao iniciar aplicativos programaticamente. Para obter mais informações sobre o uso do **ShellExecuteEx,** consulte a discussão em [Iniciando aplicativos](launch.md).

Um verbo é uma cadeia de caracteres de texto simples usada pelo Shell para identificar o comando associado. Cada verbo corresponde à cadeia de caracteres *de* comando usada para iniciar o comando em uma janela do console ou arquivo de lote (.bat). Por exemplo, o **verbo aberto** normalmente inicia um programa para abrir um arquivo. Sua cadeia de caracteres de comando normalmente tem esta aparência:

``` syntax
"My Program.exe" "%1"
```

"%1" é o espaço reservado padrão para um parâmetro de linha de comando fornecido com o nome de arquivo. Por exemplo, ele pode especificar uma página específica a ser exibida em uma exibição com guias.

> [!Note]  
> Se qualquer elemento da cadeia de caracteres de comando contiver ou contiver espaços, ele deverá ser entre aspas. Caso contrário, se o elemento contiver um espaço, ele não será analisado corretamente. Por exemplo, "Meu Program.exe" iniciará o aplicativo corretamente. Se você usar My Program.exe, o sistema tentará iniciar "My" com "Program.exe" como seu primeiro argumento de linha de comando. Você sempre deve usar aspas com argumentos como "%1" que são expandidos para cadeias de caracteres pelo Shell, porque não é possível ter certeza de que a cadeia de caracteres não conterá um espaço.

 

Os verbos também podem ter *uma* cadeia de caracteres de exibição associada a eles, que é exibida no menu de atalho em vez da própria cadeia de caracteres de verbo. Por exemplo, a cadeia de caracteres de **exibição para openas** é Abrir com. Assim como as cadeias de caracteres de menu normais, incluindo um & na cadeia de caracteres de exibição permite a seleção do teclado do comando.

### <a name="canonical-verbs"></a>Verbos canônicos

Em geral, os aplicativos são responsáveis por fornecer cadeias de caracteres de exibição localizadas para os verbos que eles definem. No entanto, para fornecer um grau de independência de idioma, o sistema define um conjunto padrão de verbos comumente usados chamados *verbos canônicos*. Um verbo canônico pode ser usado com qualquer idioma e o sistema gera automaticamente uma cadeia de caracteres de exibição localizada corretamente. Por exemplo, a cadeia **de** caracteres de exibição do verbo aberto será definida como Abrir em um sistema em inglês e como Öffnen em um sistema alemão.

Os verbos canônicos incluem:



| Valor      | Descrição                                                                                 |
|------------|---------------------------------------------------------------------------------------------|
| Abrir       | Abre o arquivo ou a pasta.                                                                   |
| Opennew    | Abre o arquivo ou a pasta em uma nova janela.                                                   |
| print      | Imprime o arquivo.                                                                            |
| explorar    | Abre Windows Explorer com a pasta selecionada.                                            |
| localizar       | Abre a **Windows caixa de diálogo Pesquisar** com a pasta definida como o local de pesquisa padrão. |
| openas     | Abre a **caixa de diálogo** Abrir com.                                                         |
| properties | Abre a folha de propriedades do objeto.                                                          |



 

O verbo printto também é canônico, mas nunca é exibido. Ele permite que o usuário imprima um arquivo arrastando-o para um objeto de impressora.

### <a name="extended-verbs"></a>Verbos estendidos

Quando o usuário clica com o botão direito do mouse em um objeto, o menu de atalho contém todos os verbos normais. No entanto, pode haver comandos aos quais você deseja dar suporte, mas que não foram exibidos em todos os menus de atalho. Por exemplo, você pode ter comandos que não são comumente usados ou que se destinam a usuários experientes. Por esse motivo, você também pode definir um ou mais *verbos estendidos.* Esses verbos também são cadeias de caracteres e são semelhantes aos verbos normais. Eles são diferenciados dos verbos normais pela maneira como são registrados. Para ter acesso aos comandos associados a verbos estendidos, o usuário deve clicar com o botão direito do mouse em um objeto ao pressionar a tecla SHIFT. Os verbos estendidos serão exibidos junto com os verbos normais.

## <a name="extending-the-shortcut-menu-for-a-file-type"></a>Estendendo o menu de atalho para um tipo de arquivo

A maneira mais simples de estender o menu de atalho para um tipo de arquivo é com o Registro. Para fazer isso, adicione uma **sub-chave** shell abaixo da chave para o ProgID do aplicativo associado ao tipo [de arquivo](fa-file-types.md). Opcionalmente, você pode definir um *verbo padrão* para o tipo de arquivo tornando-o o valor padrão da **sub-chave** shell.

O verbo padrão é exibido primeiro no menu de atalho. Sua finalidade é fornecer ao Shell um verbo que ele pode usar quando [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) é chamado, mas nenhum verbo é especificado. O Shell não seleciona necessariamente o verbo padrão quando **ShellExecuteEx** é usado dessa maneira. Para as versões do Shell [5.0](versions.md) e posteriores, encontradas no Windows 2000 e sistemas posteriores, o Shell usa o primeiro verbo disponível na lista a seguir. Se nenhum estiver disponível, a operação falhará.

-   O verbo aberto
-   O verbo padrão
-   O primeiro verbo no Registro
-   O verbo openwith

Para versões do Shell [anteriores à versão 5.0,](versions.md)omita o terceiro item.

Abaixo da **sub-chave** shell, crie uma sub-chave para cada verbo que você deseja adicionar. Cada uma dessas sub-chaves terá um valor **REG \_ SZ** definido como a cadeia de caracteres de exibição do verbo. Você pode omitir a cadeia de caracteres de exibição para verbos canônicos porque o sistema exibirá automaticamente uma cadeia de caracteres localizada corretamente. Se você omitir a cadeia de caracteres de exibição para verbos não não ínteegóricos, a cadeia de caracteres do verbo será exibida. Para cada subkey de verbo, crie uma sub-chave **de** comando com o valor padrão definido como a cadeia de caracteres de comando.

A ilustração a seguir mostra um menu de atalho para o tipo de arquivo .myp usado [em](fa-file-types.md) Tipos de Arquivo e [Ícones de Personalização](icon.md). Agora ele tem verbos open, doit, print e printto em seu menu de atalho, com doit como o verbo padrão. O menu de atalho tem esta aparência.

![captura de tela do menu de atalho personalizado](images/context3.jpg)

As entradas do Registro usadas para estender o menu de atalho mostrado na ilustração anterior são:

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   MyProgram.1
      (Default) = MyProgram Application
      Shell
         (Default) = doit
         open
            command
               (Default) = C:\MyDir\MyProgram.exe "%1"
         doit
            (Default) = &Do It
            command
               (Default) = C:\MyDir\MyProgram.exe /d "%1"
         print
            command
               (Default) = C:\MyDir\MyProgram.exe /p "%1"
         printto
            command
               (Default) = C:\MyDir\MyProgram.exe /p "%1" "%2" %3 %4
```

Embora o **comando Open With** seja acima do primeiro separador, ele é criado automaticamente pelo sistema e não requer uma entrada do Registro. O sistema cria automaticamente nomes de exibição para os verbos canônicos abertos e impressos. Como doit não é um verbo canônico, ele recebe um nome de exibição, "&Fazer Isso", que pode ser selecionado pressionando a tecla D. O verbo printto não aparece no menu de atalho, mas incluí-lo permite que o usuário imprima arquivos soltando-os em um ícone de impressora. Neste exemplo, %1 representa o nome do arquivo e %2 o nome da impressora.

Os verbos podem ser suprimidos por meio de configurações de política adicionando um valor SuppressionPolicy à chave do verbo. De definir o valor de SuppressionPolicy como a ID da política. Se a política estiver ligada, o verbo e sua entrada de menu de atalho associada serão suprimidos. Para possíveis valores de ID de política, consulte a [**enumeração RESTRICTIONS.**](/windows/desktop/api/shlobj_core/ne-shlobj_core-restrictions)

## <a name="extending-the-shortcut-menu-for-predefined-shell-objects"></a>Estendendo o menu de atalho para objetos shell predefinidos

Muitos objetos shell predefinidos têm menus de atalho que podem ser estendidos. Registre o comando da mesma maneira que você registra tipos de arquivo típicos, mas use o nome do objeto predefinido como o nome do tipo de arquivo.

Uma lista de objetos predefinidos pode ser encontrada na seção *Objetos shell predefinidos* de [Criando manipuladores de extensão de shell.](handlers.md) Esses objetos shell predefinidos cujos menus de atalho podem ser estendidos adicionando verbos no Registro são marcados na tabela com a palavra "Verbo".

## <a name="registering-an-application-to-handle-arbitrary-file-types"></a>Registrando um aplicativo para lidar com tipos de arquivo arbitrários

As seções anteriores deste documento discutiram como definir itens de menu de atalho para um tipo de arquivo específico. Entre outras coisas, definir o menu de atalho permite que você especifique como o aplicativo associado abre um membro do tipo de arquivo. No entanto, conforme discutido em Tipos de Arquivo [,](fa-file-types.md)os aplicativos também podem registrar um procedimento padrão separado a ser usado quando um usuário tenta usar seu aplicativo para abrir um tipo de arquivo que você não associou ao aplicativo. Este tópico é discutido aqui porque você registra o procedimento padrão da mesma maneira que registra itens de menu de atalho.

O procedimento padrão atende a duas finalidades básicas. Uma delas é especificar como seu aplicativo deve ser invocado para abrir um tipo de arquivo arbitrário. Você pode, por exemplo, usar um sinalizador de linha de comando para indicar que um tipo de arquivo desconhecido está sendo aberto. A outra finalidade é definir as várias características de um tipo de arquivo, como os itens de menu de atalho e o ícone. Se um usuário associar seu aplicativo a um tipo de arquivo adicional, esse tipo terá essas características. Se o tipo de arquivo adicional tiver sido associado anteriormente a outro aplicativo, essas características substituirão os originais.

Para registrar o procedimento padrão, coloque as mesmas chaves do Registro criadas para o ProgID do aplicativo na sub-chave do aplicativo de Aplicativos RAIZ **HKEY \_ \_ CLASSES** \\ . Você também pode incluir um valor FriendlyAppName para fornecer ao sistema um nome amigável para seu aplicativo. O nome amigável do aplicativo também pode ser extraído de seu arquivo executável, mas somente se o valor FriendlyAppName estiver ausente. O fragmento do Registro a seguir mostra um procedimento padrão de exemplo para MyProgram.exe que define um nome amigável e vários itens de menu de atalho. As cadeias de caracteres de comando incluem o sinalizador /a para notificar o aplicativo de que ele está abrindo um tipo de arquivo arbitrário. Se você incluir uma sub-chave **DefaultIcon,** deverá usar um ícone genérico.

```
HKEY_CLASSES_ROOT
   Applications
      MyProgram.exe
         FriendlyAppName = Friendly Name
         shell
            open
               command
                  (Default) = C:\MyDir\MyProgram.exe /a "%1"
            print
               command
                  (Default) = C:\MyDir\MyProgram.exe /a /p "%1"
            printto
               command
                  (Default) = C:\MyDir\MyProgram.exe /a /p "%1" "%2" %3 %4
```

## <a name="extending-the-new-submenu"></a>Estendendo o novo submenu

Quando um usuário abre o menu **Arquivo** no Windows Explorer, o primeiro comando é **Novo.** Selecionar esse comando exibe um submenu. Por padrão, ele contém dois comandos, **Pasta** e **Atalho,** que permitem que os usuários criem subpastas e atalhos. Esse submenu pode ser estendido para incluir comandos de criação de arquivo para qualquer tipo de arquivo.

Para adicionar um comando de criação de arquivo ao **submenu** [](fa-file-types.md) Novo, os arquivos do aplicativo devem ter um tipo de arquivo associado a eles. Inclua uma **sub-chave ShellNew** na chave para a extensão de nome de arquivo. Quando o **comando** Novo do menu **Arquivo** for selecionado, o Shell o adicionará **ao** submenu Novo. A cadeia de caracteres de exibição do comando será a cadeia de caracteres descritiva atribuída ao ProgID do programa.

Atribua um ou mais valores de dados à sub-chave **ShellNew** para especificar o método de criação de arquivo. Os valores disponíveis a seguir.



| Valor    | Descrição                                                                                                                                                   |
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Comando  | Executa um aplicativo. Esse é um **valor \_ REG SZ** que especifica o caminho do aplicativo a ser executado. Por exemplo, você pode defini-lo para iniciar um assistente. |
| Dados     | Cria um arquivo que contém dados especificados. Os dados são **um \_ valor BINARY** REG com os dados do arquivo. Os dados serão ignorados se NullFile ou FileName for especificado.  |
| FileName | Cria um arquivo que é uma cópia de um arquivo especificado. FileName é um **valor \_ REG SZ,** definido como o caminho totalmente qualificado do arquivo a ser copiado.                 |
| NullFile | Cria um arquivo vazio. NullFile não recebe um valor. Se NullFile for especificado, os valores Data e FileName serão ignorados.                                  |



 

A ilustração a seguir **mostra** o submenu Novo para o tipo de arquivo .myp usado como um exemplo em Tipos de Arquivo [e](fa-file-types.md) [Personalização de Ícones](icon.md). Agora ele tem um comando, **MyProgram Application**. Quando um usuário seleciona **MyProgram Application** no **submenu** Novo, o Shell cria um arquivo chamado "Novo MyProgram Application.myp" e o passa para MyProgram.exe.

![captura de tela do menu novo personalizado](images/context5.png)

A entrada do Registro agora é a seguinte:

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
      MyProgram.1
         ShellNew
            NullFile
   MyProgram.1
      (Default) = MyProgram Application
      DefaultIcon
         (Default) = C:\MyDir\MyProgram.exe,2
      Shell
         (Default) = doit
         open
            command
               (Default) = C:\MyDir\MyProgram.exe "%1"
         doit
            (Default) = &Do It
            command
               (Default) = C:\MyDir\MyProgram.exe /d "%1"
         print
            command
               (Default) = C:\MyDir\MyProgram.exe /p "%1"
         printto
            command
               (Default) = C:\MyDir\MyProgram.exe /p "%1" "%2" %3 %4
```

 

 



