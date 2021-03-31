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
# <a name="bits-return-values"></a><span data-ttu-id="0a5cc-105">Valores de retorno de BITS</span><span class="sxs-lookup"><span data-stu-id="0a5cc-105">BITS Return Values</span></span>

<span data-ttu-id="0a5cc-106">O arquivo Bitsmsg. h contém as seguintes constantes de valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="0a5cc-106">The Bitsmsg.h file contains the following return value constants.</span></span> <span data-ttu-id="0a5cc-107">As constantes representam valores de retorno que o BITS gera e valores de retorno HTTP que o BITS captura.</span><span class="sxs-lookup"><span data-stu-id="0a5cc-107">The constants represent return values that BITS generates and HTTP return values that BITS captures.</span></span> <span data-ttu-id="0a5cc-108">Todos os outros valores de retorno que você pode receber são COM, RPC ou valores de retorno do Windows convertidos (o BITS usa o [HRESULT \_ da macro \_ Win32](/windows/win32/api/winerror/nf-winerror-hresult_from_win32) para converter os valores de retorno do Windows em valores HRESULT).</span><span class="sxs-lookup"><span data-stu-id="0a5cc-108">All other return values that you can receive are COM, RPC, or converted Windows return values (BITS uses the [HRESULT\_FROM\_WIN32](/windows/win32/api/winerror/nf-winerror-hresult_from_win32) macro to convert the Windows return values to HRESULT values).</span></span>

<span data-ttu-id="0a5cc-109">Observe que o arquivo Bitsmsg. h contém valores de retorno adicionais não listados abaixo.</span><span class="sxs-lookup"><span data-stu-id="0a5cc-109">Note that the Bitsmsg.h file contains additional return values not listed below.</span></span>

<dl> <dt>

<span data-ttu-id="0a5cc-110"><span id="BG_S_PARTIAL_COMPLETE__0x00200017_"></span><span id="bg_s_partial_complete__0x00200017_"></span><span id="BG_S_PARTIAL_COMPLETE__0X00200017_"></span>\_ \_ Total parcial de BG S \_ (0x00200017)</span><span class="sxs-lookup"><span data-stu-id="0a5cc-110"><span id="BG_S_PARTIAL_COMPLETE__0x00200017_"></span><span id="bg_s_partial_complete__0x00200017_"></span><span id="BG_S_PARTIAL_COMPLETE__0X00200017_"></span>BG\_S\_PARTIAL\_COMPLETE (0x00200017)</span></span>
</dt> <dd>

<span data-ttu-id="0a5cc-111">Um subconjunto dos arquivos do trabalho foi transferido com êxito antes de o método [**método ibackgroundcopyjob:: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) ser chamado.</span><span class="sxs-lookup"><span data-stu-id="0a5cc-111">A subset of the job's files transferred successfully before the [**IBackgroundCopyJob::Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) method was called.</span></span> <span data-ttu-id="0a5cc-112">Os que não foram concluídos foram excluídos.</span><span class="sxs-lookup"><span data-stu-id="0a5cc-112">Those that were not complete were deleted.</span></span>

</dd> <dt>

<span data-ttu-id="0a5cc-113"><span id="BG_S_UNABLE_TO_DELETE_FILES__0x0020001A_"></span><span id="bg_s_unable_to_delete_files__0x0020001a_"></span><span id="BG_S_UNABLE_TO_DELETE_FILES__0X0020001A_"></span>BG \_ S \_ não é possível \_ \_ excluir \_ arquivos (0x0020001A)</span><span class="sxs-lookup"><span data-stu-id="0a5cc-113"><span id="BG_S_UNABLE_TO_DELETE_FILES__0x0020001A_"></span><span id="bg_s_unable_to_delete_files__0x0020001a_"></span><span id="BG_S_UNABLE_TO_DELETE_FILES__0X0020001A_"></span>BG\_S\_UNABLE\_TO\_DELETE\_FILES (0x0020001A)</span></span>
</dt> <dd>

<span data-ttu-id="0a5cc-114">Não é possível excluir todos os arquivos temporários associados ao trabalho.</span><span class="sxs-lookup"><span data-stu-id="0a5cc-114">Unable to delete all temporary files associated with the job.</span></span>

</dd> <dt>

<span data-ttu-id="0a5cc-115"><span id="BG_S_OVERRIDDEN_BY_POLICY__0x00200055_"></span><span id="bg_s_overridden_by_policy__0x00200055_"></span><span id="BG_S_OVERRIDDEN_BY_POLICY__0X00200055_"></span>BG \_ S \_ substituído \_ por \_ política (0x00200055)</span><span class="sxs-lookup"><span data-stu-id="0a5cc-115"><span id="BG_S_OVERRIDDEN_BY_POLICY__0x00200055_"></span><span id="bg_s_overridden_by_policy__0x00200055_"></span><span id="BG_S_OVERRIDDEN_BY_POLICY__0X00200055_"></span>BG\_S\_OVERRIDDEN\_BY\_POLICY (0x00200055)</span></span>
</dt> <dd>

<span data-ttu-id="0a5cc-116">A preferência de configuração foi salva com êxito, mas a preferência não será usada porque uma configuração de Política de Grupo configurada substitui a preferência.</span><span class="sxs-lookup"><span data-stu-id="0a5cc-116">The configuration preference has been saved successfully, but the preference will not be used because a configured Group Policy setting overrides the preference.</span></span>

</dd> <dt>

<span data-ttu-id="0a5cc-117"><span id="BG_E_NOT_FOUND__0x80200001_"></span><span id="bg_e_not_found__0x80200001_"></span><span id="BG_E_NOT_FOUND__0X80200001_"></span>BG \_ E \_ não \_ encontrado (0x80200001)</span><span class="sxs-lookup"><span data-stu-id="0a5cc-117"><span id="BG_E_NOT_FOUND__0x80200001_"></span><span id="bg_e_not_found__0x80200001_"></span><span id="BG_E_NOT_FOUND__0X80200001_"></span>BG\_E\_NOT\_FOUND (0x80200001)</span></span>
</dt> <dd>

<span data-ttu-id="0a5cc-118">O trabalho solicitado não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="0a5cc-118">The requested job was not found.</span></span>

</dd> <dt>

<span data-ttu-id="0a5cc-119"><span id="BG_E_INVALID_STATE__0x80200002_"></span><span id="bg_e_invalid_state__0x80200002_"></span><span id="BG_E_INVALID_STATE__0X80200002_"></span>\_Estado BG E \_ inválido \_ (0x80200002)</span><span class="sxs-lookup"><span data-stu-id="0a5cc-119"><span id="BG_E_INVALID_STATE__0x80200002_"></span><span id="bg_e_invalid_state__0x80200002_"></span><span id="BG_E_INVALID_STATE__0X80200002_"></span>BG\_E\_INVALID\_STATE (0x80200002)</span></span>
</dt> <dd>

<span data-ttu-id="0a5cc-120">A ação solicitada não é permitida no estado do trabalho atual.</span><span class="sxs-lookup"><span data-stu-id="0a5cc-120">The requested action is not allowed in the current job state.</span></span>

</dd> <dt>

<span data-ttu-id="0a5cc-121"><span id="BG_E_EMPTY__0x80200003_"></span><span id="bg_e_empty__0x80200003_"></span><span id="BG_E_EMPTY__0X80200003_"></span>BG \_ E \_ Empty (0x80200003)</span><span class="sxs-lookup"><span data-stu-id="0a5cc-121"><span id="BG_E_EMPTY__0x80200003_"></span><span id="bg_e_empty__0x80200003_"></span><span id="BG_E_EMPTY__0X80200003_"></span>BG\_E\_EMPTY (0x80200003)</span></span>
</dt> <dd>

<span data-ttu-id="0a5cc-122">O trabalho deve conter um ou mais arquivos para que você possa retomar o trabalho.</span><span class="sxs-lookup"><span data-stu-id="0a5cc-122">The job must contain one or more files before you can resume the job.</span></span>

</dd> <dt>

<span data-ttu-id="0a5cc-123"><span id="BG_E_FILE_NOT_AVAILABLE__0x80200004_"></span><span id="bg_e_file_not_available__0x80200004_"></span><span id="BG_E_FILE_NOT_AVAILABLE__0X80200004_"></span>\_Arquivo BG \_ E \_ não \_ disponível (0x80200004)</span><span class="sxs-lookup"><span data-stu-id="0a5cc-123"><span id="BG_E_FILE_NOT_AVAILABLE__0x80200004_"></span><span id="bg_e_file_not_available__0x80200004_"></span><span id="BG_E_FILE_NOT_AVAILABLE__0X80200004_"></span>BG\_E\_FILE\_NOT\_AVAILABLE (0x80200004)</span></span>
</dt> <dd>

<span data-ttu-id="0a5cc-124">As informações do arquivo não estão disponíveis porque o erro não está associado a um arquivo local ou remoto.</span><span class="sxs-lookup"><span data-stu-id="0a5cc-124">File information is not available because the error is not associated with a local or remote file.</span></span>

</dd> <dt>

<span data-ttu-id="0a5cc-125"><span id="BG_E_PROTOCOL_NOT_AVAILABLE__0x80200005_"></span><span id="bg_e_protocol_not_available__0x80200005_"></span><span id="BG_E_PROTOCOL_NOT_AVAILABLE__0X80200005_"></span>\_Protocolo BG \_ E \_ não \_ disponível (0x80200005)</span><span class="sxs-lookup"><span data-stu-id="0a5cc-125"><span id="BG_E_PROTOCOL_NOT_AVAILABLE__0x80200005_"></span><span id="bg_e_protocol_not_available__0x80200005_"></span><span id="BG_E_PROTOCOL_NOT_AVAILABLE__0X80200005_"></span>BG\_E\_PROTOCOL\_NOT\_AVAILABLE (0x80200005)</span></span>
</dt> <dd>

<span data-ttu-id="0a5cc-126">As informações de protocolo não estão disponíveis porque o erro não está associado ao protocolo de transferência especificado.</span><span class="sxs-lookup"><span data-stu-id="0a5cc-126">Protocol information is not available because the error is not associated with the specified transfer protocol.</span></span>

</dd> <dt>

<span data-ttu-id="0a5cc-127"><span id="BG_E_DESTINATION_LOCKED__0x8020000D_"></span><span id="bg_e_destination_locked__0x8020000d_"></span><span id="BG_E_DESTINATION_LOCKED__0X8020000D_"></span>BG \_ E \_ destino \_ bloqueado (0x8020000D)</span><span class="sxs-lookup"><span data-stu-id="0a5cc-127"><span id="BG_E_DESTINATION_LOCKED__0x8020000D_"></span><span id="bg_e_destination_locked__0x8020000d_"></span><span id="BG_E_DESTINATION_LOCKED__0X8020000D_"></span>BG\_E\_DESTINATION\_LOCKED (0x8020000D)</span></span>
</dt> <dd>

<span data-ttu-id="0a5cc-128">O volume do sistema de arquivos de destino, especificado no nome do arquivo local, está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="0a5cc-128">The destination file system volume, specified in the local file name, is locked.</span></span>

</dd> <dt>

<span data-ttu-id="0a5cc-129"><span id="BG_E_VOLUME_CHANGED__0x8020000E_"></span><span id="bg_e_volume_changed__0x8020000e_"></span><span id="BG_E_VOLUME_CHANGED__0X8020000E_"></span>BG \_ E \_ volume \_ alterado (0x8020000E)</span><span class="sxs-lookup"><span data-stu-id="0a5cc-129"><span id="BG_E_VOLUME_CHANGED__0x8020000E_"></span><span id="bg_e_volume_changed__0x8020000e_"></span><span id="BG_E_VOLUME_CHANGED__0X8020000E_"></span>BG\_E\_VOLUME\_CHANGED (0x8020000E)</span></span>
</dt> <dd>

<span data-ttu-id="0a5cc-130">O volume de destino, especificado no nome do arquivo local, foi alterado.</span><span class="sxs-lookup"><span data-stu-id="0a5cc-130">The destination volume, specified in the local file name, has changed.</span></span> <span data-ttu-id="0a5cc-131">Por exemplo, o disquete original foi substituído por um disquete diferente.</span><span class="sxs-lookup"><span data-stu-id="0a5cc-131">For example, the original floppy disk has been replaced with a different floppy disk.</span></span>

</dd> <dt>

<span data-ttu-id="0a5cc-132"><span id="BG_E_ERROR_INFORMATION_UNAVAILABLE__0x8020000F_"></span><span id="bg_e_error_information_unavailable__0x8020000f_"></span><span id="BG_E_ERROR_INFORMATION_UNAVAILABLE__0X8020000F_"></span>\_ \_ Informações de erro BG E \_ \_ indisponíveis (0x8020000F)</span><span class="sxs-lookup"><span data-stu-id="0a5cc-132"><span id="BG_E_ERROR_INFORMATION_UNAVAILABLE__0x8020000F_"></span><span id="bg_e_error_information_unavailable__0x8020000f_"></span><span id="BG_E_ERROR_INFORMATION_UNAVAILABLE__0X8020000F_"></span>BG\_E\_ERROR\_INFORMATION\_UNAVAILABLE (0x8020000F)</span></span>
</dt> <dd>

<span data-ttu-id="0a5cc-133">As informações de erro só estão disponíveis quando o estado do trabalho é um \_ erro de estado de trabalho BG \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="0a5cc-133">Error information is only available when the state of the job is BG\_JOB\_STATE\_ERROR.</span></span> <span data-ttu-id="0a5cc-134">As informações de erro não estão disponíveis depois que o BITS começa a transferir os dados do trabalho ou o cliente é encerrado.</span><span class="sxs-lookup"><span data-stu-id="0a5cc-134">The error information is not available after BITS begins transferring the job's data or the client exits.</span></span>

</dd> <dt>

<span data-ttu-id="0a5cc-135"><span id="BG_E_NETWORK_DISCONNECTED__0x80200010_"></span><span id="bg_e_network_disconnected__0x80200010_"></span><span id="BG_E_NETWORK_DISCONNECTED__0X80200010_"></span>BG \_ E \_ rede \_ desconectada (0x80200010)</span><span class="sxs-lookup"><span data-stu-id="0a5cc-135"><span id="BG_E_NETWORK_DISCONNECTED__0x80200010_"></span><span id="bg_e_network_disconnected__0x80200010_"></span><span id="BG_E_NETWORK_DISCONNECTED__0X80200010_"></span>BG\_E\_NETWORK\_DISCONNECTED (0x80200010)</span></span>
</dt> <dd>

<span data-ttu-id="0a5cc-136">O adaptador de rede está inativo ou desconectado.</span><span class="sxs-lookup"><span data-stu-id="0a5cc-136">The network adapter is inactive or disconnected.</span></span> <span data-ttu-id="0a5cc-137">Todos os trabalhos são colocados no \_ estado de \_ erro temporário de estado do trabalho BG \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="0a5cc-137">All jobs are placed in the BG\_JOB\_STATE\_TRANSIENT\_ERROR state.</span></span>

</dd> <dt>

<span data-ttu-id="0a5cc-138"><span id="BG_E_MISSING_FILE_SIZE__0x80200011_"></span><span id="bg_e_missing_file_size__0x80200011_"></span><span id="BG_E_MISSING_FILE_SIZE__0X80200011_"></span>BG \_ E \_ \_ \_ tamanho de arquivo ausente (0x80200011)</span><span class="sxs-lookup"><span data-stu-id="0a5cc-138"><span id="BG_E_MISSING_FILE_SIZE__0x80200011_"></span><span id="bg_e_missing_file_size__0x80200011_"></span><span id="BG_E_MISSING_FILE_SIZE__0X80200011_"></span>BG\_E\_MISSING\_FILE\_SIZE (0x80200011)</span></span>
</dt> <dd>

<span data-ttu-id="0a5cc-139">O servidor não retornou o tamanho do arquivo.</span><span class="sxs-lookup"><span data-stu-id="0a5cc-139">The server did not return the file size.</span></span> <span data-ttu-id="0a5cc-140">O BITS só transfere conteúdo estático e requer que o servidor HTTP retorne o cabeçalho Content-Length.</span><span class="sxs-lookup"><span data-stu-id="0a5cc-140">BITS only transfers static content and requires the HTTP server to return the Content-Length header.</span></span> <span data-ttu-id="0a5cc-141">A solicitação de transferência falhará se a URL apontar para o conteúdo dinâmico.</span><span class="sxs-lookup"><span data-stu-id="0a5cc-141">The transfer request fails if the URL points to dynamic content.</span></span>

</dd> <dt>

<span data-ttu-id="0a5cc-142"><span id="BG_E_INSUFFICIENT_HTTP_SUPPORT__0x80200012_"></span><span id="bg_e_insufficient_http_support__0x80200012_"></span><span id="BG_E_INSUFFICIENT_HTTP_SUPPORT__0X80200012_"></span>Suporte a BG \_ E \_ http insuficiente \_ \_ (0x80200012)</span><span class="sxs-lookup"><span data-stu-id="0a5cc-142"><span id="BG_E_INSUFFICIENT_HTTP_SUPPORT__0x80200012_"></span><span id="bg_e_insufficient_http_support__0x80200012_"></span><span id="BG_E_INSUFFICIENT_HTTP_SUPPORT__0X80200012_"></span>BG\_E\_INSUFFICIENT\_HTTP\_SUPPORT (0x80200012)</span></span>
</dt> <dd>

<span data-ttu-id="0a5cc-143">O servidor não oferece suporte ao protocolo HTTP/1.1.</span><span class="sxs-lookup"><span data-stu-id="0a5cc-143">The server does not support the HTTP/1.1 protocol.</span></span>

</dd> <dt>

<span data-ttu-id="0a5cc-144"><span id="BG_E_INSUFFICIENT_RANGE_SUPPORT__0x80200013_"></span><span id="bg_e_insufficient_range_support__0x80200013_"></span><span id="BG_E_INSUFFICIENT_RANGE_SUPPORT__0X80200013_"></span>\_Suporte a intervalo BG E \_ insuficiente \_ \_ (0x80200013)</span><span class="sxs-lookup"><span data-stu-id="0a5cc-144"><span id="BG_E_INSUFFICIENT_RANGE_SUPPORT__0x80200013_"></span><span id="bg_e_insufficient_range_support__0x80200013_"></span><span id="BG_E_INSUFFICIENT_RANGE_SUPPORT__0X80200013_"></span>BG\_E\_INSUFFICIENT\_RANGE\_SUPPORT (0x80200013)</span></span>
</dt> <dd>

<span data-ttu-id="0a5cc-145">O servidor não oferece suporte ao cabeçalho Content-Range.</span><span class="sxs-lookup"><span data-stu-id="0a5cc-145">The server does not support the Content-Range header.</span></span> <span data-ttu-id="0a5cc-146">Normalmente, você recebe esse erro quando tenta baixar conteúdo dinâmico.</span><span class="sxs-lookup"><span data-stu-id="0a5cc-146">Typically, you receive this error when you try to download dynamic content.</span></span> <span data-ttu-id="0a5cc-147">Você também poderá receber esse erro se um proxy intermediário estiver removendo o cabeçalho Content-Range ou Content-Length.</span><span class="sxs-lookup"><span data-stu-id="0a5cc-147">You can also receive this error if an intermediate proxy is removing the Content-Range or Content-Length header.</span></span>

</dd> <dt>

<span data-ttu-id="0a5cc-148"><span id="BG_E_REMOTE_NOT_SUPPORTED__0x80200014_"></span><span id="bg_e_remote_not_supported__0x80200014_"></span><span id="BG_E_REMOTE_NOT_SUPPORTED__0X80200014_"></span>\_ \_ \_ Não \_ há suporte para BG E remoto (0x80200014)</span><span class="sxs-lookup"><span data-stu-id="0a5cc-148"><span id="BG_E_REMOTE_NOT_SUPPORTED__0x80200014_"></span><span id="bg_e_remote_not_supported__0x80200014_"></span><span id="BG_E_REMOTE_NOT_SUPPORTED__0X80200014_"></span>BG\_E\_REMOTE\_NOT\_SUPPORTED (0x80200014)</span></span>
</dt> <dd>

<span data-ttu-id="0a5cc-149">Não há suporte para o uso remoto de BITS.</span><span class="sxs-lookup"><span data-stu-id="0a5cc-149">Remote use of BITS is not supported.</span></span> <span data-ttu-id="0a5cc-150">Para obter mais informações, consulte [usuários e conexões de rede](users-and-network-connections.md).</span><span class="sxs-lookup"><span data-stu-id="0a5cc-150">For more information, see [Users and Network Connections](users-and-network-connections.md).</span></span>

</dd> <dt>

<span data-ttu-id="0a5cc-151"><span id="BG_E_NEW_OWNER_DIFF_MAPPING__0x80200015_"></span><span id="bg_e_new_owner_diff_mapping__0x80200015_"></span><span id="BG_E_NEW_OWNER_DIFF_MAPPING__0X80200015_"></span>BG \_ E \_ novo \_ \_ mapeamento diff \_ do proprietário (0x80200015)</span><span class="sxs-lookup"><span data-stu-id="0a5cc-151"><span id="BG_E_NEW_OWNER_DIFF_MAPPING__0x80200015_"></span><span id="bg_e_new_owner_diff_mapping__0x80200015_"></span><span id="BG_E_NEW_OWNER_DIFF_MAPPING__0X80200015_"></span>BG\_E\_NEW\_OWNER\_DIFF\_MAPPING (0x80200015)</span></span>
</dt> <dd>

<span data-ttu-id="0a5cc-152">O mapeamento de unidade de rede para o arquivo local é diferente para o proprietário atual do que para o proprietário anterior.</span><span class="sxs-lookup"><span data-stu-id="0a5cc-152">The network drive mapping for the local file is different for the current owner than for the previous owner.</span></span>

</dd> <dt>

<span data-ttu-id="0a5cc-153"><span id="BG_E_NEW_OWNER_NO_FILE_ACCESS__0x80200016_"></span><span id="bg_e_new_owner_no_file_access__0x80200016_"></span><span id="BG_E_NEW_OWNER_NO_FILE_ACCESS__0X80200016_"></span>BG \_ E \_ novo \_ proprietário \_ sem \_ \_ acesso de arquivo (0x80200016)</span><span class="sxs-lookup"><span data-stu-id="0a5cc-153"><span id="BG_E_NEW_OWNER_NO_FILE_ACCESS__0x80200016_"></span><span id="bg_e_new_owner_no_file_access__0x80200016_"></span><span id="BG_E_NEW_OWNER_NO_FILE_ACCESS__0X80200016_"></span>BG\_E\_NEW\_OWNER\_NO\_FILE\_ACCESS (0x80200016)</span></span>
</dt> <dd>

<span data-ttu-id="0a5cc-154">O novo proprietário tem permissões insuficientes para os arquivos de trabalho temporários.</span><span class="sxs-lookup"><span data-stu-id="0a5cc-154">The new owner has insufficient permissions to the temporary job files.</span></span>

</dd> <dt>

<span data-ttu-id="0a5cc-155"><span id="BG_E_PROXY_LIST_TOO_LARGE__0x80200018_"></span><span id="bg_e_proxy_list_too_large__0x80200018_"></span><span id="BG_E_PROXY_LIST_TOO_LARGE__0X80200018_"></span>\_ \_ Lista de proxy BG E \_ \_ muito \_ grande (0x80200018)</span><span class="sxs-lookup"><span data-stu-id="0a5cc-155"><span id="BG_E_PROXY_LIST_TOO_LARGE__0x80200018_"></span><span id="bg_e_proxy_list_too_large__0x80200018_"></span><span id="BG_E_PROXY_LIST_TOO_LARGE__0X80200018_"></span>BG\_E\_PROXY\_LIST\_TOO\_LARGE (0x80200018)</span></span>
</dt> <dd>

<span data-ttu-id="0a5cc-156">A lista de proxy HTTP é muito longa.</span><span class="sxs-lookup"><span data-stu-id="0a5cc-156">The HTTP proxy list is too long.</span></span> <span data-ttu-id="0a5cc-157">A lista não deve exceder 32 KB.</span><span class="sxs-lookup"><span data-stu-id="0a5cc-157">The list must not exceed 32 KB.</span></span>

</dd> <dt>

<span data-ttu-id="0a5cc-158"><span id="BG_E_PROXY_BYPASS_LIST_TOO_LARGE__0x80200019_"></span><span id="bg_e_proxy_bypass_list_too_large__0x80200019_"></span><span id="BG_E_PROXY_BYPASS_LIST_TOO_LARGE__0X80200019_"></span>\_ \_ \_ Lista de bypass E proxy BG \_ \_ muito \_ grande (0x80200019)</span><span class="sxs-lookup"><span data-stu-id="0a5cc-158"><span id="BG_E_PROXY_BYPASS_LIST_TOO_LARGE__0x80200019_"></span><span id="bg_e_proxy_bypass_list_too_large__0x80200019_"></span><span id="BG_E_PROXY_BYPASS_LIST_TOO_LARGE__0X80200019_"></span>BG\_E\_PROXY\_BYPASS\_LIST\_TOO\_LARGE (0x80200019)</span></span>
</dt> <dd>

<span data-ttu-id="0a5cc-159">A lista de bypass de proxy HTTP é muito longa.</span><span class="sxs-lookup"><span data-stu-id="0a5cc-159">The HTTP proxy bypass list is too long.</span></span> <span data-ttu-id="0a5cc-160">A lista não deve exceder 32 KB.</span><span class="sxs-lookup"><span data-stu-id="0a5cc-160">The list must not exceed 32 KB.</span></span>

</dd> <dt>

<span data-ttu-id="0a5cc-161"><span id="BG_E_TOO_MANY_FILES__0x8020001C_"></span><span id="bg_e_too_many_files__0x8020001c_"></span><span id="BG_E_TOO_MANY_FILES__0X8020001C_"></span>BG \_ E \_ \_ muitos \_ arquivos (0x8020001C)</span><span class="sxs-lookup"><span data-stu-id="0a5cc-161"><span id="BG_E_TOO_MANY_FILES__0x8020001C_"></span><span id="bg_e_too_many_files__0x8020001c_"></span><span id="BG_E_TOO_MANY_FILES__0X8020001C_"></span>BG\_E\_TOO\_MANY\_FILES (0x8020001C)</span></span>
</dt> <dd>

<span data-ttu-id="0a5cc-162">Você não pode adicionar mais de um arquivo a um trabalho de carregamento.</span><span class="sxs-lookup"><span data-stu-id="0a5cc-162">You cannot add more than one file to an upload job.</span></span>

</dd> <dt>

<span data-ttu-id="0a5cc-163"><span id="BG_E_LOCAL_FILE_CHANGED__0x8020001D_"></span><span id="bg_e_local_file_changed__0x8020001d_"></span><span id="BG_E_LOCAL_FILE_CHANGED__0X8020001D_"></span>BG \_ E \_ \_ arquivo local \_ alterado (0x8020001D)</span><span class="sxs-lookup"><span data-stu-id="0a5cc-163"><span id="BG_E_LOCAL_FILE_CHANGED__0x8020001D_"></span><span id="bg_e_local_file_changed__0x8020001d_"></span><span id="BG_E_LOCAL_FILE_CHANGED__0X8020001D_"></span>BG\_E\_LOCAL\_FILE\_CHANGED (0x8020001D)</span></span>
</dt> <dd>

<span data-ttu-id="0a5cc-164">O conteúdo do arquivo local foi alterado após o início do processo de transferência.</span><span class="sxs-lookup"><span data-stu-id="0a5cc-164">The contents of the local file changed after the transfer process began.</span></span> <span data-ttu-id="0a5cc-165">O conteúdo do arquivo local não pode ser alterado depois que o processo de transferência é iniciado em um trabalho de upload ou de resposta de upload.</span><span class="sxs-lookup"><span data-stu-id="0a5cc-165">The contents of the local file cannot change after the transfer process begins on an upload or upload-reply job.</span></span>

</dd> <dt>

<span data-ttu-id="0a5cc-166"><span id="BG_E_TOO_LARGE__0x80200020_"></span><span id="bg_e_too_large__0x80200020_"></span><span id="BG_E_TOO_LARGE__0X80200020_"></span>BG \_ E \_ muito \_ grande (0x80200020)</span><span class="sxs-lookup"><span data-stu-id="0a5cc-166"><span id="BG_E_TOO_LARGE__0x80200020_"></span><span id="bg_e_too_large__0x80200020_"></span><span id="BG_E_TOO_LARGE__0X80200020_"></span>BG\_E\_TOO\_LARGE (0x80200020)</span></span>
</dt> <dd>

<span data-ttu-id="0a5cc-167">O tamanho do arquivo de carregamento excede o tamanho máximo de upload permitido especificado no servidor.</span><span class="sxs-lookup"><span data-stu-id="0a5cc-167">The size of the upload file exceeds the maximum allowed upload size specified on the server.</span></span>

</dd> <dt>

<span data-ttu-id="0a5cc-168"><span id="BG_E_STRING_TOO_LONG__0x80200021_"></span><span id="bg_e_string_too_long__0x80200021_"></span><span id="BG_E_STRING_TOO_LONG__0X80200021_"></span>\_ \_ Cadeia de caracteres BG E \_ muito \_ longa (0x80200021)</span><span class="sxs-lookup"><span data-stu-id="0a5cc-168"><span id="BG_E_STRING_TOO_LONG__0x80200021_"></span><span id="bg_e_string_too_long__0x80200021_"></span><span id="BG_E_STRING_TOO_LONG__0X80200021_"></span>BG\_E\_STRING\_TOO\_LONG (0x80200021)</span></span>
</dt> <dd>

<span data-ttu-id="0a5cc-169">A cadeia de caracteres especificada é muito longa.</span><span class="sxs-lookup"><span data-stu-id="0a5cc-169">The specified string is too long.</span></span>

</dd> <dt>

<span data-ttu-id="0a5cc-170"><span id="BG_E_CLIENT_SERVER_PROTOCOL_MISMATCH__0x80200022_"></span><span id="bg_e_client_server_protocol_mismatch__0x80200022_"></span><span id="BG_E_CLIENT_SERVER_PROTOCOL_MISMATCH__0X80200022_"></span>\_Incompatibilidade \_ de protocolo BG E cliente \_ do servidor \_ \_ (0x80200022)</span><span class="sxs-lookup"><span data-stu-id="0a5cc-170"><span id="BG_E_CLIENT_SERVER_PROTOCOL_MISMATCH__0x80200022_"></span><span id="bg_e_client_server_protocol_mismatch__0x80200022_"></span><span id="BG_E_CLIENT_SERVER_PROTOCOL_MISMATCH__0X80200022_"></span>BG\_E\_CLIENT\_SERVER\_PROTOCOL\_MISMATCH (0x80200022)</span></span>
</dt> <dd>

<span data-ttu-id="0a5cc-171">O cliente e o servidor não conseguiram negociar um protocolo a ser usado para o trabalho de carregamento.</span><span class="sxs-lookup"><span data-stu-id="0a5cc-171">The client and server were unable to negotiate a protocol to use for the upload job.</span></span>

</dd> <dt>

<span data-ttu-id="0a5cc-172"><span id="BG_E_SERVER_EXECUTE_ENABLED__0x80200023_"></span><span id="bg_e_server_execute_enabled__0x80200023_"></span><span id="BG_E_SERVER_EXECUTE_ENABLED__0X80200023_"></span>BG \_ E \_ Server \_ Execute \_ habilitados (0x80200023)</span><span class="sxs-lookup"><span data-stu-id="0a5cc-172"><span id="BG_E_SERVER_EXECUTE_ENABLED__0x80200023_"></span><span id="bg_e_server_execute_enabled__0x80200023_"></span><span id="BG_E_SERVER_EXECUTE_ENABLED__0X80200023_"></span>BG\_E\_SERVER\_EXECUTE\_ENABLED (0x80200023)</span></span>
</dt> <dd>

<span data-ttu-id="0a5cc-173">As permissões de script ou execução são habilitadas no diretório virtual do IIS associado ao trabalho.</span><span class="sxs-lookup"><span data-stu-id="0a5cc-173">Scripting or execute permissions are enabled on the IIS virtual directory associated with the job.</span></span> <span data-ttu-id="0a5cc-174">Para carregar arquivos no diretório virtual, desabilite as permissões de script e execução no diretório virtual.</span><span class="sxs-lookup"><span data-stu-id="0a5cc-174">To upload files to the virtual directory, disable the scripting and execute permissions on the virtual directory.</span></span>

</dd> <dt>

<span data-ttu-id="0a5cc-175"><span id="BG_E_USERNAME_TOO_LARGE__0x80200025_"></span><span id="bg_e_username_too_large__0x80200025_"></span><span id="BG_E_USERNAME_TOO_LARGE__0X80200025_"></span>BG \_ E \_ nome \_ de usuário muito \_ grande (0x80200025)</span><span class="sxs-lookup"><span data-stu-id="0a5cc-175"><span id="BG_E_USERNAME_TOO_LARGE__0x80200025_"></span><span id="bg_e_username_too_large__0x80200025_"></span><span id="BG_E_USERNAME_TOO_LARGE__0X80200025_"></span>BG\_E\_USERNAME\_TOO\_LARGE (0x80200025)</span></span>
</dt> <dd>

<span data-ttu-id="0a5cc-176">O nome de usuário não pode exceder 300 caracteres.</span><span class="sxs-lookup"><span data-stu-id="0a5cc-176">The user name cannot exceed 300 characters.</span></span>

</dd> <dt>

<span data-ttu-id="0a5cc-177"><span id="BG_E_PASSWORD_TOO_LARGE__0x80200026_"></span><span id="bg_e_password_too_large__0x80200026_"></span><span id="BG_E_PASSWORD_TOO_LARGE__0X80200026_"></span>BG \_ E \_ senha \_ muito \_ grande (0x80200026)</span><span class="sxs-lookup"><span data-stu-id="0a5cc-177"><span id="BG_E_PASSWORD_TOO_LARGE__0x80200026_"></span><span id="bg_e_password_too_large__0x80200026_"></span><span id="BG_E_PASSWORD_TOO_LARGE__0X80200026_"></span>BG\_E\_PASSWORD\_TOO\_LARGE (0x80200026)</span></span>
</dt> <dd>

<span data-ttu-id="0a5cc-178">A senha não pode exceder 65535 caracteres.</span><span class="sxs-lookup"><span data-stu-id="0a5cc-178">The password cannot exceed 65535 characters.</span></span>

</dd> <dt>

<span data-ttu-id="0a5cc-179"><span id="BG_E_INVALID_AUTH_TARGET__0x80200027_"></span><span id="bg_e_invalid_auth_target__0x80200027_"></span><span id="BG_E_INVALID_AUTH_TARGET__0X80200027_"></span>BG \_ E \_ \_ \_ destino de autenticação inválido (0x80200027)</span><span class="sxs-lookup"><span data-stu-id="0a5cc-179"><span id="BG_E_INVALID_AUTH_TARGET__0x80200027_"></span><span id="bg_e_invalid_auth_target__0x80200027_"></span><span id="BG_E_INVALID_AUTH_TARGET__0X80200027_"></span>BG\_E\_INVALID\_AUTH\_TARGET (0x80200027)</span></span>
</dt> <dd>

<span data-ttu-id="0a5cc-180">O destino de autenticação especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="0a5cc-180">The specified authentication target is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="0a5cc-181"><span id="BG_E_INVALID_AUTH_SCHEME__0x80200028_"></span><span id="bg_e_invalid_auth_scheme__0x80200028_"></span><span id="BG_E_INVALID_AUTH_SCHEME__0X80200028_"></span>BG \_ E \_ \_ \_ esquema de autenticação inválido (0x80200028)</span><span class="sxs-lookup"><span data-stu-id="0a5cc-181"><span id="BG_E_INVALID_AUTH_SCHEME__0x80200028_"></span><span id="bg_e_invalid_auth_scheme__0x80200028_"></span><span id="BG_E_INVALID_AUTH_SCHEME__0X80200028_"></span>BG\_E\_INVALID\_AUTH\_SCHEME (0x80200028)</span></span>
</dt> <dd>

<span data-ttu-id="0a5cc-182">O esquema de autenticação especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="0a5cc-182">The specified authentication scheme is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="0a5cc-183"><span id="BG_E_INVALID_RANGE__0x8020002B_"></span><span id="bg_e_invalid_range__0x8020002b_"></span><span id="BG_E_INVALID_RANGE__0X8020002B_"></span>\_Intervalo BG E \_ inválido \_ (0x8020002B)</span><span class="sxs-lookup"><span data-stu-id="0a5cc-183"><span id="BG_E_INVALID_RANGE__0x8020002B_"></span><span id="bg_e_invalid_range__0x8020002b_"></span><span id="BG_E_INVALID_RANGE__0X8020002B_"></span>BG\_E\_INVALID\_RANGE (0x8020002B)</span></span>
</dt> <dd>

<span data-ttu-id="0a5cc-184">O intervalo de bytes especificado é inválido.</span><span class="sxs-lookup"><span data-stu-id="0a5cc-184">The specified byte range is invalid.</span></span> <span data-ttu-id="0a5cc-185">O intervalo de bytes deve existir dentro do arquivo remoto especificado.</span><span class="sxs-lookup"><span data-stu-id="0a5cc-185">The byte range must exist within the specified remote file.</span></span>

</dd> <dt>

<span data-ttu-id="0a5cc-186"><span id="BG_E_OVERLAPPING_RANGES__0x8020002C_"></span><span id="bg_e_overlapping_ranges__0x8020002c_"></span><span id="BG_E_OVERLAPPING_RANGES__0X8020002C_"></span>\_ \_ \_ 0x8020002C (intervalos de sobreposição BG)</span><span class="sxs-lookup"><span data-stu-id="0a5cc-186"><span id="BG_E_OVERLAPPING_RANGES__0x8020002C_"></span><span id="bg_e_overlapping_ranges__0x8020002c_"></span><span id="BG_E_OVERLAPPING_RANGES__0X8020002C_"></span>BG\_E\_OVERLAPPING\_RANGES (0x8020002C)</span></span>
</dt> <dd>

<span data-ttu-id="0a5cc-187">A lista de intervalos de bytes contém intervalos sobrepostos ou duplicados, que não têm suporte.</span><span class="sxs-lookup"><span data-stu-id="0a5cc-187">The list of byte ranges contains overlapping or duplicate ranges, which are not supported.</span></span>

</dd> <dt>

<span data-ttu-id="0a5cc-188"><span id="BG_E_BLOCKED_BY_POLICY__0x8020003E_"></span><span id="bg_e_blocked_by_policy__0x8020003e_"></span><span id="BG_E_BLOCKED_BY_POLICY__0X8020003E_"></span>BG \_ E \_ bloqueado \_ pela \_ política (0x8020003E)</span><span class="sxs-lookup"><span data-stu-id="0a5cc-188"><span id="BG_E_BLOCKED_BY_POLICY__0x8020003E_"></span><span id="bg_e_blocked_by_policy__0x8020003e_"></span><span id="BG_E_BLOCKED_BY_POLICY__0X8020003E_"></span>BG\_E\_BLOCKED\_BY\_POLICY (0x8020003E)</span></span>
</dt> <dd>

<span data-ttu-id="0a5cc-189">Política de Grupo configurações impedem que trabalhos em segundo plano sejam executados no momento.</span><span class="sxs-lookup"><span data-stu-id="0a5cc-189">Group Policy settings prevent background jobs from running at this time.</span></span> <span data-ttu-id="0a5cc-190">Para obter detalhes, consulte a política [MaxInternetBandwidth](group-policies.md) .</span><span class="sxs-lookup"><span data-stu-id="0a5cc-190">For details, see the [MaxInternetBandwidth](group-policies.md) policy.</span></span>

</dd> <dt>

<span data-ttu-id="0a5cc-191"><span id="BG_E_INVALID_PROXY_INFO__0x8020003F_"></span><span id="bg_e_invalid_proxy_info__0x8020003f_"></span><span id="BG_E_INVALID_PROXY_INFO__0X8020003F_"></span>\_ \_ Informações de proxy inválidas BG E \_ \_ (0x8020003F)</span><span class="sxs-lookup"><span data-stu-id="0a5cc-191"><span id="BG_E_INVALID_PROXY_INFO__0x8020003F_"></span><span id="bg_e_invalid_proxy_info__0x8020003f_"></span><span id="BG_E_INVALID_PROXY_INFO__0X8020003F_"></span>BG\_E\_INVALID\_PROXY\_INFO (0x8020003F)</span></span>
</dt> <dd>

<span data-ttu-id="0a5cc-192">Erro de tempo de execução que indica que a lista de proxy ou a lista de bypass de proxy que você especificou usando o método [**método ibackgroundcopyjob:: SetProxySettings**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) é inválida.</span><span class="sxs-lookup"><span data-stu-id="0a5cc-192">Run-time error that indicates the proxy list or proxy bypass list that you specified using the [**IBackgroundCopyJob::SetProxySettings**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) method is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="0a5cc-193"><span id="BG_E_INVALID_CREDENTIALS__0x80200040_"></span><span id="bg_e_invalid_credentials__0x80200040_"></span><span id="BG_E_INVALID_CREDENTIALS__0X80200040_"></span>\_ \_ Credenciais de BG E inválidas \_ (0x80200040)</span><span class="sxs-lookup"><span data-stu-id="0a5cc-193"><span id="BG_E_INVALID_CREDENTIALS__0x80200040_"></span><span id="bg_e_invalid_credentials__0x80200040_"></span><span id="BG_E_INVALID_CREDENTIALS__0X80200040_"></span>BG\_E\_INVALID\_CREDENTIALS (0x80200040)</span></span>
</dt> <dd>

<span data-ttu-id="0a5cc-194">O formato das credenciais de segurança fornecidas não é válido.</span><span class="sxs-lookup"><span data-stu-id="0a5cc-194">The format of the supplied security credentials is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="0a5cc-195"><span id="BG_E_RECORD_DELETED__0x80200042_"></span><span id="bg_e_record_deleted__0x80200042_"></span><span id="BG_E_RECORD_DELETED__0X80200042_"></span>BG \_ E \_ registro \_ excluído (0x80200042)</span><span class="sxs-lookup"><span data-stu-id="0a5cc-195"><span id="BG_E_RECORD_DELETED__0x80200042_"></span><span id="bg_e_record_deleted__0x80200042_"></span><span id="BG_E_RECORD_DELETED__0X80200042_"></span>BG\_E\_RECORD\_DELETED (0x80200042)</span></span>
</dt> <dd>

<span data-ttu-id="0a5cc-196">O registro de cache foi excluído.</span><span class="sxs-lookup"><span data-stu-id="0a5cc-196">The cache record has been deleted.</span></span> <span data-ttu-id="0a5cc-197">A tentativa de atualizá-la foi abandonada.</span><span class="sxs-lookup"><span data-stu-id="0a5cc-197">The attempt to update it has been abandoned.</span></span>

</dd> <dt>

<span data-ttu-id="0a5cc-198"><span id="BG_E_UPNP_ERROR__0x80200045_"></span><span id="bg_e_upnp_error__0x80200045_"></span><span id="BG_E_UPNP_ERROR__0X80200045_"></span>\_Erro BG E \_ UPnP \_ (0x80200045)</span><span class="sxs-lookup"><span data-stu-id="0a5cc-198"><span id="BG_E_UPNP_ERROR__0x80200045_"></span><span id="bg_e_upnp_error__0x80200045_"></span><span id="BG_E_UPNP_ERROR__0X80200045_"></span>BG\_E\_UPNP\_ERROR (0x80200045)</span></span>
</dt> <dd>

<span data-ttu-id="0a5cc-199">Ocorreu um erro Universal Plug and Play (UPnP).</span><span class="sxs-lookup"><span data-stu-id="0a5cc-199">A Universal Plug and Play (UPnP) error has occurred.</span></span> <span data-ttu-id="0a5cc-200">Verifique seu dispositivo de gateway de Internet.</span><span class="sxs-lookup"><span data-stu-id="0a5cc-200">Please check your Internet Gateway Device.</span></span>

</dd> <dt>

<span data-ttu-id="0a5cc-201"><span id="BG_E_PEERCACHING_DISABLED__0x80200047_"></span><span id="bg_e_peercaching_disabled__0x80200047_"></span><span id="BG_E_PEERCACHING_DISABLED__0X80200047_"></span>BG \_ E em \_ cache \_ desabilitado (0x80200047)</span><span class="sxs-lookup"><span data-stu-id="0a5cc-201"><span id="BG_E_PEERCACHING_DISABLED__0x80200047_"></span><span id="bg_e_peercaching_disabled__0x80200047_"></span><span id="BG_E_PEERCACHING_DISABLED__0X80200047_"></span>BG\_E\_PEERCACHING\_DISABLED (0x80200047)</span></span>
</dt> <dd>

<span data-ttu-id="0a5cc-202">O cache de pares está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="0a5cc-202">Peer-caching is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="0a5cc-203"><span id="BG_E_BUSYCACHERECORD__0x80200048_"></span><span id="bg_e_busycacherecord__0x80200048_"></span><span id="BG_E_BUSYCACHERECORD__0X80200048_"></span>BG \_ E \_ BUSYCACHERECORD (0x80200048)</span><span class="sxs-lookup"><span data-stu-id="0a5cc-203"><span id="BG_E_BUSYCACHERECORD__0x80200048_"></span><span id="bg_e_busycacherecord__0x80200048_"></span><span id="BG_E_BUSYCACHERECORD__0X80200048_"></span>BG\_E\_BUSYCACHERECORD (0x80200048)</span></span>
</dt> <dd>

<span data-ttu-id="0a5cc-204">O registro de cache está em uso e não pode ser alterado ou excluído.</span><span class="sxs-lookup"><span data-stu-id="0a5cc-204">The cache record is in use and cannot be changed or deleted.</span></span> <span data-ttu-id="0a5cc-205">Tente novamente após alguns segundos.</span><span class="sxs-lookup"><span data-stu-id="0a5cc-205">Try again after a few seconds.</span></span>

</dd> <dt>

<span data-ttu-id="0a5cc-206"><span id="BG_E_TOO_MANY_JOBS_PER_USER__0x80200049_"></span><span id="bg_e_too_many_jobs_per_user__0x80200049_"></span><span id="BG_E_TOO_MANY_JOBS_PER_USER__0X80200049_"></span>BG \_ E \_ \_ muitos \_ trabalhos \_ por \_ usuário (0x80200049)</span><span class="sxs-lookup"><span data-stu-id="0a5cc-206"><span id="BG_E_TOO_MANY_JOBS_PER_USER__0x80200049_"></span><span id="bg_e_too_many_jobs_per_user__0x80200049_"></span><span id="BG_E_TOO_MANY_JOBS_PER_USER__0X80200049_"></span>BG\_E\_TOO\_MANY\_JOBS\_PER\_USER (0x80200049)</span></span>
</dt> <dd>

<span data-ttu-id="0a5cc-207">A contagem de trabalhos para o usuário excedeu o limite de trabalho por usuário definido pela configuração de Política de Grupo MaxJobsPerUser.</span><span class="sxs-lookup"><span data-stu-id="0a5cc-207">The job count for the user has exceeded the per user job limit set by the MaxJobsPerUser Group Policy setting.</span></span>

</dd> <dt>

<span data-ttu-id="0a5cc-208"><span id="BG_E_TOO_MANY_JOBS_PER_MACHINE__0x80200050_"></span><span id="bg_e_too_many_jobs_per_machine__0x80200050_"></span><span id="BG_E_TOO_MANY_JOBS_PER_MACHINE__0X80200050_"></span>BG \_ E \_ \_ muitos \_ trabalhos \_ por \_ máquina (0x80200050)</span><span class="sxs-lookup"><span data-stu-id="0a5cc-208"><span id="BG_E_TOO_MANY_JOBS_PER_MACHINE__0x80200050_"></span><span id="bg_e_too_many_jobs_per_machine__0x80200050_"></span><span id="BG_E_TOO_MANY_JOBS_PER_MACHINE__0X80200050_"></span>BG\_E\_TOO\_MANY\_JOBS\_PER\_MACHINE (0x80200050)</span></span>
</dt> <dd>

<span data-ttu-id="0a5cc-209">A contagem de trabalhos para o computador excedeu o limite de trabalho por computador definido pela configuração de Política de Grupo MaxJobsPerMachine.</span><span class="sxs-lookup"><span data-stu-id="0a5cc-209">The job count for the computer has exceeded the per computer job limit set by the MaxJobsPerMachine Group Policy setting.</span></span>

</dd> <dt>

<span data-ttu-id="0a5cc-210"><span id="BG_E_TOO_MANY_FILES_IN_JOB__0x80200051_"></span><span id="bg_e_too_many_files_in_job__0x80200051_"></span><span id="BG_E_TOO_MANY_FILES_IN_JOB__0X80200051_"></span>BG \_ E \_ \_ muitos \_ arquivos \_ no \_ trabalho (0x80200051)</span><span class="sxs-lookup"><span data-stu-id="0a5cc-210"><span id="BG_E_TOO_MANY_FILES_IN_JOB__0x80200051_"></span><span id="bg_e_too_many_files_in_job__0x80200051_"></span><span id="BG_E_TOO_MANY_FILES_IN_JOB__0X80200051_"></span>BG\_E\_TOO\_MANY\_FILES\_IN\_JOB (0x80200051)</span></span>
</dt> <dd>

<span data-ttu-id="0a5cc-211">A contagem de arquivos para o trabalho excedeu o limite de arquivos por trabalho definido pela configuração de Política de Grupo MaxFilesPerJob.</span><span class="sxs-lookup"><span data-stu-id="0a5cc-211">The file count for the job has exceeded the per job file limit set by the MaxFilesPerJob Group Policy setting.</span></span>

</dd> <dt>

<span data-ttu-id="0a5cc-212"><span id="BG_E_TOO_MANY_RANGES_IN_FILE__0x80200052_"></span><span id="bg_e_too_many_ranges_in_file__0x80200052_"></span><span id="BG_E_TOO_MANY_RANGES_IN_FILE__0X80200052_"></span>BG \_ E um número \_ \_ excessivo \_ \_ de intervalos no \_ arquivo (0x80200052)</span><span class="sxs-lookup"><span data-stu-id="0a5cc-212"><span id="BG_E_TOO_MANY_RANGES_IN_FILE__0x80200052_"></span><span id="bg_e_too_many_ranges_in_file__0x80200052_"></span><span id="BG_E_TOO_MANY_RANGES_IN_FILE__0X80200052_"></span>BG\_E\_TOO\_MANY\_RANGES\_IN\_FILE (0x80200052)</span></span>
</dt> <dd>

<span data-ttu-id="0a5cc-213">A contagem de intervalos para o arquivo excedeu o limite por intervalo de arquivos definido pela configuração de Política de Grupo MaxRangesPerFile.</span><span class="sxs-lookup"><span data-stu-id="0a5cc-213">The range count for the file has exceeded the per file range limit set by the MaxRangesPerFile Group Policy setting.</span></span>

</dd> <dt>

<span data-ttu-id="0a5cc-214"><span id="BG_E_VALIDATION_FAILED__0x80200053_"></span><span id="bg_e_validation_failed__0x80200053_"></span><span id="BG_E_VALIDATION_FAILED__0X80200053_"></span>\_ \_ \_ Falha na validação de BG E (0x80200053)</span><span class="sxs-lookup"><span data-stu-id="0a5cc-214"><span id="BG_E_VALIDATION_FAILED__0x80200053_"></span><span id="bg_e_validation_failed__0x80200053_"></span><span id="BG_E_VALIDATION_FAILED__0X80200053_"></span>BG\_E\_VALIDATION\_FAILED (0x80200053)</span></span>
</dt> <dd>

<span data-ttu-id="0a5cc-215">O aplicativo solicitou dados de um site, mas a resposta não era válida.</span><span class="sxs-lookup"><span data-stu-id="0a5cc-215">The application requested data from a website, but the response was not valid.</span></span> <span data-ttu-id="0a5cc-216">Para obter detalhes, use Visualizador de Eventos para exibir os logs de aplicativo \\ \\ \\ log operacional Microsoft Windows bits-cliente \\ .</span><span class="sxs-lookup"><span data-stu-id="0a5cc-216">For details, use Event Viewer to view the Application Logs\\Microsoft\\Windows\\Bits-client\\Operational log.</span></span>

</dd> <dt>

<span data-ttu-id="0a5cc-217"><span id="BG_E_MAXDOWNLOAD_TIMEOUT__0x80200054_"></span><span id="bg_e_maxdownload_timeout__0x80200054_"></span><span id="BG_E_MAXDOWNLOAD_TIMEOUT__0X80200054_"></span>\_ \_ \_ Tempo limite de BG E MAXDOWNLOAD (0x80200054)</span><span class="sxs-lookup"><span data-stu-id="0a5cc-217"><span id="BG_E_MAXDOWNLOAD_TIMEOUT__0x80200054_"></span><span id="bg_e_maxdownload_timeout__0x80200054_"></span><span id="BG_E_MAXDOWNLOAD_TIMEOUT__0X80200054_"></span>BG\_E\_MAXDOWNLOAD\_TIMEOUT (0x80200054)</span></span>
</dt> <dd>

<span data-ttu-id="0a5cc-218">O BITS atingiu o tempo limite baixando o trabalho.</span><span class="sxs-lookup"><span data-stu-id="0a5cc-218">BITS timed out downloading the job.</span></span> <span data-ttu-id="0a5cc-219">O download não foi concluído dentro do tempo de download máximo definido no trabalho ou na configuração de Política de Grupo MaxDownloadTime.</span><span class="sxs-lookup"><span data-stu-id="0a5cc-219">The download did not complete within the maximum download time set on the job or the MaxDownloadTime Group Policy setting.</span></span>

</dd> <dt>

<span data-ttu-id="0a5cc-220"><span id="BG_E_HTTP_ERROR_400__0x80190190_"></span><span id="bg_e_http_error_400__0x80190190_"></span><span id="BG_E_HTTP_ERROR_400__0X80190190_"></span>\_Erro BG \_ E \_ http \_ 400 (0x80190190)</span><span class="sxs-lookup"><span data-stu-id="0a5cc-220"><span id="BG_E_HTTP_ERROR_400__0x80190190_"></span><span id="bg_e_http_error_400__0x80190190_"></span><span id="BG_E_HTTP_ERROR_400__0X80190190_"></span>BG\_E\_HTTP\_ERROR\_400 (0x80190190)</span></span>
</dt> <dd>

<span data-ttu-id="0a5cc-221">O servidor não pôde processar a solicitação de transferência porque a sintaxe do nome do arquivo remoto é inválida.</span><span class="sxs-lookup"><span data-stu-id="0a5cc-221">The server could not process the transfer request because the syntax of the remote file name is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="0a5cc-222"><span id="BG_E_HTTP_ERROR_401__0x80190191_"></span><span id="bg_e_http_error_401__0x80190191_"></span><span id="BG_E_HTTP_ERROR_401__0X80190191_"></span>\_Erro BG \_ E \_ http \_ 401 (0x80190191)</span><span class="sxs-lookup"><span data-stu-id="0a5cc-222"><span id="BG_E_HTTP_ERROR_401__0x80190191_"></span><span id="bg_e_http_error_401__0x80190191_"></span><span id="BG_E_HTTP_ERROR_401__0X80190191_"></span>BG\_E\_HTTP\_ERROR\_401 (0x80190191)</span></span>
</dt> <dd>

<span data-ttu-id="0a5cc-223">O usuário não tem permissão para acessar o arquivo remoto.</span><span class="sxs-lookup"><span data-stu-id="0a5cc-223">The user does not have permission to access the remote file.</span></span> <span data-ttu-id="0a5cc-224">O recurso solicitado requer a autenticação do usuário.</span><span class="sxs-lookup"><span data-stu-id="0a5cc-224">The requested resource requires user authentication.</span></span>

</dd> <dt>

<span data-ttu-id="0a5cc-225"><span id="BG_E_HTTP_ERROR_404__0x80190194_"></span><span id="bg_e_http_error_404__0x80190194_"></span><span id="BG_E_HTTP_ERROR_404__0X80190194_"></span>\_Erro BG \_ E \_ http \_ 404 (0x80190194)</span><span class="sxs-lookup"><span data-stu-id="0a5cc-225"><span id="BG_E_HTTP_ERROR_404__0x80190194_"></span><span id="bg_e_http_error_404__0x80190194_"></span><span id="BG_E_HTTP_ERROR_404__0X80190194_"></span>BG\_E\_HTTP\_ERROR\_404 (0x80190194)</span></span>
</dt> <dd>

<span data-ttu-id="0a5cc-226">A URL solicitada não existe no servidor.</span><span class="sxs-lookup"><span data-stu-id="0a5cc-226">The requested URL does not exist on the server.</span></span>

<span data-ttu-id="0a5cc-227">No IIS 7, esse erro pode indicar</span><span class="sxs-lookup"><span data-stu-id="0a5cc-227">In IIS 7, this error can indicate</span></span>

-   <span data-ttu-id="0a5cc-228">Esses carregamentos do BITS não estão habilitados no diretório virtual (vdir) no servidor.</span><span class="sxs-lookup"><span data-stu-id="0a5cc-228">That BITS uploads are not enabled on the virtual directory (vdir) on the server.</span></span>
-   <span data-ttu-id="0a5cc-229">Que o tamanho do carregamento exceda o limite máximo de upload (para obter detalhes, consulte a propriedade de extensão do IIS [**BITSMaximumUploadSize**](bits-iis-extension-properties.md) ).</span><span class="sxs-lookup"><span data-stu-id="0a5cc-229">That the upload size exceeds the maximum upload limit (for details, see the [**BITSMaximumUploadSize**](bits-iis-extension-properties.md) IIS extension property).</span></span>

</dd> <dt>

<span data-ttu-id="0a5cc-230"><span id="BG_E_HTTP_ERROR_407__0x80190197_"></span><span id="bg_e_http_error_407__0x80190197_"></span><span id="BG_E_HTTP_ERROR_407__0X80190197_"></span>\_Erro BG \_ E \_ http \_ 407 (0x80190197)</span><span class="sxs-lookup"><span data-stu-id="0a5cc-230"><span id="BG_E_HTTP_ERROR_407__0x80190197_"></span><span id="bg_e_http_error_407__0x80190197_"></span><span id="BG_E_HTTP_ERROR_407__0X80190197_"></span>BG\_E\_HTTP\_ERROR\_407 (0x80190197)</span></span>
</dt> <dd>

<span data-ttu-id="0a5cc-231">O usuário não tem permissão para acessar o proxy.</span><span class="sxs-lookup"><span data-stu-id="0a5cc-231">The user does not have permission to access the proxy.</span></span> <span data-ttu-id="0a5cc-232">O proxy requer autenticação do usuário.</span><span class="sxs-lookup"><span data-stu-id="0a5cc-232">The proxy requires user authentication.</span></span>

</dd> <dt>

<span data-ttu-id="0a5cc-233"><span id="BG_E_HTTP_ERROR_414__0x8019019E_"></span><span id="bg_e_http_error_414__0x8019019e_"></span><span id="BG_E_HTTP_ERROR_414__0X8019019E_"></span>\_Erro BG \_ E \_ http \_ 414 (0x8019019E)</span><span class="sxs-lookup"><span data-stu-id="0a5cc-233"><span id="BG_E_HTTP_ERROR_414__0x8019019E_"></span><span id="bg_e_http_error_414__0x8019019e_"></span><span id="BG_E_HTTP_ERROR_414__0X8019019E_"></span>BG\_E\_HTTP\_ERROR\_414 (0x8019019E)</span></span>
</dt> <dd>

<span data-ttu-id="0a5cc-234">O servidor não pode processar a solicitação de transferência.</span><span class="sxs-lookup"><span data-stu-id="0a5cc-234">The server cannot process the transfer request.</span></span> <span data-ttu-id="0a5cc-235">O Uniform Resource Identifier (URI) no nome do arquivo remoto é maior do que o servidor pode interpretar.</span><span class="sxs-lookup"><span data-stu-id="0a5cc-235">The Uniform Resource Identifier (URI) in the remote file name is longer than the server can interpret.</span></span>

</dd> <dt>

<span data-ttu-id="0a5cc-236"><span id="BG_E_HTTP_ERROR_501__0x801901F5_"></span><span id="bg_e_http_error_501__0x801901f5_"></span><span id="BG_E_HTTP_ERROR_501__0X801901F5_"></span>\_Erro BG \_ E \_ http \_ 501 (0x801901F5)</span><span class="sxs-lookup"><span data-stu-id="0a5cc-236"><span id="BG_E_HTTP_ERROR_501__0x801901F5_"></span><span id="bg_e_http_error_501__0x801901f5_"></span><span id="BG_E_HTTP_ERROR_501__0X801901F5_"></span>BG\_E\_HTTP\_ERROR\_501 (0x801901F5)</span></span>
</dt> <dd>

<span data-ttu-id="0a5cc-237">O servidor não oferece suporte à funcionalidade necessária para atender à solicitação.</span><span class="sxs-lookup"><span data-stu-id="0a5cc-237">The server does not support the functionality required to fulfill the request.</span></span> <span data-ttu-id="0a5cc-238">No IIS 6, esse erro indica que os carregamentos do BITS não estão habilitados no diretório virtual (vdir) no servidor.</span><span class="sxs-lookup"><span data-stu-id="0a5cc-238">In IIS 6, this error indicates that BITS uploads are not enabled on the virtual directory (vdir) on the server.</span></span>

</dd> <dt>

<span data-ttu-id="0a5cc-239"><span id="BG_E_HTTP_ERROR_503__0x801901F7_"></span><span id="bg_e_http_error_503__0x801901f7_"></span><span id="BG_E_HTTP_ERROR_503__0X801901F7_"></span>\_Erro BG \_ E \_ http \_ 503 (0x801901F7)</span><span class="sxs-lookup"><span data-stu-id="0a5cc-239"><span id="BG_E_HTTP_ERROR_503__0x801901F7_"></span><span id="bg_e_http_error_503__0x801901f7_"></span><span id="BG_E_HTTP_ERROR_503__0X801901F7_"></span>BG\_E\_HTTP\_ERROR\_503 (0x801901F7)</span></span>
</dt> <dd>

<span data-ttu-id="0a5cc-240">O serviço está temporariamente sobrecarregado e não pode processar a solicitação.</span><span class="sxs-lookup"><span data-stu-id="0a5cc-240">The service is temporarily overloaded and cannot process the request.</span></span> <span data-ttu-id="0a5cc-241">Retome o trabalho em um momento posterior.</span><span class="sxs-lookup"><span data-stu-id="0a5cc-241">Resume the job at a later time.</span></span>

</dd> <dt>

<span data-ttu-id="0a5cc-242"><span id="BG_E_HTTP_ERROR_504__0x801901F8_"></span><span id="bg_e_http_error_504__0x801901f8_"></span><span id="BG_E_HTTP_ERROR_504__0X801901F8_"></span>\_Erro BG \_ E \_ http \_ 504 (0x801901F8)</span><span class="sxs-lookup"><span data-stu-id="0a5cc-242"><span id="BG_E_HTTP_ERROR_504__0x801901F8_"></span><span id="bg_e_http_error_504__0x801901f8_"></span><span id="BG_E_HTTP_ERROR_504__0X801901F8_"></span>BG\_E\_HTTP\_ERROR\_504 (0x801901F8)</span></span>
</dt> <dd>

<span data-ttu-id="0a5cc-243">A solicitação de transferência atingiu o tempo limite enquanto aguardava um gateway.</span><span class="sxs-lookup"><span data-stu-id="0a5cc-243">The transfer request timed out while waiting for a gateway.</span></span> <span data-ttu-id="0a5cc-244">Retome o trabalho em um momento posterior.</span><span class="sxs-lookup"><span data-stu-id="0a5cc-244">Resume the job at a later time.</span></span>

</dd> <dt>

<span data-ttu-id="0a5cc-245"><span id="BG_E_HTTP_ERROR_505__0x801901F9_"></span><span id="bg_e_http_error_505__0x801901f9_"></span><span id="BG_E_HTTP_ERROR_505__0X801901F9_"></span>\_Erro BG \_ E \_ http \_ 505 (0x801901F9)</span><span class="sxs-lookup"><span data-stu-id="0a5cc-245"><span id="BG_E_HTTP_ERROR_505__0x801901F9_"></span><span id="bg_e_http_error_505__0x801901f9_"></span><span id="BG_E_HTTP_ERROR_505__0X801901F9_"></span>BG\_E\_HTTP\_ERROR\_505 (0x801901F9)</span></span>
</dt> <dd>

<span data-ttu-id="0a5cc-246">O servidor não oferece suporte à versão do protocolo HTTP especificada no nome do arquivo remoto.</span><span class="sxs-lookup"><span data-stu-id="0a5cc-246">The server does not support the HTTP protocol version specified in the remote file name.</span></span>

</dd> </dl>

<span data-ttu-id="0a5cc-247">O arquivo de cabeçalho Bitsmsg. h contém valores adicionais de retorno de HTTP não listados acima que os BITS usam internamente.</span><span class="sxs-lookup"><span data-stu-id="0a5cc-247">The Bitsmsg.h header file contains additional HTTP return values not listed above that BITS uses internally.</span></span> <span data-ttu-id="0a5cc-248">Para obter informações sobre esses e outros valores de retorno de HTTP que você pode receber, consulte a especificação RFC 2616 da força de tarefas de engenharia da Internet em [https://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html\#sec10](https://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html#sec10) .</span><span class="sxs-lookup"><span data-stu-id="0a5cc-248">For information on these and other HTTP return values you can receive, see the RFC 2616 specification from the Internet Engineering Task Force at [https://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html\#sec10](https://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html#sec10).</span></span>

 

 