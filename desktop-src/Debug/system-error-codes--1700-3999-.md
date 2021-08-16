---
description: Descreve os códigos de erro 1700-3999 definidos no arquivo de título WinError.h e destina-se a desenvolvedores.
ms.assetid: 7e57c087-53e4-443d-9227-21d9eb3cc71f
title: Códigos de erro do sistema (1700-3999) (WinError.h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 707425f7714c84d92bf5bc001f57c1677183b9edbd9170236d1c629bc0aaf121
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118405597"
---
# <a name="system-error-codes-1700-3999"></a>Códigos de erro do sistema (1700-3999)

> [!NOTE]
> Essas informações são destinadas a desenvolvedores que depuram erros do sistema. Para outros erros, como problemas com Windows Atualização, há uma lista de recursos na [página Códigos de](system-error-codes.md) erro.

A lista a seguir descreve [os códigos de](system-error-codes.md) erro do sistema para erros de 1700 a 3999. Eles são retornados pela [**função GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) quando muitas funções falham. Para recuperar o texto de descrição do erro em seu aplicativo, use a [**função FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) com o **sinalizador FORMAT MESSAGE FROM \_ \_ \_ SYSTEM.**

<dl> <dt>

<span id="RPC_S_INVALID_STRING_BINDING"></span><span id="rpc_s_invalid_string_binding"></span>**ASSOCIAÇÃO DE \_ CADEIA DE \_ CARACTERES INVÁLIDA \_ DO RPC S \_**
</dt> <dd> <dl> <dt>

1700 (0x6A4)
</dt> <dt>



A associação de cadeia de caracteres é inválida.


</dt> </dl> </dd> <dt>

<span id="RPC_S_WRONG_KIND_OF_BINDING"></span><span id="rpc_s_wrong_kind_of_binding"></span>**TIPO \_ DE \_ ASSOCIAÇÃO ERRADO \_ DO \_ \_ RPC**
</dt> <dd> <dl> <dt>

1701 (0x6A5)
</dt> <dt>



O identificador de associação não é o tipo correto.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_BINDING"></span><span id="rpc_s_invalid_binding"></span>**ASSOCIAÇÃO INVÁLIDA DO RPC \_ S \_ \_**
</dt> <dd> <dl> <dt>

1702 (0x6A6)
</dt> <dt>



O alça de associação é inválido.


</dt> </dl> </dd> <dt>

<span id="RPC_S_PROTSEQ_NOT_SUPPORTED"></span><span id="rpc_s_protseq_not_supported"></span>**NÃO \_ HÁ SUPORTE PARA RPC S \_ PROTSEQ \_ \_**
</dt> <dd> <dl> <dt>

1703 (0x6A7)
</dt> <dt>



Não há suporte para a sequência de protocolo RPC.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_RPC_PROTSEQ"></span><span id="rpc_s_invalid_rpc_protseq"></span>**RPC \_ S \_ \_ \_ PROTSEQ RPC INVÁLIDO**
</dt> <dd> <dl> <dt>

1704 (0x6A8)
</dt> <dt>



A sequência de protocolo RPC é inválida.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_STRING_UUID"></span><span id="rpc_s_invalid_string_uuid"></span>**\_UUID DE CADEIA DE \_ \_ \_ CARACTERES INVÁLIDA DO RPC S**
</dt> <dd> <dl> <dt>

1705 (0x6A9)
</dt> <dt>



O UUID (identificador exclusivo universal) da cadeia de caracteres é inválido.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_ENDPOINT_FORMAT"></span><span id="rpc_s_invalid_endpoint_format"></span>**RPC \_ S FORMATO DE PONTO DE EXTREMIDADE \_ \_ \_ INVÁLIDO**
</dt> <dd> <dl> <dt>

1706 (0x6AA)
</dt> <dt>



O formato do ponto de extremidade é inválido.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_NET_ADDR"></span><span id="rpc_s_invalid_net_addr"></span>**RPC \_ S \_ \_ ADDR NET \_ INVÁLIDO**
</dt> <dd> <dl> <dt>

1707 (0x6AB)
</dt> <dt>



O endereço de rede é inválido.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_ENDPOINT_FOUND"></span><span id="rpc_s_no_endpoint_found"></span>**RPC \_ S NENHUM PONTO DE EXTREMIDADE \_ \_ \_ ENCONTRADO**
</dt> <dd> <dl> <dt>

1708 (0x6AC)
</dt> <dt>



Nenhum ponto de extremidade foi encontrado.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_TIMEOUT"></span><span id="rpc_s_invalid_timeout"></span>**TEMPOOUT INVÁLIDO DO RPC \_ S \_ \_**
</dt> <dd> <dl> <dt>

1709 (0x6AD)
</dt> <dt>



O valor de tempoout é inválido.


</dt> </dl> </dd> <dt>

<span id="RPC_S_OBJECT_NOT_FOUND"></span><span id="rpc_s_object_not_found"></span>**OBJETO RPC \_ S \_ NÃO \_ \_ ENCONTRADO**
</dt> <dd> <dl> <dt>

1710 (0x6AE)
</dt> <dt>



O UUID (identificador exclusivo universal) do objeto não foi encontrado.


</dt> </dl> </dd> <dt>

<span id="RPC_S_ALREADY_REGISTERED"></span><span id="rpc_s_already_registered"></span>**RPC \_ S \_ JÁ \_ REGISTRADOS**
</dt> <dd> <dl> <dt>

1711 (0x6AF)
</dt> <dt>



O UUID (identificador exclusivo universal) do objeto já foi registrado.


</dt> </dl> </dd> <dt>

<span id="RPC_S_TYPE_ALREADY_REGISTERED"></span><span id="rpc_s_type_already_registered"></span>**TIPO RPC \_ S \_ JÁ \_ \_ REGISTRADO**
</dt> <dd> <dl> <dt>

1712 (0x6B0)
</dt> <dt>



O UUID (identificador exclusivo universal) do tipo já foi registrado.


</dt> </dl> </dd> <dt>

<span id="RPC_S_ALREADY_LISTENING"></span><span id="rpc_s_already_listening"></span>**RPC \_ S \_ JÁ \_ ESCUTANDO**
</dt> <dd> <dl> <dt>

1713 (0x6B1)
</dt> <dt>



O servidor RPC já está escutando.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_PROTSEQS_REGISTERED"></span><span id="rpc_s_no_protseqs_registered"></span>**RPC \_ S \_ NO \_ PROTSEQS \_ REGISTRADO**
</dt> <dd> <dl> <dt>

1714 (0x6B2)
</dt> <dt>



Nenhuma sequência de protocolo foi registrada.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NOT_LISTENING"></span><span id="rpc_s_not_listening"></span>**RPC \_ S \_ NÃO \_ ESCUTANDO**
</dt> <dd> <dl> <dt>

1715 (0x6B3)
</dt> <dt>



O servidor RPC não está escutando.


</dt> </dl> </dd> <dt>

<span id="RPC_S_UNKNOWN_MGR_TYPE"></span><span id="rpc_s_unknown_mgr_type"></span>**RPC \_ S \_ UNKNOWN \_ MGR \_ TYPE**
</dt> <dd> <dl> <dt>

1716 (0x6B4)
</dt> <dt>



O tipo de gerente é desconhecido.


</dt> </dl> </dd> <dt>

<span id="RPC_S_UNKNOWN_IF"></span><span id="rpc_s_unknown_if"></span>**RPC \_ S \_ UNKNOWN \_ IF**
</dt> <dd> <dl> <dt>

1717 (0x6B5)
</dt> <dt>



A interface é desconhecida.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_BINDINGS"></span><span id="rpc_s_no_bindings"></span>**RPC \_ S \_ NO \_ BINDINGS**
</dt> <dd> <dl> <dt>

1718 (0x6B6)
</dt> <dt>



Não há nenhuma associação.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_PROTSEQS"></span><span id="rpc_s_no_protseqs"></span>**RPC \_ S \_ NO \_ PROTSEQS**
</dt> <dd> <dl> <dt>

1719 (0x6B7)
</dt> <dt>



Não há sequências de protocolo.


</dt> </dl> </dd> <dt>

<span id="RPC_S_CANT_CREATE_ENDPOINT"></span><span id="rpc_s_cant_create_endpoint"></span>**RPC \_ S \_ CANT \_ CREATE \_ ENDPOINT**
</dt> <dd> <dl> <dt>

1720 (0x6B8)
</dt> <dt>



O ponto de extremidade não pode ser criado.


</dt> </dl> </dd> <dt>

<span id="RPC_S_OUT_OF_RESOURCES"></span><span id="rpc_s_out_of_resources"></span>**RPC \_ S \_ SEM \_ \_ RECURSOS**
</dt> <dd> <dl> <dt>

1721 (0x6B9)
</dt> <dt>



Não há recursos suficientes disponíveis para concluir essa operação.


</dt> </dl> </dd> <dt>

<span id="RPC_S_SERVER_UNAVAILABLE"></span><span id="rpc_s_server_unavailable"></span>**SERVIDOR RPC \_ S \_ \_ INDISPONÍVEL**
</dt> <dd> <dl> <dt>

1722 (0x6BA)
</dt> <dt>



O servidor RPC não está disponível.


</dt> </dl> </dd> <dt>

<span id="RPC_S_SERVER_TOO_BUSY"></span><span id="rpc_s_server_too_busy"></span>**RPC \_ S SERVER MUITO \_ \_ \_ OCUPADO**
</dt> <dd> <dl> <dt>

1723 (0x6BB)
</dt> <dt>



O servidor RPC está muito ocupado para concluir essa operação.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_NETWORK_OPTIONS"></span><span id="rpc_s_invalid_network_options"></span>**OPÇÕES DE \_ REDE \_ \_ INVÁLIDAS DO \_ RPC S**
</dt> <dd> <dl> <dt>

1724 (0x6BC)
</dt> <dt>



As opções de rede são inválidas.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_CALL_ACTIVE"></span><span id="rpc_s_no_call_active"></span>**RPC \_ S SEM CHAMADA \_ \_ \_ ATIVA**
</dt> <dd> <dl> <dt>

1725 (0x6BD)
</dt> <dt>



Não há nenhuma chamada de procedimento remoto ativa nesse thread.


</dt> </dl> </dd> <dt>

<span id="RPC_S_CALL_FAILED"></span><span id="rpc_s_call_failed"></span>**FALHA NA CHAMADA DO RPC \_ S \_ \_**
</dt> <dd> <dl> <dt>

1726 (0x6BE)
</dt> <dt>



Falha na chamada de procedimento remoto.


</dt> </dl> </dd> <dt>

<span id="RPC_S_CALL_FAILED_DNE"></span><span id="rpc_s_call_failed_dne"></span>**DNE DE CHAMADA DO RPC \_ \_ COM \_ \_ FALHA**
</dt> <dd> <dl> <dt>

1727 (0x6BF)
</dt> <dt>



A chamada de procedimento remoto falhou e não foi executada.


</dt> </dl> </dd> <dt>

<span id="RPC_S_PROTOCOL_ERROR"></span><span id="rpc_s_protocol_error"></span>**ERRO DE \_ PROTOCOLO \_ \_ RPC**
</dt> <dd> <dl> <dt>

1728 (0x6C0)
</dt> <dt>



Ocorreu um erro de protocolo RPC (chamada de procedimento remoto).


</dt> </dl> </dd> <dt>

<span id="RPC_S_PROXY_ACCESS_DENIED"></span><span id="rpc_s_proxy_access_denied"></span>**ACESSO DE PROXY DO RPC \_ \_ \_ \_ NEGADO**
</dt> <dd> <dl> <dt>

1729 (0x6C1)
</dt> <dt>



O acesso ao proxy HTTP é negado.


</dt> </dl> </dd> <dt>

<span id="RPC_S_UNSUPPORTED_TRANS_SYN"></span><span id="rpc_s_unsupported_trans_syn"></span>**RPC \_ S \_ UNSUPPORTED \_ TRANS \_ SYN**
</dt> <dd> <dl> <dt>

1730 (0x6C2)
</dt> <dt>



A sintaxe de transferência não é suportada pelo servidor RPC.


</dt> </dl> </dd> <dt>

<span id="RPC_S_UNSUPPORTED_TYPE"></span><span id="rpc_s_unsupported_type"></span>**tipo de RPC \_ S \_ sem suporte \_**
</dt> <dd> <dl> <dt>

1732 (0x6C4)
</dt> <dt>



Não há suporte para o tipo de identificador exclusivo universal (UUID).


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_TAG"></span><span id="rpc_s_invalid_tag"></span>**marca de RPC \_ S \_ inválida \_**
</dt> <dd> <dl> <dt>

1733 (0x6C5)
</dt> <dt>



A marca é inválida.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_BOUND"></span><span id="rpc_s_invalid_bound"></span>**Associação de RPC \_ S \_ inválida \_**
</dt> <dd> <dl> <dt>

1734 (0x6C6)
</dt> <dt>



Os limites de matriz são inválidos.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_ENTRY_NAME"></span><span id="rpc_s_no_entry_name"></span>**\_ \_ nenhum nome de \_ entrada \_ do RPC**
</dt> <dd> <dl> <dt>

1735 (0x6C7)
</dt> <dt>



A associação não contém um nome de entrada.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_NAME_SYNTAX"></span><span id="rpc_s_invalid_name_syntax"></span>**\_sintaxe de \_ \_ nome inválido \_ de RPC S**
</dt> <dd> <dl> <dt>

1736 (0x6C8)
</dt> <dt>



A sintaxe do nome é inválida.


</dt> </dl> </dd> <dt>

<span id="RPC_S_UNSUPPORTED_NAME_SYNTAX"></span><span id="rpc_s_unsupported_name_syntax"></span>**\_sintaxe de \_ nome não suportada RPC S \_ \_**
</dt> <dd> <dl> <dt>

1737 (0x6C9)
</dt> <dt>



Não há suporte para a sintaxe de nome.


</dt> </dl> </dd> <dt>

<span id="RPC_S_UUID_NO_ADDRESS"></span><span id="rpc_s_uuid_no_address"></span>**RPC \_ S \_ UUID \_ sem \_ Endereço**
</dt> <dd> <dl> <dt>

1739 (0x6CB)
</dt> <dt>



Nenhum endereço de rede está disponível para ser usado para construir um identificador exclusivo universal (UUID).


</dt> </dl> </dd> <dt>

<span id="RPC_S_DUPLICATE_ENDPOINT"></span><span id="rpc_s_duplicate_endpoint"></span>**\_ponto de \_ extremidade duplicado \_ de RPC**
</dt> <dd> <dl> <dt>

1740 (0x6CC)
</dt> <dt>



O ponto de extremidade é uma duplicata.


</dt> </dl> </dd> <dt>

<span id="RPC_S_UNKNOWN_AUTHN_TYPE"></span><span id="rpc_s_unknown_authn_type"></span>**\_tipo de \_ \_ autenticação desconhecido RPC \_ S**
</dt> <dd> <dl> <dt>

1741 (0x6CD)
</dt> <dt>



O tipo de autenticação é desconhecido.


</dt> </dl> </dd> <dt>

<span id="RPC_S_MAX_CALLS_TOO_SMALL"></span><span id="rpc_s_max_calls_too_small"></span>**\_ \_ chamadas máximas RPC S \_ \_ muito \_ pequenas**
</dt> <dd> <dl> <dt>

1742 (0x6CE)
</dt> <dt>



O número máximo de chamadas é muito pequeno.


</dt> </dl> </dd> <dt>

<span id="RPC_S_STRING_TOO_LONG"></span><span id="rpc_s_string_too_long"></span>**\_cadeia de caracteres RPC S \_ \_ muito \_ longa**
</dt> <dd> <dl> <dt>

1743 (0x6CF)
</dt> <dt>



A cadeia de caracteres é longa demais.


</dt> </dl> </dd> <dt>

<span id="RPC_S_PROTSEQ_NOT_FOUND"></span><span id="rpc_s_protseq_not_found"></span>**PROTSEQ de RPC \_ S \_ \_ não \_ encontrado**
</dt> <dd> <dl> <dt>

1744 (0x6D0)
</dt> <dt>



A sequência do Protocolo RPC não foi encontrada.


</dt> </dl> </dd> <dt>

<span id="RPC_S_PROCNUM_OUT_OF_RANGE"></span><span id="rpc_s_procnum_out_of_range"></span>**RPC \_ S \_ PROCNUM \_ fora \_ do \_ intervalo**
</dt> <dd> <dl> <dt>

1745 (0x6D1)
</dt> <dt>



O número do procedimento está fora do intervalo.


</dt> </dl> </dd> <dt>

<span id="RPC_S_BINDING_HAS_NO_AUTH"></span><span id="rpc_s_binding_has_no_auth"></span>**a \_ Associação RPC S \_ \_ \_ não tem \_ autenticação**
</dt> <dd> <dl> <dt>

1746 (0x6D2)
</dt> <dt>



A associação não contém nenhuma informação de autenticação.


</dt> </dl> </dd> <dt>

<span id="RPC_S_UNKNOWN_AUTHN_SERVICE"></span><span id="rpc_s_unknown_authn_service"></span>**\_serviço de \_ \_ autenticação desconhecido RPC \_ S**
</dt> <dd> <dl> <dt>

1747 (0x6D3)
</dt> <dt>



O serviço de autenticação é desconhecido.


</dt> </dl> </dd> <dt>

<span id="RPC_S_UNKNOWN_AUTHN_LEVEL"></span><span id="rpc_s_unknown_authn_level"></span>**\_nível de \_ \_ autenticação desconhecido \_ de RPC S**
</dt> <dd> <dl> <dt>

1748 (0x6D4)
</dt> <dt>



O nível de autenticação é desconhecido.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_AUTH_IDENTITY"></span><span id="rpc_s_invalid_auth_identity"></span>**identidade de autenticação de RPC \_ S \_ inválida \_ \_**
</dt> <dd> <dl> <dt>

1749 (0x6D5)
</dt> <dt>



O contexto de segurança é inválido.


</dt> </dl> </dd> <dt>

<span id="RPC_S_UNKNOWN_AUTHZ_SERVICE"></span><span id="rpc_s_unknown_authz_service"></span>**\_serviço de \_ \_ AUTHZ desconhecido \_ do RPC**
</dt> <dd> <dl> <dt>

1750 (0x6D6)
</dt> <dt>



O serviço de autorização é desconhecido.


</dt> </dl> </dd> <dt>

<span id="EPT_S_INVALID_ENTRY"></span><span id="ept_s_invalid_entry"></span>**EPT \_ S \_ entrada inválida \_**
</dt> <dd> <dl> <dt>

1751 (0x6D7)
</dt> <dt>



A entrada é inválida.


</dt> </dl> </dd> <dt>

<span id="EPT_S_CANT_PERFORM_OP"></span><span id="ept_s_cant_perform_op"></span>**EPT \_ S não \_ consegue \_ executar \_ op**
</dt> <dd> <dl> <dt>

1752 (0x6D8)
</dt> <dt>



O ponto de extremidade do servidor não pode executar a operação.


</dt> </dl> </dd> <dt>

<span id="EPT_S_NOT_REGISTERED"></span><span id="ept_s_not_registered"></span>**EPT \_ S \_ não \_ registrados**
</dt> <dd> <dl> <dt>

1753 (0x6D9)
</dt> <dt>



Não há mais pontos de extremidade disponíveis no mapeador de pontos de extremidades.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NOTHING_TO_EXPORT"></span><span id="rpc_s_nothing_to_export"></span>**\_ \_ nada \_ para \_ Exportar RPC**
</dt> <dd> <dl> <dt>

1754 (0x6DA)
</dt> <dt>



Nenhuma interface foi exportada.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INCOMPLETE_NAME"></span><span id="rpc_s_incomplete_name"></span>**\_ \_ nome incompleto de RPC S \_**
</dt> <dd> <dl> <dt>

1755 (0x6DB)
</dt> <dt>



O nome da entrada está incompleto.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_VERS_OPTION"></span><span id="rpc_s_invalid_vers_option"></span>**\_opção de \_ \_ inversão de RPC S inválida \_**
</dt> <dd> <dl> <dt>

1756 (0x6DC)
</dt> <dt>



A opção de versão é inválida.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_MORE_MEMBERS"></span><span id="rpc_s_no_more_members"></span>**RPC \_ S \_ não \_ mais \_ Membros**
</dt> <dd> <dl> <dt>

1757 (0x6DD)
</dt> <dt>



Não há mais membros.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NOT_ALL_OBJS_UNEXPORTED"></span><span id="rpc_s_not_all_objs_unexported"></span>**RPC \_ S \_ nem \_ todos os \_ objs tivessem não \_ exportados**
</dt> <dd> <dl> <dt>

1758 (0x6DE)
</dt> <dt>



Não há nada para não exportar.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INTERFACE_NOT_FOUND"></span><span id="rpc_s_interface_not_found"></span>**\_interface RPC \_ S \_ não \_ encontrada**
</dt> <dd> <dl> <dt>

1759 (0x6DF)
</dt> <dt>



A interface não foi encontrada.


</dt> </dl> </dd> <dt>

<span id="RPC_S_ENTRY_ALREADY_EXISTS"></span><span id="rpc_s_entry_already_exists"></span>**a \_ entrada de RPC S \_ \_ já \_ existe**
</dt> <dd> <dl> <dt>

1760 (0x6E0)
</dt> <dt>



A entrada já existe.


</dt> </dl> </dd> <dt>

<span id="RPC_S_ENTRY_NOT_FOUND"></span><span id="rpc_s_entry_not_found"></span>**\_entrada RPC \_ S \_ não \_ encontrada**
</dt> <dd> <dl> <dt>

1761 (0x6E1)
</dt> <dt>



A entrada não foi encontrada.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NAME_SERVICE_UNAVAILABLE"></span><span id="rpc_s_name_service_unavailable"></span>**\_serviço de nome RPC S \_ \_ \_ indisponível**
</dt> <dd> <dl> <dt>

1762 (0x6E2)
</dt> <dt>



O serviço de nome não está disponível.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_NAF_ID"></span><span id="rpc_s_invalid_naf_id"></span>**\_ \_ \_ ID NAF inválido do RPC S \_**
</dt> <dd> <dl> <dt>

1763 (0x6E3)
</dt> <dt>



A família de endereços de rede é inválida.


</dt> </dl> </dd> <dt>

<span id="RPC_S_CANNOT_SUPPORT"></span><span id="rpc_s_cannot_support"></span>**\_ \_ não é possível \_ dar suporte a RPC S**
</dt> <dd> <dl> <dt>

1764 (0x6E4)
</dt> <dt>



Não há suporte para a operação solicitada.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_CONTEXT_AVAILABLE"></span><span id="rpc_s_no_context_available"></span>**RPC \_ S \_ nenhum \_ contexto \_ disponível**
</dt> <dd> <dl> <dt>

1765 (0x6E5)
</dt> <dt>



Nenhum contexto de segurança está disponível para permitir a representação.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INTERNAL_ERROR"></span><span id="rpc_s_internal_error"></span>**ERRO INTERNO \_ DO \_ \_ RPC**
</dt> <dd> <dl> <dt>

1766 (0x6E6)
</dt> <dt>



Ocorreu um erro interno em uma RPC (chamada de procedimento remoto).


</dt> </dl> </dd> <dt>

<span id="RPC_S_ZERO_DIVIDE"></span><span id="rpc_s_zero_divide"></span>**RPC \_ S \_ ZERO \_ DIVIDE**
</dt> <dd> <dl> <dt>

1767 (0x6E7)
</dt> <dt>



O servidor RPC tentou uma divisão de inteiros por zero.


</dt> </dl> </dd> <dt>

<span id="RPC_S_ADDRESS_ERROR"></span><span id="rpc_s_address_error"></span>**ERRO DE \_ ENDEREÇO DO \_ \_ RPC**
</dt> <dd> <dl> <dt>

1768 (0x6E8)
</dt> <dt>



Ocorreu um erro de endereçamento no servidor RPC.


</dt> </dl> </dd> <dt>

<span id="RPC_S_FP_DIV_ZERO"></span><span id="rpc_s_fp_div_zero"></span>**RPC \_ S \_ FP \_ DIV \_ ZERO**
</dt> <dd> <dl> <dt>

1769 (0x6E9)
</dt> <dt>



Uma operação de ponto flutuante no servidor RPC causou uma divisão por zero.


</dt> </dl> </dd> <dt>

<span id="RPC_S_FP_UNDERFLOW"></span><span id="rpc_s_fp_underflow"></span>**RPC \_ S \_ FP \_ UNDERFLOW**
</dt> <dd> <dl> <dt>

1770 (0x6EA)
</dt> <dt>



Ocorreu um subfluxo de ponto flutuante no servidor RPC.


</dt> </dl> </dd> <dt>

<span id="RPC_S_FP_OVERFLOW"></span><span id="rpc_s_fp_overflow"></span>**ESTOURO \_ RPC S \_ FP \_**
</dt> <dd> <dl> <dt>

1771 (0x6EB)
</dt> <dt>



Ocorreu um estouro de ponto flutuante no servidor RPC.


</dt> </dl> </dd> <dt>

<span id="RPC_X_NO_MORE_ENTRIES"></span><span id="rpc_x_no_more_entries"></span>**RPC \_ X SEM MAIS \_ \_ \_ ENTRADAS**
</dt> <dd> <dl> <dt>

1772 (0x6EC)
</dt> <dt>



A lista de servidores RPC disponíveis para a associação de alças automáticas foi esgotada.


</dt> </dl> </dd> <dt>

<span id="RPC_X_SS_CHAR_TRANS_OPEN_FAIL"></span><span id="rpc_x_ss_char_trans_open_fail"></span>**FALHA NO RPC \_ X \_ SS \_ CHAR TRANS \_ \_ \_ OPEN**
</dt> <dd> <dl> <dt>

1773 (0x6ED)
</dt> <dt>



Não é possível abrir o arquivo de tabela de conversão de caracteres.


</dt> </dl> </dd> <dt>

<span id="RPC_X_SS_CHAR_TRANS_SHORT_FILE"></span><span id="rpc_x_ss_char_trans_short_file"></span>**RPC \_ X \_ SS \_ CHAR \_ TRANS \_ SHORT \_ FILE**
</dt> <dd> <dl> <dt>

1774 (0x6EE)
</dt> <dt>



O arquivo que contém a tabela de conversão de caracteres tem menos de 512 bytes.


</dt> </dl> </dd> <dt>

<span id="RPC_X_SS_IN_NULL_CONTEXT"></span><span id="rpc_x_ss_in_null_context"></span>**RPC \_ X \_ SS NO CONTEXTO \_ \_ \_ NULO**
</dt> <dd> <dl> <dt>

1775 (0x6EF)
</dt> <dt>



Um handle de contexto nulo foi passado do cliente para o host durante uma chamada de procedimento remoto.


</dt> </dl> </dd> <dt>

<span id="RPC_X_SS_CONTEXT_DAMAGED"></span><span id="rpc_x_ss_context_damaged"></span>**CONTEXTO RPC \_ X \_ SS \_ \_ DANIFICADO**
</dt> <dd> <dl> <dt>

1777 (0x6F1)
</dt> <dt>



O handle de contexto foi alterado durante uma chamada de procedimento remoto.


</dt> </dl> </dd> <dt>

<span id="RPC_X_SS_HANDLES_MISMATCH"></span><span id="rpc_x_ss_handles_mismatch"></span>**RPC \_ X \_ SS LIDA COM \_ \_ INCOMPATIBILIDADE**
</dt> <dd> <dl> <dt>

1778 (0x6F2)
</dt> <dt>



Os alças de associação passados para uma chamada de procedimento remoto não são semelhantes.


</dt> </dl> </dd> <dt>

<span id="RPC_X_SS_CANNOT_GET_CALL_HANDLE"></span><span id="rpc_x_ss_cannot_get_call_handle"></span>**RPC \_ X \_ SS NÃO PODE OBTER O \_ \_ \_ ALÇAMENTO DE \_ CHAMADA**
</dt> <dd> <dl> <dt>

1779 (0x6F3)
</dt> <dt>



O stub não pode obter o alça de chamada de procedimento remoto.


</dt> </dl> </dd> <dt>

<span id="RPC_X_NULL_REF_POINTER"></span><span id="rpc_x_null_ref_pointer"></span>**PONTEIRO REF \_ \_ NULO \_ RPC X \_**
</dt> <dd> <dl> <dt>

1780 (0x6F4)
</dt> <dt>



Um ponteiro de referência nulo foi passado para o stub.


</dt> </dl> </dd> <dt>

<span id="RPC_X_ENUM_VALUE_OUT_OF_RANGE"></span><span id="rpc_x_enum_value_out_of_range"></span>**RPC \_ X \_ VALOR ENUM FORA DO \_ \_ \_ \_ INTERVALO**
</dt> <dd> <dl> <dt>

1781 (0x6F5)
</dt> <dt>



O valor da enumeração está fora do intervalo.


</dt> </dl> </dd> <dt>

<span id="RPC_X_BYTE_COUNT_TOO_SMALL"></span><span id="rpc_x_byte_count_too_small"></span>**CONTAGEM DE BYTE DE RPC \_ X \_ MUITO \_ \_ \_ PEQUENA**
</dt> <dd> <dl> <dt>

1782 (0x6F6)
</dt> <dt>



A contagem de byte é muito pequena.


</dt> </dl> </dd> <dt>

<span id="RPC_X_BAD_STUB_DATA"></span><span id="rpc_x_bad_stub_data"></span>**RPC \_ X DADOS DE \_ \_ STUB \_ RUINS**
</dt> <dd> <dl> <dt>

1783 (0x6F7)
</dt> <dt>



O stub recebeu dados ruins.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_USER_BUFFER"></span><span id="error_invalid_user_buffer"></span>**ERRO \_ BUFFER DE USUÁRIO \_ \_ INVÁLIDO**
</dt> <dd> <dl> <dt>

1784 (0x6F8)
</dt> <dt>



O buffer de usuário fornecido não é válido para a operação solicitada.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNRECOGNIZED_MEDIA"></span><span id="error_unrecognized_media"></span>**ERRO \_ DE MÍDIA NÃO \_ INTERNA**
</dt> <dd> <dl> <dt>

1785 (0x6F9)
</dt> <dt>



A mídia de disco não é reconhecida. Ele pode não ser formatado.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_TRUST_LSA_SECRET"></span><span id="error_no_trust_lsa_secret"></span>**ERRO \_ NENHUM \_ SEGREDO \_ LSA \_ DE CONFIANÇA**
</dt> <dd> <dl> <dt>

1786 (0x6FA)
</dt> <dt>



A estação de trabalho não tem um segredo de confiança.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_TRUST_SAM_ACCOUNT"></span><span id="error_no_trust_sam_account"></span>**ERRO \_ NENHUMA CONTA SAM DE \_ \_ \_ CONFIANÇA**
</dt> <dd> <dl> <dt>

1787 (0x6FB)
</dt> <dt>



O banco de dados de segurança no servidor não tem uma conta de computador para essa relação de confiança de estação de trabalho.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRUSTED_DOMAIN_FAILURE"></span><span id="error_trusted_domain_failure"></span>**ERRO \_ FALHA DE DOMÍNIO \_ \_ CONFIÁVEL**
</dt> <dd> <dl> <dt>

1788 (0x6FC)
</dt> <dt>



Falha na relação de confiança entre o domínio primário e o domínio confiável.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRUSTED_RELATIONSHIP_FAILURE"></span><span id="error_trusted_relationship_failure"></span>**FALHA \_ DE RELAÇÃO CONFIÁVEL DE \_ \_ ERRO**
</dt> <dd> <dl> <dt>

1789 (0x6FD)
</dt> <dt>



A relação de confiança entre esta estação de trabalho e o domínio primário falhou.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRUST_FAILURE"></span><span id="error_trust_failure"></span>**FALHA \_ DE CONFIANÇA DE \_ ERRO**
</dt> <dd> <dl> <dt>

1790 (0x6FE)
</dt> <dt>



Falha no logon de rede.


</dt> </dl> </dd> <dt>

<span id="RPC_S_CALL_IN_PROGRESS"></span><span id="rpc_s_call_in_progress"></span>**CHAMADA \_ RPC S \_ \_ EM \_ ANDAMENTO**
</dt> <dd> <dl> <dt>

1791 (0x6FF)
</dt> <dt>



Uma chamada de procedimento remoto já está em andamento para esse thread.


</dt> </dl> </dd> <dt>

<span id="ERROR_NETLOGON_NOT_STARTED"></span><span id="error_netlogon_not_started"></span>**ERRO \_ NETLOGON \_ NÃO \_ INICIADO**
</dt> <dd> <dl> <dt>

1792 (0x700)
</dt> <dt>



Foi feita uma tentativa de logon, mas o serviço de logon de rede não foi iniciado.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCOUNT_EXPIRED"></span><span id="error_account_expired"></span>**CONTA \_ DE ERRO \_ EXPIRADA**
</dt> <dd> <dl> <dt>

1793 (0x701)
</dt> <dt>



A conta do usuário expirou.


</dt> </dl> </dd> <dt>

<span id="ERROR_REDIRECTOR_HAS_OPEN_HANDLES"></span><span id="error_redirector_has_open_handles"></span>**REDIRECIONADOR \_ DE \_ ERRO TEM \_ \_ ALÇAS ABERTAS**
</dt> <dd> <dl> <dt>

1794 (0x702)
</dt> <dt>



O redirecionador está em uso e não pode ser descarregado.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_DRIVER_ALREADY_INSTALLED"></span><span id="error_printer_driver_already_installed"></span>**DRIVER \_ DE IMPRESSORA DE ERRO JÁ \_ \_ \_ INSTALADO**
</dt> <dd> <dl> <dt>

1795 (0x703)
</dt> <dt>



O driver de impressora especificado já está instalado.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNKNOWN_PORT"></span><span id="error_unknown_port"></span>**ERRO \_ PORTA \_ DESCONHECIDA**
</dt> <dd> <dl> <dt>

1796 (0x704)
</dt> <dt>



A porta especificada é desconhecida.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNKNOWN_PRINTER_DRIVER"></span><span id="error_unknown_printer_driver"></span>**ERRO \_ DRIVER DE IMPRESSORA \_ \_ DESCONHECIDO**
</dt> <dd> <dl> <dt>

1797 (0x705)
</dt> <dt>



O driver de impressora é desconhecido.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNKNOWN_PRINTPROCESSOR"></span><span id="error_unknown_printprocessor"></span>**ERRO \_ \_ PRINTPROCESSOR DESCONHECIDO**
</dt> <dd> <dl> <dt>

1798 (0x706)
</dt> <dt>



O processador de impressão é desconhecido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SEPARATOR_FILE"></span><span id="error_invalid_separator_file"></span>**ERRO \_ ARQUIVO \_ SEPARADOR \_ INVÁLIDO**
</dt> <dd> <dl> <dt>

1799 (0x707)
</dt> <dt>



O arquivo separador especificado é inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PRIORITY"></span><span id="error_invalid_priority"></span>**ERRO \_ de \_ prioridade inválida**
</dt> <dd> <dl> <dt>

1800 (0x708)
</dt> <dt>



A prioridade especificada é inválida.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PRINTER_NAME"></span><span id="error_invalid_printer_name"></span>**\_nome de \_ impressora \_ inválido do erro**
</dt> <dd> <dl> <dt>

1801 (0x709)
</dt> <dt>



O nome da impressora é inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_ALREADY_EXISTS"></span><span id="error_printer_already_exists"></span>**a \_ impressora de erro \_ já \_ existe**
</dt> <dd> <dl> <dt>

1802 (0x70A)
</dt> <dt>



A impressora já existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PRINTER_COMMAND"></span><span id="error_invalid_printer_command"></span>**ERRO \_ de \_ comando de impressora inválido \_**
</dt> <dd> <dl> <dt>

1803 (0x70B)
</dt> <dt>



O comando de impressora é inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DATATYPE"></span><span id="error_invalid_datatype"></span>**ERRO \_ de \_ tipo de dados inválido**
</dt> <dd> <dl> <dt>

1804 (0x70C)
</dt> <dt>



O tipo de dados especificado é inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ENVIRONMENT"></span><span id="error_invalid_environment"></span>**ERRO \_ de \_ ambiente inválido**
</dt> <dd> <dl> <dt>

1805 (0x70D)
</dt> <dt>



O ambiente especificado é inválido.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_MORE_BINDINGS"></span><span id="rpc_s_no_more_bindings"></span>**\_ \_ não há \_ mais \_ associações de RPC**
</dt> <dd> <dl> <dt>

1806 (0x70E)
</dt> <dt>



Não há mais associações.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOLOGON_INTERDOMAIN_TRUST_ACCOUNT"></span><span id="error_nologon_interdomain_trust_account"></span>**ERRO \_ NOlogon da \_ conta de \_ confiança entre domínios \_**
</dt> <dd> <dl> <dt>

1807 (0x70F)
</dt> <dt>



A conta usada é uma conta de confiança entre domínios. Use sua conta de usuário global ou conta de usuário local para acessar este servidor.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOLOGON_WORKSTATION_TRUST_ACCOUNT"></span><span id="error_nologon_workstation_trust_account"></span>**ERRO \_ NOlogon da \_ \_ conta de confiança da estação de trabalho \_**
</dt> <dd> <dl> <dt>

1808 (0x710)
</dt> <dt>



A conta usada é uma conta de computador. Use sua conta de usuário global ou conta de usuário local para acessar este servidor.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOLOGON_SERVER_TRUST_ACCOUNT"></span><span id="error_nologon_server_trust_account"></span>**ERRO \_ NOlogon da \_ \_ conta de confiança do servidor \_**
</dt> <dd> <dl> <dt>

1809 (0x711)
</dt> <dt>



A conta usada é uma conta de confiança do servidor. Use sua conta de usuário global ou conta de usuário local para acessar este servidor.


</dt> </dl> </dd> <dt>

<span id="ERROR_DOMAIN_TRUST_INCONSISTENT"></span><span id="error_domain_trust_inconsistent"></span>**ERRO \_ de \_ confiança de domínio \_ inconsistente**
</dt> <dd> <dl> <dt>

1810 (0x712)
</dt> <dt>



O nome ou a ID de segurança (SID) do domínio especificado é inconsistente com as informações de confiança para esse domínio.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVER_HAS_OPEN_HANDLES"></span><span id="error_server_has_open_handles"></span>**o \_ servidor de erro \_ tem \_ \_ identificadores abertos**
</dt> <dd> <dl> <dt>

1811 (0x713)
</dt> <dt>



O servidor está em uso e não pode ser descarregado.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_DATA_NOT_FOUND"></span><span id="error_resource_data_not_found"></span>**dados de recurso de erro \_ \_ \_ não \_ encontrados**
</dt> <dd> <dl> <dt>

1812 (0x714)
</dt> <dt>



O arquivo de imagem especificado não continha uma seção de recursos.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_TYPE_NOT_FOUND"></span><span id="error_resource_type_not_found"></span>**tipo de recurso de erro \_ \_ \_ não \_ encontrado**
</dt> <dd> <dl> <dt>

1813 (0x715)
</dt> <dt>



O tipo de recurso especificado não pode ser encontrado no arquivo de imagem.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_NAME_NOT_FOUND"></span><span id="error_resource_name_not_found"></span>**nome do recurso de erro \_ \_ \_ não \_ encontrado**
</dt> <dd> <dl> <dt>

1814 (0x716)
</dt> <dt>



O nome do recurso especificado não pode ser encontrado no arquivo de imagem.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_LANG_NOT_FOUND"></span><span id="error_resource_lang_not_found"></span>**LANG de recurso de erro \_ \_ \_ não \_ encontrado**
</dt> <dd> <dl> <dt>

1815 (0x717)
</dt> <dt>



A ID do idioma do recurso especificado não pode ser encontrada no arquivo de imagem.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_ENOUGH_QUOTA"></span><span id="error_not_enough_quota"></span>**ERRO \_ sem \_ \_ cota suficiente**
</dt> <dd> <dl> <dt>

1816 (0x718)
</dt> <dt>



Não há cota suficiente para processar este comando.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_INTERFACES"></span><span id="rpc_s_no_interfaces"></span>**RPC \_ S \_ sem \_ interfaces**
</dt> <dd> <dl> <dt>

1817 (0x719)
</dt> <dt>



Nenhuma interface foi registrada.


</dt> </dl> </dd> <dt>

<span id="RPC_S_CALL_CANCELLED"></span><span id="rpc_s_call_cancelled"></span>**\_chamada RPC \_ S \_ cancelada**
</dt> <dd> <dl> <dt>

1818 (0x71A)
</dt> <dt>



A chamada de procedimento remoto foi cancelada.


</dt> </dl> </dd> <dt>

<span id="RPC_S_BINDING_INCOMPLETE"></span><span id="rpc_s_binding_incomplete"></span>**Associação de RPC \_ S \_ \_ incompleta**
</dt> <dd> <dl> <dt>

1819 (0x71B)
</dt> <dt>



O identificador de associação não contém todas as informações necessárias.


</dt> </dl> </dd> <dt>

<span id="RPC_S_COMM_FAILURE"></span><span id="rpc_s_comm_failure"></span>**falha de comunicação de RPC \_ S \_ \_**
</dt> <dd> <dl> <dt>

1820 (0x71C)
</dt> <dt>



Ocorreu uma falha de comunicação durante uma chamada de procedimento remoto.


</dt> </dl> </dd> <dt>

<span id="RPC_S_UNSUPPORTED_AUTHN_LEVEL"></span><span id="rpc_s_unsupported_authn_level"></span>**nível de autenticação do RPC \_ S \_ sem suporte \_ \_**
</dt> <dd> <dl> <dt>

1821 (0x71D)
</dt> <dt>



Não há suporte para o nível de autenticação solicitado.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_PRINC_NAME"></span><span id="rpc_s_no_princ_name"></span>**\_ \_ não \_ princ \_ nome do RPC**
</dt> <dd> <dl> <dt>

1822 (0x71E)
</dt> <dt>



Nenhum nome de entidade de segurança registrado.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NOT_RPC_ERROR"></span><span id="rpc_s_not_rpc_error"></span>**\_erro RPC S \_ not \_ RPC \_**
</dt> <dd> <dl> <dt>

1823 (0x71F)
</dt> <dt>



o erro especificado não é um código de erro de RPC de Windows válido.


</dt> </dl> </dd> <dt>

<span id="RPC_S_UUID_LOCAL_ONLY"></span><span id="rpc_s_uuid_local_only"></span>**\_ \_ \_ somente local do UUID \_ de RPC S**
</dt> <dd> <dl> <dt>

1824 (0x720)
</dt> <dt>



Um UUID que é válido somente neste computador foi alocado.


</dt> </dl> </dd> <dt>

<span id="RPC_S_SEC_PKG_ERROR"></span><span id="rpc_s_sec_pkg_error"></span>**\_erro de pacote RPC s \_ seg \_ \_**
</dt> <dd> <dl> <dt>

1825 (0x721)
</dt> <dt>



Ocorreu um erro específico do pacote de segurança.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NOT_CANCELLED"></span><span id="rpc_s_not_cancelled"></span>**RPC \_ S \_ não \_ cancelado**
</dt> <dd> <dl> <dt>

1826 (0x722)
</dt> <dt>



O thread não foi cancelado.


</dt> </dl> </dd> <dt>

<span id="RPC_X_INVALID_ES_ACTION"></span><span id="rpc_x_invalid_es_action"></span>**ação de es de RPC \_ X \_ inválido \_ \_**
</dt> <dd> <dl> <dt>

1827 (0x723)
</dt> <dt>



Operação inválida no identificador de codificação/decodificação.


</dt> </dl> </dd> <dt>

<span id="RPC_X_WRONG_ES_VERSION"></span><span id="rpc_x_wrong_es_version"></span>**versão de es de RPC \_ X \_ incorreta \_ \_**
</dt> <dd> <dl> <dt>

1828 (0x724)
</dt> <dt>



Versão incompatível do pacote de serialização.


</dt> </dl> </dd> <dt>

<span id="RPC_X_WRONG_STUB_VERSION"></span><span id="rpc_x_wrong_stub_version"></span>**versão de stub de RPC \_ X \_ incorreta \_ \_**
</dt> <dd> <dl> <dt>

1829 (0x725)
</dt> <dt>



Versão incompatível do stub RPC.


</dt> </dl> </dd> <dt>

<span id="RPC_X_INVALID_PIPE_OBJECT"></span><span id="rpc_x_invalid_pipe_object"></span>**\_objeto de \_ \_ pipe inválido RPC X \_**
</dt> <dd> <dl> <dt>

1830 (0x726)
</dt> <dt>



O objeto de pipe de RPC é inválido ou está corrompido.


</dt> </dl> </dd> <dt>

<span id="RPC_X_WRONG_PIPE_ORDER"></span><span id="rpc_x_wrong_pipe_order"></span>**ordem de pipe de RPC \_ X \_ incorreta \_ \_**
</dt> <dd> <dl> <dt>

1831 (0x727)
</dt> <dt>



Tentativa de operação inválida em um objeto de pipe RPC.


</dt> </dl> </dd> <dt>

<span id="RPC_X_WRONG_PIPE_VERSION"></span><span id="rpc_x_wrong_pipe_version"></span>**\_versão de \_ pipe incorreta de RPC X \_ \_**
</dt> <dd> <dl> <dt>

1832 (0x728)
</dt> <dt>



Versão do pipe RPC sem suporte.


</dt> </dl> </dd> <dt>

<span id="RPC_S_COOKIE_AUTH_FAILED"></span><span id="rpc_s_cookie_auth_failed"></span>**FALHA NA \_ \_ \_ AUTH DO COOKIE RPC S \_**
</dt> <dd> <dl> <dt>

1833 (0x729)
</dt> <dt>



O servidor proxy HTTP rejeitou a conexão porque a autenticação de cookie falhou.


</dt> </dl> </dd> <dt>

<span id="RPC_S_GROUP_MEMBER_NOT_FOUND"></span><span id="rpc_s_group_member_not_found"></span>**MEMBRO DO \_ GRUPO RPC \_ S NÃO \_ \_ \_ ENCONTRADO**
</dt> <dd> <dl> <dt>

1898 (0x76A)
</dt> <dt>



O membro do grupo não foi encontrado.


</dt> </dl> </dd> <dt>

<span id="EPT_S_CANT_CREATE"></span><span id="ept_s_cant_create"></span>**EPT \_ S \_ CANT \_ CREATE**
</dt> <dd> <dl> <dt>

1899 (0x76B)
</dt> <dt>



Não foi possível criar a entrada do banco de dados mapeado do ponto de extremidade.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_OBJECT"></span><span id="rpc_s_invalid_object"></span>**OBJETO INVÁLIDO \_ RPC S \_ \_**
</dt> <dd> <dl> <dt>

1900 (0x76C)
</dt> <dt>



O UUID (identificador exclusivo universal) do objeto é o UUID nulo.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_TIME"></span><span id="error_invalid_time"></span>**HORA \_ INVÁLIDA \_ DO ERRO**
</dt> <dd> <dl> <dt>

1901 (0x76D)
</dt> <dt>



A hora especificada é inválida.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_FORM_NAME"></span><span id="error_invalid_form_name"></span>**ERRO \_ NOME DE FORMULÁRIO \_ \_ INVÁLIDO**
</dt> <dd> <dl> <dt>

1902 (0x76E)
</dt> <dt>



O nome do formulário especificado é inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_FORM_SIZE"></span><span id="error_invalid_form_size"></span>**ERRO \_ TAMANHO DO FORMULÁRIO \_ \_ INVÁLIDO**
</dt> <dd> <dl> <dt>

1903 (0x76F)
</dt> <dt>



O tamanho do formulário especificado é inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALREADY_WAITING"></span><span id="error_already_waiting"></span>**ERRO \_ JÁ \_ AGUARDANDO**
</dt> <dd> <dl> <dt>

1904 (0x770)
</dt> <dt>



A alça de impressora especificada já está sendo aguardada.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_DELETED"></span><span id="error_printer_deleted"></span>**IMPRESSORA \_ DE ERRO \_ EXCLUÍDA**
</dt> <dd> <dl> <dt>

1905 (0x771)
</dt> <dt>



A impressora especificada foi excluída.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PRINTER_STATE"></span><span id="error_invalid_printer_state"></span>**ERRO \_ ESTADO INVÁLIDO DA \_ \_ IMPRESSORA**
</dt> <dd> <dl> <dt>

1906 (0x772)
</dt> <dt>



O estado da impressora é inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_PASSWORD_MUST_CHANGE"></span><span id="error_password_must_change"></span>**A \_ SENHA DE ERRO DEVE SER \_ \_ ALTERE**
</dt> <dd> <dl> <dt>

1907 (0x773)
</dt> <dt>



A senha do usuário deve ser alterada antes de entrar.


</dt> </dl> </dd> <dt>

<span id="ERROR_DOMAIN_CONTROLLER_NOT_FOUND"></span><span id="error_domain_controller_not_found"></span>**ERRO \_ CONTROLADOR DE DOMÍNIO NÃO \_ \_ \_ ENCONTRADO**
</dt> <dd> <dl> <dt>

1908 (0x774)
</dt> <dt>



Não foi possível encontrar o controlador de domínio para esse domínio.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCOUNT_LOCKED_OUT"></span><span id="error_account_locked_out"></span>**CONTA \_ DE ERRO \_ \_ BLOQUEADA**
</dt> <dd> <dl> <dt>

1909 (0x775)
</dt> <dt>



A conta referenciada está bloqueada no momento e pode não estar conectado.


</dt> </dl> </dd> <dt>

<span id="OR_INVALID_OXID"></span><span id="or_invalid_oxid"></span>**OU \_ \_ OXID INVÁLIDO**
</dt> <dd> <dl> <dt>

1910 (0x776)
</dt> <dt>



O exportador de objetos especificado não foi encontrado.


</dt> </dl> </dd> <dt>

<span id="OR_INVALID_OID"></span><span id="or_invalid_oid"></span>**OU \_ \_ OID INVÁLIDO**
</dt> <dd> <dl> <dt>

1911 (0x777)
</dt> <dt>



O objeto especificado não foi encontrado.


</dt> </dl> </dd> <dt>

<span id="OR_INVALID_SET"></span><span id="or_invalid_set"></span>**OU \_ CONJUNTO \_ INVÁLIDO**
</dt> <dd> <dl> <dt>

1912 (0x778)
</dt> <dt>



O conjunto de resolvedor de objetos especificado não foi encontrado.


</dt> </dl> </dd> <dt>

<span id="RPC_S_SEND_INCOMPLETE"></span><span id="rpc_s_send_incomplete"></span>**RPC \_ S \_ SEND \_ INCOMPLETE**
</dt> <dd> <dl> <dt>

1913 (0x779)
</dt> <dt>



Alguns dados permanecem a ser enviados no buffer de solicitação.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_ASYNC_HANDLE"></span><span id="rpc_s_invalid_async_handle"></span>**RPC \_ S \_ INVALID \_ ASYNC \_ HANDLE**
</dt> <dd> <dl> <dt>

1914 (0x77A)
</dt> <dt>



Handle de chamada de procedimento remoto assíncrono inválido.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_ASYNC_CALL"></span><span id="rpc_s_invalid_async_call"></span>**RPC \_ S \_ CHAMADA \_ ASSÍNCRONA \_ INVÁLIDA**
</dt> <dd> <dl> <dt>

1915 (0x77B)
</dt> <dt>



Alça de chamada RPC assíncrona inválida para esta operação.


</dt> </dl> </dd> <dt>

<span id="RPC_X_PIPE_CLOSED"></span><span id="rpc_x_pipe_closed"></span>**PIPE RPC \_ X \_ \_ FECHADO**
</dt> <dd> <dl> <dt>

1916 (0x77C)
</dt> <dt>



O objeto de pipe RPC já foi fechado.


</dt> </dl> </dd> <dt>

<span id="RPC_X_PIPE_DISCIPLINE_ERROR"></span><span id="rpc_x_pipe_discipline_error"></span>**ERRO DE DISCIPLINA DE PIPE DE RPC \_ X \_ \_ \_**
</dt> <dd> <dl> <dt>

1917 (0x77D)
</dt> <dt>



A chamada RPC foi concluída antes que todos os pipes fossem processados.


</dt> </dl> </dd> <dt>

<span id="RPC_X_PIPE_EMPTY"></span><span id="rpc_x_pipe_empty"></span>**PIPE \_ RPC X \_ \_ VAZIO**
</dt> <dd> <dl> <dt>

1918 (0x77E)
</dt> <dt>



Não há mais dados disponíveis no pipe RPC.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SITENAME"></span><span id="error_no_sitename"></span>**ERRO \_ SEM NOME DO \_ SITE**
</dt> <dd> <dl> <dt>

1919 (0x77F)
</dt> <dt>



Nenhum nome de site está disponível para este computador.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_ACCESS_FILE"></span><span id="error_cant_access_file"></span>**ERRO \_ NÃO PODE ACESSAR O \_ \_ ARQUIVO**
</dt> <dd> <dl> <dt>

1920 (0x780)
</dt> <dt>



O arquivo não pode ser acessado pelo sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_RESOLVE_FILENAME"></span><span id="error_cant_resolve_filename"></span>**ERRO \_ NÃO É POSSÍVEL RESOLVER \_ \_ FILENAME**
</dt> <dd> <dl> <dt>

1921 (0x781)
</dt> <dt>



O nome do arquivo não pode ser resolvido pelo sistema.


</dt> </dl> </dd> <dt>

<span id="RPC_S_ENTRY_TYPE_MISMATCH"></span><span id="rpc_s_entry_type_mismatch"></span>**INCOMPATIBILIDADE \_ DO TIPO DE ENTRADA \_ \_ \_ RPC S**
</dt> <dd> <dl> <dt>

1922 (0x782)
</dt> <dt>



A entrada não é do tipo esperado.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NOT_ALL_OBJS_EXPORTED"></span><span id="rpc_s_not_all_objs_exported"></span>**RPC \_ S NEM TODOS OS \_ \_ \_ OBJS \_ EXPORTADOS**
</dt> <dd> <dl> <dt>

1923 (0x783)
</dt> <dt>



Nem todos os UUIDs de objeto podem ser exportados para a entrada especificada.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INTERFACE_NOT_EXPORTED"></span><span id="rpc_s_interface_not_exported"></span>**INTERFACE \_ RPC \_ NÃO \_ \_ EXPORTADA**
</dt> <dd> <dl> <dt>

1924 (0x784)
</dt> <dt>



Não foi possível exportar a interface para a entrada especificada.


</dt> </dl> </dd> <dt>

<span id="RPC_S_PROFILE_NOT_ADDED"></span><span id="rpc_s_profile_not_added"></span>**PERFIL RPC \_ S \_ NÃO \_ \_ ADICIONADO**
</dt> <dd> <dl> <dt>

1925 (0x785)
</dt> <dt>



Não foi possível adicionar a entrada de perfil especificada.


</dt> </dl> </dd> <dt>

<span id="RPC_S_PRF_ELT_NOT_ADDED"></span><span id="rpc_s_prf_elt_not_added"></span>**RPC \_ S \_ PRF \_ ELT NÃO \_ \_ ADICIONADO**
</dt> <dd> <dl> <dt>

1926 (0x786)
</dt> <dt>



Não foi possível adicionar o elemento de perfil especificado.


</dt> </dl> </dd> <dt>

<span id="RPC_S_PRF_ELT_NOT_REMOVED"></span><span id="rpc_s_prf_elt_not_removed"></span>**RPC \_ S \_ PRF \_ ELT NÃO \_ \_ REMOVIDO**
</dt> <dd> <dl> <dt>

1927 (0x787)
</dt> <dt>



Não foi possível remover o elemento de perfil especificado.


</dt> </dl> </dd> <dt>

<span id="RPC_S_GRP_ELT_NOT_ADDED"></span><span id="rpc_s_grp_elt_not_added"></span>**RPC \_ S \_ GRP \_ ELT NÃO \_ \_ ADICIONADO**
</dt> <dd> <dl> <dt>

1928 (0x788)
</dt> <dt>



Não foi possível adicionar o elemento group.


</dt> </dl> </dd> <dt>

<span id="RPC_S_GRP_ELT_NOT_REMOVED"></span><span id="rpc_s_grp_elt_not_removed"></span>**RPC \_ S \_ GRP \_ ELT NÃO \_ \_ REMOVIDO**
</dt> <dd> <dl> <dt>

1929 (0x789)
</dt> <dt>



O elemento group não pôde ser removido.


</dt> </dl> </dd> <dt>

<span id="ERROR_KM_DRIVER_BLOCKED"></span><span id="error_km_driver_blocked"></span>**DRIVER \_ KM DE ERRO \_ \_ BLOQUEADO**
</dt> <dd> <dl> <dt>

1930 (0x78A)
</dt> <dt>



O driver de impressora não é compatível com uma política habilitada no computador que bloqueia os drivers NT 4.0.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONTEXT_EXPIRED"></span><span id="error_context_expired"></span>**CONTEXTO \_ DE \_ ERRO EXPIRADO**
</dt> <dd> <dl> <dt>

1931 (0x78B)
</dt> <dt>



O contexto expirou e não pode mais ser usado.


</dt> </dl> </dd> <dt>

<span id="ERROR_PER_USER_TRUST_QUOTA_EXCEEDED"></span><span id="error_per_user_trust_quota_exceeded"></span>**ERRO \_ POR COTA DE CONFIANÇA DO USUÁRIO \_ \_ \_ \_ EXCEDIDO**
</dt> <dd> <dl> <dt>

1932 (0x78C)
</dt> <dt>



A cota de criação de confiança delegada do usuário atual foi excedida.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALL_USER_TRUST_QUOTA_EXCEEDED"></span><span id="error_all_user_trust_quota_exceeded"></span>**ERRO \_ TODAS AS \_ \_ COTAS DE CONFIANÇA DO USUÁRIO \_ \_ EXCEDIDA**
</dt> <dd> <dl> <dt>

1933 (0x78D)
</dt> <dt>



A cota total de criação de confiança delegada foi excedida.


</dt> </dl> </dd> <dt>

<span id="ERROR_USER_DELETE_TRUST_QUOTA_EXCEEDED"></span><span id="error_user_delete_trust_quota_exceeded"></span>**ERRO \_ A COTA DE CONFIANÇA DE \_ \_ \_ EXCLUSÃO DO USUÁRIO \_ EXCEDIDA**
</dt> <dd> <dl> <dt>

1934 (0x78E)
</dt> <dt>



A cota de exclusão de confiança delegada do usuário atual foi excedida.


</dt> </dl> </dd> <dt>

<span id="ERROR_AUTHENTICATION_FIREWALL_FAILED"></span><span id="error_authentication_firewall_failed"></span>**FALHA NO \_ FIREWALL DE \_ \_ AUTENTICAÇÃO DE ERRO**
</dt> <dd> <dl> <dt>

1935 (0x78F)
</dt> <dt>



O computador em que você está entrando é protegido por um firewall de autenticação. A conta especificada não tem permissão para autenticar no computador.


</dt> </dl> </dd> <dt>

<span id="ERROR_REMOTE_PRINT_CONNECTIONS_BLOCKED"></span><span id="error_remote_print_connections_blocked"></span>**ERRO \_ CONEXÕES DE \_ IMPRESSÃO REMOTA \_ \_ BLOQUEADAS**
</dt> <dd> <dl> <dt>

1936 (0x790)
</dt> <dt>



As conexões remotas com o Spooler de Impressão são bloqueadas por um conjunto de políticas em seu computador.


</dt> </dl> </dd> <dt>

<span id="ERROR_NTLM_BLOCKED"></span><span id="error_ntlm_blocked"></span>**ERRO \_ NTLM \_ BLOQUEADO**
</dt> <dd> <dl> <dt>

1937 (0x791)
</dt> <dt>



Falha na autenticação porque a autenticação NTLM foi desabilitada.


</dt> </dl> </dd> <dt>

<span id="ERROR_PASSWORD_CHANGE_REQUIRED"></span><span id="error_password_change_required"></span>**ALTERAÇÃO \_ DE SENHA DE ERRO \_ \_ NECESSÁRIA**
</dt> <dd> <dl> <dt>

1938 (0x792)
</dt> <dt>



Falha de logon: a política de EAS requer que o usuário altere sua senha antes que essa operação possa ser executada.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PIXEL_FORMAT"></span><span id="error_invalid_pixel_format"></span>**ERRO \_ FORMATO DE PIXEL \_ \_ INVÁLIDO**
</dt> <dd> <dl> <dt>

2000 (0x7D0)
</dt> <dt>



O formato de pixel é inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_DRIVER"></span><span id="error_bad_driver"></span>**ERRO \_ DE \_ DRIVER RUIM**
</dt> <dd> <dl> <dt>

2001 (0x7D1)
</dt> <dt>



O driver especificado é inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_WINDOW_STYLE"></span><span id="error_invalid_window_style"></span>**ERRO \_ ESTILO DE JANELA \_ \_ INVÁLIDO**
</dt> <dd> <dl> <dt>

2002 (0x7D2)
</dt> <dt>



O atributo de classe ou estilo de janela é inválido para esta operação.


</dt> </dl> </dd> <dt>

<span id="ERROR_METAFILE_NOT_SUPPORTED"></span><span id="error_metafile_not_supported"></span>**NÃO \_ HÁ SUPORTE PARA \_ \_ METADADOS DE ERRO**
</dt> <dd> <dl> <dt>

2003 (0x7D3)
</dt> <dt>



Não há suporte para a operação de metadados solicitada.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSFORM_NOT_SUPPORTED"></span><span id="error_transform_not_supported"></span>**TRANSFORMAÇÃO \_ DE ERRO SEM \_ \_ SUPORTE**
</dt> <dd> <dl> <dt>

2004 (0x7D4)
</dt> <dt>



Não há suporte para a operação de transformação solicitada.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLIPPING_NOT_SUPPORTED"></span><span id="error_clipping_not_supported"></span>**NÃO \_ HÁ SUPORTE PARA RECORTE DE \_ \_ ERRO**
</dt> <dd> <dl> <dt>

2005 (0x7D5)
</dt> <dt>



Não há suporte para a operação de recorte solicitada.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_CMM"></span><span id="error_invalid_cmm"></span>**ERRO \_ \_ CMM INVÁLIDO**
</dt> <dd> <dl> <dt>

2010 (0x7DA)
</dt> <dt>



O módulo de gerenciamento de cores especificado é inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PROFILE"></span><span id="error_invalid_profile"></span>**ERRO \_ PERFIL \_ INVÁLIDO**
</dt> <dd> <dl> <dt>

2011 (0x7DB)
</dt> <dt>



O perfil de cor especificado é inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_TAG_NOT_FOUND"></span><span id="error_tag_not_found"></span>**MARCA \_ DE ERRO NÃO \_ \_ ENCONTRADA**
</dt> <dd> <dl> <dt>

2012 (0x7DC)
</dt> <dt>



A marca especificada não foi encontrada.


</dt> </dl> </dd> <dt>

<span id="ERROR_TAG_NOT_PRESENT"></span><span id="error_tag_not_present"></span>**MARCA \_ DE ERRO NÃO \_ \_ PRESENTE**
</dt> <dd> <dl> <dt>

2013 (0x7DD)
</dt> <dt>



Uma marca necessária não está presente.


</dt> </dl> </dd> <dt>

<span id="ERROR_DUPLICATE_TAG"></span><span id="error_duplicate_tag"></span>**MARCAÇÃO \_ \_ DUPLICADA DE ERRO**
</dt> <dd> <dl> <dt>

2014 (0x7DE)
</dt> <dt>



A marca especificada já está presente.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROFILE_NOT_ASSOCIATED_WITH_DEVICE"></span><span id="error_profile_not_associated_with_device"></span>**PERFIL \_ DE ERRO NÃO ASSOCIADO AO \_ \_ \_ \_ DISPOSITIVO**
</dt> <dd> <dl> <dt>

2015 (0x7DF)
</dt> <dt>



O perfil de cor especificado não está associado ao dispositivo especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROFILE_NOT_FOUND"></span><span id="error_profile_not_found"></span>**PERFIL \_ DE ERRO NÃO \_ \_ ENCONTRADO**
</dt> <dd> <dl> <dt>

2016 (0x7E0)
</dt> <dt>



O perfil de cor especificado não foi encontrado.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_COLORSPACE"></span><span id="error_invalid_colorspace"></span>**ERRO \_ \_ COLORSPACE INVÁLIDO**
</dt> <dd> <dl> <dt>

2017 (0x7E1)
</dt> <dt>



O espaço de cores especificado é inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_ICM_NOT_ENABLED"></span><span id="error_icm_not_enabled"></span>**ERRO \_ ICM \_ NÃO \_ HABILITADO**
</dt> <dd> <dl> <dt>

2018 (0x7E2)
</dt> <dt>



O Gerenciamento de Cores da Imagem não está habilitado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DELETING_ICM_XFORM"></span><span id="error_deleting_icm_xform"></span>**ERRO \_ AO EXCLUIR ICM \_ \_ XFORM**
</dt> <dd> <dl> <dt>

2019 (0x7E3)
</dt> <dt>



Ocorreu um erro ao excluir a transformação de cor.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_TRANSFORM"></span><span id="error_invalid_transform"></span>**ERRO \_ TRANSFORMAÇÃO \_ INVÁLIDA**
</dt> <dd> <dl> <dt>

2020 (0x7E4)
</dt> <dt>



A transformação de cor especificada é inválida.


</dt> </dl> </dd> <dt>

<span id="ERROR_COLORSPACE_MISMATCH"></span><span id="error_colorspace_mismatch"></span>**ERRO \_ INCOMPATIBILIDADE DE COLORSPACE \_**
</dt> <dd> <dl> <dt>

2021 (0x7E5)
</dt> <dt>



A transformação especificada não corresponderá ao espaço de cores do bitmap.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_COLORINDEX"></span><span id="error_invalid_colorindex"></span>**ERRO \_ \_ COLORINDEX INVÁLIDO**
</dt> <dd> <dl> <dt>

2022 (0x7E6)
</dt> <dt>



O índice de cores nomeado especificado não está presente no perfil.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROFILE_DOES_NOT_MATCH_DEVICE"></span><span id="error_profile_does_not_match_device"></span>**O \_ PERFIL DE ERRO NÃO COMBINA COM O \_ \_ \_ \_ DISPOSITIVO**
</dt> <dd> <dl> <dt>

2023 (0x7E7)
</dt> <dt>



O perfil especificado destina-se a um dispositivo de um tipo diferente do dispositivo especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONNECTED_OTHER_PASSWORD"></span><span id="error_connected_other_password"></span>**ERRO \_ OUTRA \_ SENHA \_ CONECTADA**
</dt> <dd> <dl> <dt>

2108 (0x83C)
</dt> <dt>



A conexão de rede foi feita com êxito, mas o usuário precisou solicitar uma senha diferente da especificada originalmente.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONNECTED_OTHER_PASSWORD_DEFAULT"></span><span id="error_connected_other_password_default"></span>**ERRO \_ CONECTADO PADRÃO DE OUTRA \_ \_ \_ SENHA**
</dt> <dd> <dl> <dt>

2109 (0x83D)
</dt> <dt>



A conexão de rede foi feita com êxito usando as credenciais padrão.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_USERNAME"></span><span id="error_bad_username"></span>**ERRO NOME \_ DE USUÁRIO \_ RUIM**
</dt> <dd> <dl> <dt>

2202 (0x89A)
</dt> <dt>



O nome de usuário especificado é inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_CONNECTED"></span><span id="error_not_connected"></span>**ERRO \_ NÃO \_ CONECTADO**
</dt> <dd> <dl> <dt>

2250 (0x8CA)
</dt> <dt>



Esta conexão de rede não existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_OPEN_FILES"></span><span id="error_open_files"></span>**ERRO ao \_ abrir \_ arquivos**
</dt> <dd> <dl> <dt>

2401 (0x961)
</dt> <dt>



Esta conexão de rede tem arquivos abertos ou solicitações pendentes.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACTIVE_CONNECTIONS"></span><span id="error_active_connections"></span>**\_conexões ativas de erro \_**
</dt> <dd> <dl> <dt>

2402 (0x962)
</dt> <dt>



As conexões ativas ainda existem.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_IN_USE"></span><span id="error_device_in_use"></span>**\_dispositivo \_ de erro em \_ uso**
</dt> <dd> <dl> <dt>

2404 (0x964)
</dt> <dt>



O dispositivo está em uso por um processo ativo e não pode ser desconectado.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNKNOWN_PRINT_MONITOR"></span><span id="error_unknown_print_monitor"></span>**MONITOR de impressão de erro \_ desconhecido \_ \_**
</dt> <dd> <dl> <dt>

3000 (0xBB8)
</dt> <dt>



O monitor de impressão especificado é desconhecido.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_DRIVER_IN_USE"></span><span id="error_printer_driver_in_use"></span>**ERRO \_ \_ de driver \_ de impressora em \_ uso**
</dt> <dd> <dl> <dt>

3001 (0xBB9)
</dt> <dt>



O driver de impressora especificado está em uso no momento.


</dt> </dl> </dd> <dt>

<span id="ERROR_SPOOL_FILE_NOT_FOUND"></span><span id="error_spool_file_not_found"></span>**ERRO \_ de \_ arquivo de spool \_ não \_ encontrado**
</dt> <dd> <dl> <dt>

3002 (0xBBA)
</dt> <dt>



O arquivo de spool não foi encontrado.


</dt> </dl> </dd> <dt>

<span id="ERROR_SPL_NO_STARTDOC"></span><span id="error_spl_no_startdoc"></span>**ERRO \_ SPL \_ \_ StartDoc**
</dt> <dd> <dl> <dt>

3003 (0xBBB)
</dt> <dt>



Uma chamada StartDocPrinter não foi emitida.


</dt> </dl> </dd> <dt>

<span id="ERROR_SPL_NO_ADDJOB"></span><span id="error_spl_no_addjob"></span>**ERRO \_ SPL \_ \_ ADDJOB**
</dt> <dd> <dl> <dt>

3004 (0xBBC)
</dt> <dt>



Uma chamada AddJob não foi emitida.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINT_PROCESSOR_ALREADY_INSTALLED"></span><span id="error_print_processor_already_installed"></span>**ERRO \_ o \_ processador de impressão \_ já está \_ instalado**
</dt> <dd> <dl> <dt>

3005 (0xBBD)
</dt> <dt>



O processador de impressão especificado já foi instalado.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINT_MONITOR_ALREADY_INSTALLED"></span><span id="error_print_monitor_already_installed"></span>**o \_ Monitor de impressão de erro \_ \_ já está \_ instalado**
</dt> <dd> <dl> <dt>

3006 (0xBBE)
</dt> <dt>



O monitor de impressão especificado já foi instalado.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PRINT_MONITOR"></span><span id="error_invalid_print_monitor"></span>**ERRO \_ de \_ Monitor de impressão inválido \_**
</dt> <dd> <dl> <dt>

3007 (0xBBF)
</dt> <dt>



O monitor de impressão especificado não tem as funções necessárias.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINT_MONITOR_IN_USE"></span><span id="error_print_monitor_in_use"></span>**ERRO \_ \_ no monitor \_ de impressão em \_ uso**
</dt> <dd> <dl> <dt>

3008 (0xBC0)
</dt> <dt>



O monitor de impressão especificado está em uso no momento.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_HAS_JOBS_QUEUED"></span><span id="error_printer_has_jobs_queued"></span>**a \_ impressora de erro \_ tem \_ trabalhos em \_ fila**
</dt> <dd> <dl> <dt>

3009 (0xBC1)
</dt> <dt>



A operação solicitada não é permitida quando há trabalhos na fila para a impressora.


</dt> </dl> </dd> <dt>

<span id="ERROR_SUCCESS_REBOOT_REQUIRED"></span><span id="error_success_reboot_required"></span>**ERRO \_ de \_ reinicialização bem-sucedida \_ necessária**
</dt> <dd> <dl> <dt>

3010 (0xBC2)
</dt> <dt>



A operação solicitada foi bem-sucedida. As alterações não entrarão em vigor até que o sistema seja reinicializado.


</dt> </dl> </dd> <dt>

<span id="ERROR_SUCCESS_RESTART_REQUIRED"></span><span id="error_success_restart_required"></span>**ERRO \_ de \_ reinicialização bem-sucedida \_ necessária**
</dt> <dd> <dl> <dt>

3011 (0xBC3)
</dt> <dt>



A operação solicitada foi bem-sucedida. As alterações não entrarão em vigor até que o serviço seja reiniciado.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_NOT_FOUND"></span><span id="error_printer_not_found"></span>**impressora de erro \_ \_ não \_ encontrada**
</dt> <dd> <dl> <dt>

3012 (0xBC4)
</dt> <dt>



Nenhuma impressora encontrada.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_DRIVER_WARNED"></span><span id="error_printer_driver_warned"></span>**ERRO \_ de \_ Driver de impressora \_ avisado**
</dt> <dd> <dl> <dt>

3013 (0xBC5)
</dt> <dt>



O driver de impressora é conhecido como não confiável.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_DRIVER_BLOCKED"></span><span id="error_printer_driver_blocked"></span>**Driver de impressora de erro \_ \_ \_ bloqueado**
</dt> <dd> <dl> <dt>

3014 (0xBC6)
</dt> <dt>



O driver de impressora é conhecido por prejudicar o sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_DRIVER_PACKAGE_IN_USE"></span><span id="error_printer_driver_package_in_use"></span>**ERRO \_ \_ \_ \_ de pacote de driver de impressora em \_ uso**
</dt> <dd> <dl> <dt>

3015 (0xBC7)
</dt> <dt>



O pacote de driver de impressora especificado está em uso no momento.


</dt> </dl> </dd> <dt>

<span id="ERROR_CORE_DRIVER_PACKAGE_NOT_FOUND"></span><span id="error_core_driver_package_not_found"></span>**pacote de driver de núcleo de erro \_ \_ \_ \_ não \_ encontrado**
</dt> <dd> <dl> <dt>

3016 (0xBC8)
</dt> <dt>



Não é possível encontrar um pacote de driver principal exigido pelo pacote de driver de impressora.


</dt> </dl> </dd> <dt>

<span id="ERROR_FAIL_REBOOT_REQUIRED"></span><span id="error_fail_reboot_required"></span>**ERRO \_ falha na \_ reinicialização \_ necessária**
</dt> <dd> <dl> <dt>

3017 (0xBC9)
</dt> <dt>



A operação solicitada falhou. Uma reinicialização do sistema é necessária para reverter as alterações feitas.


</dt> </dl> </dd> <dt>

<span id="ERROR_FAIL_REBOOT_INITIATED"></span><span id="error_fail_reboot_initiated"></span>**ERRO \_ de \_ reinicialização \_ iniciada**
</dt> <dd> <dl> <dt>

3018 (0xBCA)
</dt> <dt>



A operação solicitada falhou. Uma reinicialização do sistema foi iniciada para reverter as alterações feitas.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_DRIVER_DOWNLOAD_NEEDED"></span><span id="error_printer_driver_download_needed"></span>**ERRO \_ de \_ download de driver de impressora \_ \_ necessário**
</dt> <dd> <dl> <dt>

3019 (0xBCB)
</dt> <dt>



O driver de impressora especificado não foi encontrado no sistema e precisa ser baixado.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINT_JOB_RESTART_REQUIRED"></span><span id="error_print_job_restart_required"></span>**ERRO \_ de \_ reinicialização do trabalho de impressão \_ \_ necessário**
</dt> <dd> <dl> <dt>

3020 (0xBCC)
</dt> <dt>



Falha ao imprimir o trabalho de impressão solicitado. Uma atualização do sistema de impressão requer que o trabalho seja reenviado.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PRINTER_DRIVER_MANIFEST"></span><span id="error_invalid_printer_driver_manifest"></span>**ERRO \_ de \_ \_ manifesto de driver de impressora inválido \_**
</dt> <dd> <dl> <dt>

3021 (0xBCD)
</dt> <dt>



O driver de impressora não contém um manifesto válido ou contém muitos manifestos.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_NOT_SHAREABLE"></span><span id="error_printer_not_shareable"></span>**ERRO de \_ impressora \_ não \_ compartilhável**
</dt> <dd> <dl> <dt>

3022 (0xBCE)
</dt> <dt>



A impressora especificada não pode ser compartilhada.


</dt> </dl> </dd> <dt>

<span id="ERROR_REQUEST_PAUSED"></span><span id="error_request_paused"></span>**solicitação de erro \_ \_ pausada**
</dt> <dd> <dl> <dt>

3050 (0xBEA)
</dt> <dt>



A operação foi pausada.


</dt> </dl> </dd> <dt>

<span id="ERROR_IO_REISSUE_AS_CACHED"></span><span id="error_io_reissue_as_cached"></span>**ERRO \_ \_ de reemissão de e/s \_ como \_ em cache**
</dt> <dd> <dl> <dt>

3950 (0xF6E)
</dt> <dt>



Emita novamente a operação especificada como uma operação de e/s em cache.


</dt> </dl> </dd> </dl>


## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>WinError. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Códigos de erro do sistema](system-error-codes.md)
</dt> </dl>

 

 




