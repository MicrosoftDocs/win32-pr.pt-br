---
description: Armazenamento de cadeias de caracteres embutidas em código no registro faz parte de um modelo de localização anterior ao Vista Windows.
ms.assetid: 70185942-7d32-4151-a4e1-f71cf45e87af
title: Usando o redirecionamento de cadeia de caracteres do registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30f0804d0586f8340e5a84e9da9c82ca39ffc30b55f72f4695d5216cbb26aab6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118389412"
---
# <a name="using-registry-string-redirection"></a>Usando o redirecionamento de cadeia de caracteres do registro

Armazenamento de cadeias de caracteres embutidas em código no registro faz parte de um modelo de localização anterior ao Vista Windows. Não há suporte para ele no MUI. No modelo atual, a interface do usuário para o sistema operacional é executada em arquivos de recursos específicos de idioma sobre uma base neutra de idioma. Os componentes do sistema operacional usam o registro de maneira neutra de linguagem.

O MUI usa apenas as cadeias de caracteres de registro redirecionadas definidas por recursos do Win32 PE no arquivo de recurso de idioma base. O redirecionamento é definido separadamente, por exemplo, em um arquivo. inf. Esse tipo de armazenamento permite que o carregador de recursos selecione os recursos de idioma corretos automaticamente durante o carregamento do módulo de recurso.

> [!Note]  
> Este tópico pertence apenas aos recursos do Win32 PE. Se você estiver usando recursos do PE não Win32, deverá fornecer redirecionamento de cadeia de caracteres de registro personalizado, se necessário.

 

## <a name="create-a-language-neutral-resource"></a>Criar um recurso de Language-Neutral

um aplicativo MUI em execução no Windows Vista e posterior usa um recurso de cadeia de caracteres com neutralidade de idioma para permitir o acesso a cadeias de caracteres específicas de idioma armazenadas em uma tabela de recursos de cadeia. O código do aplicativo que lê esses valores do registro é descrito na seção carregar um Language-Neutral valor do registro de [localizando cadeias de caracteres redirecionadas](locating-redirected-strings.md).

Os dados de um valor de registro com neutralidade de idioma têm o formato " `@<PE-path>,-<stringID>[;<comment>]` ", em que:

-   *PE-path* especifica o caminho do executável. Você pode especificar o caminho usando uma variável de ambiente, como% ProgramFiles%, para dar suporte à implantação. Uma alternativa para fazer sua referência de cadeia de caracteres é deixar as informações de caminho do arquivo. Nesse caso, seu aplicativo deve ter alguns meios, por exemplo, outro valor de registro, para comunicar seu próprio diretório de instalação.
-   *stringid* especifica o identificador de recurso numérico do recurso de cadeia de caracteres relevante, que é implementado assim como qualquer outro recurso de cadeia de caracteres localizável.
-   *Comentário* especifica informações opcionais para depuração ou legibilidade do valor do registro. As funções da API do registro ignoram o comentário ao carregar a cadeia de caracteres.

> [!Note]  
> Os dados para o valor do registro não fazem nenhuma referência explícita ao arquivo de recurso específico do idioma. O arquivo correto é determinado em tempo de execução, com base nas preferências de idioma da interface do usuário atual.

 

Um valor de registro é inserido sem um espaço entre "," e "-". Um valor correto do registro é:

`shell32.dll,-22912`

Um valor de registro incorreto é:

`shell32.dll, -22912`

um exemplo do Windows Vista é o valor do registro com os seguintes dados:

`@%SystemRoot%\system32\input.dll,-5020`

## <a name="create-resources-for-shortcut-strings"></a>Criar recursos para cadeias de caracteres de atalho

Quando o aplicativo MUI exibe seu nome na interface do usuário do Shell, uma cadeia de caracteres InfoTip é exibida para o ícone do aplicativo. Você deve criar recursos de cadeia de caracteres para o nome de exibição do aplicativo e a cadeia de caracteres InfoTip associada para cada idioma com suporte. Quando os recursos estiverem prontos, seu aplicativo poderá usar as cadeias de caracteres conforme descrito na seção usar API do Shell para carregar cadeias de caracteres de atalho da sessão de registro de [localizando cadeias de caracteres redirecionadas](locating-redirected-strings.md).

### <a name="prepare-resources-for-a-shortcut-created-with-windows-installer"></a>preparar recursos para um atalho criado com Windows Installer

se você usar Windows Installer (MSI) para criar um atalho, os recursos de cadeia de caracteres incluirão o nome de exibição e a descrição do atalho. Na [tabela de atalho MSI](../msi/shortcut-table.md), a DLL de recurso é referenciada nas colunas apropriadas e os identificadores de recurso para seu nome de exibição de atalho e descrição são usados nas colunas do identificador de recurso correspondente.

Para que o atalho do aplicativo funcione corretamente com a tecnologia de recursos do MUI, tenha em mente os seguintes pontos ao preparar as cadeias de caracteres de atalho:

-   Use variáveis de ambiente ou um caminho relativo para registrar a DLL. Você pode especificar @% SystemRoot% \\ system32shell32.dll contanto que \\ o tipo de cadeia de caracteres do registro seja reg \_ Expand \_ sz. O identificador de recurso de cadeia de caracteres para "documento de texto" em Shell32.dll é 12345.
-   Não use espaços em volta dos símbolos "," e "-". Um exemplo correto é "shell32.dll,-22912".
-   Não use um nome de arquivo curto. Esse tipo de nome não funciona com o carregador de recursos.

### <a name="prepare-resources-for-a-shortcut-using-inf-format"></a>Preparar recursos para um atalho usando o formato INF

Se você usar o formato de arquivo INF para criar cadeias de caracteres de atalho, o arquivo de recursos deverá fazer as seguintes configurações do registro. Essas instruções pressupõem o uso da sintaxe ProfileItems da API de instalação.

1.  Altere o valor de InfoTip para apontar para a referência de redirecionamento de cadeia de caracteres usando o caminho e o identificador de recurso.
2.  Adicione o novo valor DisplayResource nas seções de instalação do ProfileItems.

Veja a seguir um exemplo que mostra a adição do aplicativo Calculadora ao menu **Iniciar** :


```C++
[CalcInstallItems]
"Name" = %Calc_DESC%
"CmdLine" = 11, calc.exe
"SubDir" = %Access_GROUP%
"WorkingDir" = 11

"InfoTip" = "@%systemroot%\system32\shell32.dll,-22531"

"DisplayResource" = "%systemroot%\system32\shell32.dll",22019
```



Use a sintaxe mostrada abaixo ao usar o INF para adicionar itens, por exemplo, uma pasta de grupo de acesso, ao menu **Iniciar** . Essa sintaxe pressupõe o uso do \[ \] suporte StartMenuItems da instalação, semelhante à sintaxe usada em Syssetup. inf.


```C++
[StartMenuItems]
<description> = <binary>,<commandline>,<iconfile>,<iconnum>,<infotip>,<resDLL,resID>
```



Defina o valor *InfoTip* para a referência de cadeia de caracteres " `@<path>,-resID` ".

O nome de exibição é determinado pelos valores *resDLL* e *resID* . O valor *resID* especifica o identificador de recurso para um recurso de cadeia de caracteres associado ao arquivo de idioma neutro. O valor *resDLL* especifica o caminho para o arquivo de idioma neutro.

## <a name="create-resources-for-friendly-document-type-names"></a>Criar recursos para nomes de tipo de documento amigáveis

Você deve implementar o nome amigável e as cadeias de caracteres InfoTip para seu aplicativo como recursos de cadeia. Para permitir que nomes de tipo de documento amigáveis reajam ao idioma da interface do usuário, o aplicativo deve registrar os nomes usando o valor FriendlyTypeName na chave do identificador de programa para o tipo de arquivo. O valor padrão para a chave do identificador do programa deve ser mantido para manter a compatibilidade com versões anteriores. Para obter informações sobre como acessar os nomes do seu aplicativo, consulte os nomes de tipo de documento amigável da consulta na seção registro de [localizando cadeias de caracteres redirecionadas](locating-redirected-strings.md).

O trabalho específico envolve as seguintes etapas:

1.  Implemente o nome amigável e as cadeias de caracteres InfoTip como recursos de cadeia específicos do idioma.
2.  Adicione o valor FriendlyTypeName na chave do registro do tipo de documento. Os dados para o valor seguem o padrão " `@<path>,-<resID>` ", em que *Path* indica o executável e *resID* é o identificador de recurso de um recurso de cadeia de caracteres localizável associado a esse executável.
3.  Especifique o valor do registro InfoTip de acordo com o formato " `@<path>,-<resID>` ".

O exemplo a seguir mostra as configurações do registro para um arquivo de .txt:


```C++
HKCR\.txt
@="txtfile"
"Content Type"="text/plain"

HKCR\txtfile
@="Text Document"

"FriendlyTypeName" = "@%systemroot%\system32\shell32.dll,-12345"

"InfoTip" = "@%systemroot%\system32\shell32.dll,-12346"
```



## <a name="provide-resources-for-shell-verb-action-strings"></a>Fornecer recursos para cadeias de caracteres de ação de verbo do Shell

cadeias de caracteres de ação para determinados verbos, por exemplo, "abrir" e "editar", são mostradas no menu pop-up exibido quando o usuário clica com o botão direito do mouse em um arquivo no Windows Explorer. Seu aplicativo não precisa especificar cadeias de caracteres para verbos de shell comuns, pois o Shell tem seus próprios padrões habilitados para MUI para esses verbos. No entanto, você deve fornecer recursos de cadeia de caracteres localizáveis para cadeias que representam verbos não comuns.

em sistemas operacionais Windows XP, cadeias de caracteres para verbos de shell no registro são renderizadas usando a sintaxe a seguir, em que *verb* especifica o nome real do verbo:


```C++
HKCR\<progid>\shell\<verb>
@ = <friendly-name>
```



Veja um exemplo:


```C++
HKCR\Sample.app\shell\Disc
@ = "Disconnect"
```



no Windows XP e posterior, você pode usar um nível de indireção para fazer uma cadeia de caracteres de ação depender do idioma da interface do usuário. Esses sistemas operacionais dão suporte a um valor de MUIVerb para definição de uma cadeia de caracteres compatível com MUI. Aqui está um exemplo de uma entrada de registro para um verbo incomum:


```C++
HKCR\Sample.app\shell\Disc
@ = "Disconnect"
"MUIVerb" = "@%systemroot%\system32\sample.exe,-9875"
```



Seu aplicativo MUI também deve ser capaz de registrar o valor padrão antigo como uma cadeia de caracteres localizável, conforme mostrado abaixo:


```C++
HKCR\Sample.app\shell\Disc
@ = "@%systemroot%\system32\sample.exe,-9875"
```



> [!Note]  
> o registro do valor padrão antigo não é recomendado porque requer uma instalação diferente no Windows XP e posterior da instalação usada em sistemas operacionais anteriores.

 

## <a name="create-resources-for-verb-protocol-and-auxusertype-strings"></a>Criar recursos para cadeias de caracteres verbo, protocolo e AuxUserType

Você deve criar recursos de cadeia de caracteres localizáveis para sequências de verbo, protocolo e AuxUserType. Use as seguintes configurações do registro:


```C++
HKCR\CLSID\{<Your_CLSID>}\Verb\<number> @="<Your Verb>, <menu_flag>, <verb_flag>"
"LocalizedString"="@<resDLLpath\resDLL.DLL>,-resStrID"
...

HKCR\CLSID\{<Your_CLSID>}\AuxUserType\<number>
@="<Your Short Name>"
"LocalizedString"="@<resDLLpath\resDLL.DLL>,-resStrID1"
...

HKCR\<Your_Name>\protocol\StdFileEditing\verb\<number>
@="<Your Verb>"
"LocalizedString"="@<resDLLpath\resDLL.DLL>,-resStrID"
...
```



O valor especificado para a Localizadastring contém apenas ou substitui o valor para *o verbo*, não os dois valores de sinalizador.

Aqui está um resumo para ajudá-lo a garantir as configurações corretas do registro:

-   Se CLSID tiver uma \\ chave de inserção de CLSID \\ {CLSID} de HKCR \\ , defina o valor padrão de CLSID usando CLSID de HKCR \\ \\ {CLSID} \\ localizadastring.
-   Se CLSID tiver uma ou mais subchaves no \\ \\ verbo {CLSID} do CLSID \\ de HKCR, defina cada cadeia de caracteres de verbo individual usando o verbo do% \\ CLSID} de HKCR \\ \\ \\ XXX \\ .
-   Se CLSID tiver uma ou mais subchaves no \\ verbo de StdFileEditing do protocolo HKCR {ProgID} \\ \\ \\ , defina cada cadeia de caracteres de verbo individual usando o \\ protocolo HKCR {ProgID} \\ \\ StdFileEditing \\ verbo \\ XXX \\ localizadastring.
-   Se CLSID tiver uma ou mais subchaves AuxUserType listadas em \\ CLSID \\ de HKCR {CLSID} \\ AuxUserType, defina cada entrada AuxUserType usando o CLSID do HKCR \\ \\ {CLSID} \\ AuxUserType \\ XXX \\ .

## <a name="create-a-resource-for-the-uninstall-program"></a>Criar um recurso para o programa de desinstalação

para registrar o programa de desinstalação do aplicativo, você pode criar valores de registro na subchave do identificador exclusivo para o aplicativo na chave do registro HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ uninstall. os valores a serem definidos incluem: DisplayName, DisplayVersion, Publisher, ProductID, RegOwner, RegCompany, UrlInfoAbout, HelpTelephone, HelpLink, InstallLocation, installname, InstallDate, Contact, comments, DisplayIcon, Readme, UrlUpdateInfo.

> [!Note]  
> Para habilitar a tecnologia MUI para cada valor, você pode acrescentar " \_ localizado" ao nome do valor.

 

Os componentes do sistema operacional são necessários para fornecer um valor para DisplayName \_ localizado de uma maneira específica de MUI. Você deve posicionar o nome de exibição em uma DLL, como Res.dll, como um recurso de cadeia de caracteres, supondo que o identificador seja 1245. Em seguida, o aplicativo pode registrar o nome de exibição como DisplayName \_ localizado com o valor "@ \\res.DLL,-1245". Todas as outras configurações do registro devem ser mantidas como estão, incluindo o valor original para DisplayName.

## <a name="create-resources-for-sound-events"></a>Criar recursos para eventos de som

Windows associa determinados eventos a arquivos de som, por exemplo, um novo evento de notificação de email ou um evento de alarme de bateria crítica. Os nomes de evento devem ser exibidos pela interface do usuário e devem oferecer suporte à globalização. Portanto, você deve implementar um recurso de cadeia de caracteres localizável para a descrição de cada descrição de evento. Adicione um novo valor de registro para cada nome de evento, além do valor padrão embutido em código.

Faça o seguinte para habilitar um evento de som:

1.  Implemente a descrição como um recurso de cadeia de caracteres localizável.
2.  Adicione um novo valor de registro para o nome de exibição, além do valor padrão embutido em código. O layout do registro associado é mostrado abaixo:


```C++
HKCR\AppEvents\EventLabels
<event_name>
    (Default) REG_SZ "<description>"
    DispFileName REG_EXPAND_SZ "@<path>,-<resID>"
```



Se o shell não conseguir localizar ou recuperar o valor de DispFileName, ele usará a descrição padrão.

## <a name="create-resources-for-keyboard-layout-strings"></a>Criar recursos para cadeias de caracteres de layout do teclado

Se seu aplicativo implementa um layout de teclado, ele requer um recurso de cadeia de caracteres localizável para o nome do layout para exibição de tela, por exemplo, em listas de layouts de teclado. Cada layout de teclado tem uma chave do registro em HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ Control \\ teclado layouts.

Entre os valores dessa chave estão o texto do layout, um nome legível para compatibilidade com versões anteriores e o nome de exibição do layout. Os dados fornecidos para o nome de exibição de layout devem ser uma referência de cadeia de caracteres do formato " `@<path>,-resID` ", referindo-se a um recurso de cadeia de caracteres localizável associado ao layout do teclado.

Aqui está um exemplo de uma configuração de registro para o layout de teclado espanhol (Espanha):

`Layout Display Name=@%SystemRoot%\system32\input.dll,-5020`

## <a name="represent-ole-insert-object-common-dialog-strings"></a>Representar cadeias de diálogo comuns de objeto de inserção OLE

Você pode implementar o nome de exibição de um objeto OLE insertável como um recurso de cadeia de caracteres localizável associado ao código que implementa esse objeto. A [caixa de diálogo objeto de inserção OLE](/cpp/mfc/reference/coleinsertdialog-class) Obtém um nome de exibição da chave do registro do \\ CLSID \\ { *<GUID>* }, em que *GUID* identifica o identificador de classe de um objeto OLE que poderia ser inserido. Windows O Vista e posterior implementa esse tipo de objeto de forma localizável, usando um nome de exibição compatível com MUI que permite a personalização para o idioma da interface do usuário. por outro lado, os sistemas operacionais Windows Vista implementam o nome de exibição desse tipo de objeto usando o valor padrão da chave do registro correspondente. Normalmente, esse nome é um nome em inglês (Estados Unidos) ou um nome no idioma da interface do usuário padrão do sistema.

> [!Note]  
> Nem todos os objetos que correspondem a subchaves da chave do registro podem ser inseridos.

 

O valor padrão da chave do \\ CLSID de HKCR \\ { *<GUID>* } deve reter um nome legível para compatibilidade com versões anteriores. No entanto, ele também deve definir o valor de localizadores, no formato " `@<path>,-ResID` ", em que Path identifica o arquivo executável que implementa o objeto. O valor ResID especifica o identificador de recurso da cadeia de caracteres localizável para o nome de exibição.

Por exemplo, o script de registro para o objeto de clipe de mídia que poderia ser inserido inclui as seguintes linhas:


```C++
HKCR,"CLSID\%CLSID_Media_Clip%",,,"%default description%"
HKCR,"CLSID\%CLSID_Media_Clip%","LocalizedString",,"@%systemroot%\system32\mplay32.exe,-9217"
```



A primeira linha fornece compatibilidade com versões anteriores, colocando uma cadeia de texto simples no registro como um nome de exibição padrão. A segunda linha fornece acesso ao nome de exibição compatível com MUI. Indica o identificador de cadeia de caracteres armazenado em Mplay32.exe. A cadeia de caracteres com o identificador 9217 em Mplay32.exe pode ser associada a valores de recursos de cadeia de caracteres para qualquer número de idiomas. Seu nome em inglês (Estados Unidos) é "Media clip".

## <a name="create-string-resources-for-microsoft-management-console-snap-ins"></a>Criar recursos de cadeia de caracteres para o console de gerenciamento Microsoft Snap-Ins

Você deve criar um recurso de cadeia de caracteres localizável para cada snap-in do MMC (console de gerenciamento Microsoft) usado pelo seu aplicativo MUI. Como um snap-in faz parte de um console do, ele tem uma interface do usuário e deve ser globalizado para operar em mais de um idioma.

Na maior parte, os snap-ins do MMC geram os mesmos problemas de globalização e localização que o próprio aplicativo MUI. Um snap-in do MMC deve refletir seu nome no registro para exibição. A entrada do registro deve incluir uma referência indireta a um recurso de cadeia de caracteres localizável e uma cadeia de caracteres literal para compatibilidade com versões anteriores.

Cada snap-in do MMC tem uma chave do registro em HKEY \_ local \_ Machine \\ software \\ Microsoft \\ MMC \\ Snaps. Entre os valores dessa chave estão namestring, especificando um nome legível por humanos para compatibilidade com versões anteriores e NameStringIndirect, especificando uma referência indireta a um recurso de cadeia de caracteres localizável. Para NameStringIndirect, você deve fornecer uma referência de cadeia de caracteres no formato " `@<path>,-resID` ", representando um recurso de cadeia de caracteres localizável.

Por exemplo, você pode fazer a seguinte configuração para Mymmc.dll, em que 12345 é o identificador do recurso de cadeia de caracteres correspondente que contém o nome localizável do snap-in:


```C++
NameStringIndirect=@%systemroot%@c:\windir\system32\mymmc.dll,-12345
```



Alguns snap-ins registram outros valores de cadeia de caracteres do registro que o MMC não lê do registro. Para obter mais informações sobre como usar esses valores, consulte registrar o console de gerenciamento Microsoft Snap-In cadeias de caracteres não lidas do registro ao [Localizar cadeias de caracteres redirecionadas](locating-redirected-strings.md).

## <a name="create-string-resources-for-a-windows-service"></a>criar recursos de cadeia de caracteres para um serviço de Windows

embora um serviço de Windows normalmente tenha pouca ou nenhuma interface do usuário, ele deve exibir um nome em conformidade com o mui e geralmente fornece uma descrição específica de linguagem compatível com mui. a chave do registro que descreve um serviço de Windows dá suporte apenas ao valor DisplayName para o nome do serviço e o valor de descrição para a descrição do serviço.

Configurações para o serviço de Windows são feitas do aplicativo, conforme descrito em definir o nome de exibição e a descrição de um serviço de Windows do registro ao [localizar cadeias de caracteres redirecionadas](locating-redirected-strings.md). Se o seu aplicativo não definir os valores do registro para a interface do usuário do serviço, os valores no registro permanecerão definidos como Inglês, mesmo que a interface do usuário esteja em outro idioma.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Preparando recursos](preparing-resources.md)
</dt> <dt>

[Localizando cadeias de caracteres redirecionadas](locating-redirected-strings.md)
</dt> </dl>

 

 
