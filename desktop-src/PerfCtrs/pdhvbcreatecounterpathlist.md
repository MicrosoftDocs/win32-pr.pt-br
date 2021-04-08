---
description: A função PdhVbCreateCounterPathList exibe a caixa de diálogo de navegação do contador de desempenho, que permite ao usuário selecionar vários contadores de desempenho. Cada caminho de contador selecionado deve ser lido usando a função PdhVbGetCounterPathFromList.
ms.assetid: 8dda528f-2e06-4726-89a0-095781a2f80d
title: Função PdhVbCreateCounterPathList
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbCreateCounterPathList
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: bef484846507bf68d8ccfc0ad3ea10a250b83133
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828388"
---
# <a name="pdhvbcreatecounterpathlist-function"></a><span data-ttu-id="a567f-104">Função PdhVbCreateCounterPathList</span><span class="sxs-lookup"><span data-stu-id="a567f-104">PdhVbCreateCounterPathList function</span></span>

<span data-ttu-id="a567f-105">A função **PdhVbCreateCounterPathList** exibe a caixa de diálogo de navegação do contador de desempenho, que permite ao usuário selecionar vários contadores de desempenho.</span><span class="sxs-lookup"><span data-stu-id="a567f-105">The **PdhVbCreateCounterPathList** function displays the performance counter browsing dialog box, which lets the user select several performance counters.</span></span> <span data-ttu-id="a567f-106">Cada caminho de contador selecionado deve ser lido usando a função [**PdhVbGetCounterPathFromList**](pdhvbgetcounterpathfromlist.md) .</span><span class="sxs-lookup"><span data-stu-id="a567f-106">Each selected counter path must then be read using the [**PdhVbGetCounterPathFromList**](pdhvbgetcounterpathfromlist.md) function.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a567f-107">A função que este tópico descreve pode ser alterada ou indisponível no futuro.</span><span class="sxs-lookup"><span data-stu-id="a567f-107">The function that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="a567f-108">Em vez disso, a Microsoft recomenda que você use as funções descritas em [funções de contadores de desempenho](performance-counters-functions.md).</span><span class="sxs-lookup"><span data-stu-id="a567f-108">Instead, Microsoft recommends that you use the functions described in [Performance Counters Functions](performance-counters-functions.md).</span></span>

<span data-ttu-id="a567f-109">Função PdhVbCreateCounterPathList ( \_ ByVal DetailLevel as Long, \_ ByVal Legendastring as String \_ ) como Long</span><span class="sxs-lookup"><span data-stu-id="a567f-109">Function PdhVbCreateCounterPathList( \_ ByVal DetailLevel As Long, \_ ByVal CaptionString As String \_ ) As Long</span></span>

## <a name="parameters"></a><span data-ttu-id="a567f-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a567f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a567f-111">*DetailLevel*</span><span class="sxs-lookup"><span data-stu-id="a567f-111">*DetailLevel*</span></span> 
</dt> <dd>

<span data-ttu-id="a567f-112">Tipos de contadores a serem exibidos na caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="a567f-112">Types of counters to be displayed in the dialog box.</span></span> <span data-ttu-id="a567f-113">Use um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="a567f-113">Use one of the following values.</span></span>



| <span data-ttu-id="a567f-114">Valor</span><span class="sxs-lookup"><span data-stu-id="a567f-114">Value</span></span>                                                                                                                                                                               | <span data-ttu-id="a567f-115">Significado</span><span class="sxs-lookup"><span data-stu-id="a567f-115">Meaning</span></span>                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PERF_DETAIL_ADVANCED"></span><span id="perf_detail_advanced"></span><dl> <span data-ttu-id="a567f-116"><dt>**detalhes do desempenho \_ \_ avançado**</dt></span><span class="sxs-lookup"><span data-stu-id="a567f-116"><dt>**PERF\_DETAIL\_ADVANCED**</dt></span></span> </dl> | <span data-ttu-id="a567f-117">Os contadores que o usuário avançado provavelmente entenderá, além dos contadores de usuário iniciantes.</span><span class="sxs-lookup"><span data-stu-id="a567f-117">Counters that the advanced user is likely to understand, in addition to the novice-user counters.</span></span><br/>                                            |
| <span id="PERF_DETAIL_EXPERT"></span><span id="perf_detail_expert"></span><dl> <span data-ttu-id="a567f-118"><dt>**\_especialista em detalhes de desempenho \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a567f-118"><dt>**PERF\_DETAIL\_EXPERT**</dt></span></span> </dl>       | <span data-ttu-id="a567f-119">Os contadores que o usuário experiente e o desenvolvedor de software provavelmente compreenderão, além dos contadores para os usuários iniciantes e avançados.</span><span class="sxs-lookup"><span data-stu-id="a567f-119">Counters that the expert user and software developer is likely to understand, in addition to the counters for the novice and advanced users.</span></span><br/> |
| <span id="PERF_DETAIL_NOVICE"></span><span id="perf_detail_novice"></span><dl> <span data-ttu-id="a567f-120"><dt>**reiniciante de detalhes de desempenho \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a567f-120"><dt>**PERF\_DETAIL\_NOVICE**</dt></span></span> </dl>       | <span data-ttu-id="a567f-121">Somente os contadores que o usuário iniciante provavelmente entenderá.</span><span class="sxs-lookup"><span data-stu-id="a567f-121">Only counters that the novice user is likely to understand.</span></span><br/>                                                                                  |
| <span id="PERF_DETAIL_WIZARD"></span><span id="perf_detail_wizard"></span><dl> <span data-ttu-id="a567f-122"><dt>**\_Assistente de detalhes de desempenho \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a567f-122"><dt>**PERF\_DETAIL\_WIZARD**</dt></span></span> </dl>       | <span data-ttu-id="a567f-123">Todos os contadores no sistema.</span><span class="sxs-lookup"><span data-stu-id="a567f-123">All counters in the system.</span></span><br/>                                                                                                                  |



 

</dd> <dt>

<span data-ttu-id="a567f-124">*Legendastring*</span><span class="sxs-lookup"><span data-stu-id="a567f-124">*CaptionString*</span></span> 
</dt> <dd>

<span data-ttu-id="a567f-125">Variável de cadeia de caracteres que contém o texto que será exibido na barra de legenda da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="a567f-125">String variable that contains the text that will be displayed in the caption bar of the dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a567f-126">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a567f-126">Return value</span></span>

<span data-ttu-id="a567f-127">A função retorna o número de caminhos do contador que o usuário selecionou.</span><span class="sxs-lookup"><span data-stu-id="a567f-127">The function returns the number of counter paths that the user selected.</span></span>

## <a name="requirements"></a><span data-ttu-id="a567f-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a567f-128">Requirements</span></span>



| <span data-ttu-id="a567f-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="a567f-129">Requirement</span></span> | <span data-ttu-id="a567f-130">Valor</span><span class="sxs-lookup"><span data-stu-id="a567f-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a567f-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a567f-131">Minimum supported client</span></span><br/> | <span data-ttu-id="a567f-132">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a567f-132">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a567f-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a567f-133">Minimum supported server</span></span><br/> | <span data-ttu-id="a567f-134">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a567f-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a567f-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a567f-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="a567f-136"><dt>PDH. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a567f-136"><dt>Pdh.lib</dt></span></span> </dl> |
| <span data-ttu-id="a567f-137">DLL</span><span class="sxs-lookup"><span data-stu-id="a567f-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a567f-138"><dt>Pdh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a567f-138"><dt>Pdh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a567f-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="a567f-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a567f-140">**PdhVbGetCounterPathElements**</span><span class="sxs-lookup"><span data-stu-id="a567f-140">**PdhVbGetCounterPathElements**</span></span>](pdhvbgetcounterpathelements.md)
</dt> <dt>

[<span data-ttu-id="a567f-141">**PdhVbGetCounterPathFromList**</span><span class="sxs-lookup"><span data-stu-id="a567f-141">**PdhVbGetCounterPathFromList**</span></span>](pdhvbgetcounterpathfromlist.md)
</dt> <dt>

[<span data-ttu-id="a567f-142">**PdhVbGetOneCounterPath**</span><span class="sxs-lookup"><span data-stu-id="a567f-142">**PdhVbGetOneCounterPath**</span></span>](pdhvbgetonecounterpath.md)
</dt> </dl>

 

 




