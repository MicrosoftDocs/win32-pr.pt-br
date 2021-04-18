---
description: Para obter a notificação de redes lógicas invalidadas, use a função WSANSPIoctl para registrar-se para eventos de alteração de local de rede.
ms.assetid: 531b6269-5f35-44c1-ad0f-c5f103029893
title: Consultando NLA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ac7a4f57e14bb967b04d3a9fd6fe66717da3878
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782543"
---
# <a name="querying-nla"></a>Consultando NLA

Para obter a notificação de redes lógicas invalidadas, use a função [**WSANSPIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsanspioctl) para registrar-se para eventos de alteração de local de rede. Dois métodos podem ser usados para determinar se um local de rede válido anteriormente se tornou inválido: métodos de sondagem ou notificação usando mensagens sobrepostas de e/s ou Windows.

As consultas são formadas usando as funções [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) e [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) para enumerar todas as redes lógicas disponíveis. O uso de cada uma dessas funções é explicado individualmente durante o restante desta seção, começando pela função **WSALookupServiceBegin** .

> [!Note]  
> A NLA requer o arquivo de cabeçalho mswsock. h, que por padrão não está incluído no arquivo Winsock2. h.

 

## <a name="step-1-initiate-the-query"></a>Etapa 1: iniciar a consulta

Para referência rápida, a função [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) tem a seguinte sintaxe:

``` syntax
INT WSALookupServiceBegin(
  LPWSAQUERYSET lpqsRestrictions,
  DWORD dwControlFlags,
  LPHANDLE lphLookup
);
```

O NLA dá suporte aos seguintes sinalizadores de pesquisa *dwControlFlags* :

<dl> LUP \_ nome de retorno \_  
\_Comentário de retorno do Lup \_  
\_blob de retorno de Lup \_  
LUP \_ retornar \_ tudo  
LUP \_ profundo  
</dl>

Esses sinalizadores restringem os conjuntos de resultados retornados nas chamadas subsequentes para o [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta), a função para redes que contêm campos do tipo especificado. Por exemplo, a especificação de \_ blob de retorno Lup \_ no parâmetro *dwControlFlags* da chamada de função [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) restringe os conjuntos de resultados das chamadas subsequentes para **WSALookupServiceNext**, para redes que contêm informações de BLOB. Usar o sinalizador LUP de \_ retorno \_ All é equivalente a especificar \_ o \_ nome de retorno de Lup, o \_ Comentário de retorno de Lup \_ e o blob de retorno de Lup \_ \_ , mas não os Lup de \_ profundidade.

Para obter uma explicação desses sinalizadores de pesquisa, consulte a página de referência da função [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) .

O identificador de pesquisa retornado pela NLA no parâmetro *lphLookup* é privado para NLA e não deve ser modificado. Como o identificador retornado é privado para NLA, funções como [**WSAGetOverlappedResult**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetoverlappedresult) não estão disponíveis.

A NLA retorna zero após a conclusão bem-sucedida, conforme definido na página de referência da função [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) . Caso contrário, o NLA dá suporte aos seguintes códigos de erro.

| Erro                    | Significado                                                                                                                                                     |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WSANOTINITIALISED        | Uma chamada bem-sucedida para a função [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) para inicializar o NLA não foi executada.                                                   |
| WSAEINVAL                | Um ou mais parâmetros eram inválidos ou parâmetros especificados na chamada de função se aplicam a protocolos diferentes de IP.                                         |
| WSASERVICE \_ não \_ encontrado   | O parâmetro *lpServiceClassId* da estrutura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) passado no parâmetro *lpqsRestrictions* contém um GUID inválido. |
| dados do WSANO \_              | O \_ sinalizador de contêineres Lup foi especificado no parâmetro *dwControlFlags* .                                                                                       |
| WSAEFAULT                | Ocorreu uma violação de acesso ao tentar acessar os parâmetros fornecidos pelo usuário.                                                                            |
| WSASYSNOTREADY           | O serviço NLA não está disponível para processar a solicitação.                                                                                                      |
| o WSA \_ não tem \_ \_ memória suficiente | O NLA ou o serviço NLA não pôde alocar memória suficiente para processar essa solicitação.                                                                        |



 

## <a name="step-2-perform-the-query"></a>Etapa 2: executar a consulta

A próxima etapa na consulta de NLA requer o uso da função [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) . Para referência rápida, a função **WSALookupServiceNext** tem a seguinte sintaxe:

``` syntax
INT WSALookupServiceNext(
  HANDLE hLookup,
  DWORD dwControlFlags,
  LPDWORD lpdwBufferLength,
  LPWSAQUERYSET lpqsResults
);
```

O parâmetro *lLookup* é o identificador de pesquisa retornado da chamada anterior para a função [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) .

O parâmetro *dwControlFlags* dá suporte aos seguintes sinalizadores:

<dl> LUP \_ nome de retorno \_  
\_Comentário de retorno do Lup \_  
\_blob de retorno de Lup \_  
LUP \_ retornar \_ tudo  
LUP \_ FLUSHPREVIOUS  
</dl>

Esses sinalizadores são independentes dos sinalizadores com suporte na chamada de função [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) . Observe que todas as restrições especificadas na chamada anterior à função **WSALookupServiceBegin** restringem a pesquisa; a adição de sinalizadores com a função [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) em uma tentativa de ampliar a consulta além das restrições especificadas na chamada **WSALookupServiceBegin** é silenciosamente ignorada. No entanto, é permitido especificar um conjunto mais restritivo de sinalizadores do que o especificado na chamada **WSALookupServiceBegin** .

Se a rede detalhada no *lpqsResults* for uma rede ativa, uma série de estruturas de **\_ blob NLA** será anexada conforme especificado no membro **LpBlob** da estrutura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) retornada em *lpqsResults*. Essas estruturas de **\_ blob NLA** podem ser encadeadas e podem ser enumeradas atravessando a lista enquanto o NLA \_ BLOB. Header. nextOffset é diferente de zero. Para obter os resultados de todas as informações de local de rede, continue chamando o [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta), a função até que o WSA \_ E \_ nenhum \_ erro seja retornado, conforme explicado na página de referência **WSALookupServiceNext**.

A função [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) também é usada em conjunto com a função [**WSANSPIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsanspioctl) para receber notificações de alterações de rede. Consulte [notificação de NLA](notification-from-nla-2.md) para obter mais informações.

A NLA retorna zero após a conclusão bem-sucedida. Os clientes de NLA devem continuar chamando o [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta), a função até que o WSA \_ E \_ não \_ mais seja retornado, indicando que todas as informações sobre redes disponíveis foram retornadas.

Caso contrário, chamar o [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta), a função para NLA dá suporte aos seguintes códigos de erro.

| Erro                    | Significado                                                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WSANOTINITIALISED        | Uma chamada bem-sucedida para a função [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) que iniciou a NLA não foi executada.                                                                                                                                                                                                                                                                                                |
| \_identificador inválido de WSA \_     | O identificador de pesquisa fornecido no parâmetro *HLOOKUP* não era um identificador válido de SP do NLA. Os clientes devem primeiro chamar a função [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) e receber um identificador válido do NLA SP para obter os resultados da consulta.                                                                                                                                                               |
| WSAESYSNOTREADY          | O serviço NLA não está disponível para processar essa solicitação.                                                                                                                                                                                                                                                                                                                                                     |
| WSAEFAULT                | O tamanho do buffer especificado no parâmetro *lpdwBufferLength* não era suficiente para manter os resultados apontados por *lpqsResults*. O buffer necessário é especificado em *lpdwBufferLength*; Se o cliente não puder fornecer um buffer suficientemente grande, o cliente poderá chamar a função [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) com *DWCONTROLFLAGS* definido como Lup \_ FLUSHPREVIOUS para ignorar a entrada. |
| o WSA \_ não tem \_ \_ memória suficiente | A NLA não pode obter informações de rede do serviço de sistema NLA devido à memória insuficiente no processo de chamada.                                                                                                                                                                                                                                                                                  |
| CABEÇALHO \_ E \_ não \_ mais         | Não há redes adicionais a serem enumeradas para a consulta.                                                                                                                                                                                                                                                                                                                                                |



 

## <a name="step-3-terminate-the-query"></a>Etapa 3: encerrar a consulta

Quando todas as consultas para NLA são concluídas e um aplicativo não requer mais o uso de NLA, uma chamada para a função [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) deve ser feita. Não chame **WSALookupServiceEnd** se o aplicativo receber a notificação de alteração com base na consulta enviada. Consulte [notificação de NLA](notification-from-nla-2.md) para obter mais informações sobre como receber notificações. Assim como a maioria dos provedores do Windows Sockets Service, a NLA mantém uma contagem de referência para seus clientes. Chamar a função **WSALookupServiceEnd** quando as consultas para NLA são concluídas permite que os recursos do sistema não sejam mais exigidos pelo NLA para serem liberados.

O NLA dá suporte aos seguintes códigos de erro para chamadas de função [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) .

| Erro                | Significado                                                                                                   |
|----------------------|-----------------------------------------------------------------------------------------------------------|
| WSANOTINITIALISED    | Uma chamada bem-sucedida para a função [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) para inicializar o NLA não foi executada. |
| \_identificador inválido de WSA \_ | O identificador fornecido no parâmetro *HLOOKUP* não era um identificador válido de SP do NLA.                             |



 

 

 



