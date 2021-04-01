---
title: Função MpScanStart (MpClient. h)
description: Inicia uma operação de verificação.
ms.assetid: 3AF147C8-A41F-4193-AE28-72C1FBD18BA2
keywords:
- Recursos do ambiente Windows herdado da função MpScanStart
topic_type:
- apiref
api_name:
- MpScanStart
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d343787edc85a18dc7471d19165999a7252d18a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918716"
---
# <a name="mpscanstart-function"></a><span data-ttu-id="16e10-104">Função MpScanStart</span><span class="sxs-lookup"><span data-stu-id="16e10-104">MpScanStart function</span></span>

<span data-ttu-id="16e10-105">Inicia uma operação de verificação.</span><span class="sxs-lookup"><span data-stu-id="16e10-105">Starts a scanning operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="16e10-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="16e10-106">Syntax</span></span>


```C++
HRESULT WINAPI MpScanStart(
  _In_     MPHANDLE          hMpHandle,
  _In_     MPSCAN_TYPE       ScanType,
  _In_     DWORD             dwScanOptions,
  _In_opt_ PMPSCAN_RESOURCES pScanResources,
  _In_opt_ PMPCALLBACK_INFO  pCallbackInfo,
  _Out_    PMPHANDLE         phScanHandle
);
```



## <a name="parameters"></a><span data-ttu-id="16e10-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="16e10-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16e10-108">*hMpHandle* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="16e10-108">*hMpHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16e10-109">Tipo: **MPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="16e10-109">Type: **MPHANDLE**</span></span>

<span data-ttu-id="16e10-110">Identificador para a interface do Malware Protection Manager.</span><span class="sxs-lookup"><span data-stu-id="16e10-110">Handle to the malware protection manager interface.</span></span> <span data-ttu-id="16e10-111">Esse identificador é retornado pela função [**MpManagerOpen**](mpmanageropen.md) .</span><span class="sxs-lookup"><span data-stu-id="16e10-111">This handle is returned by the [**MpManagerOpen**](mpmanageropen.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="16e10-112">*Examinartype* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="16e10-112">*ScanType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16e10-113">Tipo: **[ **\_ tipo de MPSCAN**](mpscan-type.md)**</span><span class="sxs-lookup"><span data-stu-id="16e10-113">Type: **[**MPSCAN\_TYPE**](mpscan-type.md)**</span></span>

<span data-ttu-id="16e10-114">Especifica o tipo de verificação.</span><span class="sxs-lookup"><span data-stu-id="16e10-114">Specifies the type of scan.</span></span> <span data-ttu-id="16e10-115">Esse parâmetro deve ser um dos membros do [**\_ tipo MPSCAN**](mpscan-type.md) enueration.</span><span class="sxs-lookup"><span data-stu-id="16e10-115">This parameter must be one of the members of the [**MPSCAN\_TYPE**](mpscan-type.md) enueration.</span></span>

</dd> <dt>

<span data-ttu-id="16e10-116">*dwScanOptions* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="16e10-116">*dwScanOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16e10-117">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="16e10-117">Type: **DWORD**</span></span>

<span data-ttu-id="16e10-118">Especifica várias opções para a operação de verificação.</span><span class="sxs-lookup"><span data-stu-id="16e10-118">Specifies various options for scanning operation.</span></span>



| <span data-ttu-id="16e10-119">Valor</span><span class="sxs-lookup"><span data-stu-id="16e10-119">Value</span></span>                                                                                                                                                                                                       | <span data-ttu-id="16e10-120">Significado</span><span class="sxs-lookup"><span data-stu-id="16e10-120">Meaning</span></span>                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MPSCAN_OPTION_NONE"></span><span id="mpscan_option_none"></span><dl> <span data-ttu-id="16e10-121"><dt>**\_opção MPSCAN \_ None**</dt></span><span class="sxs-lookup"><span data-stu-id="16e10-121"><dt>**MPSCAN\_OPTION\_NONE**</dt></span></span> </dl>                               | <span data-ttu-id="16e10-122">Nenhuma opção específica é solicitada.</span><span class="sxs-lookup"><span data-stu-id="16e10-122">No specific option is requested.</span></span><br/>                                                                                                                                                                                                                           |
| <span id="MPSCAN_OPTION_ASYNC"></span><span id="mpscan_option_async"></span><dl> <span data-ttu-id="16e10-123"><dt>**\_opção MPSCAN \_ Async**</dt></span><span class="sxs-lookup"><span data-stu-id="16e10-123"><dt>**MPSCAN\_OPTION\_ASYNC**</dt></span></span> </dl>                            | <span data-ttu-id="16e10-124">A operação de verificação é assíncrona, em que **MpScanStart** retorna imediatamente após o início bem-sucedido da verificação.</span><span class="sxs-lookup"><span data-stu-id="16e10-124">The scan operation is to be asynchronous, where **MpScanStart** returns immediately after the successful initiation of scanning.</span></span> <span data-ttu-id="16e10-125">(Por padrão, a operação de verificação é síncrona, o que significa que **MpScanStart** retornará somente depois que a verificação for concluída.)</span><span class="sxs-lookup"><span data-stu-id="16e10-125">(By default the scan operation is synchronous, meaning **MpScanStart** will return only after the scan is finished.)</span></span><br/>      |
| <span id="MPSCAN_OPTION_PROGRESS"></span><span id="mpscan_option_progress"></span><dl> <span data-ttu-id="16e10-126"><dt>**\_progresso da opção MPSCAN \_**</dt></span><span class="sxs-lookup"><span data-stu-id="16e10-126"><dt>**MPSCAN\_OPTION\_PROGRESS**</dt></span></span> </dl>                   | <span data-ttu-id="16e10-127">O chamador está interessado em receber informações de progresso da verificação por meio de um retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="16e10-127">The caller is interested in receiving scan progress information via a callback.</span></span><br/>                                                                                                                                                                            |
| <span id="MPSCAN_OPTION_LOWPRIORITY"></span><span id="mpscan_option_lowpriority"></span><dl> <span data-ttu-id="16e10-128"><dt>**MPSCAN \_ opção \_ LOWPRIORITY**</dt></span><span class="sxs-lookup"><span data-stu-id="16e10-128"><dt>**MPSCAN\_OPTION\_LOWPRIORITY**</dt></span></span> </dl>          | <span data-ttu-id="16e10-129">Execute a verificação com baixa prioridade.</span><span class="sxs-lookup"><span data-stu-id="16e10-129">Perform the scan with low priority.</span></span> <span data-ttu-id="16e10-130">(Por padrão, a operação de verificação é executada com prioridade normal.)</span><span class="sxs-lookup"><span data-stu-id="16e10-130">(By default the scan operation is performed with normal priority.)</span></span><br/>                                                                                                                                                     |
| <span id="MPSCAN_OPTION_PACKEDEXES"></span><span id="mpscan_option_packedexes"></span><dl> <span data-ttu-id="16e10-131"><dt>**MPSCAN \_ opção \_ PACKEDEXES**</dt></span><span class="sxs-lookup"><span data-stu-id="16e10-131"><dt>**MPSCAN\_OPTION\_PACKEDEXES**</dt></span></span> </dl>             | <span data-ttu-id="16e10-132">Examine os executáveis empacotados para possíveis ameaças.</span><span class="sxs-lookup"><span data-stu-id="16e10-132">Scan packed executables for possible threats.</span></span><br/>                                                                                                                                                                                                              |
| <span id="MPSCAN_OPTION_ARCHIVES"></span><span id="mpscan_option_archives"></span><dl> <span data-ttu-id="16e10-133"><dt>**\_arquivos mortos de opção MPSCAN \_**</dt></span><span class="sxs-lookup"><span data-stu-id="16e10-133"><dt>**MPSCAN\_OPTION\_ARCHIVES**</dt></span></span> </dl>                   | <span data-ttu-id="16e10-134">Examinar o conteúdo do arquivo para possíveis ameaças.</span><span class="sxs-lookup"><span data-stu-id="16e10-134">Scan archive contents for possible threats.</span></span> <span data-ttu-id="16e10-135">Arquivos com extensões como. zip,. cab ou. tar.</span><span class="sxs-lookup"><span data-stu-id="16e10-135">Archives are files with extensions such as .zip, .cab, or .tar.</span></span><br/>                                                                                                                                                |
| <span id="MPSCAN_OPTION_HEURISTICS"></span><span id="mpscan_option_heuristics"></span><dl> <span data-ttu-id="16e10-136"><dt>**\_heurística da opção MPSCAN \_**</dt></span><span class="sxs-lookup"><span data-stu-id="16e10-136"><dt>**MPSCAN\_OPTION\_HEURISTICS**</dt></span></span> </dl>             | <span data-ttu-id="16e10-137">Habilite a verificação baseada em heurística.</span><span class="sxs-lookup"><span data-stu-id="16e10-137">Enable heuristics-based scanning.</span></span> <span data-ttu-id="16e10-138">Isso verificará se há ameaças com o tipo de detecção definido como heurística.</span><span class="sxs-lookup"><span data-stu-id="16e10-138">This will scan for threats with detection type set to heuristics.</span></span><br/>                                                                                                                                                        |
| <span id="MPSCAN_OPTION_REPORTFRIENDLY"></span><span id="mpscan_option_reportfriendly"></span><dl> <span data-ttu-id="16e10-139"><dt>**MPSCAN \_ opção \_ REPORTFRIENDLY**</dt></span><span class="sxs-lookup"><span data-stu-id="16e10-139"><dt>**MPSCAN\_OPTION\_REPORTFRIENDLY**</dt></span></span> </dl> | <span data-ttu-id="16e10-140">Relatar itens amigáveis em uma verificação de recurso.</span><span class="sxs-lookup"><span data-stu-id="16e10-140">Report friendly items in a resource scan.</span></span> <span data-ttu-id="16e10-141">Isso se destina somente ao uso interno.</span><span class="sxs-lookup"><span data-stu-id="16e10-141">This is intended for internal use only.</span></span><br/>                                                                                                                                                                          |
| <span id="MPSCAN_OPTION_REPORTUNKNOWN"></span><span id="mpscan_option_reportunknown"></span><dl> <span data-ttu-id="16e10-142"><dt>**MPSCAN \_ opção \_ REPORTUNKNOWN**</dt></span><span class="sxs-lookup"><span data-stu-id="16e10-142"><dt>**MPSCAN\_OPTION\_REPORTUNKNOWN**</dt></span></span> </dl>    | <span data-ttu-id="16e10-143">Relatar itens desconhecidos em uma verificação de recurso.</span><span class="sxs-lookup"><span data-stu-id="16e10-143">Report unknown items in a resource scan.</span></span> <span data-ttu-id="16e10-144">Isso se destina somente ao uso interno.</span><span class="sxs-lookup"><span data-stu-id="16e10-144">This is intended for internal use only.</span></span><br/>                                                                                                                                                                           |
| <span id="MPSCAN_OPTION_NOCONSOLIDATE"></span><span id="mpscan_option_noconsolidate"></span><dl> <span data-ttu-id="16e10-145"><dt>**\_opção MPSCAN \_ noconsolidate**</dt></span><span class="sxs-lookup"><span data-stu-id="16e10-145"><dt>**MPSCAN\_OPTION\_NOCONSOLIDATE**</dt></span></span> </dl>    | <span data-ttu-id="16e10-146">Não consolide os resultados da verificação com a exibição de ameaça global.</span><span class="sxs-lookup"><span data-stu-id="16e10-146">Do not consolidate scan results with global threat view.</span></span> <span data-ttu-id="16e10-147">Isso é útil para um cliente (como um cliente de email) que deseja controlar a experiência de limpeza por si só, em vez de permitir a experiência de limpeza Antimalware padrão.</span><span class="sxs-lookup"><span data-stu-id="16e10-147">This is useful for a client (such as an email client) which wants to control cleaning UX by itself rather than allowing default anti-malware cleaning UX.</span></span> <span data-ttu-id="16e10-148">Isso se destina somente ao uso interno.</span><span class="sxs-lookup"><span data-stu-id="16e10-148">This is intended for internal use only.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="16e10-149">*pScanResources* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="16e10-149">*pScanResources* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="16e10-150">Tipo: **\_ recursos de PMPSCAN**</span><span class="sxs-lookup"><span data-stu-id="16e10-150">Type: **PMPSCAN\_RESOURCES**</span></span>

<span data-ttu-id="16e10-151">Um ponteiro para as informações do recurso de verificação.</span><span class="sxs-lookup"><span data-stu-id="16e10-151">A pointer to the scan resource information.</span></span> <span data-ttu-id="16e10-152">Esse parâmetro deve ser **nulo** para uma verificação rápida.</span><span class="sxs-lookup"><span data-stu-id="16e10-152">This parameter must be **NULL** for a quick scan.</span></span> <span data-ttu-id="16e10-153">Esse é um parâmetro opcional para uma verificação completa.</span><span class="sxs-lookup"><span data-stu-id="16e10-153">This is an optional parameter for a full scan.</span></span> <span data-ttu-id="16e10-154">Para uma verificação de recurso, esse parâmetro deve ser especificado com pelo menos uma estrutura de informações de recurso.</span><span class="sxs-lookup"><span data-stu-id="16e10-154">For a resource scan this parameter must be specified with at least one resource information structure.</span></span> <span data-ttu-id="16e10-155">Para verificar recursos específicos, o chamador deve ter a permissão de **\_ leitura genérica** para o recurso.</span><span class="sxs-lookup"><span data-stu-id="16e10-155">To scan specific resources the caller must have **GENERIC\_READ** permission for the resource.</span></span> <span data-ttu-id="16e10-156">Consulte [**\_ recursos do MPSCAN**](mpscan-resources.md).</span><span class="sxs-lookup"><span data-stu-id="16e10-156">See [**MPSCAN\_RESOURCES**](mpscan-resources.md).</span></span>

</dd> <dt>

<span data-ttu-id="16e10-157">*pCallbackInfo* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="16e10-157">*pCallbackInfo* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="16e10-158">Tipo: **\_ informações de PMPCALLBACK**</span><span class="sxs-lookup"><span data-stu-id="16e10-158">Type: **PMPCALLBACK\_INFO**</span></span>

<span data-ttu-id="16e10-159">Um ponteiro para as informações de retorno de chamada usadas para alimentar o cliente com alterações de estado de verificação (como iniciar e concluir) e informações de progresso.</span><span class="sxs-lookup"><span data-stu-id="16e10-159">A pointer to the callback information used to feed the client with scan state changes (such as start and complete) and progress information.</span></span> <span data-ttu-id="16e10-160">Os [**\_ dados de MPCALLBACK**](mpcallback-data.md) passados na função de retorno de chamada relatam o estado de verificação real e as informações relacionadas ao progresso.</span><span class="sxs-lookup"><span data-stu-id="16e10-160">The [**MPCALLBACK\_DATA**](mpcallback-data.md) passed back in the callback function reports actual scan state and progress-related information.</span></span> <span data-ttu-id="16e10-161">Veja a seguir uma lista de possíveis retornos de chamada:</span><span class="sxs-lookup"><span data-stu-id="16e10-161">The following is a list of possible callbacks:</span></span>



| <span data-ttu-id="16e10-162">Valor</span><span class="sxs-lookup"><span data-stu-id="16e10-162">Value</span></span>                                                                                                                                                                                                       | <span data-ttu-id="16e10-163">Significado</span><span class="sxs-lookup"><span data-stu-id="16e10-163">Meaning</span></span>                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MPNOTIFY_SCAN_START"></span><span id="mpnotify_scan_start"></span><dl> <span data-ttu-id="16e10-164"><dt>**\_início da verificação de mpnotify \_**</dt></span><span class="sxs-lookup"><span data-stu-id="16e10-164"><dt>**MPNOTIFY\_SCAN\_START**</dt></span></span> </dl>                            | <span data-ttu-id="16e10-165">Operação de verificação iniciada.</span><span class="sxs-lookup"><span data-stu-id="16e10-165">Scan operation started.</span></span><br/>                                                                                                                                                                                                                                                                                       |
| <span id="MPNOTIFY_SCAN_COMPLETE"></span><span id="mpnotify_scan_complete"></span><dl> <span data-ttu-id="16e10-166"><dt>**verificação de MPNOTIFY \_ \_ concluída**</dt></span><span class="sxs-lookup"><span data-stu-id="16e10-166"><dt>**MPNOTIFY\_SCAN\_COMPLETE**</dt></span></span> </dl>                   | <span data-ttu-id="16e10-167">Operação de verificação concluída.</span><span class="sxs-lookup"><span data-stu-id="16e10-167">Scan operation completed.</span></span> <span data-ttu-id="16e10-168">Informações adicionais estão disponíveis por meio da estrutura de [**\_ dados MPSCAN**](mpscan-data.md) .</span><span class="sxs-lookup"><span data-stu-id="16e10-168">Additional information is available via [**MPSCAN\_DATA**](mpscan-data.md) structure.</span></span><br/>                                                                                                                                                                                              |
| <span id="MPNOTIFY_SCAN_PAUSED"></span><span id="mpnotify_scan_paused"></span><dl> <span data-ttu-id="16e10-169"><dt>**verificação de MPNOTIFY \_ \_ pausada**</dt></span><span class="sxs-lookup"><span data-stu-id="16e10-169"><dt>**MPNOTIFY\_SCAN\_PAUSED**</dt></span></span> </dl>                         | <span data-ttu-id="16e10-170">A operação de verificação está em pausa.</span><span class="sxs-lookup"><span data-stu-id="16e10-170">Scan operation is paused.</span></span><br/>                                                                                                                                                                                                                                                                                     |
| <span id="MPNOTIFY_SCAN_RESUMED"></span><span id="mpnotify_scan_resumed"></span><dl> <span data-ttu-id="16e10-171"><dt>**verificação do MPNOTIFY \_ \_ retomada**</dt></span><span class="sxs-lookup"><span data-stu-id="16e10-171"><dt>**MPNOTIFY\_SCAN\_RESUMED**</dt></span></span> </dl>                      | <span data-ttu-id="16e10-172">A operação de verificação foi retomada da pausa.</span><span class="sxs-lookup"><span data-stu-id="16e10-172">Scan operation resumed from pause.</span></span><br/>                                                                                                                                                                                                                                                                            |
| <span id="MPNOTIFY_SCAN_CANCEL"></span><span id="mpnotify_scan_cancel"></span><dl> <span data-ttu-id="16e10-173"><dt>**MPNOTIFY de \_ verificação \_ cancelada**</dt></span><span class="sxs-lookup"><span data-stu-id="16e10-173"><dt>**MPNOTIFY\_SCAN\_CANCEL**</dt></span></span> </dl>                         | <span data-ttu-id="16e10-174">A operação de verificação foi cancelada.</span><span class="sxs-lookup"><span data-stu-id="16e10-174">Scan operation was cancelled.</span></span><br/>                                                                                                                                                                                                                                                                                 |
| <span id="MPNOTIFY_SCAN_PROGRESS"></span><span id="mpnotify_scan_progress"></span><dl> <span data-ttu-id="16e10-175"><dt>**\_progresso da verificação de mpnotify \_**</dt></span><span class="sxs-lookup"><span data-stu-id="16e10-175"><dt>**MPNOTIFY\_SCAN\_PROGRESS**</dt></span></span> </dl>                   | <span data-ttu-id="16e10-176">Informações de progresso da verificação.</span><span class="sxs-lookup"><span data-stu-id="16e10-176">Scan progress information.</span></span> <span data-ttu-id="16e10-177">Informações adicionais (como estatísticas de recursos) estão disponíveis por meio da estrutura de [**\_ dados MPSCAN**](mpscan-data.md) .</span><span class="sxs-lookup"><span data-stu-id="16e10-177">Additional information (such as resource statistics) is available via [**MPSCAN\_DATA**](mpscan-data.md) structure.</span></span><br/>                                                                                                                                                               |
| <span id="MPNOTIFY_SCAN_ERROR"></span><span id="mpnotify_scan_error"></span><dl> <span data-ttu-id="16e10-178"><dt>**\_erro de verificação de mpnotify \_**</dt></span><span class="sxs-lookup"><span data-stu-id="16e10-178"><dt>**MPNOTIFY\_SCAN\_ERROR**</dt></span></span> </dl>                            | <span data-ttu-id="16e10-179">Verificar informações de erro de um recurso específico.</span><span class="sxs-lookup"><span data-stu-id="16e10-179">Scan error information for a specific resource.</span></span> <span data-ttu-id="16e10-180">As informações específicas do recurso estão disponíveis por meio da estrutura de [**\_ dados do MPSCAN**](mpscan-data.md) .</span><span class="sxs-lookup"><span data-stu-id="16e10-180">The specific resource information is available via [**MPSCAN\_DATA**](mpscan-data.md) structure.</span></span><br/>                                                                                                                                                             |
| <span id="MPNOTIFY_SCAN_INFECTED"></span><span id="mpnotify_scan_infected"></span><dl> <span data-ttu-id="16e10-181"><dt>**verificação de MPNOTIFY \_ \_ infectada**</dt></span><span class="sxs-lookup"><span data-stu-id="16e10-181"><dt>**MPNOTIFY\_SCAN\_INFECTED**</dt></span></span> </dl>                   | <span data-ttu-id="16e10-182">A verificação encontrou um recurso infectado.</span><span class="sxs-lookup"><span data-stu-id="16e10-182">Scan found an infected resource.</span></span> <span data-ttu-id="16e10-183">Observe que, na maioria dos casos, isso resultará em alguma ameaça relatada no final da verificação.</span><span class="sxs-lookup"><span data-stu-id="16e10-183">Note that in most of the cases this will result in some threat reported at the end of the scan.</span></span> <span data-ttu-id="16e10-184">Às vezes, ele não pode materializar como uma ameaça devido a exclusões.</span><span class="sxs-lookup"><span data-stu-id="16e10-184">Sometimes it may not materialize as a threat because of exclusions.</span></span> <span data-ttu-id="16e10-185">Informações adicionais sobre recursos infectados estão disponíveis por meio da estrutura de [**\_ dados do MPSCAN**](mpscan-data.md) .</span><span class="sxs-lookup"><span data-stu-id="16e10-185">Additional infected resource information is available via [**MPSCAN\_DATA**](mpscan-data.md) structure.</span></span><br/> |
| <span id="MPNOTIFY_SCAN_MEMORYSTART"></span><span id="mpnotify_scan_memorystart"></span><dl> <span data-ttu-id="16e10-186"><dt>**MPNOTIFY \_ Scan \_ MEMORYSTART**</dt></span><span class="sxs-lookup"><span data-stu-id="16e10-186"><dt>**MPNOTIFY\_SCAN\_MEMORYSTART**</dt></span></span> </dl>          | <span data-ttu-id="16e10-187">A parte de verificação rápida da verificação completa foi iniciada.</span><span class="sxs-lookup"><span data-stu-id="16e10-187">Quick scan portion of the full scan has started.</span></span><br/>                                                                                                                                                                                                                                                              |
| <span id="MPNOTIFY_SCAN_MEMORYCOMPLETE"></span><span id="mpnotify_scan_memorycomplete"></span><dl> <span data-ttu-id="16e10-188"><dt>**MPNOTIFY \_ Scan \_ MEMORYCOMPLETE**</dt></span><span class="sxs-lookup"><span data-stu-id="16e10-188"><dt>**MPNOTIFY\_SCAN\_MEMORYCOMPLETE**</dt></span></span> </dl> | <span data-ttu-id="16e10-189">A parte de verificação rápida da verificação completa foi concluída.</span><span class="sxs-lookup"><span data-stu-id="16e10-189">Quick scan portion of the full scan has completed.</span></span><br/>                                                                                                                                                                                                                                                            |
| <span id="MPNOTIFY_INTERNAL_FAILURE"></span><span id="mpnotify_internal_failure"></span><dl> <span data-ttu-id="16e10-190"><dt>**\_falha interna do mpnotify \_**</dt></span><span class="sxs-lookup"><span data-stu-id="16e10-190"><dt>**MPNOTIFY\_INTERNAL\_FAILURE**</dt></span></span> </dl>          | <span data-ttu-id="16e10-191">A operação de verificação encontrou uma falha genérica.</span><span class="sxs-lookup"><span data-stu-id="16e10-191">Scan operation has encountered a generic failure.</span></span> <span data-ttu-id="16e10-192">O *HRESULT* nos [**\_ dados MPCALLBACK**](mpcallback-data.md) tem o código de erro específico.</span><span class="sxs-lookup"><span data-stu-id="16e10-192">The *hResult* in [**MPCALLBACK\_DATA**](mpcallback-data.md) has the specific error code.</span></span><br/>                                                                                                                                                                   |



 

</dd> <dt>

<span data-ttu-id="16e10-193">*phScanHandle* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="16e10-193">*phScanHandle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="16e10-194">Tipo: **PMPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="16e10-194">Type: **PMPHANDLE**</span></span>

<span data-ttu-id="16e10-195">O identificador de verificação retornado que identifica a verificação iniciada no momento.</span><span class="sxs-lookup"><span data-stu-id="16e10-195">Returned scan handle which identifies the currently initiated scan.</span></span> <span data-ttu-id="16e10-196">Esse identificador pode ser usado em chamadas de função subsequentes, como para recuperar um resultado de verificação.</span><span class="sxs-lookup"><span data-stu-id="16e10-196">This handle can be used in subsequent function calls, such as to retrieve a scan result.</span></span> <span data-ttu-id="16e10-197">O identificador deve ser fechado com a função [**MpHandleClose**](mphandleclose.md) .</span><span class="sxs-lookup"><span data-stu-id="16e10-197">The handle must be closed with the [**MpHandleClose**](mphandleclose.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16e10-198">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="16e10-198">Return value</span></span>

<span data-ttu-id="16e10-199">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="16e10-199">Type: **HRESULT**</span></span>

<span data-ttu-id="16e10-200">Se a função for bem sucedido, o valor de retorno será **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="16e10-200">If the function succeeds the return value is **S\_OK**.</span></span>

<span data-ttu-id="16e10-201">Se a função falhar, o valor de retorno será um código **HRESULT** com falha.</span><span class="sxs-lookup"><span data-stu-id="16e10-201">If the function fails then the return value is a failed **HRESULT** code.</span></span> <span data-ttu-id="16e10-202">O chamador pode usar a função [**MpErrorMessageFormat**](mperrormessageformat.md) para obter uma descrição genérica da mensagem de erro.</span><span class="sxs-lookup"><span data-stu-id="16e10-202">The caller can use the [**MpErrorMessageFormat**](mperrormessageformat.md) function to get a generic description of the error message.</span></span>

## <a name="requirements"></a><span data-ttu-id="16e10-203">Requisitos</span><span class="sxs-lookup"><span data-stu-id="16e10-203">Requirements</span></span>



| <span data-ttu-id="16e10-204">Requisito</span><span class="sxs-lookup"><span data-stu-id="16e10-204">Requirement</span></span> | <span data-ttu-id="16e10-205">Valor</span><span class="sxs-lookup"><span data-stu-id="16e10-205">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="16e10-206">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="16e10-206">Minimum supported client</span></span><br/> | <span data-ttu-id="16e10-207">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="16e10-207">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="16e10-208">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="16e10-208">Minimum supported server</span></span><br/> | <span data-ttu-id="16e10-209">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="16e10-209">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="16e10-210">parâmetro</span><span class="sxs-lookup"><span data-stu-id="16e10-210">Header</span></span><br/>                   | <dl> <span data-ttu-id="16e10-211"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="16e10-211"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="16e10-212">DLL</span><span class="sxs-lookup"><span data-stu-id="16e10-212">DLL</span></span><br/>                      | <dl> <span data-ttu-id="16e10-213"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="16e10-213"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16e10-214">Confira também</span><span class="sxs-lookup"><span data-stu-id="16e10-214">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16e10-215">**MpErrorMessageFormat**</span><span class="sxs-lookup"><span data-stu-id="16e10-215">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="16e10-216">**MpHandleClose**</span><span class="sxs-lookup"><span data-stu-id="16e10-216">**MpHandleClose**</span></span>](mphandleclose.md)
</dt> <dt>

[<span data-ttu-id="16e10-217">**MpManagerOpen**</span><span class="sxs-lookup"><span data-stu-id="16e10-217">**MpManagerOpen**</span></span>](mpmanageropen.md)
</dt> <dt>

[<span data-ttu-id="16e10-218">**dados do MPCALLBACK \_**</span><span class="sxs-lookup"><span data-stu-id="16e10-218">**MPCALLBACK\_DATA**</span></span>](mpcallback-data.md)
</dt> <dt>

[<span data-ttu-id="16e10-219">**dados do MPSCAN \_**</span><span class="sxs-lookup"><span data-stu-id="16e10-219">**MPSCAN\_DATA**</span></span>](mpscan-data.md)
</dt> <dt>

[<span data-ttu-id="16e10-220">**recursos do MPSCAN \_**</span><span class="sxs-lookup"><span data-stu-id="16e10-220">**MPSCAN\_RESOURCES**</span></span>](mpscan-resources.md)
</dt> <dt>

[<span data-ttu-id="16e10-221">**tipo de MPSCAN \_**</span><span class="sxs-lookup"><span data-stu-id="16e10-221">**MPSCAN\_TYPE**</span></span>](mpscan-type.md)
</dt> </dl>

 

 





