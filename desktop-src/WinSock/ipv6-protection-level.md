---
description: A \_ opção de soquete de nível de proteção IPv6 \_ permite que os desenvolvedores coloquem restrições de acesso em soquetes IPv6.
ms.assetid: bfb934b3-1e86-431f-a21c-880048d32d35
title: IPV6_PROTECTION_LEVEL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e2a8dd70bb1fb5b21f74f8939f11da0d9e2a3ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105810628"
---
# <a name="ipv6_protection_level"></a>\_Nível de proteção IPv6 \_

A \_ opção de soquete de nível de proteção IPv6 \_ permite que os desenvolvedores coloquem restrições de acesso em soquetes IPv6. Essas restrições permitem que um aplicativo em execução em uma LAN privada proteja-se de modo simples e robusto contra ataques externos. A \_ opção de soquete de nível de proteção IPv6 \_ amplia ou limita o escopo de um soquete de escuta, habilitando o acesso irrestrito de usuários públicos e privados quando apropriado ou restringindo o acesso somente ao mesmo site, conforme necessário.

\_No momento, o nível de proteção IPv6 \_ tem três níveis de proteção definidos.



| Nível de proteção                                                                                                                                 | Descrição                                                                                                                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PROTECTION_LEVEL_UNRESTRICTED"></span><span id="protection_level_unrestricted"></span>nível de proteção \_ \_ irrestrito<br/>       | Usado por aplicativos projetados para operar na Internet, incluindo aplicativos que aproveitam recursos de passagem NAT do IPv6 incorporados ao Windows (Teredo, por exemplo). Esses aplicativos podem ignorar firewalls IPv4, de modo que os aplicativos devem ser protegidos contra ataques de Internet direcionados à porta aberta.<br/> |
| <span id="PROTECTION_LEVEL_EDGERESTRICTED"></span><span id="protection_level_edgerestricted"></span>nível de proteção \_ \_ EDGERESTRICTED<br/> | Usado por aplicativos projetados para operar pela Internet. Essa configuração não permite passagem NAT usando a implementação do Windows Teredo. Esses aplicativos podem ignorar firewalls IPv4, de modo que os aplicativos devem ser protegidos contra ataques de Internet direcionados à porta aberta.<br/>                                   |
| <span id="PROTECTION_LEVEL_RESTRICTED"></span><span id="protection_level_restricted"></span>nível de proteção \_ \_ restrito<br/>             | Usado por aplicativos de intranet que não implementam cenários da Internet. Esses aplicativos geralmente não são testados nem protegidos contra ataques do estilo usado na Internet.<br/> Essa configuração limitará o tráfego recebido para apenas link-local.<br/>                                                                             |



 

O exemplo de código a seguir fornece os valores definidos para cada um:

``` syntax
#define PROTECTION_LEVEL_UNRESTRICTED   10  /* for peer-to-peer apps */
#define PROTECTION_LEVEL_EDGERESTRICTED 20  /* Same as unrestricted, except for Teredo  */
#define PROTECTION_LEVEL_RESTRICTED     30  /* for Intranet apps     */
```

Esses valores são mutuamente exclusivos e não podem ser combinados em uma única chamada de função [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) . Outros valores para essa opção de soquete são reservados. Esses níveis de proteção se aplicam somente a conexões de entrada. A definição dessa opção de soquete não tem nenhum efeito sobre os pacotes de saída ou conexões.

No Windows 7 e no Windows Server 2008 R2, o valor padrão para o \_ nível de proteção IPv6 \_ não é especificado e o **\_ \_ padrão de nível de proteção** é definido como-1, um valor ilegal para o nível de proteção IPv6 \_ \_ .

No Windows Vista e no Windows Server 2008, o valor padrão para o \_ nível de proteção IPv6 é o nível de \_ **proteção \_ \_ irrestrito** e o **\_ \_ padrão de nível de proteção** é definido como-1, um valor ilegal para o nível de proteção IPv6 \_ \_ .

No Windows Server 2003 e no Windows XP, o valor padrão para o \_ nível de proteção IPv6 é o nível de \_ **proteção \_ \_ EDGERESTRICTED** e o **\_ \_ padrão de nível de proteção** é definido para ser o nível de **proteção \_ \_ EDGERESTRICTED**.

> [!Note]  
> A \_ opção de soquete de nível de proteção IPv6 \_ deve ser definida antes do soquete ser associado. Caso contrário, os pacotes recebidos entre chamadas [**BIND**](/windows/desktop/api/winsock/nf-winsock-bind) e [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) estarão em conformidade com o **nível de proteção \_ \_ EDGERESTRICTED** e poderão ser entregues ao aplicativo.

 

A tabela a seguir descreve o efeito de aplicar cada nível de proteção a um soquete de escuta.

Nível de proteção

Tráfego de entrada permitido

Mesmo site

Externo

NAT Traversal (Teredo)

nível de proteção \_ \_ restrito

Sim

Não

Não

nível de proteção \_ \_ EDGERESTRICTED

Sim

Sim

Não

nível de proteção \_ \_ irrestrito

Sim

Sim

Sim



 

Na tabela acima, a mesma coluna de **site** é uma combinação do seguinte:

-   Vincular endereços locais
-   Endereços locais do site
-   Endereços globais conhecidos por pertencerem ao mesmo site (correspondendo à tabela de prefixo do site)

No Windows 7 e no Windows Server 2008 R2, o valor padrão para o \_ nível de proteção IPv6 \_ não é especificado. Se não houver nenhum software de firewall com reconhecimento de borda instalado no computador local (o Firewall do Windows está desabilitado ou algum outro firewall está instalado e ignora o tráfego de Teredo), você receberá o tráfego de Teredo somente se definir a \_ opção de soquete de nível de proteção IPv6 \_ como nível de **proteção \_ \_ irrestrito**. No entanto, o Firewall do Windows ou qualquer política de firewall com reconhecimento de borda transversal pode ignorar essa opção com base nas configurações de política do firewall. Ao definir essa opção de soquete para o **nível de proteção \_ \_ irrestrito**, o aplicativo está comunicando sua intenção explícita de receber o tráfego de borda atravessado pelo firewall do host instalado no computador local. Portanto, se houver um firewall de host com reconhecimento de borda, ele terá a decisão final sobre a aceitação de um pacote. Por padrão, sem qualquer conjunto de opções de soquete:

-   o se o Firewall do Windows estiver habilitado (ou se outro firewall de host com reconhecimento de borda estiver instalado) no computador local, o que for imposto será observado. O firewall de host com reconhecimento de borda típico bloqueará o tráfego de Teredo por padrão. Portanto, os aplicativos observarão o padrão como se fosse o **nível de proteção \_ \_ EDGERESTRICTED**.
-   o se o Firewall do Windows não estiver habilitado e nenhum outro firewall de host com reconhecimento de borda estiver instalado no sistema local, o padrão será **o \_ nível \_ de proteção EDGERESTRICTED**.

No Windows Vista e no Windows Server 2008, o valor padrão para \_ nível de proteção IPv6 \_ é o nível de **proteção \_ \_ irrestrito**. Mas o valor efetivo depende se o Firewall do Windows está habilitado. O Firewall do Windows tem reconhecimento de percurso de borda (reconhecimento de Teredo), independentemente do valor definido para o nível de proteção IPV6 e ignora se o nível de proteção \_ \_ IPv6 \_ \_ é **\_ \_ irrestrito no nível de proteção**. Portanto, o valor efetivo depende da política de firewall. Quando o Firewall do Windows está desabilitado e nenhum outro firewall com reconhecimento de borda, está instalado no computador local, o valor padrão do \_ nível de proteção IPv6 \_ é **\_ \_ irrestrito de nível de proteção**.

No Windows Server 2003 e no Windows XP, o valor padrão para o \_ nível de proteção IPv6 é o nível de \_ **proteção \_ \_ EDGERESTRICTED**. A menos que você tenha definido a \_ opção de soquete de nível de proteção IPv6 para o \_ **nível de proteção \_ \_ irrestrito**, você não receberá nenhum tráfego Teredo.

Dependendo do nível de proteção do IPV6 \_ \_ , um aplicativo que requer tráfego não solicitado da Internet pode não ser capaz de receber tráfego não solicitado. No entanto, esses requisitos não são necessários para receber tráfego solicitado pela interface do Windows Teredo. Para obter mais detalhes sobre a interação com o Teredo, consulte [recebendo tráfego solicitado por Teredo](../teredo/receiving-solicited-traffic-over-teredo.md).

Quando os pacotes de entrada ou conexões são recusados devido ao nível de proteção definido, a rejeição é tratada como se nenhum aplicativo estivesse escutando nesse soquete.

> [!Note]
>
> A opção de soquete de nível de proteção IPV6 não \_ \_ necessariamente coloca restrições de acesso em soquetes IPv6 ou restrição de NAT transversal usando algum método diferente do Windows Teredo ou até mesmo usando outra implementação de Teredo por outro fornecedor.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[Recebendo tráfego solicitado por Teredo](../teredo/receiving-solicited-traffic-over-teredo.md)
</dt> <dt>

[**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> </dl>

 

 
