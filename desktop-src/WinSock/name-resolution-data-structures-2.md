---
description: estruturas de dados de resolução de nomes em soquetes de Windows (Winsock).
ms.assetid: 87c54141-41e2-4eaa-ae3b-84598e8281d9
title: Estruturas de dados de resolução de nomes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93e6f3b889d295241bb0cdb9c0182babf0c5b8115e7eff7e86c27b65c992c452
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119794786"
---
# <a name="name-resolution-data-structures"></a>Estruturas de dados de resolução de nomes

Há várias estruturas de dados importantes que são usadas extensivamente em todas as funções de resolução de nomes.

## <a name="query-related-data-structures"></a>Estruturas de dados de Query-Related

A estrutura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) é usada para formar consultas para [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)e é usada para fornecer resultados de consulta para [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta). É uma estrutura complexa, pois contém ponteiros para várias outras estruturas, algumas das quais a referência ainda tem outras estruturas. A relação entre a estrutura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) e as estruturas que ela faz referência é ilustrada a seguir.

![relação entre WSAQUERYSET e suas estruturas associadas](images/ovrvw3-2.png)

Na estrutura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) , a maioria dos membros é auto-explicativa, mas alguns merecem uma explicação adicional. O membro **dwSize** sempre deve ser preenchido com sizeof (**WSAQUERYSET**), pois ele é usado por provedores de namespace para detectar e se adaptar a versões diferentes da estrutura **WSAQUERYSET** que podem aparecer ao longo do tempo.

O membro **dwOutputFlags** é usado por um provedor de namespace para fornecer informações adicionais sobre os resultados da consulta. Para obter detalhes, consulte a função [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) .

A estrutura [**WSAECOMPARATOR**](/windows/desktop/api/Winsock2/ne-winsock2-wsaecomparator) referenciada pelo membro **lpversion** é usada para a restrição de consulta e os resultados. Para consultas, o membro **DW** indica a versão desejada do serviço. O membro **ecHow** é um tipo enumerado que especifica como a comparação pode ser feita. As opções são COMP \_ Equals, que requer que uma correspondência exata na versão ocorra, ou comp less, que \_ especifica que o número de versão do serviço não é menor que o valor do membro **DW** .

A interpretação de **dwNameSpace** e **lpNSProviderId** depende de como a estrutura está sendo usada e é descrita mais detalhadamente nas descrições de função individuais que utilizam essa estrutura.

O membro **lpszContext** se aplica a namespaces hierárquicos e especifica o ponto de partida de uma consulta ou o local dentro da hierarquia em que o serviço reside. As regras gerais são:

-   Um valor **nulo**, em branco (""), inicia a pesquisa no contexto padrão.
-   Um valor de " \\ " inicia a pesquisa na parte superior do namespace.
-   Qualquer outro valor inicia a pesquisa no ponto designado.

Os provedores que não dão suporte à contenção poderão retornar um erro se algo diferente de "" ou " \\ " for especificado. Provedores que dão suporte a contenção limitada, como grupos, devem aceitar "", " \\ " ou um ponto designado. Contextos são específicos do namespace. Se o membro **dwNameSpace** for NS \_ All, somente "" ou " \\ " deverá ser passado como o contexto, pois eles são reconhecidos por todos os namespaces.

O membro **lpszQueryString** é usado para fornecer informações de consulta adicionais específicas de namespace, como uma cadeia de caracteres que descreve um serviço conhecido e um nome de protocolo de transporte, como em "FTP/TCP".

A estrutura [**AFPROTOCOLS**](/windows/desktop/api/Winsock2/ns-winsock2-afprotocols) referenciada pelo membro **lpafpProtocols** é usada apenas para fins de consulta e fornece uma lista de protocolos para restringir a consulta. Esses protocolos são representados como pares (família de endereços, protocolo), pois os valores de protocolo só têm significado no contexto de uma família de endereços.

A matriz da estrutura [**de \_ informações do CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) referenciada pelo membro **lpcsaBuffer** contém todas as informações necessárias para que um serviço seja usado no estabelecimento de uma escuta ou para que um cliente use o para estabelecer uma conexão com o serviço. Os membros **localaddr** e **RemoteAddr** contêm diretamente uma estrutura [**de \_ endereço de soquete**](/windows/desktop/api/Ws2def/ns-ws2def-socket_address) .

Um serviço criaria um soquete chamando a função [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) ou [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) usando a tupla de *localaddr. lpSockAddr->SA \_ Family*, *iSocketType* e *iProtocol* como parâmetros. Um serviço associaria o soquete a um endereço local chamando a função [**BIND**](/windows/desktop/api/winsock/nf-winsock-bind) usando *localaddr. lpSockAddr* e *localaddr. lpSockaddrLength* como parâmetros.

Um cliente cria seu soquete chamando o [**soquete**](/windows/desktop/api/Winsock2/nf-winsock2-socket) ou a função [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) usando a tupla de *localaddr. lpSockAddr->a \_ família SA*, *iSocketType* e *iProtocol* como parâmetros. Um cliente usa a combinação de *RemoteAddr. lpSockAddr* e *RemoteAddr. lpSockaddrLength* como parâmetros ao fazer uma conexão remota usando a função [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect), [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex)ou [**WSAConnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect) .

## <a name="service-class-data-structures"></a>Estruturas de dados de classe de serviço

Quando uma nova classe de serviço é instalada, uma estrutura [**WSASERVICECLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsaserviceclassinfow) deve ser preparada e fornecida. Essa estrutura também consiste em subestruturas que contêm uma série de membros que se aplicam a namespaces específicos. Uma estrutura de dados de informações de classe é a seguinte:

![arquitetura de estruturas de dados de classe de serviço](images/ovrvw3-3.png)

Para cada classe de serviço, há uma única estrutura [**WSASERVICECLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsaserviceclassinfow) . Na estrutura [**WSASERVICECLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsaserviceclassinfow) , o identificador exclusivo da classe de serviço está contido no membro **lpServiceClassId** e uma cadeia de caracteres de exibição associada é referenciada pelo membro **lpServiceClassName** . Essa é a cadeia de caracteres retornada pela função [**WSAGetServiceClassNameByClassId**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida) .

O membro **lpClassInfos** na estrutura [**WSASERVICECLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsaserviceclassinfow) faz referência a uma matriz de estruturas **WSANSCLASSINFO** , cada uma delas fornece um membro nomeado e digitado que se aplica a um namespace especificado. Exemplos de valores para o membro **lpszName** incluem: "SAPID", "TCPPort", "UDPport", etc. Essas cadeias de caracteres são geralmente específicas do namespace identificado no membro **dwNameSpace** . Os valores típicos para o membro **dwValueType** podem ser reg \_ DWORD, Reg \_ sz, etc. O membro **dwValueSize** indica o comprimento do item de dados apontado por **lpValue**.

Toda a coleção de dados representada em uma estrutura **WSASERVICECLASSINFO** é fornecida para cada provedor de namespace quando a função [**WSAInstallServiceClass**](/windows/desktop/api/Winsock2/nf-winsock2-wsainstallserviceclassa) é invocada. Em seguida, cada provedor de namespace individual percorre a lista de estruturas **WSANSCLASSINFO** e retém as informações aplicáveis a ela.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**AFPROTOCOLS**](/windows/desktop/api/Winsock2/ns-winsock2-afprotocols)
</dt> <dt>

[**informações de CSADDR \_**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info)
</dt> <dt>

[Modelo de resolução de nomes](name-resolution-model-2.md)
</dt> <dt>

[Resolução de nomes independente de protocolo](protocol-independent-name-resolution-2.md)
</dt> <dt>

[Registro e resolução de nome](registration-and-name-resolution-2.md)
</dt> <dt>

[**Endereço do soquete \_**](/windows/desktop/api/Ws2def/ns-ws2def-socket_address)
</dt> <dt>

[Resumo das funções de resolução de nomes](summary-of-name-resolution-functions-2.md)
</dt> <dt>

[**WSAECOMPARATOR**](/windows/desktop/api/Winsock2/ne-winsock2-wsaecomparator)
</dt> <dt>

[**WSAGetServiceClassNameByClassId**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida)
</dt> <dt>

[**WSAInstallServiceClass**](/windows/desktop/api/Winsock2/nf-winsock2-wsainstallserviceclassa)
</dt> <dt>

[**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)
</dt> <dt>

[**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[**WSASERVICECLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsaserviceclassinfow)
</dt> </dl>

 

 
