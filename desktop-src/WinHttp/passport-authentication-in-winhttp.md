---
description: O Microsoft Windows HTTP Services (WinHTTP) dá suporte total ao uso no lado do cliente do protocolo de autenticação Microsoft Passport. Este tópico fornece uma visão geral das transações envolvidas na autenticação do Passport e como tratá-las.
ms.assetid: 395d7aef-4da0-4664-8328-7d31ce58fedd
title: Autenticação do Passport no WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b8fc00217c7c14fbd4635fab68398d2056c1ea5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457240"
---
# <a name="passport-authentication-in-winhttp"></a>Autenticação do Passport no WinHTTP

O Microsoft Windows HTTP Services (WinHTTP) dá suporte total ao uso no lado do cliente do protocolo de autenticação Microsoft Passport. Este tópico fornece uma visão geral das transações envolvidas na autenticação do Passport e como tratá-las.

> [!Note]  
> No WinHTTP 5,1, a autenticação do Passport está desabilitada por padrão.

 

## <a name="passport-14"></a>Passport 1,4

O Passport é um componente fundamental dos serviços de blocos de construção de Microsoft .NET. Ele permite que as empresas desenvolvam e ofereçam serviços Web distribuídos em uma ampla variedade de aplicativos e permite que seus membros usem um nome de entrada e senha em todos os sites participantes.

O WinHTTP fornece suporte de plataforma para o Microsoft Passport 1,4 implementando o protocolo do lado do cliente para a autenticação do Passport 1,4. Ele libera os aplicativos dos detalhes da interação com a infraestrutura do Passport e os nomes de usuário e senhas armazenados no Windows XP. Essa abstração torna o uso do Passport não diferente da perspectiva de um desenvolvedor do que usar esquemas de autenticação tradicionais, como Basic ou Digest.

**Windows XP:** A chave de registro **HKCU \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ Internet Settings \\ Passport \\ NumRegistrationRuns** identifica o número de vezes que o assistente de autenticação do Passport é exibido quando a autenticação do Passport é necessária. Se o valor dessa chave for definido como um número maior que 5, o assistente não será exibido.

As seções a seguir descrevem as transações envolvidas na autenticação do Passport a partir do ponto de vista de um aplicativo cliente. Para o desenvolvimento do Passport no lado do servidor, consulte Visão geral da documentação do SDK do Passport.

-   [Solicitação inicial](#initial-request)
-   [Servidor de logon do Passport](#passport-login-server)
-   [Solicitação autenticada](#authenticated-request)

### <a name="initial-request"></a>Solicitação inicial

Quando um cliente solicita um recurso em um servidor que requer autenticação do Passport, o servidor verifica a solicitação da presença de [*tíquetes*](glossary.md). Se um *tíquete* válido for enviado com a solicitação, o servidor responderá com o recurso solicitado. Se o *tíquete* não existir no cliente, o servidor responderá com um código de status 302. A resposta inclui o cabeçalho de desafio "WWW-Authenticate: Passport 1.4". Os clientes que não estão usando o Passport podem seguir o redirecionamento para o servidor de logon do Passport. Clientes mais avançados normalmente entram em contato com o Passport Nexus para determinar o local do servidor de logon do Passport.

> [!Note]  
> Central para a Microsoft Passport rede é o Passport *Nexus*, que facilita a sincronização de sites de participantes do Passport para garantir que cada site tenha os detalhes mais recentes sobre a configuração de rede e outros problemas. Cada componente do Passport (Gerenciador do Passport, servidores de logon, servidores de atualização e assim por diante) se comunica periodicamente com o Nexus para recuperar as informações necessárias para localizar e se comunicar corretamente com os outros componentes na rede do Passport. Essas informações são recuperadas como um documento XML chamado documento de configuração de componente ou CCD.

 

A imagem a seguir mostra a solicitação inicial para uma afiliada do Passport.

![imagem mostra a solicitação inicial para uma afiliada do Passport.](images/art-passport1.png)

### <a name="passport-login-server"></a>Servidor de logon do Passport

Um servidor de logon do Passport trata todas as solicitações de [*tíquetes*](glossary.md) para qualquer recurso em uma *autoridade de domínio* do Passport. Antes que uma solicitação possa ser autenticada usando o Passport, o aplicativo cliente deve entrar em contato com o servidor de logon para obter os *tíquetes* apropriados.

Quando um cliente solicita [*tíquetes*](glossary.md) de um servidor de logon do Passport, o servidor de logon normalmente responde com um código de status 401 para indicar que as credenciais do usuário devem ser fornecidas. Quando essas credenciais são fornecidas, o servidor de logon responde com os *tíquetes* necessários para acessar o recurso especificado no servidor que contém o recurso solicitado originalmente. O servidor de logon também pode redirecionar o cliente para outro servidor que possa fornecer o recurso solicitado.

![imagem mostra uma solicitação de tíquete de cliente para um servidor de logon do Passport.](images/art-passport2.png)

### <a name="authenticated-request"></a>Solicitação autenticada

Quando o cliente tem os [*tíquetes*](glossary.md) que correspondem a um determinado servidor, esses *tíquetes* são incluídos em todas as solicitações para esse servidor. Se os *tíquetes* não tiverem sido modificados desde que foram recuperados do servidor de logon do Passport e os *tíquetes* forem válidos para o servidor de recursos, o servidor de recursos enviará uma resposta que inclui o recurso solicitado e os cookies que indicam que o usuário é autenticado para solicitações futuras.

Os cookies adicionais na resposta destinam-se a acelerar o processo de autenticação. Todas as solicitações adicionais na mesma sessão para recursos em servidores na mesma autoridade de domínio do Passport incluem esses cookies adicionais. As credenciais não precisam ser enviadas ao servidor de logon novamente até que os cookies expirem.

![imagem mostra uma solicitação autenticada para o servidor de logon do Passport.](images/art-passport3.png)

## <a name="using-passport-in-winhttp"></a>Usando o Passport no WinHTTP

A autenticação do Passport no WinHTTP é muito semelhante a outros esquemas de autenticação. Consulte [autenticação no WinHTTP](authentication-in-winhttp.md) para obter uma visão geral da autenticação no WinHTTP.

No WinHTTP 5,1, a autenticação do Passport é desabilitada por padrão e deve ser explicitamente habilitada com [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) antes do uso.

O WinHTTP lida com muitos dos detalhes da transação internamente para autenticação do Passport. Durante a solicitação inicial, o servidor responde com um código de status 302 quando a autenticação é necessária. O código de status 302 indica, na verdade, um redirecionamento e faz parte do protocolo do Passport para compatibilidade com versões anteriores. O WinHTTP oculta o código de status 302 e entra em contato com o Passport Nexus e, em seguida, o servidor de logon. O aplicativo WinHTTP é notificado sobre o código de status 401 enviado pelo servidor de logon para solicitar credenciais de usuário. Para o aplicativo, no entanto, ele aparece como se o status 401 for originado do servidor do qual o recurso foi solicitado. Dessa forma, o aplicativo WinHTTP não está ciente de interações com outros servidores e pode manipular a autenticação do Passport com o mesmo código que lida com outros esquemas de autenticação.

Normalmente, um aplicativo WinHTTP responde a um código de status 401 fornecendo credenciais de autenticação. Quando as credenciais são fornecidas com [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) ou [**SetCredentials**](iwinhttprequest-setcredentials.md) para autenticação do Passport, as credenciais são realmente enviadas para o servidor de logon, não para o servidor indicado na solicitação.

No entanto, ao responder a um código de status 407, um aplicativo WinHTTP deve usar [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) para fornecer credenciais de proxy, em vez de [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials). Como o **WinHttpSetOption** é uma maneira menos segura de fornecer credenciais, normalmente ele deve ser evitado.

Depois de recuperados, os [*tíquetes*](glossary.md) são gerenciados internamente e enviados automaticamente aos servidores aplicáveis em futuras solicitações.

> [!Note]  
> O WinHTTP permite que você desabilite o redirecionamento automático chamando a função [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) para a [**opção WinHTTP desabilitar sinalizador de \_ \_ \_ recurso**](option-flags.md) e especificar um valor de [**WinHTTP \_ desabilitar \_ redirecionamentos**](option-flags.md). Desabilitar o redirecionamento não interfere no redirecionamento que o WinHTTP manipula internamente para transações do Passport.

 

O WinHTTP pode concluir com êxito a autenticação do Passport, mesmo que um aplicativo desabilite o redirecionamento automático. No entanto, após a conclusão da autenticação do Passport, um redirecionamento implícito deve ocorrer na URL do servidor de logon do Passport de volta para a URL original. Esse redirecionamento não é disparado por uma resposta HTTP 302, mas é implícito no protocolo do Passport.

O WinHTTP manipula esse redirecionamento implícito especialmente. Se um aplicativo tiver desabilitado o redirecionamento automático, o WinHTTP exigirá que o aplicativo conceda "permissão" de WinHTTP para redirecionar automaticamente neste caso especial.

Para fazer com que o WinHTTP Redirecione para a URL original após a autenticação, o aplicativo deve registrar uma função de retorno de chamada usando [**WinHttpSetStatusCallback**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback). O WinHTTP pode notificar o aplicativo com um \_ retorno de chamada de redirecionamento de status de retorno de chamada WinHTTP \_ \_ , que permite ao aplicativo cancelar o redirecionamento. Um aplicativo não precisa fornecer nenhuma funcionalidade na função de retorno de chamada; o registro do retorno de chamada é suficiente para habilitar o WinHTTP a seguir este redirecionamento de caso especial.

A \_ mensagem de falha de logon WinHTTP de erro \_ \_ será gerada se uma função de retorno de chamada não for definida pelo aplicativo.

### <a name="passport-cobranding"></a>Comarcação do Passport

Ao contrário dos esquemas de autenticação tradicionais com suporte do WinHTTP, o Passport pode ser amplamente [*comarcado*](glossary.md). Após receber um código de status 401 que indica um desafio, um aplicativo pode recuperar o texto e o gráfico de *comarcação* . Recupere uma URL para o gráfico de *comarcação* chamando [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) com a \_ opção WinHTTP \_ sinalizador de URL de \_ comarcação do Passport \_ . Recupere o texto da *comarcação* chamando [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) com a \_ opção WinHTTP \_ sinalizador de texto de \_ comarcação do Passport \_ . Esses itens podem ser usados para personalizar uma caixa de diálogo de coleta de credenciais.

### <a name="stored-user-names-and-passwords"></a>Nomes de usuário e senhas armazenados

O Windows XP introduziu o conceito de nomes de usuário e senhas armazenados. Se as credenciais do Passport de um usuário forem salvas por meio do **Assistente de registro do Passport** ou da caixa de **diálogo credencial** padrão, ela será salva nos nomes de usuário e senhas armazenados. Ao usar o WinHTTP no Windows XP ou posterior, o WinHTTP usará automaticamente as credenciais nos nomes de usuário e senhas armazenados se as credenciais não estiverem definidas explicitamente. Isso é semelhante ao suporte de credenciais de logon padrão para NTLM/Kerberos. No entanto, o uso de credenciais padrão do Passport não está sujeito às configurações de política de logon automático.

### <a name="disabling-passport-authentication"></a>Desabilitando a autenticação do Passport

Alguns aplicativos podem exigir a capacidade de desabilitar a autenticação do Passport. Por exemplo, quando uma afiliada do Passport responde com o código de status 302 inicial, pode ser preferível seguir o redirecionamento indicado e renderizar a página de autenticação HTML do Passport em vez de permitir que o WinHTTP manipule a autenticação internamente. A autenticação do Passport está desabilitada no WinHTTP chamando a função [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) com a \_ opção WinHTTP configure a \_ \_ \_ opção Passport auth e passando o valor WinHTTP \_ Disable \_ Passport \_ auth. Depois, ele pode ser reabilitado novamente com o WINHTTP \_ Enable \_ Passport \_ auth.

A autenticação do Passport não pode ser desabilitada ao usar o objeto [**WinHttpRequest**](winhttprequest.md) .

Conforme observado anteriormente nesta seção, a autenticação do Passport é desabilitada por padrão no WinHTTP 5,1 e deve ser explicitamente habilitada com [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) antes do uso.

## <a name="passport-configuration-overrides-used-for-testing"></a>Substituições de configuração do Passport usadas para teste

O WinHTTP conta com as informações de configuração que ele baixa do servidor do Passport Nexus para dar suporte à autenticação do Passport 1,4. Por padrão, esse servidor seguro (SSL) é nexus.passport.com, e o recurso de configuração é rdr/pprdr. asp, que é conhecido como a configuração do Passport "ao vivo". O formato das informações é um cabeçalho HTTP personalizado "PassportURLs", seguido por pares de atributo-valor delimitados por vírgula.

Por exemplo, " https://nexus.passport.com/rdr/pprdr.asp " retorna as seguintes informações de configuração:

``` syntax
PassportURLs: DARealm=Passport.net,
DALogin=login.passport.com/login2.asp,
DAReg=https://register.passport.com/defaultwiz.asp,
Properties=https://memberservices.passport.com/ppsecure/MSRV_EditProfile.asp,
Privacy=https://www.passport.com/consumer/privacypolicy.asp,
GeneralRedir=https://nexusrdr.passport.com/redir.asp,
Help=https://memberservices.passport.com/UI/MSRV_UI_Help.asp,
ConfigVersion=2
\r\n
```

As partes relevantes para o WinHTTP são DARealm, DALogin e ConfigVersion. Por motivos de desempenho, eles são armazenados em cache durante o tempo de vida de uma sessão do WinHTTP. Esses três valores podem ser substituídos por aplicativos que são necessários para trabalhar com outra infraestrutura do Passport diferente da configuração de produção "ao vivo" alterando as configurações de registro apropriadas em

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Internet Settings
                  WinHttp
                     Passport Test
```

``` syntax
LoginServerRealm (REG_SZ)    For example: abc.net
LoginServerUrl (REG_SZ)      For example: https://private-login.passport.com/login2.asp
ConfigVersion (REG_DWORD)    For example: 10
```

Se LoginServerUrl estiver presente no registro, o WinHTTP não entrará em contato com o servidor Nexus para outros valores de configuração. Nesse caso, LoginServerRealm e ConfigVersion também devem ser definidos por meio do registro para corrigir os valores.

Um aplicativo pode, para fins de teste, ser necessário para baixar a configuração do Passport de um servidor de Nexus privado. Isso pode ser feito substituindo dois valores de registro em

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Internet Settings
                  WinHttp
                     Passport Test
```

``` syntax
NexusHost (REG_SZ)    e.g. private-nexus.passport.com
NexusObj(REG_SZ)      e.g. config/passport.asp
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Autenticação no WinHTTP](authentication-in-winhttp.md)
</dt> </dl>

 

 



