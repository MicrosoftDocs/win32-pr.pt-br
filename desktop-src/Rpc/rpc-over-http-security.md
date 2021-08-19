---
title: Segurança de RPC sobre HTTP
description: O RPC sobre HTTP fornece três tipos de segurança, além da segurança RPC padrão, o que resulta na proteção do tráfego RPC sobre HTTP uma vez por RPC e, em seguida, com proteção dupla pelo mecanismo de encapsulamento fornecido pelo RPC sobre HTTP.
ms.assetid: 3a44c72b-b74c-433a-8826-1f76ca019f40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9f1ebd5a7198a2b2ccae7703b92011bbd45b037db2f7ef8eb116e28ef06d8e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118926122"
---
# <a name="rpc-over-http-security"></a>Segurança de RPC sobre HTTP

O RPC sobre HTTP fornece três tipos de segurança, além da segurança RPC padrão, o que resulta na proteção do tráfego RPC sobre HTTP uma vez por RPC e, em seguida, com proteção dupla pelo mecanismo de encapsulamento fornecido pelo RPC sobre HTTP. Para obter uma descrição dos mecanismos de segurança RPC padrão, consulte [segurança](security.md). O mecanismo de túnel RPC sobre HTTP adiciona à segurança RPC normal da seguinte maneira:

-   Fornece segurança através do IIS (disponível somente para RPC sobre HTTP v2).
-   Fornece criptografia SSL e verificação de proxy RPC (autenticação mútua). Também disponível somente no RPC por HTTP v2.
-   Fornece restrições sobre o nível de proxy RPC que determina quais computadores na rede do servidor têm permissão para receber RPC sobre chamadas HTTP.

Cada um desses três recursos de segurança é descrito mais detalhadamente nas seções a seguir.

## <a name="iis-authentication"></a>Autenticação IIS

O RPC sobre HTTP pode aproveitar o mecanismo de autenticação normal do IIS. O diretório virtual para proxy RPC pode ser configurado usando o nó RPC no site padrão no snap-in IIS MMC:

![Captura de tela mostrando o nó RPC no site da Web padrão no snap-in do MMC do IIS.](images/rpc-http-1.png)

O IIS pode ser configurado para desabilitar o acesso anônimo e exigir autenticação para o diretório virtual para o proxy RPC. Para fazer isso, clique com o botão direito do mouse no nó RPC e selecione **Propriedades**. Selecione a guia **segurança de diretório** e clique no botão **Editar** no grupo **autenticação e controle de acesso** , conforme ilustrado aqui:

![Captura de tela mostrando a caixa de diálogo Propriedades RPC.](images/rpc-http-2.png)

Embora você possa usar RPC sobre HTTP mesmo quando o diretório virtual de proxy RPC permite acesso anônimo, a Microsoft recomenda enfaticamente a desabilitação do acesso anônimo a esse diretório virtual por motivos de segurança. em vez disso, para RPC sobre HTTP, habilite a autenticação básica, Windows autenticação integrada ou ambas. lembre-se de que somente RPC sobre HTTP v2 é capaz de se autenticar no Proxy RPC que requer autenticação básica ou integrada de Windows; RPC sobre HTTP v1 não poderá se conectar se não **permitir acesso anônimo** estiver desabilitado. como o RPC sobre HTTP v2 é a implementação mais segura e robusta, o uso de uma versão do Windows que dá suporte a ela melhorará a segurança de suas instalações.

> [!Note]  
> Por padrão, o diretório virtual do proxy RPC está marcado para permitir acesso anônimo. No entanto, o proxy RPC para RPC sobre HTTP v2 rejeita solicitações que não são autenticadas por padrão.

 

## <a name="traffic-encryption"></a>Criptografia de tráfego

O RPC sobre HTTP pode criptografar o tráfego entre o cliente RPC sobre HTTP e o proxy RPC com SSL. O tráfego entre o proxy RPC e o servidor RPC sobre HTTP é criptografado usando mecanismos de segurança RPC normais e não usa SSL (mesmo que o SSL entre o cliente e o proxy RPC seja escolhido). Isso ocorre porque essa parte do tráfego viaja dentro da rede de uma organização e por trás de um firewall.

O tráfego entre o cliente RPC sobre HTTP e o proxy RPC, que geralmente viaja pela Internet, pode ser criptografado com SSL, além de qual mecanismo de criptografia foi escolhido para RPC. Nesse caso, o tráfego na parte da Internet da rota se torna criptografado duplamente. A criptografia de tráfego por meio do proxy RPC fornece uma defesa secundária, caso o proxy RPC ou outros computadores na rede de perímetro sejam comprometidos. Como o proxy RPC não pode descriptografar a camada de criptografia secundária, o proxy RPC não tem acesso aos dados que estão sendo enviados. confira [Recomendações de implantação RPC sobre HTTP](rpc-over-http-deployment-recommendations.md) para obter mais informações. A criptografia SSL está disponível somente com RPC sobre HTTP v2.

## <a name="restricting-rpc-over-http-calls-to-certain-computers"></a>Restringindo chamadas RPC sobre HTTP para determinados computadores

A configuração de segurança do IIS é baseada em intervalos de computadores e portas permitidos. A capacidade de usar RPC sobre HTTP é controlada por duas entradas do registro no computador que executa o IIS e o proxy RPC. A primeira entrada é um sinalizador que alterna a funcionalidade do proxy RPC. A segunda é uma lista opcional de computadores para os quais o proxy pode encaminhar chamadas RPC.

Por padrão, um cliente que entra em contato com o proxy RPC para túnel RPC sobre chamadas HTTP não pode acessar nenhum processo de servidor RPC, exceto os processos do servidor RPC sobre HTTP em execução no mesmo computador que o proxy RPC. Se o sinalizador habilitado não for definido ou definido como um valor zero, o IIS desabilitará o proxy RPC. Se o sinalizador habilitado for definido e definido como um valor diferente de zero, um cliente poderá se conectar ao RPC sobre servidores HTTP no computador que executa o IIS. Para permitir que o cliente seja encapsulado em um processo RPC sobre o servidor HTTP em outro computador, você deve adicionar uma entrada de registro à lista de servidores RPC sobre HTTP do computador IIS.

Os servidores RPC não podem aceitar chamadas RPC sobre HTTP, a menos que solicitou especificamente que o RPC escutasse no RPC sobre HTTP.

O exemplo a seguir demonstra como configurar o registro para permitir que os clientes se conectem a servidores pela Internet:

```
HKEY_LOCAL_MACHINE\
   Software\Microsoft\Rpc\RpcProxy\Enabled:REG_DWORD
   Software\Microsoft\Rpc\RpcProxy\ValidPorts:REG_SZ
```

A entrada **ValidPorts** é uma \_ entrada reg sz que contém uma lista de computadores aos quais o proxy RPC do IIS tem permissão para encaminhar chamadas RPC e as portas que ele deve usar para se conectar aos servidores RPC. A \_ entrada reg sz usa o seguinte formato: Rosco: 593; Rosco: 2000-8000; dados \* : 4000-8000.

Neste exemplo, o IIS pode encaminhar chamadas RPC sobre HTTP para o servidor "Rosco" nas portas 593 e 2000 até 8000. Ele também pode enviar chamadas para qualquer servidor cujo nome comece com "dados". Ele se conectará nas portas 4000 a 8000. Além disso, antes de encaminhar o tráfego para uma determinada porta no servidor RPC sobre HTTP, o proxy RPC executa uma troca de pacotes especial com o serviço RPC escutando nessa porta para verificar se está disposto a aceitar solicitações por HTTP.

Para obter um exemplo com base nessas configurações de exemplo, se um serviço RPC escuta na porta 4500 no servidor "data1", mas não chamou uma das funções [ * *RpcServerUseProtseq \** _](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) com _ * ncacn \_ http * *, ele rejeitará a solicitação. Esse comportamento fornece proteção adicional para servidores que escutam em uma porta aberta devido a um erro de configuração; a menos que o servidor solicitado especificamente a escutar no RPC sobre HTTP, ele não receberá chamadas provenientes de fora do firewall.

As entradas na chave **ValidPorts** devem ser uma correspondência exata do servidor RPC sobre http solicitado pelo cliente (não diferencia maiúsculas de minúsculas). Para simplificar o processamento, o proxy RPC não executa a canonização do nome fornecido pelo cliente RPC sobre HTTP. Portanto, se o cliente solicitar rosco.microsoft.com e, em **ValidPorts** , contiver somente Rosco, o proxy RPC não corresponderá aos nomes, mesmo que ambos os nomes possam se referir ao mesmo computador. Além disso, se o endereço IP de Rosco for 66.77.88.99 e o cliente solicitar 66.77.88.99, mas a chave **ValidPorts** contiver apenas Rosco, o proxy RPC recusará a conexão. Se um cliente pode solicitar o RPC sobre o servidor HTTP por nome ou por endereço IP, insira ambos na chave **ValidPorts** .

> [!Note]  
> Embora o RPC esteja habilitado para IPv6, o proxy RPC não oferece suporte a endereços IPv6 na chave **ValidPorts** . Se o IPv6 for usado para conectar o proxy RPC e o servidor RPC sobre HTTP, somente os nomes DNS poderão ser usados.

 

O IIS lê as entradas de registro **Enabled** e **ValidPorts** na inicialização. Além disso, o RPC sobre HTTP lê novamente o conteúdo da chave **ValidPorts** aproximadamente a cada 5 minutos. Se a entrada **ValidPorts** for alterada, as alterações serão implementadas em 5 minutos.

**RPC sobre http V1:** O serviço WEB deve ser interrompido e reiniciado usando a Service Manager da Internet para obter novos valores nas entradas do registro a serem implementadas.

 

 




