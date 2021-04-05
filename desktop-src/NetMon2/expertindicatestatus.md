---
description: A função ExpertIndicateStatus indica a porcentagem de conclusão da análise de especialistas do arquivo de captura.
ms.assetid: 6dbaa6d3-6068-4a28-9d9f-bcc7a25da407
title: Função ExpertIndicateStatus (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertIndicateStatus
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: ac707a774b667b96a4d612e9eaf7da2c779c0327
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089974"
---
# <a name="expertindicatestatus-function"></a><span data-ttu-id="38e51-103">Função ExpertIndicateStatus</span><span class="sxs-lookup"><span data-stu-id="38e51-103">ExpertIndicateStatus function</span></span>

<span data-ttu-id="38e51-104">A função **ExpertIndicateStatus** indica a porcentagem de conclusão da análise do especialista do arquivo de captura.</span><span class="sxs-lookup"><span data-stu-id="38e51-104">The **ExpertIndicateStatus** function indicates the percentage of completion of the expert's analysis of the capture file.</span></span>

## <a name="syntax"></a><span data-ttu-id="38e51-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="38e51-105">Syntax</span></span>


```C++
DWORD WINAPI ExpertIndicateStatus(
  _In_  HEXPERTKEY              hExpertKey,
  _In_  EXPERTSTATUSENUMERATION Status,
  _In_  DWORD                   SubStatus,
  _In_  char                    *sztext,
  _Out_ long                    PercentDone
);
```



## <a name="parameters"></a><span data-ttu-id="38e51-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="38e51-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38e51-107">*hExpertKey* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="38e51-107">*hExpertKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38e51-108">Identificador de especialista exclusivo.</span><span class="sxs-lookup"><span data-stu-id="38e51-108">Unique expert identifier.</span></span> <span data-ttu-id="38e51-109">Monitor de Rede passa *hExpertKey* para o especialista ao chamar a função [Run](run.md) .</span><span class="sxs-lookup"><span data-stu-id="38e51-109">Network Monitor passes *hExpertKey* to the expert when it calls the [Run](run.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="38e51-110">*Status* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="38e51-110">*Status* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38e51-111">Status atual da análise.</span><span class="sxs-lookup"><span data-stu-id="38e51-111">Current status of the analysis.</span></span> <span data-ttu-id="38e51-112">Especifique um dos seguintes valores de [EXPERTSTATUSENUMERATION](expertstatusenumeration.md) .</span><span class="sxs-lookup"><span data-stu-id="38e51-112">Specify one of the following [EXPERTSTATUSENUMERATION](expertstatusenumeration.md) values.</span></span>



| <span data-ttu-id="38e51-113">Valor</span><span class="sxs-lookup"><span data-stu-id="38e51-113">Value</span></span>                                                                                                                                                                                 | <span data-ttu-id="38e51-114">Significado</span><span class="sxs-lookup"><span data-stu-id="38e51-114">Meaning</span></span>                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <span id="EXPERTSTATUS_INACTIVE"></span><span id="expertstatus_inactive"></span><dl> <span data-ttu-id="38e51-115"><dt>**EXPERTSTATUS \_ INativo**</dt></span><span class="sxs-lookup"><span data-stu-id="38e51-115"><dt>**EXPERTSTATUS\_INACTIVE**</dt></span></span> </dl> | <span data-ttu-id="38e51-116">O especialista nunca começou.</span><span class="sxs-lookup"><span data-stu-id="38e51-116">The expert never started.</span></span> <br/>                                          |
| <span id="EXPERTSTATUS_STARTING"></span><span id="expertstatus_starting"></span><dl> <span data-ttu-id="38e51-117"><dt>**EXPERTSTATUS \_ iniciando**</dt></span><span class="sxs-lookup"><span data-stu-id="38e51-117"><dt>**EXPERTSTATUS\_STARTING**</dt></span></span> </dl> | <span data-ttu-id="38e51-118">O especialista está sendo iniciado.</span><span class="sxs-lookup"><span data-stu-id="38e51-118">The expert is starting.</span></span> <br/>                                            |
| <span id="EXPERTSTATUS_RUNNING"></span><span id="expertstatus_running"></span><dl> <span data-ttu-id="38e51-119"><dt>**EXPERTSTATUS \_ em execução**</dt></span><span class="sxs-lookup"><span data-stu-id="38e51-119"><dt>**EXPERTSTATUS\_RUNNING**</dt></span></span> </dl>    | <span data-ttu-id="38e51-120">O especialista está em execução normalmente.</span><span class="sxs-lookup"><span data-stu-id="38e51-120">The expert is running normally.</span></span> <br/>                                    |
| <span id="EXPERTSTATUS_PROBLEM"></span><span id="expertstatus_problem"></span><dl> <span data-ttu-id="38e51-121"><dt>**problema de EXPERTSTATUS \_**</dt></span><span class="sxs-lookup"><span data-stu-id="38e51-121"><dt>**EXPERTSTATUS\_PROBLEM**</dt></span></span> </dl>    | <span data-ttu-id="38e51-122">Um problema especificado no parâmetro substatus interrompeu o especialista.</span><span class="sxs-lookup"><span data-stu-id="38e51-122">A problem specified in the SubStatus parameter stopped the expert.</span></span> <br/> |
| <span id="EXPERTSTATUS_ABORTED"></span><span id="expertstatus_aborted"></span><dl> <span data-ttu-id="38e51-123"><dt>**EXPERTSTATUS \_ anulado**</dt></span><span class="sxs-lookup"><span data-stu-id="38e51-123"><dt>**EXPERTSTATUS\_ABORTED**</dt></span></span> </dl>    | <span data-ttu-id="38e51-124">Monitor de Rede parou o especialista.</span><span class="sxs-lookup"><span data-stu-id="38e51-124">Network Monitor stopped the expert.</span></span> <br/>                                |
| <span id="EXPERTSTATUS_DONE"></span><span id="expertstatus_done"></span><dl> <span data-ttu-id="38e51-125"><dt>**EXPERTSTATUS \_ concluído**</dt></span><span class="sxs-lookup"><span data-stu-id="38e51-125"><dt>**EXPERTSTATUS\_DONE**</dt></span></span> </dl>             | <span data-ttu-id="38e51-126">O especialista concluiu a análise com êxito.</span><span class="sxs-lookup"><span data-stu-id="38e51-126">The expert finished the analysis successfully.</span></span> <br/>                     |



 

</dd> <dt>

<span data-ttu-id="38e51-127">*Substatus* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="38e51-127">*SubStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38e51-128">Extensão ou esclarecimento das informações fornecidas pelo parâmetro *status* .</span><span class="sxs-lookup"><span data-stu-id="38e51-128">Extension or clarification of information provided by the *Status* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="38e51-129">*szText* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="38e51-129">*sztext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38e51-130">Indicador de status de texto opcional.</span><span class="sxs-lookup"><span data-stu-id="38e51-130">Optional text status indicator.</span></span>

<span data-ttu-id="38e51-131">Esse valor de parâmetro pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="38e51-131">This parameter value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="38e51-132">*PercentDone* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="38e51-132">*PercentDone* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="38e51-133">Porcentagem dos dados de captura que o especialista processou.</span><span class="sxs-lookup"><span data-stu-id="38e51-133">Percentage of the capture data that the expert has processed.</span></span>

<span data-ttu-id="38e51-134">Quando o especialista conclui com êxito a análise de um arquivo de captura, o sistema define o percentual como 100.</span><span class="sxs-lookup"><span data-stu-id="38e51-134">When the expert successfully completes analysis of a capture file, the system sets the percentage to 100.</span></span> <span data-ttu-id="38e51-135">Qualquer número maior que 99 será ignorado.</span><span class="sxs-lookup"><span data-stu-id="38e51-135">Any number greater than 99 will be ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38e51-136">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="38e51-136">Return value</span></span>

<span data-ttu-id="38e51-137">Se a função for bem-sucedida, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="38e51-137">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="38e51-138">Se a função não for bem-sucedida, o valor de retorno será NMERR \_ especialista \_ . o especialista deverá limpar e retornar imediatamente sem concluir a captura.</span><span class="sxs-lookup"><span data-stu-id="38e51-138">If the function is unsuccessful, the return value is NMERR\_EXPERT\_TERMINATE; the expert must immediately clean up and return without completing the capture.</span></span>

## <a name="remarks"></a><span data-ttu-id="38e51-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="38e51-139">Remarks</span></span>

<span data-ttu-id="38e51-140">A função **ExpertIndicateStatus** só pode ser chamada por especialistas que implementam a função [executar](run.md) ou [Configurar](configure.md) exportação.</span><span class="sxs-lookup"><span data-stu-id="38e51-140">The **ExpertIndicateStatus** function can only be called by experts that implement the [Run](run.md) or [Configure](configure.md) export function.</span></span>

## <a name="requirements"></a><span data-ttu-id="38e51-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="38e51-141">Requirements</span></span>



| <span data-ttu-id="38e51-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="38e51-142">Requirement</span></span> | <span data-ttu-id="38e51-143">Valor</span><span class="sxs-lookup"><span data-stu-id="38e51-143">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="38e51-144">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="38e51-144">Minimum supported client</span></span><br/> | <span data-ttu-id="38e51-145">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="38e51-145">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="38e51-146">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="38e51-146">Minimum supported server</span></span><br/> | <span data-ttu-id="38e51-147">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="38e51-147">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="38e51-148">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="38e51-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="38e51-149"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="38e51-149"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="38e51-150">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="38e51-150">Library</span></span><br/>                  | <dl> <span data-ttu-id="38e51-151"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="38e51-151"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="38e51-152">DLL</span><span class="sxs-lookup"><span data-stu-id="38e51-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="38e51-153"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="38e51-153"><dt>Nmapi.dll</dt></span></span> </dl> |
