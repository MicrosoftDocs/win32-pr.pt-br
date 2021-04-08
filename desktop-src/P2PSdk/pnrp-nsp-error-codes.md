---
description: Códigos de erro NSP PNRP
ms.assetid: adf40b1a-c5d6-418d-a012-cf6ba7d4fa24
title: Códigos de erro NSP PNRP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47b02959c921c8e3a468cadfa87dba6fb8d3c29d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828401"
---
# <a name="pnrp-nsp-error-codes"></a>Códigos de erro NSP PNRP

Se a função provedor de namespace (NSP) retornar **um \_ erro de soquete**, [WSAGetLastError](winsock-nsp-reference-links.md) deverá ser usado para obter mais informações de erro. O NSP PNRP retorna os seguintes códigos de erro:



| Termo                                                                                                                                                                     | Descrição                                                                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="WSA_E_CANCELLED"></span><span id="wsa_e_cancelled"></span>WSA \_ E \_ cancelado<br/>                                                                         | Uma operação foi cancelada.<br/>                                                                               |
| <span id="__WSA_E_NO_MORE"></span><span id="__wsa_e_no_more"></span> CABEÇALHO \_ E \_ não \_ mais<br/>                                                                         | Os resultados de uma solicitação resolvida não estão prontos. Isso pode não ser um erro.<br/>                              |
| <span id="_WSA_IO_PENDING_"></span><span id="_wsa_io_pending_"></span>\_e/s de WSA \_ pendente <br/>                                                                      | Uma operação não foi concluída.<br/>                                                                           |
| <span id="WSA_NOT_ENOUGH_MEMORY"></span><span id="wsa_not_enough_memory"></span>o WSA \_ não tem \_ \_ memória suficiente<br/>                                                      | Não há memória suficiente para concluir uma ação especificada.<br/>                                              |
| <span id="WSA_OPERATION_ABORTED"></span><span id="wsa_operation_aborted"></span>operação de WSA \_ \_ anulada<br/>                                                       | Uma operação foi cancelada.<br/>                                                                               |
| <span id="WSA_PNRP_CLOUD_DISABLED"></span><span id="wsa_pnrp_cloud_disabled"></span>\_nuvem PNRP do WSA \_ \_ desabilitada<br/>                                                | Um nome de nuvem especificado está desabilitado.<br/>                                                                     |
| <span id="WSA_PNRP_CLOUD_NOT_FOUND"></span><span id="wsa_pnrp_cloud_not_found"></span>\_nuvem PNRP do WSA \_ \_ não \_ encontrada<br/>                                            | Um nome de nuvem especificado não está disponível.<br/>                                                                |
| <span id="WSA_PNRP_CLOUD_IS_SEARCH_ONLY"></span><span id="wsa_pnrp_cloud_is_search_only"></span>o \_ WSA \_ PNRP \_ Cloud \_ é \_ somente pesquisa<br/>                            | Foi feita uma tentativa de registrar um nome em uma nuvem que foi configurada para ser resolvida apenas.<br/>     |
| <span id="WSA_PNRP_CLIENT_INVALID_COMPARTMENT_ID"></span><span id="wsa_pnrp_client_invalid_compartment_id"></span>\_ID de \_ \_ compartimento inválido \_ do cliente PNRP de WSA \_<br/> | Usando o PNRP em um compartimento fora do padrão. O PNRP só funcionará no compartimento padrão.<br/>     |
| <span id="WSA_PNRP_INVALID_IDENTITY"></span><span id="wsa_pnrp_invalid_identity"></span>\_ \_ identidade inválida do WSA PNRP \_<br/>                                          | Uma identidade especificada não pode ser acessada.<br/>                                                                |
| <span id="WSA_PNRP_TOO_MUCH_LOAD"></span><span id="wsa_pnrp_too_much_load"></span>\_ \_ carga excessiva do \_ WSA \_ PNRP<br/>                                                  | Um nome de par não pode ser criado porque o computador não tem os recursos para processar a solicitação. <br/> |
| <span id="WSAEFAULT"></span><span id="wsaefault"></span>WSAEFAULT<br/>                                                                                             | Uma operação não é permitida no estado atual.<br/>                                                        |
| <span id="WSAEINVAL"></span><span id="wsaeinval"></span>WSAEINVAL<br/>                                                                                             | Um parâmetro inválido ou uma combinação de parâmetros foi especificada.<br/>                                         |
| <span id="WSAENETUNREACH"></span><span id="wsaenetunreach"></span>WSAENETUNREACH<br/>                                                                              | Uma conexão com a rede é perdida.<br/>                                                                    |
| <span id="WSAENOTIMPLEMENTED"></span><span id="wsaenotimplemented"></span>WSAENOTIMPLEMENTED<br/>                                                                  | Uma funcionalidade especificada não é implementada pelo PNRP.<br/>                                                   |
| <span id="WSAEOPNOTSUPP"></span><span id="wsaeopnotsupp"></span>WSAEOPNOTSUPP<br/>                                                                                 | Uma funcionalidade especificada não é suportada por PNRP.<br/>                                                     |
| <span id="WSAEWOULDBLOCK"></span><span id="wsaewouldblock"></span>WSAEWOULDBLOCK<br/>                                                                              | Uma operação não foi concluída.<br/>                                                                           |
| <span id="__WSASERVICE_NOT_FOUND"></span><span id="__wsaservice_not_found"></span> WSASERVICE \_ não \_ encontrado<br/>                                                     | Não há suporte para um provedor, namespace ou ID de serviço especificado.<br/>                                       |
| <span id="WSASYSNOTREADY"></span><span id="wsasysnotready"></span>WSASYSNOTREADY<br/>                                                                              | O serviço não foi iniciado.<br/>                                                                             |



 

 

 




