---
description: Um objeto de manipulador de extensão de Shell deve ser registrado antes que o Shell possa usá-lo. Este tópico é uma discussão geral sobre como registrar um manipulador de extensão de Shell.
ms.assetid: e4b98c18-746b-4909-8821-f25de9d15373
title: Registrando manipuladores de extensão do Shell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec883f6e843bdfbf663108c0acda123d786262916f4a347d9433e7fd5f77baca
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111206"
---
# <a name="registering-shell-extension-handlers"></a>Registrando manipuladores de extensão do Shell

Um objeto de manipulador de extensão de Shell deve ser registrado antes que o Shell possa usá-lo. Este tópico é uma discussão geral sobre como registrar um manipulador de extensão de Shell.

Sempre que você criar ou alterar um manipulador de extensão de Shell, será importante notificar o sistema de que você fez uma alteração. Faça isso chamando [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify), especificando o evento **SHCNE \_ assocchanged** . Se você não chamar **SHChangeNotify**, a alteração poderá não ser reconhecida até que o sistema seja reinicializado.

há alguns fatores adicionais que se aplicam aos sistemas Windows 2000. para obter detalhes, consulte a seção [registrando manipuladores de extensão de Shell em Windows de sistemas 2000](#registering-shell-extension-handlers) .

assim como com todos os objetos com (Component Object Model), você deve criar um GUID para o manipulador usando uma ferramenta como Guidgen.exe, que é fornecida com o Software Development Kit (SDK) do Windows. Crie uma subchave em **HKEY \_ classes \_ raiz** \\ **CLSID** cujo nome é a forma de cadeia de caracteres desse GUID. Como os manipuladores de extensão do shell são servidores em processo, você também deve criar uma subchave **InprocServer32** na subchave GUID com o valor (padrão) definido como o caminho da dll do manipulador. Use o modelo de Threading Apartment. Um exemplo é mostrado aqui:

```
HKEY_CLASSES_ROOT
   CLSID
      {00021500-0000-0000-C000-000000000046}
         InprocServer32
            (Default) = %windir%\System32\Example.dll
            ThreadingModel = Apartment
```

Sempre que o Shell executar uma ação que possa envolver um manipulador de extensão de Shell, ele verificará a subchave do registro apropriada. A subchave sob a qual um manipulador de extensão é registrado controla quando ele será chamado. Por exemplo, é uma prática comum ter um manipulador de menu de atalho chamado quando o Shell exibe um menu de atalho para um membro de um [tipo de arquivo](fa-file-types.md). Nesse caso, o manipulador deve ser registrado na subchave **ProgID** do tipo de arquivo.

Este tópico discute os seguintes assuntos:

-   [Nomes de manipuladores](#handler-names)
-   [Objetos de shell predefinidos](#predefined-shell-objects)
-   [Exemplo de um registro de manipulador de extensão](#example-of-an-extension-handler-registration)
    -   [Registrando manipuladores de extensão do Shell](#registering-shell-extension-handlers)
-   [Tópicos relacionados](#related-topics)

## <a name="handler-names"></a>Nomes de manipuladores

Para habilitar um manipulador de extensão de Shell, crie uma subchave com o nome da subchave do manipulador (veja abaixo) na subchave **shellex** do **ProgID** (para tipos de arquivo) ou o nome do tipo de objeto do Shell (para [ \_ \_ objetos shell predefinidos](handlers.md)).

Por exemplo, se você quisesse registrar um manipulador de extensão de menu de atalho para myprogram. 1, comece criando a seguinte subchave:

```
HKEY_CLASSES_ROOT
   MyProgram.1
      ShellEx
         ContextMenuHandlers
```

Para os seguintes manipuladores, crie uma subchave sob a subchave "nome da subchave do manipulador" denominada como a versão da cadeia de caracteres do identificador de classe (CLSID) da extensão do Shell. Várias extensões podem ser registradas sob o nome da subchave do manipulador criando várias subchaves.



| Manipulador                 | Interface          | Nome da subchave do manipulador       |
|-------------------------|--------------------|---------------------------|
| Manipulador de provedor de coluna | IColumnProvider    | **ColumnHandlers**        |
| Manipulador de menu de atalho   | IContextMenu       | **ContextMenuHandlers**   |
| Manipulador de Copyhook        | ICopyHook          | **CopyHookHandlers**      |
| Manipulador do tipo "arrastar e soltar"   | IContextMenu       | **DragDropHandlers**      |
| Manipulador de folha de propriedades  | IShellPropSheetExt | **PropertySheetHandlers** |



 

Para os seguintes manipuladores, o valor padrão da chave "nome da subchave do manipulador" é a versão da cadeia de caracteres do CLSID da extensão do Shell. Somente uma extensão pode ser registrada para esses manipuladores.



| Manipulador                 | Interface            | Nome da subchave do manipulador                        |
|-------------------------|----------------------|--------------------------------------------|
| Manipulador de dados            | IDataObject          | **DataHandler**                            |
| Descartar manipulador            | IDropTarget          | **DropHandler**                            |
| Manipulador de ícone            | IExtractIconA/W      | **IconHandler**                            |
| Manipulador de imagem em miniatura | Manipuladordeminiaturai   | **{E357FCCD-A995-4576-B01F-234630154E96}** |
| Manipulador de infodicas         | IQueryInfo           | **{00021500-0000-0000-C000-000000000046}** |
| Link do Shell (ANSI)       | IShellLinkA          | **{000214EE-0000-0000-C000-000000000046}** |
| Link do Shell (UNICODE)    | IShellLinkW          | **{000214F9-0000-0000-C000-000000000046}** |
| Armazenamento estruturado      | IStorage             | **{0000000B-0000-0000-C000-000000000046}** |
| Metadados                | IPropertySetStorage  | **PropertyHandler**                        |
| Fixar no menu iniciar       | IStartMenuPinnedList | **{a2a9545d-a0c2-42b4-9708-a0b2badd77c8}** |
| Fixar à barra de tarefas          |                      | **{90AA3A4E-1CBA-4233-B8BB-535773D48449}** |



 

As subchaves especificadas para adicionar **Pin ao menu iniciar** e **fixar à barra de tarefas** no menu de atalho de um item só são necessárias para tipos de arquivo que incluem a entrada [IsShortcut](./links.md) .

## <a name="predefined-shell-objects"></a>Objetos de shell predefinidos

O Shell define objetos adicionais na **\_ \_ raiz de classes hKey** que podem ser estendidas da mesma maneira que os tipos de arquivo. Por exemplo, para adicionar um manipulador de folha de propriedades para todos os arquivos, você pode se registrar na subchave **PropertySheetHandlers** .

```
HKEY_CLASSES_ROOT
   *
      shellex
         PropertySheetHandlers
```

A tabela a seguir fornece as várias subchaves da **\_ \_ raiz de classes hKey** em que os manipuladores de extensão podem ser registrados. Observe que muitos manipuladores de extensão não podem ser registrados em todas as subchaves listadas. Para obter mais detalhes, consulte a documentação do manipulador específico.



| Subchave                    | Descrição                                                          | Possíveis manipuladores                                |
|---------------------------|----------------------------------------------------------------------|--------------------------------------------------|
| **\***                    | Todos os arquivos                                                            | Menu de atalho, folha de propriedades, verbos (veja abaixo) |
| **AllFileSystemObjects**  | Todos os arquivos e pastas de arquivos                                           | Menu de Atalho, Folha de Propriedades, Verbos             |
| **Pasta**                | Todas as pastas                                                          | Menu de Atalho, Folha de Propriedades, Verbos             |
| **Diretório**             | Pastas de arquivo                                                         | Menu de Atalho, Folha de Propriedades, Verbos             |
| **Plano de \\ fundo do diretório** | Plano de fundo da pasta de arquivos                                               | Somente menu de atalho                               |
| **DesktopBackground**     | Tela de fundo da área de trabalho (Windows 7 e superior)                            | Menu de atalho, verbos                             |
| **Unidade**                 | Todas as unidades no MyComputer, como "C: \\ "                             | Menu de Atalho, Folha de Propriedades, Verbos             |
| **Rede**               | Rede inteira (em Meus Locais de Rede)                             | Menu de Atalho, Folha de Propriedades, Verbos             |
| **Tipo de \\ rede\\\#**     | Todos os objetos do \# tipo (veja abaixo)                                   | Menu de Atalho, Folha de Propriedades, Verbos             |
| **Netshare**              | Todos os compartilhamentos de rede                                                   | Menu de Atalho, Folha de Propriedades, Verbos             |
| **NetServer**             | Todos os servidores de rede                                                  | Menu de Atalho, Folha de Propriedades, Verbos             |
| *nome \_ do provedor de \_ rede* | Todos os objetos fornecidos pelo provedor de rede "*nome do provedor de \_ \_ rede*" | Menu de Atalho, Folha de Propriedades, Verbos             |
| **Impressoras**              | Todas as impressoras                                                         | Menu de Atalho, Folha de Propriedades                    |
| **Audiocd**               | CD de áudio na unidade de CD                                                 | Somente verbos                                       |
| **Dvd**                   | Unidade de DVD (Windows 2000)                                             | Menu de Atalho, Folha de Propriedades, Verbos             |



 

### <a name="notes"></a>Observações

-   O menu de atalho em segundo plano da pasta de arquivos é acessado clicando com o botão direito do mouse em uma pasta de arquivos, mas não sobre qualquer conteúdo da pasta.
-   "Verbos" são comandos especiais registrados em **HKEY \_ CLASSES \_ ROOT** \\ *Subkey* \\  \\ **Shell Verb**.
-   Para **Tipo** \\ **de Rede**, " " é um código de tipo de provedor de rede em \\ **\#** \# decimal. O código de tipo de provedor de rede é a palavra alta de um tipo de rede. A lista de tipos de rede é dada no arquivo de título Winnetwk.h (valores WNNC \_ \_ \* NET). Por exemplo, WNNC NET LTD é 0x00330000, portanto, a sub-chave de tipo correspondente \_ \_ seria **HKEY CLASSES ROOT \_ \_ Network** \\  \\ **Type** \\ **51**.
-   "*nome \_ do \_ provedor* de rede " é um nome de provedor de rede conforme especificado por [**WNetGetProviderName**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetprovidernamea), com os espaços convertidos em sublinhados. Por exemplo, se o provedor de rede de Rede da Microsoft estiver instalado, seu nome de provedor será "Microsoft Windows Network" e o nome do provedor de rede correspondente será **Microsoft \_ Windows \_ Network**. *\_ \_*

## <a name="example-of-an-extension-handler-registration"></a>Exemplo de um registro de manipulador de extensão

Para habilitar um manipulador específico, crie uma sub-chave na sub-chave de tipo de manipulador de extensão com o nome do manipulador. O Shell não usa o nome do manipulador, mas deve ser diferente de todos os outros nomes nessa sub-chave de tipo. De definir o valor padrão da sub-chave de nome para a forma de cadeia de caracteres do GUID do manipulador.

O exemplo a seguir ilustra as entradas do Registro que habilitam manipuladores de extensão de menu de atalho e folha de propriedades, usando um tipo de arquivo .myp de exemplo.

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   CLSID
      {00000000-1111-2222-3333-444444444444}
         InProcServer32
            (Default) = C:\MyDir\MyCommand.dll
            ThreadingModel = Apartment
      {11111111-2222-3333-4444-555555555555}
         InProcServer32
            (Default) = C:\MyDir\MyPropSheet.dll
            ThreadingModel = Apartment
   MyProgram.1
      (Default) = MyProgram Application
      Shellex
         ContextMenuHandler
            MyCommand
               (Default) = {00000000-1111-2222-3333-444444444444}
         PropertySheetHandlers
            MyPropSheet
               (Default) = {11111111-2222-3333-4444-555555555555}
```

### <a name="registering-shell-extension-handlers"></a>Registrando manipuladores de extensão do Shell

O procedimento de registro discutido nesta seção deve ser seguido para todos os Windows sistemas. No entanto, com sistemas posteriores, uma etapa adicional pode ser necessária. Como essas versões posteriores do Windows são projetadas para serem usadas em um ambiente gerenciado, o acesso ao Registro pode ser restrito administrativamente, exigindo uma abordagem um pouco diferente da descrita na seção anterior.

> [!Note]  
> Os programas de instalação geralmente não devem gravar diretamente no Registro. Em vez disso, a instalação deve ser realizada com Windows do Instalador. Essas ferramentas garantem que o software seja executado bem e fornece acesso a recursos como registro de classe por usuário.

 

Os manipuladores de extensão do Shell são executados no processo do Shell. Como se trata de um processo do sistema, o administrador de um sistema pode limitar manipuladores de extensão do Shell aos que estão em uma lista aprovada definindo o valor EnforceShellExtensionSecurity da chave **do Explorer** como 1, conforme mostrado aqui:

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Policies
                  Explorer
                     EnforceShellExtensionSecurity = 1
```

Para colocar um manipulador de extensão do Shell na lista aprovada, crie um valor **REG \_ SZ** cujo nome é a forma de cadeia de caracteres do GUID do manipulador na **sub-chave** Aprovado.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Shell Extensions
                  Approved
```

Por exemplo, o exemplo a seguir adiciona os *manipuladores MyCommand* e *MyPropSheet* à lista aprovada.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Shell Extensions
                  Approved
                     {00000000-1111-2222-3333-444444444444} = MyCommand
                     {11111111-2222-3333-4444-555555555555} = MyPropSheet
```

O Shell não usa o valor atribuído ao GUID, mas deve ser definido para facilitar a inspeção do Registro.

Seu aplicativo de instalação poderá adicionar valores **à** sub-chave Aprovado somente se a pessoa que está instalando o aplicativo tiver privilégios suficientes. Se a tentativa de adicionar um manipulador de extensão falhar, você deverá informar ao usuário que são necessários privilégios administrativos para instalar totalmente o aplicativo. Se o manipulador for essencial para o aplicativo, você deverá falhar na instalação e notificar o usuário para entrar em contato com um administrador.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Inicializando manipuladores de extensão do Shell](int-shell-exts.md)
</dt> </dl>

 

 
