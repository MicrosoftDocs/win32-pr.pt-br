---
description: Representa uma solicitação de um exemplo de um MediaStreamSource.
ms.assetid: 43617cda-84b1-405f-8a20-be793413c186
title: Interface IMFMediaStreamSourceSampleRequest
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaStreamSourceSampleRequest
api_type:
- COM
api_location:
- mfidl.h
ms.openlocfilehash: fa159727c6e13a894148391b9508afad4b8dacfc
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104297951"
---
# <a name="imfmediastreamsourcesamplerequest-interface"></a><span data-ttu-id="5a2c3-103">Interface IMFMediaStreamSourceSampleRequest</span><span class="sxs-lookup"><span data-stu-id="5a2c3-103">IMFMediaStreamSourceSampleRequest interface</span></span>

<span data-ttu-id="5a2c3-104">Representa uma solicitação de um exemplo de um MediaStreamSource.</span><span class="sxs-lookup"><span data-stu-id="5a2c3-104">Represents a request for a sample from a MediaStreamSource.</span></span>

## <a name="members"></a><span data-ttu-id="5a2c3-105">Membros</span><span class="sxs-lookup"><span data-stu-id="5a2c3-105">Members</span></span>

<span data-ttu-id="5a2c3-106">A interface **IMFMediaStreamSourceSampleRequest** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="5a2c3-106">The **IMFMediaStreamSourceSampleRequest** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="5a2c3-107">**IMFMediaStreamSourceSampleRequest** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="5a2c3-107">**IMFMediaStreamSourceSampleRequest** also has these types of members:</span></span>

-   [<span data-ttu-id="5a2c3-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="5a2c3-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="5a2c3-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="5a2c3-109">Methods</span></span>

<span data-ttu-id="5a2c3-110">A interface **IMFMediaStreamSourceSampleRequest** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="5a2c3-110">The **IMFMediaStreamSourceSampleRequest** interface has these methods.</span></span>



| <span data-ttu-id="5a2c3-111">Método</span><span class="sxs-lookup"><span data-stu-id="5a2c3-111">Method</span></span>                                                           | <span data-ttu-id="5a2c3-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="5a2c3-112">Description</span></span>                                             |
|:-----------------------------------------------------------------|:--------------------------------------------------------|
| [<span data-ttu-id="5a2c3-113">**Setsample**</span><span class="sxs-lookup"><span data-stu-id="5a2c3-113">**SetSample**</span></span>](imfmediastreamsourcesamplerequest-setsample.md) | <span data-ttu-id="5a2c3-114">Define o exemplo para a origem do fluxo de mídia.</span><span class="sxs-lookup"><span data-stu-id="5a2c3-114">Sets the sample for the media stream source.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5a2c3-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="5a2c3-115">Remarks</span></span>

<span data-ttu-id="5a2c3-116">**MFMediaStreamSourceSampleRequest** é implementado pela classe de tempo de execução [**Windows. Media. Core. MediaStreamSourceSampleRequest**](/uwp/api/Windows.Media.Core.MediaStreamSourceSampleRequest?view=winrt-19041) .</span><span class="sxs-lookup"><span data-stu-id="5a2c3-116">**MFMediaStreamSourceSampleRequest** is implemented by the [**Windows.Media.Core.MediaStreamSourceSampleRequest**](/uwp/api/Windows.Media.Core.MediaStreamSourceSampleRequest?view=winrt-19041) runtime class.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a2c3-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5a2c3-117">Requirements</span></span>



| <span data-ttu-id="5a2c3-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a2c3-118">Requirement</span></span> | <span data-ttu-id="5a2c3-119">Valor</span><span class="sxs-lookup"><span data-stu-id="5a2c3-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5a2c3-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5a2c3-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5a2c3-121">Aplicativos Windows 8.1 aplicativos de \[ área de trabalho \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="5a2c3-121">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="5a2c3-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5a2c3-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5a2c3-123">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="5a2c3-123">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                       |
| <span data-ttu-id="5a2c3-124">INSERI</span><span class="sxs-lookup"><span data-stu-id="5a2c3-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5a2c3-125"><dt>Mfidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5a2c3-125"><dt>Mfidl.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a2c3-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="5a2c3-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a2c3-127">Interfaces Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5a2c3-127">Media Foundation Interfaces</span></span>](media-foundation-interfaces.md)
</dt> </dl>

 

 
