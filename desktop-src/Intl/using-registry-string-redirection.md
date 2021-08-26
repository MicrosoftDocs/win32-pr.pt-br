---
description: Armazenamento cadeias de caracteres em código no Registro faz parte de um modelo de localização Windows Vista pré-codificado.
ms.assetid: 70185942-7d32-4151-a4e1-f71cf45e87af
title: Usando o redirecionamento de cadeia de caracteres do Registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 561bac55f59bd414002f5dcc0ce3611102a4effd
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122887408"
---
# <a name="using-registry-string-redirection"></a>Usando o redirecionamento de cadeia de caracteres do Registro

Armazenamento cadeias de caracteres em código no Registro faz parte de um modelo de localização Windows Vista pré-codificado. Não há suporte para ela na MUI. No modelo atual, a interface do usuário do sistema operacional é executado em arquivos de recurso específicos de linguagem sobre uma base neutra em idioma. Os componentes do sistema operacional usam o Registro de maneira neutra em idioma.

A MUI usa apenas cadeias de caracteres de registro redirecionadas definidas pelos recursos do Win32 PE no arquivo de recurso de linguagem base. O redirecionamento é definido separadamente, por exemplo, em um arquivo .inf. Esse tipo de armazenamento permite que o carregador de recursos selecione os recursos de idioma corretos automaticamente durante o carregamento do módulo de recurso.

> [!Note]  
> Este tópico refere-se apenas aos recursos do Win32 PE. Se estiver usando recursos pe não Win32, você deverá fornecer redirecionamento personalizado de cadeia de caracteres do Registro, se necessário.

 

## <a name="create-a-language-neutral-resource"></a>Criar um recurso Language-Neutral dados

Um aplicativo MUI em execução no Windows Vista e posterior usa um recurso de cadeia de caracteres com neutralidade de idioma para permitir o acesso a cadeias de caracteres específicas do idioma armazenadas em uma tabela de recursos de cadeia de caracteres. O código do aplicativo que lê esses valores do Registro é descrito na seção Carregar um valor Language-Neutral registro de localização de [cadeias de caracteres redirecionadas.](locating-redirected-strings.md)

Os dados de um valor de registro com neutralidade de idioma têm o formato " `@<PE-path>,-<stringID>[;<comment>]` ", em que:

-   *PE-path* especifica o caminho do executável. Você pode especificar o caminho usando uma variável de ambiente, como %ProgramFiles%, para dar suporte à implantação. Uma alternativa para fazer sua referência de cadeia de caracteres é deixar de fora as informações de caminho do arquivo. Nesse caso, seu aplicativo deve ter alguns meios, por exemplo, outro valor do Registro, para comunicar seu próprio diretório de instalação.
-   *stringID* especifica o identificador de recurso numérico do recurso de cadeia de caracteres relevante, que é implementado assim como qualquer outro recurso de cadeia de caracteres localizável.
-   *comment* especifica informações opcionais para depuração ou capacidade de leitura do valor do Registro. As funções da API do Registro ignoram o comentário ao carregar a cadeia de caracteres.

> [!Note]  
> Os dados do valor do Registro não fazem referência explícita ao arquivo de recurso específico do idioma. O arquivo correto é determinado em runtime, com base nas preferências atuais da linguagem da interface do usuário.

 

Um valor do Registro é inserido sem um espaço entre "," e "-". Um valor correto do Registro é:

`shell32.dll,-22912`

Um valor incorreto do Registro é:

`shell32.dll, -22912`

Um exemplo do Windows Vista é o valor do Registro com os seguintes dados:

`@%SystemRoot%\system32\input.dll,-5020`

## <a name="create-resources-for-shortcut-strings"></a>Criar recursos para cadeias de caracteres de atalho

Quando o aplicativo MUI exibe seu nome na interface do usuário do shell, uma cadeia de caracteres InfoTip é exibida para o ícone do aplicativo. Você deve criar recursos de cadeia de caracteres para o nome de exibição do aplicativo e a cadeia de caracteres infotip associada para cada idioma com suporte. Quando os recursos estão prontos, seu aplicativo pode usar as cadeias de caracteres, conforme descrito na seção Usar a API do Shell para carregar cadeias de caracteres de atalho do Registro de [Localizando cadeias de caracteres redirecionadas.](locating-redirected-strings.md)

### <a name="prepare-resources-for-a-shortcut-created-with-windows-installer"></a>Preparar recursos para um atalho criado com o Windows Instalador

Se você usar o Windows (MSI) para criar um atalho, os recursos de cadeia de caracteres incluirão o nome de exibição e a descrição do atalho. Na tabela de atalho [MSI](../msi/shortcut-table.md), a DLL de recurso é referenciada nas colunas apropriadas e os identificadores de recurso para o nome de exibição e a descrição do atalho são usados nas colunas correspondentes do identificador de recurso.

Para que o atalho do aplicativo funcione corretamente com a tecnologia de recursos da MUI, tenha os seguintes pontos em mente ao preparar as cadeias de caracteres de atalho:

-   Use variáveis de ambiente ou um caminho relativo para registrar a DLL. Você pode especificar @%systemroot% system32shell32.dll desde que o tipo de cadeia de caracteres do Registro \\ \\ seja REG EXPAND \_ \_ SZ. O identificador de recurso de cadeia de caracteres para "Documento de Texto" Shell32.dll é 12345.
-   Não use espaços em torno dos símbolos "," e "-". Um exemplo correto é "shell32.dll,-22912".
-   Não use um nome de arquivo curto. Esse tipo de nome não funciona com o carregador de recursos.

### <a name="prepare-resources-for-a-shortcut-using-inf-format"></a>Preparar recursos para um atalho usando o formato INF

Se você usar o formato de arquivo INF para criar cadeias de caracteres de atalho, o arquivo de recurso deverá fazer as seguintes configurações do Registro. Estas instruções presumem o uso da sintaxe ProfileItems da API de Instalação.

1.  Altere o valor infotip para apontar para a referência de redirecionamento de cadeia de caracteres, usando o caminho e o identificador de recurso.
2.  Adicione o novo valor DisplayResource nas seções de instalação profileItems.

Veja a seguir um exemplo mostrando a adição do aplicativo Calculadora **ao** menu Iniciar:


```C++
[CalcInstallItems]
"Name" = %Calc_DESC%
"CmdLine" = 11, calc.exe
"SubDir" = %Access_GROUP%
"WorkingDir" = 11

"InfoTip" = "@%systemroot%\system32\shell32.dll,-22531"

"DisplayResource" = "%systemroot%\system32\shell32.dll",22019
```



Use a sintaxe mostrada abaixo ao usar INF para adicionar itens, por exemplo, uma pasta grupo de acesso, **ao** menu Iniciar. Essa sintaxe pressupõe o uso do suporte a StartMenuItems da Instalação, semelhante à sintaxe usada \[ \] em Syssetup.inf.


```C++
[StartMenuItems]
<description> = <binary>,<commandline>,<iconfile>,<iconnum>,<infotip>,<resDLL,resID>
```



De definir a *infotip de valor* como a referência de cadeia de caracteres " `@<path>,-resID` ".

O nome de exibição é determinado pelos *valores resDLL* *e resID.* O *valor de resID* especifica o identificador de recurso para um recurso de cadeia de caracteres associado ao arquivo com neutralidade de idioma. O *valor resDLL* especifica o caminho para o arquivo com neutralidade de idioma.

## <a name="create-resources-for-friendly-document-type-names"></a>Criar recursos para nomes de tipo de documento amigáveis

Você deve implementar cadeias de caracteres de nome amigável e InfoTip para seu aplicativo como recursos de cadeia de caracteres. Para permitir que nomes de tipo de documento amigáveis reajam à linguagem de interface do usuário, o aplicativo deve registrar os nomes usando o valor FriendlyTypeName na chave do identificador do programa para o tipo de arquivo. O valor padrão para a chave do identificador do programa deve ser mantido para manter a compatibilidade com compatibilidade com backward. Para obter informações sobre como acessar os nomes de seu aplicativo, consulte a consulta Nomes de tipo de documento amigáveis na seção Registro de [Localizando cadeias de caracteres redirecionadas](locating-redirected-strings.md).

O trabalho específico envolve as seguintes etapas:

1.  Implemente o nome amigável e as cadeias de caracteres infotip como recursos de cadeia de caracteres específicos do idioma.
2.  Adicione o valor FriendlyTypeName na chave do Registro do tipo de documento. Os dados para o valor seguem o padrão " ", em que path indica que o executável e resID é o identificador de recurso de um recurso de cadeia de caracteres localizável associado `@<path>,-<resID>` a esse  executável. 
3.  Especifique o valor do Registro infotip de acordo com o formato " `@<path>,-<resID>` ".

O exemplo a seguir mostra as configurações do Registro para um .txt arquivo:


```C++
HKCR\.txt
@="txtfile"
"Content Type"="text/plain"

HKCR\txtfile
@="Text Document"

"FriendlyTypeName" = "@%systemroot%\system32\shell32.dll,-12345"

"InfoTip" = "@%systemroot%\system32\shell32.dll,-12346"
```



## <a name="provide-resources-for-shell-verb-action-strings"></a>Fornecer recursos para cadeias de caracteres de ação de verbo do shell

Cadeias de caracteres de ação para determinados verbos, por exemplo, "abrir" e "editar", são mostradas no menu pop-up exibido quando o usuário clica com o botão direito do mouse em um arquivo no Windows Explorer. Seu aplicativo não precisa especificar cadeias de caracteres para verbos de shell comuns, pois o shell tem seus próprios padrões habilitados para MUI para esses verbos. No entanto, você deve fornecer recursos de cadeia de caracteres localizáveis para cadeias de caracteres que representam verbos incomuns.

Em sistemas operacionais XP pré-Windows, cadeias de caracteres para verbos de shell no Registro são renderizadas usando a sintaxe a seguir, em que *verb* especifica o nome do verbo real:


```C++
HKCR\<progid>\shell\<verb>
@ = <friendly-name>
```



Aqui está um exemplo:


```C++
HKCR\Sample.app\shell\Disc
@ = "Disconnect"
```



No Windows XP e posterior, você pode usar um nível de indcisão para fazer com que uma cadeia de caracteres de ação dependa da linguagem de interface do usuário. Esses sistemas operacionais são compatíveis com um valor MUIVerb para definição de uma cadeia de caracteres compatível com MUI. Aqui está um exemplo de uma entrada do Registro para um verbo incomum:


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
> O registro do valor padrão antigo não é recomendado porque requer uma configuração diferente no Windows XP e posterior da configuração usada em sistemas operacionais anteriores.

 

## <a name="create-resources-for-verb-protocol-and-auxusertype-strings"></a>Criar recursos para cadeias de caracteres Verb, Protocol e AuxUserType

Você deve criar recursos de cadeia de caracteres localizáveis para cadeias de caracteres Verb, Protocol e AuxUserType. Use as seguintes configurações do Registro:


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



O valor especificado para LocalizedString contém apenas ou substitui o valor de *Seu Verbo,* não os dois valores de sinalizador.

Aqui está um resumo para ajudá-lo a garantir as configurações corretas do Registro:

-   Se CLSID tiver uma chave inserível CLSID {clsid} do HKCR, defina o valor \\ \\ CLSID padrão usando CLSID do \\ HKCR \\ \\ {clsid} \\ LocalizedString.
-   Se CLSID tiver uma ou mais sub-chaves em HKCR \\ CLSID {clsid} Verbo, defina cada cadeia de caracteres verbo individual usando \\ CLSID do \\ HKCR \\ \\ {clsid} \\ Verbo xxx \\ \\ LocalizedString.
-   Se CLSID tiver uma ou mais sub-chaves em HKCR {progid} Protocol Stdfileediting Verb, defina cada cadeia de caracteres de Verbo individual usando \\ \\ \\ \\ HKCR \\ {progid} \\ Protocol \\ Stdfileediting \\ Verb xxx \\ \\ LocalizedString.
-   Se CLSID tiver uma ou mais sub-chaves AuxUserType listadas em CLSID do HKCR \\ \\ {clsid} \\ AuxUserType, defina cada entrada AuxUserType usando CLSID do HKCR \\ \\ {clsid} \\ AuxUserType \\ xxx \\ LocalizedString.

## <a name="create-a-resource-for-the-uninstall-program"></a>Criar um recurso para o programa de desinstalação

Para registrar o programa de desinstalação para o aplicativo, você pode criar valores de Registro na sub-chave do identificador exclusivo para o aplicativo na chave do Registro HKEY \_ LOCAL MACHINE Software Microsoft Windows \_ \\ \\ \\ \\ CurrentVersion \\ Uninstall. Os valores a definir incluem: DisplayName, DisplayVersion, Publisher, ProductID, RegOwner, RegCompany, UrlInfoAbout, HelpTelephone, HelpLink, InstallLocation, InstallSource, InstallDate, Contact, Comments, DisplayIcon, Readme, UrlUpdateInfo.

> [!Note]  
> Para habilitar a tecnologia de MUI para cada valor, você pode anexar " \_ Localizado" ao nome do valor.

 

Os componentes do sistema operacional são necessários para fornecer um valor para DisplayName \_ Localizado de maneira específica da MUI. Você deve colocar o nome de exibição em uma DLL, como Res.dll, como um recurso de cadeia de caracteres, supondo que o identificador seja 1245. Em seguida, o aplicativo pode registrar o nome de exibição como DisplayName Localizado com o valor \_ "@ \\res.DLL,-1245". Todas as outras configurações do Registro devem ser mantidas como estão, incluindo o valor original para DisplayName.

## <a name="create-resources-for-sound-events"></a>Criar recursos para eventos de som

Windows associa determinados eventos a arquivos de som, por exemplo, um evento new mail notification ou um evento De alarme de bateria crítico. Os nomes de evento devem ser exibidos pela interface do usuário e devem dar suporte à globalização. Portanto, você deve implementar um recurso de cadeia de caracteres localizável para a descrição de cada descrição do evento. Adicione um novo valor de Registro para cada nome de evento, além do valor padrão em código.

Faça o seguinte para habilitar um evento de som:

1.  Implemente a descrição como um recurso de cadeia de caracteres localizável.
2.  Adicione um novo valor de Registro para o nome de exibição, além do valor padrão em código. O layout do Registro associado é mostrado abaixo:


```C++
HKCR\AppEvents\EventLabels
<event_name>
    (Default) REG_SZ "<description>"
    DispFileName REG_EXPAND_SZ "@<path>,-<resID>"
```



Se o shell não puder encontrar ou recuperar o valor de DispFileName, ele usará a descrição padrão.

## <a name="create-resources-for-keyboard-layout-strings"></a>Criar recursos para cadeias de caracteres de layout de teclado

Se seu aplicativo implementar um layout de teclado, ele exigirá um recurso de cadeia de caracteres localizável para o nome do layout para exibição de tela, por exemplo, em listas de layouts de teclado. Cada layout de teclado tem uma chave do Registro em HKEY \_ LOCAL \_ MACHINE System \\ \\ CurrentControlSet \\ Control Keyboard \\ Layouts.

Entre os valores dessa chave estão Texto de Layout, um nome acessível por humanos para compatibilidade com compatibilidade com backward e Nome de Exibição de Layout. Os dados fornecidos para o Nome de Exibição de Layout devem ser uma referência de cadeia de caracteres do formato " ", referindo-se a um recurso de cadeia de caracteres localizável associado `@<path>,-resID` ao layout do teclado.

Aqui está um exemplo de uma configuração de Registro para o layout do teclado espanhol (Espanha) :

`Layout Display Name=@%SystemRoot%\system32\input.dll,-5020`

## <a name="represent-ole-insert-object-common-dialog-strings"></a>Representar cadeias de diálogo comuns do objeto OLE Insert

Você pode implementar o nome de exibição de um objeto inserível OLE como um recurso de cadeia de caracteres localizável associado ao código que implementa esse objeto. A caixa de diálogo Objeto de Inserção [OLE](/cpp/mfc/reference/coleinsertdialog-class) obtém um nome de exibição da chave do Registro CLSID { GUID }, em que \\ \\ *&lt; &gt; GUID*  identifica o identificador de classe de um objeto OLE insereível. Windows O Vista e posterior implementam esse tipo de objeto de maneira localizável, usando um nome de exibição em conformidade com a MUI que permite a personalização para a linguagem de interface do usuário. Por outro lado, os sistemas operacionais Windows Vista previamente implementam o nome de exibição para esse tipo de objeto usando o valor padrão da chave do Registro correspondente. Normalmente, esse nome é um nome em inglês (Estados Unidos) ou um nome no idioma da interface do usuário padrão do sistema.

> [!Note]  
> Nem todos os objetos que correspondem a sub-chaves da chave do Registro são inseríveis.

 

O valor padrão da chave \\ CLSID { \\ *&lt; GUID &gt;*} do HKCR deve reter um nome acessível por humanos para compatibilidade com compatibilidade com backward. No entanto, ele também deve definir o valor LocalizedString, no formato " ", em que path identifica o arquivo executável que `@<path>,-ResID` implementa o objeto . O valor ResID especifica o identificador de recurso da cadeia de caracteres localizável para o nome de exibição.

Por exemplo, o script de registro para o objeto de Clipe de Mídia insereível inclui as seguintes linhas:


```C++
HKCR,"CLSID\%CLSID_Media_Clip%",,,"%default description%"
HKCR,"CLSID\%CLSID_Media_Clip%","LocalizedString",,"@%systemroot%\system32\mplay32.exe,-9217"
```



A primeira linha fornece compatibilidade com backward colocando uma cadeia de caracteres de texto simples no Registro como um nome de exibição padrão. A segunda linha fornece acesso ao nome de exibição em conformidade com a MUI. Indica o identificador de cadeia de caracteres armazenado em Mplay32.exe. A cadeia de caracteres com o identificador 9217 Mplay32.exe pode ser associada a valores de recurso de cadeia de caracteres para qualquer número de idiomas. Seu nome em inglês (Estados Unidos) é "Clipe de Mídia".

## <a name="create-string-resources-for-microsoft-management-console-snap-ins"></a>Criar recursos de cadeia de caracteres para Console de Gerenciamento Microsoft Snap-Ins

Você deve criar um recurso de cadeia de caracteres localizável para cada snap-in Console de Gerenciamento Microsoft (MMC) usado pelo aplicativo MUI. Como um snap-in faz parte de um console, ele tem uma interface do usuário e deve ser globalizado para operar em mais de uma linguagem.

Na maior parte do tempo, os snap-ins do MMC gera os mesmos problemas de globalização e localização que o próprio aplicativo MUI. Um snap-in do MMC deve refletir seu nome no Registro para exibição. A entrada do Registro deve incluir uma referência indireta a um recurso de cadeia de caracteres localizável e uma cadeia de caracteres literal para compatibilidade com backward.

Cada snap-in do MMC tem uma chave do Registro em HKEY \_ LOCAL MACHINE Software Microsoft \_ \\ \\ \\ MMC \\ SnapIns. Entre os valores dessa chave estão NameString, especificando um nome acessível por humanos para compatibilidade com compatibilidade com backward e NameStringIndirect, especificando uma referência indireta a um recurso de cadeia de caracteres localizável. Para NameStringIndirect, você deve fornecer uma referência de cadeia de caracteres do formato " ", representando um recurso de cadeia `@<path>,-resID` de caracteres localizável.

Por exemplo, você pode fazer a seguinte configuração para Mymmc.dll, em que 12345 é o identificador do recurso de cadeia de caracteres correspondente que contém o nome localizável do snap-in:


```C++
NameStringIndirect=@%systemroot%@c:\windir\system32\mymmc.dll,-12345
```



Alguns snap-ins registram outros valores de cadeia de caracteres do Registro que o MMC não lê do Registro. Para obter mais informações sobre como usar esses valores, consulte Registrar Console de Gerenciamento Microsoft Snap-In cadeias de caracteres não lidas do Registro em [Localizando cadeias de caracteres redirecionadas](locating-redirected-strings.md).

## <a name="create-string-resources-for-a-windows-service"></a>Criar recursos de cadeia de caracteres para um Windows serviço

Embora um serviço Windows normalmente tenha pouca ou nenhuma interface do usuário, ele deve exibir um nome compatível com a MUI e geralmente fornece uma descrição específica do idioma em conformidade com a MUI. A chave do Registro que descreve um serviço Windows dá suporte apenas ao valor DisplayName para o nome do serviço e o valor de Descrição para a descrição do serviço.

Configurações para o serviço Windows é feito com base no aplicativo, conforme descrito em Definir o nome de exibição e a descrição para um serviço Windows do Registro em [Localizando cadeias](locating-redirected-strings.md)de caracteres redirecionadas . Se o aplicativo não definir os valores do Registro para a interface do usuário do serviço, os valores no Registro permanecerão definidos como inglês, mesmo se a interface do usuário estiver em outro idioma.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Preparando recursos](preparing-resources.md)
</dt> <dt>

[Localizando cadeias de caracteres redirecionadas](locating-redirected-strings.md)
</dt> </dl>

 

 
