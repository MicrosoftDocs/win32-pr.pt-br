---
description: A função PdhVbGetOneCounterPath exibe uma caixa de diálogo que permite ao usuário procurar os contadores de desempenho disponíveis e selecionar um contador.
ms.assetid: a42406ef-70e0-464d-90f8-fef9e1c3471d
title: Função PdhVbGetOneCounterPath
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbGetOneCounterPath
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 980665372d49f483e3fb59b7571ec38fa9c2851a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828386"
---
# <a name="pdhvbgetonecounterpath-function"></a><span data-ttu-id="297b9-103">Função PdhVbGetOneCounterPath</span><span class="sxs-lookup"><span data-stu-id="297b9-103">PdhVbGetOneCounterPath function</span></span>

<span data-ttu-id="297b9-104">A função **PdhVbGetOneCounterPath** exibe uma caixa de diálogo que permite ao usuário procurar os contadores de desempenho disponíveis e selecionar um contador.</span><span class="sxs-lookup"><span data-stu-id="297b9-104">The **PdhVbGetOneCounterPath** function displays a dialog box that lets the user browse the available performance counters and select one counter.</span></span> <span data-ttu-id="297b9-105">O contador selecionado é retornado na variável *pathstring* .</span><span class="sxs-lookup"><span data-stu-id="297b9-105">The counter selected is returned in the *PathString* variable.</span></span> <span data-ttu-id="297b9-106">A variável *pathstring* deve ser dimensionada e inicializada antes que essa função seja chamada, e o tamanho de dimensão deve ser indicado pela variável *PathLength* .</span><span class="sxs-lookup"><span data-stu-id="297b9-106">The *PathString* variable must be dimensioned and initialized before this function is called, and the dimensioned size must be indicated by the *PathLength* variable.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="297b9-107">A função que este tópico descreve pode ser alterada ou indisponível no futuro.</span><span class="sxs-lookup"><span data-stu-id="297b9-107">The function that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="297b9-108">Em vez disso, a Microsoft recomenda que você use as funções descritas em [funções de contadores de desempenho](performance-counters-functions.md).</span><span class="sxs-lookup"><span data-stu-id="297b9-108">Instead, Microsoft recommends that you use the functions described in [Performance Counters Functions](performance-counters-functions.md).</span></span>

<span data-ttu-id="297b9-109">Função PdhVbGetOneCounterPath ( \_ ByVal caminhostring como cadeia de caracteres, \_ ByVal PathLength como longo, \_ ByVal DetailLevel como Long, \_ ByVal legendastring as String \_ ) como longo</span><span class="sxs-lookup"><span data-stu-id="297b9-109">Function PdhVbGetOneCounterPath( \_ ByVal PathString As String, \_ ByVal PathLength As Long, \_ ByVal DetailLevel As Long, \_ ByVal CaptionString As String \_ ) As Long</span></span>

## <a name="parameters"></a><span data-ttu-id="297b9-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="297b9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="297b9-111">*Caminho da*</span><span class="sxs-lookup"><span data-stu-id="297b9-111">*PathString*</span></span> 
</dt> <dd>

<span data-ttu-id="297b9-112">Variável de cadeia de caracteres inicializada usada para receber o caminho do contador selecionado pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="297b9-112">Initialized string variable used to receive the counter path selected by the user.</span></span>

</dd> <dt>

<span data-ttu-id="297b9-113">*PathLength*</span><span class="sxs-lookup"><span data-stu-id="297b9-113">*PathLength*</span></span> 
</dt> <dd>

<span data-ttu-id="297b9-114">Comprimento do Caminhostring inicializado.</span><span class="sxs-lookup"><span data-stu-id="297b9-114">Length of the initialized PathString.</span></span>

</dd> <dt>

<span data-ttu-id="297b9-115">*DetailLevel*</span><span class="sxs-lookup"><span data-stu-id="297b9-115">*DetailLevel*</span></span> 
</dt> <dd>

<span data-ttu-id="297b9-116">Tipos de contadores a serem exibidos na caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="297b9-116">Types of counters to be displayed in the dialog box.</span></span> <span data-ttu-id="297b9-117">Esse parâmetro pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="297b9-117">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="297b9-118">Valor</span><span class="sxs-lookup"><span data-stu-id="297b9-118">Value</span></span>                                                                                                                                                                               | <span data-ttu-id="297b9-119">Significado</span><span class="sxs-lookup"><span data-stu-id="297b9-119">Meaning</span></span>                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PERF_DETAIL_ADVANCED"></span><span id="perf_detail_advanced"></span><dl> <span data-ttu-id="297b9-120"><dt>**detalhes do desempenho \_ \_ avançado**</dt></span><span class="sxs-lookup"><span data-stu-id="297b9-120"><dt>**PERF\_DETAIL\_ADVANCED**</dt></span></span> </dl> | <span data-ttu-id="297b9-121">Os contadores que o usuário avançado provavelmente entenderá, além dos contadores de usuário iniciantes.</span><span class="sxs-lookup"><span data-stu-id="297b9-121">Counters that the advanced user is likely to understand, in addition to the novice-user counters.</span></span><br/>                                            |
| <span id="PERF_DETAIL_EXPERT"></span><span id="perf_detail_expert"></span><dl> <span data-ttu-id="297b9-122"><dt>**\_especialista em detalhes de desempenho \_**</dt></span><span class="sxs-lookup"><span data-stu-id="297b9-122"><dt>**PERF\_DETAIL\_EXPERT**</dt></span></span> </dl>       | <span data-ttu-id="297b9-123">Os contadores que o usuário experiente e o desenvolvedor de software provavelmente compreenderão, além dos contadores para os usuários iniciantes e avançados.</span><span class="sxs-lookup"><span data-stu-id="297b9-123">Counters that the expert user and software developer is likely to understand, in addition to the counters for the novice and advanced users.</span></span><br/> |
| <span id="PERF_DETAIL_NOVICE"></span><span id="perf_detail_novice"></span><dl> <span data-ttu-id="297b9-124"><dt>**reiniciante de detalhes de desempenho \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="297b9-124"><dt>**PERF\_DETAIL\_NOVICE**</dt></span></span> </dl>       | <span data-ttu-id="297b9-125">Somente os contadores que o usuário iniciante provavelmente entenderá.</span><span class="sxs-lookup"><span data-stu-id="297b9-125">Only counters that the novice user is likely to understand.</span></span><br/>                                                                                  |
| <span id="PERF_DETAIL_WIZARD"></span><span id="perf_detail_wizard"></span><dl> <span data-ttu-id="297b9-126"><dt>**\_Assistente de detalhes de desempenho \_**</dt></span><span class="sxs-lookup"><span data-stu-id="297b9-126"><dt>**PERF\_DETAIL\_WIZARD**</dt></span></span> </dl>       | <span data-ttu-id="297b9-127">Todos os contadores no sistema.</span><span class="sxs-lookup"><span data-stu-id="297b9-127">All counters in the system.</span></span><br/>                                                                                                                  |



 

</dd> <dt>

<span data-ttu-id="297b9-128">*Legendastring*</span><span class="sxs-lookup"><span data-stu-id="297b9-128">*CaptionString*</span></span> 
</dt> <dd>

<span data-ttu-id="297b9-129">Variável de cadeia de caracteres que contém o texto que será exibido na barra de legenda da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="297b9-129">String variable that contains the text that will be displayed in the caption bar of the dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="297b9-130">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="297b9-130">Return value</span></span>

<span data-ttu-id="297b9-131">A função retorna o número de caracteres gravados no buffer *pathstring* .</span><span class="sxs-lookup"><span data-stu-id="297b9-131">The function returns the number of characters written to the *PathString* buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="297b9-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="297b9-132">Requirements</span></span>



| <span data-ttu-id="297b9-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="297b9-133">Requirement</span></span> | <span data-ttu-id="297b9-134">Valor</span><span class="sxs-lookup"><span data-stu-id="297b9-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="297b9-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="297b9-135">Minimum supported client</span></span><br/> | <span data-ttu-id="297b9-136">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="297b9-136">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="297b9-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="297b9-137">Minimum supported server</span></span><br/> | <span data-ttu-id="297b9-138">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="297b9-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="297b9-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="297b9-139">Library</span></span><br/>                  | <dl> <span data-ttu-id="297b9-140"><dt>PDH. lib</dt></span><span class="sxs-lookup"><span data-stu-id="297b9-140"><dt>Pdh.lib</dt></span></span> </dl> |
| <span data-ttu-id="297b9-141">DLL</span><span class="sxs-lookup"><span data-stu-id="297b9-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="297b9-142"><dt>Pdh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="297b9-142"><dt>Pdh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="297b9-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="297b9-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="297b9-144">**PdhVbCreateCounterPathList**</span><span class="sxs-lookup"><span data-stu-id="297b9-144">**PdhVbCreateCounterPathList**</span></span>](pdhvbcreatecounterpathlist.md)
</dt> <dt>

[<span data-ttu-id="297b9-145">**PdhVbGetCounterPathElements**</span><span class="sxs-lookup"><span data-stu-id="297b9-145">**PdhVbGetCounterPathElements**</span></span>](pdhvbgetcounterpathelements.md)
</dt> <dt>

[<span data-ttu-id="297b9-146">**PdhVbGetCounterPathFromList**</span><span class="sxs-lookup"><span data-stu-id="297b9-146">**PdhVbGetCounterPathFromList**</span></span>](pdhvbgetcounterpathfromlist.md)
</dt> </dl>

 

 




