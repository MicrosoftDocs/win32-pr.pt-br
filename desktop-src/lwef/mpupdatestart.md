---
title: Função MpUpdateStart (MpClient. h)
description: Inicia uma operação de atualização de assinatura.
ms.assetid: BB056356-17E5-42F0-9636-9E1C254361E4
keywords:
- Recursos do ambiente Windows herdado da função MpUpdateStart
topic_type:
- apiref
api_name:
- MpUpdateStart
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39867525529339c6b354ae771b070589ca52acfa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455819"
---
# <a name="mpupdatestart-function"></a><span data-ttu-id="e56d3-104">Função MpUpdateStart</span><span class="sxs-lookup"><span data-stu-id="e56d3-104">MpUpdateStart function</span></span>

<span data-ttu-id="e56d3-105">Inicia uma operação de atualização de assinatura.</span><span class="sxs-lookup"><span data-stu-id="e56d3-105">Starts a signature update operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="e56d3-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e56d3-106">Syntax</span></span>


```C++
HRESULT WINAPI MpUpdateStart(
  _In_     MPHANDLE         hMpHandle,
  _In_     DWORD            dwUpdateOptions,
  _In_opt_ PMPCALLBACK_INFO pCallbackInfo,
  _Out_    PMPHANDLE        phUpdateHandle
);
```



## <a name="parameters"></a><span data-ttu-id="e56d3-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e56d3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e56d3-108">*hMpHandle* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e56d3-108">*hMpHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e56d3-109">Tipo: **MPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="e56d3-109">Type: **MPHANDLE**</span></span>

<span data-ttu-id="e56d3-110">Identificador para a interface do Malware Protection Manager.</span><span class="sxs-lookup"><span data-stu-id="e56d3-110">Handle to the malware protection manager interface.</span></span> <span data-ttu-id="e56d3-111">Esse identificador é retornado pela função [**MpManagerOpen**](mpmanageropen.md) .</span><span class="sxs-lookup"><span data-stu-id="e56d3-111">This handle is returned by the [**MpManagerOpen**](mpmanageropen.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="e56d3-112">*dwUpdateOptions* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e56d3-112">*dwUpdateOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e56d3-113">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="e56d3-113">Type: **DWORD**</span></span>

<span data-ttu-id="e56d3-114">Especifica a opção para a operação de atualização de assinatura.</span><span class="sxs-lookup"><span data-stu-id="e56d3-114">Specifies the option for the signature update operation.</span></span> <span data-ttu-id="e56d3-115">Pode ser um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="e56d3-115">It can be one of the following values:</span></span>



| <span data-ttu-id="e56d3-116">Valor</span><span class="sxs-lookup"><span data-stu-id="e56d3-116">Value</span></span>                                                                                                                                                                                              | <span data-ttu-id="e56d3-117">Significado</span><span class="sxs-lookup"><span data-stu-id="e56d3-117">Meaning</span></span>                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MPUPDATE_OPTION_NONE"></span><span id="mpupdate_option_none"></span><dl> <span data-ttu-id="e56d3-118"><dt>**\_opção MPUPDATE \_ None**</dt></span><span class="sxs-lookup"><span data-stu-id="e56d3-118"><dt>**MPUPDATE\_OPTION\_NONE**</dt></span></span> </dl>                | <span data-ttu-id="e56d3-119">Nenhuma opção específica é solicitada.</span><span class="sxs-lookup"><span data-stu-id="e56d3-119">No specific option is requested.</span></span><br/>                                                                                                                                                                                                                                                      |
| <span id="MPUPDATE_OPTION_ASYNC"></span><span id="mpupdate_option_async"></span><dl> <span data-ttu-id="e56d3-120"><dt>**\_opção MPUPDATE \_ Async**</dt></span><span class="sxs-lookup"><span data-stu-id="e56d3-120"><dt>**MPUPDATE\_OPTION\_ASYNC**</dt></span></span> </dl>             | <span data-ttu-id="e56d3-121">A operação de atualização deve ser assíncrona, em que **MpUpdateStart** retorna imediatamente após o início bem-sucedido da atualização de assinatura.</span><span class="sxs-lookup"><span data-stu-id="e56d3-121">The update operation is to be asynchronous, where **MpUpdateStart** returns immediately after the successful initiation of the signature update.</span></span> <span data-ttu-id="e56d3-122">(Por padrão, a operação de atualização é síncrona, o que significa que **MpUpdateStart** retornará somente depois que a atualização da assinatura for concluída.)</span><span class="sxs-lookup"><span data-stu-id="e56d3-122">(By default the update operation is synchronous, meaning **MpUpdateStart** will return only after the signature update is finished.)</span></span><br/> |
| <span id="MPUPDATE_OPTION_PROGRESS"></span><span id="mpupdate_option_progress"></span><dl> <span data-ttu-id="e56d3-123"><dt>**\_progresso da opção MPUPDATE \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e56d3-123"><dt>**MPUPDATE\_OPTION\_PROGRESS**</dt></span></span> </dl>    | <span data-ttu-id="e56d3-124">O chamador está interessado em receber informações de progresso de atualização de assinatura por meio de um retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="e56d3-124">The caller is interested in receiving signature update progress information via a callback.</span></span><br/>                                                                                                                                                                                           |
| <span id="MPUPDATE_OPTION_HTTP"></span><span id="mpupdate_option_http"></span><dl> <span data-ttu-id="e56d3-125"><dt>**\_opção MPUPDATE \_ http**</dt></span><span class="sxs-lookup"><span data-stu-id="e56d3-125"><dt>**MPUPDATE\_OPTION\_HTTP**</dt></span></span> </dl>                | <span data-ttu-id="e56d3-126">A atualização de assinatura é executada baixando o pacote de assinatura completo do site do portal de segurança da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e56d3-126">The signature update is performed by downloading the full signature package from the Microsoft security portal site.</span></span> <span data-ttu-id="e56d3-127">Isso pode ser usado como uma opção de fallback se o cliente estiver enfrentando um problema de download de assinatura por meio de Microsoft Update.</span><span class="sxs-lookup"><span data-stu-id="e56d3-127">This can be used as a fallback option if the client is experiencing a signature download problem via Microsoft Update.</span></span><br/>                                           |
| <span id="MPUPDATE_OPTION_UNC"></span><span id="mpupdate_option_unc"></span><dl> <span data-ttu-id="e56d3-128"><dt>**\_UNC de opção MPUPDATE \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e56d3-128"><dt>**MPUPDATE\_OPTION\_UNC**</dt></span></span> </dl>                   | <span data-ttu-id="e56d3-129">Executa a atualização de assinatura usando download direto de compartilhamentos UNC.</span><span class="sxs-lookup"><span data-stu-id="e56d3-129">Performs signature update using direct download from UNC shares.</span></span><br/>                                                                                                                                                                                                                      |
| <span id="MPUPDATE_OPTION_MANAGED"></span><span id="mpupdate_option_managed"></span><dl> <span data-ttu-id="e56d3-130"><dt>**\_opção MPUPDATE \_ gerenciada**</dt></span><span class="sxs-lookup"><span data-stu-id="e56d3-130"><dt>**MPUPDATE\_OPTION\_MANAGED**</dt></span></span> </dl>       | <span data-ttu-id="e56d3-131">Executa a atualização de assinatura usando o WSUS do serviço gerenciado.</span><span class="sxs-lookup"><span data-stu-id="e56d3-131">Performs signature update using the Managed Service WSUS.</span></span><br/>                                                                                                                                                                                                                             |
| <span id="MPUPDATE_OPTION_UNMANAGED"></span><span id="mpupdate_option_unmanaged"></span><dl> <span data-ttu-id="e56d3-132"><dt>**\_opção MPUPDATE \_ não gerenciada**</dt></span><span class="sxs-lookup"><span data-stu-id="e56d3-132"><dt>**MPUPDATE\_OPTION\_UNMANAGED**</dt></span></span> </dl> | <span data-ttu-id="e56d3-133">Executa a atualização de assinatura usando o serviço não gerenciado MU/WU.</span><span class="sxs-lookup"><span data-stu-id="e56d3-133">Performs signature update using the Unmanaged Service MU/WU.</span></span><br/>                                                                                                                                                                                                                          |



 

</dd> <dt>

<span data-ttu-id="e56d3-134">*pCallbackInfo* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="e56d3-134">*pCallbackInfo* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e56d3-135">Tipo: **\_ informações de PMPCALLBACK**</span><span class="sxs-lookup"><span data-stu-id="e56d3-135">Type: **PMPCALLBACK\_INFO**</span></span>

<span data-ttu-id="e56d3-136">Um ponteiro para as informações de retorno de chamada usadas para alimentar o cliente com alterações de estado de atualização de assinatura (como iniciar e concluir) e informações de progresso.</span><span class="sxs-lookup"><span data-stu-id="e56d3-136">A pointer to the callback information used to feed the client with signature update state changes (such as start and complete) and progress information.</span></span> <span data-ttu-id="e56d3-137">Os [**\_ dados de MPCALLBACK**](mpcallback-data.md) passados na função de retorno de chamada relatam o estado de atualização real e informações relacionadas ao progresso.</span><span class="sxs-lookup"><span data-stu-id="e56d3-137">The [**MPCALLBACK\_DATA**](mpcallback-data.md) passed back in the callback function reports actual update state and progress-related information.</span></span> <span data-ttu-id="e56d3-138">Veja a seguir uma lista de possíveis retornos de chamada:</span><span class="sxs-lookup"><span data-stu-id="e56d3-138">The following is a list of possible callbacks:</span></span>



| <span data-ttu-id="e56d3-139">Valor</span><span class="sxs-lookup"><span data-stu-id="e56d3-139">Value</span></span>                                                                                                                                                                                                                                | <span data-ttu-id="e56d3-140">Significado</span><span class="sxs-lookup"><span data-stu-id="e56d3-140">Meaning</span></span>                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MPNOTIFY_SIGUPDATE_START"></span><span id="mpnotify_sigupdate_start"></span><dl> <span data-ttu-id="e56d3-141"><dt>**MPNOTIFY \_ SIGUPDATE \_ Start**</dt></span><span class="sxs-lookup"><span data-stu-id="e56d3-141"><dt>**MPNOTIFY\_SIGUPDATE\_START**</dt></span></span> </dl>                                      | <span data-ttu-id="e56d3-142">Operação de atualização iniciada.</span><span class="sxs-lookup"><span data-stu-id="e56d3-142">Update operation started.</span></span><br/>                                                                                                                                  |
| <span id="MPNOTIFY_SIGUPDATE_COMPLETE"></span><span id="mpnotify_sigupdate_complete"></span><dl> <span data-ttu-id="e56d3-143"><dt>**MPNOTIFY \_ SIGUPDATE \_ concluída**</dt></span><span class="sxs-lookup"><span data-stu-id="e56d3-143"><dt>**MPNOTIFY\_SIGUPDATE\_COMPLETE**</dt></span></span> </dl>                             | <span data-ttu-id="e56d3-144">Operação de atualização concluída.</span><span class="sxs-lookup"><span data-stu-id="e56d3-144">Update operation completed.</span></span><br/>                                                                                                                                |
| <span id="MPNOTIFY_SIGUPDATE_SEARCH_START"></span><span id="mpnotify_sigupdate_search_start"></span><dl> <span data-ttu-id="e56d3-145"><dt>**início da pesquisa do MPNOTIFY \_ SIGUPDATE \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e56d3-145"><dt>**MPNOTIFY\_SIGUPDATE\_SEARCH\_START**</dt></span></span> </dl>                | <span data-ttu-id="e56d3-146">Pesquisa de atualizações iniciada.</span><span class="sxs-lookup"><span data-stu-id="e56d3-146">Search for updates started.</span></span><br/>                                                                                                                                |
| <span id="MPNOTIFY_SIGUPDATE_SEARCH_COMPLETE"></span><span id="mpnotify_sigupdate_search_complete"></span><dl> <span data-ttu-id="e56d3-147"><dt>**pesquisa do MPNOTIFY \_ SIGUPDATE \_ \_ concluída**</dt></span><span class="sxs-lookup"><span data-stu-id="e56d3-147"><dt>**MPNOTIFY\_SIGUPDATE\_SEARCH\_COMPLETE**</dt></span></span> </dl>       | <span data-ttu-id="e56d3-148">Pesquisa de atualizações concluída.</span><span class="sxs-lookup"><span data-stu-id="e56d3-148">Search for updates completed.</span></span> <span data-ttu-id="e56d3-149">Informações adicionais estão disponíveis por meio da estrutura de [**\_ dados MPSIGUPDATE**](mpsigupdate-data.md) .</span><span class="sxs-lookup"><span data-stu-id="e56d3-149">Additional information is available via [**MPSIGUPDATE\_DATA**](mpsigupdate-data.md) structure.</span></span><br/>                             |
| <span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_START"></span><span id="mpnotify_sigupdate_download_start"></span><dl> <span data-ttu-id="e56d3-150"><dt>**início do download do MPNOTIFY \_ SIGUPDATE \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e56d3-150"><dt>**MPNOTIFY\_SIGUPDATE\_DOWNLOAD\_START**</dt></span></span> </dl>          | <span data-ttu-id="e56d3-151">Download para a atualização iniciado.</span><span class="sxs-lookup"><span data-stu-id="e56d3-151">Download for update started.</span></span><br/>                                                                                                                               |
| <span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_PROGRESS"></span><span id="mpnotify_sigupdate_download_progress"></span><dl> <span data-ttu-id="e56d3-152"><dt>**progresso do download do MPNOTIFY \_ SIGUPDATE \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e56d3-152"><dt>**MPNOTIFY\_SIGUPDATE\_DOWNLOAD\_PROGRESS**</dt></span></span> </dl> | <span data-ttu-id="e56d3-153">Baixar informações de progresso.</span><span class="sxs-lookup"><span data-stu-id="e56d3-153">Download progress information.</span></span> <span data-ttu-id="e56d3-154">Informações adicionais estão disponíveis por meio da estrutura de [**\_ dados MPSIGUPDATE**](mpsigupdate-data.md) .</span><span class="sxs-lookup"><span data-stu-id="e56d3-154">Additional information is available via [**MPSIGUPDATE\_DATA**](mpsigupdate-data.md) structure.</span></span><br/>                            |
| <span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_COMPLETE"></span><span id="mpnotify_sigupdate_download_complete"></span><dl> <span data-ttu-id="e56d3-155"><dt>**Download do MPNOTIFY \_ SIGUPDATE \_ \_ concluído**</dt></span><span class="sxs-lookup"><span data-stu-id="e56d3-155"><dt>**MPNOTIFY\_SIGUPDATE\_DOWNLOAD\_COMPLETE**</dt></span></span> </dl> | <span data-ttu-id="e56d3-156">Download para atualização concluído.</span><span class="sxs-lookup"><span data-stu-id="e56d3-156">Download for update complete.</span></span> <span data-ttu-id="e56d3-157">Informações adicionais estão disponíveis por meio da estrutura de [**\_ dados MPSIGUPDATE**](mpsigupdate-data.md) .</span><span class="sxs-lookup"><span data-stu-id="e56d3-157">Additional information is available via [**MPSIGUPDATE\_DATA**](mpsigupdate-data.md) structure.</span></span><br/>                             |
| <span id="MPNOTIFY_SIGUPDATE_INSTALL_START"></span><span id="mpnotify_sigupdate_install_start"></span><dl> <span data-ttu-id="e56d3-158"><dt>**início da instalação do MPNOTIFY \_ SIGUPDATE \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e56d3-158"><dt>**MPNOTIFY\_SIGUPDATE\_INSTALL\_START**</dt></span></span> </dl>             | <span data-ttu-id="e56d3-159">Instalação da atualização iniciada.</span><span class="sxs-lookup"><span data-stu-id="e56d3-159">Installation of update started.</span></span><br/>                                                                                                                            |
| <span id="MPNOTIFY_SIGUPDATE_INSTALL_PROGRESS"></span><span id="mpnotify_sigupdate_install_progress"></span><dl> <span data-ttu-id="e56d3-160"><dt>**progresso da instalação do MPNOTIFY \_ SIGUPDATE \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e56d3-160"><dt>**MPNOTIFY\_SIGUPDATE\_INSTALL\_PROGRESS**</dt></span></span> </dl>    | <span data-ttu-id="e56d3-161">Informações de progresso da instalação.</span><span class="sxs-lookup"><span data-stu-id="e56d3-161">Installation progress information.</span></span> <span data-ttu-id="e56d3-162">Informações adicionais estão disponíveis por meio da estrutura de [**\_ dados MPSIGUPDATE**](mpsigupdate-data.md) .</span><span class="sxs-lookup"><span data-stu-id="e56d3-162">Additional information is available via [**MPSIGUPDATE\_DATA**](mpsigupdate-data.md) structure.</span></span><br/>                        |
| <span id="MPNOTIFY_SIGUPDATE_INSTALL_COMPLETE"></span><span id="mpnotify_sigupdate_install_complete"></span><dl> <span data-ttu-id="e56d3-163"><dt>**instalação do MPNOTIFY \_ SIGUPDATE \_ \_ concluída**</dt></span><span class="sxs-lookup"><span data-stu-id="e56d3-163"><dt>**MPNOTIFY\_SIGUPDATE\_INSTALL\_COMPLETE**</dt></span></span> </dl>    | <span data-ttu-id="e56d3-164">Instalação da atualização concluída.</span><span class="sxs-lookup"><span data-stu-id="e56d3-164">Installation of update completed.</span></span> <span data-ttu-id="e56d3-165">Informações adicionais estão disponíveis por meio da estrutura de [**\_ dados MPSIGUPDATE**](mpsigupdate-data.md) .</span><span class="sxs-lookup"><span data-stu-id="e56d3-165">Additional information is available via [**MPSIGUPDATE\_DATA**](mpsigupdate-data.md) structure.</span></span><br/>                         |
| <span id="MPNOTIFY_SIGUPDATE_REQUEST_PROCESSED"></span><span id="mpnotify_sigupdate_request_processed"></span><dl> <span data-ttu-id="e56d3-166"><dt>**\_solicitação mpnotify \_ SIGUPDATE \_ processada**</dt></span><span class="sxs-lookup"><span data-stu-id="e56d3-166"><dt>**MPNOTIFY\_SIGUPDATE\_REQUEST\_PROCESSED**</dt></span></span> </dl> | <span data-ttu-id="e56d3-167">O serviço Antimalware processou uma solicitação de atualização de assinatura.</span><span class="sxs-lookup"><span data-stu-id="e56d3-167">The antimalware service processed a signature update request.</span></span> <span data-ttu-id="e56d3-168">A falha ou o êxito é indicado por *HRESULT* nos [**\_ dados de MPCALLBACK**](mpcallback-data.md).</span><span class="sxs-lookup"><span data-stu-id="e56d3-168">Failure or success is indicated by *hResult* in [**MPCALLBACK\_DATA**](mpcallback-data.md).</span></span><br/> |
| <span id="MPNOTIFY_SIGUPDATE_REBOOT_REQUIRED"></span><span id="mpnotify_sigupdate_reboot_required"></span><dl> <span data-ttu-id="e56d3-169"><dt>**\_reinicialização mpnotify SIGUPDATE \_ \_ necessária**</dt></span><span class="sxs-lookup"><span data-stu-id="e56d3-169"><dt>**MPNOTIFY\_SIGUPDATE\_REBOOT\_REQUIRED**</dt></span></span> </dl>       | <span data-ttu-id="e56d3-170">Requer reinicialização para concluir a operação de atualização.</span><span class="sxs-lookup"><span data-stu-id="e56d3-170">Requires reboot to complete the update operation.</span></span> <span data-ttu-id="e56d3-171">A falha ou o êxito é indicado por *HRESULT* nos [**\_ dados de MPCALLBACK**](mpcallback-data.md).</span><span class="sxs-lookup"><span data-stu-id="e56d3-171">Failure or success is indicated by *hResult* in [**MPCALLBACK\_DATA**](mpcallback-data.md).</span></span><br/>             |
| <span id="MPNOTIFY_INTERNAL_FAILURE"></span><span id="mpnotify_internal_failure"></span><dl> <span data-ttu-id="e56d3-172"><dt>**\_falha interna do mpnotify \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e56d3-172"><dt>**MPNOTIFY\_INTERNAL\_FAILURE**</dt></span></span> </dl>                                   | <span data-ttu-id="e56d3-173">A operação de atualização de assinatura encontrou uma falha genérica.</span><span class="sxs-lookup"><span data-stu-id="e56d3-173">Signature update operation has encountered a generic failure.</span></span> <span data-ttu-id="e56d3-174">O *HRESULT* nos [**\_ dados MPCALLBACK**](mpcallback-data.md) tem o código de erro específico.</span><span class="sxs-lookup"><span data-stu-id="e56d3-174">The *hResult* in [**MPCALLBACK\_DATA**](mpcallback-data.md) has the specific error code.</span></span><br/>    |



 

</dd> <dt>

<span data-ttu-id="e56d3-175">*phUpdateHandle* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e56d3-175">*phUpdateHandle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e56d3-176">Tipo: **PMPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="e56d3-176">Type: **PMPHANDLE**</span></span>

<span data-ttu-id="e56d3-177">O identificador de atualização retornado que identifica a operação de atualização de assinatura iniciada no momento.</span><span class="sxs-lookup"><span data-stu-id="e56d3-177">Returned update handle which identifies the currently initiated signature update operation.</span></span> <span data-ttu-id="e56d3-178">Esse identificador pode ser usado em chamadas de função subsequentes, como para controlar a operação de atualização de assinatura.</span><span class="sxs-lookup"><span data-stu-id="e56d3-178">This handle can be used in subsequent function calls, such as to control the signature update operation.</span></span> <span data-ttu-id="e56d3-179">O identificador deve ser fechado com a função [**MpHandleClose**](mphandleclose.md) .</span><span class="sxs-lookup"><span data-stu-id="e56d3-179">The handle must be closed with the [**MpHandleClose**](mphandleclose.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e56d3-180">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e56d3-180">Return value</span></span>

<span data-ttu-id="e56d3-181">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="e56d3-181">Type: **HRESULT**</span></span>

<span data-ttu-id="e56d3-182">Se a função for bem sucedido, o valor de retorno será **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="e56d3-182">If the function succeeds the return value is **S\_OK**.</span></span>

<span data-ttu-id="e56d3-183">Se a função falhar, o valor de retorno será um código **HRESULT** com falha.</span><span class="sxs-lookup"><span data-stu-id="e56d3-183">If the function fails then the return value is a failed **HRESULT** code.</span></span> <span data-ttu-id="e56d3-184">O chamador pode usar a função [**MpErrorMessageFormat**](mperrormessageformat.md) para obter uma descrição genérica da mensagem de erro.</span><span class="sxs-lookup"><span data-stu-id="e56d3-184">The caller can use the [**MpErrorMessageFormat**](mperrormessageformat.md) function to get a generic description of the error message.</span></span>

## <a name="requirements"></a><span data-ttu-id="e56d3-185">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e56d3-185">Requirements</span></span>



| <span data-ttu-id="e56d3-186">Requisito</span><span class="sxs-lookup"><span data-stu-id="e56d3-186">Requirement</span></span> | <span data-ttu-id="e56d3-187">Valor</span><span class="sxs-lookup"><span data-stu-id="e56d3-187">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e56d3-188">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e56d3-188">Minimum supported client</span></span><br/> | <span data-ttu-id="e56d3-189">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="e56d3-189">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="e56d3-190">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e56d3-190">Minimum supported server</span></span><br/> | <span data-ttu-id="e56d3-191">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="e56d3-191">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e56d3-192">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e56d3-192">Header</span></span><br/>                   | <dl> <span data-ttu-id="e56d3-193"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="e56d3-193"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="e56d3-194">DLL</span><span class="sxs-lookup"><span data-stu-id="e56d3-194">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e56d3-195"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e56d3-195"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e56d3-196">Confira também</span><span class="sxs-lookup"><span data-stu-id="e56d3-196">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e56d3-197">**MpErrorMessageFormat**</span><span class="sxs-lookup"><span data-stu-id="e56d3-197">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="e56d3-198">**MpHandleClose**</span><span class="sxs-lookup"><span data-stu-id="e56d3-198">**MpHandleClose**</span></span>](mphandleclose.md)
</dt> <dt>

[<span data-ttu-id="e56d3-199">**MpManagerOpen**</span><span class="sxs-lookup"><span data-stu-id="e56d3-199">**MpManagerOpen**</span></span>](mpmanageropen.md)
</dt> <dt>

[<span data-ttu-id="e56d3-200">**dados do MPCALLBACK \_**</span><span class="sxs-lookup"><span data-stu-id="e56d3-200">**MPCALLBACK\_DATA**</span></span>](mpcallback-data.md)
</dt> <dt>

[<span data-ttu-id="e56d3-201">**dados do MPSIGUPDATE \_**</span><span class="sxs-lookup"><span data-stu-id="e56d3-201">**MPSIGUPDATE\_DATA**</span></span>](mpsigupdate-data.md)
</dt> </dl>

 

 





