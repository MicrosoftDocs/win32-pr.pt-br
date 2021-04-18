---
description: 'Saiba mais sobre: códigos de erro de rede do WUA'
ms.assetid: 07ff2ed7-09bc-4af7-84f9-66a921c0f53f
title: Códigos de erro de rede do WUA (Wuerror. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4fb2c027939afda3fe5817a8a860469fc90b766
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105764113"
---
# <a name="wua-networking-error-codes"></a>Códigos de erro de rede do WUA

A API do WUA (agente de Windows Update) pode retornar os seguintes códigos de erro ao executar operações de rede, como Pesquisar atualizações:



| Constante/valor                                                                                                                                                                                                                                                                                        | Descrição                                                                                                                                                                                  |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WU_E_WINHTTP_INVALID_FILE"></span><span id="wu_e_winhttp_invalid_file"></span><dl> <dt>**Wu \_ E \_ WinHTTP 0x80240038 de \_ \_ arquivo inválido**</dt> <dt></dt> </dl>                                  | O arquivo baixado tem um tipo de conteúdo inesperado.<br/>                                                                                                                               |
| <span id="WU_E_PT_HTTP_STATUS_BAD_REQUEST"></span><span id="wu_e_pt_http_status_bad_request"></span><dl> <dt>**Wu \_ \_Status HTTP de E pt- \_ \_ \_ \_ solicitação inadequada**</dt> <dt>0x80244016</dt> </dl>              | Igual ao status do HTTP 400 – o servidor não pôde processar a solicitação devido a uma sintaxe inválida.<br/>                                                                                         |
| <span id="WU_E_PT_HTTP_STATUS_DENIED"></span><span id="wu_e_pt_http_status_denied"></span><dl> <dt>**Wu \_ \_Status HTTP do E pt \_ \_ \_ negado**</dt> <dt>0x80244017</dt> </dl>                              | Igual ao status do HTTP 401 – o recurso solicitado requer autenticação do usuário.<br/>                                                                                                    |
| <span id="WU_E_PT_HTTP_STATUS_FORBIDDEN"></span><span id="wu_e_pt_http_status_forbidden"></span><dl> <dt>**Wu \_ \_Status HTTP do E pt \_ \_ \_ proibido**</dt> <dt>0x80244018</dt> </dl>                     | Igual ao status do HTTP 403 – o servidor entendeu a solicitação, mas recusa a atendê-la.<br/>                                                                                              |
| <span id="WU_E_PT_HTTP_STATUS_NOT_FOUND"></span><span id="wu_e_pt_http_status_not_found"></span><dl> <dt>**Wu \_ \_Status HTTP do E pt \_ \_ \_ não \_ encontrado**</dt> <dt>0x80244019</dt> </dl>                    | Igual ao status HTTP 404 – o servidor não pode localizar o URI solicitado (Uniform Resource Identifier).<br/>                                                                                 |
| <span id="WU_E_PT_HTTP_STATUS_BAD_METHOD"></span><span id="wu_e_pt_http_status_bad_method"></span><dl> <dt>**Wu \_ \_Status HTTP de E pt- \_ \_ \_ \_ método inadequado**</dt> <dt>0x8024401A</dt> </dl>                 | Igual ao status HTTP 405 – o método HTTP não é permitido.<br/>                                                                                                                         |
| <span id="WU_E_PT_HTTP_STATUS_PROXY_AUTH_REQ"></span><span id="wu_e_pt_http_status_proxy_auth_req"></span><dl> <dt>**Wu \_ \_Autenticação de \_ \_ proxy de \_ status \_ \_ de http de E pt**</dt> <dt>0x8024401B</dt> </dl>    | Igual ao status do HTTP 407 – a autenticação de proxy é necessária.<br/>                                                                                                                       |
| <span id="WU_E_PT_HTTP_STATUS_REQUEST_TIMEOUT"></span><span id="wu_e_pt_http_status_request_timeout"></span><dl> <dt>**Wu \_ \_ \_ \_ \_ \_ Tempo limite de solicitação de status http E pt**</dt> <dt>0x8024401C</dt> </dl>  | Igual ao status HTTP 408 – o servidor atingiu o tempo limite ao aguardar a solicitação.<br/>                                                                                                           |
| <span id="WU_E_PT_HTTP_STATUS_CONFLICT"></span><span id="wu_e_pt_http_status_conflict"></span><dl> <dt>**Wu \_ 0x8024401D \_ de \_ \_ \_ conflito de status HTTP de E pt**</dt> <dt></dt> </dl>                        | Igual ao status HTTP 409 – a solicitação não foi concluída devido a um conflito com o estado atual do recurso.<br/>                                                                 |
| <span id="WU_E_PT_HTTP_STATUS_GONE"></span><span id="wu_e_pt_http_status_gone"></span><dl> <dt>**Wu \_ O \_ status HTTP de E pt \_ \_ \_ já**</dt> <dt>0x8024401E</dt> </dl>                                    | Igual ao status do HTTP 410 – o recurso solicitado não está mais disponível no servidor.<br/>                                                                                                |
| <span id="WU_E_PT_HTTP_STATUS_SERVER_ERROR"></span><span id="wu_e_pt_http_status_server_error"></span><dl> <dt>**Wu \_ \_Erro de \_ \_ servidor de \_ \_ status http E pt**</dt> <dt>0x8024401F</dt> </dl>           | Igual ao status HTTP 500 – um erro interno ao servidor impediu a conclusão da solicitação.<br/>                                                                                       |
| <span id="WU_E_PT_HTTP_STATUS_NOT_SUPPORTED"></span><span id="wu_e_pt_http_status_not_supported"></span><dl> <dt>**Wu \_ \_ \_ \_ \_ Não \_ há suporte para o status HTTP do E pt**</dt> <dt>0x80244020</dt> </dl>        | Igual ao status do HTTP 501 – o servidor não oferece suporte à funcionalidade necessária para atender à solicitação. <br/>                                                                             |
| <span id="WU_E_PT_HTTP_STATUS_BAD_GATEWAY"></span><span id="wu_e_pt_http_status_bad_gateway"></span><dl> <dt>**Wu \_ STATUS HTTP de E pt 0x80244021 de \_ \_ \_ \_ \_ Gateway inválidos**</dt> <dt></dt> </dl>              | Igual ao status HTTP 502 – o servidor, ao atuar como gateway ou proxy, recebeu uma resposta inválida do servidor upstream que ele acessou ao tentar atender à solicitação.<br/> |
| <span id="WU_E_PT_HTTP_STATUS_SERVICE_UNAVAIL"></span><span id="wu_e_pt_http_status_service_unavail"></span><dl> <dt>**Wu \_ \_Serviço de \_ \_ status http \_ \_ do E pt**</dt> <dt>0x80244022</dt> não disp. </dl>  | Igual ao status HTTP 503 – o serviço está temporariamente sobrecarregado.<br/>                                                                                                                  |
| <span id="WU_E_PT_HTTP_STATUS_GATEWAY_TIMEOUT"></span><span id="wu_e_pt_http_status_gateway_timeout"></span><dl> <dt>**Wu \_ \_ \_ \_ \_ \_ Tempo limite do gateway de status http E pt**</dt> <dt>0x80244023</dt> </dl>  | Igual ao status HTTP 504 – a solicitação atingiu o tempo limite aguardando um gateway.<br/>                                                                                                        |
| <span id="WU_E_PT_HTTP_STATUS_VERSION_NOT_SUP"></span><span id="wu_e_pt_http_status_version_not_sup"></span><dl> <dt>**Wu \_ \_Versão de \_ status http E pt \_ \_ \_ não \_ sup**</dt> <dt>0x80244024</dt> </dl> | Igual ao status HTTP 505 – o servidor não oferece suporte à versão do protocolo HTTP usada para a solicitação.<br/>                                                                             |
| <span id="WU_E_PT_HTTP_STATUS_NOT_MAPPED"></span><span id="wu_e_pt_http_status_not_mapped"></span><dl> <dt>**Wu \_ \_ \_ Status http E \_ pt \_ não \_ mapeado**</dt> <dt>0x8024402B</dt> </dl>                 | A solicitação não pôde ser concluída e o motivo não correspondeu a nenhum dos códigos de \_ erro http do Wu E \_ pt \_ \_ \* .<br/>                                                               |
| <span id="WU_E_PT_WINHTTP_NAME_NOT_RESOLVED"></span><span id="wu_e_pt_winhttp_name_not_resolved"></span><dl> <dt>**Wu \_ \_Nome WinHTTP do E pt \_ \_ \_ não \_ resolvido**</dt> <dt>0x8024402C</dt> </dl>        | Igual ao erro \_ \_ nome \_ do WinHTTP não \_ resolvido-o servidor proxy ou o nome do servidor de destino não pode ser resolvido.<br/>                                                                          |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|--------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wuerror. h</dt> </dl> |



 

 




