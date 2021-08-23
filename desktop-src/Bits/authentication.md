---
title: Autenticação (BITS)
description: O BITS dá suporte à autenticação básica, autenticação do Passport e vários esquemas de autenticação de desafio/resposta.
ms.assetid: cfd4aec3-79d0-4971-93f8-df797e5c0f75
ms.topic: article
ms.date: 10/09/2018
ms.openlocfilehash: 9cb3d50f6689ed28889c68388969c1cb7d06ea912bc5d5ed4384f45a4e740f79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119021284"
---
# <a name="authentication-bits"></a>Autenticação (BITS)

O BITS dá suporte à autenticação básica, autenticação do Passport e vários esquemas de autenticação de desafio/resposta. Se o servidor ou proxy exigir autenticação de usuário, use a função [**IBackgroundCopyJob2:: SetCredentials**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) para especificar as credenciais do usuário. O BITS usa o [CryptoAPI](/windows/desktop/SecCrypto/cryptography-portal) para proteger as credenciais.

Para definir credenciais para autenticação básica, use a função [**SetCredentials**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) para especificar o nome de usuário e a senha. Você só deve usar a autenticação básica com sites seguros protegidos pelo https://; caso contrário, o nome de usuário e a senha ficarão visíveis para os usuários. 

É possível inserir o nome de usuário e a senha na URL. Isso não é considerado uma boa prática de segurança e é preterido no RFC 3986 (seção 3.2.1).

Para a autenticação do [Passport](/windows/desktop/WinHttp/passport-authentication-in-winhttp) , o bits dá suporte apenas a credenciais explícitas, não a credenciais implícitas ligadas à conta.

Para a autenticação de desafio/resposta, o BITS representa o usuário e usa [Snego](../com/snego.md) para determinar qual autenticação de desafio/resposta usar, como NTLM ou o protocolo Kerberos. Para obter uma lista de esquemas de desafio/resposta aos quais o BITS dá suporte, consulte [**BG \_ auth \_ Scheme**](/windows/desktop/api/Bits1_5/ne-bits1_5-bg_auth_scheme).

Os trabalhos do BITS poderão falhar se o diretório virtual no servidor tiver autenticação anônima e outro esquema de autenticação habilitado e se as ACLs protegerem o diretório virtual ou os arquivos de download. Por exemplo, um trabalho falhará com "acesso negado" se o diretório virtual tiver a autenticação anônima e integrada habilitada e o arquivo contiver uma ACL que permita apenas Ben ler o arquivo. Isso ocorre porque o diretório virtual permite acesso anônimo, portanto o IIS não autentica explicitamente Ben (as credenciais de Ben não são usadas para acessar o arquivo e o acesso é negado).

## <a name="using-implicit-credentials"></a>Usando credenciais implícitas

Para usar as credenciais implícitas (logon) do usuário para autenticação NTLM ou Kerberos, chame o método [**IBackgroundCopyJob2:: SetCredentials**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) e defina os membros **nome de usuário** e **senha** da estrutura de [**\_ \_ credenciais básica BG**](/windows/desktop/api/Bits1_5/ns-bits1_5-bg_basic_credentials) como **NULL**. Se você especificar credenciais implícitas para um proxy, os BITS também usarão as credenciais implícitas para autenticação de servidor, a menos que você especifique credenciais de servidor explícitas.

Para obter informações adicionais para serviços, consulte [contas de serviço e bits](service-accounts-and-bits.md).

Você também pode alterar o valor do registro **LmCompatibilityLevel** ou **UseLMCompat** ; no entanto, você deve alterar esses valores somente se tiver um aplicativo existente que não pode ser alterado para chamar o método [**SetCredentials**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) .

O BITS usará credenciais implícitas para autenticação se o valor do registro **LmCompatibilityLevel** for dois ou maior, e você não tiver chamado o método [**SetCredentials**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) . O caminho completo para o valor do registro **LmCompatibilityLevel** é **HKEY \_ local \_ Machine** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **LSA** \\ **LmCompatibilityLevel**.

Observe que alterar o valor do registro **LmCompatibilityLevel** pode afetar outros aplicativos e serviços em execução no computador. Para obter mais informações sobre como usar o valor do registro **LmCompatibilityLevel** , consulte [KB147706](https://support.microsoft.com/kb/147706).

se a definição do valor do registro **LMCompatibilityLevel** for um problema, você poderá criar o valor do registro **UseLMCompat** em **HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **BITS**. O valor do registro é um DWORD. A tabela a seguir lista os possíveis valores para **UseLMCompat**:

|Valor|Descrição|
|-|-|
| 0     | O BITS enviará credenciais implícitas sempre que o servidor solicitar credenciais NTLM ou Kerberos.                                                                                           |
| 1     | O BITS enviará credenciais implícitas somente se o valor do registro **LmCompatibilityLevel** do computador cliente for maior ou igual a 2.<br/>     |
| 2     | O BITS enviará credenciais implícitas somente se o aplicativo tiver chamado o método [**SetCredentials**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) .<br/> |

Os BITS usarão um valor padrão de "2" para o valor do registro **UseLMCompat** se o valor do registro não existir.

## <a name="using-certificates-for-clientserver-authentication"></a>Usando certificados para autenticação de cliente/servidor

Na comunicação segura do cliente/servidor, os clientes e servidores podem usar certificados digitais para se autenticar mutuamente. O BITS dá suporte automaticamente à autenticação de servidor baseada em certificado para transportes HTTP seguros. Para fornecer BITS o certificado de cliente necessário para a autenticação mútua, chame o método [**IBackgroundCopyJobHttpOptions:: SetClientCertificateByID**](/windows/desktop/api/Bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setclientcertificatebyid) ou [**IBackgroundCopyJobHttpOptions:: SetClientCertificateByName**](/windows/desktop/api/Bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setclientcertificatebyname) .

Quando um site aceita, mas não requer um certificado de cliente SSL, e o trabalho BITS não especifica um certificado de cliente, o trabalho falhará com o **erro \_ WinHTTP \_ Client \_ auth \_ CERT \_ necessário** (0x80072f0c).

## <a name="how-to-handle-authenticated-proxy-scenarios-that-require-user-specific-settings"></a>Como lidar com cenários de proxy autenticados que exigem configurações específicas do usuário

Se você estiver usando BITS em um ambiente que exija autenticação de proxy durante a execução como uma conta sem credenciais NTLM ou Kerberos utilizáveis no domínio de rede da máquina, será necessário executar etapas adicionais para autenticar corretamente usando as credenciais de outra conta de usuário que tenha credenciais no domínio. Esse é um cenário típico quando o código BITS está sendo executado como um serviço de sistema, como LocalService, NetworkService ou LocalSystem, pois essas contas não têm credenciais NTLM ou Kerberos utilizáveis.

A lógica de detecção de proxy usada em BITS faz o seguinte quando um token auxiliar de rede ( \_ rede de token BG \_ ) é definido:

-   Se [**método ibackgroundcopyjob:: SetProxySettings**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) foi chamado com **a \_ \_ configuração de \_ uso \_ de proxy de trabalho BG**, leia as configurações de proxy do IE local usando a representação do contexto do token do proprietário do trabalho por meio de [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser). a partir do Windows 10, versão 1809 (10,0; Build 17763), a identidade do token auxiliar é usada para esta etapa.
-   Se [**método ibackgroundcopyjob:: SetProxySettings**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) for chamado com a detecção automática de uso de proxy de BG ou se as configurações do IE do caso de configuração de uso do proxy de trabalho BG especificarem uma **\_ \_ \_ \_ AutoConfig** ou uma URL de configuração automática, realize a detecção de proxy automático ou o protocolo de descoberta automática de proxy da Web (WPAD), usando a representação de token auxiliar via [**WinHttpGetProxyForUrl**](/windows/desktop/api/winhttp/nf-winhttp-winhttpgetproxyforurl). **\_ \_ \_**

Depois disso, a representação do token auxiliar é usada para autenticação de proxy ou de servidor em todo o.

a partir do Windows 10, versão 1809 (10,0; Build 17763), o cenário de proxy autenticado com credenciais específicas do usuário é simplificado.

1.  Chame o método [**SetCredentials**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) do trabalho do bits com o **BG \_ auth \_ Scheme \_ Negotiate**, *username* definido como **NULL**, *password* Set como **null** e *target* Set como **BG \_ auth \_ target \_ proxy**. Isso faz com que as credenciais implícitas da conta do usuário sejam usadas para a autenticação NTLM e Kerberos com o proxy e o servidor.
2.  Chame [**método ibackgroundcopyjob:: SetProxySettings**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) com o **BG \_ uso de proxy de trabalho de \_ \_ \_ configuração**.
3.  QueryInterface para [**IBitsTokenOptions**](/windows/desktop/api/Bits4_0/nn-bits4_0-ibitstokenoptions).
4.  Representar a conta de usuário que você está usando para credenciais NTLM/Kerberos.
5.  Chame [**SetHelperToken**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken).
6. Chame [**SetHelperTokenFlags**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertokenflags) com **a \_ \_ rede de token bg**.
7. Reverta a representação.
8. Continuar a instalação do trabalho.
9. Chame [**resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) no trabalho.

antes de Windows 10, versão 1809 (10,0; Build 17763), a identidade de usuário correta (a identidade do token auxiliar) é usada para a detecção de proxy baseada em rede (WPAD) e para autenticação de proxy, mas a detecção real de configurações de proxy locais (IE) é sempre feita usando o token do proprietário do trabalho, mesmo quando um token auxiliar é configurado. Para contornar essa deficiência, você pode seguir estas etapas.

1.  Representar a conta de usuário que você está usando para credenciais NTLM/Kerberos.
2.  Recupere as configurações de proxy do IE da conta de usuário chamando [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser).
3.  Reverta a representação.
4.  Chame o método [**SetCredentials**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) do trabalho do bits com o **BG \_ auth \_ Scheme \_ Negotiate**, *username* definido como **NULL**, *password* Set como **null** e *target* Set como **BG \_ auth \_ target \_ proxy**. Isso faz com que as credenciais implícitas da conta do usuário sejam usadas para a autenticação NTLM e Kerberos com o proxy e o servidor.
5.  Se a etapa 2 gerou quaisquer configurações de proxy específicas de usuário (ou seja, *lpszProxy* ou *LpszProxyBypass* não forem **nulas**), defina as configurações de trabalho correspondentes manualmente, usando [**SetProxySettings**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) com a configuração de substituição de uso de **proxy de \_ trabalho \_ \_ \_ BG** .
6.  Se a etapa 2 não gerar nenhuma configuração de proxy específica do usuário, chame [**SetProxySettings**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) com o **BG uso de trabalho de \_ \_ \_ configuração**.
7.  QueryInterface para [**IBitsTokenOptions**](/windows/desktop/api/Bits4_0/nn-bits4_0-ibitstokenoptions).
8.  Represente a conta de usuário.
9.  Chame [**SetHelperToken**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken).
10. Chame [**SetHelperTokenFlags**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertokenflags) com **a \_ \_ rede de token bg**.
11. Reverta a representação.
12. Continuar a instalação do trabalho.
13. Chame [**resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) no trabalho.
