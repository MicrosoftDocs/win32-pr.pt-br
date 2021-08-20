---
title: Constantes de DNS
description: As constantes a seguir são definidas para DNS na ordem de bytes do host.
ms.assetid: 95bc9193-7962-498a-9abd-c4718ac35f0f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61da11c9d8f5af28e2152bad5fe9c7b5eb6eb7d83fdb7f94c11e8c2f3c04d9f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118164152"
---
# <a name="dns-constants"></a>Constantes de DNS

As constantes a seguir são definidas para DNS na ordem de bytes do host.

## <a name="dns-record-types"></a>Tipos de registro DNS



| Constante           | Valor            |
|--------------------|------------------|
| \_tipo \_ de DNS A       | 0x0001           |
| tipo de DNS \_ \_ ns      | 0x0002           |
| tipo de DNS \_ \_ MD      | 0x0003           |
| tipo de DNS \_ \_ MF      | 0x0004           |
| tipo de DNS \_ \_ CNAME   | 0x0005           |
| tipo de DNS \_ \_ soa     | 0x0006           |
| tipo de DNS \_ \_ MB      | 0x0007           |
| tipo de DNS \_ \_ mg      | 0x0008           |
| tipo de DNS \_ \_ Sr      | 0x0009           |
| tipo de DNS \_ \_ nulo    | 0x000a           |
| tipo de DNS \_ \_ WKS     | 0x000b           |
| tipo de DNS \_ \_ PTR     | 0x000c           |
| tipo de DNS \_ \_ HINFO   | 0x000d           |
| tipo de DNS \_ \_ MINFO   | 0x000e           |
| tipo de DNS \_ \_ MX      | 0x000f           |
| \_texto do tipo DNS \_    | 0x0010           |
| tipo de DNS \_ \_ RP      | 0x0011           |
| tipo de DNS \_ \_ AFSDB   | 0x0012           |
| Tipo de DNS \_ \_ X25     | 0x0013           |
| tipo de DNS \_ \_ ISDN    | 0x0014           |
| tipo de DNS \_ \_ RT      | 0x0015           |
| tipo de DNS \_ \_ NSAP    | 0x0016           |
| tipo de DNS \_ \_ NSAPPTR | 0x0017           |
| \_SIG do tipo DNS \_     | 0x0018           |
| \_chave de tipo DNS \_     | 0x0019           |
| tipo de DNS \_ \_ px      | 0x001a           |
| \_GPOs de tipo DNS \_    | 0x001b           |
| tipo de DNS \_ \_ aaaa    | 0x001c           |
| tipo de DNS \_ \_ Loc     | 0x001d           |
| \_tipo DNS \_ NXT     | 0x001e           |
| tipo de DNS \_ \_ Eid     | 0x001F           |
| tipo de DNS \_ \_ NIMLOC  | 0x0020           |
| tipo de DNS \_ \_ SRV     | 0x0021           |
| tipo de DNS \_ \_ Atma    | 0x0022           |
| tipo de DNS \_ \_ NAPTR   | 0x0023           |
| tipo de DNS \_ \_ Kx      | 0x0024           |
| \_certificado de tipo DNS \_    | 0x0025           |
| Tipo de DNS \_ \_ a6      | 0x0026           |
| tipo de DNS \_ \_ dname   | 0x0027           |
| \_coletor de tipo DNS \_    | 0x0028           |
| \_opção de tipo de DNS \_     | 0x0029           |
| tipo de DNS \_ \_ DS      | 0x002B           |
| tipo de DNS \_ \_ RRSIG   | 0x002E           |
| tipo de DNS \_ \_ NSEC    | 0x002F           |
| tipo de DNS \_ \_ DNSKEY  | 0x0030           |
| tipo de DNS \_ \_ DHCID   | 0x0031           |
| tipo de DNS \_ \_ UINFO   | 0x0064           |
| \_UID DO \_ TIPO DNS     | 0x0065           |
| TIPO \_ \_ DNS GID     | 0x0066           |
| TIPO \_ DNS \_ UNSPEC  | 0x0067           |
| COMPLEMENTOS \_ DE \_ TIPO DNS   | 0x00f8           |
| TKEY \_ DE \_ TIPO DNS    | 0x00f9           |
| TIPO \_ DNS \_ TSIG    | 0x00fa           |
| \_TIPO DNS \_ IXFR    | 0x00fb           |
| TIPO \_ DNS \_ AXFR    | 0x00fc           |
| TIPO \_ \_ DNS MAILB   | 0x00fd           |
| TIPO \_ \_ DNS MAILA   | 0x00fe           |
| TIPO \_ DNS \_ ALL     | 0x00ff           |
| TIPO \_ DNS \_ ANY     | 0x00ff           |
| O TIPO \_ DNS \_ VENCE    | 0xff01           |
| TIPO DNS \_ \_ WINSR   | 0xff02           |
| TIPO \_ DNS \_ NBSTAT  | TIPO DNS \_ \_ WINSR |



 

## <a name="dns-class-types"></a>Tipos de classe DNS



| Constante             | Valor  |
|----------------------|--------|
| INTERNET \_ DA CLASSE \_ DNS | 0x0001 |
| CLASSE DNS \_ \_ CSNET    | 0x0002 |
| DNS \_ CLASS \_ CHAOS    | 0x0003 |
| CLASSE DNS \_ \_ HESIOD   | 0x0004 |
| CLASSE DNS \_ \_ NONE     | 0x00fe |
| CLASSE DNS \_ \_ ALL      | 0x00ff |
| CLASSE DNS \_ \_ ANY      | 0x00ff |



 

## <a name="dns-query-types"></a>Tipos de consulta DNS



| Constante                    | Valor  |
|-----------------------------|--------|
| CONSULTA \_ OPCODE \_ DNS          | 0x0000 |
| \_IQUERY DE OPCODE \_ DNS         | 0x0001 |
| STATUS \_ DO SERVIDOR OPCODE \_ \_ DNS | 0x0002 |
| \_OPCODE \_ DNS DESCONHECIDO        | 0x0003 |
| DNS \_ OPCODE \_ NOTIFY         | 0x0004 |
| ATUALIZAÇÃO \_ DO OPCODE \_ DNS         | 0x0005 |



 

## <a name="dns-record-flags"></a>Sinalizadores de registro DNS

Os sinalizadores a seguir referem-se à seção RR (registro de recurso) dentro de uma mensagem DNS:



| Constante           | Valor      | Significado                         |
|--------------------|------------|---------------------------------|
| PERGUNTA \_ DNSREC   | 0x00000000 | RR está na seção de pergunta   |
| RESPOSTA \_ DNSREC     | 0x00000001 | RR está na seção de resposta     |
| AUTORIDADE \_ DNSREC  | 0x00000002 | RR está na seção autoridade  |
| DNSREC \_ ADICIONAL | 0x00000003 | RR está na seção adicional |



 

Os sinalizadores a seguir referem-se à seção de uma RR dentro de uma mensagem DNS de atualização por [RFC 2136:](https://www.ietf.org/rfc/rfc2136.txt)



| Constante       | Valor      | Significado                           |
|----------------|------------|-----------------------------------|
| ZONA \_ DNSREC   | 0x00000000 | O RR está na seção de zona         |
| PRÉ-REQUISITO DE DNSREC \_ | 0x00000001 | O RR está na seção de pré-requisitos |
| ATUALIZAÇÃO \_ DNSREC | 0x00000002 | O RR está na seção de atualização       |



 

Os sinalizadores a seguir são mutuamente exclusivos:



| Constante        | Valor      | Significado                                                    |
|-----------------|------------|------------------------------------------------------------|
| DNSREC \_ DELETE  | 0x00000004 | Exclua um RR. Usado em conjunto com a \_ atualização do DNSREC       |
| DNSREC \_ NOexistente | 0x00000004 | RR não existe. Usado em conjunto com DNSREC \_ pré-requisito |



 

## <a name="dns-query-options"></a>Opções de consulta DNS



| Constante                                | Valor      | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-----------------------------------------|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_padrão de consulta DNS \_                    | 0x00000000 | Consulta padrão.                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| resposta do DNS \_ \_ aceita \_ respostas truncadas \_ | 0x00000001 | Retorna resultados truncados. Não tenta novamente em TCP.                                                                                                                                                                                                                                                                                                                                                                                                   |
| \_consulta DNS \_ usar \_ \_ somente TCP              | 0x00000002 | Usa TCP somente para a consulta.                                                                                                                                                                                                                                                                                                                                                                                                                           |
| \_consulta DNS \_ sem \_ recursão               | 0x00000004 | Direciona o servidor DNS para executar uma consulta iterativa (especificamente, direciona o servidor DNS para não executar a resolução recursiva para resolver a consulta).                                                                                                                                                                                                                                                                                                   |
| \_cache de \_ bypass de consulta DNS \_               | 0x00000008 | Ignora o cache do [*resolvedor*](r-gly.md) na pesquisa.                                                                                                                                                                                                                                                                                                                                                                            |
| consulta \_ DNS \_ sem \_ transmissão \_             | 0x00000010 | Direciona o DNS para executar uma consulta somente no cache local. **Windows servidor 2000 e Windows 2000 Professional:** Não há suporte para esse valor. Para funcionalidade semelhante, use **\_ somente o \_ cache \_ de consulta DNS**.<br/>                                                                                                                                                                                                                                      |
| \_consulta DNS \_ sem \_ \_ nome local             | 0x00000020 | Direciona o DNS para ignorar o nome local. **Windows servidor 2000 e Windows 2000 Professional:** Não há suporte para esse valor.<br/>                                                                                                                                                                                                                                                                                                                    |
| \_consulta DNS \_ sem \_ arquivo de hosts \_             | 0x00000040 | Impede que a consulta DNS consulte o arquivo de HOSTs. **Windows servidor 2000 e Windows 2000 Professional:** Não há suporte para esse valor.<br/>                                                                                                                                                                                                                                                                                                   |
| \_consulta DNS \_ sem \_ NetBT                   | 0x00000080 | Impede que a consulta DNS use o NetBT para resolução. **Windows servidor 2000 e Windows 2000 Professional:** Não há suporte para esse valor.<br/>                                                                                                                                                                                                                                                                                                  |
| \_ \_ somente transmissão de consulta DNS \_                  | 0x00000100 | Direciona o DNS para executar uma consulta usando apenas a rede, ignorando informações locais. **Windows servidor 2000 e Windows 2000 Professional:** Não há suporte para esse valor.<br/>                                                                                                                                                                                                                                                                      |
| \_mensagem de \_ retorno da consulta DNS \_             | 0x00000200 | Direciona o DNS para retornar a mensagem de resposta de DNS inteira. **Windows servidor 2000 e Windows 2000 Professional:** Não há suporte para esse valor.<br/>                                                                                                                                                                                                                                                                                                   |
| \_ \_ somente multicast de consulta DNS \_             | 0x00000400 | Impede que a consulta use o DNS e use apenas o LLMNR (resolução de nomes de multicast de link local). **Windows Vista e Windows Server 2008 ou posterior.:** Há suporte para esse valor.<br/>                                                                                                                                                                                                                                                                  |
| \_consulta DNS \_ sem \_ multicast               | 0x00000800 |                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| \_a consulta DNS \_ trata \_ como \_ FQDN             | 0x00001000 | Impede que a resposta DNS anexe sufixos ao nome enviado em um processo de resolução de nomes.                                                                                                                                                                                                                                                                                                                                                  |
| \_ADDRCONFIG de consulta DNS \_                  | 0x00002000 | somente Windows 7: não envie consultas [**de**](/windows/win32/api/windns/ns-windns-dns_a_data) tipo se os endereços IPv4 não estiverem disponíveis em uma interface e não enviar consultas de tipo [**AAAA**](/windows/win32/api/windns/ns-windns-dns_aaaa_data) se os endereços IPv6 não estiverem disponíveis.                                                                                                                                                                                                                                   |
| \_ \_ endereço duplo de consulta DNS \_                  | 0x00004000 | somente Windows 7: consultar [**AAAA**](/windows/win32/api/windns/ns-windns-dns_aaaa_data) e [**um**](/windows/win32/api/windns/ns-windns-dns_a_data) tipo registros e retornar resultados para cada um. Os resultados de um tipo registros são mapeados para **o** tipo **aaaa** .                                                                                                                                                                                                                                                           |
| \_espera de \_ multicast de consulta DNS \_             | 0x00020000 | Aguarda um tempo limite completo para coletar todas as respostas do link local. Se não for definido, o comportamento padrão será retornar com a primeira resposta. **Windows Vista e Windows Server 2008 ou posterior.:** Há suporte para esse valor.<br/>                                                                                                                                                                                                              |
| \_verificação de \_ multicast de consulta DNS \_           | 0x00040000 | Direciona um teste usando o nome do host do computador local para verificar a exclusividade do nome no mesmo link local. Coleta todas as respostas, mesmo que o comportamento normal do remetente de LLMNR não esteja habilitado. **Windows Vista e Windows Server 2008 ou posterior.:** Há suporte para esse valor.<br/>                                                                                                                                                                                  |
| \_consulta DNS \_ não \_ Redefinir \_ valores de TTL \_    | 0x00100000 | Se definido, e se a resposta contiver vários registros, os registros serão armazenados com o TTL correspondente ao valor mínimo de TTL entre todos os registros. Quando essa opção é definida, "não altere o TTL de registros individuais" no conjunto de registros retornado não é modificado.                                                                                                                                                                               |
| \_consulta DNS \_ desabilitar \_ \_ codificação IDN      | 0x00200000 | Desabilita o suporte à codificação de nome de domínio internacional (IDN) nas APIs [**DnsQuery**](/windows/desktop/api/Windns/nf-windns-dnsquery_a), [**DnsQueryEx**](/windows/desktop/api/Windns/nf-windns-dnsqueryex), [**DnsModifyRecordsInSet**](/windows/desktop/api/Windns/nf-windns-dnsmodifyrecordsinset_a)e [**DnsReplaceRecordSet**](/windows/desktop/api/Windns/nf-windns-dnsreplacerecordseta) . Todos os nomes de Punycode são tratados como ASCII e serão codificados em ASCII na conexão. Todos os nomes não ASCII são codificados em UTF8 na transmissão. **Windows 8 ou posterior.:** Há suporte para esse valor.<br/> |
| \_consulta DNS \_ acrescentar \_ multirótulo          | 0x00800000 |                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| \_consulta DNS \_ reservada                    | 0xf0000000 | Reservado.                                                                                                                                                                                                                                                                                                                                                                                                                                              |



 

## <a name="dns-update-options"></a>Opções de atualização de DNS



| Constante                                 | Valor      | Significado                                                                                                                                                       |
|------------------------------------------|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ \_ \_ uso padrão de segurança de atualização de DNS \_      | 0x00000000 | Usa o comportamento padrão, que é especificado no registro, para atualizações de DNS dinâmicas seguras.                                                                |
| segurança de atualização de DNS \_ \_ \_ desativada               | 0x00000010 | Não tenta atualizações dinâmicas seguras.                                                                                                                      |
| \_ \_ segurança de atualização \_ de DNS em                | 0x00000020 | Tentativas de atualização dinâmica não segura; Se for recusado, o tentará uma atualização dinâmica segura.                                                                               |
| \_ \_ somente segurança de atualização de DNS \_              | 0x00000100 | Tenta somente atualizações dinâmicas seguras.                                                                                                                         |
| \_contexto de \_ segurança do cache de atualização de DNS \_ \_    | 0x00000200 | Armazena em cache o contexto de segurança para uso em transações futuras.                                                                                                   |
| teste de atualização de DNS \_ \_ \_ usar \_ \_ conta sys local \_ | 0x00000400 | Usa credenciais da conta do computador local.                                                                                                               |
| \_nego de \_ segurança forçada de atualização \_ de DNS \_       | 0x00000800 | Não usa contexto de segurança em cache.                                                                                                                         |
| atualização de DNS \_ \_ Experimente \_ todos os \_ \_ servidores mestres   | 0x00001000 | Envia atualizações de DNS para todos os servidores DNS de vários mestres.                                                                                                            |
| atualização de DNS \_ \_ ignorar \_ nenhum \_ adaptador de atualização \_  | 0x00002000 | Não atualize os adaptadores em que as atualizações dinâmicas de DNS estão desabilitadas. **Windows servidor 2000 com SP2 ou posterior.:** Há suporte para esse valor.<br/>                 |
| \_ \_ servidor remoto de atualização de DNS \_              | 0x00004000 | Registre os registros CNAME em um servidor remoto além do servidor DNS local. **Windows servidor 2000 com SP2 ou posterior.:** Há suporte para esse valor.<br/> |
| atualização de DNS \_ \_ reservada                    | 0xffff0000 | Reservado para uso futuro.                                                                                                                                      |



 

## <a name="dns-response-codes"></a>Códigos de resposta DNS



| Erro                | Significado                                        |
|----------------------|------------------------------------------------|
| \_NOERROR RCODE \_ DNS  | Nenhum erro                                       |
| \_RCODE DNS \_ anterior  | Erro de formato                                   |
| \_SERVFAIL RCODE \_ DNS | Falha do servidor                                 |
| \_NXDOMAIN RCODE \_ DNS | Erro de nome                                     |
| \_NOTIMPL RCODE \_ DNS  | Não implementado                                |
| \_RCODE DNS \_ recusado  | Conexão recusada                             |
| \_YXDOMAIN RCODE \_ DNS | O nome de domínio não deve existir                   |
| \_YXRRSET RCODE \_ DNS  | O conjunto de registros de recursos (RR) não deve existir      |
| \_NXRRSET RCODE \_ DNS  | O RR set não existe                          |
| RCODE do DNS \ \_ \_ auth  | Não autoritativo para zona                     |
| DNS \_ RCODE não \_ zona  | Nome não está na zona                               |
| \_BADVERS RCODE \_ DNS  | Mecanismo de extensão inadequado para a versão do DNS (EDNS) |
| \_BADSIG RCODE \_ DNS   | Assinatura inadequada                                  |
| \_BADKEY RCODE \_ DNS   | Chave inadequada                                        |
| \_Badtime RCODE \_ DNS  | Timestamp inválido                                  |



 

 

 





