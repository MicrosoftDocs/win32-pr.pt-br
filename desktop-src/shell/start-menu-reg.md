---
description: O menu iniciar no Windows XP e no Windows Vista contém Slots reservados para os clientes padrão de Internet (navegador) e email (email), juntos conhecidos como aplicativos de Internet do menu iniciar.
ms.assetid: a3d7416f-0dbd-4af2-ab38-758f9cc8aec5
title: Como registrar um navegador da Internet ou cliente de email com o menu Iniciar do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eccdd8fb8efe32522947b30ab2ce1a50b7058e97
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104172538"
---
# <a name="how-to-register-an-internet-browser-or-email-client-with-the-windows-start-menu"></a>Como registrar um navegador da Internet ou cliente de email com o menu Iniciar do Windows

> [!Note]  
> Este tópico aplica-se ao Windows XP, Windows Vista e Windows 7.

 

O menu iniciar no Windows XP e no Windows Vista contém Slots reservados para os clientes padrão de **Internet** (navegador) e **email** (email), juntos conhecidos como *aplicativos de Internet do menu iniciar*. Os aplicativos que se registram como menu iniciar aplicativos de Internet fazem isso em todo o sistema (por máquina). No Windows Vista, o usuário pode usar o recurso **programas padrão** para definir um padrão por usuário.

Quando os aplicativos são registrados como menu iniciar aplicativos de Internet, o Windows XP e o Windows Vista criam ícones de **Internet** e **email** no menu iniciar. Clicar nesses ícones faz com que o menu iniciar Verifique a subárvore do registro por usuário (**HKEY \_ Current \_ User**). Se nenhuma configuração padrão por usuário for encontrada, o menu iniciar procurará a subchave padrão por máquina na subárvore **do \_ \_ computador local hKey** .

> [!Note]  
> A instalação padrão do Windows não registra um programa de email ou Internet padrão por usuário, apenas um padrão em todo o sistema. Isso fornece um caminho de atualização suave de versões anteriores do sistema operacional, em que apenas a \_ subárvore do computador local hKey tem \_ suporte para registros de cliente.

 

Este tópico discute os seguintes itens:

-   [Registro no link da Internet do menu iniciar](#registering-for-the-start-menu-internet-link)
    -   [Como registrar-se como o cliente de Internet padrão](#how-to-register-as-the-default-internet-client)
-   [Registro para o link de email do menu iniciar](#registering-for-the-start-menu-email-link)
    -   [Como o menu iniciar exibe o cliente de email padrão](#how-the-start-menu-displays-the-default-email-client)
    -   [Como registrar-se como o cliente de EMail padrão](#how-to-register-as-the-default-email-client)
-   [Personalizando o menu de contexto](#customizing-the-context-menu)

## <a name="registering-for-the-start-menu-internet-link"></a>Registro no link da Internet do menu iniciar

> [!Note]  
> Esse registro é preterido a partir do Windows 7, que não fornece mais um link de Internet do menu iniciar. Os registros existentes são ignorados no Windows 7 e versões posteriores. Ser registrado como o aplicativo de Internet do menu Iniciar padrão não é o mesmo que está sendo registrado como o navegador da Web padrão. O navegador da Web padrão é usado para iniciar URLs arbitrárias de qualquer lugar no sistema. O menu iniciar aplicativo de Internet simplesmente controla o programa que é iniciado quando o usuário clica no ícone Internet no menu iniciar.

 

Qualquer aplicativo de navegador da Web pode se registrar para aparecer como um cliente de Internet no menu iniciar. Essa visibilidade, associada ao registro adequado para os tipos de [arquivo](fa-intro.md) e [protocolo](/previous-versions//aa767743(v=vs.85)) de um aplicativo, fornece um status de navegador padrão do aplicativo.

Os registros feitos na subárvore do **\_ \_ usuário atual do hKey** têm maior precedência para o usuário do console do que os registros correspondentes feitos no **\_ \_ computador local hKey**. Para novos usuários no sistema, as configurações armazenadas na **\_ \_ máquina local hKey** são usadas. A partir do Windows XP, as configurações de Internet do menu iniciar são mantidas nas entradas padrão de dois locais de registro:

-   **HKEY \_ \_** Clientes de \\ **software** do usuário atual \\  \\ **StartMenuInternet**
-   **HKEY \_ \_** Clientes de \\ **software** de computador local \\  \\ **StartMenuInternet**

A subchave **HKEY \_ Current \_ User** \\ **software** \\ **clients** \\ **StartMenuInternet** descreve o navegador da Internet que é iniciado quando o usuário clica no ícone **Internet** no menu iniciar. Se essa subchave estiver em branco ou ausente, o ícone da **Internet** no menu iniciar será definido como o padrão do sistema armazenado no segundo local em **HKEY \_ local \_ Machine** \\ **software** \\ **clients** \\ **StartMenuInternet** , que descreve todos os aplicativos de navegador da Internet instalados no sistema.

Quando um novo usuário faz logon no sistema, o menu iniciar usa o valor padrão na subchave em **HKEY \_ local \_ Machine** \\ **software** \\ **clients** \\ **StartMenuInternet** para exibir o cliente de Internet padrão e inicia o aplicativo registrado quando esse ícone é clicado.

### <a name="how-to-register-as-the-default-internet-client"></a>Como registrar-se como o cliente de Internet padrão

Abaixo da subchave **HKEY \_ \_ computador local** \\ **software** \\ **clients** \\ **StartMenuInternet** pode haver zero ou mais subchaves, uma para cada aplicativo registrado de navegador da Internet. Por exemplo, um sistema hipotético pode ter essa disposição:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         StartMenuInternet
            IEXPLORE.EXE
            BROWSER2.EXE
            BROWSER3.EXE
```

Demonstraremos as entradas do registro com um navegador hipotético chamado "visão acesa" de uma empresa fictícia chamada Litware Inc. suponha que o nome do executável para exibição acesa seja Litview.exe. O registro da exibição acesa ocorre conforme mostrado aqui:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         StartMenuInternet
            LITVIEW.EXE
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
```

Os dados de localizadas são do tipo REG \_ sz ou reg \_ Expand \_ sz Se variáveis de caminho, como `%programfiles%` são usadas. A localizadastring fornece o caminho para um arquivo executável (. exe) ou de biblioteca (. dll). Observe que a cadeia de caracteres do caminho começa com um sinal de "arroba" (@) e que nenhuma aspa é necessária em relação ao caminho, independentemente dos espaços dentro dela. O inteiro decimal é a ID de um recurso de cadeia de caracteres, contido na DLL especificada, cujo valor deve ser exibido ao usuário. Isso permite que o mesmo registro seja usado para vários idiomas. Cada idioma fornece um ResourceDLL.dll diferente. Isso permite que o sistema exiba a cadeia de caracteres correta com base no idioma selecionado no momento.

O seguinte \_ valor de sz de reg-sz ou reg \_ Expand \_ informa o menu Iniciar do ícone padrão a ser exibido quando o usuário seleciona a exibição acesa como o navegador de Internet do menu iniciar.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         StartMenuInternet
            LITVIEW.EXE
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LitView.exe,1
```

A subchave do registro a seguir especifica uma linha de comando a ser executada quando o usuário clica no comando de menu da Internet no menu Iniciar, supondo que a exibição acesa seja o navegador da Internet do menu iniciar selecionado. Por exemplo, o comando pode abrir o navegador com o home page do usuário ou o comando pode iniciar uma interface do usuário introdutória que as funcionalidades do ISV (fornecedor independente de software) são apropriadas. Os dados são do tipo REG \_ sz ou reg \_ Expand \_ sz, mas observe que, como há um espaço no caminho da linha de comando, o caminho do executável é colocado entre aspas.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         StartMenuInternet
            LITVIEW.EXE
               shell
                  open
                     (Default) = "C:\Program Files\LitwareInc\LitView.exe" -welcome
```

Quando o usuário especifica por meio de [Definir acesso do programa e padrões do computador (SPAD)](cpl-setprogramaccess.md) que a exibição acesa deve ser usada como o navegador da Web padrão no nível do computador, o aplicativo deve definir a entrada reg sz a seguir \_ . Observe que, como o SPAD é executado com privilégios de administrador, o acesso a essa subchave é permitido.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         StartMenuInternet
            (Default) = LITVIEW.EXE
```

> [!Note]
> No Windows Vista, o navegador da Web padrão de nível de usuário deve ser definido usando a ferramenta **programas padrão** , não o [SPAD](cpl-setprogramaccess.md).
> 
> **As informações a seguir aplicam-se apenas ao Windows XP.**
> 
> Se o registro do navegador da Web padrão no nível do computador em HKEY \_ local \_ Machine como mostrado acima for bem-sucedido, o aplicativo deverá excluir a entrada padrão na seguinte subchave:
> 
> ```
> HKEY_CURRENT_USER
>    SOFTWARE
>       Clients
>          StartMenuInternet
> ```
> 
> Se o registro do navegador da Web padrão no nível do computador em HKEY \_ local \_ Machine falhar, o aplicativo deverá definir os \_ dados de reg sz, conforme mostrado neste exemplo para o aplicativo de exibição iluminada:
> 
> ```
> HKEY_CURRENT_USER
>    SOFTWARE
>       Clients
>          (Default) = LITVIEW.EXE
> ```

 

Depois de atualizar as subchaves apropriadas, o aplicativo transmite a mensagem do [**WM \_ SETTINGCHANGE**](../winmsg/wm-settingchange.md) com seu parâmetro *wParam* definido como 0 e seu parâmetro *lParam* apontando para a cadeia de caracteres terminada em nulo `"Software\Clients\StartMenuInternet"` . Isso notifica o sistema operacional que o cliente padrão alterou.

A definição dessas subchaves para o navegador da Internet do menu Iniciar padrão é necessária para preservar a compatibilidade com versões anteriores de navegadores da Web que não dão suporte a registros por usuário.

## <a name="registering-for-the-start-menu-email-link"></a>Registro para o link de email do menu iniciar

> [!Note]  
> O link email do menu iniciar foi removido do Windows 7. No entanto, esse registro abordado nesta seção ainda deve ser executado para seu efeito na atribuição do cliente MAPI padrão.

 

### <a name="how-the-start-menu-displays-the-default-email-client"></a>Como o menu iniciar exibe o cliente de email padrão

Qualquer aplicativo de email pode se registrar para aparecer como um cliente de email no menu iniciar. Essa visibilidade, associada ao registro adequado para os tipos de [arquivo](fa-intro.md) e [protocolo](/previous-versions//aa767743(v=vs.85)) de um aplicativo, fornece um status de email padrão do aplicativo.

Os registros feitos na subárvore do **\_ \_ usuário atual do hKey** têm maior precedência para o usuário do console do que os registros correspondentes feitos no **\_ \_ computador local hKey**. Para novos usuários no sistema, as configurações armazenadas na **\_ \_ máquina local hKey** são usadas. A partir do Windows XP, as configurações de email do menu iniciar são mantidas nas entradas padrão de dois locais de registro:

-   **HKEY \_ \_** Email de \\  \\ **clientes** \\  de software do usuário atual
-   **HKEY \_ \_** Email de \\  \\ **clientes** \\  de software do computador local

A subchave **HKEY \_ Current \_ User** \\ **software** \\ **clients** \\ **mail** descreve o cliente de email que é iniciado quando o usuário clica no ícone de **email** no menu iniciar.

A subchave **HKEY do \_ \_ computador local** \\ **software** \\ **clients** \\ **mail** descreve os aplicativos de email que estão instalados no sistema, bem como o aplicativo de email padrão.

Se o **HKEY \_ atual \_ User** \\ **software** \\ **clients** \\ **mail** estiver em branco ou ausente, o valor padrão definido em **HKEY \_ local \_ Machine** \\ **software** \\ **clients** \\ **mail** será usado para selecionar o aplicativo de email que aparece no menu iniciar.

Quando um novo usuário faz logon no sistema, o menu iniciar usa o valor padrão na subchave em **HKEY \_ local \_ Machine** \\ **software** \\ **clients** \\ **mail** para exibir o cliente de email padrão e inicia o aplicativo registrado quando esse ícone é clicado.

### <a name="how-to-register-as-the-default-email-client"></a>Como registrar-se como o cliente de EMail padrão

**HKEY \_ O \_** \\  \\  \\ **email** de clientes de software de computador local pode conter zero ou mais subchaves, um para cada aplicativo de email registrado. Por exemplo, um sistema hipotético pode definir as seguintes subchaves:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            Eudora
            Windows Mail
```

Demonstraremos as entradas do registro com um cliente de email hipotético chamado "email aceso" da empresa fictícia chamada Litware Inc. Litware Inc. decide registrar esse cliente de email com o nome interno "LitMail". Assim como em um navegador, o nome interno é uma cadeia de caracteres exclusiva usada como o nome da subchave, mas nunca é mostrado ao usuário.

Para instalar o cliente de email de email aceso como o padrão, eles usam a seguinte subchave e suas entradas:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            LitMail
               (Default) = Lit Mail
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-456
```

Os dados de localizadas são do tipo REG \_ sz ou reg \_ Expand \_ sz Se variáveis de caminho, como `%programfiles%` são usadas. A localizadastring fornece o caminho para um arquivo executável (. exe) ou de biblioteca (. dll). Observe que a cadeia de caracteres do caminho começa com um sinal de "arroba" (@) e que nenhuma aspa é necessária em relação ao caminho, independentemente dos espaços dentro dela. O inteiro decimal é a ID de um recurso de cadeia de caracteres, contido na DLL especificada, cujo valor deve ser exibido ao usuário. Isso permite que o mesmo registro seja usado para vários idiomas. Cada idioma fornece um ResourceDLL.dll diferente. Isso permite que o sistema exiba a cadeia de caracteres correta com base no idioma selecionado no momento.

Depois de atualizar as subchaves apropriadas, o aplicativo transmite a mensagem do [**WM \_ SETTINGCHANGE**](../winmsg/wm-settingchange.md) com seu parâmetro *wParam* definido como 0 e seu parâmetro *lParam* apontando para a cadeia de caracteres terminada em nulo `"Software\Clients\Mail"` . Isso notifica o sistema operacional que o cliente padrão alterou.

Para compatibilidade com versões anteriores com aplicativos que não dão suporte a cadeias de caracteres localizadas, o nome do aplicativo no idioma instalado também deve ser definido como o valor padrão para a subchave.

O seguinte valor de sz- **\_ sz reg** ou **reg \_ expande \_** informa o menu Iniciar do ícone padrão a ser exibido quando o usuário seleciona email aceso como o programa de email do menu iniciar:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            LitMail
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LitMail.exe,1
```

A entrada a seguir especifica uma linha de comando a ser executada quando o usuário clica no item de menu de **email** no menu Iniciar, supondo que email aceso seja o programa de email do menu iniciar selecionado. Essa linha de comando também será executada se o usuário selecionar **ler email** no menu **ferramentas** do Internet Explorer do Windows. Os dados são do tipo **reg \_ sz** ou **reg \_ Expand \_ sz**, mas observe que, como há um espaço no caminho da linha de comando, o caminho do executável é colocado entre aspas.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            shell
               open
                  command
                     (Default) = "C:\Program Files\LitwareInc\LitMail.exe" -inbox
```

Se (e somente se) *o usuário* especificar email aceso como o aplicativo de email do menu Iniciar padrão, o aplicativo de email aceso pode gravar seu nome interno no seguinte valor de **reg \_ sz** :

```
HKEY_CURRENT_USER
   SOFTWARE
      Clients
         Mail
            (Default) = LitMail
```

Se (e somente se) *o usuário* especificar o email aceso para ser o aplicativo de email padrão em todo o sistema, o aplicativo de email aceso poderá gravar seu nome interno no valor de **\_ sz do reg** especificado abaixo. Observe que o acesso a essa subchave pode ser restrito. Os aplicativos não devem pressupor que todos os usuários tenham permissão para alterar o aplicativo de email padrão de todo o sistema.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            (Default) = LitMail
```

O registro como o aplicativo de email do menu Iniciar padrão não é equivalente ao registro como o cliente de email padrão do sistema ou o manipulador do *mailto* registrado.

-   O cliente de email padrão do sistema é iniciado quando o usuário clica em **ler email** no menu **ferramentas** do Internet Explorer.
-   O manipulador *mailto* registrado é iniciado quando o usuário clica em uma URL do formulário `mailto:someone@example.com` .
-   O aplicativo de email do menu iniciar é iniciado quando o usuário clica no ícone de **email** no menu iniciar.

Se nenhum aplicativo de email do menu Iniciar padrão for especificado, o ícone de email no menu iniciar inicia o cliente de email padrão do sistema.

Este tópico não abrange o registro do aplicativo como o manipulador de protocolo padrão *mailto* . Os aplicativos que desejam se registrar dessa maneira devem continuar a seguir as especificações existentes sobre esse assunto.

## <a name="customizing-the-context-menu"></a>Personalizando o menu de contexto

Um aplicativo pode personalizar as páginas de propriedades que são exibidas quando o usuário seleciona **Propriedades** no menu de atalho do ícone **email** (ou **Internet**). Por exemplo, o aplicativo de email Litware adiciona os seguintes dados **reg \_ sz** ou **reg \_ expande \_ sz** para exibir uma folha de propriedades Personalizada para o ícone de **email** em vez de sua folha de propriedades padrão.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            LitMail
               shell
                  properties
                     MUIVerb = @C:\Program Files\LitwareInc\ResourceDLL.dll,-789
                     command
                        (Default) = "C:\Program Files\LitwareInc\LitMail.exe" -properties
```

O item de dados MUIVerb é construído começando com um sinal "arroba" (@), seguido pelo caminho completo para a DLL de recurso, uma vírgula, um sinal de menos (-) e o identificador de recurso de cadeia de caracteres decimal a ser exibido. Observe que o caminho para o programa de LitMail.exe contém espaços, portanto, a cadeia de caracteres do caminho é colocada entre aspas.

Um aplicativo também pode adicionar outros comandos ao menu de contexto. Por exemplo, o aplicativo de email Litware adiciona um comando **Find** com os seguintes dados **reg \_ sz** :

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            LitMail
               shell
                  find
                     MUIVerb = @C:\Program File\LitwareInc\ResourceDLL.dll,-790
                     command
                        (Default) = "C:\Program Files\LitwareInc\LitMail.exe" -contacts
```

O nome da subchave abaixo do **shell** (nesse caso, "Find") é um nome arbitrário e não-local. Mais uma vez, os dados de MUIVerb contêm um sinal de "arroba" (@) como o primeiro elemento, seguido pelo caminho para uma DLL de recurso, um separador de vírgula e um sinal de subtração que antecede o identificador de recurso de cadeia de caracteres decimal. Por exemplo, esse recurso de cadeia de caracteres pode ser "abrir catálogo de endereços". Por fim, observe que a cadeia de caracteres de linha de comando contém espaços, portanto, ela é colocada entre aspas.

 

 
