---
description: A classe CImageSample implementa um exemplo de mídia que gerencia um bitmap independente de dispositivo (DIB) GDI.
ms.assetid: 620ea791-458e-441e-8f0c-2184c44c742e
title: Classe CImageSample (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2235d50c952ce1b76e4a70eda0341f0fe3c4167c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789975"
---
# <a name="cimagesample-class"></a><span data-ttu-id="2daf0-103">Classe CImageSample</span><span class="sxs-lookup"><span data-stu-id="2daf0-103">CImageSample class</span></span>

![hierarquia de classe cimagesample](images/wutil03.png)

<span data-ttu-id="2daf0-105">A `CImageSample` classe implementa um exemplo de mídia que gerencia um bitmap independente de dispositivo (DIB) do GDI.</span><span class="sxs-lookup"><span data-stu-id="2daf0-105">The `CImageSample` class implements a media sample that manages a GDI device-independent bitmap (DIB).</span></span> <span data-ttu-id="2daf0-106">Essa classe deriva da classe [**CMediaSample**](cmediasample.md) .</span><span class="sxs-lookup"><span data-stu-id="2daf0-106">This class derives from the [**CMediaSample**](cmediasample.md) class.</span></span> <span data-ttu-id="2daf0-107">Ele se destina a ser usado com a classe [**CImageAllocator**](cimageallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="2daf0-107">It is intended to be used with the [**CImageAllocator**](cimageallocator.md) class.</span></span> <span data-ttu-id="2daf0-108">A classe **CImageAllocator** fornece um alocador que cria `CImageSample` objetos.</span><span class="sxs-lookup"><span data-stu-id="2daf0-108">The **CImageAllocator** class provides an allocator that creates `CImageSample` objects.</span></span>



| <span data-ttu-id="2daf0-109">Variáveis de membro protegido</span><span class="sxs-lookup"><span data-stu-id="2daf0-109">Protected Member Variables</span></span>                        | <span data-ttu-id="2daf0-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="2daf0-110">Description</span></span>                                                       |
|---------------------------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="2daf0-111">**\_DibData m**</span><span class="sxs-lookup"><span data-stu-id="2daf0-111">**m\_DibData**</span></span>](cimagesample-m-dibdata.md)      | <span data-ttu-id="2daf0-112">Contém informações sobre o DIB que esse objeto está gerenciando.</span><span class="sxs-lookup"><span data-stu-id="2daf0-112">Contains information about the DIB that this object is managing.</span></span>  |
| [<span data-ttu-id="2daf0-113">**\_bInit m**</span><span class="sxs-lookup"><span data-stu-id="2daf0-113">**m\_bInit**</span></span>](cimagesample-m-binit.md)          | <span data-ttu-id="2daf0-114">Indica se o objeto foi inicializado.</span><span class="sxs-lookup"><span data-stu-id="2daf0-114">Indicates whether the object has been initialized.</span></span>                |
| <span data-ttu-id="2daf0-115">Métodos públicos</span><span class="sxs-lookup"><span data-stu-id="2daf0-115">Public Methods</span></span>                                    | <span data-ttu-id="2daf0-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="2daf0-116">Description</span></span>                                                       |
| [<span data-ttu-id="2daf0-117">**CImageSample**</span><span class="sxs-lookup"><span data-stu-id="2daf0-117">**CImageSample**</span></span>](cimagesample-cimagesample.md) | <span data-ttu-id="2daf0-118">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="2daf0-118">Constructor method.</span></span>                                               |
| [<span data-ttu-id="2daf0-119">**GetDIBData**</span><span class="sxs-lookup"><span data-stu-id="2daf0-119">**GetDIBData**</span></span>](cimagesample-getdibdata.md)     | <span data-ttu-id="2daf0-120">Recupera informações sobre o DIB que esse objeto está gerenciando.</span><span class="sxs-lookup"><span data-stu-id="2daf0-120">Retrieves information about the DIB that this object is managing.</span></span> |
| [<span data-ttu-id="2daf0-121">**SetDIBData**</span><span class="sxs-lookup"><span data-stu-id="2daf0-121">**SetDIBData**</span></span>](cimagesample-setdibdata.md)     | <span data-ttu-id="2daf0-122">Define informações sobre o DIB que esse objeto está gerenciando.</span><span class="sxs-lookup"><span data-stu-id="2daf0-122">Sets information about the DIB that this object is managing.</span></span>      |



 

## <a name="requirements"></a><span data-ttu-id="2daf0-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2daf0-123">Requirements</span></span>



| <span data-ttu-id="2daf0-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="2daf0-124">Requirement</span></span> | <span data-ttu-id="2daf0-125">Valor</span><span class="sxs-lookup"><span data-stu-id="2daf0-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2daf0-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2daf0-126">Header</span></span><br/>  | <dl> <span data-ttu-id="2daf0-127"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2daf0-127"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2daf0-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2daf0-128">Library</span></span><br/> | <dl> <span data-ttu-id="2daf0-129"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="2daf0-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




