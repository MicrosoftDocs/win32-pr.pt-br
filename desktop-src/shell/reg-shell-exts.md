---
description: Um objeto de manipulador de extensão de Shell deve ser registrado antes que o Shell possa usá-lo. Este tópico é uma discussão geral sobre como registrar um manipulador de extensão de Shell.
ms.assetid: e4b98c18-746b-4909-8821-f25de9d15373
title: Registrando manipuladores de extensão do Shell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ca50bfaff984884b74ecc8572d4af9d96c55d0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968063"
---
# <a name="registering-shell-extension-handlers"></a>Registrando manipuladores de extensão do Shell

Um objeto de manipulador de extensão de Shell deve ser registrado antes que o Shell possa usá-lo. Este tópico é uma discussão geral sobre como registrar um manipulador de extensão de Shell.

Sempre que você criar ou alterar um manipulador de extensão de Shell, será importante notificar o sistema de que você fez uma alteração. Faça isso chamando [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify), especificando o evento **SHCNE \_ assocchanged** . Se você não chamar **SHChangeNotify**, a alteração poderá não ser reconhecida até que o sistema seja reinicializado.

Há alguns fatores adicionais que se aplicam aos sistemas Windows 2000. Para obter detalhes, consulte a seção [Registrando manipuladores de extensão de Shell em sistemas Windows 2000](#registering-shell-extension-handlers) .

Assim como com todos os objetos COM (Component Object Model), você deve criar um GUID para o manipulador usando uma ferramenta como Guidgen.exe, que é fornecida com o SDK (Software Development Kit) do Windows. Crie uma subchave em **HKEY \_ classes \_ raiz** \\ **CLSID** cujo nome é a forma de cadeia de caracteres desse GUID. Como os manipuladores de extensão do shell são servidores em processo, você também deve criar uma subchave **InprocServer32** na subchave GUID com o valor (padrão) definido como o caminho da dll do manipulador. Use o modelo de Threading Apartment. Um exemplo é mostrado aqui:

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



| Subchave                    | Description                                                          | Possíveis manipuladores                                |
|---------------------------|----------------------------------------------------------------------|--------------------------------------------------|
| **\** _                    | Todos os arquivos                                                            | Menu de atalho, folha de propriedades, verbos (veja abaixo) |
| _ *AllFileSystemObjects**  | Todos os arquivos e pastas de arquivos                                           | Menu de atalho, folha de propriedades, verbos             |
| **Pasta**                | Todas as pastas                                                          | Menu de atalho, folha de propriedades, verbos             |
| **Active**             | Pastas de arquivos                                                         | Menu de atalho, folha de propriedades, verbos             |
| **Plano de fundo do diretório \\** | Plano de fundo da pasta de arquivos                                               | Somente menu de atalho                               |
| **DesktopBackground**     | Plano de fundo da área de trabalho (Windows 7 e superior)                            | Menu de atalho, verbos                             |
| **Unidade**                 | Todas as unidades em MyComputer, como "C: \\ "                             | Menu de atalho, folha de propriedades, verbos             |
| **Rede**               | Rede inteira (em meus locais de rede)                             | Menu de atalho, folha de propriedades, verbos             |
| **Tipo de rede \\\\\#**     | Todos os objetos do tipo \# (veja abaixo)                                   | Menu de atalho, folha de propriedades, verbos             |
| **NetShare**              | Todos os compartilhamentos de rede                                                   | Menu de atalho, folha de propriedades, verbos             |
| **NetServer**             | Todos os servidores de rede                                                  | Menu de atalho, folha de propriedades, verbos             |
| *\_nome do provedor de rede \_* | Todos os objetos fornecidos pelo "*nome do \_ provedor \_ de rede*" do provedor de rede | Menu de atalho, folha de propriedades, verbos             |
| **Impressoras**              | Todas as impressoras                                                         | Menu de atalho, folha de propriedades                    |
| **AudioCD**               | CD de áudio na unidade de CD                                                 | Somente verbos                                       |
| **DVD**                   | Unidade de DVD (Windows 2000)                                             | Menu de atalho, folha de propriedades, verbos             |



 

### <a name="notes"></a>Observações

-   O menu de atalho de segundo plano da pasta de arquivo é acessado clicando com o botão direito do mouse em uma pasta de arquivo, mas não em qualquer conteúdo da pasta.
-   "Verbos" são comandos especiais registrados sob o verbo do Shell de subchave do **HKEY \_ classes \_ raiz** \\  \\  \\ .
-   Para o tipo de **rede** \\  \\ **\#** , " \# " é um código de tipo de provedor de rede em decimal. O código do tipo de provedor de rede é a palavra alta de um tipo de rede. A lista de tipos de rede é fornecida no arquivo de cabeçalho Winnetwk. h (WNNC \_ net \_ \* Values). Por exemplo, WNNC \_ net \_ Shiva é 0x00330000, portanto, a subchave de tipo correspondente seria tipo de rede **\_ \_ raiz de classes hKey** \\  \\  \\ **51**.
-   "*\_ \_ nome do provedor de rede*" é um nome de provedor de rede, conforme especificado por [**WNetGetProviderName**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetprovidernamea), com os espaços convertidos em sublinhados. Por exemplo, se o provedor de rede de rede da Microsoft estiver instalado, o nome do provedor será "rede do Microsoft Windows" e o *\_ \_ nome do provedor de rede* correspondente será a **\_ \_ rede do Microsoft Windows**.

## <a name="example-of-an-extension-handler-registration"></a>Exemplo de um registro de manipulador de extensão

Para habilitar um manipulador específico, crie uma subchave na subchave do tipo de manipulador de extensão com o nome do manipulador. O shell não usa o nome do manipulador, mas ele deve ser diferente de todos os outros nomes nessa subchave de tipo. Defina o valor padrão da subchave Name para a forma de cadeia de caracteres do GUID do manipulador.

O exemplo a seguir ilustra as entradas do registro que habilitam manipuladores de extensão de folha de propriedades e de menu de atalho, usando um tipo de arquivo. MYP de exemplo.

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

O procedimento de registro discutido nesta seção deve ser seguido para todos os sistemas Windows. No entanto, com os sistemas posteriores, uma etapa adicional pode ser necessária. Como essas versões posteriores do Windows são projetadas para serem usadas em um ambiente gerenciado, o acesso ao registro pode ser administrativamente restrito, exigindo uma abordagem um pouco diferente da instalação do que a descrita na seção anterior.

> [!Note]  
> Os programas de instalação geralmente não devem gravar diretamente no registro. Em vez disso, a instalação deve ser realizada com Windows Installer pacotes. Essas ferramentas garantem que o software seja executado bem e fornece acesso a recursos como registro de classe por usuário.

 

Os manipuladores de extensão do shell são executados no processo do Shell. Como é um processo do sistema, o administrador de um sistema pode limitar os manipuladores de extensão do Shell àqueles em uma lista aprovada definindo o valor de EnforceShellExtensionSecurity da chave do **Gerenciador** como 1, conforme mostrado aqui:

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

Para posicionar um manipulador de extensão de Shell na lista aprovada, crie um valor **reg \_ sz** cujo nome seja a forma de cadeia de caracteres do GUID do manipulador sob a subchave **aprovada** .

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Shell Extensions
                  Approved
```

Por exemplo, o exemplo a seguir adiciona os manipuladores *myCommand* e *MyPropSheet* à lista aprovada.

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

O shell não usa o valor atribuído ao GUID, mas deve ser definido para facilitar a inspeção do registro.

Seu aplicativo de instalação poderá adicionar valores à subchave **aprovada** somente se a pessoa que está instalando o aplicativo tiver privilégios suficientes. Se a tentativa de adicionar um manipulador de extensão falhar, você deverá informar ao usuário que privilégios administrativos são necessários para instalar totalmente o aplicativo. Se o manipulador for essencial para o aplicativo, você deverá falhar a instalação e notificar o usuário para entrar em contato com um administrador.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Inicializando manipuladores de extensão do Shell](int-shell-exts.md)
</dt> </dl>

 

 
