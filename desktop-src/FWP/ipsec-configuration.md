---
title: Configuração do IPsec
description: Windows A WFP (Plataforma de Filtragem) é a plataforma subjacente para Windows Firewall com Segurança Avançada.
ms.assetid: d54b5caa-daea-4231-9909-7a8d388df661
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34cf20fc8c95aafe3c387195b02468cec3ce884cc97287adde44a594305ee189
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069006"
---
# <a name="ipsec-configuration"></a>Configuração do IPsec

Windows A WFP (Plataforma de Filtragem) é a plataforma subjacente para Windows Firewall com Segurança Avançada. O WFP é usado para configurar regras de filtragem de rede, que incluem regras que regem a proteção do tráfego de rede com IPsec. Os desenvolvedores de aplicativos podem configurar o IPsec diretamente usando a API do WFP para aproveitar um modelo de filtragem de tráfego de rede mais granular do que o modelo exposto por meio do snap-in do MMC (Console de Gerenciamento Microsoft) para o Firewall do Windows com Segurança Avançada.

## <a name="what-is-ipsec"></a>O que é o IPsec

O IPsec (Internet Protocol Security) é um conjunto de protocolos de segurança usados para transferir pacotes IP confidencialmente pela Internet. O IPsec é obrigatório para todas as implementações de IPv6 e opcional para IPv4.

O tráfego IP protegido tem dois headers IPsec opcionais, que identificam os tipos de proteção criptográfica aplicada ao pacote IP e incluem informações para decodificar o pacote protegido.

O título ESP (Conteúdo de Segurança de Encapsulamento) é usado para privacidade e proteção contra modificações mal-intencionadas executando autenticação e criptografia opcional. Ele pode ser usado para tráfego que atravessa roteadores NAT (Conversão de Endereços de Rede).

O Cabeçalho de Autenticação (AH) é usado apenas para proteção contra modificações mal-intencionadas executando a autenticação. Ele não pode ser usado para o tráfego que atravessa roteadores NAT.

Para obter mais informações sobre o IPsec, confira também:

<dl>

[Referência técnica do IPsec](/previous-versions/windows/it-pro/windows-server-2003/cc740240(v=ws.10))  
</dl>

## <a name="what-is-ike"></a>O que é IKE

O IKE (internet key Exchange) é um protocolo de troca de chaves que faz parte do conjunto de protocolos IPsec. O IKE é usado durante a configuração de uma conexão segura e realiza a troca segura de chaves secretas e outros parâmetros relacionados à proteção sem a intervenção do usuário.

Para obter mais informações sobre o IKE, confira também:

<dl>

[Chave da Internet Exchange](/previous-versions/windows/it-pro/windows-server-2003/cc784994(v=ws.10))  
</dl>

## <a name="what-is-authip"></a>O que é a AuthIP

protocolo Authenticated IP (AuthIP) é um novo protocolo de troca de chaves que expande o IKE da seguinte forma.

<dl> Embora o IKE só seja compatível com credenciais de autenticação de computador, o AuthIP também dá suporte a:

-   Credenciais do usuário: NTLM, Kerberos, certificados.
-   Certificados de saúde nap (Proteção de Acesso à Rede).
-   Credencial anônima, usada para autenticação opcional.
-   Combinação de credenciais; por exemplo, uma combinação de credenciais Kerberos do computador e do usuário.

  
O AuthIP tem um mecanismo de autenticação de nova tentativa que verifica todos os métodos de autenticação configurados antes de falhar a conexão.  
O AuthIP pode ser usado com soquetes seguros para implementar o tráfego protegido IPsec baseado em aplicativo. Ele fornece:

-   Autenticação e criptografia por soquete. Consulte [**WSASetSocketSecurity para**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity) obter mais informações.
-   Representação do cliente. (O IPsec representa o contexto de segurança no qual o soquete é criado.)
-   Validação de nome de par de entrada e saída. Consulte [**WSASetSocketPeerTargetName**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname) para obter mais informações.

  
</dl>

Para obter mais informações sobre o AuthIP, confira também:

<dl>

[AuthIP no Windows Vista](https://www.microsoft.com/technet/community/columns/cableguy/cg0806.mspx)  
</dl>

## <a name="what-is-an-ipsec-policy"></a>O que é uma política IPsec

Uma política de IPsec é um conjunto de regras que determinam qual tipo de tráfego IP precisa ser protegido usando IPsec e como proteger esse tráfego. Apenas uma política IPsec está ativa em um computador ao mesmo tempo.

Para saber mais sobre como implementar políticas IPsec, abra o snap-in MMC da Política de Segurança Local (secpol.msc), pressione F1 para exibir a Ajuda e, em seguida, selecione Criando e usando políticas IPsec no tabela de conteúdo.

Para obter mais informações sobre políticas IPsec, consulte também:

<dl>

[Visão geral dos conceitos de política do IPsec](/previous-versions/windows/it-pro/windows-server-2003/cc776080(v=ws.10))  
[Descrição de uma política IPsec](/previous-versions/windows/it-pro/windows-server-2003/cc781593(v=ws.10))  
</dl>

## <a name="how-to-use-wfp-to-configure-ipsec-policies"></a>Como usar o WFP para configurar políticas IPsec

A implementação da Microsoft do IPsec usa Windows Filtering Platform para configurar políticas de IPsec. As políticas de IPsec são implementadas adicionando filtros em várias camadas do WFP da seguinte forma.

-   Nas camadas da CAMADA FWPM IKEEXT V{4 6}, adicione filtros que especificam as políticas de negociação usadas pelos módulos de chave \_ \_ \_ \| (IKE/AuthIP) durante as trocas de MM (Modo Principal). Métodos de autenticação e algoritmos criptográficos são especificados nessas camadas.
-   Nas \_ \_ camadas IPSEC V{4 6} da CAMADA FWPM, adicione filtros que especificam as políticas de negociação usadas pelos módulos de chave durante as trocas do Modo Rápido \_ \| (QM) e do Modo Estendido (EM). Os headers IPsec (AH/ESP) e os algoritmos criptográficos são especificados nessas camadas.

    Uma política de negociação é especificada como um contexto de provedor de política associado ao filtro. O módulo de chave enumera os contextos do provedor de política com base nas características de tráfego e obtém a política a ser usada para a negociação de segurança.

    > [!Note]  
    > A API do WFP pode ser usada para especificar as SAs (Associações de Segurança) diretamente e, portanto, ignorar a política de negociação do módulo de chave.

     

-   Nas camadas FWPM \_ LAYER \_ INBOUND \_ TRANSPORT \_ V{4 \| 6} e FWPM \_ LAYER \_ OUTBOUND TRANSPORT \_ \_ V{4 \| 6} adicionam filtros que invocam textos explicadores e determinam qual fluxo de tráfego deve ser protegido.
-   Nas camadas DO \_ \_ ALE \_ AUTH \_ RECV \_ ACCEPT \_ V{4 \| 6} da CAMADA FWPM, adicione filtros que implementam a filtragem de identidade e a política por aplicativo.

O diagrama a seguir ilustra a interação dos vários componentes do WFP em relação à operação IPsec.![configuração de ipsec usando a plataforma de filtragem do Windows](images/ipsec-configuration.jpg)

Depois que o IPsec é configurado, ele se integra ao WFP e estende os recursos de filtragem do WFP fornecendo informações a serem usadas como condições de filtragem nas camadas de autorização da ALE (Imposição da Camada de Aplicativo). Por exemplo, o IPsec fornece a identidade remota do usuário e do computador remoto, que o WFP expõe nas camadas de autorização ALE connect e accept. Essas informações podem ser usadas para autorização de identidade remota desalocada por uma implementação de firewall baseada em WFP.

Veja abaixo uma política de isolamento de exemplo que pode ser implementada usando IPsec:

-   Camadas \_ \_ IKEEXT V{4 6} da CAMADA FWPM \_ \| – autenticação Kerberos.
-   CamadaS \_ \_ IPSEC \_ V{4 6} da CAMADA FWPM \| – AH/SHA-1.
-   Camada FWPM \_ TRANSPORT \_ \_ V{4 6} e camadas \_ \| FWPM \_ LAYER \_ OUTBOUND TRANSPORT \_ \_ V{4 \| 6} – descoberta de negociação para todo o tráfego de rede.
-   Camadas DE \_ \_ ALE \_ AUTH \_ RECV \_ ACCEPT \_ V{4 \| 6} da CAMADA FWPM – IPsec necessária para todo o tráfego de rede.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Camadas WFP**
</dt> <dt>

[**Filtrando identificadores de camada**](management-filtering-layer-identifiers-.md)
</dt> <dt>

[Camadas ALE](ale-layers.md)
</dt> <dt>

**Cenários de política IPsec implementados usando a API do WFP:**
</dt> <dt>

[Modo de transporte](regular-transport-mode.md)
</dt> <dt>

[Modo de transporte de descoberta de negociação](negotiation-discovery-transport-mode.md)
</dt> <dt>

[Modo de transporte de descoberta de negociação no modo de limite](negotiation-discovery-transport-mode-in-boundary-mode.md)
</dt> <dt>

[Tunnel Modo](tunnel-mode.md)
</dt> <dt>

[Criptografia Garantida](guaranteed-encryption.md)
</dt> <dt>

[Autorização de Identidade Remota](remote-identity-authorization.md)
</dt> <dt>

[SAs IPsec manuais](manual-ipsec-sas.md)
</dt> <dt>

[Isenções de IKE/AuthIP](ike-exemptions.md)
</dt> <dt>

**Soluções IPsec:**
</dt> <dt>

[Isolamento de domínio e servidor](/previous-versions/windows/it-pro/windows-server-2003/cc776080(v=ws.10))
</dt> </dl>

 

 