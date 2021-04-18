---
description: A classe CSeekingPassThru é um objeto auxiliar que cria objetos CPosPassThru e CRendererPosPassThru.
ms.assetid: a748ea5c-d93f-4f80-9d2f-bef5a5c1c2fb
title: Classe CSeekingPassThru (Seekpt. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSeekingPassThru
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 273f9b6686c4455452924dc43628801fae5d518a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105767685"
---
# <a name="cseekingpassthru-class"></a><span data-ttu-id="5e064-103">Classe CSeekingPassThru</span><span class="sxs-lookup"><span data-stu-id="5e064-103">CSeekingPassThru class</span></span>

<span data-ttu-id="5e064-104">A `CSeekingPassThru` classe é um objeto auxiliar que cria objetos [**CPosPassThru**](cpospassthru.md) e [**CRendererPosPassThru**](crendererpospassthru.md) .</span><span class="sxs-lookup"><span data-stu-id="5e064-104">The `CSeekingPassThru` class is a helper object that creates [**CPosPassThru**](cpospassthru.md) and [**CRendererPosPassThru**](crendererpospassthru.md) objects.</span></span>

<span data-ttu-id="5e064-105">As classes **CPosPassThru** e **CRendererPosPassThru** são objetos auxiliares que passam comandos de busca ascendentes, portanto, a `CSeekingPassThru` classe é um objeto auxiliar para criar objetos auxiliares.</span><span class="sxs-lookup"><span data-stu-id="5e064-105">The **CPosPassThru** and **CRendererPosPassThru** classes are helper objects that pass seeking commands upstream, so the `CSeekingPassThru` class is a helper object for creating helper objects.</span></span>

<span data-ttu-id="5e064-106">Não é necessário usar essa classe diretamente.</span><span class="sxs-lookup"><span data-stu-id="5e064-106">It is not necessary to use this class directly.</span></span> <span data-ttu-id="5e064-107">Em vez disso, use a função [**CreatePosPassThru**](createpospassthru.md) , que lida com todos os detalhes do uso dessa classe.</span><span class="sxs-lookup"><span data-stu-id="5e064-107">Instead, use the [**CreatePosPassThru**](createpospassthru.md) function, which handles all of the details of using this class.</span></span> <span data-ttu-id="5e064-108">Ele tem a maior vantagem de carregar o objeto de Quartz.dll, o que reduz um pouco o tamanho do código de seu filtro.</span><span class="sxs-lookup"><span data-stu-id="5e064-108">It has the further advantage of loading the object from Quartz.dll, which reduces the code size of your filter somewhat.</span></span> <span data-ttu-id="5e064-109">Para obter mais informações, consulte [**CPosPassThru**](cpospassthru.md).</span><span class="sxs-lookup"><span data-stu-id="5e064-109">For more information, see [**CPosPassThru**](cpospassthru.md).</span></span>

<span data-ttu-id="5e064-110">A `CSeekingPassThru` classe expõe a interface [**ISeekingPassThru**](/windows/desktop/api/Strmif/nn-strmif-iseekingpassthru) .</span><span class="sxs-lookup"><span data-stu-id="5e064-110">The `CSeekingPassThru` class exposes the [**ISeekingPassThru**](/windows/desktop/api/Strmif/nn-strmif-iseekingpassthru) interface.</span></span> <span data-ttu-id="5e064-111">O método [**ISeekingPassThru:: init**](/windows/desktop/api/Strmif/nf-strmif-iseekingpassthru-init) Inicializa o objeto.</span><span class="sxs-lookup"><span data-stu-id="5e064-111">The [**ISeekingPassThru::Init**](/windows/desktop/api/Strmif/nf-strmif-iseekingpassthru-init) method initializes the object.</span></span> <span data-ttu-id="5e064-112">Depois que o objeto é inicializado, o filtro pode consultá-lo para as interfaces [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) e [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) .</span><span class="sxs-lookup"><span data-stu-id="5e064-112">After the object is initialized, the filter can query it for the [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) and [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) interfaces.</span></span>



| <span data-ttu-id="5e064-113">Métodos públicos</span><span class="sxs-lookup"><span data-stu-id="5e064-113">Public Methods</span></span>                                                  | <span data-ttu-id="5e064-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="5e064-114">Description</span></span>                        |
|-----------------------------------------------------------------|------------------------------------|
| [<span data-ttu-id="5e064-115">**CSeekingPassThru**</span><span class="sxs-lookup"><span data-stu-id="5e064-115">**CSeekingPassThru**</span></span>](cseekingpassthru-cseekingpassthru.md)   | <span data-ttu-id="5e064-116">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="5e064-116">Constructor method.</span></span>                |
| [<span data-ttu-id="5e064-117">**~ CSeekingPassThru**</span><span class="sxs-lookup"><span data-stu-id="5e064-117">**~CSeekingPassThru**</span></span>](cseekingpassthru--cseekingpassthru.md) | <span data-ttu-id="5e064-118">Método destruidor.</span><span class="sxs-lookup"><span data-stu-id="5e064-118">Destructor method.</span></span>                 |
| [<span data-ttu-id="5e064-119">**CreateInstance**</span><span class="sxs-lookup"><span data-stu-id="5e064-119">**CreateInstance**</span></span>](cseekingpassthru-createinstance.md)       | <span data-ttu-id="5e064-120">Cria uma instância do objeto.</span><span class="sxs-lookup"><span data-stu-id="5e064-120">Creates an instance of the object.</span></span> |
| <span data-ttu-id="5e064-121">Métodos ISeekingPassThru</span><span class="sxs-lookup"><span data-stu-id="5e064-121">ISeekingPassThru Methods</span></span>                                        | <span data-ttu-id="5e064-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="5e064-122">Description</span></span>                        |
| [<span data-ttu-id="5e064-123">**Init**</span><span class="sxs-lookup"><span data-stu-id="5e064-123">**Init**</span></span>](cseekingpassthru-init.md)                           | <span data-ttu-id="5e064-124">Inicializa o objeto.</span><span class="sxs-lookup"><span data-stu-id="5e064-124">Initializes the object.</span></span>            |



 

## <a name="requirements"></a><span data-ttu-id="5e064-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e064-125">Requirements</span></span>



| <span data-ttu-id="5e064-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e064-126">Requirement</span></span> | <span data-ttu-id="5e064-127">Valor</span><span class="sxs-lookup"><span data-stu-id="5e064-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e064-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5e064-128">Header</span></span><br/>  | <dl> <span data-ttu-id="5e064-129"><dt>Seekpt. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5e064-129"><dt>Seekpt.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="5e064-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5e064-130">Library</span></span><br/> | <dl> <span data-ttu-id="5e064-131"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="5e064-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




