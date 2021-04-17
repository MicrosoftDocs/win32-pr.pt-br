---
description: Uma enumeração usada para enviar respostas do mecanismo de captura para Diagnóstico de Gráficos.
MS-HAID: vspixengine.PixPipeResponse
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Enumeração PixPipeResponse
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5BFEE25D-3E03-493E-AFEF-DD8C70C53FC5
api_name:
- PixPipeResponse
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 09ab253be5e02cc7329195016a406758b7a82e2b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105762462"
---
# <a name="span-idvspixenginepixpiperesponsespanpixpiperesponse-enumeration"></a><span data-ttu-id="70f9a-103"><span id="vspixengine.pixpiperesponse"></span>Enumeração PixPipeResponse</span><span class="sxs-lookup"><span data-stu-id="70f9a-103"><span id="vspixengine.pixpiperesponse"></span>PixPipeResponse enumeration</span></span>

<span data-ttu-id="70f9a-104">Uma enumeração usada para enviar respostas do mecanismo de captura para Diagnóstico de Gráficos.</span><span class="sxs-lookup"><span data-stu-id="70f9a-104">An enum used to send responses from the capture engine to Graphics Diagnostics.</span></span>

## <a name="syntax"></a><span data-ttu-id="70f9a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="70f9a-105">Syntax</span></span>


```C++
};
```

## <a name="constants"></a><span data-ttu-id="70f9a-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="70f9a-106">Constants</span></span>

<span data-ttu-id="70f9a-107"><span id="NEW_DATA_AVAILABLE"></span><span id="new_data_available"></span>**NOVOS \_ dados \_ disponíveis**</span><span class="sxs-lookup"><span data-stu-id="70f9a-107"><span id="NEW_DATA_AVAILABLE"></span><span id="new_data_available"></span>**NEW\_DATA\_AVAILABLE**</span></span>  
<span data-ttu-id="70f9a-108">Uma resposta que indica que novos dados foram gravados no log de gráficos e estão prontos para serem lidos.</span><span class="sxs-lookup"><span data-stu-id="70f9a-108">A response which indicates that new data has been written to the graphics log and is ready to be read.</span></span>

<span data-ttu-id="70f9a-109"><span id="EXPERIMENT_DATA"></span><span id="experiment_data"></span>**dados de teste \_**</span><span class="sxs-lookup"><span data-stu-id="70f9a-109"><span id="EXPERIMENT_DATA"></span><span id="experiment_data"></span>**EXPERIMENT\_DATA**</span></span>  
<span data-ttu-id="70f9a-110">Uma resposta que indica informações de configuração sobre a sessão de captura.</span><span class="sxs-lookup"><span data-stu-id="70f9a-110">A response which indicates configuration information about the capture session.</span></span>

<span data-ttu-id="70f9a-111"><span id="ERRORCODE"></span><span id="errorcode"></span>**ERRORCODE**</span><span class="sxs-lookup"><span data-stu-id="70f9a-111"><span id="ERRORCODE"></span><span id="errorcode"></span>**ERRORCODE**</span></span>  
<span data-ttu-id="70f9a-112">Uma resposta que indica que o mecanismo de captura encontrou um erro.</span><span class="sxs-lookup"><span data-stu-id="70f9a-112">A response which indicates that the capture engine has encountered an error.</span></span>

<span data-ttu-id="70f9a-113"><span id="APPLICATIONCAPTUREINPROGRESS"></span><span id="applicationcaptureinprogress"></span>**APPLICATIONCAPTUREINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="70f9a-113"><span id="APPLICATIONCAPTUREINPROGRESS"></span><span id="applicationcaptureinprogress"></span>**APPLICATIONCAPTUREINPROGRESS**</span></span>  
<span data-ttu-id="70f9a-114">Uma resposta que indica que o mecanismo de captura iniciou a captura de informações de gráficos.</span><span class="sxs-lookup"><span data-stu-id="70f9a-114">A response which indicates that the capture engine has started capturing graphics information.</span></span> <span data-ttu-id="70f9a-115">Isso não indica que os dados estão disponíveis para serem examinados ainda.</span><span class="sxs-lookup"><span data-stu-id="70f9a-115">This does not indicate that data is available to be examined yet.</span></span>

<span data-ttu-id="70f9a-116"><span id="PARTIAL_DATA"></span><span id="partial_data"></span>**dados PARCIAIs \_**</span><span class="sxs-lookup"><span data-stu-id="70f9a-116"><span id="PARTIAL_DATA"></span><span id="partial_data"></span>**PARTIAL\_DATA**</span></span>  
<span data-ttu-id="70f9a-117">Uma resposta que indica que dados parciais foram gravados no log de gráficos.</span><span class="sxs-lookup"><span data-stu-id="70f9a-117">A response which indicates that partial data has been written to the graphics log.</span></span>

<span data-ttu-id="70f9a-118"><span id="READY"></span><span id="ready"></span>**ESTEJA**</span><span class="sxs-lookup"><span data-stu-id="70f9a-118"><span id="READY"></span><span id="ready"></span>**READY**</span></span>  
<span data-ttu-id="70f9a-119">Uma resposta que indica que o mecanismo de captura está pronto para iniciar a captura de informações de gráficos.</span><span class="sxs-lookup"><span data-stu-id="70f9a-119">A response which indicates that the capture engine is ready to start capturing graphics information.</span></span>

<span data-ttu-id="70f9a-120"><span id="DONE"></span><span id="done"></span>**TRABALHADO**</span><span class="sxs-lookup"><span data-stu-id="70f9a-120"><span id="DONE"></span><span id="done"></span>**DONE**</span></span>  
<span data-ttu-id="70f9a-121">Interna</span><span class="sxs-lookup"><span data-stu-id="70f9a-121">Internal</span></span>

<span data-ttu-id="70f9a-122"><span id="CAPTURESTARTED"></span><span id="capturestarted"></span>**CAPTURESTARTED**</span><span class="sxs-lookup"><span data-stu-id="70f9a-122"><span id="CAPTURESTARTED"></span><span id="capturestarted"></span>**CAPTURESTARTED**</span></span>  
<span data-ttu-id="70f9a-123">Uma resposta que indica que uma captura de quadro foi iniciada.</span><span class="sxs-lookup"><span data-stu-id="70f9a-123">A response which indicates that a frame capture has started.</span></span>

<span data-ttu-id="70f9a-124"><span id="STATUS"></span><span id="status"></span>**Estado**</span><span class="sxs-lookup"><span data-stu-id="70f9a-124"><span id="STATUS"></span><span id="status"></span>**STATUS**</span></span>  
<span data-ttu-id="70f9a-125">Uma resposta que indica informações de status sobre o aplicativo que está sendo capturado; por exemplo, taxa de quadros.</span><span class="sxs-lookup"><span data-stu-id="70f9a-125">A response which indicates status information about the app being captured; for example, framerate.</span></span>

## <a name="requirements"></a><span data-ttu-id="70f9a-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="70f9a-126">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="70f9a-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="70f9a-127">Header</span></span></p></td><td><span data-ttu-id="70f9a-128">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="70f9a-128">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



