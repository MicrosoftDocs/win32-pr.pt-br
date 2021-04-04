---
title: Configuração de IPsec
description: A WFP (Windows Filtering Platform) é a plataforma subjacente para o Firewall do Windows com segurança avançada.
ms.assetid: d54b5caa-daea-4231-9909-7a8d388df661
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78af8e3d0a23713c0505082555fe260bc562dfa4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103917246"
---
# <a name="ipsec-configuration"></a>Configuração de IPsec

A WFP (Windows Filtering Platform) é a plataforma subjacente para o Firewall do Windows com segurança avançada. A WFP é usada para configurar regras de filtragem de rede, que incluem regras que regem a proteção do tráfego de rede com IPsec. Os desenvolvedores de aplicativos podem configurar o IPsec diretamente usando a API WFP, a fim de aproveitar um modelo de filtragem de tráfego de rede mais granular do que o modelo exposto por meio do snap-in do MMC (console de gerenciamento Microsoft) para o Firewall do Windows com segurança avançada.

## <a name="what-is-ipsec"></a>O que é IPsec

O IPsec (Internet Protocol Security) é um conjunto de protocolos de segurança usados para transferir os pacotes de IP confidencialmente pela Internet. O IPsec é obrigatório para todas as implementações de IPv6 e opcional para IPv4.

O tráfego IP protegido tem dois cabeçalhos IPsec opcionais, que identificam os tipos de proteção de criptografia aplicados ao pacote IP e incluem informações para decodificar o pacote protegido.

O cabeçalho da carga de segurança de encapsulamento (ESP) é usado para privacidade e proteção contra modificações mal-intencionadas por meio da autenticação e criptografia opcional. Ele pode ser usado para tráfego que atravessa roteadores NAT (conversão de endereços de rede).

O Cabeçalho de Autenticação (AH) é usado somente para proteção contra modificações mal-intencionadas por meio da autenticação. Ele não pode ser usado para tráfego que atravessa roteadores NAT.

Para obter mais informações sobre IPsec, consulte também:

<dl>

[Referência técnica de IPsec](/previous-versions/windows/it-pro/windows-server-2003/cc740240(v=ws.10))  
</dl>

## <a name="what-is-ike"></a>O que é IKE

O protocolo IKE (IKE) é um protocolo de troca de chaves que faz parte do conjunto de protocolos IPsec. O IKE é usado durante a configuração de uma conexão segura e realiza a troca segura de chaves secretas e outros parâmetros relacionados à proteção sem a intervenção do usuário.

Para obter mais informações sobre IKE, consulte também:

<dl>

[protocolo IKE](/previous-versions/windows/it-pro/windows-server-2003/cc784994(v=ws.10))  
</dl>

## <a name="what-is-authip"></a>O que é AuthIP

O protocolo Authenticated IP (AuthIP) é um novo protocolo de troca de chaves que expande o IKE da seguinte maneira.

<dl> Embora o IKE dê suporte apenas às credenciais de autenticação do computador, o AuthIP também oferece suporte a:

-   Credenciais do usuário: NTLM, Kerberos, certificados.
-   Certificados de integridade NAP (proteção de acesso à rede).
-   Credencial anônima, usada para autenticação opcional.
-   Combinação de credenciais; por exemplo, uma combinação de credenciais Kerberos de computador e de usuário.

  
O AuthIP tem um mecanismo de repetição de autenticação que verifica todos os métodos de autenticação configurados antes de falhar a conexão.  
O AuthIP pode ser usado com soquetes seguros para implementar o tráfego protegido por IPsec baseado em aplicativo. Ele fornece:

-   Autenticação por soquete e criptografia. Consulte [**WSASetSocketSecurity**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity) para obter mais informações.
-   Representação do cliente. (O IPsec representa o contexto de segurança no qual o soquete é criado.)
-   Validação de nome de par de entrada e saída. Consulte [**WSASetSocketPeerTargetName**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname) para obter mais informações.

  
</dl>

Para obter mais informações sobre AuthIP, consulte também:

<dl>

[AuthIP no Windows Vista](https://www.microsoft.com/technet/community/columns/cableguy/cg0806.mspx)  
</dl>

## <a name="what-is-an-ipsec-policy"></a>O que é uma política IPsec

Uma política IPsec é um conjunto de regras que determinam qual tipo de tráfego IP precisa ser protegido usando IPsec e como proteger esse tráfego. Apenas uma política IPsec está ativa em um computador ao mesmo tempo.

Para saber mais sobre como implementar diretivas IPsec, abra o snap-in do MMC diretiva de segurança local (secpol. msc), pressione F1 para exibir a ajuda e, em seguida, selecione criando e usando políticas IPsec do Sumário.

Para obter mais informações sobre diretivas IPsec, consulte também:

<dl>

[Visão geral dos conceitos da política IPsec](/previous-versions/windows/it-pro/windows-server-2003/cc776080(v=ws.10))  
[Descrição de uma política IPsec](/previous-versions/windows/it-pro/windows-server-2003/cc781593(v=ws.10))  
</dl>

## <a name="how-to-use-wfp-to-configure-ipsec-policies"></a>Como usar o WFP para configurar as políticas de IPsec

A implementação do IPsec da Microsoft usa a plataforma de filtragem do Windows para configurar as políticas de IPsec. As diretivas IPsec são implementadas pela adição de filtros em várias camadas de WFP, como a seguir.

-   Na camada FWPM \_ \_ IKEEXT \_ V {4 \| 6} camadas, adicione filtros que especificam as políticas de negociação usadas pelos módulos de chaveamento (Ike/AuthIP) durante as trocas de modo principal (mm). Os métodos de autenticação e os algoritmos criptográficos são especificados nessas camadas.
-   Na camada FWPM \_ \_ IPSec \_ V {4 \| 6} camadas, adicione filtros que especificam as políticas de negociação usadas pelos módulos de criação de chaves durante as trocas de modo rápido (QM) e modo estendido (em). Os cabeçalhos IPsec (AH/ESP) e os algoritmos criptográficos são especificados nessas camadas.

    Uma política de negociação é especificada como um contexto de provedor de política associado ao filtro. O módulo de chaveamento enumera os contextos do provedor de política com base nas características de tráfego e obtém a política a ser usada para a negociação de segurança.

    > [!Note]  
    > A API WFP pode ser usada para especificar as associações de segurança (SAs) diretamente e, portanto, ignorar a política de negociação do módulo de chave.

     

-   Nas camadas FWPM do \_ transporte de entrada da camada \_ \_ \_ v {4 \| 6} e do transporte de saída da camada do FWPM \_ \_ \_ \_ v {4 \| 6}, adicione filtros que invoquem textos explicativos e determine qual fluxo de tráfego deve ser protegido.
-   No FWPM da \_ camada \_ de \_ autenticação Ale, aceite as \_ \_ \_ camadas V {4 \| 6} adicionar filtros que implementam a filtragem de identidade e a política por aplicativo.

O diagrama a seguir ilustra a interação dos vários componentes de WFP, em relação à operação de IPsec.![configuração de IPSec usando a plataforma de filtragem do Windows](images/ipsec-configuration.jpg)

Quando o IPsec é configurado, ele se integra com o WFP e estende os recursos de filtragem de WFP, fornecendo informações a serem usadas como condições de filtragem nas camadas de autorização da camada de aplicação (ALE). Por exemplo, o IPsec fornece a identidade do usuário remoto e do computador remoto, que a WFP expõe na conexão ALE e aceita camadas de autorização. Essas informações podem ser usadas para a autorização de identidade remota refinada por uma implementação de firewall baseada em WFP.

Veja abaixo uma política de isolamento de exemplo que pode ser implementada usando o IPsec:

-   Camadas FWPM de \_ camada \_ \_ V { \| 4 6} – autenticação Kerberos.
-   \_Camada FWPM \_ IPSec \_ V {4 \| 6} camadas – Ah/SHA-1.
-   \_ \_ Transporte de entrada da camada FWPM \_ \_ v {4 \| 6} e \_ FWPM \_ camada \_ de transporte de saída \_ v {4 \| 6} camadas – descoberta de negociação para todo o tráfego de rede.
-   FWPM \_ de \_ autenticação Ale de camada \_ \_ \_ \_ de rede aceita V {4 \| 6} camadas-IPSec necessário para todo o tráfego de redes.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Camadas WFP**
</dt> <dt>

[**Filtrando identificadores de camada**](management-filtering-layer-identifiers-.md)
</dt> <dt>

[Camadas ALE](ale-layers.md)
</dt> <dt>

**Cenários de política IPsec implementados usando a API WFP:**
</dt> <dt>

[Modo de transporte](regular-transport-mode.md)
</dt> <dt>

[Modo de transporte de descoberta de negociação](negotiation-discovery-transport-mode.md)
</dt> <dt>

[Modo de transporte de descoberta de negociação no modo de limite](negotiation-discovery-transport-mode-in-boundary-mode.md)
</dt> <dt>

[Modo de túnel](tunnel-mode.md)
</dt> <dt>

[Criptografia garantida](guaranteed-encryption.md)
</dt> <dt>

[Autorização de identidade remota](remote-identity-authorization.md)
</dt> <dt>

[SAs IPsec manual](manual-ipsec-sas.md)
</dt> <dt>

[Isenções de IKE/AuthIP](ike-exemptions.md)
</dt> <dt>

**Soluções IPsec:**
</dt> <dt>

[Isolamento de domínio e servidor](/previous-versions/windows/it-pro/windows-server-2003/cc776080(v=ws.10))
</dt> </dl>

 

 