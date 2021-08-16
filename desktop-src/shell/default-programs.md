---
description: Use Programas Padrão para definir a experiência do usuário padrão.
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

Use **Programas Padrão para** definir a experiência do usuário padrão. Os usuários podem **acessar Programas** Padrão Painel de Controle ou diretamente **no** menu Iniciar. [Definir a ferramenta SPAD (Acesso](cpl-setprogramaccess.md) ao Programa e Padrões do Computador), a experiência padrão principal para usuários no Windows XP, agora faz parte **dos Programas Padrão.**

> [!IMPORTANT]
> Este tópico não se aplica a Windows 10. A maneira como as associações de arquivos padrão funcionam mudou Windows 10. Para obter mais informações, consulte a seção sobre **Alterações em como Windows 10 lida com aplicativos padrão** nesta [postagem](https://blogs.windows.com/windowsexperience/2015/05/20/announcing-windows-10-insider-preview-build-10122-for-pcs/).

 

Quando um usuário define o programa como padrão usando Programas **Padrão,** a configuração padrão se aplica somente a esse usuário e não a outros usuários que podem usar o mesmo computador. **Os Programas** Padrão fornece um conjunto de APIs (preterido no Windows 8) que permitem que isVs (fornecedores independentes de software) incluam seus programas ou aplicativos no sistema de padrões. O conjunto de API também ajuda os ISVs a gerenciar melhor seu status como padrões.

Este tópico é organizado da seguinte forma:

-   [Introdução aos programas padrão e seu conjunto de API relacionado](#introduction-to-default-programs-and-its-related-api-set)
-   [Registrando um aplicativo para uso com programas padrão](#registering-an-application-for-use-with-default-programs)
    -   [Progids](#progids)
    -   [Sub-chave de registro e descrições de valor](#registration-subkey-and-value-descriptions)
    -   [RegisteredApplications](#registeredapplications)
    -   [Exemplo de registro completo](#full-registration-example)
-   [Tornando-se o navegador padrão](#becoming-the-default-browser)
-   [Interface do usuário de programas padrão](#default-programs-ui)
-   [Práticas recomendadas para usar programas padrão](#best-practices-for-using-default-programs)
    -   [Durante a instalação](#during-installation)
    -   [Após a instalação](#after-installation)
-   [Recursos adicionais](#additional-resources)
-   [Tópicos relacionados](#related-topics)

## <a name="introduction-to-default-programs-and-its-related-api-set"></a>Introdução aos programas padrão e seu conjunto de API relacionado

**Os Programas Padrão** são projetados principalmente para aplicativos que usam tipos de arquivo padrão, como arquivos .mp3 ou .jpg ou protocolos padrão, como HTTP ou mailto. Aplicativos que usam seus próprios protocolos proprietários e associações de arquivos normalmente não usam a **funcionalidade Programas** Padrão.

Depois de registrar um aplicativo **para a funcionalidade Programas** Padrão, as seguintes opções e funcionalidades estarão disponíveis usando o conjunto de API:

-   Restaure todos os padrões registrados para um aplicativo. Preterido para Windows 8.
-   Restaure um único padrão registrado para um aplicativo. Preterido para Windows 8.
-   Consulte o proprietário de um padrão específico em uma única chamada em vez de pesquisar no Registro. Você pode consultar o padrão de uma associação de arquivo, protocolo ou **verbo** canônico do menu Iniciar.
-   Iniciar uma interface do usuário para um aplicativo específico em que um usuário pode definir padrões individuais.
-   Remova todas as associações por usuário.

**Os Programas** Padrão também fornecem uma interface do usuário que permite registrar um aplicativo para fornecer informações adicionais ao usuário. Por exemplo, um aplicativo assinado digitalmente pode incluir uma URL para o home page.

O uso do conjunto de API associado pode ajudar uma função de aplicativo corretamente sob o recurso UAC (controle de conta de usuário) introduzido no Windows Vista. Em UAC, um administrador aparece no sistema como um usuário padrão, de modo que o administrador normalmente não pode gravar na subárvore **HKEY \_ LOCAL \_ MACHINE.** Essa restrição é um recurso de segurança que impede que um processo adoe como administrador sem o conhecimento do administrador.

A instalação de um programa por um usuário normalmente é executada como um processo elevado. No entanto, as tentativas de um aplicativo de modificar comportamentos de associação padrão em um nível de computador após a instalação não serão bem-sucedidas. Em vez disso, os padrões devem ser registrados em um nível por usuário, o que impede que vários usuários sobrescrevam os padrões uns dos outros.

A estrutura hierárquica do Registro para associações de arquivo e protocolo dá precedência aos padrões por usuário em relação aos padrões de nível de computador. Alguns aplicativos incluem pontos em seu código que elevam temporariamente seus direitos quando eles reivindicam padrões registrados no **HKEY \_ LOCAL \_ MACHINE.** Esses aplicativos poderão ter resultados inesperados se outro aplicativo já estiver registrado como o padrão por usuário. O uso **de Programas Padrão** impede essa ambiguidade e garante os resultados esperados em um nível por usuário.

## <a name="registering-an-application-for-use-with-default-programs"></a>Registrando um aplicativo para uso com programas padrão

Esta seção mostra as sub-chaves e os valores do Registro necessários para registrar um aplicativo com **Programas Padrão.** Ele inclui um exemplo completo.

Esta seção contém os seguintes tópicos:

-   [Progids](#progids)
-   [Sub-chave de registro e descrições de valor](#registration-subkey-and-value-descriptions)
-   [RegisteredApplications](#registeredapplications)
-   [Exemplo de registro completo](#full-registration-example)

**Os Programas** Padrão exigem que cada aplicativo registre explicitamente as associações de arquivo, associações MIME e protocolos para os quais o aplicativo deve ser listado como um padrão possível. Registre as associações usando os seguintes elementos do Registro, que são explicados em detalhes posteriormente neste tópico em [Sub-chave de](#registration-subkey-and-value-descriptions)registro e Descrições de valor :

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

O exemplo a seguir mostra as entradas do Registro para um navegador contoso fictício chamado WebBrowser:

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

### <a name="progids"></a>Progids

Um aplicativo deve fornecer um [ProgID específico.](fa-progids.md) Certifique-se de incluir todas as informações que normalmente são escritas na sub-chave padrão genérica para a extensão. Por exemplo, o player de mídia litware fictício fornece as classes de software **HKEY \_ LOCAL \_ MACHINE** \\  \\ **específicas** do aplicativo \\ **LitwarePlayer11.AssocFile.MP3** subkey. Essa sub-chave inclui todas as informações na sub-chave padrão **genérica HKEY \_ LOCAL \_ MACHINE** SOFTWARE Classes.mp3mais quaisquer informações adicionais que você deseja que \\  \\  \\ **** o aplicativo registre. Isso garante que, se o usuário restaurar a associação .mp3 para o player litware, as informações do jogador litware estão intactas e não foram substituídas por outro aplicativo. (A substituição poderá ocorrer se a sub-chave padrão for a única fonte dessas informações.)

Quando você mapeia um ProgID para uma extensão de nome de arquivo ou protocolo, um aplicativo pode mapear um para um ou um para muitos. No exemplo da Contoso, ContosoHTML aponta para um único ProgID que fornece informações de shellexecute para as extensões .htm, .html, .shtml, .xht e .xhtml. Como existe um ProgID diferente para cada protocolo, quando você usa protocolos, permite que cada protocolo tenha sua própria cadeia de caracteres de execução.

Quando o tipo MIME pode ser exibido em linha em um navegador, o ProgID para o tipo MIME deve conter a sub-chave **CLSID** que usa o CLSID (identificador de classe) do aplicativo correspondente. Esse CLSID é usado em uma olhada no CLSID no banco de dados MIME armazenado em Classes de SOFTWARE MIME classes de SOFTWARE LOCAL **HKEY \_ \_** \\  \\  \\ **.** \\  \\  Se o tipo MIME não se destina a ser exibido em linha em um navegador, essa etapa pode ser omitida.

### <a name="registration-subkey-and-value-descriptions"></a>Sub-chave de registro e descrições de valor

Esta seção descreve as sub-chaves e os valores individuais do Registro usados no registro de um aplicativo com Programas Padrão **,** conforme ilustrado anteriormente.

### <a name="capabilities"></a>Funcionalidades

A  sub-chave Funcionalidades contém todas as **informações de Programas Padrão** para um aplicativo específico. O espaço reservado %ApplicationCapabilityPath% refere-se ao caminho do Registro de **HKEY \_ CURRENT \_ USER** ou **HKEY \_ LOCAL \_ MACHINE** para a sub-chave **Funcionalidades** do aplicativo. Essa sub-chave contém os valores significativos mostrados na tabela a seguir.



| Valor                  | Type                       | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------------------|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ApplicationDescription | REG \_ SZ ou REG \_ EXPAND \_ SZ | **Obrigatório**. Para permitir que um usuário faça uma escolha de atribuição padrão informada, um aplicativo deve fornecer uma cadeia de caracteres que descreve os recursos do aplicativo. Embora o exemplo anterior da Contoso atribua a descrição diretamente ao valor ApplicationDescription, os aplicativos normalmente fornecem a descrição como um recurso inserido em um arquivo .dll para facilitar a localização. Se ApplicationDescription não for fornecido, o aplicativo não aparecerá nas listas de interface do usuário de programas padrão potenciais.                                                            |
| ApplicationName        | REG \_ SZ ou REG \_ EXPAND \_ SZ | **Opcional.** O nome pelo qual o programa aparece na interface do usuário de Programas Padrão. Se esses dados não são fornecidos pelo aplicativo, o nome do programa executável associado ao primeiro ProgID registrado para o aplicativo será usado na interface do usuário. ApplicationName sempre deve corresponder ao nome registrado em [RegisteredApplications.](#registeredapplications) Você pode usar ApplicationName se quiser tipos de aplicativos diferentes, como um navegador e um cliente de email, para apontar para o mesmo arquivo executável enquanto eles aparecem como nomes diferentes.<br/> |
| Hidden                 | REG \_ DWORD                 | **Opcional.** De definir esse valor como 1 para suprimir o aplicativo da lista de programas na caixa **de diálogo Definir seus programas padrão.** Se esse valor for 0 ou não estiver presente, o aplicativo aparecerá na lista normalmente.                                                                                                                                                                                                                                                                                                                                                              |



 

### <a name="fileassociations"></a>Associações de

A **subchave** FileAssociations contém associações de arquivo específicas que são reivindicadas pelo aplicativo. Essas declarações são armazenadas como valores, com um valor para cada extensão. As associações apontam para um ProgID específico do aplicativo em vez de um ProgID genérico. No entanto, não é necessário que todas as associações apontem para a mesma ProgID.

### <a name="mimeassociations"></a>MIMEAssociations

A subchave **MIMEAssociations** contém tipos MIME específicos que são reivindicados pelo aplicativo. Essas declarações são armazenadas como valores, com um valor para cada tipo de MIME. O nome do valor para cada tipo MIME deve corresponder exatamente ao nome MIME armazenado no banco de dados MIME. O valor também deve ser atribuído a um ProgID específico do aplicativo que contém o CLSID correspondente do aplicativo.

### <a name="startmenu"></a>Assumirá

A subchave **assumirá** está associada às entradas de **email** e **Internet** atribuíveis ao usuário no menu **Iniciar** . Um aplicativo deve ser registrado separadamente como um Contender para essas entradas. Para obter mais informações, consulte [registrando programas com tipos de cliente](reg-middleware-apps.md).

> [!Note]  
> a partir do Windows 7, não há mais entradas de **Internet** e **email** no menu **iniciar** . os dados de registro associados à entrada de **email** ainda são usados para o cliente MAPI padrão, mas os dados do registro associados à entrada da **Internet** não são usados pelo Windows.

 

Ao associar o registro do menu **Iniciar** de um aplicativo com seu registro de **programas padrão** , o aplicativo aparece como um padrão potencial na interface do usuário **definir associações** . Se o usuário tiver escolhido o aplicativo como o padrão e, em seguida, optar por restaurar todos os padrões do aplicativo posteriormente, o aplicativo será restaurado para a posição do menu **Iniciar** para esse usuário. Para obter mais informações e uma ilustração, consulte a seção [interface do usuário de programas padrão](#default-programs-ui) mais adiante neste tópico.

A subchave **assumirá** tem duas entradas: StartMenuInternet e mail, que correspondem às posições canônicas de **Internet** e **email** no menu **Iniciar** . Um aplicativo atribui o StartMenuInternet ou o mail a um valor igual ao nome da subchave registrada do aplicativo em **HKEY \_ local \_ Machine** \\ **software** \\ **clients** \\ **StartMenuInternet** ou **HKEY \_ local \_ Machine** \\ **software** \\ **clients** \\ **mail** (conforme descrito em [registrando programas com tipos de cliente](reg-middleware-apps.md)).

No caso da posição canônica do **email** no menu **Iniciar** , ele representa o cliente MAPI padrão e, portanto, pode ser considerado capaz de distribuir chamadas MAPI. em Windows 7, embora não haja mais uma posição canônica de **email** no menu **iniciar** , essa subchave continua a ser usada para o cliente MAPI padrão. Um aplicativo que reivindica o padrão de email deve se registrar como um manipulador MAPI na seguinte subchave:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            CanonicalName
```

Se um cliente de email não puder dar suporte a MAPI, mas ainda quiser lutar para a posição canônica de **email** do menu **Iniciar** , ele poderá registrar uma linha de comando na seguinte subchave:

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

Além disso, em **HKEY \_ local \_ Machine** \\ **software** \\ **clients** \\ **mail** \\ *canôniconame* , adicione um valor padrão com o nome do aplicativo.

Essas entradas permitem que o aplicativo seja iniciado a partir da posição de **email** do menu **Iniciar** . Observe que as chamadas MAPI ainda são feitas no aplicativo, e que se enquadram no manipulador MAPI anterior ou falham se nenhum manipulador MAPI foi definido. Para obter mais informações, consulte [registrando programas com tipos de cliente](reg-middleware-apps.md).

### <a name="urlassociations"></a>UrlAssociations

A subchave **UrlAssociations** contém os protocolos de URL específicos que são reivindicados pelo aplicativo. Essas declarações são armazenadas como valores, com um valor para cada protocolo. Cada protocolo deve apontar para um ProgID específico do aplicativo em vez de para um ProgID genérico. Conforme mencionado no exemplo da Contoso, você pode usar um ProgID diferente para cada protocolo para que cada um tenha sua própria cadeia de caracteres de execução.

### <a name="registeredapplications"></a>RegisteredApplications

A subchave completa para **RegisteredApplications** é:

**HKEY \_ \_** RegisteredApplications de \\ **software** \\  do computador local

Essa subchave fornece ao sistema operacional o local do registro das informações de **programas padrão** para o aplicativo. O local é armazenado como um valor cujo nome deve corresponder ao nome do aplicativo.

### <a name="full-registration-example"></a>Exemplo de registro completo

Este exemplo mostra as subchaves e os valores que são usados no registro do player de mídia da Litware fictícia. O exemplo inclui as entradas de ProgID para mostrar como todas se encaixam.

A subchave a seguir mostra o ProgID específico do aplicativo para o tipo MIME .mp3:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         LitwarePlayer11.MIME.MP3
            CLSID
               (Default) = {CD3AFA76-B84F-48F0-9393-7EDC34128127}
```

Em seguida, está o ProgID específico do aplicativo que associa o programa Litware com a extensão de nome de arquivo .mp3.

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

As entradas a seguir mostram o ProgID combinado para o tipo MIME .mpeg e a extensão de nome de arquivo.

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

As próximas entradas registram o programa Litware em **programas padrão** e usam ProgIDs registrados anteriormente

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

Por fim, este exemplo registra o local do registro de **programas padrão** Litware.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      RegisteredApplications
         Litware Player = Software\Litware\LitwarePlayer\Capabilities
```

## <a name="becoming-the-default-browser"></a>Tornando-se o navegador padrão

O registro do navegador deve seguir as práticas recomendadas descritas neste tópico. quando o navegador é instalado, Windows pode apresentar ao usuário uma notificação do sistema por meio da qual o usuário pode selecionar o navegador como o padrão do sistema. Essa notificação é mostrada quando essas condições são atendidas:

-   o instalador do navegador chama [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) com o sinalizador **SHCNE \_ assocchanged** para informar Windows que novos manipuladores de protocolo foram registrados.
-   Windows detecta que um ou mais aplicativos novos foram registrados para lidar com os protocolos http://e https://, e o usuário ainda não foi notificado. Em outras palavras, nenhum dos itens a seguir foi mostrado ao usuário: uma notificação do sistema anuncia o aplicativo, um submenu OpenWith que contém o aplicativo ou a página do painel de controle definir padrões do usuário (SUD) para o aplicativo.

O exemplo a seguir mostra o código de registro recomendado que o instalador do navegador deve executar depois de gravar suas chaves de registro.

O [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) primeiro notifica o sistema de que novas opções de associação estão disponíveis. A chamada **SHChangeNotify** é necessária para garantir o funcionamento adequado dos padrões do sistema.

Em seguida, uma instrução [**Sleep**](/windows/win32/api/synchapi/nf-synchapi-sleep) permite que os processos do sistema manipulem a notificação.


```C++
void NotifySystemOfNewRegistration()
{
    SHChangeNotify(SHCNE_ASSOCCHANGED, SHCNF_DWORD | SHCNF_FLUSH, nullptr, nullptr);
    Sleep(1000);
}
```



Se o usuário descartar ou ignorar a notificação ou submenu resultante sem fazer uma nova seleção de navegador padrão, o navegador padrão permanecerá inalterado. Observe que o usuário também pode alterar o navegador padrão a qualquer momento por meio de outros mecanismos, incluindo definir padrões do usuário no painel de controle.

## <a name="default-programs-ui"></a>Interface do usuário de programas padrão

As ilustrações nesta seção mostram a interface do usuário para **programas padrão** , como visto pelo usuário.

A ilustração a seguir mostra a janela principais **programas padrão** no painel de controle.

![captura de tela da página de entrada de programas padrão](images/defaultprogramsmain.png)

Quando um usuário escolhe a opção **definir os programas padrão** , a janela a seguir é exibida. Os usuários podem usar essa página para atribuir um programa padrão para todos os tipos de arquivo e protocolos para os quais o programa é um padrão possível. Conforme mostrado na ilustração a seguir, todos os programas [registrados](#registering-an-application-for-use-with-default-programs) e o ícone do programa aparecem na caixa **programas** à esquerda.

![captura de tela da página definir programas padrão](images/setyourdefaultprograms.png)

Quando o usuário seleciona um programa da lista, o ícone do programa e o provedor são exibidos. Se a URL for inserida no certificado assinado digitalmente do programa, o programa também poderá exibir uma URL. Os programas que não são assinados digitalmente não podem exibir uma URL.

O texto descritivo, fornecido pelo programa durante o registro, também é exibido. Esse texto é necessário. Abaixo da caixa Descrição, há uma indicação de quantos padrões o programa está atualmente atribuído do número completo que está registrado para manipular.

Para atribuir ou restaurar um programa como o padrão para todos os arquivos e protocolos para os quais ele está registrado, o usuário clica na opção **definir este programa como padrão** .

Para atribuir tipos de arquivo e protocolos individuais a um programa, o usuário clica na opção **escolher padrões para este programa** , que exibe um **conjunto de associações para uma** janela de programa como a mostrada na ilustração a seguir.

> [!Note]  
> Recomendamos que você chame as **associações de conjunto para um programa** usando [**IApplicationAssociationRegistrationUI:: LaunchAdvancedAssociationUI**](/windows/desktop/api/Shobjidl/nf-shobjidl-iapplicationassociationregistrationui-launchadvancedassociationui).

 

![captura de tela da página definir associações para um programa](images/setassociationsforaprogram.png)

## <a name="best-practices-for-using-default-programs"></a>Práticas recomendadas para o uso de programas padrão

Esta seção fornece as diretrizes de práticas recomendadas para o uso de **programas padrão** ao registrar aplicativos. Ele também oferece sugestões de design para a criação de um aplicativo que forneça aos usuários a funcionalidade ideal de **programas padrão** .

### <a name="during-installation"></a>Durante a instalação

além dos procedimentos de instalação normalmente praticado em Windows XP, um aplicativo com base no Windows Vista ou posterior deve se registrar com o recurso de **programas padrão** para aproveitar sua funcionalidade.

Execute a seguinte sequência de etapas durante a instalação. as etapas 1-3 correspondem às etapas que foram usadas no Windows XP; a etapa 4 foi nova no Windows Vista.

1.  Instale os arquivos binários necessários.
2.  Escreva ProgIDs para o \_ computador local hKey \_ . Observe que os aplicativos devem criar ProgIDs específicos do aplicativo para suas associações.
3.  Registre o aplicativo com **programas padrão** conforme explicado anteriormente no [registro de um aplicativo para uso com programas padrão](#registering-an-application-for-use-with-default-programs).

### <a name="after-installation"></a>Após a instalação

Esta seção discute como o prompt do aplicativo deve primeiro apresentar suas opções padrão para cada usuário. Ele também discute como um aplicativo pode monitorar seu status como o padrão para suas possíveis associações e protocolos.

### <a name="first-run-experiences"></a>Experiências da primeira execução

Quando o aplicativo é executado por um usuário pela primeira vez, é recomendável que o aplicativo exiba a IU para o usuário que normalmente inclui essas duas opções:

-   Aceite as configurações de aplicativo padrão. Essa opção é habilitada por padrão.
-   Personalize as configurações de aplicativo padrão.

antes da Windows 8, se o usuário aceitar as configurações padrão, seu aplicativo chamará [**IApplicationAssociationRegistration:: SetAppAsDefaultAll**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-setappasdefaultall), que converte todas as associações em nível de máquina que são declaradas durante a instalação para as configurações por usuário para esse usuário.

Se o usuário decidir personalizar as configurações, seu aplicativo chamará [**IApplicationAssociationRegistrationUI:: LaunchAdvancedAssociationUI**](/windows/desktop/api/Shobjidl/nf-shobjidl-iapplicationassociationregistrationui-launchadvancedassociationui) para exibir a interface do usuário de associação de arquivo. A ilustração a seguir mostra essa janela para o player de mídia da Litware fictícia.

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

 

 
