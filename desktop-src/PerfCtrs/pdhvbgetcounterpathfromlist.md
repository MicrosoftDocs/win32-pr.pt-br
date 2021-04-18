---
description: A função PdhVbGetCounterPathFromList copia o caminho do contador referenciado pelo parâmetro de índice de uma lista de caminhos de contador criada pelo usuário a partir da chamada mais recente para a função PdhVbCreateCounterPathList.
ms.assetid: e77a022d-42f2-4c48-acb7-36cb013730dd
title: Função PdhVbGetCounterPathFromList
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbGetCounterPathFromList
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 4c5ae4632ede898b7cd323723037ea68d53455b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756700"
---
# <a name="pdhvbgetcounterpathfromlist-function"></a><span data-ttu-id="7b91f-103">Função PdhVbGetCounterPathFromList</span><span class="sxs-lookup"><span data-stu-id="7b91f-103">PdhVbGetCounterPathFromList function</span></span>

<span data-ttu-id="7b91f-104">A função **PdhVbGetCounterPathFromList** copia o caminho do contador referenciado pelo parâmetro de *índice* de uma lista de caminhos de contador criada pelo usuário a partir da chamada mais recente para a função [**PdhVbCreateCounterPathList**](pdhvbcreatecounterpathlist.md) .</span><span class="sxs-lookup"><span data-stu-id="7b91f-104">The **PdhVbGetCounterPathFromList** function copies the counter path referenced by the *Index* parameter from a counter path list created by the user from the most recent call to the [**PdhVbCreateCounterPathList**](pdhvbcreatecounterpathlist.md) function.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7b91f-105">A função que este tópico descreve pode ser alterada ou indisponível no futuro.</span><span class="sxs-lookup"><span data-stu-id="7b91f-105">The function that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="7b91f-106">Em vez disso, a Microsoft recomenda que você use as funções descritas em [funções de contadores de desempenho](performance-counters-functions.md).</span><span class="sxs-lookup"><span data-stu-id="7b91f-106">Instead, Microsoft recommends that you use the functions described in [Performance Counters Functions](performance-counters-functions.md).</span></span>

<span data-ttu-id="7b91f-107">Função PdhVbGetCounterPathFromList ( \_ o índice ByVal como longo, \_ ByVal buffer como cadeia de caracteres, \_ ByVal BufferLength como longo \_ ) enquanto longo</span><span class="sxs-lookup"><span data-stu-id="7b91f-107">Function PdhVbGetCounterPathFromList( \_ ByVal Index As Long, \_ ByVal Buffer As String, \_ ByVal BufferLength As Long \_ ) As Long</span></span>

## <a name="parameters"></a><span data-ttu-id="7b91f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7b91f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b91f-109">*Index*</span><span class="sxs-lookup"><span data-stu-id="7b91f-109">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="7b91f-110">Índice do caminho do contador a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="7b91f-110">Index of the counter path to retrieve.</span></span> <span data-ttu-id="7b91f-111">Deve ser um valor que seja maior ou igual a 1 e menor ou igual ao valor retornado pela função [**PdhVbCreateCounterPathList**](pdhvbcreatecounterpathlist.md) .</span><span class="sxs-lookup"><span data-stu-id="7b91f-111">This must be a value that is greater than or equal to 1, and less than or equal to the value returned by the [**PdhVbCreateCounterPathList**](pdhvbcreatecounterpathlist.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="7b91f-112">*Buffer*</span><span class="sxs-lookup"><span data-stu-id="7b91f-112">*Buffer*</span></span> 
</dt> <dd>

<span data-ttu-id="7b91f-113">Cadeia de caracteres dimensioned e Initialized que receberá o caminho do contador que corresponde ao valor do parâmetro de índice.</span><span class="sxs-lookup"><span data-stu-id="7b91f-113">Dimensioned and initialized string that will receive the counter path that corresponds to the value of the Index parameter.</span></span>

</dd> <dt>

<span data-ttu-id="7b91f-114">*BufferLength*</span><span class="sxs-lookup"><span data-stu-id="7b91f-114">*BufferLength*</span></span> 
</dt> <dd>

<span data-ttu-id="7b91f-115">Número máximo de caracteres que se ajustarão à cadeia de caracteres referenciada pelo buffer.</span><span class="sxs-lookup"><span data-stu-id="7b91f-115">Maximum number of characters that will fit in the string referenced by Buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b91f-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7b91f-116">Return value</span></span>

<span data-ttu-id="7b91f-117">A função retorna o número de caracteres copiados para o buffer.</span><span class="sxs-lookup"><span data-stu-id="7b91f-117">The function returns the number of characters copied to Buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b91f-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7b91f-118">Requirements</span></span>



| <span data-ttu-id="7b91f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b91f-119">Requirement</span></span> | <span data-ttu-id="7b91f-120">Valor</span><span class="sxs-lookup"><span data-stu-id="7b91f-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7b91f-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7b91f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7b91f-122">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="7b91f-122">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7b91f-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7b91f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7b91f-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7b91f-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="7b91f-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7b91f-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="7b91f-126"><dt>PDH. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7b91f-126"><dt>Pdh.lib</dt></span></span> </dl> |
| <span data-ttu-id="7b91f-127">DLL</span><span class="sxs-lookup"><span data-stu-id="7b91f-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7b91f-128"><dt>Pdh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b91f-128"><dt>Pdh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b91f-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="7b91f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b91f-130">**PdhVbCreateCounterPathList**</span><span class="sxs-lookup"><span data-stu-id="7b91f-130">**PdhVbCreateCounterPathList**</span></span>](pdhvbcreatecounterpathlist.md)
</dt> <dt>

[<span data-ttu-id="7b91f-131">**PdhVbGetCounterPathElements**</span><span class="sxs-lookup"><span data-stu-id="7b91f-131">**PdhVbGetCounterPathElements**</span></span>](pdhvbgetcounterpathelements.md)
</dt> <dt>

[<span data-ttu-id="7b91f-132">**PdhVbGetOneCounterPath**</span><span class="sxs-lookup"><span data-stu-id="7b91f-132">**PdhVbGetOneCounterPath**</span></span>](pdhvbgetonecounterpath.md)
</dt> </dl>

 

 




