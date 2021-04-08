---
title: Propriedades de controle
description: Propriedades de controle
ms.assetid: 29c2cca3-9460-45d1-9591-026e8c18f26f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4749a7a7e408f6cd58951a72207ed801e4104d65
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103823010"
---
# <a name="control-properties"></a><span data-ttu-id="39068-103">Propriedades de controle</span><span class="sxs-lookup"><span data-stu-id="39068-103">Control Properties</span></span>

<span data-ttu-id="39068-104">Além das propriedades definidas e implementadas pelo próprio controle, a tecnologia controles ActiveX também envolve:</span><span class="sxs-lookup"><span data-stu-id="39068-104">In addition to properties defined and implemented by the control itself, ActiveX controls technology also involves:</span></span>

<dl> <dt>

<span data-ttu-id="39068-105"><span id="Ambient_properties"></span><span id="ambient_properties"></span><span id="AMBIENT_PROPERTIES"></span>Propriedades de ambiente</span><span class="sxs-lookup"><span data-stu-id="39068-105"><span id="Ambient_properties"></span><span id="ambient_properties"></span><span id="AMBIENT_PROPERTIES"></span>Ambient properties</span></span>
</dt> <dd>

<span data-ttu-id="39068-106">Elas são expostas pelo contêiner por meio de um site do cliente de controle para fornecer valores ambientais que se aplicam a todos os controles inseridos no contêiner.</span><span class="sxs-lookup"><span data-stu-id="39068-106">These are exposed by the container through a control client site to provide environmental values that apply to all controls embedded in the container.</span></span> <span data-ttu-id="39068-107">Por exemplo, um contêiner pode fornecer uma cor de plano de fundo padrão ou uma fonte padrão que o controle possa usar.</span><span class="sxs-lookup"><span data-stu-id="39068-107">For example, a container can provide a default background color or a default font that the control can use.</span></span> <span data-ttu-id="39068-108">As propriedades de ambiente são expostas por meio de **IDispatch** implementadas no objeto do site de um contêiner.</span><span class="sxs-lookup"><span data-stu-id="39068-108">Ambient properties are exposed through **IDispatch** implemented on a container's site object.</span></span> <span data-ttu-id="39068-109">O contêiner chama o método [**IOleControl:: OnAmbientPropertyChange**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onambientpropertychange) do controle quando qualquer uma de suas propriedades de ambiente altera o valor.</span><span class="sxs-lookup"><span data-stu-id="39068-109">The container calls the control's [**IOleControl::OnAmbientPropertyChange**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onambientpropertychange) method when any of its ambient properties change value.</span></span> <span data-ttu-id="39068-110">Em resposta, um controle pode precisar atualizar seu próprio estado interno ou Visual em resposta.</span><span class="sxs-lookup"><span data-stu-id="39068-110">In response, a control may need to update its own internal or visual state in response.</span></span> <span data-ttu-id="39068-111">O contêiner indica qual propriedade de ambiente mudou com o parâmetro DISPID ou pode passar DISPID \_ Unknown para indicar que várias propriedades de ambiente foram alteradas.</span><span class="sxs-lookup"><span data-stu-id="39068-111">The container indicates which ambient property changed with the DISPID parameter or may pass DISPID\_UNKNOWN to indicate that multiple ambient properties changed.</span></span>

</dd> <dt>

<span data-ttu-id="39068-112"><span id="Extended_properties"></span><span id="extended_properties"></span><span id="EXTENDED_PROPERTIES"></span>Propriedades estendidas</span><span class="sxs-lookup"><span data-stu-id="39068-112"><span id="Extended_properties"></span><span id="extended_properties"></span><span id="EXTENDED_PROPERTIES"></span>Extended properties</span></span>
</dt> <dd>

<span data-ttu-id="39068-113">Na verdade, eles são implementados por um contêiner para encapsular os controles que ele contém para fornecer propriedades gerenciadas por contêiner que aparecem como se fossem Propriedades de controle nativo.</span><span class="sxs-lookup"><span data-stu-id="39068-113">These are actually implemented by a container to wrap the controls it contains to provide container-managed properties that appear as if they were native control properties.</span></span> <span data-ttu-id="39068-114">O contêiner pode agregar o controle, adicionando as propriedades estendidas para complementar ou substituir as propriedades do controle.</span><span class="sxs-lookup"><span data-stu-id="39068-114">The container can aggregate the control, adding the extended properties to supplement or override the control's properties.</span></span> <span data-ttu-id="39068-115">O objeto agregado é chamado de controle estendido.</span><span class="sxs-lookup"><span data-stu-id="39068-115">The aggregated object is called an extended control.</span></span> <span data-ttu-id="39068-116">Para o contêiner, o controle estendido aparece como o próprio controle e as propriedades estendidas parecem ser expostas pelo controle.</span><span class="sxs-lookup"><span data-stu-id="39068-116">To the container, the extended control appears as the control itself and extended properties appear to be exposed by the control.</span></span> <span data-ttu-id="39068-117">O contêiner dá suporte a um controle estendido por meio de seu método de site do cliente [**IOleControlSite:: GetExtendedControl**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-getextendedcontrol).</span><span class="sxs-lookup"><span data-stu-id="39068-117">The container supports an extended control through its client site method [**IOleControlSite::GetExtendedControl**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-getextendedcontrol).</span></span> <span data-ttu-id="39068-118">O método **GetExtendedControl** permite que os controles naveguem pelo site até o objeto de controle estendido fornecido para eles pelo contêiner, se o contêiner oferecer suporte a esse recurso.</span><span class="sxs-lookup"><span data-stu-id="39068-118">The **GetExtendedControl** method allows controls to navigate through the site to the extended control object provided for them by the container, if the container supports this feature.</span></span> <span data-ttu-id="39068-119">Um contêiner também pode optar por mostrar páginas de propriedades para seus controles estendidos, além das páginas que um controle normalmente especificaria por meio de [**ISpecifyPropertyPages**](/windows/desktop/api/OCIdl/nn-ocidl-ispecifypropertypages).</span><span class="sxs-lookup"><span data-stu-id="39068-119">A container can also choose to show property pages for its extended controls in addition to those pages that a control would normally specify through [**ISpecifyPropertyPages**](/windows/desktop/api/OCIdl/nn-ocidl-ispecifypropertypages).</span></span> <span data-ttu-id="39068-120">Por isso, um controle precisa pedir a um contêiner para mostrar um quadro de propriedade antes que o controle tente fazer isso por conta própria.</span><span class="sxs-lookup"><span data-stu-id="39068-120">Because of this, a control has to ask a container to show a property frame before the control attempts to do so itself.</span></span> <span data-ttu-id="39068-121">O controle chama [**IOleControlSite:: ShowPropertyFrame**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-showpropertyframe) para fazer isso.</span><span class="sxs-lookup"><span data-stu-id="39068-121">The control calls [**IOleControlSite::ShowPropertyFrame**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-showpropertyframe) to do this.</span></span> <span data-ttu-id="39068-122">Se o contêiner implementar essa função, ele mostrará o próprio quadro da propriedade; Se o método retornar um erro, o controle poderá mostrar o quadro de propriedade.</span><span class="sxs-lookup"><span data-stu-id="39068-122">If the container implements this function then it shows the property frame itself; if the method returns an error then the control can show the property frame.</span></span>

</dd> </dl>

<span data-ttu-id="39068-123">Para mais informações, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="39068-123">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="39068-124">Propriedades padrão</span><span class="sxs-lookup"><span data-stu-id="39068-124">Standard Properties</span></span>](standard-properties.md)
-   [<span data-ttu-id="39068-125">Objeto de fonte padrão</span><span class="sxs-lookup"><span data-stu-id="39068-125">Standard Font Object</span></span>](standard-font-object.md)
-   [<span data-ttu-id="39068-126">Objeto de imagem padrão</span><span class="sxs-lookup"><span data-stu-id="39068-126">Standard Picture Object</span></span>](standard-picture-object.md)

## <a name="related-topics"></a><span data-ttu-id="39068-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="39068-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39068-128">Métodos de controle</span><span class="sxs-lookup"><span data-stu-id="39068-128">Control Methods</span></span>](control-methods.md)
</dt> </dl>

 

 




