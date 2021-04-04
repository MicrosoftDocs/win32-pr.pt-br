---
title: Gerenciando registros de recursos de DNS
description: Um registro de recurso, conhecido como RR, é a unidade de entrada de informações nos arquivos de zona DNS; RRs são os blocos de construção básicos de nome de host e informações de IP e são usados para resolver todas as consultas DNS.
ms.assetid: ddad5f14-5a2d-4966-87b7-b354666f9e24
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99edffa52b5137858468fd64122d2af826a896ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822820"
---
# <a name="managing-dns-resource-records"></a>Gerenciando registros de recursos de DNS

Um registro de recurso, conhecido como RR, é a unidade de entrada de informações nos arquivos de zona DNS; RRs são os blocos de construção básicos de nome de host e informações de IP e são usados para resolver todas as consultas DNS. Os registros de recursos são fornecidos em uma variedade bastante ampla de tipos para fornecer serviços estendidos de resolução de nomes.

Tipos diferentes de RRs têm formatos diferentes, pois contêm dados diferentes. Muitos RRs compartilham um formato comum. Cada servidor DNS contém RRs para a parte do espaço de nome para o qual ele é autoritativo.

O provedor WMI de DNS atualmente dá suporte aos seguintes tipos de RR. Clique no nome do registro de recurso para ir para sua página de referência.



| Registro de recurso (no provedor)                             | Descrição                                                  |
|-----------------------------------------------------------|--------------------------------------------------------------|
| [**MicrosoftDNS \_ AType**](microsoftdns-atype.md)         | Nome para o registro de mapeamento de endereço                               |
| [**MicrosoftDNS \_ aaaatype**](microsoftdns-aaaatype.md)   | Registro de endereço do host para IPv6                                  |
| [**MicrosoftDNS \_ AFSDBType**](microsoftdns-afsdbtype.md) | O registro do servidor de banco de dados Andrew File System                    |
| [**MicrosoftDNS \_ ATMAType**](microsoftdns-atmatype.md)   | Registro de endereço para nome do ATM                                   |
| [**\_Cnametype MicrosoftDNS**](microsoftdns-cnametype.md) | Registro de [*nome canônico*](c-gly.md) |
| [**MicrosoftDNS \_ HINFOType**](microsoftdns-hinfotype.md) | Registro de informações do host                                      |
| [**\_Isdntype MicrosoftDNS**](microsoftdns-isdntype.md)   | Registro de rede digital de serviços integrados                   |
| [**KeyType MicrosoftDNS \_**](microsoftdns-keytype.md)     | Registro de chave. Consulte RFC 2535                                     |
| [**MicrosoftDNS \_ MBType**](microsoftdns-mbtype.md)       | Registro da caixa de correio                                               |
| [**MicrosoftDNS \_ MDType**](microsoftdns-mdtype.md)       | Agente de email para o registro de domínio                             |
| [**MicrosoftDNS \_ MFType**](microsoftdns-mftype.md)       | Agente de encaminhamento de email para o registro de domínio                  |
| [**MicrosoftDNS \_ MGType**](microsoftdns-mgtype.md)       | Registro do grupo de emails                                            |
| [**MicrosoftDNS \_ MINFOType**](microsoftdns-minfotype.md) | Registro de informações de email                                      |
| [**MicrosoftDNS \_ MRType**](microsoftdns-mrtype.md)       | Registro de renomear caixa de correio                                        |
| [**MicrosoftDNS \_ MXType**](microsoftdns-mxtype.md)       | Registro do servidor de mensagens                                        |
| [**MicrosoftDNS \_ NSType**](microsoftdns-nstype.md)       | Registro de servidor de nomes                                           |
| [**MicrosoftDNS \_ NXTType**](microsoftdns-nxttype.md)     | Próximo registro                                                  |
| [**MicrosoftDNS \_ PTRType**](microsoftdns-ptrtype.md)     | Endereço para registro de mapeamento de nome                               |
| [**MicrosoftDNS \_ RPType**](microsoftdns-rptype.md)       | Registro de pessoa responsável                                    |
| [**MicrosoftDNS \_ RTType**](microsoftdns-rttype.md)       | Rotear por registro                                         |
| [**MicrosoftDNS \_ SIGType**](microsoftdns-sigtype.md)     | Registro de assinatura                                             |
| [**MicrosoftDNS \_ SOAType**](microsoftdns-soatype.md)     | Início de autoridade                                           |
| [**MicrosoftDNS \_ SRVType**](microsoftdns-srvtype.md)     | Registro de serviço                                               |
| [**MicrosoftDNS \_ TXTType**](microsoftdns-txttype.md)     | Registro de texto                                                  |
| [**MicrosoftDNS \_ winstype**](microsoftdns-winstype.md)   | Registro do servidor WINS                                           |
| [**MicrosoftDNS \_ WINSRType**](microsoftdns-winsrtype.md) | Registro de pesquisa inversa do WINS                                   |
| [**MicrosoftDNS \_ WKSType**](microsoftdns-wkstype.md)     | Bem-registro de serviços conhecidos                                   |
| [**MicrosoftDNS \_ X25Type**](microsoftdns-x25type.md)     | Registro de mapeamento de endereço para nome X. 121                         |



 

## <a name="administration-steps"></a>Etapas de administração

O provedor WMI de DNS permite a administração de RRs do próprio servidor ou de hosts remotos. As etapas gerais necessárias para administrar RRs usando o provedor WMI de DNS são:

-   Conectando-se ao provedor WMI de DNS
-   Obtendo uma instância de registro de recurso
-   Listando ou modificando uma propriedade de registro de recurso ou usando um método

As tarefas a seguir estão vinculadas a seus exemplos de script associados.

-   [Listando tipos de recursos](dns-wmi-provider-samples-managing-dns-resource-records.md)
-   [Adicionando um registro de recurso](dns-wmi-provider-samples-managing-dns-resource-records.md)
-   [Excluindo um registro de recurso](dns-wmi-provider-samples-managing-dns-resource-records.md)
-   [Modificando um registro de recurso](dns-wmi-provider-samples-managing-dns-resource-records.md)

 

 




