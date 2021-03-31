---
title: Valores de retorno de BITS
description: O arquivo Bitsmsg. h contém as seguintes constantes de valor de retorno.
ms.assetid: 8df5022a-b161-4558-9d60-efdbdf1754d6
keywords:
- BITS de erros
- BITS de erros, códigos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9086de1d55bbdc9695876bd06368ab28dbbb161
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917550"
---
# <a name="bits-return-values"></a>Valores de retorno de BITS

O arquivo Bitsmsg. h contém as seguintes constantes de valor de retorno. As constantes representam valores de retorno que o BITS gera e valores de retorno HTTP que o BITS captura. Todos os outros valores de retorno que você pode receber são COM, RPC ou valores de retorno do Windows convertidos (o BITS usa o [HRESULT \_ da macro \_ Win32](/windows/win32/api/winerror/nf-winerror-hresult_from_win32) para converter os valores de retorno do Windows em valores HRESULT).

Observe que o arquivo Bitsmsg. h contém valores de retorno adicionais não listados abaixo.

<dl> <dt>

<span id="BG_S_PARTIAL_COMPLETE__0x00200017_"></span><span id="bg_s_partial_complete__0x00200017_"></span><span id="BG_S_PARTIAL_COMPLETE__0X00200017_"></span>\_ \_ Total parcial de BG S \_ (0x00200017)
</dt> <dd>

Um subconjunto dos arquivos do trabalho foi transferido com êxito antes de o método [**método ibackgroundcopyjob:: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) ser chamado. Os que não foram concluídos foram excluídos.

</dd> <dt>

<span id="BG_S_UNABLE_TO_DELETE_FILES__0x0020001A_"></span><span id="bg_s_unable_to_delete_files__0x0020001a_"></span><span id="BG_S_UNABLE_TO_DELETE_FILES__0X0020001A_"></span>BG \_ S \_ não é possível \_ \_ excluir \_ arquivos (0x0020001A)
</dt> <dd>

Não é possível excluir todos os arquivos temporários associados ao trabalho.

</dd> <dt>

<span id="BG_S_OVERRIDDEN_BY_POLICY__0x00200055_"></span><span id="bg_s_overridden_by_policy__0x00200055_"></span><span id="BG_S_OVERRIDDEN_BY_POLICY__0X00200055_"></span>BG \_ S \_ substituído \_ por \_ política (0x00200055)
</dt> <dd>

A preferência de configuração foi salva com êxito, mas a preferência não será usada porque uma configuração de Política de Grupo configurada substitui a preferência.

</dd> <dt>

<span id="BG_E_NOT_FOUND__0x80200001_"></span><span id="bg_e_not_found__0x80200001_"></span><span id="BG_E_NOT_FOUND__0X80200001_"></span>BG \_ E \_ não \_ encontrado (0x80200001)
</dt> <dd>

O trabalho solicitado não foi encontrado.

</dd> <dt>

<span id="BG_E_INVALID_STATE__0x80200002_"></span><span id="bg_e_invalid_state__0x80200002_"></span><span id="BG_E_INVALID_STATE__0X80200002_"></span>\_Estado BG E \_ inválido \_ (0x80200002)
</dt> <dd>

A ação solicitada não é permitida no estado do trabalho atual.

</dd> <dt>

<span id="BG_E_EMPTY__0x80200003_"></span><span id="bg_e_empty__0x80200003_"></span><span id="BG_E_EMPTY__0X80200003_"></span>BG \_ E \_ Empty (0x80200003)
</dt> <dd>

O trabalho deve conter um ou mais arquivos para que você possa retomar o trabalho.

</dd> <dt>

<span id="BG_E_FILE_NOT_AVAILABLE__0x80200004_"></span><span id="bg_e_file_not_available__0x80200004_"></span><span id="BG_E_FILE_NOT_AVAILABLE__0X80200004_"></span>\_Arquivo BG \_ E \_ não \_ disponível (0x80200004)
</dt> <dd>

As informações do arquivo não estão disponíveis porque o erro não está associado a um arquivo local ou remoto.

</dd> <dt>

<span id="BG_E_PROTOCOL_NOT_AVAILABLE__0x80200005_"></span><span id="bg_e_protocol_not_available__0x80200005_"></span><span id="BG_E_PROTOCOL_NOT_AVAILABLE__0X80200005_"></span>\_Protocolo BG \_ E \_ não \_ disponível (0x80200005)
</dt> <dd>

As informações de protocolo não estão disponíveis porque o erro não está associado ao protocolo de transferência especificado.

</dd> <dt>

<span id="BG_E_DESTINATION_LOCKED__0x8020000D_"></span><span id="bg_e_destination_locked__0x8020000d_"></span><span id="BG_E_DESTINATION_LOCKED__0X8020000D_"></span>BG \_ E \_ destino \_ bloqueado (0x8020000D)
</dt> <dd>

O volume do sistema de arquivos de destino, especificado no nome do arquivo local, está bloqueado.

</dd> <dt>

<span id="BG_E_VOLUME_CHANGED__0x8020000E_"></span><span id="bg_e_volume_changed__0x8020000e_"></span><span id="BG_E_VOLUME_CHANGED__0X8020000E_"></span>BG \_ E \_ volume \_ alterado (0x8020000E)
</dt> <dd>

O volume de destino, especificado no nome do arquivo local, foi alterado. Por exemplo, o disquete original foi substituído por um disquete diferente.

</dd> <dt>

<span id="BG_E_ERROR_INFORMATION_UNAVAILABLE__0x8020000F_"></span><span id="bg_e_error_information_unavailable__0x8020000f_"></span><span id="BG_E_ERROR_INFORMATION_UNAVAILABLE__0X8020000F_"></span>\_ \_ Informações de erro BG E \_ \_ indisponíveis (0x8020000F)
</dt> <dd>

As informações de erro só estão disponíveis quando o estado do trabalho é um \_ erro de estado de trabalho BG \_ \_ . As informações de erro não estão disponíveis depois que o BITS começa a transferir os dados do trabalho ou o cliente é encerrado.

</dd> <dt>

<span id="BG_E_NETWORK_DISCONNECTED__0x80200010_"></span><span id="bg_e_network_disconnected__0x80200010_"></span><span id="BG_E_NETWORK_DISCONNECTED__0X80200010_"></span>BG \_ E \_ rede \_ desconectada (0x80200010)
</dt> <dd>

O adaptador de rede está inativo ou desconectado. Todos os trabalhos são colocados no \_ estado de \_ erro temporário de estado do trabalho BG \_ \_ .

</dd> <dt>

<span id="BG_E_MISSING_FILE_SIZE__0x80200011_"></span><span id="bg_e_missing_file_size__0x80200011_"></span><span id="BG_E_MISSING_FILE_SIZE__0X80200011_"></span>BG \_ E \_ \_ \_ tamanho de arquivo ausente (0x80200011)
</dt> <dd>

O servidor não retornou o tamanho do arquivo. O BITS só transfere conteúdo estático e requer que o servidor HTTP retorne o cabeçalho Content-Length. A solicitação de transferência falhará se a URL apontar para o conteúdo dinâmico.

</dd> <dt>

<span id="BG_E_INSUFFICIENT_HTTP_SUPPORT__0x80200012_"></span><span id="bg_e_insufficient_http_support__0x80200012_"></span><span id="BG_E_INSUFFICIENT_HTTP_SUPPORT__0X80200012_"></span>Suporte a BG \_ E \_ http insuficiente \_ \_ (0x80200012)
</dt> <dd>

O servidor não oferece suporte ao protocolo HTTP/1.1.

</dd> <dt>

<span id="BG_E_INSUFFICIENT_RANGE_SUPPORT__0x80200013_"></span><span id="bg_e_insufficient_range_support__0x80200013_"></span><span id="BG_E_INSUFFICIENT_RANGE_SUPPORT__0X80200013_"></span>\_Suporte a intervalo BG E \_ insuficiente \_ \_ (0x80200013)
</dt> <dd>

O servidor não oferece suporte ao cabeçalho Content-Range. Normalmente, você recebe esse erro quando tenta baixar conteúdo dinâmico. Você também poderá receber esse erro se um proxy intermediário estiver removendo o cabeçalho Content-Range ou Content-Length.

</dd> <dt>

<span id="BG_E_REMOTE_NOT_SUPPORTED__0x80200014_"></span><span id="bg_e_remote_not_supported__0x80200014_"></span><span id="BG_E_REMOTE_NOT_SUPPORTED__0X80200014_"></span>\_ \_ \_ Não \_ há suporte para BG E remoto (0x80200014)
</dt> <dd>

Não há suporte para o uso remoto de BITS. Para obter mais informações, consulte [usuários e conexões de rede](users-and-network-connections.md).

</dd> <dt>

<span id="BG_E_NEW_OWNER_DIFF_MAPPING__0x80200015_"></span><span id="bg_e_new_owner_diff_mapping__0x80200015_"></span><span id="BG_E_NEW_OWNER_DIFF_MAPPING__0X80200015_"></span>BG \_ E \_ novo \_ \_ mapeamento diff \_ do proprietário (0x80200015)
</dt> <dd>

O mapeamento de unidade de rede para o arquivo local é diferente para o proprietário atual do que para o proprietário anterior.

</dd> <dt>

<span id="BG_E_NEW_OWNER_NO_FILE_ACCESS__0x80200016_"></span><span id="bg_e_new_owner_no_file_access__0x80200016_"></span><span id="BG_E_NEW_OWNER_NO_FILE_ACCESS__0X80200016_"></span>BG \_ E \_ novo \_ proprietário \_ sem \_ \_ acesso de arquivo (0x80200016)
</dt> <dd>

O novo proprietário tem permissões insuficientes para os arquivos de trabalho temporários.

</dd> <dt>

<span id="BG_E_PROXY_LIST_TOO_LARGE__0x80200018_"></span><span id="bg_e_proxy_list_too_large__0x80200018_"></span><span id="BG_E_PROXY_LIST_TOO_LARGE__0X80200018_"></span>\_ \_ Lista de proxy BG E \_ \_ muito \_ grande (0x80200018)
</dt> <dd>

A lista de proxy HTTP é muito longa. A lista não deve exceder 32 KB.

</dd> <dt>

<span id="BG_E_PROXY_BYPASS_LIST_TOO_LARGE__0x80200019_"></span><span id="bg_e_proxy_bypass_list_too_large__0x80200019_"></span><span id="BG_E_PROXY_BYPASS_LIST_TOO_LARGE__0X80200019_"></span>\_ \_ \_ Lista de bypass E proxy BG \_ \_ muito \_ grande (0x80200019)
</dt> <dd>

A lista de bypass de proxy HTTP é muito longa. A lista não deve exceder 32 KB.

</dd> <dt>

<span id="BG_E_TOO_MANY_FILES__0x8020001C_"></span><span id="bg_e_too_many_files__0x8020001c_"></span><span id="BG_E_TOO_MANY_FILES__0X8020001C_"></span>BG \_ E \_ \_ muitos \_ arquivos (0x8020001C)
</dt> <dd>

Você não pode adicionar mais de um arquivo a um trabalho de carregamento.

</dd> <dt>

<span id="BG_E_LOCAL_FILE_CHANGED__0x8020001D_"></span><span id="bg_e_local_file_changed__0x8020001d_"></span><span id="BG_E_LOCAL_FILE_CHANGED__0X8020001D_"></span>BG \_ E \_ \_ arquivo local \_ alterado (0x8020001D)
</dt> <dd>

O conteúdo do arquivo local foi alterado após o início do processo de transferência. O conteúdo do arquivo local não pode ser alterado depois que o processo de transferência é iniciado em um trabalho de upload ou de resposta de upload.

</dd> <dt>

<span id="BG_E_TOO_LARGE__0x80200020_"></span><span id="bg_e_too_large__0x80200020_"></span><span id="BG_E_TOO_LARGE__0X80200020_"></span>BG \_ E \_ muito \_ grande (0x80200020)
</dt> <dd>

O tamanho do arquivo de carregamento excede o tamanho máximo de upload permitido especificado no servidor.

</dd> <dt>

<span id="BG_E_STRING_TOO_LONG__0x80200021_"></span><span id="bg_e_string_too_long__0x80200021_"></span><span id="BG_E_STRING_TOO_LONG__0X80200021_"></span>\_ \_ Cadeia de caracteres BG E \_ muito \_ longa (0x80200021)
</dt> <dd>

A cadeia de caracteres especificada é muito longa.

</dd> <dt>

<span id="BG_E_CLIENT_SERVER_PROTOCOL_MISMATCH__0x80200022_"></span><span id="bg_e_client_server_protocol_mismatch__0x80200022_"></span><span id="BG_E_CLIENT_SERVER_PROTOCOL_MISMATCH__0X80200022_"></span>\_Incompatibilidade \_ de protocolo BG E cliente \_ do servidor \_ \_ (0x80200022)
</dt> <dd>

O cliente e o servidor não conseguiram negociar um protocolo a ser usado para o trabalho de carregamento.

</dd> <dt>

<span id="BG_E_SERVER_EXECUTE_ENABLED__0x80200023_"></span><span id="bg_e_server_execute_enabled__0x80200023_"></span><span id="BG_E_SERVER_EXECUTE_ENABLED__0X80200023_"></span>BG \_ E \_ Server \_ Execute \_ habilitados (0x80200023)
</dt> <dd>

As permissões de script ou execução são habilitadas no diretório virtual do IIS associado ao trabalho. Para carregar arquivos no diretório virtual, desabilite as permissões de script e execução no diretório virtual.

</dd> <dt>

<span id="BG_E_USERNAME_TOO_LARGE__0x80200025_"></span><span id="bg_e_username_too_large__0x80200025_"></span><span id="BG_E_USERNAME_TOO_LARGE__0X80200025_"></span>BG \_ E \_ nome \_ de usuário muito \_ grande (0x80200025)
</dt> <dd>

O nome de usuário não pode exceder 300 caracteres.

</dd> <dt>

<span id="BG_E_PASSWORD_TOO_LARGE__0x80200026_"></span><span id="bg_e_password_too_large__0x80200026_"></span><span id="BG_E_PASSWORD_TOO_LARGE__0X80200026_"></span>BG \_ E \_ senha \_ muito \_ grande (0x80200026)
</dt> <dd>

A senha não pode exceder 65535 caracteres.

</dd> <dt>

<span id="BG_E_INVALID_AUTH_TARGET__0x80200027_"></span><span id="bg_e_invalid_auth_target__0x80200027_"></span><span id="BG_E_INVALID_AUTH_TARGET__0X80200027_"></span>BG \_ E \_ \_ \_ destino de autenticação inválido (0x80200027)
</dt> <dd>

O destino de autenticação especificado não é válido.

</dd> <dt>

<span id="BG_E_INVALID_AUTH_SCHEME__0x80200028_"></span><span id="bg_e_invalid_auth_scheme__0x80200028_"></span><span id="BG_E_INVALID_AUTH_SCHEME__0X80200028_"></span>BG \_ E \_ \_ \_ esquema de autenticação inválido (0x80200028)
</dt> <dd>

O esquema de autenticação especificado não é válido.

</dd> <dt>

<span id="BG_E_INVALID_RANGE__0x8020002B_"></span><span id="bg_e_invalid_range__0x8020002b_"></span><span id="BG_E_INVALID_RANGE__0X8020002B_"></span>\_Intervalo BG E \_ inválido \_ (0x8020002B)
</dt> <dd>

O intervalo de bytes especificado é inválido. O intervalo de bytes deve existir dentro do arquivo remoto especificado.

</dd> <dt>

<span id="BG_E_OVERLAPPING_RANGES__0x8020002C_"></span><span id="bg_e_overlapping_ranges__0x8020002c_"></span><span id="BG_E_OVERLAPPING_RANGES__0X8020002C_"></span>\_ \_ \_ 0x8020002C (intervalos de sobreposição BG)
</dt> <dd>

A lista de intervalos de bytes contém intervalos sobrepostos ou duplicados, que não têm suporte.

</dd> <dt>

<span id="BG_E_BLOCKED_BY_POLICY__0x8020003E_"></span><span id="bg_e_blocked_by_policy__0x8020003e_"></span><span id="BG_E_BLOCKED_BY_POLICY__0X8020003E_"></span>BG \_ E \_ bloqueado \_ pela \_ política (0x8020003E)
</dt> <dd>

Política de Grupo configurações impedem que trabalhos em segundo plano sejam executados no momento. Para obter detalhes, consulte a política [MaxInternetBandwidth](group-policies.md) .

</dd> <dt>

<span id="BG_E_INVALID_PROXY_INFO__0x8020003F_"></span><span id="bg_e_invalid_proxy_info__0x8020003f_"></span><span id="BG_E_INVALID_PROXY_INFO__0X8020003F_"></span>\_ \_ Informações de proxy inválidas BG E \_ \_ (0x8020003F)
</dt> <dd>

Erro de tempo de execução que indica que a lista de proxy ou a lista de bypass de proxy que você especificou usando o método [**método ibackgroundcopyjob:: SetProxySettings**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) é inválida.

</dd> <dt>

<span id="BG_E_INVALID_CREDENTIALS__0x80200040_"></span><span id="bg_e_invalid_credentials__0x80200040_"></span><span id="BG_E_INVALID_CREDENTIALS__0X80200040_"></span>\_ \_ Credenciais de BG E inválidas \_ (0x80200040)
</dt> <dd>

O formato das credenciais de segurança fornecidas não é válido.

</dd> <dt>

<span id="BG_E_RECORD_DELETED__0x80200042_"></span><span id="bg_e_record_deleted__0x80200042_"></span><span id="BG_E_RECORD_DELETED__0X80200042_"></span>BG \_ E \_ registro \_ excluído (0x80200042)
</dt> <dd>

O registro de cache foi excluído. A tentativa de atualizá-la foi abandonada.

</dd> <dt>

<span id="BG_E_UPNP_ERROR__0x80200045_"></span><span id="bg_e_upnp_error__0x80200045_"></span><span id="BG_E_UPNP_ERROR__0X80200045_"></span>\_Erro BG E \_ UPnP \_ (0x80200045)
</dt> <dd>

Ocorreu um erro Universal Plug and Play (UPnP). Verifique seu dispositivo de gateway de Internet.

</dd> <dt>

<span id="BG_E_PEERCACHING_DISABLED__0x80200047_"></span><span id="bg_e_peercaching_disabled__0x80200047_"></span><span id="BG_E_PEERCACHING_DISABLED__0X80200047_"></span>BG \_ E em \_ cache \_ desabilitado (0x80200047)
</dt> <dd>

O cache de pares está desabilitado.

</dd> <dt>

<span id="BG_E_BUSYCACHERECORD__0x80200048_"></span><span id="bg_e_busycacherecord__0x80200048_"></span><span id="BG_E_BUSYCACHERECORD__0X80200048_"></span>BG \_ E \_ BUSYCACHERECORD (0x80200048)
</dt> <dd>

O registro de cache está em uso e não pode ser alterado ou excluído. Tente novamente após alguns segundos.

</dd> <dt>

<span id="BG_E_TOO_MANY_JOBS_PER_USER__0x80200049_"></span><span id="bg_e_too_many_jobs_per_user__0x80200049_"></span><span id="BG_E_TOO_MANY_JOBS_PER_USER__0X80200049_"></span>BG \_ E \_ \_ muitos \_ trabalhos \_ por \_ usuário (0x80200049)
</dt> <dd>

A contagem de trabalhos para o usuário excedeu o limite de trabalho por usuário definido pela configuração de Política de Grupo MaxJobsPerUser.

</dd> <dt>

<span id="BG_E_TOO_MANY_JOBS_PER_MACHINE__0x80200050_"></span><span id="bg_e_too_many_jobs_per_machine__0x80200050_"></span><span id="BG_E_TOO_MANY_JOBS_PER_MACHINE__0X80200050_"></span>BG \_ E \_ \_ muitos \_ trabalhos \_ por \_ máquina (0x80200050)
</dt> <dd>

A contagem de trabalhos para o computador excedeu o limite de trabalho por computador definido pela configuração de Política de Grupo MaxJobsPerMachine.

</dd> <dt>

<span id="BG_E_TOO_MANY_FILES_IN_JOB__0x80200051_"></span><span id="bg_e_too_many_files_in_job__0x80200051_"></span><span id="BG_E_TOO_MANY_FILES_IN_JOB__0X80200051_"></span>BG \_ E \_ \_ muitos \_ arquivos \_ no \_ trabalho (0x80200051)
</dt> <dd>

A contagem de arquivos para o trabalho excedeu o limite de arquivos por trabalho definido pela configuração de Política de Grupo MaxFilesPerJob.

</dd> <dt>

<span id="BG_E_TOO_MANY_RANGES_IN_FILE__0x80200052_"></span><span id="bg_e_too_many_ranges_in_file__0x80200052_"></span><span id="BG_E_TOO_MANY_RANGES_IN_FILE__0X80200052_"></span>BG \_ E um número \_ \_ excessivo \_ \_ de intervalos no \_ arquivo (0x80200052)
</dt> <dd>

A contagem de intervalos para o arquivo excedeu o limite por intervalo de arquivos definido pela configuração de Política de Grupo MaxRangesPerFile.

</dd> <dt>

<span id="BG_E_VALIDATION_FAILED__0x80200053_"></span><span id="bg_e_validation_failed__0x80200053_"></span><span id="BG_E_VALIDATION_FAILED__0X80200053_"></span>\_ \_ \_ Falha na validação de BG E (0x80200053)
</dt> <dd>

O aplicativo solicitou dados de um site, mas a resposta não era válida. Para obter detalhes, use Visualizador de Eventos para exibir os logs de aplicativo \\ \\ \\ log operacional Microsoft Windows bits-cliente \\ .

</dd> <dt>

<span id="BG_E_MAXDOWNLOAD_TIMEOUT__0x80200054_"></span><span id="bg_e_maxdownload_timeout__0x80200054_"></span><span id="BG_E_MAXDOWNLOAD_TIMEOUT__0X80200054_"></span>\_ \_ \_ Tempo limite de BG E MAXDOWNLOAD (0x80200054)
</dt> <dd>

O BITS atingiu o tempo limite baixando o trabalho. O download não foi concluído dentro do tempo de download máximo definido no trabalho ou na configuração de Política de Grupo MaxDownloadTime.

</dd> <dt>

<span id="BG_E_HTTP_ERROR_400__0x80190190_"></span><span id="bg_e_http_error_400__0x80190190_"></span><span id="BG_E_HTTP_ERROR_400__0X80190190_"></span>\_Erro BG \_ E \_ http \_ 400 (0x80190190)
</dt> <dd>

O servidor não pôde processar a solicitação de transferência porque a sintaxe do nome do arquivo remoto é inválida.

</dd> <dt>

<span id="BG_E_HTTP_ERROR_401__0x80190191_"></span><span id="bg_e_http_error_401__0x80190191_"></span><span id="BG_E_HTTP_ERROR_401__0X80190191_"></span>\_Erro BG \_ E \_ http \_ 401 (0x80190191)
</dt> <dd>

O usuário não tem permissão para acessar o arquivo remoto. O recurso solicitado requer a autenticação do usuário.

</dd> <dt>

<span id="BG_E_HTTP_ERROR_404__0x80190194_"></span><span id="bg_e_http_error_404__0x80190194_"></span><span id="BG_E_HTTP_ERROR_404__0X80190194_"></span>\_Erro BG \_ E \_ http \_ 404 (0x80190194)
</dt> <dd>

A URL solicitada não existe no servidor.

No IIS 7, esse erro pode indicar

-   Esses carregamentos do BITS não estão habilitados no diretório virtual (vdir) no servidor.
-   Que o tamanho do carregamento exceda o limite máximo de upload (para obter detalhes, consulte a propriedade de extensão do IIS [**BITSMaximumUploadSize**](bits-iis-extension-properties.md) ).

</dd> <dt>

<span id="BG_E_HTTP_ERROR_407__0x80190197_"></span><span id="bg_e_http_error_407__0x80190197_"></span><span id="BG_E_HTTP_ERROR_407__0X80190197_"></span>\_Erro BG \_ E \_ http \_ 407 (0x80190197)
</dt> <dd>

O usuário não tem permissão para acessar o proxy. O proxy requer autenticação do usuário.

</dd> <dt>

<span id="BG_E_HTTP_ERROR_414__0x8019019E_"></span><span id="bg_e_http_error_414__0x8019019e_"></span><span id="BG_E_HTTP_ERROR_414__0X8019019E_"></span>\_Erro BG \_ E \_ http \_ 414 (0x8019019E)
</dt> <dd>

O servidor não pode processar a solicitação de transferência. O Uniform Resource Identifier (URI) no nome do arquivo remoto é maior do que o servidor pode interpretar.

</dd> <dt>

<span id="BG_E_HTTP_ERROR_501__0x801901F5_"></span><span id="bg_e_http_error_501__0x801901f5_"></span><span id="BG_E_HTTP_ERROR_501__0X801901F5_"></span>\_Erro BG \_ E \_ http \_ 501 (0x801901F5)
</dt> <dd>

O servidor não oferece suporte à funcionalidade necessária para atender à solicitação. No IIS 6, esse erro indica que os carregamentos do BITS não estão habilitados no diretório virtual (vdir) no servidor.

</dd> <dt>

<span id="BG_E_HTTP_ERROR_503__0x801901F7_"></span><span id="bg_e_http_error_503__0x801901f7_"></span><span id="BG_E_HTTP_ERROR_503__0X801901F7_"></span>\_Erro BG \_ E \_ http \_ 503 (0x801901F7)
</dt> <dd>

O serviço está temporariamente sobrecarregado e não pode processar a solicitação. Retome o trabalho em um momento posterior.

</dd> <dt>

<span id="BG_E_HTTP_ERROR_504__0x801901F8_"></span><span id="bg_e_http_error_504__0x801901f8_"></span><span id="BG_E_HTTP_ERROR_504__0X801901F8_"></span>\_Erro BG \_ E \_ http \_ 504 (0x801901F8)
</dt> <dd>

A solicitação de transferência atingiu o tempo limite enquanto aguardava um gateway. Retome o trabalho em um momento posterior.

</dd> <dt>

<span id="BG_E_HTTP_ERROR_505__0x801901F9_"></span><span id="bg_e_http_error_505__0x801901f9_"></span><span id="BG_E_HTTP_ERROR_505__0X801901F9_"></span>\_Erro BG \_ E \_ http \_ 505 (0x801901F9)
</dt> <dd>

O servidor não oferece suporte à versão do protocolo HTTP especificada no nome do arquivo remoto.

</dd> </dl>

O arquivo de cabeçalho Bitsmsg. h contém valores adicionais de retorno de HTTP não listados acima que os BITS usam internamente. Para obter informações sobre esses e outros valores de retorno de HTTP que você pode receber, consulte a especificação RFC 2616 da força de tarefas de engenharia da Internet em [https://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html\#sec10](https://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html#sec10) .

 

 