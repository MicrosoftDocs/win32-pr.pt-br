---
title: Servidores proxy e WinRM
description: Gerenciamento Remoto do Windows (WinRM) usa HTTP e HTTPS para enviar mensagens entre os computadores cliente e servidor. Em geral, o cliente WinRM envia mensagens diretamente ao servidor WinRM. Os clientes WinRM também podem ser configurados para usar um servidor proxy.
ms.assetid: f8137b3a-7704-4b21-a923-6e2692e18d90
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e07bbfebb4c8f0eb9e77a8942d54677b55c60006
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641124"
---
# <a name="proxy-servers-and-winrm"></a>Servidores proxy e WinRM

Gerenciamento Remoto do Windows (WinRM) usa HTTP e HTTPS para enviar mensagens entre os computadores cliente e servidor. Em geral, o cliente WinRM envia mensagens diretamente ao servidor WinRM. Os clientes WinRM também podem ser configurados para usar um servidor proxy.

Para obter mais informações, consulte as seções a seguir:

-   [Configurando um servidor proxy para o WinRM 2,0](#configuring-a-proxy-server-for-winrm-20)
    -   [Conexões de proxy baseadas em HTTPS](#https-based-proxy-connections)
    -   [Conexões de proxy baseadas em HTTP](#http-based-proxy-connections)
-   [Configurando um servidor proxy para o WinRM 1,1 e anterior](#configuring-a-proxy-server-for-winrm-11-and-earlier)

## <a name="configuring-a-proxy-server-for-winrm-20"></a>Configurando um servidor proxy para o WinRM 2,0

O WinRM 2,0 oferece suporte a uma ampla gama de configurações de proxy. Por exemplo, o WinRM dá suporte a proxies para transportes HTTP e HTTPS e para servidores proxy autenticados e não autenticados.

### <a name="https-based-proxy-connections"></a>HTTPS-Based conexões de proxy

Para maior afinidade baseada em conexão e segurança, o HTTPS deve ser usado como o mecanismo de transporte.

Se o servidor proxy exigir autenticação, os clientes e servidores WinRM deverão usar HTTPS.

> [!Note]  
> A autenticação para o servidor proxy é independente da autenticação para o servidor de destino.

 

### <a name="http-based-proxy-connections"></a>HTTP-Based conexões de proxy

Se nenhuma autenticação de servidor proxy for necessária, HTTP ou HTTPs poderá ser usado para transporte. No entanto, as conexões baseadas em HTTP de um cliente WinRM para um servidor WinRM por meio de um servidor proxy podem ser problemáticas.

Os seguintes problemas podem ser encontrados ao usar conexões baseadas em HTTP:

-   O servidor proxy não oferece suporte à autenticação baseada em conexão, o que pode fazer com que a autenticação no servidor de destino falhe com um erro de acesso negado.
-   Mais de um conjunto de credenciais é necessário para se conectar ao servidor de destino e ao servidor proxy.
-   Os servidores proxy baseados em HTTP podem não oferecer suporte à capacidade de manter as conexões baseadas em servidor e baseadas no cliente associadas. Se o proxy não vincular fortemente um cliente a um servidor e manter a conexão TCP/IP, os clientes não autenticados poderão obter acesso aos dados. Além disso, a falta de afinidade de conexão pode fazer com que a autenticação falhe no servidor.

Se HTTP deve ser usado como transporte, o servidor proxy deve dar suporte à configuração a seguir para obter uma resposta melhor do WinRM e evitar falhas de acesso negado para clientes WinRM:

-   Suporte para HTTP/1.1. O HTTP/1.1 é mais estrito no mapeamento da afinidade de conexão entre o cliente e o servidor.
-   Autenticação baseada em conexão para autenticação Negotiate, Kerberos e CredSSP.

    A autenticação de uma solicitação requer várias viagens de ida e volta entre o cliente e o servidor. A maior parte da negociação para autenticação é concluída depois que o servidor de autenticação (WinRM) envia uma resposta ao cliente que não é uma resposta 401 (não autorizado). Se o servidor WinRM retornar uma resposta ao cliente que não seja uma resposta 401, o proxy não deverá fechar a conexão.

    Vários pares de solicitação/resposta podem ser enviados entre o cliente e o servidor antes que os dados reais do pacote sejam enviados. O WinRM 2,0 usa os esquemas de autenticação Negotiate e Kerberos com criptografia, o que pode adicionar viagens de ida e volta extras. Os dados não podem ser enviados para o servidor até que a autenticação seja concluída.

    O servidor WinRM retorna uma resposta de nível 200 que indica que a autenticação foi concluída. Os servidores proxy baseados em HTTP podem encerrar a afinidade de autenticação baseada em conexão e fechar a conexão TCP/IP depois de receber a resposta de nível 200 do servidor WinRM. A viagem de ida e volta do cliente para o servidor não inclui o pacote de solicitação original. Se o servidor proxy fechar a conexão, o servidor tentará autenticar novamente o cliente e a solicitação do cliente nunca poderá ser enviada ao servidor. Se a afinidade baseada em conexão não for mantida, a autenticação no servidor de destino poderá falhar com um erro de acesso negado.

-   Persistência de conexão. A conexão TCP/IP do cliente com o proxy deve continuar a mapear para a mesma conexão TCP/IP do proxy para o servidor. Manter essa conexão ajuda a atingir um nível mais alto de desempenho. Se a conexão não for mantida, cada solicitação deverá ser autenticada novamente, o que pode afetar o desempenho.

### <a name="encryption-and-winrm-20"></a>Criptografia e WinRM 2,0

O WinRM 2,0 dá suporte à criptografia via HTTP usando os esquemas de autenticação Negotiate, Kerberos e CredSSP. Se um servidor WinRM oferecer suporte a HTTP e for acessado por meio de um proxy, o servidor WinRM deverá impor a criptografia e não permitir o tráfego de rede não criptografado.

Sob nenhuma circunstância, as solicitações HTTP não criptografadas são enviadas por meio de servidores proxy. Quando os dados devem passar por um servidor proxy antes de serem enviados ao servidor de destino, os seguintes problemas de segurança são muito importantes:

-   É possível que um servidor proxy mal-intencionado possa examinar cada par de solicitação/resposta, incluindo as credenciais.
-   Se as conexões TCP/IP não forem fortemente mapeadas entre o cliente WinRM e o servidor proxy e entre o servidor proxy e o servidor de destino, um cliente não autorizado poderá se conectar ao servidor de destino usando a mesma conexão autenticada do servidor proxy para o servidor de destino. O servidor de destino pode permitir o acesso de cliente não autenticado aos dados. Se a criptografia for imposta, o servidor de destino enviará uma mensagem de acesso negado ao cliente não autenticado.

O uso da criptografia atenua esses possíveis problemas de segurança.

## <a name="configuring-a-proxy-server-for-winrm-11-and-earlier"></a>Configurando um servidor proxy para o WinRM 1,1 e anterior

Se um proxy for necessário para acessar o servidor WinRM, o cliente WinRM dependerá da configuração de proxy do WinHTTP (serviços HTTP do Windows). Por padrão, o WinHTTP não está configurado para usar um servidor proxy. A configuração de proxy WinHTTP pode ser alterada usando os utilitários de linha de comando [ProxyCfg.exe](/previous-versions/windows/desktop/ms761351(v=vs.85)) ou [netsh](/previous-versions/windows/it-pro/windows-server-2003/cc785383(v=ws.10)) .

**WinRM 1,1 e anterior:** O WinRM não usa as configurações de proxy do Internet Explorer.

 

 