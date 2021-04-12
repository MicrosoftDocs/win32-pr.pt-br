---
title: Objeto de compartilhamento de largura de banda
description: Objeto de compartilhamento de largura de banda
ms.assetid: 9dc863da-1842-41e7-b66c-c97e0140046d
keywords:
- SDK do Windows Media Format, objetos de compartilhamento de largura de banda
- ASF (Advanced Systems Format), objetos de compartilhamento de largura de banda
- ASF (formato de sistemas avançados), objetos de compartilhamento de largura de banda
- objetos, objetos de compartilhamento de largura de banda
- compartilhamento de largura de banda, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d29048e3094f1a12775dfbec7422baf349c18be7
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104365589"
---
# <a name="bandwidth-sharing-object"></a><span data-ttu-id="cdaf9-108">Objeto de compartilhamento de largura de banda</span><span class="sxs-lookup"><span data-stu-id="cdaf9-108">Bandwidth Sharing Object</span></span>

<span data-ttu-id="cdaf9-109">Um objeto de compartilhamento de largura de banda é usado para indicar que dois ou mais fluxos, independentemente de suas taxas de bits individuais, nunca usarão mais do que uma quantidade especificada de largura de banda entre eles.</span><span class="sxs-lookup"><span data-stu-id="cdaf9-109">A bandwidth sharing object is used to indicate that two or more streams, regardless of their individual bit rates, will never use more than a specified amount of bandwidth between them.</span></span> <span data-ttu-id="cdaf9-110">Esse é um objeto puramente informativo; as taxas de bits definidas dentro dela não são impostas programaticamente por qualquer objeto desse SDK.</span><span class="sxs-lookup"><span data-stu-id="cdaf9-110">This is a purely informational object; the bit rates set within it are not enforced programmatically by any object of this SDK.</span></span>

<span data-ttu-id="cdaf9-111">As informações de compartilhamento de largura de banda são uma parte opcional de um perfil.</span><span class="sxs-lookup"><span data-stu-id="cdaf9-111">Bandwidth sharing information is an optional part of a profile.</span></span> <span data-ttu-id="cdaf9-112">Objetos de compartilhamento de largura de banda podem ser criados para informações de compartilhamento de largura de banda existentes em um perfil ou podem ser criados em branco, prontos para receber novos dados.</span><span class="sxs-lookup"><span data-stu-id="cdaf9-112">Bandwidth sharing objects can be created for existing bandwidth sharing information in a profile or can be created empty, ready to receive new data.</span></span> <span data-ttu-id="cdaf9-113">Os objetos de compartilhamento de largura de banda não podem existir independentemente de um objeto de perfil.</span><span class="sxs-lookup"><span data-stu-id="cdaf9-113">Bandwidth sharing objects cannot exist independently of a profile object.</span></span> <span data-ttu-id="cdaf9-114">Para salvar o conteúdo de um objeto de compartilhamento de largura de banda, você deve chamar [**IWMProfile3:: AddBandwidthSharing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-addbandwidthsharing).</span><span class="sxs-lookup"><span data-stu-id="cdaf9-114">To save the contents of a bandwidth sharing object, you must call [**IWMProfile3::AddBandwidthSharing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-addbandwidthsharing).</span></span>

<span data-ttu-id="cdaf9-115">Para criar um objeto de compartilhamento de largura de banda, chame um dos métodos a seguir.</span><span class="sxs-lookup"><span data-stu-id="cdaf9-115">To create a bandwidth sharing object, call one of the following methods.</span></span>



| <span data-ttu-id="cdaf9-116">Método</span><span class="sxs-lookup"><span data-stu-id="cdaf9-116">Method</span></span>                                                                                  | <span data-ttu-id="cdaf9-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="cdaf9-117">Description</span></span>                                                                                                                                                    |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cdaf9-118">**IWMProfile3::CreateNewBandwidthSharing**</span><span class="sxs-lookup"><span data-stu-id="cdaf9-118">**IWMProfile3::CreateNewBandwidthSharing**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewbandwidthsharing) | <span data-ttu-id="cdaf9-119">Cria um objeto de compartilhamento de largura de banda sem nenhum dado.</span><span class="sxs-lookup"><span data-stu-id="cdaf9-119">Creates a bandwidth sharing object without any data.</span></span>                                                                                                           |
| [<span data-ttu-id="cdaf9-120">**IWMProfile3::GetBandwidthSharing**</span><span class="sxs-lookup"><span data-stu-id="cdaf9-120">**IWMProfile3::GetBandwidthSharing**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-getbandwidthsharing)             | <span data-ttu-id="cdaf9-121">Cria um objeto de compartilhamento de largura de banda preenchido com dados de um perfil.</span><span class="sxs-lookup"><span data-stu-id="cdaf9-121">Creates a bandwidth sharing object populated with data from a profile.</span></span> <span data-ttu-id="cdaf9-122">Usa o índice de compartilhamento de largura de banda para identificar as informações de compartilhamento de largura de banda desejada.</span><span class="sxs-lookup"><span data-stu-id="cdaf9-122">Uses the bandwidth sharing index to identify the desired bandwidth sharing information.</span></span> |



 

<span data-ttu-id="cdaf9-123">Os dois métodos na tabela anterior definiram um ponteiro para uma interface **IWMBandwidthSharing** .</span><span class="sxs-lookup"><span data-stu-id="cdaf9-123">Both methods in the preceding table set a pointer to an **IWMBandwidthSharing** interface.</span></span> <span data-ttu-id="cdaf9-124">A interface **IWMStreamList** é herdada por **IWMBandwidthSharing**, portanto, não é necessário chamar **QueryInterface** com esse objeto.</span><span class="sxs-lookup"><span data-stu-id="cdaf9-124">The **IWMStreamList** interface is inherited by **IWMBandwidthSharing**, so there is no need to call **QueryInterface** with this object.</span></span>

<span data-ttu-id="cdaf9-125">As interfaces a seguir têm suporte em cada objeto de compartilhamento de largura de banda.</span><span class="sxs-lookup"><span data-stu-id="cdaf9-125">The following interfaces are supported by every bandwidth sharing object.</span></span>



| <span data-ttu-id="cdaf9-126">Interface</span><span class="sxs-lookup"><span data-stu-id="cdaf9-126">Interface</span></span>                                          | <span data-ttu-id="cdaf9-127">Descrição</span><span class="sxs-lookup"><span data-stu-id="cdaf9-127">Description</span></span>                                                             |
|----------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="cdaf9-128">**IWMBandwidthSharing**</span><span class="sxs-lookup"><span data-stu-id="cdaf9-128">**IWMBandwidthSharing**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbandwidthsharing) | <span data-ttu-id="cdaf9-129">Gerencia as propriedades de um grupo de fluxos que compartilharão a largura de banda.</span><span class="sxs-lookup"><span data-stu-id="cdaf9-129">Manages the properties of a group of streams that will share bandwidth.</span></span> |
| [<span data-ttu-id="cdaf9-130">**IWMStreamList**</span><span class="sxs-lookup"><span data-stu-id="cdaf9-130">**IWMStreamList**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist)             | <span data-ttu-id="cdaf9-131">Gerencia a lista de fluxos que compartilharão a largura de banda.</span><span class="sxs-lookup"><span data-stu-id="cdaf9-131">Manages the list of streams that will share bandwidth.</span></span>                  |



 

## <a name="related-topics"></a><span data-ttu-id="cdaf9-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="cdaf9-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cdaf9-133">**Compartilhamento de largura de banda**</span><span class="sxs-lookup"><span data-stu-id="cdaf9-133">**Bandwidth Sharing**</span></span>](bandwidth-sharing.md)
</dt> <dt>

[<span data-ttu-id="cdaf9-134">**Objeto do gerenciador de perfis**</span><span class="sxs-lookup"><span data-stu-id="cdaf9-134">**Profile Manager Object**</span></span>](profile-manager-object.md)
</dt> <dt>

[<span data-ttu-id="cdaf9-135">**Objeto de perfil**</span><span class="sxs-lookup"><span data-stu-id="cdaf9-135">**Profile Object**</span></span>](profile-object.md)
</dt> </dl>

 

 




