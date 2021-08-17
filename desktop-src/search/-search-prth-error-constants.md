---
description: 'Mensagens de erro retornadas por manipuladores de protocolo:'
ms.assetid: b5e99ad1-1698-483c-8173-796af33085c4
title: Mensagens de erro do manipulador de protocolo de pesquisa (Searchapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4473e3e235641e5b4bb5d86313b4154cd00ec029fe96d42d8964dab51f33780f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118969725"
---
# <a name="search-protocol-handler-error-messages"></a>Mensagens de erro do manipulador de protocolo de pesquisa

Mensagens de erro retornadas por manipuladores de protocolo:



| Constante/valor                                                                                                                                                                                                                                                    | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PRTH_E_ACCESS_DENIED"></span><span id="prth_e_access_denied"></span><dl> <dt>**PRTH \_ E \_ acesso \_ negado**</dt> <dt>0x80041205L</dt> </dl>             | Acesso negado. Se isso ocorrer durante um rastreamento incremental, o arquivo será excluído da fila de URL do coletor.<br/>                                                                                                                                                                                                                                                                                                                |
| <span id="PRTH_E_ACL_IS_READ_NONE"></span><span id="prth_e_acl_is_read_none"></span><dl> <dt>**PRTH \_ E \_ ACL não \_ é \_ lido \_ nenhum**</dt> <dt>0x80041211L</dt> </dl>  | O item não será indexado. Sua ACL não permite ler o item.<br/>                                                                                                                                                                                                                                                                                                                                                                |
| <span id="PRTH_E_ACL_TOO_BIG"></span><span id="prth_e_acl_too_big"></span><dl> <dt>**PRTH \_ E \_ ACL \_ muito \_ grandes**</dt> <dt>0x80041212L</dt> </dl>                  | A ACL excedeu 64 KB. A pesquisa não indexa o item.<br/>                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="PRTH_E_BAD_REQUEST"></span><span id="prth_e_bad_request"></span><dl> <dt>**PRTH \_ E 0x80041208L de \_ \_ solicitação inadequada**</dt> <dt></dt> </dl>                   | A solicitação era inválida devido a um erro na URL.<br/>                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="PRTH_E_COMM_ERROR"></span><span id="prth_e_comm_error"></span><dl> <dt>**PRTH \_ 0x80041200L \_ de \_ erro de E comm**</dt> <dt></dt> </dl>                      | Indica um erro de comunicação ou servidor. Se houver muitos desses erros para um servidor específico, o coletor marcará o servidor como indisponível.<br/>                                                                                                                                                                                                                                                                          |
| <span id="PRTH_E_NOT_REDIRECTED"></span><span id="prth_e_not_redirected"></span><dl> <dt>**PRTH \_ E \_ não \_ 0X80041207L Redirecionado**</dt> <dt></dt> </dl>          | A URL redirecionada não existe.<br/>                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="PRTH_E_OBJ_NOT_FOUND"></span><span id="prth_e_obj_not_found"></span><dl> <dt>**PRTH \_ E \_ obj \_ não \_ encontrado**</dt> <dt>0x80041201L</dt> </dl>            | Objeto não localizado. Indica que o gatherer deve excluir o documento da fila se ele não for encontrado durante um rastreamento incremental.<br/>                                                                                                                                                                                                                                                                                          |
| <span id="PRTH_E_REQUEST_ERROR"></span><span id="prth_e_request_error"></span><dl> <dt>**PRTH \_ \_ \_ Erro de solicitação E**</dt> <dt>0x80041202L</dt> </dl>             | Não há suporte para as opções usadas.<br/>                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="PRTH_E_SERVER_ERROR"></span><span id="prth_e_server_error"></span><dl> <dt>**PRTH \_ 0x80041206L \_ de \_ erro do servidor E**</dt> <dt></dt> </dl>                | Erro de comunicação ou servidor. Se houver muitos desses erros para um servidor específico, o coletor marcará o servidor como indisponível.<br/>                                                                                                                                                                                                                                                                                      |
| <span id="PRTH_S_NOT_ALL_PARTS"></span><span id="prth_s_not_all_parts"></span><dl> <dt>**PRTH \_ S \_ nem \_ todas as \_ partes**</dt> <dt>0x8004121BL</dt> </dl>            | Partes de um item não podem ser acessadas.<br/>                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="PRTH_S_NOT_MODIFIED"></span><span id="prth_s_not_modified"></span><dl> <dt>**PRTH \_ 0x00041203L S \_ não \_ modificados**</dt> <dt></dt> </dl>                | O conteúdo do item não foi alterado. Se esse erro ocorrer durante um rastreamento incremental, o gatherer ignorará este item porque o item não foi alterado.<br/>                                                                                                                                                                                                                                                                                   |
| <span id="PRTH_S_TRY_IMPERSONATING"></span><span id="prth_s_try_impersonating"></span><dl> <dt>**PRTH \_ S \_ Experimente \_ representar**</dt> <dt>0x00041225L</dt> </dl> | O item deve ser acessado ao representar um usuário. O manipulador de protocolo deve implementar [**IUrlAccessor3:: GetImpersonationSidBlobs**](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor3-getimpersonationsidblobs) para que o host de protocolo de pesquisa possa recuperar uma lista de SIDs a serem usados para representação e pode reverter para o uso de [**IUrlAccessor2**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor2), representando um dos usuários permitidos ao abrir o item. <br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP com SP2, somente aplicativos do Windows Vista \[ desktop\]<br/>                    |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                   |
| Redistribuível<br/>          | Windows Pesquisa de desktop (WDS) 3,0<br/>                                            |
| Cabeçalho<br/>                   | <dl> <dt>Searchapi. h</dt> </dl> |



 

 




