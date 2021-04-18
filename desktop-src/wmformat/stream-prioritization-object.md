---
title: Objeto de priorização de fluxo
description: Objeto de priorização de fluxo
ms.assetid: cb0345ce-6847-435b-8cbb-f8b93856af9f
keywords:
- SDK do Windows Media Format, objetos de priorização de fluxo
- ASF (Advanced Systems Format), objetos de priorização de fluxo
- ASF (formato de sistemas avançados), objetos de priorização de fluxo
- objetos, objetos de priorização de fluxo
- objetos de priorização de fluxo
- fluxos, objetos de priorização de fluxo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cce4189f64e85cca4e0d649dbc00409cf9d7c06
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "105793982"
---
# <a name="stream-prioritization-object"></a><span data-ttu-id="30d63-109">Objeto de priorização de fluxo</span><span class="sxs-lookup"><span data-stu-id="30d63-109">Stream Prioritization Object</span></span>

<span data-ttu-id="30d63-110">Um objeto de priorização de fluxo é usado para especificar uma ordem de importância para os fluxos em um perfil.</span><span class="sxs-lookup"><span data-stu-id="30d63-110">A stream prioritization object is used to specify an order of importance for the streams in a profile.</span></span> <span data-ttu-id="30d63-111">Quando a reprodução completa não é possível devido a limitações de taxa de bits, os fluxos de prioridade mais baixos serão os primeiros a serem descartados.</span><span class="sxs-lookup"><span data-stu-id="30d63-111">When full playback is not possible due to bit-rate limitations, the lowest priority streams will be the first to be dropped.</span></span>

<span data-ttu-id="30d63-112">Os objetos de priorização de fluxo podem ser criados para dados de priorização de fluxo existentes em um perfil ou podem ser criados em branco, prontos para receber novos dados.</span><span class="sxs-lookup"><span data-stu-id="30d63-112">Stream prioritization objects can be created for existing stream prioritization data in a profile or can be created empty, ready to receive new data.</span></span> <span data-ttu-id="30d63-113">Os objetos de priorização de fluxo não podem existir independentemente de um objeto de perfil.</span><span class="sxs-lookup"><span data-stu-id="30d63-113">Stream prioritization objects cannot exist independently of a profile object.</span></span> <span data-ttu-id="30d63-114">Para salvar o conteúdo de um objeto de priorização de fluxo, você deve chamar [**IWMProfile3:: SetStreamPrioritization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-setstreamprioritization).</span><span class="sxs-lookup"><span data-stu-id="30d63-114">To save the contents of a stream prioritization object, you must call [**IWMProfile3::SetStreamPrioritization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-setstreamprioritization).</span></span> <span data-ttu-id="30d63-115">Para criar um objeto de priorização de fluxo, use um dos métodos a seguir.</span><span class="sxs-lookup"><span data-stu-id="30d63-115">To create a stream prioritization object, use one of the following methods.</span></span>



| <span data-ttu-id="30d63-116">Método</span><span class="sxs-lookup"><span data-stu-id="30d63-116">Method</span></span>                                                                                          | <span data-ttu-id="30d63-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="30d63-117">Description</span></span>                                                                  |
|-------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="30d63-118">**IWMProfile3::CreateNewStreamPrioritization**</span><span class="sxs-lookup"><span data-stu-id="30d63-118">**IWMProfile3::CreateNewStreamPrioritization**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewstreamprioritization) | <span data-ttu-id="30d63-119">Cria um objeto de priorização de fluxo sem nenhum dado.</span><span class="sxs-lookup"><span data-stu-id="30d63-119">Creates a stream prioritization object without any data.</span></span>                     |
| [<span data-ttu-id="30d63-120">**IWMProfile3::GetStreamPrioritization**</span><span class="sxs-lookup"><span data-stu-id="30d63-120">**IWMProfile3::GetStreamPrioritization**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-getstreamprioritization)             | <span data-ttu-id="30d63-121">Cria um objeto de priorização de fluxo populado com dados do perfil.</span><span class="sxs-lookup"><span data-stu-id="30d63-121">Creates a stream prioritization object populated with data from the profile.</span></span> |



 

<span data-ttu-id="30d63-122">Os dois métodos na tabela anterior definiram um ponteiro para uma interface **IWMStreamPrioritization** .</span><span class="sxs-lookup"><span data-stu-id="30d63-122">Both methods in the preceding table set a pointer to an **IWMStreamPrioritization** interface.</span></span> <span data-ttu-id="30d63-123">Essa é a única interface suportada pelo objeto de priorização de fluxo.</span><span class="sxs-lookup"><span data-stu-id="30d63-123">This is the only interface supported by the stream prioritization object.</span></span>



| <span data-ttu-id="30d63-124">Interface</span><span class="sxs-lookup"><span data-stu-id="30d63-124">Interface</span></span>                                                  | <span data-ttu-id="30d63-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="30d63-125">Description</span></span>                                                          |
|------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="30d63-126">**IWMStreamPrioritization**</span><span class="sxs-lookup"><span data-stu-id="30d63-126">**IWMStreamPrioritization**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamprioritization) | <span data-ttu-id="30d63-127">Gerencia a lista de fluxos dentro do objeto de priorização de fluxo.</span><span class="sxs-lookup"><span data-stu-id="30d63-127">Manages the list of streams within the stream prioritization object.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="30d63-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="30d63-128">Remarks</span></span>

<span data-ttu-id="30d63-129">Pode existir apenas uma priorização de fluxo para um determinado perfil.</span><span class="sxs-lookup"><span data-stu-id="30d63-129">Only one stream prioritization can exist for a given profile.</span></span> <span data-ttu-id="30d63-130">Se você criar uma nova priorização de fluxo para um perfil que já contém uma priorização de fluxo, a antiga será excluída.</span><span class="sxs-lookup"><span data-stu-id="30d63-130">If you create a new stream prioritization for a profile that already contains a stream prioritization, the old one will be deleted.</span></span>

## <a name="related-topics"></a><span data-ttu-id="30d63-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="30d63-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="30d63-132">**Objetos**</span><span class="sxs-lookup"><span data-stu-id="30d63-132">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="30d63-133">**Objeto de perfil**</span><span class="sxs-lookup"><span data-stu-id="30d63-133">**Profile Object**</span></span>](profile-object.md)
</dt> <dt>

[<span data-ttu-id="30d63-134">**Usando a priorização de fluxo**</span><span class="sxs-lookup"><span data-stu-id="30d63-134">**Using Stream Prioritization**</span></span>](using-stream-prioritization.md)
</dt> </dl>

 

 




