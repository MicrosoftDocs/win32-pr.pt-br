---
description: A API de DRT (tabela de roteamento distribuído) utiliza as funções a seguir.
ms.assetid: 1ceff217-d410-47fa-99a2-8588f001859e
title: Funções de tabela de roteamento distribuído
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cd48c3a60f458285ce5f607f9ab6bcf7a557cd9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770364"
---
# <a name="distributed-routing-table-functions"></a>Funções de tabela de roteamento distribuído

A API de DRT (tabela de roteamento distribuído) utiliza as funções a seguir.

## <a name="lifetime-management-functions"></a>Funções de gerenciamento de tempo de vida



| Função                                           | Descrição                                                                                                    |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**DrtOpen**](/windows/desktop/api/drt/nf-drt-drtopen)                         | Cria uma instância DRT local usando critérios especificados pela estrutura [**de \_ configurações DRT**](/windows/desktop/api/drt/ns-drt-drt_settings) .  |
| [**DrtClose**](/windows/desktop/api/drt/nf-drt-drtclose)                       | Fecha e remove a instância local do DRT.                                                              |
| [**DrtGetEventData**](/windows/desktop/api/drt/nf-drt-drtgeteventdata)         | Recupera dados de evento associados a um evento sinalizado.                                                         |
| [**DrtGetEventDataSize**](/windows/desktop/api/drt/nf-drt-drtgeteventdatasize) | Retorna o tamanho da estrutura [**de \_ \_ dados de evento DRT**](/windows/desktop/api/drt/ns-drt-drt_event_data) associada a um evento sinalizado. |



 

## <a name="module-management-functions"></a>Funções de gerenciamento de módulo



| Função                                                                           | Descrição                                                                                                                           |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**DrtCreatePnrpBootstrapResolver**](/windows/desktop/api/drt/nf-drt-drtcreatepnrpbootstrapresolver)           | Cria um resolvedor de inicialização com base no protocolo PNRP.                                                                              |
| [**DrtDeletePnrpBootstrapResolver**](/windows/desktop/api/drt/nf-drt-drtdeletepnrpbootstrapresolver)           | Exclui um resolvedor de inicialização com base no protocolo PNRP.                                                                              |
| [**DrtCreateDnsBootstrapResolver**](/windows/desktop/api/drt/nf-drt-drtcreatednsbootstrapresolver)             | Cria um provedor de inicialização que entrará em contato com um host bem conhecido pelo nome.                                                             |
| [**DrtDeleteDnsBootstrapResolver**](/windows/desktop/api/drt/nf-drt-drtdeletednsbootstrapresolver)             | Exclui um provedor de inicialização que entrará em contato com um host bem conhecido pelo nome.                                                             |
| [**DrtCreateIpv6UdpTransport**](/windows/desktop/api/drt/nf-drt-drtcreateipv6udptransport)                     | Cria um transporte com base no protocolo UDP IPv6.                                                                                   |
| [**DrtDeleteIpv6UdpTransport**](/windows/desktop/api/drt/nf-drt-drtdeleteipv6udptransport)                     | Exclui um transporte com base no protocolo UDP IPv6.                                                                                   |
| [**DrtCreateDerivedKeySecurityProvider**](/windows/desktop/api/drt/nf-drt-drtcreatederivedkeysecurityprovider) | Cria um provedor de segurança de chave derivada para o DRT.                                                                                  |
| [**DrtCreateDerivedKey**](/windows/desktop/api/drt/nf-drt-drtcreatederivedkey)                                 | Cria uma chave que pode ser utilizada por [**DrtRegisterKey**](/windows/desktop/api/drt/nf-drt-drtregisterkey) quando a DRT estiver usando um provedor de segurança de chave derivada. |
| [**DrtDeleteDerivedKeySecurityProvider**](/windows/desktop/api/drt/nf-drt-drtdeletederivedkeysecurityprovider) | Exclui um provedor de segurança de chave derivada para o DRT.                                                                                  |
| [**DrtCreateNullSecurityProvider**](/windows/desktop/api/drt/nf-drt-drtcreatenullsecurityprovider)             | Cria um provedor de segurança nulo. Esse provedor de segurança não exige que os nós autentiquem chaves.                                 |
| [**DrtDeleteNullSecurityProvider**](/windows/desktop/api/drt/nf-drt-drtdeletenullsecurityprovider)             | Exclui um provedor de segurança nulo.                                                                                                     |



 

## <a name="registration-functions"></a>Funções de registro



| Função                                     | Descrição                                                    |
|----------------------------------------------|----------------------------------------------------------------|
| [**DrtRegisterKey**](/windows/desktop/api/drt/nf-drt-drtregisterkey)     | Registra uma chave no DRT.                                    |
| [**DrtUpdateKey**](/windows/desktop/api/drt/nf-drt-drtupdatekey)         | Atualiza os dados de aplicativo associados a uma chave registrada. |
| [**DrtUnregisterKey**](/windows/desktop/api/drt/nf-drt-drtunregisterkey) | Cancela o registro de uma chave do DRT.                                |



 

## <a name="search-functions"></a>Funções de pesquisa



| Função                                                 | Descrição                                                                                                                                                                                                             |
|----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DrtStartSearch**](/windows/desktop/api/drt/nf-drt-drtstartsearch)                 | Pesquisa a DRT em busca de uma chave usando critérios especificados na estrutura de [**\_ \_ informações de pesquisa DRT**](/windows/desktop/api/drt/ns-drt-drt_search_info) .                                                                                                      |
| [**DrtContinueSearch**](/windows/desktop/api/drt/nf-drt-drtcontinuesearch)           | Continua um \_ caminho de \_ retorno de pesquisa DRT \_ pesquisando uma chave no DRT. Essa função é usada somente quando o sinalizador **fIterative** é definido como **true** na estrutura de [**\_ \_ informações de pesquisa DRT**](/windows/desktop/api/drt/ns-drt-drt_search_info) associada. |
| [**DrtGetSearchResult**](/windows/desktop/api/drt/nf-drt-drtgetsearchresult)         | Recupera os resultados da pesquisa.                                                                                                                                                                                         |
| [**DrtGetSearchResultSize**](/windows/desktop/api/drt/nf-drt-drtgetsearchresultsize) | Retorna o tamanho do próximo resultado de pesquisa disponível.                                                                                                                                                                   |
| [**DrtGetSearchPath**](/windows/desktop/api/drt/nf-drt-drtgetsearchpath)             | Retorna uma lista de nós contatados durante a operação de pesquisa.                                                                                                                                                          |
| [**DrtGetSearchPathSize**](/windows/desktop/api/drt/nf-drt-drtgetsearchpathsize)     | Retorna o tamanho do caminho de pesquisa, que representa o número de nós utilizados na operação de pesquisa.                                                                                                             |
| [**DrtEndSearch**](/windows/desktop/api/drt/nf-drt-drtendsearch)                     | Cancela uma pesquisa de uma chave em uma DRT e, como resultado, o retorno dos resultados por meio do [**\_ \_ resultado da pesquisa DRT**](/windows/desktop/api/drt/ns-drt-drt_search_result) é interrompido. Essa API pode ser chamada a qualquer momento depois que uma pesquisa é emitida.              |



 

## <a name="instance-name-functions"></a>Funções de nome de instância



| Função                                                 | Descrição                                                      |
|----------------------------------------------------------|------------------------------------------------------------------|
| [**DrtGetInstanceName**](/windows/desktop/api/drt/nf-drt-drtgetinstancename)         | Obtém o nome associado a uma instância de DRT.                    |
| [**DrtGetInstanceNameSize**](/windows/desktop/api/drt/nf-drt-drtgetinstancenamesize) | Retorna o tamanho do nome da instância da tabela de roteamento distribuído. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Enumerações de tabela de roteamento distribuído](distributed-routing-table-enumerations.md)
</dt> <dt>

[Estruturas de tabela de roteamento distribuído](distributed-routing-table-structures.md)
</dt> <dt>

[Referência de API de Tabela de roteamento distribuído](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 



