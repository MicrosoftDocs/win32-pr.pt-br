---
description: O Microsoft Windows Http Services (WinHTTP) usa alças para controlar as configurações e as informações necessárias ao usar o protocolo HTTP.
ms.assetid: 0bd82860-1347-40c8-ae77-c4d865c109be
title: Alças HINTERNET no WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a76f925d11646ed2fe5b5d3732fe8972d979cdc6383a4d47e955c0e60a1390e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118563262"
---
# <a name="hinternet-handles-in-winhttp"></a>Alças HINTERNET no WinHTTP

O Microsoft Windows Http Services (WinHTTP) usa alças para controlar as configurações e as informações necessárias ao usar o protocolo HTTP. Cada alça mantém informações pertinentes a uma sessão HTTP, uma conexão com um servidor HTTP ou um recurso específico. Este tópico descreve os vários tipos de alças, as convenções de nomen por esses alças e sua estrutura hierárquica.

-   [Sobre os alças HINTERNET](#about-hinternet-handles)
-   [Alças de nomeação](#naming-handles)
-   [Hierarquia de alça](#handle-hierarchy)
-   [Explicação da hierarquia de alça](#explanation-of-the-handle-hierarchy)

## <a name="about-hinternet-handles"></a>Sobre os alças HINTERNET

Os alças criados e usados pelo WinHTTP são chamados de alças **HINTERNET.** As funções WinHTTP retornam os alças **HINTERNET** que não são intercambiáveis com outros alças, portanto, eles não podem ser usados com funções como [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) ou [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle). Da mesma forma, outros alças não podem ser usados com funções WinHTTP. Por exemplo, um handle retornado por [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) não pode ser passado [**para WinHttpReadData.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata) Esses **alças HINTERNET** não podem ser fechados enquanto uma chamada à API usando o handle está em andamento. Para evitar uma condição de corrida, os aplicativos devem proteger o handle e impedir que ele seja fechado enquanto a chamada à API está em andamento.

As funções do WinInet (Microsoft Win32 Internet) também usam **os alças HINTERNET.** No entanto, os alças usados em funções WinInet não podem ser intercambiados com os alças usados em funções WinHTTP. Para obter mais informações sobre o WinInet, consulte [Sobre o WinINet.](/windows/desktop/WinInet/about-wininet)

A [**função WinHttpCloseHandle**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpclosehandle) fecha os alças **HINTERNET** do WinHTTP.

## <a name="naming-handles"></a>Alças de nomeação

Em toda a documentação do WinHTTP, as descrições de funções na API (interface de programação de aplicativo) e o código de exemplo mostram a criação e o uso de vários tipos de alças **HINTERNET.** Para acompanhar os diferentes tipos de alças disponíveis, a nomeação desses alças é consistente. A tabela a seguir mostra os identificadores usados por convenção na documentação.



| Tipo de identificador       | Função que cria o handle                                                                                                          | Identificador |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------|------------|
| Alça genérica    | [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen), [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect)ou [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) | Hinternet  |
| Alça de sessão    | [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen)                                                                                                | hSession   |
| Alça de conexão | [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect)                                                                                          | hConnect   |
| Alça de solicitação    | [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)                                                                                  | hRequest   |



 

## <a name="handle-hierarchy"></a>Hierarquia de alça

Os **alças HINTERNET** são mantidos em uma hierarquia. O handle retornado por [**WinHttpOpen é o**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) handle **HINTERNET da** sessão. Chamar **WinHttpOpen** inicializa as funções WinHTTP e inicia um contexto de sessão que mantém as informações e as configurações do usuário ao longo da vida útil do alçamento de sessão. [**WinHttpConnect especifica**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect) um servidor HTTP ou HTTPS de destino e cria um handle **HINTERNET de** conexão. Por padrão, o alça de conexão herda as configurações para o alça de sessão. Cada recurso especificado com uma chamada para [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) recebe um handle **HINTERNET de** solicitação.

O diagrama a seguir ilustra a hierarquia de **alças HINTERNET.** Cada caixa no diagrama representa uma função WinHTTP que retorna um **handle HINTERNET.**

![funções que criam alças](images/art-winhttp2.png)

Depois de fechar um handle, o aplicativo deve estar preparado para receber notificações de retorno de chamada no alçamento até que o valor final DE HANDLE CLOSED DE STATUS DE RETORNO DE CHAMADA WINHTTP seja retornado para indicar que o alça está completamente fechado. **\_ \_ \_ \_**

Um alça de sessão é o pai de qualquer alça de conexão que ele usou para criar; Da mesma forma, o alça de conexão e seu alça de sessão pai são os pais de qualquer alça de solicitação que o alça de conexão é usado para criar.

Quando um handle pai é fechado, todos os filhos que ele tem são invalidados indiretamente, mesmo que não sejam fechados por conta própria, e as solicitações subsequentes que o usam falham com o erro **ERROR \_ INVALID \_ HANDLE**. Solicitações assíncronas pendentes não podem ser contadas para serem concluídas corretamente.

O diagrama a seguir mostra as funções que usam o handle **HINTERNET** criado por [**WinHttpOpenRequest.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) As caixas sombreadas representam funções WinHTTP que criam alças e as caixas simples mostram as funções que usam esses alças **HINTERNET.** O diagrama também é organizado para mostrar a ordem em que as funções WinHTTP normalmente são chamadas.

![funções que criam alças](images/art-winhttp2.png)

## <a name="explanation-of-the-handle-hierarchy"></a>Explicação da hierarquia de alça

Primeiro, um alça de sessão é criado com [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen). [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect) requer o alça de sessão como seu primeiro parâmetro e retorna um alça de conexão para um servidor especificado. Um alça de solicitação é criado [**por WinHttpOpenRequest,**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)que usa o alça de conexão criado por [**WinHttpConnect.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect) Se o aplicativo optar por adicionar outros headers à solicitação ou se for necessário para o aplicativo definir credenciais para autenticação, [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) e [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) poderão ser chamados usando esse identificador de solicitação. A solicitação é enviada por [**WinHttpSendRequest,**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)que usa o handle de solicitação. Depois de enviar a solicitação, dados adicionais podem ser enviados para o servidor usando [**WinHttpWriteData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata)ou o aplicativo pode pular diretamente para [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) para especificar que nenhuma outra informação é enviada ao servidor. Neste ponto, dependendo da finalidade do aplicativo, o handle de solicitação pode ser usado para chamar [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders), [**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes)ou recuperar um recurso com [**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable) e [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata).

 

 
