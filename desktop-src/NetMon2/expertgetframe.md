---
description: Retorna o quadro solicitado de uma captura carregada.
ms.assetid: efd1cff5-a3a1-4910-b003-25b6e10dad6e
title: Função ExpertGetFrame (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertGetFrame
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2bd02bde8caf157b6df6b1dd772a8f7574df0e57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826840"
---
# <a name="expertgetframe-function"></a><span data-ttu-id="5972a-103">Função ExpertGetFrame</span><span class="sxs-lookup"><span data-stu-id="5972a-103">ExpertGetFrame function</span></span>

<span data-ttu-id="5972a-104">A função **ExpertGetFrame** retorna o quadro solicitado de uma captura carregada.</span><span class="sxs-lookup"><span data-stu-id="5972a-104">The **ExpertGetFrame** function returns the requested frame from a loaded capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="5972a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5972a-105">Syntax</span></span>


```C++
DWORD WINAPI ExpertGetFrame(
  _In_  HEXPERTKEY              hExpertKey,
  _In_  DWORD                   Direction,
  _In_  DWORD                   RequestFlags,
  _In_  DWORD                   RequestedFrameNumber,
  _In_  HFILTER                 hFilter,
  _Out_ LPEXPERTFRAMEDESCRIPTOR pEFrameDescriptor
);
```



## <a name="parameters"></a><span data-ttu-id="5972a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5972a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5972a-107">*hExpertKey* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5972a-107">*hExpertKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5972a-108">Um identificador de especialista exclusivo.</span><span class="sxs-lookup"><span data-stu-id="5972a-108">A unique expert identifier.</span></span> <span data-ttu-id="5972a-109">Monitor de Rede passa o identificador *hExpertKey* para o especialista ao chamar a função [**Run**](run.md) .</span><span class="sxs-lookup"><span data-stu-id="5972a-109">Network Monitor passes the *hExpertKey* identifier to the expert when it calls the [**Run**](run.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="5972a-110">*Direção* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="5972a-110">*Direction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5972a-111">Um valor que identifica como Monitor de Rede procura o quadro.</span><span class="sxs-lookup"><span data-stu-id="5972a-111">A value that identifies how Network Monitor searches for the frame.</span></span>



| <span data-ttu-id="5972a-112">Valor</span><span class="sxs-lookup"><span data-stu-id="5972a-112">Value</span></span>                                                                                                                                                                                         | <span data-ttu-id="5972a-113">Significado</span><span class="sxs-lookup"><span data-stu-id="5972a-113">Meaning</span></span>                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="GET_SPECIFIED_FRAME"></span><span id="get_specified_frame"></span><dl> <span data-ttu-id="5972a-114"><dt>**OBTER \_ \_ quadro especificado**</dt></span><span class="sxs-lookup"><span data-stu-id="5972a-114"><dt>**GET\_SPECIFIED\_FRAME**</dt></span></span> </dl>              | <span data-ttu-id="5972a-115">Retornar o quadro solicitado.</span><span class="sxs-lookup"><span data-stu-id="5972a-115">Return the requested frame.</span></span><br/> |
| <span id="GET_FRAME_NEXT_FORWARD"></span><span id="get_frame_next_forward"></span><dl> <span data-ttu-id="5972a-116"><dt>**OBTER \_ \_ próximo quadro avançar \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5972a-116"><dt>**GET\_FRAME\_NEXT\_FORWARD**</dt></span></span> </dl>    | <span data-ttu-id="5972a-117">Retornar o próximo quadro.</span><span class="sxs-lookup"><span data-stu-id="5972a-117">Return the next frame.</span></span><br/>      |
| <span id="GET_FRAME_NEXT_BACKWARD"></span><span id="get_frame_next_backward"></span><dl> <span data-ttu-id="5972a-118"><dt>**OBTER \_ quadro \_ próximo \_ atrás**</dt></span><span class="sxs-lookup"><span data-stu-id="5972a-118"><dt>**GET\_FRAME\_NEXT\_BACKWARD**</dt></span></span> </dl> | <span data-ttu-id="5972a-119">Retornar o quadro anterior.</span><span class="sxs-lookup"><span data-stu-id="5972a-119">Return the previous frame.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="5972a-120">*RequestFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5972a-120">*RequestFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5972a-121">Os sinalizadores que especificam como Monitor de Rede devem tratar a solicitação.</span><span class="sxs-lookup"><span data-stu-id="5972a-121">The flags that specify how Network Monitor should handle the request.</span></span> <span data-ttu-id="5972a-122">Especifique um ou mais dos sinalizadores a seguir.</span><span class="sxs-lookup"><span data-stu-id="5972a-122">Specify one or more of the following flags.</span></span>



| <span data-ttu-id="5972a-123">Valor</span><span class="sxs-lookup"><span data-stu-id="5972a-123">Value</span></span>                                                                                                                                                                                             | <span data-ttu-id="5972a-124">Significado</span><span class="sxs-lookup"><span data-stu-id="5972a-124">Meaning</span></span>                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FLAGS_DEFER_TO_UI_FILTER"></span><span id="flags_defer_to_ui_filter"></span><dl> <span data-ttu-id="5972a-125"><dt>**SINALIZADORES \_ adiados \_ para o \_ filtro de interface do usuário \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5972a-125"><dt>**FLAGS\_DEFER\_TO\_UI\_FILTER**</dt></span></span> </dl> | <span data-ttu-id="5972a-126">Antes de aplicar o parâmetro de filtro de exibição do especialista que é especificado em *hFilter*, aplique o filtro de exibição que monitor de rede está usando quando o especialista é iniciado.</span><span class="sxs-lookup"><span data-stu-id="5972a-126">Before applying the display filter parameter of the expert which is specified in *hFilter*, apply the display filter that Network Monitor is using when the expert starts.</span></span><br/>                                                                                                                              |
| <span id="FLAGS_ATTACH_PROPERTIES"></span><span id="flags_attach_properties"></span><dl> <span data-ttu-id="5972a-127"><dt>**\_Propriedades de anexação de sinalizadores \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5972a-127"><dt>**FLAGS\_ATTACH\_PROPERTIES**</dt></span></span> </dl>      | <span data-ttu-id="5972a-128">As propriedades que todos os analisadores de protocolo encontram com as seções reivindicadas desse quadro são anexadas ao quadro.</span><span class="sxs-lookup"><span data-stu-id="5972a-128">The properties that all protocol parsers find with claimed sections of this frame are attached to the frame.</span></span> <span data-ttu-id="5972a-129">Se o sinalizador não for definido, o campo **lpPropertyTable** da estrutura [**EXPERTFRAMEDESCRIPTOR**](expertframedescriptor.md) (retornado por **PEFrameDescriptor**) será definido como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="5972a-129">If the flag is not set, the **lpPropertyTable** field of the [**EXPERTFRAMEDESCRIPTOR**](expertframedescriptor.md) structure (returned by **pEFrameDescriptor**) will be set to **NULL**.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="5972a-130">*RequestedFrameNumber* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5972a-130">*RequestedFrameNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5972a-131">O número do quadro solicitado.</span><span class="sxs-lookup"><span data-stu-id="5972a-131">The number of the requested frame.</span></span>

</dd> <dt>

<span data-ttu-id="5972a-132">*hFilter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5972a-132">*hFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5972a-133">Um identificador para o filtro de exibição de especialista.</span><span class="sxs-lookup"><span data-stu-id="5972a-133">A handle to the expert display filter.</span></span> <span data-ttu-id="5972a-134">Se o especialista não tiver um filtro de exibição, defina o parâmetro como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="5972a-134">If the expert does not have a display filter, set the parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="5972a-135">*pEFrameDescriptor* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="5972a-135">*pEFrameDescriptor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5972a-136">A estrutura [**EXPERTFRAMEDESCRIPTOR**](expertframedescriptor.md) que, no retorno, descreve o quadro.</span><span class="sxs-lookup"><span data-stu-id="5972a-136">The [**EXPERTFRAMEDESCRIPTOR**](expertframedescriptor.md) structure that, on return, describes the frame.</span></span> <span data-ttu-id="5972a-137">O especialista deve alocar e liberar a memória que essa estrutura usa.</span><span class="sxs-lookup"><span data-stu-id="5972a-137">The expert must allocate and free the memory that this structure uses.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5972a-138">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5972a-138">Return value</span></span>

<span data-ttu-id="5972a-139">Se a função for bem-sucedida, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="5972a-139">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="5972a-140">Se a função não for bem-sucedida, o valor de retorno indicará o motivo da falha.</span><span class="sxs-lookup"><span data-stu-id="5972a-140">If the function is unsuccessful, the return value indicates the reason for the failure.</span></span> <span data-ttu-id="5972a-141">Se o valor de retorno for NMERR \_ especialista \_ , o especialista deverá limpar e retornar imediatamente; o usuário anulou a execução do especialista.</span><span class="sxs-lookup"><span data-stu-id="5972a-141">If the return value is NMERR\_EXPERT\_TERMINATE, the expert must immediately clean up and return; the user has aborted the expert run.</span></span>

## <a name="remarks"></a><span data-ttu-id="5972a-142">Comentários</span><span class="sxs-lookup"><span data-stu-id="5972a-142">Remarks</span></span>

<span data-ttu-id="5972a-143">Se você definir sinalizadores \_ anexar \_ Propriedades, a chamada exigirá mais recursos do que se você não definir o sinalizador.</span><span class="sxs-lookup"><span data-stu-id="5972a-143">If you set FLAGS\_ATTACH\_PROPERTIES, the call requires more resources than if you do not set the flag.</span></span> <span data-ttu-id="5972a-144">Se o sinalizador não estiver definido, um ponteiro apontará para o quadro bruto e para os dados sobre o quadro.</span><span class="sxs-lookup"><span data-stu-id="5972a-144">If the flag is not set, a pointer points to the raw frame and to data about the frame.</span></span> <span data-ttu-id="5972a-145">Se esse sinalizador for definido, Monitor de Rede anexará todas as propriedades ao quadro chamando todos os analisadores que alegam uma parte do quadro.</span><span class="sxs-lookup"><span data-stu-id="5972a-145">If this flag is set, Network Monitor attaches all properties to the frame by calling every parser that claims a portion of the frame.</span></span> <span data-ttu-id="5972a-146">Isso pode ser um processo lento.</span><span class="sxs-lookup"><span data-stu-id="5972a-146">This can be a slow process.</span></span>

<span data-ttu-id="5972a-147">Os especialistas não devem definir o \_ sinalizador de propriedades anexar sinalizadores \_ , a menos que os especialistas exijam as propriedades que os analisadores anexam ao quadro.</span><span class="sxs-lookup"><span data-stu-id="5972a-147">Experts should not set the FLAGS\_ATTACH\_PROPERTIES flag unless the experts require the properties that parsers attach to the frame.</span></span> <span data-ttu-id="5972a-148">Se possível, os especialistas devem chamar a função **ExpertGetFrame** sem o sinalizador e, em seguida, extrair os dados necessários diretamente do quadro.</span><span class="sxs-lookup"><span data-stu-id="5972a-148">If possible, experts should call the **ExpertGetFrame** function without the flag, and then extract the required data directly from the frame.</span></span>

<span data-ttu-id="5972a-149">Se o especialista chamar **ExpertGetFrame** sem o \_ sinalizador de propriedades de anexação de sinalizadores \_ e exigir as propriedades associadas a esse quadro (um evento, por exemplo), o especialista chamará **ExpertGetFrame** com os mesmos parâmetros, exceto para o seguinte:</span><span class="sxs-lookup"><span data-stu-id="5972a-149">If the expert calls **ExpertGetFrame** without the FLAGS\_ATTACH\_PROPERTIES flag and requires the properties associated with that frame (an event, for example), the expert calls **ExpertGetFrame** with the same parameters except for the following:</span></span>

``` syntax
Direction = EXPERT_GET_SPECIFIED_FRAME;
RequestFlags &= (~EXPERT_DEFER_TO_UI_FILTER) | EXPERT_ATTACH_PROPERTIES;
RequestedFrameNumber= (The actual frame number you want);
hFilter = NULL;
pEFrameDescriptor = (The same one as last time);
```

<span data-ttu-id="5972a-150">O uso do código anterior garante que o especialista obtenha o quadro necessário sem precisar chamar o código de filtro novamente.</span><span class="sxs-lookup"><span data-stu-id="5972a-150">Using the preceding code ensures that the expert gets the required frame without having to call filter code again.</span></span>

<span data-ttu-id="5972a-151">Você pode definir o parâmetro *hFilter* como um **LPVOID**.</span><span class="sxs-lookup"><span data-stu-id="5972a-151">You can set the *hFilter* parameter as an **LPVOID**.</span></span> <span data-ttu-id="5972a-152">Se existir, o quadro retornado passará por esse filtro.</span><span class="sxs-lookup"><span data-stu-id="5972a-152">If it exists, the returned frame passes this filter.</span></span> <span data-ttu-id="5972a-153">Se o especialista não tiver um filtro de exibição para passar para a função (se *hFilter* for **nulo** ), o quadro retornado não será filtrado.</span><span class="sxs-lookup"><span data-stu-id="5972a-153">If the expert does not have a display filter to pass to the function (if *hFilter* is **NULL** ), then the frame returned is not filtered.</span></span>

<span data-ttu-id="5972a-154">A função **ExpertGetFrame** só pode ser chamada por especialistas que implementam a função [**executar**](run.md) ou [**Configurar**](configure.md) exportação.</span><span class="sxs-lookup"><span data-stu-id="5972a-154">The **ExpertGetFrame** function can only be called by experts that implement the [**Run**](run.md) or [**Configure**](configure.md) export function.</span></span>

## <a name="requirements"></a><span data-ttu-id="5972a-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5972a-155">Requirements</span></span>



| <span data-ttu-id="5972a-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="5972a-156">Requirement</span></span> | <span data-ttu-id="5972a-157">Valor</span><span class="sxs-lookup"><span data-stu-id="5972a-157">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5972a-158">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5972a-158">Minimum supported client</span></span><br/> | <span data-ttu-id="5972a-159">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5972a-159">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="5972a-160">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5972a-160">Minimum supported server</span></span><br/> | <span data-ttu-id="5972a-161">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5972a-161">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="5972a-162">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="5972a-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="5972a-163"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="5972a-163"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="5972a-164">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5972a-164">Library</span></span><br/>                  | <dl> <span data-ttu-id="5972a-165"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5972a-165"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="5972a-166">DLL</span><span class="sxs-lookup"><span data-stu-id="5972a-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5972a-167"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5972a-167"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




