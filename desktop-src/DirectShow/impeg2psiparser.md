---
description: A implementação dessa interface é fornecida como um código de exemplo com o SDK do DirectShow.
ms.assetid: a18fc6b6-f37e-4c87-9150-0504333d33c2
title: Interface IMpeg2PsiParser
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser
api_type:
- COM
api_location: ''
ms.openlocfilehash: 51f0f3373c67da75c50ecc2f6bc234e0351f5dc3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105754760"
---
# <a name="impeg2psiparser-interface"></a><span data-ttu-id="f9ca1-103">Interface IMpeg2PsiParser</span><span class="sxs-lookup"><span data-stu-id="f9ca1-103">IMpeg2PsiParser interface</span></span>

<span data-ttu-id="f9ca1-104">A implementação dessa interface é fornecida como um código de exemplo com o SDK do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="f9ca1-104">The implementation of this interface is provided as sample code with the DirectShow SDK.</span></span> <span data-ttu-id="f9ca1-105">Não é uma API do DirectShow com suporte.</span><span class="sxs-lookup"><span data-stu-id="f9ca1-105">It is not a supported DirectShow API.</span></span>

<span data-ttu-id="f9ca1-106">A `IMpeg2PsiParser` interface recupera informações específicas do programa (psi) do filtro do analisador psi, que é fornecido no SDK do DirectShow como um filtro de exemplo.</span><span class="sxs-lookup"><span data-stu-id="f9ca1-106">The `IMpeg2PsiParser` interface retrieves Program Specific Information (PSI) from the PSI Parser filter, which is provided in the DirectShow SDK as a sample filter.</span></span> <span data-ttu-id="f9ca1-107">Um aplicativo pode usar esse filtro para mapear IDs de programa (PIDs) no filtro de demultiplexador MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="f9ca1-107">An application can use this filter to map program IDs (PIDs) on the MPEG-2 Demultiplexer filter.</span></span>

## <a name="members"></a><span data-ttu-id="f9ca1-108">Membros</span><span class="sxs-lookup"><span data-stu-id="f9ca1-108">Members</span></span>

<span data-ttu-id="f9ca1-109">A interface **IMpeg2PsiParser** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="f9ca1-109">The **IMpeg2PsiParser** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="f9ca1-110">**IMpeg2PsiParser** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="f9ca1-110">**IMpeg2PsiParser** also has these types of members:</span></span>

-   [<span data-ttu-id="f9ca1-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="f9ca1-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f9ca1-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="f9ca1-112">Methods</span></span>

<span data-ttu-id="f9ca1-113">A interface **IMpeg2PsiParser** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="f9ca1-113">The **IMpeg2PsiParser** interface has these methods.</span></span>



| <span data-ttu-id="f9ca1-114">Método</span><span class="sxs-lookup"><span data-stu-id="f9ca1-114">Method</span></span>                                                                             | <span data-ttu-id="f9ca1-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="f9ca1-115">Description</span></span>                                                                               |
|:-----------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9ca1-116">[**FindRecordProgramMapPid**](/previous-versions/windows/desktop/legacy/dd407137(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f9ca1-116">[**FindRecordProgramMapPid**](/previous-versions/windows/desktop/legacy/dd407137(v=vs.85))</span></span>         | <span data-ttu-id="f9ca1-117">Localiza o PID da tabela de mapa do programa (PGTO) para um programa, dado o número do programa.</span><span class="sxs-lookup"><span data-stu-id="f9ca1-117">Finds the Program Map Table (PMT) PID for a program, given the program number.</span></span><br/> |
| [<span data-ttu-id="f9ca1-118">**GetCountOfElementaryStreams**</span><span class="sxs-lookup"><span data-stu-id="f9ca1-118">**GetCountOfElementaryStreams**</span></span>](impeg2psiparser-getcountofelementarystreams.md) | <span data-ttu-id="f9ca1-119">Recupera o número de fluxos elementares em um programa especificado.</span><span class="sxs-lookup"><span data-stu-id="f9ca1-119">Retrieves the number of elementary streams in a specified program.</span></span><br/>             |
| [<span data-ttu-id="f9ca1-120">**GetCountOfPrograms**</span><span class="sxs-lookup"><span data-stu-id="f9ca1-120">**GetCountOfPrograms**</span></span>](impeg2psiparser-getcountofprograms.md)                   | <span data-ttu-id="f9ca1-121">Recupera o número de programas no fluxo de transporte.</span><span class="sxs-lookup"><span data-stu-id="f9ca1-121">Retrieves the number of programs in the transport stream.</span></span><br/>                      |
| [<span data-ttu-id="f9ca1-122">**GetPatVersionNumber**</span><span class="sxs-lookup"><span data-stu-id="f9ca1-122">**GetPatVersionNumber**</span></span>](impeg2psiparser-getpatversionnumber.md)                 | <span data-ttu-id="f9ca1-123">Recupera o \_ campo de número de versão da Pat (tabela de associação de programa).</span><span class="sxs-lookup"><span data-stu-id="f9ca1-123">Retrieves the version\_number field from the Program Association Table (PAT).</span></span><br/>  |
| [<span data-ttu-id="f9ca1-124">**GetPmtVersionNumber**</span><span class="sxs-lookup"><span data-stu-id="f9ca1-124">**GetPmtVersionNumber**</span></span>](impeg2psiparser-getpmtversionnumber.md)                 | <span data-ttu-id="f9ca1-125">Recupera o \_ campo de número de versão de um PGTO especificado.</span><span class="sxs-lookup"><span data-stu-id="f9ca1-125">Retrieves the version\_number field from a specified PMT.</span></span><br/>                      |
| <span data-ttu-id="f9ca1-126">[**GetRecordElementaryPid**](/previous-versions/windows/desktop/legacy/dd376623(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f9ca1-126">[**GetRecordElementaryPid**](/previous-versions/windows/desktop/legacy/dd376623(v=vs.85))</span></span>           | <span data-ttu-id="f9ca1-127">Recupera a atribuição de PID para um fluxo elementar especificado em um programa.</span><span class="sxs-lookup"><span data-stu-id="f9ca1-127">Retrieves the PID assignment for a specified elementary stream in a program.</span></span><br/>   |
| <span data-ttu-id="f9ca1-128">[**GetRecordProgramMapPid**](/previous-versions/windows/desktop/legacy/dd376624(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f9ca1-128">[**GetRecordProgramMapPid**](/previous-versions/windows/desktop/legacy/dd376624(v=vs.85))</span></span>           | <span data-ttu-id="f9ca1-129">Recupera a atribuição de PID para um PGTO especificado.</span><span class="sxs-lookup"><span data-stu-id="f9ca1-129">Retrieves the PID assignment for a specified PMT.</span></span><br/>                              |
| [<span data-ttu-id="f9ca1-130">**GetRecordProgramNumber**</span><span class="sxs-lookup"><span data-stu-id="f9ca1-130">**GetRecordProgramNumber**</span></span>](impeg2psiparser-getrecordprogramnumber.md)           | <span data-ttu-id="f9ca1-131">Recupera o número do programa de um programa especificado.</span><span class="sxs-lookup"><span data-stu-id="f9ca1-131">Retrieves the program number for a specified program.</span></span><br/>                          |
| <span data-ttu-id="f9ca1-132">[**GetRecordStreamType**](/previous-versions/windows/desktop/legacy/dd376626(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f9ca1-132">[**GetRecordStreamType**](/previous-versions/windows/desktop/legacy/dd376626(v=vs.85))</span></span>                 | <span data-ttu-id="f9ca1-133">Recupera o tipo de fluxo para um fluxo elementar especificado em um programa.</span><span class="sxs-lookup"><span data-stu-id="f9ca1-133">Retrieves the stream type for a specified elementary stream in a program.</span></span><br/>      |
| [<span data-ttu-id="f9ca1-134">**GetTransportStreamId**</span><span class="sxs-lookup"><span data-stu-id="f9ca1-134">**GetTransportStreamId**</span></span>](impeg2psiparser-gettransportstreamid.md)               | <span data-ttu-id="f9ca1-135">Recupera o \_ \_ campo ID do fluxo de transporte do Pat.</span><span class="sxs-lookup"><span data-stu-id="f9ca1-135">Retrieves the transport\_stream\_id field from the PAT.</span></span><br/>                        |



 

## <a name="see-also"></a><span data-ttu-id="f9ca1-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="f9ca1-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9ca1-137">Exemplo de filtro do analisador PSI</span><span class="sxs-lookup"><span data-stu-id="f9ca1-137">PSI Parser Filter Sample</span></span>](psi-parser-filter-sample.md)
</dt> </dl>

 

 
