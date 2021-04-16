---
description: Define o número de threads de trabalho que são usados por um decodificador de vídeo.
ms.assetid: A1570BB5-62BC-46C0-B9C9-61F99AA13BBE
title: Propriedade CODECAPI_AVDecNumWorkerThreads (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5d7c57d1b4176ad65313a5583a70f9ba4f7427a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105772643"
---
# <a name="codecapi_avdecnumworkerthreads-property"></a><span data-ttu-id="dc944-103">\_Propriedade CODECAPI AVDecNumWorkerThreads</span><span class="sxs-lookup"><span data-stu-id="dc944-103">CODECAPI\_AVDecNumWorkerThreads property</span></span>

<span data-ttu-id="dc944-104">Define o número de threads de trabalho que são usados por um decodificador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="dc944-104">Sets the number of worker threads that are used by a video decoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="dc944-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="dc944-105">Data type</span></span>

<span data-ttu-id="dc944-106">**Long** (**VT \_ i4**)</span><span class="sxs-lookup"><span data-stu-id="dc944-106">**LONG** (**VT\_I4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="dc944-107">GUID da propriedade</span><span class="sxs-lookup"><span data-stu-id="dc944-107">Property GUID</span></span>

<span data-ttu-id="dc944-108">CODECAPI \_ AVDecNumWorkerThreads</span><span class="sxs-lookup"><span data-stu-id="dc944-108">CODECAPI\_AVDecNumWorkerThreads</span></span>

## <a name="remarks"></a><span data-ttu-id="dc944-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="dc944-109">Remarks</span></span>

<span data-ttu-id="dc944-110">Se o valor for 1, o decodificador selecionará o número de threads.</span><span class="sxs-lookup"><span data-stu-id="dc944-110">If the value is  1, the decoder selects the number of threads.</span></span>

<span data-ttu-id="dc944-111">Para a interface [**ICodecAPI**](/windows/desktop/api/strmif/nn-strmif-icodecapi) , defina essa propriedade como um valor **longo** (**VT \_ i4**).</span><span class="sxs-lookup"><span data-stu-id="dc944-111">For the [**ICodecAPI**](/windows/desktop/api/strmif/nn-strmif-icodecapi) interface, set this property as a **LONG** value (**VT\_I4**).</span></span> <span data-ttu-id="dc944-112">Para a interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) , defina essa propriedade como um **UINT32**, embora o valor seja assinado.</span><span class="sxs-lookup"><span data-stu-id="dc944-112">For the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface, set this property as a **UINT32**, although the value is signed.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc944-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dc944-113">Requirements</span></span>



| <span data-ttu-id="dc944-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc944-114">Requirement</span></span> | <span data-ttu-id="dc944-115">Valor</span><span class="sxs-lookup"><span data-stu-id="dc944-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dc944-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dc944-116">Minimum supported client</span></span><br/> | <span data-ttu-id="dc944-117">Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="dc944-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="dc944-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dc944-118">Minimum supported server</span></span><br/> | <span data-ttu-id="dc944-119">Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="dc944-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="dc944-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dc944-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc944-121"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc944-121"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc944-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="dc944-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc944-123">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="dc944-123">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="dc944-124">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="dc944-124">**ICodecAPI**</span></span>](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

