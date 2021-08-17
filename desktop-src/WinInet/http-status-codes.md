---
title: Códigos de status HTTP (Wininet. h)
description: A tabela a seguir contém as constantes e os valores correspondentes para os códigos de status HTTP retornados pelos servidores na Internet.
ms.assetid: 28a5e889-c8f3-4996-a1ca-c48866fa59d7
topic_type:
- apiref
api_name:
- HTTP_STATUS_CONTINUE
- HTTP_STATUS_SWITCH_PROTOCOLS
- HTTP_STATUS_OK
- HTTP_STATUS_CREATED
- HTTP_STATUS_ACCEPTED
- HTTP_STATUS_PARTIAL
- HTTP_STATUS_NO_CONTENT
- HTTP_STATUS_RESET_CONTENT
- HTTP_STATUS_PARTIAL_CONTENT
- HTTP_STATUS_AMBIGUOUS
- HTTP_STATUS_MOVED
- HTTP_STATUS_REDIRECT
- HTTP_STATUS_REDIRECT_METHOD
- HTTP_STATUS_NOT_MODIFIED
- HTTP_STATUS_USE_PROXY
- HTTP_STATUS_REDIRECT_KEEP_VERB
- HTTP_STATUS_BAD_REQUEST
- HTTP_STATUS_DENIED
- HTTP_STATUS_PAYMENT_REQ
- HTTP_STATUS_FORBIDDEN
- HTTP_STATUS_NOT_FOUND
- HTTP_STATUS_BAD_METHOD
- HTTP_STATUS_NONE_ACCEPTABLE
- HTTP_STATUS_PROXY_AUTH_REQ
- HTTP_STATUS_REQUEST_TIMEOUT
- HTTP_STATUS_CONFLICT
- HTTP_STATUS_GONE
- HTTP_STATUS_LENGTH_REQUIRED
- HTTP_STATUS_PRECOND_FAILED
- HTTP_STATUS_REQUEST_TOO_LARGE
- HTTP_STATUS_URI_TOO_LONG
- HTTP_STATUS_UNSUPPORTED_MEDIA
- HTTP_STATUS_RETRY_WITH
- HTTP_STATUS_SERVER_ERROR
- HTTP_STATUS_NOT_SUPPORTED
- HTTP_STATUS_BAD_GATEWAY
- HTTP_STATUS_SERVICE_UNAVAIL
- HTTP_STATUS_GATEWAY_TIMEOUT
- HTTP_STATUS_VERSION_NOT_SUP
api_location:
- Wininet.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01c6a8fecf7d1c7b3f95c1d4ce8040b9ba25e7d72ee4a41c8cbbcd24cd0da4bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117743804"
---
# <a name="http-status-codes-winineth"></a>Códigos de status HTTP (Wininet. h)

A tabela a seguir contém as constantes e os valores correspondentes para os códigos de status HTTP retornados pelos servidores na Internet.

<dl> <dt>

<span id="HTTP_STATUS_CONTINUE"></span><span id="http_status_continue"></span>**STATUS do HTTP \_ \_ continuar**
</dt> <dd> <dl> <dt>

100
</dt> <dt>



A solicitação pode ser continuada.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_SWITCH_PROTOCOLS"></span><span id="http_status_switch_protocols"></span>**\_protocolos de \_ comutação de status http \_**
</dt> <dd> <dl> <dt>

101
</dt> <dt>



O servidor alternou protocolos em um cabeçalho de atualização.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_OK"></span><span id="http_status_ok"></span>**STATUS do HTTP \_ \_ OK**
</dt> <dd> <dl> <dt>

200
</dt> <dt>



A solicitação foi concluída com êxito.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_CREATED"></span><span id="http_status_created"></span>**STATUS do HTTP \_ \_ criado**
</dt> <dd> <dl> <dt>

201
</dt> <dt>



A solicitação foi atendida e resultou na criação de um novo recurso.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_ACCEPTED"></span><span id="http_status_accepted"></span>**\_status http \_ aceito**
</dt> <dd> <dl> <dt>

202
</dt> <dt>



A solicitação foi aceita para processamento, mas o processamento não foi concluído.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_PARTIAL"></span><span id="http_status_partial"></span>**STATUS do HTTP \_ \_ parcial**
</dt> <dd> <dl> <dt>

203
</dt> <dt>



As informações meta retornadas no cabeçalho da entidade não são o conjunto definitivo disponível do servidor de origem.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_NO_CONTENT"></span><span id="http_status_no_content"></span>**STATUS do HTTP \_ \_ sem \_ conteúdo**
</dt> <dd> <dl> <dt>

204
</dt> <dt>



O servidor atendeu à solicitação, mas não há nenhuma informação nova a ser enviada de volta.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_RESET_CONTENT"></span><span id="http_status_reset_content"></span>**\_conteúdo de \_ redefinição de status http \_**
</dt> <dd> <dl> <dt>

205
</dt> <dt>



A solicitação foi concluída e o programa cliente deve redefinir a exibição de documento que fez com que a solicitação fosse enviada para permitir que o usuário inicie facilmente outra ação de entrada.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_PARTIAL_CONTENT"></span><span id="http_status_partial_content"></span>**\_ \_ conteúdo parcial do status http \_**
</dt> <dd> <dl> <dt>

206
</dt> <dt>



O servidor atendeu à solicitação GET parcial para o recurso.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_AMBIGUOUS"></span><span id="http_status_ambiguous"></span>**\_status http \_ ambíguo**
</dt> <dd> <dl> <dt>

300
</dt> <dt>



O servidor não pôde decidir o que retornar.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_MOVED"></span><span id="http_status_moved"></span>**STATUS do HTTP \_ \_ movido**
</dt> <dd> <dl> <dt>

301
</dt> <dt>



O recurso solicitado foi atribuído a um novo URI permanente (Uniform Resource Identifier) e todas as referências futuras a esse recurso devem ser feitas usando um dos URIs retornados.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_REDIRECT"></span><span id="http_status_redirect"></span>**\_redirecionamento de status http \_**
</dt> <dd> <dl> <dt>

302
</dt> <dt>



O recurso solicitado reside temporariamente em um URI diferente (Uniform Resource Identifier).


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_REDIRECT_METHOD"></span><span id="http_status_redirect_method"></span>**\_método de \_ redirecionamento de status http \_**
</dt> <dd> <dl> <dt>

303
</dt> <dt>



A resposta à solicitação pode ser encontrada em um URI diferente (Uniform Resource Identifier) e deve ser recuperada usando um verbo HTTP GET nesse recurso.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_NOT_MODIFIED"></span><span id="http_status_not_modified"></span>**\_status http \_ não \_ modificado**
</dt> <dd> <dl> <dt>

304
</dt> <dt>



O recurso solicitado não foi modificado.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_USE_PROXY"></span><span id="http_status_use_proxy"></span>**\_proxy de \_ uso de status http \_**
</dt> <dd> <dl> <dt>

305
</dt> <dt>



O recurso solicitado deve ser acessado por meio do proxy fornecido pelo campo local.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_REDIRECT_KEEP_VERB"></span><span id="http_status_redirect_keep_verb"></span>**\_verbo de \_ redirecionamento de status http \_ Keep \_**
</dt> <dd> <dl> <dt>

307
</dt> <dt>



A solicitação redirecionada mantém o mesmo verbo HTTP. Comportamento de HTTP/1.1.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_BAD_REQUEST"></span><span id="http_status_bad_request"></span>**\_ \_ solicitação inadequada de status http \_**
</dt> <dd> <dl> <dt>

400
</dt> <dt>



A solicitação não pôde ser processada pelo servidor devido à sintaxe inválida.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_DENIED"></span><span id="http_status_denied"></span>**STATUS do HTTP \_ \_ negado**
</dt> <dd> <dl> <dt>

401
</dt> <dt>



O recurso solicitado requer a autenticação do usuário.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_PAYMENT_REQ"></span><span id="http_status_payment_req"></span>**Req. de \_ pagamento de status http \_ \_**
</dt> <dd> <dl> <dt>

402
</dt> <dt>



Não implementado atualmente no protocolo HTTP.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_FORBIDDEN"></span><span id="http_status_forbidden"></span>**STATUS de HTTP \_ \_ proibido**
</dt> <dd> <dl> <dt>

403
</dt> <dt>



O servidor entendeu a solicitação, mas está se recusando a atendê-la.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_NOT_FOUND"></span><span id="http_status_not_found"></span>**\_status http \_ não \_ encontrado**
</dt> <dd> <dl> <dt>

404
</dt> <dt>



O servidor não encontrou nada correspondente ao URI solicitado (Uniform Resource Identifier).


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_BAD_METHOD"></span><span id="http_status_bad_method"></span>**\_ \_ método inadequado de status http \_**
</dt> <dd> <dl> <dt>

405
</dt> <dt>



O verbo HTTP usado não é permitido.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_NONE_ACCEPTABLE"></span><span id="http_status_none_acceptable"></span>**\_status http \_ nenhum \_ aceitável**
</dt> <dd> <dl> <dt>

406
</dt> <dt>



Nenhuma resposta aceitável para o cliente foi encontrada.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_PROXY_AUTH_REQ"></span><span id="http_status_proxy_auth_req"></span>**Req. de autenticação de proxy de \_ status http \_ \_ \_**
</dt> <dd> <dl> <dt>

407
</dt> <dt>



Autenticação de proxy necessária.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_REQUEST_TIMEOUT"></span><span id="http_status_request_timeout"></span>**\_ \_ tempo limite de solicitação de status http \_**
</dt> <dd> <dl> <dt>

408
</dt> <dt>



O servidor atingiu o tempo limite ao aguardar a solicitação.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_CONFLICT"></span><span id="http_status_conflict"></span>**\_conflito de status http \_**
</dt> <dd> <dl> <dt>

409
</dt> <dt>



A solicitação não pôde ser concluída devido a um conflito com o estado atual do recurso. O usuário deve enviar novamente com mais informações.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_GONE"></span><span id="http_status_gone"></span>**\_status http \_ ausente**
</dt> <dd> <dl> <dt>

410
</dt> <dt>



O recurso solicitado não está mais disponível no servidor e nenhum endereço de encaminhamento é conhecido.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_LENGTH_REQUIRED"></span><span id="http_status_length_required"></span>**\_comprimento de status http \_ \_ necessário**
</dt> <dd> <dl> <dt>

411
</dt> <dt>



O servidor se recusa a aceitar a solicitação sem um comprimento de conteúdo definido.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_PRECOND_FAILED"></span><span id="http_status_precond_failed"></span>**\_falha de \_ PRECOND de status http \_**
</dt> <dd> <dl> <dt>

412
</dt> <dt>



A pré-condição fornecida em um ou mais dos campos de cabeçalho da solicitação foi avaliada como falsa quando foi testada no servidor.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_REQUEST_TOO_LARGE"></span><span id="http_status_request_too_large"></span>**\_solicitação de status http \_ \_ muito \_ grande**
</dt> <dd> <dl> <dt>

413
</dt> <dt>



O servidor está se recusando a processar uma solicitação porque a entidade de solicitação é maior do que o servidor está disposto ou pode processar.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_URI_TOO_LONG"></span><span id="http_status_uri_too_long"></span>**\_URI de status http \_ \_ muito \_ longo**
</dt> <dd> <dl> <dt>

414
</dt> <dt>



O servidor está se recusando a atender à solicitação porque o URI de solicitação (Uniform Resource Identifier) é maior do que o servidor está disposto a interpretar.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_UNSUPPORTED_MEDIA"></span><span id="http_status_unsupported_media"></span>**\_mídia de status http \_ sem suporte \_**
</dt> <dd> <dl> <dt>

415
</dt> <dt>



O servidor está se recusando a atender à solicitação porque a entidade da solicitação está em um formato não suportado pelo recurso solicitado para o método solicitado.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_RETRY_WITH"></span><span id="http_status_retry_with"></span>**\_ \_ repetição de status http \_ com**
</dt> <dd> <dl> <dt>

449
</dt> <dt>



A solicitação deve ser repetida após a ação apropriada.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_SERVER_ERROR"></span><span id="http_status_server_error"></span>**\_ \_ erro do servidor de status http \_**
</dt> <dd> <dl> <dt>

500
</dt> <dt>



O servidor encontrou uma condição inesperada que o impediu de atender à solicitação.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_NOT_SUPPORTED"></span><span id="http_status_not_supported"></span>**\_status http \_ sem \_ suporte**
</dt> <dd> <dl> <dt>

501
</dt> <dt>



O servidor não oferece suporte à funcionalidade necessária para atender à solicitação.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_BAD_GATEWAY"></span><span id="http_status_bad_gateway"></span>**\_ \_ Gateway insatisfatório de status http \_**
</dt> <dd> <dl> <dt>

502
</dt> <dt>



O servidor, ao atuar como gateway ou proxy, recebeu uma resposta inválida do servidor upstream acessado na tentativa de atender à solicitação.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_SERVICE_UNAVAIL"></span><span id="http_status_service_unavail"></span>**serviço de status HTTP não \_ \_ \_ disp.**
</dt> <dd> <dl> <dt>

503
</dt> <dt>



O serviço está temporariamente sobrecarregado.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_GATEWAY_TIMEOUT"></span><span id="http_status_gateway_timeout"></span>**\_ \_ tempo limite do gateway de status http \_**
</dt> <dd> <dl> <dt>

504
</dt> <dt>



A solicitação atingiu o tempo limite ao aguardar um gateway.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_VERSION_NOT_SUP"></span><span id="http_status_version_not_sup"></span>**\_versão de status http \_ \_ não \_ sup**
</dt> <dd> <dl> <dt>

505
</dt> <dt>



O servidor não dá suporte a, ou recusa-se a oferecer suporte à versão do protocolo HTTP que foi usada na mensagem de solicitação.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

> [!Note]  
> O WinINet não oferece suporte a implementações de servidor. Além disso, ele não deve ser usado de um serviço. para implementações de servidor ou serviços, use [o Microsoft Windows HTTP services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>WinInet. h</dt> </dl> |



 

