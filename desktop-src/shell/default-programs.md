---
description: Use programas padrão para definir a experiência do usuário padrão.
ms.assetid: 78cd05a4-df33-42b5-91b9-826ebce04a1d
title: Programas padrão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f1cd54afe23291c191fdd045ca3cb42b68361aa8f7f3d8ef431042cfe9f5c06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117861353"
---
# <a name="default-programs"></a>Programas padrão

Use **programas padrão** para definir a experiência do usuário padrão. Os usuários podem acessar os **programas padrão** no painel de controle ou diretamente no menu **Iniciar** . definir a ferramenta de [acesso do programa e padrões do computador (SPAD)](cpl-setprogramaccess.md) , a experiência dos padrões primários para usuários no Windows XP, agora é uma parte dos **programas padrão**.

> [!IMPORTANT]
> Este tópico não se aplica a Windows 10. A maneira como as associações de arquivo padrão funcionam em Windows 10. para obter mais informações, consulte a seção sobre **alterações em como Windows 10 trata os aplicativos padrão** nesta [postagem](https://blogs.windows.com/windowsexperience/2015/05/20/announcing-windows-10-insider-preview-build-10122-for-pcs/).

 

Quando um usuário define padrões de programa usando **programas padrão**, a configuração padrão aplica-se somente a esse usuário e não a outros usuários que podem usar o mesmo computador. **os programas padrão** fornecem um conjunto de APIs (preteridas no Windows 8) que permitem que fornecedores independentes de software (ISVs) incluam seus programas ou aplicativos no sistema de padrões. O conjunto de APIs também ajuda os ISVs a gerenciar melhor seu status como padrões.

Este tópico é organizado da seguinte maneira:

-   [Introdução aos programas padrão e seu conjunto de API relacionado](#introduction-to-default-programs-and-its-related-api-set)
-   [Registrando um aplicativo para uso com programas padrão](#registering-an-application-for-use-with-default-programs)
    -   [ProgIDs](#progids)
    -   [Descrições de subchave e valor do registro](#registration-subkey-and-value-descriptions)
    -   [RegisteredApplications](#registeredapplications)
    -   [Exemplo de registro completo](#full-registration-example)
-   [Tornando-se o navegador padrão](#becoming-the-default-browser)
-   [Interface do usuário de programas padrão](#default-programs-ui)
-   [Práticas recomendadas para o uso de programas padrão](#best-practices-for-using-default-programs)
    -   [Durante a instalação](#during-installation)
    -   [Após a instalação](#after-installation)
-   [Recursos adicionais](#additional-resources)
-   [Tópicos relacionados](#related-topics)

## <a name="introduction-to-default-programs-and-its-related-api-set"></a>Introdução aos programas padrão e seu conjunto de API relacionado

Os **programas padrão** são projetados principalmente para aplicativos que usam tipos de arquivo padrão, como .mp3 ou .jpg arquivos ou protocolos padrão, como http ou mailto. Os aplicativos que usam seus próprios protocolos proprietários e associações de arquivos normalmente não usam a funcionalidade de **programas padrão** .

Depois de registrar um aplicativo para a funcionalidade de **programas padrão** , as seguintes opções e funcionalidades estão disponíveis usando o conjunto de API:

-   Restaure todos os padrões registrados para um aplicativo. Preterido por Windows 8.
-   Restaurar um único padrão registrado para um aplicativo. Preterido por Windows 8.
-   Consulta para o proprietário de um padrão específico em uma única chamada em vez de Pesquisar o registro. Você pode consultar o padrão de uma associação de arquivo, um protocolo ou um verbo canônico do menu **Iniciar** .
-   Inicie uma interface do usuário para um aplicativo específico em que um usuário pode definir padrões individuais.
-   Remova todas as associações por usuário.

**Os programas padrão** também fornecem uma interface do usuário que permite registrar um aplicativo a fim de fornecer informações adicionais ao usuário. Por exemplo, um aplicativo assinado digitalmente pode incluir uma URL para o home page do fabricante.

o uso do conjunto de apis associado pode ajudar um aplicativo a funcionar corretamente no recurso de controle de conta de usuário (UAC) introduzido no Windows Vista. No UAC, um administrador aparece no sistema como um usuário padrão, de modo que o administrador não possa, normalmente, gravar na subárvore do **\_ \_ computador local hKey** . Essa restrição é um recurso de segurança que impede que um processo atue como administrador sem o conhecimento do administrador.

A instalação de um programa por um usuário geralmente é executada como um processo elevado. No entanto, as tentativas de um aplicativo para modificar os comportamentos de associação padrão em uma pós-instalação no nível do computador não serão bem-sucedidas. Em vez disso, os padrões devem ser registrados em um nível por usuário, o que impede que vários usuários substituam os padrões uns dos outros.

A estrutura hierárquica do registro para associações de arquivo e protocolo fornece precedência para padrões por usuário em padrões de nível de máquina. Alguns aplicativos incluem pontos em seu código que elevam temporariamente seus direitos quando eles afirmam padrões registrados no **\_ \_ computador local hKey**. Esses aplicativos poderão apresentar resultados inesperados se outro aplicativo já estiver registrado como o padrão por usuário. O uso de **programas padrão** impede essa ambiguidade e garante os resultados esperados em um nível por usuário.

## <a name="registering-an-application-for-use-with-default-programs"></a>Registrando um aplicativo para uso com programas padrão

Esta seção mostra as subchaves e os valores do registro necessários para registrar um aplicativo com **programas padrão**. Ele inclui um exemplo completo.

Esta seção contém os seguintes tópicos:

-   [ProgIDs](#progids)
-   [Descrições de subchave e valor do registro](#registration-subkey-and-value-descriptions)
-   [RegisteredApplications](#registeredapplications)
-   [Exemplo de registro completo](#full-registration-example)

Os **programas padrão** exigem que cada aplicativo registre explicitamente as associações de arquivo, associações de MIME e protocolos para os quais o aplicativo deve ser listado como um padrão possível. Registre as associações usando os seguintes elementos do registro, que são explicados em detalhes posteriormente neste tópico em [descrições de subchave de registro e valor](#registration-subkey-and-value-descriptions):

```
HKEY_LOCAL_MACHINE
   %ApplicationCapabilityPath%
      ApplicationDescription
      ApplicationName
      Hidden
      FileAssociations
         .file-extension1
         .file-extension2
         ...
         .file-extensionX
      MIMEAssociations
         MIME
      Startmenu
         StartmenuInternet
         Mail
      UrlAssociations
         url-scheme
   SOFTWARE
      RegisteredApplications
         Unique Application Name = %ApplicationCapabilityPath%
```

O exemplo a seguir mostra as entradas do registro para um navegador da Contoso fictício chamado WebBrowser:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Contoso
         WebBrowser
            Capabilities
               ApplicationDescription = This award-winning Contoso browser is better than ever. Search the Internet and find exactly what you want in just seconds. Use integrated tabs and new phishing detectors to enhance your Internet experience.
               FileAssociations
                  .htm = ContosoHTML
                  .html = ContosoHTML
                  .shtml = ContosoHTML
                  .xht = ContosoHTML
                  .xhtml = ContosoHTML
               Startmenu
                  StartmenuInternet = Contoso.exe
               UrlAssociations
                  http = Contoso.Url.Http
                  https = Contoso.Url.Https
                  ftp = Contoso.Url.ftp
   SOFTWARE
      RegisteredApplications
         Contoso.WebBrowser.1.06 = SOFTWARE\Contoso\WebBrowser\Capabilities
```

### <a name="progids"></a>ProgIDs

Um aplicativo deve fornecer um [ProgID](fa-progids.md)específico. Certifique-se de incluir todas as informações que normalmente são gravadas na subchave padrão genérica para a extensão. Por exemplo, o player de mídia fictício do fictícia fornece as classes de software de **\_ \_ computador local de hKey locais** de aplicativo \\  \\  \\ **LitwarePlayer11.AssocFile.MP3** subchave. Essa subchave inclui todas as informações na subchave padrão genérica **HKEY \_ local \_ Machine** \\ **software** \\ **classes** \\ **.mp3** mais todas as informações adicionais que você deseja que o aplicativo registre. Isso garante que, se o usuário restaurar a associação de .mp3 para o Litware Player, as informações do Litware Player ficarão intactas e não foram substituídas por outro aplicativo. (A substituição poderá ocorrer se a subchave padrão for a única fonte dessas informações.)

Quando você mapeia um ProgID para uma extensão de nome de arquivo ou protocolo, um aplicativo pode mapear um-para-um ou um para muitos. No exemplo da Contoso, ContosoHTML aponta para um único ProgID que fornece informações de ShellExecute para as extensões .htm, .html,. shtml,. XHT e. xhtml. Como existe um ProgID diferente para cada protocolo, quando você usa protocolos, você habilita cada protocolo para ter sua própria cadeia de caracteres de execução.

Quando o tipo MIME pode ser exibido embutido em um navegador, o ProgID do tipo MIME deve conter a subchave **CLSID** que usa o CLSID (identificador de classe) do aplicativo correspondente. Esse CLSID é usado em uma pesquisa em relação ao CLSID no banco de dados MIME que é armazenado em **HKEY \_ local \_ Machine** \\ **software** \\ **classes** \\  \\ tipo de conteúdo de **banco de dados** MIME \\ . Se o tipo MIME não se destina a ser exibido embutido em um navegador, essa etapa poderá ser omitida.

### <a name="registration-subkey-and-value-descriptions"></a>Descrições de subchave e valor do registro

Esta seção descreve as subchaves de registro individuais e os valores usados no registro de um aplicativo com **programas padrão**, conforme ilustrado anteriormente.

### <a name="capabilities"></a>Funcionalidades

A subchave **Capabilities** contém todas as informações de **programas padrão** para um aplicativo específico. O espaço reservado% ApplicationCapabilityPath% refere-se ao caminho do registro de **HKEY \_ Current \_ User** ou **HKEY \_ local \_ Machine** à subchave de **funcionalidades** do aplicativo. Essa subchave contém os valores significativos mostrados na tabela a seguir.



| Valor                  | Type                       | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------------------|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ApplicationDescription | REG \_ sz ou reg \_ Expand \_ sz | **Obrigatório**. Para permitir que um usuário faça uma escolha de atribuição padrão informada, um aplicativo deve fornecer uma cadeia de caracteres que descreva os recursos do aplicativo. Embora o exemplo anterior da Contoso atribua a descrição diretamente ao valor ApplicationDescription, os aplicativos normalmente fornecem a descrição como um recurso que é inserido em um arquivo de .dll para facilitar a localização. Se ApplicationDescription não for fornecido, o aplicativo não aparecerá em listas de IU de programas padrão potenciais.                                                            |
| ApplicationName        | REG \_ sz ou reg \_ Expand \_ sz | **Opcional.** O nome pelo qual o programa aparece na interface do usuário de programas padrão. Se esses dados não forem fornecidos pelo aplicativo, o nome do programa executável associado ao primeiro ProgID registrado para o aplicativo será usado na interface do usuário. ApplicationName deve sempre corresponder ao nome registrado em [RegisteredApplications](#registeredapplications). Você pode usar ApplicationName se desejar diferentes tipos de aplicativo, como um navegador e um cliente de email, para apontar para o mesmo arquivo executável enquanto eles aparecem como nomes diferentes.<br/> |
| Hidden                 | REG \_ DWORD                 | **Opcional.** Defina esse valor como 1 para suprimir o aplicativo da lista de programas na caixa de diálogo **definir programas padrão** . Se esse valor for 0 ou não estiver presente, o aplicativo aparecerá na lista normalmente.                                                                                                                                                                                                                                                                                                                                                              |



 

### <a name="fileassociations"></a>FileAssociations

A **subchava FileAssociations** contém associações de arquivo específicas que são reivindicadas pelo aplicativo. Essas declarações são armazenadas como valores, com um valor para cada extensão. As associações apontam para um ProgID específico do aplicativo em vez de um ProgID genérico. No entanto, todas as associações não são necessárias para apontar para o mesmo ProgID.

### <a name="mimeassociations"></a>MIMEAssociations

A **subchava MIMEAssociations** contém tipos MIME específicos que são reivindicados pelo aplicativo. Essas declarações são armazenadas como valores, com um valor para cada tipo MIME. O nome do valor para cada tipo MIME deve corresponder exatamente ao nome MIME armazenado no banco de dados MIME. O valor também deve ser atribuído a um ProgID específico do aplicativo que contém o CLSID correspondente do aplicativo.

### <a name="startmenu"></a>Startmenu

A **subchava Startmenu** está associada às entradas de **Internet** e email atribuíveis **pelo** **usuário** no menu Iniciar. Um aplicativo deve se registrar separadamente como um candidato para essas entradas. Para obter mais informações, consulte [Registrando programas com tipos de cliente](reg-middleware-apps.md).

> [!Note]  
> A partir Windows 7, não há mais entradas de **Internet** e **email** **no** menu Iniciar. Os dados do Registro  associados à entrada de email ainda são usados para o cliente MAPI padrão, mas os dados do Registro associados à entrada da **Internet** não são usados pelo Windows.

 

Associando o **registro** do menu Iniciar  de um aplicativo ao registro de Programas Padrão, o aplicativo aparece como um padrão potencial na interface do usuário Definir **associações.** Se o usuário tiver escolhido o aplicativo como o padrão e, em seguida, optar por restaurar todos os padrões de aplicativo posteriormente, o aplicativo será restaurado para sua posição de **menu** Iniciar para esse usuário. Para obter mais informações e uma ilustração, consulte a [seção Interface](#default-programs-ui) do usuário de Programas Padrão mais adiante neste tópico.

A subchava **Startmenu** tem duas entradas: StartMenuInternet e Mail,  que correspondem às posições canônicas de **Internet** e email no **menu** Iniciar. Um aplicativo atribui a StartMenuInternet ou Mail um valor igual ao nome da subchava registrada do aplicativo em **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Clients** \\ **StartMenuInternet** ou **HKEY LOCAL \_ \_ MACHINE** \\ **SOFTWARE** \\  \\ **Clients Mail** (conforme [](reg-middleware-apps.md)descrito em Registrando programas com tipos de cliente ).

No caso da posição **canônica** de email no **menu** Iniciar, ele representa o cliente MAPI padrão e, portanto, é assumido capaz de entregar chamadas MAPI. Em Windows 7, embora não haja  mais uma posição canônica de email no **menu** Iniciar, essa subchava continua sendo usada para o cliente MAPI padrão. Um aplicativo que reivindica o padrão de email deve se registrar como um manipulador MAPI na seguinte subchava:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            CanonicalName
```

Se um cliente de email não puder dar suporte  ao MAPI, mas ainda quiser disputar a posição canônica do **menu** Iniciar email, ele poderá registrar uma linha de comando na seguinte subchava:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            CanonicalName
               shell
                  open
                     command
```

Além disso, em **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Clients** \\ **Mail** \\ *CanonicalName,* adicione um valor padrão com o nome do aplicativo.

Essas entradas permitem que o aplicativo seja lançado na **posição** de **email do** menu Iniciar. Observe que as chamadas MAPI ainda são feitas para o aplicativo e se enquadram no manipulador MAPI anterior ou falham se nenhum manipulador MAPI foi definido. Para obter mais informações, consulte [Registrando programas com tipos de cliente](reg-middleware-apps.md).

### <a name="urlassociations"></a>UrlAssociations

A **subchava UrlAssociations** contém os protocolos de URL específicos que são reivindicados pelo aplicativo. Essas declarações são armazenadas como valores, com um valor para cada protocolo. Cada protocolo deve apontar para um ProgID específico do aplicativo em vez de para um ProgID genérico. Conforme mencionado no exemplo da Contoso, você pode usar um ProgID diferente para cada protocolo para que cada um tenha sua própria cadeia de caracteres de execução.

### <a name="registeredapplications"></a>RegisteredApplications

A sub-chave completa **para RegisteredApplications** é:

**HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **RegisteredApplications**

Essa sub-chave fornece ao sistema operacional o local do Registro das **informações de Programas Padrão** para o aplicativo. O local é armazenado como um valor cujo nome deve corresponder ao nome do aplicativo.

### <a name="full-registration-example"></a>Exemplo de registro completo

Este exemplo mostra as sub-chaves e os valores usados no registro do player de mídia litware fictício. O exemplo inclui as entradas ProgID para mostrar como tudo se encaixa.

A sub-chave a seguir mostra o ProgID específico do aplicativo para o tipo .mp3 MIME:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         LitwarePlayer11.MIME.MP3
            CLSID
               (Default) = {CD3AFA76-B84F-48F0-9393-7EDC34128127}
```

Em seguida, está o ProgID específico do aplicativo que associa o programa Litware à extensão .mp3 nome de arquivo.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         LitwarePlayer11.AssocFile.MP3
            (Default) = MP3 Format Sound
            DefaultIcon
               (Default) = %ProgramFiles%\Litware\litware.dll, 0
            shell
               open
                  command
                     (Default) = %ProgramFiles%\Litware\litware.exe
```

As entradas a seguir mostram o ProgID combinado para a extensão de nome de arquivo e .mpeg MIME.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         LitwarePlayer11.AssocFile.MPG
            (Default) = Movie Clip
            CLSID
               (Default) = {D92B76F4-CFA0-4b93-866B-7730FEB4CD7B}
            DefaultIcon
               (Default) = %ProgramFiles%\Litware\litware.dll, 0
            shell
               open
                  command
                     (Default) = %ProgramFiles%\Litware\litware.exe
```

As próximas entradas registram o programa Litware em **Programas Padrão** e usam os ProgIDs registrados anteriormente

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Litware
         LitwarePlayer
            Capabilities
               ApplicationDescription = The new Litware Media Player breaks new ground in exciting fictional programs.
               FileAssociations
                  .mp3 = LitwarePlayer11.AssocFile.MP3
                  .mpeg = LitwarePlayer11.AssocFile.MPG
               MimeAssociations
                  audio/mp3 = LitwarePlayer11.MIME.MP3
                  audio/mpeg = LitwarePlayer11.AssocFile.MPG
```

Por fim, este exemplo registra o local do registro de Programas **Padrão** da Litware.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      RegisteredApplications
         Litware Player = Software\Litware\LitwarePlayer\Capabilities
```

## <a name="becoming-the-default-browser"></a>Tornando-se o navegador padrão

O registro do navegador deve seguir as práticas recomendadas descritas neste tópico. Quando o navegador é instalado, Windows pode apresentar ao usuário uma notificação do sistema por meio da qual o usuário pode selecionar o navegador como o padrão do sistema. Essa notificação é mostrada quando essas condições são atendidas:

-   O instalador do navegador chama [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) com o sinalizador **\_ SHCNE ASSOCCHANGED** para Windows que novos manipuladores de protocolo foram registrados.
-   Windows detecta que um ou mais aplicativos novos foram registrados para lidar com protocolos http:// e https:// e o usuário ainda não foi notificado. Em outras palavras, nenhuma das seguintes palavras foi mostrada ao usuário: uma notificação do sistema anunciando o aplicativo, um flyout OpenWith que contém o aplicativo ou a página de Painel de Controle SET User Defaults (LTD) para o aplicativo.

O exemplo a seguir mostra o código de registro recomendado que o instalador do navegador deve executar depois de escrever suas chaves do Registro.

[**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) primeiro notifica o sistema de que novas opções de associação estão disponíveis. A **chamada SHChangeNotify** é necessária para garantir o funcionamento adequado dos padrões do sistema.

Em [**seguida,**](/windows/win32/api/synchapi/nf-synchapi-sleep) uma instrução Sleep permite tempo para que os processos do sistema processem a notificação.


```C++
void NotifySystemOfNewRegistration()
{
    SHChangeNotify(SHCNE_ASSOCCHANGED, SHCNF_DWORD | SHCNF_FLUSH, nullptr, nullptr);
    Sleep(1000);
}
```



Se o usuário ignorar ou ignorar a notificação ou o flyout resultante sem fazer uma nova seleção de navegador padrão, o navegador padrão permanecerá inalterado. Observe que o usuário também pode alterar o navegador padrão a qualquer momento por meio de outros mecanismos, incluindo Definir Padrões de Usuário no Painel de Controle.

## <a name="default-programs-ui"></a>Interface do usuário de programas padrão

As ilustrações nesta seção mostram a interface do usuário para **Programas Padrão,** conforme visto pelo usuário.

A ilustração a seguir mostra a **janela principal Programas** Padrão Painel de Controle.

![captura de tela da página de entrada de programas padrão](images/defaultprogramsmain.png)

Quando um usuário escolhe a **opção Definir seus programas padrão,** a janela a seguir é exibida. Os usuários podem usar essa página para atribuir um programa padrão para todos os tipos de arquivo e protocolos para os quais o programa é um padrão possível. Conforme mostrado na ilustração a seguir, todos [os programas](#registering-an-application-for-use-with-default-programs) registrados e o ícone do programa aparecem na caixa **Programas** à esquerda.

![captura de tela da página definir seus programas padrão](images/setyourdefaultprograms.png)

Quando o usuário seleciona um programa na lista, o ícone do programa e o provedor são exibidos. Se a URL for inserida no certificado assinado digitalmente do programa, o programa também poderá exibir uma URL. Programas que não são assinados digitalmente não podem exibir uma URL.

Texto descritivo, que é fornecido pelo programa durante o registro, também é exibido. Esse texto é necessário. Abaixo da caixa de descrição há uma indicação de quantos padrões o programa está atribuído no momento do número completo que está registrado para manipular.

Para atribuir ou restaurar um programa como o padrão para todos os arquivos e protocolos para os quais ele está registrado, o usuário clica na opção Definir este programa **como** padrão.

Para atribuir tipos de arquivo individuais e protocolos  a um programa, o usuário clica na opção Escolher padrões para este programa, que exibe uma janela Definir associações para um programa como a ilustração **a** seguir.

> [!Note]  
> Recomendamos que  você chame Definir associações para um programa usando [**IApplicationAssociationRegistrationUI::LaunchAdvancedAssociationUI**](/windows/desktop/api/Shobjidl/nf-shobjidl-iapplicationassociationregistrationui-launchadvancedassociationui).

 

![captura de tela das assocações definidas para uma página do programa](images/setassociationsforaprogram.png)

## <a name="best-practices-for-using-default-programs"></a>Práticas recomendadas para usar programas padrão

Esta seção fornece diretrizes de melhores práticas para usar **programas padrão** ao registrar aplicativos. Ele também oferece sugestões de design para criar um aplicativo que fornece aos usuários a funcionalidade ideal **de Programas** Padrão.

### <a name="during-installation"></a>Durante a instalação

Além dos procedimentos de instalação normalmente realizados no Windows XP, um aplicativo baseado no  Windows Vista ou posterior deve se registrar com o recurso Programas Padrão para aproveitar sua funcionalidade.

Execute a sequência de etapas a seguir durante a instalação. As etapas 1 a 3 corresponderão às etapas que foram usadas no Windows XP; A etapa 4 era nova no Windows Vista.

1.  Instale os arquivos binários necessários.
2.  Escreva ProgIDs em HKEY \_ LOCAL \_ MACHINE. Observe que os aplicativos devem criar ProgIDs específicos do aplicativo para suas associações.
3.  Registre o aplicativo com **Programas Padrão,** conforme explicado anteriormente em [Registrando um aplicativo para uso com programas padrão.](#registering-an-application-for-use-with-default-programs)

### <a name="after-installation"></a>Após a instalação

Esta seção discute como o prompt de aplicativo deve primeiro apresentar suas opções padrão para cada usuário. Ele também discute como um aplicativo pode monitorar seu status como o padrão para suas possíveis associações e protocolos.

### <a name="first-run-experiences"></a>Primeira experiência de executar

Quando o aplicativo é executado por um usuário pela primeira vez, é recomendável que o aplicativo exibe a interface do usuário para o usuário que normalmente inclui essas duas opções:

-   Aceite as configurações padrão do aplicativo. Essa opção é habilitada por padrão.
-   Personalize as configurações padrão do aplicativo.

Antes do Windows 8, se o usuário aceita as configurações padrão, seu aplicativo chama [**IApplicationAssociationRegistration::SetAppAsDefaultAll**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-setappasdefaultall), que converte todas as associações de nível de computador declaradas durante a instalação em configurações por usuário para esse usuário.

Se o usuário decidir personalizar as configurações, seu aplicativo [**chamará IApplicationAssociationRegistrationUI::LaunchAdvancedAssociationUI**](/windows/desktop/api/Shobjidl/nf-shobjidl-iapplicationassociationregistrationui-launchadvancedassociationui) para exibir a interface do usuário de associação de arquivo. A ilustração a seguir mostra essa janela para o player de mídia da Litware fictícia.

![captura de tela da página definir associações para um programa para Litware](images/setassociationsforaprogramforlitware.png)

A janela Associação de arquivo mostra os padrões que o aplicativo registrou e também mostra o padrão atual para outras extensões e protocolos. Depois que o usuário terminar de personalizar seus padrões, ele clicará no botão **salvar** para confirmar as alterações. Se o usuário clicar em **Cancelar**, a janela será fechada sem salvar as alterações.

Você deve usar essa interface do usuário para seus aplicativos em vez de criar o seu próprio. Ao fazer isso, você salva os recursos que antes eram necessários para desenvolver a interface do usuário da Associação de arquivos. Você também garante que as associações sejam salvas corretamente.

### <a name="set-an-application-to-check-whether-it-is-the-default"></a>Definir um aplicativo para verificar se ele é o padrão

> [!Note]  
> Não há mais suporte para isso a partir de Windows 8.

 

Normalmente, os aplicativos verificam se estão definidos como padrão quando são executados. Defina seus aplicativos para fazer essa verificação chamando [**IApplicationAssociationRegistration:: QueryAppIsDefault**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefault) ou [**IApplicationAssociationRegistration:: QueryAppIsDefaultAll**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefaultall).

Se o aplicativo determinar que ele não é o padrão, ele poderá apresentar a interface do usuário que pergunta se a situação atual deve ser aceita ou para tornar o aplicativo o padrão. Sempre inclua uma caixa de seleção nesta interface do usuário que esteja selecionada por padrão e que apresente a opção para não ser solicitada novamente.

> [!Note]  
> A escolha do padrão deve ser orientada pelo usuário. Um aplicativo nunca deve recuperar um padrão sem solicitar o usuário.

 

A ilustração a seguir mostra uma caixa de diálogo de exemplo.

![captura de tela de uma caixa de diálogo de exemplo](images/notthedefaultui.png)

## <a name="additional-resources"></a>Recursos adicionais

-   [**IApplicationAssociationRegistration**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration)
-   [**IApplicationAssociationRegistrationUI**](/windows/desktop/api/Shobjidl/nn-shobjidl-iapplicationassociationregistrationui)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Práticas recomendadas para associações de arquivo](fa-best-practices.md)
</dt> <dt>

[Cenário de exemplo de associação de arquivo](fa-sample-scenarios.md)
</dt> <dt>

[diretrizes para o gerenciamento de aplicativos padrão no Windows Vista e posterior](vista-managing-defaults.md)
</dt> <dt>

[Definir o acesso do programa e padrões do computador (SPAD)](cpl-setprogramaccess.md)
</dt> </dl>

 

 
