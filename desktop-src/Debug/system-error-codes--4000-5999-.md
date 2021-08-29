---
description: Descreve os códigos de erro 4000-5999 definidos no arquivo de cabeçalho WinError. h e destina-se a desenvolvedores.
ms.assetid: 1d2f7160-6322-4c75-abbc-4a882bbdf7ce
title: Códigos de erro do sistema (4000-5999) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: ada3f091671fd865f76faa830b89393ecc80176021a4990a71d4715886a3ffea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956925"
---
# <a name="system-error-codes-4000-5999"></a>Códigos de erro do sistema (4000-5999)

> [!NOTE]
> Essas informações destinam-se a desenvolvedores Depurando erros do sistema. para outros erros, como problemas com Windows Update, há uma lista de recursos na página códigos de [erro](system-error-codes.md) .

A lista a seguir descreve os [códigos de erro do sistema](system-error-codes.md) para erros 4000 a 5999. Elas são retornadas pela função [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) quando muitas funções falham. Para recuperar o texto de descrição do erro em seu aplicativo, use a função [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) com a **mensagem de formato \_ \_ do sinalizador do \_ sistema** .

<dl> <dt>

<span id="ERROR_WINS_INTERNAL"></span><span id="error_wins_internal"></span>**ERRO \_ interno do WINS \_**
</dt> <dd> <dl> <dt>

4000 (0xFA0)
</dt> <dt>



O WINS encontrou um erro ao processar o comando.


</dt> </dl> </dd> <dt>

<span id="ERROR_CAN_NOT_DEL_LOCAL_WINS"></span><span id="error_can_not_del_local_wins"></span>**ERRO \_ não é possível \_ \_ excluir o \_ \_ WINS local**
</dt> <dd> <dl> <dt>

4001 (0xFA1)
</dt> <dt>



O WINS local não pode ser excluído.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATIC_INIT"></span><span id="error_static_init"></span>**ERRO \_ de \_ inicialização estática**
</dt> <dd> <dl> <dt>

4002 (0xFA2)
</dt> <dt>



Falha na importação do arquivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_INC_BACKUP"></span><span id="error_inc_backup"></span>**BACKUP do ERROR \_ Inc \_**
</dt> <dd> <dl> <dt>

4003 (0xFA3)
</dt> <dt>



Falha no backup. Um backup completo foi feito antes?


</dt> </dl> </dd> <dt>

<span id="ERROR_FULL_BACKUP"></span><span id="error_full_backup"></span>**ERRO \_ de \_ backup completo**
</dt> <dd> <dl> <dt>

4004 (0xFA4)
</dt> <dt>



Falha no backup. Verifique o diretório para o qual você está fazendo backup do banco de dados.


</dt> </dl> </dd> <dt>

<span id="ERROR_REC_NON_EXISTENT"></span><span id="error_rec_non_existent"></span>**o erro \_ REC \_ não \_ existe**
</dt> <dd> <dl> <dt>

4005 (0xFA5)
</dt> <dt>



O nome não existe no banco de dados WINS.


</dt> </dl> </dd> <dt>

<span id="ERROR_RPL_NOT_ALLOWED"></span><span id="error_rpl_not_allowed"></span>**ERRO \_ RPL \_ não \_ permitido**
</dt> <dd> <dl> <dt>

4006 (0xFA6)
</dt> <dt>



A replicação com um parceiro não configurado não é permitida.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_CONTENTINFO_VERSION_UNSUPPORTED"></span><span id="peerdist_error_contentinfo_version_unsupported"></span>**\_versão do CONTENTINFO de erro PEERDIST \_ \_ \_ sem suporte**
</dt> <dd> <dl> <dt>

4050 (0xFD2)
</dt> <dt>



Não há suporte para a versão das informações de conteúdo fornecidas.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_CANNOT_PARSE_CONTENTINFO"></span><span id="peerdist_error_cannot_parse_contentinfo"></span>**\_erro PEERDIST \_ não pode \_ analisar \_ CONTENTINFO**
</dt> <dd> <dl> <dt>

4051 (0xFD3)
</dt> <dt>



As informações de conteúdo fornecidas estão malformadas.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_MISSING_DATA"></span><span id="peerdist_error_missing_data"></span>**\_ \_ dados ausentes no erro PEERDIST \_**
</dt> <dd> <dl> <dt>

4052 (0xFD4)
</dt> <dt>



Os dados solicitados não podem ser encontrados em caches locais ou pares.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_NO_MORE"></span><span id="peerdist_error_no_more"></span>**\_ \_ não há mais erro no PEERDIST \_**
</dt> <dd> <dl> <dt>

4053 (0xFD5)
</dt> <dt>



Não há mais dados disponíveis ou necessários.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_NOT_INITIALIZED"></span><span id="peerdist_error_not_initialized"></span>**\_erro PEERDIST \_ não \_ inicializado**
</dt> <dd> <dl> <dt>

4054 (0xFD6)
</dt> <dt>



O objeto fornecido não foi inicializado.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_ALREADY_INITIALIZED"></span><span id="peerdist_error_already_initialized"></span>**\_erro PEERDIST \_ já \_ inicializado**
</dt> <dd> <dl> <dt>

4055 (0xFD7)
</dt> <dt>



O objeto fornecido já foi inicializado.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_SHUTDOWN_IN_PROGRESS"></span><span id="peerdist_error_shutdown_in_progress"></span>**\_ \_ desligamento \_ de erro PEERDIST em \_ andamento**
</dt> <dd> <dl> <dt>

4056 (0xFD8)
</dt> <dt>



Uma operação de desligamento já está em andamento.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_INVALIDATED"></span><span id="peerdist_error_invalidated"></span>**\_erro PEERDIST \_ invalidado**
</dt> <dd> <dl> <dt>

4057 (0xFD9)
</dt> <dt>



O objeto fornecido já foi invalidado.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_ALREADY_EXISTS"></span><span id="peerdist_error_already_exists"></span>**o \_ erro PEERDIST \_ já \_ existe**
</dt> <dd> <dl> <dt>

4058 (0xFDA)
</dt> <dt>



Um elemento já existe e não foi substituído.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_OPERATION_NOTFOUND"></span><span id="peerdist_error_operation_notfound"></span>**operação de erro PEERDIST não \_ \_ \_ encontrada**
</dt> <dd> <dl> <dt>

4059 (0xFDB)
</dt> <dt>



Não é possível cancelar a operação solicitada, pois ela já foi concluída.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_ALREADY_COMPLETED"></span><span id="peerdist_error_already_completed"></span>**\_erro PEERDIST \_ já \_ concluído**
</dt> <dd> <dl> <dt>

4060 (0xFDC)
</dt> <dt>



Não é possível executar a operação solicitada porque ela já foi executada.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_OUT_OF_BOUNDS"></span><span id="peerdist_error_out_of_bounds"></span>**\_erro PEERDIST \_ fora \_ dos \_ limites**
</dt> <dd> <dl> <dt>

4061 (0xFDD)
</dt> <dt>



Uma operação acessou dados além dos limites de dados válidos.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_VERSION_UNSUPPORTED"></span><span id="peerdist_error_version_unsupported"></span>**\_versão de erro PEERDIST \_ \_ sem suporte**
</dt> <dd> <dl> <dt>

4062 (0xFDE)
</dt> <dt>



Não há suporte para a versão solicitada.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_INVALID_CONFIGURATION"></span><span id="peerdist_error_invalid_configuration"></span>**\_ \_ Configuração inválida de erro PEERDIST \_**
</dt> <dd> <dl> <dt>

4063 (0xFDF)
</dt> <dt>



Um valor de configuração é inválido.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_NOT_LICENSED"></span><span id="peerdist_error_not_licensed"></span>**\_erro PEERDIST \_ não \_ licenciado**
</dt> <dd> <dl> <dt>

4064 (0xFE0)
</dt> <dt>



A SKU não está licenciada.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_SERVICE_UNAVAILABLE"></span><span id="peerdist_error_service_unavailable"></span>**\_serviço de erro PEERDIST \_ \_ indisponível**
</dt> <dd> <dl> <dt>

4065 (0xFE1)
</dt> <dt>



O serviço PeerDist ainda está sendo inicializado e estará disponível em breve.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_TRUST_FAILURE"></span><span id="peerdist_error_trust_failure"></span>**\_falha de \_ confiança de erro PEERDIST \_**
</dt> <dd> <dl> <dt>

4066 (0xFE2)
</dt> <dt>



A comunicação com um ou mais computadores será temporariamente bloqueada devido a erros recentes.


</dt> </dl> </dd> <dt>

<span id="ERROR_DHCP_ADDRESS_CONFLICT"></span><span id="error_dhcp_address_conflict"></span>**ERRO \_ de \_ conflito de endereço DHCP \_**
</dt> <dd> <dl> <dt>

4100 (0x1004)
</dt> <dt>



O cliente DHCP obteve um endereço IP que já está em uso na rede. A interface local será desabilitada até que o cliente DHCP possa obter um novo endereço.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_GUID_NOT_FOUND"></span><span id="error_wmi_guid_not_found"></span>**ERRO \_ \_ GUID WMI \_ não \_ encontrado**
</dt> <dd> <dl> <dt>

4200 (0x1068)
</dt> <dt>



O GUID passado não foi reconhecido como válido por um provedor de dados WMI.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_INSTANCE_NOT_FOUND"></span><span id="error_wmi_instance_not_found"></span>**ERRO \_ de \_ instância WMI \_ não \_ encontrada**
</dt> <dd> <dl> <dt>

4201 (0x1069)
</dt> <dt>



O nome da instância passado não foi reconhecido como válido por um provedor de dados WMI.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_ITEMID_NOT_FOUND"></span><span id="error_wmi_itemid_not_found"></span>**ERRO \_ WMI \_ ItemId \_ não \_ encontrado**
</dt> <dd> <dl> <dt>

4202 (0x106A)
</dt> <dt>



A ID do item de dados passada não foi reconhecida como válida por um provedor de dados WMI.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_TRY_AGAIN"></span><span id="error_wmi_try_again"></span>**ERRO de \_ WMI \_ tente \_ novamente**
</dt> <dd> <dl> <dt>

4203 (0x106B)
</dt> <dt>



A solicitação WMI não pôde ser concluída e deve ser repetida.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_DP_NOT_FOUND"></span><span id="error_wmi_dp_not_found"></span>**ERRO do \_ WMI \_ DP \_ não \_ encontrado**
</dt> <dd> <dl> <dt>

4204 (0x106C)
</dt> <dt>



Não foi possível localizar o provedor de dados WMI.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_UNRESOLVED_INSTANCE_REF"></span><span id="error_wmi_unresolved_instance_ref"></span>**ERRO \_ \_ referência de instância não resolvida do WMI \_ \_**
</dt> <dd> <dl> <dt>

4205 (0x106D)
</dt> <dt>



O provedor de dados WMI faz referência a um conjunto de instâncias que não foi registrado.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_ALREADY_ENABLED"></span><span id="error_wmi_already_enabled"></span>**ERRO o \_ WMI \_ já está \_ habilitado**
</dt> <dd> <dl> <dt>

4206 (0x106E)
</dt> <dt>



A notificação de eventos ou o bloco de dados do WMI já foi habilitado.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_GUID_DISCONNECTED"></span><span id="error_wmi_guid_disconnected"></span>**ERRO \_ \_ GUID WMI \_ desconectado**
</dt> <dd> <dl> <dt>

4207 (0x106F)
</dt> <dt>



O bloco de dados WMI não está mais disponível.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_SERVER_UNAVAILABLE"></span><span id="error_wmi_server_unavailable"></span>**ERRO \_ o \_ servidor WMI \_ não está disponível**
</dt> <dd> <dl> <dt>

4208 (0x1070)
</dt> <dt>



O serviço de dados WMI não está disponível.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_DP_FAILED"></span><span id="error_wmi_dp_failed"></span>**ERRO \_ \_ \_ falha no WMI DP**
</dt> <dd> <dl> <dt>

4209 (0x1071)
</dt> <dt>



Falha do provedor de dados WMI ao executar a solicitação.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_INVALID_MOF"></span><span id="error_wmi_invalid_mof"></span>**ERRO \_ \_ MOF inválido do WMI \_**
</dt> <dd> <dl> <dt>

4210 (0x1072)
</dt> <dt>



As informações do WMI MOF não são válidas.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_INVALID_REGINFO"></span><span id="error_wmi_invalid_reginfo"></span>**ERRO \_ \_ REGINFO inválido do WMI \_**
</dt> <dd> <dl> <dt>

4211 (0x1073)
</dt> <dt>



As informações de registro do WMI não são válidas.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_ALREADY_DISABLED"></span><span id="error_wmi_already_disabled"></span>**ERRO o \_ WMI \_ já está \_ desabilitado**
</dt> <dd> <dl> <dt>

4212 (0x1074)
</dt> <dt>



A notificação de eventos ou o bloco de dados do WMI já foi desabilitado.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_READ_ONLY"></span><span id="error_wmi_read_only"></span>**ERRO \_ \_ somente leitura do WMI \_**
</dt> <dd> <dl> <dt>

4213 (0x1075)
</dt> <dt>



O bloco de dados ou o item de dados WMI é somente leitura.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_SET_FAILURE"></span><span id="error_wmi_set_failure"></span>**ERRO \_ ao \_ definir \_ falha do WMI**
</dt> <dd> <dl> <dt>

4214 (0x1076)
</dt> <dt>



Não foi possível alterar o bloco de dados ou o item de dados WMI.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_APPCONTAINER"></span><span id="error_not_appcontainer"></span>**ERRO \_ não \_ APPCONTAINER**
</dt> <dd> <dl> <dt>

4250 (0x109A)
</dt> <dt>



Esta operação só é válida no contexto de um contêiner de aplicativo.


</dt> </dl> </dd> <dt>

<span id="ERROR_APPCONTAINER_REQUIRED"></span><span id="error_appcontainer_required"></span>**ERRO de \_ APPCONTAINER \_ necessário**
</dt> <dd> <dl> <dt>

4251 (0x109B)
</dt> <dt>



Este aplicativo só pode ser executado no contexto de um contêiner de aplicativo.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SUPPORTED_IN_APPCONTAINER"></span><span id="error_not_supported_in_appcontainer"></span>**ERRO \_ sem \_ suporte \_ no \_ APPCONTAINER**
</dt> <dd> <dl> <dt>

4252 (0x109C)
</dt> <dt>



Não há suporte para essa funcionalidade no contexto de um contêiner de aplicativo.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PACKAGE_SID_LENGTH"></span><span id="error_invalid_package_sid_length"></span>**ERRO \_ de \_ \_ comprimento de Sid de pacote inválido \_**
</dt> <dd> <dl> <dt>

4253 (0x109D)
</dt> <dt>



O comprimento do SID fornecido não é um comprimento válido para SIDs de contêiner de aplicativo.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MEDIA"></span><span id="error_invalid_media"></span>**\_mídia inválida de erro \_**
</dt> <dd> <dl> <dt>

4300 (0x10CC)
</dt> <dt>



O identificador de mídia não representa um meio válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LIBRARY"></span><span id="error_invalid_library"></span>**ERRO \_ de \_ biblioteca inválida**
</dt> <dd> <dl> <dt>

4301 (0x10CD)
</dt> <dt>



O identificador de biblioteca não representa uma biblioteca válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MEDIA_POOL"></span><span id="error_invalid_media_pool"></span>**ERRO \_ de \_ pool de mídia inválido \_**
</dt> <dd> <dl> <dt>

4302 (0x10CE)
</dt> <dt>



O identificador do pool de mídias não representa um pool de mídia válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_DRIVE_MEDIA_MISMATCH"></span><span id="error_drive_media_mismatch"></span>**incompatibilidade de mídia de unidade de erro \_ \_ \_**
</dt> <dd> <dl> <dt>

4303 (0x10CF)
</dt> <dt>



A unidade e a mídia não são compatíveis ou existem em bibliotecas diferentes.


</dt> </dl> </dd> <dt>

<span id="ERROR_MEDIA_OFFLINE"></span><span id="error_media_offline"></span>**mídia de erro \_ \_ offline**
</dt> <dd> <dl> <dt>

4304 (0x10D0)
</dt> <dt>



A mídia existe atualmente em uma biblioteca offline e deve estar online para executar esta operação.


</dt> </dl> </dd> <dt>

<span id="ERROR_LIBRARY_OFFLINE"></span><span id="error_library_offline"></span>**biblioteca de erros \_ \_ offline**
</dt> <dd> <dl> <dt>

4305 (0x10D1)
</dt> <dt>



A operação não pode ser executada em uma biblioteca offline.


</dt> </dl> </dd> <dt>

<span id="ERROR_EMPTY"></span><span id="error_empty"></span>**ERRO \_ vazio**
</dt> <dd> <dl> <dt>

4306 (0x10D2)
</dt> <dt>



A biblioteca, a unidade ou o pool de mídia está vazio.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_EMPTY"></span><span id="error_not_empty"></span>**ERRO \_ não \_ vazio**
</dt> <dd> <dl> <dt>

4307 (0x10D3)
</dt> <dt>



A biblioteca, a unidade ou o pool de mídias devem estar vazios para executar esta operação.


</dt> </dl> </dd> <dt>

<span id="ERROR_MEDIA_UNAVAILABLE"></span><span id="error_media_unavailable"></span>**mídia de erro \_ \_ indisponível**
</dt> <dd> <dl> <dt>

4308 (0x10D4)
</dt> <dt>



Não há mídia disponível no momento neste pool de mídias ou biblioteca.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_DISABLED"></span><span id="error_resource_disabled"></span>**recurso de erro \_ \_ desabilitado**
</dt> <dd> <dl> <dt>

4309 (0x10D5)
</dt> <dt>



Um recurso necessário para esta operação está desabilitado.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_CLEANER"></span><span id="error_invalid_cleaner"></span>**ERRO \_ de \_ limpeza inválida**
</dt> <dd> <dl> <dt>

4310 (0x10D6)
</dt> <dt>



O identificador de mídia não representa um limpador válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_CLEAN"></span><span id="error_unable_to_clean"></span>**ERRO \_ não é possível \_ \_ limpar**
</dt> <dd> <dl> <dt>

4311 (0x10D7)
</dt> <dt>



A unidade não pode ser limpa ou não dá suporte à limpeza.


</dt> </dl> </dd> <dt>

<span id="ERROR_OBJECT_NOT_FOUND"></span><span id="error_object_not_found"></span>**objeto de erro \_ \_ não \_ encontrado**
</dt> <dd> <dl> <dt>

4312 (0x10D8)
</dt> <dt>



O identificador de objeto não representa um objeto válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_DATABASE_FAILURE"></span><span id="error_database_failure"></span>**\_falha no banco de dados de erro \_**
</dt> <dd> <dl> <dt>

4313 (0x10D9)
</dt> <dt>



Não é possível ler ou gravar no banco de dados.


</dt> </dl> </dd> <dt>

<span id="ERROR_DATABASE_FULL"></span><span id="error_database_full"></span>**ERRO de \_ banco de dados \_ cheio**
</dt> <dd> <dl> <dt>

4314 (0x10DA)
</dt> <dt>



O banco de dados está cheio.


</dt> </dl> </dd> <dt>

<span id="ERROR_MEDIA_INCOMPATIBLE"></span><span id="error_media_incompatible"></span>**mídia de erro \_ \_ incompatível**
</dt> <dd> <dl> <dt>

4315 (0x10DB)
</dt> <dt>



A mídia não é compatível com o dispositivo ou com o pool de mídias.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_NOT_PRESENT"></span><span id="error_resource_not_present"></span>**o \_ recurso de erro \_ não \_ está presente**
</dt> <dd> <dl> <dt>

4316 (0x10DC)
</dt> <dt>



O recurso necessário para esta operação não existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_OPERATION"></span><span id="error_invalid_operation"></span>**ERRO \_ de \_ operação inválida**
</dt> <dd> <dl> <dt>

4317 (0x10DD)
</dt> <dt>



O identificador de operação não é válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_MEDIA_NOT_AVAILABLE"></span><span id="error_media_not_available"></span>**mídia de erro \_ \_ não \_ disponível**
</dt> <dd> <dl> <dt>

4318 (0x10DE)
</dt> <dt>



A mídia não está montada ou pronta para uso.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_NOT_AVAILABLE"></span><span id="error_device_not_available"></span>**DISPOSITIVO \_ DE ERRO NÃO \_ \_ DISPONÍVEL**
</dt> <dd> <dl> <dt>

4319 (0x10DF)
</dt> <dt>



O dispositivo não está pronto para uso.


</dt> </dl> </dd> <dt>

<span id="ERROR_REQUEST_REFUSED"></span><span id="error_request_refused"></span>**SOLICITAÇÃO \_ DE \_ ERRO RECUSADA**
</dt> <dd> <dl> <dt>

4320 (0x10E0)
</dt> <dt>



O operador ou administrador recusou a solicitação.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DRIVE_OBJECT"></span><span id="error_invalid_drive_object"></span>**ERRO \_ OBJETO DE UNIDADE \_ \_ INVÁLIDO**
</dt> <dd> <dl> <dt>

4321 (0x10E1)
</dt> <dt>



O identificador de unidade não representa uma unidade válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_LIBRARY_FULL"></span><span id="error_library_full"></span>**BIBLIOTECA \_ DE ERROS \_ COMPLETA**
</dt> <dd> <dl> <dt>

4322 (0x10E2)
</dt> <dt>



A biblioteca está cheia. Nenhum slot está disponível para uso.


</dt> </dl> </dd> <dt>

<span id="ERROR_MEDIUM_NOT_ACCESSIBLE"></span><span id="error_medium_not_accessible"></span>**MEIO \_ DE ERRO NÃO \_ \_ ACESSÍVEL**
</dt> <dd> <dl> <dt>

4323 (0x10E3)
</dt> <dt>



O transporte não pode acessar a mídia.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_LOAD_MEDIUM"></span><span id="error_unable_to_load_medium"></span>**ERRO \_ NÃO É POSSÍVEL CARREGAR \_ \_ MÉDIO \_**
</dt> <dd> <dl> <dt>

4324 (0x10E4)
</dt> <dt>



Não é possível carregar o meio na unidade.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_INVENTORY_DRIVE"></span><span id="error_unable_to_inventory_drive"></span>**ERRO \_ NÃO É POSSÍVEL PARA A UNIDADE DE \_ \_ \_ INVENTÁRIO**
</dt> <dd> <dl> <dt>

4325 (0x10E5)
</dt> <dt>



Não é possível recuperar o status da unidade.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_INVENTORY_SLOT"></span><span id="error_unable_to_inventory_slot"></span>**ERRO \_ NÃO É POSSÍVEL PARA O SLOT DE \_ \_ \_ INVENTÁRIO**
</dt> <dd> <dl> <dt>

4326 (0x10E6)
</dt> <dt>



Não é possível recuperar o status do slot.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_INVENTORY_TRANSPORT"></span><span id="error_unable_to_inventory_transport"></span>**ERRO \_ NÃO É POSSÍVEL \_ \_ \_ INVENTARIAR TRANSPORTE**
</dt> <dd> <dl> <dt>

4327 (0x10E7)
</dt> <dt>



Não é possível recuperar o status sobre o transporte.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSPORT_FULL"></span><span id="error_transport_full"></span>**ERRO \_ TRANSPORTE \_ COMPLETO**
</dt> <dd> <dl> <dt>

4328 (0x10E8)
</dt> <dt>



Não é possível usar o transporte porque ele já está em uso.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONTROLLING_IEPORT"></span><span id="error_controlling_ieport"></span>**ERRO \_ AO CONTROLAR O \_ IEPORT**
</dt> <dd> <dl> <dt>

4329 (0x10E9)
</dt> <dt>



Não é possível abrir ou fechar a porta de injeção/ejetamento.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_EJECT_MOUNTED_MEDIA"></span><span id="error_unable_to_eject_mounted_media"></span>**ERRO \_ NÃO É POSSÍVEL \_ \_ \_ EJETAR A MÍDIA \_ MONTADA**
</dt> <dd> <dl> <dt>

4330 (0x10EA)
</dt> <dt>



Não é possível ejetar a mídia porque ela está em uma unidade.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLEANER_SLOT_SET"></span><span id="error_cleaner_slot_set"></span>**CONJUNTO DE \_ \_ SLOTS DE LIMPEZA \_ DE ERROS**
</dt> <dd> <dl> <dt>

4331 (0x10EB)
</dt> <dt>



Um slot de limpeza já está reservado.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLEANER_SLOT_NOT_SET"></span><span id="error_cleaner_slot_not_set"></span>**SLOT \_ DE LIMPEZA DE ERRO NÃO \_ \_ \_ DEFINIDO**
</dt> <dd> <dl> <dt>

4332 (0x10EC)
</dt> <dt>



Um slot de limpeza não é reservado.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLEANER_CARTRIDGE_SPENT"></span><span id="error_cleaner_cartridge_spent"></span>**LIMPEZA \_ DE ERRO LIMPEZA \_ GASTO \_**
</dt> <dd> <dl> <dt>

4333 (0x10ED)
</dt> <dt>



A limpeza de limpeza realizou o número máximo de limpezas de unidade.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNEXPECTED_OMID"></span><span id="error_unexpected_omid"></span>**ERRO \_ \_ OMID INESPERADO**
</dt> <dd> <dl> <dt>

4334 (0x10EE)
</dt> <dt>



Identificador em média inesperado.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_DELETE_LAST_ITEM"></span><span id="error_cant_delete_last_item"></span>**ERRO \_ NÃO PODE EXCLUIR O ÚLTIMO \_ \_ \_ ITEM**
</dt> <dd> <dl> <dt>

4335 (0x10EF)
</dt> <dt>



O último item restante neste grupo ou recurso não pode ser excluído.


</dt> </dl> </dd> <dt>

<span id="ERROR_MESSAGE_EXCEEDS_MAX_SIZE"></span><span id="error_message_exceeds_max_size"></span>**MENSAGEM \_ DE ERRO EXCEDE O TAMANHO \_ \_ \_ MÁXIMO**
</dt> <dd> <dl> <dt>

4336 (0x10F0)
</dt> <dt>



A mensagem fornecida excede o tamanho máximo permitido para esse parâmetro.


</dt> </dl> </dd> <dt>

<span id="ERROR_VOLUME_CONTAINS_SYS_FILES"></span><span id="error_volume_contains_sys_files"></span>**VOLUME \_ DE ERRO CONTÉM ARQUIVOS \_ \_ \_ SYS**
</dt> <dd> <dl> <dt>

4337 (0x10F1)
</dt> <dt>



O volume contém arquivos de sistema ou paging.


</dt> </dl> </dd> <dt>

<span id="ERROR_INDIGENOUS_TYPE"></span><span id="error_indigenous_type"></span>**TIPO \_ ERROR DIGITS \_**
</dt> <dd> <dl> <dt>

4338 (0x10F2)
</dt> <dt>



O tipo de mídia não pode ser removido dessa biblioteca, pois pelo menos uma unidade nos relatórios da biblioteca pode dar suporte a esse tipo de mídia.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUPPORTING_DRIVES"></span><span id="error_no_supporting_drives"></span>**ERRO \_ SEM UNIDADES DE \_ \_ SUPORTE**
</dt> <dd> <dl> <dt>

4339 (0x10F3)
</dt> <dt>



Essa mídia offline não pode ser montada nesse sistema, pois não há unidades habilitadas que possam ser usadas.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLEANER_CARTRIDGE_INSTALLED"></span><span id="error_cleaner_cartridge_installed"></span>**LIMPEZA \_ DE ERROS DE LIMPEZA \_ \_ INSTALADA**
</dt> <dd> <dl> <dt>

4340 (0x10F4)
</dt> <dt>



Um produto de limpeza está presente na biblioteca de fitas.


</dt> </dl> </dd> <dt>

<span id="ERROR_IEPORT_FULL"></span><span id="error_ieport_full"></span>**\_ERRO IEPORT \_ FULL**
</dt> <dd> <dl> <dt>

4341 (0x10F5)
</dt> <dt>



Não é possível usar a porta de injeção/ejetamento porque ela não está vazia.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_OFFLINE"></span><span id="error_file_offline"></span>**ARQUIVO \_ DE ERRO \_ OFFLINE**
</dt> <dd> <dl> <dt>

4350 (0x10FE)
</dt> <dt>



Atualmente, esse arquivo não está disponível para uso neste computador.


</dt> </dl> </dd> <dt>

<span id="ERROR_REMOTE_STORAGE_NOT_ACTIVE"></span><span id="error_remote_storage_not_active"></span>**ERRO \_ ARMAZENAMENTO REMOTO NÃO \_ \_ \_ ATIVO**
</dt> <dd> <dl> <dt>

4351 (0x10FF)
</dt> <dt>



O serviço de armazenamento remoto não está operacional no momento.


</dt> </dl> </dd> <dt>

<span id="ERROR_REMOTE_STORAGE_MEDIA_ERROR"></span><span id="error_remote_storage_media_error"></span>**ERRO DE \_ MÍDIA \_ DE ARMAZENAMENTO \_ \_ REMOTO**
</dt> <dd> <dl> <dt>

4352 (0x1100)
</dt> <dt>



O serviço de armazenamento remoto encontrou um erro de mídia.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_A_REPARSE_POINT"></span><span id="error_not_a_reparse_point"></span>**ERRO \_ NÃO É UM PONTO DE NOVA \_ \_ \_ PESQUISA**
</dt> <dd> <dl> <dt>

4390 (0x1126)
</dt> <dt>



O arquivo ou diretório não é um ponto de novaparção.


</dt> </dl> </dd> <dt>

<span id="ERROR_REPARSE_ATTRIBUTE_CONFLICT"></span><span id="error_reparse_attribute_conflict"></span>**ERRO \_ REPARSE \_ ATTRIBUTE \_ CONFLICT**
</dt> <dd> <dl> <dt>

4391 (0x1127)
</dt> <dt>



O atributo de ponto de reparse não pode ser definido porque está em conflito com um atributo existente.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_REPARSE_DATA"></span><span id="error_invalid_reparse_data"></span>**ERRO \_ DADOS \_ DE REPARSE \_ INVÁLIDOS**
</dt> <dd> <dl> <dt>

4392 (0x1128)
</dt> <dt>



Os dados presentes no buffer de ponto de análise são inválidos.


</dt> </dl> </dd> <dt>

<span id="ERROR_REPARSE_TAG_INVALID"></span><span id="error_reparse_tag_invalid"></span>**ERRO \_ MARCA DE REPARSE \_ \_ INVÁLIDA**
</dt> <dd> <dl> <dt>

4393 (0x1129)
</dt> <dt>



A marca presente no buffer de ponto de reparse é inválida.


</dt> </dl> </dd> <dt>

<span id="ERROR_REPARSE_TAG_MISMATCH"></span><span id="error_reparse_tag_mismatch"></span>**ERRO \_ REPARSE \_ TAG \_ MISMATCH**
</dt> <dd> <dl> <dt>

4394 (0x112A)
</dt> <dt>



Há uma incompatibilidade entre a marca especificada na solicitação e a marca presente no ponto de nova consulta.


</dt> </dl> </dd> <dt>

<span id="ERROR_APP_DATA_NOT_FOUND"></span><span id="error_app_data_not_found"></span>**DADOS \_ DO APLICATIVO DE ERRO NÃO \_ \_ \_ ENCONTRADOS**
</dt> <dd> <dl> <dt>

4400 (0x1130)
</dt> <dt>



Dados de Cache Rápido não encontrados.


</dt> </dl> </dd> <dt>

<span id="ERROR_APP_DATA_EXPIRED"></span><span id="error_app_data_expired"></span>**DADOS \_ DO APLICATIVO DE ERRO \_ \_ EXPIRADOS**
</dt> <dd> <dl> <dt>

4401 (0x1131)
</dt> <dt>



Os dados do Cache Rápido expiraram.


</dt> </dl> </dd> <dt>

<span id="ERROR_APP_DATA_CORRUPT"></span><span id="error_app_data_corrupt"></span>**ERROS \_ DE DADOS DO APLICATIVO \_ \_ CORROMPIDOS**
</dt> <dd> <dl> <dt>

4402 (0x1132)
</dt> <dt>



Dados de Cache Rápido corrompidos.


</dt> </dl> </dd> <dt>

<span id="ERROR_APP_DATA_LIMIT_EXCEEDED"></span><span id="error_app_data_limit_exceeded"></span>**ERRO \_ LIMITE DE DADOS DO APLICATIVO \_ \_ \_ EXCEDIDO**
</dt> <dd> <dl> <dt>

4403 (0x1133)
</dt> <dt>



Os dados de Cache Rápido excederam seu tamanho máximo e não podem ser atualizados.


</dt> </dl> </dd> <dt>

<span id="ERROR_APP_DATA_REBOOT_REQUIRED"></span><span id="error_app_data_reboot_required"></span>**REINICIALIZAÇÃO \_ DE DADOS DO APLICATIVO DE ERRO \_ \_ \_ NECESSÁRIA**
</dt> <dd> <dl> <dt>

4404 (0x1134)
</dt> <dt>



O Cache Rápido foi ReEso e requer uma reinicialização até que possa ser atualizado.


</dt> </dl> </dd> <dt>

<span id="ERROR_SECUREBOOT_ROLLBACK_DETECTED"></span><span id="error_secureboot_rollback_detected"></span>**ERRO \_ SECUREBOOT \_ ROLLBACK \_ DETECTADO**
</dt> <dd> <dl> <dt>

4420 (0x1144)
</dt> <dt>



A inicialização segura detectou que foi tentada a reação de dados protegidos.


</dt> </dl> </dd> <dt>

<span id="ERROR_SECUREBOOT_POLICY_VIOLATION"></span><span id="error_secureboot_policy_violation"></span>**ERRO \_ SECUREBOOT \_ POLICY \_ VIOLATION**
</dt> <dd> <dl> <dt>

4421 (0x1145)
</dt> <dt>



O valor é protegido pela política de Inicialização Segura e não pode ser modificado ou excluído.


</dt> </dl> </dd> <dt>

<span id="ERROR_SECUREBOOT_INVALID_POLICY"></span><span id="error_secureboot_invalid_policy"></span>**ERRO \_ SECUREBOOT \_ INVALID \_ POLICY**
</dt> <dd> <dl> <dt>

4422 (0x1146)
</dt> <dt>



A política inicialização segura é inválida.


</dt> </dl> </dd> <dt>

<span id="ERROR_SECUREBOOT_POLICY_PUBLISHER_NOT_FOUND"></span><span id="error_secureboot_policy_publisher_not_found"></span>**ERRO \_ SECUREBOOT \_ POLICY PUBLISHER NÃO \_ \_ \_ ENCONTRADO**
</dt> <dd> <dl> <dt>

4423 (0x1147)
</dt> <dt>



Uma nova política de Inicialização Segura não continha o publicador atual em sua lista de atualizações.


</dt> </dl> </dd> <dt>

<span id="ERROR_SECUREBOOT_POLICY_NOT_SIGNED"></span><span id="error_secureboot_policy_not_signed"></span>**ERRO \_ SECUREBOOT \_ POLICY NÃO \_ \_ ASSINADO**
</dt> <dd> <dl> <dt>

4424 (0x1148)
</dt> <dt>



A política inicialização segura não está assinada ou é assinada por um signante não confiável.


</dt> </dl> </dd> <dt>

<span id="ERROR_SECUREBOOT_NOT_ENABLED"></span><span id="error_secureboot_not_enabled"></span>**ERRO \_ SECUREBOOT \_ NÃO \_ HABILITADO**
</dt> <dd> <dl> <dt>

4425 (0x1149)
</dt> <dt>



A Inicialização Segura não está habilitada neste computador.


</dt> </dl> </dd> <dt>

<span id="ERROR_SECUREBOOT_FILE_REPLACED"></span><span id="error_secureboot_file_replaced"></span>**ERRO \_ SECUREBOOT \_ FILE \_ REPLACED**
</dt> <dd> <dl> <dt>

4426 (0x114A)
</dt> <dt>



A Inicialização Segura requer que determinados arquivos e drivers não sejam substituídos por outros arquivos ou drivers.


</dt> </dl> </dd> <dt>

<span id="ERROR_OFFLOAD_READ_FLT_NOT_SUPPORTED"></span><span id="error_offload_read_flt_not_supported"></span>**ERRO \_ AO \_ DESCARREGAR \_ FLT DE LEITURA SEM \_ \_ SUPORTE**
</dt> <dd> <dl> <dt>

4440 (0x1158)
</dt> <dt>



A operação de leitura de descarregar cópia não é suportada por um filtro.


</dt> </dl> </dd> <dt>

<span id="ERROR_OFFLOAD_WRITE_FLT_NOT_SUPPORTED"></span><span id="error_offload_write_flt_not_supported"></span>**NÃO \_ HÁ SUPORTE PARA ERRO AO \_ \_ DESCARREGAR FLT \_ DE \_ GRAVAÇÃO**
</dt> <dd> <dl> <dt>

4441 (0x1159)
</dt> <dt>



Não há suporte para a operação de gravação de descarregador de cópia por um filtro.


</dt> </dl> </dd> <dt>

<span id="ERROR_OFFLOAD_READ_FILE_NOT_SUPPORTED"></span><span id="error_offload_read_file_not_supported"></span>**ERRO \_ AO DESCARREGAR \_ O ARQUIVO DE LEITURA SEM \_ \_ \_ SUPORTE**
</dt> <dd> <dl> <dt>

4442 (0x115A)
</dt> <dt>



Não há suporte para a operação de leitura de descarregar cópia para o arquivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_OFFLOAD_WRITE_FILE_NOT_SUPPORTED"></span><span id="error_offload_write_file_not_supported"></span>**ERRO \_ AO \_ DESCARREGAR O ARQUIVO DE GRAVAÇÃO \_ SEM \_ \_ SUPORTE**
</dt> <dd> <dl> <dt>

4443 (0x115B)
</dt> <dt>



Não há suporte para a operação de gravação de descarregador de cópia para o arquivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_VOLUME_NOT_SIS_ENABLED"></span><span id="error_volume_not_sis_enabled"></span>**VOLUME \_ DE ERRO NÃO \_ \_ SIS \_ HABILITADO**
</dt> <dd> <dl> <dt>

4500 (0x1194)
</dt> <dt>



O Armazenamento instância única não está disponível neste volume.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEPENDENT_RESOURCE_EXISTS"></span><span id="error_dependent_resource_exists"></span>**O RECURSO \_ DEPENDENTE \_ DE ERRO \_ EXISTE**
</dt> <dd> <dl> <dt>

5001 (0x1389)
</dt> <dt>



A operação não pode ser concluída porque outros recursos dependem desse recurso.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEPENDENCY_NOT_FOUND"></span><span id="error_dependency_not_found"></span>**DEPENDÊNCIA \_ DE ERRO NÃO \_ \_ ENCONTRADA**
</dt> <dd> <dl> <dt>

5002 (0x138A)
</dt> <dt>



A dependência de recurso de cluster não pode ser encontrada.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEPENDENCY_ALREADY_EXISTS"></span><span id="error_dependency_already_exists"></span>**A \_ DEPENDÊNCIA DE ERRO JÁ \_ \_ EXISTE**
</dt> <dd> <dl> <dt>

5003 (0x138B)
</dt> <dt>



O recurso de cluster não pode ser dependente do recurso especificado porque ele já é dependente.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_NOT_ONLINE"></span><span id="error_resource_not_online"></span>**RECURSO \_ DE ERRO NÃO \_ \_ ONLINE**
</dt> <dd> <dl> <dt>

5004 (0x138C)
</dt> <dt>



O recurso de cluster não está online.


</dt> </dl> </dd> <dt>

<span id="ERROR_HOST_NODE_NOT_AVAILABLE"></span><span id="error_host_node_not_available"></span>**NÓ \_ DE HOST DE ERRO NÃO \_ \_ \_ DISPONÍVEL**
</dt> <dd> <dl> <dt>

5005 (0x138D)
</dt> <dt>



Um nó de cluster não está disponível para essa operação.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_NOT_AVAILABLE"></span><span id="error_resource_not_available"></span>**RECURSO \_ DE ERRO NÃO \_ \_ DISPONÍVEL**
</dt> <dd> <dl> <dt>

5006 (0x138E)
</dt> <dt>



O recurso de cluster não está disponível.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_NOT_FOUND"></span><span id="error_resource_not_found"></span>**RECURSO \_ DE ERRO NÃO \_ \_ ENCONTRADO**
</dt> <dd> <dl> <dt>

5007 (0x138F)
</dt> <dt>



Não foi possível encontrar o recurso de cluster.


</dt> </dl> </dd> <dt>

<span id="ERROR_SHUTDOWN_CLUSTER"></span><span id="error_shutdown_cluster"></span>**CLUSTER DE \_ DESLIGAMENTO \_ DE ERRO**
</dt> <dd> <dl> <dt>

5008 (0x1390)
</dt> <dt>



O cluster está sendo desligado.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_EVICT_ACTIVE_NODE"></span><span id="error_cant_evict_active_node"></span>**ERRO \_ NÃO É POSSÍVEL \_ \_ REATIVAR O NÓ \_ ATIVO**
</dt> <dd> <dl> <dt>

5009 (0x1391)
</dt> <dt>



Um nó de cluster não pode ser despejado do cluster, a menos que o nó esteja inoado ou seja o último nó.


</dt> </dl> </dd> <dt>

<span id="ERROR_OBJECT_ALREADY_EXISTS"></span><span id="error_object_already_exists"></span>**O \_ OBJETO ERROR JÁ \_ \_ EXISTE**
</dt> <dd> <dl> <dt>

5010 (0x1392)
</dt> <dt>



O objeto já existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_OBJECT_IN_LIST"></span><span id="error_object_in_list"></span>**OBJETO \_ ERROR \_ IN \_ LIST**
</dt> <dd> <dl> <dt>

5011 (0x1393)
</dt> <dt>



O objeto já está na lista.


</dt> </dl> </dd> <dt>

<span id="ERROR_GROUP_NOT_AVAILABLE"></span><span id="error_group_not_available"></span>**GRUPO \_ DE ERROS NÃO \_ \_ DISPONÍVEL**
</dt> <dd> <dl> <dt>

5012 (0x1394)
</dt> <dt>



O grupo de clusters não está disponível para novas solicitações.


</dt> </dl> </dd> <dt>

<span id="ERROR_GROUP_NOT_FOUND"></span><span id="error_group_not_found"></span>**GRUPO \_ DE ERROS NÃO \_ \_ ENCONTRADO**
</dt> <dd> <dl> <dt>

5013 (0x1395)
</dt> <dt>



Não foi possível encontrar o grupo de clusters.


</dt> </dl> </dd> <dt>

<span id="ERROR_GROUP_NOT_ONLINE"></span><span id="error_group_not_online"></span>**GRUPO \_ DE ERROS NÃO \_ \_ ONLINE**
</dt> <dd> <dl> <dt>

5014 (0x1396)
</dt> <dt>



Não foi possível concluir a operação porque o grupo de clusters não está online.


</dt> </dl> </dd> <dt>

<span id="ERROR_HOST_NODE_NOT_RESOURCE_OWNER"></span><span id="error_host_node_not_resource_owner"></span>**NÓ \_ DE HOST DE ERRO NÃO PROPRIETÁRIO DO \_ \_ \_ \_ RECURSO**
</dt> <dd> <dl> <dt>

5015 (0x1397)
</dt> <dt>



A operação falhou porque o nó de cluster especificado não é o proprietário do recurso ou o nó não é um possível proprietário do recurso.


</dt> </dl> </dd> <dt>

<span id="ERROR_HOST_NODE_NOT_GROUP_OWNER"></span><span id="error_host_node_not_group_owner"></span>**NÓ \_ DE HOST DE ERRO NÃO PROPRIETÁRIO DO \_ \_ \_ \_ GRUPO**
</dt> <dd> <dl> <dt>

5016 (0x1398)
</dt> <dt>



A operação falhou porque o nó do cluster especificado não é o proprietário do grupo ou o nó não é um possível proprietário do grupo.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESMON_CREATE_FAILED"></span><span id="error_resmon_create_failed"></span>**ERRO \_ FALHA AO CRIAR RESMON \_ \_**
</dt> <dd> <dl> <dt>

5017 (0x1399)
</dt> <dt>



Não foi possível criar o recurso de cluster no monitor de recursos especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESMON_ONLINE_FAILED"></span><span id="error_resmon_online_failed"></span>**ERRO \_ FALHA NO RESMON \_ ONLINE \_**
</dt> <dd> <dl> <dt>

5018 (0x139A)
</dt> <dt>



O recurso de cluster não pôde ser online pelo monitor de recursos.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_ONLINE"></span><span id="error_resource_online"></span>**RECURSO \_ DE ERRO \_ ONLINE**
</dt> <dd> <dl> <dt>

5019 (0x139B)
</dt> <dt>



A operação não pôde ser concluída porque o recurso de cluster está online.


</dt> </dl> </dd> <dt>

<span id="ERROR_QUORUM_RESOURCE"></span><span id="error_quorum_resource"></span>**\_recurso de quorum de erro \_**
</dt> <dd> <dl> <dt>

5020 (0x139C)
</dt> <dt>



O recurso de cluster não pôde ser excluído ou colocado offline porque é o recurso de quorum.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_QUORUM_CAPABLE"></span><span id="error_not_quorum_capable"></span>**ERRO \_ não \_ \_ compatível com quorum**
</dt> <dd> <dl> <dt>

5021 (0x139D)
</dt> <dt>



O cluster não pôde tornar o recurso especificado um recurso de quorum porque ele não é capaz de ser um recurso de quorum.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_SHUTTING_DOWN"></span><span id="error_cluster_shutting_down"></span>**ERRO \_ ao \_ desligar o cluster \_**
</dt> <dd> <dl> <dt>

5022 (0x139E)
</dt> <dt>



O software do cluster está sendo desligado.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_STATE"></span><span id="error_invalid_state"></span>**\_estado inválido do erro \_**
</dt> <dd> <dl> <dt>

5023 (0x139F)
</dt> <dt>



O grupo ou recurso não está no estado correto para executar a operação solicitada.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_PROPERTIES_STORED"></span><span id="error_resource_properties_stored"></span>**Propriedades do recurso de erro \_ \_ \_ armazenadas**
</dt> <dd> <dl> <dt>

5024 (0x13A0)
</dt> <dt>



As propriedades foram armazenadas, mas nem todas as alterações entrarão em vigor até a próxima vez que o recurso for colocado online.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_QUORUM_CLASS"></span><span id="error_not_quorum_class"></span>**ERRO \_ não \_ classe de quorum \_**
</dt> <dd> <dl> <dt>

5025 (0x13A1)
</dt> <dt>



O cluster não pôde tornar o recurso especificado um recurso de quorum porque ele não pertence a uma classe de armazenamento compartilhada.


</dt> </dl> </dd> <dt>

<span id="ERROR_CORE_RESOURCE"></span><span id="error_core_resource"></span>**\_recurso de núcleo de erro \_**
</dt> <dd> <dl> <dt>

5026 (0x13A2)
</dt> <dt>



Não foi possível excluir o recurso de cluster porque ele é um recurso principal.


</dt> </dl> </dd> <dt>

<span id="ERROR_QUORUM_RESOURCE_ONLINE_FAILED"></span><span id="error_quorum_resource_online_failed"></span>**ERRO \_ \_ falha no recurso de quorum \_ online \_**
</dt> <dd> <dl> <dt>

5027 (0x13A3)
</dt> <dt>



O recurso de quorum não pôde ser colocado online.


</dt> </dl> </dd> <dt>

<span id="ERROR_QUORUMLOG_OPEN_FAILED"></span><span id="error_quorumlog_open_failed"></span>**ERRO \_ QUORUMLOG \_ \_ falha ao abrir**
</dt> <dd> <dl> <dt>

5028 (0x13A4)
</dt> <dt>



Não foi possível criar ou montar o log de quorum com êxito.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTERLOG_CORRUPT"></span><span id="error_clusterlog_corrupt"></span>**ERRO \_ CLUSTERLOG \_ corrompido**
</dt> <dd> <dl> <dt>

5029 (0x13A5)
</dt> <dt>



O log do cluster está corrompido.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTERLOG_RECORD_EXCEEDS_MAXSIZE"></span><span id="error_clusterlog_record_exceeds_maxsize"></span>**o \_ registro CLUSTERLOG de erro \_ \_ excede \_ MaxSize**
</dt> <dd> <dl> <dt>

5030 (0x13A6)
</dt> <dt>



Não foi possível gravar o registro no log do cluster, pois ele excede o tamanho máximo.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTERLOG_EXCEEDS_MAXSIZE"></span><span id="error_clusterlog_exceeds_maxsize"></span>**o erro \_ CLUSTERLOG \_ excede \_ MaxSize**
</dt> <dd> <dl> <dt>

5031 (0x13A7)
</dt> <dt>



O log do cluster excede seu tamanho máximo.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTERLOG_CHKPOINT_NOT_FOUND"></span><span id="error_clusterlog_chkpoint_not_found"></span>**ERRO \_ CLUSTERLOG \_ CHKPOINT \_ não \_ encontrado**
</dt> <dd> <dl> <dt>

5032 (0x13A8)
</dt> <dt>



Nenhum registro de ponto de verificação foi encontrado no log do cluster.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTERLOG_NOT_ENOUGH_SPACE"></span><span id="error_clusterlog_not_enough_space"></span>**ERRO \_ CLUSTERLOG \_ não \_ há \_ espaço suficiente**
</dt> <dd> <dl> <dt>

5033 (0x13A9)
</dt> <dt>



O espaço em disco mínimo necessário para o registro em log não está disponível.


</dt> </dl> </dd> <dt>

<span id="ERROR_QUORUM_OWNER_ALIVE"></span><span id="error_quorum_owner_alive"></span>**ERRO \_ de \_ proprietário do quorum \_ ativo**
</dt> <dd> <dl> <dt>

5034 (0x13AA)
</dt> <dt>



O nó de cluster falhou ao assumir o controle do recurso de quorum porque o recurso pertence a outro nó ativo.


</dt> </dl> </dd> <dt>

<span id="ERROR_NETWORK_NOT_AVAILABLE"></span><span id="error_network_not_available"></span>**ERRO de \_ rede \_ não \_ disponível**
</dt> <dd> <dl> <dt>

5035 (0x13AB)
</dt> <dt>



Uma rede de cluster não está disponível para esta operação.


</dt> </dl> </dd> <dt>

<span id="ERROR_NODE_NOT_AVAILABLE"></span><span id="error_node_not_available"></span>**nó de erro \_ \_ não \_ disponível**
</dt> <dd> <dl> <dt>

5036 (0x13AC)
</dt> <dt>



Um nó de cluster não está disponível para esta operação.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALL_NODES_NOT_AVAILABLE"></span><span id="error_all_nodes_not_available"></span>**ERRO \_ todos os \_ nós \_ não \_ estão disponíveis**
</dt> <dd> <dl> <dt>

5037 (0x13AD)
</dt> <dt>



Todos os nós de cluster devem estar em execução para executar esta operação.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_FAILED"></span><span id="error_resource_failed"></span>**\_falha no recurso de erro \_**
</dt> <dd> <dl> <dt>

5038 (0x13AE)
</dt> <dt>



Um recurso de cluster falhou.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INVALID_NODE"></span><span id="error_cluster_invalid_node"></span>**ERRO \_ de \_ nó inválido do cluster \_**
</dt> <dd> <dl> <dt>

5039 (0x13AF)
</dt> <dt>



O nó do cluster não é válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_EXISTS"></span><span id="error_cluster_node_exists"></span>**o \_ nó de cluster de erros \_ \_ existe**
</dt> <dd> <dl> <dt>

5040 (0x13B0)
</dt> <dt>



O nó de cluster já existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_JOIN_IN_PROGRESS"></span><span id="error_cluster_join_in_progress"></span>**ERRO \_ \_ de ingresso \_ no cluster em \_ andamento**
</dt> <dd> <dl> <dt>

5041 (0x13B1)
</dt> <dt>



Um nó está no processo de ingressar no cluster.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_NOT_FOUND"></span><span id="error_cluster_node_not_found"></span>**nó de cluster de erros \_ \_ \_ não \_ encontrado**
</dt> <dd> <dl> <dt>

5042 (0x13B2)
</dt> <dt>



O nó do cluster não foi encontrado.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_LOCAL_NODE_NOT_FOUND"></span><span id="error_cluster_local_node_not_found"></span>**\_nó local do cluster de erros \_ \_ \_ não \_ encontrado**
</dt> <dd> <dl> <dt>

5043 (0x13B3)
</dt> <dt>



As informações do nó local do cluster não foram encontradas.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NETWORK_EXISTS"></span><span id="error_cluster_network_exists"></span>**ERRO a \_ rede de clusters \_ \_ existe**
</dt> <dd> <dl> <dt>

5044 (0x13B4)
</dt> <dt>



A rede de cluster já existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NETWORK_NOT_FOUND"></span><span id="error_cluster_network_not_found"></span>**ERRO \_ de \_ rede de cluster \_ não \_ encontrada**
</dt> <dd> <dl> <dt>

5045 (0x13B5)
</dt> <dt>



A rede de cluster não foi encontrada.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NETINTERFACE_EXISTS"></span><span id="error_cluster_netinterface_exists"></span>**ERRO o \_ cluster \_ netinterface \_ existe**
</dt> <dd> <dl> <dt>

5046 (0x13B6)
</dt> <dt>



A interface de rede do cluster já existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NETINTERFACE_NOT_FOUND"></span><span id="error_cluster_netinterface_not_found"></span>**ERRO de \_ cluster de \_ netinterface \_ não \_ encontrado**
</dt> <dd> <dl> <dt>

5047 (0x13B7)
</dt> <dt>



A interface de rede do cluster não foi encontrada.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INVALID_REQUEST"></span><span id="error_cluster_invalid_request"></span>**ERRO de \_ solicitação de cluster \_ inválida \_**
</dt> <dd> <dl> <dt>

5048 (0x13B8)
</dt> <dt>



A solicitação de cluster não é válida para este objeto.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INVALID_NETWORK_PROVIDER"></span><span id="error_cluster_invalid_network_provider"></span>**ERRO \_ do \_ \_ provedor de rede inválido do cluster \_**
</dt> <dd> <dl> <dt>

5049 (0x13B9)
</dt> <dt>



O provedor de rede de cluster não é válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_DOWN"></span><span id="error_cluster_node_down"></span>**ERRO \_ no \_ nó do cluster \_ inoperante**
</dt> <dd> <dl> <dt>

5050 (0x13BA)
</dt> <dt>



O nó do cluster está inoperante.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_UNREACHABLE"></span><span id="error_cluster_node_unreachable"></span>**nó de cluster de erros \_ \_ \_ inacessível**
</dt> <dd> <dl> <dt>

5051 (0x13BB)
</dt> <dt>



O nó do cluster não está acessível.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_NOT_MEMBER"></span><span id="error_cluster_node_not_member"></span>**ERRO \_ nó de cluster \_ \_ não \_ membro**
</dt> <dd> <dl> <dt>

5052 (0x13BC)
</dt> <dt>



O nó de cluster não é um membro do cluster.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_JOIN_NOT_IN_PROGRESS"></span><span id="error_cluster_join_not_in_progress"></span>**JUNÇÃO \_ DE CLUSTER DE ERROS NÃO EM \_ \_ \_ \_ ANDAMENTO**
</dt> <dd> <dl> <dt>

5053 (0x13BD)
</dt> <dt>



Uma operação de junção de cluster não está em andamento.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INVALID_NETWORK"></span><span id="error_cluster_invalid_network"></span>**REDE \_ INVÁLIDA DO CLUSTER DE \_ \_ ERROS**
</dt> <dd> <dl> <dt>

5054 (0x13BE)
</dt> <dt>



A rede de cluster não é válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_UP"></span><span id="error_cluster_node_up"></span>**NÓ \_ DE CLUSTER DE ERRO PARA \_ \_ CIMA**
</dt> <dd> <dl> <dt>

5056 (0x13C0)
</dt> <dt>



O nó do cluster está ativo.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_IPADDR_IN_USE"></span><span id="error_cluster_ipaddr_in_use"></span>**ERRO \_ DE \_ CLUSTER IPADDR \_ EM \_ USO**
</dt> <dd> <dl> <dt>

5057 (0x13C1)
</dt> <dt>



O endereço IP do cluster já está em uso.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_NOT_PAUSED"></span><span id="error_cluster_node_not_paused"></span>**NÓ \_ DE CLUSTER DE ERRO NÃO \_ \_ \_ PAUSADO**
</dt> <dd> <dl> <dt>

5058 (0x13C2)
</dt> <dt>



O nó de cluster não está em pausa.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NO_SECURITY_CONTEXT"></span><span id="error_cluster_no_security_context"></span>**CLUSTER DE \_ ERRO SEM CONTEXTO DE \_ \_ \_ SEGURANÇA**
</dt> <dd> <dl> <dt>

5059 (0x13C3)
</dt> <dt>



Nenhum contexto de segurança de cluster está disponível.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NETWORK_NOT_INTERNAL"></span><span id="error_cluster_network_not_internal"></span>**REDE \_ DE CLUSTER DE ERRO NÃO \_ \_ \_ INTERNA**
</dt> <dd> <dl> <dt>

5060 (0x13C4)
</dt> <dt>



A rede de cluster não está configurada para comunicação interna do cluster.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_ALREADY_UP"></span><span id="error_cluster_node_already_up"></span>**NÓ \_ DE CLUSTER DE ERROS JÁ \_ \_ \_ ATIVO**
</dt> <dd> <dl> <dt>

5061 (0x13C5)
</dt> <dt>



O nó de cluster já está ativo.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_ALREADY_DOWN"></span><span id="error_cluster_node_already_down"></span>**NÓ \_ DE CLUSTER DE ERROS JÁ \_ \_ \_ INOBADO**
</dt> <dd> <dl> <dt>

5062 (0x13C6)
</dt> <dt>



O nó de cluster já está inoado.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NETWORK_ALREADY_ONLINE"></span><span id="error_cluster_network_already_online"></span>**REDE \_ DE CLUSTER DE ERROS JÁ \_ \_ \_ ONLINE**
</dt> <dd> <dl> <dt>

5063 (0x13C7)
</dt> <dt>



A rede de cluster já está online.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NETWORK_ALREADY_OFFLINE"></span><span id="error_cluster_network_already_offline"></span>**REDE \_ DE CLUSTER DE ERROS JÁ \_ \_ \_ OFFLINE**
</dt> <dd> <dl> <dt>

5064 (0x13C8)
</dt> <dt>



A rede de cluster já está offline.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_ALREADY_MEMBER"></span><span id="error_cluster_node_already_member"></span>**NÓ \_ DO CLUSTER DE ERROS JÁ \_ \_ \_ MEMBRO**
</dt> <dd> <dl> <dt>

5065 (0x13C9)
</dt> <dt>



O nó de cluster já é membro do cluster.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_LAST_INTERNAL_NETWORK"></span><span id="error_cluster_last_internal_network"></span>**CLUSTER DE \_ ERRO \_ ÚLTIMA REDE \_ \_ INTERNA**
</dt> <dd> <dl> <dt>

5066 (0x13CA)
</dt> <dt>



A rede de cluster é a única configurada para comunicação interna de cluster entre dois ou mais nós de cluster ativos. A funcionalidade de comunicação interna não pode ser removida da rede.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NETWORK_HAS_DEPENDENTS"></span><span id="error_cluster_network_has_dependents"></span>**A \_ REDE DE CLUSTER DE ERROS TEM \_ \_ \_ DEPENDENTES**
</dt> <dd> <dl> <dt>

5067 (0x13CB)
</dt> <dt>



Um ou mais recursos de cluster dependem da rede para fornecer serviço aos clientes. A funcionalidade de acesso do cliente não pode ser removida da rede.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_OPERATION_ON_QUORUM"></span><span id="error_invalid_operation_on_quorum"></span>**ERRO \_ OPERAÇÃO INVÁLIDA NO \_ \_ \_ QUORUM**
</dt> <dd> <dl> <dt>

5068 (0x13CC)
</dt> <dt>



Essa operação não pode ser executada no recurso de cluster, pois ele é o recurso de quorum. Você não pode colocar o recurso de quorum offline ou modificar sua lista de possíveis proprietários.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEPENDENCY_NOT_ALLOWED"></span><span id="error_dependency_not_allowed"></span>**DEPENDÊNCIA \_ DE ERRO NÃO \_ \_ PERMITIDA**
</dt> <dd> <dl> <dt>

5069 (0x13CD)
</dt> <dt>



O recurso de quorum do cluster não tem permissão para ter dependências.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_PAUSED"></span><span id="error_cluster_node_paused"></span>**NÓ \_ DO CLUSTER DE ERROS EM \_ \_ PAUSA**
</dt> <dd> <dl> <dt>

5070 (0x13CE)
</dt> <dt>



O nó do cluster está em pausa.


</dt> </dl> </dd> <dt>

<span id="ERROR_NODE_CANT_HOST_RESOURCE"></span><span id="error_node_cant_host_resource"></span>**RECURSO \_ DE HOST DO NÓ DE ERRO NÃO \_ \_ \_ PODE**
</dt> <dd> <dl> <dt>

5071 (0x13CF)
</dt> <dt>



O recurso de cluster não pode ser online. O nó proprietário não pode executar esse recurso.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_NOT_READY"></span><span id="error_cluster_node_not_ready"></span>**NÓ \_ DE CLUSTER DE ERRO NÃO \_ \_ \_ PRONTO**
</dt> <dd> <dl> <dt>

5072 (0x13D0)
</dt> <dt>



O nó de cluster não está pronto para executar a operação solicitada.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_SHUTTING_DOWN"></span><span id="error_cluster_node_shutting_down"></span>**ERRO \_ AO DESLIGAR O NÓ DO \_ \_ \_ CLUSTER**
</dt> <dd> <dl> <dt>

5073 (0x13D1)
</dt> <dt>



O nó do cluster está sendo desligado.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_JOIN_ABORTED"></span><span id="error_cluster_join_aborted"></span>**ERRO DE \_ \_ JUNÇÃO DE CLUSTER \_ ANULADA**
</dt> <dd> <dl> <dt>

5074 (0x13D2)
</dt> <dt>



A operação de junção de cluster foi anulada.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INCOMPATIBLE_VERSIONS"></span><span id="error_cluster_incompatible_versions"></span>**VERSÕES \_ INCOMPATÍVEIS DO CLUSTER \_ DE \_ ERROS**
</dt> <dd> <dl> <dt>

5075 (0x13D3)
</dt> <dt>



A operação de junção de cluster falhou devido a versões de software incompatíveis entre o nó de junção e seu responsável.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_MAXNUM_OF_RESOURCES_EXCEEDED"></span><span id="error_cluster_maxnum_of_resources_exceeded"></span>**ERRO \_ CLUSTER \_ MAXNUM DE RECURSOS \_ \_ \_ EXCEDIDO**
</dt> <dd> <dl> <dt>

5076 (0x13D4)
</dt> <dt>



Esse recurso não pode ser criado porque o cluster atingiu o limite do número de recursos que ele pode monitorar.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_SYSTEM_CONFIG_CHANGED"></span><span id="error_cluster_system_config_changed"></span>**CONFIGURAÇÃO \_ DO SISTEMA DE CLUSTER DE ERROS \_ \_ \_ ALTERADA**
</dt> <dd> <dl> <dt>

5077 (0x13D5)
</dt> <dt>



A configuração do sistema foi alterada durante a operação de junção ou formulário do cluster. A operação de junção ou formulário foi anulada.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCE_TYPE_NOT_FOUND"></span><span id="error_cluster_resource_type_not_found"></span>**TIPO \_ DE RECURSO DE CLUSTER DE ERRO NÃO \_ \_ \_ \_ ENCONTRADO**
</dt> <dd> <dl> <dt>

5078 (0x13D6)
</dt> <dt>



O tipo de recurso especificado não foi encontrado.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESTYPE_NOT_SUPPORTED"></span><span id="error_cluster_restype_not_supported"></span>**NÃO \_ HÁ SUPORTE PARA \_ RESTYPE DE CLUSTER \_ DE \_ ERRO**
</dt> <dd> <dl> <dt>

5079 (0x13D7)
</dt> <dt>



O nó especificado não dá suporte a um recurso desse tipo. Isso pode ser devido a inconsistências de versão ou à ausência da DLL de recurso neste nó.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESNAME_NOT_FOUND"></span><span id="error_cluster_resname_not_found"></span>**ERRO \_ NOME DO CLUSTER NÃO \_ \_ \_ ENCONTRADO**
</dt> <dd> <dl> <dt>

5080 (0x13D8)
</dt> <dt>



Não há suporte para o nome do recurso especificado por essa DLL de recurso. Isso pode ser devido a um nome ruim (ou alterado) fornecido para a DLL do recurso.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NO_RPC_PACKAGES_REGISTERED"></span><span id="error_cluster_no_rpc_packages_registered"></span>**CLUSTER \_ DE ERRO NENHUM PACOTE \_ \_ RPC \_ \_ REGISTRADO**
</dt> <dd> <dl> <dt>

5081 (0x13D9)
</dt> <dt>



Nenhum pacote de autenticação pode ser registrado com o servidor RPC.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_OWNER_NOT_IN_PREFLIST"></span><span id="error_cluster_owner_not_in_preflist"></span>**PROPRIETÁRIO \_ DO CLUSTER DE ERROS NÃO EM \_ \_ \_ \_ PREFLIST**
</dt> <dd> <dl> <dt>

5082 (0x13DA)
</dt> <dt>



Não é possível colocar o grupo online porque o proprietário do grupo não está na lista preferencial para o grupo. Para alterar o nó proprietário do grupo, mova o grupo.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_DATABASE_SEQMISMATCH"></span><span id="error_cluster_database_seqmismatch"></span>**\_SEQMISMATCH DO BANCO DE DADOS DE CLUSTER \_ \_ DE ERROS**
</dt> <dd> <dl> <dt>

5083 (0x13DB)
</dt> <dt>



A operação de junção falhou porque o número da sequência de banco de dados do cluster foi alterado ou é incompatível com o nó do cofre. Isso pode acontecer durante uma operação de junção se o banco de dados de cluster foi sendo mudado durante a junção.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESMON_INVALID_STATE"></span><span id="error_resmon_invalid_state"></span>**ERRO \_ ESTADO INVÁLIDO DE RESMON \_ \_**
</dt> <dd> <dl> <dt>

5084 (0x13DC)
</dt> <dt>



O monitor de recursos não permitirá que a operação de falha seja executada enquanto o recurso estiver em seu estado atual. Isso pode acontecer se o recurso estiver em um estado pendente.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_GUM_NOT_LOCKER"></span><span id="error_cluster_gum_not_locker"></span>**ERRO \_ CLUSTER \_ NÃO COFRE \_ \_**
</dt> <dd> <dl> <dt>

5085 (0x13DD)
</dt> <dt>



Um código não cofre recebeu uma solicitação para reservar o bloqueio para fazer atualizações globais.


</dt> </dl> </dd> <dt>

<span id="ERROR_QUORUM_DISK_NOT_FOUND"></span><span id="error_quorum_disk_not_found"></span>**DISCO \_ DE QUORUM \_ DE ERRO \_ NÃO \_ ENCONTRADO**
</dt> <dd> <dl> <dt>

5086 (0x13DE)
</dt> <dt>



O disco de quorum não pôde ser localizado pelo serviço de cluster.


</dt> </dl> </dd> <dt>

<span id="ERROR_DATABASE_BACKUP_CORRUPT"></span><span id="error_database_backup_corrupt"></span>**ERRO BACKUP \_ DO BANCO DE DADOS \_ \_ CORROMPIDO**
</dt> <dd> <dl> <dt>

5087 (0x13DF)
</dt> <dt>



O banco de dados de cluster com backup possivelmente está corrompido.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_ALREADY_HAS_DFS_ROOT"></span><span id="error_cluster_node_already_has_dfs_root"></span>**O \_ NÓ DO CLUSTER DE ERROS JÁ TEM A RAIZ DO \_ \_ \_ \_ \_ DFS**
</dt> <dd> <dl> <dt>

5088 (0x13E0)
</dt> <dt>



Uma raiz dfs já existe nesse nó de cluster.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_PROPERTY_UNCHANGEABLE"></span><span id="error_resource_property_unchangeable"></span>**PROPRIEDADE \_ DE RECURSO DE ERRO \_ \_ INALTERÁVEL**
</dt> <dd> <dl> <dt>

5089 (0x13E1)
</dt> <dt>



Falha ao tentar modificar uma propriedade de recurso porque ela está em conflito com outra propriedade existente.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_MEMBERSHIP_INVALID_STATE"></span><span id="error_cluster_membership_invalid_state"></span>**ESTADO \_ INVÁLIDO DE ASSOCIAÇÃO DE CLUSTER DE \_ \_ \_ ERRO**
</dt> <dd> <dl> <dt>

5890 (0x1702)
</dt> <dt>



Foi tentada uma operação incompatível com o estado de associação atual do nó.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_QUORUMLOG_NOT_FOUND"></span><span id="error_cluster_quorumlog_not_found"></span>**ERRO \_ \_ QUORUMLOG DO CLUSTER \_ NÃO \_ ENCONTRADO**
</dt> <dd> <dl> <dt>

5891 (0x1703)
</dt> <dt>



O recurso de quorum não contém o log de quorum.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_MEMBERSHIP_HALT"></span><span id="error_cluster_membership_halt"></span>**PARADA DE \_ ASSOCIAÇÃO DO CLUSTER DE \_ \_ ERROS**
</dt> <dd> <dl> <dt>

5892 (0x1704)
</dt> <dt>



O mecanismo de associação solicitou o desligamento do serviço de cluster neste nó.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INSTANCE_ID_MISMATCH"></span><span id="error_cluster_instance_id_mismatch"></span>**INCOMPATIBILIDADE \_ \_ DE ID DA INSTÂNCIA DE CLUSTER \_ DE \_ ERRO**
</dt> <dd> <dl> <dt>

5893 (0x1705)
</dt> <dt>



A operação de junção falhou porque a ID da instância de cluster do nó de junção não é correspondente à ID da instância de cluster do nó do responsável.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NETWORK_NOT_FOUND_FOR_IP"></span><span id="error_cluster_network_not_found_for_ip"></span>**REDE \_ DE CLUSTER DE ERROS NÃO ENCONTRADA PARA \_ \_ \_ \_ \_ IP**
</dt> <dd> <dl> <dt>

5894 (0x1706)
</dt> <dt>



Não foi possível encontrar uma rede de cluster correspondente para o endereço IP especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_PROPERTY_DATA_TYPE_MISMATCH"></span><span id="error_cluster_property_data_type_mismatch"></span>**INCOMPATIBILIDADE \_ DO TIPO DE DADOS DE PROPRIEDADE DO CLUSTER DE \_ \_ \_ \_ ERROS**
</dt> <dd> <dl> <dt>

5895 (0x1707)
</dt> <dt>



O tipo de dados real da propriedade não corresponder ao tipo de dados esperado da propriedade.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_EVICT_WITHOUT_CLEANUP"></span><span id="error_cluster_evict_without_cleanup"></span>**ERRO \_ DE \_ RESSALÇÃO \_ DO CLUSTER SEM \_ LIMPEZA**
</dt> <dd> <dl> <dt>

5896 (0x1708)
</dt> <dt>



O nó de cluster foi despejado do cluster com êxito, mas o nó não foi limpo. Para determinar quais etapas de limpeza falharam e como recuperar, consulte o log de eventos do aplicativo clustering de failover usando Visualizador de Eventos.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_PARAMETER_MISMATCH"></span><span id="error_cluster_parameter_mismatch"></span>**INCOMPATIBILIDADE \_ DE PARÂMETRO DE CLUSTER DE \_ \_ ERRO**
</dt> <dd> <dl> <dt>

5897 (0x1709)
</dt> <dt>



Dois ou mais valores de parâmetro especificados para as propriedades de um recurso estão em conflito.


</dt> </dl> </dd> <dt>

<span id="ERROR_NODE_CANNOT_BE_CLUSTERED"></span><span id="error_node_cannot_be_clustered"></span>**O \_ NÓ DE ERRO NÃO PODE SER \_ \_ \_ CLUSTERADO**
</dt> <dd> <dl> <dt>

5898 (0x170A)
</dt> <dt>



Esse computador não pode ser membro de um cluster.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_WRONG_OS_VERSION"></span><span id="error_cluster_wrong_os_version"></span>**VERSÃO DO \_ SISTEMA OPERACIONAL ERRADA DO CLUSTER DE \_ \_ \_ ERROS**
</dt> <dd> <dl> <dt>

5899 (0x170B)
</dt> <dt>



Esse computador não pode se fazer membro de um cluster porque não tem a versão correta do Windows instalado.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_CANT_CREATE_DUP_CLUSTER_NAME"></span><span id="error_cluster_cant_create_dup_cluster_name"></span>**O \_ CLUSTER DE ERROS NÃO PODE CRIAR O NOME DO CLUSTER \_ \_ \_ \_ \_ DUP**
</dt> <dd> <dl> <dt>

5900 (0x170C)
</dt> <dt>



Um cluster não pode ser criado com o nome do cluster especificado porque esse nome de cluster já está em uso. Especifique um nome diferente para o cluster.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSCFG_ALREADY_COMMITTED"></span><span id="error_cluscfg_already_committed"></span>**ERRO \_ CLUSCFG \_ JÁ FOI \_ COMPROMETIDO**
</dt> <dd> <dl> <dt>

5901 (0x170D)
</dt> <dt>



A ação de configuração de cluster já foi comprometida.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSCFG_ROLLBACK_FAILED"></span><span id="error_cluscfg_rollback_failed"></span>**ERRO \_ FALHA NA RE \_ ROLLBACK DO CLUSCFG \_**
</dt> <dd> <dl> <dt>

5902 (0x170E)
</dt> <dt>



Não foi possível reverter a ação de configuração do cluster.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSCFG_SYSTEM_DISK_DRIVE_LETTER_CONFLICT"></span><span id="error_cluscfg_system_disk_drive_letter_conflict"></span>**ERRO \_ CONFLITO DE LETRA DA UNIDADE DE DISCO \_ DO SISTEMA CLUSCFG \_ \_ \_ \_**
</dt> <dd> <dl> <dt>

5903 (0x170F)
</dt> <dt>



A letra da unidade atribuída a um disco do sistema em um nó entrou em conflito com a letra da unidade atribuída a um disco em outro nó.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_OLD_VERSION"></span><span id="error_cluster_old_version"></span>**VERSÃO \_ ANTIGA DO CLUSTER DE \_ \_ ERROS**
</dt> <dd> <dl> <dt>

5904 (0x1710)
</dt> <dt>



Um ou mais nós no cluster estão executando uma versão do Windows que não dá suporte a essa operação.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_MISMATCHED_COMPUTER_ACCT_NAME"></span><span id="error_cluster_mismatched_computer_acct_name"></span>**NOME DE ACCT DO \_ \_ COMPUTADOR COM \_ \_ INCOMPATIBILIDADE DO CLUSTER DE \_ ERROS**
</dt> <dd> <dl> <dt>

5905 (0x1711)
</dt> <dt>



O nome da conta de computador correspondente não corresponde ao Nome da Rede desse recurso.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NO_NET_ADAPTERS"></span><span id="error_cluster_no_net_adapters"></span>**CLUSTER \_ DE ERRO SEM \_ \_ \_ ADAPTADORES NET**
</dt> <dd> <dl> <dt>

5906 (0x1712)
</dt> <dt>



Nenhum adaptador de rede está disponível.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_POISONED"></span><span id="error_cluster_poisoned"></span>**CLUSTER \_ DE ERRO \_ SUSPEITO**
</dt> <dd> <dl> <dt>

5907 (0x1713)
</dt> <dt>



O nó do cluster foi suspeito.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_GROUP_MOVING"></span><span id="error_cluster_group_moving"></span>**ERRO DE \_ \_ MOVIMENTAÇÃO DO GRUPO DE \_ CLUSTERS**
</dt> <dd> <dl> <dt>

5908 (0x1714)
</dt> <dt>



O grupo não pode aceitar a solicitação, pois está mudando para outro nó.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCE_TYPE_BUSY"></span><span id="error_cluster_resource_type_busy"></span>**TIPO DE \_ RECURSO DE CLUSTER DE ERRO \_ \_ \_ OCUPADO**
</dt> <dd> <dl> <dt>

5909 (0x1715)
</dt> <dt>



O tipo de recurso não pode aceitar a solicitação, pois está muito ocupado executando outra operação.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_CALL_TIMED_OUT"></span><span id="error_resource_call_timed_out"></span>**A \_ CHAMADA DE RECURSO DE ERRO FOI \_ \_ \_ ESGOTADA**
</dt> <dd> <dl> <dt>

5910 (0x1716)
</dt> <dt>



A chamada para a DLL de recurso de cluster foi esgotada.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_CLUSTER_IPV6_ADDRESS"></span><span id="error_invalid_cluster_ipv6_address"></span>**ERRO \_ ENDEREÇO \_ IPV6 DE CLUSTER \_ \_ INVÁLIDO**
</dt> <dd> <dl> <dt>

5911 (0x1717)
</dt> <dt>



O endereço não é válido para um recurso de Endereço IPv6. Um endereço IPv6 global é necessário e deve corresponder a uma rede de cluster. Endereços de compatibilidade não são permitidos.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INTERNAL_INVALID_FUNCTION"></span><span id="error_cluster_internal_invalid_function"></span>**FUNÇÃO \_ INVÁLIDA INTERNA DO CLUSTER DE \_ \_ \_ ERROS**
</dt> <dd> <dl> <dt>

5912 (0x1718)
</dt> <dt>



Ocorreu um erro de cluster interno. Foi tentada uma chamada para uma função inválida.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_PARAMETER_OUT_OF_BOUNDS"></span><span id="error_cluster_parameter_out_of_bounds"></span>**PARÂMETRO \_ DE CLUSTER DE ERRO FORA DOS \_ \_ \_ \_ LIMITES**
</dt> <dd> <dl> <dt>

5913 (0x1719)
</dt> <dt>



Um valor de parâmetro está fora do intervalo aceitável.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_PARTIAL_SEND"></span><span id="error_cluster_partial_send"></span>**ENVIO \_ PARCIAL DO CLUSTER DE \_ \_ ERROS**
</dt> <dd> <dl> <dt>

5914 (0x171A)
</dt> <dt>



Ocorreu um erro de rede ao enviar dados para outro nó no cluster. O número de bytes transmitidos foi menor que o necessário.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_REGISTRY_INVALID_FUNCTION"></span><span id="error_cluster_registry_invalid_function"></span>**ERRO \_ de \_ \_ função inválida no registro de cluster \_**
</dt> <dd> <dl> <dt>

5915 (0x171B)
</dt> <dt>



Tentativa de operação de registro de cluster inválida.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INVALID_STRING_TERMINATION"></span><span id="error_cluster_invalid_string_termination"></span>**ERRO \_ de \_ encerramento de cadeia de caracteres inválido do cluster \_ \_**
</dt> <dd> <dl> <dt>

5916 (0x171C)
</dt> <dt>



Uma cadeia de caracteres de entrada não é encerrada corretamente.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INVALID_STRING_FORMAT"></span><span id="error_cluster_invalid_string_format"></span>**ERRO \_ de \_ formato de cadeia de caracteres inválido do cluster \_ \_**
</dt> <dd> <dl> <dt>

5917 (0x171D)
</dt> <dt>



Uma cadeia de caracteres de entrada não está em um formato válido para os dados que ele representa.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_DATABASE_TRANSACTION_IN_PROGRESS"></span><span id="error_cluster_database_transaction_in_progress"></span>**ERRO \_ \_ \_ \_ na transação de banco de dados de cluster em \_ andamento**
</dt> <dd> <dl> <dt>

5918 (0x171E)
</dt> <dt>



Ocorreu um erro de cluster interno. Uma transação de banco de dados de cluster foi tentada enquanto uma transação já estava em andamento.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_DATABASE_TRANSACTION_NOT_IN_PROGRESS"></span><span id="error_cluster_database_transaction_not_in_progress"></span>**ERRO \_ \_ \_ \_ de transação de banco de dados de cluster não está \_ em \_ andamento**
</dt> <dd> <dl> <dt>

5919 (0x171F)
</dt> <dt>



Ocorreu um erro de cluster interno. Houve uma tentativa de confirmar uma transação de banco de dados de cluster enquanto nenhuma transação estava em andamento.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NULL_DATA"></span><span id="error_cluster_null_data"></span>**ERRO \_ de \_ dados nulos do cluster \_**
</dt> <dd> <dl> <dt>

5920 (0x1720)
</dt> <dt>



Ocorreu um erro de cluster interno. Os dados não foram inicializados corretamente.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_PARTIAL_READ"></span><span id="error_cluster_partial_read"></span>**ERRO \_ de \_ leitura parcial do cluster \_**
</dt> <dd> <dl> <dt>

5921 (0x1721)
</dt> <dt>



Ocorreu um erro ao ler de um fluxo de dados. Um número inesperado de bytes foi retornado.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_PARTIAL_WRITE"></span><span id="error_cluster_partial_write"></span>**ERRO \_ de \_ gravação parcial do cluster \_**
</dt> <dd> <dl> <dt>

5922 (0x1722)
</dt> <dt>



Ocorreu um erro ao gravar em um fluxo de dados. O número necessário de bytes não pôde ser gravado.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_CANT_DESERIALIZE_DATA"></span><span id="error_cluster_cant_deserialize_data"></span>**ERRO o \_ cluster não \_ consegue \_ desserializar \_ dados**
</dt> <dd> <dl> <dt>

5923 (0x1723)
</dt> <dt>



Ocorreu um erro ao desserializar um fluxo de dados do cluster.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEPENDENT_RESOURCE_PROPERTY_CONFLICT"></span><span id="error_dependent_resource_property_conflict"></span>**\_conflito de \_ Propriedades de recursos dependentes de \_ erro \_**
</dt> <dd> <dl> <dt>

5924 (0x1724)
</dt> <dt>



Um ou mais valores de propriedade para esse recurso estão em conflito com um ou mais valores de propriedade associados a seus recursos dependentes.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NO_QUORUM"></span><span id="error_cluster_no_quorum"></span>**ERRO de \_ cluster \_ sem \_ Quorum**
</dt> <dd> <dl> <dt>

5925 (0x1725)
</dt> <dt>



Um quorum de nós de cluster não estava presente para formar um cluster.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INVALID_IPV6_NETWORK"></span><span id="error_cluster_invalid_ipv6_network"></span>**ERRO \_ de \_ \_ rede IPv6 inválida do cluster \_**
</dt> <dd> <dl> <dt>

5926 (0x1726)
</dt> <dt>



A rede de cluster não é válida para um recurso de endereço IPv6 ou não corresponde ao endereço configurado.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INVALID_IPV6_TUNNEL_NETWORK"></span><span id="error_cluster_invalid_ipv6_tunnel_network"></span>**ERRO \_ de \_ \_ rede de \_ túnel \_ IPv6 inválida do cluster**
</dt> <dd> <dl> <dt>

5927 (0x1727)
</dt> <dt>



a rede de cluster não é válida para um recurso de Tunnel IPv6. verifique a configuração do recurso de endereço IP no qual o recurso de Tunnel IPv6 depende.


</dt> </dl> </dd> <dt>

<span id="ERROR_QUORUM_NOT_ALLOWED_IN_THIS_GROUP"></span><span id="error_quorum_not_allowed_in_this_group"></span>**\_o quorum \_ de erro não é \_ permitido \_ neste \_ \_ grupo**
</dt> <dd> <dl> <dt>

5928 (0x1728)
</dt> <dt>



o recurso de Quorum não pode residir no grupo de Armazenamento disponível.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEPENDENCY_TREE_TOO_COMPLEX"></span><span id="error_dependency_tree_too_complex"></span>**árvore de dependência de erro \_ \_ \_ muito \_ complexa**
</dt> <dd> <dl> <dt>

5929 (0x1729)
</dt> <dt>



As dependências para esse recurso estão aninhadas muito profundamente.


</dt> </dl> </dd> <dt>

<span id="ERROR_EXCEPTION_IN_RESOURCE_CALL"></span><span id="error_exception_in_resource_call"></span>**\_exceção \_ de erro \_ na \_ chamada de recurso**
</dt> <dd> <dl> <dt>

5930 (0x172A)
</dt> <dt>



A chamada para a DLL de recurso gerou uma exceção sem tratamento.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RHS_FAILED_INITIALIZATION"></span><span id="error_cluster_rhs_failed_initialization"></span>**ERRO \_ \_ \_ na inicialização do RHS do cluster de erros \_**
</dt> <dd> <dl> <dt>

5931 (0x172B)
</dt> <dt>



Falha ao inicializar o processo de RHS.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NOT_INSTALLED"></span><span id="error_cluster_not_installed"></span>**CLUSTER de erros \_ \_ não \_ instalado**
</dt> <dd> <dl> <dt>

5932 (0x172C)
</dt> <dt>



O recurso de clustering de failover não está instalado neste nó.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCES_MUST_BE_ONLINE_ON_THE_SAME_NODE"></span><span id="error_cluster_resources_must_be_online_on_the_same_node"></span>**\_ \_ os recursos de cluster de erros \_ devem \_ estar \_ online \_ no \_ \_ mesmo \_ nó**
</dt> <dd> <dl> <dt>

5933 (0x172D)
</dt> <dt>



Os recursos devem estar online no mesmo nó para esta operação.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_MAX_NODES_IN_CLUSTER"></span><span id="error_cluster_max_nodes_in_cluster"></span>**ERRO \_ \_ no máximo \_ \_ de nós do cluster no \_ cluster**
</dt> <dd> <dl> <dt>

5934 (0x172E)
</dt> <dt>



Não é possível adicionar um novo nó, pois esse cluster já está em seu número máximo de nós.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_TOO_MANY_NODES"></span><span id="error_cluster_too_many_nodes"></span>**ERRO de \_ cluster em \_ excesso de \_ \_ nós**
</dt> <dd> <dl> <dt>

5935 (0x172F)
</dt> <dt>



Este cluster não pode ser criado porque o número especificado de nós excede o limite máximo permitido.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_OBJECT_ALREADY_USED"></span><span id="error_cluster_object_already_used"></span>**ERRO \_ de \_ objeto de cluster \_ já \_ usado**
</dt> <dd> <dl> <dt>

5936 (0x1730)
</dt> <dt>



Falha ao tentar usar o nome de cluster especificado porque já existe um objeto de computador habilitado com o nome fornecido no domínio.


</dt> </dl> </dd> <dt>

<span id="ERROR_NONCORE_GROUPS_FOUND"></span><span id="error_noncore_groups_found"></span>**ERRO de \_ grupos não principais \_ \_ encontrados**
</dt> <dd> <dl> <dt>

5937 (0x1731)
</dt> <dt>



Este cluster não pode ser destruído. Ele tem grupos de aplicativos não principais que devem ser excluídos antes que o cluster possa ser destruído.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_SHARE_RESOURCE_CONFLICT"></span><span id="error_file_share_resource_conflict"></span>**\_conflito de \_ recurso de compartilhamento de arquivo de erro \_ \_**
</dt> <dd> <dl> <dt>

5938 (0x1732)
</dt> <dt>



O compartilhamento de arquivos associado ao recurso de testemunha de compartilhamento de arquivos não pode ser hospedado por este cluster ou por qualquer um de seus nós.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_EVICT_INVALID_REQUEST"></span><span id="error_cluster_evict_invalid_request"></span>**ERRO \_ ao \_ Remover \_ solicitação inválida de cluster \_**
</dt> <dd> <dl> <dt>

5939 (0x1733)
</dt> <dt>



A remoção deste nó é inválida no momento. Devido a requisitos de quorum, a remoção do nó resultará no desligamento do cluster. Se for o último nó no cluster, o comando destruir cluster deverá ser usado.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_SINGLETON_RESOURCE"></span><span id="error_cluster_singleton_resource"></span>**\_ \_ recurso singleton do cluster de erros \_**
</dt> <dd> <dl> <dt>

5940 (0x1734)
</dt> <dt>



Somente uma instância desse tipo de recurso é permitida no cluster.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_GROUP_SINGLETON_RESOURCE"></span><span id="error_cluster_group_singleton_resource"></span>**ERRO \_ de \_ \_ recurso singleton do grupo de clusters \_**
</dt> <dd> <dl> <dt>

5941 (0x1735)
</dt> <dt>



Somente uma instância desse tipo de recurso é permitida por grupo de recursos.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCE_PROVIDER_FAILED"></span><span id="error_cluster_resource_provider_failed"></span>**ERRO \_ \_ \_ falha no provedor de recursos de cluster \_**
</dt> <dd> <dl> <dt>

5942 (0x1736)
</dt> <dt>



O recurso não pôde ficar online devido à falha de um ou mais recursos do provedor.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCE_CONFIGURATION_ERROR"></span><span id="error_cluster_resource_configuration_error"></span>**erro \_ de \_ \_ erro de configuração de recurso de cluster \_**
</dt> <dd> <dl> <dt>

5943 (0x1737)
</dt> <dt>



O recurso indicou que ele não pode ficar online em nenhum nó.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_GROUP_BUSY"></span><span id="error_cluster_group_busy"></span>**ERRO no \_ grupo de clusters \_ \_ ocupado**
</dt> <dd> <dl> <dt>

5944 (0x1738)
</dt> <dt>



A operação atual não pode ser executada neste grupo no momento.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NOT_SHARED_VOLUME"></span><span id="error_cluster_not_shared_volume"></span>**ERRO \_ de \_ \_ volume não \_ compartilhado de cluster**
</dt> <dd> <dl> <dt>

5945 (0x1739)
</dt> <dt>



O diretório ou arquivo não está localizado em um volume compartilhado clusterizado.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INVALID_SECURITY_DESCRIPTOR"></span><span id="error_cluster_invalid_security_descriptor"></span>**ERRO \_ \_ \_ descritor de segurança inválido do cluster \_**
</dt> <dd> <dl> <dt>

5946 (0x173A)
</dt> <dt>



O descritor de segurança não atende aos requisitos de um cluster.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_SHARED_VOLUMES_IN_USE"></span><span id="error_cluster_shared_volumes_in_use"></span>**ERRO \_ \_ de volumes compartilhados clusterizados \_ \_ em \_ uso**
</dt> <dd> <dl> <dt>

5947 (0x173B)
</dt> <dt>



Há um ou mais recursos de volumes compartilhados configurados no cluster. Esses recursos devem ser movidos para o armazenamento disponível para que a operação tenha sucesso.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_USE_SHARED_VOLUMES_API"></span><span id="error_cluster_use_shared_volumes_api"></span>**CLUSTER de erros \_ \_ usar a \_ API de \_ volumes compartilhados \_**
</dt> <dd> <dl> <dt>

5948 (0x173C)
</dt> <dt>



Este grupo ou recurso não pode ser manipulado diretamente. Use APIs de volume compartilhado para executar a operação desejada.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_BACKUP_IN_PROGRESS"></span><span id="error_cluster_backup_in_progress"></span>**ERRO \_ \_ de backup \_ do cluster em \_ andamento**
</dt> <dd> <dl> <dt>

5949 (0x173D)
</dt> <dt>



O backup está em andamento. Aguarde a conclusão do backup antes de tentar esta operação novamente.


</dt> </dl> </dd> <dt>

<span id="ERROR_NON_CSV_PATH"></span><span id="error_non_csv_path"></span>**ERRO \_ de \_ caminho não CSV \_**
</dt> <dd> <dl> <dt>

5950 (0x173E)
</dt> <dt>



O caminho não pertence a um volume compartilhado clusterizado.


</dt> </dl> </dd> <dt>

<span id="ERROR_CSV_VOLUME_NOT_LOCAL"></span><span id="error_csv_volume_not_local"></span>**ERRO \_ CSV \_ volume \_ não \_ local**
</dt> <dd> <dl> <dt>

5951 (0x173F)
</dt> <dt>



O volume compartilhado clusterizado não está montado localmente neste nó.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_WATCHDOG_TERMINATING"></span><span id="error_cluster_watchdog_terminating"></span>**ERRO \_ ao \_ encerrar o WATCHDOG do cluster \_**
</dt> <dd> <dl> <dt>

5952 (0x1740)
</dt> <dt>



O Watchdog do cluster está sendo encerrado.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCE_VETOED_MOVE_INCOMPATIBLE_NODES"></span><span id="error_cluster_resource_vetoed_move_incompatible_nodes"></span>**ERRO de \_ cluster de \_ recursos \_ vetado \_ mover \_ nós incompatíveis \_**
</dt> <dd> <dl> <dt>

5953 (0x1741)
</dt> <dt>



Um recurso proibiu uma movimentação entre dois nós porque eles são incompatíveis.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INVALID_NODE_WEIGHT"></span><span id="error_cluster_invalid_node_weight"></span>**ERRO \_ de \_ \_ peso de nó inválido do cluster \_**
</dt> <dd> <dl> <dt>

5954 (0x1742)
</dt> <dt>



A solicitação é inválida porque o peso do nó não pode ser alterado enquanto o cluster estiver no modo de quorum somente de disco ou porque a alteração do peso do nó violaria os requisitos mínimos de quorum do cluster.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCE_VETOED_CALL"></span><span id="error_cluster_resource_vetoed_call"></span>**ERRO \_ de \_ \_ chamada vetada de recurso de cluster \_**
</dt> <dd> <dl> <dt>

5955 (0x1743)
</dt> <dt>



O recurso vetou a chamada.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESMON_SYSTEM_RESOURCES_LACKING"></span><span id="error_resmon_system_resources_lacking"></span>**ERRO \_ resmon \_ recursos do sistema \_ ausentes \_**
</dt> <dd> <dl> <dt>

5956 (0x1744)
</dt> <dt>



O recurso não pôde ser iniciado ou executado porque não pôde reservar recursos de sistema suficientes.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCE_VETOED_MOVE_NOT_ENOUGH_RESOURCES_ON_DESTINATION"></span><span id="error_cluster_resource_vetoed_move_not_enough_resources_on_destination"></span>**ERRO \_ \_ de cluster \_ vetado \_ de recurso mover \_ não \_ há \_ recursos suficientes \_ no \_ destino**
</dt> <dd> <dl> <dt>

5957 (0x1745)
</dt> <dt>



Um recurso proibiu uma movimentação entre dois nós porque o destino atualmente não tem recursos suficientes para concluir a operação.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCE_VETOED_MOVE_NOT_ENOUGH_RESOURCES_ON_SOURCE"></span><span id="error_cluster_resource_vetoed_move_not_enough_resources_on_source"></span>**ERRO \_ \_ de cluster \_ vetado \_ de recurso mover \_ não \_ há \_ recursos suficientes \_ na \_ origem**
</dt> <dd> <dl> <dt>

5958 (0x1746)
</dt> <dt>



Um recurso proibiu uma movimentação entre dois nós porque a origem atualmente não tem recursos suficientes para concluir a operação.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_GROUP_QUEUED"></span><span id="error_cluster_group_queued"></span>**ERRO no \_ grupo de clusters \_ \_ na fila**
</dt> <dd> <dl> <dt>

5959 (0x1747)
</dt> <dt>



A operação solicitada não pode ser concluída porque o grupo está na fila para uma operação.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCE_LOCKED_STATUS"></span><span id="error_cluster_resource_locked_status"></span>**ERRO \_ de \_ \_ status bloqueado do recurso de cluster \_**
</dt> <dd> <dl> <dt>

5960 (0x1748)
</dt> <dt>



A operação solicitada não pode ser concluída porque um recurso tem status bloqueado.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_SHARED_VOLUME_FAILOVER_NOT_ALLOWED"></span><span id="error_cluster_shared_volume_failover_not_allowed"></span>**ERRO \_ de \_ failover de volume compartilhado clusterizado \_ \_ \_ não \_ permitido**
</dt> <dd> <dl> <dt>

5961 (0x1749)
</dt> <dt>



O recurso não pode ser movido para outro nó porque um volume compartilhado clusterizado vetou a operação.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_DRAIN_IN_PROGRESS"></span><span id="error_cluster_node_drain_in_progress"></span>**ERRO \_ \_ \_ no descarregamento \_ do nó de cluster em \_ andamento**
</dt> <dd> <dl> <dt>

5962 (0x174A)
</dt> <dt>



Um descarregamento de nó já está em andamento.

Esse valor também foi chamado **\_ \_ \_ de evacuação de nó \_ de cluster de erro em \_ andamento**


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_DISK_NOT_CONNECTED"></span><span id="error_cluster_disk_not_connected"></span>**ERRO \_ disco de cluster \_ \_ não \_ conectado**
</dt> <dd> <dl> <dt>

5963 (0x174B)
</dt> <dt>



O armazenamento clusterizado não está conectado ao nó.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_NOT_CSV_CAPABLE"></span><span id="error_disk_not_csv_capable"></span>**disco de erro \_ \_ sem \_ capacidade de CSV \_**
</dt> <dd> <dl> <dt>

5964 (0x174C)
</dt> <dt>



O disco não está configurado de forma a ser usado com CSV. Os discos CSV devem ter pelo menos uma partição formatada com NTFS.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_NOT_IN_AVAILABLE_STORAGE"></span><span id="error_resource_not_in_available_storage"></span>**o \_ recurso \_ de erro não \_ \_ está no \_ armazenamento disponível**
</dt> <dd> <dl> <dt>

5965 (0x174D)
</dt> <dt>



o recurso deve fazer parte do grupo de Armazenamento disponível para concluir esta ação.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_SHARED_VOLUME_REDIRECTED"></span><span id="error_cluster_shared_volume_redirected"></span>**ERRO \_ de \_ volume compartilhado clusterizado \_ \_ Redirecionado**
</dt> <dd> <dl> <dt>

5966 (0x174E)
</dt> <dt>



A operação CSVFS com falha como volume está no modo Redirecionado.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_SHARED_VOLUME_NOT_REDIRECTED"></span><span id="error_cluster_shared_volume_not_redirected"></span>**ERRO \_ de \_ volume compartilhado clusterizado \_ \_ não \_ Redirecionado**
</dt> <dd> <dl> <dt>

5967 (0x174F)
</dt> <dt>



A operação CSVFS com falha porque o volume não está no modo Redirecionado.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_CANNOT_RETURN_PROPERTIES"></span><span id="error_cluster_cannot_return_properties"></span>**o \_ cluster de erros \_ não pode \_ retornar \_ Propriedades**
</dt> <dd> <dl> <dt>

5968 (0x1750)
</dt> <dt>



As propriedades do cluster não podem ser retornadas neste momento.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCE_CONTAINS_UNSUPPORTED_DIFF_AREA_FOR_SHARED_VOLUMES"></span><span id="error_cluster_resource_contains_unsupported_diff_area_for_shared_volumes"></span>**o \_ \_ recurso \_ de cluster de erros contém uma \_ \_ área de comparação sem suporte \_ \_ para \_ \_ volumes compartilhados**
</dt> <dd> <dl> <dt>

5969 (0x1751)
</dt> <dt>



O recurso de disco clusterizado contém uma área de comparação de instantâneo de software que não tem suporte para volumes compartilhados clusterizados.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCE_IS_IN_MAINTENANCE_MODE"></span><span id="error_cluster_resource_is_in_maintenance_mode"></span>**ERRO \_ o \_ recurso \_ de cluster está \_ no \_ modo de manutenção \_**
</dt> <dd> <dl> <dt>

5970 (0x1752)
</dt> <dt>



A operação não pode ser concluída porque o recurso está no modo de manutenção.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_AFFINITY_CONFLICT"></span><span id="error_cluster_affinity_conflict"></span>**ERRO \_ de \_ conflito de afinidade de cluster \_**
</dt> <dd> <dl> <dt>

5971 (0x1753)
</dt> <dt>



A operação não pode ser concluída devido a conflitos de afinidade de cluster.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCE_IS_REPLICA_VIRTUAL_MACHINE"></span><span id="error_cluster_resource_is_replica_virtual_machine"></span>**o \_ recurso de cluster de erros \_ é uma \_ \_ \_ máquina virtual de réplica \_**
</dt> <dd> <dl> <dt>

5972 (0x1754)
</dt> <dt>



A operação não pode ser concluída porque o recurso é uma máquina virtual de réplica.


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

 

 




