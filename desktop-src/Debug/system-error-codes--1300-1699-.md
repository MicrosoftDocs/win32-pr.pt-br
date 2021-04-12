---
description: Descreve os códigos de erro 1300-1699 definidos no arquivo de cabeçalho WinError. h e destina-se a desenvolvedores.
ms.assetid: 7b04a2ba-7bf9-4bff-93c8-cbb0060e069d
title: Códigos de erro do sistema (1300-1699) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 8fa0cbc312c8d82879322f0bc0c79533ddb961ce
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457024"
---
# <a name="system-error-codes-1300-1699"></a>Códigos de erro do sistema (1300-1699)

> [!NOTE]
> Essas informações destinam-se a desenvolvedores Depurando erros do sistema. Para outros erros, como problemas com Windows Update, há uma lista de recursos na página códigos de [erro](system-error-codes.md) .

A lista a seguir descreve os [códigos de erro do sistema](system-error-codes.md) para erros 1300 a 1699. Elas são retornadas pela função [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) quando muitas funções falham. Para recuperar o texto de descrição do erro em seu aplicativo, use a função [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) com a **mensagem de formato \_ \_ do sinalizador do \_ sistema** .

<dl> <dt>

<span id="ERROR_NOT_ALL_ASSIGNED"></span><span id="error_not_all_assigned"></span>**ERRO \_ nem \_ todos \_ atribuídos**
</dt> <dd> <dl> <dt>

1300 (0x514)
</dt> <dt>



Nem todos os privilégios ou grupos referenciados são atribuídos ao chamador.


</dt> </dl> </dd> <dt>

<span id="ERROR_SOME_NOT_MAPPED"></span><span id="error_some_not_mapped"></span>**ERRO \_ algum \_ não \_ mapeado**
</dt> <dd> <dl> <dt>

1301 (0x515)
</dt> <dt>



Não foi feito um mapeamento entre os nomes de conta e as IDs de segurança.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_QUOTAS_FOR_ACCOUNT"></span><span id="error_no_quotas_for_account"></span>**ERRO \_ sem \_ cotas \_ para a \_ conta**
</dt> <dd> <dl> <dt>

1302 (0x516)
</dt> <dt>



Nenhum limite de cota de sistema é definido especificamente para essa conta.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOCAL_USER_SESSION_KEY"></span><span id="error_local_user_session_key"></span>**ERRO \_ de \_ \_ chave de sessão de usuário local \_**
</dt> <dd> <dl> <dt>

1303 (0x517)
</dt> <dt>



Nenhuma chave de criptografia está disponível. Uma chave de criptografia bem conhecida foi retornada.


</dt> </dl> </dd> <dt>

<span id="ERROR_NULL_LM_PASSWORD"></span><span id="error_null_lm_password"></span>**ERRO \_ de \_ senha LM nula \_**
</dt> <dd> <dl> <dt>

1304 (0x518)
</dt> <dt>



A senha é muito complexa para ser convertida em uma senha do Gerenciador de LAN. A senha do Gerenciador de LAN retornada é uma cadeia de caracteres **nula** .


</dt> </dl> </dd> <dt>

<span id="ERROR_UNKNOWN_REVISION"></span><span id="error_unknown_revision"></span>**revisão de erro \_ desconhecida \_**
</dt> <dd> <dl> <dt>

1305 (0x519)
</dt> <dt>



O nível de revisão é desconhecido.


</dt> </dl> </dd> <dt>

<span id="ERROR_REVISION_MISMATCH"></span><span id="error_revision_mismatch"></span>**incompatibilidade de revisão de erro \_ \_**
</dt> <dd> <dl> <dt>

1306 (0x51A)
</dt> <dt>



Indica que dois níveis de revisão são incompatíveis.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_OWNER"></span><span id="error_invalid_owner"></span>**\_proprietário inválido do erro \_**
</dt> <dd> <dl> <dt>

1307 (0x51B)
</dt> <dt>



Esta ID de segurança não pode ser atribuída como o proprietário deste objeto.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PRIMARY_GROUP"></span><span id="error_invalid_primary_group"></span>**ERRO \_ de \_ grupo primário inválido \_**
</dt> <dd> <dl> <dt>

1308 (0x51C)
</dt> <dt>



Essa ID de segurança não pode ser atribuída como o grupo primário de um objeto.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_IMPERSONATION_TOKEN"></span><span id="error_no_impersonation_token"></span>**ERRO \_ sem \_ token de representação \_**
</dt> <dd> <dl> <dt>

1309 (0x51D)
</dt> <dt>



Foi feita uma tentativa de operar em um token de representação por um thread que não está representando um cliente no momento.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_DISABLE_MANDATORY"></span><span id="error_cant_disable_mandatory"></span>**ERRO não é possível \_ \_ desabilitar \_ obrigatório**
</dt> <dd> <dl> <dt>

1310 (0x51E)
</dt> <dt>



O grupo pode não estar desabilitado.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_LOGON_SERVERS"></span><span id="error_no_logon_servers"></span>**ERRO \_ sem \_ servidores de logon \_**
</dt> <dd> <dl> <dt>

1311 (0x51F)
</dt> <dt>



No momento, não há servidores de logon disponíveis para atender à solicitação de logon.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUCH_LOGON_SESSION"></span><span id="error_no_such_logon_session"></span>**ERRO \_ sem \_ \_ sessão de logon \_**
</dt> <dd> <dl> <dt>

1312 (0x520)
</dt> <dt>



Uma sessão de logon especificada não existe. Ele pode já ter sido encerrado.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUCH_PRIVILEGE"></span><span id="error_no_such_privilege"></span>**ERRO \_ sem \_ esse \_ privilégio**
</dt> <dd> <dl> <dt>

1313 (0x521)
</dt> <dt>



Um privilégio especificado não existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRIVILEGE_NOT_HELD"></span><span id="error_privilege_not_held"></span>**privilégio de erro \_ \_ não \_ mantido**
</dt> <dd> <dl> <dt>

1314 (0x522)
</dt> <dt>



O cliente não possui o privilégio exigido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ACCOUNT_NAME"></span><span id="error_invalid_account_name"></span>**\_nome de \_ conta \_ inválido do erro**
</dt> <dd> <dl> <dt>

1315 (0x523)
</dt> <dt>



O nome fornecido não é um nome de conta formado corretamente.


</dt> </dl> </dd> <dt>

<span id="ERROR_USER_EXISTS"></span><span id="error_user_exists"></span>**ERRO o \_ usuário \_ existe**
</dt> <dd> <dl> <dt>

1316 (0x524)
</dt> <dt>



A conta especificada já existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUCH_USER"></span><span id="error_no_such_user"></span>**ERRO \_ não é \_ desse \_ usuário**
</dt> <dd> <dl> <dt>

1317 (0x525)
</dt> <dt>



A conta especificada não existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_GROUP_EXISTS"></span><span id="error_group_exists"></span>**o \_ grupo de erros \_ existe**
</dt> <dd> <dl> <dt>

1318 (0x526)
</dt> <dt>



O grupo especificado já existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUCH_GROUP"></span><span id="error_no_such_group"></span>**ERRO \_ não \_ existe \_ grupo**
</dt> <dd> <dl> <dt>

1319 (0x527)
</dt> <dt>



O grupo especificado não existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_MEMBER_IN_GROUP"></span><span id="error_member_in_group"></span>**\_membro \_ de erro no \_ grupo**
</dt> <dd> <dl> <dt>

1320 (0x528)
</dt> <dt>



A conta de usuário especificada já é um membro do grupo especificado ou o grupo especificado não pode ser excluído porque contém um membro.


</dt> </dl> </dd> <dt>

<span id="ERROR_MEMBER_NOT_IN_GROUP"></span><span id="error_member_not_in_group"></span>**o \_ membro \_ de erro não está \_ no \_ grupo**
</dt> <dd> <dl> <dt>

1321 (0x529)
</dt> <dt>



A conta de usuário especificada não é membro da conta de grupo especificada.


</dt> </dl> </dd> <dt>

<span id="ERROR_LAST_ADMIN"></span><span id="error_last_admin"></span>**ERRO do \_ último \_ administrador**
</dt> <dd> <dl> <dt>

1322 (0x52A)
</dt> <dt>



Esta operação não é permitida, pois pode resultar em uma conta de administração desabilitada, excluída ou não conseguir fazer logon.


</dt> </dl> </dd> <dt>

<span id="ERROR_WRONG_PASSWORD"></span><span id="error_wrong_password"></span>**ERRO \_ de \_ senha incorreta**
</dt> <dd> <dl> <dt>

1323 (0x52B)
</dt> <dt>



Não é possível atualizar a senha. O valor fornecido como a senha atual está incorreto.


</dt> </dl> </dd> <dt>

<span id="ERROR_ILL_FORMED_PASSWORD"></span><span id="error_ill_formed_password"></span>**ERRO \_ de \_ senha mal formada \_**
</dt> <dd> <dl> <dt>

1324 (0x52C)
</dt> <dt>



Não é possível atualizar a senha. O valor fornecido para a nova senha contém valores que não são permitidos em senhas.


</dt> </dl> </dd> <dt>

<span id="ERROR_PASSWORD_RESTRICTION"></span><span id="error_password_restriction"></span>**\_restrição de senha de erro \_**
</dt> <dd> <dl> <dt>

1325 (0x52D)
</dt> <dt>



Não é possível atualizar a senha. O valor fornecido para a nova senha não atende aos requisitos de comprimento, complexidade ou histórico do domínio.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOGON_FAILURE"></span><span id="error_logon_failure"></span>**\_falha no logon do erro \_**
</dt> <dd> <dl> <dt>

1326 (0x52E)
</dt> <dt>



O nome de usuário ou senha está incorreta.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCOUNT_RESTRICTION"></span><span id="error_account_restriction"></span>**\_restrição de conta de erro \_**
</dt> <dd> <dl> <dt>

1327 (0x52F)
</dt> <dt>



As restrições de conta estão impedindo o usuário de entrar. Por exemplo: senhas em branco não são permitidas, tempos de entrada são limitados ou uma restrição de política foi imposta.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LOGON_HOURS"></span><span id="error_invalid_logon_hours"></span>**\_horário de \_ logon \_ inválido do erro**
</dt> <dd> <dl> <dt>

1328 (0x530)
</dt> <dt>



Sua conta tem restrições de tempo que o impedem de entrar no momento.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_WORKSTATION"></span><span id="error_invalid_workstation"></span>**ERRO \_ de \_ estação de trabalho inválida**
</dt> <dd> <dl> <dt>

1329 (0x531)
</dt> <dt>



Este usuário não tem permissão para entrar neste computador.


</dt> </dl> </dd> <dt>

<span id="ERROR_PASSWORD_EXPIRED"></span><span id="error_password_expired"></span>**ERRO de \_ senha \_ expirada**
</dt> <dd> <dl> <dt>

1330 (0x532)
</dt> <dt>



A senha desta conta expirou.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCOUNT_DISABLED"></span><span id="error_account_disabled"></span>**conta de erro \_ \_ desabilitada**
</dt> <dd> <dl> <dt>

1331 (0x533)
</dt> <dt>



Este usuário não pode entrar porque esta conta está desabilitada no momento.


</dt> </dl> </dd> <dt>

<span id="ERROR_NONE_MAPPED"></span><span id="error_none_mapped"></span>**ERRO \_ nenhum \_ mapeado**
</dt> <dd> <dl> <dt>

1332 (0x534)
</dt> <dt>



Nenhum mapeamento entre os nomes de conta e as IDs de segurança foi feito.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_LUIDS_REQUESTED"></span><span id="error_too_many_luids_requested"></span>**ERRO \_ número \_ excessivo de \_ LUIDS \_ solicitados**
</dt> <dd> <dl> <dt>

1333 (0x535)
</dt> <dt>



Um número excessivo de identificadores de usuário local (LUIDs) foi solicitado ao mesmo tempo.


</dt> </dl> </dd> <dt>

<span id="ERROR_LUIDS_EXHAUSTED"></span><span id="error_luids_exhausted"></span>**ERRO \_ LUIDS \_ esgotado**
</dt> <dd> <dl> <dt>

1334 (0x536)
</dt> <dt>



Não há mais identificadores de usuário local (LUIDs) disponíveis.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SUB_AUTHORITY"></span><span id="error_invalid_sub_authority"></span>**\_sub- \_ \_ autoridade INválida de erro**
</dt> <dd> <dl> <dt>

1335 (0x537)
</dt> <dt>



A parte de subautoridade de uma ID de segurança é inválida para esse uso específico.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ACL"></span><span id="error_invalid_acl"></span>**ERRO \_ \_ ACL inválido**
</dt> <dd> <dl> <dt>

1336 (0x538)
</dt> <dt>



A estrutura da ACL (lista de controle de acesso) é inválida.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SID"></span><span id="error_invalid_sid"></span>**ERRO \_ \_ Sid inválido**
</dt> <dd> <dl> <dt>

1337 (0x539)
</dt> <dt>



A estrutura da ID de segurança é inválida.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SECURITY_DESCR"></span><span id="error_invalid_security_descr"></span>**ERRO \_ de \_ descr de segurança inválido \_**
</dt> <dd> <dl> <dt>

1338 (0x53A)
</dt> <dt>



A estrutura do descritor de segurança é inválida.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_INHERITANCE_ACL"></span><span id="error_bad_inheritance_acl"></span>**ERRO \_ \_ ACL de herança inadequada \_**
</dt> <dd> <dl> <dt>

1340 (0x53C)
</dt> <dt>



Não foi possível criar a ACL (lista de controle de acesso) herdada ou a ACE (entrada de controle de acesso).


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVER_DISABLED"></span><span id="error_server_disabled"></span>**servidor de erro \_ \_ desabilitado**
</dt> <dd> <dl> <dt>

1341 (0x53D)
</dt> <dt>



O servidor está desabilitado no momento.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVER_NOT_DISABLED"></span><span id="error_server_not_disabled"></span>**servidor de erro \_ \_ não \_ desabilitado**
</dt> <dd> <dl> <dt>

1342 (0x53E)
</dt> <dt>



O servidor está habilitado no momento.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ID_AUTHORITY"></span><span id="error_invalid_id_authority"></span>**ERRO \_ de \_ autoridade de identificação inválida \_**
</dt> <dd> <dl> <dt>

1343 (0x53F)
</dt> <dt>



O valor fornecido era um valor inválido para uma autoridade de identificador.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALLOTTED_SPACE_EXCEEDED"></span><span id="error_allotted_space_exceeded"></span>**\_espaço alocado de \_ erro \_ excedido**
</dt> <dd> <dl> <dt>

1344 (0x540)
</dt> <dt>



Não há mais memória disponível para atualizações de informações de segurança.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_GROUP_ATTRIBUTES"></span><span id="error_invalid_group_attributes"></span>**ERRO \_ de \_ atributos de grupo inválidos \_**
</dt> <dd> <dl> <dt>

1345 (0x541)
</dt> <dt>



Os atributos especificados são inválidos ou incompatíveis com os atributos do grupo como um todo.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_IMPERSONATION_LEVEL"></span><span id="error_bad_impersonation_level"></span>**ERRO \_ de \_ nível de representação insatisfatório \_**
</dt> <dd> <dl> <dt>

1346 (0x542)
</dt> <dt>



O nível de representação necessário não foi fornecido ou o nível de representação fornecido é inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_OPEN_ANONYMOUS"></span><span id="error_cant_open_anonymous"></span>**ERRO não é possível \_ \_ abrir \_ anônimo**
</dt> <dd> <dl> <dt>

1347 (0x543)
</dt> <dt>



Não é possível abrir um token de segurança de nível anônimo.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_VALIDATION_CLASS"></span><span id="error_bad_validation_class"></span>**ERRO \_ de \_ classe de validação inadequada \_**
</dt> <dd> <dl> <dt>

1348 (0x544)
</dt> <dt>



A classe de informações de validação solicitada era inválida.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_TOKEN_TYPE"></span><span id="error_bad_token_type"></span>**ERRO \_ de \_ tipo de token insatisfatório \_**
</dt> <dd> <dl> <dt>

1349 (0x545)
</dt> <dt>



O tipo do token não é apropriado para o uso tentado.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SECURITY_ON_OBJECT"></span><span id="error_no_security_on_object"></span>**ERRO \_ sem \_ segurança \_ no \_ objeto**
</dt> <dd> <dl> <dt>

1350 (0x546)
</dt> <dt>



Não é possível executar uma operação de segurança em um objeto que não tem segurança associada.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_ACCESS_DOMAIN_INFO"></span><span id="error_cant_access_domain_info"></span>**ERRO não é possível \_ \_ acessar as \_ informações do domínio \_**
</dt> <dd> <dl> <dt>

1351 (0x547)
</dt> <dt>



Não foi possível ler as informações de configuração do controlador de domínio porque o computador não está disponível ou o acesso foi negado.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SERVER_STATE"></span><span id="error_invalid_server_state"></span>**ERRO \_ inválido \_ no \_ estado do servidor**
</dt> <dd> <dl> <dt>

1352 (0x548)
</dt> <dt>



O Gerenciador de contas de segurança (SAM) ou o servidor de autoridade de segurança local (LSA) estava no estado incorreto para executar a operação de segurança.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DOMAIN_STATE"></span><span id="error_invalid_domain_state"></span>**ERRO \_ de \_ estado de domínio inválido \_**
</dt> <dd> <dl> <dt>

1353 (0x549)
</dt> <dt>



O domínio estava no estado incorreto para executar a operação de segurança.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DOMAIN_ROLE"></span><span id="error_invalid_domain_role"></span>**ERRO \_ de \_ função de domínio inválida \_**
</dt> <dd> <dl> <dt>

1354 (0x54A)
</dt> <dt>



Esta operação só é permitida para o controlador de domínio primário do domínio.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUCH_DOMAIN"></span><span id="error_no_such_domain"></span>**ERRO \_ no domínio inexistente \_ \_**
</dt> <dd> <dl> <dt>

1355 (0x54B)
</dt> <dt>



O domínio especificado não existe ou não pôde ser contatado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DOMAIN_EXISTS"></span><span id="error_domain_exists"></span>**o \_ domínio de erro \_ existe**
</dt> <dd> <dl> <dt>

1356 (0x54C)
</dt> <dt>



O domínio especificado já existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_DOMAIN_LIMIT_EXCEEDED"></span><span id="error_domain_limit_exceeded"></span>**limite de domínio de erro \_ \_ \_ excedido**
</dt> <dd> <dl> <dt>

1357 (0x54D)
</dt> <dt>



Foi feita uma tentativa de exceder o limite do número de domínios por servidor.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNAL_DB_CORRUPTION"></span><span id="error_internal_db_corruption"></span>**ERRO \_ de \_ corrupção interna do BD \_**
</dt> <dd> <dl> <dt>

1358 (0x54E)
</dt> <dt>



Não é possível concluir a operação solicitada devido a uma falha catastrófica na mídia ou à corrupção de uma estrutura de dados no disco.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNAL_ERROR"></span><span id="error_internal_error"></span>**erro \_ interno de erro \_**
</dt> <dd> <dl> <dt>

1359 (0x54F)
</dt> <dt>



Ocorreu um erro interno.


</dt> </dl> </dd> <dt>

<span id="ERROR_GENERIC_NOT_MAPPED"></span><span id="error_generic_not_mapped"></span>**ERRO \_ genérico \_ não \_ mapeado**
</dt> <dd> <dl> <dt>

1360 (0x550)
</dt> <dt>



Os tipos de acesso genéricos estavam contidos em uma máscara de acesso que já deve estar mapeada para tipos não genéricos.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_DESCRIPTOR_FORMAT"></span><span id="error_bad_descriptor_format"></span>**ERRO \_ de \_ formato de descritor inválido \_**
</dt> <dd> <dl> <dt>

1361 (0x551)
</dt> <dt>



Um descritor de segurança não está no formato correto (absoluto ou auto-relativo).


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_LOGON_PROCESS"></span><span id="error_not_logon_process"></span>**ERRO \_ não \_ processo de logon \_**
</dt> <dd> <dl> <dt>

1362 (0x552)
</dt> <dt>



A ação solicitada é restrita para uso somente por processos de logon. O processo de chamada não foi registrado como um processo de logon.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOGON_SESSION_EXISTS"></span><span id="error_logon_session_exists"></span>**a \_ sessão de logon de erro \_ \_ existe**
</dt> <dd> <dl> <dt>

1363 (0x553)
</dt> <dt>



Não é possível iniciar uma nova sessão de logon com uma ID que já está em uso.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUCH_PACKAGE"></span><span id="error_no_such_package"></span>**ERRO \_ nenhum \_ pacote desse tipo \_**
</dt> <dd> <dl> <dt>

1364 (0x554)
</dt> <dt>



Um pacote de autenticação especificado é desconhecido.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_LOGON_SESSION_STATE"></span><span id="error_bad_logon_session_state"></span>**ERRO \_ \_ estado de \_ sessão de logon insatisfatório \_**
</dt> <dd> <dl> <dt>

1365 (0x555)
</dt> <dt>



A sessão de logon não está em um estado consistente com a operação solicitada.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOGON_SESSION_COLLISION"></span><span id="error_logon_session_collision"></span>**ERRO \_ de \_ colisão de sessão de logon \_**
</dt> <dd> <dl> <dt>

1366 (0x556)
</dt> <dt>



A ID da sessão de logon já está em uso.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LOGON_TYPE"></span><span id="error_invalid_logon_type"></span>**ERRO \_ de \_ tipo de logon inválido \_**
</dt> <dd> <dl> <dt>

1367 (0x557)
</dt> <dt>



Uma solicitação de logon continha um valor de tipo de logon inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_IMPERSONATE"></span><span id="error_cannot_impersonate"></span>**ERRO \_ não pode \_ representar**
</dt> <dd> <dl> <dt>

1368 (0x558)
</dt> <dt>



Não é possível representar usando um pipe nomeado até que os dados tenham sido lidos desse pipe.


</dt> </dl> </dd> <dt>

<span id="ERROR_RXACT_INVALID_STATE"></span><span id="error_rxact_invalid_state"></span>**ERRO \_ RXACT \_ \_ estado inválido**
</dt> <dd> <dl> <dt>

1369 (0x559)
</dt> <dt>



O estado de transação de uma subárvore do registro é incompatível com a operação solicitada.


</dt> </dl> </dd> <dt>

<span id="ERROR_RXACT_COMMIT_FAILURE"></span><span id="error_rxact_commit_failure"></span>**ERRO \_ RXACT \_ \_ falha na confirmação**
</dt> <dd> <dl> <dt>

1370 (0x55A)
</dt> <dt>



Foi encontrado um banco de dados de segurança interno corrompido.


</dt> </dl> </dd> <dt>

<span id="ERROR_SPECIAL_ACCOUNT"></span><span id="error_special_account"></span>**ERRO \_ de \_ conta especial**
</dt> <dd> <dl> <dt>

1371 (0x55B)
</dt> <dt>



Não é possível executar esta operação em contas internas.


</dt> </dl> </dd> <dt>

<span id="ERROR_SPECIAL_GROUP"></span><span id="error_special_group"></span>**ERRO \_ de \_ grupo especial**
</dt> <dd> <dl> <dt>

1372 (0x55C)
</dt> <dt>



Não é possível executar esta operação neste grupo especial interno.


</dt> </dl> </dd> <dt>

<span id="ERROR_SPECIAL_USER"></span><span id="error_special_user"></span>**ERRO \_ especial do \_ usuário**
</dt> <dd> <dl> <dt>

1373 (0x55D)
</dt> <dt>



Não é possível executar esta operação neste usuário especial interno.


</dt> </dl> </dd> <dt>

<span id="ERROR_MEMBERS_PRIMARY_GROUP"></span><span id="error_members_primary_group"></span>**\_ \_ grupo primário de membros de erro \_**
</dt> <dd> <dl> <dt>

1374 (0x55E)
</dt> <dt>



O usuário não pode ser removido de um grupo porque o grupo é atualmente o grupo primário do usuário.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOKEN_ALREADY_IN_USE"></span><span id="error_token_already_in_use"></span>**o \_ token \_ de erro já está \_ em \_ uso**
</dt> <dd> <dl> <dt>

1375 (0x55F)
</dt> <dt>



O token já está em uso como um token primário.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUCH_ALIAS"></span><span id="error_no_such_alias"></span>**ERRO \_ sem \_ \_ alias**
</dt> <dd> <dl> <dt>

1376 (0x560)
</dt> <dt>



O grupo local especificado não existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_MEMBER_NOT_IN_ALIAS"></span><span id="error_member_not_in_alias"></span>**o \_ membro \_ do erro não está \_ no \_ alias**
</dt> <dd> <dl> <dt>

1377 (0x561)
</dt> <dt>



O nome de conta especificado não é um membro do grupo.


</dt> </dl> </dd> <dt>

<span id="ERROR_MEMBER_IN_ALIAS"></span><span id="error_member_in_alias"></span>**\_membro \_ de erro no \_ alias**
</dt> <dd> <dl> <dt>

1378 (0x562)
</dt> <dt>



O nome de conta especificado já é um membro do grupo.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALIAS_EXISTS"></span><span id="error_alias_exists"></span>**o \_ alias de erro \_ existe**
</dt> <dd> <dl> <dt>

1379 (0x563)
</dt> <dt>



O grupo local especificado já existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOGON_NOT_GRANTED"></span><span id="error_logon_not_granted"></span>**ERRO de \_ logon \_ não \_ concedido**
</dt> <dd> <dl> <dt>

1380 (0x564)
</dt> <dt>



Falha de logon: o usuário não recebeu o tipo de logon solicitado neste computador.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_SECRETS"></span><span id="error_too_many_secrets"></span>**ERRO \_ de \_ muitos \_ segredos**
</dt> <dd> <dl> <dt>

1381 (0x565)
</dt> <dt>



O número máximo de segredos que podem ser armazenados em um único sistema foi excedido.


</dt> </dl> </dd> <dt>

<span id="ERROR_SECRET_TOO_LONG"></span><span id="error_secret_too_long"></span>**segredo de erro \_ \_ muito \_ longo**
</dt> <dd> <dl> <dt>

1382 (0x566)
</dt> <dt>



O comprimento de um segredo excede o comprimento máximo permitido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNAL_DB_ERROR"></span><span id="error_internal_db_error"></span>**erro \_ interno do \_ BD de \_ erros**
</dt> <dd> <dl> <dt>

1383 (0x567)
</dt> <dt>



O banco de dados da autoridade de segurança local contém uma inconsistência interna.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_CONTEXT_IDS"></span><span id="error_too_many_context_ids"></span>**ERRO em excesso de \_ \_ \_ IDs de contexto \_**
</dt> <dd> <dl> <dt>

1384 (0x568)
</dt> <dt>



Durante uma tentativa de logon, o contexto de segurança do usuário acumulou muitas identificações de segurança.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOGON_TYPE_NOT_GRANTED"></span><span id="error_logon_type_not_granted"></span>**tipo de logon de erro \_ \_ \_ não \_ concedido**
</dt> <dd> <dl> <dt>

1385 (0x569)
</dt> <dt>



Falha de logon: o usuário não recebeu o tipo de logon solicitado neste computador.


</dt> </dl> </dd> <dt>

<span id="ERROR_NT_CROSS_ENCRYPTION_REQUIRED"></span><span id="error_nt_cross_encryption_required"></span>**ERRO \_ de \_ criptografia cruzada do NT \_ \_ necessária**
</dt> <dd> <dl> <dt>

1386 (0x56A)
</dt> <dt>



Uma senha com criptografia cruzada é necessária para alterar uma senha de usuário.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUCH_MEMBER"></span><span id="error_no_such_member"></span>**\_não há \_ tal \_ membro**
</dt> <dd> <dl> <dt>

1387 (0x56B)
</dt> <dt>



Um membro não pôde ser adicionado ou removido do grupo local porque o membro não existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MEMBER"></span><span id="error_invalid_member"></span>**\_membro inválido do erro \_**
</dt> <dd> <dl> <dt>

1388 (0x56C)
</dt> <dt>



Não foi possível adicionar um novo membro a um grupo local porque o membro tem o tipo de conta incorreto.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_SIDS"></span><span id="error_too_many_sids"></span>**ERRO em excesso de \_ \_ \_ SIDs**
</dt> <dd> <dl> <dt>

1389 (0x56D)
</dt> <dt>



Foram especificadas muitas IDs de segurança.


</dt> </dl> </dd> <dt>

<span id="ERROR_LM_CROSS_ENCRYPTION_REQUIRED"></span><span id="error_lm_cross_encryption_required"></span>**ERRO \_ de \_ criptografia cruzada de LM \_ \_ necessária**
</dt> <dd> <dl> <dt>

1390 (0x56E)
</dt> <dt>



Uma senha com criptografia cruzada é necessária para alterar essa senha de usuário.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_INHERITANCE"></span><span id="error_no_inheritance"></span>**ERRO \_ sem \_ herança**
</dt> <dd> <dl> <dt>

1391 (0x56F)
</dt> <dt>



Indica que uma ACL não contém componentes herdáveis.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_CORRUPT"></span><span id="error_file_corrupt"></span>**arquivo de erro \_ \_ corrompido**
</dt> <dd> <dl> <dt>

1392 (0x570)
</dt> <dt>



O arquivo ou diretório está corrompido e ilegível.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_CORRUPT"></span><span id="error_disk_corrupt"></span>**disco de erro \_ \_ corrompido**
</dt> <dd> <dl> <dt>

1393 (0x571)
</dt> <dt>



A estrutura do disco está corrompida e ilegível.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_USER_SESSION_KEY"></span><span id="error_no_user_session_key"></span>**ERRO \_ sem \_ \_ chave de sessão de usuário \_**
</dt> <dd> <dl> <dt>

1394 (0x572)
</dt> <dt>



Não há nenhuma chave de sessão de usuário para a sessão de logon especificada.


</dt> </dl> </dd> <dt>

<span id="ERROR_LICENSE_QUOTA_EXCEEDED"></span><span id="error_license_quota_exceeded"></span>**cota de licença de erro \_ \_ \_ excedida**
</dt> <dd> <dl> <dt>

1395 (0x573)
</dt> <dt>



O serviço que está sendo acessado é licenciado para um determinado número de conexões. Não é possível fazer mais conexões com o serviço no momento porque já existem tantas conexões quantas o serviço pode aceitar.


</dt> </dl> </dd> <dt>

<span id="ERROR_WRONG_TARGET_NAME"></span><span id="error_wrong_target_name"></span>**ERRO \_ de \_ nome de destino incorreto \_**
</dt> <dd> <dl> <dt>

1396 (0x574)
</dt> <dt>



O nome da conta de destino está incorreto.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUTUAL_AUTH_FAILED"></span><span id="error_mutual_auth_failed"></span>**ERRO \_ de \_ autenticação mútua \_ falhou**
</dt> <dd> <dl> <dt>

1397 (0x575)
</dt> <dt>



Falha na autenticação mútua. A senha do servidor está desatualizada no controlador de domínio.


</dt> </dl> </dd> <dt>

<span id="ERROR_TIME_SKEW"></span><span id="error_time_skew"></span>**distorção de tempo de erro \_ \_**
</dt> <dd> <dl> <dt>

1398 (0x576)
</dt> <dt>



Há uma diferença de hora e/ou data entre o cliente e o servidor.


</dt> </dl> </dd> <dt>

<span id="ERROR_CURRENT_DOMAIN_NOT_ALLOWED"></span><span id="error_current_domain_not_allowed"></span>**ERRO \_ \_ domínio atual \_ não \_ permitido**
</dt> <dd> <dl> <dt>

1399 (0x577)
</dt> <dt>



Esta operação não pode ser executada no domínio atual.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_WINDOW_HANDLE"></span><span id="error_invalid_window_handle"></span>**ERRO \_ de \_ identificador de janela inválido \_**
</dt> <dd> <dl> <dt>

1400 (0x578)
</dt> <dt>



Identificador de janela inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MENU_HANDLE"></span><span id="error_invalid_menu_handle"></span>**ERRO \_ de \_ identificador de menu inválido \_**
</dt> <dd> <dl> <dt>

1401 (0x579)
</dt> <dt>



Identificador de menu inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_CURSOR_HANDLE"></span><span id="error_invalid_cursor_handle"></span>**ERRO \_ de \_ identificador de cursor inválido \_**
</dt> <dd> <dl> <dt>

1402 (0x57A)
</dt> <dt>



Identificador de cursor inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ACCEL_HANDLE"></span><span id="error_invalid_accel_handle"></span>**ERRO \_ \_ identificador de da aceleração extra inválido \_**
</dt> <dd> <dl> <dt>

1403 (0x57B)
</dt> <dt>



Identificador de tabela de acelerador inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_HOOK_HANDLE"></span><span id="error_invalid_hook_handle"></span>**ERRO \_ de \_ identificador de gancho inválido \_**
</dt> <dd> <dl> <dt>

1404 (0x57C)
</dt> <dt>



Identificador de gancho inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DWP_HANDLE"></span><span id="error_invalid_dwp_handle"></span>**ERRO \_ de \_ identificador DWP inválido \_**
</dt> <dd> <dl> <dt>

1405 (0x57D)
</dt> <dt>



Identificador inválido para uma estrutura de posição de várias janelas.


</dt> </dl> </dd> <dt>

<span id="ERROR_TLW_WITH_WSCHILD"></span><span id="error_tlw_with_wschild"></span>**ERRO \_ TLW \_ com \_ WSCHILD**
</dt> <dd> <dl> <dt>

1406 (0x57E)
</dt> <dt>



Não é possível criar uma janela filho de nível superior.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_FIND_WND_CLASS"></span><span id="error_cannot_find_wnd_class"></span>**ERRO \_ não é possível \_ localizar a \_ \_ classe WND**
</dt> <dd> <dl> <dt>

1407 (0x57F)
</dt> <dt>



Não é possível localizar a classe Window.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINDOW_OF_OTHER_THREAD"></span><span id="error_window_of_other_thread"></span>**\_janela \_ de erro de \_ outro \_ thread**
</dt> <dd> <dl> <dt>

1408 (0x580)
</dt> <dt>



Janela inválida; Ele pertence a outro thread.


</dt> </dl> </dd> <dt>

<span id="ERROR_HOTKEY_ALREADY_REGISTERED"></span><span id="error_hotkey_already_registered"></span>**ERRO de \_ tecla de atalho \_ já \_ registrado**
</dt> <dd> <dl> <dt>

1409 (0x581)
</dt> <dt>



A tecla de acesso já está registrada.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLASS_ALREADY_EXISTS"></span><span id="error_class_already_exists"></span>**a \_ classe de erro \_ já \_ existe**
</dt> <dd> <dl> <dt>

1410 (0x582)
</dt> <dt>



A classe já existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLASS_DOES_NOT_EXIST"></span><span id="error_class_does_not_exist"></span>**a classe de erro não \_ \_ \_ \_ existe**
</dt> <dd> <dl> <dt>

1411 (0x583)
</dt> <dt>



A classe não existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLASS_HAS_WINDOWS"></span><span id="error_class_has_windows"></span>**classe de erro \_ \_ tem \_ Windows**
</dt> <dd> <dl> <dt>

1412 (0x584)
</dt> <dt>



A classe ainda tem janelas abertas.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_INDEX"></span><span id="error_invalid_index"></span>**ERRO \_ de \_ índice inválido**
</dt> <dd> <dl> <dt>

1413 (0x585)
</dt> <dt>



Índice inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ICON_HANDLE"></span><span id="error_invalid_icon_handle"></span>**ERRO \_ \_ identificador de ícone inválido \_**
</dt> <dd> <dl> <dt>

1414 (0x586)
</dt> <dt>



Identificador de ícone inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRIVATE_DIALOG_INDEX"></span><span id="error_private_dialog_index"></span>**ERRO \_ de \_ índice de caixa de diálogo particular \_**
</dt> <dd> <dl> <dt>

1415 (0x587)
</dt> <dt>



Usando palavras de janela de caixa de diálogo particulares.


</dt> </dl> </dd> <dt>

<span id="ERROR_LISTBOX_ID_NOT_FOUND"></span><span id="error_listbox_id_not_found"></span>**ID da caixa de listagem de erro \_ \_ \_ não \_ encontrada**
</dt> <dd> <dl> <dt>

1416 (0x588)
</dt> <dt>



O identificador da caixa de listagem não foi encontrado.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_WILDCARD_CHARACTERS"></span><span id="error_no_wildcard_characters"></span>**ERRO \_ nenhum caractere \_ curinga \_**
</dt> <dd> <dl> <dt>

1417 (0x589)
</dt> <dt>



Nenhum caractere curinga foi encontrado.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLIPBOARD_NOT_OPEN"></span><span id="error_clipboard_not_open"></span>**área de transferência de erro \_ \_ não \_ aberta**
</dt> <dd> <dl> <dt>

1418 (0x58A)
</dt> <dt>



O thread não tem uma área de transferência aberta.


</dt> </dl> </dd> <dt>

<span id="ERROR_HOTKEY_NOT_REGISTERED"></span><span id="error_hotkey_not_registered"></span>**ERRO de \_ tecla de atalho \_ não \_ registrado**
</dt> <dd> <dl> <dt>

1419 (0x58B)
</dt> <dt>



A tecla de acesso não está registrada.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINDOW_NOT_DIALOG"></span><span id="error_window_not_dialog"></span>**janela de erro \_ \_ não \_ caixa de diálogo**
</dt> <dd> <dl> <dt>

1420 (0x58C)
</dt> <dt>



A janela não é uma janela de diálogo válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONTROL_ID_NOT_FOUND"></span><span id="error_control_id_not_found"></span>**ID de controle de erro \_ \_ \_ não \_ encontrada**
</dt> <dd> <dl> <dt>

1421 (0x58D)
</dt> <dt>



ID de controle não encontrada.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_COMBOBOX_MESSAGE"></span><span id="error_invalid_combobox_message"></span>**ERRO \_ \_ mensagem de ComboBox inválida \_**
</dt> <dd> <dl> <dt>

1422 (0x58E)
</dt> <dt>



Mensagem inválida para uma caixa de combinação porque não tem um controle de edição.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINDOW_NOT_COMBOBOX"></span><span id="error_window_not_combobox"></span>**janela de erro \_ \_ sem \_ ComboBox**
</dt> <dd> <dl> <dt>

1423 (0x58F)
</dt> <dt>



A janela não é uma caixa de combinação.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_EDIT_HEIGHT"></span><span id="error_invalid_edit_height"></span>**ERRO \_ de \_ edição de \_ altura inválido**
</dt> <dd> <dl> <dt>

1424 (0x590)
</dt> <dt>



A altura deve ser menor que 256.


</dt> </dl> </dd> <dt>

<span id="ERROR_DC_NOT_FOUND"></span><span id="error_dc_not_found"></span>**ERRO de \_ DC \_ não \_ encontrado**
</dt> <dd> <dl> <dt>

1425 (0x591)
</dt> <dt>



Identificador de contexto de dispositivo (DC) inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_HOOK_FILTER"></span><span id="error_invalid_hook_filter"></span>**ERRO \_ de \_ filtro de gancho inválido \_**
</dt> <dd> <dl> <dt>

1426 (0x592)
</dt> <dt>



Tipo de procedimento de Hook inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_FILTER_PROC"></span><span id="error_invalid_filter_proc"></span>**ERRO \_ \_ procedimento de filtro inválido \_**
</dt> <dd> <dl> <dt>

1427 (0x593)
</dt> <dt>



Procedimento de gancho inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_HOOK_NEEDS_HMOD"></span><span id="error_hook_needs_hmod"></span>**o \_ gancho de erro \_ precisa de \_ HMOD**
</dt> <dd> <dl> <dt>

1428 (0x594)
</dt> <dt>



Não é possível definir um gancho não local sem um identificador de módulo.


</dt> </dl> </dd> <dt>

<span id="ERROR_GLOBAL_ONLY_HOOK"></span><span id="error_global_only_hook"></span>**\_ \_ somente gancho global \_ de erro**
</dt> <dd> <dl> <dt>

1429 (0x595)
</dt> <dt>



Esse procedimento de gancho só pode ser definido globalmente.


</dt> </dl> </dd> <dt>

<span id="ERROR_JOURNAL_HOOK_SET"></span><span id="error_journal_hook_set"></span>**\_conjunto de \_ ganchos do diário de erros \_**
</dt> <dd> <dl> <dt>

1430 (0x596)
</dt> <dt>



O procedimento de gancho de diário já está instalado.


</dt> </dl> </dd> <dt>

<span id="ERROR_HOOK_NOT_INSTALLED"></span><span id="error_hook_not_installed"></span>**gancho de erro \_ \_ não \_ instalado**
</dt> <dd> <dl> <dt>

1431 (0x597)
</dt> <dt>



O procedimento de gancho não está instalado.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LB_MESSAGE"></span><span id="error_invalid_lb_message"></span>**ERRO \_ de \_ mensagem lb inválida \_**
</dt> <dd> <dl> <dt>

1432 (0x598)
</dt> <dt>



Mensagem inválida para caixa de listagem de seleção única.


</dt> </dl> </dd> <dt>

<span id="ERROR_SETCOUNT_ON_BAD_LB"></span><span id="error_setcount_on_bad_lb"></span>**ERRO \_ SetCount \_ em \_ lb insatisfatório \_**
</dt> <dd> <dl> <dt>

1433 (0x599)
</dt> <dt>



\_Contagem de lb para a caixa de listagem não Lazy enviada.


</dt> </dl> </dd> <dt>

<span id="ERROR_LB_WITHOUT_TABSTOPS"></span><span id="error_lb_without_tabstops"></span>**ERRO \_ lb \_ sem \_ TabStops**
</dt> <dd> <dl> <dt>

1434 (0x59A)
</dt> <dt>



Esta caixa de listagem não dá suporte para paradas de tabulação.


</dt> </dl> </dd> <dt>

<span id="ERROR_DESTROY_OBJECT_OF_OTHER_THREAD"></span><span id="error_destroy_object_of_other_thread"></span>**ERRO \_ destruir \_ objeto \_ de \_ outro \_ thread**
</dt> <dd> <dl> <dt>

1435 (0x59B)
</dt> <dt>



Não é possível destruir o objeto criado por outro thread.


</dt> </dl> </dd> <dt>

<span id="ERROR_CHILD_WINDOW_MENU"></span><span id="error_child_window_menu"></span>**\_menu da \_ janela \_ filho do erro**
</dt> <dd> <dl> <dt>

1436 (0x59C)
</dt> <dt>



Janelas filhas não podem ter menus.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SYSTEM_MENU"></span><span id="error_no_system_menu"></span>**ERRO \_ nenhum \_ menu do sistema \_**
</dt> <dd> <dl> <dt>

1437 (0x59D)
</dt> <dt>



A janela não tem um menu do sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MSGBOX_STYLE"></span><span id="error_invalid_msgbox_style"></span>**ERRO \_ \_ estilo MSGBOX \_ inválido**
</dt> <dd> <dl> <dt>

1438 (0x59E)
</dt> <dt>



Estilo de caixa de mensagem inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SPI_VALUE"></span><span id="error_invalid_spi_value"></span>**ERRO \_ de \_ valor SPI inválido \_**
</dt> <dd> <dl> <dt>

1439 (0x59F)
</dt> <dt>



Parâmetro de todo o sistema (SPI \_ \* ) inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_SCREEN_ALREADY_LOCKED"></span><span id="error_screen_already_locked"></span>**tela de erro \_ \_ já \_ bloqueada**
</dt> <dd> <dl> <dt>

1440 (0x5A0)
</dt> <dt>



Tela já bloqueada.


</dt> </dl> </dd> <dt>

<span id="ERROR_HWNDS_HAVE_DIFF_PARENT"></span><span id="error_hwnds_have_diff_parent"></span>**os \_ HWNDs de erro \_ têm o \_ \_ pai diff**
</dt> <dd> <dl> <dt>

1441 (0x5A1)
</dt> <dt>



Todos os identificadores para o Windows em uma estrutura de posição de várias janelas devem ter o mesmo pai.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_CHILD_WINDOW"></span><span id="error_not_child_window"></span>**ERRO \_ não \_ é \_ janela filho**
</dt> <dd> <dl> <dt>

1442 (0x5A2)
</dt> <dt>



A janela não é uma janela filho.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_GW_COMMAND"></span><span id="error_invalid_gw_command"></span>**ERRO \_ inválido \_ do \_ comando GW**
</dt> <dd> <dl> <dt>

1443 (0x5A3)
</dt> <dt>



Comando GW inválido \_ \* .


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_THREAD_ID"></span><span id="error_invalid_thread_id"></span>**ERRO \_ \_ ID de thread inválida \_**
</dt> <dd> <dl> <dt>

1444 (0x5A4)
</dt> <dt>



Identificador de thread inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_NON_MDICHILD_WINDOW"></span><span id="error_non_mdichild_window"></span>**ERRO \_ de \_ janela não MDICHILD \_**
</dt> <dd> <dl> <dt>

1445 (0x5A5)
</dt> <dt>



Não é possível processar uma mensagem de uma janela que não seja uma janela de interface de vários documentos (MDI).


</dt> </dl> </dd> <dt>

<span id="ERROR_POPUP_ALREADY_ACTIVE"></span><span id="error_popup_already_active"></span>**\_pop-up de erro \_ já \_ ativo**
</dt> <dd> <dl> <dt>

1446 (0x5A6)
</dt> <dt>



O menu pop-up já está ativo.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SCROLLBARS"></span><span id="error_no_scrollbars"></span>**ERRO \_ sem \_ barras de rolagem**
</dt> <dd> <dl> <dt>

1447 (0x5A7)
</dt> <dt>



A janela não tem barras de rolagem.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SCROLLBAR_RANGE"></span><span id="error_invalid_scrollbar_range"></span>**ERRO \_ de \_ intervalo de barra de rolagem inválido \_**
</dt> <dd> <dl> <dt>

1448 (0x5A8)
</dt> <dt>



O intervalo da barra de rolagem não pode ser maior que MAXLONG.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SHOWWIN_COMMAND"></span><span id="error_invalid_showwin_command"></span>**ERRO \_ de \_ comando SHOWWIN inválido \_**
</dt> <dd> <dl> <dt>

1449 (0x5A9)
</dt> <dt>



Não é possível mostrar ou remover a janela da maneira especificada.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SYSTEM_RESOURCES"></span><span id="error_no_system_resources"></span>**ERRO \_ sem \_ recursos do sistema \_**
</dt> <dd> <dl> <dt>

1450 (0x5AA)
</dt> <dt>



Existem recursos do sistema insuficientes para concluir o serviço solicitado.


</dt> </dl> </dd> <dt>

<span id="ERROR_NONPAGED_SYSTEM_RESOURCES"></span><span id="error_nonpaged_system_resources"></span>**ERRO de \_ recursos do \_ sistema não paginável \_**
</dt> <dd> <dl> <dt>

1451 (0x5AB)
</dt> <dt>



Existem recursos do sistema insuficientes para concluir o serviço solicitado.


</dt> </dl> </dd> <dt>

<span id="ERROR_PAGED_SYSTEM_RESOURCES"></span><span id="error_paged_system_resources"></span>**ERRO na \_ paginação de \_ recursos do sistema \_**
</dt> <dd> <dl> <dt>

1452 (0x5AC)
</dt> <dt>



Existem recursos do sistema insuficientes para concluir o serviço solicitado.


</dt> </dl> </dd> <dt>

<span id="ERROR_WORKING_SET_QUOTA"></span><span id="error_working_set_quota"></span>**ERRO \_ de \_ cota de conjunto de trabalho \_**
</dt> <dd> <dl> <dt>

1453 (0x5AD)
</dt> <dt>



Cota insuficiente para concluir o serviço solicitado.


</dt> </dl> </dd> <dt>

<span id="ERROR_PAGEFILE_QUOTA"></span><span id="error_pagefile_quota"></span>**\_cota de arquivo de erro \_**
</dt> <dd> <dl> <dt>

1454 (0x5AE)
</dt> <dt>



Cota insuficiente para concluir o serviço solicitado.


</dt> </dl> </dd> <dt>

<span id="ERROR_COMMITMENT_LIMIT"></span><span id="error_commitment_limit"></span>**\_limite de compromisso de erro \_**
</dt> <dd> <dl> <dt>

1455 (0x5AF)
</dt> <dt>



O arquivo de paginação é muito pequeno para que esta operação seja concluída.


</dt> </dl> </dd> <dt>

<span id="ERROR_MENU_ITEM_NOT_FOUND"></span><span id="error_menu_item_not_found"></span>**ITEM de menu de erro \_ \_ \_ não \_ encontrado**
</dt> <dd> <dl> <dt>

1456 (0x5B0)
</dt> <dt>



Um item de menu não foi encontrado.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_KEYBOARD_HANDLE"></span><span id="error_invalid_keyboard_handle"></span>**ERRO \_ de \_ identificador de teclado inválido \_**
</dt> <dd> <dl> <dt>

1457 (0x5B1)
</dt> <dt>



Identificador de layout de teclado inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_HOOK_TYPE_NOT_ALLOWED"></span><span id="error_hook_type_not_allowed"></span>**tipo de gancho de erro \_ \_ \_ não \_ permitido**
</dt> <dd> <dl> <dt>

1458 (0x5B2)
</dt> <dt>



Tipo de gancho não permitido.


</dt> </dl> </dd> <dt>

<span id="ERROR_REQUIRES_INTERACTIVE_WINDOWSTATION"></span><span id="error_requires_interactive_windowstation"></span>**ERRO \_ requer \_ \_ WINDOWSTATION interativo**
</dt> <dd> <dl> <dt>

1459 (0x5B3)
</dt> <dt>



Esta operação requer uma estação de janela interativa.


</dt> </dl> </dd> <dt>

<span id="ERROR_TIMEOUT"></span><span id="error_timeout"></span>**\_tempo limite do erro**
</dt> <dd> <dl> <dt>

1460 (0x5B4)
</dt> <dt>



Esta operação foi retornada porque o período de tempo limite expirou.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MONITOR_HANDLE"></span><span id="error_invalid_monitor_handle"></span>**ERRO \_ de \_ identificador de monitor inválido \_**
</dt> <dd> <dl> <dt>

1461 (0x5B5)
</dt> <dt>



Identificador de monitor inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INCORRECT_SIZE"></span><span id="error_incorrect_size"></span>**\_Tamanho incorreto do erro \_**
</dt> <dd> <dl> <dt>

1462 (0x5B6)
</dt> <dt>



Argumento de tamanho incorreto.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYMLINK_CLASS_DISABLED"></span><span id="error_symlink_class_disabled"></span>**ERRO \_ de \_ classe SYMLINK \_ desabilitada**
</dt> <dd> <dl> <dt>

1463 (0x5B7)
</dt> <dt>



O link simbólico não pode ser seguido porque seu tipo está desabilitado.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYMLINK_NOT_SUPPORTED"></span><span id="error_symlink_not_supported"></span>**ERRO \_ SYMLINK \_ não \_ suportado**
</dt> <dd> <dl> <dt>

1464 (0x5B8)
</dt> <dt>



Este aplicativo não oferece suporte à operação atual em links simbólicos.


</dt> </dl> </dd> <dt>

<span id="ERROR_XML_PARSE_ERROR"></span><span id="error_xml_parse_error"></span>**erro de \_ análise de XML de erro \_ \_**
</dt> <dd> <dl> <dt>

1465 (0x5B9)
</dt> <dt>



O Windows não pôde analisar os dados XML solicitados.


</dt> </dl> </dd> <dt>

<span id="ERROR_XMLDSIG_ERROR"></span><span id="error_xmldsig_error"></span>**erro \_ XMLDSIG \_**
</dt> <dd> <dl> <dt>

1466 (0x5BA)
</dt> <dt>



Foi encontrado um erro ao processar uma assinatura digital XML.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESTART_APPLICATION"></span><span id="error_restart_application"></span>**ERRO ao \_ reiniciar o \_ aplicativo**
</dt> <dd> <dl> <dt>

1467 (0x5BB)
</dt> <dt>



Esse aplicativo deve ser reiniciado.


</dt> </dl> </dd> <dt>

<span id="ERROR_WRONG_COMPARTMENT"></span><span id="error_wrong_compartment"></span>**\_compartimento errado de erro \_**
</dt> <dd> <dl> <dt>

1468 (0x5BC)
</dt> <dt>



O chamador fez a solicitação de conexão no compartimento de roteamento incorreto.


</dt> </dl> </dd> <dt>

<span id="ERROR_AUTHIP_FAILURE"></span><span id="error_authip_failure"></span>**ERRO de \_ AUTHIP da \_ falha**
</dt> <dd> <dl> <dt>

1469 (0x5BD)
</dt> <dt>



Houve uma falha de AuthIP ao tentar se conectar ao host remoto.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_NVRAM_RESOURCES"></span><span id="error_no_nvram_resources"></span>**ERRO \_ nenhum \_ recurso de NVRAM \_**
</dt> <dd> <dl> <dt>

1470 (0x5BE)
</dt> <dt>



Existem recursos de NVRAM insuficientes para concluir o serviço solicitado. Uma reinicialização pode ser necessária.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_GUI_PROCESS"></span><span id="error_not_gui_process"></span>**ERRO \_ não \_ processo de GUI \_**
</dt> <dd> <dl> <dt>

1471 (0x5BF)
</dt> <dt>



Não é possível concluir a operação solicitada porque o processo especificado não é um processo de GUI.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVENTLOG_FILE_CORRUPT"></span><span id="error_eventlog_file_corrupt"></span>**ERRO \_ de \_ arquivo EventLog \_ corrompido**
</dt> <dd> <dl> <dt>

1500 (0x5DC)
</dt> <dt>



O arquivo de log de eventos está corrompido.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVENTLOG_CANT_START"></span><span id="error_eventlog_cant_start"></span>**ERRO \_ EventLog não \_ consegue \_ Iniciar**
</dt> <dd> <dl> <dt>

1501 (0x5DD)
</dt> <dt>



Nenhum arquivo de log de eventos pôde ser aberto, portanto, o serviço de log de eventos não foi iniciado.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_FILE_FULL"></span><span id="error_log_file_full"></span>**arquivo de log de erros \_ \_ \_ completo**
</dt> <dd> <dl> <dt>

1502 (0x5DE)
</dt> <dt>



O arquivo de log de eventos está cheio.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVENTLOG_FILE_CHANGED"></span><span id="error_eventlog_file_changed"></span>**ERRO \_ de \_ arquivo EventLog \_ alterado**
</dt> <dd> <dl> <dt>

1503 (0x5DF)
</dt> <dt>



O arquivo de log de eventos foi alterado entre operações de leitura.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_TASK_NAME"></span><span id="error_invalid_task_name"></span>**nome da tarefa de erro \_ inválido \_ \_**
</dt> <dd> <dl> <dt>

1550 (0x60E)
</dt> <dt>



O nome de tarefa especificado é inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_TASK_INDEX"></span><span id="error_invalid_task_index"></span>**ERRO \_ de \_ índice de tarefa inválido \_**
</dt> <dd> <dl> <dt>

1551 (0x60F)
</dt> <dt>



O índice de tarefa especificado é inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_THREAD_ALREADY_IN_TASK"></span><span id="error_thread_already_in_task"></span>**\_thread \_ de erro já está \_ na \_ tarefa**
</dt> <dd> <dl> <dt>

1552 (0x610)
</dt> <dt>



O thread especificado já está ingressando em uma tarefa.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_SERVICE_FAILURE"></span><span id="error_install_service_failure"></span>**ERRO \_ ao \_ instalar \_ falha do serviço**
</dt> <dd> <dl> <dt>

1601 (0x641)
</dt> <dt>



Não foi possível acessar o serviço de Windows Installer. Isso pode ocorrer se o Windows Installer não estiver instalado corretamente. Contate a equipe de suporte para obter assistência.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_USEREXIT"></span><span id="error_install_userexit"></span>**ERRO ao \_ instalar o \_ UserExit**
</dt> <dd> <dl> <dt>

1602 (0x642)
</dt> <dt>



O usuário cancelou a instalação.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_FAILURE"></span><span id="error_install_failure"></span>**\_falha na instalação do erro \_**
</dt> <dd> <dl> <dt>

1603 (0x643)
</dt> <dt>



Erro fatal durante a instalação.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_SUSPEND"></span><span id="error_install_suspend"></span>**ERRO ao \_ instalar \_ suspensão**
</dt> <dd> <dl> <dt>

1604 (0x644)
</dt> <dt>



Instalação suspensa, incompleta.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNKNOWN_PRODUCT"></span><span id="error_unknown_product"></span>**ERRO \_ de \_ produto desconhecido**
</dt> <dd> <dl> <dt>

1605 (0x645)
</dt> <dt>



Esta ação só é válida para produtos que estão instalados no momento.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNKNOWN_FEATURE"></span><span id="error_unknown_feature"></span>**ERRO \_ desconhecido \_ recurso**
</dt> <dd> <dl> <dt>

1606 (0x646)
</dt> <dt>



ID do recurso não registrada.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNKNOWN_COMPONENT"></span><span id="error_unknown_component"></span>**ERRO \_ de \_ componente desconhecido**
</dt> <dd> <dl> <dt>

1607 (0x647)
</dt> <dt>



ID do componente não registrada.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNKNOWN_PROPERTY"></span><span id="error_unknown_property"></span>**ERRO \_ de \_ Propriedade desconhecida**
</dt> <dd> <dl> <dt>

1608 (0x648)
</dt> <dt>



Propriedade desconhecida.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_HANDLE_STATE"></span><span id="error_invalid_handle_state"></span>**ERRO \_ de \_ identificador de \_ estado inválido**
</dt> <dd> <dl> <dt>

1609 (0x649)
</dt> <dt>



O identificador está em um estado inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_CONFIGURATION"></span><span id="error_bad_configuration"></span>**ERRO \_ de \_ configuração incorreta**
</dt> <dd> <dl> <dt>

1610 (0x64A)
</dt> <dt>



Os dados de configuração deste produto estão corrompidos. Contate a equipe de suporte.


</dt> </dl> </dd> <dt>

<span id="ERROR_INDEX_ABSENT"></span><span id="error_index_absent"></span>**índice de erro \_ \_ ausente**
</dt> <dd> <dl> <dt>

1611 (0x64B)
</dt> <dt>



Qualificador de componente não presente.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_SOURCE_ABSENT"></span><span id="error_install_source_absent"></span>**ERRO \_ de \_ origem de instalação \_ ausente**
</dt> <dd> <dl> <dt>

1612 (0x64C)
</dt> <dt>



A origem da instalação para este produto não está disponível. Verifique se a origem existe e se você pode acessá-la.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_PACKAGE_VERSION"></span><span id="error_install_package_version"></span>**ERRO ao \_ instalar a \_ versão do pacote \_**
</dt> <dd> <dl> <dt>

1613 (0x64D)
</dt> <dt>



Este pacote de instalação não pode ser instalado pelo serviço de Windows Installer. Você deve instalar um service pack do Windows que contenha uma versão mais recente do serviço Windows Installer.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRODUCT_UNINSTALLED"></span><span id="error_product_uninstalled"></span>**produto de erro \_ \_ desinstalado**
</dt> <dd> <dl> <dt>

1614 (0x64E)
</dt> <dt>



O produto será desinstalado.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_QUERY_SYNTAX"></span><span id="error_bad_query_syntax"></span>**ERRO \_ de \_ sintaxe de consulta inadequada \_**
</dt> <dd> <dl> <dt>

1615 (0x64F)
</dt> <dt>



Sintaxe de consulta SQL inválida ou sem suporte.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_FIELD"></span><span id="error_invalid_field"></span>**campo de erro \_ inválido \_**
</dt> <dd> <dl> <dt>

1616 (0x650)
</dt> <dt>



O campo de registro não existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_REMOVED"></span><span id="error_device_removed"></span>**dispositivo de erro \_ \_ removido**
</dt> <dd> <dl> <dt>

1617 (0x651)
</dt> <dt>



O dispositivo foi removido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_ALREADY_RUNNING"></span><span id="error_install_already_running"></span>**ERRO de \_ instalação \_ já \_ em execução**
</dt> <dd> <dl> <dt>

1618 (0x652)
</dt> <dt>



Outra instalação já está em andamento. Conclua essa instalação antes de prosseguir com esta instalação.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_PACKAGE_OPEN_FAILED"></span><span id="error_install_package_open_failed"></span>**ERRO \_ \_ falha ao \_ abrir o pacote de instalação \_**
</dt> <dd> <dl> <dt>

1619 (0x653)
</dt> <dt>



Não foi possível abrir este pacote de instalação. Verifique se o pacote existe e se você pode acessá-lo ou contate o fornecedor do aplicativo para verificar se esse é um pacote de Windows Installer válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_PACKAGE_INVALID"></span><span id="error_install_package_invalid"></span>**ERRO ao \_ instalar o \_ pacote \_ inválido**
</dt> <dd> <dl> <dt>

1620 (0x654)
</dt> <dt>



Não foi possível abrir este pacote de instalação. Contate o fornecedor do aplicativo para verificar se este é um pacote de Windows Installer válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_UI_FAILURE"></span><span id="error_install_ui_failure"></span>**ERRO ao \_ instalar \_ falha da interface do usuário \_**
</dt> <dd> <dl> <dt>

1621 (0x655)
</dt> <dt>



Erro ao iniciar a interface do usuário do serviço de Windows Installer. Contate a equipe de suporte.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_LOG_FAILURE"></span><span id="error_install_log_failure"></span>**ERRO \_ ao \_ instalar \_ falha no log**
</dt> <dd> <dl> <dt>

1622 (0x656)
</dt> <dt>



Erro ao abrir o arquivo de log de instalação. Verifique se o local do arquivo de log especificado existe e se você pode gravar nele.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_LANGUAGE_UNSUPPORTED"></span><span id="error_install_language_unsupported"></span>**ERRO ao \_ instalar o \_ idioma \_ sem suporte**
</dt> <dd> <dl> <dt>

1623 (0x657)
</dt> <dt>



O idioma deste pacote de instalação não é suportado pelo seu sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_TRANSFORM_FAILURE"></span><span id="error_install_transform_failure"></span>**ERRO ao \_ instalar a \_ falha de transformação \_**
</dt> <dd> <dl> <dt>

1624 (0x658)
</dt> <dt>



Erro ao aplicar transformações. Verifique se os caminhos de transformação especificados são válidos.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_PACKAGE_REJECTED"></span><span id="error_install_package_rejected"></span>**ERRO ao \_ instalar \_ pacote \_ rejeitado**
</dt> <dd> <dl> <dt>

1625 (0x659)
</dt> <dt>



Essa instalação é proibida pela política do sistema. Entre em contato com o administrador do sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_FUNCTION_NOT_CALLED"></span><span id="error_function_not_called"></span>**função de erro \_ \_ não \_ chamada**
</dt> <dd> <dl> <dt>

1626 (0x65A)
</dt> <dt>



A função não pôde ser executada.


</dt> </dl> </dd> <dt>

<span id="ERROR_FUNCTION_FAILED"></span><span id="error_function_failed"></span>**\_falha na função de erro \_**
</dt> <dd> <dl> <dt>

1627 (0x65B)
</dt> <dt>



A função falhou durante a execução.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_TABLE"></span><span id="error_invalid_table"></span>**ERRO \_ de \_ tabela inválida**
</dt> <dd> <dl> <dt>

1628 (0x65C)
</dt> <dt>



Tabela inválida ou desconhecida especificada.


</dt> </dl> </dd> <dt>

<span id="ERROR_DATATYPE_MISMATCH"></span><span id="error_datatype_mismatch"></span>**tipo de dados de erro \_ \_ incompatível**
</dt> <dd> <dl> <dt>

1629 (0x65D)
</dt> <dt>



Os dados fornecidos são do tipo incorreto.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNSUPPORTED_TYPE"></span><span id="error_unsupported_type"></span>**ERRO de \_ tipo sem suporte \_**
</dt> <dd> <dl> <dt>

1630 (0x65E)
</dt> <dt>



Não há suporte para dados desse tipo.


</dt> </dl> </dd> <dt>

<span id="ERROR_CREATE_FAILED"></span><span id="error_create_failed"></span>**\_ \_ falha ao criar erro**
</dt> <dd> <dl> <dt>

1631 (0x65F)
</dt> <dt>



Falha ao iniciar o serviço de Windows Installer. Contate a equipe de suporte.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_TEMP_UNWRITABLE"></span><span id="error_install_temp_unwritable"></span>**ERRO ao \_ instalar o \_ Temp não \_ gravável**
</dt> <dd> <dl> <dt>

1632 (0x660)
</dt> <dt>



A pasta temporária está em uma unidade que está cheia ou está inacessível. Libere espaço na unidade ou verifique se você tem permissão de gravação na pasta Temp.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_PLATFORM_UNSUPPORTED"></span><span id="error_install_platform_unsupported"></span>**ERRO ao \_ instalar \_ plataforma \_ sem suporte**
</dt> <dd> <dl> <dt>

1633 (0x661)
</dt> <dt>



Este pacote de instalação não tem suporte deste tipo de processador. Contate o fornecedor do produto.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_NOTUSED"></span><span id="error_install_notused"></span>**ERRO de \_ instalação \_ não usada**
</dt> <dd> <dl> <dt>

1634 (0x662)
</dt> <dt>



Componente não usado neste computador.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATCH_PACKAGE_OPEN_FAILED"></span><span id="error_patch_package_open_failed"></span>**ERRO \_ \_ ao abrir o pacote de patches \_ \_**
</dt> <dd> <dl> <dt>

1635 (0x663)
</dt> <dt>



Não foi possível abrir este pacote de atualização. Verifique se o pacote de atualização existe e se você pode acessá-lo ou contate o fornecedor do aplicativo para verificar se este é um pacote de atualização de Windows Installer válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATCH_PACKAGE_INVALID"></span><span id="error_patch_package_invalid"></span>**ERRO \_ de \_ pacote de patch \_ inválido**
</dt> <dd> <dl> <dt>

1636 (0x664)
</dt> <dt>



Não foi possível abrir este pacote de atualização. Contate o fornecedor do aplicativo para verificar se este é um pacote de atualização de Windows Installer válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATCH_PACKAGE_UNSUPPORTED"></span><span id="error_patch_package_unsupported"></span>**pacote de patch de erro \_ \_ \_ sem suporte**
</dt> <dd> <dl> <dt>

1637 (0x665)
</dt> <dt>



Este pacote de atualização não pode ser processado pelo serviço de Windows Installer. Você deve instalar um service pack do Windows que contenha uma versão mais recente do serviço Windows Installer.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRODUCT_VERSION"></span><span id="error_product_version"></span>**\_versão do produto de erro \_**
</dt> <dd> <dl> <dt>

1638 (0x666)
</dt> <dt>



Outra versão deste produto já está instalada. Não é possível continuar a instalação desta versão. Para configurar ou remover a versão existente deste produto, use adicionar/remover programas no painel de controle.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_COMMAND_LINE"></span><span id="error_invalid_command_line"></span>**ERRO \_ de \_ linha de comando inválida \_**
</dt> <dd> <dl> <dt>

1639 (0x667)
</dt> <dt>



Argumento de linha de comando inválido. Consulte o SDK do Windows Installer para obter ajuda de linha de comando detalhada.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_REMOTE_DISALLOWED"></span><span id="error_install_remote_disallowed"></span>**ERRO ao \_ instalar \_ remoto não \_ permitido**
</dt> <dd> <dl> <dt>

1640 (0x668)
</dt> <dt>



Somente os administradores têm permissão para adicionar, remover ou configurar o software do servidor durante uma sessão remota dos serviços de terminal. Se você quiser instalar ou configurar o software no servidor, entre em contato com o administrador da rede.


</dt> </dl> </dd> <dt>

<span id="ERROR_SUCCESS_REBOOT_INITIATED"></span><span id="error_success_reboot_initiated"></span>**ERRO \_ de \_ reinicialização de êxito \_ iniciada**
</dt> <dd> <dl> <dt>

1641 (0x669)
</dt> <dt>



A operação solicitada foi concluída com êxito. O sistema será reiniciado para que as alterações entrem em vigor.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATCH_TARGET_NOT_FOUND"></span><span id="error_patch_target_not_found"></span>**ERRO \_ de \_ destino de patch \_ não \_ encontrado**
</dt> <dd> <dl> <dt>

1642 (0x66A)
</dt> <dt>



A atualização não pode ser instalada pelo serviço de Windows Installer porque o programa a ser atualizado pode estar ausente ou a atualização pode atualizar uma versão diferente do programa. Verifique se o programa a ser atualizado existe no computador e se você tem a atualização correta.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATCH_PACKAGE_REJECTED"></span><span id="error_patch_package_rejected"></span>**ERRO \_ de \_ pacote de patch \_ rejeitado**
</dt> <dd> <dl> <dt>

1643 (0x66B)
</dt> <dt>



O pacote de atualização não é permitido pela política de restrição de software.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_TRANSFORM_REJECTED"></span><span id="error_install_transform_rejected"></span>**ERRO ao \_ instalar a \_ transformação \_ rejeitada**
</dt> <dd> <dl> <dt>

1644 (0x66C)
</dt> <dt>



Uma ou mais personalizações não são permitidas pela política de restrição de software.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_REMOTE_PROHIBITED"></span><span id="error_install_remote_prohibited"></span>**ERRO ao \_ instalar \_ remoto \_ proibido**
</dt> <dd> <dl> <dt>

1645 (0x66D)
</dt> <dt>



O Windows Installer não permite a instalação de um Conexão de Área de Trabalho Remota.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATCH_REMOVAL_UNSUPPORTED"></span><span id="error_patch_removal_unsupported"></span>**remoção de patch de erro \_ \_ \_ sem suporte**
</dt> <dd> <dl> <dt>

1646 (0x66E)
</dt> <dt>



Não há suporte para a desinstalação do pacote de atualização.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNKNOWN_PATCH"></span><span id="error_unknown_patch"></span>**ERRO \_ de \_ patch desconhecido**
</dt> <dd> <dl> <dt>

1647 (0x66F)
</dt> <dt>



A atualização não é aplicada a este produto.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATCH_NO_SEQUENCE"></span><span id="error_patch_no_sequence"></span>**PATCH de erro \_ \_ sem \_ sequência**
</dt> <dd> <dl> <dt>

1648 (0x670)
</dt> <dt>



Nenhuma sequência válida foi encontrada para o conjunto de atualizações.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATCH_REMOVAL_DISALLOWED"></span><span id="error_patch_removal_disallowed"></span>**remoção de patch de erro não \_ \_ \_ permitida**
</dt> <dd> <dl> <dt>

1649 (0x671)
</dt> <dt>



A remoção da atualização não foi permitida pela política.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PATCH_XML"></span><span id="error_invalid_patch_xml"></span>**ERRO \_ \_ XML de patch inválido \_**
</dt> <dd> <dl> <dt>

1650 (0x672)
</dt> <dt>



Os dados de atualização XML são inválidos.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATCH_MANAGED_ADVERTISED_PRODUCT"></span><span id="error_patch_managed_advertised_product"></span>**ERRO \_ de \_ \_ produto anunciado gerenciado por patch \_**
</dt> <dd> <dl> <dt>

1651 (0x673)
</dt> <dt>



Windows Installer não permite a atualização de produtos anunciados gerenciados. Pelo menos um recurso do produto deve ser instalado antes da aplicação da atualização.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_SERVICE_SAFEBOOT"></span><span id="error_install_service_safeboot"></span>**ERRO ao \_ instalar o \_ serviço de \_ inicialização segura**
</dt> <dd> <dl> <dt>

1652 (0x674)
</dt> <dt>



O serviço de Windows Installer não está acessível no modo de segurança. Tente novamente quando o computador não estiver no modo de segurança ou você pode usar a restauração do sistema para retornar o computador a um estado bom anterior.


</dt> </dl> </dd> <dt>

<span id="ERROR_FAIL_FAST_EXCEPTION"></span><span id="error_fail_fast_exception"></span>**exceção de erro com \_ falha \_ rápida \_**
</dt> <dd> <dl> <dt>

1653 (0x675)
</dt> <dt>



Ocorreu uma exceção fail fast. Os manipuladores de exceção não serão invocados e o processo será encerrado imediatamente.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_REJECTED"></span><span id="error_install_rejected"></span>**instalação de erro \_ \_ rejeitada**
</dt> <dd> <dl> <dt>

1654 (0x676)
</dt> <dt>



O aplicativo que você está tentando executar não tem suporte nesta versão do Windows.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>WinError. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Códigos de erro do sistema](system-error-codes.md)
</dt> </dl>

 

 




