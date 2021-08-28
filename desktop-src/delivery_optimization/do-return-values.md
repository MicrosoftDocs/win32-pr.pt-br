---
title: Valores de retorno
description: As constantes abaixo representam valores de retorno que a otimização de entrega gera e valores de retorno HTTP que capturam.
ms.assetid: 68AC4581-C748-49AB-A588-15816E534756
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e16dc435fa22268d92c4403709a5444b1b87e325d66429da853844fd7f836b40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118101847"
---
# <a name="do-return-values"></a>Valores de retorno

As constantes abaixo representam valores de retorno que a otimização de entrega gera e valores de retorno HTTP que capturam. todos os outros valores de retorno que você pode receber são COM, RPC ou convertidos Windows valores de retorno (usa a macro [HRESULT_FROM_WIN32](/windows/win32/api/winerror/nf-winerror-hresult_from_win32) para converter os valores de retorno Windows em valores HRESULT).

<dl> <dt>

<span id="DO_E_NO_SERVICE__0x80d01001_"></span><span id="do_e_no_service__0x80d01001_"></span><span id="DO_E_NO_SERVICE__0X80D01001_"></span>DO_E_NO_SERVICE (0x80d01001)
</dt> <dd>

A otimização de entrega não pôde fornecer o serviço.

</dd> <dt>

<span id="DO_E_DOWNLOAD_NO_PROGRESS__0x80d02002_"></span><span id="do_e_download_no_progress__0x80d02002_"></span><span id="DO_E_DOWNLOAD_NO_PROGRESS__0X80D02002_"></span>DO_E_DOWNLOAD_NO_PROGRESS (0x80d02002)
</dt> <dd>

O download de um arquivo não viu nenhum progresso dentro do período definido.

</dd> <dt>

<span id="DO_E_JOB_NOT_FOUND__0x80d02003_"></span><span id="do_e_job_not_found__0x80d02003_"></span><span id="DO_E_JOB_NOT_FOUND__0X80D02003_"></span>DO_E_JOB_NOT_FOUND (0x80d02003)
</dt> <dd>

O trabalho não foi encontrado, esperando que um trabalho esteja presente.

</dd> <dt>

<span id="DO_E_JOB_EMPTY__0x80d02004_"></span><span id="do_e_job_empty__0x80d02004_"></span><span id="DO_E_JOB_EMPTY__0X80D02004_"></span>DO_E_JOB_EMPTY (0x80d02004)
</dt> <dd>

Não havia nenhum arquivo no trabalho, esperando pelo menos um arquivo.

</dd> <dt>

<span id="DO_E_LOCALPATH_NOT_SET__0x80d0200d_"></span><span id="do_e_localpath_not_set__0x80d0200d_"></span><span id="DO_E_LOCALPATH_NOT_SET__0X80D0200D_"></span>DO_E_LOCALPATH_NOT_SET (0x80d0200d)
</dt> <dd>

Não há nenhum caminho de arquivo local especificado para este download.

</dd> <dt>

<span id="DO_E_FILE_NOT_AVAILABLE__0x80d02010_"></span><span id="do_e_file_not_available__0x80d02010_"></span><span id="DO_E_FILE_NOT_AVAILABLE__0X80D02010_"></span>DO_E_FILE_NOT_AVAILABLE (0x80d02010)
</dt> <dd>

Nenhum arquivo está disponível porque nenhuma URL gerou um erro.

</dd> <dt>

<span id="DO_E_UNKNOWN_PROPERTY_ID__0x80d02011_"></span><span id="do_e_unknown_property_id__0x80d02011_"></span><span id="DO_E_UNKNOWN_PROPERTY_ID__0X80D02011_"></span>DO_E_UNKNOWN_PROPERTY_ID (0x80d02011)
</dt> <dd>

SetProperty () ou GetProperty () chamado com uma ID de propriedade desconhecida.

</dd> <dt>

<span id="DO_E_READ_ONLY_PROPERTY__0x80d02012_"></span><span id="do_e_read_only_property__0x80d02012_"></span><span id="DO_E_READ_ONLY_PROPERTY__0X80D02012_"></span>DO_E_READ_ONLY_PROPERTY (0x80d02012)
</dt> <dd>

Não é possível chamar SetProperty () em uma propriedade somente leitura.

</dd> <dt>

<span id="DO_E_INVALID_STATE__0x80d02013_"></span><span id="do_e_invalid_state__0x80d02013_"></span><span id="DO_E_INVALID_STATE__0X80D02013_"></span>DO_E_INVALID_STATE (0x80d02013)
</dt> <dd>

A operação solicitada não é permitida no estado de trabalho atual. O trabalho poderia ter sido cancelado ou concluído a transferência.

</dd> <dt>

<span id="DO_E_ERROR_INFORMATION_UNAVAILABLE__0x80d02014_"></span><span id="do_e_error_information_unavailable__0x80d02014_"></span><span id="DO_E_ERROR_INFORMATION_UNAVAILABLE__0X80D02014_"></span>DO_E_ERROR_INFORMATION_UNAVAILABLE (0x80d02014)
</dt> <dd>

Não ocorreu nenhum erro.

</dd> <dt>

<span id="DO_E_NO_DOWNLOAD_EXTSETTINGS__0x80d03002_"></span><span id="do_e_no_download_extsettings__0x80d03002_"></span><span id="DO_E_NO_DOWNLOAD_EXTSETTINGS__0X80D03002_"></span>DO_E_NO_DOWNLOAD_EXTSETTINGS (0x80d03002)
</dt> <dd>

O trabalho de download não é permitido devido a configurações de usuário/administrador.

</dd> <dt>

<span id="DO_E_BLOCKED_BY_COST_TRANSFER_POLICY__0x80d03801_"></span><span id="do_e_blocked_by_cost_transfer_policy__0x80d03801_"></span><span id="DO_E_BLOCKED_BY_COST_TRANSFER_POLICY__0X80D03801_"></span>DO_E_BLOCKED_BY_COST_TRANSFER_POLICY (0x80d03801)
</dt> <dd>

O trabalho foi pausado devido a restrições de política de custo.

</dd> <dt>

<span id="DO_E_BLOCKED_BY_CELLULAR_POLICY__0x80d03803_"></span><span id="do_e_blocked_by_cellular_policy__0x80d03803_"></span><span id="DO_E_BLOCKED_BY_CELLULAR_POLICY__0X80D03803_"></span>DO_E_BLOCKED_BY_CELLULAR_POLICY (0x80d03803)
</dt> <dd>

Pausou o trabalho devido à detecção de restrições de política e rede celular.

</dd> <dt>

<span id="DO_E_BLOCKED_BY_POWER_STATE__0x80d03804_"></span><span id="do_e_blocked_by_power_state__0x80d03804_"></span><span id="DO_E_BLOCKED_BY_POWER_STATE__0X80D03804_"></span>DO_E_BLOCKED_BY_POWER_STATE (0x80d03804)
</dt> <dd>

Pausou o trabalho devido à detecção da alteração do estado de energia no modo não AC.

</dd> <dt>

<span id="DO_E_BLOCKED_BY_NO_NETWORK__0x80d03805_"></span><span id="do_e_blocked_by_no_network__0x80d03805_"></span><span id="DO_E_BLOCKED_BY_NO_NETWORK__0X80D03805_"></span>DO_E_BLOCKED_BY_NO_NETWORK (0x80d03805)
</dt> <dd>

Pausou o trabalho devido à perda de conectividade de rede.

</dd> <dt>

<span id="DO_E_BLOCKED_BY_VPN_POLICY__0x80d03807_"></span><span id="do_e_blocked_by_vpn_policy__0x80d03807_"></span><span id="DO_E_BLOCKED_BY_VPN_POLICY__0X80D03807_"></span>DO_E_BLOCKED_BY_VPN_POLICY (0x80d03807)
</dt> <dd>

Pausou o trabalho concluído devido à detecção da rede VPN.

</dd> <dt>

<span id="DO_E_BLOCKED_BY_CRITICAL_MEMORY_USAGE__0x80d03808_"></span><span id="do_e_blocked_by_critical_memory_usage__0x80d03808_"></span><span id="DO_E_BLOCKED_BY_CRITICAL_MEMORY_USAGE__0X80D03808_"></span>DO_E_BLOCKED_BY_CRITICAL_MEMORY_USAGE (0x80d03808)
</dt> <dd>

Pausou o trabalho concluído devido à detecção de uso de memória crítica no sistema.

</dd> <dt>

<span id="DO_E_HTTP_BLOCKSIZE_MISMATCH__0x80d05001_"></span><span id="do_e_http_blocksize_mismatch__0x80d05001_"></span><span id="DO_E_HTTP_BLOCKSIZE_MISMATCH__0X80D05001_"></span>DO_E_HTTP_BLOCKSIZE_MISMATCH (0x80d05001)
</dt> <dd>

O servidor HTTP retornou uma resposta com tamanho de dados diferente do que foi solicitado.

</dd> <dt>

<span id="DO_E_INVALID_RANGE__0x80d05010_"></span><span id="do_e_invalid_range__0x80d05010_"></span><span id="DO_E_INVALID_RANGE__0X80D05010_"></span>DO_E_INVALID_RANGE (0x80d05010)
</dt> <dd>

O intervalo de bytes especificado é inválido.

</dd> <dt>

<span id="DO_E_INSUFFICIENT_RANGE_SUPPORT__0x80d05011_"></span><span id="do_e_insufficient_range_support__0x80d05011_"></span><span id="DO_E_INSUFFICIENT_RANGE_SUPPORT__0X80D05011_"></span>DO_E_INSUFFICIENT_RANGE_SUPPORT (0x80d05011)
</dt> <dd>

O servidor não oferece suporte ao protocolo HTTP necessário. A otimização de entrega (DO) exige que o servidor dê suporte ao cabeçalho de protocolo do intervalo.

</dd> <dt>

<span id="DO_E_OVERLAPPING_RANGES__0x80d05012_"></span><span id="do_e_overlapping_ranges__0x80d05012_"></span><span id="DO_E_OVERLAPPING_RANGES__0X80D05012_"></span>DO_E_OVERLAPPING_RANGES (0x80d05012)
</dt> <dd>

A lista de intervalos de bytes contém alguns intervalos sobrepostos, que não têm suporte.

</dd> <dt>

<span id="DO_E_FATAL_CORE_ERROR__0x80d06802_"></span><span id="do_e_fatal_core_error__0x80d06802_"></span><span id="DO_E_FATAL_CORE_ERROR__0X80D06802_"></span>DO_E_FATAL_CORE_ERROR (0x80d06802)
</dt> <dd>

Erro fatal encontrado no núcleo.

</dd> </dl>

 

 