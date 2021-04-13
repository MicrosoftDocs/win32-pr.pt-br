---
description: O Microsoft Windows HTTP Services (WinHTTP) usa identificadores para controlar as configurações e as informações necessárias ao usar o protocolo HTTP.
ms.assetid: 0bd82860-1347-40c8-ae77-c4d865c109be
title: HINTERNET identificadores no WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf374675ad6f2114dd48e0a3ff1db50cd0dd7f9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104568407"
---
# <a name="hinternet-handles-in-winhttp"></a>HINTERNET identificadores no WinHTTP

O Microsoft Windows HTTP Services (WinHTTP) usa identificadores para controlar as configurações e as informações necessárias ao usar o protocolo HTTP. Cada identificador mantém informações pertinentes a uma sessão HTTP, uma conexão com um servidor HTTP ou um recurso específico. Este tópico descreve os vários tipos de identificadores, as convenções de nomenclatura para esses identificadores e sua estrutura hierárquica.

-   [Sobre identificadores de HINTERNET](#about-hinternet-handles)
-   [Identificadores de nomenclatura](#naming-handles)
-   [Hierarquia de identificadores](#handle-hierarchy)
-   [Explicação da hierarquia de identificadores](#explanation-of-the-handle-hierarchy)

## <a name="about-hinternet-handles"></a>Sobre identificadores de HINTERNET

Os identificadores criados e usados pelo WinHTTP são chamados de identificadores **HINTERNET** . As funções WinHTTP retornam identificadores **HINTERNET** que não são intercambiáveis com outros identificadores, portanto, não podem ser usadas com funções como [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) ou [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle). Da mesma forma, outros identificadores não podem ser usados com funções WinHTTP. Por exemplo, um identificador retornado por [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) não pode ser passado para [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata). Esses identificadores **HINTERNET** não podem ser fechados enquanto uma chamada à API usando o identificador está em andamento. Para evitar uma condição de corrida, os aplicativos devem proteger o identificador e impedir que ele seja fechado enquanto a chamada à API estiver em andamento.

As funções do Microsoft Win32 Internet (WinInet) também usam identificadores **HINTERNET** . No entanto, os identificadores usados nas funções do WinInet não podem ser trocados com os identificadores usados nas funções do WinHTTP. Para obter mais informações sobre o WinInet, consulte [sobre o WinInet](/windows/desktop/WinInet/about-wininet).

A função [**WinHttpCloseHandle**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpclosehandle) fecha os identificadores de **HINTERNET** do WinHTTP.

## <a name="naming-handles"></a>Identificadores de nomenclatura

Em toda a documentação do WinHTTP, as descrições das funções na API (interface de programação de aplicativo) e no código de exemplo mostram a criação e o uso de vários tipos de identificadores de **HINTERNET** . Para controlar os diferentes tipos de identificadores disponíveis, a nomeação desses identificadores é consistente. A tabela a seguir mostra os identificadores usados pela Convenção na documentação do.



| Tipo de identificador       | Identificador de criação de função                                                                                                          | Identificador |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------|------------|
| Identificador genérico    | [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen), [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect)ou [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) | hInternet  |
| Identificador de sessão    | [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen)                                                                                                | hSession   |
| Identificador de conexão | [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect)                                                                                          | hConnect   |
| Identificador de solicitação    | [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)                                                                                  | hRequest   |



 

## <a name="handle-hierarchy"></a>Hierarquia de identificadores

Os identificadores **HINTERNET** são mantidos em uma hierarquia. O identificador retornado por [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) é o identificador de **HINTERNET** de sessão. Chamar **WinHttpOpen** inicializa as funções WinHTTP e inicia um contexto de sessão que mantém as informações e configurações do usuário durante a vida útil do identificador da sessão. [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect) especifica um servidor http ou HTTPS de destino e cria um identificador de **HINTERNET** de conexão. Por padrão, o identificador de conexão herda as configurações do identificador de sessão. Cada recurso especificado com uma chamada para [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) é atribuído a um identificador **HINTERNET** de solicitação.

O diagrama a seguir ilustra a hierarquia de identificadores **HINTERNET** . Cada caixa no diagrama representa uma função WinHTTP que retorna um identificador **HINTERNET** .

![funções que criam identificadores](images/art-winhttp2.png)

Depois de fechar um identificador, o aplicativo deve estar preparado para receber notificações de retorno de chamada no identificador até que o valor final do **identificador de retorno de chamada do WinHTTP seja retornado para indicar \_ \_ \_ \_** que o identificador está completamente fechado.

Um identificador de sessão é chamado de pai de qualquer identificador de conexão usado para criar; da mesma forma, o identificador de conexão e seu identificador de sessão pai são chamados de pais de qualquer identificador de solicitação que o identificador de conexão é usado para criar.

Quando um identificador pai é fechado, todos os filhos que ele tem são indiretamente invalidados, mesmo que não sejam fechados, e as solicitações subsequentes que os utilizam falham com o **\_ \_ identificador inválido de erro** de erro. Não é possível confiar em solicitações assíncronas pendentes para concluir corretamente.

O diagrama a seguir mostra as funções que usam o identificador **HINTERNET** criado pelo [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest). As caixas sombreadas representam as funções do WinHTTP que criam identificadores, e as caixas simples mostram as funções que usam esses identificadores de **HINTERNET** . O diagrama também é organizado para mostrar a ordem na qual as funções de WinHTTP são normalmente chamadas.

![funções que criam identificadores](images/art-winhttp2.png)

## <a name="explanation-of-the-handle-hierarchy"></a>Explicação da hierarquia de identificadores

Primeiro, um identificador de sessão é criado com [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen). [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect) requer o identificador de sessão como seu primeiro parâmetro e retorna um identificador de conexão para um servidor especificado. Um identificador de solicitação é criado por [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest), que usa o identificador de conexão criado pelo [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect). Se o aplicativo optar por adicionar mais cabeçalhos à solicitação, ou se for necessário que o aplicativo defina credenciais para autenticação, [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) e [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) poderão ser chamados usando esse identificador de solicitação. A solicitação é enviada pelo [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest), que usa o identificador de solicitação. Depois de enviar a solicitação, os dados adicionais podem ser enviados ao servidor usando [**WinHttpWriteData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata)ou o aplicativo pode pular diretamente para [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) para especificar que nenhuma informação é enviada ao servidor. Neste ponto, dependendo da finalidade do aplicativo, o identificador de solicitação pode ser usado para chamar [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders), [**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes)ou recuperar um recurso com [**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable) e [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata).

 

 
